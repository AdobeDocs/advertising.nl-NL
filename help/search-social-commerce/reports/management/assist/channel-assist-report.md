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

*Adverteerders met Onderzoek, Sociaal, &amp; Commerce klikken het volgen en met omzetting het volgen van van Adobe Advertising, Adobe Analytics (met een [!DNL Analytics] integratie), of verstrekt in voer gebruikend een teken (`ef_id`) slechts*

In [!UICONTROL Channel Assist Report] wordt aangegeven hoe verschillende marketingkanalen (search of social vanuit Search, Social en Commerce, of display of video vanuit Advertising DSP) het conversieproces hebben ondersteund. Het rapport toont hoe elk patroon van gebeurtenistypen dat tot één of meerdere omzettingen heeft geleid aan uw algemene omzettingen heeft bijgedragen. U kunt bijvoorbeeld zien hoeveel conversies er zijn geweest wanneer gebruikers voor het eerst een display-advertentie-impressie zagen, vervolgens op een zoekadvertentie hadden geklikt en vervolgens een bestelling hadden geplaatst, of u kunt zien hoeveel conversies er zijn opgetreden nadat gebruikers met meer dan 10 advertenties hadden gewerkt. Gebeurtenistypen omvatten zoekklikken, weergave-impressies en -klikken, video-impressies en -klikken, en andere impressies en andere kliks. <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

De rapportresultaten omvatten samengevoegde gegevens voor elk patroon van gebeurtenistypen in de omzettingspad - tot de vroegste gebeurtenistypen van N - die binnen het 2} impressievenster van de adverteerder [ voorkwam terugkijkvenster ](/help/search-social-commerce/glossary.md#c-d) en [ impotlood terugkijkervenster ](/help/search-social-commerce/glossary.md#i-j). Als u bijvoorbeeld een padgrootte van vijf (5) selecteert, bevat het rapport conversiepaden met maximaal de vijf vroegste gebeurtenissen, met één rij voor elk bijgehouden patroon van gebeurtenistypen (zoals &quot;zoekklik&quot; en &quot;weergave-impressie&quot;). In elke rij ziet u één gebeurtenispatroon, inclusief de eerste gebeurtenis in het pad en de laatste gebeurtenis die tot conversies heeft geleid (zelfs als de laatste gebeurtenis zich buiten de opgegeven padgrootte bevindt). Standaard staan de rijen in oplopende volgorde volgens het aantal gebeurtenissen in het pad.

U kunt optioneel voor elke rij geaggregeerde conversiegegevens opnemen. Wanneer u conversie-/omzetkolommen in het rapport opneemt, wordt elk conversietype weergegeven in vier kolommen, met a) het totale aantal conversies, b) het percentage van uw totale conversies dat werd toegewezen aan dat gebeurtenispatroon, c) de gemiddelde latentie in de dag vanaf de eerste gebeurtenis tot een conversie, en d) de gemiddelde latentie in dagen vanaf de laatste gebeurtenis tot een conversie. Wanneer het conversiepad meer gebeurtenissen dan de opgegeven padgrootte bevat, bevat het rapport extra rijen die gegevens samenvoegen voor conversies die het resultaat zijn van een groter aantal gebeurtenissen (zoals alle patronen met zes gebeurtenistypen).

U kunt gegevens van de vorige 18 maanden bekijken.

## Beschikbare kolommen

Het volgende is de kolommen die voor elk rapport beschikbaar zijn. Standaard worden de standaardkolommen automatisch opgenomen. U kunt de beschikbare douanekolommen van de sectie van Kolommen van de rapportmontages toevoegen.

| Kolom | Standaard? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] tot [!UICONTROL 5th Event] | Standaard | De vijf vroegste gebeurtenistypes in de omzettingsweg die binnen het 20} klikken van de adverteerder terugkijkvenster ](/help/search-social-commerce/glossary.md#c-d) en [ impressiecontrollback venster ](/help/search-social-commerce/glossary.md#i-j) voorkwam.[ |
| [!UICONTROL Path Size] | Standaard | Het aantal gebeurtenistypes in de omzettingsweg die binnen het 20} klikken van de adverteerder terugkijkvenster ](/help/search-social-commerce/glossary.md#c-d) en [ impotentie terugkijkvenster ](/help/search-social-commerce/glossary.md#i-j) voorkwam.[ |
| [!UICONTROL First Event Type] | Standaard | Het gebeurtenistype van de eerste (vroegste) gebeurtenis in het conversiepad. |
| [!UICONTROL Last Event Type] | Standaard | Het gebeurtenistype van de laatste gebeurtenis die tot conversies heeft geleid (zelfs als de laatste gebeurtenis zich buiten de opgegeven padgrootte bevindt). |
| \[Advertiser-specifieke, aangepaste (afgeleide) metrics\] | Aangepast | De waarde voor een aangepaste metriek die je hebt gemaakt en die wordt berekend op basis van bestaande metrieken. |
| \[Conversiemetrieken voor adverteerders\] | Aangepast | Het aantal conversies voor een opgegeven metrische of metrische conversiemethode voor sitebetrokkenheid. |
| [!UICONTROL % of Total] \[metrisch omzetten\] | Automatisch | (Niet beschikbaar in rapportinstellingen maar automatisch opgenomen in de rapportuitvoer voor elke omrekeningsmaatstaf inbegrepen) Het percentage van uw totale omzettingen over portefeuilles die aan het gebeurtenispatroon werden toegeschreven. |
| [!UICONTROL 6th Event] t/m [!UICONTROL 30th Event] | Aangepast | Zesde door 30th gebeurtenistypes in de omzettingsweg die binnen het 0} voorkwam van de adverteerder terugkijkvenster ](/help/search-social-commerce/glossary.md#c-d) en [ impotentie terugkijkvenster ](/help/search-social-commerce/glossary.md#i-j).[ |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[metrisch omzetten\] | Automatisch | (Niet beschikbaar in rapportinstellingen, maar automatisch opgenomen in rapportuitvoer voor elke opgenomen conversiemethode) De gemiddelde latentie in dagen vanaf de eerste gebeurtenis tot een conversie. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[metrisch omzetten\] | Automatisch | (Niet beschikbaar in rapportinstellingen maar automatisch opgenomen in rapportuitvoer) De gemiddelde latentie in dagen vanaf de laatste gebeurtenis tot een conversie. |
| [!UICONTROL Path Frequency] | Aangepast | Het aantal keren dat het pad voor deze rij is opgetreden vóór de conversie. |

>[!MORELIKETHIS]
>
>* [ Ongeveer bijstaat rapporten ](assist-report-about.md)
>* [ De [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [ De [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [ sta rapportmontages ](assist-report-settings.md) bij
>* [ produceer een hulprapport ](assist-report-generate.md)
