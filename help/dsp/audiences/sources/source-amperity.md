---
title: Gebruikersnamen converteren van [!DNL Amperity] naar universele id's
description: Leer hoe u DSP kunt inschakelen om uw [!DNL Amperity] eerste-partijsegmenten.
feature: DSP Audiences
source-git-commit: 29fd744ba993e65b43cdf24a49b57208f0b06177
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# Gebruikersnamen converteren van [!DNL Amperity] naar universele id&#39;s

Gebruik de DSP integratie met de [!DNL Amperity] gegevensplatform van de klant om de gehashte e-mailadressen van de eerste partij van uw organisatie om te zetten in universele id&#39;s voor gerichte reclame.

1. (E-mailadressen converteren naar [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Tekstspatiëring instellen om in te schakelen [!DNL Analytics] meting](#analytics-tracking).

1. [Een publieksbron maken in DSP](#source-create).

1. [Segmenttoewijzingsgegevens voorbereiden en delen](#map-data).

1. [Een gegevenspush aanvragen van [!DNL Amperity] naar DSP](#push-data).

1. [Vergelijk het aantal universele id&#39;s met het aantal gehashte e-mailadressen](#compare-id-count).

## Stap 1: Tekstspatiëring instellen voor [!DNL Analytics] meting {#analytics-tracking}

*Adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

E-mailadressen converteren naar [!DNL RampIDs] of [!DNL ID5] In id&#39;s moet u het volgende doen:

1. (Als u dit nog niet hebt gedaan) Alle gegevens invullen [voorwaarden voor de uitvoering [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) en zorgt ervoor dat de [AMO-id en EF-id](/help/integrations/analytics/ids.md) worden ingevuld in uw URL&#39;s voor bijhouden.

1. Registreer u bij de partner voor de universele id en implementeer de specifieke code voor de universele id op uw webpagina&#39;s om de conversies van de id&#39;s in de webbrowsers voor bureaublad en mobiele apparaten (maar niet voor mobiele apps) aan te passen aan de doorzoekresultaten:

   * **Voor [!DNL RampIDs]:** U moet een extra JavaScript-tag op uw webpagina&#39;s implementeren om conversies van de id&#39;s in desktopbrowsers en mobiele webbrowsers (maar niet mobiele apps) aan te passen aan doorzoekacties. Neem contact op met het accountteam van de Adobe, dat u instructies geeft om u te registreren voor een [!DNL LiveRamp] [!DNL LaunchPad] tag van [!DNL LiveRamp] De Oplossingen van het Verkeer van de authentificatie. De registratie is gratis, maar u moet een overeenkomst ondertekenen. Nadat u zich hebt geregistreerd, genereert uw accountteam van de Adobe een unieke tag die uw organisatie op uw webpagina&#39;s kan implementeren.

## Stap 2: Een publieksbron maken in DSP {#source-create}

1. [Een publieksbron maken](source-manage.md) om soorten publiek te importeren naar uw DSP of een adverteerderaccount. U kunt uw gebruikers-id&#39;s omzetten in een van de [beschikbare Universal ID-indelingen](source-about.md).

   De bronmontages zullen een auto-geproduceerde bronsleutel omvatten, die u zult gebruiken om de segmentgegevens te duwen.

1. Nadat u de publieksbron creeert, deel de sleutel van de broncode met [!DNL Amperity] gebruiker.

## Stap 3: Voorbereiden en delen van segmenttoewijzingsgegevens {#map-data}

De adverteerder moet segmenttoewijzingsgegevens voorbereiden en delen.

1. Within [!DNL Amperity], hash de e-mailadressen voor het publiek via het algoritme SHA-256.

1. De adverteerder moet segment-kaartgegevens aan het Team van de Rekening van de Adobe geven om de segmenten in DSP tot stand te brengen. Gebruik de volgende kolomnamen en -waarden in een bestand met door komma&#39;s gescheiden waarden:

   * **Sleutel extern segment:** De [!DNL Amperity] segmentsleutel die aan het segment is gekoppeld.

   * **Segmentnaam:** De segmentnaam.

   * **Segmentbeschrijving:** Het doel of de regel van het segment, of allebei.

   * **Bovenliggende id:** Leeg houden

   * **Video CPM:** 0

   * **CPM weergeven:** 0

   * **Segmentvenster:** Het segment time-to-live.

## Stap 4: verzoek om een gegevenspush van [!DNL Amperity] naar DSP {#push-data}

1. Nadat het segment binnen DSP is toegewezen, moet de adverteerder met hun [!DNL Amperity] representatief om de segmentgegevens aan DSP te verdelen.

1. De adverteerder moet dan met het Team van de Rekening van de Adobe bevestigen dat de segmentgegevens werden ontvangen.

De segmenten moeten binnen 24 uur in DSP beschikbaar zijn en worden vernieuwd zoals geconfigureerd voor de adverteerder. Ongeacht hoe vaak het segment wordt vernieuwd, verloopt de opname in een segment na 30 dagen om ervoor te zorgen dat de privacy wordt nageleefd. Vernieuw dus het publiek door het opnieuw vanaf te drukken [!DNL Amperity] om de 30 dagen of minder.

## Stap 5: Vergelijk het aantal universele id&#39;s met het aantal gehashte e-mailadressen {#compare-id-count}

Nadat u alle stappen hebt uitgevoerd, controleert u het bestand in de publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen plaatsingsinstellingen) dat het segment beschikbaar is en binnen 24 uur vult. Vergelijk het aantal universele id&#39;s met het aantal originele hashed-e-mailadressen.

De vertaalsnelheid van gehashte e-mailadressen naar universele id&#39;s moet groter zijn dan 90%. Als u bijvoorbeeld 100 gehashte e-mailadressen verzendt van het gegevensplatform van uw klant, moeten deze worden vertaald naar meer dan 90 universele id&#39;s. Een vertaalsnelheid van 90% of minder is een probleem. Voor meer informatie over hoe de segmenttellingen kunnen variëren, zie &quot;[Oorzaken voor gegevensvariaties tussen e-mailadressen en universele id&#39;s](#universal-ids-data-variances).&quot;

Neem voor probleemoplossing contact op met uw accountteam van de Adobe of `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Ongeveer de Bronnen van het Publiek van de Eerste Partij](/help/dsp/audiences/sources/source-about.md)
>* [Bronnen voor publiek beheren om Universal ID-publiek te activeren](source-manage.md)
>* [Ondersteuning voor het activeren van Universal ID&#39;s](/help/dsp/audiences/universal-ids.md)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
