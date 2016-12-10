title: Stratum 3 - möte 1
tags:
  - Stratum 3
categories: []
date: 2015-02-04 14:13:00
---
## ExtJS hela vägen?

### Fördelar
* Ett ramverk som innehåller (i princip) allt vi behöver!
* Vi kan det rätt väl.

### Nackdelar
* ExtJS 5.1 är uttryckligen inte för smartphones ([Ext JS 5 currently does not support phones](http://www.sencha.com/products/extjs/details)).
* Responsivitet svårt att uppnå även om Sencha jobbat en del på det (se [artikel om responsiveConfig](http://www.sencha.com/blog/designing-responsive-applications-with-ext-js/)).
* Stor footprint i ramverket. Drabbar alla användare, även på "rotnivå".

## Alternativ utan ExtJS hela vägen?
* [Keystone JS](https://github.com/keystonejs/keystone) som CMS. Alternativ till Keystone finns också, [Apostrophe](https://github.com/punkave/apostrophe) (+ för WYSIWYG), [Ghost](https://github.com/TryGhost/Ghost). Dessa två är relativt etablerade. [Zero](https://github.com/sskyy/zero), [PencilBlue](https://github.com/pencilblue/pencilblue) är mer nyetablerade men ser spännande ut. En fördel med Keystone är att det är många som följer och bidrar. Samtliga ovan är Node.js-baserade. Körs lämpligen under [iisnode](https://github.com/tjanczuk/iisnode) på befintlig IIS-server. Hur bra fungerar det? Förmodligen bra eftersom [Microsoft Azure använder det](http://blogs.msdn.com/b/hanuk/archive/2012/05/05/top-benefits-of-running-node-js-on-windows-azure.aspx). 
* Registreringsapplikationen får göras om som "widget", eller åtminstone bli api-driven till 100%.
* Ramverk på klientsidan? [React](http://facebook.github.io/react/) skulle nog passa fint men vi får ta reda på framöver vad vi behöver.

## Annat värt att notera
* Direct-api:et försvinner och ersätts med REST! **Dock får vi inte ta bort stödet för SFRs applikation.**
* Widgets till GitHub! Strategi? Struktur? Arbetsmetoder?
* ExtJS för Widgets nödvändigt. Det är trots allt det mest heltäckande ramverket för den typen av grafisk återkoppling. Dessutom vore det väldigt mycket arbete att byta ut.

## Strategi
* Viktigt att avgöra om *vi bygger för hela RC eller enbart Stratum?*
* Om vi bygger för RC också är det viktigt att vi intervjuar och kartlägger Charlottas arbetssätt. Vad är det som fungerar dåligt idag? Vad fungerar bra? Vad är superviktigt?
* Bygg i så fall ny webbplats vid sidan av och presentera när det är någorlunda färdigt. Då blir det väsentligt att CMS-funktionerna erbjuder något nytt. Måste också se ut som RCs nuvarande webbplats.
* Viktigt att våra användare får en möjlighet att se vad som är på gång när det finns något vettigt att visa.
* Sencha Touch droppas helt. Eftersom vi bygger en responsiv webbplats skall inte sådan teknik behövas. Detta innebär att en ny registreringsapplikation för PROM, eller rättare sagt en "en-fråga-per-sida"-applikation tas fram som en widget. Gamla "missbenämnda" MetaBrowser görs också om och den funktionaliteten (och mer därtill) läggs upp som en widget.

Att också ersätta den här bloggen med en som finns i Keystone känns lämpligt- :-)

![Registercentrum Västra Götaland](http://demo.registercentrum.se/Images/HeadLogoRC.png)