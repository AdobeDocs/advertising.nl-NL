---
title: Instellingen van Campagne-componenten controleren en bewerken met behulp van bulksbladen
description: Leer hoe u sleutelpakket-, plaatsings- en advertentie-instellingen bulksgewijs kunt bekijken en bewerken met behulp van spreadsheets.
feature: DSP Placements
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 0%

---

# Instellingen van Campagne-componenten controleren en bewerken met behulp van bulksbladen

<!-- Update headers as needed once the original download become editable and we call everything bulksheets. -->

U kunt de instellingen voor de pakketten, plaatsen en advertenties in één campagne downloaden in de XLSX-indeling ([!DNL Microsoft Excel] spreadsheet) voor revisie. Standaard bevat het gedownloade bestand afzonderlijke tabbladen voor pakketinstellingen, vluchtinformatie voor pakketten, plaatsingsinstellingen en plaatsings- en planningen. U kunt de instellingen voor bepaalde typen campagnecomponenten optioneel uitsluiten.

Als u meerdere instellingen tegelijk wilt bijwerken, uploadt u een geldig bulksheet-bestand met de wijzigingen. Om het bulksblad tot stand te brengen, kunt u een leeg malplaatje downloaden bulksheet dat lusjes voor elk type van campagnecomponent omvat, nieuwe of bijgewerkte montages in het malplaatjedossier ingaan of kleven, en dan sparen het dossier om het te uploaden. Bewerkbare velden bevatten de meeste instellingen die normaal gesproken bewerkbaar zijn.

>[!NOTE]
>
>U kunt ook de instellingen voor alleen specifieke pakketten en specifieke plaatsingen downloaden en bewerken. Zie &quot;[ Overzicht en geef de Montages van het Pakket uit Gebruikend Bulksheets ](/help/dsp/campaign-management/packages/package-qa.md)&quot;en &quot;[ Overzicht en geef de Montages van de Plaatsing Gebruikend Bulksheets ](/help/dsp/campaign-management/placements/placement-qa.md) uit.&quot;

## Downloadinstellingen voor pakketten, plaatsingen en advertenties in een campagne

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik rechtsboven op **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]** .

1. Hef in het dialoogvenster [!UICONTROL QA Sheet Download] de selectie op van de campagnecomponenten waarvan u de instellingen wilt uitsluiten van het gedownloade bestand en klik vervolgens op **[!UICONTROL Download]** .

Standaard zijn instellingen voor alle campagnecomponenten geselecteerd.

Een bericht geeft aan wanneer het bestand beschikbaar is om te downloaden.

1. Voer een van de volgende twee handelingen uit om het bestand te downloaden:

   * Klik in het meldingsbericht op **[!UICONTROL Download].**

   * In het recht van de hoogste menubar, klik ![ Banen ](/help/dsp/assets/downloads.png). Klik op **[!UICONTROL Download]** naast de taak.

     Het bestand wordt opgeslagen in de map Downloads van de browser. Zie &quot;[ de Kolommen van de Plaatsing in Gedownloade/Geüploade Spreadsheets ](#qa-sheet-columns)&quot;voor een lijst van de inbegrepen kolommen.

>[!NOTE]
>
>U kunt QA-bestanden op campagneniveau niet bewerken en opnieuw uploaden. Om veranderingen in de montages van de campagnecomponent in deze dossiers aan te brengen, [ download een afzonderlijk dossier van het montagesmalplaatje (opstellingsdossier) ](#download-template), ga of plak rijen van het dossier QA in het malplaatje in en bewaar het dossier, en dan [ upload het bevolkte malplaatjedossier ](#upload-bulksheet-campaign-components).

## Een bladsjabloon voor een campagne downloaden {#download-template}

Download een leeg bulksheet malplaatje dat lusjes voor elk type van campagnecomponent omvat. U kunt rijen aan om het even welk lusje op het malplaatje later toevoegen en [ uploadt het uitgegeven dossier ](##upload-bulksheet-campaign-components) om veranderingen in de campagnecomponenten aan te brengen.

1. Klik op de naam van de campagne.

1. Klik in de rechterbovenhoek op **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]** .

1. Klik in het dialoogvenster [!UICONTROL Upload Bulksheet] op **[!UICONTROL Bulksheet Template].**

   Het bestand wordt opgeslagen in de map Downloads van de browser. Zie &quot;[ de Kolommen van de Plaatsing in Gedownloade/Geüploade Spreadsheets ](#qa-sheet-columns)&quot;voor een lijst van de inbegrepen kolommen.

## Upload een Bulksheet met de Montages van het Pakket, van de Plaatsing, en van de Advertentie voor een Campagne{#upload-bulksheet-campaign-components}

Upload instellingen voor pakketten, plaatsen en advertenties in één campagne allemaal tegelijk in een gevuld bulksheet.

1. [ Download een bulksheet malplaatje ](#download-template) indien nodig, ga of deeg pakket, plaatsing, en/of advertentiemontages op de relevante lusjes van een bulksheet malplaatje in, en bewaar dan het dossier aan uw apparaat of netwerk.

   Zie de beschikbare instellingen hieronder.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik op de naam van de campagne.

1. Klik in de rechterbovenhoek op **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]** .

1. In het dialoogvenster [!UICONTROL Upload Bulksheet] :

   1. Sleep een bestand naar het vak of klik in het vak om een bestand van het apparaat of het netwerk te selecteren.

   1. Klik op **[!UICONTROL Upload]**.

1. (Facultatief) om te verifiëren dat de updates werden verwerkt, klik ![ Banen ](/help/dsp/assets/downloads.png) in het recht van de hoogste menubar.

## Plaatsingsinstellingskolommen in gedownloade/geüploade spreadsheets{#qa-sheet-columns}

>[!TIP]
>
> In een gedownload werkblad worden alle bewerkbare kolommen in blauw gemarkeerd.

### Spreadsheets op campagneniveau

| Sectie | Kolom | Beschrijving | Bewerkbaar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | De numerieke id van de plaatsing. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | De naam van de plaatsing. | Ja |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Alle toegepaste labels voor rapportage. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Een koppeling om de plaatsing te openen in de modus Bewerken. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | De plaatsingsstatus: *[!UICONTROL active]* of *[!UICONTROL inactive]* . | Ja |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | Het plaatsingstype. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | De naam van het bovenliggende pakket, indien van toepassing. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | De begindatum van de plaatsing. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | De einddatum van de plaatsing. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Bepaalt of zomertijd *[!UICONTROL ON]* of *[!UICONTROL OFF]* is.<br><b> Nota:</b> om het daadwerkelijke dagparting programma te controleren, open de plaatsingsmontages in DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | Het budget voor plaatsing, als dat er is. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | Het budgetinterval: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* of *[!UICONTROL All Time]* . | Ja |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | Het doel van het pakket. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | De doelwaarde van het doel. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Geeft aan of de plaatsing in de richting van de *[!UICONTROL Budget]* of *[!UICONTROL Impressions]* loopt. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | Het maximumbod voor de plaatsing. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | De vliegpakketstrategie voor de plaatsing: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* of *[!UICONTROL aggressive frontload]* . | Ja |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | De pakketstrategie binnen de dag voor de plaatsing: *[!UICONTROL Even]* of *[!UICONTROL ASAP]* . | Ja |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Alle filtercriteria die moeten worden toegepast. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Of biedregels (afgekeurd) *[!UICONTROL ON]* of *[!UICONTROL OFF]* zijn. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | De primaire frequentiedop voor de plaatsing tijdens de opgegeven [!UICONTROL Frequency Cap Interval] . | Ja |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Het interval voor de primaire frequentieklep: *[!UICONTROL Day]*, *[!UICONTROL Week]* of *[!UICONTROL Month]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | De secundaire frequentiekapitaal voor de plaatsing tijdens de opgegeven [!UICONTROL Secondary Frequency Cap Interval] | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | Het type interval voor de secundaire frequentielimiet: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* of *[!UICONTROL Minute]* . Het toepasselijke aantal weken, dagen, uren of minuten wordt aangegeven door de [!UICONTROL Secondary Frequency Cap Interval Value] . | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Het aantal weken, dagen, uren of minuten waarop [!UICONTROL Secondary Frequency Cap] van toepassing is. Als het secundaire uiteinde bijvoorbeeld drie indrukkingen per zes uur heeft, is de waarde hier `6` . | Ja |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | Het aantal doelgeografische locaties, *[!UICONTROL All]* of *[!UICONTROL None]* . | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | De beoogde geografische locaties, gescheiden door puntkomma&#39;s, of *[!UICONTROL All Locations]* . | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | Het aantal uitgesloten geografische locaties of *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | De uitgesloten geografische locaties, gescheiden door puntkomma&#39;s, of *[!UICONTROL None]* . | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | Het aantal gerichte aanbiedingen voor openbare inventarissen, indien van toepassing, dat wordt opgegeven, *[!UICONTROL All]* of *[!UICONTROL None]* . | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | Het aantal uitgesloten aanbiedingen in de openbare inventaris, indien van toepassing, of *[!UICONTROL None]* . | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | Het aantal gerichte particuliere inventorydeals, indien van toepassing, opgegeven, *[!UICONTROL All]* of *[!UICONTROL None]* . | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | Het aantal uitgesloten deals in de privévoorraad, indien van toepassing, of *[!UICONTROL None]* . | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | Het aantal beoogde [!UICONTROL On-Demand Inventory] -deals, indien van toepassing, dat wordt opgegeven, *[!UICONTROL All]* of *[!UICONTROL None]* . | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | Het aantal uitgesloten transacties in de On-Demand Inventory, indien van toepassing, of *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | Het beoogde type verkeer: *[!UICONTROL Website]* en/of *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Of de optie van de Targeting van de Inventaris om stroomafwaarts verkeer uit te sluiten is &lt;i[!UICONTROL >ON] * of *[!UICONTROL OFF]*.<br> de outstream advertenties verschijnen gewoonlijk over de inhoud als pop-up of opgevuld in inhoud (in de inheemse ervaring), eerder dan als regelmatige videoadvertenties in een videospeler. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | De kwaliteit van de sites waarop u wilt verwijzen: *[!UICONTROL Tier 1]* , *[!UICONTROL Tier 2]* , *[!UICONTROL Tier 3]* of *[!UICONTROL All Sites]* . | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | Het aantal doelsitecategorieën, indien opgegeven, of *[!UICONTROL All]* . | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | Het aantal uitgesloten sitecategorieën, indien opgegeven, of *[!UICONTROL All]* . | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | De uitgesloten sites, indien opgegeven, of *[!UICONTROL None]* . | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | De doeltalen van de site. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Alleen standaardpresentaties) Geeft aan of levering op niet-gecontroleerde sites is toegestaan of niet: *[!UICONTROL ON]* of *[!UICONTROL OFF]* . Wanneer de plaatsing privé-inventory als doel heeft, kan deze optie advertenties op geblokkeerde sites leveren. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | Het aantal doelsites, indien aanwezig, of *[!UICONTROL None]* . | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | Het beoogde publiek, indien aanwezig, of *[!UICONTROL None]* . | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | De uitgesloten doelgroepen, indien van toepassing, worden opgegeven of *[!UICONTROL None]* . | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Of [!DNL Comscore] demografische segmenten zijn ingeschakeld voor de plaatsing (en andere plaatsingen in de campagne): *[!UICONTROL ON]* of *[!UICONTROL OFF]* . Deze functie kan alleen worden ingeschakeld voor campagnes waarvoor de functie [!DNL Audience Verification] is ingeschakeld voor [!DNL Nielsen] en/of [!DNL Comscore] .  Er worden extra kosten in rekening gebracht. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Geeft aan of de advertentie wordt uitgebreid naar verschillende apparaten: *[!UICONTROL ON]* of *[!UICONTROL OFF]* . Bij het kiezen tussen verschillende apparaten wordt de doelversie uitgebreid naar alle bekende apparaten van een persoon, op basis van de apparaatgrafiek die is opgegeven in de campagne-instellingen. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Ingesloten # | Het aantal doelonderwerpcodes, indien van toepassing, of *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | Het aantal uitgesloten onderwerpcodes, indien van toepassing, of *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | Het aantal beoogde apparaatdoelen, indien van toepassing, of *[!UICONTROL All]* . | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | Het aantal uitgesloten apparaatdoelen, indien opgegeven, of *[!UICONTROL None]* . | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | Het aantal gerichte ISP leveranciers, als om het even welk worden gespecificeerd, of * [!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | Het aantal uitgesloten ISP-providers, indien opgegeven, of *[!UICONTROL None]* . | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | Het aantal toegepaste merkveiligheidsfilters, indien van toepassing, of *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | Het aantal vooraf biedende fraudeblokkeringsfilters toegepast, indien van toepassing, of *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | Het aantal vooraf biedbare weergavefilters dat wordt toegepast, indien aanwezig, of *[!UICONTROL None]* . | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Bepaalt of Siteveiligheidsblok is ingeschakeld: *[!UICONTROL ON]* of *[!UICONTROL OFF]* .<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | Het aantal pixels voor het bijhouden van gebeurtenissen van derden dat aan de plaatsing of *[!UICONTROL None]* is gekoppeld. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | Het aantal conversiepixels dat aan de plaatsing is gekoppeld, of *[!UICONTROL None]* . | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Een statisch tarief voor een vergoeding van derden dat moet worden bijgehouden als een niet-factureerbare kostprijs per 1000 impressies, indien van toepassing. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | Het aantal advertenties dat aan de plaatsing is gekoppeld, als er advertenties zijn toegevoegd, of *[!UICONTROL None]* . | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | De namen van advertenties die aan de plaatsing zijn gekoppeld, of *[!UICONTROL None]* . | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | De unieke, DSP gegenereerde advertentie-id&#39;s van advertenties die aan de plaatsing zijn gekoppeld, gescheiden door puntkomma&#39;s. Om een lijst van advertentienamen en bijbehorende identiteitskaarts van de [!UICONTROL Ads] mening te downloaden, creeer een douanemening die [!UICONTROL Ad ID] metrisch omvat, en dan [ voer de gegevens ](/help/dsp/campaign-management/reports/campaign-export-data.md) uit. | Ja |

>[!MORELIKETHIS]
>
>* [ Overzicht en geef de Montages van het Pakket uit gebruikend Bulksheets ](/help/dsp/campaign-management/packages/package-qa.md)
>* [ Overzicht en geeft de Montages van de Plaatsing Gebruikend Bulksheets uit ](/help/dsp/campaign-management/placements/placement-qa.md)
