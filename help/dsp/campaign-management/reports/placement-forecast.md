---
title: Het rapport Placement Forecast weergeven
description: Bekijk het aantal indrukkingen, uitgaven en het optimale maximumbod dat is voorspeld voor een bepaalde doelstrategie voor een plaatsing.
feature: DSP Placements
exl-id: 6ff228b2-b656-493e-a299-98c7a68a0f51
source-git-commit: e901087b9128779bb4d55194cebfdc84c7c2ba2a
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Het rapport Placement Forecast weergeven

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

Het hulpmiddel van de Plaatsingsvoorspelling toont het voorspelde aantal indrukken, uitgaven, en optimale maximumbod voor een bepaalde het richten strategie. De prognose wordt berekend op basis van de totale inventaris die beschikbaar is met de plaatsing en de unieke gebruikers die beschikbaar zijn.

>[!NOTE]
>
>* Postcodes worden niet meegenomen in de voorspelde plaatsingsberekeningen.
>* Er wordt geen prognose gegenereerd voor stages waarvoor alleen programmatic Guarantee (PG) geldt, omdat beschikbaarheid en uitgaven bepalend zijn.

## Informatie in de prognose

De prognose bevat de volgende informatie:

* **[!UICONTROL Summary]:**

   * **[!UICONTROL Estimated CPM]:** De geschatte kosten per duizend indrukken (eCPM) die de het richten montages kunnen verwachten te bereiken.

   * **[!UICONTROL Budget]:** Het geschatte budget voor de doelinstellingen.

   * **[!UICONTROL Impression]:** Het geschatte aantal afbeeldingen voor de doelinstellingen.

* **[!UICONTROL Budget Yield Curve]:** Het geschatte aantal indrukken die de plaatsing op verschillende begrotingsniveaus kan leveren als alle andere het richten montages het zelfde zijn.

* **[!UICONTROL Max Bid Yield Curve]:** De geschatte uitgave voor de plaatsing op verschillende Max. biedniveaus, wanneer alle andere het richten montages het zelfde zijn.

* **[!UICONTROL Message]:** Verstrekt informatie over de voorspelde output, met inbegrip van om het even welke scenario&#39;s waarin de voorspelling niet kon worden geproduceerd. Ook worden de instellingen voor het opgeven van doelen gemarkeerd die in dat scenario zijn herzien, maar die in dat scenario niet in overweging zijn genomen vanwege een gebrek aan gegevens.

### Begrotingsberekening

* Voor plaatsen die niet aan een pakket worden toegewezen, wordt het plaatsingsbudget gebruikt voor berekeningen. Binnen een vlucht wordt hetzelfde totale budget berekend.

* Voor plaatsingen binnen een pakket wordt het budget dat aan de plaatsing wordt toegewezen, gebruikt voor berekeningen. Tijdens de vlucht wordt het aan de plaatsing toegewezen budget berekend en in het bericht opgenomen.

* Voor stages die aan een vluchtpakket worden toegevoegd, wordt de begroting gelijkelijk verdeeld op basis van het aantal stages. Wanneer de plaatsing live gaat, wordt het door het pakket toegewezen budget berekend.

## Vereisten

* Minimale uitgaven: $25 per dag of equivalent in lokale valuta per plaatsing.

* Maximale uitgaven: $15.000 per dag of het equivalent in lokale valuta per plaatsing.

* Minimumbod, Maximum maximumbod: er is een minimum maximumbod (voor de curve van de begrotingsopbrengst) en maximum maximumbod (voor de curve van het maximumbod) per plaatsingstype. Deze waarden gelden wereldwijd en houden geen rekening met regionale verschillen. Soms zijn deze waarden te hoog of te laag voor het doelgebied.

* Historische gegevens: de plaatsingsprognose is beschikbaar wanneer voldoende historische gegevens beschikbaar zijn. Hieronder volgen voorbeelden van gevallen waarin onvoldoende historische gegevens beschikbaar kunnen zijn:

   * De plaatsing richt een nieuwe regio voor de campagne.

   * De plaatsing richt een nieuwe inventarisovereenkomst voor de campagne.

   * De plaatsing gebruikt een nieuw advertentietype voor de campagne.

     Een plaatsing is gewoonlijk een inzameling van veelvoudige advertentiesjablonen zoals die door levering-zijplatforms worden bepaald. Dus zelfs als de plaatsing al lange tijd bestaat, kan de onderliggende advertentiesjabloon nieuw zijn, en het voorspellingsinstrument zal niet kunnen voorspellen.

## Het rapport Placement Forecast openen

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

1. Klik op de naam van de campagne en klik vervolgens op **[!UICONTROL Placements]**.

1. Klik naast de plaatsingsnaam op  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Zoek de **[!UICONTROL Forecast]** rechtsboven. Klik indien nodig op ![Voorspelling](/help/dsp/assets/placement-forecast.png).

   >[!NOTE]
   >
   >* Soms is de voorspelling niet beschikbaar vanwege de cache van de browser. Als dit gebeurt, wist u de cache en probeert u het opnieuw.

>[!MORELIKETHIS]
>
>* [Typen prestatierapporten in Campaign Management-weergaven](campaign-reports-about.md)
>* [De Placement Diagnostic Reports weergeven](/help/dsp/campaign-management/reports/placement-diagnostics.md)
>* [Plaatsingsinstellingen](/help/dsp/campaign-management/placements/placement-settings.md)
