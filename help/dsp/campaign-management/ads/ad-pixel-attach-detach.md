---
title: Pixels koppelen aan en verwijderen uit advertenties
description: Leer hoe u pixels die van derden worden bijgehouden, kunt toevoegen aan of verwijderen uit advertenties.
feature: DSP Ads
source-git-commit: a3bd04da6c6f428fdb6e1f05187ea3de0174c9d7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# Pixels koppelen aan en verwijderen uit advertenties

U kunt pixels die van derden worden bijgehouden, aan advertenties koppelen en van elkaar scheiden.

## De weergave van [!UICONTROL Ad Tools] openen {#ad-tools-open}

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik op de naam van de campagne.

1. Open de weergave [!UICONTROL Ad Tools] op een van de volgende manieren:

   * (In de [!UICONTROL Campaigns] weergave) Klik naast de naam van de campagne op **[!UICONTROL ...]** > **[!UICONTROL Ad Tools].**

   * (Klik in de weergave [!UICONTROL Packages] , [!UICONTROL Placements] of [!UICONTROL Ads] rechtsboven op **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]** .

## Pixels van derden bijvoegen bij advertenties in een plaatsing {#attach-pixels-ads}

1. [&#x200B; open de [!UICONTROL Ad Tools] mening &#x200B;](#ad-tools-open).

   Het tabblad **[!UICONTROL Attach Pixels]** wordt geopend.

1. In de subweergave [!UICONTROL Edit] :

   1. (Optioneel) Zoek op de volgende manieren advertenties en pixels van derden:

      * Boven de linkerlijst, klik ![&#x200B; Filter &#x200B;](/help/dsp/assets/filter.png) en filter de lijsten door ad status, ad type, pixel integratiegebeurtenis, of pixeltype.

      * Zoek boven de linker- en rechtertabellen naar specifieke tekstreeksen in de namen van advertenties en pixels.

   1. (Als er geen pixels voor het bijhouden van derden voor de campagne bestaan) Maak een pixel:

      1. Klik in de rechtertabel op **[!UICONTROL Create pixel]** .

      1. Geef de instellingen op:

         **[!UICONTROL Integration Event]:** De gebeurtenis die de pixel activeert, zoals *[!UICONTROL Impression]* of *[!UICONTROL Click-through]* .

         **[!UICONTROL Pixel Type]:** Of de pixel een *[!UICONTROL IMG URL]* (1x1 pixelafbeeldingsbestand), *[!UICONTROL HTML]* of *[!UICONTROL JavaScript URL]* is.

         **[!UICONTROL Pixel URL or Code]:** De URL van het pixelbeeld, in het aangewezen formaat voor het gespecificeerde Type van Pixel.

         **[!UICONTROL Pixel Name]:** De pixelnaam. Gebruik een naam waarmee u de pixel gemakkelijk kunt herkennen.

         **[!UICONTROL Pixel Provider]:** De pixelprovider: *[!UICONTROL None]* , *[!UICONTROL Comscore]* , *[!UICONTROL WhiteOps]* of *[!UICONTROL IAS]* .

      1. Klik op **[!UICONTROL Save]**.

   1. Schakel in de linkertabel het selectievakje in naast elke advertentie waarvoor u pixels voor het bijhouden van derden wilt toevoegen.

   1. Schakel in de rechtertabel het selectievakje in naast elke pixel van derden die u wilt koppelen aan de geselecteerde advertenties.

      Alleen pixels die nog niet aan de geselecteerde advertenties zijn gekoppeld, kunnen worden geselecteerd.

   1. Klik in de rechterbenedenhoek op **[!UICONTROL Attach]** .

1. (Facultatief) om op de meningen van het campagnedetail terug te keren, klik ![&#x200B; Terugkeer aan omslag &#x200B;](/help/dsp/assets/breadcrumb-return.png " Terugkeer aan omslag ") links van [!UICONTROL Ad Tools] en selecteer de campagnenaam.

## Pixels van derden loskoppelen van advertenties in een plaatsing {#detach-pixels-ads}

1. [&#x200B; open de [!UICONTROL Ad Tools] mening &#x200B;](#ad-tools-open).

   Het tabblad **[!UICONTROL Attach Pixels]** wordt geopend.

1. In de subweergave [!UICONTROL Edit] :

   1. (Optioneel) Zoek op de volgende manieren advertenties en pixels van derden:

      * Boven de linkerlijst, klik ![&#x200B; Filter &#x200B;](/help/dsp/assets/filter.png) en filter de lijsten door ad status, ad type, pixel integratiegebeurtenis, of pixeltype.

      * Zoek boven de linker- en rechtertabellen naar specifieke tekstreeksen in de namen van advertenties en pixels.

   1. Schakel in de linkertabel het selectievakje in naast elke advertentie waarvan u pixels voor het bijhouden van derden wilt loskoppelen.

   1. Schakel in de rechtertabel het selectievakje in naast de pixels die u wilt loskoppelen van de geselecteerde advertenties.

      Alleen pixels die aan alle geselecteerde advertenties zijn gekoppeld, kunnen worden geselecteerd.

   1. Klik in de rechterbenedenhoek op **[!UICONTROL Detach]** .

1. (Facultatief) om op de meningen van het campagnedetail terug te keren, klik ![&#x200B; Terugkeer aan omslag &#x200B;](/help/dsp/assets/breadcrumb-return.png " Terugkeer aan omslag ") links van [!UICONTROL Ad Tools] en selecteer de campagnenaam.

## Pixels weergeven die zijn gekoppeld aan advertenties {#view-pixels-ads}

1. [&#x200B; open de [!UICONTROL Ad Tools] mening &#x200B;](#ad-tools-open).

   Het tabblad **[!UICONTROL Attach Pixels]** wordt geopend.

1. Schakel over naar de optie **[!UICONTROL View]** rechtsboven.

1. (Optioneel) Zoek zo nodig advertenties en pixels van derden:

   * Boven de linkerlijst, klik ![&#x200B; Filter &#x200B;](/help/dsp/assets/filter.png) en filter de lijsten door ad status, ad type, pixel integratiegebeurtenis, of pixeltype.

   * Zoek boven de linker- en rechtertabellen naar specifieke tekstreeksen in de namen van advertenties en pixels.

1. Klik op een willekeurige advertentierij in de linkertabel om de gekoppelde pixels in de rechtertabel weer te geven.

1. (Optioneel) Als u meer pixels aan de advertenties wilt koppelen, schakelt u over naar de weergave **[!UICONTROL Edit]** in de rechterbovenhoek. Zie Stap 3 in de vorige procedure, &quot;[&#x200B; het Volgen Pixels van de Derde aan Ads in een Plaatsing &#x200B;](#attach-pixels-ads) vastmaken,&quot;voor instructies.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer Advertentiebeheer &#x200B;](ad-about.md)
>* [&#x200B; Advertenties aan Plaatsingen &#x200B;](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) vastmaken
>* [&#x200B; creeer Één enkele Advertentie &#x200B;](ad-create.md)
>* [&#x200B; creeer Veelvoudige Derde Advertenties &#x200B;](ad-create-multiple.md)
>* [&#x200B; geef een Advertentie uit &#x200B;](ad-edit.md)
>* [&#x200B; maak een lijst van de Plaatsen verbonden aan een Advertentie &#x200B;](ad-list-placements.md)
>* [&#x200B; geef de Advertentieschema&#39;s voor Plaatsen uit &#x200B;](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [&#x200B; Veelgestelde vragen over Universele Video &#x200B;](/help/dsp/campaign-management/faq-universal-video.md)

