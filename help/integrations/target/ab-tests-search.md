---
title: A/B-tests configureren voor Adobe Advertising Search, Social & Commerce Ads in Adobe Target
description: Leer hoe u een A/B-test instelt in [!DNL Target] voor uw [!DNL Google Ads] en [!DNL Microsoft® Advertising] advertenties in Zoeken, Sociale Zaken en Handel.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# A/B-tests configureren in Adobe Target voor advertenties, zoek-, sociale en commerciële advertenties

*Adverteerders met alleen reclame, sociale zaken en handel*

*[!DNL Google Ads]en [!DNL Microsoft® Advertising] alleen accounts*

Adobe Advertising en Adobe Target maken het gemakkelijk om landingspagina-ervaring A/B tests voor digitaal reclameverkeer op te zetten [!DNL Google Ads] en [!DNL Microsoft® Advertising] tot:

* Verbeteren van de omrekeningskoersen (CVR) en de maatregelen ter verbetering van de efficiëntie bij aankopen (zoals CPA, CPL en CAC).

* Lever een meer persoonlijke landingspagina-ervaring die relevant is voor de advertentie (bijvoorbeeld, die het beeld/video creatief, exemplaar, sleutelwoord, of ander reclamesignaal aan de landende pagina aanpast).

U kunt ook de native [[!DNL Analytics] voor reclame](/help/integrations/analytics/overview.md) en [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integratie rapporteringsdimensies die in Adobe Analytics zijn geïntegreerd om uw testgegevens te meten en te visualiseren met [!DNL Analytics] metriek en succesgebeurtenissen.

Zie de volgende secties voor de voorwaarden, instructies voor het instellen van A/B-tests in [!DNL Target] voor doorklikverkeer van advertenties in Zoeken, Sociaal, &amp; Handel, en tips voor het meten en visualiseren van uw tests in [!DNL Analytics].

## Vereisten

### Vereiste producten

* Zoeken, sociale zaken en handel
* [!DNL Target]

### Aanbevolen producten en integratie

* [!DNL Analytics]

* [[!DNL Analytics] voor reclame](/help/integrations/analytics/overview.md) integratie<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integratie

## Stap 1: Een testactiviteit A/B maken in [!DNL Target] for Search, Social &amp; Commerce

In de volgende instructies wordt informatie over de Gebruikszaak Zoeken, Sociale zaken en Handel gemarkeerd.

1. [Aanmelden bij Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Een A/B-test maken](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. In de **[!UICONTROL Enter Activity URL]** Voer de URL van de bestemmingspagina voor de test in.

   1. In de **[!UICONTROL Goal]** voert u de succesmetrische waarde voor de test in.

      >[!NOTE]
      >
      >Controleer of [!DNL Analytics] is ingeschakeld als gegevensbron binnen [!DNL Target]en dat de juiste rapportsuite is geselecteerd.

   1. Stel de **[!UICONTROL Priority]** tot `High` of `999` om conflicten te voorkomen wanneer gebruikers in het testsegment een onjuiste ervaring op locatie ontvangen.


   1. Within **[!UICONTROL Reporting Settings]**, selecteert u de **[!UICONTROL Company Name]** en **[!UICONTROL Report Suite]** verbonden met uw account voor Zoeken, Sociale Zaken en Handel.

      Zie &quot;[Best practices en probleemoplossing rapporteren](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. In de **[!UICONTROL Date Range]** Voer de juiste begin- en einddatum voor de test in.

   1. Selecteren **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. In de **[!UICONTROL Value]** veld, voert u de [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID], of [!UICONTROL Network Ad ID] voor de relevante netwerkentiteit in Search, Social, &amp; Commerce. Hierdoor kunt u de [!DNL Target] de parameters van het vraagkoord voor klik-door publiek voor de entiteit.

      U kunt de id vinden op [toevoegen van de desbetreffende kolom Id aan de entiteitsweergave](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] in de [!UICONTROL Accounts] weergave](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] in de [!UICONTROL Accounts] weergave")

      Werk met uw accountteam van de Adobe als u hulp nodig hebt.

   1. Voor de **[!UICONTROL Traffic Allocation Method]**, selecteert u **[!UICONTROL Manual (Default)]** en splitst het publiek 50/50.

   1. Sla de activiteit op.

1. Gebruiken [Composer visuele doelervaring](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) om ontwerpwijzigingen aan te brengen in de sjabloon voor de landingspagina van de A/B-test.

   * Ervaar A: Bewerk niet omdat het de standaard/controle landende paginaervaring zonder personalisatie is.

   * Ervaring B: De [!DNL Target] gebruikersinterface om de landingspagina-sjabloon aan te passen op basis van de elementen die in de test zijn opgenomen (zoals kopregels, kopiëren, knopplaatsing en creatieve elementen).

   >[!NOTE]
   >
   >Neem bijvoorbeeld contact op met het accountteam van uw Adobe voor creatieve testdoeleinden.

## Stap 2: Stel uw [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

[!DNL Analytics for Target] (A4T) is een integratie tussen oplossingen die adverteerders in staat stelt [!DNL Target] activiteiten op basis van [!DNL Analytics] conversiemetriek en publiekssegmenten en meet de resultaten vervolgens met [!DNL Analytics] als de bron van de rapportage. Alle rapportage en segmentering voor die activiteit zijn gebaseerd op [!DNL Analytics] gegevensverzameling.

Voor meer informatie over [!DNL Analytics for Target], met inbegrip van een koppeling naar de uitvoeringsinstructies, zie &quot;[Adobe Analytics als bron van rapportage voor Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Stel de [!DNL Analytics for Target] Deelvenster

In Analysis Workspace configureert u de [!DNL Analytics for Target panel] om uw [!DNL Target] activiteiten en ervaringen. Houd rekening met de volgende belangrijke aanwijzingen en informatie over uw rapporten.

#### Metrisch

* Een deelvenster maken in de werkruimte dat specifiek is voor de account, campagne of groep Adoben Advertising<!-- only applicable entities? --> waarvoor de test is uitgevoerd. De summiere visualisaties van het gebruik om Adobe Advertising metriek in het zelfde rapport te tonen zoals [!DNL Target] testprestaties.

* Prioriteit geven aan het gebruik van onsite metriek (zoals bezoeken en conversies) om de prestaties te meten.

* Begrijp dat de samengevoegde media metriek van Adobe Advertising (zoals impressies, kliks, en kosten) niet kan worden aangepast aan [!DNL Target] metriek.

#### Dimensionen

De volgende afmetingen hebben betrekking op [!DNL Analytics for Target]:

* **Doelactiviteiten**: Naam van de A/B-test

* **Doelervaringen**: Namen van ervaringen met landingspagina&#39;s die binnen de activiteit worden gebruikt

* **Doelactiviteit** > **Ervaring**: De naam van de activiteit en de ervaring in dezelfde rij

### Analyses voor probleemoplossing voor [!DNL Target] Gegevens

Als u in Analysis Workspace opmerkt dat de activiteit en de ervaring gegevens minimaal of niet vullen, doet u het volgende:

* Controleren of hetzelfde [!UICONTROL Supplemental Data ID] (SDID) wordt voor beide gebruikt [!DNL Target] en [!DNL Analytics]. U kunt de waarden van SDID verifiëren door [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) op de landingspagina waarop de campagne de gebruikers drijft.

[Aanvullende waarden voor de gegevens-id (SDID) in de Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Controleer op dezelfde landingspagina of a) de [!UICONTROL Hostname] in de Adobe Debugger [!UICONTROL Solutions] > [!UICONTROL Target] overeenkomsten b) de [!UICONTROL Tracking Server] getoond in [!DNL Target] voor de activiteit (onder [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] vereist een [!DNL Analytics] volgende server die in vraag van moet worden verzonden [!DNL Target] aan de [!DNL Modstats] gegevensverzamelingsserver voor Analytics.<!-- just "to Analytics?"-->

[Hostnaamwaarde in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Waarde van volgserver in doel](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Verdere lezing

* [Doel integreren met analyse](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Verklaart hoe te opstelling [!DNL Target] rapporteren in Analysis Workspace.
* [A/B-testoverzicht](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Beschrijft A/B testactiviteiten, die u met Onderzoek, Sociale, &amp; de advertenties van de Handel kunt gebruiken.
* [Overzicht van analytische gegevens voor reclame](/help/integrations/analytics/overview.md) - Introduceert Analytics voor Advertising, waarmee u doorklikinteracties en doorkijkinteracties van sites in uw Analytics-instanties kunt bijhouden.

>[!MORELIKETHIS]
>
>* [A/B-tests configureren in Adobe Target voor advertenties DSP advertenties](ab-tests-dsp.md)
