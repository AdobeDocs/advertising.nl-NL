---
title: De DSP-integratie gebruiken met  [!DNL Adobe] [!DNL Real-time CDP]
description: Leer hoe te om DSP toe te laten om uw  [!DNL Adobe] [!DNL Real-time CDP] eerste-partijsegmenten op te nemen.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 2dddf3560e1f98dab7158c28625bcd54b4efbdb2
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# Gebruikers-id&#39;s converteren van [!DNL Adobe Real-Time CDP] naar universele id&#39;s

*eigenschap van Beta*

Gebruik de integratie van DSP met [&#x200B;  [!DNL Adobe Real-Time CDP] &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=nl-NL), die deel van Adobe Experience Platform uitmaakt, om uw gebruiker IDs — met inbegrip van gehakte e-mailadressen, koekjes, en mobiele reclame IDs — aan universele IDs voor gerichte reclame om te zetten.

1. (Gebruikers-id&#39;s omzetten in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) ) Tekstspatiëring instellen voor [!DNL Analytics] -meting:

   1. (Als u dit nog niet hebt gedaan) Voltooi alle [&#x200B; eerste vereisten voor het uitvoeren van  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) en [&#x200B; identiteitskaart van AMO en identiteitskaart EF in uw het volgen URLs &#x200B;](/help/integrations/analytics/ids.md).

   1. Registreer u bij de partner voor de universele id en implementeer de specifieke code voor de universele id op uw webpagina&#39;s om de conversies van de id&#39;s in de webbrowsers voor bureaublad en mobiele apparaten (maar niet voor mobiele apps) aan te passen aan de doorzoekresultaten:

      * **voor [!DNL RampIDs]:** u moet een extra markering van JavaScript op uw webpagina&#39;s opstellen om omzettingen van identiteitskaarts op Desktop en mobiele Webbrowsers (maar niet mobiele apps) aan mening-door aan te passen. Neem contact op met uw Adobe-accountteam. Dit team geeft u instructies om u te registreren voor een [!DNL LiveRamp] [!DNL LaunchPad] -tag van [!DNL LiveRamp] Authentication Traffic Solutions. De registratie is gratis, maar u moet een overeenkomst ondertekenen. Nadat u zich hebt geregistreerd, genereert uw Adobe-accountteam een unieke tag die uw organisatie op uw webpagina&#39;s kan implementeren.

1. [&#x200B; creeer een publieksbron &#x200B;](source-manage.md) om publiek in uw rekening van DSP of een adverteerderrekening in te voeren. U kunt verkiezen om uw gebruikersherkenningstekens in om het even welke [&#x200B; beschikbare universele formaten van identiteitskaart &#x200B;](source-about.md) om te zetten.

   De broninstellingen bevatten een automatisch gegenereerde bronsleutel die u in de volgende stap gebruikt.

1. In Adobe Experience Platform configureert u een Advertising DSP-doelverbinding met de [!UICONTROL Source Key] die is gegenereerd in de DSP-broninstellingen.

   De e-mailadressen moeten worden gehakt gebruikend het algoritme SHA-256.

   Voor instructies voor het activeren van de de bestemmingsverbinding van DSP, het activeren van publiek, en het bevestigen van gegevensuitvoer, zie &quot;[&#x200B; de verbinding van Adobe Advertising DSP &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=nl-NL).&quot;

   >[!NOTE]
   >
   >De erfenisverbinding, die steun voor slechts gehakt e-mailadressen omvat, wordt nu genoemd &quot;[&#x200B; Verouderde de verbinding van DSP van de Advertising Cloud van Adobe Advertising &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection-legacy). Als u reeds de erfenisverbinding gebruikt, te hoeven u om geen veranderingen onmiddellijk aan te brengen. De verouderde verbinding wordt echter uiteindelijk verwijderd.

1. Controleer in de publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen de plaatsingsinstellingen) of het segment vult en vergelijk het aantal universele id&#39;s met het aantal oorspronkelijke gebruikers-id&#39;s.

   De segmenten moeten binnen 24 uur beschikbaar zijn in DSP. Nadat DSP de segmentgegevens heeft ontvangen, moet het aantal gebruikers binnen negen (9) uur zichtbaar zijn. Voor informatie over aanvaardbare identiteitskaart vertaaltarieven en waarom de segmenttellingen kunnen variëren, zie &quot;[&#x200B; de variaties van Gegevens tussen e-mail IDs en universele IDs &#x200B;](#universal-ids-data-variances).&quot;

Segmenten worden elke 24 uur vernieuwd. Nochtans, verloopt de opneming in een segment na 30 dagen door gebrek of na een klant-gespecificeerde vervalperiode. Vernieuw uw segmenten door deze vóór het verlopen opnieuw vanuit Real-Time CDP te duwen. Neem contact op met uw Adobe-accountteam als u een aanvraag wilt indienen voor het verlopen van een aangepast segment.

## Problemen oplossen

Om vertaaltarief en gebruikerstellingskwesties problemen op te lossen, zie &quot;[&#x200B; Steun voor het activeren van universele IDs &#x200B;](/help/dsp/audiences/universal-ids.md).&quot;

Neem contact op met uw Adobe-accountteam of `adcloud-support@adobe.com` om problemen met de conversieprocedure op te lossen.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer eerste-partijpublieksbronnen &#x200B;](/help/dsp/audiences/sources/source-about.md)
>* [&#x200B; beheert publieksbronnen om universele identiteitskaart te activeren &#x200B;](source-manage.md)
>* [&#x200B; verbinding van Adobe Advertising DSP &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=nl-NL)
>* Adobe Experience Platform [&#x200B; het catalogusoverzicht van Doelen &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html?lang=nl-NL)
>* [&#x200B; Steun voor het activeren van Universal IDs &#x200B;](/help/dsp/audiences/universal-ids.md)
>* [&#x200B; Ongeveer publieksbeheer &#x200B;](/help/dsp/audiences/audience-about.md)
