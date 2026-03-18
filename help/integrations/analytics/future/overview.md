---
title: Adobe Advertising-integratie met Adobe Analytics
description: Leer hoe Adobe Advertising gegevens kan uitwisselen met Adobe Analytics en hoe u de gegevens kunt gebruiken in Zoeken, Sociaal en Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Adobe Advertising-integratie met Adobe Analytics

U kunt Adobe Advertising op de volgende manieren integreren met Analytics.

## Gegevens uitwisselen tussen [!DNL Analytics] en Adobe Advertising

### [!DNL Analytics] gegevens ophalen in Adobe Advertising

Met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md), [!DNL Search, Social, & Commerce] en DSP trekken binnen:

* **[!DNL Analytics]segmenten:** Metagegevens, hiërarchiegegevens en unieke publieksgegevens voor alle segmenten van een adverteerder of een agentschap die in [!DNL Analytics] zijn gemaakt en naar Experience Cloud zijn gepubliceerd.

* **[!DNL Analytics]maatstaven voor de betrokkenheid van de site**

* **[!DNL Analytics]standaard, douane, en gereserveerde metriek**

### Adobe Advertising-gegevens verzenden naar [!DNL Analytics]

* **metriek van het Verkeer van Adobe Advertising**

* **Dimensies van Adobe Advertising**

>[!NOTE]
>
>Voor [!DNL Search, Social, & Commerce] wordt deze functie ondersteund voor de meeste advertentienetwerken en campagneretypen. Zie &quot;Ondersteunde voorraad&quot; in de [!DNL Search, Social, & Commerce] Guide voor meer informatie. <!-- add link when that's published in ExL -->

### Gebruik [!DNL Analytics] -segmenten om [!DNL Google Ads] publiek te maken {#audience-manager-google-audiences}

*Opted-in adverteerders met [!DNL Advertising Search, Social, & Commerce] slechts*

<!-- Verify all -->

Binnen [!DNL Search, Social, & Commerce] kunt u met behulp van uw bestaande [!DNL Google Ads] -segmenten [!DNL Analytics] overeenkomende soorten publiek voor Google-klanten maken op basis van gebruikers-id&#39;s. Dit zijn onder andere Adobe Analytics-segmenten die naar Adobe Experience Cloud worden gepubliceerd en segmenten die met de Adobe Experience Cloud [!DNL Audience Library] zijn gemaakt. Voor meer informatie, zie &quot;[  [!DNL Google Ads]  de publiek van de klantengelijke van  [!DNL Adobe]  publiek ](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) creëren.&quot;

[ de gelijke van de Klant publiek van gebruiker IDs ](https://support.google.com/google-ads/answer/9199250) werk als website op markering-gebaseerde publiek, maar niet-PII identiteitskaart wordt toegewezen aan unieke publieksleden voor duidelijke voordelen over standaardklantengelijke en website op markering-gebaseerde publiek.

Om tot de noodzakelijke gebruikers-ids te leiden, moet u een markering van Adobe Advertising JavaScript <!-- with a user ID parameter --> op uw websites gebruiken. Neem contact op met uw Adobe-accountteam voor meer informatie.

![ proces van de segmentverwezenlijking ](/help/integrations/assets/ad_search_user_id_pic.png)

Zodra u het publiek creeert, kunt u hen in [!DNL Google Ads] campagnes als [ campagne-niveau of ad groep-vlakke doelstellingen of uitsluitingen ](#audience-manager-targets) gebruiken.

### Gebruik [!DNL Analytics] segmenten om advertenties te activeren of uit te sluiten {#analytics-targets}

* (Opted-in adverteerders met [!DNL Search, Social, & Commerce]) U kunt om het even welk [!DNL Google Ads] publiek gebruiken dat [ werd gecreeerd gebruikend  [!DNL Analytics]  segmenten ](#audience-manager-google-audiences) als campagne-niveau of ad groep-vlakke doelstellingen of uitsluitingen in uw [!DNL Google Ads] campagnes.

* (Advertisers met DSP) U kunt uw bestaande [!DNL Analytics] -segmenten gebruiken als doelen voor uw advertentieplaatsen. U kunt de segmenten desgewenst opnemen in herbruikbare doelgroepen, die u kunt gebruiken als doelen of uitsluitingen voor meerdere plaatsingen.

* (Advertisers met Advertising Creative) U kunt uw bestaande [!DNL Analytics] -segmenten gebruiken als doelen voor specifieke creatieve objecten in uw advertentiervaringen.
