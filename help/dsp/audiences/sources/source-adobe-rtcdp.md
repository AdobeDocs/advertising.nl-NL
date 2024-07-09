---
title: Het gebruiken van de DSP Integratie met [!DNL Adobe] [!DNL Real-time CDP]
description: Leer hoe u DSP kunt inschakelen om uw [!DNL Adobe] [!DNL Real-time CDP] eerste-partijsegmenten.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# Gebruikersnamen converteren van [!DNL Adobe Real-Time CDP] naar universele id&#39;s

*Beta-functie*

Gebruik de DSP integratie met [de [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), onderdeel van de Adobe Experience Platform, om uw gehashte e-mailadressen om te zetten in universele id&#39;s voor gerichte advertenties.

1. (E-mailadressen converteren naar [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Tracking instellen voor [!DNL Analytics] meting:

   1. (Als u dit nog niet hebt gedaan) Alle gegevens invullen [voorwaarden voor de uitvoering [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) en de [AMO-id en EF-id in URL&#39;s voor bijhouden](/help/integrations/analytics/ids.md).

   1. Registreer u bij de partner voor de universele id en implementeer de specifieke code voor de universele id op uw webpagina&#39;s om de conversies van de id&#39;s in de webbrowsers voor bureaublad en mobiele apparaten (maar niet voor mobiele apps) aan te passen aan de doorzoekresultaten:

      * **Voor [!DNL RampIDs]:** U moet een extra JavaScript-tag op uw webpagina&#39;s implementeren om conversies van de id&#39;s in desktopbrowsers en mobiele webbrowsers (maar niet mobiele apps) aan te passen aan doorzoekacties. Neem contact op met het accountteam van de Adobe, dat u instructies geeft om u te registreren voor een [!DNL LiveRamp] [!DNL LaunchPad] tag van [!DNL LiveRamp] De Oplossingen van het Verkeer van de authentificatie. De registratie is gratis, maar u moet een overeenkomst ondertekenen. Nadat u zich hebt geregistreerd, genereert uw accountteam van de Adobe een unieke tag die uw organisatie op uw webpagina&#39;s kan implementeren.

1. [Een publieksbron maken](source-manage.md) om soorten publiek te importeren naar uw DSP of een adverteerderaccount. U kunt uw gebruikers-id&#39;s omzetten in een van de [beschikbare Universal ID-indelingen](source-about.md).

   De broninstellingen bevatten een automatisch gegenereerde bronsleutel die u in de volgende stap gebruikt.

1. In Adobe Experience Platform configureert u een Advertising DSP-doelverbinding met de [!UICONTROL Source Key] die is gegenereerd in de DSP broninstellingen.

   Voor instructies voor het activeren van de DSP bestemmingsverbinding, het selecteren van segmenten, en de toegang tot van controletoestemmingen, zie &quot;[Adobe Advertising Cloud DSP-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

   De bron-e-mailadressen moeten worden gehashed gebruikend het algoritme SHA-256.

1. Verifieer in uw publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen plaatsingsinstellingen) dat het segment vult en het aantal universele id&#39;s vergelijkt met het aantal oorspronkelijke gehashte e-mailadressen.

   De segmenten moeten binnen 24 uur in DSP beschikbaar zijn. Nadat DSP de segmentgegevens ontvangt, moet het aantal gebruikers binnen negen (9) uur zichtbaar zijn.

   Voor informatie over aanvaardbare ID vertaaltarieven en waarom de segmenttellingen kunnen variëren, zie &quot;[Gegevensvariaties tussen e-mailadressen en universele id&#39;s](#universal-ids-data-variances).&quot;

   Neem voor probleemoplossing contact op met uw accountteam van de Adobe of `adcloud-support@adobe.com`.

Segmenten worden elke 24 uur vernieuwd. Nochtans, verloopt de opneming in een segment na 30 dagen door gebrek of na een klant-gespecificeerde vervalperiode. Vernieuw uw segmenten door deze vóór het verlopen opnieuw vanuit Real-Time CDP te duwen. Neem contact op met het accountteam van de Adobe om een vervaldatum van een aangepast segment aan te vragen.

>[!MORELIKETHIS]
>
>* [Ongeveer de Bronnen van het Publiek van de Eerste Partij](/help/dsp/audiences/sources/source-about.md)
>* [Bronnen voor publiek beheren om Universal ID-publiek te activeren](source-manage.md)
>* [Adobe Advertising DSP-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Overzicht van de doelcatalogus](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Ondersteuning voor het activeren van Universal ID&#39;s](/help/dsp/audiences/universal-ids.md)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
