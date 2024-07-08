---
title: Gebruikers-id's omzetten van [!DNL Optimizely] universele id's
description: Leer hoe u DSP inschakelt om uw [!DNL Optimizely] first-party segmenten op te nemen.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 31713da81bbb1eb840de0f8e0d40013b42cd3140
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Gebruikers-id&#39;s omzetten van [!DNL Optimizely] universele id&#39;s

*Bètafunctie*

Gebruik de DSP integratie met de [!DNL Optimizely] gegevensplatform van de klant om de gehashte e-mailadressen van de eerste partij van uw organisatie om te zetten in universele id&#39;s voor gerichte reclame.

1. (E-mailadressen converteren naar [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Tekstspatiëring instellen om in te schakelen [!DNL Analytics] meting](#analytics-tracking).

1. [Een publieksbron maken in DSP](#source-create).

1. [De segmentgegevens voorbereiden en duwen](#push-data).

1. [Vergelijk het aantal universele id&#39;s met het aantal gehashte e-mailadressen](#compare-id-count).

## Stap 1: Tekstspatiëring instellen voor [!DNL Analytics] meting {#analytics-tracking}

*Adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Ga als volgt te werk om [!DNL RampIDs] e-mailadressen of [!DNL ID5] id&#39;s om te zetten:

1. (Als u dat nog niet hebt gedaan) Voldoe aan alle [vereisten voor de implementatie [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) en zorg ervoor dat de [AMO ID en EF ID](/help/integrations/analytics/ids.md) worden ingevuld in uw tracerings-URL&#39;s.

1. Registreer de universele id-partner en distribueer universele ID-specifieke code op uw webpagina&#39;s om de conversies van id&#39;s in desktop- en mobiele webbrowsers (maar niet van mobiele apps) te koppelen aan doors:

   * **Voor [!DNL RampIDs]:** U moet een extra JavaScript-tag op uw webpagina&#39;s distribueren om te overeenkomen met conversies van id&#39;s in bureaublad- en mobiele webbrowsers (maar niet van mobiele apps) naar doorsweergaven. Neem contact op met het accountteam van de Adobe, dat u instructies geeft om u te registreren voor een [!DNL LiveRamp] [!DNL LaunchPad] tag van [!DNL LiveRamp] De Oplossingen van het Verkeer van de authentificatie. De registratie is gratis, maar u moet een overeenkomst ondertekenen. Nadat u zich hebt geregistreerd, genereert uw accountteam van de Adobe een unieke tag die uw organisatie op uw webpagina&#39;s kan implementeren.

## Stap 2: Een publieksbron maken in DSP {#source-create}

1. [Een publieksbron maken](source-manage.md) om soorten publiek te importeren naar uw DSP of een adverteerderaccount. U kunt uw gebruikers-id&#39;s omzetten in een van de [beschikbare Universal ID-indelingen](source-about.md).

   De bronmontages zullen een auto-geproduceerde bronsleutel omvatten, die u zult gebruiken om de segmentgegevens te duwen.

1. Nadat u de doelgroepbron hebt gemaakt, deelt u de broncodesleutel met de [!DNL Optimizely] gebruiker.

## Stap 3: Bereid de segmentgegevens voor en push deze {#push-data}

De adverteerder moet de gegevens voorbereiden en pushen met behulp van de [!DNL Optimizely Data Platform]. Neem bij vragen over het proces contact op met je [!DNL Optimizely] vertegenwoordiger.

1. Binnen [!DNL Optimizely Data Platform], hash de e-mail-id&#39;s voor de doelgroep die het SHA-256-algoritme gebruikt.

1. Volg de [[!DNL Optimizely's] instructies om het segment naar DSP te pushen](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Neem de volgende informatie op om de integratie mogelijk te maken:

   * **Source-sleutel:** Dit is de bronsleutel die is gemaakt in [Stap 2](#source-create).

   * **Accountcode:** Dit is de alfanumerieke DSP Account Code, die u kunt vinden in DSP op [!UICONTROL Settings] > [!UICONTROL Account].

De segmenten moeten binnen 24 uur in DSP beschikbaar zijn en worden vernieuwd zoals geconfigureerd voor de adverteerder. Ongeacht hoe vaak het segment wordt verfrist, verloopt de opneming in een segment na 30 dagen door gebrek of na een klant-gespecificeerde vervalperiode. Vernieuw de segmenten door ze te verplaatsen [!DNL Optimizely] vóór de vervaldatum. Neem contact op met het accountteam van de Adobe om een vervaldatum van een aangepast segment aan te vragen.

## Stap 4: Vergelijk het aantal universele id&#39;s met het aantal gehashte e-mailadressen {#compare-id-count}

Nadat u alle stappen hebt uitgevoerd, controleert u het bestand in de publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen plaatsingsinstellingen) dat het segment beschikbaar is en binnen 24 uur vult. Vergelijk het aantal universele id&#39;s met het aantal oorspronkelijk gehashte e-mailadressen.

De vertaalsnelheid van gehashte e-mailadressen naar universele id&#39;s moet hoger zijn dan 90%. Als u bijvoorbeeld 100 gehashte e-mailadressen verzendt vanuit uw klantgegevensplatform, moeten deze worden vertaald naar meer dan 90 universele id&#39;s. Een omzettingspercentage van 90% of minder is een probleem. Zie &#39;[Oorzaken van gegevensvariantie tussen e-mail-id&#39;s en universele id&#39;s&#39; voor meer informatie over de verschillen tussen het aantal segmenten](#universal-ids-data-variances).

Neem contact op met uw Adobe-accountteam als u ondersteuning wilt bieden voor problemen of `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Ongeveer de Bronnen van het Publiek van de Eerste Partij](/help/dsp/audiences/sources/source-about.md)
>* [Bronnen voor publiek beheren om Universal ID-publiek te activeren](source-manage.md)
>* [Ondersteuning voor het activeren van Universal ID&#39;s](/help/dsp/audiences/universal-ids.md)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
