---
title: Een tag voor een advertentie exporteren en implementeren voor een live beleving
description: Leer hoe u een advertentietag exporteert en optioneel uploadt naar een Advertising DSP-campagne.
feature: Creative Experiences
source-git-commit: fc2cd07944026badc0722c1449aa9aaf2c94bfd7
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---

# Een tag voor een advertentie exporteren en implementeren voor een live beleving

*Gesloten bèta*

Zodra een ad markering voor een specifieke creatieve grootte voor a [ levende ](experience-about.md#experience-statuses) ervaring beschikbaar is, kunt u de markering in JavaScript en iframe formaten voor implementatie op Advertising DSP of andere DSP produceren en kopiëren. De tags voor DSP bevatten alle macro&#39;s die zijn vereist voor DSP.

Adverteerders met Advertising DSP kunnen optioneel tags als advertenties rechtstreeks uploaden naar een Advertising DSP-campagne.

>[!NOTE]
>
>* Wanneer u een ervaring met doelstructuurbeleid maakt, maakt [!DNL Creative] automatisch een ad-tag voor elke toepasbare creatieve grootte.
>* Wanneer u een ervaring zonder beslissingsboom het richten creeert, moet u [ manueel een ad markering ](experience-tag-create-manually.md) voor elke toepasselijke creatieve grootte creëren.
>* Ervingstags zijn dynamisch. U hoeft de tags niet bij te werken als u een ervaring bewerkt.

## Een ad-tag exporteren voor een ervaring met doelstructuurtoewijzing

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** .

1. Voer een van de volgende handelingen uit:<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * Klik in de kaartweergave op **[!UICONTROL ...]** naast de naam van de ervaring en klik vervolgens op **[!UICONTROL Tag Manager]** .

   * Houd in de tabelweergave de cursor boven de rij, klik op **[!UICONTROL More]** en klik vervolgens op **[!UICONTROL Tag Manager]**

1. Houd de curseur over de rij voor de toepasselijke advertentietag en klik of ![ Uitvoer en markeringen ](/help/creative/assets/export.png " de Uitvoer en markeringen ") **[!UICONTROL Export ad tags]** of ** [!UICONTROL ... More] > **[!UICONTROL Export ad tags]**.

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. (Optioneel) Geef op het tabblad [!UICONTROL Macros] maximaal vijf aangepaste macro&#39;s op die u in de tag wilt opnemen. Voor elke macro die moet worden opgenomen:

   1. Selecteer een selectievakje.<!-- Explain more -->

   1. Voer de aangepaste macro in.<!-- Explain more -->

1. Klik op **[!UICONTROL Next]** in de rechterbovenhoek of klik op **[!UICONTROL Generate ad tags]** in het linkermenu.

1. Selecteer het markeringstype: ** *JavaScript<!-- sic -->* ** of ** *IFRAME* ** <!-- sic -->.

1. Selecteer in de lijst [!UICONTROL Destinations] waar u advertenties wilt maken.

   * *Adobe Advertising:* voor advertenties zult u in Advertising DSP creëren.

   * *Algemeen:* voor advertenties zult u in andere DSP creëren. **Nota:** u kunt extra macro&#39;s moeten manueel omvatten zonodig.

1. Klik op **[!UICONTROL Generate tags]**.

1. Kopieer of download de tags:

   * Om een markering voor één enkele advertentiegrootte te kopiëren, breid de markeringsrij uit, houd de curseur over de rij, en klik dan ](/help/creative/assets/copy.png " Exemplaar ") **[!UICONTROL Copy]**.<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->![

   * Om alle geproduceerde markeringen als dossier aan de standaarddownloadplaats van uw browser te downloaden, klik ![ de markeringen van de Download ](/help/creative/assets/download.png " Codes van de Download ").

   U kunt het bestand openen in een teksteditor om elke tag te kopiëren. Voor JavaScript-tags wordt de tag ingesloten in `<script></script>` - en `<noscript></noscript>` -tags. Voor iframe-tags wordt de tag ingesloten in `<iframe></iframe>` -tags.

1. De labels voor de desbetreffende DSP implementeren:

   * Geef voor andere DSP dan Advertising DSP de tags op aan wie de advertenties binnen de DSP maakt.

   * Voor Advertising DSP:

      1. Klik op **[!UICONTROL Next]** in de rechterbovenhoek of klik op **[!UICONTROL DSP link]** in het linkermenu.

      1. Selecteer de campagne waarvoor de tag ad beschikbaar wordt.

      1. Klik op **[!UICONTROL Assign Tags]**.

         DSP wordt geopend in de [!UICONTROL Ads] -weergave voor de geselecteerde campagne.

      1. Reviseer in de [!UICONTROL Create ads] -weergave de advertentietags, selecteer elke tag waarvoor u een advertentie wilt maken en klik op **[!UICONTROL Create]** .

         De weergave [!UICONTROL Ads] bevat nu de nieuwe advertenties, die dezelfde namen hebben als de advertentietags in [!DNL Creative] . U kunt [ de advertenties aan om het even welke plaatsing ](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) in de campagne vastmaken.

<!-- no way to get back to the Creative Tag Manager -- you have to click back through the main menu -->

<!-- Add this info, with descriptions:

## Ad tag formats

### JavaScript

### Iframe

-->

>[!MORELIKETHIS]
>
>* [ creeer manueel een ad markering voor een toepasselijke creatieve grootte ](experience-tag-create-manually.md)
>* [ wijs creatieve elementen aan een ad markering voor ervaringen toe zonder zich te richten ](experience-tag-assign-creatives.md)
>* [ noem een advertentietag anders ](experience-tag-rename.md)
