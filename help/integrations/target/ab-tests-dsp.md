---
title: A/B-tests configureren voor Adobe Advertising DSP-advertenties in Adobe Target
description: Leer hoe te opstelling een test A/B in  [!DNL Target]  voor uw advertenties van DSP.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: bbb5feaf96a9be28e112544e34f11fc8f7015946
workflow-type: tm+mt
source-wordcount: '1411'
ht-degree: 0%

---

# A/B-tests configureren in Adobe Target voor Advertising DSP Ads

*Advertisers met slechts Advertising DSP*

Adobe Advertising en Adobe Target maken het nog eenvoudiger voor marketers om een gepersonaliseerde en verbonden ervaring te bieden op alle betaalmedia en onsite berichten. Door signalen tussen de producten te delen, kunt u:

* Verlaag de mate waarin de site doorvalt door de advertenties van klanten van DSP-campagnes te koppelen aan hun ervaringen ter plaatse.

* A/B-tests maken door de ervaringen ter plaatse te weerspiegelen met advertentiemateriaal met behulp van Adobe Audience Manager-belichtingsgegevens en klik-naar-feed [!DNL Target] publiek.

* Meet het effect van verenigde overseinen op een onsite objectieve lift met eenvoudige visualisaties in Adobe Analytics for [!DNL Target].

Zie de volgende secties voor de voorwaarden en voor instructies voor het instellen van doorklikken en doorzien van beelden, het implementeren van signaaldeling tussen DSP en [!DNL Target] en het instellen van een A/B-testactiviteit, en het instellen van [!DNL Analytics] Analysis Workspace om de testgegevens weer te geven.

Neem contact op met adcloud_support@adobe.com als u nog meer vragen hebt.

## Vereisten

Voor dit gebruiksgeval zijn de volgende producten en integraties vereist:

* [!DNL Target]

* [[!DNL Analytics]  voor Advertising ](/help/integrations/analytics/overview.md) integratie <!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics]  voor  [!DNL Target] ](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integratie

* Audience Manager (alleen vereist voor doorkijktests)

## Stap 1: Opstelling het Click-through Kader {#click-through-framework}

![ klik-door kader ](/help/integrations/assets/target-ct-framework.png)

Wanneer u DSP-macro&#39;s toevoegt aan een doorklikURL (de URL die wordt weergegeven wanneer een gebruiker op een advertentie klikt en de landingspagina bereikt), legt DSP automatisch de plaatsingssleutel vast door `${TM_PLACEMENT_ID}` op te nemen in de doorklikURL. In deze macro wordt de alfanumerieke plaatsingssleutel vastgelegd en niet de numerieke plaatsings-id.

![ klik-door URL wordt toegevoegd aan de het landen pagina URL ](/help/integrations/assets/target-ct-url.jpg)

### (Alleen DSP) DSP-macro&#39;s toevoegen aan uw doorklikURL&#39;s

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Werk in Flash Talk of Google Campagne Manager 360 de doorklikURL voor elke advertentie handmatig bij om de macro&#39;s op te nemen die nodig zijn om AMO-id-variabelen vast te leggen. De variabelen van AMO ID worden gebruikt om klikgegevens naar Adobe Analytics te verzenden en plaatsingssleutels voor A/B het testen te delen. Zie de volgende pagina&#39;s voor instructies:

* [ voeg  [!DNL Analytics for Advertising]  Macro&#39;s aan  [!DNL Flashtalking]  toe - Markeringen ](/help/integrations/analytics/macros-flashtalking.md). **Nota:** Deze procedure is niet noodzakelijk als uw organisatie een direct partnerschap met [!DNL Flashtalking] heeft en u gegevens-pas macro&#39;s gebruikt om klikgegevens per [!DNL Flashtalking] steundocumentatie bij `https://support.flashtalking.com%2Fhc%2Fen-us%2Farticles%2F4409808166419-Accessing-Data-Pass-Macros` te verzamelen.

* [Voeg  [!DNL Analytics for Advertising]  Macro&#39;s aan  [!DNL Google Campaign Manager 360]  toe en Markeringen](/help/integrations/analytics/macros-google-campaign-manager.md)

Neem contact op met uw Adobe-accountteam en de Advertising Solutions Group (aac-advertising-solutions-group@adobe.com) om de vereiste plaatsingssleutel op te halen en de installatie te voltooien en om ervoor te zorgen dat elke doorklikURL wordt gevuld met de plaatsingssleutel.

## Stap 2: Opstelling het Kader View-through Gebruikend Audience Manager {#view-through-framework}

![ mening-door kader ](/help/integrations/assets/targetr-vt-framework.png)

Door een Audience Manager-imitatiepixel toe te voegen in uw advertentietags en plaatsingsinstellingen, kunt u een testsegment maken voor extra mogelijkheden voor doorkijktests.

1. Implementeer een Audience Manager-imitatiepixel in uw advertentietags en DSP-plaatsingsinstellingen.

   Voor instructies, zie &quot;[ de Gegevens van de Belichting van Media van de Campagnes van Advertising DSP ](/help/integrations/audience-manager/media-data-integration/collect.md) verzamelen.&quot;

   Zorg ervoor u [ de macro&#39;s van DSP ](/help/dsp/campaign-management/macros.md) toevoegt om alle gegevens te vangen u de pixel van de impositiegebeurtenis wilt teruggeven, met inbegrip van `${TM_PLACEMENT_ID_NUM}` voor numerieke plaatsingsidentiteitskaart

   >[!NOTE]
   >
   >Klik-volgende URLs omvat de `${TM_PLACEMENT_ID}` macro voor de alfanumerieke plaatsingssleutel, in plaats van `${TM_PLACEMENT_ID_NUM}` voor numerieke plaatsings identiteitskaart

1. Configureer een Audience Manager-segment van de DSP-impressiegegevens:

   1. Controleer of segmentgegevens beschikbaar zijn:

      1. [ Onderzoek naar het signaal ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) voor het [ zeer belangrijk-waardepaar ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) dat bepaalt op welk niveau de segmentgebruikers worden gegroepeerd.

         Gebruik a [ gesteunde sleutel ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) met een waarde die aan een macro beantwoordt die u aan het pixel van de de impositiegebeurtenis van Audience Manager toevoegde.

         Als u bijvoorbeeld gebruikers voor een bepaalde plaatsing wilt groeperen, gebruikt u de `d_placement` -toets. Voor de waarde gebruikt u een numerieke plaatsing-id (zoals 2501853) die wordt vastgelegd door de DSP-macro `${TM_PLACEMENT_ID_NUM}` . <!-- Explain where to find the placement ID, other than in a custom report. -->

         Als de onderzoeksresultaten gebruikertellingen voor het zeer belangrijk-waardepaar tonen, dat erop wijst dat de pixel correct werd geplaatst en de gegevens stromen, dan ga aan de volgende stap verder.

   1. [ creeer een op regel-gebaseerd bezit ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) voor segmentverwezenlijking in Audience Manager.

      * Geef de eigenschap een naam, zodat deze binnen de testactiviteiten gemakkelijk kan worden herkend. Sla de eigenschap op in de gewenste map.

      * Selecteer `Ad Cloud` als de **[!UICONTROL Data Source]** .

      * Gebruik voor de expressie trait `d_event` als de **[!UICONTROL Key]** en `imp` als de **[!UICONTROL Value]** .

   1. [ opstelling een testsegment ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) voor het nieuwe bezit in Audience Manager, die `Ad Cloud` als **[!UICONTROL Data Source]** selecteren.

      Audience Manager splitst het segment automatisch in een controlegroep die de standaard landende paginaervaring en een testgroep ontvangt die een gepersonaliseerde onsite ervaring ontvingen.

## Stap 3: Een testactiviteit A/B instellen in [!DNL Target] voor DSP

In de volgende instructies wordt informatie over het DSP-gebruiksgeval gemarkeerd.

1. [ Login aan Adobe Target ](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [ creeer een test A/B ](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. Voer in het veld **[!UICONTROL Enter Activity URL]** de URL van de bestemmingspagina voor de test in.

      >[!NOTE]
      >
      >U kunt meerdere URL&#39;s gebruiken om het doorzoeken van sites te testen. Voor meer informatie, zie &quot;[ Multipage Activiteit ](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; U kunt bovenkant ingangen door pagina URL gemakkelijk identificeren door het rapport van de Ingang van de a [ Plaats ](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports) in Analytics te creëren.

   1. Voer in het veld **[!UICONTROL Goal]** de succesmaatstaf voor de test in.

      >[!NOTE]
      >
      >Controleer of [!DNL Analytics] is ingeschakeld als een gegevensbron in [!DNL Target] en of de juiste rapportsuite is geselecteerd.

   1. Stel de waarde **[!UICONTROL Priority]** in op `High` of `999` om conflicten te voorkomen wanneer gebruikers in het testsegment een onjuiste ervaring op locatie ontvangen.

   1. Selecteer in **[!UICONTROL Reporting Settings]** de **[!UICONTROL Company Name]** en **[!UICONTROL Report Suite]** die zijn verbonden met uw DSP-account.

      Voor extra rapporteringsuiteinden, zie &quot;[ het Melden van beste praktijken en het oplossen van problemen ](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. Voer in het veld **[!UICONTROL Date Range]** de juiste begin- en einddatum in voor de test.

   1. Soorten publiek toevoegen aan de activiteit:

      1. Kies het [ segment dat u eerder in Audience Manager aan testmening-door publiek ](#view-through-framework) creeerde.

      1. Selecteer **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** en typ de DSP-plaatsingssleutel in het **[!UICONTROL Value]** -veld om de parameters van de doelqueryreeks te gebruiken voor doorklikken.

   1. Selecteer **[!UICONTROL Manual (Default)]** voor **[!UICONTROL Traffic Allocation Method]** en deel het publiek 50/50.

   1. Sla de activiteit op.

1. Gebruik [ Composer van de Ervaring van het Doel Visuele ](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) om ontwerpveranderingen in het malplaatje van de A/B test het landen van de paginalplaatje aan te brengen.

   * Ervaar A: Bewerk niet omdat het de standaard/controle landende paginaervaring zonder personalisatie is.

   * Ervaring B: gebruik de gebruikersinterface van [!DNL Target] om de sjabloon van de bestemmingspagina aan te passen op basis van de elementen die in de test zijn opgenomen (zoals koppen, kopiëren, knopplaatsing en creatieve elementen).

   >[!NOTE]
   >
   >Neem bijvoorbeeld contact op met uw Adobe-accountteam voor creatieve testdoeleinden.

## Stap 4: stel uw [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics] in

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) is een integratie tussen oplossingen waarmee adverteerders [!DNL Target] -activiteiten kunnen maken op basis van [!DNL Analytics] omzettingsmaatstaven en publiekssegmenten en de resultaten vervolgens kunnen meten met [!DNL Analytics] als rapportbron. Alle rapportage en segmentatie voor die activiteit is gebaseerd op [!DNL Analytics] gegevensverzameling.

Voor meer informatie over [!DNL Analytics for Target], met inbegrip van een verbinding aan implementatieinstructies, zie &quot;[ Adobe Analytics als rapporteringsbron voor Adobe Target (A4T) ](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Het deelvenster [!DNL Analytics for Target] instellen

Configureer in Analysis Workspace de [!DNL Analytics for Target panel] om uw [!DNL Target] -activiteiten en -ervaringen te analyseren. Houd rekening met de volgende belangrijke aanwijzingen en informatie over uw rapporten.

#### Metrisch

* Maak een deelvenster binnen de werkruimte die specifiek is voor de Adobe Advertising-campagne, -pakket of -plaatsing waarvoor de test is uitgevoerd. Met samenvattingsweergaven kunt u Adobe Advertising-meetgegevens in hetzelfde rapport weergeven als de testprestaties van [!DNL Target] .

* Prioriteit geven aan het gebruik van onsite metriek (zoals bezoeken en conversies) om de prestaties te meten.

* Begrijp dat de samengevoegde media metriek van Adobe Advertising (zoals impressies, kliks, en kosten) niet aan [!DNL Target] metriek kan worden aangepast.

#### Afmetingen

De volgende afmetingen hebben betrekking op [!DNL Analytics for Target] :

* **[!UICONTROL Target Activities]**: naam van de A/B-test

* **[!UICONTROL Target Experiences]**: Namen van ervaringen met bestemmingspagina&#39;s die binnen de activiteit worden gebruikt

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**: De naam van de activiteit en ervaring in dezelfde rij

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
* [ A/B het Overzicht van de Test ](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - beschrijft A/B testactiviteiten, die u met de advertenties van DSP kunt gebruiken.
* [ Ervaringen en aanbiedingen ](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Verklaart [!DNL Target] hulpmiddelen om de inhoud ter plaatse te bepalen waaraan de testgebruikers van DSP worden blootgesteld.
* [ de Signalen, de Sporen, en de Segmenten ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - bepalen enkele hulpmiddelen van Audience Manager die met het mening-door testen van DSP kunnen helpen.
* [ Overzicht van Analytics voor Advertising ](/help/integrations/analytics/overview.md) - introduceert Analytics voor Advertising, die u toestaat om klik-door en mening-door plaatsinteractie in uw instanties van Analytics te volgen.

>[!MORELIKETHIS]
>
>* [ vorm A/B Tests in Adobe Target voor het Onderzoek van Advertising, Sociale, &amp; Advertenties van Commerce ](ab-tests-search.md)
