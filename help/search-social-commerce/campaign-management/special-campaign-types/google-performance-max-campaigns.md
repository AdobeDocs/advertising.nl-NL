---
title: Implementeren [!DNL Google Ads] maximale prestatiecampagnes
description: Meer informatie over de workflow voor het instellen van [!DNL Google Ads] maximale prestaties.
source-git-commit: 333d32963b96d2add1d99b2e27d7725341b4cfdf
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Implementeren [!DNL Google Ads] maximale prestatiecampagnes

In [!DNL Google Ads] geen opmaakcampagnes voor advertenties, advertenties of trefwoorden. In plaats daarvan geeft u binnen de instellingen voor de campagne een of meer elementgroepen op, waaronder koppen, beschrijvingen en geüploade afbeeldingen, logo&#39;s en [!DNL YouTube videos]. [!DNL Google Ads] combineert automatisch de elementen om advertenties te bedienen op basis van het kanaal (zoals [!DNL YouTube], [!DNL Gmail], of [!DNL Search]).

U kunt uw bestaande prestaties maximumcampagnes, met prestatiesgegevens in lijst en tendensen grafiekformaat bekijken, in [!DNL Campaigns] zicht; gegevens zijn niet beschikbaar op lagere niveaus. Gegevens over de prestaties op campagnereniveau zijn ook beschikbaar in rapporten en in Adobe Analytics (voor adverteerders met een [Integratie van analysemogelijkheden](/help/integrations/analytics/overview.md). Om prestatiesgegevens voor prestaties te bekijken maximumcampagnes in [!DNL Analytics]moet de campagne [bijgewerkte s_kwcid-trackingcode](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md) (voor het bijhouden van de campagne-id en de advertentie-ID).

>[!NOTE]
>
>* U moet alle afbeeldingsbestanden handmatig uploaden. Koppelingen naar [!DNL Google Merchant Center] productfeeds worden niet ondersteund.
>* Alleen de vereiste instellingen zijn beschikbaar. Meld u aan bij de [!DNL Google Ads] editor.
>* Ondersteuning voor aanbiedingsgroepen is niet beschikbaar. Meld u aan bij de [!DNL Google Ads] editor.


## Stappen die moeten worden ingesteld [!DNL Google Ads] maximale prestatiecampagnes

U kunt maximaal prestatiecampagnes afzonderlijk instellen via de [!UICONTROL Campaigns] > [!UICONTROL Campaigns] weergeven.

1. [Een campagne maken](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) met type campagne **[!UICONTROL Performance Max]**.

   Geef de [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting], en [!UICONTROL URL Options]. Optioneel invoeren [!UICONTROL Negative Keywords], enter [!UICONTROL Negative Websites]en/of de [!UICONTROL Campaign Tracking] opties.

1. Elementgroepen maken en elementen uploaden voor de campagne:

   1. Klik onder aan de instellingen voor de campagne op **[!UICONTROL Manage Asset Groups]**.

   1. Geef de instellingen voor de eerste elementgroep op en upload de afbeeldingen, logo&#39;s en optionele video&#39;s voor de elementgroep.

      Zie [beschrijvingen van de instellingen van de elementgroep](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) de eisen en specificaties te begrijpen.

   1. Voeg zo nodig extra elementgroepen toe.

1. Klik op **[!UICONTROL Post]**.

1. (Optioneel) Voeg de campagne toe aan een hybride portfolio voor optimalisatie.
