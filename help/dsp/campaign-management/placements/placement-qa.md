---
title: Plaatsingsinstellingen controleren en bewerken met werkbladen
description: Leer hoe u de instellingen voor toetsplaatsing kunt bekijken en bewerken met spreadsheets.
feature: DSP Placements
exl-id: 2de4407d-eb3b-44ff-893c-9fdf6921d4b3
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 0%

---

# Plaatsingsinstellingen controleren en bewerken met werkbladen

U kunt de instellingen voor een of meer plaatsingen of voor alle plaatsingen in een campagne downloaden in de XLSX-indeling (Excel-spreadsheet) voor revisie. Met deze functie kunt u snel details bekijken zoals:

* Dit publiek past de campagnedoelen toe.
* Wanneer de plaatsingen beginnen te leveren, en wanneer zij ophouden.
* Welke advertenties zijn gekoppeld aan de plaatsingen.

Vervolgens kunt u wijzigingen aanbrengen in de geselecteerde velden en deze weer uploaden naar DSP allemaal tegelijk. Bewerkbare velden bevatten de plaatsingsnamen, statussen, biedingen, budgetten, pacingstrategieën en frequentiecaps.

>[!TIP]
>
>Als u meer velden voor een of meer plaatsen wilt bewerken, raadpleegt u &quot;[Plaatsen bewerken](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

## Instellingen downloaden voor alle locaties in een campagne

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

1. Voer een van de volgende handelingen uit:

   * Klik naast de naam van de campagne op **[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**.

   * Klik op de naam van de campagne om de details van de campagne weer te geven. Klik rechtsboven op **[!UICONTROL ...]** > **[!UICONTROL Download Excel QA sheet]**.

   Een bericht geeft aan wanneer het bestand beschikbaar is om te downloaden.

1. Voer een van de volgende handelingen uit:

   * Klik in het bericht op **[!UICONTROL Download].**

   * Klik rechts van de bovenste menubalk op ![Taken](/help/dsp/assets/downloads.png). Klikken **[!UICONTROL Download]** naast de taak.

   Het bestand wordt opgeslagen in de map Downloads van de browser. Zie &quot;[Kolommen in gedownloade/geüploade werkbladen](#qa-sheet-columns)&quot; voor een lijst van de opgenomen kolommen.

## Downloadinstellingen voor een of meer locaties

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

1. Klik op de naam van de campagne.

1. Klik in het submenu op **[!UICONTROL Placements]**.

1. Schakel het selectievakje in naast elke plaatsing waarvan u de instellingen wilt downloaden.

1. Klik op de werkbalk voor bulkacties op **[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**.

Het bestand wordt automatisch opgeslagen in de downloadmap van de browser. Zie &quot;[Kolommen in gedownloade/geüploade werkbladen](#qa-sheet-columns)&quot; voor een lijst van de opgenomen kolommen.

## Instellingen voor alle locaties in een campagne uploaden

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

1. Voer een van de volgende handelingen uit:

   * Klik naast de naam van de campagne op **[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**.

   * Klik op de naam van de campagne om de details van de campagne weer te geven. Klik rechtsboven op **[!UICONTROL ...]** > **[!UICONTROL Upload Excel QA sheet]**.

1. In de [!UICONTROL Edit in Excel] dialoogvenster:

   1. Sleep een bestand naar het vak of klik in het vak om een bestand van het apparaat of het netwerk te selecteren.

   1. Klik op **[!UICONTROL Upload]**.

1. (Optioneel) Als u wilt controleren of de updates zijn verwerkt, klikt u op ![Taken](/help/dsp/assets/downloads.png) rechts van de bovenste menubalk.

## Instellingen uploaden voor een of meer locaties

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

1. Klik op de naam van de campagne.

1. Klik in het submenu op **[!UICONTROL Placements]**.

1. Schakel het selectievakje in naast elke plaatsing waarvan u de instellingen wilt uploaden.

1. Klik op de werkbalk voor bulkacties op **[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**.

1. In de [!UICONTROL Edit in Excel] dialoogvenster:

   1. Sleep een bestand naar het vak of klik in het vak om een bestand van het apparaat of het netwerk te selecteren.

   1. Klik op **[!UICONTROL Upload]**.

1. (Optioneel) Als u wilt controleren of de updates zijn verwerkt, klikt u op ![Taken](/help/dsp/assets/downloads.png) rechts van de bovenste menubalk.

## Plaatsingsinstellingskolommen in gedownloade/geüploade werkbladen{#qa-sheet-columns}

>[!TIP]
>
> In een gedownloade spreadsheet worden alle bewerkbare kolommen in blauw gemarkeerd.

### Spreadsheets op campagnereniveau

| Sectie | Kolom | Beschrijving | Bewerkbaar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | De numerieke id van de plaatsing. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | De naam van de plaatsing. | Ja |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Alle toegepaste labels voor rapportage. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Een koppeling om de plaatsing te openen in de modus Bewerken. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | De plaatsingsstatus: *[!UICONTROL active]* of *[!UICONTROL inactive]*. | Ja |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | Het plaatsingstype. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | De naam van het bovenliggende pakket, indien van toepassing. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | De begindatum van de plaatsing. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | De einddatum van de plaatsing. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Of overdag is *[!UICONTROL ON]* of *[!UICONTROL OFF]*.<br><b>Opmerking:</b> Als u het feitelijke zomertijdschema wilt controleren, opent u de plaatsingsinstellingen in DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | Het budget voor plaatsing, als dat er is. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | Het begrotingsinterval: &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, of *[!UICONTROL All Time]*.[!UICONTROL >Daily] | Ja |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | Het doel van het pakket. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | De doelwaarde van het doel. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Of de plaatsing in de richting van *[!UICONTROL Budget]* of *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | Het maximumbod voor de plaatsing. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | De vliegpakketstrategie voor de plaatsing: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, of *[!UICONTROL aggressive frontload]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | De pakketstrategie binnen de dag voor de plaatsing: *[!UICONTROL Even]* of *[!UICONTROL ASAP]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Alle filtercriteria die moeten worden toegepast. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Of biedregels (afgekeurd) zijn *[!UICONTROL ON]* of *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | De primaire frequentiedop voor de plaatsing tijdens de opgegeven [!UICONTROL Frequency Cap Interval]. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Het interval voor de primaire frequentiedop: *[!UICONTROL Day]*, *[!UICONTROL Week]*, of *[!UICONTROL Month]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | De secundaire frequentiedop voor de plaatsing tijdens de opgegeven [!UICONTROL Secondary Frequency Cap Interval] | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | Het type interval voor de secundaire frequentiedop: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, of *[!UICONTROL Minute]*. Het toepasselijke aantal weken, dagen, uren of minuten wordt aangegeven door de [!UICONTROL Secondary Frequency Cap Interval Value]. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Het aantal weken, dagen, uren of minuten waarvoor de [!UICONTROL Secondary Frequency Cap] van toepassing. Als de secundaire dop bijvoorbeeld drie indrukkingen per zes uur heeft, is de waarde hier `6`. | Ja |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | het aantal beoogde geografische locaties; *[!UICONTROL All]*, of *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | de beoogde geografische locaties, gescheiden door puntkomma&#39;s, of *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | Het aantal uitgesloten geografische locaties of *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | de uitgesloten geografische locaties, gescheiden door puntkomma&#39;s, of *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | het aantal beoogde transacties in het kader van de openbare inventaris, indien van toepassing, *[!UICONTROL All]*, of *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | het aantal uitgesloten transacties in het kader van de openbare inventaris, indien van toepassing, of *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | het aantal beoogde transacties in de particuliere inventaris, indien van toepassing, *[!UICONTROL All]*, of *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | het aantal eventuele uitgesloten transacties in de particuliere inventaris, of *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | Het aantal doelgroepen [!UICONTROL On-Demand Inventory] transacties, indien gespecificeerd; *[!UICONTROL All]*, of *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | het aantal uitgesloten transacties in de inventarisatie op aanvraag, indien van toepassing, of *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | Het beoogde type verkeer: *[!UICONTROL Website]* en/of *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Of de het Targeteren optie van de Inventaris om stroomafwaarts verkeer uit te sluiten is &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />* of *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>Outstream-advertenties worden doorgaans als een pop-up of opgevuld in inhoud (in de eigen ervaring) weergegeven in plaats van als gewone videobanden in een videospeler. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | De kwaliteit van de sites waarop u zich wilt richten: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*, of *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | het aantal doelcategorieën, indien van toepassing, of *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | het aantal categorieën van uitgesloten sites, indien gespecificeerd, of *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | de uitgesloten sites, indien gespecificeerd, of *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | De doeltalen van de site. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Alleen standaardplaatjes) Of het al dan niet toestaan van levering op niet-gecontroleerde sites: *[!UICONTROL ON]* of *[!UICONTROL OFF]*. Wanneer de plaatsing privé-inventarisatie als doel heeft, kan deze optie advertenties op geblokkeerde sites leveren. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | het aantal beoogde sites, indien van toepassing, of *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | het beoogde publiek, indien van toepassing, of *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | het eventuele uitgesloten publiek, of *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Al dan niet [!DNL Comscore] demografische segmenten zijn geschikt voor de plaatsing (en andere plaatsen in de campagne): *[!UICONTROL ON]* of *[!UICONTROL OFF]*. Deze functie kan alleen worden ingeschakeld voor campagnes waarvoor de [!DNL Audience Verification] functie is ingeschakeld voor [!DNL Nielsen] en/of [!DNL Comscore].  Er worden extra kosten in rekening gebracht. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Of de advertentie moet worden uitgebreid naar andere apparaten: *[!UICONTROL ON]* of *[!UICONTROL OFF]*. Bij het kiezen tussen verschillende apparaten wordt de doelversie uitgebreid naar alle bekende apparaten van een persoon, op basis van de apparaatgrafiek die is opgegeven in de campagne-instellingen. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Ingesloten # | Het aantal doelonderwerpcodes, indien van toepassing, of *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | het aantal codes van uitgesloten onderwerpen, indien van toepassing, of *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | het aantal beoogde apparaatdoelen, indien van toepassing, of *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | het aantal eventueel gespecificeerde uitgesloten apparaatdoelen, of *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | Het aantal gerichte ISP leveranciers, als om het even welk wordt gespecificeerd, of *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | Het aantal uitgesloten ISP leveranciers, als om het even welk wordt gespecificeerd, of *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | het aantal toegepaste merkveiligheidsfilters, indien van toepassing, of *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | het aantal filters die fraude blokkeren bij voorbiedingen, indien gespecificeerd, of *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | het aantal eventueel opgegeven filters voor de weergave vóór het bod, of *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Of Site Safety Block is ingeschakeld of niet: *[!UICONTROL ON]* of *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | Het aantal pixels voor het bijhouden van gebeurtenissen van derden dat aan de plaatsing is gekoppeld, of *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | Het aantal conversiepixels dat aan de plaatsing is gekoppeld, of *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Een statisch tarief van een vergoeding van derden dat moet worden bijgehouden als niet-factureerbare kosten per 1000 impressies, indien van toepassing. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | het aantal advertenties dat aan de plaatsing is gekoppeld, indien aanwezig, of *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | de namen van advertenties die aan de plaatsing zijn gekoppeld, of *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | De unieke, DSP gegenereerde advertentie-id&#39;s van advertenties die aan de plaatsing zijn gekoppeld, gescheiden door puntkomma&#39;s. Een lijst met advertentienamen en bijbehorende advertentie-id&#39;s downloaden van de [!UICONTROL Ads] een aangepaste weergave maken die de [!UICONTROL Ad ID] metrisch, en dan [de gegevens exporteren](/help/dsp/campaign-management/reports/campaign-export-data.md). | Ja |

### Werkbladen op plaatsingsniveau

| Kolom | Beschrijving | Bewerkbaar? |
|--------|-------------|-----------|
| [!UICONTROL Placement ID] | De numerieke id van de plaatsing. | — |
| [!UICONTROL Placement Name] | De naam van de plaatsing. | Ja |
| [!UICONTROL Package Name] | De naam van het bovenliggende pakket, indien van toepassing. | — |
| [!UICONTROL Start Date] | De begindatum van de plaatsing. | — |
| [!UICONTROL End Date] | De einddatum van de plaatsing. | — |
| [!UICONTROL Status] | De plaatsingsstatus: *[!UICONTROL active]* of *[!UICONTROL inactive]*. | — |
| [!UICONTROL Max Bid] | Het maximumbod voor de plaatsing. | Ja |
| [!UICONTROL Budget] | Het budget voor plaatsing, als dat er is. | Ja |
| [!UICONTROL Budget Interval] | Het begrotingsinterval: &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, of *[!UICONTROL All Time]*.[!UICONTROL >Daily] | Ja |
| [!UICONTROL Primary Frequency Cap] | De primaire frequentiedop voor de plaatsing tijdens de opgegeven [!UICONTROL Primary Frequency Cap Interval]. | Ja |
| [!UICONTROL Primary Frequency Cap Interval] | Het interval voor de primaire frequentiedop: *[!UICONTROL Day]*, *[!UICONTROL Week]*, of *[!UICONTROL Month]*. | Ja |
| [!UICONTROL Secondary Frequency Cap] | De secundaire frequentiedop voor de plaatsing tijdens de opgegeven [!UICONTROL Secondary Frequency Cap Interval] | Ja |
| [!UICONTROL Secondary Frequency Cap Interval] | Het type interval voor de secundaire frequentiedop: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, of *[!UICONTROL Minute]*. Het toepasselijke aantal weken, dagen, uren of minuten wordt aangegeven door de [!UICONTROL Secondary Frequency Cap Interval Value]. | Ja |
| [!UICONTROL Secondary Frequency Cap Interval Value] | Het aantal weken, dagen, uren of minuten waarvoor de [!UICONTROL Secondary Frequency Cap] van toepassing. Als de secundaire dop bijvoorbeeld drie indrukkingen per zes uur heeft, is de waarde hier `6`. | Ja |
| [!UICONTROL Attached Ad ID] | De unieke, DSP gegenereerde advertentie-id&#39;s van advertenties die aan de plaatsing zijn gekoppeld, gescheiden door puntkomma&#39;s. Een lijst met advertentienamen en bijbehorende advertentie-id&#39;s downloaden van de [!UICONTROL Ads] een aangepaste weergave maken die de [!UICONTROL Ad ID] metrisch, en dan [de gegevens exporteren](/help/dsp/campaign-management/reports/campaign-export-data.md). | Ja |

>[!MORELIKETHIS]
>
>* [Plaatsen bewerken](/help/dsp/campaign-management/placements/placement-edit.md)
>* [Plaatsingsinstellingen](/help/dsp/campaign-management/placements/placement-settings.md)
