---
title: A/B-tests configureren voor Adobe Advertising Search, Social en Commerce Ads in Adobe Target
description: Leer hoe te opstelling een test A/B in  [!DNL Target]  voor uw  [!DNL Google Ads]  en  [!DNL Microsoft Advertising]  advertenties in Onderzoek, Sociaal, & Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# A/B-tests configureren in Adobe Target voor Advertising Search-, Social- en Commerce-advertenties

*Advertisers met het Onderzoek van Advertising, Sociale, &amp; Commerce slechts*

*[!DNL Google Ads]en [!DNL Microsoft Advertising] alleen accounts*

Adobe Advertising en Adobe Target maken het gemakkelijk om landingspagina-ervaring A/B tests voor digitaal advertentieverkeer in te stellen [!DNL Google Ads] en [!DNL Microsoft Advertising] aan:

* Verbeteren van de omrekeningskoersen (CVR) en de maatregelen ter verbetering van de efficiëntie bij aankopen (zoals CPA, CPL en CAC).

* Lever een meer persoonlijke landingspagina-ervaring die relevant is voor de advertentie (bijvoorbeeld, die het beeld/video creatief, exemplaar, sleutelwoord, of ander reclamesignaal aan de landende pagina aanpast).

U kunt inheems [[!DNL Analytics]  voor Advertising ](/help/integrations/analytics/overview.md) en [[!DNL Analytics]  voor  [!DNL Target] ](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integratie ook combineren meldend dimensies die in Adobe Analytics worden geïntegreerd om uw testgegevens met [!DNL Analytics] metriek en succesgebeurtenissen te meten en te visualiseren.

Zie de volgende secties voor de voorwaarden, instructies voor het instellen van A/B-tests in [!DNL Target] voor doorklikverkeer van advertenties in Zoeken, Sociaal en Commerce en tips voor het meten en visualiseren van uw tests in [!DNL Analytics] .

## Vereisten

### Vereiste producten

* Zoeken, sociaal en Commerce
* [!DNL Target]

### Aanbevolen producten en integratie

* [!DNL Analytics]

* [[!DNL Analytics]  voor Advertising ](/help/integrations/analytics/overview.md) integratie <!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics]  voor  [!DNL Target] ](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integratie

## Stap 1: Maak een testactiviteit A/B in [!DNL Target] voor Zoeken, Sociaal en Commerce

In de volgende instructies wordt informatie over het gebruik van de optie Zoeken, Sociaal en Commerce gemarkeerd.

1. [ Teken binnen aan Adobe Target ](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [ creeer een test A/B ](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. Voer in het veld **[!UICONTROL Enter Activity URL]** de URL van de bestemmingspagina voor de test in.

   1. Voer in het veld **[!UICONTROL Goal]** de succesmaatstaf voor de test in.

      >[!NOTE]
      >
      >Controleer of [!DNL Analytics] is ingeschakeld als een gegevensbron in [!DNL Target] en of de juiste rapportsuite is geselecteerd.

   1. Stel de waarde **[!UICONTROL Priority]** in op `High` of `999` om conflicten te voorkomen wanneer gebruikers in het testsegment een onjuiste ervaring op locatie ontvangen.


   1. Selecteer in **[!UICONTROL Reporting Settings]** de **[!UICONTROL Company Name]** en **[!UICONTROL Report Suite]** die zijn verbonden met uw account voor Zoeken, Sociaal en Commerce.

      Voor extra rapporteringsuiteinden, zie &quot;[ het Melden van beste praktijken en het oplossen van problemen ](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. Voer in het veld **[!UICONTROL Date Range]** de juiste begin- en einddatum in voor de test.

   1. Selecteer **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** . Voer in het veld **[!UICONTROL Value]** de waarden [!UICONTROL Network Account ID] , [!UICONTROL Network Campaign ID] , [!UICONTROL Network Adgroup ID] of [!UICONTROL Network Ad ID] voor de relevante netwerkentiteit in Zoeken, Sociaal en Commerce in. Op deze manier kunt u de parameters van de queryreeks [!DNL Target] gebruiken voor doorklikken voor het publiek voor de entiteit.

      U kunt identiteitskaart vinden door de relevante kolom van identiteitskaart aan de entiteitmening ](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) toe te voegen.[

      ![[!UICONTROL Network Account ID] kolom in de [!UICONTROL Accounts] view ](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] kolom in de [!UICONTROL Accounts] mening ")

      Werk met uw Adobe-accountteam als u hulp nodig hebt.

   1. Selecteer **[!UICONTROL Manual (Default)]** voor **[!UICONTROL Traffic Allocation Method]** en deel het publiek 50/50.

   1. Sla de activiteit op.

1. Gebruik [ Composer van de Ervaring van het Doel Visuele ](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) om ontwerpveranderingen in het malplaatje van de A/B test het landen van de paginalplaatje aan te brengen.

   * Ervaar A: Bewerk niet omdat het de standaard/controle landende paginaervaring zonder personalisatie is.

   * Ervaring B: gebruik de gebruikersinterface van [!DNL Target] om de sjabloon van de bestemmingspagina aan te passen op basis van de elementen die in de test zijn opgenomen (zoals koppen, kopiëren, knopplaatsing en creatieve elementen).

   >[!NOTE]
   >
   >Neem bijvoorbeeld contact op met uw Adobe-accountteam voor creatieve testdoeleinden.

## Stap 2: stel uw [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics] in

[!DNL Analytics for Target] (A4T) is een integratie tussen oplossingen waarmee adverteerders [!DNL Target] -activiteiten kunnen maken op basis van [!DNL Analytics] omzettingsmaatstaven en publiekssegmenten en de resultaten vervolgens kunnen meten met [!DNL Analytics] als rapportbron. Alle rapportage en segmentatie voor die activiteit is gebaseerd op [!DNL Analytics] gegevensverzameling.

Voor meer informatie over [!DNL Analytics for Target], met inbegrip van een verbinding aan implementatieinstructies, zie &quot;[ Adobe Analytics als rapporteringsbron voor Adobe Target (A4T) ](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Het deelvenster [!DNL Analytics for Target] instellen

Configureer in Analysis Workspace de [!DNL Analytics for Target panel] om uw [!DNL Target] -activiteiten en -ervaringen te analyseren. Houd rekening met de volgende belangrijke aanwijzingen en informatie over uw rapporten.

#### Metrisch

* Creeer een paneel binnen de werkruimte specifiek voor de Adobe Advertising rekening, de campagne, of de ad groep <!-- only applicable entities? --> waarvoor de test in werking werd gesteld. Met samenvattingsweergaven kunt u Adobe Advertising-meetgegevens in hetzelfde rapport weergeven als de testprestaties van [!DNL Target] .

* Prioriteit geven aan het gebruik van onsite metriek (zoals bezoeken en conversies) om de prestaties te meten.

* Begrijp dat de samengevoegde media metriek van Adobe Advertising (zoals impressies, kliks, en kosten) niet aan [!DNL Target] metriek kan worden aangepast.

#### Afmetingen

De volgende afmetingen hebben betrekking op [!DNL Analytics for Target] :

* **Activiteiten van het Doel**: Naam van de Test A/B

* **Ervaringen van het Doel**: Namen van het landen van paginaervaringen die binnen de activiteit worden gebruikt

* **Activiteit van het Doel** > **Ervaring**: De naam van de activiteit en ervaring in de zelfde rij

### Problemen met Analyses oplossen voor [!DNL Target] gegevens

Als u in Analysis Workspace opmerkt dat de activiteit en de ervaring gegevens minimaal of niet vullen, doet u het volgende:

* Controleer of dezelfde [!UICONTROL Supplemental Data ID] (SDID) wordt gebruikt voor zowel [!DNL Target] als [!DNL Analytics] . U kunt de waarden verifiëren SDID door [ Debugger van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) op de het landen pagina te gebruiken waarop de campagne gebruikers drijft.

[Aanvullende waarden voor de gegevens-id (SDID) in Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Controleer op dezelfde landingspagina of a) de [!UICONTROL Hostname] die in de Adobe Debugger wordt weergegeven onder [!UICONTROL Solutions] > [!UICONTROL Target] overeenkomt met b) de [!UICONTROL Tracking Server] die in [!DNL Target] wordt weergegeven voor de activiteit (onder [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings] ).

  [!DNL Analytics For Target] vereist dat een [!DNL Analytics] tracking-server wordt verzonden in aanroepen van [!DNL Target] naar de [!DNL Modstats] data collection server for Analytics. <!-- just "to Analytics?"-->

[Hostnaamwaarde in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Waarde van volgserver in doel](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Verdere lezing

* [ integreer Doel met Analytics ](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - verklaart hoe te opstelling [!DNL Target] rapporterend in Analysis Workspace.
* [ A/B het Overzicht van de Test ](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Beschrijft A/B testactiviteiten, die u met Onderzoek, Sociale, &amp; de advertenties van Commerce kunt gebruiken.
* [ Overzicht van Analytics voor Advertising ](/help/integrations/analytics/overview.md) - introduceert Analytics voor Advertising, die u toestaat om klik-door en mening-door plaatsinteractie in uw instanties van Analytics te volgen.

>[!MORELIKETHIS]
>
>* [ vorm A/B Tests in Adobe Target voor de Advertenties van Advertising DSP ](ab-tests-dsp.md)
