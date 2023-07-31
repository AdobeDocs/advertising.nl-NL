---
title: Gegevensvereisten voor gegevensfeeds met een transactie-id
description: Verwijs naar de gegevensvereisten voor gegevensvoer gebruikend een transactie ID.
exl-id: 67e1cadd-b607-465c-9db6-ca76d8ca84c5
feature: Search Tracking
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Gegevensvereisten voor gegevensfeeds met een transactie-id

Hieronder vindt u de koptekstvelden en de bijbehorende gegevensvelden die zijn vereist voor elk type feed-bestand.

>[!NOTE]
>* De kopballen kunnen in om het even welke orde zijn zolang de gegevens in de verdere rijen de zelfde orde volgen. Als u geen kopbal omvat, dan moet de orde van de gegevensrijen met elk inputdossier verenigbaar zijn.
>* Elke regel van het feed-bestand moet gegevens voor één transactie bevatten en de transactie moet door een transactie-id worden geïdentificeerd.

| Koptekstveld/kolomnaam | Type | Beschrijving |
| ---- | ---- | ---- |
| Transactie-id (ev_transid) | Hoofdlettergevoelige tekenreeks | De door de adverteerder gegenereerde id die aan de transactie is gekoppeld. Omdat de conversie-volgende markering van de Adobe Advertising voor de online gedeelten van de transactie wordt gebruikt, moet dit het zelfde als transactie identiteitskaart (ev_transid) zijn die Adobe Advertising voor het vroegere deel van de transactie verstrekte. Dit betekent dat de omzettingsmarkering voor het online gedeelte van de transactie omzettings metrisch voor een unieke transactie-identiteitskaart moet omvatten.<br><br>**Opmerking:** De Adobe Advertising gebruikt identiteitskaart om van de oude transactiegegevens de plaats te bepalen en het bij te werken volgens een overeengekomen-op toevoegingswijze (bijvoorbeeld, om de bestaande gegevens te vervangen of het met de nieuwe gegevens te verhogen). |
| Transactiedatum | DateTime | De datum van de transactie. De indeling moet consistent zijn voor elke transactie. |
| Clientspecifieke conversie | String | Een conversie die wordt bijgehouden (zoals het transactietype of het bedrag). Bespreek de omzettingen die met het de implementatieteam van de Adobe Advertising moeten worden omvat alvorens het voer te beginnen. |

## Voorbeeld

Het volgende voorbeeldbestand bevat gegevens voor twee conversiemetriek (Product en Opbrengst).

```
Transaction ID,Transaction Date,Product,Revenue
12345,2010-02-17,Coffee,15.00
12346,2010-02-17,Tea,42.00
12347,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Bestandsvereisten voor de conversie van feed-bestanden](feed-file-requirements.md)
>* [Conversie bijhouden met een transactie-id-feed](/help/search-social-commerce/tracking/feed-transaction-id.md)
