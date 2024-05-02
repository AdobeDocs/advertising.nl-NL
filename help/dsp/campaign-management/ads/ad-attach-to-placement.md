---
title: Advertenties toevoegen aan plaatsingen
description: Leer hoe u advertenties aan plaatsingen koppelt.
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
source-git-commit: 86acfaecdf761adc7c6585a49dbcdf4490290a8c
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# Advertenties toevoegen aan plaatsingen

Gebruik de [!UICONTROL Ad Tools] om advertenties aan plaatsingen te koppelen, pixels voor tekstspatiëring van derden aan de advertenties te koppelen en bestaande pixels voor tekstspatiëring van derden los te koppelen van de advertenties.

>[!NOTE]
>
>Universele video-advertenties kunnen alleen worden gekoppeld aan universele video-opnamen.

## Open de [!UICONTROL Ad Tools] Weergave {#ad-tools-open}

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

1. Klik op de naam van de campagne.

1. Open de [!UICONTROL Ad Tools] op een van de volgende manieren te bekijken:

   * (Vanaf de [!UICONTROL Packages] , [!UICONTROL Placements], of [!UICONTROL Ads] weergave) Klik in de rechterbovenhoek op **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

   * (Vanaf de [!UICONTROL Placements] (weergave) Naast de plaatsingsnaam klikt u op **[!UICONTROL ...]** > **[!UICONTROL Attach Ads].**

   * (Vanaf de [!UICONTROL Ads] (weergave) Naast de naam van de advertentie klikt u op  **[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**.

   De [!UICONTROL Attach Ads] is standaard geselecteerd.

## Advertenties toevoegen aan plaatsingen {#attach-ads-campaign}

1. [Open de [!UICONTROL Ad Tools] weergave](#ad-tools-open).

1. In de [!UICONTROL Edit] Ga als volgt te werk voor elke groep advertenties die u aan plaatsingen wilt koppelen:

   1. (Optioneel) Zoek op een van de volgende manieren specifieke plaatsen en advertenties:

      * Klik boven de linkertabel op ![Filter](/help/dsp/assets/filter.png) en filtert de lijsten op pakket, plaatsingstype, plaatsingsstatus, en type, of advertentiestatus.

      * Zoek boven de tabellen rechts en links naar specifieke tekstreeksen in de plaatsings- en advertentienamen.

   1. Schakel in de linkertabel het selectievakje in naast elke plaatsing waaraan u de advertenties wilt koppelen.

   1. Selecteer in de rechtertabel het selectievakje naast elke advertentie die u aan de geselecteerde plaatsingen wilt koppelen.

      Alleen advertenties die van toepassing zijn op het plaatsingstype en die nog niet aan de geselecteerde plaatsingen zijn gekoppeld, kunnen worden geselecteerd.

   1. Klik in de rechteronderhoek op **[!UICONTROL Attach]**.

1. (Optioneel) Klik op ![Terug naar map](/help/dsp/assets/breadcrumb-return.png "Terug naar map") links van [!UICONTROL Ad Tools] en selecteert u de naam van de campagne.

## Advertenties weergeven die zijn gekoppeld aan plaatsingen {#view-ads-campaign}

<!-- should be a separate page, combined with "List the Placements Associated with an Ad" (although that pertains to a single ad only), or maybe just rename this topic -->

1. [Open de [!UICONTROL Ad Tools] weergave](#ad-tools-open).

1. Schakel over naar de **[!UICONTROL View]** rechtsboven.

1. (Optioneel) Zoek zo nodig specifieke plaatsen en advertenties:

   * Klik boven de linkertabel op ![Filter](/help/dsp/assets/filter.png) en filtert de lijsten op pakket, plaatsingstype, plaatsingsstatus, en type, of advertentiestatus.

   * Zoek in de rechter- en linkertabellen naar specifieke tekstreeksen in de plaatsings- of advertentienaam.

1. Klik op een plaatsingsrij in de linkertabel om de bijgevoegde advertenties in de rechtertabel weer te geven.

1. (Optioneel) Als u meer advertenties wilt toevoegen aan de plaatsing van de campagne, schakelt u over op de knop **[!UICONTROL Edit]** in de rechterbovenhoek. Zie Stap 2 in de vorige procedure, &quot;[Advertenties toevoegen aan plaatsingen](#attach-ads-campaign),&quot; voor instructies.

## Pixels van derden bijvoegen bij advertenties in een plaatsing {#attach-pixels-ads}

1. [Open de [!UICONTROL Ad Tools] weergave](#ad-tools-open).

1. Klik op de knop **[!UICONTROL Attach Pixels]** tab.

1. In de [!UICONTROL Edit] subweergave:

   1. (Optioneel) Zoek op de volgende manieren advertenties en pixels van derden:

      * Klik boven de linkertabel op ![Filter](/help/dsp/assets/filter.png) en filtert u de lijsten op advertentiestatus, advertentietype, gebeurtenis voor pixelintegratie of pixeltype.

      * Zoek boven de linker- en rechtertabellen naar specifieke tekstreeksen in de namen van advertenties en pixels.

   1. (Als er geen pixels voor het bijhouden van derden voor de campagne bestaan) Maak een pixel:

      1. Klik in de rechtertabel op **[!UICONTROL Create pixel]**.

      1. Geef de instellingen op:

         **[!UICONTROL Integration Event]:** De gebeurtenis die de pixel activeert, zoals *[!UICONTROL Impression]* of *[!UICONTROL Click-through]*.

         **[!UICONTROL Pixel Type]:** Of de pixel een *[!UICONTROL IMG URL]* (afbeeldingsbestand van 1 x 1 pixel), *[!UICONTROL HTML]*, of *[!UICONTROL JavaScript URL]*.

         **[!UICONTROL Pixel URL or Code]:** De URL van de pixelafbeelding, in de juiste indeling voor het opgegeven pixeltype.

         **[!UICONTROL Pixel Name]:** De pixelnaam. Gebruik een naam waarmee u de pixel gemakkelijk kunt herkennen.

         **[!UICONTROL Pixel Provider]:** De pixelprovider: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, of *[!UICONTROL IAS]*.

      1. Klik op **[!UICONTROL Save]**.

   1. Schakel in de linkertabel het selectievakje in naast elke advertentie waarvoor u pixels voor het bijhouden van derden wilt toevoegen.

   1. Schakel in de rechtertabel het selectievakje in naast elke pixel van derden die u wilt koppelen aan de geselecteerde advertenties.

      Alleen pixels die nog niet aan de geselecteerde advertenties zijn gekoppeld, kunnen worden geselecteerd.

   1. Klik in de rechteronderhoek op **[!UICONTROL Attach]**.

1. (Optioneel) Klik op ![Terug naar map](/help/dsp/assets/breadcrumb-return.png "Terug naar map") links van [!UICONTROL Ad Tools] en selecteert u de naam van de campagne.

## Pixels van derden loskoppelen van advertenties in een plaatsing {#detach-pixels-ads}

1. [Open de [!UICONTROL Ad Tools] weergave](#ad-tools-open).

1. Klik op de knop **[!UICONTROL Attach Pixels]** tab.

1. In de [!UICONTROL Edit] subweergave:

   1. (Optioneel) Zoek op de volgende manieren advertenties en pixels van derden:

      * Klik boven de linkertabel op ![Filter](/help/dsp/assets/filter.png) en filtert u de lijsten op advertentiestatus, advertentietype, gebeurtenis voor pixelintegratie of pixeltype.

      * Zoek boven de linker- en rechtertabellen naar specifieke tekstreeksen in de namen van advertenties en pixels.

   1. Schakel in de linkertabel het selectievakje in naast elke advertentie waarvan u pixels voor het bijhouden van derden wilt loskoppelen.

   1. Schakel in de rechtertabel het selectievakje in naast de pixels die u wilt loskoppelen van de geselecteerde advertenties.

      Alleen pixels die aan alle geselecteerde advertenties zijn gekoppeld, kunnen worden geselecteerd.

   1. Klik in de rechteronderhoek op **[!UICONTROL Detach]**.

1. (Optioneel) Klik op ![Terug naar map](/help/dsp/assets/breadcrumb-return.png "Terug naar map") links van [!UICONTROL Ad Tools] en selecteert u de naam van de campagne.

## Pixels weergeven die zijn gekoppeld aan advertenties {#view-pixels-ads}

1. [Open de [!UICONTROL Ad Tools] weergave](#ad-tools-open).

1. Klik op de knop **[!UICONTROL Attach Pixels]** tab.

1. Schakel over naar de **[!UICONTROL View]** rechtsboven.

1. (Optioneel) Zoek zo nodig advertenties en pixels van derden:

   * Klik boven de linkertabel op ![Filter](/help/dsp/assets/filter.png) en filtert u de lijsten op advertentiestatus, advertentietype, gebeurtenis voor pixelintegratie of pixeltype.

   * Zoek boven de linker- en rechtertabellen naar specifieke tekstreeksen in de namen van advertenties en pixels.

1. Klik op een willekeurige advertentierij in de linkertabel om de gekoppelde pixels in de rechtertabel weer te geven.

1. (Optioneel) Als u meer pixels aan de advertenties wilt koppelen, schakelt u over naar de **[!UICONTROL Edit]** in de rechterbovenhoek. Zie Stap 3 in de vorige procedure. &quot;[Pixels van derden bijvoegen bij advertenties in een plaatsing](#attach-pixels-ads),&quot; voor instructies.

>[!MORELIKETHIS]
>
>* [Over Advertentiebeheer](ad-about.md)
>* [Eén advertentie maken](ad-create.md)
>* [Meerdere externe advertenties maken](ad-create-multiple.md)
>* [Een advertentie bewerken](ad-edit.md)
>* [De aan een advertentie gekoppelde plaatsen weergeven](ad-list-placements.md)
>* [Advertentieschema&#39;s voor plaatsingen bewerken](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [Veelgestelde vragen over Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
