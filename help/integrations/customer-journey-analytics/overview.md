---
title: Overzicht van de integratie tussen Adobe Advertising en Adobe Customer Journey Analytics
description: Meer informatie over opties voor de integratie van Adobe Advertising met Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
exl-id: 57636259-f91a-404f-b972-994af67098b1
source-git-commit: 545dcedda0a593ebd3424cda33e5c85a7fb7a28d
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Overzicht van de integratie tussen Adobe Advertising en Customer Journey Analytics

<!-- title? If I change, change refs throughout -->

*Advertisers met Advertising DSP en[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising is geïntegreerd met Adobe Customer Journey Analytics voor tweerichtingsgegevensuitwisseling en -rapportage. U hebt twee opties om de integratie in te stellen:

* Adverteerders met zowel [!DNL Analytics for Advertising] als Customer Journey Analytics beschikken over dezelfde functionaliteit als [!DNL Analytics for Advertising] , met toevoeging van visuele effecten in Customer Journey Analytics.

  U zult klik-door gebeurtenissen nog volgen gebruikend het Web SDK van Adobe Experience Platform (`alloy.js`) of de Dienst van de Identiteit van Adobe Experience Cloud (`visitorAPI.js`). Adverteerders met Advertising DSP gebruiken nog steeds een JavaScript-fragment om doorkijkgebeurtenissen bij te houden. De gegevens die beschikbaar zijn in Customer Journey Analytics zijn onder meer:

   * Campagne-prestatiegegevens van Adobe Advertising in Customer Journey Analytics

   * Site-activiteit en conversies bijgehouden door [!DNL Google Ads] en [!DNL Microsoft Advertising] in Customer Journey Analytics, dagelijks bijgewerkt

   * Attributiegegevens van [!DNL Analytics] in Adobe Advertising, waar deze kunnen worden gebruikt voor optimalisatie en rapportage

  In dit gebruiksgeval, te hoeven u om het even welke extra stappen behalve naar keuze uit te voeren [ gegevens voor AMO IDs en EF IDs voor gebruik in Customer Journey Analytics ](/help/integrations/analytics/rvars-to-evars.md) verzamelen.

* (De aanstaande bèta eigenschap) Advertisers met Customer Journey Analytics maar niet [!DNL Analytics for Advertising] kunnen gegevens tussen Adobe Advertising en Customer Journey Analytics nefaste uitwisseling gebruikend [ Adobe Experience Platform  [!DNL Web SDK] ](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=nl-NL) bibliotheek (`alloy.js`). U kunt plaatsgebeurtenissen volgen gebruikend koekjes, gehakt IP, en universele IDs ([!DNL LiveRamp RampIDs] en ID5 IDs) en de gebeurtenissen van de attributenplaats aan betaalde media activiteit. De volgende gegevens zijn beschikbaar op de campagne-, ad-group-, package-, placement- en trefwoordniveaus:

   * Campagne-prestatiegegevens van Adobe Advertising in Customer Journey Analytics

     **Nota:** Gegevens van [!DNL Apple] en [!DNL Tiktok] is niet beschikbaar.

   * Siteactiviteit en conversies die door [!DNL Google Ads] en [!DNL Microsoft Advertising] in Customer Journey Analytics worden bijgehouden

   * Attributiegegevens van Customer Journey Analytics in Adobe Advertising, waar deze kunnen worden gebruikt voor optimalisatie en rapportage

  In dit geval kunt u Web SDK gebruiken om sitegebeurtenissen bij te houden (met behulp van cookies, gehashte IP-adressen of universele id&#39;s) en de sitegebeurtenissen aan betaalde mediaconcentraties in [!DNL Google Ads] , [!DNL Microsoft Advertising] en [!DNL Meta] en Adobe DSP te koppelen. U gebruikt ook Adobe Experience Platform voor gegevensverzameling.

## Een eigen integratie tussen Adobe Advertising en Customer Journey Analytics op gang brengen

Neem contact op met uw Adobe-accountteam, dat de initiële configuratie die nodig is om te beginnen, zal voltooien en u zal helpen uw implementatie en gegevensgebruik te plannen op basis van de behoeften van uw organisatie.

>[!MORELIKETHIS]
>
>* [ Eerste vereisten ](prerequisites.md)
>* (de gebruikers van Adobe Analytics) [ verzamel Historische Gegevens voor AMO IDs en EF IDs voor Gebruik in Adobe Customer Journey Analytics ](/help/integrations/analytics/rvars-to-evars.md).
