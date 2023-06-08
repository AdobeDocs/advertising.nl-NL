---
title: Implementeren [!DNL Microsoft® Advertising] winkelcampagnes
description: Meer informatie over de workflow voor het instellen van [!DNL Microsoft® Advertising] winkelcampagnes.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Implementeren [!DNL Microsoft® Advertising] winkelcampagnes

Advertenties in winkelcampagnes gebruiken gegevens over producten in uw bestaande [!DNL Microsoft® Merchant Center] in plaats van trefwoorden kunt u bepalen hoe en waar u uw advertenties wilt weergeven.

[!DNL Microsoft®] boodschappencampagnes gericht op [!DNL Microsoft® Advertising Shopping Network]. De instellingen voor winkelcampagnes omvatten een bepaald land waarin de producten worden verkocht en een prioriteit ([!DNL High], [!DNL Medium], of [!DNL Low]). U kunt uw voorraad optioneel filteren om producten met specifieke kenmerken te adverteren en specifieke locaties en apparaattypen als doel in te stellen of uit te sluiten.

U kunt bepalen welke producten met uw winkeladvertenties worden weergegeven door meerdere niveaus in te stellen *[productgroepen](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* op het niveau van de advertentiegroep. Productgroepen zijn gebaseerd op alle productkenmerken (categorie, producttype, merk, conditie, product-id en aangepaste labels) en u kunt maximaal zeven niveaus productgroepen maken die u kunt opnemen in of uitsluiten van biedingen, met uitzondering van &quot;[!DNL Add Products].&quot; Je kunt biedingen instellen op het laagste niveau van productgroepen, waarbij hetzelfde bod wordt uitgebracht voor alle overeenkomende producten. Wanneer hetzelfde product in meer dan één campagne is opgenomen, [!DNL Microsoft® Advertising] gebruikt eerst de prioriteit op campagnereniveau om te bepalen welke campagne (en het bijbehorende bod) in aanmerking komt voor de advertentievieiling. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel.

## Stappen die moeten worden ingesteld [!DNL Microsoft® Advertising] winkelcampagnes

U kunt winkelcampagnes instellen met [voorraadvoedersjablonen](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) for [!DNL Microsoft® Advertising], door [bollen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), of afzonderlijk. De volgende instructies bevatten koppelingen naar het maken van afzonderlijke entiteiten.

1. Stel uw [!DNL Microsoft® Merchant Center] en vult deze met productgegevens.

1. [Zoeken, sociale zaken en handel toestaan om gegevens te downloaden van de [!DNL Microsoft® Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Een campagne maken](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) op het winkelnetwerk.

1. [Een advertentiegroep maken](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) in de campagne en het standaardbod voor alle advertenties instellen.

U kunt het standaardbod voor afzonderlijke productgroepen overschrijven.

1. Productgroepen maken voor de advertentiegroep:

   1. [Een productgroep &quot;Alle producten&quot; maken](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Optioneel) [Onderliggende productgroepen maken](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Maken [productadvertenties](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) with [promotielijnen die mogelijk in elke winkeladvertentie worden opgenomen](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) in de advertentiegroep.

      Microsoft® Advertising genereert dynamisch de advertentie-kopie en de bestemmingspagina-URL voor elke advertentie.

      >[!NOTE]
      >
      >Zelfs als de advertentiegroep geen ad-entiteiten bevat, [!DNL Microsoft® Advertising] geeft nog steeds advertenties voor de producten weer.

1. (Optioneel) U kunt klikken op de advertentie bijhouden door [een URL voor bijhouden genereren met het gereedschap URL&#39;s bijhouden](/help/search-social-commerce/tools/click-tracking-url-generate.md). De beste manier is om de URL voor bijhouden toe te voegen aan de [!UICONTROL Tracking Template] in de account-, campagne- of productgroepinstellingen. Voeg het op het hoogst mogelijke niveau toe voor een eenvoudiger onderhoud.

   U kunt de URL voor bijhouden ook toevoegen aan de productgegevens in het dialoogvenster [!DNL Microsoft® Merchant Center] account. Hiervoor neemt u de URL voor het bijhouden van de gegevens samen met de waarde in het veld &quot;link&quot; of &quot;mobile_link&quot;, naar gelang van het geval, op in een aangepaste kolom &quot;[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)&quot; in het diervoeder. De waarde in het veld &quot;bingads_redirect&quot; vervangt de waarden in de velden &quot;link&quot; en &quot;mobile_link&quot;. URL&#39;s die met deze methode worden gegenereerd, bevatten geen traceerparameters die zijn opgegeven in de account- of campagnemontages Zoeken, Sociaal en Handel.

1. Prestaties bewaken met [de [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Indien nodig:

   1. [De instellingen voor de campagne bewerken](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) de campagnebegroting aanpassen.

      Als de campagne deel uitmaakt van een portfolio, wordt de instelling voor het portfolio &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; staat Search, Social, &amp; Commerce toe om de begrotingen voor alle campagnes in de portefeuille te optimaliseren.

   1. Pas het maximumbod voor bestaande productgroepen aan, verwijder productgroepen waarvoor u geen advertenties meer wilt maken of voeg een nieuwe productgroep &quot;alle producten&quot; of nieuwe productgroepen toe om advertenties voor extra producten te maken.

>[!NOTE]
>
>* Zie de vereiste velden voor het beheer [!DNL Microsoft® Shopping] campagnes en productgroepen die [bollen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) en [voorraadvoedersjablonen](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Meer informatie over [!DNL Microsoft® Shopping] campagnes, zie [[!DNL Microsoft® Advertising] documentatie](https://help.ads.microsoft.com/#apex/3/en/50903).

