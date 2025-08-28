---
title: Voorwaarden voor de integratie van Adobe Advertising met Customer Journey Analytics
description: Voorwaarden voor de integratie van Adobe Advertising met Customer Journey Analytics
feature: Integration with Adobe Customer Journey Analytics
exl-id: 4bd14178-5003-4da6-9034-d070c57f0e9b
source-git-commit: 194675147b64af37de6373116f246f1e61388a23
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Voorwaarden voor de integratie van Adobe Advertising met Customer Journey Analytics

*Advertisers met Advertising DSP en[!DNL Advertising Search, Social, & Commerce]*

* Adverteerders met zowel [!DNL Analytics for Advertising] als Customer Journey Analytics:

   * Adobe Customer Journey Analytics<!-- any specific version? -->

   * [ Alle andere eerste vereisten voor  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md).

* Adverteerders met Customer Journey Analytics, maar niet [!DNL Analytics for Advertising]:

   * Adobe Experience Platform Web SDK-bibliotheek: `alloy.js`

     De [!DNL Org ID] die wordt gebruikt voor Web SDK en voor de Adobe Advertising-advertentieaccount, moet hetzelfde zijn. U kunt dit identiteitskaart op het [ Summiere lusje van Debugger van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) vinden.

     ![ het Summiere scherm van Foutopsporing van de Wolk van de Ervaring ](/help/integrations/assets/a4adc-debugger-summary.png)

     U hebt ondersteuning nodig van uw Experience Platform-sitebeheerder om een Experience Platform-gegevensstroom en XDM-schema te maken.

   * Adobe Customer Journey Analytics<!-- any specific version? -->

     U zult steun van uw interne Webanalist aan opstelling een verbinding aan uw dataset nodig hebben en rapportering vormen.

>[!TIP]
>
>Gebruik de meest recente versie van elke bibliotheek om de gegevensgetrouwheid te verbeteren.

>[!MORELIKETHIS]
>
>* [ Overzicht ](overview.md)
>* (de gebruikers van Adobe Analytics) [ verzamel Historische Gegevens voor AMO IDs en EF IDs voor Gebruik in Adobe Customer Journey Analytics ](/help/integrations/analytics/rvars-to-evars.md).
