---
title: '''[!DNL Microsoft Advertising] trefwoordinstellingen'
description: Verwijs naar de instellingen voor [!DNL Microsoft Advertising] trefwoorden.
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

**[!UICONTROL Keywords]:** De trefwoorden, inclusief alle [!DNL Microsoft Advertising] overeenkomende syntaxis en plaatsaanduidingen. De maximumlengte per trefwoord is 100 tekens.

U kunt maximaal 2000 trefwoorden invoeren of plakken. Scheid meerdere trefwoorden met komma&#39;s of voer deze op aparte regels in.

>[!NOTE]
>
>* U kunt negatieve trefwoorden maken van het menu [!UICONTROL Keywords] > [!UICONTROL Negatives] en in de instellingen van de advertentiegroep en de campagne.
>* Een [!DNL Microsoft Advertising] trefwoord verwijdert het bestaande trefwoord en maakt een nieuw trefwoord met een nieuwe id. Als u het overeenkomsttype wijzigt, wordt het bestaande trefwoord echter niet verwijderd.

**[!UICONTROL Status]:** De weergavestatus van het trefwoord: *Actief* of *Gepauzeerd*. De standaardwaarde voor nieuwe trefwoorden is *Actief*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Plaatsaanduidingen

**[!UICONTROL Param2]:** De tekenreeks die als vervangende waarde moet worden gebruikt als de basis-URL van het trefwoord of de titel, beschrijving of basis-URL van de advertentie bevat [de `{Param2}` dynamische substitutiereeks](https://help.bingads.microsoft.com/#apex/3/en/53079/0). De maximumlengte is 70 tekens, maar houd rekening met de maximumlengte van de advertentie-elementen waarin u deze gebruikt (de combinatie van Titel 1 en Titel 2 kan bijvoorbeeld maximaal 76 tekens bevatten).

**[!UICONTROL Param3]:** De tekenreeks die als vervangende waarde moet worden gebruikt als de basis-URL van het trefwoord of de titel, beschrijving of basis-URL van de advertentie bevat [de `{Param3}` dynamische substitutiereeks](https://help.bingads.microsoft.com/#apex/3/en/53079/0). De maximumlengte is 70 tekens, maar houd rekening met de maximumlengte van de advertentie-elementen waarin u deze gebruikt (de combinatie van Titel 1 en Titel 2 kan bijvoorbeeld maximaal 76 tekens bevatten).

## URL-opties

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

In dit veld kan optioneel de opdracht `{Param2}` en `{Param3}` dynamische vervangingsvariabelen.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Trefwoorden beheren](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
