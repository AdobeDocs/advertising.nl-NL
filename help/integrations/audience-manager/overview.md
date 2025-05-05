---
title: Integratie van Adobe Advertising met Adobe Audience Manager
description: Leer hoe Adobe Advertising gegevens kan uitwisselen met Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: d0260fc3b10f1944b82cdc4c1e3b8137a695e05e
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Integratie van Adobe Advertising met Adobe Audience Manager

U kunt Adobe Advertising met Audience Manager op de volgende manieren integreren.

## Audience Manager en andere synchroniseren [!DNL Adobe] Segmenten voor advertentiedoeleinden

[!DNL Search, Social, & Commerce] en DSP kunnen metagegevens, hiërarchische gegevens en unieke publieksgegevens ophalen voor alle Audience Managers en andere [!DNL Adobe] publiek. Deze unieke verbinding is alleen beschikbaar voor marketers die Adobe Advertising gebruiken. Zie &quot;[Adobe Audience Manager-segmenten importeren voor advertentiedoeleinden](/help/integrations/audience-manager/import-audiences.md).&quot;

### Audience Manager en overige gebruiken [!DNL Adobe] Te maken segmenten [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Geopende adverteerders met [!DNL Advertising Search, Social, & Commerce] alleen*

Within [!DNL Search, Social, & Commerce]kunt u [!DNL Google Ads] klant past publiek van gebruiker IDs aan gebruikend uw bestaande segmenten van de Audience Manager die hebben [!UICONTROL Adobe Media Optimizer (HTTP)] en [!UICONTROL Adobe Media Optimizer Batch Destination] als bestemmingen. ([!DNL Media Optimizer] is een vroegere naam voor [!DNL Search, Social, & Commerce].) Dit omvat Adobe Analytics-segmenten die naar Adobe Experience Cloud worden gepubliceerd en segmenten die met de Adobe Experience Cloud zijn gemaakt [!DNL Audience Library]. Zie voor meer informatie &quot;[Maken [!DNL Google Ads] klant stemt doelgroep van [!DNL Adobe] publiek](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[Klanten komen overeen met gebruikers-id&#39;s](https://support.google.com/google-ads/answer/9199250) werkt zoals publiek op basis van tags op de website, maar een niet-PII-id wordt toegewezen aan unieke publieksleden voor duidelijke voordelen ten opzichte van standaardklantovereenkomsten en publiek op basis van tags op de website.

Als u de benodigde gebruikers-id&#39;s wilt maken, moet u een JavaScript-tag voor Adoben Advertising gebruiken <!-- with a user ID parameter -->op uw websites. Neem contact op met het accountteam van de Adobe voor meer informatie.

![segmentaanmaakproces](/help/integrations/assets/ad_search_user_id_pic.png)

Wanneer u het publiek hebt gemaakt, kunt u deze gebruiken in [!DNL Google Ads] campagnes als [streefcijfers of uitsluitingen op campagneniveau of op ad-groepsniveau](#audience-manager-targets).

### Audience Manager en andere [!DNL Adobe] Segmenten voor doel- of uitsluitingsadvertenties {#audience-manager-targets}

* (Geopende adverteerders met [!DNL Search, Social, & Commerce]) U kunt alle [!DNL Google Ads] publiek dat [gemaakt met [!DNL Adobe] segmenten](#audience-manager-google-audiences) als streefdoelen of uitsluitingen op campagnereniveau of op ad-groepsniveau in uw [!DNL Google Ads] campagnes.

* (Adverteerders met DSP) U kunt uw bestaande [!DNL Adobe] segmenten als doelen voor uw advertentieplaatsen. U kunt de segmenten desgewenst opnemen in herbruikbare doelgroepen, die u kunt gebruiken als doelen of uitsluitingen voor meerdere plaatsingen.

* (Adverteerders met Advertising Creative) U kunt uw bestaande [!DNL Adobe] segmenten als doelen voor specifieke creatieve objecten in uw advertentie.

>[!NOTE]
>
>Voor meer informatie over hoe u een publiek kunt maken in de Audience Manager en het Experience Cloud [!DNL Audience Library] interfaces, en gemeenschappelijke gebruiksgevallen voor verschillende publiekstypes, zie &quot;[Opties voor het maken van publiek](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=nl-NL).&quot;

## Gegevens over belichting van DSP media naar Audience Manager verzenden

*Adverteerders met alleen DSP*

DSP klanten met Adobe Audience Manager kunnen gegevens uit advertentiecampagnes vastleggen met behulp van pixelaanroepen naar Audience Manager. U kunt de campagnegegevens dan gebruiken om op regel-gebaseerde eigenschappen te bouwen, die u kunt gebruiken om nieuwe segmenten te bepalen om diverse DSP gebruiksgevallen, zoals geavanceerdere segmentatie, frequentiebeheer, marketing analyses, en het melden van inzichten toe te laten.

Zie &quot;[Overzicht van het verzenden van gegevens over DSP mediablootstelling naar Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; voor meer informatie .

## Rijkere inzichten in de activiteit van de Plaats met Audience Analytics krijgen

Adobe Advertising klanten met [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=nl-NL) kan zowel Adobe Advertising-gevolgde gegevens als Audience Manager segmenten naar verzenden [!DNL Analytics] voor verrijkte inzichten in de activiteit van de site.

Zie voor meer informatie &quot;[[!DNL Adobe Audience Analytics] voor klanten van de Adobe Advertising](/help/integrations/audience-manager/audience-analytics.md).&quot;
