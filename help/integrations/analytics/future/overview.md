---
title: Adobe Advertising Integrations with Adobe Analytics
description: Leer hoe Adobe Advertising gegevens kan uitwisselen met Adobe Analytics en hoe u de gegevens kunt gebruiken in Search, Social & Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: def6a3a8d1de1f9f80dee6ecd1a18667afc79fd3
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Adobe Advertising Integrations with Adobe Analytics

U kunt reclame voor Adobe op de volgende manieren integreren met Analytics.

## Gegevens uitwisselen tussen [!AAnalyse] en Adobe-reclame

### Draaien [!AAnalyse] Gegevens over Adobe-reclame

Met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] en DSP trekken in:

* **[!DNL Analytics]segmenten:**  Metagegevens, hiërarchiegegevens en unieke publieksgegevens voor alle segmenten van een adverteerder of instantie die zijn gemaakt in [!DNL Analytics] en gepubliceerd aan Experience Cloud.

* **[!DNL Analytics]maatstaven voor sitebetrokkenheid**

* **[!DNL Analytics]Standaard, aangepaste en gereserveerde cijfers**

### Adobe-advertentiegegevens verzenden naar [!AAnalyse]

* **Verkeersmetriek van Adobe Advertising**

* **Dimension van Adobe-reclame**

>[!NOTE]
>
>Voor [!DNL Search, Social, & Commerce], wordt deze functie ondersteund voor de meeste advertentienetwerken en campagneretypen. Zie &quot;Ondersteunde voorraad&quot; in het dialoogvenster [!DNL Search, Social, & Commerce] Voor meer informatie.<!-- add link when that's published in ExL -->

### Gebruiken [!DNL Analytics] Te maken segmenten [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Geopende adverteerders met [!DNL Advertising Search, Social, & Commerce] alleen*

<!-- Verify all -->

Within [!DNL Search, Social, & Commerce]kunt u [!DNL Google Ads] Google-klanten komen overeen met gebruikers-id&#39;s die uw bestaande [!DNL Analytics] segmenten. Dit omvat Adobe Analytics-segmenten die naar Adobe Experience Cloud worden gepubliceerd en segmenten die met de Adobe Experience Cloud zijn gemaakt [!DNL Audience Library]. Raadpleeg de Help in het product voor meer informatie [!DNL Search, Social, & Commerce].

[Klanten komen overeen met gebruikers-id&#39;s](https://support.google.com/google-ads/answer/9199250) werkt net als publiek met tags op de website, maar een niet-PII-id wordt toegewezen aan unieke publieksleden voor duidelijke voordelen ten opzichte van standaardklantovereenkomsten en op websites gebaseerde doelgroepen.

Als u de benodigde gebruikers-id&#39;s wilt maken, moet u een JavaScript-tag voor reclame voor Adobe gebruiken <!-- with a user ID parameter -->op uw websites. Neem contact op met het accountteam van uw Adobe voor meer informatie.

![segmentaanmaakproces](/help/integrations/assets/ad_search_user_id_pic.png)

Wanneer u het publiek hebt gemaakt, kunt u deze gebruiken in [!DNL Google Ads] campagnes als [streefcijfers of uitsluitingen op campagneniveau of op ad-groepsniveau](#audience-manager-targets).

### Gebruiken [!DNL Analytics] Segmenten voor doel- of uitsluitingsadvertenties {#analytics-targets}

* (Geopende adverteerders met [!DNL Search, Social, & Commerce]) U kunt alle [!DNL Google Ads] publiek dat [gemaakt met [!DNL Analytics] segmenten](#audience-manager-google-audiences) als streefdoelen of uitsluitingen op campagnereniveau of op ad-groepsniveau in uw [!DNL Google Ads] campagnes.

* (Adverteerders met DSP) U kunt uw bestaande [!DNL Analytics] segmenten als doelen voor uw advertentieplaatsen. U kunt de segmenten desgewenst opnemen in herbruikbare doelgroepen, die u kunt gebruiken als doelen of uitsluitingen voor meerdere plaatsingen.

* (Adverteerders met Creatief Adverteren) U kunt uw bestaande [!DNL Analytics] segmenten als doelen voor specifieke creatieve objecten in uw advertentie.
