---
title: Merk, veiligheid en mediakwaliteit
description: Meer informatie over de functies voor merkveiligheid en mediakwaliteit.
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: 7ee798e11375863e776ac3e802efc9112280e750
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---

# Merk, veiligheid en mediakwaliteit

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP biedt een reeks functies voor merkbescherming om ervoor te zorgen dat elk van uw campagnes echte gebruikers bereikt in een merkveilige omgeving.

Ons team voor fraudebewaking werkt nauw samen met toonaangevende partners uit de branche, zoals [!DNL Interactive Advertising Bureau] , [!DNL Trust and Accountability Group] [!DNL (TAG)] en [!DNL WhiteOps] , om de inventaris op ons platform zorgvuldig te beheren. Door ons aanbod proactief te beheren, zorgt DSP ervoor dat alle adverteerders op het platform beschermd zijn tegen niet-menselijk verkeer (bots, crawlers, datacenterverkeer en fraude) en alleen in merkveilige contexten leveren.

Naast centraal kwaliteitsbeheer geloven wij in het vermogen van adverteerders om de controles te ontwerpen die op hun merk zijn afgestemd. DSP biedt integratie met [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] en [!DNL Peer39], zodat elke adverteerder zijn gewenste niveau van fraudebescherming, contextafhankelijke filtering en trefwoordgerichtheid kan kiezen.

## Kwaliteitsinitiatieven

### Inventarisverificatie met ondersteuning voor [!DNL Ads.txt]

[[!DNL Ads.txt], dat voor  [!DNL Authorized Digital Sellers] ](https://iabtechlab.com/ads-txt) staat is een initiatief dat door [!DNL Interactive Advertising Bureau] ([!DNL IAB]) in juni 2017 wordt gelanceerd om de juiste vertegenwoordiging van inventaris op de open markt te vergemakkelijken, daardoor bestrijden van onwettige bronnen van verkeer en domeinspoofing. Deelnemende uitgevers en distributeurs geven publiekelijk aan welke bedrijven toestemming hebben om hun digitale inventaris te verkopen en wat de aard van deze relaties is, door een pagina `ads.txt` op het hoogste niveau van het domein te houden (zoals `example.com/ads.txt` ).

DSP ondersteunt [!DNL ads.txt] door het `ads.txt` -bestand van elke uitgever te lezen en u de optie te geven om alleen bij geverifieerde [!DNL ads.txt] -verkopers aankopen te doen. Als we bijvoorbeeld de verkopers vergelijken die we zien openen in `nytimes.com` naar het bestand van de New York Times `ads.txt` , kunnen we vaststellen welke verkopers wel en welke niet legitiem zijn. Als de plaatsing is geconfigureerd om alleen van geverifieerde verkopers te kopen, blokkeren we de overtreders. <!-- can we actually mention NY Times? -->

U kunt standaard [!DNL ads.txt] controles voor elke adverteerder <!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> plaatsen, en dan naar keuze [ de montages voor elke plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md) aanpassen:

* Alleen door directe verkopers binnen een domein geautoriseerde voorraad kopen

* Alleen bij geautoriseerde directe verkopers en wederverkopers van een domein voorraad kopen

* prioriteit geven aan inkoopvoorraad van geautoriseerde directe verkopers en wederverkopers van een domein

* Winkelvoorraad kopen van alle verkopers

### Platform Fraud Surveillance

DSP heeft sterke interne hulpmiddelen en systemen gebouwd om fraude over ons platform te beheren, in samenwerking met toonaangevende industrieleveranciers zoals [!DNL Whiteops] en [!DNL Integral Ad Science].

Bovendien werkt Adobe nauw samen met [!DNL IAB] en [!DNL TAG] om robuuste, industriestandaard fraudeblokkering te garanderen om onze adverteerders te beschermen door hulpmiddelen zoals [!DNL ads.txt] (zie de vorige sectie), de [!DNL IAB] Bots and Spiders lijst, en de [!DNL TAG] IP lijst van Datacenter te gebruiken.

Door onze multidimensionale benadering van kwaliteit, controleert ons team anomalieën en ongeldige verkeerspatronen, die minder dan 3% ongeldig verkeer op beschermde inventaris verzekeren. Elke verdachte voorraad — inclusief inventarisatie op specifieke domeinen of van specifieke uitgevers of verkopers — wordt onmiddellijk geblokkeerd op het hele platform.

### Inventaristoewijzing, lagen en categorisering

Het in kaart brengen van de inventaris is het gedetailleerde overzicht en het aan boord nemen proces dat voor alle nieuwe inventaris wordt vereist alvorens het aan ons platform wordt toegevoegd. Dit proces is bedoeld om de veiligheid en de kwaliteit van alle inventarislijsten bij DSP te waarborgen.

* **Afbeelding:** Ons team van de Inventaris herziet zorgvuldig elk domein, evaluerend aspecten zoals:

   * Brand-veiligheid

   * Typegoedkeuring van advertentie

   * Algemene inhoud, dubbele domeinen en nagemaakte advertentie

* **het Eind:** wij onderzoeken holistisch merkaanwezigheid in het algemene ecosysteem om inventaris over verschillende lijsten te classificeren. U kunt [ uw plaatsen ](/help/dsp/campaign-management/placements/placement-settings.md) aan deze rijen voor het gewenste niveau van bereik richten:

   * **[!UICONTROL T1]** — Merk-naam, internationaal herkenbare sites

   * **[!UICONTROL T2]** — Geweldige sites die actueel en up-to-date zijn, geen door de gebruiker gegenereerde inhoud bevatten en die gewoonlijk geen algemene herkenning hebben

   * **[!UICONTROL T3]** — Door de gebruiker gegenereerde inhoud en niche-inhoud

* **categorisering van de Plaats:** om gemakkelijke inhoud te verzekeren richtend en blokkerend, etiketteren wij elk bezit met een DSP-bepaalde plaatscategorie die op de inhoud van het bezit wordt gebaseerd. U kunt [ richten of deze plaatscategorieën voor elke plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md) uitsluiten die op de plaatsingsdoelstellingen wordt gebaseerd.

### Uitgebreide ondersteuning voor blokkeren van sites

DSP biedt zowel een globaal geblokkeerde lijst met sites als de optie om aangepaste lijsten met geblokkeerde sites voor adverteerders en accounts te maken.

#### Lijst met wereldwijd geblokkeerde sites DSP {#global-blocked-sites}

DSP houdt een wereldwijd geblokkeerde lijst met sites bij die onveilig worden geacht om advertenties uit te voeren. Deze lijst bevat sites met aanstootgevende inhoud (zoals haat of terreur) en sites die besmet zijn met bots, valse pre-roll, niet-afgedekte domeinen en andere frauduleuze activiteiten.

In het kader van ons Brand Safety-initiatief om activiteiten die adverteerders bedriegen uit te roeien, worden alle sites gescreend met behulp van de maatregelen in de lijst met geblokkeerde sites. Alle sites die niet voldoen aan de veiligheidscontroles worden toegevoegd aan de lijst met wereldwijd geblokkeerde sites. Omdat DSP deze lijst dynamisch beheert, kunnen sites op elk gewenst moment van de lijst worden verwijderd of in- en uitgeschakeld, op basis van de meest recente analyse van de merkveiligheid.

Wanneer u een site in de lijst met wereldwijd geblokkeerde sites opneemt als plaatsingsdoel, wordt de site gemarkeerd met een rood uitroepteken (!). Dit geeft aan dat advertenties niet worden uitgevoerd op de gemarkeerde site.

>[!NOTE]
>
>U kunt naar keuze de globale geblokkeerde plaatsenlijst voor standaardvertoningsadvertenties in bijlage aan een vertrouwde op privé overeenkomst omzeilen door &quot;[!UICONTROL Allow unscreened sites]&quot;optie in de [ plaatsingsmontages ](/help/dsp/campaign-management/placements/placement-settings.md) toe te laten. Indien nodig, kan het Team van de Rekening van de Adobe plaats naar keuze het blokkeren voor een openbare (veiling-niveau) overeenkomst in de uitgeversmontages voor de overeenkomst ook onbruikbaar maken.

#### Geblokkeerde sitelijsten op accountniveau en op advertentieniveau

De gebruikers kunnen rekening-niveau en adverteerder-vlakke geblokkeerde plaatsenlijsten <!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) --> ook handhaven, die automatisch voor alle plaatsen worden gebruikt. De lijst met geblokkeerde sites op een lager niveau wordt naast de lijst met wereldwijd geblokkeerde sites toegepast.

## Integraties van derden

### Contextueel filteren

Met contextafhankelijke filters kunt u advertentiemogelijkheden activeren of blokkeren op basis van de context van de pagina waarop de advertentie zou worden geplaatst. Adobe biedt contextuele filtering via integratie met toonaangevende leveranciers in de branche: [!DNL Comscore] , [!DNL DoubleVerify] , [!DNL Integral Ad Science] en [!DNL Peer39] . Voorbeelden van huidige filters zijn [!UICONTROL Adult Content] , [!UICONTROL Natural Disasters] , [!UICONTROL Legal Drinking Age] , [!UICONTROL MANGA] , [!UICONTROL Epidemics] en [!UICONTROL G-rated Sites] .

U kunt standaard contextafhankelijke filtercontroles voor elke adverteerder <!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> plaatsen, en dan naar keuze [ de montages voor elke plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md) aanpassen. Er kunnen extra kosten van toepassing zijn wanneer u deze functie gebruikt.

![ het embleem van de Comscore ](/help/dsp/assets/comscore-logo.png) ![ het embleem DoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![ het Integrale embleem van de Wetenschap Ad ](/help/dsp/assets/ias-logo.png) ![ Peer39 embleem ](/help/dsp/assets/peer39-logo.png)

### Blokkeren van voorbiedingsfraude

Gebruik onze integratie van derden met [!DNL DoubleVerify] , [!DNL Integral Ad Science] en [!DNL Peer39] om niet-menselijk verkeer uit uw campagnes te blokkeren. Deze integratie biedt toonaangevende functies voor het blokkeren van voorbiedingen om zowel het algemene als het geavanceerde ongeldige verkeer (GIVT en SIVT) in uw campagnes te minimaliseren.

U kunt standaard pre-bid fraude blokkerende controles voor elke adverteerder <!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> plaatsen, en dan naar keuze [ de montages voor elke plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md) aanpassen. Er kunnen extra kosten van toepassing zijn wanneer u deze functie gebruikt.

Neem voor meer informatie over functionaliteit rechtstreeks contact op met de voorkeursleverancier of neem contact op met het accountteam van de Adobe.

![ DoubleVerify embleem ](/help/dsp/assets/doubleverify-logo.png) ![ het Integrale Ad- embleem van de Wetenschap ](/help/dsp/assets/ias-logo.png) ![ Peer39 embleem ](/help/dsp/assets/peer39-logo.png)

### Viewability vóór het bod {#pre-bid-viewability}

Met weergavefilters vóór biedingen van onze toonaangevende partners [!DNL DoubleVerify] en [!DNL Integral Ad Science] kunnen adverteerders ervoor zorgen dat hun campagnes in de video- en weergaveinventarisatie aan hun gewenste prestatiedoelstellingen voldoen.

U kunt standaardviewability filters voor elke adverteerder <!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> plaatsen, en dan naar keuze [ de montages voor elke plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md) aanpassen. Er kunnen extra kosten van toepassing zijn wanneer u deze functie gebruikt.

![ DoubleVerify embleem ](/help/dsp/assets/doubleverify-logo.png) ![ het Integrale embleem van de Wetenschap Ad ](/help/dsp/assets/ias-logo.png)

### Doelstelling en meting van aandacht

[!DNL Adobe's] partnership with [!DNL Adelaide] biedt adverteerders ondersteuning voor de Adelaide-metrische methode [!DNL Attention Units] , die de mediakwaliteit meet op basis van oogwaarneming, belichting en resultaatgegevens.

[ plaatsen-vlakke pre-biederaandacht richtend ](/help/dsp/campaign-management/placements/placement-settings.md) staat adverteerders toe om specifieke concentratieniveaus te richten om klantenbetrokkenheid te verbeteren.

Bovendien kunnen de adverteerders [ het volgen voor plaatsing-niveau [!UICONTROL Attention Score] metrisch ](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement) (het gewogen gemiddelde aantal [!DNL Attention Units] over beelden) voor om het even welke campagne toelaten om te begrijpen welke plaatsingstactieken de beste bedrijfsresultaten produceren.

Voor elk onderdeel zijn extra kosten van toepassing.

### Doel van onderwerp

DSP onderwerp het richten staat u toe om sleutelwoordlijsten te richten of te blokkeren door onze industrie-leidende contextafhankelijke partner [!DNL Comscore] te gebruiken. Met onderwerpgerichte toepassingen kunt u ervoor zorgen dat uw advertenties altijd worden aangeboden in een omgeving die op uw merk is afgestemd. Dit geldt zowel voor het blokkeren van schadelijke inhoud als voor het veiligstellen van uitgaven in een context die een groter resultaat biedt.

Het richten van het onderwerp vereist u om de segmenten van het douaneonderwerp direct met het partnerplatform tot stand te brengen. Zodra de segmenten worden gecreeerd, kunt u [ richten of een segmentidentiteitskaart in de [!UICONTROL Audience Targeting] sectie voor elke plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md) uitsluiten. Voor deze functie kunnen extra kosten in rekening worden gebracht.

Om een [!DNL Comscore] rekening tot stand te brengen en de segmenten van het douaneonderwerp tot stand te brengen, kunt u login voor [!DNL Activation Segment Manager] bij [ https://agents.comscore.com ](https://agents.comscore.com) verzoeken. Zie [[!DNL Comscore]  hulp centrum ](https://comscoreactivation.zendesk.com/hc/) voor volledige instructies voor vestiging douanesegmenten. De kosten voor aangepaste segmenten worden in [!DNL Segment Manager] weergegeven wanneer u ze maakt.

![ het embleem van de Comscore ](/help/dsp/assets/comscore-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP heeft met [!DNL DoubleVerify] samengewerkt om de [!DNL Authentic Brand Safety] -oplossing te bieden, waarmee u een gecentraliseerde set vereisten voor merkveiligheid kunt maken die op al uw aankoopplatforms zijn afgestemd voor consistentie.

Als u eenmaal een [!DNL DoubleVerify] brandveiligheidssegment hebt gemaakt met de vereiste focus, kunt u dit segment binnen DSP gebruiken om de regels voor blokvoorbiedingen na het bieden te repliceren in webomgevingen.

U kunt a [!DNL DoubleVerify] segmentidentiteitskaart voor elke adverteerder <!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> specificeren, en dan naar keuze [ [!UICONTROL Authentic Brand Safety] voor elke plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md) toelaten of onbruikbaar maken. DSP uw account aan voor gebruik van de segment-id.

Neem voor meer informatie over functionaliteit rechtstreeks contact op met [!DNL DoubleVerify] of neem contact op met het accountteam van de Adobe.

![ DoubleVerify embleem ](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [ Montages van de Plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
