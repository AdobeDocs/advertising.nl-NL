---
title: Implementeren [!DNL Google Ads] winkelcampagnes
description: Meer informatie over de workflow voor het instellen van [!DNL Google Ads] winkelcampagnes.
exl-id: aab61d94-861f-4072-b044-f9ae6759e028
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Implementeren [!DNL Google Ads] winkelcampagnes

Advertenties in winkelcampagnes gebruiken gegevens over producten in uw bestaande [!DNL Google Merchant Center] in plaats van trefwoorden kunt u bepalen hoe en waar u uw advertenties wilt weergeven.

[!DNL Google Ads] campagnes kunnen gericht zijn op [!DNL Google Shopping Network] met de [!UICONTROL Campaign Type] &quot;[!UICONTROL Shopping Network].&quot; De instellingen voor [!DNL Google Shopping] de campagnes hebben een prioriteit ([!UICONTROL High], [!UICONTROL Medium], of [!UICONTROL Low]). U kunt desgewenst uw lokale inventarisgegevens in uw winkeladvertenties weergeven met een instelling op campagnereniveau.

U kunt bepalen welke producten met uw winkeladvertenties worden weergegeven door meerdere niveaus in te stellen *[productgroepen](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* op het niveau van de advertentiegroep. Productgroepen zijn gebaseerd op alle productkenmerken (categorie, producttype, merk, conditie, product-id en aangepaste labels) en u kunt maximaal zeven niveaus productgroepen maken om producten op te nemen of van bieden uit te sluiten. Je kunt biedingen instellen op het laagste niveau van productgroepen, waarbij hetzelfde bod wordt uitgebracht voor alle overeenkomende producten. Wanneer hetzelfde product in meer dan één campagne is opgenomen, [!DNL Google Ads] gebruikt eerst de prioriteit op campagnereniveau om te bepalen welke campagne (en het bijbehorende bod) in aanmerking komt voor de advertentievieiling. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel.

## Stappen die moeten worden ingesteld [!DNL Google Ads] winkelcampagnes

U kunt winkelcampagnes instellen met [voorraadvoedersjablonen](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) for [!DNL Google Shopping], door [bulksbladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), of afzonderlijk. De volgende instructies bevatten koppelingen naar het maken van afzonderlijke entiteiten.

1. Stel uw [!DNL Google Merchant Center] en vult deze met productgegevens.

1. [Zoeken, sociale zaken en handel toestaan om gegevens te downloaden van de [!DNL Google Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Een campagne maken](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) op het winkelnetwerk.

1. [Een advertentiegroep maken](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) in de campagne en het standaardbod voor alle advertenties instellen.

U kunt het standaardbod voor afzonderlijke productgroepen overschrijven.

1. Productgroepen maken voor de advertentiegroep:

   1. [Een productgroep &quot;Alle producten&quot; maken](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Optioneel) [Onderliggende productgroepen maken](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >Je hoeft geen winkeladvertenties te maken. Zelfs als de advertentiegroep geen ad-entiteiten bevat, [!DNL Google Ads] geeft nog steeds advertenties voor de producten weer.

1. (Optioneel) U kunt klikken op de advertentie bijhouden door [een URL voor bijhouden genereren met het gereedschap URL&#39;s bijhouden](/help/search-social-commerce/tools/click-tracking-url-generate.md)en voeg deze vervolgens toe aan de account-, campagne- of productgroepinstellingen.

1. Prestaties bewaken met [het genereren van [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) en [de [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Indien nodig:

   1. [De instellingen voor de campagne bewerken](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) de campagnebegroting aanpassen.

      Als de campagne deel uitmaakt van een portfolio, wordt de instelling voor het portfolio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; staat Search, Social, &amp; Commerce toe om de begrotingen voor alle campagnes in de portefeuille te optimaliseren.

   1. [Het maximumbod voor bestaande productgroepen aanpassen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [productgroepen verwijderen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) waarvoor u geen advertenties meer wilt maken of waarvoor u een [nieuwe productgroep &quot; alle producten &quot;](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) of [nieuwe productgroepen voor kinderen](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) om advertenties te maken voor extra producten.

>[!NOTE]
>
>* Zie de vereiste velden voor het beheer [!DNL Google Shopping] campagnes en productgroepen die [bulksbladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) en [voorraadvoedersjablonen](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* Voor meer informatie over [!DNL Google Shopping] campagnes, zie [[!DNL Google Ads] documentatie](https://support.google.com/google-ads/answer/2454022).
