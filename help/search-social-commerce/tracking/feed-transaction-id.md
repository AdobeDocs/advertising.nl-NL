---
title: Conversie bijhouden met een transactie-id-feed
description: Meer informatie over het gebruik van een feed met een transactie-id voor het bijhouden van gegevens voor conversie.
exl-id: 58f231a6-970b-46b4-824b-67b3d3f83051
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Conversie bijhouden met een transactie-id-feed

Wanneer een adverteerder zowel online als offline transacties heeft, kan de Adobe Advertising de online transacties volgen via de Adobe Advertising conversie-volgende pixel, en de adverteerder kan de offlinetransacties volgen gebruikend een transactie-identiteitskaart en hen leveren via een voer:

* Voor de online transacties houdt de Adobe Advertising de muisklikken op uw advertenties en de resulterende transacties op uw website bij.

* De adverteerder moet offline conversies volgen en feed-bestanden op transactieniveau naar Adobe Advertising verzenden.

## Overzicht van implementatie

*Accountmanager van het Agentschap, [!DNL Adobe] alleen accountmanager en beheerdersgebruikersrollen*

1. De opties voor het bijhouden van accounts of campagnes gebruiken &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload]&quot; om automatisch een doel-URL of uiteindelijke URL te genereren voor elk trefwoord (voor reeksspatiëring) of elke advertentie (voor reeksopvolging op advertentieniveau) in de account of campagne.

1. De omzetcontrole van de Adobe Advertising van de opstelling voor de online omzettingen. Dit proces is hetzelfde als voor adverteerders met Adobe Advertising pixelgebaseerde conversie. Het is belangrijk conversietags te genereren die een parameter voor een unieke transactie-id bevatten (`ev_transid=<transid>`).

1. Voor het offline gedeelte van elke transactie genereert de adverteerder dezelfde transactie-id die in het online gedeelte van de transactie werd gebruikt om in het feed-bestand op te nemen.

1. De adverteerder uploadt een bestand met de [vereiste conversiegegevens](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) naar de aangewezen serverlocatie.

1. Technical Services parseert de conversiegegevens in de geüploade bestanden en uploadt de gegevens vervolgens naar Adobe Advertising. De Adobe Advertising volgt de gegevens dan tegen individuele sleutelwoorden, advertenties, en plaatsingen en leidt tot opbrengst het voorspellen voor elk.

1. Technische diensten valideert de verwerkte gegevens aan de voedergegevens en controles voor om het even welk [verweesde transacties](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Bestandsvereisten voor de conversie van feed-bestanden](feed-file-requirements.md)
>* [Gegevensvereisten voor gegevensfeeds met een transactie-id](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
