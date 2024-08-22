---
title: Instellingen voor aangepaste rapporten
description: Zie beschrijvingen van de montages van het douanerapport.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 4fb843e66edddd4585d4a9b142eb9a7750152d27
workflow-type: tm+mt
source-wordcount: '1436'
ht-degree: 0%

---

# Instellingen voor aangepaste rapporten

**[!UICONTROL Name]:** De rapportnaam. De maximumlengte is 180 tekens.

**[!UICONTROL Report Type]:** Het type rapport: *[!UICONTROL Custom]* (met de meeste beschikbare opties), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*, *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*, *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]* of *[!UICONTROL Household Conversions]* .

## [!UICONTROL Report Range] Sectie

Deze sectie bepaalt de gegevens die in het rapport inbegrepen zijn. Aan opstellingsdata voor het rapportprogramma, zie &quot;[!UICONTROL Report run schedule]&quot;sectie.

**[!UICONTROL Timezone]:** De tijdzone voor het melden.

**[!UICONTROL Observe Daylight Savings Time]:** beschouwt zomertijd in de gemelde tijden.

**Waaier:** de datumwaaier waarvoor om gegevens te produceren. Het aantal beschikbare dagen varieert per rapport en per geselecteerde afmeting. Kies een optie:

* **[!UICONTROL Last Calendar Week]:** Bevat gegevens voor de vorige kalenderweek.

* **[!UICONTROL Last Calendar Month]:** Bevat gegevens voor de vorige kalendermaand.

* **[!UICONTROL Custom Range]:** omvat gegevens tussen specifieke begin en einddata. Selecteer **[!UICONTROL Present]** als u gegevens tot en met de vorige dag wilt rapporteren.

## [!UICONTROL Report Run schedule] Sectie

Deze sectie bepaalt de data waarop het rapport in werking wordt gesteld. Aan opstelling de data waarvoor om rapportgegevens te omvatten, zie &quot;[!UICONTROL Report range]&quot;sectie.

**\[Schedule\]:** Wanneer genereert u het rapport:

* *[!UICONTROL Immediately]*: voegt het rapport onmiddellijk toe aan de rapportwachtrij.

  >[!NOTE]
  >
  >U kunt ook [ een douanerapport op elk ogenblik ](report-run-now.md) van de [!UICONTROL Reports] mening in werking stellen.

* *[!UICONTROL On]\&lt;Date\>:* stelt het rapport op een gespecificeerde datum voor voltooiing door 09:00 in de tijdzone van de rekening in werking.

* *[!UICONTROL Recurring]:* stelt het rapport volgens een programma tijdens een gespecificeerde tijdspanne in werking.

   * **\[Schedule\]:** Hoe vaak het rapport moet worden uitgevoerd:

      * *Dagelijks* om het rapport om het aantal dagen in werking te stellen N. Bijvoorbeeld, om het rapport om de twee weken (14 dagen) in werking te stellen, selecteer deze optie en ga **14** in.

      * *wekelijks* om het rapport op gespecificeerde dagen van de week in werking te stellen. Bijvoorbeeld, om het rapport elke Maandag en Vrijdag in werking te stellen, selecteer deze optie en selecteer de controledozen naast **Maandag** en **Vrijdag**.

      * *Maandelijks* om het rapport op een specifieke numerieke dag van de maand, van 1 tot 30 in werking te stellen. Bijvoorbeeld, stel het rapport op de eerste dag van elke maand in werking, selecteer deze optie en ga **1** in.

   * **van**: De eerste datum waarop het rapport kan worden in werking gesteld. Afhankelijk van het gespecificeerde programma, kan de eerste rapportinstantie na deze datum voorkomen.

   * **tot**: De datum van de rapportvervaldatum, die tot vier kalendermaanden weg kan zijn. Voordat een rapport verloopt, ontvangen alle opgegeven e-maildoelen zeven dagen en één dag vóór de vervaldatum een e-mailwaarschuwing. Wijzig deze datum om het rapport langer te houden.

## [!UICONTROL Apply Filters] Sectie

**[!UICONTROL Add Filters]:** (Facultatieve) Extra afmetingen waardoor om de gegevens te filtreren, al dan niet de afmetingen als kolommen in het rapport inbegrepen zijn. De beschikbare filters verschillen per rapporttype en kunnen zijn: *[!UICONTROL Account]*\*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]* en *[!UICONTROL Video Duration]* .

\* *[!UICONTROL Account]* is beschikbaar voor de volgende rapporttypes slechts wanneer uw organisatie voor [ cross-account rapportering ](report-about.md#cross-account-reporting) wordt gevormd: [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], en [!UICONTROL Conversion]. Neem contact op met het accountteam van de Adobe voor meer informatie over het melden van overschrijvingen.

Ga als volgt te werk om een of meer filters toe te passen:

* Selecteer een afmeting, selecteer de exploitant (*evenaart* of *niet evenaart*), en selecteer dan de toepasselijke waarde. Bijvoorbeeld, om gegevens voor slechts preroll advertenties terug te keren, specificeer &quot;[!UICONTROL Ad Type equals Preroll]&quot;.
* (Optioneel) Voeg aanvullende criteria toe aan het filter.
* (Optioneel) Voeg aanvullende filters toe, elk met een of meer criteria.

## [!UICONTROL Build Your Report] Sectie

**[!UICONTROL Select To Add As Report Headers]:** de gegevenskolommen, of kopballen, om in het rapport te omvatten. Als u een kolom wilt toevoegen, vouwt u de categorie uit en schakelt u het selectievakje naast de kolomnaam in. De beschikbare kolommen variëren per rapport en alle niet-beschikbare metriek zijn uitgeschakeld. De beschikbare gegevenscategorieën zijn onder meer:

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > Het [!UICONTROL Household Reach & Frequency] -rapport kan slechts één dimensie bevatten.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >Het [!UICONTROL Household Reach & Frequency] -rapport kan cijfers overlappen of cijfers die elkaar niet overlappen, maar niet beide.

* [!UICONTROL Conversion Metrics] (gesorteerd op adverteerder)

* [!UICONTROL Custom Goals] (gesorteerd op adverteerder)

Zie &quot;[ Beschikbare Kolommen van het Rapport ](report-columns.md)&quot;voor beschrijvingen van alle opties.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** de orde van de kolomkopballen. U kunt elke kolom slepen en neerzetten om de volgorde aan te passen.

**[!UICONTROL Format]:** Of een rapport moet worden gegenereerd in de indeling *[!UICONTROL CSV]* (door komma&#39;s gescheiden waarden) of *[!UICONTROL Tab]* (door tabs gescheiden waarden).

**[!UICONTROL Headers]:** Of *[!UICONTROL Include]* of *[!UICONTROL Do Not Include]* kolomkoppen.

## [!UICONTROL Multi-Touch Conversion Options] Sectie

**[!UICONTROL Attribution Rule Settings]:** de montages variëren door rapporttype:

* **\[Type kenmerk\]:** ([!UICONTROL Household Conversion] rapporteert met [!UICONTROL Conversion Metrics] of [!UICONTROL Custom Goals] kolommen; adverteerders met alleen Adobe Advertising conversie) In het rapport, hoe u conversiegegevens kunt toewijzen in een reeks gebeurtenissen die tot conversie leiden:

   * *[!UICONTROL Unique]:* (het gebrek) telt het aantal tijden een afmetingswaarde (zoals een apparaat of plaatsing) op de weg aan omzetting was.

   * *[!UICONTROL Multi-Touch Attribution (MTA)]:* verdeelt het krediet van elke omzetting die op de frequentie van voorkomen van de afmetingswaarde (zoals een apparaat of plaatsing) op de weg aan omzetting wordt gebaseerd. Als er bijvoorbeeld in totaal 10 indrukken waren vóór de conversie, met 8 op CTV en 2 op Mobile, wordt 80% van het krediet (0,8) aan CTV-schermen en 0,2 aan Mobiel gegeven.

* **\[Type regel\]:** (Alle [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] en [!UICONTROL Site] rapporteren met [!UICONTROL Conversion Metrics] of [!UICONTROL Custom Goals] kolommen; adverteerders met alleen het bijhouden van Adoben Advertising) In het rapport, hoe u conversiegegevens kunt toewijzen in een reeks gebeurtenissen die tot een conversie leiden. U kunt meer dan één regel kiezen als u de verschillen tussen de regels wilt vergelijken.

  >[!NOTE]
  >
  >Conversiepaden bevatten alle indrukken en klikken binnen de indruk van de adverteerder of klik op terugkijkvensters, die zijn geconfigureerd in [!DNL Advertising Search, Social, & Commerce] . Klikken krijgen de voorkeur boven indrukken tijdens conversie-toewijzing. Om het even welke kliks in een omzettingsweg ontvangen volledige kredieten die op de attributieregel worden gebaseerd. Impressies krijgen alleen krediet als er geen klikken worden bijgehouden in het conversiepad.

   * *[!UICONTROL Last Event]:* Kenmerken conversies naar de laatste klik of indruk in het conversiepad.

   * *[!UICONTROL Weight Last More]:* kenmerkt omzettingen aan alle gebeurtenissen in de omzettingsweg maar geeft het meeste gewicht aan de laatste gebeurtenis en opeenvolgend minder gewicht aan de voorafgaande gebeurtenissen.

   * *[!UICONTROL Even Distribution]:* kenmerken conversies in gelijke mate naar elke gebeurtenis in het conversiepad.

   * *[!UICONTROL Weight First More]:* kenmerkt omzettingen aan alle gebeurtenissen in de omzettingsweg maar geeft het meeste gewicht aan de eerste gebeurtenis en opeenvolgend minder gewicht aan de volgende gebeurtenissen.

   * *[!UICONTROL First Event]:* Kenmerken conversies naar de eerste klik of indruk in het conversiepad.

   * *[!UICONTROL U-shaped]:* kenmerkt de omzetting aan alle gebeurtenissen in de omzettingsweg maar geeft het meeste gewicht aan de eerste en laatste gebeurtenissen, met opeenvolgend minder gewicht aan de gebeurtenissen in het midden van de omzettingsweg.

   * *[!UICONTROL Display Only]:* Kenmerken conversies naar de laatste DSP klik of indruk in het conversiepad. Dit omvat video- en aangesloten tv-advertenties en sluit kliks op [!DNL Advertising Search, Social, & Commerce] -advertenties uit.

   * *[!UICONTROL Social Only]:* Verouderd

  <!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

* **Lookback:** ([!UICONTROL Household Conversion] rapporten met [!UICONTROL Conversion Metrics] of [!UICONTROL Custom Goals] kolommen; adverteerders met slechts het volgen van de omzetting van de Adobe Advertising) binnen het rapport, het maximumaantal dagen na een impeilingsgebeurtenis waarin een omzettingsgebeurtenis aan het kan worden toegeschreven. De standaardwaarde is *[!UICONTROL 30 days]* en het maximum is 92 dagen.

**[!UICONTROL Paths as Columns]:** (Alle [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment] en [!UICONTROL Site] rapporteren met [!UICONTROL Conversion Metrics] of [!UICONTROL Custom Goals] kolommen) Welke typen conversies moeten worden gerapporteerd wanneer eerdere gebeurtenissen zich op hetzelfde apparaat hebben voorgedaan. U kunt maximaal drie typen opnemen. Voor elk geselecteerd type wordt een aparte kolom opgenomen voor elke omzettingsmetrische waarde en toegevoegd met het opgegeven achtervoegsel ([!UICONTROL (tl)], [!UICONTROL (ct)] of [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* omvat omzettingen die aan kliks (CT voor klik-door) en aan impressies (VT voor mening-door) worden toegewezen. Conversies die worden toegewezen aan impressies worden vermenigvuldigd met het opgegeven doorkijkgewicht. Het standaardgezichtsdoorsgewicht is 100%, wat betekent dat omzettingen die aan indrukkingen worden toegeschreven, worden geteld als 100% van de waarde van omzettingen die aan kliks worden toegeschreven.

* *[!UICONTROL With Clicks (CT)]:* omvat slechts omzettingen die aan kliks worden toegewezen.

* *[!UICONTROL Impressions Only (VT)]:* Omvat slechts omzettingen die aan impressies werden toegeschreven omdat geen kliks in de omzettingsweg werden gevolgd.

**[!UICONTROL Conversion Reporting Based On]:** Conversiegegevens rapporteren:

* *[!UICONTROL Conversion Timestamp]:* (De gebrek) Conversies worden geassocieerd met de omzettingsdatum.

* *[!UICONTROL Event Timestamp]:* Conversies worden gerapporteerd op basis van de datum van de indruk of klik die de conversie heeft veroorzaakt, zoals bepaald door het opgegeven [!UICONTROL Attribution Rule Settings] .

## [!UICONTROL Add Report Destinations] Sectie

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

**[!UICONTROL Destination Name]:** (S3, FTP, sFTP, en de bestemmingstypes van FTP SSL slechts) De namen van de rapportbestemmingen waarnaar het douanerapport wordt verzonden.

* Selecteer een doelnaam in de lijst om een bestaand doel op te geven. U kunt meerdere doelnamen afzonderlijk selecteren.

* Een nieuw doel maken:

   1. Klik **toevoegen Nieuwe Bestemming**.

   1. Ga de [ montages van de rapportbestemming ](/help/dsp/reports/report-destinations/report-destination-settings.md) in, en klik **sparen**.

   1. Terug in de rapportmontages, klik **verfrissen de Namen van de Bestemming.**

      De nieuwe bestemming is nu beschikbaar van de lijst van bestaande bestemmingen, en u kunt naar keuze het aan het rapport toevoegen.

>[!MORELIKETHIS]
>
>* [ Ongeveer de Rapporten van de Douane ](/help/dsp/reports/report-about.md)
>* [ creeer een Rapport van de Douane ](/help/dsp/reports/report-create.md)
>* [ dupliceer een Rapport van de Douane ](/help/dsp/reports/report-copy.md)
>* [ geef een Rapport van de Douane uit ](/help/dsp/reports/report-edit.md)
>* [ Download een Rapport van de Douane ](/help/dsp/reports/report-download.md)
>* [ stel een Rapport van de Douane in werking ](/help/dsp/reports/report-run-now.md)
>* [ de Montages van het Rapport van de Douane ](/help/dsp/reports/report-settings.md)
>* [ Ongeveer de Doelen van het Rapport ](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [ Beschikbare Kolommen van het Rapport ](/help/dsp/reports/report-columns.md)
