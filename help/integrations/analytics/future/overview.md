---
title: Integratie van Adobe Advertising met Adobe Analytics
description: Leer hoe Adobe Advertising gegevens kan uitwisselen met Adobe Analytics en hoe u de gegevens kunt gebruiken in Zoeken, Sociale Zaken en Handel.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 78f69587771d9e72eb137f1e0866d782ed5c4d01
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Integratie van Adobe Advertising met Adobe Analytics

U kunt Adobe Advertising op de volgende manieren integreren met Analytics.

## Gegevens uitwisselen tussen [!DNL Analytics] en Adobe Advertising

### Draaien [!DNL Analytics] Gegevens in Adobe Advertising

Met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] en DSP trekken in:

* **[!DNL Analytics]segmenten:**  Metagegevens, hiërarchiegegevens en unieke publieksgegevens voor alle segmenten van een adverteerder of een instantie die zijn gemaakt in [!DNL Analytics] en bekendgemaakt aan het Experience Cloud.

* **[!DNL Analytics]maatstaven voor sitebetrokkenheid**

* **[!DNL Analytics]standaard, aangepaste en gereserveerde cijfers**

### Gegevens Adobe Advertising verzenden naar [!DNL Analytics]

* **Verkeersmetriek van Adobe Advertising**

* **Dimensionen van Adobe Advertising**

>[!NOTE]
>
>Voor [!DNL Search, Social, & Commerce], wordt deze functie ondersteund voor de meeste advertentienetwerken en campagneretypen. Zie &quot;Ondersteunde voorraad&quot; in het dialoogvenster [!DNL Search, Social, & Commerce] Voor meer informatie.<!-- add link when that's published in ExL -->

### Gebruiken [!DNL Analytics] Te maken segmenten [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Geopende adverteerders met [!DNL Advertising Search, Social, & Commerce] alleen*

<!-- Verify all -->

Within [!DNL Search, Social, & Commerce]kunt u [!DNL Google Ads] Google-klanten komen overeen met gebruikers-id&#39;s die uw bestaande [!DNL Analytics] segmenten. Dit omvat Adobe Analytics-segmenten die naar Adobe Experience Cloud worden gepubliceerd en segmenten die met de Adobe Experience Cloud zijn gemaakt [!DNL Audience Library]. Zie voor meer informatie &quot;[Maken [!DNL Google Ads] klant stemt doelgroep van [!DNL Adobe] publiek](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[Klanten komen overeen met gebruikers-id&#39;s](https://support.google.com/google-ads/answer/9199250) werkt zoals publiek op basis van tags op de website, maar een niet-PII-id wordt toegewezen aan unieke publieksleden voor duidelijke voordelen ten opzichte van standaardklantovereenkomsten en publiek op basis van tags op de website.

Als u de benodigde gebruikers-id&#39;s wilt maken, moet u een JavaScript-tag voor Adoben Advertising gebruiken <!-- with a user ID parameter -->op uw websites. Neem contact op met het accountteam van de Adobe voor meer informatie.

![segmentaanmaakproces](/help/integrations/assets/ad_search_user_id_pic.png)

Wanneer u het publiek hebt gemaakt, kunt u deze gebruiken in [!DNL Google Ads] campagnes als [streefcijfers of uitsluitingen op campagneniveau of op ad-groepsniveau](#audience-manager-targets).

### Gebruiken [!DNL Analytics] Segmenten voor doel- of uitsluitingsadvertenties {#analytics-targets}

* (Geopende adverteerders met [!DNL Search, Social, & Commerce]) U kunt alle [!DNL Google Ads] publiek dat [gemaakt met [!DNL Analytics] segmenten](#audience-manager-google-audiences) als streefdoelen of uitsluitingen op campagnereniveau of op ad-groepsniveau in uw [!DNL Google Ads] campagnes.

* (Adverteerders met DSP) U kunt uw bestaande [!DNL Analytics] segmenten als doelen voor uw advertentieplaatsen. U kunt de segmenten desgewenst opnemen in herbruikbare doelgroepen, die u kunt gebruiken als doelen of uitsluitingen voor meerdere plaatsingen.

* (Adverteerders met Advertising Creative) U kunt uw bestaande [!DNL Analytics] segmenten als doelen voor specifieke creatieve objecten in uw advertentie.
