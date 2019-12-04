---
title: "Nadiren Sorulan Sorular"
permalink: /nss/
author_profile: true
redirect_from:
  - /nss
excerpt:
share: false


nss:
  - question: Lise öğrencisiyim.
    answer: Robotik 
    
---



<style>


a.nss_question{
  color: inherit;
  text-align: justify;
}

a:link.nss_question {
  text-decoration: none;  
}

a:visited.nss_question{
  text-decoration: none;  
}

a:hover.nss_question {
  text-decoration: none;
}

a:active.nss_question {
  text-decoration: none;
}  


.nss_answer {
  display: none;
  text-align: justify;
  background-color: #F0F0FF;
}

</style>



<div>
    <p id="nss_question_check" style="text-align: justify;"> Aşağıdaki listede eposta ve sosyal medya aracılığıyla bana nadiren yöneltilen soruları ve cevaplarımı okuyabilirsiniz. Cevaplarım tamamen kişisel görüşlerim olup tecrübelerime dayanarak edindiğim fikirlerden oluşmaktadır. Bana katılmak ve tavsiyelerimi uygulamak zorunda değilsiniz!</p>

  <ol>
      <li> 
        <a data-toggle="collapse" class = "nss_question"> 
        Mezun olduğunuz ikinci bölüm (bilgisayar mühendisliği) için tekrar üniversite sınavına mı hazırlandınız?
        </a> 
      </li>
      <div class = "nss_answer">
      Hayır. 2000 yılından itibaren İTÜ'de Çift Anadal Programı uygulamaya koyuldu. Bu program kapsamında ağırlıklı genel not ortalaması en az 3.0 (4.0 üzerinden) olan lisans öğrencileri istedikleri takdirde üniversite içindeki ikinci bir bölümü okumak için başvurabiliyordu. Lisans öğrencileri başvuran adaylar arasından seçildikleri takdirde, ikinci sınıftan itibaren diğer bölümün derslerini de alarak her iki programdan mezun olabiliyorlardı. Ben de çift anadal programı sayesinde ikinci sınıftan itibaren bilgisayar mühendisliği bölümünden 51 kredi fazladan dersler alarak mezun oldum. Detaylı bilgi için <a href="http://www.sis.itu.edu.tr/tr/capprg/KON_BLG.html">KON-BLG</a> çift anadal programını tıklayınız.
      </div>
      <li> 
        <a  data-toggle="collapse" class = "nss_question"> 
        Roket yapmak istiyorum; nasıl yapmalıyım?
        </a> 
      </li>
      <div class = "nss_answer">
        Maalesef roket yapımı konusunda çok fazla bir bilgim yok. Türkiye'de roket alanında çalışan ve sizi yönlendirebileceğim herhangi bir kimseyi de tanımıyorum. İnternet üzerinden Roketsan'da çalışan arkadaşlara ulaşmayı ve onlardan yardım istemeyi deneyebilirsiniz.
      </div>
      <li> 
        <a data-toggle="collapse" class = "nss_question"> 
        51. Bölge hakkında bilginiz var mı?
        </a> 
      </li>
      <div class = "nss_answer">
        Maalesef herhangi bir bilgim yok. Benim bildiklerim de şehir efsanelerinden çok farklı değil.
      </div>
      
      <!--
      <li> 
        <a data-toggle="collapse" class = "nss_question"> 
        Soru:
        </a> 
      </li>
      <div class = "nss_answer">
        Cevap:
      </div>
     -->

   </ol>
</div>


<script type="text/javascript">
   var questions = document.getElementsByClassName("nss_question");
   var answers = document.getElementsByClassName("nss_answer");

   //document.getElementById("nss_question_check").innerHTML = "Number of Questions: " + questions.length.toString();

   for (i = 0; i < questions.length ; i++)
   {
      var question_name = "question_" + i;
      var answer_name = "answer_" + i;

      questions[i].id = question_name;
      questions[i].href = "javascript:toggleDiv(\'" + answer_name + "\')";
      
      answers[i].id = answer_name;
   } 

  function toggleDiv(div_id) {
    var x = document.getElementById(div_id);
    if (x.style.display == "none") {
      x.style.display = "block";
    } 
    else {
      x.style.display = "none";
    }
  }
</script>


<!--
<div>
	<ul>
	{% for item in page.sss %}
      <li> <a data-toggle="collapse" href="javascript:toggleDiv('{{item.question}}')">{{item.question}}</a>  </li>
      <div id="{{item.question}}" style="display:none; background-color: lightgray">
       {{item.answer}}
       </div>

    {% endfor %}
    </ul>
</div>

-->

<!--

<section class="faq">
	<ul>
		{% for item in page.faq %}
			<li><a href="#{{ item.question | slugify }}">{{ item.question }}</a></li>
		{% endfor %}
	</ul>

	{% for item in page.faq %}
		<h2 id="{{ item.question | slugify}}">{{ item.question }}<a class="header-link" href="#{{ item.question | slugify }}"></a></h2>
		{{ item.answer | markdownify }}
	{% endfor %}
</section>

-->
