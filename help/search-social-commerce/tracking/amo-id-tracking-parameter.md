---
title: De trackingparameter voor AMO-id's (s_kwcid)
description: Meer informatie over de parameter tracking die wordt gebruikt om Adobe Advertising-gegevens te delen met Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '409'
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

## AMO ID-indeling voor advertenties DSP advertenties

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

waarbij:

* `AC` Hiermee wordt het weergavekanaal aangegeven.

* `{TM_AD_ID}` is de alfanumerieke ad-toets.

* `{TM_PLACEMENT_ID}` is de alfanumerieke plaatsingssleutel.

## AMO ID-indelingen voor advertenties voor zoeken, sociale media en handel

De parameters variëren per advertentienetwerk, maar de volgende parameters zijn gemeenschappelijk voor allen:

* `AL` Hiermee wordt het zoekkanaal aangegeven. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` is een unieke gebruikersnaam die aan de adverteerder is toegewezen.

* `{sid}` wordt vervangen door de numerieke id van de advertentienetwerkaccount van de adverteerder: *3* for [!DNL Google Ads], *10* for [!DNL Microsoft Advertising], *45* for [!DNL Meta], *86* for [!DNL Yahoo! Display Network], *87* for [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (afgekeurd), of *106* for [!DNL Pinterest] (vervangen).

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

Hieronder vallen ook boodschappencampagnes die [!DNL Google Merchant Center].

* Accounts die gebruikmaken van de nieuwste AMO ID-indeling, die rapportage op campagne- en groepsniveau voor maximale prestaties ondersteunt voor campagnes en concepten en experimentatiecampagnes:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alle overige rekeningen:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* Voor dynamische zoekopdrachten {keyword} wordt gevuld met het automatische doel.
>* Wanneer u tekstspatiëring genereert voor [!DNL Google] winkeladvertenties, een product-id-parameter, `{adwords_producttargetid}`, wordt ingevoegd vóór de trefwoordparameter. De parameter product-id wordt niet weergegeven in het dialoogvenster [!DNL Google Ads] parameters voor het bijhouden op accountniveau en op campagnereniveau.
>* Als u de nieuwste trackingcode voor de AMO-id wilt gebruiken, raadpleegt u &quot;[De trackingcode van de AMO-id bijwerken voor een [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

### [!DNL Microsoft Advertising]

* Zoekcampagnes:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Winkelcampagnes (gebruiken [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Campagnes van het netwerk van het publiek:

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

>[!MORELIKETHIS]
>
>* [Overzicht van [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Netwerkaccounts beheren](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Instellingen voor Baidu-campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Instellingen voor Google Ads-campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Instellingen voor Microsoft-advertentiecampagnes](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Campagne voor Japan Adds](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Instellingen voor Yandex-campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
