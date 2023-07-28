---
title: Statussen van gegevens die zijn gegenereerd uit feeds
description: Meer informatie over de status van gegevens die zijn gegenereerd op basis van de invoer van inventarisgegevens.
exl-id: 8e5e7649-a16b-4634-896a-7c216185b367
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Statussen van gegevens die zijn gegenereerd uit feeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

Elke component kan een van de volgende statussen hebben:

* *[!UICONTROL New]:* De component bestaat niet op het advertentienetwerk en werd niet gepost aan het advertentienetwerk, en u kunt nog zijn montages uitgeven indien nodig door de componentennaam te klikken. Als u klaar bent om de gegevens te posten, klikt u op **[!UICONTROL Post to SE]** en geeft u de gegevens op die moeten worden verzonden.

* *[!UICONTROL Posted]:* (Alleen campagnes en advertentiegroepen) De campagne of advertentiegroep is gedeeltelijk gepost naar het advertentienetwerk, maar sommige componenten zijn niet gepost vanwege fouten. De validatiestatus van elk trefwoord en elke advertentie toont welke informatie moet worden gecorrigeerd. U kunt de instellingen van de component desgewenst bewerken door op de naam van de component te klikken.

* *[!UICONTROL Active]:* De component is al actief op het advertentienetwerk, en u kunt zijn montages hier niet uitgeven. Actieve componenten kunnen subcomponenten bevatten die [!UICONTROL New], die kunnen worden gepost als de gegevens geldig zijn.

* *[!UICONTROL Paused]:* De component is al gepauzeerd op het advertentienetwerk, en u kunt zijn montages hier niet uitgeven. Gepauzeerde componenten kunnen subcomponenten bevatten die [!UICONTROL New], die kunnen worden gepost als de gegevens geldig zijn.

* *[!UICONTROL Deleted]:* De component is reeds geschrapt op het advertentienetwerk, en u kunt zijn montages hier niet uitgeven. Verwijderde componenten kunnen subcomponenten bevatten die [!UICONTROL New], die kunnen worden gepost als de gegevens geldig zijn.

>[!MORELIKETHIS]
>
>* [Informatie over voorraadfeeds](inventory-feeds-about.md)
>* [Gegevens weergeven die zijn gegenereerd uit feeds](propagated-data-view.md)
>* [Uit feeds gegenereerde gegevens bewerken](propagated-data-edit.md)
>* [Gegevens van de post campagne die van voer aan advertentienetwerken worden geproduceerd](propagated-data-post.md)
>* [Een publicatietaak voor de gegevens van de inventarisfeed stoppen](stop-job.md)
