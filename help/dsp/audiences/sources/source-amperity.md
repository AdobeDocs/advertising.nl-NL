---
title: Zet gebruiker IDs van  [!DNL Amperity]  in Universele IDs om
description: Leer hoe te om DSP toe te laten om uw  [!DNL Amperity]  eerste-partijsegmenten in te voeren.
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Gebruikers-id&#39;s converteren van [!DNL Amperity] naar universele id&#39;s

*eigenschap van Beta*

Gebruik de DSP-integratie met het [!DNL Amperity] -klantgegevensplatform om de gehashte e-mailadressen van de eerste partij van uw organisatie om te zetten in universele id&#39;s voor gerichte advertenties.

1. (Om e-mailadressen in [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> om te zetten; adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [ Opstelling het volgen om  [!DNL Analytics]  meting ](#analytics-tracking) toe te laten.

1. [ creeer een publieksbron in DSP ](#source-create).

1. [ voorbereidingen treffen en deel segment-afbeelding gegevens ](#map-data).

1. [ Verzoek om een gegevensduw van  [!DNL Amperity]  aan DSP ](#push-data).

1. [ vergelijk het aantal universele IDs met het aantal gehakte e-mailadressen ](#compare-id-count).

## Stap 1: Tekstspatiëring instellen voor [!DNL Analytics] -meting {#analytics-tracking}

*Advertisers met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Als u e-mailadressen wilt converteren naar [!DNL RampIDs] - of [!DNL ID5] -id&#39;s, moet u het volgende doen:

1. (Als u dit nog niet hebt gedaan) voltooi alle [ eerste vereisten voor het uitvoeren van  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) en zorg ervoor dat [ identiteitskaart van AMO en identiteitskaart EF ](/help/integrations/analytics/ids.md) in uw het volgen URLs wordt bevolkt.

1. Registreer u bij de partner voor de universele id en implementeer de specifieke code voor de universele id op uw webpagina&#39;s om de conversies van de id&#39;s in de webbrowsers voor bureaublad en mobiele apparaten (maar niet voor mobiele apps) aan te passen aan de doorzoekresultaten:

   * **voor [!DNL RampIDs]:** u moet een extra markering van JavaScript op uw webpagina&#39;s opstellen om omzettingen van identiteitskaarts op Desktop en mobiele Webbrowsers (maar niet mobiele apps) aan mening-door aan te passen. Neem contact op met uw Adobe-accountteam. Dit team geeft u instructies om u te registreren voor een [!DNL LiveRamp] [!DNL LaunchPad] -tag van [!DNL LiveRamp] Authentication Traffic Solutions. De registratie is gratis, maar u moet een overeenkomst ondertekenen. Nadat u zich hebt geregistreerd, genereert uw Adobe-accountteam een unieke tag die uw organisatie op uw webpagina&#39;s kan implementeren.

## Stap 2: Een publieksbron maken in DSP {#source-create}

1. [ creeer een publieksbron ](source-manage.md) om publiek in uw rekening van DSP of een adverteerderrekening in te voeren. U kunt verkiezen om uw gebruikersherkenningstekens in om het even welke [ beschikbare universele formaten van identiteitskaart ](source-about.md) om te zetten.

   De bronmontages zullen een auto-geproduceerde bronsleutel omvatten, die u zult gebruiken om de segmentgegevens te duwen.

1. Nadat u de publieksbron hebt gemaakt, deelt u de broncodesleutel met de [!DNL Amperity] -gebruiker.

## Stap 3: Voorbereiden en delen van segmenttoewijzingsgegevens {#map-data}

De adverteerder moet segmenttoewijzingsgegevens voorbereiden en delen.

1. Koppel binnen [!DNL Amperity] de e-mailadressen aan voor het publiek met behulp van het algoritme SHA-256.

1. De adverteerder moet segmenttoewijzingsgegevens aan het Adobe Account Team geven om de segmenten in DSP te maken. Gebruik de volgende kolomnamen en -waarden in een bestand met door komma&#39;s gescheiden waarden:

   * **Externe Sleutel van het Segment:** De [!DNL Amperity] segmentsleutel verbonden aan het segment.

   * **Naam van het segment:** de segmentnaam.

   * **Beschrijving van het Segment:** Het doel of de regel van het segment, of allebei.

   * **identiteitskaart van de Ouder:** houd leeg

   * **Video CPM:** 0

   * **Vertoning CPM:** 0

   * **Venster van het Segment:** de segment tijd-aan-levende.

## Stap 4: Vraag een gegevenspush aan van [!DNL Amperity] naar DSP {#push-data}

1. Nadat het segment in DSP is toegewezen, moet de adverteerder met zijn [!DNL Amperity] vertegenwoordiger samenwerken om de segmentgegevens naar DSP te verspreiden.

1. De adverteerder moet vervolgens met het Adobe Account Team bevestigen dat de segmentgegevens zijn ontvangen.

De segmenten moeten binnen 24 uur beschikbaar zijn in DSP. Controleer in de publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen de plaatsingsinstellingen) of het segment beschikbaar en gevuld is.

De segmenten worden vernieuwd op de manier die voor de adverteerder is geconfigureerd in [!DNL Amperity] . Ongeacht hoe vaak het segment wordt verfrist, verloopt de opneming in een segment na 30 dagen door gebrek of na een klant-gespecificeerde vervalperiode. Vernieuw de segmenten door deze vóór het verlopen opnieuw te duwen vanuit [!DNL Amperity] . Neem contact op met uw Adobe-accountteam als u een aanvraag wilt indienen voor het verlopen van een aangepast segment.

## Stap 5: Vergelijk het aantal universele id&#39;s met het aantal gehashte e-mailadressen {#compare-id-count}

Nadat DSP de segmentgegevens heeft ontvangen, moet het aantal gebruikers binnen negen (9) uur zichtbaar zijn.

Vergelijk in de publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen de plaatsingsinstellingen) het aantal universele id&#39;s met het aantal oorspronkelijke gehashte e-mailadressen. Voor informatie over aanvaardbare identiteitskaart vertaaltarieven en waarom de segmenttellingen kunnen variëren, zie &quot;[ Varianties van Gegevens tussen E-mail IDs en Universele IDs ](#universal-ids-data-variances).&quot;

## Problemen oplossen

Om vertaaltarief en gebruikerstellingskwesties problemen op te lossen, zie &quot;[ Steun voor het Activeren van Universal IDs ](/help/dsp/audiences/universal-ids.md).&quot;

Neem contact op met uw Adobe-accountteam of `adcloud-support@adobe.com` om problemen met de conversieprocedure op te lossen.

>[!MORELIKETHIS]
>
>* [ Ongeveer de Bronnen van het Publiek van de Eerste Partij ](/help/dsp/audiences/sources/source-about.md)
>* [ beheert de Bronnen van het Publiek om Universele Soorten van identiteitskaart ](source-manage.md) te activeren
>* [ Steun voor het Activeren van Universal IDs ](/help/dsp/audiences/universal-ids.md)
>* [ Ongeveer het Beheer van het Publiek ](/help/dsp/audiences/audience-about.md)
