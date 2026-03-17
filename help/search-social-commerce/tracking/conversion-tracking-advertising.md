---
title: Informatie over Adobe Advertising-tags voor conversie en bijhouden
description: Meer informatie over het gebruik van de Adobe Advertising-tags voor conversie-tracking.
exl-id: 8194d5eb-9a5d-4c4e-bb02-e578ffb84d18
feature: Search Tracking
source-git-commit: 3f91cd92a364a8e9dd569bd590c59740ea1493d7
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Informatie over Adobe Advertising-tags voor conversie en bijhouden

Adobe Advertising houdt conversies bij die het resultaat zijn van klikken op advertenties die gebruikmaken van trackingtags voor Adobe Advertising-conversie en die worden ingevoegd in de webpagina&#39;s die worden geopend wanneer een conversiegebeurtenis plaatsvindt, zoals een pagina &quot;success&quot;. De tags bevatten ingesloten informatie om de transactiegegevens samen met de Adobe Advertising-cookie van de gebruiker naar een trackingserver te verzenden, van waaruit de transactie wordt gecrediteerd naar de juiste advertentie-klik of -indruk (volgens de conversie-attributie-instellingen van de adverteerder).

U kunt [ conversie-volgende markeringen ](/help/search-social-commerce/tools/conversion-tag-generate.md) binnen Onderzoek, Sociaal, &amp; Commerce produceren of markeringen in Adobe Experience Platform (vroeger genoemd als Adobe Experience Platform Launch) gebruiken.

>[!NOTE]
>
>Als de gebruiker geen geldige cookie heeft, rapporteert Adobe Advertising de conversie niet.

Voor elke set conversiemetriek die u wilt bijhouden, moet u een aparte conversietag maken en implementeren. U kunt een van de volgende typen conversietags genereren.

* (Aanbevolen) JavaScript-tags (versie 3 of versie 2) die niet zichtbaar zijn op de webpagina&#39;s.

* HTML-afbeeldingstags voor het weergeven van transparante afbeeldingen (pixels) van 1 x 1 pixel (onzichtbaar voor eindgebruikers) op webpagina&#39;s. Gebruik afbeeldingstags alleen als het bedrijf een beleid heeft tegen het gebruik van JavaScript-tags.

Voor meer informatie over de verschillen tussen de markeringstypes, zie &quot;[ FAQs over de omzetting van de Wolk van de Reclame volgende markeringen ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

>[!NOTE]
>
>* Met deze functie worden geen afbeeldingstags of JavaScript-tags toegevoegd aan de webpagina&#39;s van de adverteerder. De tags moeten worden toegevoegd volgens de normale procedure van de adverteerder voor het bijwerken van webpagina&#39;s.
>* Denk na over de tijd die nodig is om de tags te implementeren. Afhankelijk van het beleid van het bedrijf kan de implementatie weken of zelfs maanden duren.

## Functies van de Adobe Advertising-tags voor conversietracering

Met de pixel voor het bijhouden van conversies kan Adobe Advertising het volgende doen:

* Conversiegegevens bijhouden en rapporteren op trefwoordniveau voor zoekcampagnes.

* Conversiegegevens op advertentieniveau (creatief) bijhouden en rapporteren over alle marketingkanalen (betaald zoeken en weergeven), wat creatieve tests mogelijk maakt.

* Conversiegegevens bijhouden en rapporteren op transactieniveau in al uw marketingkanalen.

* Toon hoe uw omzettingen over uw verschillende marketing kanalen worden verdeeld zodat kunt u zien welke het meest effectief is.

* Rapporteer en optimaliseer de bewerkingen op verschillende toewijzingsniveaus (zoals conversies toewijzen aan de laatste gerelateerde gebeurtenis of alle gebeurtenissen gelijkmatig afwegen).

* U kunt hulp bieden bij klikken (zoektrefwoorden of plaatsen die hebben bijgedragen aan een conversie-funnel) en kanaalassistenten (gebruikersgebeurtenissen die hebben bijgedragen aan een conversie-funnel, mogelijk via meerdere marketingkanalen).

* Geef zichtbaarheid in de geografische distributie- en verwijzingsdomeinen van uw siteverkeer en conversies zodat u uw geografische en websitegerichtheid kunt verfijnen.

* Analyseer de trends binnen de week of binnen de dag, die kunnen worden gebruikt om de conversietarieven te verbeteren.

>[!MORELIKETHIS]
>
>* [ het volgen van de Omzetting opties ](conversion-tracking-about.md)
>* [ produceer en voer een de omzettingsmarkering van Adobe Advertising uit ](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [ Formaat van de conversie van JavaScript volgmerkversie 3 ](format-conversion-tag-jsv3.md)
>* [ Formaat van de conversie van JavaScript volgmerkversie 2 ](format-conversion-tag-jsv2.md)
>* [ Formaat van beeldomzetting volgende markeringen ](format-conversion-tag-image.md)
>* [ Veelgestelde vragen over omzetting en de het volgen markeringen van de paginamening ](faqs-conversion-page-view-tracking-tags.md)
>* [ de de omzettingsafbeelding van Adobe Advertising JavaScript markering ](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
