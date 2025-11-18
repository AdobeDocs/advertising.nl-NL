---
title: '[!UICONTROL Manage custom reports]'
description: Leer hoe u de kruiservaring genereert [!UICONTROL Custom Creative Report] .
feature: Creative Reporting
source-git-commit: 5b644fb2eb881b8180932bb9449dd303a70d9647
workflow-type: tm+mt
source-wordcount: '1461'
ht-degree: 0%

---

# [!UICONTROL Manage custom reports]





## Een aangepast rapport maken {#report-create}

1. Klik in het hoofdmenu op **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** .

1. Klik in de rechterbovenhoek op **[!UICONTROL Create]** .

1. Specificeer de [&#x200B; rapportmontages &#x200B;](#report-settings).

1. Klik op **[!UICONTROL Create Custom Report]**.

## Een aangepast rapport dupliceren

Dupliceer een douanerapport om een nieuw rapport met gelijkaardige montages tot stand te brengen.

1. Klik in het hoofdmenu op **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** .

1. Klik naast de rapportnaam op **[!UICONTROL ...]** > **[!UICONTROL Copy]** .

1. (Facultatief) geef de [&#x200B; rapportmontages &#x200B;](#report-settings.md) uit zoals nodig.

   De rapportnaam, door gebrek, is &quot;\&lt; *bestaande rapportnaam* \> \#2&quot;(of het volgende aantal in de opeenvolging).

## Een aangepast rapport bewerken {#report-edit}

1. Klik in het hoofdmenu op **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** .

1. Klik naast de rapportnaam op **[!UICONTROL ...]** > **[!UICONTROL Edit]** .

1. Bewerk de [&#x200B; rapportmontages &#x200B;](#report-settings.md).

1. Klik op **[!UICONTROL Edit Custom Report]**.

## Een aangepast rapport verwijderen

1. Klik in het hoofdmenu op **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** .

1. Klik naast de rapportnaam op **[!UICONTROL ...]** > **[!UICONTROL Delete]** .

1. Klik in het bevestigingsbericht op **[!UICONTROL Delete]** .

## Een aangepast rapport uitvoeren &lbrace;report-run-now&rbrace;

U kunt elk rapport uitvoeren dat nog niet is verlopen en momenteel niet wordt uitgevoerd.

>[!NOTE]
>
>U kunt een douanerapport ook in werking stellen wanneer u [&#x200B; &#x200B;](#report-create) creeert of [&#x200B; &#x200B;](#report-edit) het uitgeeft.

1. Klik in het hoofdmenu op **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** .

1. Klik naast de rapportnaam op **[!UICONTROL ...]** > **[!UICONTROL Run Now]** .

   Wanneer het rapport wordt voltooid, wordt het verzonden naar de bestemmingen die in de rapportmontages worden gespecificeerd.

## Een aangepast rapport downloaden

U kunt om het even welke voltooide rapportinstantie van de laatste vier maanden downloaden, die met de status &quot;[!UICONTROL Ready to Download]&quot;of &quot;[!UICONTROL Completed]&quot;heeft.

1. Klik in het hoofdmenu op **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]** .

1. Ga als volgt te werk in de kolom [!UICONTROL Download Report] voor de rapportrij:

   * Klik op **[!UICONTROL Download]** om de meest recente versie van het rapport te downloaden.

   * (Rapporten met veelvoudige instanties) klik ![&#x200B; de benedenpijl &#x200B;](/help/dsp/assets/chevron-down.png " de benedenpijl ") naast [!UICONTROL Download], en klik dan de voltooiingsdatum voor het rapport u wilt downloaden. Downloadbare rapportinstanties worden aangeduid met een downloadpictogram (![downloadpictogram](/help/dsp/assets/indicator-downloadable.png "downloadpictogram")).

     Wanneer er veel exemplaren beschikbaar zijn, klikt u indien nodig op **[!UICONTROL Load More]** onder aan de lijst.

     Wanneer een rapport veelvoudige tijden op de zelfde dag in werking stelt, zijn de rapportinstanties voor die dag vermeld in chronologische orde, met de meest recente instantie bovenop.

     De ontbroken rapportbanen worden vermeld met een foutenpictogram (![&#x200B; foutenindicator &#x200B;](/help/dsp/assets/indicator-critical.png " foutenindicator ")) en kunnen niet worden gedownload. Plaats de cursor op het foutpictogram voor een beschrijving van de fout.

## Rapportinstellingen {#report-settings}

**[!UICONTROL Name]:** De rapportnaam. De maximumlengte is 180 tekens.

**[!UICONTROL Report Type]:** Het type van rapport.

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
  >U kunt ook [&#x200B; een douanerapport op elk ogenblik &#x200B;](#report-run-now) van de [!UICONTROL Reports] mening in werking stellen.

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

**[!UICONTROL Select To Add As Report Headers]:** de gegevenskolommen, of kopballen, om in het rapport te omvatten. Als u een kolom wilt toevoegen, vouwt u de categorie uit en schakelt u het selectievakje naast de kolomnaam in. De beschikbare kolommen variëren door rapport, en alle niet beschikbare metriek zijn gehandicapt.<!-- Add back once I have this completed, and reconsider wording of link/anchor:  See "[Available Report Columns](#report-custom-creative-columns)" for descriptions of all options. -->

**[!UICONTROL Drag to Re-Order Report Headers Below]:** de orde van de kolomkopballen. U kunt elke kolom slepen en neerzetten om de volgorde aan te passen.

**[!UICONTROL Format]:** Of een rapport moet worden gegenereerd in de indeling *[!UICONTROL CSV]* (door komma&#39;s gescheiden waarden) of *[!UICONTROL Tab]* (door tabs gescheiden waarden).

**[!UICONTROL Headers]:** Of *[!UICONTROL Include]* of *[!UICONTROL Do Not Include]* kolomkoppen.

### [!UICONTROL Multi-Touch Conversion Options] Sectie

**[!UICONTROL Attribution Rule Settings]:** de montages variëren door rapporttype:

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

Zie ook &quot;[&#x200B; hoe de Regels van de Attributie voor Adobe Advertising &#x200B;](/help/search-social-commerce/reports/attribution-rules.md) worden berekend.&quot;

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

* *[!UICONTROL FTP SSL] (Momenteel in Beta):* Als u het voltooide rapport wilt verzenden naar een of meer FTP SSL-locaties, moet u deze selecteren in het veld **[!UICONTROL Destination Name]** .

* *[!UICONTROL Email]:* Om e-mailadres(sen) op te geven waarnaar voltooide rapporten of meldingen moeten worden verzonden als het rapport door fouten wordt geannuleerd.

**[!UICONTROL Email]:** (E-mail bestemmingstype slechts) voor elk adres, ga het adres in en klik **+**.

**[!UICONTROL Destination Name]:** (S3, FTP, sFTP, en de bestemmingstypes van FTP SSL slechts) De namen van de [&#x200B; rapportbestemmingen &#x200B;](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} waarnaar het douanerapport wordt verzonden.

* Selecteer een doelnaam in de lijst om een bestaand doel op te geven. U kunt meerdere doelnamen afzonderlijk selecteren.

* Een nieuw doel maken:

   1. Klik **toevoegen Nieuwe Bestemming**.

   1. Ga de [&#x200B; montages van de rapportbestemming &#x200B;](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"} in, en klik **sparen**.

   1. Terug in de rapportmontages, klik **verfrissen de Namen van de Bestemming.**

      De nieuwe bestemming is nu beschikbaar van de lijst van bestaande bestemmingen, en u kunt naar keuze het aan het rapport toevoegen.


<!-- This needs a lot of updating for new report:

## Available Report Columns {#report-custom-creative-columns}

|Metric Type|Subtype|Column Name|Description|
|-----------|-------|-----------|-----------|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Ad Size]|The dimensions of the published ad.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Is Default]|Whether the served ad was a default image ad or video ad for the experience.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Rotation Type]| Whether ads were rotated algorithmically (*Algorithmic*), in a specified sequence (*Sequenced*), or according to relative weights (*Weighted*).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative ID]| The ID that [!UICONTROL Creative] assigned to the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Name]| The name of the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Type]| The type of creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative ID]| The ID that [!UICONTROL Creative] assigned to the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Name]| The name of the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Type]| The type of parent creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Ad Link]| The landing page URL.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Click Type]| The specific type of user interaction.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Direction]| The directional flow or navigation path of the user's click interaction within the creative experience. |
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 1]| The value of Attribute 1 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 2]| The value of Attribute 2 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 3]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 4]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 5]| The value of Attribute 5 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Browser]|The browser in which the ad was shown (such as [!UICONTROL Chrome] or [!UICONTROL Firefox]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device OS]|The operating system on which the ad was shown (such as [!UICONTROL Windows]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Type]|The type of device on which the ad was shown (such as [!UICONTROL Desktop]).|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Name]| The name of the DSP on which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement ID]| The ID of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement Name]| The name of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site ID]| The ID of the site on which ads were run.|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site Name]| The name of the site on which ads were run. |
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Ad Tag Id]|The ID that [!UICONTROL Creative] assigned to the ad experience tag.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Advertiser Name]| The name of the advertiser.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Date/Time]|The date and time of the event.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience ID]| The ID that [!UICONTROL Creative] assigned to the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience Name]| The name of the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Targeting Branch Value]| The specific path through the targeting decision tree that determined which creative experience variant was served to the user.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Trafficking Line]| The name of the ad tag. |
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL City]|The city to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Country Code]|The country code for the country to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL DMA]|The Designated Market Area (DMA) to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL State Code]|The state code for the state to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Zip Code]|The zip code to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category ID]|(Dynamic ads) The target product category ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category Name]|(Dynamic ads) The target product category name.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 1]|(Dynamic ads) The first creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 2]|(Dynamic ads) The second creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 3]|(Dynamic ads) The third creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 4]|(Dynamic ads) The fourth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 5]|(Dynamic ads) The fifth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product ID]|(Dynamic ads) The target product ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product Name]|(Dynamic ads) The target product name.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Matched Audience Segment ID]|The IDs for up to five user segments that matched the ad theme.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment ID]|The ID for a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment Name]|The name of a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Segment Values]|The attributes for an audience segment to which the reported data is attributed.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Clicks]|The sum of all clicks on an ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL CTR]|The click-through rate, which is the percentage of clicks divided by ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagement Rate]|The percentage of impressions served that resulted in user engagements.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagements]|The number of interactions on a served ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Impressions]|The total number of ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Media Match Rate]| The percentage of impressions with a retargeted cookie. |
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Clicks]|(Dynamic ads only) The sum of all clicks on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion]|(Dynamic ads only) The sum of all conversions on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion Rate]|(Dynamic ads only) The percentage of ads for a product that resulted in conversions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product CTR]|(Dynamic ads only) The click-through rate for ads for a product, which is the percentage of clicks divided by ad impressions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Impressions]|(Dynamic ads only) The total number of impressions for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Revenue]|(Dynamic ads only) The total revenue on served ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Revenue]|The total revenue on served ads.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completion Rate]|The percentage of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completion Rate]|The percentage of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completion Rate]|The percentage of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completion Rate]|The percentage of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completions]|The number of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completions]|The number of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completions]|The number of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completions]|The number of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Avg Percent Viewed]|The average percentage an ad was watched to completion, accounting for all views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Play Rate]|The percentage of impressions served that resulted in video views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Playtime per View]|The average duration of a video view, measured in seconds.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Viewed Minutes]|The total number of minutes a video ad was viewed.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Views]|The total number of video ad views.




|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 100% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 50% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewability Rate (%)]|The percentage of viewable impressions out of all measurable impressions, calculated as <code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>.|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewable Impressions]|The number of ad impressions considered viewable.|
|[!UICONTROL Conversion Metrics]|[Grouped by advertiser in report settings]|[Advertiser-specific conversion]| The total for a specified advertiser-specific conversion metric or Adobe Analytics event.|
|[!UICONTROL Custom Goals]|[Grouped by advertiser in report settings]|[Advertiser-specific custom goal]|(Advertisers with Advertising DSP) The weighted sum of all conversions that are included in the specified [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).|

{style="table-layout:auto"}

-->

>[!MORELIKETHIS]
>
>* [&#x200B; ervaring-vlakke prestatiesrapporten &#x200B;](/help/creative/experiences/experience-performance-details.md)
>* [&#x200B; Ongeveer DSP douanerapporten &#x200B;](/help/dsp/reports/report-about.md){target="_blank"}
>* [&#x200B; Over [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
