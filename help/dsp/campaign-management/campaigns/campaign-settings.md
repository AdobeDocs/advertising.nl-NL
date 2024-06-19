---
title: Campagne-instellingen
description: Zie beschrijvingen van de beschikbare campagnemontages.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: d572a406be9271c6ca14d35740f04d15ddbf7364
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Campagne-instellingen

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** De naam van de campagne.

**[!UICONTROL Advertiser]:** (Alleen-lezen voor bestaande campagnes) De toepasselijke adverteerder (merk). Selecteer een bestaande adverteerder of maak een nieuwe adverteerder.

**[!UICONTROL Advertiser URL]:** De officiële pagina van de adverteerder. Dit veld versnelt het goedkeuringsproces voor advertenties met inventarispartners.

**[!UICONTROL Timezone]:** (Alleen-lezen voor bestaande campagnes) De tijdzone voor rapportage en biedingen.

**[!UICONTROL Customer PO]:** (Optioneel) Een inkooporder van een klant voor de invoegorder/inkooporder.

**[Campagnedatums]:** De begin- en einddatum van de campagne.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Of marges voor de campagne moeten worden beheerd: *[!UICONTROL Yes]* of *[!UICONTROL No]* (de standaardwaarde).

Wanneer u *[!UICONTROL Yes],* het type en het bedrag van de marge specificeren:

* **[!UICONTROL Margin Type]:** Het type marge. U kunt het margetype niet veranderen zodra u margebeheer toelaat en de campagne bewaart.

   * *[!UICONTROL Fixed]:* (de standaardinstelling) Hiermee wordt DSP toegestaan uitgaven automatisch te berekenen en te beperken op basis van een vast margepercentage van het [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Hiermee kunt u marges tot het plaatsingsniveau beheren door een aparte instelling op te geven [!UICONTROL Budget Reserve %] en [!UICONTROL Gross Budget] voor elk pakket en elke plaatsing in de campagne. DSP optimaliseert op basis van de financiële efficiëntie van elke plaatsing, zonder een specifieke marge te garanderen. Gebruik dit voor toevoegingsorden die uit veelvoudige lijnpunten bestaan waarvoor u bent overeengekomen om een vaste hoeveelheid eenheden of eenheidstypes aan een vaste tarief te leveren.

* **[!UICONTROL Fixed Margin %]:** (Alleen campagnes met vaste marges) De standaardmarkering voor elke invoegvolgorde <!-- impression? -->, als percentage. Dit bedrag wordt in mindering gebracht op het [!UICONTROL Gross Budget] de begroting van de nettocampagne vaststellen.

* **[!UICONTROL Budget Reserve %]:** (Campagnes met alleen vaste marges; optioneel) Reserveert een bepaald percentage van de [!UICONTROL Gross Budget] als vrijwaringsmaatregel. Dit bedrag wordt in mindering gebracht op het [!UICONTROL Gross Budget] de begroting van de nettocampagne vaststellen.

**[!UICONTROL Gross Budget]:** (Campagnes met uitsluitend margebeheer) De begroting voor het bruto-prijsbeleid, vóór de opgegeven marginale aanpassingen worden toegepast.

U kunt desgewenst een extra bruto-budget per dag, week of maand toevoegen:

1. Klik op **[!UICONTROL Add an additional Gross Budget]**.

1. Voer de **[!UICONTROL Gross Budget]** en selecteert u de budgetinterval: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* of *[!UICONTROL Monthly]*.

De totale nettobegroting, de uitgavenlimiet voor de campagne, wordt automatisch berekend op basis van de marge-instellingen en wordt onder deze waarde aangegeven.

**[!UICONTROL Budget]:** (Campagnes zonder margebeheer) Het totale campagnebudget.

**[!UICONTROL Estimated Tax Withholding]:** Hiermee wordt een percentage van de totale uitgaven bespaard voor advertentiekosten, honoreringskosten en/of gegevenskosten op rekeningniveau voor land- of lokale belastingen. Tarieven zijn ramingen voor budgettering en prijsstelling, zodat de gefactureerde belastingtarieven kunnen variëren.

Belastingen die moeten worden ingehouden ramen:

1. Klik op **[!UICONTROL Update rates here]**.

1. Geef de **[!UICONTROL Estimated tax rate]**, als percentage.

1. Schakel het selectievakje in naast elk type kosten waarvoor belastingen moeten worden ingehouden. De vergoedingstypen omvatten:

   * *[!UICONTROL Include estimated tax - ads fee]:* Is van toepassing op alle uitgaven voor advertenties DSP media, inclusief belastingen op kosten voor campagnebeheer.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Is van toepassing op alle uitgaven voor DSP, met uitzondering van media en gegevens. Hieronder vallen geen belastingen voor campagnebeheerkosten

   * *[!UICONTROL Include estimated tax - data fee]:* Is van toepassing op alle gegevens die worden besteed aan DSP.

1. Klik op **[!UICONTROL Submit]**.

>[!NOTE]
>
>* In de V.S., kunnen de staten in hun opname van belastingtarieven tussen advertenties, het dienen van, en gegevens variëren. Voor organisaties in andere landen worden alle drie de categorieën belastingtarieven opgenomen om de BTW te vergoeden.
>
>* U kunt deze waarden ook configureren in de instellingen voor accountkosten.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Alleen-lezen voor bestaande campagnes die sinds 22 juni 2020 zijn gemaakt; niet beschikbaar voor campagnes die vóór 22 juni 2020 zijn gemaakt) Het niveau waarop DSP advertenties aanstuurt en frequentieplafonds toepast: *Zelfde apparaat* een apparaat of *Mensen* om een persoon over al hun bekende apparaten te richten. **Opmerking:** Ondersteuning voor verschillende apparaten is niet beschikbaar voor plaatsen die universele id&#39;s als doel hebben.

**[!UICONTROL Device Graph]:** (Alleen-lezen voor bestaande campagnes; campagnes met alleen op personen gebaseerde cross-device focus) De apparaatgrafiek die moet worden gebruikt voor apparaatbesturing en frequentiebeheer:

* *[!UICONTROL LiveRamp - U.S. only]:* Beschikbaar aan alle adverteerders voor dwars-apparaat richtend bij $0.35 CPM voor beelden die door te gebruiken worden geleverd [!DNL LiveRamp] apparaatgrafiek (dat wil zeggen voor apparaten die niet worden gevonden binnen de doelpubliekssegmenten). U kunt een apparaatmarkering instellen op plaatsingsniveau.

  Deze optie is ook beschikbaar voor alle adverteerders, zonder vergoedingen, voor frequentiebeheer en attributiemeting.

  Ondersteuning voor verschillende apparaten is alleen van toepassing op plaatsen die oudere id&#39;s als doel hebben, maar niet op plaatsen die universele id&#39;s als doel hebben (inclusief [!DNL LiveRamps]). Het richten, frequentiebeheer, en de attributie voor universele IDs wordt toegepast slechts op het niveau van identiteitskaart.

**[!UICONTROL Frequency Cap]:** (Optioneel) Het aantal keren dat een uniek apparaat, een universele id of een persoon (afhankelijk van het opgegeven [!UICONTROL Cross Device Level] en de plaatsing [!UICONTROL Targeting] instellen) kan advertenties uit de campagne ontvangen. Opties omvatten *[!UICONTROL Unlimited]* of een specifiek bedrag per dag, week of maand.

>[!NOTE]
>
> U kunt frequentiecappen instellen op campagne-, pakket- en plaatsingsniveaus. DSP respecteert de strengste frequentiegrens in de campagnehiërarchie.

**[!UICONTROL Packages]:** De [pakketten](/help/dsp/campaign-management/packages/package-about.md) in de campagne op te nemen. Selecteer bestaande pakketten en/of maak pakketten die u wilt opnemen. Als u pakketten maakt, raadpleegt u de beschrijvingen over de [pakketinstellingen](/help/dsp/campaign-management/packages/package-settings.md) voor meer informatie .

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Met de volgende instellingen worden alleen meet- en rapportagemogelijkheden ingeschakeld. Prestaties worden alleen geoptimaliseerd op pakket- en plaatsingsniveau.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Optioneel) Inschakelen [!DNL IAS] meting en rapportage van gezichtsvermogen, fraude, merkveiligheid en verificatie van het publiek, met behulp van de opgegeven instellingen. Er zijn extra kosten van toepassing.

* **[!UICONTROL Measure On]:** De inventaris waarop wordt gemeten: *[!UICONTROL Display and VPAID video inventory]* (de standaardwaarde) of *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >De videoviewability is meetbaar op VPAID slechts inventaris.

* **[!UICONTROL IAS Account ID (AnID)]:** (Adverteerders [!DNL IAS] accounts; optioneel) De organisatie [!DNL IAS] account-id, die [!DNL IAS] rechtstreeks factureren voor gebruik.

* **[!UICONTROL IAS Team ID]:** (Adverteerders [!DNL IAS] accounts; optioneel) De team-id voor de organisatie [!DNL IAS] account, welke [!DNL IAS] rechtstreeks factureren voor gebruik. <!-- verify -->

**[!UICONTROL MOAT]:** (Optioneel) Inschakelen [!DNL MOAT] meting en rapportage van gezichtsvermogen, fraude, merkveiligheid en verificatie van het publiek. Er zijn extra kosten van toepassing.

#### Verificatie door het publiek

**[!UICONTROL comScore Campaign Ratings]:** (Optioneel) Inschakelen [!DNL Comscore] gevalideerd [!DNL Campaign Ratings] meting en rapportage van publieksverificatie, met behulp van de opgegeven instellingen. Er zijn extra kosten van toepassing.

* **[!UICONTROL Target Gender]:** Te bereiken geslacht: *[!UICONTROL Both]* (standaard), *[!UICONTROL Male]*, of *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** Het leeftijdsbereik dat moet worden nagestreefd. Gebruik de linker- en rechterschuifregelaars om het bereik zo nodig te verkleinen.

* **[!UICONTROL Target Country]:** (Optioneel) Een land dat als doel moet dienen. [!DNL Comscore] maatregelen die alleen in de gesteunde landen worden genomen.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Hiermee wordt tracering ingeschakeld voor het plaatsingsniveau [!UICONTROL Attention Score] (het gewogen gemiddelde aantal [!DNL Adelaide] &quot;[!DNL Attention Units]&quot; door de indrukken heen). De metriek is beschikbaar voor alle plaatsingstypes behalve [!DNL Roku] Aangesloten tv, pre-roll VPAID en audio die geen podcast is. DSP automatisch een JavaScript-tag aan alle bijbehorende creatieve elementen koppelt, en [!DNL Adelaide] volgt de blootstellingsgegevens en stuurt deze dagelijks naar DSP. U kunt de datum gebruiken om uw uitgaven voor plaatsingstactieken handmatig te optimaliseren met betere aandachtscores.

De [!UICONTROL Attention Score] is beschikbaar in het dialoogvenster [!UICONTROL Metrics] deel van de verslagen; binnen de [!UICONTROL Campaigns], [!UICONTROL Packages], en [!UICONTROL Placements] standpunten en over de [!UICONTROL Sites], [!UICONTROL Ads], en [!UICONTROL Inventory] tabs van de [weergave met plaatsingsdetails](/help/dsp/campaign-management/reports/placement-details-view.md).

Gebruiken [!DNL Adelaide] Segmenten voor metingen worden in een CPM-vergoeding opgenomen voor elke indruk die wordt geleverd door advertenties met [!DNL Adelaide] metinglabels. Deze kosten zijn niet gelijk aan de kosten voor [aandacht op plaatsingsniveau gericht](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Hiermee worden metingen en rapportage van de gezichtsvermogen door de eerste partij mogelijk gemaakt [!DNL IAB Open Video Viewability (OpenVV)] technologie, gebaseerd op het gespecificeerde gevoeligheidsniveau:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Informatie over Campaign Management](campaign-about.md)
>* [Een campagne maken](campaign-create.md)
>* [Een campagne bewerken](campaign-edit.md)
>* [Het Wijzigingslogboek voor een campagne weergeven](campaign-change-log.md)
