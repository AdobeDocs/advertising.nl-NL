---
title: "[!DNL Google Ads] winkelen en sjablooninstellingen voor voorraadfeeds"
description: Verwijs naar de instellingen voor [!DNL Google Ads] winkelen en sjablonen voor voorraadfeeds.
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# [!DNL Google Ads] winkelen en sjablooninstellingen voor voorraadfeeds

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

Voor het bijhouden van reclame-conversies voor Adobe, die wordt toegepast wanneer de instellingen voor de campagne &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; gebruikt u de [Sjabloonformaat voor winkelen in Google Ads volgen](/help/search-social-commerce/tracking/formats-click-tracking-google.md). Als de hele account is toegewezen aan winkeladvertenties, kunt u in plaats daarvan een trackingsjabloon op accountniveau definiëren.

Voer een waarde in voor omleidingen en bijhouden door derden.

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

**[!UICONTROL Networks]:** De netwerken waarop advertenties moeten worden geplaatst. *[!UICONTROL Search]* is al geselecteerd. Biedingen op aanbiedingen opnemen voor [!DNL Google Ads] zoekpartners, schakel het selectievakje in naast **[!UICONTROL Search partners]**.

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

Voor het bijhouden van reclame-conversies voor Adobe hoeft u geen waarde in te voeren. De waarde op campagnereniveau is voldoende.

Voer een waarde in voor omleidingen en bijhouden door derden.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** De standaardproductgroep met alle mogelijke productgroepen, &quot;[!UICONTROL All products].&quot; U kunt deze bovenliggende productgroep niet verwijderen, maar deze wordt automatisch verwijderd wanneer alle lagere lagen in de feed ontbreken.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Eenheden zonder onderliggende productgroepen; (optioneel) De sjabloon voor bijhouden van gegevens voor de productgroep, die alle parameters voor omleiding en tekstspatiëring buiten het landingsdomein opgeeft en de laatste URL in een [!DNL ValueTrack] parameter. Deze sjabloon negeert sjablonen op hogere niveaus.

Voor het bijhouden van reclame-conversies voor Adobe hoeft u geen waarde in te voeren. De waarde op campagnereniveau is voldoende.

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
