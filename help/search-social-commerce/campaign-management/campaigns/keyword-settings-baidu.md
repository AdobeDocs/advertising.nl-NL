---
title: '[!DNL Baidu] trefwoordinstellingen'
description: Verwijs de montages voor  [!DNL Baidu]  sleutelwoorden.
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# [!DNL Baidu] trefwoordinstellingen

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** De sleutelwoorden. De maximumlengte per trefwoord is 30 single-byte of 15 double-byte tekens

U kunt maximaal 2000 trefwoorden invoeren of plakken. Scheid meerdere trefwoorden met komma&#39;s of voer deze op aparte regels in. Gebruik de volgende syntaxis:

* `keyword` voor brede overeenkomst
* `"keyword"` voor woordovereenkomst
* `[keyword]` voor exacte overeenkomst

>[!NOTE]
>
>* [!DNL Baidu] staat slechts één gelijke type per sleutelwoord per ad groep toe. Advertentiegroep 1 kan bijvoorbeeld niet zowel `"keyword"` als `[keyword]` bevatten.
>* U kunt negatieve trefwoorden maken in de weergave [!UICONTROL Keywords] > [!UICONTROL Negatives] en in de instellingen voor de advertentiegroep en de campagne.
>* Als u het trefwoord [!DNL Baidu] wijzigt, wordt het bestaande trefwoord verwijderd en wordt een nieuw trefwoord met een nieuwe id gemaakt. Als u het overeenkomsttype wijzigt, wordt het bestaande trefwoord echter niet verwijderd.

**[!UICONTROL Status]:** De vertoningsstatus van het sleutelwoord: *Actief* of *Gepauzeerd*. Het gebrek voor nieuwe sleutelwoorden is Actief **.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL-opties

**[!UICONTROL Base URL]:** (Campagnes with keyword-level tracking only; optional) De bestemmingspagina URL waarnaar gebruikers worden geleid wanneer zij op uw advertentie klikken. Dit kan
omleiding- en trackingcode van derden. Als u een waarde opgeeft, wordt de basis-URL voor de advertentie hierdoor genegeerd.

Nadat u de record hebt opgeslagen, bevat de basis-URL alle toevoegingsparameters die zijn geconfigureerd voor de campagne of account.

Als u de service voor het bijhouden van Adoben Advertising voor conversie gebruikt en de instellingen voor de campagne het gebruik van [!UICONTROL EF Redirect] omvatten en reeksspatiëring op trefwoordniveau toevoegt, wordt door Zoeken, Sociaal en Commerce automatisch een eigen code voor het bijhouden van klikken toegevoegd.

>[!MORELIKETHIS]
>
>* [&#x200B; beheert sleutelwoorden &#x200B;](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
