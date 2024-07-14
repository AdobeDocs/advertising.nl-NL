---
title: Campagne-instellingen
description: Zie beschrijvingen van de beschikbare campagnemontages.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 0fbdc7e38026d71483c2de1406a4110066690130
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---

# Campagne-instellingen

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** De naam van de campagne.

**[!UICONTROL Advertiser]:** (Alleen-lezen voor bestaande campagnes) De toepasselijke adverteerder (merk). Selecteer een bestaande adverteerder of maak een nieuwe adverteerder.

**[!UICONTROL Advertiser URL]:** De officiële pagina van de adverteerder. Dit veld versnelt het goedkeuringsproces voor advertenties met inventarispartners.

**[!UICONTROL Timezone]:** (Alleen-lezen voor bestaande campagnes) De tijdzone voor rapportage en biedingen.

**[!UICONTROL Customer PO]:** (Optioneel) Een kooporder van een klant voor de invoegorder/kooporder.

**[de Datums van de Campagne ]:** de begin en einddata van de campagne.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Of de marges voor de campagne moeten worden beheerd: *[!UICONTROL Yes]* of *[!UICONTROL No]* (de standaardinstelling).

Wanneer u *[!UICONTROL Yes]kiest,* specificeer het margetype en de hoeveelheid:

* **[!UICONTROL Margin Type]:** Het type van marge. U kunt het margetype niet veranderen zodra u margebeheer toelaat en de campagne bewaart.

   * *[!UICONTROL Fixed]:* (het gebrek) staat DSP toe om uitgaven automatisch te berekenen en te besnoeien gebaseerd op een vast margepercentage van [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Hiermee kunt u marges tot het plaatsingsniveau beheren door een aparte [!UICONTROL Budget Reserve %] en [!UICONTROL Gross Budget] op te geven voor elk pakket en elke plaatsing in de campagne. DSP optimaliseert op basis van de financiële efficiëntie van elke plaatsing, zonder een specifieke marge te garanderen. Gebruik dit voor toevoegingsorden die uit veelvoudige lijnpunten bestaan waarvoor u bent overeengekomen om een vaste hoeveelheid eenheden of eenheidstypes aan een vaste tarief te leveren.

* **[!UICONTROL Fixed Margin %]:** (Campagnes met vaste marges slechts) de standaardprijsverhoging voor elke toevoegingsorde <!-- impression? -->, als percentage. Dit bedrag wordt in mindering gebracht op de [!UICONTROL Gross Budget] om het netto campagnebudget te bepalen.

* **[!UICONTROL Budget Reserve %]:** (Campagnes met vaste marges slechts; facultatief) behoudt een gespecificeerd percentage van [!UICONTROL Gross Budget] als vrijwaring. Dit bedrag wordt in mindering gebracht op de [!UICONTROL Gross Budget] om het netto campagnebudget te bepalen.

**[!UICONTROL Gross Budget]:** (Campagnes met slechts margebeheer) De bruto campagnebegroting, alvorens de gespecificeerde marginale aanpassingen worden toegepast.

U kunt desgewenst een extra bruto-budget per dag, week of maand toevoegen:

1. Klik op **[!UICONTROL Add an additional Gross Budget]**.

1. Voer de **[!UICONTROL Gross Budget]** in en selecteer het interval voor het budget: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* of *[!UICONTROL Monthly]* .

De totale nettobegroting, de uitgavenlimiet voor de campagne, wordt automatisch berekend op basis van de marge-instellingen en wordt onder deze waarde aangegeven.

**[!UICONTROL Budget]:** (Campagnes zonder margebeheer) het algemene campagnebudget.

**[!UICONTROL Estimated Tax Withholding]:** houdt een percentage van de totale uitgaven voor advertentiekosten, kosten voor het aanbieden van diensten en/of gegevenskosten op rekeningniveau in voor land- of lokale belastingen. Tarieven zijn ramingen voor budgettering en prijsstelling, zodat de gefactureerde belastingtarieven kunnen variëren.

Belastingen die moeten worden ingehouden ramen:

1. Klik op **[!UICONTROL Update rates here]**.

1. Geef de waarde **[!UICONTROL Estimated tax rate]** op als een percentage.

1. Schakel het selectievakje in naast elk type kosten waarvoor belastingen moeten worden ingehouden. De vergoedingstypen omvatten:

   * *[!UICONTROL Include estimated tax - ads fee]:* is van toepassing op alle uitgaven voor Advertising DSP-media, inclusief belastingen op kosten voor campagnebeheer.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* is van toepassing op alle uitgaven voor Advertising DSP, behalve voor media en gegevens. Hieronder vallen geen belastingen voor campagnebeheerkosten

   * *[!UICONTROL Include estimated tax - data fee]:* is van toepassing op alle gegevensuitgaven voor Advertising DSP.

1. Klik op **[!UICONTROL Submit]**.

>[!NOTE]
>
>* In de V.S., kunnen de staten in hun opname van belastingtarieven tussen advertenties, het dienen van, en gegevens variëren. Voor organisaties in andere landen worden alle drie de categorieën belastingtarieven opgenomen om de BTW te vergoeden.
>
>* U kunt deze waarden in de de vergoedingsmontages van de rekening ook vormen.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Read-only voor bestaande campagnes die sinds 22 juni 2020 worden gecreeerd; niet beschikbaar voor campagnes die vóór 22 juni 2020 worden gecreeerd) het niveau waarop DSP doelt adverteert en frequentiecaps toepast: *Zelfde Apparaat* om een apparaat te richten of *Mensen* om een persoon over al hun bekende apparaten te richten. **Nota:** de steun van het dwars-apparaat is niet beschikbaar voor plaatsen die universele IDs richten.

**[!UICONTROL Device Graph]:** (Alleen-lezen voor bestaande campagnes; campagnes met alleen op personen gebaseerde cross-device gericht) De apparaatgrafiek die moet worden gebruikt voor apparaatbesturing en frequentiebeheer:

* *[!UICONTROL LiveRamp - U.S. only]:* Beschikbaar aan alle adverteerders voor dwars-apparaat richtend bij $0.35 CPM voor beelden die door de [!DNL LiveRamp] apparatengrafiek (namelijk voor apparaten worden geleverd die niet binnen de gerichte publiekssegmenten worden gevonden) worden geleverd. U kunt een apparaatmarkering instellen op plaatsingsniveau.

  Deze optie is ook beschikbaar voor alle adverteerders, zonder vergoedingen, voor frequentiebeheer en attributiemeting.

  Ondersteuning voor verschillende apparaten is alleen van toepassing op plaatsen die oudere id&#39;s als doel hebben, maar niet op plaatsen die universele id&#39;s als doel hebben (inclusief [!DNL LiveRamps]). Het richten, frequentiebeheer, en de attributie voor universele IDs wordt toegepast slechts op het niveau van identiteitskaart.

**[!UICONTROL Frequency Cap]:** (Optioneel) Het aantal keren dat een uniek apparaat, een universele id of een persoon (afhankelijk van de opgegeven [!UICONTROL Cross Device Level] en de instelling [!UICONTROL Targeting] van de plaatsing) advertenties van de campagne kan ontvangen. U kunt kiezen uit *[!UICONTROL Unlimited]* of een bepaald bedrag per dag, week of maand.

>[!NOTE]
>
> U kunt frequentiecappen instellen op campagne-, pakket- en plaatsingsniveaus. DSP respecteert de strengste frequentiegrens in de campagnehiërarchie.

**[!UICONTROL Packages]:** de [ pakketten ](/help/dsp/campaign-management/packages/package-about.md) om in de campagne te omvatten. Selecteer bestaande pakketten en/of maak pakketten die u wilt opnemen. Als u pakketten creeert, zie beschrijvingen over de [ pakketmontages ](/help/dsp/campaign-management/packages/package-settings.md) voor meer informatie.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Met de volgende instellingen worden alleen meet- en rapportagemogelijkheden ingeschakeld. Prestaties worden alleen geoptimaliseerd op pakket- en plaatsingsniveau.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Optioneel) Hiermee schakelt u [!DNL IAS] het meten en rapporteren van de zichtbaarheid, fraude, merkveiligheid en publieksverificatie in met de opgegeven instellingen. Er zijn extra kosten van toepassing.

* **[!UICONTROL Measure On]:** De voorraad waarop wordt gemeten: *[!UICONTROL Display and VPAID video inventory]* (de standaardwaarde) of *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >De videoviewability is meetbaar op VPAID slechts inventaris.

* **[!UICONTROL IAS Account ID (AnID)]:** (Adverteerders met hun eigen [!DNL IAS] -accounts; optioneel) De [!DNL IAS] account-id van de organisatie, die [!DNL IAS] rechtstreeks aanrekent voor gebruik.

* **[!UICONTROL IAS Team ID]:** (Adverteerders met hun eigen [!DNL IAS] -accounts; optioneel) De team-id voor de [!DNL IAS] -account van de organisatie, die [!DNL IAS] rechtstreeks aanrekent voor gebruik. <!-- verify -->

**[!UICONTROL MOAT]:** (Optioneel) Hiermee kunt u [!DNL MOAT] de zichtbaarheid, fraude, merkveiligheid en publieksverificatie meten en melden. Er zijn extra kosten van toepassing. **Nota:** [!DNL Oracle] zal zijn reclamezaken tegen 30 september 2024, met inbegrip van alle diensten van [!DNL MOAT] beëindigen.

#### Verificatie door het publiek

**[!UICONTROL Comscore Campaign Ratings]:** (Optioneel) Schakelt [!DNL Comscore] gevalideerde [!DNL Campaign Ratings] meting en rapportage van publieksverificatie in met de opgegeven instellingen. Er zijn extra kosten van toepassing.

* **[!UICONTROL Target Gender]:** The gender to target: *[!UICONTROL Both]* (the default), *[!UICONTROL Male]*, or *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** De leeftijdswaaier aan doel. Gebruik de linker- en rechterschuifregelaars om het bereik zo nodig te verkleinen.

* **[!UICONTROL Target Country]:** (Facultatief) een land om te richten. [!DNL Comscore] meet alleen indrukken die in ondersteunde landen worden gebruikt.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** laat het volgen voor metrisch plaatsing-niveau [!UICONTROL Attention Score] toe (het gewogen gemiddelde aantal [!DNL Adelaide] &quot;[!DNL Attention Units]&quot;over beelden). Metrische gegevens zijn beschikbaar voor alle plaatsingstypen, behalve voor [!DNL Roku] aangesloten tv&#39;s, VPAID-bestanden (pre-roll) en audio die geen podcast is. DSP voegt automatisch een JavaScript-tag toe aan alle bijbehorende creatieve instellingen en [!DNL Adelaide] volgt de belichtingsgegevens en stuurt deze dagelijks naar DSP. U kunt de datum gebruiken om uw uitgaven voor plaatsingstactieken handmatig te optimaliseren met betere aandachtscores.

Het [!UICONTROL Attention Score] gebied is beschikbaar in de [!UICONTROL Metrics] sectie van rapporten; binnen [!UICONTROL Campaigns], [!UICONTROL Packages], en [!UICONTROL Placements] meningen; en op [!UICONTROL Sites], [!UICONTROL Ads], en [!UICONTROL Inventory] lusjes van de [ mening van de plaatsingsdetails ](/help/dsp/campaign-management/reports/placement-details-view.md).

Wanneer u [!DNL Adelaide] -segmenten gebruikt voor metingen, wordt een CPM-vergoeding aangerekend voor elke indruk die wordt geleverd door advertenties met [!DNL Adelaide] -metingtags. Deze vergoeding is gescheiden van kosten voor [ plaatsing-vlakke aandacht richtend ](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** laat eerste-partijmeting en rapportering van viewability toe gebruikend de [!DNL IAB Open Video Viewability (OpenVV)] technologie, die op het gespecificeerde gevoeligheidsniveau wordt gebaseerd:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [ Ongeveer Campaign Management ](campaign-about.md)
>* [ creeer een Campagne ](campaign-create.md)
>* [ geef een Campagne ](campaign-edit.md) uit
>* [ Mening het Logboek van de Verandering voor een Campagne ](campaign-change-log.md)
