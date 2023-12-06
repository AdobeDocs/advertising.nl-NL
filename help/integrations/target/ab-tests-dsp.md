---
title: A/B-tests configureren voor Adobe Advertising-advertenties in Adobe Target
description: Leer hoe u een A/B-test instelt in [!DNL Target] voor uw DSP advertenties.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 48f755b6f3ac00a69086fe4c7ce69d320946635b
workflow-type: tm+mt
source-wordcount: '1427'
ht-degree: 0%

---

# A/B-tests configureren in Adobe Target voor advertenties DSP advertenties

<!-- In title and Heading1:  DSP and [!DNL Advertising Search, Social, & Commerce] Ads -->

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*Adverteerders DSP alleen reclame*

Adobe Advertising en Adobe Target maken het nog eenvoudiger voor marketers om een persoonlijke en verbonden ervaring te bieden op alle betaalmedia en onsite berichten. Door signalen tussen de producten te delen, kunt u:

* Verlaag de mate van verschuiving van de site door de advertenties van klanten te koppelen van DSP campagnes aan hun ervaringen ter plaatse.

* A/B-tests uitvoeren door de ervaringen ter plaatse met reclameberichten te weerspiegelen met behulp van Adobe Audience Manager-blootstellingsgegevens en klik-naar-feed doelpubliek.

* Meet het effect van verenigde overseinen op een onsite objectieve lift met eenvoudige visualisaties in Adobe Analytics voor [!DNL Target].

Zie de volgende secties voor de eerste vereisten en voor instructies aan opstelling klik-door en mening-door het volgen, voer signaal uit het delen tussen DSP en [!DNL Target] en stelt een A/B-testactiviteit in en zet deze op [!DNL Analytics] Analysis Workspace om de testgegevens weer te geven.

Neem contact op met adcloud_support@adobe.com als u nog meer vragen hebt.

## Vereisten

Voor dit gebruiksgeval zijn de volgende producten en integraties vereist:

* [!DNL Target]

* [[!DNL Analytics] voor reclame](/help/integrations/analytics/overview.md) integratie<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integratie

* Audience Manager (alleen vereist voor doorkijktests)

## Stap 1: Opstelling het Click-through Kader {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Doorklikframework](/help/integrations/assets/target-ct-framework.png)

Wanneer u DSP macro&#39;s toevoegt aan een doorklikURL (de URL die wordt weergegeven wanneer een gebruiker op een advertentie klikt en de openingspagina bereikt), DSP automatisch de plaatsingssleutel vastleggen door `${TM_PLACEMENT_ID}` in de doorklikURL. In deze macro wordt de alfanumerieke plaatsingssleutel vastgelegd en niet de numerieke plaatsings-id.

![DoorklikURL toegevoegd aan URL landingspagina](/help/integrations/assets/target-ct-url.jpg)

### (Alleen DSP) DSP macro&#39;s toevoegen aan uw doorklikURL&#39;s

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Werk binnen het spreken van Flash of Google Campagne Manager 360, manueel klik-door URL voor elke advertentie bij om de macro&#39;s te omvatten die worden vereist om de variabelen van identiteitskaart van AMO te vangen. De variabelen van AMO ID worden gebruikt om klikgegevens naar Adobe Analytics te verzenden en plaatsingssleutels voor A/B het testen te delen. Zie de volgende pagina&#39;s voor instructies:

* [Toevoegen [!DNL Analytics for Advertising] Macro&#39;s naar [!DNL Flashtalking] Labels toevoegen](/help/integrations/analytics/macros-flashtalking.md)

* [Toevoegen [!DNL Analytics for Advertising] Macro&#39;s naar [!DNL Google Campaign Manager 360] Labels toevoegen](/help/integrations/analytics/macros-google-campaign-manager.md)

Neem contact op met het accountteam van de Adobe en de groep Advertising Solutions (aac-advertising-solutions-group@adobe.com) om de vereiste plaatsingssleutel op te halen en de installatie te voltooien en om ervoor te zorgen dat elke doorklikURL wordt gevuld met de plaatsingssleutel.

## Stap 2: Opstelling het Kader View-through Gebruikend Audience Manager {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Doorkijkkader](/help/integrations/assets/targetr-vt-framework.png)

Door een Audience Manager imitatiepixel toe te voegen in uw advertentietags en plaatsingsinstellingen, kunt u een testsegment maken voor extra mogelijkheden voor doorkijktests.

1. Hiermee implementeert u een Audience Manager-imitatiepixel in uw advertentietags en DSP plaatsingsinstellingen.

   Zie voor instructies &quot;[Blootstellingsgegevens van media verzamelen van advertenties DSP campagnes](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Controleer of u [DSP macro&#39;s](/help/dsp/campaign-management/macros.md) om alle gegevens vast te leggen die de pixel van de impressiegebeurtenis moet teruggeven, inclusief `${TM_PLACEMENT_ID_NUM}` voor de numerieke plaatsing-id.

   >[!NOTE]
   >
   >URL&#39;s die worden gevolgd door klikken bevatten de `${TM_PLACEMENT_ID}` macro voor de alfanumerieke plaatsingssleutel in plaats van `${TM_PLACEMENT_ID_NUM}` voor de numerieke plaatsing-id.

1. Vorm een segment van de Audience Manager van de gegevens van de DSP:

   1. Controleer of segmentgegevens beschikbaar zijn:

      1. [Zoeken naar het signaal](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) voor de [sleutelwaardepaar](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) dat bepaalt op welk niveau de segmentgebruikers worden gegroepeerd.

         Een [ondersteunde toets](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) met een waarde die overeenkomt met een macro die u hebt toegevoegd aan de Audience Manager-imitatiepixel.

         Als u bijvoorbeeld gebruikers voor een bepaalde plaatsing wilt groeperen, gebruikt u de opdracht `d_placement` toets. Voor de waarde gebruikt u een numerieke plaatsing-id (zoals 2501853) die door de DSP macro wordt vastgelegd `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         Als de onderzoeksresultaten gebruikertellingen voor het zeer belangrijk-waardepaar tonen, dat erop wijst dat de pixel correct werd geplaatst en de gegevens stromen, dan ga aan de volgende stap verder.

   1. [Een op regels gebaseerd kenmerk maken](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) voor het maken van segmenten in Audience Manager.

      * Geef de eigenschap een naam, zodat deze binnen de testactiviteiten gemakkelijk kan worden herkend. Sla de eigenschap op in de gewenste map.

      * Selecteren `Ad Cloud` als de **Gegevensbron**.

      * Voor de expressie trait gebruikt u `d_event` als de **Sleutel** en `imp` als de **Waarde**.

   1. [Een testsegment instellen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) voor het nieuwe kenmerk in de Audience Manager selecteert u `Ad Cloud` als de **Gegevensbron**.

      De Audience Manager splitst automatisch het segment in een controlegroep die de standaard het landen paginaervaring en een testgroep ontvangt die een gepersonaliseerde onplaatservaring ontvingen.

## Stap 3: Een &quot;A/B Test&quot;-activiteit instellen in het doel

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

In de volgende instructies wordt informatie over het DSP-gebruiksgeval gemarkeerd. Zie &quot;&quot; voor volledige instructies.

1. [Aanmelden bij Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Een A/B-test maken](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. In de **URL voor activiteit invoeren** Voer de URL van de bestemmingspagina voor de test in.

      >[!NOTE]
      >
      >U kunt meerdere URL&#39;s gebruiken om het doorzoeken van sites te testen. Zie voor meer informatie &quot;[Meerdere pagina&#39;s](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; U kunt de bovenste items gemakkelijk herkennen aan de hand van de pagina-URL door een [Rapport over sitetoegang](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) in Analytics.

   1. In de **Goal** voert u de succesmetrische waarde voor de test in.

      >[!NOTE]
      >
      >Controleer of [!DNL Analytics] is ingeschakeld als gegevensbron binnen [!DNL Target]en dat de juiste rapportsuite is geselecteerd.

   1. Stel de **Prioriteit** tot `High` of `999` om conflicten te voorkomen wanneer gebruikers in het testsegment een onjuiste ervaring op locatie ontvangen.

   1. Within **Rapportinstellingen**, selecteert u de **Bedrijfsnaam** en **Rapportsuite** is verbonden met uw DSP account.

      Zie &quot;[Best practices en probleemoplossing rapporteren](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. In de **Datumbereik** Voer de juiste begin- en einddatum voor de test in.

   1. Soorten publiek toevoegen aan de activiteit:

      1. Kies de optie [segment dat u eerder in Audience Manager creeerde om mening door publiek te testen](#view-through-framework).

      1. Selecteren **Sitepagina&#39;s** > **Openingspagina** > **Query** en voert u de DSP plaatsingssleutel in het dialoogvenster **Waarde** veld voor gebruik van de parameters van de doelqueryreeks voor doorklikken.

   1. Voor de **Methode voor verkeerstoewijzing**, selecteert u **Handmatig (standaard)** en splitst het publiek 50/50.

   1. Sla de activiteit op.

1. Gebruiken [!DNL Target] [Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) om ontwerpwijzigingen aan te brengen in de sjabloon voor de landingspagina van de A/B-test.

   * Ervaar A: Bewerk niet omdat het de standaard/controle landende paginaervaring zonder personalisatie is.

   * Ervaring B: De [!DNL Target] gebruikersinterface om de landingspagina-sjabloon aan te passen op basis van de elementen die in de test zijn opgenomen (zoals kopregels, kopiëren, knopplaatsing en creatieve elementen).

   >[!NOTE]
   >
   >Neem bijvoorbeeld contact op met het accountteam van uw Adobe voor creatieve testdoeleinden.

## Stap 4: Stel uw [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) is een integratie tussen oplossingen die adverteerders in staat stelt [!DNL Target] activiteiten op basis van [!DNL Analytics] conversiemetriek en publiekssegmenten en meet de resultaten vervolgens met [!DNL Analytics] als de bron van de rapportage. Alle rapportage en segmentering voor die activiteit zijn gebaseerd op [!DNL Analytics] gegevensverzameling.

Voor meer informatie over [!DNL Analytics for Target], met inbegrip van een koppeling naar de uitvoeringsinstructies, zie &quot;[Adobe Analytics als bron van rapportage voor Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Stel de [!DNL Analytics for Target] Deelvenster

In Analysis Workspace configureert u de [!DNL Analytics for Target panel] om uw [!DNL Target] activiteiten en ervaringen. Houd rekening met de volgende belangrijke aanwijzingen en informatie over uw rapporten.

#### Metrisch

* Maak een deelvenster in de werkruimte dat specifiek is voor de Adobe Advertising-campagne, het -pakket of de -plaatsing waarvoor de test is uitgevoerd. De summiere visualisaties van het gebruik om Adobe Advertising metriek in het zelfde rapport te tonen zoals de de testprestaties van het Doel.

* Prioriteit geven aan het gebruik van onsite metriek (zoals bezoeken en conversies) om de prestaties te meten.

* Begrijp dat de samengevoegde media metriek van Adobe Advertising (zoals impressies, kliks, en kosten) niet aan de metriek van het Doel kan worden aangepast.

#### Dimensionen

De volgende afmetingen hebben betrekking op [!DNL Analytics for Target]:

* **Doelactiviteiten**: Naam van de A/B-test

* **Doelervaringen**: Namen van ervaringen met landingspagina&#39;s die binnen de activiteit worden gebruikt

* **Doelactiviteit** > **Ervaring**: De naam van de activiteit en de ervaring in dezelfde rij

### Analyses voor probleemoplossing voor [!DNL Target] Gegevens

Als u in Analysis Workspace opmerkt dat de activiteit en de ervaring gegevens minimaal of niet vullen, doet u het volgende:

* Controleer of dezelfde SDID (Supplemental Data ID) wordt gebruikt voor zowel Doel als Analytics. U kunt de waarden van SDID verifiëren door [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) op de landingspagina waarop de campagne de gebruikers drijft.

[Aanvullende waarden voor de gegevens-id (SDID) in de Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Controleer op dezelfde landingspagina of a) de hostnaam in de Adobe Debugger onder Oplossingen > Doel overeenkomt met b) de trackingserver die wordt weergegeven in [!DNL Target] voor de activiteit (onder Doelstellingen en instellingen > Rapportinstellingen).

  [!DNL Analytics For Target] vereist een [!DNL Analytics] volgende server die in vraag van moet worden verzonden [!DNL Target] aan de [!DNL Modstats] gegevensverzamelingsserver voor Analytics.<!-- just "to Analytics?"-->

[Hostnaamwaarde in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Waarde van volgserver in doel](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Verdere lezing

* [Doel integreren met analyse](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)- Verklaart hoe te opstelling de Rapportering van het Doel in Analysis Workspace.
* [A/B-testoverzicht](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Beschrijft A/B testactiviteiten, die u met DSP advertenties kunt gebruiken.
* [Ervaringen en aanbiedingen](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Verklaringen [!DNL Target] hulpmiddelen om de inhoud ter plaatse te bepalen waaraan DSP testgebruikers worden blootgesteld.
* [Signalen, Traits en Segmenten](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Hiermee definieert u een aantal Audience Managers die u kunnen helpen bij DSP doorkijktests.
* [Overzicht van analytische gegevens voor reclame](/help/integrations/analytics/overview.md) - Introduceert Analytics voor Advertising, waarmee u doorklikinteracties en doorkijkinteracties van sites in uw Analytics-instanties kunt bijhouden.

<!-- 
>[!MORELIKETHIS]
>
>* 
-->