---
title: Voer  [!DNL Microsoft Advertising]  het winkelen campagnes uit
description: Leer over het werkschema voor vestiging  [!DNL Microsoft Advertising]  het winkelen campagnes.
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] winkelcampagnes implementeren

Advertenties in winkelcampagnes gebruiken in plaats van trefwoorden gegevens over producten in de bestaande [!DNL Microsoft Merchant Center] -productfeed om te bepalen hoe en waar u uw advertenties wilt weergeven.

[!DNL Microsoft] winkelcampagnes zijn gericht op [!DNL Microsoft Advertising Shopping Network] . De instellingen voor winkelcampagnes omvatten een bepaald land waarin de producten worden verkocht en een prioriteit ([!DNL High], [!DNL Medium] of [!DNL Low] ). U kunt uw voorraad optioneel filteren om producten met specifieke kenmerken te adverteren en specifieke locaties en apparaattypen als doel in te stellen of uit te sluiten.

U kunt controleren welke producten met uw het winkelen advertenties door opstelling multi-level *[productgroepen](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* op het niveau van de advertentiegroep worden getoond. De groepen van het product zijn gebaseerd op om het even welke productattributen (categorie, producttype, merk, voorwaarde, product identiteitskaart, en douanelabels), en u kunt tot zeven niveaus van productgroepen tot stand brengen om van het bieden te omvatten of uit te sluiten, niet met inbegrip van &quot;[!DNL Add Products]&quot;. Je kunt biedingen instellen op het laagste niveau van productgroepen, waarbij hetzelfde bod wordt uitgebracht voor alle overeenkomende producten. Wanneer hetzelfde product in meer dan één campagne is opgenomen, gebruikt [!DNL Microsoft Advertising] eerst de prioriteit op campagnereniveau om te bepalen welke campagne (en het bijbehorende bod) in aanmerking komt voor de advertentieveiling. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel.

## Stappen voor het opzetten van [!DNL Microsoft Advertising] winkelcampagnes

U kunt opstelling het winkelen campagnes door [ voorraadvoedermalplaatjes ](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) voor [!DNL Microsoft Advertising] te gebruiken, door [ bulksbladen ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), of individueel te gebruiken. De volgende instructies bevatten koppelingen naar het maken van afzonderlijke entiteiten.

1. Stel uw [!DNL Microsoft Merchant Center] -account in en vul deze met productgegevens.

1. [ sta Onderzoek, Sociale, &amp; Commerce toe om gegevens van de  [!DNL Microsoft Merchant Center]  rekening ](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md) te downloaden.

1. [ creeer een campagne ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) op het het winkelen netwerk.

1. [ creeer een advertentiegroep ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) binnen de campagne, en plaats het standaardbod voor alle advertenties.

   U kunt het standaardbod voor afzonderlijke productgroepen overschrijven.

1. Productgroepen maken voor de advertentiegroep:

   1. [ creeer een &quot;Alle Producten&quot;productgroep ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. (Facultatief) [ creeer de groepen van het kindproduct ](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Creeer [ productadvertenties ](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) met [ bevorderingslijnen potentieel om in elke het winkelen en ](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) binnen de advertentiegroep te omvatten.

      Microsoft Advertising genereert dynamisch de advertentie-kopie en de bestemmingspagina-URL voor elke advertentie.

      >[!NOTE]
      >
      >Zelfs als de advertentiegroep geen ad-entiteiten bevat, geeft [!DNL Microsoft Advertising] nog steeds advertenties voor de producten weer.

1. (Facultatief) om kliks op de advertentie te volgen, [ produceert het volgen URL gebruikend het het Volgen hulpmiddel URLs ](/help/search-social-commerce/tools/click-tracking-url-generate.md). U kunt het beste de URL voor bijhouden toevoegen aan het veld [!UICONTROL Tracking Template] in de account-, campagne- of productgroepinstellingen. Voeg het op het hoogst mogelijke niveau toe om het onderhoud te vereenvoudigen.

   U kunt ook de URL voor bijhouden toevoegen aan de productgegevens in de [!DNL Microsoft Merchant Center] -account. Om dit te doen, omvat het volgen URL, samen met de waarde in het &quot;verbinding&quot;of &quot;mobile_link&quot;gebied, zoals aangewezen, in een douanekolom &quot;[ bingads_redirect ](https://help.ads.microsoft.com/#apex/3/en/51084)&quot;binnen de productvoer. De waarde in het veld &quot;bingads_redirect&quot; vervangt de waarden in de velden &quot;link&quot; en &quot;mobile_link&quot;. URL&#39;s die met deze methode worden gegenereerd, bevatten geen volgparameters die zijn opgegeven in de instellingen voor Zoeken, Sociaal zoeken en Commerce.

1. De prestaties van de monitor door [ te produceren [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. Indien nodig:

   1. [ geef de campagnemontages ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) uit om het campagnebudget aan te passen.

      Als de campagne deel van een portefeuille uitmaakt, dan staat het portefeuille plaatsen &quot;[!UICONTROL Auto adjust campaign budget limits]&quot;Onderzoek, Sociale, &amp; Commerce toe om de begrotingen voor alle campagnes in de portefeuille te optimaliseren.

   1. Pas het maximumbod voor bestaande productgroepen aan, verwijder productgroepen waarvoor u geen advertenties meer wilt maken of voeg een nieuwe productgroep &quot;alle producten&quot; of nieuwe productgroepen toe om advertenties voor extra producten te maken.

>[!NOTE]
>
>* Zie de vereiste gebieden voor het beheren van [!DNL Microsoft Shopping] campagnes en productgroepen gebruikend [ bulksbladen ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) en [ de malplaatjes van de inventarisvoer ](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* Voor meer informatie over [!DNL Microsoft Shopping] campagnes, zie de [[!DNL Microsoft Advertising]  documentatie ](https://help.ads.microsoft.com/#apex/3/en/50903).
