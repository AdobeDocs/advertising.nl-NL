---
title: De gegevens die voor rapporten worden gebruikt
description: Leer meer over de verschillende typen gegevens die beschikbaar zijn in gegevensweergaven en aangepaste rapporten.
exl-id: ba808b21-4421-4de5-9293-a20ec67cc81c
feature: Search Reports
source-git-commit: f357d9a9ec0f8b38fbc43726265521e6fd77c7d0
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# De gegevens die voor rapporten worden gebruikt

Search, Social &amp; Commerce bevat een uitgebreide reeks prestatierapporten op basis van klik- en conversiegegevens. U kunt elementaire prestatiegegevens voor de verschillende componenten van een portfolio of advertentieaccount bekijken vanuit de weergaven [!UICONTROL Portfolios] en [!UICONTROL Campaigns] en door verschillende basis- en geavanceerd-rapporten te genereren.

Adverteerders die de de conversie volgende dienst van de Adobe Advertising gebruiken kunnen ook het aantal klikken voor een geografische plaats of domeinnaam van een verwijzende website identificeren, hoe de advertenties in elk kanaal en de diverse gebeurtenissen die tot een omzetting leiden tot de algemene omzettingspercentage bijdragen, en de distributie van omzettingen voor één enkele [ omzettings metrische ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) door marketing kanaal. De beschikbare rapporten variëren per type gebruikersaccount. Het team van de Rekening van de Adobe heeft toegang tot alle rapporten.

De meeste rapporten kunnen worden aangepast om slechts de informatie te tonen u wilt zien. De volgende standaardmetriek is beschikbaar in de meeste rapporten en op het advertentieniveau berekend:

* **Standaard prestatiesmetriek:**

   * **[!UICONTROL Impressions]:** Het totale aantal keren dat de advertentie is geplaatst.

   * **[!UICONTROL Clicks]:** Het totale aantal keren dat een koppeling in de advertentie is aangeklikt.

   * **[!UICONTROL Cost]:** De totale kosten van de advertentie. De kosten voor advertentie per klik (PPC) zijn altijd het aantal klikken vermenigvuldigd met de kosten per klik.

   * **[!UICONTROL Cost per Click]:** De gemiddelde kosten voor één klik voor een advertentie, die de kosten van de advertentie is gedeeld door het totale aantal klikken voor de advertentie. Als u bijvoorbeeld 100 USD voor een advertentie uitgeeft en de advertentie 10 klikken genereert, bedragen de kosten per klik 100 USD/10=10 USD per klik.

   * **[!UICONTROL Average Position]:** (Indien van toepassing) De gemiddelde positie van een advertentie die is geplaatst, gewogen door het aantal impressies.

   * **[!UICONTROL Estimated Clicks]:** (Opgenomen in geavanceerde rapporten voor adverteerders met de dienst van het de converteren van de Adobe Advertising slechts) het totale aantal geschatte klikken voor een stad of domeinnaam van een verwijzende website. Dit kunnen gegevens zijn voor advertentienetwerken waarvoor een adverteerder geen advertentieaccount heeft.

* {de metriek van de Omzetting 0}:**het totale aantal omzettingen voor elk van de omzettingsmetriek van adverteerders, of transactiegegevens die naar metrische omzettingen worden gevolgd.** Dit kan conversie- en plaatsingsmetriek omvatten, maar niet berekende metriek en geavanceerde berekende metriek, die van Adobe Analytics worden gesynchroniseerd.

  Dit kan ook [[!DNL Google Ads] - bijgehouden omzettingen ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) en [[!DNL Google Analytics] - bijgehouden omzettingen ](/help/search-social-commerce/admin/data-sources/data-source-about.md) omvatten die voor de adverteerderrekening worden gesynchroniseerd.

* **de metriek van de Douane:** Uw eigen metriek, die u door formules leidt tot die op bestaande metriek (zoals kosten per orde) worden gebaseerd.

## Beschikbaarheid van gegevens

Wanneer u rapporten genereert, kunt u kiezen hoe u conversiegegevens kunt toewijzen in een reeks gebeurtenissen die tot conversie leiden. U kunt bijvoorbeeld de volledige conversie toewijzen aan de laatste gebeurtenis of de laatste gebeurtenis meer gewicht geven dan de andere. Standaard worden conversies toegewezen aan de laatste gebeurtenis.

Afhankelijk van de attributieregel u voor het rapport specificeert, zijn de gegevens voor elk rapporttype beschikbaar voor de volgende data.

| Rapportgroep | Rapport | Data waarvoor gegevens beschikbaar zijn |
| --- | --- | --- |
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | Vanaf 15 mei 2021.<br><br><b> Uitzondering:</b> de metrieke gegevens van de Aanwezigheid zijn beschikbaar die op 8 september 2022 beginnen. |
| | Alle andere [!UICONTROL Basic Reports] | De voorgaande 36 maanden.<br><br><b> Uitzondering:</b> de metrieke gegevens van de Aanwezigheid zijn beschikbaar die op 8 september 2022 beginnen. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | De voorgaande 45 dagen. |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | De voorafgaande twee (2) maanden plus de huidige maand. |
| [!UICONTROL Assist Reports] | Alles | De voorafgaande 18 maanden. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | Het voorgaande jaar. |
| | [!UICONTROL Google Asset Group Performance Report] | Geen beperkingen |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report], [!UICONTROL MSA Network Impression Share Report], [!UICONTROL MSA Network Performance Report] | De laatste 180 dagen. |
| | [!UICONTROL RSA Assets Report] | Vanaf 10 augustus 2022. |
| | Alle andere [!UICONTROL Specialty Reports] | De twee voorgaande (2) maanden. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | De voorafgaande 18 maanden. |
| [!UICONTROL Change History Report] | — | De voorafgaande 31 dagen. |

>[!MORELIKETHIS]
>
>* [ Ongeveer rapporten ](report-about.md)
>* [ Aanvankelijke opstellingstaken voor rapporten ](initial-setup.md)
