---
title: '[!UICONTROL Keyword Assist Report]'
description: Meer informatie over de [!UICONTROL Keyword Assist Report].
exl-id: 07de2880-111b-498f-9f7f-ec15f89230ae
feature: Search Reports, Search Assist Reports
source-git-commit: 97111c6cd38098cac72b8773390afd254a017d1d
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# De [!UICONTROL Keyword Assist Report]

*Adverteerders met Zoeken, Sociale Zaken &amp; Handel klikken het volgen en met omzetting het volgen van van Adobe Advertising, Adobe Analytics (met [!DNL Analytics] integratie), of verstrekt in voer gebruikend een teken (`ef_id`alleen )*

De [!UICONTROL Keyword Assist Report] Hiermee wordt aangegeven op welke trefwoorden of plaatsen de schijf klikt. Het rapport toont elk patroon van betaalde onderzoekssleutelwoorden of plaatsingen die in een omzettingsweg klikken en wijst erop hoe dat patroon aan uw algemene omzettingen droeg. U ziet bijvoorbeeld hoeveel conversies hebben plaatsgevonden wanneer gebruikers eerst op een advertentie klikten die het resultaat was van een trefwoordzoekopdracht naar &quot;leren schoenen&quot; en vervolgens op een advertentie klikte na een trefwoordzoekopdracht naar &quot;schoenen overslaan&quot; en vervolgens een bestelling plaatste. U kunt ook zien hoeveel conversies er zijn opgetreden nadat gebruikers op advertenties hadden geklikt die het resultaat waren van meer dan 10 trefwoorden.

De rapportresultaten omvatten samengevoegde gegevens voor tot N het vroegste betaalde onderzoekssleutelwoord of de plaatsing klikt in de omzettingsweg die binnen de klikraadplegings en de venster van de impressiegolf van de adverteerder optrad. Bijvoorbeeld, als u een weggrootte van vijf (5) selecteert, dan bestaat het rapport uit omzettingspaden die tot de vijf vroegste sleutelwoorden of plaatsen omvatten die klikken, met één rij voor elk patroon van gevolgde kliks kregen. Elke rij omvat het eerste sleutelwoord of de plaatsing in de weg en laatste sleutelwoord of de plaatsing die in omzettingen resulteerden (zelfs als het laatste sleutelwoord buiten de gespecificeerde weggrootte is.) Standaard staan de rijen in oplopende volgorde met het aantal gebeurtenissen in het pad.

>[!NOTE]
>
>Als het rapport plaatsingen van inhoud-toegelaten onderzoekscampagnes omvat (die geen sleutelwoorden omvatten), dan [!UICONTROL Keyword] in de kolom staan de toepasselijke namen van de advertentiegroepen, zoals &#39;(Inhoud adgroup) Uw naam van de advertentiegroep.&#39;

U kunt optioneel voor elke rij geaggregeerde conversiegegevens opnemen. Wanneer u omzettingen/opbrengstkolommen in het rapport omvat, wordt elk omzettingstype vertegenwoordigd in vier kolommen, die a) het totale aantal omzettingen tonen, b) het percentage van uw algemene omzettingen die aan dat sleutelwoordpatroon werden toegeschreven, c) de gemiddelde latentie in dagen van de eerste gebeurtenis (op het eerste sleutelwoord) aan een omzetting tonen, en d) de gemiddelde latentie in dagen van de laatste gebeurtenis (op het laatste sleutelwoord) aan een omzetting. Wanneer het omzettingspad meer trefwoorden bevat dan de opgegeven padgrootte, bevat het rapport extra rijen waarin gegevens worden samengevoegd voor conversies die het resultaat zijn van de hogere aantallen trefwoorden (zoals alle patronen waarin wordt geklikt op zes trefwoorden).

U kunt gegevens van de vorige 18 maanden bekijken.

## Beschikbare kolommen

Het volgende is de kolommen die voor elk rapport beschikbaar zijn. De standaardkolommen worden standaard automatisch opgenomen. U kunt de beschikbare douanekolommen van de sectie van Kolommen van de rapportmontages toevoegen.

| Kolom | Standaard? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] tot [!UICONTROL 5th Keyword] | Standaard | De vijf oudste betaalde zoektrefwoorden of -plaatsing klikken in het conversiepad dat binnen het adverteerderspad is opgetreden [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Opmerking:</b> Als het rapport plaatsingen van inhoud-toegelaten onderzoekscampagnes omvat (die geen sleutelwoorden omvatten), dan tonen deze kolommen de toepasselijke namen van de advertentiegroep, zoals &quot;(adgroup inhoud) Uw Naam van de Groep van de Advertentie,&quot;in plaats daarvan. |
| [!UICONTROL Path Size] | Standaard | Het aantal trefwoorden en/of plaatsen in het conversiepad dat is opgetreden binnen de adverteerders [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | Standaard | Het eerste trefwoord of de eerste plaatsing in het conversiepad. |
| [!UICONTROL Last Keyword] | Standaard | Het laatste trefwoord of de laatste plaatsing die tot omzettingen heeft geleid (zelfs als het laatste trefwoord zich buiten de opgegeven padgrootte bevindt). |
| \[Advertiser-specifieke, aangepaste (afgeleide) metriek\] | Aangepast | De waarde voor een aangepaste metrische waarde die u hebt gemaakt en die wordt berekend op basis van bestaande metriek. |
| \[Advertiser-specifieke transactieeigenschappen\] | Aangepast | Het aantal omzettingen voor een gespecificeerde transactiebezit of metrisch van de plaatsovereenkomst. |
| [!UICONTROL % of Total] \[eigenschap transactie\] | Automatisch | (Niet beschikbaar in rapportinstellingen maar automatisch opgenomen in de rapportuitvoer voor elke opgenomen transactie-eigenschap) Het percentage van de totale conversies over portfolio&#39;s dat is toegewezen aan het trefwoord en/of plaatsingspatroon. |
| [!UICONTROL 6th Keyword] tot [!UICONTROL 10th Keyword] | Aangepast | Het zesde tot en met tiende betaalde zoekwoord of de plaatsing klikt in het conversiepad dat binnen de adverteerders is opgetreden [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Opmerking:</b> Als het rapport plaatsingen van inhoud-toegelaten onderzoekscampagnes omvat (die geen sleutelwoorden omvatten), dan tonen deze kolommen de toepasselijke namen van de advertentiegroep, zoals &quot;(adgroup inhoud) Uw Naam van de Groep van de Advertentie,&quot;in plaats daarvan. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[eigenschap transactie\] | Automatisch | (Niet beschikbaar in rapportmontages maar automatisch inbegrepen in rapportoutput voor elk inbegrepen transactiebezit) De gemiddelde vertraging in dagen van de eerste gebeurtenis (op het eerste sleutelwoord of de plaatsing) aan een omzetting. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[eigenschap transactie\] | Automatisch | (Niet beschikbaar in rapportmontages maar automatisch inbegrepen in rapportoutput) De gemiddelde latentie in dagen van de laatste gebeurtenis (op het laatste sleutelwoord of de plaatsing) aan een omzetting. |
| [!UICONTROL Path Frequency] | Aangepast | Het aantal keren dat het pad voor deze rij is opgetreden vóór de conversie. |

>[!MORELIKETHIS]
>
>* [Over rapporten voor Help](assist-report-about.md)
>* [De [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [De [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Rapportinstellingen voor assistentie](assist-report-settings.md)
>* [Een rapport voor assistentie genereren](assist-report-generate.md)
