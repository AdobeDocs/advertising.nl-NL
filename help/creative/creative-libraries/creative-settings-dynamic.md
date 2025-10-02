---
title: Dynamische creatieve instellingen
description: Verwijs naar de instellingen voor dynamische creatieven.
feature: Creative Dynamic Creatives
source-git-commit: e7642f11503ebb972d23fe6d28020b3b198657b0
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# Dynamische creatieve instellingen

<!-- add a description -->

<!-- This looks the same for me for either HTML5 type as of 9/24:

## Dynamic ad settings for static HTML5 ads {#dynamic-ad-settings-static-html5}

### Basic Details

**[!UICONTROL Advertiser]:** The advertiser for which to create the ads.

**[!UICONTROL Library]:** The creative library in which to create the ads.

**[!UICONTROL Dynamic Ad Name]:** A unique name for the creative.

**[!UICONTROL Ad Template Size]:** The ad dimensions for the ad template from which to create the ad. If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template Type]:** The type of ad template from which to create the ad: *[!UICONTROL Static HTML5]* or *[!UICONTROL Dynamic HTML5]*.  If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template]:** The ad template from which to create the ad.

**[!UICONTROL clickURL]:** A valid landing page URL to which users are redirected when they click the ad.

### [!UICONTROL Attributes Details]

-->

## Dynamische advertentie-instellingen <!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Basic Details

**[!UICONTROL Dynamic Ad Name]:** Een unieke naam voor de creatieve.

**[!UICONTROL Advertiser]:** De adverteerder waarvoor de advertenties moeten worden gemaakt.

**[!UICONTROL Library]:** De creatieve bibliotheek waarin om de advertenties tot stand te brengen. Als u de advertenties maakt vanuit [!UICONTROL Creatives] > [!UICONTROL Creative Libraries] , is de bibliotheeknaam al geselecteerd en is deze alleen-lezen.

**[!UICONTROL Ad Template Size]:** de [ en afmetingen ](/help/creative/creative-libraries/creative-sizes.md) voor het advertentiesjabloon waarvan om de advertentie te creëren. Als u eerst een specifieke [!UICONTROL Ad Template] selecteert, wordt deze waarde automatisch geselecteerd.

## Advertentiesjabloon

**[!UICONTROL Ad Template]:** De advertentiesjabloon waaruit de advertenties moeten worden gemaakt. Selecteer een bestaand advertentiemalplaatje, of upload een nieuw advertentiemalplaatje en selecteer het malplaatjetype (*Statisch* of *Dynamisch*). Een geüploade sjabloon moet de ZIP-indeling hebben en HTML5-bestanden en het sjabloondefinitiebestand (template.TDF) bevatten. <!-- Need to add more specs for that -->

**[!UICONTROL Number of offers (Max 50)]:** Het aantal producten dat in een carrousel moet worden getoond.

## Catalogi

**[!UICONTROL Template]:** De voedermalplaatje aan gebruik om de advertenties tot stand te brengen.

**\ [Catalogi\]**: Één of meerdere catalogi waarvan om advertenties te produceren. Selecteer een bestaande catalogus of maak een nieuwe catalogus door een bestaande voedersjabloon te downloaden en de nieuwe catalogus te maken en te uploaden.

Geüploade catalogi moeten de ZIP-indeling hebben en het volgende bevatten:

* Een of meer feed-bestanden in de indeling CSV, TSV of Microsoft Excel-spreadsheet (XLSX). De maximale bestandsgrootte is 512 MB.<!-- Need to add more specs for the feed files -->

* Afbeeldingselementen in de GIF-, JPEG-, JPG- of PNG-indeling

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP --> de types van kolommen in het voederdossier waarvoor de waarden moeten aanwezig zijn om tot advertenties te leiden: *[!UICONTROL Profile data]*, * [!UICONTROL Geographic data], * [!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Nota:** Deze montages werken onafhankelijk van de geavanceerde montages in en ervaringsmontages.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Wijs elk kenmerk (dynamisch en veld) in de opgegeven advertentiesjabloon toe aan een kolom in de opgegeven catalogus (cataloguslabel) of voer een statische waarde in.

>[!MORELIKETHIS]
>
>* [ voeg dynamische creatieve creatieve bibliotheek ](creative-add-dynamic.md) toe
>* [ geef dynamische creatieve creatieve bibliotheek ](creative-edit-dynamic.md) uit
>* [ Werkstromen voor dynamische advertenties ](/help/creative/introduction/workflow-dynamic-ads.md)
