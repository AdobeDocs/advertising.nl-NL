---
title: Adobe Advertising-cijfers en -afmetingen in Customer Journey Analytics
description: Verwijs naar de metriek en de afmetingen van Adobe Advertising die in Customer Journey Analytics beschikbaar zijn.
feature: Integration with Adobe Customer Journey Analytics
exl-id: 97c89e03-ab15-4906-96fc-6bb77ea0cd7c
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# Adobe Advertising-cijfers en -afmetingen in Customer Journey Analytics

*Advertisers met slechts een integratie Adobe Advertising-Customer Journey Analytics*

*eigenschap van Beta*

Adobe Advertising geeft verkeersmaatstaven en -afmetingen door aan [!DNL Customer Journey Analytics] per dag. Met [!DNL Web SDK] worden doorklikbewerkingen en doorzoekacties van Adobe Advertising in real-time vastgelegd en doorgegeven aan Customer Journey Analytics.

## Adobe Advertising-verkeerscijfers

<!-- Verify column names -->

In de volgende tabel:

* &quot;XDM Field Name&quot; is de veldnaam in Adobe Experience Platform.

* &quot;Weergavenaam XDM-veld&quot; geeft de weergavenaam aan in Customer Journey Analytics.

| Adobe Advertising-veldnaam | XDM-veldnaam | Weergavenaam XDM-veld | Source |
|------------------------------|----------------|------------------------|--------|
| Datum | Datum | Alles | |
| AMO-id | skwcid | Adobe Advertising-id | Alles |
| AMO-indrukkingen | adobe_advertences | Adobe Advertising-impressies | Alles |
| AMO-klikken | adobe_advertenties_clicks | Adobe Advertising Kliks | Alles |
| AMO-kosten | adobe_advertence_cost | Adobe Advertising Kosten | Alles |
| Valuta | valuta | Valuta | Alles |
| AMO-weergaven | adobe_advertence_views | Adobe Advertising Views | Ad Cloud DSP |
| AMO Views 25% voltooid | adobe_advertence_views_25_pct | Adobe Advertising Views 25% voltooid | Ad Cloud DSP |
| AMO Views 50% voltooid | adobe_advertence_views_50_pct | Adobe Advertising Views 50% voltooid | Ad Cloud DSP |
| AMO Views 75% voltooid | adobe_advertence_views_75_pct | Adobe Advertising Views 75% voltooid | Ad Cloud DSP |
| AMO Views 100% voltooid | adobe_advertence_views_100_pct | Adobe Advertising Views 100% voltooid | Ad Cloud DSP |
| AMO-minuten weergegeven | adobe_advertence_minutes_displayed | Adobe Advertising-minuten weergegeven | Ad Cloud DSP |
| AMO-weergaven | adobe_advertable_impressions | Adobe Advertising Viewable Impressions | Ad Cloud DSP |
| AMO: geen zichtbare indrukken | adobe_advertence_not_viewable_impressions | Adobe Advertising, geen zichtbare indrukken | Ad Cloud DSP |
| AMO meetbare indrukkingen | adobe_advertence_meetbaar_impressions | Metbare Adobe Advertising-indrukkingen | Ad Cloud DSP |

<!--
| Adobe Advertising Landing Page Views | adobe_advertising_landing_page_views | Adobe Advertising Landing Page Views | Meta Only |
| Adobe Advertising App Events | adobe_advertising_app_events | Adobe Advertising App Events | Meta Only |
| Adobe Advertising Engagements | adobe_advertising_engagements | Adobe Advertising Engagements | Meta Only |
| Adobe Advertising Ad Platform Conversions | adobe_advertising_ad_platform_conversions | Adobe Advertising Ad Platform Conversions | Meta Only |
| Adobe Advertising App Installs | adobe_advertising_app_installs | Adobe Advertising App Installs | Meta Only |
| Adobe Advertising Ad Platform Conversion Value | adobe_advertising_ad_platform_conversion_value | Adobe Advertising Ad Platform Conversion Value | Meta Only |
| Adobe Advertising Ad Platform Leads | adobe_advertising_ad_platform_leads | Adobe Advertising Ad Platform Leads | Meta Only |
| Adobe Advertising Page Like | adobe_advertising_page_like | Adobe Advertising Page Like | Meta Only |
| Adobe Advertising Phone Calls | adobe_advertising_phone_calls | Adobe Advertising Phone Calls | Meta Only |
| Adobe Advertising Messages | adobe_advertising_messages | Adobe Advertising Messages | Meta Only |
-->

## Adobe Advertising-afmetingen

In de volgende tabel:

* &quot;XDM Field Name&quot; is de veldnaam in Adobe Experience Platform.

* &quot;Weergavenaam XDM-veld&quot; geeft de weergavenaam aan in Customer Journey Analytics.

| Adobe Advertising-veldnaam | XDM-veldnaam | Weergavenaam XDM-veld | Source |
|------------------------------|----------------|------------------------|--------|
| Sleutel | skwcid | Adobe Advertising-id |  |
| Advertentieplatform | adobe_advertence_ad_platform | Adobe Advertising Ad Platform |  |
| Account | adobe_advertence_account | Adobe Advertising-account |  |
| Campagne | adobe_advertence_campagne | Adobe Advertising-campagne |  |
| Advertentiegroep | adobe_advertence_ad_group | Adobe Advertising Advertentiegroep |  |
| Trefwoord | adobe_advertence_keyword | Adobe Advertising-trefwoord |  |
| Advertentie | adobe_advertence_ad | Adobe Advertising Ad |  |
| Plaatsing | adobe_advertence_placement | Adobe Advertising-plaatsing |  |
| Type afstemmen | adobe_advertence_match_type | Type Adobe Advertising-overeenkomst |  |
| Titel van advertentie | adobe_advertence_ad_title | Adobe Advertising Advertentie Titel |  |
| Advertentiebeschrijving | adobe_advertence_ad_description | Adobe Advertising - advertentiebeschrijving |  |
| Doel-URL toevoegen | adobe_advertence_ad_destination_url | URL Adobe Advertising-advertentie |  |
| URL voor advertentie | adobe_advertence_ad_display_url | URL Adobe Advertising AdDisplay |  |
| Apparaat | adobe_advertence_device | Adobe Advertising-apparaat |  |
| Trefwoord MatchType | adobe_advertence_keyword_matchtype | Adobe Advertising-trefwoordmatchtype |  |
| Netwerk | adobe_advertence_network | Adobe Advertising Network |  |
| Advertentietype | adobe_advertence_ad_type | Adobe Advertising Advertentietype |  |
| Productdoel | adobe_advertence_product_target | Adobe Advertising-productdoel |  |
| Landingstype | adobe_advertence_landing_type | Adobe Advertising-landingstype |  |
| Optimalisatie | adobe_advertence_optimization | Adobe Advertising optimaliseren |  |

>[!MORELIKETHIS]
>
>* [&#x200B; Overzicht &#x200B;](overview.md)
>* [&#x200B; Eerste vereisten &#x200B;](prerequisites.md)
>* [&#x200B; Adobe Advertising IDs die door  [!DNL Customer Journey Analytics]](ids.md) wordt gebruikt
>* [&#x200B; de inzameling van opstellingsgegevens, gegevensoverdracht, en het melden &#x200B;](set-up.md)
