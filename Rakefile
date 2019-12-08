desc "Commit _site/"
task :commit_site do
  puts "\n## Removing Gemfile.lock"
  status = system("rm Gemfile.lock")
  
  puts "\n## Staging modified files"
  status = system("git add -A")
  puts status ? "Success" : "Failed"
  
  puts "\n## Committing a site build at #{Time.now.utc}"
  message = "Build site at #{Time.now.utc}"
  status = system("git commit -m \"#{message}\"")
  puts status ? "Success" : "Failed"
  
  puts "\n## Pushing commits to remote"
  status = system("git push origin source")
  puts status ? "Success" : "Failed"
end

desc "Deploy _site/ to master branch"
task :deploy_site do
  puts "\n## Deleting master branch"
  status = system("git branch -D master")
  puts status ? "Success" : "Failed"
  
  puts "\n## Creating new master branch and switching to it"
  status = system("git checkout -b master")
  puts status ? "Success" : "Failed"
  
  puts "\n## Forcing the _site subdirectory to be project root"
  status = system("git filter-branch --subdirectory-filter _site/ -f")
  puts status ? "Success" : "Failed"
  
  puts "\n## Moving the content of _site to the root folder"
  status = system("mv _site/* .")
  puts status ? "Success" : "Failed"
  
  puts "\n## Deleting the empty _site folder"
  status = system("rm _site")
  puts status ? "Success" : "Failed"
  
  puts "\n## Staging all files"
  status = system("git add .")
  puts status ? "Success" : "Failed"

  puts "\n## Committing a site build at #{Time.now.utc}"
  message = "Build site at #{Time.now.utc}"
  status = system("git commit -m \"#{message}\"")
  puts status ? "Success" : "Failed"

  puts "\n## Switching back to source branch"
  status = system("git checkout source")
  puts status ? "Success" : "Failed"
  
  puts "\n## Pushing all branches to origin"
  status = system("git push --all origin --force")
  puts status ? "Success" : "Failed"
end

desc "Commit and deploy _site/"
task :commit_deploy_site => [:commit_site, :deploy_site] do
end