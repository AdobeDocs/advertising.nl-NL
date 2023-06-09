---
title: De parameter s_kwcid tracking
description: Meer informatie over de parameter tracking die wordt gebruikt om Adobe Advertising-gegevens te delen met Adobe Analytics.
source-git-commit: a9e23de134274d8f5004a908853c4132300b84e8
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# De parameter s_kwcid tracking

*Adverteerders met alleen Adobe Advertising-Adobe Analytics-integratie*

<!-- Where should this go? It probably belongs in the Analytics integration chapter, but I'll need to fit it in/create context around it/explain more about implementation and how this works.  SPECIFICALLY, I'll need to update the second section that explains when/where to add the code for DSP clients. -->

Adobe Advertising deelt gegevens over je campagnes met Adobe Analytics via `s_kwcid` voeg parameter toe, die uit ad-channel en ad-network-specific elementen bestaat. De parameter wordt op een van de volgende manieren toegevoegd aan de URL&#39;s die worden gevolgd:

* (Aanbevolen)<!--; the only option for Advertising DSP-->) De functie s_kwcid aan de serverzijde is geïmplementeerd.

  Voor [!DNL Google Ads] en [!DNL Microsoft Advertising] rekeningen bij de [!UICONTROL Auto Upload] de pixelserver die voor de account of campagne is ingeschakeld, voegt de parameter s_kwcid automatisch toe aan de achtervoegsels van de bestemmingspagina wanneer een eindgebruiker op een advertentie klikt <!-- click a search ad or views a display ad --> met de Adobe Advertising pixel.

  voor andere advertentienetwerken, of [!DNL Google Ads] en [!DNL Microsoft Advertising] rekeningen bij de [!UICONTROL Auto Upload] Als u uitgeschakelde instellingen instelt, voegt u de parameter handmatig toe aan de toevoegingsparameters op accountniveau, die u vervolgens toevoegt aan de basis-URL&#39;s.

* <!-- (Search, Social, & Commerce only) -->De server-kant s_kwcid eigenschap wordt niet uitgevoerd, en u moet de s_kwcid parameter aan uw manueel toevoegen ([!DNL Google Ads] en [!DNL Microsoft Advertising]) het landen pagina achtervoegsels of (andere ad netwerken) rekening-vlakke toevoegingsparameters.

Om de server-kant s_kwcid eigenschap uit te voeren, of de beste optie voor uw zaken te bepalen, spreek met uw Team van de Rekening van Adobe.

## s_kwcid-indeling voor advertenties DSP advertenties

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

waarbij:

* `AC` Hiermee wordt het weergavekanaal aangegeven.

* `{TM_AD_ID}` is de alfanumerieke ad-toets.

* `{TM_PLACEMENT_ID}` is de alfanumerieke plaatsingssleutel.

## s_kwcid-indelingen voor advertenties voor zoeken, sociale media en handel

De parameters variëren per advertentienetwerk, maar de volgende parameters zijn gemeenschappelijk voor allen:

* `AL` Hiermee wordt het zoekkanaal aangegeven. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` is een unieke gebruikersnaam die aan de adverteerder is toegewezen.

* `{sid}` wordt vervangen door de numerieke id van de advertentienetwerkaccount van de adverteerder: *3* for [!DNL Google Ads], *10* for [!DNL Microsoft Advertising], *45* for [!DNL Meta], *86* for [!DNL Yahoo! Display Network], *87* for [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (afgekeurd), of *106* for [!DNL Pinterest] (afgekeurd).

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

Hieronder vallen ook boodschappencampagnes die [!DNL Google Merchant Center].

* Rekeningen die het recentste s_kwcid formaat gebruiken, dat campagne- en ad groep-vlakke rapportering voor prestaties maximumcampagnes en concepten en experimentatiecampagnes steunt:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alle overige rekeningen:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* Voor dynamische zoekopdrachten {keyword} wordt gevuld met het automatische doel.
>* Wanneer u tekstspatiëring genereert voor [!DNL Google] winkeladvertenties, een product-id-parameter, `{adwords_producttargetid}`, wordt ingevoegd vóór de trefwoordparameter. De parameter product-id wordt niet weergegeven in het dialoogvenster [!DNL Google Ads] parameters voor het bijhouden op accountniveau en op campagnereniveau.
>* Ga naar &quot;[De s_kwcid-trackingcode bijwerken voor een [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-skwcid-google.md).&quot;

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
