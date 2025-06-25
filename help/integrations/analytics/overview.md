---
title: Overzicht van  [!DNL Analytics for Advertising]
description: Overzicht van  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Overzicht van [!DNL Analytics for Advertising]

*Advertisers met Advertising DSP en[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] integreert Adobe Analytics en Adobe Advertising om de mogelijkheden van elk product uit te breiden en te verbeteren.

Dankzij de integratie kunnen adverteerders doorklikken en interacties op de site doorzien in hun [!DNL Analytics] -exemplaar, zodat merknamen kunnen zien hoe hun advertentieformaat leidt tot de betrokkenheid van de site en kritieke bedrijfsdoelstellingen.

Bovendien heeft Adobe Advertising toegang tot de grote gegevens van de eerste partij die [!DNL Analytics] verzamelt met [!DNL Analytics] -tags die al op de site staan. Dit maakt een robuuster reisbeheer, hermarketing van de eerste partij en rapportage van betaalde mediasites mogelijk. Adobe Advertising kan de [!DNL Analytics] -gegevens verder gebruiken voor optimalisatie van uitgaven en biedingen.

Als [!DNL Analytics for Advertising] correct wordt gebruikt, vervaagt u de grenzen tussen twee traditionele rollen: het beheer van de advertentietraject (het verzenden van gebruikers naar de site via advertenties) en het begrijpen van die betrokkenheid via webanalyses.

Primaire voordelen:

* Verzend [!DNL Analytics] -segmenten rechtstreeks naar Adobe Advertising voor hermarketing van de eerste site.
* Gebruik [!DNL Analytics] aangepaste en standaardgebeurtenissen als conversiesignalen voor het optimaliseren van betaalde mediacereclame.
* Profiteer van [!DNL Analytics] Analysis Workspace voor een beter begrip van de toegangspunten voor sites en het gedrag van bezoekers.
* Nauwere samenwerking tussen webanalisten en betaalde medieteams mogelijk maken.
* Gebruik doorlopende Adobe Advertising-weergave en doorklikid&#39;s binnen [!DNL Analytics] om inzicht te krijgen in de betrokkenheid van de site.
* Verbeter traditionele betaalde media rapporten in Analysis Workspace met douanemetriek, douanedimensies, en plaatsactiviteit niet haalbaar wanneer het uitvoeren van gegevens of pixel aan add servers of andere DSPs.
* Gebruik [!DNL Analytics] -code die al op uw website staat voor tracering en optimalisatie in Adobe Advertising.

>[!TIP]
>
> Bekijk a [ videoinleiding aan  [!DNL Analytics for Advertising] ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Analyses gebruiken voor rapportage van betaalde media

[!DNL Analytics for Advertising] verbetert de rapportage en insight over het gedrag van sites door uw advertenties te laten beïnvloeden door het volgende toe te staan:

* Gebruik doorlopende Adobe Advertising-weergave en doorklikid&#39;s binnen [!DNL Analytics] om inzicht te krijgen in de betrokkenheid van de site.
* Profiteer van Analysis Workspace voor een beter begrip van de toegangspunten voor sites en het gedrag van bezoekers. U kunt betaalde media dimensionaal en gebeurtenisgegevens, die namen van de de campagneentiteit van Adobe Advertising (tot plaatsen en advertenties) en hun bijbehorende metriek, zoals kliks, beelden, en kosten omvatten.

Uw organisatie heeft een Experience Cloud-aanmelding met toegang tot Analysis Workspace nodig om [!DNL Analytics] te kunnen gebruiken als hulpmiddel voor het rapporteren van betaalde media. Uw Adobe Advertising-team helpt u uw Adobe Advertising-gegevens toe te wijzen aan individuele rapportsuite in Analysis Workspace. U kunt Adobe Advertising-gegevens naar elke rapportsuite verzenden, maar u dient op de hoogte te zijn van de rapportsuites die aan Adobe Advertising zijn toegewezen en van de suites die dat nog niet hebben gedaan. Afhankelijk van de rapportsuite kunnen de gerapporteerde gegevens hierdoor worden gewijzigd.

[ Adobe Advertising IDs binnen  [!DNL Analytics]](ids.md) werk zoals andere [!DNL eVars], met een douane, blijvende afloop. Standaard wordt het terugzoekvenster voor toewijzing ingesteld op 60 dagen tijdens de Adobe Advertising-implementatie. Werk samen met uw Adobe-accountteam om deze instelling te wijzigen.

Adobe Advertising-afmetingen worden toegevoegd met het achtervoegsel &quot;(AMO-id)&quot; (zoals &quot;Ad Type (AMO-id)&quot;). Zie &quot;[ Metriek van Adobe Advertising in Analysis Workspace ](advertising-metrics-in-analytics.md)&quot;voor een lijst van de beschikbare afmetingen.

>[!NOTE]
>
> Wanneer u Adobe Advertising-gegevens (of gegevenssets) in [!DNL Analytics] bekijkt, moet u er rekening mee houden dat metrische gegevens en rapporten zijn gebaseerd op de regels die binnen [!DNL Analytics] zijn ingesteld. De gegevens kunnen anders zijn dan wat u ziet in andere rapportagesystemen, zoals serverrapporten, [!DNL DSP] -rapporten of zoekprogrammarapporten. Als u de gegevensverschillen in [!DNL Analytics] wilt begrijpen, moet u weten wanneer [!DNL eVar] -gegevens verlopen, wat een bezoek definieert, wat als laatste aanraakkenmerk wordt beschouwd en wat als totale aanhoudend kenmerk wordt beschouwd, en andere factoren. Voor meer informatie, zie [ Verwachte Variaties van Gegevens tussen  [!DNL Analytics]  en Adobe Advertising ](data-variances.md).

## Analyses gebruiken voor Power Adobe Advertising-campagnes en -portfolio&#39;s

[!DNL Analytics for Advertising] vereist geen extra pixels en maakt een betere optimalisatie en eenvoudigere publiekssegmentatie mogelijk door twee hoofdsignalen naar Adobe Advertising te verzenden:

* Omrekeningswaarden die als biedsignalen moeten worden gebruikt:
   * standaardmetriek, zoals [!UICONTROL Revenue] en [!UICONTROL Cart Views] .
   * metriek voor de betrokkenheid van de site, zoals de paginaweergave en de meetgegevens voor bezoeken.
   * maatstaven voor aangepaste omzet.
   * gereserveerde inkomstenwaarden.
* Segmenten gemaakt in [!DNL Analytics] en gepubliceerd naar Experience Cloud.

  U kunt [!DNL Analytics] -segmenten gebruiken voor het opnieuw toewijzen van sites aan eerste partijen in [!DNL DSP] en voor betaalde zoekopdrachten.

  ([!DNL Search, Social, & Commerce] slechts) Adverteerders met [!DNL Analytics] maar niet Audience Manager kunnen ook op tags gebaseerde soorten publiek op de website van Google (remarketing lijsten) en klantgericht publiek (klantenlijsten) van [!DNL Analytics] segmenten tot stand brengen die met Experience Cloud worden gedeeld.

### Metrische gegevens voor siteconversie als biedsignalen

U kunt uw standaardgebeurtenissen en aangepaste gebeurtenissen van [!DNL Analytics] gebruiken om gewogen doelstellingen te maken in Adobe Advertising. Doelstellingen informeren biedingsbeslissingen voor uw [!DNL DSP] -pakketten en zoek-, sociale en Commerce-portfolio&#39;s.

Voor [!DNL Google Ads] - en [!DNL Google Microsoft Advertising] -campagnes in hybride portfolio&#39;s Zoeken, Sociaal en Commerce kunt u optioneel de doelstellingen, inclusief alle [!DNL Analytics] -gebeurtenissen in de doelstellingen, rechtstreeks uploaden naar advertentienetwerken, waar deze beschikbaar komen als conversieacties voor aangepaste conversiedoelstellingen op accountniveau en op campagnereniveau.

>[!NOTE]
>
> U kunt berekende metriek van [!DNL Analytics] niet in Adobe Advertising in kaart brengen.

Uw Adobe Advertising-team helpt u de gebeurtenissen die van toepassing zijn op betaalde mediaprestaties te identificeren en in kaart te brengen in Adobe Advertising, waar ze worden weergegeven in [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Conversions] .

Zie &quot;[ Metriek van Analytics in Adobe Advertising ](analytics-data-in-advertising.md)&quot;voor een lijst van beschikbare metriek.

### Analysesegmenten voor het opnieuw oprichten van sites

Adobe Advertising kan [!DNL Analytics] -segmenten opnemen voor marketingdoeleinden voor Advertising DSP- en [!DNL Search, Social, & Commerce] -advertenties die gebruikmaken van de geïntegreerde Experience Cloud-publiek tussen [!DNL Analytics] en Experience Cloud.

Om tot de [!DNL Analytics] segmenten toegang te hebben, moet een adverteerderrekening de [ Dienst van identiteitskaart van Experience Cloud ](https://experienceleague.adobe.com/docs/id-service/using/home.html) toelaten. Wanneer de ID Service is ingeschakeld, worden alle Experience Cloud-segmenten (inclusief segmenten die in [!DNL Analytics] zijn gemaakt en naar Experience Cloud zijn gepubliceerd, segmenten die in Adobe Audience Manager zijn gemaakt, segmenten die in Experience Cloud zijn gemaakt met [!DNL People core service] en segmenten die in Adobe Experience Platform zijn gemaakt en via Audience Manager naar Adobe Advertising zijn verzonden) in Adobe Advertising beschikbaar zodra ze worden verwerkt.

[!DNL Analytics] -segmenten zijn binnen 24 uur beschikbaar en worden dagelijks bijgewerkt.

Voor meer informatie over de dienst van het Soorten publiek van Experience Cloud, zie [ Soorten publiek van Experience Cloud ](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Voorbeelden van hoe te om de Integratie te gebruiken {#integration-examples}

### Adobe Advertising-gegevens gebruiken in Analysis Workspace

Leren hoe u uw gegevens van Adobe Advertising kunt gebruiken om visuele rapporten in Analysis Workspace tot stand te brengen, zie de video &quot;[ Inleiding aan Workspace en het Melden ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

#### Connected TV View-through-conversies gebruiken in rapporten

*slechts de gebruikers van Advertising DSP*

U kunt de effectiviteit van de CTV-campagnes (full-funnel) van uw aangesloten tv-apparaten meten door deze te koppelen aan en belichten op CTV-apparaten op onsite conversies. Met het nieuwe [!UICONTROL Landing Type] filter &quot;[!UICONTROL View-through (CTV)]&quot; worden omzettingen gesplitst in afzonderlijke rijen voor [!UICONTROL Click Through] -, [!UICONTROL View Through] - en [!UICONTROL View Through (CTV)] -waarden.

Als u de conversiemetriek van uw CTV-weergave wilt bekijken, gebruikt u de weergave Plaatsen of de weergave Marketingkanaal in Analysis Workspace.

De weergave Plaatsing gebruiken:

1. Plaats de plaatsen voor CTV-uitgaven in de rapportweergave.

1. Neem de gewenste afmetingen op, zoals &#39;Impressies&#39;, &#39;Klikken&#39; enzovoort.

1. Pas de volgende filters toe:

   Advertentieplatform: `Advertising Cloud DSP`

   Openingspagina: `View-Through (CTV)`

De weergave Marketing kanaal gebruiken:

1. Neem de dimensie `Marketing Channel` op.

1. Neem de gewenste afmetingen op, zoals &#39;Impressies&#39;, &#39;Klikken&#39; enzovoort.

1. Pas de volgende filters toe:

   Advertentieplatform: `Advertising Cloud DSP`

   Openingspagina: `View-Through (CTV)`

### Adobe Advertising-dashboards maken

Leren hoe u uw gegevens van Adobe Advertising tegen uw doelstellingen in Analysis Workspace kunt volgen, zie de video &quot;[ Adobe Advertising Dashboards met Adobe Analytics ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html) tot stand brengen.&quot;

### Adobe Advertising-id gebruiken voor analyse van siteinvoer

Om te zien hoe u een rapport van de de plaatsingang van Adobe Advertising kunt tot stand brengen om dag-van-week, tijd-van-dag, browser, en geografische invloeden te controleren, de video &quot;[ Create de Rapporten van de Ingang van de Plaats van Adobe Advertising ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html)&quot;.

## Een [!DNL Analytics for Advertising] -implementatie starten

Neem contact op met uw Adobe-accountteam, dat de initiële configuratie die nodig is om te beginnen, zal voltooien en u zal helpen uw implementatie en gegevensgebruik te plannen op basis van de behoeften van uw organisatie.

>[!MORELIKETHIS]
>
>* [ Video: Inleiding aan  [!DNL Analytics for Advertising] ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [ Eerste vereisten en Zeer belangrijke Informatie voor het Uitvoeren  [!DNL Analytics for Advertising]](prerequisites.md)
>* [ Adobe Advertising IDs die door Analytics ](ids.md) wordt gebruikt
>* [ Code van JavaScript voor Analytics voor Advertising ](/help/integrations/analytics/javascript.md)
>* [ Verwachte Variaties van Gegevens tussen  [!DNL Analytics]  en Adobe Advertising ](data-variances.md)
>* [ Metriek van Adobe Advertising in Analysis Workspace ](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics]  Gegevens in Adobe Advertising ](/help/integrations/analytics/analytics-data-in-advertising.md)
