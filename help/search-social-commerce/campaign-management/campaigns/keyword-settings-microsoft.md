---
title: '[!DNL Microsoft Advertising] trefwoordinstellingen'
description: Verwijs de montages voor  [!DNL Microsoft Advertising]  sleutelwoorden.
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] trefwoordinstellingen

U kunt sleutelwoorden voor campagnes tot stand brengen die het onderzoek en vertoningsnetwerken gebruiken.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** De trefwoorden, inclusief eventuele [!DNL Microsoft Advertising] overeenkomende syntaxis en plaatsaanduidingen. De maximumlengte per trefwoord is 100 tekens.

U kunt maximaal 2000 trefwoorden invoeren of plakken. Scheid meerdere trefwoorden met komma&#39;s of voer deze op aparte regels in.

>[!NOTE]
>
>* U kunt negatieve trefwoorden maken in de weergave [!UICONTROL Keywords] > [!UICONTROL Negatives] en in de instellingen voor de advertentiegroep en de campagne.
>* Als u het trefwoord [!DNL Microsoft Advertising] wijzigt, wordt het bestaande trefwoord verwijderd en wordt een nieuw trefwoord met een nieuwe id gemaakt. Als u het overeenkomsttype wijzigt, wordt het bestaande trefwoord echter niet verwijderd.

**[!UICONTROL Status]:** De vertoningsstatus van het sleutelwoord: *Actief* of *Gepauzeerd*. Het gebrek voor nieuwe sleutelwoorden is Actief **.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Plaatsaanduidingen

**[!UICONTROL Param2]:** het koord als substitutiewaarde te gebruiken als basisURL van het sleutelwoord of de titel, beschrijving, of basisURL van de advertentie [ het `{Param2}` dynamische substitutiereeks ](https://help.bingads.microsoft.com/#apex/3/en/53079/0) bevat. De maximumlengte is 70 tekens, maar houd rekening met de maximumlengte van de advertentie-elementen waarin u deze gebruikt (de combinatie van Titel 1 en Titel 2 kan bijvoorbeeld maximaal 76 tekens bevatten).

**[!UICONTROL Param3]:** het koord als substitutiewaarde te gebruiken als basisURL van het sleutelwoord of de titel, beschrijving, of basisURL van de advertentie [ het `{Param3}` dynamische substitutiereeks ](https://help.bingads.microsoft.com/#apex/3/en/53079/0) bevat. De maximumlengte is 70 tekens, maar houd rekening met de maximumlengte van de advertentie-elementen waarin u deze gebruikt (de combinatie van Titel 1 en Titel 2 kan bijvoorbeeld maximaal 76 tekens bevatten).

## URL-opties

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

In dit veld kunnen eventueel de variabelen `{Param2}` en `{Param3}` dynamic worden opgenomen.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [ beheert sleutelwoorden ](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
