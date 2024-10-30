---
title: Pakketinstellingen controleren en bewerken met behulp van bulksbladen
description: Leer hoe u de instellingen van een sleutelpakket bulksgewijs kunt bekijken en bewerken met behulp van spreadsheets.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# Pakketinstellingen controleren en bewerken met behulp van bulksbladen

U kunt de instellingen voor een of meer pakketten in de XLSX-indeling ([!DNL Microsoft Excel] spreadsheet) downloaden voor revisie. Het werkblad bevat een aparte tab met vluchtinformatie.

Als u meerdere instellingen tegelijk wilt bijwerken, kunt u een van de volgende twee handelingen uitvoeren:

* Breng de gewenste wijzigingen aan in de geselecteerde velden, sla het bestand op en upload het bewerkte bulkbladbestand weer naar DSP.

* Als u wijzigingen wilt aanbrengen in extra pakketten en in de instellingen voor elke plaatsing of advertentie, downloadt u een lege sjabloon voor het opsommingsblad met tabbladen voor elk type campagnecomponent, typt of plakt u nieuwe of bijgewerkte instellingen in het sjabloonbestand en uploadt u het bestand om de wijzigingen aan te brengen. Voor instructies, zie &quot;[ Overzicht en geef de Montages van de Component van de Campagne uit Gebruikend Bulksheets ](/help/dsp/campaign-management/campaign-components-review-edit.md).&quot;

Bewerkbare velden bevatten de meeste instellingen die normaal gesproken bewerkbaar zijn.

>[!TIP]
>
>Om meer gebieden voor één of meerdere pakketten snel uit te geven, zie &quot;[ Pakketten ](/help/dsp/campaign-management/packages/package-edit.md) uitgeven.&quot;

## Instellingen downloaden voor alle pakketten in een campagne

Wanneer u instellingen downloadt voor alle pakketten in een campagne, bevat het werkblad aparte tabbladen voor de pakketinstellingen en voor de vluchtinformatie. U kunt desgewenst instellingen opnemen voor de plaatsingen en advertenties die aan de pakketten zijn gekoppeld. Er worden extra tabbladen toegevoegd voor de plaatsings- en advertentie-instellingen.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik op de naam van de campagne.

1. Klik in de rechterbovenhoek op **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]** .

1. Hef in het dialoogvenster [!UICONTROL QA Sheet Download] de selectie op van de campagnecomponenten waarvan u de instellingen wilt uitsluiten van het gedownloade bestand en klik vervolgens op **[!UICONTROL Download]** .

Standaard zijn de instellingen voor alle aan de pakketten gekoppelde plaatsen en advertenties geselecteerd.

Een bericht geeft aan wanneer het bestand beschikbaar is om te downloaden.

1. Voer een van de volgende twee handelingen uit om het bestand te downloaden:

   * Klik in het meldingsbericht op **[!UICONTROL Download].**

   * In het recht van de hoogste menubar, klik ![ Banen ](/help/dsp/assets/downloads.png). Klik op **[!UICONTROL Download]** naast de taak.

     Het bestand wordt opgeslagen in de map Downloads van de browser. Zie &quot;[ de Kolommen van de Plaatsing in Gedownloade/Geüploade Spreadsheets ](#qa-sheet-columns)&quot;voor een lijst van de inbegrepen kolommen.

>[!NOTE]
>
>U kunt QA-bladen op campagnereniveau niet bewerken en opnieuw uploaden. Als u wijzigingen wilt aanbrengen in de instellingen van de campagnecomponent in deze bestanden, downloadt u een afzonderlijke sjabloon voor een bulksblad, typt of plakt u rijen van het QA-blad in de sjabloon voor het bulksblad en slaat u het bestand op. Vervolgens uploadt u het gevulde bulksblad. Voor instructies, zie &quot;[ Overzicht en geef de Montages van de Component van de Campagne uit Gebruikend Bulksheets ](/help/dsp/campaign-management/campaign-components-review-edit.md).&quot;

## Downloadinstellingen voor een of meer pakketten

Wanneer u instellingen voor specifieke pakketten downloadt, bevat het bulksbladbestand aparte tabbladen voor de pakketinstellingen en voor de vluchtinformatie, en kan het bestand worden bewerkt.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik op de naam van de campagne.

1. Klik in het submenu op **[!UICONTROL Packages]** .

1. Klik op de werkbalk voor bulkacties op **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]** .

   Een meldingsbericht geeft aan wanneer het bulksheet-bestand beschikbaar is om te downloaden.

1. Voer een van de volgende twee handelingen uit om het werkblad te downloaden:

   * Klik in het meldingsbericht op **[!UICONTROL Download].**

   * In het recht van de hoogste menubar, klik ![ Banen ](/help/dsp/assets/downloads.png). Klik op **[!UICONTROL Download]** naast de taak.

     Het bestand wordt opgeslagen in de map Downloads van de browser. Zie &quot;[ de Kolommen van de Plaatsing in Gedownloade/Geüploade Spreadsheets ](#qa-sheet-columns)&quot;voor een lijst van de inbegrepen kolommen.

<!-- I don't think I need this here

## Download a Bulksheet Template {#download-template}

You can optionally download a blank bulksheet template that includes tabs for each type of campaign component. You can later add rows to any tab on the template and [upload the edited file](##upload-bulksheet-package) to make changes. 

1. Click the name of the campaign.

1.  In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   The file is saved to the browser's Downloads folder. See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns.

-->

## Een werkblad met pakketinstellingen uploaden {#upload-bulksheet-package}

U kunt instellingen voor uw pakketten, inclusief de plaatsingen en advertenties die aan de pakketten zijn gekoppeld, uploaden naar een bestand met opsommingstekens.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik op de naam van de campagne.

1. Klik in de rechterbovenhoek op **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]** .

1. In het dialoogvenster [!UICONTROL Upload Bulksheet] :

   1. Sleep een bestand naar het vak of klik in het vak om een bestand van het apparaat of het netwerk te selecteren.

   1. Klik op **[!UICONTROL Upload]**.

1. (Facultatief) om te verifiëren dat de updates werden verwerkt, klik ![ Banen ](/help/dsp/assets/downloads.png) in het recht van de hoogste menubar.

## Kolommen met pakketinstellingen in gedownloade/geüploade werkbladen{#qa-sheet-columns-packages}

>[!TIP]
>
> In een gedownloade spreadsheet worden alle bewerkbare kolommen in blauw gemarkeerd.

### [!UICONTROL Package] Tab

| Sectie | Kolom | Beschrijving | Bewerkbaar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | De numerieke id van het pakket. | — |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | De naam van het pakket. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL Status] | De pakketstatus: *[!UICONTROL active]* of *[!UICONTROL inactive]* . | Ja |
| [!UICONTROL Basic details] | [!UICONTROL Description] | Een optionele beschrijving van het pakket. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | Een statisch tarief van een vergoeding van derden dat moet worden bijgehouden als niet-factureerbare kosten per 1000 impressies, indien van toepassing. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | Een facultatieve beschrijving van het tarief van de derdenvergoeding, indien van toepassing. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | De begindatum van het pakket. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | De einddatum van het pakket. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | Op welk niveau moet de positie en het uiteinde van de plaatsingen in het pakket worden geplaatst: *[!UICONTROL Package]* of *[!UICONTROL Placement]* . | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | De pakketbegroting. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | Het budgetinterval: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* of *[!UICONTROL All Time]* . | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | Een optionele budgetintervallimiet. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | Het interval voor de optionele budgetinterval-uiteinde: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* of *[!UICONTROL All Time]* . | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | Het doel van het pakket. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | De doelwaarde van het doel. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Pakketten met &quot;[!UICONTROL Highest Return on Ad Spend]&quot;en &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;optimaliseringsdoelstellingen slechts) A [ douanedoel ](/help/dsp/optimization/custom-goal.md) dat de opbrengst of omzettingsgebeurtenissen omvat die worden gebruikt om metrische CPA of ROAS te berekenen. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Optioneel; pakketten met alleen de optimalisatiedoelstellingen &quot;[!UICONTROL Highest Return on Ad Spend]&quot; en &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;) De uiteindelijke conversiegebeurtenis of inkomstengebeurtenis/-verkoop is bedoeld voor het berekenen van het rendement op advertentie-uitgaven of de kosten per aankoop. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Pakketten met alleen aangepaste optimalisatiedoelen) Het doel van het pakket, waarmee u kunt bepalen hoe het pakket moet worden geoptimaliseerd: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]* of *[!UICONTROL Other]* . | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Pakketten met alleen aangepaste optimalisatiedoelen) De pakket-id voor een ander pakket waarvan de historische gegevens worden gebruikt als invoer voor het optimaliseren van het pakket. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Pakketten met alleen aangepaste optimalisatiedoelen) Een ander pakket waarvan de historische gegevens worden gebruikt als invoer voor het optimaliseren van het pakket. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Geeft aan of het pakket in de richting van de *[!UICONTROL budget]* - of *[!UICONTROL primary_goal]* -afbeelding loopt (voor afbeeldingen). | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (Wanneer u het pakket plaatst bij afbeeldingen) Het doelaantal indrukkingen tijdens het opgegeven tijdsinterval. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (Wanneer u het pakket op afbeeldingen plaatst) Het tijdinterval voor het doelaantal afbeeldingen. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | De vliegpakketstrategie voor het pakket: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* of *[!UICONTROL aggressive frontload]* . | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | De pakketstrategie binnen de dag voor het pakket: *[!UICONTROL Even]* of *[!UICONTROL ASAP]* . | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | De primaire frequentiedop voor de verpakking tijdens de opgegeven [!UICONTROL Frequency Cap Interval] . | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | Het interval voor de primaire frequentieklep: *[!UICONTROL Day]*, *[!UICONTROL Week]* of *[!UICONTROL Month]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | Het aantal weken, dagen, uren of minuten waarop de primaire [!UICONTROL Frequency Cap] van toepassing is. Als het primaire uiteinde bijvoorbeeld 12 afdrukken per maand is, is de waarde hier `12` . | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | De secundaire frequentiedop voor de verpakking tijdens de opgegeven [!UICONTROL Secondary Frequency Cap Interval] | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | Het type interval voor de secundaire frequentieklep: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* of *[!UICONTROL Minute]*. Het toepasselijke aantal weken, dagen, uren of minuten wordt aangegeven door de [!UICONTROL Secondary Frequency Cap Interval Value] . | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | Het aantal weken, dagen, uren of minuten waarop [!UICONTROL Secondary Frequency Cap] van toepassing is. Als het secundaire uiteinde bijvoorbeeld drie indrukkingen per zes uur heeft, is de waarde hier `6` . | Ja |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Al dan niet om niet-even het afvangen van vluchten voor het pakket *T* (waar) of *F* (vals) te creëren. Nadat u aangepaste flighting hebt ingeschakeld en het pakket hebt opgeslagen, kunt u aangepaste flighting niet uitschakelen en de begindatum van het pakket niet meer bewerken. | — |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Beschikbaar slechts wanneer de [!UICONTROL Activate Custom Flighting] optie) wordt toegelaten al dan niet om het even welk resterende budget van de vorige vlucht aan het bestaande budget voor de volgende vlucht automatisch toe te voegen: *T* (waar) of *F* (vals). | Ja |
| [!UICONTROL Error] | [!UICONTROL Error] | Eventuele relevante fouten. | — |

### [!UICONTROL Package_Flights] Tab {#qa-sheet-columns-package-flights}

| Sectie | Kolom | Beschrijving | Bewerkbaar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | De numerieke id van het pakket. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | De numerieke id van de vlucht. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | De eerste vluchtdatum. | Ja |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | De einddatum van de vlucht. | Ja |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | Het doel waarvoor de vlucht wordt uitgegeven. | Ja |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Bestaande pakketten zonder de optie &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot; ingeschakeld) Een hoeveelheid potentieel onuitgegeven budget om toe te voegen aan de volgende vlucht. | Ja |

>[!MORELIKETHIS]
>
>* [ Overzicht en geeft de Montages van de Component van de Campagne uit Gebruikend Bulksheets ](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [ geef Pakketten ](/help/dsp/campaign-management/packages/package-edit.md) uit
>* [ de Montages van het Pakket ](/help/dsp/campaign-management/packages/package-settings.md)
