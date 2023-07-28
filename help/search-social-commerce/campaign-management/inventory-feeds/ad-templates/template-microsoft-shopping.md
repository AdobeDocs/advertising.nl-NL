---
title: '''[!DNL Microsoft® Ads] winkelen en sjablooninstellingen voor voorraadfeeds"'
description: Verwijs naar de instellingen voor [!DNL Microsoft® Ads] winkelen en sjablonen voor voorraadfeeds.
exl-id: 64d0092a-bd63-48f4-8e15-f5585f7a022a
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# [!DNL Microsoft® Ads] winkelen en sjablooninstellingen voor voorraadfeeds

Gebruik winkels en sjablonen om winkeladvertenties te configureren.

>[!NOTE]
>
>* De volgende tekens zijn gereserveerd voor het aangeven van kolomnamen en wijzigingsnamen in de sjabloon en zijn daarom niet toegestaan als tekst in alle kenmerkvelden:  `[ ] < > `


## \[Boven alle tabbladen\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Deelvenster Links\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

<!-- **[!UICONTROL Campaign Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-only.md}}

<!-- **[!UICONTROL Campaign Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-method.md}}

**[!UICONTROL Campaign Tracking Template]:** (Optioneel voor sjablonen voor clientfeed-bestanden) De sjabloon voor bijhouden op campagnereniveau, waarmee alle niet-landende domein-omleidingen en volgparameters worden opgegeven en de uiteindelijke URL wordt ingesloten in een parameter. Deze waarde overschrijft de instelling op accountniveau, maar sjablonen bijhouden op meer granulaire niveaus (met trefwoord als meest korrelige) overschrijven deze waarde.

* Voor het bijhouden van Adoben Advertising voor conversie, die wordt toegepast wanneer de instellingen voor de campagne &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; voer een van de volgende handelingen uit&quot;:

   * (Aanbevolen) Gebruik de [Sjabloonformaat volgen voor Microsoft®-winkelcampagnes](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md). Als de hele account is toegewezen aan winkeladvertenties, kunt u in plaats daarvan een trackingsjabloon op accountniveau definiëren.

   * Als u in plaats daarvan een waarde voor elk product in de feed opneemt met &quot;[!DNL bingads_redirect]&quot; kolom (met de [juiste indeling](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)), voert u vervolgens de parameter in `{lpurl}`. U kunt desgewenst omleidingen en tekstspatiëring van derden toevoegen aan de `{lpurl}` parameter.

* Voer een waarde in voor omleidingen en bijhouden door derden.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** De klant-id van de zakelijke account waarvan de producten voor de campagne worden gebruikt.

**[!UICONTROL Sales Country]:** Het land waar de producten van de campagne worden verkocht. Omdat de producten met doellanden worden geassocieerd, bepaalt dit het plaatsen welke producten in de campagne worden geadverteerd.

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Campaign Priority]:** De prioriteit waarmee de campagne wordt gebruikt wanneer de veelvoudige campagnes het zelfde product adverteren: *[!UICONTROL Low]* (standaard voor nieuwe campagnes), *[!UICONTROL Medium]*, of *[!UICONTROL High]*. Wanneer hetzelfde product in meer dan één campagne is opgenomen, gebruikt het advertentienetwerk eerst de campagneprioriteit om te bepalen welke campagne (en het bijbehorende bod) in aanmerking komt voor de advertentieveiling. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel.

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Optioneel) Een sjabloon voor reeksspatiëring op advertentieniveau, waarmee alle parameters voor het omleiden en bijhouden van domeinen worden opgegeven en de laatste URL wordt ingesloten in een parameter. Deze waarde overschrijft de instellingen op account- en campagnereniveau, maar sjablonen bijhouden op meer granulaire niveaus overschrijven deze waarde.

Voor het bijhouden van Adoben Advertising hoeft u geen waarde in te voeren. De waarde op campagnereniveau is voldoende.

Voer een waarde in voor omleidingen en bijhouden door derden.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** De standaardproductgroep met alle mogelijke productgroepen, &quot;[!UICONTROL All products].&quot; U kunt deze bovenliggende productgroep niet verwijderen, maar deze wordt automatisch verwijderd wanneer alle lagere lagen in de feed ontbreken.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Eenheden zonder onderliggende productgroepen; optioneel) De sjabloon voor bijhouden voor de productgroep, die alle omleidingen en volgparameters van een extern domein opgeeft en de laatste URL in een [!DNL ValueTrack] parameter. Deze sjabloon negeert sjablonen op hogere niveaus.

Voor het bijhouden van Adoben Advertising hoeft u geen waarde in te voeren. De waarde op campagnereniveau is voldoende.

Voer een waarde in voor omleidingen en bijhouden door derden.

**[!UICONTROL Initial Bid]:** Het eerste bod voor elke advertentie.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [Informatie over het automatiseren en beheren van voorraden](../inventory-feeds-about.md)
>* [Wijzigingstoetsen beheren](../modifiers-manage.md)
>* [Invoerbestanden voor inventarisgegevens beheren](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Doorvoergegevens doorgeven via sjablonen](../feed-data-propagate.md)
>* [Campagnegegevens van voorraadfeeds aan advertentienetwerken posten](../propagated-data-post.md)
