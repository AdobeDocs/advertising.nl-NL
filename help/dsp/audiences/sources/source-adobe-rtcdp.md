---
title: Het gebruiken van de DSP Integratie met  [!DNL Adobe] [!DNL Real-time CDP]
description: Leer hoe te om DSP toe te laten om uw  [!DNL Adobe] [!DNL Real-time CDP] eerste-partijsegmenten in te voeren.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 3a641db6b145e67e6e1f1daca271dd524973e075
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Gebruikersnamen converteren van [!DNL Adobe Real-Time CDP] naar universele id&#39;s

*eigenschap van Beta*

Gebruik de DSP integratie met [&#x200B;  [!DNL Adobe Real-Time CDP] &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=nl-NL), die deel van Adobe Experience Platform uitmaakt, om uw gehakt e-mailadressen in universele IDs voor gerichte reclame om te zetten.

1. (E-mailadressen omzetten in [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Tekstspatiëring instellen voor [!DNL Analytics] meting:

   1. (Als u dit nog niet hebt gedaan) Voltooi alle [&#x200B; eerste vereisten voor het uitvoeren van  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) en [&#x200B; identiteitskaart van AMO en identiteitskaart EF in uw het volgen URLs &#x200B;](/help/integrations/analytics/ids.md).

   1. Registreer u bij de partner voor de universele id en implementeer de specifieke code voor de universele id op uw webpagina&#39;s om de conversies van de id&#39;s in de webbrowsers voor bureaublad en mobiele apparaten (maar niet voor mobiele apps) aan te passen aan de doorzoekresultaten:

      * **voor [!DNL RampIDs]:** u moet een extra markering van JavaScript op uw webpagina&#39;s opstellen om omzettingen van identiteitskaarts op Desktop en mobiele Webbrowsers (maar niet mobiele apps) aan mening-door aan te passen. Neem contact op met het accountteam van de Adobe, dat u instructies zal geven om u te registreren voor een [!DNL LiveRamp] [!DNL LaunchPad] -tag van [!DNL LiveRamp] Authentication Traffic Solutions. De registratie is gratis, maar u moet een overeenkomst ondertekenen. Nadat u zich hebt geregistreerd, genereert uw accountteam van de Adobe een unieke tag die uw organisatie op uw webpagina&#39;s kan implementeren.

1. [&#x200B; creeer een publieksbron &#x200B;](source-manage.md) om publiek in uw DSP rekening of een adverteerderrekening in te voeren. U kunt verkiezen om uw gebruikersherkenningstekens in om het even welke [&#x200B; beschikbare universele formaten van identiteitskaart &#x200B;](source-about.md) om te zetten.

   De broninstellingen bevatten een automatisch gegenereerde bronsleutel die u in de volgende stap gebruikt.

1. In Adobe Experience Platform configureert u een Advertising DSP-doelverbinding met de [!UICONTROL Source Key] die is gegenereerd in de DSP broninstellingen.

   Voor instructies om de DSP bestemmingsverbinding te activeren, die segmenten, en tot controletoestemmingen toegang hebben, zie &quot;[&#x200B; verbinding van Adobe Advertising Cloud DSP &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=nl-NL).&quot;

   De bron-e-mailadressen moeten worden gehashed gebruikend het algoritme SHA-256.

1. Controleer in uw publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen de plaatsingsinstellingen) of het segment vult en vergelijk het aantal universele id&#39;s met het aantal oorspronkelijke gehashte e-mailadressen.

   De segmenten moeten binnen 24 uur in DSP beschikbaar zijn. Nadat DSP de segmentgegevens ontvangt, moet het aantal gebruikers binnen negen (9) uur zichtbaar zijn. Voor informatie over aanvaardbare identiteitskaart vertaaltarieven en waarom de segmenttellingen kunnen variëren, zie &quot;[&#x200B; Varianties van Gegevens tussen E-mail IDs en Universele IDs &#x200B;](#universal-ids-data-variances).&quot;

Segmenten worden elke 24 uur vernieuwd. Nochtans, verloopt de opneming in een segment na 30 dagen door gebrek of na een klant-gespecificeerde vervalperiode. Vernieuw uw segmenten door deze vóór het verlopen opnieuw vanuit Real-Time CDP te duwen. Neem contact op met het accountteam van de Adobe om een vervaldatum van een aangepast segment aan te vragen.

## Problemen oplossen

Om vertaaltarief en gebruikerstellingskwesties problemen op te lossen, zie &quot;[&#x200B; Steun voor het Activeren van Universal IDs &#x200B;](/help/dsp/audiences/universal-ids.md).&quot;

Neem contact op met het accountteam van de Adobe of `adcloud-support@adobe.com` om problemen met de conversieprocedure op te lossen.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer de Bronnen van het Publiek van de Eerste Partij &#x200B;](/help/dsp/audiences/sources/source-about.md)
>* [&#x200B; beheert de Bronnen van het Publiek om Universele Soorten van identiteitskaart &#x200B;](source-manage.md) te activeren
>* [&#x200B; Verbinding van Adobe Advertising DSP &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=nl-NL)
>* Adobe Experience Platform [&#x200B; het catalogusoverzicht van Doelen &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html?lang=nl-NL)
>* [&#x200B; Steun voor het Activeren van Universal IDs &#x200B;](/help/dsp/audiences/universal-ids.md)
>* [&#x200B; Ongeveer het Beheer van het Publiek &#x200B;](/help/dsp/audiences/audience-about.md)
