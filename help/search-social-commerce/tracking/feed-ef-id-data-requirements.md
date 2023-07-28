---
title: Gegevensvereisten voor gegevensfeeds die gebruikmaken van EF-id's
description: Verwijs naar de gegevensvereisten voor gegevensfeeds die gebruikmaken van EF-id's.
exl-id: 15e76f3a-c376-4e7b-b3c8-ca76fd427002
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Gegevensvereisten voor gegevensfeeds die gebruikmaken van EF-id&#39;s

Hieronder vindt u de koptekstvelden en de bijbehorende gegevensvelden die zijn vereist voor elk type feed-bestand.

>[!NOTE]
>* De kopballen kunnen in om het even welke orde zijn zolang de gegevens in de verdere rijen de zelfde orde volgen. Als u geen kopbal omvat, dan moet de orde van de gegevensrijen met elk inputdossier verenigbaar zijn.
>* Elke regel van het voederbestand moet gegevens voor één transactie bevatten en de transactie moet worden geïdentificeerd door een door de Adobe Advertising gegenereerde ef_id (token).

| Koptekstveld/kolomnaam | Type | Beschrijving |
| ---- | ---- | ---- |
| EF-id | Hoofdlettergevoelige tekenreeks | De ef_id (teken) die u op de klik voor de transactie vaststelde, die uit afleveridentiteitskaart, de kliktijd, en het netwerktype bestaat. Wijzig de waarde niet. |
| Transactie-id | Hoofdlettergevoelige tekenreeks | (Optioneel, maar aanbevolen) De door de adverteerder gegenereerde transactie-id. De beste praktijken moeten dit voor elke transactie omvatten alhoewel ef_id wordt gebruikt om de transactie op het tijdstip van omleiding te volgen. |
| Transactiedatum | DateTime | De datum van de transactie. De indeling moet consistent zijn voor elke transactie. |
| Clientspecifieke conversie | String | Een conversie die wordt bijgehouden (zoals het transactietype of het bedrag). Bespreek de omzettingen die met het de implementatieteam van de Adobe Advertising moeten worden omvat alvorens het voer te beginnen. |

## Voorbeeld

Het volgende voorbeeldbestand bevat gegevens voor twee transactie-eigenschappen (Product en Opbrengst).

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Bestandsvereisten voor de conversie van feed-bestanden](feed-file-requirements.md)
>* [Conversie bijhouden met een EF-id-feed](/help/search-social-commerce/tracking/feed-efid.md)
