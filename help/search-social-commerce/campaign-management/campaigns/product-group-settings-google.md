---
title: '[!DNL Google Ads] instellingen productgroep'
description: Verwijs naar de instellingen voor [!DNL Google Ads] winkelgroepen.
exl-id: 3bf33d78-0ad5-43c7-970a-2f2d2e591802
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Google Ads] productgroepinstellingen

## &quot;Alle productgroepen&quot;

**[!UICONTROL Condition]:** (Alleen-lezen) Alle producten

**[!UICONTROL Bid]:** (Alleen inbegrepen productgroepen) De maximale kosten per klik (CPC). Dit is het hoogste bedrag dat voor een advertentie wordt betaald. Deze waarde wordt alleen gebruikt voor eenheden zonder onderliggende productgroepen en wordt gebruikt in plaats van de waarde op ad-groepsniveau.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

Deze sjabloon negeert sjablonen op hogere niveaus en wordt alleen gebruikt voor eenheden zonder onderliggende productgroepen.

## Alle andere productgroepen

**[!UICONTROL Condition/Value]:** (Alleen-lezen voor bestaande productgroepen) De productafmetingen waarop u zich wilt richten. Voor nieuwe productgroepen, ga de afmeting in waardoor om producten te richten, en het kwalificerende attribuut voor de geselecteerde informatiecategorie (zoals &quot;Acme&quot;wanneer u zich door merk richt, of &quot;Nieuw&quot;wanneer u door voorwaarde richt).

Als u een productgroep hebt gemaakt voor specifieke productafmetingen (dus niet voor &quot;Alle producten&quot;), maakt u met Zoeken, Sociaal en Handel automatisch een productgroep voor &quot;Alles anders&quot;.

Voor een lijst met beschikbare productafmetingen raadpleegt u &quot;[Productfilters voor winkelcampagne](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot; Uw lijst met afmetingen kan beperkt zijn op basis van de campagne [!UICONTROL Inventory Filter] instellen.

**[!UICONTROL Excluded]:** (Optioneel voor nieuwe productgroepen; alleen-lezen voor bestaande productgroepen) Biedt geen biedingen op advertenties voor overeenkomende producten.

**[!UICONTROL Bid]:** (Alleen inbegrepen productgroepen) De maximale kosten per klik (CPC). Dit is het hoogste bedrag dat voor een advertentie wordt betaald. Deze waarde wordt alleen gebruikt voor eenheden zonder onderliggende productgroepen en wordt gebruikt in plaats van de waarde op ad-groepsniveau.

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

Deze sjabloon negeert sjablonen op hogere niveaus en wordt alleen gebruikt voor eenheden zonder onderliggende productgroepen.

>[!MORELIKETHIS]
>
>* [Over winkelproductgroepen](product-group-about.md)
>* [Winkelproductgroepen beheren](product-group-manage.md)
>* [Productfilters voor winkelcampagne](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implementeren [!DNL Google Ads] winkelcampagnes](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
