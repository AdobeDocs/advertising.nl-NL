---
title: Integratie met Adobe Experience Cloud-oplossingen en -services
description: Leer over de integratie van Zoeken, Sociale Zaken & Handel met de oplossingen en de diensten van Adobe Experience Cloud.
exl-id: e8b521f5-f426-4c50-9df4-361a047c9ff0
feature: Search Introduction
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Integratie met Adobe Experience Cloud-oplossingen en -services

Zoeken naar advertenties, sociale zaken en handel is geïntegreerd met het volgende: [!DNL Adobe] producten.

* [Labels uit Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html?lang=nl-NL) — U kunt de [Adobe Advertising Cloud-extensie](https://exchange.adobe.com/apps/ec/100155) voor Adobe Experience Platform om tags voor conversie van Adoben Advertising en trackingtags van derden te maken voor uw bestemmingspagina&#39;s. (U kunt [direct tags voor conversie bijhouden maken in Zoeken, Sociale zaken en Handel](/help/search-social-commerce/tools/conversion-tag-generate.md).) Neem contact op met uw Adobe-accountteam of -implementatieteam voor informatie die u in uw tags wilt opnemen.

* Adobe Analytics — (Opt-in-functie) Adobe Advertising en [!DNL Analytics] zijn op de volgende manieren geïntegreerd:

   * Adobe Advertising en [!DNL Analytics] gegevens naadloos delen. [!DNL Analytics] kan gegevens over de betrokkenheid en conversie van de site dagelijks verzenden naar Zoeken, Sociale Zaken en Handel, waar de gegevens beschikbaar zijn voor optimalisatie en rapportage. Ook, kan de Adobe Advertising en verkeersgegevens - met inbegrip van indrukkingen, klikken, en kosten - van uw advertentienetwerken dagelijks verzenden aan [!DNL Analytics], indien de gegevens beschikbaar zijn in alle rapportageinstrumenten.

     Zie &quot;[Ondersteunde voorraad](/help/search-social-commerce/introduction/supported-inventory.md)&quot; voor meer informatie over [!DNL Analytics] ondersteuning voor elk advertentienetwerk en advertentietype. Zie ook &quot;[Overzicht van [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=nl-NL){target="_blank"}&quot; voor meer informatie over de gegevensuitwisseling .

     Om gegevens uit te wisselen, zowel Adobe Advertising als [!DNL Analytics] moet aanvankelijk worden geconfigureerd. Neem contact op met het accountteam van uw Adobe voor meer informatie over de eerste configuratie.

     >[!NOTE]
     >
     >Standaard worden de [!DNL Analytics] metriek zijn niet zichtbaar in de schermen Zoeken, Sociale Zaken en Handel. U moet expliciet [stelt de metriek beschikbaar in de meningen, de portefeuilles, en de rapporten van het campagnebeheer](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) na de [!DNL Adobe] Het implementatieteam heeft geselecteerde standaard- of aangepaste gebeurtenissen geconfigureerd om over te gaan naar de Adobe Advertising. U kunt de weergegeven metrische namen desgewenst wijzigen (zonder ze te wijzigen in [!DNL Analytics]). U kunt metriek viewable in UI maken en metriek anders noemen van [!UICONTROL Admin] > [!UICONTROL Conversions].

   * Adverteerders met [!DNL Analytics] maar Audience Manager kan niet [maken [!DNL Google Ads] publiek klantovereenkomst](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) van [!DNL Analytics] segmenten die met Adobe Experience Cloud worden gedeeld. Om in aanmerking te komen moet een adverteerder de [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=nl-NL) en implementeert u een tag op de websites. Vervolgens kunt u het publiek gebruiken in [!DNL Google Ads] campagnes op campagneniveau of op groepsniveau [streefdoelen](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) of [uitsluitingen](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Adobe Audience Manager-segmenten — (functie Inschakelen) U kunt [maken [!DNL Google Ads] publiek klantovereenkomst](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) van de segmenten van de Audience Manager die Onderzoek, Sociale, &amp; Handel als bestemming hebben. Dit kan [!DNL Analytics] segmenten die worden gepubliceerd naar Adobe Experience Cloud en segmenten die worden gemaakt met de Adobe Experience Cloud Audience Library. Vervolgens kunt u het publiek gebruiken in [!DNL Google Ads] campagnes op campagneniveau of op groepsniveau [streefdoelen](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) of [uitsluitingen](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

  Zie &quot;[Integratie van Adobe Advertising met Adobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html?lang=nl-NL)&quot; voor meer informatie .

* Adobe Target — U kunt doorklikken-door signaal het delen tussen Onderzoek, Sociale, &amp; Handel uitvoeren en [!DNL Target]een A/B-testactiviteit in [!DNL Target] voor uw advertenties en gebruik vervolgens [!DNL Analytics] Analysis Workspace om de testgegevens weer te geven.

* Adobe Campaign — Je kan [een [!DNL Google Ads] klant stemt publiek overeen met gebruik van een e-maillijst in [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Adobe Experience Cloud-berichten — (Wanneer u bent aangemeld via Adobe Experience Cloud) Via de koppeling voor meldingen ([Waarschuwingsmeldingen](/help/search-social-commerce/assets/notifications-panel.png "Waarschuwingsmeldingen")) boven aan elke pagina kunt u alle updates, posts, opmerkingen en gedeelde elementen van het Adobe Experience Cloud-systeem weergeven. Neem contact op met het accountteam van uw Adobe voor informatie over toegang tot Adobe Experience Cloud.
