---
title: Campagne-instellingen
description: Zie beschrijvingen van de beschikbare campagnemontages.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 1b15b14b0ace6137e79b456c7c8f8444efa8acac
workflow-type: tm+mt
source-wordcount: '1062'
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

**[!UICONTROL Margin Management]:** (Zelfbediening rekeningen die door agentschappen gebruikend marges worden onderhouden) Opties voor margebeheer:

* **[!UICONTROL Would you like to manage margins for this campaign?]:** Of de marges voor de campagne moeten worden beheerd: *[!UICONTROL Yes]* of *[!UICONTROL No]* (de standaardinstelling). Wanneer u *[!UICONTROL Yes]kiest,* specificeer de extra montages. Zodra u margebeheer toelaat en de campagne bewaart, kunt u margebeheer niet onbruikbaar maken.

* **[!UICONTROL How would you like to compute agency fees?]:** (Campagnes met margebeheer slechts) hoe te om agentuurkosten te berekenen:

   * *[!UICONTROL Margin % of Total Budget]:* (de standaardwaarde) berekent de kosten als een percentage van [!UICONTROL Gross Budget] . Geef de waarden [!UICONTROL Agency Fee Type] (vast of samengesteld) en [!UICONTROL Margin %] of [!UICONTROL Composite Margin %] op.

   * *[!UICONTROL Apply Markup % on top of individual cost components]:* voegt een bepaald percentage toe aan uw mediakosten, gegevens en andere kosten, en/of [!DNL Adobe] aan technische kosten. Geef de [!UICONTROL Markup %] op en selecteer de componenten waarop de markering moet worden toegepast.

* **[!UICONTROL Agency Fee Type]:** (Campagnes die [!UICONTROL Margin % of Total Budget] gebruiken) het type van agentuurkosten.

   * *[!UICONTROL Fixed]:* (het gebrek) staat DSP toe om uitgaven automatisch te berekenen en te bedekken gebaseerd op een vast percentage van [!UICONTROL Gross Budget]. Geef de waarde [!UICONTROL Margin %] op.

   * *[!UICONTROL Composite]:* Hiermee staat u DSP toe om uitgaven automatisch te berekenen en te beperken op basis van een percentage van de [!UICONTROL Gross Budget] , waarbij het samengestelde percentage aan agentschapkosten en [!DNL Adobe] technische kosten wordt gebruikt. Geef de waarde [!UICONTROL Composite Margin %] op.

* **[!UICONTROL Margin %]:** (Campagnes die [!UICONTROL Margin % of Total Budget] met vaste marges gebruiken) De standaardprijsverhoging voor elke toevoegingsorde <!-- impression? -->, als percentage. Dit bedrag wordt in mindering gebracht op de [!UICONTROL Gross Budget] om het netto campagnebudget te bepalen. De marge wordt niet toegepast op de [!UICONTROL Estimated Tax Withholding] op de [!UICONTROL Gross Budget] .

* **[!UICONTROL Composite Margin %]:** (Campagnes die [!UICONTROL Margin % of Total Budget] met samengestelde marges gebruiken) De som van agentschapkosten en [!DNL Adobe] tech-kosten, als percentage. Dit bedrag wordt in mindering gebracht op de [!UICONTROL Gross Budget] om het netto campagnebudget te bepalen. De marge wordt niet toegepast op de [!UICONTROL Estimated Tax Withholding] op de [!UICONTROL Gross Budget] .

* **[!UICONTROL Markup %]:** (Campagnes die [!UICONTROL Apply Markup % on top of individual cost components] gebruiken) het percentage om aan gespecificeerde kostencomponenten toe te voegen.

* **[!UICONTROL Select cost components on which markup will be applied]:** (Campagnes die [!UICONTROL Apply Markup % on top of individual cost components] gebruiken) de kostencomponenten waarvoor [!UICONTROL Markup %] wordt toegepast. Selecteer alle toepasselijke componenten: *[!UICONTROL Media cost]*, *[!UICONTROL Data and Other costs]* en/of *[!UICONTROL Adobe tech fees]* .

**[!UICONTROL Gross Budget]:** (Campagnes met slechts margebeheer) De bruto campagnebegroting, alvorens de gespecificeerde marginale aanpassingen worden toegepast.

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

**[!UICONTROL Cross Device Level]:** (Read-only voor bestaande campagnes die sinds 22 juni 2020 worden gecreeerd; niet beschikbaar voor campagnes die vóór 22 juni 2020 worden gecreeerd) het niveau waarop DSP adverteert en frequentiecaps toepast: *Zelfde Apparaat* om een apparaat te richten of *Mensen* om een persoon over al hun bekende apparaten te richten. **Nota:** de steun van het dwars-apparaat is niet beschikbaar voor plaatsen die universele IDs richten.

**[!UICONTROL Device Graph]:** (Alleen-lezen voor bestaande campagnes; campagnes met alleen op personen gebaseerde cross-device gericht) De apparaatgrafiek die moet worden gebruikt voor apparaatbesturing en frequentiebeheer:

* *[!UICONTROL LiveRamp - U.S. only]:* Beschikbaar voor alle adverteerders voor apparaten met een CPM van $0.35 voor indrukken die door de [!DNL LiveRamp] apparatengrafiek worden geleverd (namelijk voor apparaten die niet binnen de gerichte publiekssegmenten worden gevonden). U kunt een apparaatmarkering instellen op plaatsingsniveau.

  Deze optie is ook beschikbaar voor alle adverteerders, zonder vergoedingen, voor frequentiebeheer en attributiemeting.

  Ondersteuning voor verschillende apparaten is alleen van toepassing op plaatsen die oudere id&#39;s als doel hebben, maar niet op plaatsen die universele id&#39;s als doel hebben (inclusief [!DNL LiveRamps]). Het richten, frequentiebeheer, en de attributie voor universele IDs wordt toegepast slechts op het niveau van identiteitskaart.

**[!UICONTROL Frequency Cap]:** (Optioneel) Het aantal keren dat een uniek apparaat, een universele id of een persoon (afhankelijk van de opgegeven [!UICONTROL Cross Device Level] en de instelling [!UICONTROL Targeting] van de plaatsing) advertenties van de campagne kan ontvangen. U kunt kiezen uit *[!UICONTROL Unlimited]* of een bepaald bedrag per dag, week of maand.

>[!NOTE]
>
> U kunt frequentiecappen instellen op campagne-, pakket- en plaatsingsniveaus. DSP respecteert de strengste frequentiegrens in de campagnehiërarchie.

**[!UICONTROL Packages]:** de [&#x200B; pakketten &#x200B;](/help/dsp/campaign-management/packages/package-about.md) om in de campagne te omvatten. Selecteer bestaande pakketten en/of maak pakketten die u wilt opnemen. Als u pakketten creeert, zie beschrijvingen over de [&#x200B; pakketmontages &#x200B;](/help/dsp/campaign-management/packages/package-settings.md) voor meer informatie.

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

#### Verificatie door het publiek

**[!UICONTROL Comscore Campaign Ratings]:** (Optioneel) Schakelt [!DNL Comscore] gevalideerde [!DNL Campaign Ratings] meting en rapportage van publieksverificatie in met de opgegeven instellingen. Er zijn extra kosten van toepassing.

* **[!UICONTROL Target Gender]:** The gender to target: *[!UICONTROL Both]* (the default), *[!UICONTROL Male]*, or *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** De leeftijdswaaier aan doel. Gebruik de linker- en rechterschuifregelaars om het bereik zo nodig te verkleinen.

* **[!UICONTROL Target Country]:** (Facultatief) een land om te richten. [!DNL Comscore] meet alleen indrukken die in ondersteunde landen worden gebruikt.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** laat het volgen voor metrisch plaatsing-niveau [!UICONTROL Attention Score] toe (het gewogen gemiddelde aantal [!DNL Adelaide] &quot;[!DNL Attention Units]&quot;over beelden). Metrische gegevens zijn beschikbaar voor alle plaatsingstypen, behalve voor [!DNL Roku] aangesloten tv&#39;s, VPAID-bestanden (pre-roll) en audio die geen podcast is. DSP koppelt automatisch een JavaScript-tag aan alle bijbehorende creatieven, en [!DNL Adelaide] volgt de belichtingsgegevens en stuurt deze dagelijks naar DSP. U kunt de datum gebruiken om uw uitgaven voor plaatsingstactieken handmatig te optimaliseren met betere aandachtscores.

Het [!UICONTROL Attention Score] gebied is beschikbaar in de [!UICONTROL Metrics] sectie van rapporten; binnen [!UICONTROL Campaigns], [!UICONTROL Packages], en [!UICONTROL Placements] meningen; en op [!UICONTROL Sites], [!UICONTROL Ads], en [!UICONTROL Inventory] lusjes van de [&#x200B; mening van de plaatsingsdetails &#x200B;](/help/dsp/campaign-management/reports/placement-details-view.md).

Wanneer u [!DNL Adelaide] -segmenten gebruikt voor metingen, wordt voor elke indruk die wordt geleverd door advertenties met [!DNL Adelaide] -meettags een CPM-vergoeding in rekening gebracht. Deze vergoeding is gescheiden van kosten voor [&#x200B; plaatsing-vlakke aandacht richtend &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md).

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
>* [&#x200B; Ongeveer het Beheer van de Campagne &#x200B;](campaign-about.md)
>* [&#x200B; creeer een Campagne &#x200B;](campaign-create.md)
>* [&#x200B; geef een Campagne &#x200B;](campaign-edit.md) uit
>* [&#x200B; Mening het Logboek van de Verandering voor een Campagne &#x200B;](campaign-change-log.md)
