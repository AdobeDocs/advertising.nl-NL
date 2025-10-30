---
title: Aangepaste rapporten
description: Leer over opties om douanerapporten manueel tot stand te brengen of pre-gevormde rapportmalplaatjes te gebruiken.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: f2b912a9e4952d2ccb9a461cdbc56c7bc731e690
workflow-type: tm+mt
source-wordcount: '1560'
ht-degree: 0%

---

# Aangepaste rapporten

Met aangepaste rapporten kunt u de inhoud en levering van uw rapportgegevens aanpassen aan de hand van de campagneafmetingen (zoals de adverteerder, plaatsing, sites of geos) en de maatstaven die het belangrijkst voor u zijn. U kunt:

* Vorm volledig de rapporten van de campagneprestaties op een korrelig niveau.

* Kies uit vooraf geconfigureerde rapportsjablonen en pas deze desgewenst verder aan.

U kunt rapporten eens produceren, of hen dagelijks, wekelijks, of maandelijks bij 03 :00 in de gespecificeerde tijdzone volgens gespecificeerde criteria (zoals om de 15 dagen of op de 1e van elke maand) plannen. Zodra een rapport wordt geproduceerd, kunt u het van [!UICONTROL Reports] > [!UICONTROL Custom Reports] of van verbonden [&#x200B; rapportbestemmingen &#x200B;](/help/dsp/reports/report-destinations/report-destination-about.md) van de volgende types downloaden:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

>[!NOTE]
>
>U kunt gegevens op bestelling op alle niveaus van een campagne (campagne, pakket, plaatsing, of advertentie) ook bekijken [&#x200B; binnen de relevante mening van het campagnebeheer &#x200B;](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Beschikbare rapporttypen

* **[!UICONTROL Custom]:** Dit rapport is een leeg malplaatje dat u kunt gebruiken om uw eigen douanerapport tot stand te brengen gebruikend de meeste dimensies en metriek. Rapporten [!UICONTROL Conversion] , [!UICONTROL Device] , [!UICONTROL Geo] en [!UICONTROL Site] zijn variaties van deze sjabloon met vooraf geselecteerde kolommen en dimensies voor hun respectievelijke gebruiksgevallen.

* Vooraf geconfigureerde rapportsjablonen

   * **[!UICONTROL Billing]:** gebruik dit rapport om zeer belangrijke het factureren metriek zoals uitgavenmetriek voor media het factureren door campagne te begrijpen. Gegevens zijn niet beschikbaar voor plaatsen die universele id&#39;s als doel hebben.

     >[!NOTE]
     >
     >Dit rapport bevat gegevens over het factureringssegment. Als een gebruiker of een apparaat een indruk krijgt die tot veelvoudige segmenten behoort, slechts wordt één factureerbare segment met de indruk gecrediteerd.

   * **[!UICONTROL Conversion]:** gebruik dit rapport om te begrijpen hoe uw campagnes worden uitgevoerd op basis van conversiemetriek die is vastgelegd met behulp van het bijhouden van Adobe Advertising-conversies. Dit rapport bevat multi-touchattributie.

  <!--
    * **[!UICONTROL Custom Creative Report Beta]:** (Beta feature) Use this report to monitor performance across your Advertising Creative ad experiences.
    -->

   * **[!UICONTROL Device]:** gebruik deze vooraf ingevulde sjabloon om belangrijke metriek per apparaat-gerelateerde afmetingen te zien.

   * **[!UICONTROL Frequency (by Impression)]:** gebruik dit rapport om de distributie te begrijpen van de beelden die aan unieke kijkers worden getoond (bijvoorbeeld, hoeveel unieke kijkers één indruk, twee beelden, drie beelden, etc. zagen. Gegevens zijn beschikbaar via plaatsing of campagne.

     >[!NOTE]
     >
     >* Gegevens zijn beschikbaar na 1 maart 2019.
     >* De frequentie wordt geschat op basis van een steekproef van gegevens.
     >* Voor sommige inventarisaties geven uitgevers geen apparaat-id door, waardoor het bijhouden van de frequentie wordt verhinderd. Dit rapport bevat alleen afbeeldingen waarvoor een apparaat-id beschikbaar was.

   * **[!UICONTROL Frequency (by App/Site)]:** gebruik dit rapport om te begrijpen hoeveel unieke gebruikers uw advertenties per app of per site hebben bereikt. U kunt ook zien hoeveel unieke gebruikers uw advertenties hebben bereikt via alleen een bepaalde app of site (&quot;verschillende unieke gebruikers&quot;).

     >[!NOTE]
     >
     >* Gegevens zijn beschikbaar na 15 november 2018.
     >* Voor sommige privéinventarisaties geven uitgevers geen apparaat-id door, waardoor het bijhouden van de frequentie wordt verhinderd.

   * **[!UICONTROL Geo]**: Gebruik deze vooraf ingevulde sjabloon om de belangrijkste metriek op geografische afmetingen weer te geven.

   * **[!UICONTROL Margin]:** gebruik dit rapport om zeer belangrijke metriek zoals marge, winst, en andere uitgavenmetriek door campagne of plaatsing te zien. Gegevens zijn niet beschikbaar voor plaatsen die universele id&#39;s als doel hebben.

   * **[!UICONTROL Segment]:** gebruik dit vooraf ingevulde malplaatje om zeer belangrijke metriek door segment te zien.

     >[!NOTE]
     >
     >* Dit rapport is bedoeld om te tonen hoe de verschillende doelsegmenten presteren. Het gebruikt de gegevens van het segmentlidmaatschap. Wanneer een persoon of een apparaat dat tot twee of meer doelsegmenten behoort, de indruk krijgt, bevat dit rapport één rij voor elk segment. Daarom komen de totalen in dit rapport mogelijk niet overeen met de werkelijke levering.
     >* De metriek van de omzetting en de gegevens van het douanedoel voor segmenten zijn beschikbaar na 2 augustus 2019. Alle andere gegevens voor segmenten zijn beschikbaar vanaf 1 juni 2018.

   * **[!UICONTROL Site]:** door gebrek, omvat standaardmetriek, totale media netto uitgaven, en totale factureerbare netto uitgaven door plaats.

   * **[!UICONTROL Household Reach & Frequency]:** gebruik dit rapport om beelden, bereik en frequentie voor één enkele afmeting over ad formaten op het niveau van het huishouden te zien die op IP adres, eerder dan op een apparaat/koekjesniveau wordt gebaseerd. Gebruik de inzichten om uw media mengeling te optimaliseren, prestaties te verbeteren, en mogelijkheden voor stijgende bereik te identificeren. Zie &quot;[&#x200B; FAQs over de Rapporten van de Huishouden &#x200B;](/help/dsp/reports/faq-reports.md)&quot;voor meer informatie. Gegevens zijn niet beschikbaar voor plaatsen die universele id&#39;s als doel hebben.

   * **[!UICONTROL Household Conversions]:** gebruik dit rapport om mening-door omzettingen op het niveau van het huishouden te zien die op IP adres, eerder dan op een apparaat/koekjesniveau wordt gebaseerd. Gebruik de inzichten om campagneprestaties te meten en te optimaliseren. Zie &quot;[&#x200B; FAQs over de Rapporten van de Huishouden &#x200B;](/help/dsp/reports/faq-reports.md)&quot;voor meer informatie. Gegevens zijn niet beschikbaar voor plaatsen die universele id&#39;s als doel hebben.

   * **[!UICONTROL Path to Conversion]:** gebruik dit rapport om te identificeren hoe u budgetten optimaliseert en advertenties personaliseert op basis van de best presterende en interactiereeksen. Het rapport bevat de reeks interactiepunten in hetzelfde huishouden die leiden tot elk van de geselecteerde conversiemetriek in het opgegeven gegevensbereik. Het rapport gebruikt een gespecificeerde raadplegingsperiode tussen de eerste interactie en een omzetting en kan één dimensie omvatten:

      * [!UICONTROL Channel Assist Type]: laat zien hoe de volgende marketingkanalen het conversieproces hebben geholpen: [!UICONTROL Audio Impression] , [!UICONTROL CTV Impression] , [!UICONTROL Display Click] , [!UICONTROL Display Impression] , [!UICONTROL Native Click] , [!UICONTROL Native Impression] , [!UICONTROL Search Click] , [!UICONTROL Video Click] of [!UICONTROL Video Impression] .

      * [!UICONTROL Campaign ID] of [!UICONTROL Campaign Name]: toont welke campagnes het conversieproces hebben ondersteund.

      * [!UICONTROL Ad ID] of [!UICONTROL Ad Name] geeft aan welke DSP-advertenties hebben geresulteerd in conversies.

      * [!UICONTROL Ad ID & Paid Keyword (SSC)] of [!UICONTROL Ad Name & Paid Keyword (SSC)] toont welke trefwoorden voor Zoeken, Sociaal en Commerce hebben geresulteerd in conversies.

     De kolommen in het rapport omvatten &quot;[!UICONTROL Event #1]&quot;door &quot;[!UICONTROL Event #10],&quot;&quot;[!UICONTROL Path Length], &quot;% \&lt;Metrische Naam van de Omzetting 1 \>,&quot;&quot;% \&lt;Metrische Naam van de Omzetting 2 \>,&quot;etc.

     Tot de 10 meest recente interactiepunten zijn inbegrepen. De padrijen worden geordend met het aantal conversies.

     Voor een vergelijking van dit rapport aan rapporten die door [!DNL Advanced Measurement Services] en Analytische Adobe worden gecreeerd, zie &quot;[&#x200B; FAQs over de Rapporten van de Douane &#x200B;](/help/dsp/reports/faq-reports.md).&quot;

   * **[!UICONTROL Path Length]:** gebruik dit rapport om het aantal punten van de gebruikersinteractie te volgen die voor omzettingen in tijd worden vereist zodat u de optimale en frequentie kunt kiezen. Het rapport toont het aantal omzettingen door weglengte (interactiepunten), zoals hoeveel omzettingen voorkwamen nadat de gebruikers slechts één ad interactie, twee en interactie, etc. hadden. Het rapport kan gegevens voor veelvoudige omzettingsmetriek omvatten en gebruikt een gespecificeerde raadplegingsperiode tussen de eerste interactie en een omzetting. De kolommen in het rapport omvatten &quot;[!UICONTROL Path Length],&quot; &quot;[!UICONTROL Number of] \&lt;Conversion Metric Name 1\>,&quot; &quot;% \&lt;Conversion Metric Name 1\>,&quot; \&lt;Conversion Metric Name 2\>, &quot;% \&lt;Conversion Metric Name 2\>,&quot; etc.

     De gegevens worden weergegeven voor elke padlengte van maximaal 10 en gegevens voor padlengten van meer dan 10 worden gegroepeerd.

   * **[!UICONTROL Time to Conversion]:** gebruik dit rapport om het optimale venster van de attributieraadpleging te bepalen en campagnes met langere tijden aan omzetting te identificeren, die van het opnieuw richten kunnen profiteren. Het rapport toont het aantal omzettingen door de tijdsduur in dagen van de laatste interactie (en blootstelling of klik) aan omzetting. Het rapport kan gegevens voor veelvoudige omzettingsmetriek omvatten en gebruikt een gespecificeerde raadplegingsperiode tussen de eerste interactie en een omzetting. De kolommen in het rapport omvatten &quot;[!UICONTROL Time Taken (in days)],&quot; &quot;[!UICONTROL Number of] \&lt;Conversion Metric Name 1\>,&quot; &quot;% \&lt;Conversion Metric Name 1\>,&quot; \&lt;Conversion Metric Name 2\>, &quot;% \&lt;Conversion Metric Name 2\>,&quot; etc. De omzettingen die langer duren dan de raadplegingsperiode worden gegroepeerd in één rij (bijvoorbeeld, als het rapport een periode van de 30 dagraadpleging gebruikt, dan worden alle omzettingen die langer duren dan 30 dagen om voor te komen gegroepeerd in een rij met een &quot;[!UICONTROL Time Taken (in days)]&quot;waarde van &quot;30+&quot;).

   * **[!UICONTROL Content]:** gebruik dit rapport om een goed begrip te krijgen van de aflevering van de indruk en andere maatstaven op basis van opgegeven afmetingen (zoals genre, productiekwaliteit en classificatie van inhoud), zodat u de functie voor afstemmen kunt optimaliseren en de merkveiligheid kunt garanderen. Naast inhoudsafmetingen bevat het rapport de meeste standaardafmetingen, meetgegevens en filters. Gegevens per inhoudsdimensie zijn beschikbaar voor [!DNL Freewheel] , [!DNL Index] , [!DNL Magnite] , [!DNL Microsoft] , [!DNL Nexxen] , [!DNL Pubmatic] , [!DNL Sharethrough] en [!DNL Triplelift] . Inhoudssignalen worden door uitgevers doorgegeven tijdens de bidstream en zijn afhankelijk van beschikbaarheid.

## Rapportage tussen accounts {#cross-account-reporting}

Elke organisatie met meerdere DSP-accounts kan desgewenst gegevens voor meerdere accounts mogelijk maken in aangepaste rapporten, afhankelijk van de behoeften van de organisatie. U kunt bijvoorbeeld Account A toegang geven tot de gegevens van Account B en Account B toegang geven tot de gegevens van Account C (maar niet van Account A). Neem contact op met uw Adobe-accountteam om deze functie in te schakelen en te configureren.

Zodra de eigenschap voor uw organisatie wordt toegelaten, kunt u [&#x200B; &#x200B;](report-settings.md) om het even welke volgende rapporttypes door rekening filtreren: [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], en [!UICONTROL Conversion].

Uw accountinstellingen op [!UICONTROL Settings] > [!UICONTROL Account] geven a) de andere accounts aan waarvan de gegevens beschikbaar zijn voor uw account en b) de andere accounts die toegang hebben tot de gegevens van uw account.

## De [!UICONTROL Custom Reports] -weergave

[!UICONTROL Reports] > [!UICONTROL Custom Reports] geeft een overzicht van uw bestaande rapporten, inclusief gegenereerde rapporten, rapporten die zijn gepland voor toekomstige generatie en rapporten die zijn mislukt. De kolom &quot;[!UICONTROL Report Run]&quot;toont data waarop het rapport werd teweeggebracht die op 22 augustus 2024 begonnen. Standaard worden alle niet-gearchiveerde rapporten die door de gebruiker zijn gemaakt, weergegeven met de meest recente bovenaan. U kunt de lijst door status verder filtreren, of het rapport terugkomt of eenmalig, het rapporttype, het bestemmingstype, en de rapportschepper is.

U kunt nieuwe douanerapporten tot stand brengen, bestaande rapporten uitgeven of hen dupliceren om nieuwe rapporten tot stand te brengen, rapporten onmiddellijk in werking te stellen, om het even welke rapportinstantie van de laatste vier maanden te downloaden, en rapporten te schrappen.

## Statussen rapporteren {#custom-report-status}

* **[!UICONTROL Yet to start]:** Het rapport is nooit uitgevoerd.

* **[!UICONTROL Report generating]:** Het rapport wordt momenteel gemaakt.

* **[!UICONTROL Ready to download]:** (Terugkerende rapporten slechts) één of meerdere instanties van het rapport is beschikbaar om te downloaden, en meer rapportinstanties zijn gepland.

* **[!UICONTROL Failed]:** De rapporttaak is mislukt. Om te zien waarom de individuele rapportinstanties voor een rapportduw ontbroken, klik ![&#x200B; de benedenpijl &#x200B;](/help/dsp/assets/chevron-down.png " pijl ") naast [!UICONTROL Download]. Mislukte rapporttaken zijn vermeld met een foutenpictogram (![foutindicator](/help/dsp/assets/indicator-critical.png "foutindicator")). Plaats de cursor op het foutpictogram voor een beschrijving van de fout.

* **[!UICONTROL Completed]:** Voor niet-terugkerende rapporten, wordt het rapport voltooid. Voor terugkerende rapporten, worden alle rapportinstanties voltooid. U kunt alle rapporten downloaden die in de laatste vier maanden zijn voltooid.

* **[!UICONTROL Archived]:** het rapport is gearchiveerd en kan niet in werking worden gesteld. Deze status wordt geplaatst wanneer de rapportgeneratie veelvoudige tijden voor een rapport ontbreekt. U kunt deze status momenteel niet instellen vanuit de gebruikersinterface.

>[!MORELIKETHIS]
>
>* [&#x200B; creeer een Rapport van de Douane &#x200B;](/help/dsp/reports/report-create.md)
>* [&#x200B; Download een Rapport van de Douane &#x200B;](/help/dsp/reports/report-download.md)
>* [&#x200B; de Montages van het Rapport van de Douane &#x200B;](/help/dsp/reports/report-settings.md)
>* [&#x200B; Veelgestelde vragen over de Rapporten van de Huishouden &#x200B;](/help/dsp/reports/faq-reports.md)
>* [&#x200B; Types van Rapporten van Prestaties in de Meningen van het Beheer van de Campagne &#x200B;](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [&#x200B; Beschikbare Kolommen van het Rapport &#x200B;](/help/dsp/reports/report-columns.md)
>* [&#x200B; Over [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
