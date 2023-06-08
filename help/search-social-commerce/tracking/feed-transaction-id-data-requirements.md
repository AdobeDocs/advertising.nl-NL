---
title: Gegevensvereisten voor gegevensfeeds met een transactie-id
description: Verwijs naar de gegevensvereisten voor gegevensvoer gebruikend een transactie ID.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Gegevensvereisten voor gegevensfeeds met een transactie-id

Hieronder vindt u de koptekstvelden en de bijbehorende gegevensvelden die zijn vereist voor elk type feed-bestand.

>[!NOTE]
>* De kopballen kunnen in om het even welke orde zijn zolang de gegevens in de verdere rijen de zelfde orde volgen. Als u geen kopbal omvat, dan moet de orde van de gegevensrijen met elk inputdossier verenigbaar zijn.
>* Elke regel van het feed-bestand moet gegevens voor één transactie bevatten en de transactie moet door een transactie-id worden geïdentificeerd.


| Koptekstveld/kolomnaam | Type | Beschrijving |
| ---- | ---- | ---- |
| Transactie-id (ev_transid) | Hoofdlettergevoelige tekenreeks | De door de adverteerder gegenereerde id die aan de transactie is gekoppeld. Omdat de conversie-tracking-tag voor Adobe-advertenties wordt gebruikt voor de onlinegedeelten van de transactie, moet deze dezelfde zijn als de transactie-id (ev_transid) die Adobe-advertentie voor het eerdere gedeelte van de transactie heeft opgegeven. Dit betekent dat de conversietag voor het online gedeelte van de transactie een bezit voor een unieke transactie-identiteitskaart moet omvatten.<br><br>**Opmerking:** In advertentie van Adobe wordt de id gebruikt om de oude transactiegegevens te zoeken en bij te werken volgens een modus voor het invoegen van de gegevens (bijvoorbeeld om de bestaande gegevens te vervangen of om deze aan te vullen met de nieuwe gegevens). |
| Transactiedatum | DateTime | De datum van de transactie. De indeling moet consistent zijn voor elke transactie. |
| Clientspecifieke conversie | String | Een conversie die wordt bijgehouden (zoals het transactietype of het bedrag). Bespreek de conversies die u wilt opnemen bij het Adobe Advertising-implementatieteam voordat u de feed start. |

## Voorbeeld

Het volgende voorbeeldbestand bevat gegevens voor twee transactie-eigenschappen (Product en Opbrengst).

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

