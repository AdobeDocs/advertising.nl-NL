---
title: '[!UICONTROL Custom Creative Report]'
description: Leer hoe u de kruiservaring genereert [!UICONTROL Custom Creative Report] .
feature: Creative Reporting
exl-id: 13687d9d-6283-40ac-86a2-bb88b9fdfcc3
source-git-commit: a271589a2cb51ec50c37a52254fd8d1b535f279a
workflow-type: tm+mt
source-wordcount: '2026'
ht-degree: 0%

---

# [!UICONTROL Custom Creative Report]

*eigenschap van Beta*

Met [!UICONTROL Custom Creative Report] kunt u de inhoud en levering van rapportgegevens aanpassen voor al uw advertentieervaringen.

U kunt rapporten eenmaal produceren, of u kunt hen dagelijks, wekelijks, of maandelijks bij 03 :00 in de gespecificeerde tijdzone volgens gespecificeerde criteria (zoals om de 15 dagen of op de 1e van elke maand) plannen. Zodra een rapport wordt geproduceerd, kunt u het van [!UICONTROL Reports] > [!UICONTROL Custom Reports] of van verbonden [ rapportbestemmingen ](/help/dsp/reports/report-destinations/report-destination-about.md) van de volgende types downloaden:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

## Een [!UICONTROL Custom Creative Report] maken

1. Klik in het hoofdmenu op **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** .

1. Klik in de rechterbovenhoek op **[!UICONTROL Create]** .

1. Specificeer de [ rapportmontages ](#report-settings).

1. Klik op **[!UICONTROL Create Custom Report]**.

## Rapportinstellingen {#report-settings}

**[!UICONTROL Name]:** De rapportnaam. De maximumlengte is 180 tekens.

**[!UICONTROL Report Type]:** Het type rapport: *[!UICONTROL Custom Creative Beta]*.

### [!UICONTROL Report Range] Sectie

Deze sectie bepaalt de gegevens die in het rapport inbegrepen zijn. Aan opstellingsdata voor het rapportprogramma, zie &quot;[!UICONTROL Report run schedule]&quot;sectie.

**[!UICONTROL Timezone]:** De tijdzone voor het melden.

**[!UICONTROL Observe Daylight Savings Time]:** beschouwt zomertijd in de gemelde tijden.

**Waaier:** de datumwaaier waarvoor om gegevens te produceren. Het aantal beschikbare dagen varieert per rapport en per geselecteerde afmeting. Kies een optie:

* **[!UICONTROL Previous Calendar Week]:** Bevat gegevens voor de vorige kalenderweek.

* **[!UICONTROL Previous Calendar Month]:** Bevat gegevens voor de vorige kalendermaand.

* **[!UICONTROL Custom Range]:** omvat gegevens tussen specifieke begin en einddata. Selecteer **[!UICONTROL Present]** als u gegevens tot en met de vorige dag wilt rapporteren.

### [!UICONTROL Report Run schedule] Sectie

Deze sectie bepaalt de data waarop het rapport in werking wordt gesteld. Aan opstelling de data waarvoor om rapportgegevens te omvatten, zie &quot;[!UICONTROL Report range]&quot;sectie.

**\[Schedule\]:** Wanneer genereert u het rapport:

* *[!UICONTROL Immediately]*: voegt het rapport onmiddellijk toe aan de rapportwachtrij.

  >[!NOTE]
  >
  >U kunt ook [ een douanerapport op elk ogenblik ](/help/dsp/reports/report-run-now.md) van de [!UICONTROL Reports] mening in werking stellen.

* *[!UICONTROL On]\&lt;Date\>:* stelt het rapport op een gespecificeerde datum voor voltooiing door 09 :00 in de tijdzone van de rekening in werking.

* *[!UICONTROL Recurring]:* stelt het rapport volgens een programma tijdens een gespecificeerde tijdspanne in werking.

   * **\[Schedule\]:** Hoe vaak het rapport moet worden uitgevoerd:

      * *Dagelijks* om het rapport om het aantal dagen in werking te stellen N. Bijvoorbeeld, om het rapport om de twee weken (14 dagen) in werking te stellen, selecteer deze optie en ga **14** in.

      * *wekelijks* om het rapport op gespecificeerde dagen van de week in werking te stellen. Bijvoorbeeld, om het rapport elke Maandag en Vrijdag in werking te stellen, selecteer deze optie en selecteer de controledozen naast **Maandag** en **Vrijdag**.

      * *Maandelijks* om het rapport op een specifieke numerieke dag van de maand, van 1 tot 30 in werking te stellen. Bijvoorbeeld, stel het rapport op de eerste dag van elke maand in werking, selecteer deze optie en ga **1** in.

   * **van**: De eerste datum waarop het rapport kan worden in werking gesteld. Afhankelijk van het gespecificeerde programma, kan de eerste rapportinstantie na deze datum voorkomen.

   * **tot**: De datum van de rapportvervaldatum, die tot vier kalendermaanden weg kan zijn. Voordat een rapport verloopt, ontvangen alle opgegeven e-maildoelen zeven dagen en één dag vóór de vervaldatum een e-mailwaarschuwing. Wijzig deze datum om het rapport langer te houden.

### [!UICONTROL Apply Filters] Sectie

**[!UICONTROL Filter by]:** (Facultatieve) Extra afmetingen waardoor om de gegevens te filtreren, al dan niet de afmetingen als kolommen in het rapport inbegrepen zijn. De beschikbare filters verschillen per rapporttype en kunnen de volgende zijn: *[!UICONTROL Advertiser]* , *[!UICONTROL Experience]* , *[!UICONTROL Creative Library]* en *[!UICONTROL DSP]*<!-- Clarify what this is for, Advertising DSP or whatever DSP the ads were run from? -->.

Ga als volgt te werk om een of meer filters toe te passen:

* Selecteer een afmeting, selecteer de exploitant (*evenaart* of *niet evenaart*), en selecteer dan de toepasselijke waarde. Bijvoorbeeld, om gegevens voor slechts preroll advertenties terug te keren, specificeer &quot;[!UICONTROL Ad Type equals Preroll]&quot;.
* (Optioneel) Voeg aanvullende criteria toe aan het filter.
* (Optioneel) Voeg aanvullende filters toe, elk met een of meer criteria.

### [!UICONTROL Build Your Report] Sectie

**[!UICONTROL Select To Add As Report Headers]:** de gegevenskolommen, of kopballen, om in het rapport te omvatten. Als u een kolom wilt toevoegen, vouwt u de categorie uit en schakelt u het selectievakje naast de kolomnaam in. De beschikbare kolommen variëren per rapport en alle niet-beschikbare metriek zijn uitgeschakeld. Zie &quot;[ Beschikbare Kolommen van het Rapport ](#report-custom-creative-columns)&quot;voor beschrijvingen van alle opties.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** de orde van de kolomkopballen. U kunt elke kolom slepen en neerzetten om de volgorde aan te passen.

**[!UICONTROL Format]:** Of een rapport moet worden gegenereerd in de indeling *[!UICONTROL CSV]* (door komma&#39;s gescheiden waarden) of *[!UICONTROL Tab]* (door tabs gescheiden waarden).

**[!UICONTROL Headers]:** Of *[!UICONTROL Include]* of *[!UICONTROL Do Not Include]* kolomkoppen.

### [!UICONTROL Multi-Touch Conversion Options] Sectie

**[!UICONTROL Attribution Rule Settings]:** de montages variëren door rapporttype:

* **\[Type kenmerk\]:** (Advertisers met alleen het bijhouden van Adobe Advertising-conversies) In het rapport leert u hoe u conversiegegevens kunt toewijzen in een reeks gebeurtenissen die tot conversie leiden:

   * *[!UICONTROL Unique]:* (het gebrek) telt het aantal tijden een afmetingswaarde (zoals een apparaat of plaatsing) op de weg aan omzetting was.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* verdeelt het krediet van elke omzetting die op de frequentie van voorkomen van de afmetingswaarde (zoals een apparaat of plaatsing) op de weg aan omzetting wordt gebaseerd. Als er bijvoorbeeld in totaal 10 indrukken waren vóór de conversie, met 8 op CTV en 2 op Mobile, wordt 80% van het krediet (0,8) aan CTV-schermen en 0,2 aan Mobiel gegeven.

* **\[Type regel\]:** (Adverteerders met alleen het bijhouden van Adobe Advertising-conversies) In het rapport leert u hoe u conversiegegevens kunt toewijzen in een reeks gebeurtenissen die tot conversie leiden. U kunt meer dan één regel kiezen als u de verschillen tussen de regels wilt vergelijken.

  >[!NOTE]
  >
  >Conversiepaden bevatten alle indrukken en klikken binnen de indruk van de adverteerder of klik op terugkijkvensters, die zijn geconfigureerd in [!DNL Advertising Search, Social, & Commerce] . Klikken krijgen de voorkeur boven indrukken tijdens conversie-toewijzing. Om het even welke kliks in een omzettingsweg ontvangen volledige kredieten die op de attributieregel worden gebaseerd. Impressies krijgen alleen krediet als er geen klikken worden bijgehouden in het conversiepad.

   * *[!UICONTROL Last Event]:* Kenmerken conversies naar de laatste klik of indruk in het conversiepad.

   * *[!UICONTROL Weight Last More]:* kenmerkt omzettingen aan alle gebeurtenissen in de omzettingsweg maar geeft het meeste gewicht aan de laatste gebeurtenis en opeenvolgend minder gewicht aan de voorafgaande gebeurtenissen.

   * *[!UICONTROL Even Distribution]:* kenmerken conversies in gelijke mate naar elke gebeurtenis in het conversiepad.

   * *[!UICONTROL Weight First More]:* kenmerkt omzettingen aan alle gebeurtenissen in de omzettingsweg maar geeft het meeste gewicht aan de eerste gebeurtenis en opeenvolgend minder gewicht aan de volgende gebeurtenissen.

   * *[!UICONTROL First Event]:* Kenmerken conversies naar de eerste klik of indruk in het conversiepad.

   * *[!UICONTROL U-shaped]:* kenmerkt de omzetting aan alle gebeurtenissen in de omzettingsweg maar geeft het meeste gewicht aan de eerste en laatste gebeurtenissen, met opeenvolgend minder gewicht aan de gebeurtenissen in het midden van de omzettingsweg.

   * *[!UICONTROL Display Only]:* Kenmerken conversies naar de laatste DSP-klik of -indruk in het conversiepad. Dit omvat video- en aangesloten tv-advertenties en sluit kliks op [!DNL Advertising Search, Social, & Commerce] -advertenties uit.

   * *[!UICONTROL Social Only]:* Verouderd

Zie ook &quot;[ hoe de Regels van de Attributie voor Adobe Advertising ](/help/search-social-commerce/reports/attribution-rules.md) worden berekend.&quot;

**[!UICONTROL Paths as Columns]:** welke soorten omzettingen om te melden wanneer de vroegere gebeurtenissen op het zelfde apparaat voorkwamen. U kunt maximaal drie typen opnemen. Voor elk geselecteerd type wordt een aparte kolom opgenomen voor elke omzettingsmetrische waarde en toegevoegd met het opgegeven achtervoegsel ([!UICONTROL (tl)], [!UICONTROL (ct)] of [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* omvat omzettingen die aan kliks (CT voor klik-door) en aan impressies (VT voor mening-door) worden toegewezen. Conversies die worden toegewezen aan impressies worden vermenigvuldigd met het opgegeven doorkijkgewicht. Het standaardgezichtsdoorsgewicht is 100%, wat betekent dat omzettingen die aan indrukkingen worden toegeschreven, worden geteld als 100% van de waarde van omzettingen die aan kliks worden toegeschreven.

* *[!UICONTROL With Clicks (CT)]:* omvat slechts omzettingen die aan kliks worden toegewezen.

* *[!UICONTROL Impressions Only (VT)]:* Omvat slechts omzettingen die aan impressies werden toegeschreven omdat geen kliks in de omzettingsweg werden gevolgd.

### [!UICONTROL Add Report Destinations] Sectie

**[!UICONTROL Destination Type]:** waar de voltooide rapporten en foutmeldingen moeten worden geleverd. U kunt niet het bestemmingstype veranderen zodra u het rapport opslaat.

>[!NOTE]
>
>U kunt voltooide rapporten altijd downloaden vanuit de weergave [!UICONTROL Reports] > [!UICONTROL Custom Reports] .

* *[!UICONTROL None]:* om geen rapporten of berichten te leveren.

* *[!UICONTROL S3]:* om het voltooide rapport naar één of meerdere [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) plaatsen te verzenden, die u op het **[!UICONTROL Destination Name]** gebied moet selecteren.

* *[!UICONTROL sFTP]:* om het voltooide rapport naar één of meerdere plaatsen te verzenden SFTP, die u op het **[!UICONTROL Destination Name]** gebied moet selecteren.

* *[!UICONTROL FTP]:* om het voltooide rapport naar één of meerdere plaatsen van FTP te verzenden, die u op het **[!UICONTROL Destination Name]** gebied moet selecteren.

* *[!UICONTROL FTP SSL](Momenteel in Beta):* Als u het voltooide rapport wilt verzenden naar een of meer FTP SSL-locaties, moet u deze selecteren in het veld **[!UICONTROL Destination Name]** .

* *[!UICONTROL Email]:* Om e-mailadres(sen) op te geven waarnaar voltooide rapporten of meldingen moeten worden verzonden als het rapport door fouten wordt geannuleerd.

**[!UICONTROL Email]:** (E-mail bestemmingstype slechts) voor elk adres, ga het adres in en klik **+**.

**[!UICONTROL Destination Name]:** (S3, FTP, sFTP, en de bestemmingstypes van FTP SSL slechts) De namen van de [ rapportbestemmingen ](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} waarnaar het douanerapport wordt verzonden.

* Selecteer een doelnaam in de lijst om een bestaand doel op te geven. U kunt meerdere doelnamen afzonderlijk selecteren.

* Een nieuw doel maken:

   1. Klik **toevoegen Nieuwe Bestemming**.

   1. Ga de [ montages van de rapportbestemming ](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"} in, en klik **sparen**.

   1. Terug in de rapportmontages, klik **verfrissen de Namen van de Bestemming.**

      De nieuwe bestemming is nu beschikbaar van de lijst van bestaande bestemmingen, en u kunt naar keuze het aan het rapport toevoegen.

## Beschikbare rapportkolommen {#report-custom-creative-columns}

| Metrisch type | Subtype | Kolomnaam | Beschrijving |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Size] | De afmetingen van de gepubliceerde advertentie. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Is Default] | Geeft aan of de geleverde advertentie een standaardafbeeldings- of videoadvertentie was voor de beleving. |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Rotation Type] | Of de advertenties algoritmisch werden geroteerd (*Algorithmic*), in een gespecificeerde opeenvolging (*Opeengeschakeld*), of volgens relatieve gewichten (*Gewogen*). |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative ID] | De id die [!UICONTROL Creative] aan de creatieve persoon heeft toegewezen. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Name] | De naam van de creatieve. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Creative Type] | Het type creatief (zoals [!UICONTROL HTML5]). |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative ID] | De id die [!UICONTROL Creative] heeft toegewezen aan de bovenliggende creatieve server. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Name] | De naam van de ouder creatief. |
| [!UICONTROL Dimension] | [!UICONTROL Creative] | [!UICONTROL Parent Creative Type] | Het type van bovenliggende creatieve elementen (zoals [!UICONTROL HTML5] ). |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Ad Link] | De bestemmingspagina-URL. |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Click Type] | Het specifieke type gebruikersinteractie. |
| [!UICONTROL Dimension] | [!UICONTROL Click Events] | [!UICONTROL Direction] | De richting of het navigatiepad van de klikinteractie van de gebruiker binnen de creatieve ervaring. |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Browser] | De browser waarin de advertentie is weergegeven (bijvoorbeeld [!UICONTROL Chrome] of [!UICONTROL Firefox] ). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device OS] | Het besturingssysteem waarop de advertentie is weergegeven (bijvoorbeeld [!UICONTROL Windows] ). |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Type] | Het type apparaat waarop de advertentie is weergegeven (bijvoorbeeld [!UICONTROL Desktop] ). |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Name] | De naam van de DSP waarop advertenties zijn uitgevoerd. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement ID] | De id van de plaatsing waarvoor advertenties zijn uitgevoerd. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Placement Name] | De naam van de plaatsing waarvoor advertenties zijn uitgevoerd. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site ID] | De id van de site waarop advertenties zijn uitgevoerd. |
| [!UICONTROL Dimension] | [!UICONTROL DSP] | [!UICONTROL DSP Site Name] | De naam van de site waarop advertenties zijn uitgevoerd. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Ad Tag Id] | De id die [!UICONTROL Creative] aan de advertentietag heeft toegewezen. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Advertiser Name] | De naam van de adverteerder. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Date/Time] | De datum en het tijdstip van de gebeurtenis. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience ID] | De id die [!UICONTROL Creative] aan de ervaring heeft toegewezen. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Experience Name] | De naam van de ervaring. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Targeting Branch Value] | De specifieke weg door de het richten beslissingsboom die bepaalde welke creatieve ervaringsvariant aan de gebruiker werd gediend. |
| [!UICONTROL Dimension] | [!UICONTROL Experiences] | [!UICONTROL Trafficking Line] | De naam van de advertentietag. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL City] | De stad waaraan de gerapporteerde gegevens worden toegeschreven. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Country Code] | De landcode voor het land waaraan de gerapporteerde gegevens zijn toegewezen. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL DMA] | Het aangewezen marktgebied (DMA) waaraan de gerapporteerde gegevens zijn toegewezen. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL State Code] | De statuscode voor de staat waaraan de gerapporteerde gegevens worden toegeschreven. |
| [!UICONTROL Dimension] | [!UICONTROL Geo] | [!UICONTROL Zip Code] | De postcode waaraan de gerapporteerde gegevens zijn toegewezen. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category ID] | (Dynamische advertenties) De doel-productcategorie-id. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Category Name] | (Dynamische advertenties) De naam van de doelproductcategorie. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 1] | (Dynamische advertenties) Het eerste creatieve kenmerk. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 2] | (Dynamische advertenties) Het tweede creatieve kenmerk. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 3] | (Dynamische advertenties) Het derde creatieve kenmerk. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 4] | (Dynamische advertenties) Het vierde creatieve kenmerk. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Creative Attribute 5] | (Dynamische advertenties) Het vijfde creatieve kenmerk. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product ID] | (Dynamische advertenties) De doel-product-id. |
| [!UICONTROL Dimension] | [!UICONTROL Product] | [!UICONTROL Product Name] | (Dynamische advertenties) De doelproductnaam. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Matched Audience Segment ID] | De id&#39;s voor maximaal vijf gebruikerssegmenten die overeenkomen met het advertentiethema. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment ID] | De id voor een doelpixel waaraan de gerapporteerde gegevens worden toegewezen. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Pixel Segment Name] | De naam van een herrichtingspixel waaraan de gerapporteerde gegevens zijn toegewezen. |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Values] | De kenmerken voor een publiekssegment waaraan de gerapporteerde gegevens worden toegewezen. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks] | De som van alle klikken op een advertentie. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL CTR] | De doorkliksnelheid. Dit is het percentage klikken gedeeld door indrukken. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagement Rate] | Het percentage indrukken dat tot gebruikersbetrokkenheid heeft geleid. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | Het aantal interacties op een betekende advertentie. |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | The total number of ad impressions. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Media Match Rate] | Het percentage van de indrukken met een opnieuw gericht cookie. |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Clicks] | (Alleen dynamische advertenties) De som van alle klikken op advertenties voor een product. Wanneer het product null is, is deze waarde nul (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion] | (Alleen dynamische advertenties) De som van alle conversies op advertenties voor een product. Wanneer het product null is, is deze waarde nul (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Conversion Rate] | (Alleen dynamische advertenties) Het percentage advertenties voor een product dat tot conversies heeft geleid. Wanneer het product null is, is deze waarde nul (0). |
| [!UICONTROL Metric] | [!UICONTROL Standard Metrics] | [!UICONTROL Product CTR] | (Alleen dynamische advertenties) De doorklikfrequentie voor advertenties voor een product. Dit is het percentage klikken gedeeld door advertenties. Wanneer het product null is, is deze waarde nul (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Impressions] | (Alleen dynamische advertenties) The total number of impressions for a product. Wanneer het product null is, is deze waarde nul (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Product Revenue] | (Alleen dynamische advertenties) De totale inkomsten aan bediende advertenties voor een product. Wanneer het product null is, is deze waarde nul (0). |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Revenue] | De totale inkomsten voor bediende reclame. |
| [!UICONTROL Conversion Metrics] | [ Gegroepeerd door adverteerder in rapportmontages ] | [ Advertiser-specifieke omzetting ] | Het totaal voor een opgegeven, voor adverteerders specifieke conversie-metrische of Adobe Analytics-gebeurtenis. |
| [!UICONTROL Custom Goals] | [ Gegroepeerd door adverteerder in rapportmontages ] | [ Advertiser-specifiek douanedoel ] | (Advertisers met Advertising DSP) de gewogen som alle omzettingen die in het gespecificeerde [ douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md) inbegrepen zijn. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [ ervaring-vlakke prestatiesrapporten ](/help/creative/experiences/experience-performance-details.md)
>* [ Ongeveer DSP douanerapporten ](/help/dsp/reports/report-about.md){target="_blank"}
>* [ Over [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
