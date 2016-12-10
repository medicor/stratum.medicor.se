title: Stratum 3 - möte 2
tags:
  - Stratum 3
categories: []
date: 2015-02-17 13:55:00
---
Det finns ett antal saker som vi borde få gjort, eller åtminstone påbörja innan vi dyker allt för djupt ner i Keystone JS:

**A.** Uppgradering till ExtJS 5.1. Här är det framför allt diagramhanteringen som blir annorlunda då vi nu satsar på den bättre och modernare "Sencha Charts". Vad gäller själva Stratum (registreringsapplikation plus portal) samt SFRs registreringsapplikation så är det inte så mycket arbete. Vi har redan uppgraderat till ExtJS 5.0 så det mesta arbetet är taget. Däremot så innebär det en hel del för våra widgets eftersom just diagramhanteringen är ganska annorlunda. I ExtJS 5.0 så fungerade vare sig nya "Sencha Charts" eller gamla "ExtJS 4 Legacy Charts" tillräckligt bra för att vi skulle kunna växla, vilket är främsta skälet till att vi ligger kvar på v4.2.2. "Sencha Charts" fungerar under IE8, det har vi testat idag. **OBS! byt sidbredd till 960px (nu 920px).**

**B.** Byte av tema till "Crisp" (eller "Crisp Touch" &mdash; åldersfördelningen kan tala för den sistnämnda, se nedan). Detta kan låta enkelt men det är rätt mycket CSS-hack som tillkommit genom åren plus att en del vyer inte alls är gjorda för att kunna skalas på ett tillfredsställande sätt. Inte minst kan jag misstänka att det blir en del arbete i SFRs registreringsapplikation, där fler antaganden gjorts om typsnitt och grad.

![Åldersfördelning bland registrerande användare i Stratum](http://res.cloudinary.com/medicor/image/upload/v1424271560/https_docs.google.com_drawings_d_1KUPTksf5iMcnFaU_jQfzRtZZW95s3gZNzaR66FppgTM_pub_w_1475_h_581_tzo9yn.png)

**C.** Direct api:et behöver elimineras och gå upp i övrigt REST api. Hela Stratums registreringsapplikation behöver kapslas in api också. Oavsett lösning på detaljproblem är det viktigt för att lättare kunna identifiera vad som är "special" för SFR att särskilja det i "FractureApplication.js" (som tidigare), "FractureManagement.cs", där vi lägger allt som är noterat "//SFR Exclusive" i C#-koden, och SFR-specifik CSS "Default.css" till "Fracture.css".

Bildbank med Cloudinary kan vi titta på tidigt. Strategiskt då det gynnar vår webbredaktör. Kika på att flytta över hennes befintliga attribut på bilder plus själva bilderna. Hur funkar det? Kan vi bygga in den funktionaliteten i vårt CMS någorlunda enkelt?

![Registercentrum Västra Götaland](http://demo.registercentrum.se/Images/HeadLogoRC.png)