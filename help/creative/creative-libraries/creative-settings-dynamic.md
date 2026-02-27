---
title: Dynamische creatieve instellingen
description: Verwijs naar de instellingen voor dynamische creatieven.
feature: Creative Dynamic Creatives
exl-id: 9dcd7245-fa02-4082-9abb-8c0792322a68
source-git-commit: 164ee92f85c0e649dc2bd6c0224a531eb72d1962
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Dynamische creatieve instellingen

<!-- add a description -->

## Dynamische advertentie-instellingen <!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Basic Details

**[!UICONTROL Creative Type]:** Of creatief een *[!UICONTROL Display]* advertentie (HTML5) of een *[!UICONTROL Video]* advertentie is.

**[!UICONTROL Dynamic Display Ad Name]** of **[!UICONTROL Dynamic Video Ad Name]:** Een unieke naam voor creatief.

**[!UICONTROL Advertiser]:** De adverteerder waarvoor de advertenties moeten worden gemaakt. Als u de advertenties maakt vanuit [!UICONTROL Creatives] > [!UICONTROL Creative Libraries] , is de adverteerder al geselecteerd en is deze alleen-lezen.

**[!UICONTROL Library]:** De creatieve bibliotheek waarin om de advertenties tot stand te brengen. Als u de advertenties maakt vanuit [!UICONTROL Creatives] > [!UICONTROL Creative Libraries] , is de bibliotheeknaam al geselecteerd en is deze alleen-lezen.

## Advertentiesjabloon

**[!UICONTROL Ad Template]:** De advertentiesjabloon waaruit de advertenties moeten worden gemaakt. Selecteer een bestaand advertentiemalplaatje, of upload een nieuw advertentiemalplaatje en selecteer het malplaatjetype (*Statisch* of *Dynamisch*). De sjabloon moet de ZIP-indeling hebben en het volgende bevatten:<!-- Need to add more specs for templates -->

* Creatief weergeven: HTML5-bestanden met de gewenste advertentievorm en (alleen dynamische HTML5-advertenties) een bestand met de advertentiekenmerken (.tdf)

* Videoontwerpers: Een scènebestand met de gewenste advertentievorm. Het ZIP-bestand kan maximaal 512 MB groot zijn.

Klik op **[!UICONTROL Select Ad Template]** om door te gaan.

**[!UICONTROL Size]:** (Dynamische vertoningsadvertenties slechts; read-only) [&#x200B; en afmetingen &#x200B;](/help/creative/creative-libraries/creative-sizes.md) voor het geselecteerde advertentiemalplaatje, dat wordt gebruikt om tot de advertenties te leiden.

**[!UICONTROL Card Count (Max 50)]:** (Alleen advertenties weergeven) Het aantal producten dat in een carrousel moet worden weergegeven.

**[!UICONTROL Duration]:** (Alleen videolagen; alleen-lezen) De videoduur die is afgeleid van de geselecteerde advertentiesjabloon. De duur van elke video moet tussen 1 en 90 seconden liggen.

## Catalogi

**\ [Catalogi\]**: Één of meerdere catalogi waarvan om advertenties te produceren. Selecteer een bestaande catalogus of maak een nieuwe catalogus door een bestaande voedersjabloon te downloaden en de nieuwe catalogus te maken en te uploaden. Klik op **[!UICONTROL Select Catalog]**.

Geüploade catalogi moeten de ZIP-indeling hebben en het volgende bevatten:

* (Dynamische weergave- en videoadvertenties) Een of meer feed-bestanden in de indeling CSV, TSV of Microsoft Excel-spreadsheet (XLSX). De maximale bestandsgrootte is 512 MB.<!-- Need to add more specs for the feed files -->

* (Advertenties weergeven) Afbeeldingselementen in GIF-, JPEG-, JPG- of PNG-indeling

* (Videoadvertenties) Video-elementen in MP4-, MOV- of WEBM-indeling. Tot de ondersteunde advertentiesjablonen behoren startkaart, eindkaart, overlay bovenaan, bedekking onderaan of L-vormig. De duur van elke video moet tussen 1 en 90 seconden liggen.

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP --> de types van kolommen in het voederdossier waarvoor de waarden moeten aanwezig zijn om tot advertenties te leiden: *[!UICONTROL Profile data]*, * [!UICONTROL Geographic data], * [!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Nota:** Deze montages werken onafhankelijk van de geavanceerde montages in en ervaringsmontages.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Wijs elk kenmerk (dynamisch en veld) in de opgegeven advertentiesjabloon toe aan een kolom in de opgegeven catalogus (cataloguslabel) of voer een statische waarde in.

>[!MORELIKETHIS]
>
>* [&#x200B; voeg dynamische creatieve creatieve bibliotheek &#x200B;](creative-add-dynamic.md) toe
>* [&#x200B; geef dynamische creatieve creatieve bibliotheek &#x200B;](creative-edit-dynamic.md) uit
>* [&#x200B; Werkstromen voor dynamische advertenties &#x200B;](/help/creative/introduction/workflow-dynamic-ads.md)
