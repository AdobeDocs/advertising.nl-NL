---
title: '[!DNL Microsoft Advertising] productgroepinstellingen'
description: Verwijs de montages voor  [!DNL Microsoft Advertising]  het winkelen productgroepen.
exl-id: ea3a4137-1396-430f-9d6c-8e1e1f1f52c2
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] productgroepinstellingen

## &quot;Alle productgroepen&quot;

**[!UICONTROL Condition]:** (Alleen-lezen) Alle producten

**[!UICONTROL Bid]:** (Alleen inbegrepen productgroepen) De maximale kosten per klik (CPC). Dit is het hoogste bedrag dat u voor een advertentie moet betalen. Deze waarde wordt alleen gebruikt voor eenheden zonder onderliggende productgroepen en wordt gebruikt in plaats van de waarde op ad-groepsniveau.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Deze sjabloon negeert sjablonen op hogere niveaus en wordt alleen gebruikt voor eenheden zonder onderliggende productgroepen.

## Alle andere productgroepen

**[!UICONTROL Condition/Value]:** (Alleen-lezen voor bestaande productgroepen) De productafmetingen die als doel moeten worden ingesteld. Voor nieuwe productgroepen, ga de afmeting in waarmee om producten en het kwalificerende attribuut voor de geselecteerde informatiecategorie (zoals &quot;Acme&quot;wanneer u zich door merk richt, of &quot;Nieuw&quot;wanneer u door voorwaarde richt) te richten.

Als u een productgroep voor specifieke productafmetingen hebt gemaakt (dus niet &quot;Alle producten&quot;), maakt u met Zoeken, Sociaal en Commerce automatisch een productgroep voor &quot;Alles anders&quot;.

Voor een lijst van beschikbare productafmetingen, zie &quot;[ het Verkopen de filters van het campagneproduct ](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot; Uw lijst met afmetingen kan beperkt zijn op basis van de instelling voor [!UICONTROL Inventory Filter] van de campagne.

**[!UICONTROL Excluded]:** (Optioneel voor nieuwe productgroepen; alleen-lezen voor bestaande productgroepen) Hiermee sluit u biedingen op advertenties voor overeenkomende producten uit.

**[!UICONTROL Bid]:** (Alleen inbegrepen productgroepen) De maximale kosten per klik (CPC). Dit is het hoogste bedrag dat u voor een advertentie moet betalen. Deze waarde wordt alleen gebruikt voor eenheden zonder onderliggende productgroepen en wordt gebruikt in plaats van de waarde op ad-groepsniveau.

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Deze sjabloon negeert sjablonen op hogere niveaus en wordt alleen gebruikt voor eenheden zonder onderliggende productgroepen.

>[!MORELIKETHIS]
>
>* [ Ongeveer het winkelen productgroepen ](product-group-about.md)
>* [ beheer het winkelen productgroepen ](product-group-manage.md)
>* [ het Verkopen filters van het campagneproduct ](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [ voert  [!DNL Microsoft Advertising]  het winkelen campagnes ](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md) uit
