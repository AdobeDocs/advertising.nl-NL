---
title: De gegevens die voor rapporten worden gebruikt
description: Leer meer over de verschillende typen gegevens die beschikbaar zijn in gegevensweergaven en aangepaste rapporten.
exl-id: 3e1f2967-5034-46bc-8473-63cffeeeecba
feature: Search Reports
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# De gegevens die voor rapporten worden gebruikt

Search, Social &amp; Commerce bevat een uitgebreide reeks prestatierapporten die zijn gebaseerd op klik- en conversiegegevens. U kunt elementaire prestatiegegevens voor de verschillende componenten van een portfolio of advertentieaccount bekijken via het tabblad [!UICONTROL Portfolios] en [!UICONTROL Campaigns] en door verschillende basis - en geavanceerd - rapporten op te stellen .

Adverteerders die de service Adobe Advertising converteren volgen gebruiken, kunnen ook het aantal klikken voor een geografische locatie of domeinnaam van een verwijzende website identificeren, de manier waarop advertenties in elk kanaal en de verschillende gebeurtenissen die tot een conversie leiden, bijdragen aan de algemene conversiekoers en de distributie van conversies voor één enkele website [omzettingsmetrisch](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) via het marketingkanaal. De beschikbare rapporten variëren per type gebruikersaccount. Het Adobe Account Team heeft toegang tot alle rapporten.

De meeste rapporten kunnen worden aangepast om slechts de informatie te tonen u wilt zien. De volgende standaardmetriek is beschikbaar in de meeste rapporten en op het advertentieniveau berekend:

* **Standaardprestatiewaarden:**

   * **[!UICONTROL Impressions]:** Het totale aantal keren dat de advertentie is geplaatst.

   * **[!UICONTROL Clicks]:** Het totale aantal keren dat op een koppeling in de advertentie is geklikt.

   * **[!UICONTROL Cost]:** De totale kosten van de advertentie. De kosten voor advertentie per klik (PPC) zijn altijd het aantal klikken vermenigvuldigd met de kosten per klik.

   * **[!UICONTROL Cost per Click]:** De gemiddelde kosten voor één klik voor een advertentie. Dit zijn de kosten van de advertentie gedeeld door het totale aantal klikken voor de advertentie. Als u bijvoorbeeld 100 USD voor een advertentie uitgeeft en de advertentie 10 klikken genereert, bedragen de kosten per klik 100 USD/10=10 USD per klik.

   * **[!UICONTROL Average Position]:** (Indien van toepassing) De gemiddelde positie van een geplaatste advertentie, gewogen door het aantal indrukken.

   * **[!UICONTROL Estimated Clicks]:** (Opgenomen in geavanceerde rapporten voor adverteerders met alleen de service Adobe Advertising converteren) Het totale aantal geschatte klikken voor een stad of domeinnaam van een verwijzende website. Dit kunnen gegevens zijn voor advertentienetwerken waarvoor een adverteerder geen advertentieaccount heeft.

* **Omzettingscijfers:** Het totale aantal omzettingen voor elk van de omzettingsmetriek van de adverteerder, of transactiegegevens die in de richting van omzettingsmetrisch worden gevolgd. Dit kan conversie- en plaatsingsmetriek omvatten, maar niet berekende metriek en geavanceerde berekende metriek, die van Adobe Analytics worden gesynchroniseerd.

  Dit kan ook [[!DNL Google Ads]-trackconversies](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) en [[!DNL Google Analytics]-trackconversies](/help/search-social-commerce/admin/data-sources/data-source-about.md) die worden gesynchroniseerd voor het adverteerderaccount.

* **Aangepaste maatstaven:** Uw eigen metriek, die u door formules tot stand te brengen leidt die op bestaande metriek (zoals de kosten per orde) worden gebaseerd.

## Beschikbaarheid van gegevens

Wanneer u rapporten genereert, kunt u kiezen hoe u conversiegegevens kunt toewijzen in een reeks gebeurtenissen die tot conversie leiden. U kunt bijvoorbeeld de volledige conversie toewijzen aan de laatste gebeurtenis of de laatste gebeurtenis meer gewicht geven dan de andere. Standaard worden conversies toegewezen aan de laatste gebeurtenis.

Afhankelijk van de attributieregel u voor het rapport specificeert, zijn de gegevens voor elk rapporttype beschikbaar voor de volgende data.

| Rapportgroep | Rapport | Data waarvoor gegevens beschikbaar zijn |
|---|---|---|
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | Vanaf 15 mei 2021.<br><br><b>Uitzondering:</b> Gegevens over prominentiemetriek zijn beschikbaar vanaf 8 september 2022. |
| | Alle andere [!UICONTROL Basic Reports] | De voorgaande 36 maanden.<br><br><b>Uitzondering:</b> Gegevens over prominentiemetriek zijn beschikbaar vanaf 8 september 2022. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | De voorgaande 45 dagen. |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | De voorafgaande twee (2) maanden plus de huidige maand. |
| [!UICONTROL Assist Reports] | Alles | De voorafgaande 18 maanden. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | Het voorgaande jaar. |
| | [!UICONTROL RSA Assets Report] | Vanaf 10 augustus 2022. |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report] | De laatste 180 dagen. |
| | Alle andere [!UICONTROL Specialty Reports] | De twee voorgaande (2) maanden. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | De voorafgaande 18 maanden. |
| [!UICONTROL Change History Report] | — | De voorafgaande 31 dagen. |

>[!MORELIKETHIS]
>
>* [Informatie over rapporten](report-about.md)
>* [Eerste instellingstaken voor rapporten](initial-setup.md)
