---
title: '[!UICONTROL Keyword Assist Report]'
description: Meer informatie over de [!UICONTROL Keyword Assist Report] .
exl-id: 24e5854c-5696-43cd-ac21-64209f9f57d4
feature: Search Reports, Search Assist Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# De [!UICONTROL Keyword Assist Report]

*Advertisers met Onderzoek, Sociale, &amp; Commerce klikken het volgen en met omzetting het volgen van Adobe Advertising, Adobe Analytics (met een [!DNL Analytics] integratie), of verstrekt in voer gebruikend een teken (`ef_id`) slechts*

De [!UICONTROL Keyword Assist Report] geeft aan op welke trefwoorden of plaatsen de schijf klikt. Het rapport toont elk patroon van betaalde onderzoekssleutelwoorden of plaatsingen die in een omzettingsweg klikken en wijst erop hoe dat patroon aan uw algemene omzettingen droeg. U ziet bijvoorbeeld hoeveel conversies hebben plaatsgevonden wanneer gebruikers eerst op een advertentie klikten die het resultaat was van een trefwoordzoekopdracht naar &quot;leren schoenen&quot; en vervolgens op een advertentie klikte na een trefwoordzoekopdracht naar &quot;schoenen overslaan&quot; en vervolgens een bestelling plaatste. U kunt ook zien hoeveel conversies er zijn opgetreden nadat gebruikers op advertenties hadden geklikt die het resultaat waren van meer dan 10 trefwoorden.

De rapportresultaten omvatten samengevoegde gegevens voor maximaal N het oudste betaalde zoekwoord of de plaatsingsklikjes in de omzettingsweg die binnen adverteerders voorkwamen
Klik op terugzoekvensters en terugkijkvensters. Bijvoorbeeld, als u een weggrootte van vijf (5) selecteert, dan bestaat het rapport uit omzettingspaden die tot de vijf vroegste sleutelwoorden of plaatsen omvatten die klikken, met één rij voor elk patroon van gevolgde kliks kregen. Elke rij omvat het eerste sleutelwoord of de plaatsing in de weg en laatste sleutelwoord of de plaatsing die in omzettingen resulteerden (zelfs als het laatste sleutelwoord buiten de gespecificeerde weggrootte is.) Standaard staan de rijen in oplopende volgorde met het aantal gebeurtenissen in het pad.

>[!NOTE]
>
>Als het rapport plaatsingen van inhoud-toegelaten onderzoekscampagnes omvat (die geen sleutelwoorden omvatten), dan toont de [!UICONTROL Keyword] kolom de toepasselijke namen van de advertentiegroep, zoals &quot;(adgroup inhoud) Uw Naam van de Groep van de Advertentie.&quot;

U kunt optioneel voor elke rij geaggregeerde conversiegegevens opnemen. Wanneer u omzettingen/opbrengstkolommen in het rapport omvat, wordt elk omzettingstype vertegenwoordigd in vier kolommen, die a) het totale aantal omzettingen tonen, b) het percentage van uw algemene omzettingen die aan dat sleutelwoordpatroon werden toegeschreven, c) de gemiddelde latentie in dagen van de eerste gebeurtenis (op het eerste sleutelwoord) aan een omzetting tonen, en d) de gemiddelde latentie in dagen van de laatste gebeurtenis (op het laatste sleutelwoord) aan een omzetting. Wanneer het omzettingspad meer trefwoorden bevat dan de opgegeven padgrootte, bevat het rapport extra rijen waarin gegevens worden samengevoegd voor conversies die het resultaat zijn van de hogere aantallen trefwoorden (zoals alle patronen waarin wordt geklikt op zes trefwoorden).

U kunt gegevens van de vorige 18 maanden bekijken.

## Beschikbare kolommen

Het volgende is de kolommen die voor elk rapport beschikbaar zijn. De standaardkolommen worden standaard automatisch opgenomen. U kunt de beschikbare douanekolommen van de sectie van Kolommen van de rapportmontages toevoegen.

| Kolom | Standaard? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] t/m [!UICONTROL 5th Keyword] | Standaard | Het vijf vroegste betaalde onderzoekssleutelwoord of de plaatsing klikt in de omzettingsweg die binnen het venster van de adverteerder [&#x200B; klikte terugkijkvenster &#x200B;](/help/search-social-commerce/glossary.md#c-d) en [&#x200B; venster van de imkerraadpleging &#x200B;](/help/search-social-commerce/glossary.md#i-j) voorkwam.<br><br><b> Nota:</b> als het rapport plaatsingen van inhoud-toegelaten onderzoekscampagnes omvat (die geen sleutelwoorden omvatten), dan tonen deze kolommen de toepasselijke namen van de ad groep, zoals &quot;(adgroup inhoud) Uw Naam van de Groep van de Advertentie,&quot;in plaats daarvan. |
| [!UICONTROL Path Size] | Standaard | Het aantal sleutelwoorden en/of plaatsen in de omzettingsweg die binnen het paneel van de adverteerder [&#x200B; voorkwam klikken raadplegings achteruit &#x200B;](/help/search-social-commerce/glossary.md#c-d) en [&#x200B; venster van de imkerraadpleging &#x200B;](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | Standaard | Het eerste trefwoord of de eerste plaatsing in het conversiepad. |
| [!UICONTROL Last Keyword] | Standaard | Het laatste trefwoord of de laatste plaatsing die tot omzettingen heeft geleid (zelfs als het laatste trefwoord zich buiten de opgegeven padgrootte bevindt). |
| \[Advertiser-specifieke, aangepaste (afgeleide) metriek\] | Aangepast | De waarde voor een aangepaste metrische waarde die u hebt gemaakt en die wordt berekend op basis van bestaande metriek. |
| \[Specifieke conversiemetriek voor adverteerders\] | Aangepast | Het aantal omzettingen voor een gespecificeerde metrische of metrische plaatsbepaling van de omzetting. |
| [!UICONTROL % of Total] \[metrisch omzetten\] | Automatisch | (Niet beschikbaar in rapportmontages maar automatisch inbegrepen in rapportoutput voor elke inbegrepen metrische omzettingen) Het percentage van uw algemene omzettingen over portefeuilles die aan het sleutelwoord en/of plaatsingspatroon werden toegewezen. |
| [!UICONTROL 6th Keyword] t/m [!UICONTROL 10th Keyword] | Aangepast | Zesde door tiende betaald onderzoekssleutelwoord of plaatsing klikt in de omzettingsweg die binnen het venster van de adverteerder [&#x200B; klikte raadplegingsterugkijker &#x200B;](/help/search-social-commerce/glossary.md#c-d) en [&#x200B; venster van de imkerraadpleging &#x200B;](/help/search-social-commerce/glossary.md#i-j) voorkwam.<br><br><b> Nota:</b> als het rapport plaatsingen van inhoud-toegelaten onderzoekscampagnes omvat (die geen sleutelwoorden omvatten), dan tonen deze kolommen de toepasselijke namen van de ad groep, zoals &quot;(adgroup inhoud) Uw Naam van de Groep van de Advertentie,&quot;in plaats daarvan. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[metrisch omzetten\] | Automatisch | (Niet beschikbaar in rapportmontages maar automatisch inbegrepen in rapportoutput voor elke inbegrepen metrisch van de omzetting) De gemiddelde vertraging in dagen van de eerste gebeurtenis (op het eerste sleutelwoord of de plaatsing) aan een omzetting. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[metrisch omzetten\] | Automatisch | (Niet beschikbaar in rapportmontages maar automatisch inbegrepen in rapportoutput) De gemiddelde latentie in dagen van de laatste gebeurtenis (op het laatste sleutelwoord of de plaatsing) aan een omzetting. |
| [!UICONTROL Path Frequency] | Aangepast | Het aantal keren dat het pad voor deze rij is opgetreden vóór de conversie. |

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer bijstaat rapporten &#x200B;](assist-report-about.md)
>* [&#x200B; De [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [&#x200B; De [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [&#x200B; sta rapportmontages &#x200B;](assist-report-settings.md) bij
>* [&#x200B; produceer en bijstaat rapport &#x200B;](assist-report-generate.md)
