---
title: Beste praktijken voor de Campagnes van Prestaties van de Opstelling
description: Leer beste praktijken voor het opzetten van uw prestaties-gerichte campagnes, die plaatsingen omvatten die voor laagste CPA of hoogste ROAS worden geoptimaliseerd.
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---

# Beste praktijken voor de Campagnes van Prestaties van de Opstelling

DSP kan uw prestatiegerichte campagnes optimaliseren. Raadpleeg de volgende aanbevolen procedures voor prestatiecampagnes:

* Stap 1 - Bepaal uw Doel
* Stap 2 - Definieer uw strategie
* Stap 3 - Pakketten maken
* Stap 4 - Plaatsingsstructuur maken
* Stap 5 - De juiste Creative Assets gebruiken

## Stap 1 - Bepaal uw doel

Het is belangrijk om het doel van de campagne te begrijpen, zoals het bereiken van hoogst mogelijke ROAS of laagst mogelijke CPA. De campagnes van prestaties hebben de [&#x200B; optimalisatiedoelstellingen &#x200B;](/help/dsp/optimization/optimization-goals.md) &quot; [!UICONTROL Highest Return on Ad Spend (ROAS)"] of &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)].&quot; Geef voor elk pakket in de campagne dienovereenkomstig het optimalisatiedoel op.

![&#x200B; optimalisatiedoel &#x200B;](/help/dsp/assets/optimization-goals.png)

U moet ook de succesgebeurtenis(sen) bepalen die tot het algemene doel leiden en dienovereenkomstig aangepaste doelen maken. Geef voor elk pakket een aangepast doel op dat moet worden gebruikt met het algemene optimalisatiedoel voor rapportage en algoritmische optimalisatie met [!DNL Adobe AI] . Voor meer informatie over het creëren van douanedoelstellingen, met inbegrip van beste praktijken, zie [&#x200B; Doelen van de Douane &#x200B;](custom-goal.md).

## Stap 2 - Bepaal uw strategie

### Verkennende strategieën

De pakketten van de funnel in de eerste plaats bevatten plaatsen die zeer breed zijn gericht op het bereiken van nieuwe consumenten.

#### Aanbevolen plaatsingsstrategieën voor prospectie

* Zoek naar nieuwe soorten publiek die met de volgende tactieken kunnen worden omgezet:

   * Modellering van look-alike van een platform van het gegevensbeheer (DMP), zoals Adobe Audience Manager.
   * Gedragingen waarbij gegevens van derden worden gebruikt.
   * Contextafhankelijke doelframes.
   * Doellocatie/categorie.

* De looppas van het gebruik van netwerk (RON) richtend: Het is belangrijk om een looppas van netwerkplaatsing zonder publiek te omvatten richtend en met brede inventarisgericht. Hierdoor kan het algoritme met [!DNL Adobe AI] waardevolle gebruikers vinden die nieuwere cookies hebben die nog niet in een publiek zijn gecategoriseerd.

### Strategieën opnieuw rangschikken

Lagere funnel-pakketten bevatten plaatsen die gebruikers betreffen die al op de webpagina van de adverteerder zijn geweest of waarvoor de adverteerder CRM-gegevens heeft.

#### Aanbevolen plaatsingsstrategieën voor opnieuw toewijzen

* Als de adverteerder een Adobe Analytics- of Adobe Audience Manager-klant is, kunt u eerste-partijsegmenten (zoals bezoekers van de homepage, productpagina&#39;s of winkels voor winkelwagens) maken en deze gebruiken als plaatsingsdoelen in DSP.

* Vermijd het toewijzen van te veel budget aan een doelgerichte plaatsing. Als algemene regel geldt dat budget $30 per 1.000 gebruikers per maand bedraagt.

## Stap 3 - Pakketten maken

De beste praktijken moeten afzonderlijke pakketten voor het hogere funnel prospecteren en voor het lagere herrichten van funnel tot stand brengen. Optimalisatie vindt plaats op pakketniveau, zodat de prestatiegegevens van alle plaatsen binnen een pakket worden samengevoegd. Daarom groepeert u plaatsingen in pakketten met vergelijkbare verwachte prestaties.

![&#x200B; voorbeeld van afzonderlijke pakketten voor het prospecteren en het opnieuw richten &#x200B;](/help/dsp/assets/p-r.png)

Gebruik ook de volgende instellingen.

### Doelstellingen en budget

* **Pacing &amp; het Afschilderen:** om een CPA of het optimalisatiedoel van ROAS te selecteren, moet het pakket pakket-vlakke het oppassen gebruiken. Dit zorgt ervoor dat alle plaatsen binnen het pakket worden geoptimaliseerd om uitgaven op basis van prestaties en schaal aan de geselecteerde doelstellingen te verdelen.

* **Datums van de Vlucht:** (Verkennende pakketten) wanneer uw campagne langer dan 25 dagen loopt, gebruik de [!UICONTROL Activate Custom Flighting] eigenschap. Eerst, plaats een douanevlucht voor de eerste 10 dagen bij ongeveer 75% van het noodzakelijke dagelijkse budget om uitgaven tijdens de *het leren fase* te verminderen. Stel vervolgens een tweede aangepaste vlucht in voor de rest van de begroting.

  Als u bijvoorbeeld $100.000 wilt besteden in 30 dagen, stelt u het budget voor vlucht 1 (dagen 1-10) in op $25.000 (75% x $100.000/30 dagen = $2.500 per dag). Gebruik het resterende budget van $75.000 voor Vlucht 2 (Dagen 11-30).

* **Begroting:** DSP probeert altijd om 100% van het pakketbudget gelijkmatig tussen alle plaatsen in een pakket toe te wijzen. Als een baan weinig of geen uitgaven heeft, adviseren wij begroting die de plaatsing begrenzen om meer van het budget toe te staan om aan stages met schaal toe te wijzen. 24-48 uur toestaan voor begrotingswijzigingen.

* **Doelstellingen van de Optimalisering:** gebruik één van de twee doelstellingen van de prestatiesoptimalisering, *[!UICONTROL Highest Return on Ad Spend]* of *[!UICONTROL Lowest Cost per Acquisition]*, afhankelijk van het pakketdoel. Met deze doelen wordt het pakket automatisch geoptimaliseerd in de richting van respectievelijk de beste ROAS- of laagste CPA-plaatsing.

* **Doelen van de Douane:**
   * Als een nieuw pakket hetzelfde doel heeft als een bestaand pakket, kunt u optioneel het bestaande pakket koppelen, zodat het algoritme de bestaande leergegevens voor computers kan gebruiken.
   * Voer de juiste [!UICONTROL Target CPA] of [!UICONTROL Target ROAS] in.

* **Vlucht het Pacing en Intraday het Pacing:** voor beide types van het Pakkeren, selecteer *[!UICONTROL Even]* om uw prestatiesdoelstellingen te maximaliseren door uniform door elke dag en door de volledige vlucht te passen.

  >[!CAUTION]
  >
  >Gebruik *[!UICONTROL FrontLoad]* en *[!UICONTROL Aggressive Front Load]* voor het plaatsen van vluchten en *[!UICONTROL ASAP]* het plaatsen voor intraday-pacing slechts wanneer u volledig voorrang geeft aan levering en besteedt over prestatiesoptimalisering omdat die strategieën negatieve gevolgen voor uw gewenste prestaties KPIs kunnen hebben.

## Stap 4 - Plaatsingsstructuur maken

Minder is meer. Als u minder dan zes plaatsen per pakket kunt instellen, dan kan het beschikbare budget dynamisch verschuiven naar de best presterende plaatsen het gemakkelijkst.

Zorg er ook voor dat u elke plaatsing aan een pakket met het doeltype van het pakket *[!UICONTROL Prospecting]* of *[!UICONTROL Retargeting]* toevoegt.

Hieronder vindt u de aanbevolen plaatsingsinstellingen voor prestatiecampagnes.

### Doelen

U moet CPA of ROAS optimalisering op het pakketniveau vormen (zie Stap 3 - creeer Pakketten), maar u kunt extra plaatsing-vlakke montages toevoegen.

* **Maximale BOD:**
   * Gebruik een laag maximumbod ($5) voor het zoeken naar plaatsen.
   * Gebruik een hoog maximumbod ($12) als u plaatsingen opnieuw wilt toewijzen.

* **Vooraf biedende Filters:** minimaliseer, of vermijd idealiter, plaatsend agressieve voorbiedingsfilters, die de plaatsing verhinderen schaal te bereiken. De beste praktijken omvatten het volgende:

   * Gebruik één (1) voorbiedingsfilter per plaatsing. Wanneer u meerdere filters voor een voorbod gebruikt, moet aan beide voorwaarden worden voldaan, waardoor de schaal afneemt.

   * U kunt minder strikte voorbiedingsfilters instellen in gevallen waarin extra doelframes (zoals publiek, geo en doellocatie) worden toegepast.

Zie beschrijvingen van wanneer om elk pre-bieder filter op [&#x200B; plaats-vlakke pre-Biedfilters te gebruiken en hoe te om hen &#x200B;](/help/dsp/optimization/optimization-pre-bid-filters.md) te gebruiken.

### Inventaris

Gebruik [!UICONTROL Public] (Open Exchange) en [!UICONTROL On Demand] -voorraad om de schaal te maximaliseren.

### Sitedoelen

* **[!UICONTROL Traffic Type]** : [!UICONTROL Websites] alleen
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### Doelgerichtheid publiek

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * Voor prospectieve plaatsingen, groepeer gelijkaardige publiekscategorieën en gelijkaardige publieksgrootte in één plaatsing. Voer vervolgens op basis van prestaties een van de volgende handelingen uit:
      * Verwijder ondermaats presterende soorten publiek uit bestaande plaatsen.
      * Verplaats toppresterende doelgroepen naar een aparte plaatsing voor betere beheerbudgetten.
   * Voor het opnieuw plaatsen, zou u idealiter één publiekssegment per plaatsing moeten omvatten om biedingen en begroting gemakkelijk te controleren.

>[!NOTE]
>
>Uw advertenties presteren het best als een gebruiker door slechts één plaatsing kan worden bereikt. Een aanzienlijke overlapping van gebruikers tussen verschillende plaatsen kan concurrentie veroorzaken, wat een cyclus van voortdurend stijgende biedingen oplevert, waardoor de kosten per gebruiker stijgen. Daarom als u veelvoudige publiek omvat, zorg ervoor zij niet uit overlappende gebruikers/publieksleden bestaan.
>
> U kunt overlappende soorten publiek voorkomen door uw publiek in lagen te maken, zodat u de hogere, meer inclusieve lagen van plaatsingen desgewenst kunt onderdrukken.

* **[!UICONTROL Frequency Capping]:**
   * Gebruik voor prospectie van plaatsingen krappe frequenties (één indruk per dag).
   * Stel voor het opnieuw plaatsen de primaire plaatsingsdop in op 6-10 indrukkingen per dag en de secundaire dop op 1 indruk per uur.

* **[!UICONTROL Device Targeting]**:
   * Neem [!UICONTROL Computer], [!UICONTROL Mobile] en [!UICONTROL Tablet] op.
   * Niet richten [!UICONTROL Firefox] en [!UICONTROL Safari] wegens het richten en metingsbeperkingen. Neem contact op met uw Adobe-accountteam voor meer informatie over [!DNL Adobe] ondersteuning voor [!DNL Safari ITP] .
   * Als u mobiel webverkeer als doel instelt, schakelt u alle mobiele browsers uit, behalve [!UICONTROL Chrome] en [!UICONTROL Edge] .

### Merk, veiligheid en mediakwaliteit

Door contextafhankelijke filters, het blokkeren van voorbiedingsfraude en/of het filteren van [!UICONTROL Ads.txt] wordt de schaal van uw plaatsingen beperkt, maar kunt u ze indien nodig gebruiken.

## Stap 5 - De juiste Creative Assets gebruiken

* De beste manier is om zoveel mogelijk unieke advertentiegrootten op te nemen om het bereik te maximaliseren. Met de universele weergavesjabloon kunt u elke standaardweergave en -grootte uploaden.
* Zorg ervoor alle plaatsen *minstens* alle primaire vertoning en grootte (300x250, 728x90, 160x600, 300x600, 320x50, en 300x50) bevatten.
* Werk creatieve middelen regelmatig bij om creatieve vermoeidheid te voorkomen.

>[!MORELIKETHIS]
>
>* [&#x200B; de Montages van het Pakket &#x200B;](/help/dsp/campaign-management/packages/package-settings.md)
>* [&#x200B; Montages van de Plaatsing &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)
> * [&#x200B; hoe DSP Uw campagnes optimaliseert &#x200B;](optimization-how-dsp-optimizes-campaigns.md)
>* [&#x200B; Doelstellingen van de optimalisering en hoe te om hen te gebruiken &#x200B;](optimization-goals.md)
>* [&#x200B; plaatsing-vlakke pre-Bodende Filters en hoe te om hen te gebruiken &#x200B;](optimization-pre-bid-filters.md)
>* [&#x200B; Controlelijst van de Lancering van de Campagne &#x200B;](/help/dsp/campaign-management/campaign-launch-checklist.md)
