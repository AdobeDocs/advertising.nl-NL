---
title: De trackingparameter voor AMO-id's (s_kwcid)
description: Meer informatie over de parameter tracking die wordt gebruikt om Adobe Advertising-gegevens te delen met Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: a150a55fd8d97db83cc269c787a1c67d557b7e3a
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# De trackingparameter voor AMO-id&#39;s (s_kwcid)

*Adverteerders die alleen Adobe Advertising-Adobe Analytics-integratie hebben*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs."  But I'll need to update with when/where to add the code for DSP clients. -->

Adobe Advertising deelt gegevens over uw campagnes met Adobe Analytics met behulp van de AMO ID append parameter, ook wel de `s_kwcid` parameter, die bestaat uit ad-channel en ad-network-specific elementen.

<!-- add everything below to IDs page -->

De parameter wordt op een van de volgende manieren toegevoegd aan de URL&#39;s die worden gevolgd:

* (Aanbevolen) De invoegfunctie aan de serverzijde is geïmplementeerd.

  Voor [!DNL Google Ads] en [!DNL Microsoft Advertising] rekeningen bij de [!UICONTROL Auto Upload] de pixelserver die is ingeschakeld voor de account of campagne, voegt de parameter AMO ID automatisch toe aan de achtervoegsels van de bestemmingspagina wanneer een eindgebruiker op een advertentie klikt. <!-- click a search ad or views a display ad --> met de Adobe Advertising pixel.

  voor andere advertentienetwerken, of [!DNL Google Ads] en [!DNL Microsoft Advertising] rekeningen bij de [!UICONTROL Auto Upload] Als u de uitgeschakelde instelling instelt, voegt u de parameter AMO ID handmatig toe aan de toevoegingsparameters op accountniveau, die u vervolgens toevoegt aan de basis-URL&#39;s.

* <!-- (Search, Social, & Commerce only) -->De invoegfunctie aan de serverzijde is niet geïmplementeerd en u moet de parameter AMO ID handmatig aan uw ([!DNL Google Ads] en [!DNL Microsoft Advertising]) het landen pagina achtervoegsels of (andere ad netwerken) rekening-vlakke toevoegingsparameters.

Als u de invoegfunctie aan de serverzijde wilt implementeren of de beste optie voor uw bedrijf wilt bepalen, neemt u contact op met het accountteam van Adobe.

Voor de AMO-id-indelingen voor DSP en Zoeken, Sociaal en Handel raadpleegt u &quot;[Adobe Advertising-id&#39;s gebruikt door [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Overzicht van [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Adobe Advertising-id&#39;s gebruikt door [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* [Netwerkaccounts beheren](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Instellingen voor Baidu-campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Instellingen voor Google Ads-campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Instellingen voor Microsoft-advertentiecampagnes](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Campagne voor Japan Adds](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Instellingen voor Yandex-campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
