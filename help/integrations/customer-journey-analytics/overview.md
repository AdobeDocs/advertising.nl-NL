---
title: Overzicht van de integratie tussen Adobe Advertising en Adobe Customer Journey Analytics
description: Meer informatie over opties voor de integratie van Adobe Advertising met Adobe Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: ed3c3b4331b743d0c40f04fb8543c535d80ca1d5
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Overzicht van de integratie tussen Adobe Advertising en Customer Journey Analytics

<!-- title? If I change, change refs throughout -->

*Advertisers met Advertising DSP en[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising is geïntegreerd met Adobe Customer Journey Analytics voor tweerichtingsgegevensuitwisseling. U hebt twee opties om de integratie in te stellen:

* Adverteerders met zowel [!DNL Analytics for Advertising] als Customer Journey Analytics beschikken over dezelfde functionaliteit als [!DNL Analytics for Advertising] , met toevoeging van visuele effecten in Customer Journey Analytics.

  U zult klik-door gebeurtenissen nog volgen gebruikend het Web SDK van Adobe Experience Platform (`alloy.js`) of de Dienst van de Identiteit van Adobe Experience Cloud (`visitorAPI.js`). Adverteerders met Advertising DSP gebruiken nog steeds een JavaScript-fragment om doorkijkgebeurtenissen bij te houden. De gegevens die beschikbaar zijn in Customer Journey Analytics zijn onder meer:

   * Prestatiegegevens van campagnes vanuit Adobe Advertising

     **Nota:** Gegevens van [!DNL Apple] en [!DNL Tiktok] is niet beschikbaar.

   * Site-activiteit en conversies die worden bijgehouden door [!DNL Google Ads] , [!DNL Microsoft Advertising] en [!DNL Meta]

   * Attributiegegevens van [!DNL Analytics] die kunnen worden gebruikt voor optimalisatie en rapportage in Adobe Advertising

  In dit gebruiksgeval, te hoeven u om het even welke extra stappen behalve naar keuze uit te voeren [ gegevens voor AMO IDs en EF IDs voor gebruik in Customer Journey Analytics ](/help/integrations/analytics/rvars-to-evars.md) verzamelen.

* (De aanstaande bètaeigenschap) Adverteerders met Customer Journey Analytics maar niet [!DNL Analytics for Advertising] kunnen de volgende gegevens tussen Adobe Advertising en Customer Journey Analytics native ruilen door klikthrough en mening-through gebeurtenissen te volgen gebruikend Adobe Experience Platform Web SDK (`alloy.js`). De gegevens zijn beschikbaar bij de campagne, de groep, het pakket, de plaatsing, en sleutelwoordniveaus.

   * Prestatiegegevens van campagnes vanuit Adobe Advertising

     **Nota:** Gegevens van [!DNL Apple] en [!DNL Tiktok] is niet beschikbaar.

   * Site-activiteit en conversies die worden bijgehouden door [!DNL Google Ads] , [!DNL Microsoft Advertising] en [!DNL Meta]

   * Attributiegegevens van Customer Journey Analytics, die kunnen worden gebruikt voor optimalisatie en rapportage in Adobe Advertising

  **Nota:** Geen biologische gegevens is nog beschikbaar.<!-- Does that belong somewhere up above? -->

  In dit geval kunt u Web SDK gebruiken om sitegebeurtenissen bij te houden (met behulp van cookies, gehashte IP-adressen of universele id&#39;s) en de sitegebeurtenissen aan betaalde mediaconcentraties in [!DNL Google Ads] , [!DNL Microsoft Advertising] en [!DNL Meta] en Adobe DSP te koppelen. U gebruikt ook Adobe Experience Platform voor gegevensverzameling.

## Een eigen integratie tussen Adobe Advertising en Customer Journey Analytics op gang brengen

Neem contact op met uw Adobe-accountteam, dat de initiële configuratie die nodig is om te beginnen, zal voltooien en u zal helpen uw implementatie en gegevensgebruik te plannen op basis van de behoeften van uw organisatie.

>[!MORELIKETHIS]
>
>* [ Eerste vereisten ](prerequisites.md)
>* (de gebruikers van Adobe Analytics) [ verzamel Historische Gegevens voor AMO IDs en EF IDs voor Gebruik in Adobe Customer Journey Analytics ](/help/integrations/analytics/rvars-to-evars.md).
