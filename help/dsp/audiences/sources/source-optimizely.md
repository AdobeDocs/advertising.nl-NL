---
title: Zet gebruiker IDs van  [!DNL Optimizely]  in universele IDs om
description: Leer hoe te om DSP toe te laten om uw  [!DNL Optimizely]  eerste-partijsegmenten in te voeren.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: cff6b5ad2c66699a6e0402bce6685acc536fd0a0
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Gebruikers-id&#39;s converteren van [!DNL Optimizely] naar universele id&#39;s

*eigenschap van Beta*

Gebruik de DSP-integratie met het [!DNL Optimizely] -klantgegevensplatform om de gehashte e-mailadressen van de eerste partij van uw organisatie om te zetten in universele id&#39;s voor gerichte advertenties.

1. (Om e-mailadressen in [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> om te zetten; adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [ Opstelling het volgen om  [!DNL Analytics]  meting ](#analytics-tracking) toe te laten.

1. [ creeer een publieksbron in DSP ](#source-create).

1. [ voorbereidingen treffen en duwen de segmentgegevens ](#push-data).

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

1. Nadat u de publieksbron hebt gemaakt, deelt u de broncodesleutel met de [!DNL Optimizely] -gebruiker.

## Stap 3: De segmentgegevens voorbereiden en duwen {#push-data}

De adverteerder moet de gegevens voorbereiden en drukken met de [!DNL Optimizely Data Platform] . Neem voor alle vragen over het proces contact op met uw [!DNL Optimizely] -vertegenwoordiger.

1. Koppel binnen [!DNL Optimizely Data Platform] de e-mailadressen aan voor het publiek met behulp van het algoritme SHA-256.

1. Volg [[!DNL Optimizely's]  instructies om het segment aan DSP ](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads) te duwen. Neem de volgende informatie op om de integratie in te schakelen:

   * **Sleutel van Source:** dit is de bronsleutel die in [ wordt gecreeerd Stap 2 ](#source-create).

   * **de Code van de Rekening:** dit is de alfanumerieke Code van de Rekening van DSP, die u binnen DSP bij [!UICONTROL Settings] kunt vinden > [!UICONTROL Account].

De segmenten worden vernieuwd zoals deze voor de adverteerder zijn geconfigureerd. Ongeacht hoe vaak het segment wordt verfrist, verloopt de opneming in een segment na 30 dagen door gebrek of na een klant-gespecificeerde vervalperiode. Vernieuw de segmenten door deze vóór het verlopen opnieuw te duwen vanuit [!DNL Optimizely] . Neem contact op met uw Adobe-accountteam als u een aanvraag wilt indienen voor het verlopen van een aangepast segment.

## Stap 4: Vergelijk het aantal universele id&#39;s met het aantal gehashte e-mailadressen {#compare-id-count}

De segmenten moeten binnen 24 uur beschikbaar zijn in DSP. Nadat DSP de segmentgegevens heeft ontvangen, moet het aantal gebruikers binnen negen (9) uur zichtbaar zijn.

Controleer in uw publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen de plaatsingsinstellingen) of het segment beschikbaar en gevuld is en vergelijk het aantal universele id&#39;s met het aantal oorspronkelijke gehashte e-mailadressen. Voor informatie over aanvaardbare identiteitskaart vertaaltarieven en waarom de segmenttellingen kunnen variëren, zie &quot;[ de variaties van Gegevens tussen e-mail IDs en universele IDs ](#universal-ids-data-variances).&quot;

## Problemen oplossen

Om vertaaltarief en gebruikerstellingskwesties problemen op te lossen, zie &quot;[ Steun voor het activeren van universele IDs ](/help/dsp/audiences/universal-ids.md).&quot;

Neem contact op met uw Adobe-accountteam of `adcloud-support@adobe.com` om problemen met de conversieprocedure op te lossen.

>[!MORELIKETHIS]
>
>* [ Ongeveer eerste-partijpublieksbronnen ](/help/dsp/audiences/sources/source-about.md)
>* [ beheert publieksbronnen om universele identiteitskaart te activeren ](source-manage.md)
>* [ Steun voor het activeren van Universal IDs ](/help/dsp/audiences/universal-ids.md)
>* [ Ongeveer publieksbeheer ](/help/dsp/audiences/audience-about.md)
