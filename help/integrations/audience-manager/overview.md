---
title: Adobe Advertising-integratie met Adobe Audience Manager
description: Meer informatie over de verschillende manieren waarop Adobe Advertising gegevens kan uitwisselen met Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Adobe Advertising-integratie met Adobe Audience Manager

U kunt Adobe Advertising op de volgende manieren integreren met Audience Manager.

## Audience Manager en andere [!DNL Adobe] -segmenten synchroniseren voor advertentie

[!DNL Search, Social, & Commerce] en DSP kunnen metagegevens, hiërarchische gegevens en unieke publieksgegevens ophalen voor alle Audience Manager&#39;s en andere [!DNL Adobe] -doelgroepen van adverteerders of bureaus. Deze unieke verbinding is alleen beschikbaar voor marketers die Adobe Advertising gebruiken. Zie &quot;[ de segmenten van Adobe Audience Manager van de Invoer voor en richten ](/help/integrations/audience-manager/import-audiences.md).&quot;

### Audience Manager en andere [!DNL Adobe] -segmenten gebruiken om [!DNL Google Ads] publiek te maken {#audience-manager-google-audiences}

*Opted-in adverteerders met [!DNL Advertising Search, Social, & Commerce] slechts*

Binnen [!DNL Search, Social, & Commerce] kunt u [!DNL Google Ads] klantovereenkomsten van gebruikers-id&#39;s maken met behulp van bestaande Audience Manager-segmenten met [!UICONTROL Adobe Media Optimizer (HTTP)] en [!UICONTROL Adobe Media Optimizer Batch Destination] als doelen. ([!DNL Media Optimizer] is een vroegere naam voor [!DNL Search, Social, & Commerce].) Dit omvat Adobe Analytics-segmenten die naar Adobe Experience Cloud worden gepubliceerd en segmenten die met de Adobe Experience Cloud [!DNL Audience Library] worden gemaakt. Voor meer informatie, zie &quot;[  [!DNL Google Ads]  de publiek van de klantengelijke van  [!DNL Adobe]  publiek ](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) creëren.&quot;

[ de gelijke van de Klant publiek van gebruiker IDs ](https://support.google.com/google-ads/answer/9199250) werk als website op markering-gebaseerde publiek, maar niet-PII identiteitskaart wordt toegewezen aan unieke publieksleden voor duidelijke voordelen over standaardklantengelijke en website op markering-gebaseerde publiek.

Om tot de noodzakelijke gebruikers-ids te leiden, moet u een markering van Adobe Advertising JavaScript <!-- with a user ID parameter --> op uw websites gebruiken. Neem contact op met uw Adobe-accountteam voor meer informatie.

![ proces van de segmentverwezenlijking ](/help/integrations/assets/ad_search_user_id_pic.png)

Zodra u het publiek creeert, kunt u hen in [!DNL Google Ads] campagnes als [ campagne-niveau of ad groep-vlakke doelstellingen of uitsluitingen ](#audience-manager-targets) gebruiken.

### Audience Manager en andere [!DNL Adobe] -segmenten gebruiken om advertenties te activeren of uit te sluiten {#audience-manager-targets}

* (Opted-in adverteerders met [!DNL Search, Social, & Commerce]) U kunt om het even welk [!DNL Google Ads] publiek gebruiken dat [ werd gecreeerd gebruikend  [!DNL Adobe]  segmenten ](#audience-manager-google-audiences) als campagne-niveau of ad groep-vlakke doelstellingen of uitsluitingen in uw [!DNL Google Ads] campagnes.

* (Advertisers met DSP) U kunt uw bestaande [!DNL Adobe] -segmenten gebruiken als doelen voor uw advertentieplaatsen. U kunt de segmenten desgewenst opnemen in herbruikbare doelgroepen, die u kunt gebruiken als doelen of uitsluitingen voor meerdere plaatsingen.

* (Advertisers met Advertising Creative) U kunt uw bestaande [!DNL Adobe] -segmenten gebruiken als doelen voor specifieke creatieve objecten in uw advertentiervaringen.

>[!NOTE]
>
>Voor meer informatie over hoe te om publiek in Audience Manager en Experience Cloud [!DNL Audience Library] interfaces tot stand te brengen, en gemeenschappelijke gebruiksgevallen voor verschillende publiekstypes, zie &quot;[ de schepingsopties van het Publiek ](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## DSP-mediabelichtingsgegevens naar Audience Manager verzenden

*Advertisers met slechts DSP*

DSP-klanten met Adobe Audience Manager kunnen gegevens van advertentiecampagnes vastleggen met behulp van pixelaanroepen naar Audience Manager. U kunt de campagnegegevens dan gebruiken om op regel-gebaseerde eigenschappen te bouwen, die u kunt gebruiken om nieuwe segmenten te bepalen om diverse DSP gebruiksgevallen, zoals geavanceerdere segmentatie, frequentiebeheer, marketing analyses, en rapporteringsinzichten toe te laten.

Zie &quot;[ Overzicht van het verzenden van de media van DSP blootstellingsgegevens naar Adobe Audience Manager ](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;voor meer informatie.

## Meer inzicht in de activiteiten van sites krijgt u met Audience Analytics

Adobe Advertising-klanten met [[!DNL Adobe Audience Analytics] ](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) kunnen zowel Adobe Advertising-bijgehouden gegevens als Audience Manager-segmenten naar [!DNL Analytics] verzenden voor verrijkte inzichten in siteactiviteit.

Voor meer informatie, zie &quot;[[!DNL Adobe Audience Analytics]  voor de klanten van Adobe Advertising ](/help/integrations/audience-manager/audience-analytics.md).&quot;
