---
title: '''[!DNL Baidu] trefwoordinstellingen'
description: Verwijs naar de instellingen voor [!DNL Baidu] trefwoorden.
exl-id: 70ecb5da-1056-4d87-82ba-ac03e0c81761
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# [!DNL Baidu] trefwoordinstellingen

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** De trefwoorden. De maximumlengte per trefwoord is 30 single-byte of 15 double-byte tekens

U kunt maximaal 2000 trefwoorden invoeren of plakken. Scheid meerdere trefwoorden met komma&#39;s of voer deze op aparte regels in. Gebruik de volgende syntaxis:

* `keyword` voor brede overeenkomst
* `"keyword"` voor woordovereenkomst
* `[keyword]` voor exacte overeenkomst

>[!NOTE]
>
>* [!DNL Baidu] staat slechts één gelijke type per sleutelwoord per advertentiegroep toe. Groep 1 toevoegen kan bijvoorbeeld niet beide opnemen `"keyword"` en `[keyword]`.
>* U kunt negatieve trefwoorden maken van het menu [!UICONTROL Keywords] > [!UICONTROL Negatives] en in de instellingen van de advertentiegroep en de campagne.
>* Een [!DNL Baidu] trefwoord verwijdert het bestaande trefwoord en maakt een nieuw trefwoord met een nieuwe id. Als u het overeenkomsttype wijzigt, wordt het bestaande trefwoord echter niet verwijderd.

**[!UICONTROL Status]:** De weergavestatus van het trefwoord: *Actief* of *Gepauzeerd*. De standaardwaarde voor nieuwe trefwoorden is *Actief*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL-opties

**[!UICONTROL Base URL]:** (Campagnes with keyword-level tracking only; optional) De bestemmingspagina URL waarnaar gebruikers worden geleid wanneer ze op uw advertentie klikken. Het kan herrichtings- en volgcode van derden bevatten. Als u een waarde opgeeft, wordt de basis-URL voor de advertentie hierdoor genegeerd.

Nadat u de record hebt opgeslagen, bevat de basis-URL alle toevoegingsparameters die zijn geconfigureerd voor de campagne of account.

Als u de service voor het bijhouden van de conversie van de Adobe Advertising gebruikt en de instellingen voor de campagne ook het gebruik van de functie [!UICONTROL EF Redirect] en het toevoegen van het volgen op het sleutelwoordniveau, dan voegt het Onderzoek, Sociale, &amp; Handel automatisch zijn eigen klik-volgende code toe.

>[!MORELIKETHIS]
>
>* [Trefwoorden beheren](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
