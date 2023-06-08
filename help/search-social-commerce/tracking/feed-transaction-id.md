---
title: Conversie bijhouden met een transactie-id-feed
description: Meer informatie over het gebruik van een feed met een transactie-id voor het bijhouden van gegevens voor conversie.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Conversie bijhouden met een transactie-id-feed

Wanneer een adverteerder zowel online als offline transacties heeft, kan Adobe Advertising de online transacties volgen via de Adobe Advertising conversion-tracking pixel. De adverteerder kan de offline transacties bijhouden met behulp van een transactie-id en ze via een feed leveren:

* Voor de online transacties houdt Adobe Advertising de kliks op uw advertenties en de resulterende transacties op uw website bij.

* De adverteerder moet offline conversies volgen en feed-bestanden op transactieniveau naar Adobe Advertising verzenden.

## Overzicht van implementatie

*Accountmanager van het Agentschap, [!DNL Adobe] alleen accountmanager en beheerdersgebruikersrollen*

1. De opties voor het bijhouden van accounts of campagnes gebruiken &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload]&quot; om automatisch een doel-URL of uiteindelijke URL te genereren voor elk trefwoord (voor reeksspatiëring) of elke advertentie (voor reeksopvolging op advertentieniveau) in de account of campagne.

1. Adobe Reclame omzettingen volgen voor de online omzettingen. Dit proces is hetzelfde als voor adverteerders met Adobe Advertising pixel-based conversion tracking. Het is belangrijk conversietags te genereren die een parameter voor een unieke transactie-id bevatten (`ev_transid=<transid>`).

1. Voor het offline gedeelte van elke transactie genereert de adverteerder dezelfde transactie-id die in het online gedeelte van de transactie werd gebruikt om in het feed-bestand op te nemen.

1. De adverteerder uploadt een bestand met de [vereiste conversiegegevens](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) naar de aangewezen serverlocatie.

1. Technical Services parseert de conversiegegevens in de geüploade bestanden en uploadt de gegevens vervolgens naar Adobe Advertising. In Advertising worden de gegevens vervolgens bijgehouden op basis van afzonderlijke trefwoorden, advertenties en plaatsingen en wordt voor elke trefwoorden een schatting van de omzet gemaakt.

1. Technische diensten valideert de verwerkte gegevens tegen de voedergegevens en controles voor om het even welk [verweesde transacties](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Bestandsvereisten voor de conversie van feed-bestanden](feed-file-requirements.md)
>* [Gegevensvereisten voor gegevensfeeds met een transactie-id](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)

