---
title: De trackingparameter voor AMO-id's (s_kwcid)
description: Meer informatie over de parameter tracking die wordt gebruikt om Adobe Advertising-gegevens te delen met Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
source-git-commit: 3c91d0a764397fd72192f5a522ac936176047bc2
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# De trackingparameter voor AMO-id&#39;s (s_kwcid)

*Adverteerders die alleen Adobe Advertising-Adobe Analytics-integratie hebben*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs" once I've finalized content for DSP clients.  -->

Adobe Advertising deelt gegevens over uw campagnes met Adobe Analytics met behulp van de AMO ID append parameter, ook wel de `s_kwcid` parameter, die bestaat uit ad-channel en ad-network-specific elementen.

De parameter wordt op een van de volgende manieren toegevoegd aan de URL&#39;s die worden gevolgd:

* (Aanbevolen) De invoegfunctie aan de serverzijde is geïmplementeerd.

   * DSP klanten: De pixelserver voegt automatisch de parameter s_kwcid aan uw het landen paginaachtervoegsels toe wanneer een eind - gebruiker een vertoningsadvertentie met de Adobe Advertising pixel bekijkt.

   * Zoek-, sociale en commerciële klanten:

      * Voor [!DNL Google Ads] en [!DNL Microsoft® Advertising] rekeningen bij de [!UICONTROL Auto Upload] Wanneer de pixelserver de voor de account of campagne ingeschakelde instelling instelt, voegt deze automatisch de parameter s_kwcid toe aan de achtervoegsels van de bestemmingspagina wanneer een eindgebruiker op een advertentie met de Adobe Advertising pixel klikt.

      * voor andere advertentienetwerken, of [!DNL Google Ads] en [!DNL Microsoft® Advertising] rekeningen bij de [!UICONTROL Auto Upload] Als u uitgeschakelde instellingen instelt, voegt u de parameter handmatig toe aan de toevoegingsparameters op accountniveau, die deze toevoegen aan de basis-URL&#39;s.

* De invoegfunctie aan de serverzijde is niet geïmplementeerd:

   * DSP klanten:

      * Voor [!DNL Flashtalking] ad-tags, voeg handmatig extra macro&#39;s in per &quot;[Toevoegen [!DNL Analytics for Advertising] Macro&#39;s naar [!DNL Flashtalking] Labels toevoegen](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * Voor [!DNL Google Campaign Manager 360] ad-tags, voeg handmatig extra macro&#39;s in per &quot;[Toevoegen [!DNL Analytics for Advertising] Macro&#39;s naar [!DNL Google Campaign Manager 360] Labels toevoegen](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

  <!--  * For all other ads, XXXX. -->

   * Zoek-, sociale en commerciële klanten:

      * Voor ([!DNL Google Ads] en [!DNL Microsoft® Advertising]), voegt u handmatig de parameter AMO ID toe aan de achtervoegsels van de bestemmingspagina.

      * Voor advertenties op alle andere advertentienetwerken voegt u handmatig de parameter AMO ID toe aan de parameters op accountniveau om deze toe te voegen aan uw basis-URL&#39;s.

Als u de invoegfunctie aan de serverzijde wilt implementeren of de beste optie voor uw bedrijf wilt bepalen, neemt u contact op met het accountteam van de Adobe.

Voor de AMO-id-indelingen voor DSP en Zoeken, Sociaal en Handel raadpleegt u &quot;[Adobe Advertising-id&#39;s gebruikt door [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id).&quot;

>[!MORELIKETHIS]
>
>* [Overzicht van [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Adobe Advertising-id&#39;s gebruikt door [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* (Zoeken, Sociaal, &amp; Handel) [Netwerkaccounts beheren](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* (Zoeken, Sociaal, &amp; Handel) [Instellingen voor Baidu-campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* (Zoeken, Sociaal, &amp; Handel) [Instellingen voor Google Ads-campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* (Zoeken, Sociaal, &amp; Handel) [Instellingen voor Microsoft® Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* (Zoeken, Sociaal, &amp; Handel) [Yahoo! Campagne voor Japan Adds](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* (Zoeken, Sociaal, &amp; Handel) [Instellingen voor Yandex-campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
