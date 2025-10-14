---
title: '[!DNL Microsoft Ads] winkelen en sjablooninstellingen voor voorraadfeeds'
description: Verwijs de montages voor  [!DNL Microsoft Ads]  het winkelen en malplaatjes voor inventarisvoer.
exl-id: a0dd6542-0516-406a-b8c5-2e102ec7ab3d
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# [!DNL Microsoft Ads] winkelen en sjablooninstellingen voor voorraadfeeds

Gebruik winkels en sjablonen om winkeladvertenties te configureren.

>[!NOTE]
>
>* De volgende tekens zijn gereserveerd voor het aangeven van kolomnamen en wijzigingsnamen in de sjabloon en zijn daarom niet toegestaan als tekst in alle kenmerkvelden: `[ ] < > `


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

**[!UICONTROL Campaign Tracking Template]:** (Facultatief voor malplaatjes voor de dossiers van de cliëntvoer) het campagne-vlakke het volgen malplaatje, dat alle off-landing domeinomleidingen en het volgen parameters specificeert en definitieve URL in een parameter inbedt. Deze waarde overschrijft de instelling op accountniveau, maar sjablonen bijhouden op meer granulaire niveaus (met trefwoord als meest korrelige) overschrijven deze waarde.

* Voor het volgen van de omzetting van de Adobe Advertising, die wordt toegepast wanneer de campagnemontages &quot; [!UICONTROL EF Redirect]&quot;en &quot;[!UICONTROL Auto Upload] omvatten,&quot;doe één van het volgende&quot;:

   * (Aanbevolen) Gebruik het [&#x200B; het volgen malplaatjeformaat voor het winkelen van Microsoft campagnes &#x200B;](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md). Als de hele account is toegewezen aan winkeladvertenties, kunt u in plaats daarvan een trackingsjabloon op accountniveau definiëren.

   * Als u in plaats daarvan een waarde voor elk product in het voer gebruikend de &quot;[!DNL bingads_redirect]&quot;kolom (gebruikend het [&#x200B; correcte formaat &#x200B;](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)) omvat, dan ga de parameter `{lpurl}` in. U kunt desgewenst omleidingen en tekstspatiëring van derden toevoegen aan de parameter `{lpurl}` .

* Voer een waarde in voor omleidingen en bijhouden door derden.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** De klant-id van de zakelijke account waarvan de producten voor de campagne worden gebruikt.

**[!UICONTROL Sales Country]:** Het land waarin de producten van de campagne worden verkocht. Omdat producten aan elkaar gekoppeld zijn
met de doellanden bepaalt deze instelling welke producten in de campagne worden geadverteerd .

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

**[!UICONTROL Campaign Priority]:** De prioriteit waarmee de campagne wordt gebruikt wanneer de veelvoudige campagnes adverteren
hetzelfde product: *[!UICONTROL Low]* (de standaardinstelling voor nieuwe campagnes), *[!UICONTROL Medium]* of *[!UICONTROL High]* . Wanneer het zelfde product in meer dan één campagne inbegrepen is, het gebruik van het advertentienetwerk
de prioriteit van de campagne om eerst te bepalen welke campagne (en het bijbehorende bod) in aanmerking komt voor de advertentievieg. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel.

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Facultatief) een a-groep-vlakke het volgen malplaatje, dat alle off-landing domeinomleidingen en het volgen parameters specificeert en definitieve URL in een parameter inbedt. Deze waarde overschrijft de instellingen op account- en campagnereniveau, maar sjablonen bijhouden op meer granulaire niveaus overschrijven deze waarde.

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

**[!UICONTROL Tier 1]:** de gebrek, alle-inclusieve productgroep, &quot;[!UICONTROL All products]&quot;. U kunt deze bovenliggende productgroep niet verwijderen, maar deze wordt automatisch verwijderd wanneer alle lagere lagen in de feed ontbreken.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Eenheden zonder onderliggende productgroepen; facultatief) het volgen malplaatje voor het product
groep, die alle parameters voor het omleiden en bijhouden van domeinen buiten de landinstelling opgeeft en de laatste URL in een parameter [!DNL ValueTrack] insluit. Deze sjabloon negeert sjablonen op hogere niveaus.

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
>* [&#x200B; Ongeveer automatiserend en beheer gebruikend inventarisvoer &#x200B;](../inventory-feeds-about.md)
>* [&#x200B; het Leiden bepalingen &#x200B;](../modifiers-manage.md)
>* [&#x200B; het Leiden dossiers van de materiaalvoer van inventarisgegevens &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [&#x200B; doorgeven voedergegevens door malplaatjes &#x200B;](../feed-data-propagate.md)
>* [&#x200B; de campagnegegevens van inventarisvoer aan ad netwerken &#x200B;](../propagated-data-post.md)
