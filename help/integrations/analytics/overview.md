---
title: Overzicht van [!DNL Analytics for Advertising]
description: Overzicht van [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---

# Overzicht van [!DNL Analytics for Advertising]

*Adverteerders met DSP en[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] Adobe Analytics en Adobe Advertising integreren om de mogelijkheden van elk product uit te breiden en te verbeteren.

Dankzij de integratie kunnen adverteerders doorklikken en de interacties van sites bekijken in hun [!DNL Analytics] exemplaren, zodat merknamen kunnen zien hoe hun advertentiepijfer leidt tot betrokkenheid van sites en kritieke bedrijfsdoelstellingen.

Bovendien kan de Adobe Advertising tot de grote first-party gegevens toegang hebben die [!DNL Analytics] verzamelt met [!DNL Analytics] tags die al op de site staan. Dit maakt een robuuster reisbeheer, hermarketing van de eerste partij en rapportage van betaalde mediasites mogelijk. Adobe Advertising kan de [!DNL Analytics] gegevens voor optimalisatie van uitgaven en biedingen.

Indien naar behoren in dienst genomen, [!DNL Analytics for Advertising] vervaagt de grenzen tussen twee traditionele rollen : het maken van reclame voor het beheer van reizen ( het verzenden van gebruikers naar de site via advertenties ) en het begrijpen van die betrokkenheid via webanalyses .

Primaire voordelen:

* Verzenden [!DNL Analytics] segmenten direct aan Adobe Advertising voor de hermarketing van de eerste plaats.
* Gebruiken [!DNL Analytics] aangepaste en standaardgebeurtenissen als conversiesignalen voor het optimaliseren van betaalde mediaclame.
* Profiteer van [!DNL Analytics] Analysis Workspace voor een beter begrip van de toegangspunten van sites en het gedrag van bezoekers.
* Nauwere samenwerking tussen webanalisten en betaalde medieteams mogelijk maken.
* Doorlopende weergave van permanente Adobe Advertising gebruiken en doorklikid&#39;s gebruiken binnen [!DNL Analytics] de betrokkenheid van de site te begrijpen.
* Verbeter traditionele betaalde mediapporten in Analysis Workspace met aangepaste meetwaarden, aangepaste afmetingen en sitetaken die niet haalbaar zijn wanneer u gegevens of pixels exporteert naar servers of andere DSP.
* Profiteer van [!DNL Analytics] code die al op uw website staat voor het bijhouden en optimaliseren binnen de Adobe Advertising.

>[!TIP]
>
> Kijk eens naar [videopresentatie van [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Analyses gebruiken voor rapportage van betaalde media

[!DNL Analytics for Advertising] verbetert de rapportage en het inzicht in de manier waarop uw advertenties het gedrag van sites beïnvloeden door het volgende toe te staan:

* Doorlopende weergave van permanente Adobe Advertising gebruiken en doorklikid&#39;s gebruiken binnen [!DNL Analytics] de betrokkenheid van de site te begrijpen.
* Profiteer van Analysis Workspace voor een beter begrip van de toegangspunten voor sites en het gedrag van bezoekers. U hebt toegang tot betaalde media-dimensionale en gebeurtenisgegevens, waaronder namen van campagneentiteiten (tot plaatsen en advertenties) en de bijbehorende metriek, zoals klikken, indrukken en kosten.

Te gebruiken [!DNL Analytics] uw organisatie heeft als betaalmiddel voor mediarapportage een aanmeldingsnaam voor het Experience Cloud nodig voor toegang tot Analysis Workspace. Uw team van de Adobe Advertising zal u helpen om uw gegevens van de Adobe Advertising aan individuele rapportreeksen in Analysis Workspace in kaart te brengen. U kunt de gegevens van de Adobe Advertising naar om het even welke rapportreeks verzenden, maar u zou van de rapportsuites op de hoogte moeten zijn die aan Adobe Advertising en die in kaart zijn gebracht die niet hebben. Afhankelijk van de rapportsuite kunnen de gerapporteerde gegevens hierdoor worden gewijzigd.

[Adobe Advertising-id&#39;s binnen [!DNL Analytics]](ids.md) werken zoals andere [!DNL eVars], met een aangepaste, blijvende vervaldatum. Standaard wordt het terugzoekvenster voor toewijzing ingesteld op 60 dagen tijdens de implementatie van de Adobe Advertising. Werk met het accountteam van uw Adobe om deze instelling te wijzigen.

De afmetingen van de Adobe Advertising worden toegevoegd met het achtervoegsel &quot;(AMO-id)&quot; (zoals &quot;Advertentietype (AMO-id)&quot;). Zie &quot;[Adoben Advertising in Analysis Workspace](advertising-metrics-in-analytics.md)&quot; voor een lijst van de beschikbare afmetingen.

>[!NOTE]
>
> Wanneer u de gegevens van de Adobe Advertising (of om het even welke gegevensreeks) binnen bekijkt [!DNL Analytics], moet u er rekening mee houden dat metriek en rapporten zijn gebaseerd op de regels die zijn ingesteld binnen [!DNL Analytics]. De gegevens kunnen anders zijn dan wat u ziet in andere rapportsystemen, zoals advertentierapporten. [!DNL DSP] rapporten of rapporten van zoekmachines. Om inzicht te krijgen in de gegevensverschillen in [!DNL Analytics], moet u weten wanneer [!DNL eVar] gegevens verlopen, wat een bezoek bepaalt, wat als laatste aanraking tegenover totale persisterende attributie wordt beschouwd, en andere factoren. Zie voor meer informatie [Verwachte gegevensvariaties tussen [!DNL Analytics] en Adobe Advertising](data-variances.md).

## Analyses gebruiken voor Power Adobe Advertising-campagnes en -Portfolio&#39;s

Zonder extra pixels te vereisen, [!DNL Analytics for Advertising] laat betere optimalisering en gemakkelijkere publiekssegmentatie toe door twee belangrijkste signalen naar Adobe Advertising te verzenden:

* Omrekeningswaarden die als biedsignalen moeten worden gebruikt:
   * standaardmeetwaarden, zoals [!UICONTROL Revenue] en [!UICONTROL Cart Views].
   * metriek voor de betrokkenheid van de site, zoals de paginaweergave en de meetgegevens voor bezoeken.
   * maatstaven voor aangepaste omzet.
   * gereserveerde inkomstenwaarden.
* Segmenten gemaakt in [!DNL Analytics] en bekendgemaakt aan het Experience Cloud.

  U kunt [!DNL Analytics] segmenten voor herbestemming van eerste site in [!DNL DSP] en betaalde zoekopdrachten.

  ([!DNL Search, Social, & Commerce] alleen) Adverteerders met [!DNL Analytics] maar Audience Managers kunnen ook op tags gebaseerde soorten publiek (remarketing lijsten) en publiek met klantovereenkomsten (klantlijsten) maken op basis van Google-websites [!DNL Analytics] segmenten die met Experience Cloud worden gedeeld.

### Metrische gegevens voor siteconversie als biedsignalen

U kunt uw standaardgebeurtenissen en aangepaste gebeurtenissen gebruiken vanuit [!DNL Analytics] het opbouwen van gewogen doelstellingen in de Adobe Advertising. Doelstellingen informeren biedingsbeslissingen voor je [!DNL DSP] pakketten en zoekportfolio&#39;s.

>[!NOTE]
>
> U kunt berekende metriek niet in kaart brengen van [!DNL Analytics] in Adobe Advertising.

Uw team van de Adobe Advertising zal u helpen de gebeurtenissen identificeren en in kaart brengen die op betaalde media prestaties in Adobe Advertising van toepassing zijn, waar zij vermeld in [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions].

Zie &quot;[Analytische gegevens in Adobe Advertising](analytics-data-in-advertising.md)&quot; voor een lijst van beschikbare metriek.

### Analysesegmenten voor het opnieuw oprichten van sites

Adobe Advertising kan worden opgenomen [!DNL Analytics] segmenten voor het opnieuw in de handel brengen van DSP en [!DNL Search, Social, & Commerce] advertenties die gebruikmaken van de integratie van het native Experience Cloud publiek tussen [!DNL Analytics] en Experience Cloud.

Als u toegang wilt krijgen tot [!DNL Analytics] segmenten, moet een adverteerderaccount de [Experience Cloud-id-service](https://experienceleague.adobe.com/docs/id-service/using/home.html) ingeschakeld. Wanneer de Dienst van identiteitskaart wordt toegelaten, alle segmenten van het Experience Cloud (met inbegrip van segmenten die in worden gecreeerd [!DNL Analytics] en gepubliceerd naar Experience Cloud, segmenten gemaakt in Adobe Audience Manager, segmenten gemaakt in Experience Cloud met behulp van de [!DNL People core service]en segmenten die in Adobe Experience Platform zijn gemaakt en via Audience Manager naar de Adobe Advertising worden verzonden), worden in de Adobe Advertising beschikbaar zodra ze worden verwerkt.

[!DNL Analytics] segmenten zijn binnen 24 uur beschikbaar en worden dagelijks bijgewerkt.

Voor meer informatie over de dienst van het Publiek van de Experience Cloud, zie [Soorten publiek Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Voorbeelden van hoe te om de Integratie te gebruiken {#integration-examples}

### Gegevens van Adobe Advertising gebruiken in Analysis Workspace

Bekijk de video &quot;[Inleiding tot werkruimte en rapportage](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

#### Connected TV View-through-conversies gebruiken in rapporten

*Uitsluitend voor DSP*

U kunt de effectiviteit van de CTV-campagnes (full-funnel) van uw aangesloten tv-apparaten meten door deze te koppelen aan en belichten op CTV-apparaten op onsite conversies. De nieuwe [!UICONTROL Landing Type] filter &quot;[!UICONTROL View-through (CTV)]&quot; hiermee worden omzettingen in afzonderlijke rijen gesplitst voor [!UICONTROL Click Through], [!UICONTROL View Through], en [!UICONTROL View Through (CTV)] waarden.

Als u de conversiemetriek van uw CTV-weergave wilt bekijken, gebruikt u de weergave Plaatsen of de weergave Marketingkanaal in Analysis Workspace.

De weergave Plaatsing gebruiken:

1. Plaats de plaatsen voor CTV-uitgaven in de rapportweergave.

1. Neem de gewenste afmetingen op, zoals &#39;Impressies&#39;, &#39;Klikken&#39; enzovoort.

1. Pas de volgende filters toe:

   Advertentieplatform: `Advertising Cloud DSP`

   Openingspagina: `View-Through (CTV)`

De weergave Marketing kanaal gebruiken:

1. De dimensie opnemen `Marketing Channel`.

1. Neem de gewenste afmetingen op, zoals &#39;Impressies&#39;, &#39;Klikken&#39; enzovoort.

1. Pas de volgende filters toe:

   Advertentieplatform: `Advertising Cloud DSP`

   Openingspagina: `View-Through (CTV)`

### Adobe Advertising-dashboards maken

Als u wilt weten hoe u de gegevens van uw Adobe Advertising kunt bijhouden op basis van uw doelstellingen in Analysis Workspace, raadpleegt u de video &quot;[Adobe Advertising-dashboards maken met Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Gebruikend Adobe Advertising identiteitskaart voor de Analyse van de Ingang van de Plaats

Om te zien hoe u een rapport van de de plaatsingang van de Adobe Advertising kunt creëren om dag-van-week, tijd-van-dag, browser, en geografische invloeden te controleren, zie de video &quot;[Rapporten over site-invoer voor Adobe Advertising maken](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Video: Inleiding tot [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Vereisten en belangrijke Informatie voor het Uitvoeren [!DNL Analytics for Advertising]](prerequisites.md)
>* [Adobe Advertising-id&#39;s gebruikt door Analytics](ids.md)
>* [JavaScript-code voor analyses voor advertenties](/help/integrations/analytics/javascript.md)
>* [Verwachte gegevensvariaties tussen [!DNL Analytics] en Adobe Advertising](data-variances.md)
>* [Adoben Advertising in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Gegevens in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
