---
title: Plaatsingsinstellingen
description: Zie beschrijvingen van de beschikbare plaatsingsmontages.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: f8f877552018de50649fbba22c56452775e72df3
workflow-type: tm+mt
source-wordcount: '4436'
ht-degree: 0%

---

# Plaatsingsinstellingen

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** De plaatsingsnaam.

>[!TIP]
>Gebruik een naamgevingsconventie die voor uw situatie zinnig is. Één gesuggereerde noemende overeenkomst is &quot;*\ &lt;Campagne Naam \>: \&lt;Advertentie Eenheid\>: \&lt;Duration\>: \&lt;Targeting\>*.&quot;

**[!UICONTROL Status]:** De plaatsingsstatus: *[!UICONTROL Active]* (de standaardwaarde) of *[!UICONTROL Paused]*.

>[!TIP]
>De beste manier is om de plaatsing te pauzeren tot u bereid bent om het te lanceren.

**[!UICONTROL Details]:** (read-only) het toepasselijke advertentietype, de rekening die tot de plaatsing leidt of creeerde, en de oudercampagne. Klik op **[!UICONTROL Show more]** voor meer informatie.

**[!UICONTROL Templates]:** opent een lijst met bestaande plaatsingssjablonen. Als u doelinstellingen automatisch wilt invullen vanuit een sjabloon:

1. Voer een van de volgende handelingen uit:

   * Als u al het doel uit een sjabloon opnieuw wilt gebruiken, schakelt u het selectievakje naast de sjabloonnaam in.

   * Als u afzonderlijke doeltypen uit een sjabloon opnieuw wilt gebruiken, vouwt u de sjabloonnaam uit en schakelt u het selectievakje in naast de doeltypen die u opnieuw wilt gebruiken.

1. Klik op **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Video en formaten slechts) de adduur en/of advertentiespecificaties, die worden gebruikt om de projectie van de Vooruitzichten op het recht te berekenen. De velden verschillen per advertentietype.

**[!UICONTROL Environment]:** (Alleen Universal Video ad format) De apparaatomgevingen (Computer, Mobile, Connected TV) die als doelen in de plaatsing moeten worden opgenomen. Geef ten minste één waarde op.

In douanerapporten, wijst de plaatsing-vlakke dimensie &quot;het Milieu van het Apparaat&quot;op het gerichte milieu.

**[!UICONTROL Placement tags]:** (Facultatieve) Sleutelwoorden of bijnamen helpen u van deze plaatsing de plaats bepalen.

## Doelen

**[!UICONTROL Package]:** (Facultatief) een pakket waaraan de plaatsing wordt toegewezen. Klik ![ uitgeven ](/help/dsp/assets/edit.png) om een bestaand pakket te selecteren of een pakket tot stand te brengen. Wanneer u de plaatsing toewijst aan een pakket, wordt de sectie [!UICONTROL Goals] bijgewerkt met de vluchtdatums, het leveringsdoel en het budget uit het pakket.

**[!UICONTROL Flight Dates]:** De begin- en einddatum voor de plaatsing. Goedgekeurde advertenties komen in aanmerking om tijdens de vlucht te worden uitgevoerd wanneer de plaatsing actief is en wordt toegewezen aan een actief pakket of een actieve campagne.

De datums voor het pakket (indien van toepassing) of de campagne worden standaard automatisch ingevuld.

>[!NOTE]
>
>* De vluchtdata moeten worden opgenomen in de campagnevluchtdata en de pakketvliegdata.

### Plaatsen die aan Pakketten met pakket-vlakke Tussenruimte worden toegewezen

**[!UICONTROL Placement Funding]:** Hoe begroot u de plaatsing:

* *[!UICONTROL Optimize based on performance]:* controleert het budget op pakketniveau.
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* Staat u toe om een minimum en/of een maximumplaatsingsbudget te plaatsen. Geef ten minste één soort begroting op:

   * *[!UICONTROL Maximum Budget]*: voer een waarde en de duur in (*[!UICONTROL All time]* , *[!UICONTROL Daily]* , *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

   * *[!UICONTROL Minimum Budget]*: De minimale begroting als een percentage van de pakketbegroting. Wanneer een intervalmaximum wordt gespecificeerd, wordt de minimumbegrotingswaarde altijd berekend als percentage van het intervalmaximum. Anders wordt het berekend als een percentage van de pakketbegroting.

**[!UICONTROL Max Bid]:** Het maximum dat voor 1000 beelden moet worden betaald.

**[!UICONTROL Min Bid]:** (Alleen voor persoonlijke en [!DNL On-Demand] deals) Het minimale bod op basis van het voorraadtype. Selecteer een optie:

* *[!UICONTROL None]*: Geen minimumbod voor een voorraadtype. Als het berekende bod lager is dan de vaste prijs/minimumprijs van de beoogde deals, biedt DSP geen bod. Dit kan de schaal beïnvloeden.

* *[!UICONTROL Fixed/floor price for Private deals only]*: DSP biedt ten minste de vaste prijs/ondergrens voor de beoogde privédeals, zelfs als het algoritmisch berekende bod lager is. Dit kan de prestaties beïnvloeden.

* *[!UICONTROL Fixed/floor price for On-demand deals only]*: DSP biedt ten minste een bod op de vaste prijs/ondergrens voor de beoogde [!DNL On-Demand] -deals, zelfs als het algoritmisch berekende bod lager is. Dit kan de prestaties beïnvloeden.

* *[!UICONTROL Fixed/floor price for both Private and On-demand deals]*: DSP biedt ten minste een bod op de vaste prijs/ondergrens voor de beoogde persoonlijke en [!DNL On-Demand] -deals, zelfs als het algoritmisch berekende bod lager is. Dit kan de prestaties beïnvloeden.

**[!UICONTROL Placement Pre-bid Filters]:** tot vijf KPI drempels (zoals een minimum viewability metrisch of klikthrough tarief) die moeten worden ontmoet om voor te komen bod. U kunt voorbiedingsfilters gebruiken als optimalisatietactiek, maar u weet dat elke regel de mogelijkheden waarop deze plaatsing kan bieden, kan beperken. Filters toevoegen of bewerken:

1. Klik ![ uitgeven ](/help/dsp/assets/edit.png).
1. Voer een van de volgende handelingen uit:
   * Een filter toevoegen:
      1. Klik op **[!UICONTROL Add Filter]**.
      1. Selecteer naast **[!UICONTROL Only bid if]** een metrische waarde en voer een waarde in.
   * Als u een filter wilt verwijderen, klikt u op **[!UICONTROL X]** in de filterrij.
1. Klik op **[!UICONTROL Save]**.

Zie beschrijvingen van elk pre-bieder filter bij &quot;[ plaatsing-vlakke pre-Biedfilters en hoe te om hen ](/help/dsp/optimization/optimization-pre-bid-filters.md) te gebruiken.&quot;

### Alle andere plaatsen

**[!UICONTROL Budget Goal]:** Het bruto begrotingsmaximum en het begrotingsinterval (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Plaatsingen in campagnes met slechts marginbeheer) het bruto begrotingsmaximum en het begrotingsinterval (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:** De optimalisatiedoelstelling voor het pakket. Zie beschrijvingen van elk optimalisatiedoel bij &quot;[ de Doelstellingen van de Optimalisering en hoe te om hen ](/help/dsp/optimization/optimization-goals.md)&quot;te gebruiken.

**[!UICONTROL Target Goal]:** het doeldoel, dat wordt gebruikt om prestaties te volgen.

>[!NOTE]
>
>Dit veld is alleen een benchmark en wordt niet gebruikt voor beslissingen.

**[!UICONTROL Pace on]:** De basis voor het afvangen:

* **[!UICONTROL Budget goal]:** (Gebrek) deze optie levert zoveel mogelijk beelden binnen het toegewezen budget.

* **[!UICONTROL Impressions]:** deze optie levert beelden tot een gespecificeerde hoeveelheid binnen een gespecificeerd interval wordt bereikt. Wanneer u deze optie selecteert, geeft u het aantal afbeeldingen en het interval op: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* of *[!UICONTROL Weekly]* .

**[!UICONTROL Max Bid]:** Het maximum dat voor 1000 beelden moet worden betaald.

**[!UICONTROL Flight pacing]:** (Plaatsen met plaatsing-vlakke het passen slechts) hoe te plaats en levering:

* *[!UICONTROL Even]:* (het gebrek) plaatst gelijkmatig levering door elke vlucht, met een doel van 50% van de levering in de eerste helft van de vlucht.

* *[!UICONTROL Slightly Ahead]:* (het gebrek) versnelt levering zodat het 55-65% volledig halverwege de vluchtduur is.

* *[!UICONTROL Frontload]:* versnelt levering zodat het 65-75% volledig halverwege de vlucht is.

* *[!UICONTROL Aggressive Frontload]:* versnelt levering zodat het 75-85% volledig halverwege de vlucht is.

**[!UICONTROL Intraday pacing]:** (Plaatsen met plaatsing-vlakke het plaatsen slechts) hoe te plaats en levering over elke dag binnen de vlucht:

* *[!UICONTROL Even]:* (het gebrek) schalen levering op inventarisbeschikbaarheid wordt gebaseerd die. Over het algemeen worden meer advertenties overdag per uur geleverd, wanneer het veilingsvolume hoger is en er minder advertenties &#39;s ochtends en &#39;s avonds worden geleverd.

* *[!UICONTROL ASAP]:* (het gebrek) versnelt levering aan tweemaal de snelheid van *Even*.

  >[!CAUTION]
  >
  >Deze optie kan de prestaties negatief beïnvloeden. Gebruik dit alleen als u volledige prioriteit geeft aan levering en meer geld besteedt aan optimalisatie van prestaties.

**[!UICONTROL Placement Pre-bid Filters]:** (Optioneel) Maximaal vijf filters waaraan moet worden voldaan om te kunnen bieden. U kunt voorbiedingsfilters gebruiken als optimalisatietechniek, maar houd er rekening mee dat elke regel de mogelijkheden waarop deze plaatsing kan bieden, kan beperken. Filters toevoegen of bewerken:

1. Klik ![ uitgeven ](/help/dsp/assets/edit.png).
1. Voer een van de volgende handelingen uit:
   * Een filter toevoegen:
      1. Klik op **[!UICONTROL Add Filter]**.
      1. Selecteer naast **[!UICONTROL Only bid if]** een metrische waarde en voer een waarde in.
   * Als u een filter wilt verwijderen, klikt u op **[!UICONTROL X]** in de filterrij.
1. Klik op **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Optioneel) Specifieke locaties waar u advertenties in de plaatsing wilt opnemen of uitsluiten. Als u geen plaatsen specificeert, worden alle plaatsen gericht.

>[!NOTE]
>
>De plaatsen van de Stad en DMA zijn niet beschikbaar voor Plaatsen Roku.

Locaties opgeven:

1. Klik ![ uitgeven ](/help/dsp/assets/edit.png).
1. Voer een van de volgende handelingen uit:
   * Een land, een staat, een stad, een DMA, een federaal wetsdistrict of een wetsdistrict van een staat op te nemen of uit te sluiten:
      1. Selecteer het locatietype in de linkerkolom.
      1. (Indien nodig) Klik op een locatie om deze uit te vouwen.
      1. Klik naast de locatie op *[!UICONTROL Include]* om deze als doel op te nemen of op *[!UICONTROL Exclude]* om deze als doel uit te sluiten.
   * U kunt als volgt naar een postcode zoeken en alle geselecteerde resultaten opnemen of uitsluiten:
      1. Klik op **[!UICONTROL Search Postal Code]**.
      1. Selecteer het land.
      1. Ga de plaatsnaam in, en klik dan ![ uitgeven ](/help/dsp/assets/search.png).
      1. Klik op het juiste zoekresultaat.
      1. Klik op *[!UICONTROL Include All]* om alle locaties als doelen op te nemen of op *[!UICONTROL Exclude All]* om alle locaties als doelen uit te sluiten.
   * U kunt als volgt postcodes invoeren of plakken en deze allemaal opnemen of uitsluiten:
      1. Klik op **[!UICONTROL Paste Postal Code]**.
      1. Selecteer het land.
      1. Voer maximaal 1000 postcodes in of plak deze.
Neem één postcode per regel op of voer meerdere waarden in, gescheiden door komma&#39;s of tabs.
      1. Klik op *[!UICONTROL Include All]* om alle locaties als doelen op te nemen of op *[!UICONTROL Exclude All]* om alle locaties als doelen uit te sluiten.
   * Als u een locatie uit de lijst [!UICONTROL Included] of [!UICONTROL Excluded] wilt verwijderen, klikt u op **[!UICONTROL X]** naast de locatie in de rechterkolom.
1. Klik op **[!UICONTROL Done]**.

>[!NOTE]
>
>* Niet alle landen hebben de locatie Staat, de plaats of de postcode.
>* DMA (aangewezen marktgebied), Federal Legislative Districts, en de Wetgevende Districten van de Staat zijn beschikbaar voor de plaatsen van de V.S. slechts.

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** inventarisbronnen die als doelen moeten worden opgenomen of uitgesloten. Voor de meeste plaatsingstypen worden alle voorraadtypen en alle bronnen voor elk type standaard opgenomen. Voor [!DNL Roku] plaatsingen, moet u het inventaristype en de bronnen specificeren. U kunt uit de volgende soorten inventaris kiezen:

* [!UICONTROL Public]: (Alle plaatsingstypen behalve Roku) Alle open-uitwisselingsinventaris waartoe DSP toegang heeft. U kunt openbare voorraad opnemen en uitsluiten.

  U kunt de lijst bekijken door bron of door voer. Wanneer u de lijst weergeeft op basis van feed, kunt u zoeken op naam van de feed, op basis van de feed of op basis van een geselecteerde kenmerkende tag.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: Uw bestaande privé overeenkomsten (of bestaande privé [!DNL Roku] overeenkomsten voor [!DNL Roku] plaatsen) met uitgevers die u opstelling in DSP hebt, en uw bestaande [ privé overeenkomstenlijsten ](/help/dsp/inventory/lists-deals-manage.md). U kunt een openbare voorraad opnemen, maar niet uitsluiten.

  Vanuit het tabblad [!UICONTROL Deals] kunt u de lijst doorzoeken op trefwoord, sleutel, deal-id of aangepaste tag. Van het [!UICONTROL Deal Lists] lusje, kunt u de lijst door naam van de overeenkomstenlijst of identiteitskaart van de overeenkomstenlijst zoeken.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: Alle [ premie, niet-gegarandeerde [!UICONTROL On Demand] inventaris ](/help/dsp/inventory/on-demand-inventory-about.md) (of [!UICONTROL On Demand] [!DNL Roku] overeenkomsten voor [!DNL Roku] plaatsen) waarop u in [!DNL DSP] hebt ingetekend. U kunt [!UICONTROL On Demand] voorraad opnemen en uitsluiten.

  U kunt de lijst bekijken door bron of door voer. Wanneer u de lijst op feed weergeeft, kunt u zoeken op naam van feed, feed-sleutel of een geselecteerd uitgeversgebied, een categorietag of een kenmerkende tag.

Opgeven welke inventarisdoelen worden gebruikt:

* Als u een voorraadtype wilt uitsluiten, schakelt u het selectievakje naast de naam uit.
* Een voorraadtype als doel instellen:
   1. Schakel het selectievakje naast de naam van het voorraadtype in.
   1. (Optioneel) Wijzig de bronnen in:
      1. Klik ![ uitgeven ](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] en [!UICONTROL On Demand] voorraad) Klik op **[!UICONTROL View by Source]** of **[!UICONTROL View by Feed]** om te wijzigen hoe de bronnen worden weergegeven.
      1. (Indien van toepassing) Filter de voorraad naar wens.
      1. Geef de bronnen op die u wilt opnemen en uitsluiten:
         * Voor [!UICONTROL Public] of [!UICONTROL On Demand] voorraad:
            * Als u een bron wilt opnemen, klikt u op **[!UICONTROL Include]** naast de naam van de bron.
            * Als u een bron wilt uitsluiten, klikt u op **[!UICONTROL Exclude]** naast de naam van de bron.
         * Voor [!UICONTROL Private] voorraad:
            * Op het tabblad [!UICONTROL Deals] :
               * Om al inventaris in een overeenkomst te omvatten, klik **[!UICONTROL Include all]** naast de overeenkomstennaam.
               * Om een individuele inventarisbron te omvatten, breid de overeenkomstennaam uit, en klik dan het controlevakje naast de bronnaam.
            * Voor het [!UICONTROL Deal Lists] lusje, klik de controledoos naast de naam van de overeenkomstenlijst.
   1. (Optioneel) Als u een CSV-bestand met de doelgegevens naar de downloadlocatie van uw browser wilt downloaden, klikt u op **[!UICONTROL Export]** .
   1. Klik op **[!UICONTROL Save]**.

>[!TIP]
>
>Als u zich hebt geabonneerd op de [!UICONTROL On Demand] -voorraad maar de uitgevers of deals niet als doel kunt instellen, controleert u de status van de deals. Voor meer informatie over statussen, zie [ Ongeveer  [!DNL On Demand]  Voorraad van de Premie ](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Video targeting]:** Doel (maar niet uitsluiten) voorraad door voorraadkenmerken. Wanneer u meerdere waarden voor hetzelfde videokenmerk als doel instelt, kunnen alle geselecteerde kenmerken worden aangewezen (bijvoorbeeld \[Player size = large OR Player size = HD\]). Wanneer u meerdere kenmerken als doel instelt, moet elk van de opgegeven kenmerken aanwezig zijn (bijvoorbeeld \[Duur = 30-60 min] EN \[Speler grootte = grote OF Player grootte = HD\]).

* **[!UICONTROL Player size]:** Doel (maar niet uitsluiten) voorraad per spelergrootte. De instelling is van toepassing op preroll-plaatsingen, voorlopige mobiele standaardplaatsingen en universele videoplaatsingen voor desktops en mobiele omgevingen. Standaard worden alle grootten als doelgrootten gebruikt. Om onderaan de doelstellingen te beperken, selecteer specifieke doelgrootte en/of *Onbekend*.

* **[!UICONTROL Playback mode]:** Doel (maar niet uitsluiten) voorraad door hoe het afspelen wordt geïnitieerd. De instelling is van toepassing op preroll-plaatsingen, voorlopige mobiele standaardplaatsingen en universele videoplaatsingen voor desktops en mobiele omgevingen. Standaard worden alle modi geactiveerd. Om onderaan de doelstellingen te beperken, selecteer specifieke doelwijzen en/of *Onbekend*.

* **[!UICONTROL Skippability]:** Doel (maar niet uitsluiten) inventaris volgens al dan niet het skippable is. De instelling is van toepassing op alle VAST/VPAID-plaatsingen, inclusief preroll, preroll voor mobiele apparatuur, aangesloten tv en universele videoplaatsingen. Standaard zijn alle opties geactiveerd. Om de doelstellingen te beperken, selecteer specifieke doelstellingen en/of *Onbekend*.

**[!UICONTROL Position targeting]:** Doel (maar niet uitsluiten) voorraad per advertentiepunt. De instelling is van toepassing op alle VAST/VPAID-plaatsingen, inclusief preroll, preroll voor mobiele apparatuur, aangesloten tv en universele videoplaatsingen. Standaard worden alle posities geactiveerd. Om onderaan de doelstellingen te beperken, selecteer specifieke doelposities en/of *Onbekend*.

## [!UICONTROL Site or App and Keyword Targeting]

**[!UICONTROL Traffic type]:** de types van verkeer aan doel. De opties zijn **[!UICONTROL Websites]** en **[!UICONTROL Apps]** .

**[!UICONTROL Tier]:** (Beschikbaar wanneer **[!UICONTROL Toggle for Sites or Apps Tiering]** *[!UICONTROL On]* is) de kwaliteit van het verkeer om te richten. Tiers 1-3 zijn allemaal merkveilig en zijn goedgekeurd door het DSP-kaartteam.

* *[!UICONTROL Tier 1]:* Premiumsites en -toepassingen die nationaal herkenbaar zijn.

* *[!UICONTROL Tier 2]:* richt Niveau 1 evenals kwaliteitsplaatsen en toepassingen die minder algemeen dan Reeks 1 bekend zijn.

* *[!UICONTROL Tier 3]:* richt Tiers 1-2 plus legitieme en merkveilige plaatsen en toepassingen die aan een nichepubliek aanpassen. Gebruik Niveau 3 voor bereik of gegevens die op aankopen gericht zijn.

* *[!UICONTROL All Sites or Apps]:* richt Tiers 1-3 en nieuwe inventaris die niet is onderzocht of gecategoriseerd, die u voor bereik kunt gebruiken.

>[!NOTE]
>
>Inventaris is specifiek voor de advertentie-eenheden in de plaatsing.

>[!TIP]
>
>Voor prestatiecampagnes, is de beste praktijken om *[!UICONTROL All Sites]* te selecteren.

**[!UICONTROL Site or App Categories]:** (Facultatieve) categorieën van de Plaats binnen de geselecteerde verkeerstypes en (indien gespecificeerd) de plaatslagen om of (maar niet allebei) als doelstellingen te omvatten of uit te sluiten. Maak een keuze uit verticale sitelijsten die door DSP zijn toegewezen op basis van het onderwerp:

1. Klik ![ uitgeven ](/help/dsp/assets/edit.png).
1. Geef de sitecategorieën op die u wilt opnemen of uitsluiten:
   * Sitecategorieën opnemen:
      1. Klik op **[!UICONTROL Include categories]**.
      1. Schakel het selectievakje naast elke categorie in die u wilt activeren.
   * Sitecategorieën uitsluiten:
      1. Klik op **[!UICONTROL Exclude categories]**.
      1. Schakel het selectievakje naast elke categorie in die u wilt uitsluiten.
1. (Optioneel) Als u een CSV-bestand met de doelgegevens naar de downloadlocatie van uw browser wilt downloaden, klikt u op **[!UICONTROL Export]** .
1. Klik op **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites or Apps]:** (Facultatief; beschikbaar wanneer **[!UICONTROL Toggle for Sites or Apps Tiering]** *[!UICONTROL On]*) Sites/apps en [ URL lijsten ](/help/dsp/resources/lists-url-manage.md) is om uit te sluiten. Via het tabblad [!UICONTROL Paste URL] kunt u naar sites zoeken en deze selecteren, of domeinnamen invoeren of plakken. Via het tabblad [!UICONTROL URL Lists] kunt u URL-lijsten selecteren.

1. Klik ![ uitgeven ](/help/dsp/assets/edit.png).
1. Geef de sites op:
   * Op het tabblad [!UICONTROL Paste URL] :
      * Ga als volgt te werk om een site te zoeken:
         1. Klik op **[!UICONTROL Search]**.
         1. Voer een trefwoord in, selecteer een sitelaag en/of selecteer een sitecategorie.
         1. Selecteer in de zoekresultaten de sites die u wilt uitsluiten:
            * Als u een afzonderlijke site wilt uitsluiten, schakelt u het selectievakje ernaast in.
            * (Als er meer dan 50 resultaten beschikbaar zijn) Klik op **[!UICONTROL Exclude these 50]** om de eerste 50 resultaten uit te sluiten. Om alle onderzoeksresultaten uit te sluiten, klik **[!UICONTROL Exclude these \<*NN *\>]**.
      * Domeinnamen invoeren:
         1. Klik op **[!UICONTROL Paste]**.
         1. Voer een of meer domeinnamen op afzonderlijke regels in.
         1. Klik op **[!UICONTROL Exclude All]**.
   * Op het tabblad [!UICONTROL URL Lists] :
      1. (Optioneel) Zoek naar een URL-lijst door de naam van de lijst geheel of gedeeltelijk in te voeren in het zoekveld.
      1. Schakel het selectievakje naast elke URL-lijst in die u wilt uitsluiten.
1. Klik op **[!UICONTROL Done]** wanneer u klaar bent.

>[!NOTE]
>
>* De rekening-niveau en adverteerder-vlakke geblokkeerde plaatslijsten worden ook toegepast, naast de DSP [ globaal geblokkeerde plaatsenlijst ](/help/dsp/introduction/features/brand-safety-media-quality.md), die plaatsen omvat die onveilig voor advertenties worden geacht.
>* Geblokkeerde sitelijsten overschrijven altijd de doelsites en sitelijsten. Als een plaatsing zowel het zelfde doel voor een advertentie uitsluit als omvat, dan wordt het doel uitgesloten.

**[!UICONTROL Context of Sites or App]:** (Facultatief) Contextuele doelsegmenten om te richten of uit te sluiten. Selecteren in de volgende lijst

* **[!UICONTROL Marketplace]** tab: geeft [!DNL Peer39] segmenten weer die voor de opgegeven kosten beschikbaar zijn voor alle gebruikers.

* **[!UICONTROL Custom Segments]** tab: geeft de [!DNL Peer39] aangepaste segmenten van uw organisatie weer.

* **[!UICONTROL Paste Segments]** tab: (Advertisers wiens organisaties [!DNL Comscore] partnership hebben; beschikbaar na activering van uw Adobe-accountteam) Voer een of meer segment-id&#39;s of segmentnamen in voor de contextafhankelijke segmenten van uw organisatie. [!DNL Comscore] Scheid meerdere waarden met komma&#39;s (zoals Segment1,Segment2, Segment3).

**[!UICONTROL Language]:** (Facultatief) één enkele taal aan doel.

**[!UICONTROL Site or app list preview]:** (Alleen-lezen; beschikbaar als **[!UICONTROL Toggle for Sites or Apps Tiering]** *[!UICONTROL On]* is) Alle beoogde en geblokkeerde sites/apps voor de plaatsing, inclusief sites/apps op accountniveau, lijsten met geblokkeerde sites op adverteerderniveau en lijsten met geblokkeerde sites op DSP-niveau.

U kunt de lijst met doelsites en geblokkeerde sites optioneel exporteren als een CSV-bestand (comma-separated values, door komma&#39;s gescheiden waarden). Als u de lijst wilt exporteren, klikt u op **[!UICONTROL Export full site list]** en opent of slaat u het bestand op volgens de normale procedure van uw browser.

**[!UICONTROL Allow unscreened sites]:** (Alleen de standaardweergave) Hiermee schakelt u levering en levering in op niet-gecontroleerde sites. Wanneer de plaatsing privé-inventarisatie als doel heeft, kan deze optie advertenties op geblokkeerde sites leveren.

**[!UICONTROL Toggle for Sites or Apps Tiering]:** Hiermee kunt u site- of toepassingslagen opgeven om deze te activeren of uit te sluiten.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Om het even welke publieksdoelstellingen voor de plaatsing, met inbegrip van [ derdesegmenten, eerste-partijsegmenten, de segmenten van Adobe, douanesegmenten, en bewaard publiek ](/help/dsp/audiences/audience-settings.md). De totale en actieve gededupliceerde publieksgrootte voor alle geselecteerde segmenten en opgeslagen doelgroepen wordt ook weergegeven. U kunt een bestaand publiek selecteren, een publiek maken dat u later opnieuw kunt gebruiken of specifieke publiekssegmenten selecteren:

* Om een bestaand publiek te selecteren, klik ![ Uitgezocht ](/help/dsp/assets/chevron-down.png) naast [!UICONTROL Included Audiences], en selecteer dan het publiek.
* Om een publiek tot stand te brengen, klik ![ Uitgezocht ](/help/dsp/assets/chevron-down.png) naast [!UICONTROL Included Audiences], en selecteer dan **[!UICONTROL + Create Audience]**. Voor instructies, zie [ een Herbruikbaar publiek ](/help/dsp/audiences/reusable-audience-create.md) creëren, die met Stap 3 beginnen.
* Klik op **[!UICONTROL Select segments for this placement only]** om specifieke publiekssegmenten te selecteren. Selecteer de segmentlogica; voor instructies, zie Stap 6 in &quot;[ een Herbruikbaar publiek ](/help/dsp/audiences/reusable-audience-create.md) creëren.&quot; Wanneer u wordt gedaan, klik **sparen**.

>[!NOTE]
>
>De segmenten van eerste-partij RampID die niet aan een actieve, geplande, of gepauzeerde plaatsing in bijlage zijn worden gepauzeerd. Het segment wordt in de segmentlijst genoteerd als &quot;Automatisch gepauzeerd&quot;.

**[!UICONTROL Excluded Audiences]:** Om het even welk publiek om voor de plaatsing uit te sluiten, met inbegrip van publiek met [ derdesegmenten, eerste-partijsegmenten, de segmenten van Adobe, douanesegmenten, en bewaard publiek ](/help/dsp/audiences/audience-settings.md). De totale en actieve gededupliceerde publieksgrootte voor alle uitgesloten doelgroepen wordt ook weergegeven. U kunt een bestaand publiek selecteren of een nieuw publiek maken dat u later opnieuw kunt gebruiken:

* Om een bestaand publiek te selecteren, klik ![ Uitgezocht ](/help/dsp/assets/chevron-down.png) naast [!UICONTROL Excluded Audiences], en selecteer dan het publiek.

* Om een publiek tot stand te brengen, klik ![ Uitgezocht ](/help/dsp/assets/chevron-down.png) naast [!UICONTROL Excluded Audiences], en selecteer dan **+ leidt tot Audience**. Voor instructies, zie [ een Herbruikbaar publiek ](/help/dsp/audiences/reusable-audience-create.md) creëren, die met Stap 3 beginnen.

**[!UICONTROL Targeting]:** De typen gebruikers-id&#39;s die u als doel wilt instellen. U kunt deze instelling niet wijzigen nadat de plaatsing live is (dus nadat de vlucht is gestart).

Wanneer je zowel oude als universele id&#39;s selecteert, krijgt universele id&#39;s de voorkeur voor biedingen.

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*: (De standaardinstelling) richt zich op gebruikers op basis van hun cookies, mobiele advertentie-id&#39;s of aangesloten tv-id&#39;s (CTV). De id&#39;s worden geselecteerd op basis van de browser, in-app of CTV-inventaris.

* *[!UICONTROL Universal ID Beta]*: doel op de privacy van gebruikers. Selecteer één id-type. De beschikbare opties worden bepaald door de geselecteerde geografische doelen in de sectie [!UICONTROL Geo-Targeting] . Gebruik met [[!DNL RampID]  segmenten die direct in DSP ](/help/dsp/audiences/sources/source-import-liveramp-segments.md) worden ingevoerd, [ segmenten waarvoor DSP uw PII in universele IDs ](/help/dsp/audiences/sources/source-about.md) omzet, of [ douanesegmenten die universele IDs ](/help/dsp/audiences/custom-segment-create.md) volgen.

   * *[!UICONTROL ID5]*: doelen voor [!DNL ID5] id&#39;s die waarschijnlijk zijn gemaakt op basis van e-mailadressen en andere signalen.<!-- What countries/geos are these available for? Everywhere?--> ID5-id&#39;s zijn gratis beschikbaar. **Nota:** De segmenten van de derdepartij van [!DNL Eyeota] kunnen ID5 IDs omvatten.

   * *[!UICONTROL RampID]*: doelen [!DNL LiveRamp] [!DNL RampIDs] van gebruikers die zich via hun e-mailadres bij uw site hebben aangemeld. <!-- Verify --> [!DNL RampIDs] zijn beschikbaar voor gebruikers in Noord-Amerika, Australië en Nieuw-Zeeland.

   * *[!UICONTROL Unified ID2.0]*: doel [!DNL Unified ID2.0] (UID2) id&#39;s van gebruikers die zich bij uw site hebben aangemeld met hun e-mailadres.<!-- Verify -->[!DNL UID2 IDs] zijn niet beschikbaar voor gebruikers in de Europese Economische Ruimte en enkele andere landen. Zie de [ lijst van verboden landen ](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  **[!UICONTROL Terms of service]**: De serviceovereenkomst voor het gebruik van universele id&#39;s. Je of een andere gebruiker in de DSP-account moet de voorwaarden één keer accepteren voordat je gegevens kunt converteren naar een nieuw ID-type. Voor klanten met beheerde servicecontracten krijgt uw Adobe-accountteam uw toestemming en accepteert u de voorwaarden namens uw organisatie. Om de termijnen te lezen, klik **>**. Schuif naar de onderkant van de voorwaarden en klik op **[!UICONTROL Accept]** om de voorwaarden te accepteren.

**[!UICONTROL Cross Device Targeting]:** (Beschikbaar wanneer de [ campagne voor op mensen-gebaseerd dwars-apparaat richtend ](/help/dsp/campaign-management/campaigns/campaign-settings.md) wordt gevormd, richt u erfenis IDs slechts (niet universele IDs), en u selecteert minstens één segment of publiek. Staat u toe om uw het richten over alle bekende apparaten van een persoon (per de apparatengrafiek uit te breiden die in de campagnemontages wordt gespecificeerd), zelfs apparaten die niet in de gespecificeerde segmenten zijn. De kosten kunnen van toepassing zijn afhankelijk van de grafiek die voor de campagne wordt gespecificeerd. Apparaatgrafiekgegevens zijn alleen beschikbaar in Noord-Amerika.

**[!UICONTROL Placement Cap]:** (Optioneel) Het aantal keren dat een uniek apparaat, een universele id of een persoon (afhankelijk van de opgegeven [!UICONTROL Cross Device Level] voor de campagne en de instelling [!UICONTROL Targeting] van de plaatsing) advertenties van de plaatsing kan ontvangen. U kunt kiezen uit *[!UICONTROL Unlimited]* of een bepaald bedrag per dag, week of maand.

>[!NOTE]
>
> U kunt frequentiecappen instellen op campagne-, pakket- en plaatsingsniveaus. DSP respecteert de strengste frequentiegrens in de campagnehiërarchie.

**[!UICONTROL Secondary Cap]:** (Optioneel; beschikbaar als u een numerieke waarde toevoegt [!UICONTROL Placement Cap]) Een extra beperking binnen de grenzen van de primaire plaatsingslimiet. Selecteer het aantal afbeeldingen en de tijdsperiode (bijvoorbeeld 3 per 12 uur).

**[!UICONTROL Day Parting]:** (Optioneel) Specifieke dagen van de week en het tijdstip van de dag waarop advertenties kunnen worden uitgevoerd. De zomerintervallen opgeven:

1. Klik ![ uitgeven ](/help/dsp/assets/edit.png).
1. Selecteer de toepasselijke tijdzone.
1. Geef de intervallen op:
   * Klik op een van de intervalknoppen om een vooraf ingesteld interval te selecteren. U kunt onder andere *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]* , *[!UICONTROL Morning]* , *[!UICONTROL Lunch]* , *[!UICONTROL Dinner]* of *[!UICONTROL Prime]* (primetime) kiezen.
   * Als u handmatig een interval wilt selecteren, klikt u in een cel en sleept u optioneel om het interval te selecteren.
1. Klik op **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Optioneel; beschikbaar voor adverteerders die zijn geconfigureerd met [!DNL Proximic by Comscore] segmenten) Specifieke segmentnamen of id&#39;s van [!DNL Proximic by Comscore] voor opname als doelen. Voor deze functie kunnen extra kosten in rekening worden gebracht. Neem contact op met uw Adobe-accountteam om deze functie te activeren en onderwerpsegmenten in te stellen.

Onderwerpgerichte onderwerpen opgeven:

1. Klik ![ uitgeven ](/help/dsp/assets/edit.png).
1. Geef de gewenste segmenten op:
   1. In de linkerkolom, selecteer de partner: (*[!UICONTROL Comscore]*.
   1. Voer in het invoerveld de segmentnamen of segment-id&#39;s in.
1. (Optioneel) Als u een CSV-bestand met de onderwerpgegevens wilt downloaden naar de downloadlocatie van uw browser, klikt u op **[!UICONTROL Export]** .
1. Klik op **[!UICONTROL Save]**.

>[!TIP]
>
>* Objectgerichte aanbiedingen beperken de voorraad waarop de plaatsing kan bieden. Gebruik daarom onderwerpen die voor slechts een klein percentage van de totale aankoop zijn bestemd.
>
>* Stel eventuele negatieve doelen in binnen het segment op [!DNL Proximic by Comscore] .

**[!UICONTROL Device Targeting]:** (Facultatieve) Specifieke apparateninformatie, met inbegrip van apparatentypen, fabrikanten, werkende systemen, browsers, en connectiviteitstypes, om als doelstellingen te omvatten en uit te sluiten. De typen variëren per plaatsingstype. Apparaatdoelframes opgeven:

1. Klik ![ uitgeven ](/help/dsp/assets/edit.png).
1. Geef de apparaatdetails op die u wilt opnemen en uitsluiten:
   1. Selecteer de categorie in de linkerkolom.
   1. Doelstelling opgeven:
      * Klik op **[!UICONTROL Include]** naast de naam van de waarde als u een waarde wilt opnemen.
      * Als u een waarde wilt uitsluiten, klikt u op **[!UICONTROL Exclude]** naast de naam van de waarde.
1. (Optioneel) Als u een CSV-bestand met de doelgegevens van het apparaat naar de downloadlocatie van uw browser wilt downloaden, klikt u op **[!UICONTROL Export]** .
1. Klik op **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Facultatieve) specifieke Internet dienstverlener (ISPs) om of (maar niet allebei) als doelstellingen te omvatten of uit te sluiten. Om ISP het richten te specificeren:

1. Klik ![ uitgeven ](/help/dsp/assets/edit.png).
1. Specificeer ISPs om te omvatten of uit te sluiten:
   * ISPs omvatten:
      1. Klik op **[!UICONTROL Include ISPs]**.
      1. (Optioneel) Filter de lijst op trefwoord.
      1. Selecteer de controledoos naast elke ISP aan doel.
   * ISPs uitsluiten:
      1. Klik op **[!UICONTROL Exclude ISPs]**.
      1. (Optioneel) Filter de lijst op trefwoord.
      1. Selecteer de controledoos naast elke ISP om uit te sluiten.
1. (Optioneel) Als u een CSV-bestand met de ISP-doelgegevens wilt downloaden naar de downloadlocatie van uw browser, klikt u op **[!UICONTROL Export]** .
1. Klik op **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Quality]

**[!UICONTROL DoubleVerify ABS segment ID]:** (Facultatief; [!DNL DoubleVerify] klanten slechts; beschikbaar voor pre-rol van de Desktop, standaard en klik-aan-spel vertoning, en inheemse vertoning en videoplaatsen slechts; niet gesteund voor [ standaard programmatic gewaarborgde Plaatsen voor overeenkomsten ](/help/dsp/inventory/programmatic-guaranteed-about.md)) A [!DNL DoubleVerify Authentic Brand Safety] segment ID verbonden aan de rekening van organisatie [!DNL DoubleVerify] voor de plaatsing te gebruiken. Het specificeren van een identiteitskaart blokkeert impressies na-bieding gebruikend de veiligheidsregels van het douanemerk die voor gespecificeerde segment ID worden gevormd. DSP factureert uw account voor gebruik voor de segment-id.

De id moet beginnen met &quot;51&quot; en uit acht cijfers bestaan. Als een segment-id standaard is opgegeven in de accountinstellingen van de adverteerder, wordt de id op adverteerderniveau ingevoerd, maar u kunt de id wijzigen in een ander segment of de id verwijderen om de functie uit te schakelen.

**[!UICONTROL Contextual filtering]:** (Van toepassing op desktopcomputers en mobiele webweergaven, eigen advertenties en video&#39;s) Typen [!DNL Comscore] -, [!DNL DoubleVerify] -, [!DNL Integral Ad Science] - en [!DNL Peer39] contextafhankelijke filters die moeten worden toegepast. De standaardinstellingen op adverteerderniveau worden geselecteerd voor nieuwe plaatsingen, maar u kunt de instellingen wijzigen:

<!-- Looks like we didn't rename this:
**[!UICONTROL Brand Safety categories]:** Types of [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39] brand safety category filters to apply. The advertiser-level defaults are selected for new placements, but you can change the settings:
-->

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Facultatief) Één of meerdere soorten voorraadcontext om door gebrek te blokkeren. Er kunnen extra kosten van toepassing zijn.

* [!UICONTROL Peer 39]:

   * **plaatsen van het Doel die zijn:** (Facultatief) Één of meerdere soorten inventarisattributen aan doel door gebrek. Er kunnen extra kosten van toepassing zijn.

* [!UICONTROL ComScore]:

   * **de plaatsen van het Blok die zijn:** (Facultatief) Één of meerdere types van inventarisattributen om door gebrek te blokkeren. Er kunnen extra kosten van toepassing zijn.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Optioneel) De mate van inhoud voor volwassenen waarvoor standaardadvertenties moeten worden geblokkeerd: *[!UICONTROL Do Not Block]* (de standaardinstelling), *[!UICONTROL Standard]* of *[!UICONTROL Strict]* . Er kunnen extra kosten van toepassing zijn.

   * **[!UICONTROL Alcohol Content]:** (Optioneel) De mate van het alcoholgehalte waarvoor advertenties standaard worden geblokkeerd: *[!UICONTROL Do Not Block]* (de standaardwaarde), *[!UICONTROL Standard]* of *[!UICONTROL Strict]* . Er kunnen extra kosten van toepassing zijn.

**[!UICONTROL Pre-bid fraud blocking]:** Typen sites die worden geblokkeerd op basis van frauduleus verkeer en verdachte activiteiten die worden gemeten via [!DNL DoubleVerify] , [!DNL Integral Ad Science] en [!DNL Peer39] . De standaardinstellingen op adverteerderniveau worden geselecteerd voor nieuwe plaatsingen, maar u kunt de instellingen wijzigen:

* [!UICONTROL DoubleVerify]: (Van toepassing op desktopcomputers en mobiele webweergaven, eigen tv-advertenties, video-advertenties en standaardadvertenties op aangesloten tv)

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Door gebrek, blokkeert al 100% ongeldig verkeer, met inbegrip van verkeer op gekaapte apparaten, voor nieuwe plaatsingen. Er kunnen extra kosten van toepassing zijn.

   * **[!UICONTROL Also block sites with]:** (Optioneel) Een extra niveau van fraude en ongeldig verkeer waardoor DSP advertenties standaard blokkeert: *[!UICONTROL None]* (de standaardinstelling, die geen extra verkeer blokkeert), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* of *[!UICONTROL >25% Average Fraud/IVT levels]* . Er kunnen extra kosten van toepassing zijn.

* [!UICONTROL Peer 39]: (Van toepassing op desktopcomputers en mobiele webweergaven, eigen advertenties en videoclips)

   * **[!UICONTROL Block sites that are]:** (Optioneel) Een of meer soorten fraude waardoor DSP standaard advertenties blokkeert: *[!UICONTROL Fraud]* (die alle sites blokkeert met fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* en/of *[!UICONTROL Fraud: Zero Ads]* . Er kunnen extra kosten van toepassing zijn.

* [!UICONTROL Integral Ad Science]: (Van toepassing op desktopcomputers en mobiele webweergaven, eigen advertenties en videoclips)

   * **[!UICONTROL Block sites that are]:** (Optioneel) Een type verdachte website- of app-activiteit waardoor DSP advertenties standaard blokkeert: *[!UICONTROL None]* (de standaardinstelling, die advertenties niet blokkeert op basis van verdachte activiteiten), *[!UICONTROL Suspicious Activity - High Risk]* of *[!UICONTROL Suspicious Activity - High or Moderate Risk]* . Er kunnen extra kosten van toepassing zijn.

**[!UICONTROL Pre-bid viewability]:** (Van toepassing op desktopcomputers en mobiele webweergaven, eigen advertenties en videobanden) Welke filters voor weergave vooraf bieden door [!DNL DoubleVerify] en [!DNL Integral Ad Science] die moeten worden toegepast voor de plaatsing. De standaardinstellingen op advertentieniveau worden geselecteerd voor nieuwe plaatsingen, maar u kunt de instellingen wijzigen. Er kunnen extra kosten van toepassing zijn.

**[!UICONTROL Ads.txt filtering]:** (Van toepassing op Desktop en mobiele Webvertoning, inheems, video, en audioadvertenties) Welk niveau van [ Ads.txt ](https://iabtechlab.com/ads-txt-about/) pre-bid het filtreren door de Erkende lijst van Digitale Verkopers van elke uitgever toe te passen. De standaardinstelling op advertentieniveau is geselecteerd voor nieuwe plaatsingen, maar u kunt de instellingen wijzigen:

* *[!UICONTROL Opt out of ads.txt (default)]*: voorraad kopen van alle verkopers.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: prioriteit geven aan inkoopvoorraad van geautoriseerde directe verkopers en wederverkopers van een domein.
* *[!UICONTROL Ads.txt sellers only]*: voorraad alleen kopen bij geautoriseerde directe verkopers en wederverkopers van een domein.
* *[!UICONTROL Ads.txt sellers only]*: voorraad alleen kopen bij geautoriseerde directe verkopers van een domein.

**[!UICONTROL Attention Targeting]:** (Van toepassing op desktopcomputers en mobiele webweergaven, video en standaard aangesloten tv-advertenties) [!DNL Adelaide] Hiermee kunt u vooraf biedende segmenten met een specifiek concentratieniveau (hoog, gemiddeld of laag) benaderen op basis van de opgegeven site, indeling en advertentiegrootte. De segmenten worden wekelijks bijgewerkt. **Nota:** Gebruikend [!DNL Adelaide] segmenten voor het richten maakt een CPM vergoeding voor elke indruk die met [!DNL Adelaide] aandacht het richten wordt geleverd; dit tarief is gescheiden van kosten voor [ aandachtmeting ](/help/dsp/campaign-management/campaigns/campaign-settings.md). Voor interactieve pre-roll plaatsingen, wordt u slechts voor VAST beelden in rekening gebracht.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] plaatsen) Externe leveranciers van trackingservices die zijn goedgekeurd door [!DNL Roku] include [!DNL Acxiom] , [!DNL Comscore], [!DNL Data Plus Math] , [!DNL Experian], [!DNL Factual] , [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] en [!DNL Research Now] .

**[!UICONTROL Event Pixels]:** (Optioneel) Pixels voor het bijhouden van gebeurtenissen van derden die standaard aan alle nieuwe advertenties in de plaatsing moeten worden gekoppeld. Gebeurtenispixels opgeven:

1. Klik ![ uitgeven ](/help/dsp/assets/edit.png).
1. Voer een van de volgende handelingen uit:
   * Als u een bestaande pixel wilt selecteren, schakelt u het selectievakje in de pixelrij in.
   * Een pixel maken:
      1. Klik op **[!UICONTROL Create]**.
      1. Voer de volgende gegevens in:
         * **[!UICONTROL Pixel name]:** De pixelnaam; de maximumlengte is 500 karakters. Gebruik een naam waarmee u de pixel gemakkelijk kunt herkennen.
         * **[!UICONTROL Pixel event fires on]:** De gebeurtenis die de pixel in brand zet. De beschikbare gebeurtenissen variëren per advertentietype.
         * **[!UICONTROL Pixel type]:** Of de pixel een *[!UICONTROL IMG URL]* (1x1 pixelafbeeldingsbestand), *[!UICONTROL HTML]* of *[!UICONTROL JavaScript URL]* is.
         * **[!UICONTROL Pixel URL]:** De URL van de pixelafbeelding.
      1. Klik op **[!UICONTROL Create and attach]**.
   1. Klik op **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Optioneel) Conversie van pixels die standaard aan alle nieuwe advertenties in de plaatsing worden gekoppeld. Omzetpixels opgeven:

1. Klik ![ uitgeven ](/help/dsp/assets/edit.png).
1. Voer een van de volgende handelingen uit:
   * Als u een bestaande pixel wilt selecteren, schakelt u het selectievakje in de pixelrij in.
   * Een pixel maken:
      1. Klik op **[!UICONTROL Create]**.
      1. Voer de volgende gegevens in:
         * **[!UICONTROL Conversion pixel name]:** De pixelnaam; de maximumlengte is 500 karakters. Gebruik een naam waarmee u de pixel gemakkelijk kunt herkennen.
         * **[!UICONTROL Conversion category]:** Het type conversie.
         * **[!UICONTROL Impression conversion window]:** Het aantal dagen na een advertentie waarin de indruk aan een omzetting kan worden toegeschreven. De standaardwaarde is 30 dagen.
         * **[!UICONTROL Click conversion window]:** Het aantal dagen na een advertentie waarop de klik kan worden toegewezen aan een conversie. De standaardwaarde is 30 dagen.
         * **[!UICONTROL Notes]:** (Optioneel) Een beschrijving of andere informatie over de pixel.
      1. Klik op **[!UICONTROL Create and attach]**.
      1. Implementeer de conversiepixel op de relevante webpagina&#39;s:
         1. Ga in het hoofdmenu naar **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]** .
         1. Klik in de pixelrij op **[!UICONTROL edit]** .
         1. Kopieer zo nodig de waarde(n) in de velden [!UICONTROL HTML Tag] en [!UICONTROL Flash Tag] om de adverteerder of de websitecontactpersoon te voorzien.

            De IT-afdeling of andere groep van de adverteerder moet mogelijk de implementatie van de tag plannen of hierover worden geïnformeerd.
   1. Klik op **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Facultatief) een statisch tarief van de derdelengrijs dat als niet factureerbare kosten per 1000 beelden moet worden gevolgd. De standaardinstelling op pakketniveau wordt, indien van toepassing, automatisch toegepast op nieuwe plaatsingen, tenzij u een andere waarde opgeeft.

>[!NOTE]
>
>Billable-kosten worden weergegeven in de [!UICONTROL Net CPM] -norm.

>[!MORELIKETHIS]
>
>* [ Ongeveer het Beheer van de Plaatsing ](placement-about.md)
>* [ creeer een Plaatsing ](placement-create.md)
>* [ geeft Plaatsen ](placement-edit.md) uit
>* [ beheert Bodmultipliers voor Plaatsingen ](placement-manage-bid-multipliers.md)
>* [ Mening het Logboek van de Verandering voor een Plaatsing ](placement-change-log.md)
>* [ Sneltoetsen ](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [ Veelgestelde vragen over het Beheer van de Campagne ](/help/dsp/campaign-management/faq-campaign-management.md)
