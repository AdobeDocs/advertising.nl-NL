---
title: Campagne-instellingen
description: Zie beschrijvingen van de beschikbare campagnemontages.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 9d26e097f007b570c0f0e3b7f02c683a84d5e647
workflow-type: tm+mt
source-wordcount: '1434'
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

* **[!UICONTROL How would you like to compute agency fees?]:** (Campagnes met margebeheer slechts) hoe te om uitzendingsvergoedingen te berekenen, die het gedeelte van het bruto budget van de campagne zijn dat wordt ingehouden en niet inbegrepen in de netto uitgaven:

   * *[!UICONTROL Margin % of Total Budget]:* (het gebrek) berekent de taksen als percentage van de bruto uitgave. Geef de waarden [!UICONTROL Agency Fee Type] (vast of samengesteld) en [!UICONTROL Margin %] of [!UICONTROL Composite Margin %] op.

   * *[!UICONTROL Apply Markup % on top of individual cost components]:* bereken de kosten als een bepaald percentage van de mediakosten, gegevens en andere kosten, en/of [!DNL Adobe] technische kosten. Geef de [!UICONTROL Markup %] op en selecteer de componenten waarop de markering moet worden toegepast.

* **[!UICONTROL Agency Fee Type]:** (Campagnes die [!UICONTROL Margin % of Total Budget] gebruiken) het type van agentuurkosten.

   * *[!UICONTROL Fixed]:* (het gebrek) staat DSP toe om een vast percentage van de bruto uitgave als agentschapkosten te houden. Geef de waarde [!UICONTROL Margin %] op.

   * *[!UICONTROL Composite]:* Hiermee staat u DSP toe een percentage van de bruto-uitgave in te houden voor rekening van zowel agentschapkosten als technische kosten van [!DNL Adobe] . Geef de waarde [!UICONTROL Composite Margin %] op.

* **[!UICONTROL Margin %]:** (Campagnes die [!UICONTROL Margin % of Total Budget] met vaste marges gebruiken) Het percentage van de bruto uitgave dat als agentschapkosten moet worden ingehouden. Wijzigingen in de margewaarde worden alleen toegepast op toekomstige bruto-uitgaven en niet op de historische bruto-uitgaven voor de campagne. De waarde [!UICONTROL Estimated Tax Withholding] wordt niet opgenomen in de bruto-uitgave voordat de marge wordt toegepast. Zie de volgende voorbeelden, die veronderstellen dat de campagne niet onderbesteedt of overgeeft.

   * Voorbeeld 1: Stel dat [!UICONTROL Gross Budget] `100 USD` is en [!UICONTROL Margin %] `5%` gedurende de vlucht. Aan het einde van de campagnevlucht worden de kosten berekend als `5 USD` (dat is `5% of 100 USD` ) en de netto uitgave is `95 USD` (dat is `campaign budget [100 USD] - agency fees [5 USD]` ).

   * Voorbeeld 2 met wijzigingen in de marge: Stel dat [!UICONTROL Margin %] voor dezelfde campagne is gewijzigd van `5%` in `10%` toen de bruto uitgave `40 USD` was. Voor de periode vóór de wijziging worden de agentschapkosten berekend als `2 USD` (dat is `5% of 40 USD` ); voor de periode na de wijziging worden de agentschapkosten berekend als `6 USD` (dat is `10% of 60 USD`). De totale agentschapkosten worden berekend als `8 USD` (dit is `2 USD + 6 USD` ) en de nettouitgave is `92 USD` (dit is `campaign budget [100 USD] - total agency fees [8 USD]` ).

   * Voorbeeld 3 met belastingaftrek: Stel dat [!UICONTROL Gross Budget] `100 USD` is, de [!UICONTROL Estimated Tax Withholding] aan het einde van de campagnevlucht `10 USD` is en de [!UICONTROL Margin %] `5%` gedurende de hele vlucht. Aan het einde van de campagnevlucht worden de kosten berekend als `4.5 USD` (dat is `5% of (campaign budget [100 USD] - tax withholding [USD 10])` ) en de netto uitgave is `85.5 USD` (dat is `campaign budget [100 USD] - agency fees [4.5 USD] - tax withholding [10 USD]` ).

* **[!UICONTROL Composite Margin %]:** (Campagnes die [!UICONTROL Margin % of Total Budget] met samengestelde marges gebruiken) Het percentage van de bruto uitgave die, om als [!DNL Adobe] technische kosten en uitzendkosten samen te worden ingehouden. De vergoedingen voor uitzendbureaus worden berekend door de technische kosten van Adobe af te trekken van het samengestelde margebedrag. Wijzigingen in de samengestelde margewaarde worden alleen toegepast op toekomstige bruto-uitgaven en niet op de historische bruto-uitgaven voor de campagne. De waarde [!UICONTROL Estimated Tax Withholding] wordt niet opgenomen in de bruto-uitgave voordat de samengestelde marge wordt toegepast.

  Stel dat de waarde [!UICONTROL Gross Budget] `100 USD` is, de technische kosten [!DNL Adobe] aan het einde van de campagne `10 USD` zijn en de waarde [!UICONTROL Composite Margin %] `17%` gedurende de hele vlucht is. Aan het einde van de campagnevlucht (ervan uitgaande dat de campagne niet te laag of te veel besteedt) worden de agentuurkosten berekend als `7 USD` (dat is `(17% of 100 USD) - 10` ), en de netto uitgave is `93 USD` (dat is `campaign budget [100 USD] - agency fees [7 USD]`).

* **[!UICONTROL Markup %]:** (Campagnes die [!UICONTROL Apply Markup % on top of individual cost components] gebruiken) het percentage dat op gespecificeerde kostencomponenten moet worden toegepast om agentschapkosten te berekenen. Wijzigingen in de opmaakwaarde worden alleen toegepast op toekomstige kosten en niet op de historische kosten voor de campagne.

* **[!UICONTROL Select cost components on which markup will be applied]:** (Campagnes die [!UICONTROL Apply Markup % on top of individual cost components] gebruiken) de kostencomponenten waarvoor [!UICONTROL Markup %] wordt toegepast. Selecteer alle toepasselijke componenten: *[!UICONTROL Media cost]*, *[!UICONTROL Data and Other costs]* en/of *[!UICONTROL Adobe tech fees]* . Wijzigingen in de selectie van onderdelen worden alleen toegepast op toekomstige kosten en niet op de historische kosten voor de campagne.

  Bijvoorbeeld, [!UICONTROL Markup %] is `10%` voor &quot;[!UICONTROL Media cost]&quot;en &quot;[!UICONTROL Data and Other costs]. Als op een gegeven moment in de campagne de mediadracht `20 USD` is, de data en andere kosten `5 USD` zijn en [!DNL Adobe] de tech-kosten `2 USD` zijn, worden de kosten van de service berekend als `2.50 USD` (dat wil zeggen `10% of (20 USD + 5 USD)` en is de bruto-uitgave `29.50 USD` (dat is `media cost [20 USD] + data and other costs [5 USD] + [!DNL Adobe] tech fees [2 USD] + agency fees [2.50 USD]`).

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
