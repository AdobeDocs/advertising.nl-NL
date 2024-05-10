---
title: Tags voor conversie naar Adobe Advertising bijhouden
description: Meer informatie over het gebruik van conversie-trackingtags voor Adoben Advertising.
exl-id: 8194d5eb-9a5d-4c4e-bb02-e578ffb84d18
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Tags voor conversie naar Adobe Advertising bijhouden

Adobe Advertising houdt conversies bij die het resultaat zijn van klikken op advertenties met behulp van trackingcodes voor Adobe Advertising conversie die worden ingevoegd in de webpagina&#39;s die worden geopend wanneer een conversiegebeurtenis plaatsvindt, zoals een pagina &quot;success&quot;. De tags bevatten ingesloten informatie om de transactiegegevens samen met het cookie van de Adobe Advertising van de gebruiker naar een trackingserver te verzenden, waaruit de transactie wordt gecrediteerd naar de juiste advertentie-klik of -indruk (volgens de toewijzingsinstellingen van de converteerder).

>[!NOTE]
>
>Als de gebruiker geen geldige cookie heeft, rapporteert de Adobe Advertising de conversie niet.

Voor elke set conversiemetriek die u wilt bijhouden, moet u een aparte conversietag maken. Geef de tags aan de adverteerder of het bureau een lijst met webpagina&#39;s waarop u ze wilt invoegen. U kunt een van de volgende typen conversietags genereren. Zie &quot;[Een conversietag voor Adoben Advertising genereren](/help/search-social-commerce/tools/conversion-tag-generate.md)&quot; voor instructies.

* (Aanbevolen) JavaScript-tags (versie 3 of versie 2) die niet zichtbaar zijn op de webpagina&#39;s.

* HTML-afbeeldingstags om transparante afbeeldingen (pixels) van 1 pixel x 1 pixel weer te geven, die onzichtbaar zijn voor eindgebruikers, op de webpagina&#39;s. Gebruik afbeeldingstags alleen wanneer het bedrijf een beleid heeft dat is ingesteld tegen het gebruik van JavaScript-tags.

Raadpleeg voor meer informatie over de verschillen tussen de verschillende tagtypen &quot;[Veelgestelde vragen over trackingtags voor Advertising Cloud-conversie](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

>[!NOTE]
>
>* Deze functie voegt geen afbeeldingstags of JavaScript-tags toe aan de webpagina&#39;s van de adverteerder. De tags moeten worden toegevoegd volgens de normale procedure van de adverteerder voor het bijwerken van webpagina&#39;s.
>* Denk na over de tijd die nodig is om de tags te implementeren. Afhankelijk van het beleid van het bedrijf kan de implementatie weken of zelfs maanden duren.

## Functies van de conversietags voor Adoben Advertising

Met de pixel voor het bijhouden van conversies kan Adobe Advertising het volgende doen:

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
>* [Een conversietag voor Adoben Advertising genereren](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Indeling van JavaScript-tags voor conversie bijhouden versie 3](format-conversion-tag-jsv3.md)
>* [Indeling van JavaScript-tags voor bijhouden van conversie versie 2](format-conversion-tag-jsv2.md)
>* [Opmaak van trackingtags voor afbeeldingsconversie](format-conversion-tag-image.md)
>* [Veelgestelde vragen over tags voor conversie en bijhouden van paginaweergaven](faqs-conversion-page-view-tracking-tags.md)
>* [De JavaScript-conversietoewijzingstag Adobe Advertising](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
