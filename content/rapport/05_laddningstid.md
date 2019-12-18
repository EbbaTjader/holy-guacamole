---
---
Webbplatsers laddningstid och användbarhet
=======================

Urval
-----------------------
Jag väljer samma webbplatser som för min tidigare rapport om färgval. De har alla väldigt många bilder och jag tror därför de passar väldigt bra att använda till denna rapport med.

####1. [Lyko](https://www.lyko.se/)
####2. [Bangerhead](https://www.bangerhead.se/)
####3. [Eleven](https://eleven.se/)

Metod
-----------------------
Jag använder mig av [Google PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/) för att se prestandan på webbplatsen i både Mobile och Desktop mode. Jag mäter sidans laddningtid i Devtools Networks används för att mäta sidans laddningstid, antalet resurser som laddas och sidans totala storlek. Mätningen görs tre gånger på tre olika sidor och jag tar fram ett snittvärde av det.

Resultat
-----------------------

[Excellänk](https://docs.google.com/spreadsheets/d/1_-llsA2N_AEr2zvnX24dAWjW2kBnuHQD-_TS622_4n4/edit?usp=sharing)

####__Lyko__

[FIGURE src=image/lyko.PNG?h=300]

Sidorna som mättes:
####1. [Hårvård](https://www.lyko.se/harvard)
####2. [Hudvård](https://www.lyko.se/hudvard)
####3. [Parfym](https://www.lyko.se/parfym)



####__Bangerhead__

[FIGURE src=image/bangerhead.PNG?h=300]

Sidorna som mättes:
####1. [Hårvård](https://www.bangerhead.se/harvard)
####2. [Hudvård](https://www.bangerhead.se/hudvard)
####3. [Parfym](https://www.bangerhead.se/parfym)


####__Eleven__

[FIGURE src=image/eleven.PNG?h=300]

Sidorna som mättes:
####1. [Hårvård](https://www.eleven.se/harvard)
####2. [Hudvård](https://www.eleven.se/hudvard)
####3. [Parfym](https://www.eleven.se/parfym)

Analys
-----------------------

Lyko hade längst laddningstid, störst storlek av sidorna och ett stort antal resurser. Det var en hel del PageSpeed sade som skulle kunna förbättra sidan. Bland annat genom att undvika upprepade omdirigeringar, se till att texten förblir synlig för användaren medan webbteckensnittet läses in, minska tiden det tar att tolka, kompilera och köra JS-kod, samt lagra cachefilerna en längre tid så att upprepade besök på sidan går snabbare. De tipsade även om att undvika en hög nätverksbelastning och testa att låta tredjepartskod läsas in efter sidans huvudinnehåll lästs in helt. Lyko har även ett väldigt stort DOM-träd som innehåller 1525 element vilket ökar minnesförbrukningen och förlänger formatberäkningarna. Det rekommenderade antalet DOM-element bör vara mindre är 1500.

Bangerhead hade helt okej laddningstid då det inte översteg fyra sekunder. Deras betyg för mobile mode var väldigt dåligt och för desktop mode var det okej. De hade fem gånger mindre resurser än Lyko och hälften av Lykos storlek. Man skulle tro att deras laddningstid då bör vara mycket bättre än Lykos men skillnaderna var inte så stora. Förbättringar som Bangerhead skulle kunna göra innefattar bland annat att ta bort oanvänd CSS-kod, ta bort resurser som blockerar renderingar, alltså att infoga nödvändig JS-/CSS-kod diekt på sidan och skjuta upp inläsningen av JS-kod som är mindre viktiga. De kan även använda bilder i modernare format istället för PNG eller JPG, använda rätt storlek på bilder samt aktivera textkomprimering. Bangerhead bör även åtgärda samma saker som Lyko: se till att texten är synlig för användaren medan webbteckensnittet läses in, minska påverkan från tredjepartskod, undvika ett onödigt stort DOM-träd (3651 element), minska körningstiden för JavaScript och lagra cachen en längre tid.

Eleven fick högst betyg i både mobile och desktop mode. De hade även överlägset bäst laddningstid vilket kan förklaras av att de hade lägst antal resurser (hälften av Bangerheads) och minst storlek på sidan. PageSpeed tipsar om att det kan vara bra att använda '< link rel=preload >' för att prioritera hämtningar av resurser som kommer begäras senare i sidinläsningen, alltså att läsa in viktiga resurser i förväg. Eleven bör även skjuta upp inläsningen av bilder som inte visas på skärmen.
Eleven delar många förbättringsaspekter med de två andra webbplatserna: ta bort oanvänd CSS-kod, ta bort resurser som blockerar renderingen, använd bilder med rätt storlek och i ett modernare format, aktivera textkomprimering, se till att all text förblir synlig medan webbteckensnittet läses in, minska påverkan från tredjepartskod, lagra cachen en längre tid, minska körningstiden för JavaScript samt minska storleken på DOM-trädet (1430 element).


En snabb laddningtid för mig är om det inte överstiger fyra sekunder. Allt över det klassar jag som långsamt. Baserat på det så blir endast Bangerhead och Eleven godkända, men Eleven är en klar vinnare. Det märks rätt tydligt nu när man fokuserar på laddningstiden, skillnaderna mellan Lyko som är långsammast och Eleven som är snabbast. Eleven fick klart bäst betyg av PageSpeed, de har en liten sidstorlek och ett lågt antal resurser. Bangerhead hamnar på andra plats med lite större antal resurser och lite större sidstorlek. Lyko har väldigt många resurser (363 jämfört med Elevens ynka 33), lång laddningstid samt en storlek på 2,2 MB. Därför hamnar Lyko på sista plats.
