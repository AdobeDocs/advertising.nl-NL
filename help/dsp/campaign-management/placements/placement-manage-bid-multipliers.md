---
title: Bodmultiplicatoren voor plaatsen beheren
description: Leer hoe u de biedvermenigvuldigingsfactoren voor uw plaatsingsdoelen kunt maken en bewerken.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
source-git-commit: 18c68edec80a80d236df138c05fba8d857c9ed9e
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 1%

---

# Bodmultiplicatoren voor plaatsen beheren

U kunt biedvermenigvuldigers tot stand brengen en beheren, waardoor een algoritmisch gegevens verwerkte bieding wordt vermenigvuldigd om de bieding te verhogen of te verminderen, voor uw bestaande plaatsingsdoelstellingen van [ in aanmerking komende doeltypes ](#bid-multiplier-by-target). U kunt de waarden van de biedvermenigvuldiger voor een plaatsing handmatig bewerken of een spreadsheet met waarden voor een of meer plaatsen uploaden.

Standaard is de biedvermenigvuldiger voor een doel 1,00, wat betekent dat het bod niet voor dat doel is aangepast. Waarden kunnen variëren van 0,10 tot 10,00. Een inschrijvingsvermenigvuldiger van 0,5 verlaagt bijvoorbeeld een bod van USD 6 naar USD 3 (0,5 x 6). Wanneer een veiling in aanmerking komt voor meerdere biedmodifiers, worden alle toepasselijke biedvermenigvuldigingsfactoren vermenigvuldigd. Als Californië bijvoorbeeld een Bodmultiplier van 2 heeft en San Francisco een Bodmultiplier van 3 heeft, is de laatste Bodmultiplier voor advertenties die in San Francisco lopen 6.

>[!NOTE]
>
>Bodmultipliers verhogen het bod nooit tot meer dan het maximumbod.

U kunt biedende vermenigvuldigers (met waarden buiten 1.00) voor a [ beperkte aantal doelstellingen ](#bid-multiplier-limits-by-target) plaatsen.

Deze functie werkt met uw bestaande plaatsingsdoelen. Om de geselecteerde doelstellingen voor uw plaatsen te veranderen, zie &quot;[ Plaatsen ](/help/dsp/campaign-management/placements/placement-edit.md) uitgeven.&quot;

## Bodvermenigvuldigers voor één plaatsing beheren

U kunt waarden handmatig bewerken of een spreadsheet uploaden voor één plaatsing.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik op de naam van de campagne.

1. Klik in het submenu op **[!UICONTROL Placements]** .

1. Klik naast de plaatsingsnaam op **[!UICONTROL ...]** > **[!UICONTROL Edit]** > **[!UICONTROL Bid Multiplier]** .

1. Pas de biedvermenigvuldigingsfactoren voor in aanmerking komende doelen aan:

   * Om de bewaarde vermenigvuldigingswaarden manueel aan te passen, beweging aan elk [ doel-specifiek lusje ](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], en [!UICONTROL Brand Safety]) en geef de bestaande waarden voor de plaatsingsdoelstellingen uit.

     De meeste doelcategorieën maken een lijst van subcategorieën op de linkerzijde. Klik op een subcategorie om de biedvermenigvuldigingsfactoren voor die subcategorie te beheren, al naar gelang van toepassing.

   * U kunt als volgt een CSV-bestand met waarden voor de vermenigvuldigingsfactor van het bod uploaden om alle bestaande waarden te overschrijven:

      1. Klik op **[!UICONTROL CSV File Edit]** rechtsboven.

      1. (a) klik **[!UICONTROL Download Template]** en bewerk het bestand of b) bewerk een eerder gedownloade sjabloon. Sla het bewerkte bestand op uw apparaat of netwerk op.

         De gedownloade spreadsheets bevatten één blad voor elk doeltype (zoals Land, Bronnen en Sitecategorie). Alleen bestaande bodvermenigvuldigers met waarden &lt; 1.0 of > 1.0 worden opgenomen.

         * Als u een bodvermenigvuldiger voor een bestaand doel wilt toevoegen, voert u het doel in met dezelfde syntaxis die zichtbaar is in de gebruikersinterface en de bijbehorende bodvermenigvuldigingswaarde.

         * Als u een biedwijziging wilt verwijderen, stelt u de vermenigvuldigingswaarde van het bod in op 1,0 of verwijdert u alle informatie voor de rij.

         ![ de rij van het Voorbeeld in een bieder multiplier spreadsheetdossier ](/help/dsp/assets/bid-multiplier-spreadsheet.png " rij van het Voorbeeld in een bieder multiplier spreadsheetdossier ")

      1. Klik op **[!UICONTROL Next]** om naar de sectie [!UICONTROL Upload File] te gaan en sleep a) het bewerkte bestand naar het vak of b) klik in het vak om het bestand van uw apparaat of netwerk te selecteren.

      1. Controleer de geüploade gegevens in de sectie [!UICONTROL Review & Submit] en klik op **[!UICONTROL Save]** .

## Biedvermenigvuldigers uploaden voor een of meer plaatsen

Upload een spreadsheet om dezelfde waarden toe te passen op alle geselecteerde plaatsingen.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik op de naam van de campagne.

1. Klik in het submenu op **[!UICONTROL Placements]** .

1. Schakel het selectievakje in naast elke plaatsing waarvan u de biedvermenigvuldigingsfactoren wilt beheren.

1. Klik op de werkbalk voor bulkacties op **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]** .

1. Upload een CSV-bestand met waarden voor de vermenigvuldigingsfactor van het bod om alle bestaande waarden voor alle geselecteerde plaatsen te overschrijven.

   1. (a) klik **[!UICONTROL Download Template]** en bewerk het bestand of b) bewerk een eerder gedownloade sjabloon. Sla het bewerkte bestand op uw apparaat of netwerk op.

      De gedownloade spreadsheets bevatten één blad voor elk doeltype (zoals Land, Bronnen en Sitecategorie). Alleen bestaande bodvermenigvuldigers met waarden &lt; 1.0 of > 1.0 worden opgenomen.

      * Als u een bodvermenigvuldiger voor een bestaand doel wilt toevoegen, voert u het doel in met dezelfde syntaxis die zichtbaar is in de gebruikersinterface en de bijbehorende bodvermenigvuldigingswaarde.

      * Als u een biedwijziging wilt verwijderen, stelt u de vermenigvuldigingswaarde van het bod in op 1,0 of verwijdert u alle informatie voor de rij.

      ![ de rij van het Voorbeeld in een bieder multiplier spreadsheetdossier ](/help/dsp/assets/bid-multiplier-spreadsheet.png " rij van het Voorbeeld in een bieder multiplier spreadsheetdossier ")

   1. Klik op **[!UICONTROL Next]** om naar de sectie [!UICONTROL Upload File] te gaan en sleep a) het bewerkte bestand naar het vak of b) klik in het vak om het bestand van uw apparaat of netwerk te selecteren.

   1. Controleer de geüploade gegevens in de sectie [!UICONTROL Review & Submit] en klik op **[!UICONTROL Save]** .

## Doeltypen die in aanmerking komen voor biedvermenigvuldigingsfactoren {#bid-multiplier-by-target}

U kunt biedingsbepalingen alleen configureren voor opgenomen doelen, niet voor uitgesloten doelen.

* **Geo richt**: geografie (landen, staten, en steden), postcodes, en DMAs

* **doelstellingen van de Inventaris**: bronnen en voer voor openbare inventaris en [!UICONTROL On Demand] inventaris

* **doelstellingen van de Plaats:** gerichte (maar niet uitgesloten) plaatsen/apps, plaatscategorieën

* **doelstellingen van het publiek:** segmenten, dagdelen, en onderwerpen

* **ads.txt doelstellingen:** (Wanneer u van ads.txt opteert, die u toestaat om inventaris van alle verkopers te kopen) advertenties.txt slechts verkopers, advertenties.txt directe verkopers, en advertenties.txt verkopers plus plaatsen zonder ads.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

## Maximum aantal biedvermenigvuldigers per doeltype {#bid-multiplier-limits-by-target}

U kunt biedvermenigvuldigingsfactoren (met andere waarden dan 1,00) instellen voor een beperkt aantal doelen. U kunt bijvoorbeeld biedvermenigvuldigingsfactoren instellen voor maximaal twintig landdoelen. Het maximumaantal doelen voor elk doeltype dat biedvermenigvuldigingsfactoren kan hebben, wordt hieronder vermeld.

| Categorie | Parameter | Maximum aantal |
| -------- | --------- | ----- |
| Geo | Land | 20 |
| Geo | Staat | 100 |
| Geo | Plaats | 100 |
| Geo | Metro | 100 |
| Geo | Postcodes | 100 |
| Inventaris | Bronnen | 100 |
| Inventaris | Feeds | 100 |
| Sites | Categorie Site | 100 |
| Sites | Sites/apps | 100 |
| Publiek | Segmenten | 500 |
| Publiek | Onderwerpen | 100 |
| Merkveiligheid | Ads.txt | NVT |

>[!MORELIKETHIS]
>
>* [ Ongeveer het Beheer van de Plaatsing ](placement-about.md)
>* [ geeft Plaatsen ](placement-edit.md) uit
>* [ Mening het Logboek van de Verandering voor een Plaatsing ](placement-change-log.md)
>* [ Montages van de Plaatsing ](placement-settings.md)
