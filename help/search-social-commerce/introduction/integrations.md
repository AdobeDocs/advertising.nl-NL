---
title: Integratie met Adobe Experience Cloud-oplossingen en -services
description: Leer meer over de integratie van Zoeken, Sociale Zaken en Commerce met Adobe Experience Cloud-oplossingen en -services.
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: 3f91cd92a364a8e9dd569bd590c59740ea1493d7
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Integratie met Adobe Experience Cloud-oplossingen en -services

Advertising Search, Social &amp; Commerce is geïntegreerd met de volgende [!DNL Adobe] -producten.

* [ Markeringen van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) — U kunt de [ Uitbreiding van de Wolk van Adobe Advertising ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud) voor Adobe Experience Platform gebruiken om [ Adobe Advertising conversie volgende markeringen ](/help/search-social-commerce/tools/conversion-tag-generate.md), evenals derde volgende markeringen, voor uw advertentie het landen pagina&#39;s tot stand te brengen. Als uw organisatie geen rekening van Experience Platform heeft, dan kunt u de uitbreiding direct in het [ gebruikersinterface voor de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/#/data-collection/) installeren, die voor klanten van Adobe Experience Cloud vrij beschikbaar is.

  Als u de vereiste extensie wilt installeren, neemt u contact op met de systeembeheerder van uw organisatie voor toegang tot de functies voor gegevensverzameling in de gebruikersinterface en vraagt u deze om u de machtiging `manage_properties` te verlenen.

  **Nota:** u kunt conversie het volgen markeringen binnen Onderzoek, Sociaal ook [ tot stand brengen, &amp; Commerce ](/help/search-social-commerce/tools/conversion-tag-generate.md).

<!-- another link re tags, which is more direct within the tags docs but not very useful:  https://exchange.adobe.com/apps/ec/100155 -->

* Adobe Analytics — (Opt-in-functie) Adobe Advertising en [!DNL Analytics] zijn op de volgende manieren geïntegreerd:

   * Adobe Advertising en [!DNL Analytics] delen naadloos gegevens. [!DNL Analytics] kan gegevens over de betrokkenheid en conversie van de site dagelijks verzenden naar Zoeken, Sociaal en Commerce, waar de gegevens beschikbaar zijn voor optimalisatie van advertenties en voor rapportage. Bovendien kan Adobe Advertising dagelijks gegevens over advertentie-verkeer (inclusief indrukken, klikken en kosten) verzenden van uw advertentienetwerken naar [!DNL Analytics] , waar de gegevens beschikbaar zijn in alle rapportagetools.

     Zie &quot;[ Gesteunde Inventaris ](/help/search-social-commerce/introduction/supported-inventory.md)&quot;voor meer informatie over [!DNL Analytics] steun voor elk advertentienetwerk en advertentietype. Zie ook &quot;[ Overzicht van  [!DNL Analytics for Advertising] ](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}&quot;voor meer informatie over de gegevensuitwisseling.

     Adobe Advertising en [!DNL Analytics] moeten eerst zijn geconfigureerd voor gegevensuitwisseling. Neem contact op met uw Adobe-accountteam voor meer informatie over de eerste installatie.

     >[!NOTE]
     >
     >Standaard zijn de metriek van [!DNL Analytics] niet zichtbaar in de schermen Search, Social, &amp; Commerce. U moet uitdrukkelijk [ de metriek beschikbaar maken in de meningen, de portefeuilles, en de rapporten van het campagnebeheer ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) nadat het [!DNL Adobe] implementatieteam geselecteerde standaard of douanegebeurtenissen heeft gevormd om in Adobe Advertising over te gaan. U kunt de weergegeven metrische namen desgewenst wijzigen (zonder deze in [!DNL Analytics] te wijzigen). U kunt metriek viewable in UI maken en metriek anders noemen van [!UICONTROL Admin] > [!UICONTROL Conversions].

   * Advertisers met [!DNL Analytics] maar niet Audience Manager kunnen [  [!DNL Google Ads]  klantengelijke publiek ](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) van [!DNL Analytics] segmenten tot stand brengen die met Adobe Experience Cloud worden gedeeld. Om in aanmerking te komen, moet een adverteerder de [ Dienst van de Identiteit van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/id-service/using/home.html) uitvoeren en een markering op zijn websites opstellen. U kunt het publiek in [!DNL Google Ads] campagnes dan gebruiken als campagne-niveau of ad groep-niveau [ doelstellingen ](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) of [ uitsluitingen ](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* De segmenten van Adobe Audience Manager — (Opt-in eigenschap) u [ kunt  [!DNL Google Ads]  klanten tot gelijke publiek ](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) van de segmenten van Audience Manager leiden die Onderzoek, Sociale, &amp; Commerce als bestemming hebben. Dit kunnen [!DNL Analytics] segmenten zijn die naar Adobe Experience Cloud worden gepubliceerd en segmenten die met de Audience Library van Adobe Experience Cloud worden gemaakt. U kunt het publiek in [!DNL Google Ads] campagnes dan gebruiken als campagne-niveau of ad groep-niveau [ doelstellingen ](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) of [ uitsluitingen ](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

  Zie &quot;[ de Integraties van Adobe Advertising met Adobe Audience Manager ](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)&quot;voor meer informatie.

* Adobe Target — U kunt doorklikken-door signaal het delen tussen Onderzoek, Sociale, &amp; Commerce en [!DNL Target] uitvoeren, A/B testactiviteit in [!DNL Target] voor uw advertenties plaatsen, en dan [!DNL Analytics] Analysis Workspace gebruiken om de testgegevens te bekijken.

* Adobe Campaign — U kunt [ tot stand brengen en a  [!DNL Google Ads]  klantengelijke publiek bijwerken gebruikend een e-maillijst binnen  [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* De Meldingen van Adobe Experience Cloud — (Wanneer u door Adobe Experience Cloud) van de berichtverbinding ([ Waakzame Meldingen ](/help/search-social-commerce/assets/notifications-panel.png "Waarschuwingsmeldingen")) bij de bovenkant van elke pagina wordt het programma geopend, kunt u alle het systeemupdates van Adobe Experience Cloud, posten, verwijzingen, en gedeelde activa bekijken. Neem contact op met uw Adobe-accountteam voor informatie over toegang tot Adobe Experience Cloud.
