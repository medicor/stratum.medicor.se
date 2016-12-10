title: Stratum 3 - möte 3
tags:
  - Stratum 3
categories: []
date: 2015-03-24 09:29:00
---
Initialt fokus på Cloudinary som tjänst för bildhantering - vad behöver vi ha för konto? Börja med gratiskonto och se när vi slår i taket. Flera typer av uppgradering av konto finns. Hur skall vi hantera stora bilder? Kan vi "resampla" genom Cloudinarys api? Hur väl fungerar integrationen med Keystone? Får vår kommunikatör det som behövs? Här borde vi sitta med henne för att mer i detalj avgöra hur hon arbetar. Vi skulle kunna åta oss att importerar hennes nuvarande bilder med taggar och titlar. Är det görbart?

När vi ändå talar om import - är det möjligt att importera sidor i största allmänhet? Då kanske vi kan flytta hela gamla webbplatsen på ett automatiserat sätt. Under tiden som vi ändå implementerar de första sidorna kan vi undesöka hur svårt det skulle vara.

Vad gäller mallar så föreslås att vi utgår från de ursprungliga skisserna från Ibiz. Härifrån avvaktar vi resultatet från Tonsillregistrets genomgång av sin befintliga och nya webbplats med vår kommunikatör. En snarlik fråga är: skall vi ha med registerbegreppet i Keystone och arbeta med en databas eller skall vi satsa på flera Keystone-instanser?

Teknikval i allmänhet och stack på klientsidan i synnerhet. Keystones admingränssnitt är numera implementerat med Facebooks React. Föreslår att vi använder React då det finns med i Keystone. Keystone-projektet och dess community kommer troligen använda det än mer, då [Jed Watson](https://github.com/JedWatson) visat vägen. Läs också om hans argument för att [använda React](https://github.com/keystonejs/keystone/issues/503). Däremot kanske vi borde välja bort JSX på grund av förkompilering och jobbig syntax? Angular JS som alternativ skulle kunna vara intressant då de också har komponenttänkandet i fokus (via Directives) och att det används i nya NDR.

Handlebars använder vi som "template engine" då känns mest "klassisk". Dessutom kan Keystones generator producera vyer på detta sätt "out-of-the-box".

IISNode och övrig IIS-integration. Hur väl fungerar det? Tänker då på hantering av certifikat, tvingande HTTPS, loggning och annat. Kanske bäst att förpassa så mycket som möjligt till Node.js och Keystone.

Vår Github-organisation:
<div class="github-card" data-github="Registercentrum" data-width="400" data-height="150" data-theme="default"></div>
<script src="//cdn.jsdelivr.net/github-cards/latest/widget.js"></script>

![Registercentrum Västra Götaland](http://demo.registercentrum.se/Images/HeadLogoRC.png)