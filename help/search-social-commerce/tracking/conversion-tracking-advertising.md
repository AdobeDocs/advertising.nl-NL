---
title: Informatie over conversietags voor Adobe-advertenties
description: Meer informatie over het gebruik van conversietags voor Adobe-advertenties.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Informatie over conversietags voor Adobe-advertenties

Adobe In advertenties worden omzettingen bijgehouden die het gevolg zijn van klikken op advertenties met Adobe Advertising tracking-tags die worden ingevoegd in de webpagina&#39;s die worden geopend wanneer een conversiegebeurtenis plaatsvindt, zoals een pagina &quot;success&quot;. De tags bevatten ingesloten informatie om de transactiegegevens samen met het Adobe Advertising-cookie van de gebruiker te verzenden naar een trackingserver, waar de transactie wordt gecrediteerd naar de juiste advertentie-klik of -indruk (volgens de conversie-attributie-instellingen van de adverteerder).

>[!NOTE]
>
>Als de gebruiker geen geldige cookie heeft, rapporteert Advertising de conversie niet.

Voor elke set conversiemetriek die u wilt bijhouden, moet u een aparte conversietag maken. Geef de tags aan de adverteerder of het bureau een lijst met webpagina&#39;s waarop u ze wilt invoegen. U kunt een van de volgende typen conversietags genereren. Zie &quot;[Een conversietag voor Adobe-advertenties genereren](/help/search-social-commerce/tools/conversion-tag-generate.md)&quot; voor instructies.

* (Aanbevolen) JavaScript-tags (versie 3 of versie 2) die niet zichtbaar zijn op de webpagina&#39;s.

* HTML-afbeeldingstags om transparante afbeeldingen (pixels) van 1 pixel x 1 pixel weer te geven, die onzichtbaar zijn voor eindgebruikers, op de webpagina&#39;s. Gebruik afbeeldingstags alleen wanneer het bedrijf een beleid heeft dat is ingesteld tegen het gebruik van JavaScript-tags.

Zie &quot;[Veelgestelde vragen over trackingtags voor Advertising Cloud-conversie](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

>[!NOTE]
>
>* Deze functie voegt geen afbeeldingstags of JavaScript-tags toe aan de webpagina&#39;s van de adverteerder. De tags moeten worden toegevoegd volgens de normale procedure van de adverteerder voor het bijwerken van webpagina&#39;s.
>* Zorg ervoor dat u rekening houdt met de tijd die nodig is om de tags te implementeren. Afhankelijk van het beleid van het bedrijf kan de implementatie weken of zelfs maanden duren.


## Kenmerken van de conversietags voor Adobe-advertenties

Met de pixel voor het bijhouden van conversies kan Adobe-reclame het volgende doen:

* Conversiegegevens bijhouden en rapporteren op trefwoordniveau voor zoekcampagnes.

* Conversiegegevens op advertentieniveau (creatief) bijhouden en rapporteren over alle marketingkanalen (betaald zoeken en weergeven), wat creatieve tests mogelijk maakt.

* Conversiegegevens bijhouden en rapporteren op transactieniveau in al uw marketingkanalen.

* Toon hoe uw omzettingen over uw verschillende marketing kanalen worden verdeeld zodat kunt u zien welke het meest effectief is.

* Rapporteer en optimaliseer de bewerkingen op verschillende toewijzingsniveaus (zoals conversies toewijzen aan de laatste gerelateerde gebeurtenis of alle gebeurtenissen gelijkmatig afwegen).

* U kunt de hulp bij klikken (zoektrefwoorden of plaatsen die hebben bijgedragen aan een conversietrechter) en kanaalassistenten (gebruikersgebeurtenissen die hebben bijgedragen aan een conversietrechter, mogelijk via meerdere marketingkanalen) zichtbaar maken.

* Geef zichtbaarheid in de geografische distributie- en verwijzingsdomeinen van uw siteverkeer en conversies zodat u uw geografische en websitegerichtheid kunt verfijnen.

* Analyseer de trends binnen de week of binnen de dag, die kunnen worden gebruikt om de conversietarieven te verbeteren.

>[!MORELIKETHIS]
>
>* [Opties voor bijhouden van conversie](conversion-tracking-about.md)
>* [Een conversietag voor Adobe-advertenties genereren](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Indeling van JavaScript-tags voor conversie bijhouden versie 3](format-conversion-tag-jsv3.md)
>* [Indeling van JavaScript-tags voor bijhouden van conversie versie 2](format-conversion-tag-jsv2.md)
>* [Opmaak van trackingtags voor afbeeldingsconversie](format-conversion-tag-image.md)
>* [Veelgestelde vragen over tags voor conversie en bijhouden van paginaweergaven](faqs-conversion-page-view-tracking-tags.md)
>* [De conversietoewijzingstag voor JavaScript-Adobe-reclame](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)

