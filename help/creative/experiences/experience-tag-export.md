---
title: Een tag voor een advertentie exporteren en implementeren voor een live beleving
description: Leer hoe u een advertentietag exporteert en optioneel uploadt naar een Advertising DSP-campagne.
feature: Creative Experiences
exl-id: 4ae05142-8319-4329-96d7-f87d77f02745
source-git-commit: 45b2dad83aa626ea30e7553df7caaf5e7f53b3e1
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Een tag voor een advertentie exporteren en implementeren voor een live beleving

*Gesloten bèta*

Zodra een ad markering voor een specifieke creatieve grootte voor a [ levende ](experience-about.md#experience-statuses) ervaring beschikbaar is, kunt u de markering in JavaScript en iframe formaten voor implementatie op Advertising DSP of andere DSPs produceren en kopiëren. De tags voor DSP bevatten alle macro&#39;s die vereist zijn voor DSP.

Adverteerders met Advertising DSP kunnen optioneel tags rechtstreeks uploaden naar een Advertising DSP-campagne als advertenties met het advertentietype &quot;standaarddisplay&quot;.

>[!NOTE]
>
>* Wanneer u een ervaring met doelstructuurbeleid maakt, maakt [!DNL Creative] automatisch een ad-tag voor elke toepasbare creatieve grootte.
>* Wanneer u een ervaring zonder beslissingsboom het richten creeert, moet u [ manueel een ad markering ](experience-tag-create-manually.md) voor elke toepasselijke creatieve grootte creëren.
>* Ervingstags zijn dynamisch. U hoeft de tags niet bij te werken als u een ervaring bewerkt.
>* Zorg ervoor dat de campagnes waarin u een advertentie-ervaring zult uitvoeren richten die met de ervaring compatibel is. Het gedrag voor hiërarchische activering kan per DSP variëren. In Advertising DSP wordt &#39;ad-level&#39;-doelen toegepast boven op (niet in plaats van) het doel op plaatsingsniveau.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** .

1. Voer een van de volgende handelingen uit:<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * Klik in de kaartweergave op **[!UICONTROL ...]** naast de naam van de ervaring en klik vervolgens op **[!UICONTROL Tag Manager]** .

   * Houd in de tabelweergave de cursor boven de rij, klik op **[!UICONTROL More]** en klik vervolgens op **[!UICONTROL Tag Manager]** .

1. Houd de curseur over de rij voor de toepasselijke advertentietag en klik of ![ Uitvoer en markeringen ](/help/creative/assets/export.png " de Uitvoer en markeringen ") **[!UICONTROL Export ad tags]** of **&#x200B; [!UICONTROL ... More] > &#x200B;** [!UICONTROL Export ad tags]**.

>[!NOTE]
>
>Voor standaardvideo en ervaringen wacht u tot de kolom [!UICONTROL Tag Status] &quot; [!UICONTROL Ready]&quot; toont. Dit geeft aan dat alle video&#39;s in de ervaring zijn getranscodeerd. Alle videocreatieve beelden worden automatisch getranscodeerd door DSP, maar u kunt naar keuze [ uitgever-specifieke transcodering ](experience-tag-video-transcoding.md) op om het even welke video en ervaringstag toepassen.

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. (Optioneel) Geef op het tabblad [!UICONTROL Macros] maximaal vijf aangepaste macro&#39;s op die u in de tag wilt opnemen. Voor elke macro die moet worden opgenomen:

   1. Selecteer een selectievakje.<!-- Explain more -->

   1. Voer de aangepaste macro in.<!-- Explain more -->

1. Klik op **[!UICONTROL Next]** in de rechterbovenhoek of klik op **[!UICONTROL Generate ad tags]** in het linkermenu.

1. Selecteer het markeringstype: ** *JavaScript<!-- sic -->* **&#x200B; of &#x200B;** *IFRAME* ** <!-- sic -->.

1. Selecteer in de lijst [!UICONTROL Destinations] waar u advertenties wilt maken.

   * *Algemeen:* voor advertenties zult u in andere DSPs creëren. **Nota:** u kunt [ extra macro&#39;s ](/help/creative/creative-macros.md) moeten manueel omvatten zonodig.

   * *Adobe AdCloud:* voor advertenties zult u in Advertising DSP creëren.

   * *Google CM360:* voor advertenties zult u in [!DNL Google Campaign Manager 360] creëren. **Nota:** u kunt [ extra macro&#39;s ](/help/creative/creative-macros.md) moeten manueel omvatten zonodig.

1. Klik op **[!UICONTROL Generate tags]**.

1. Kopieer of download de tags:

   * Om een markering voor één enkele advertentiegrootte te kopiëren, breid de markeringsrij uit, houd de curseur over de rij, en klik dan ![ Exemplaar ](/help/creative/assets/copy.png " ").**[!UICONTROL Copy]**<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->

   * Om alle geproduceerde markeringen als dossier aan de standaarddownloadplaats van uw browser te downloaden, klik ![ de markeringen van de Download ](/help/creative/assets/download.png " Codes van de Download ").

   U kunt het bestand openen in een teksteditor om elke tag te kopiëren. Voor JavaScript-tags wordt de tag ingesloten in `<script></script>` - en `<noscript></noscript>` -tags. Voor iframe-tags wordt de tag ingesloten in `<iframe></iframe>` -tags.

1. De labels voor de desbetreffende DSP implementeren:

   * Voor andere DSPs dan Advertising DSP, verstrek de markeringen aan wie de advertenties binnen DSP zal creëren.

   * Voor Advertising DSP:

      1. Klik op **[!UICONTROL Next]** in de rechterbovenhoek of klik op **[!UICONTROL DSP link]** in het linkermenu.

      1. Selecteer de campagne waarnaar u de advertentietag wilt uploaden.

      1. Klik op **[!UICONTROL Assign Tags]**.

         DSP wordt geopend in de [!UICONTROL Ads] -weergave voor de geselecteerde campagne.

      1. Reviseer in de [!UICONTROL Create ads] -weergave de advertentietags, selecteer elke tag waarvoor u een advertentie wilt maken en klik op **[!UICONTROL Create]** .

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
>* [ pas transcoderingsopties voor een video en ervaringstag aan ](experience-tag-video-transcoding.md)
