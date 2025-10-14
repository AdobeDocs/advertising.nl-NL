---
title: Voer  [!DNL Google Ads]  het winkelen campagnes uit
description: Leer over het werkschema voor vestiging  [!DNL Google Ads]  het winkelen campagnes.
exl-id: d80370d9-534d-4854-b7d3-1384a84320ad
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# [!DNL Google Ads] winkelcampagnes implementeren

Advertenties in winkelcampagnes gebruiken in plaats van trefwoorden gegevens over producten in de bestaande [!DNL Google Merchant Center] -productfeed om te bepalen hoe en waar u uw advertenties wilt weergeven.

[!DNL Google Ads] -campagnes kunnen de [!DNL Google Shopping Network] als doel hebben met [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network]&quot;. De instellingen voor [!DNL Google Shopping] -campagnes omvatten een prioriteit ( [!UICONTROL High] , [!UICONTROL Medium] of [!UICONTROL Low] ). U kunt desgewenst uw lokale inventarisgegevens in uw winkeladvertenties weergeven met een instelling op campagnereniveau.

U kunt controleren welke producten met uw het winkelen advertenties door opstelling multi-level *[productgroepen](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* op het niveau van de advertentiegroep worden getoond. Productgroepen zijn gebaseerd op alle productkenmerken (categorie, producttype, merk, conditie, product-id en aangepaste labels) en u kunt maximaal zeven niveaus productgroepen maken om producten op te nemen of van bieden uit te sluiten. Je kunt biedingen instellen op het laagste niveau van productgroepen, waarbij hetzelfde bod wordt uitgebracht voor alle overeenkomende producten. Wanneer hetzelfde product in meer dan één campagne is opgenomen, gebruikt [!DNL Google Ads] eerst de prioriteit op campagnereniveau om te bepalen welke campagne (en het bijbehorende bod) in aanmerking komt voor de advertentieveiling. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel.

## Stappen voor het opzetten van [!DNL Google Ads] winkelcampagnes

U kunt opstelling het winkelen campagnes door [&#x200B; voorraadvoedermalplaatjes &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) voor [!DNL Google Shopping] te gebruiken, door [&#x200B; bulksbladen &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), of individueel te gebruiken. De volgende instructies bevatten koppelingen naar het maken van afzonderlijke entiteiten.

1. Stel uw [!DNL Google Merchant Center] -account in en vul deze met productgegevens.

1. [&#x200B; sta Onderzoek, Sociale, &amp; Commerce toe om gegevens van de  [!DNL Google Merchant Center]  rekening &#x200B;](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md) te downloaden.

1. [&#x200B; creeer een campagne &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) op het het winkelen netwerk.

1. [&#x200B; creeer een advertentiegroep &#x200B;](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) binnen de campagne, en plaats het standaardbod voor alle advertenties.

   U kunt het standaardbod voor afzonderlijke productgroepen overschrijven.

1. Productgroepen maken voor de advertentiegroep:

   1. [&#x200B; creeer een &quot;Alle Producten&quot;productgroep &#x200B;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Facultatief) [&#x200B; creeer de groepen van het kindproduct &#x200B;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >Je hoeft geen winkeladvertenties te maken. Zelfs als de advertentiegroep geen ad-entiteiten bevat, geeft [!DNL Google Ads] nog steeds advertenties voor de producten weer.

1. (Facultatief) om kliks op de advertentie te volgen, [&#x200B; produceert het volgen URL gebruikend het Volgen hulpmiddel URLs &#x200B;](/help/search-social-commerce/tools/click-tracking-url-generate.md), en voegt het dan aan de rekening, de campagne, of de montages van de productgroep toe.

1. De prestaties van de monitor door [&#x200B; te produceren [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) en [&#x200B; [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Indien nodig:

   1. [&#x200B; geef de campagnemontages &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) uit om het campagnebudget aan te passen.

      Als de campagne deel van een portefeuille uitmaakt, dan staat het portefeuille plaatsen &quot;[!UICONTROL Auto adjust campaign budget limits]&quot;Onderzoek, Sociale, &amp; Commerce toe om de begrotingen voor alle campagnes in de portefeuille te optimaliseren.

   1. [&#x200B; pas het maximumbod voor bestaande productgroepen &#x200B;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) aan, [&#x200B; schrapt productgroepen &#x200B;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) waarvoor u niet meer advertenties wilt creëren, of a [&#x200B; nieuwe &quot;alle producten&quot;productgroep &#x200B;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) of [&#x200B; nieuwe groepen van het kindproduct &#x200B;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) toevoegen om advertenties voor extra producten tot stand te brengen.

>[!NOTE]
>
>* Zie de vereiste gebieden voor het beheren van [!DNL Google Shopping] campagnes en productgroepen gebruikend [&#x200B; bulksbladen &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) en [&#x200B; de malplaatjes van de inventarisvoer &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Voor meer informatie over [!DNL Google Shopping] campagnes, zie de [[!DNL Google Ads]  documentatie &#x200B;](https://support.google.com/google-ads/answer/2454022).
