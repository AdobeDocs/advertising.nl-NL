---
title: Het gebruiken van de DSP Integratie met [!DNL Adobe] [!DNL Real-time CDP]
description: Leer hoe u DSP kunt inschakelen om uw [!DNL Adobe] [!DNL Real-time CDP] eerste-partijsegmenten.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: bd0586516c2457e4dfcd1a23046707e8bf652e3b
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Gebruikersnamen converteren van [!DNL Adobe Real-Time CDP] naar universele id&#39;s

*Beta, functie*

Gebruik de DSP integratie met [de [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), onderdeel van de Adobe Experience Platform, om uw gehashte e-mailadressen om te zetten in universele id&#39;s voor gerichte advertenties.

1. (E-mailadressen converteren naar [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Tracking instellen voor [!DNL Analytics] meting:

   1. (Als u dit nog niet hebt gedaan) Alle gegevens invullen [voorwaarden voor de uitvoering [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) en de [AMO-id en EF-id in URL&#39;s voor bijhouden](/help/integrations/analytics/ids.md).

   1. Registreer u bij de partner voor de universele id en implementeer de specifieke code voor de universele id op uw webpagina&#39;s om de conversies van de id&#39;s in de webbrowsers voor bureaublad en mobiele apparaten (maar niet voor mobiele apps) aan te passen aan de doorzoekresultaten:

      * **Voor [!DNL RampIDs]:** U moet een extra JavaScript-tag op uw webpagina&#39;s implementeren om conversies van de id&#39;s in desktopbrowsers en mobiele webbrowsers (maar niet mobiele apps) aan te passen aan doorzoekacties. Neem contact op met het accountteam van de Adobe, dat u instructies geeft om u te registreren voor een [!DNL LiveRamp] [!DNL LaunchPad] tag van [!DNL LiveRamp] De Oplossingen van het Verkeer van de authentificatie. De registratie is gratis, maar u moet een overeenkomst ondertekenen. Nadat u zich hebt geregistreerd, genereert uw accountteam van de Adobe een unieke tag die uw organisatie op uw webpagina&#39;s kan implementeren.

1. [Een publieksbron maken](source-create.md) om soorten publiek te importeren naar uw DSP of een adverteerderaccount. U kunt uw gebruikers-id&#39;s omzetten in een van de [beschikbare Universal ID-indelingen](source-about.md).

   De broninstellingen bevatten een automatisch gegenereerde bronsleutel die u in de volgende stap gebruikt.

1. In Adobe Experience Platform configureert u een DSP voor advertentie met de [!UICONTROL Source Key] die is gegenereerd in de DSP broninstellingen.

   Voor instructies voor het activeren van de DSP bestemmingsverbinding, het selecteren van segmenten, en de toegang tot van controletoestemmingen, zie &quot;[Adobe Advertising Cloud DSP-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

   De bron-e-mailadressen moeten worden gehashed gebruikend het algoritme SHA-256.

1. Nadat u alle stappen hebt uitgevoerd, controleert u het bestand in de publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen plaatsingsinstellingen) dat het segment binnen 24 uur vult. Vergelijk het aantal universele id&#39;s met het aantal originele hashed-e-mailadressen.

   De vertaalsnelheid van gehashte e-mailadressen naar universele id&#39;s moet groter zijn dan 90%. Als u bijvoorbeeld 100 gehashte e-mailadressen verzendt van het gegevensplatform van uw klant, moeten deze worden vertaald naar meer dan 90 universele id&#39;s. Een vertaalsnelheid van 90% of minder is een probleem. Voor meer informatie over hoe de segmenttellingen kunnen variëren, zie &quot;[Oorzaken voor gegevensvariaties tussen e-mailadressen en universele id&#39;s](#universal-ids-data-variances).&quot;

   Neem voor probleemoplossing contact op met uw accountteam van de Adobe of `adcloud-support@adobe.com`.

Segmenten worden elke 24 uur vernieuwd. Opname in een segment verloopt echter na 30 dagen om ervoor te zorgen dat de privacy wordt gerespecteerd. Vernieuw daarom het publiek door ze om de 30 dagen opnieuw van Real-Time CDP te verdringen.

>[!MORELIKETHIS]
>
>* [Een doelbron maken om Universal ID-publiek te activeren](source-create.md)
>* [Broninstellingen voor publiek](source-settings.md)
>* [Adobe Advertising DSP-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Overzicht van de doelcatalogus](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Geverifieerde segmenten handmatig importeren uit [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Gebruikersnamen converteren van [!DNL Tealium] naar universele id&#39;s](/help/dsp/audiences/sources/source-tealium.md)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)

<!--
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
-->
