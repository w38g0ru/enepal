---
layout: post
title:  "गिटहब ट्युटोरियल"
date:   2018-12-17 20:38:12 +0545
---

कमान्डलाईन वा भनौ टर्मिनलमा केही फरक कमाण्डहरुले लेखेर काम गरिने भएको हुनाले हुन सक्छ धेरैलाई गिटहब धेरै नै गार्हो लाग्छ । तर केही कमाण्डहरु मात्र भए पनि सम्झीने भने गिटहब धेरैले सोचे जस्तो अप्ठेरो छैन र यसको महत्व बुझे पछी त झनै काम गर्न सजिलो र रमाईलो छ ।<br />
यहाँ म युबुन्तुको Apache सर्भरमा रहेको www(html) भित्र रहेको डाईरेक्ट्रीमा रहेको कुनै पनि वेबसाईटको सबै फाईलहरु कसरी गिटहब मा पुस (अपलोड) गर्ने भन्ने बारेमा मैले जानेको तरिका बताउन गई रहेको छु ।<br />
<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="https://4.bp.blogspot.com/-d6diYiS8-UA/XBZcpR6OkII/AAAAAAAAFqo/sZHdk9SP_lop_HBp4tvLrPyoPO4bo8r8ACLcBGAs/s1600/git-hub.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" data-original-height="275" data-original-width="575" src="https://4.bp.blogspot.com/-d6diYiS8-UA/XBZcpR6OkII/AAAAAAAAFqo/sZHdk9SP_lop_HBp4tvLrPyoPO4bo8r8ACLcBGAs/s1600/git-hub.png" /></a></div>
<br />
सबै भन्दा पहिले तपाईले गिटहबलाई तपाई को हो भनेर चिनाउन पर्ने हुन्छ त्यसको लागी ईमेल र आफ्नो नाम लेख्नु होला । उदारणको लागि मेरो गिटहब ईमेल w38g0ru@anish.com.np होआ त्यसैले त्यही राखे username w38g0ru राखे<br />
<pre class="jumbotron">
git config - - global user.email "w38g0ru@anish.com.np"
git config - - global user.name w38g0ru</pre>
अब सबै भन्दा पहिले www(html) फोल्डर भित्र रहेको जुन साईट (फोल्डर) लाई गिटहबमा अपलोड गर्ने हो त्यसमा पस्ने । उदारणको लागी : cd /var/www/html/mysite यो कमाण्डले mysite भन्ने फोल्डरलाई गिटहबमा पुस गर्न खोजीएको हो भन्ने जनाउछ ।<br />
<br />
अब गिटहबलाई ईनिसियट (सञ्चालन गर्ने)<br />
<pre>git init</pre>
(यस कमाण्डले /var/www/html भित्र रहेको mysite भन्ने फोल्डरमा गिट ईनिसियट हुन्छ र यसले .git भन्ने एउटा हिडेन फोल्डर बनाउछ । फेरी फेरी यसै साईटमा (गिटहबमा) काम गर्ने हो भने त्यो फोल्डरलाई डिलिट हुन दिन हुन्न ।)<br />
<br />
गिट फोल्डर भित्र आफ्ना सबै फाईल घुसाउनको लागी तल दिएको कमान्ड टाईप गरी ईन्टर थिच्न पर्छ । यहाँ - - all भन्नाले माथि उल्लेखति mysite भन्ने फोल्डर भित्र रहेको सबै फोल्डर , सबफोल्डर र फाईलहरु बुझाउछ । सबै फोल्डर पुस गर्न छैन भने - - - all को सट्टामा फाईलको मान्तर नाम दिए हुन्छ । उदारणको लागी git add index.php भन्नाले index.php भन्ने फोल्डर मा्तर अपलोड गरीयोस भन्ने बुझिन्छ । थप जानकारिको लागि यहाँ क्लिक गर्नुहोस ।<br />
<pre>git add --all</pre>
माथि एड गरेका फाईलहरु कमिट गर्नको लाई तल दिएको कमाण्ड प्रयोग गर्नु पर्दछ । यहाँ कमिट भन्नाले कुनै पनि फाईलहरुमा के परिवर्तन गरिएको हो पछी याद रहोस भनि त्यो परिवर्तन जनाउने कुनै एक वाक्य वा शब्द भन्ने जाउछ । यस सम्बन्धी बिस्तृत जानकारीको लागी यहाँ क्लिक गर्नुहोस ।<br />
<pre>git commit -m "working file"</pre>
अब सबै फाईलहरु गिटहब सर्भरमा तपाईको www(html)फोल्डर भित्र रहेको mysite भन्ने फोल्डरमा जे जुन अवश्थामा फाईल फोल्डर छन त्यसै अनुसार गिटहब सर्भरमा अपलोड गर्नको लागि तल दिएको कमाण्ड प्रयोग गर्नु पर्दछ । git-remote कमाण्डबारे बिस्तृत जानकारीको लागि यो लिक्ङ्क खोल्नु होला ।<br />
<pre>git remote add origin https://github.com/githutusername/repository.git</pre>
र अन्तमा सबै फाईल अपलडो गर्नको लागी तल दिए अनुसार कमान्ड प्रयोग गर्नु पर्दछ । git push कमाण्ड बारे बिस्तृत जान्नको लागी यहाँ क्लिक गर्नुहोस ।<br />
<pre>git push -force origin master</pre>
<h3>
मोडिफाई गरेको फाईल मात्र कसरि हाल्ने</h3>
गिटहबमा पुस गरी सकेको फाईलहरु मध्ये कुनै एउटामा केहि मोडिफाई गर्नु भो र त्यो मोडिफिकेशन मात्र पुस (अपलोड) गर्ने हो भने तल दिएको कमाण्ड प्रयोग गर्नु पर्दछ ।<br />
<pre>git add -u</pre>
अब यो मोडिफाई गरेको फाईलमा के चेन्ज गरेको हो त्यसलाई 'कमिट' गर्नु पर्दछ ।<br />
<pre>git commit -m "correcting placeholder"</pre>
यती गरेको पछी सो फाईल(हरु) लाई पुस (अपलोड) गर्नको लागि तल दिएको कमाण्ड प्रयोग गर्नु पर्दछ ।<br />
<pre>git push origin master - force</pre>

> प्रो टिप्स : मानि लिनुस , तपाई फाईल अपडेट गर्दै सर्भरमा पुस गर्दै हुनुहुन्थ्यो । कारणबस पछिल्लो तेस्रो कमिट (पुस गर्नु अगाडी) को अवश्थामा पुग्न पर्ने (अनडु गर्न पर्ने) भयो रे  । के गर्ने ??  सिम्पल छ  - सबै भन्दा पहिले  git log कमाण्डको साहायताले सुरुमा जुन कमिट सुधार्ने हो, त्यो फेला पार्ने र त्यस कमिटको ह्यास कपी गर्ने अनि git revert लेखेर अगि कपि गरेको ह्यास पेष्ट गर्ने ।  अब फाईल पछिल्लो तेस्रो कमिट अगाडीको अवश्थामा पुग्छ ।   

<h3>
कुनै फोल्डर / फाईल कसरी हटाउने</h3>
गिटहबमा यदी कुनै फाईल वा फोल्डर डिलिट गर्नु परेमा git rm कमाण्डको प्रयोग गरिन्छ । स्मरण रहोस git rm - ले वर्किङ्ग डाईरेक्ट्रीको फाईल हटाउने काम गर्दछ ।<br />
<pre>git rm --cached filename</pre>
यो कमान्डले लोकल डाईरेकट््रीमा रहेको फाई सुरक्षित रहन्छ भने गिट रिपोजटरीको फाईल मात्र डिलिट हुन्छ ।

