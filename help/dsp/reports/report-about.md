---
title: Aangepaste rapporten
description: Leer over opties om douanerapporten manueel tot stand te brengen of pre-gevormde rapportmalplaatjes te gebruiken.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 0ecceaf30ce135dd0083e34dd5c8c5bafb5a3c16
workflow-type: tm+mt
source-wordcount: '1466'
ht-degree: 0%

---

# Aangepaste rapporten

Met aangepaste rapporten kun je de content en levering van je rapportdata aanpassen aan de hand van de campagnedimensies (zoals de adverteerder, plaatsing, sites of geo’s) en de metrics die voor jou het belangrijkst zijn. U kunt:

* Vorm volledig de rapporten van de campagneprestaties op een korrelig niveau.

* Kies uit vooraf geconfigureerde rapportsjablonen en pas deze desgewenst verder aan.

U kunt rapporten eenmaal genereren of dagelijks, wekelijks of maandelijks om 3:00 uur plannen in de opgegeven tijdzone volgens opgegeven criteria (zoals elke 15 dagen of op de eerste van elke maand). Zodra een rapport wordt geproduceerd, kunt u het van [!UICONTROL Reports] > [!UICONTROL Custom Reports] of van verbonden [ rapportbestemmingen ](/help/dsp/reports/report-destinations/report-destination-about.md) van de volgende types downloaden:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

>[!NOTE]
>
>U kunt gegevens op bestelling op alle niveaus van een campagne (campagne, pakket, plaatsing, of advertentie) ook bekijken [ binnen de relevante mening van het campagnebeheer ](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Beschikbare rapporttypen

* **[!UICONTROL Custom]:** Dit rapport is een leeg malplaatje dat u kunt gebruiken om uw eigen douanerapport tot stand te brengen gebruikend de meeste dimensies en metriek. Rapporten [!UICONTROL Conversion] , [!UICONTROL Device] , [!UICONTROL Geo] en [!UICONTROL Site] zijn variaties van deze sjabloon met vooraf geselecteerde kolommen en dimensies voor hun respectievelijke gebruiksgevallen.

* Vooraf geconfigureerde rapportsjablonen

   * **[!UICONTROL Billing]:** gebruik dit rapport om zeer belangrijke het factureren metriek zoals uitgavenmetriek voor media het factureren door campagne te begrijpen. Gegevens zijn niet beschikbaar voor plaatsen die universele id&#39;s als doel hebben.

     >[!NOTE]
     >
     >Dit rapport bevat gegevens over het factureringssegment. Als een gebruiker of een apparaat een indruk krijgt die tot veelvoudige segmenten behoort, slechts wordt één factureerbare segment met de indruk gecrediteerd.

   * **[!UICONTROL Conversion]:** gebruik dit rapport om te begrijpen hoe uw campagnes worden uitgevoerd op basis van conversiemetriek die is vastgelegd met het bijhouden van Adoben Advertising conversie. Dit rapport bevat multi-touchattributie.

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

   * **[!UICONTROL Geo]**: Gebruik deze vooraf ingevulde sjabloon om de belangrijkste metrics op geografische afmetingen weer te geven.

   * **[!UICONTROL Margin]:** gebruik dit rapport om belangrijke metrieken zoals marge, winst, en andere uitgavenmetriek door campagne of plaatsing te zien. Gegevens zijn niet beschikbaar voor plaatsen die universele id&#39;s als doel hebben.

   * **[!UICONTROL Segment]:** Gebruik deze vooraf ingevulde sjabloon om de belangrijkste metrics per segment te zien.

     >[!NOTE]
     >
     >* Dit rapport is bedoeld om te laten zien hoe de verschillende doelsegmenten presteren. Er worden segmentlidmaatschapsgegevens gebruikt. Wanneer een persoon of apparaat die tot twee of meer doelsegmenten behoort, de indruk krijgt dat dit rapport één rij voor elk segment bevat. Daarom komen de totalen in dit rapport mogelijk niet overeen met de werkelijke levering.
     >* De metriek van de omzetting en de gegevens van het douanedoel voor segmenten zijn beschikbaar na 2 augustus 2019. Alle andere gegevens voor segmenten zijn beschikbaar vanaf 1 juni 2018.

   * **[!UICONTROL Site]:** Standaard bevat dit standaardcijfers, de totale netto media-uitgaven en de totale factureerbare netto-uitgaven per site.

   * **[!UICONTROL Household Reach & Frequency]:** gebruik dit rapport om de impressies, het bereik en de frequentie voor een enkele dimensie in verschillende advertentieformaten op huishoudniveau te bekijken op basis van IP-adres, in plaats van op apparaat-/cookieniveau. Gebruik de inzichten om je mediacomix te optimaliseren, de prestaties te verbeteren en mogelijkheden voor incrementeel bereik te identificeren. Zie &quot;[ Veelgestelde vragen over de Rapporten van het Huishouden ](/help/dsp/reports/faq-reports.md)&quot;voor meer informatie. Gegevens zijn niet beschikbaar voor plaatsen die universele id&#39;s als doel hebben.

   * **[!UICONTROL Household Conversions]:** gebruik dit rapport om mening-door omzettingen op het niveau van het huishouden te zien die op IP adres, eerder dan op een apparaat/koekjesniveau wordt gebaseerd. Gebruik de inzichten om campagneprestaties te meten en te optimaliseren. Zie &quot;[ FAQs over de Rapporten van de Huishouden ](/help/dsp/reports/faq-reports.md)&quot;voor meer informatie. Gegevens zijn niet beschikbaar voor plaatsen die universele id&#39;s als doel hebben.

   * **[!UICONTROL Path to Conversion Beta]:** (de eigenschap van Beta) gebruik dit rapport om te identificeren hoe te om begrotingen te optimaliseren en advertenties te personaliseren die op top-presterende en interactiereeksen worden gebaseerd. Het rapport bevat de reeks interactiepunten in hetzelfde huishouden die leiden tot elk van de geselecteerde conversiemetriek in het opgegeven gegevensbereik. Het rapport gebruikt een gespecificeerde raadplegingsperiode tussen de eerste interactie en een omzetting en kan één dimensie omvatten:

      * [!UICONTROL Channel Assist Type]: laat zien hoe de volgende marketingkanalen het conversieproces hebben geholpen: [!UICONTROL Audio Impression] , [!UICONTROL CTV Impression] , [!UICONTROL Display Click] , [!UICONTROL Display Impression] , [!UICONTROL Native Click] , [!UICONTROL Native Impression] , [!UICONTROL Search Click] , [!UICONTROL Video Click] of [!UICONTROL Video Impression] .

      * [!UICONTROL Campaign ID] of [!UICONTROL Campaign Name]: Toont welke campagnes het conversieproces hebben ondersteund.

      * [!UICONTROL Ad ID] of [!UICONTROL Ad Name] toont welke DSP advertenties tot conversies hebben geleid.

      * [!UICONTROL Ad ID & Paid Keyword (SSC)] of [!UICONTROL Ad Name & Paid Keyword (SSC)] toont welke trefwoorden voor Zoeken, Sociaal zoeken en Commerce hebben geresulteerd in conversies.

     De kolommen in het rapport omvatten &quot;[!UICONTROL Event #1]&quot; door &quot;[!UICONTROL Event #10],&quot;&quot;[!UICONTROL Path Length], &quot;% \&lt;Conversion Metric Name 1\>,&quot;% \&lt;Conversion Metric Name 2\>,&quot;etc.

     Tot de 10 meest recente interactiepunten zijn opgenomen. De padrijen worden gerangschikt op basis van het aantal conversies.

   * **[!UICONTROL Path Length Beta]:** (de eigenschap van Beta) gebruik dit rapport om ad frequentie te beheren die op het aantal gebruikers interactiepunten wordt gebaseerd die voor omzettingen wordt vereist. Het rapport toont het aantal omzettingen door weglengte (interactiepunten), zoals hoeveel omzettingen voorkwamen nadat de gebruikers slechts één ad interactie, twee en interactie, etc. hadden. Het rapport kan gegevens voor veelvoudige omzettingsmetriek omvatten en gebruikt een gespecificeerde raadplegingsperiode tussen de eerste interactie en een omzetting. De kolommen in het rapport omvatten &quot;[!UICONTROL Path Length],&quot; &quot;[!UICONTROL Number of] \&lt;Conversion Metric Name 1\>,&quot; &quot;% \&lt;Conversion Metric Name 1\>,&quot; \&lt;Conversion Metric Name 2\>, &quot;% \&lt;Conversion Metric Name 2\>,&quot; etc.

     Er worden gegevens weergegeven voor elke padlengte van maximaal 10 en gegevens voor padlengten groter dan 10 worden gegroepeerd.

   * **[!UICONTROL Time to Conversion Beta]:** (Beta eigenschap) Gebruik dit rapport om het optimale venster van de attributieraadpleging te bepalen en nieuwe kansen voor retargeting te identificeren. Het rapport toont het aantal conversies op basis van de tijdsduur in dagen vanaf de laatste interactie (advertentie-belichting of klik) tot de conversie. Het rapport kan gegevens bevatten voor meerdere conversiemetrieken en gebruikt een opgegeven terugzoekperiode tussen de eerste interactie en een conversie. De kolommen in het rapport omvatten &quot;[!UICONTROL Time Taken (in days)],&quot; &quot;[!UICONTROL Number of] \&lt;Conversion Metric Name 1\>,&quot; &quot;% \&lt;Conversion Metric Name 1\>,&quot; \&lt;Conversion Metric Name 2\>, &quot;% \&lt;Conversion Metric Name 2\>,&quot; etc. De omzettingen die langer duren dan de raadplegingsperiode worden gegroepeerd in één rij (bijvoorbeeld, als het rapport een periode van de 30 dagraadpleging gebruikt, dan worden alle omzettingen die langer duren dan 30 dagen om voor te komen gegroepeerd in een rij met een &quot;[!UICONTROL Time Taken (in days)]&quot;waarde van &quot;30+&quot;).

## Rapportage tussen accounts {#cross-account-reporting}

Om het even welke organisatie met veelvoudige DSP rekeningen kan naar keuze dwars-rekeningsgegevens in douanerapporten toelaten, volgens de behoeften van de organisatie. U kunt bijvoorbeeld Account A toegang geven tot de gegevens van Account B en Account B toegang geven tot de gegevens van Account C (maar niet van Account A). Neem contact op met het accountteam van de Adobe om deze functie in te schakelen en te configureren.

Zodra de eigenschap voor uw organisatie wordt toegelaten, kunt u [ ](report-settings.md) om het even welke volgende rapporttypes door rekening filtreren: [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], en [!UICONTROL Conversion].

Uw accountinstellingen op [!UICONTROL Settings] > [!UICONTROL Account] geven a) de andere accounts waarvan de gegevens beschikbaar zijn voor uw account en b) de andere accounts die toegang hebben tot de gegevens van uw account.

## De [!UICONTROL Custom Reports] -weergave

[!UICONTROL Reports] > [!UICONTROL Custom Reports] geeft een overzicht van uw bestaande rapporten, inclusief gegenereerde rapporten, rapporten die zijn gepland voor toekomstige generatie en rapporten die zijn mislukt. De kolom &quot;[!UICONTROL Report Run]&quot;toont data waarop het rapport werd teweeggebracht die op 22 augustus 2024 begonnen. Standaard worden alle niet-gearchiveerde rapporten die door de gebruiker zijn gemaakt, weergegeven met de meest recente bovenaan. U kunt de lijst door status verder filtreren, of het rapport terugkomt of eenmalig, het rapporttype, het bestemmingstype, en de rapportschepper is.

U kunt nieuwe douanerapporten tot stand brengen, bestaande rapporten uitgeven of hen dupliceren om nieuwe rapporten tot stand te brengen, rapporten onmiddellijk in werking te stellen, om het even welke rapportinstantie van de laatste vier maanden te downloaden, en rapporten te schrappen.

## Statussen rapporteren {#custom-report-status}

* **[!UICONTROL Yet to start]:** Het rapport is nooit uitgevoerd.

* **[!UICONTROL Report generating]:** Het rapport wordt momenteel gemaakt.

* **[!UICONTROL Ready to download]:** (Terugkerende rapporten slechts) één of meerdere instanties van het rapport is beschikbaar om te downloaden, en meer rapportinstanties zijn gepland.

* **[!UICONTROL Failed]:** De rapporttaak is mislukt. Om te zien waarom de individuele rapportinstanties voor een rapportduw ontbroken, klik ![ de benedenpijl ](/help/dsp/assets/chevron-down.png " pijl ") naast [!UICONTROL Download]. Mislukte rapporttaken zijn vermeld met een foutenpictogram (![foutindicator](/help/dsp/assets/indicator-critical.png "foutindicator")). Plaats de cursor op het foutpictogram voor een beschrijving van de fout.

* **[!UICONTROL Completed]:** Voor niet-terugkerende rapporten, wordt het rapport voltooid. Voor terugkerende rapporten, worden alle rapportinstanties voltooid. U kunt alle rapporten downloaden die in de laatste vier maanden zijn voltooid.

* **[!UICONTROL Archived]:** het rapport is gearchiveerd en kan niet in werking worden gesteld. Deze status wordt geplaatst wanneer de rapportgeneratie veelvoudige tijden voor een rapport ontbreekt. U kunt deze status momenteel niet instellen vanuit de gebruikersinterface.

>[!MORELIKETHIS]
>
>* [ creeer een Rapport van de Douane ](/help/dsp/reports/report-create.md)
>* [ Download een Rapport van de Douane ](/help/dsp/reports/report-download.md)
>* [ de Montages van het Rapport van de Douane ](/help/dsp/reports/report-settings.md)
>* [ Veelgestelde vragen over de Rapporten van de Huishouden ](/help/dsp/reports/faq-reports.md)
>* [ Types van Rapporten van Prestaties in de Meningen van Campaign Management ](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [ Beschikbare Kolommen van het Rapport ](/help/dsp/reports/report-columns.md)
>* [ Over [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
