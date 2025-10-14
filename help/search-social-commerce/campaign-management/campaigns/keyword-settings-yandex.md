---
title: '[!DNL Yandex] trefwoordinstellingen'
description: Verwijs de montages voor  [!DNL Yandex]  sleutelwoorden.
exl-id: 973be0df-9b3c-4f33-b48b-ef1db4ab35da
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# [!DNL Yandex] trefwoordinstellingen

Yandex-trefwoorden worden gebruikt voor zoeknetwerken en weergavenetwerken (content).

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** de sleutelwoorduitdrukkingen, met inbegrip van om het even welke [&#x200B; yandex typesyntaxis &#x200B;](https://yandex.com/support/direct/keywords/symbols-and-operators.html) voor sleutelwoorden. Elk trefwoord mag maximaal zeven woorden bevatten, met uitzondering van stopwoorden.

U kunt maximaal 2000 trefwoorden invoeren of plakken. Scheid meerdere trefwoorden met komma&#39;s of voer deze op aparte regels in.

>[!NOTE]
>
>* Als u het trefwoord [!DNL Yandex] of het type overeenkomst wijzigt, wordt het bestaande trefwoord verwijderd en wordt een nieuw trefwoord gemaakt.
>* Elke Yandex en groep kan maximaal 200 trefwoorden bevatten.

**[!UICONTROL Status]:** De vertoningsstatus van het sleutelwoord: *Actief* of *Gepauzeerd*. Het gebrek voor nieuwe sleutelwoorden is Actief **.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Plaatsaanduidingen

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** De waarde van de vervangingsvariabelen `{param1}` en `{param2}` , die instanties van {param1} en {param2} in de basis-URL voor advertenties en sitelinks vervangen wanneer het trefwoord wordt gebruikt om de advertentie weer te geven. De maximumlengte is 255 bytes.

Speciale tekens worden automatisch gecodeerd in UTF-8. Als de gekoppelde advertentie bijvoorbeeld een basis-URL heeft van &quot;http://www.example.com/{param1} en de waarde op trefwoordniveau van {param1} &quot;shoes/flats.html&quot; is, wordt de advertentie verzonden naar http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [&#x200B; beheert sleutelwoorden &#x200B;](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
