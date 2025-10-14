---
title: Instellingen van Campagne-componenten controleren en bewerken met behulp van bulksbladen
description: Leer hoe u sleutelpakket-, plaatsings- en advertentie-instellingen bulksgewijs kunt bekijken en bewerken met behulp van spreadsheets.
feature: DSP Placements
exl-id: 1ec8362a-d37b-4fd7-becd-3a5b4f0c9504
source-git-commit: 18c68edec80a80d236df138c05fba8d857c9ed9e
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 0%

---

# Instellingen van Campagne-componenten controleren en bewerken met behulp van bulksbladen

U kunt de instellingen voor de pakketten, plaatsingen en advertenties in één campagne downloaden in de XLSX-indeling ([!DNL Microsoft Excel] spreadsheet) om de instellingen te bekijken en te bewerken. Door gebrek, omvat het gedownloade dossier, genoemd a *bulksheet,* afzonderlijke lusjes voor pakketmontages, de informatie van de pakketvlucht, plaatsingsmontages, en plaatsing en programma&#39;s. U kunt de instellingen voor bepaalde typen campagnecomponenten optioneel uitsluiten.

Als u meerdere instellingen tegelijk wilt bijwerken, uploadt u een geldig bulksheet-bestand met de wijzigingen. Als u het werkblad wilt maken, bewerkt u een gedownload werkblad met de bestaande instellingen. Bewerkbare velden bevatten de meeste instellingen die normaal gesproken bewerkbaar zijn. Velden voor instellingen die niet worden gebruikt, bevatten lege waarden.

>[!NOTE]
>
>U kunt ook de instellingen voor alleen specifieke pakketten en specifieke plaatsingen downloaden en bewerken. Zie &quot;[&#x200B; Overzicht en geef de Montages van het Pakket uit Gebruikend Bulksheets &#x200B;](/help/dsp/campaign-management/packages/package-qa.md)&quot;en &quot;[&#x200B; Overzicht en geef de Montages van de Plaatsing Gebruikend Bulksheets &#x200B;](/help/dsp/campaign-management/placements/placement-qa.md) uit.&quot;

## Downloadinstellingen voor pakketten, plaatsingen en advertenties in een campagne {#download-bulksheet-campaign}

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Voer een van de volgende handelingen uit:

   * Klik naast de campagne op **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]** .

   * Klik op de naam van de campagne. Klik in de rechterbovenhoek op **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]** .

1. Hef in het dialoogvenster [!UICONTROL Bulksheet Download] de selectie op van de campagnecomponenten waarvan u de instellingen wilt uitsluiten van het gedownloade bestand en klik vervolgens op **[!UICONTROL Download]** .

Standaard zijn instellingen voor alle campagnecomponenten geselecteerd.

Een bericht geeft aan wanneer het bestand beschikbaar is om te downloaden.

1. Voer een van de volgende twee handelingen uit om het bestand te downloaden:

   * Klik in het meldingsbericht op **[!UICONTROL Download].**

   * In het recht van de hoogste menubar, klik ![&#x200B; Banen &#x200B;](/help/dsp/assets/downloads.png). Klik op **[!UICONTROL Download]** naast de taak.

     Het bestand wordt opgeslagen in de map Downloads van de browser.<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

     Als u een van de instellingen wilt bewerken, bewerkt u het bestand rechtstreeks en uploadt u de wijzigingen. Alle bewerkbare kolommen worden gemarkeerd in blauw. Als u de juiste indeling voor een veld wilt gebruiken, selecteert en kopieert u de waarde uit de relevante pakketinstelling of plaatsingsinstelling. Voor sommige doelinstellingen, zoals dagpartering, aangepaste doelen en conversiemetriek, is een kopieeroptie beschikbaar binnen de instelling.

     >[!NOTE]
     >
     >Voor sommige doelinstellingen worden alle opties standaard ingesteld, tenzij u de selectie beperkt tot specifieke doelen. Wanneer u de doelen niet hebt verkleind, is het veld voor de opsommingstekens leeg, wat betekent dat alle opties als doel zijn ingesteld.

## Upload een Bulksheet met de Montages van het Pakket, van de Plaatsing, en van de Advertentie voor een Campagne{#upload-bulksheet-campaign-components}

Upload instellingen voor pakketten, plaatsen en advertenties in één campagne allemaal tegelijk in een gevuld bulksheet.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Voer een van de volgende handelingen uit:

   * Klik naast de campagne op **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]** .

   * Klik op de naam van de campagne. Klik in de rechterbovenhoek op **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]** .

1. In het dialoogvenster [!UICONTROL Upload Bulksheet] :

   1. Sleep een bestand naar het vak of klik in het vak om een bestand van het apparaat of het netwerk te selecteren.

   1. Klik op **[!UICONTROL Upload]**.

1. (Facultatief) om te verifiëren dat de updates werden verwerkt, klik ![&#x200B; Banen &#x200B;](/help/dsp/assets/downloads.png) in het recht van de hoogste menubar.

Wanneer een instellingsupdate mislukt, kunt u een foutbestand voor een bulksheet met kleurcodering downloaden om te tonen welke instellingen (rijen) zijn opgeslagen en welke zijn mislukt, met een reden voor elke fout. Vervolgens kunt u de problemen in hetzelfde bestand verhelpen en het bestand opnieuw uploaden om de gecorrigeerde gegevens te verwerken.


<!--
## Placement Setting Columns in Downloaded/Uploaded Spreadsheets{#qa-sheet-columns}

>[!TIP]
>
> In a downloaded spreadsheet, all editable columns are highlighted in blue.

### Campaign-level Spreadsheets

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | The name of the placement. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Any applied labels, for reporting. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | A link to open the placement in Edit mode. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Status] | The placement status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | The placement type. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | The name of the parent package, when applicable. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | The start date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL End Date] | The end date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Whether dayparting is *[!UICONTROL ON]* or *[!UICONTROL OFF]*.<br><b>Note:</b> To check the actual dayparting schedule, open the placement settings in DSP. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Budget] | The placement budget, if there is one. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | The objective of the package. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | The target value of the goal. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Whether the placement is pacing towards the *[!UICONTROL Budget]* or *[!UICONTROL Impressions]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | The maximum bid for the placement. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the placement: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the placement: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Any pre-bid filter criteria to be applied. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Whether bidding rules (deprecated) are *[!UICONTROL ON]* or *[!UICONTROL OFF]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | The primary frequency cap for the placement during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the placement during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | The number of targeted geographical locations, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | The targeted geographical locations, separated by semi-colons,or *[!UICONTROL All Locations]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | The number of excluded geographical locations or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | The excluded geographical locations, separated by semi-colons,  or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | The number of targeted public inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | The number of excluded public inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | The number of targeted private inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | The number of excluded private inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | The number of targeted [!UICONTROL On-Demand Inventory] deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | The number of excluded On-Demand Inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | The targeted type of traffic: *[!UICONTROL Website]* and/or *[!UICONTROL Apps]* | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | The quality of the sites to target: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*, or *[!UICONTROL All Sites]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | The number of targeted site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | The number of excluded site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | The excluded sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Language] | The targeted site languages. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Standard display placements only) Whether or not to allow ad delivery on non-audited sites: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. When the placement targets private inventory, this option may deliver ads on blocked sites. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | The number of targeted sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | The targeted audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | The excluded audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Whether or not [!DNL Comscore] demographic segments are enabled for the placement (and other placements in the campaign): *[!UICONTROL ON]* or *[!UICONTROL OFF]*. This feature may be enabled only for campaigns for which the [!DNL Audience Verification] feature is enabled for [!DNL Nielsen] and/or [!DNL Comscore].  It incurs additional fees.  | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Whether or not to extend the ad targeting across devices: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Included # | The number of targeted topic codes, if any are specified, or *[!UICONTROL All]*.   | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | The number of excluded topic codes, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | The number of targeted device targets, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | The number of excluded device targets, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | The number of targeted ISP providers, if any are specified, or *[!UICONTROL All]/i>. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | The number of excluded ISP providers, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | The number of brand safety filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | The number of pre-bid fraud blocking filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | The number of pre-bid viewability filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Whether or not Site Safety Block is enabled: *[!UICONTROL ON]* or *[!UICONTROL OFF]*.[Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don't see this option at the placement level. Should there be one?] | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | The number of third-party  event-tracking pixels attached to the placement, or *[!UICONTROL None]*.| &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | The number of conversion tracking pixels attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | The number of ads attached to the placement, if any are attached, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | The names of any ads attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | The unique DSP-generated Ad IDs of any ads attached to the placement, separated by semi-colons. To download a list of ad names and associated Ad IDs from the [!UICONTROL Ads] view, create a custom view that includes the [!UICONTROL Ad ID] metric, and then [export the data](/help/dsp/campaign-management/reports/campaign-export-data.md). | Yes |
-->

>[!MORELIKETHIS]
>
>* [&#x200B; Overzicht en geef de Montages van het Pakket uit Gebruikend Bulksheets &#x200B;](/help/dsp/campaign-management/packages/package-qa.md)
>* [&#x200B; de Montages van het Pakket &#x200B;](/help/dsp/campaign-management/packages/package-settings.md)
>* [&#x200B; Overzicht en geeft de Montages van de Plaatsing Gebruikend Bulksheets uit &#x200B;](/help/dsp/campaign-management/placements/placement-qa.md)
>* [&#x200B; Montages van de Plaatsing &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)
>* [&#x200B; Audio Advertentie Montages &#x200B;](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [&#x200B; Verbonden de Montages van TV &#x200B;](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [&#x200B; Vertoning en Montages &#x200B;](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [&#x200B; Mobiele Advertentie Montages &#x200B;](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [&#x200B; Inheemse Montages van de Vertoning &#x200B;](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [&#x200B; pre-rol en Montages &#x200B;](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [&#x200B; Universele Video en Montages &#x200B;](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
