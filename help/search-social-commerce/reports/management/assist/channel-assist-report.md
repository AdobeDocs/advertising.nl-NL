---
title: '[!UICONTROL Channel Assist Report]'
description: Meer informatie over de [!UICONTROL Channel Assist Report] .
exl-id: 67bce347-2776-4585-adb4-e1a4d76fbadc
feature: Search Reports, Search Assist Reports
source-git-commit: 45920c6ea9d2953c963ddf6472966b3fc3a91395
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# De [!UICONTROL Channel Assist Report]

*Advertisers met Onderzoek, Sociale, &amp; Commerce klikken het volgen en met omzetting het volgen van Adobe Advertising, Adobe Analytics (met een [!DNL Analytics] integratie), of verstrekt in voer gebruikend een teken (`ef_id`) slechts*

In [!UICONTROL Channel Assist Report] wordt aangegeven hoe verschillende marketingkanalen (zoeken of sociaal zoeken op Zoeken, Sociaal en Commerce, of weergave of video van Advertising DSP) het conversieproces hebben ondersteund. Het rapport toont hoe elk patroon van gebeurtenistypen dat tot één of meerdere omzettingen heeft geleid aan uw algemene omzettingen heeft bijgedragen. U kunt bijvoorbeeld zien hoeveel conversies hebben plaatsgevonden wanneer gebruikers eerst een weergave en een indruk zagen, vervolgens op een zoekadvertentie hebben geklikt en vervolgens een bestelling hebben geplaatst. U kunt ook zien hoeveel conversies er zijn opgetreden nadat gebruikers met meer dan 10 advertenties hebben gewerkt. Gebeurtenistypen zijn zoekklikken, weergave-impressies en -klikken, video-impressies en -kliks, en andere impressies en andere kliks. <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

De rapportresultaten omvatten samengevoegde gegevens voor elk patroon van gebeurtenistypen in de omzettingsweg - tot N vroegste gebeurtenistypen - die binnen het 2&rbrace; de raadplegingsvenster van de adverteerder [&#x200B; voorkwamen klikken terugkijkvenster &#x200B;](/help/search-social-commerce/glossary.md#c-d) en [&#x200B; het venster van de imkerraadpleging &#x200B;](/help/search-social-commerce/glossary.md#i-j). Als u bijvoorbeeld een padgrootte van vijf (5) selecteert, bevat het rapport conversiepaden die maximaal de vijf vroegste gebeurtenissen bevatten, met één rij voor elk bijgehouden patroon van gebeurtenistypen (zoals &quot;zoekklik&quot; en &quot;weergaveindruk&quot;). In elke rij wordt één gebeurtenispatroon weergegeven, inclusief de eerste gebeurtenis in het pad en de laatste gebeurtenis die tot conversies heeft geleid (zelfs als de laatste gebeurtenis zich buiten de opgegeven padgrootte bevindt). Standaard staan de rijen in oplopende volgorde met het aantal gebeurtenissen in het pad.

U kunt optioneel voor elke rij geaggregeerde conversiegegevens opnemen. Wanneer u omzettingen/opbrengstkolommen in het rapport omvat, wordt elk omzettingstype vertegenwoordigd in vier kolommen, die a) het totale aantal omzettingen tonen, b) het percentage van uw algemene omzettingen die aan dat gebeurtenispatroon werden toegeschreven, c) de gemiddelde latentie in dag van de eerste gebeurtenis aan een omzetting, en d) de gemiddelde latentie in dagen van de laatste gebeurtenis aan een omzetting. Wanneer het conversiepad meer gebeurtenissen dan de opgegeven padgrootte bevat, bevat het rapport extra rijen waarin gegevens worden samengevoegd voor conversies die het resultaat zijn van hogere aantallen gebeurtenissen (zoals alle patronen die zes gebeurtenistypen bevatten).

U kunt gegevens van de vorige 18 maanden bekijken.

## Beschikbare kolommen

Het volgende is de kolommen die voor elk rapport beschikbaar zijn. De standaardkolommen worden standaard automatisch opgenomen. U kunt de beschikbare douanekolommen van de sectie van Kolommen van de rapportmontages toevoegen.

| Kolom | Standaard? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] t/m [!UICONTROL 5th Event] | Standaard | De vijf vroegste gebeurtenistypen in de omzettingsweg die binnen de adverteerder [&#x200B; voorkwam klikken raadplegingsvenster &#x200B;](/help/search-social-commerce/glossary.md#c-d) en [&#x200B; venster van de imkerraadpleging &#x200B;](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Path Size] | Standaard | Het aantal gebeurtenistypen in de omzettingsweg die binnen de adverteerder [&#x200B; voorkwam klikt raadplegingsvenster &#x200B;](/help/search-social-commerce/glossary.md#c-d) en [&#x200B; venster van de imkerraadpleging &#x200B;](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Event Type] | Standaard | Het gebeurtenistype van de eerste (vroegste) gebeurtenis in het conversiepad. |
| [!UICONTROL Last Event Type] | Standaard | Het gebeurtenistype van de laatste gebeurtenis die tot omzettingen heeft geleid (zelfs als de laatste gebeurtenis zich buiten de opgegeven padgrootte bevindt). |
| \[Advertiser-specifieke, aangepaste (afgeleide) metriek\] | Aangepast | De waarde voor een aangepaste metrische waarde die u hebt gemaakt en die wordt berekend op basis van bestaande metriek. |
| \[Specifieke conversiemetriek voor adverteerders\] | Aangepast | Het aantal omzettingen voor een gespecificeerde metrische of metrische plaatsbepaling van de omzetting. |
| [!UICONTROL % of Total] \[metrisch omzetten\] | Automatisch | (Niet beschikbaar in rapportinstellingen maar automatisch opgenomen in de rapportuitvoer voor elke omrekeningsmaatstaf inbegrepen) Het percentage van uw totale omzettingen over portefeuilles die aan het gebeurtenispatroon werden toegeschreven. |
| [!UICONTROL 6th Event] t/m [!UICONTROL 30th Event] | Aangepast | Zesde door 30th gebeurtenistypen in de omzettingsweg die binnen het paneel van de adverteerder [&#x200B; voorkwam klikken raadplegings achteruit &#x200B;](/help/search-social-commerce/glossary.md#c-d) en [&#x200B; venster van de imkerraadpleging &#x200B;](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[metrisch omzetten\] | Automatisch | (Niet beschikbaar in rapportinstellingen maar automatisch opgenomen in de rapportuitvoer voor elke omrekeningsfactor inbegrepen) De gemiddelde vertraging in dagen van de eerste gebeurtenis naar een omzetting. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[metrisch omzetten\] | Automatisch | (Niet beschikbaar in rapportinstellingen maar automatisch opgenomen in de rapportuitvoer) De gemiddelde vertraging in dagen vanaf de laatste gebeurtenis tot een conversie. |
| [!UICONTROL Path Frequency] | Aangepast | Het aantal keren dat het pad voor deze rij is opgetreden vóór de conversie. |

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer bijstaat rapporten &#x200B;](assist-report-about.md)
>* [&#x200B; De [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [&#x200B; De [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [&#x200B; sta rapportmontages &#x200B;](assist-report-settings.md) bij
>* [&#x200B; produceer en bijstaat rapport &#x200B;](assist-report-generate.md)
