---
title: Zet gebruiker IDs van  [!DNL Tealium]  in universele IDs om
description: Leer hoe te om DSP toe te laten om uw  [!DNL Tealium]  eerste-partijsegmenten in te voeren.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 5110e9b4c966f5d719743d09b5a3aebbb37e0a05
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Gebruikers-id&#39;s converteren van [!DNL Tealium] naar universele id&#39;s

*eigenschap van Beta*

Gebruik de DSP-integratie met het [!DNL Tealium] -klantgegevensplatform om de gehashte e-mailadressen van de eerste partij van uw organisatie om te zetten in universele id&#39;s voor gerichte advertenties. Het proces gebruikt de [!DNL Amazon Web Services] (AWS) brandslangaansluiting. Voer de volgende stappen uit om gegevens uit Tealium te delen met DSP:

1. (Om e-mailadressen in [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> om te zetten; adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [ Opstelling het volgen om  [!DNL Analytics]  meting ](#analytics-tracking) toe te laten.

1. [ creeer een publieksbron in DSP ](#source-create).

1. [ voorbereidingen treffen en deel segment-afbeelding gegevens ](#map-data).

1. [ creeer schakelaars in  [!DNL Tealium]  om segmentgegevens ](#tealium-connector) te delen.

1. [ dupliceer de bestaande schakelaar in  [!DNL Tealium]  om segmenten ](#duplicate-connector) te blijven delen.

1. [ vergelijk het aantal universele IDs met het aantal gehakte e-mailadressen ](#compare-id-count).

## Stap 1: Tekstspatiëring instellen voor [!DNL Analytics] -meting {#analytics-tracking}

*Advertisers met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Als u e-mailadressen wilt converteren naar [!DNL RampIDs] - of [!DNL ID5] -id&#39;s, moet u het volgende doen:

1. (Als u dit nog niet hebt gedaan) voltooi alle [ eerste vereisten voor het uitvoeren van  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) en zorg ervoor dat [ identiteitskaart van AMO en identiteitskaart EF ](/help/integrations/analytics/ids.md) in uw het volgen URLs wordt bevolkt.

1. Registreer u bij de partner voor de universele id en implementeer de specifieke code voor de universele id op uw webpagina&#39;s om de conversies van de id&#39;s in de webbrowsers voor bureaublad en mobiele apparaten (maar niet voor mobiele apps) aan te passen aan de doorzoekresultaten:

   * **voor [!DNL RampIDs]:** u moet een extra markering van JavaScript op uw webpagina&#39;s opstellen om omzettingen van identiteitskaarts op Desktop en mobiele Webbrowsers (maar niet mobiele apps) aan mening-door aan te passen. Neem contact op met uw Adobe-accountteam. Dit team geeft u instructies om u te registreren voor een [!DNL LiveRamp] [!DNL LaunchPad] -tag van [!DNL LiveRamp] Authentication Traffic Solutions. De registratie is gratis, maar u moet een overeenkomst ondertekenen. Nadat u zich hebt geregistreerd, genereert uw Adobe-accountteam een unieke tag die uw organisatie op uw webpagina&#39;s kan implementeren.

## Stap 2: Een publieksbron maken in DSP {#source-create}

1. [ creeer een publieksbron ](source-manage.md) om publiek in uw rekening van DSP of een adverteerderrekening in te voeren. U kunt verkiezen om uw gebruikersherkenningstekens in om het even welke [ beschikbare universele formaten van identiteitskaart ](source-about.md) om te zetten.

   De bronmontages zullen een auto-geproduceerde bronsleutel omvatten, die u zult gebruiken om de segment-afbeelding gegevens voor te bereiden.

1. Nadat u de publieksbron hebt gemaakt, deelt u de broncodesleutel met de [!DNL Tealium] -gebruiker.

## Stap 3: Voorbereiden en delen van segmenttoewijzingsgegevens {#map-data}

De adverteerder moet segmenttoewijzingsgegevens voorbereiden en delen.

1. De adverteerder moet de gegevens voorbereiden binnen [!DNL Tealium] :

   1. Verberg de e-mailadressen voor het publiek van de adverteerder met behulp van het SHA-256-algoritme.

   1. Wijs de kolom met gehashte e-mailadressen toe aan het kenmerk van het type bezoeker-id.

   1. Maak een publiek met het kenmerk `Tealium_visitor_id` . Pas de juiste verrijking toe om het publiek te activeren. Zie de [[!DNL Tealium]  documentatie over de attributen van bezoekersidentiteitskaart ](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. De adverteerder moet segmenttoewijzingsgegevens aan het Adobe Account Team geven om de segmenten in DSP te maken. Gebruik de volgende kolomnamen en -waarden in een bestand met door komma&#39;s gescheiden waarden:

   * **Externe Sleutel van het Segment:** De externe segmentsleutel, die u later in de actiemontages voor de schakelaar in [!DNL Tealium] zult specificeren. De geadviseerde noemende overeenkomst is &quot;`<DSP source key>_<Tealium segment name>`,&quot;zoals &quot;57bf424dc10_koffie-drinkers.&quot; Gebruik voor de DSP-bronsleutel de [!UICONTROL Source Key] van de broninstellingen van de DSP-doelgroep.

   * **Naam van het segment:** de segmentnaam.

   * **Beschrijving van het Segment:** Het doel of de regel van het segment, of allebei.

   * **identiteitskaart van de Ouder:** houd leeg

   * **Video CPM:** 0

   * **Vertoning CPM:** 0

   * **Venster van het Segment:** de segment tijd-aan-levende.

## Stap 4: Maak connectors in [!DNL Tealium] om segmentgegevens te delen {#tealium-connector}

Voor elk segment dat u wilt delen, creeer een afzonderlijke schakelaar voor elke actie die gegevensveranderingen teweegbrengt. Bijvoorbeeld, om twee segmenten te delen die elk twee trekkers hebben, creeer vier schakelaars.

1. Het Adobe-accountteam biedt de adverteerder de verbindingsgegevens van de AWS-brandslangaansluiting.

1. In [!DNL Tealium], [ voeg een schakelaar ](https://docs.tealium.com/server-side/connectors/add/) toe, gebruikend de volgende opties:

   1. Selecteer de [!DNL AWS Firehose] -connector.

   1. In de broninstellingen:

      1. Selecteer het publiekssegment dat u wilt delen.

      1. Een trigger instellen:

         * Selecteer de trigger `Joined Audience` voor de eerste connector voor het segment. Dit zorgt ervoor dat gegevens met DSP worden gedeeld wanneer een gebruiker tot een segment toetreedt.

         * Selecteer de trigger `Left Audience` voor de tweede connector voor het segment. Deze aansluiting wordt gebruikt voor alle opt-outs en gebruikers die het segment in DSP verlaten.

   1. Geef in de configuratie-instellingen de AWS-brandstofinbinding op. Als u nog niet de brandslangaansluiting voor DSP hebt toegevoegd, voegt u een brandslangaansluiting toe met behulp van de volgende informatie:

      * **Naam:** De naam van de schakelaar.

      * **Sleutel van de Toegang:** de toegangssleutel die door het Team van de Rekening van Adobe wordt verstrekt.

      * **Geheime Sleutel:** De geheime sleutel die door het Team van de Rekening van Adobe wordt verstrekt.

      * **Regio:** Amerikaanse East North Virginia (wij-oost-1)

   1. Voer de volgende handelingen uit in de handelingsinstellingen:

      1. Maak een actie &quot;Customer Data to Delivery Stream (Advanced) verzenden&quot; om gegevens aan het segment toe te voegen met behulp van de volgende informatie:

         * **Naam van de Actie:** De naam van de actie.

         * **Type van Actie:** verzendt de Gegevens van de Klant naar (Geavanceerde) Stroom van de Levering

         * **leveringsstroom:** Tealium_CDP_Connector

         * **Gegevens van het Bericht:** doe het volgende:

            1. Kies één kenmerk voor het segment:

               * Geef voor het kenmerk Hashed_Email een naam voor het aangepaste bericht `hashed_email` .

               * Geef voor het kenmerk Cookies het aangepaste bericht `cookies` een naam.

            1. In de optie om een douanegebied tot stand te brengen, op het [!DNL Source Key] gebied, ga [!UICONTROL External Segment Key] in die in de [ segment-afbeelding gegevens ](#map-data) in de vorige procedure inbegrepen was.

               DSP gebruikt deze sleutel om uw segment te vullen.

            1. (Aanbevolen) Maak een updateactie om het segment vers te houden.

## Stap 5: Dupliceer de bestaande schakelaar in [!DNL Tealium] om segmenten te blijven delen {#duplicate-connector}

U kunt slechts één schakelaar per segment en één segment per schakelaar hebben.

1. In [!DNL Tealium], dupliceer het segment waarvoor u een ander segment wilt tot stand brengen, en noem het nieuwe segment anders.

1. In [!DNL Tealium], dupliceer [ de schakelaar u ](#tealium-connector) in de vorige procedure creeerde, en noem de nieuwe schakelaar van &quot;`<original name>-copy`&quot;aan de nieuwe segmentnaam anders.

## Stap 6: Vergelijk het aantal universele id&#39;s met het aantal gehashte e-mailadressen {#compare-id-count}

De segmenten moeten binnen 24 uur beschikbaar zijn in DSP. Nadat DSP de segmentgegevens heeft ontvangen, moet het aantal gebruikers binnen negen (9) uur zichtbaar zijn.

Controleer in uw publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen de plaatsingsinstellingen) of het segment vult en vergelijk het aantal universele id&#39;s met het aantal oorspronkelijke gehashte e-mailadressen. Voor informatie over aanvaardbare identiteitskaart vertaaltarieven en waarom de segmenttellingen kunnen variëren, zie &quot;[ Varianties van Gegevens tussen E-mail IDs en Universele IDs ](#universal-ids-data-variances).&quot;

Segmenten worden elke 24 uur vernieuwd. Nochtans, verloopt de opneming in een segment na 30 dagen door gebrek of na een klant-gespecificeerde vervalperiode. Vernieuw de segmenten door deze vóór het verlopen opnieuw te duwen vanuit [!DNL Tealium] . Neem contact op met uw Adobe-accountteam als u een aanvraag wilt indienen voor het verlopen van een aangepast segment.

## Problemen oplossen

Om vertaaltarief en gebruikerstellingskwesties problemen op te lossen, zie &quot;[ Steun voor het Activeren van Universal IDs ](/help/dsp/audiences/universal-ids.md).&quot;

Neem contact op met uw Adobe-accountteam of `adcloud-support@adobe.com` om problemen met de conversieprocedure op te lossen.

>[!MORELIKETHIS]
>
>* [ Ongeveer de Bronnen van het Publiek van de Eerste Partij ](/help/dsp/audiences/sources/source-about.md)
>* [ beheert de Bronnen van het Publiek om Universele Soorten van identiteitskaart ](source-manage.md) te activeren
>* [ Steun voor het Activeren van Universal IDs ](/help/dsp/audiences/universal-ids.md)
>* [ Ongeveer het Beheer van het Publiek ](/help/dsp/audiences/audience-about.md)
