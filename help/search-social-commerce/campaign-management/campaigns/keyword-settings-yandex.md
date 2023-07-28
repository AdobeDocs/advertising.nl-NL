---
title: '''[!DNL Yandex] trefwoordinstellingen'
description: Verwijs naar de instellingen voor [!DNL Yandex] trefwoorden.
exl-id: 276f991b-f604-445c-8dd0-481b6eaee3d2
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# [!DNL Yandex] trefwoordinstellingen

Yandex-trefwoorden worden gebruikt voor zoeknetwerken en weergavenetwerken (content).

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** De trefwoordzinnen, inclusief alle [Yandex, type syntaxis](https://yandex.com/support/direct/keywords/symbols-and-operators.html) voor trefwoorden. Elk trefwoord mag maximaal zeven woorden bevatten, met uitzondering van stopwoorden.

U kunt maximaal 2000 trefwoorden invoeren of plakken. Scheid meerdere trefwoorden met komma&#39;s of voer deze op aparte regels in.

>[!NOTE]
>
>* Een [!DNL Yandex] het bestaande trefwoord of het overeenkomende type wordt verwijderd en er wordt een nieuw trefwoord gemaakt.
>* Elke Yandex en groep kan maximaal 200 trefwoorden bevatten.

**[!UICONTROL Status]:** De weergavestatus van het trefwoord: *Actief* of *Gepauzeerd*. De standaardwaarde voor nieuwe trefwoorden is *Actief*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Plaatsaanduidingen

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** De waarde van `{param1}` en `{param2}` vervangende variabelen, die in de plaats komen van {param1} en {param2} in de basis-URL voor advertenties en sitelinks wanneer het trefwoord wordt gebruikt om de advertentie weer te geven. De maximumlengte is 255 bytes.

Speciale tekens worden automatisch gecodeerd in UTF-8. Als de gekoppelde advertentie bijvoorbeeld een basis-URL heeft van &quot;http://www.example.com/{param1} en de waarde op trefwoordniveau van {param1} is &quot;shoes/flats.html&quot;, dan leidt de advertentie naar http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Trefwoorden beheren](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
