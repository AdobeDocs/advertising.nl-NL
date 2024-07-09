---
title: Gebruikersnamen converteren van [!DNL Tealium] naar universele id's
description: Leer hoe u DSP kunt inschakelen om uw [!DNL Tealium] eerste-partijsegmenten.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 44c2fcad42be2d25524a49cdc9cb4184297cd3a1
workflow-type: tm+mt
source-wordcount: '1140'
ht-degree: 0%

---

# Gebruikersnamen converteren van [!DNL Tealium] naar universele id&#39;s

*Beta-functie*

Gebruik de DSP integratie met de [!DNL Tealium] gegevensplatform van de klant om de gehashte e-mailadressen van de eerste partij van uw organisatie om te zetten in universele id&#39;s voor gerichte reclame. Het proces gebruikt het [!DNL Amazon Web Services] (AWS) brandslangaansluiting. Voer de volgende stappen uit om gegevens uit Tealium te delen met DSP:

1. (E-mailadressen converteren naar [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Tekstspatiëring instellen om in te schakelen [!DNL Analytics] meting](#analytics-tracking).

1. [Een publieksbron maken in DSP](#source-create).

1. [Segmenttoewijzingsgegevens voorbereiden en delen](#map-data).

1. [Verbindingen maken in [!DNL Tealium] segmentgegevens delen](#tealium-connector).

1. [De bestaande connector dupliceren in [!DNL Tealium] segmenten blijven delen](#duplicate-connector).

1. [Vergelijk het aantal universele id&#39;s met het aantal gehashte e-mailadressen](#compare-id-count).

## Stap 1: Tekstspatiëring instellen voor [!DNL Analytics] meting {#analytics-tracking}

*Adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

E-mailadressen converteren naar [!DNL RampIDs] of [!DNL ID5] In id&#39;s moet u het volgende doen:

1. (Als u dit nog niet hebt gedaan) Alle gegevens invullen [voorwaarden voor de uitvoering [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) en zorgt ervoor dat de [AMO-id en EF-id](/help/integrations/analytics/ids.md) worden ingevuld in uw URL&#39;s voor bijhouden.

1. Registreer u bij de partner voor de universele id en implementeer de specifieke code voor de universele id op uw webpagina&#39;s om de conversies van de id&#39;s in de webbrowsers voor bureaublad en mobiele apparaten (maar niet voor mobiele apps) aan te passen aan de doorzoekresultaten:

   * **Voor [!DNL RampIDs]:** U moet een extra JavaScript-tag op uw webpagina&#39;s implementeren om conversies van de id&#39;s in desktopbrowsers en mobiele webbrowsers (maar niet mobiele apps) aan te passen aan doorzoekacties. Neem contact op met het accountteam van de Adobe, dat u instructies geeft om u te registreren voor een [!DNL LiveRamp] [!DNL LaunchPad] tag van [!DNL LiveRamp] De Oplossingen van het Verkeer van de authentificatie. De registratie is gratis, maar u moet een overeenkomst ondertekenen. Nadat u zich hebt geregistreerd, genereert uw accountteam van de Adobe een unieke tag die uw organisatie op uw webpagina&#39;s kan implementeren.

## Stap 2: Een publieksbron maken in DSP {#source-create}

1. [Een publieksbron maken](source-manage.md) om soorten publiek te importeren naar uw DSP of een adverteerderaccount. U kunt uw gebruikers-id&#39;s omzetten in een van de [beschikbare Universal ID-indelingen](source-about.md).

   De bronmontages zullen een auto-geproduceerde bronsleutel omvatten, die u zult gebruiken om de segment-afbeelding gegevens voor te bereiden.

1. Nadat u de publieksbron creeert, deel de sleutel van de broncode met [!DNL Tealium] gebruiker.

## Stap 3: Voorbereiden en delen van segmenttoewijzingsgegevens {#map-data}

De adverteerder moet segmenttoewijzingsgegevens voorbereiden en delen.

1. De adverteerder moet de gegevens binnen [!DNL Tealium]:

   1. Verberg de e-mailadressen voor het publiek van de adverteerder met behulp van het SHA-256-algoritme.

   1. Wijs de kolom met gehashte e-mailadressen toe aan het kenmerk van het type bezoeker-id.

   1. Maak het publiek met de `Tealium_visitor_id` kenmerk. Pas de juiste verrijking toe om het publiek te activeren. Zie de [[!DNL Tealium] documentatie over kenmerken van bezoekersidentiteitskaart](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. De adverteerder moet segment-kaartgegevens aan het Team van de Rekening van de Adobe geven om de segmenten in DSP tot stand te brengen. Gebruik de volgende kolomnamen en -waarden in een bestand met door komma&#39;s gescheiden waarden:

   * **Sleutel extern segment:** De externe segmentsleutel, die u later in de actiemontages voor de schakelaar binnen zult specificeren [!DNL Tealium]. De aanbevolen naamgevingsconventie is &quot;`<DSP source key>_<Tealium segment name>`,&quot; zoals &quot;57bf424dc10_koffiedrinkers.&quot; Voor de DSP bronsleutel gebruikt u de [!UICONTROL Source Key] uit de broninstellingen voor DSP publiek.

   * **Segmentnaam:** De segmentnaam.

   * **Segmentbeschrijving:** Het doel of de regel van het segment, of allebei.

   * **Bovenliggende id:** Leeg houden

   * **Video CPM:** 0

   * **CPM weergeven:** 0

   * **Segmentvenster:** Het segment time-to-live.

## Stap 4: Maak connectors in [!DNL Tealium] segmentgegevens delen {#tealium-connector}

Voor elk segment dat u wilt delen, creeer een afzonderlijke schakelaar voor elke actie die gegevensveranderingen teweegbrengt. Bijvoorbeeld, om twee segmenten te delen die elk twee trekkers hebben, creeer vier schakelaars.

1. Het accountteam van de Adobe verschaft de adverteerder de verbindingsgegevens van de AWS-brandslangaansluiting.

1. In [!DNL Tealium], [een aansluiting toevoegen](https://docs.tealium.com/server-side/connectors/add/)met de volgende opties:

   1. Selecteer de [!DNL AWS Firehose] -aansluiting.

   1. In de broninstellingen:

      1. Selecteer het publiekssegment dat u wilt delen.

      1. Een trigger instellen:

         * Voor de eerste schakelaar voor het segment, selecteer de trekker `Joined Audience`. Dit zorgt ervoor dat de gegevens met DSP worden gedeeld wanneer een gebruiker zich bij een segment aansluit.

         * Voor de tweede schakelaar voor het segment, selecteer de trekker `Left Audience`. Deze schakelaar wordt gebruikt om alle opt-outs en gebruikers te behandelen die het segment in DSP verlaten.

   1. Geef in de configuratie-instellingen de AWS-brandstofinbinding op. Als u nog niet de vuurslangschakelaar voor DSP hebt toegevoegd, dan voeg een vuurslangschakelaar toe gebruikend de volgende informatie:

      * **Naam:** De naam van de connector.

      * **Toegangstoets:** De toegangssleutel die door het Team van de Rekening van de Adobe wordt verstrekt.

      * **Geheime sleutel:** De geheime sleutel die door het Team van de Rekening van de Adobe wordt verstrekt.

      * **Regio:** US East North Virginia (VS-oost-1)

   1. Voer de volgende handelingen uit in de handelingsinstellingen:

      1. Maak een actie &quot;Customer Data to Delivery Stream (Advanced) verzenden&quot; om gegevens aan het segment toe te voegen met behulp van de volgende informatie:

         * **Naam van handeling:** De naam van de handeling.

         * **Type handeling:** Klantgegevens naar leveringsstroom verzenden (geavanceerd)

         * **Bezorgingsstroom:** Tealium_CDP_Connector

         * **Berichtgegevens:**  Ga als volgt te werk:

            1. Kies één kenmerk voor het segment:

               * Geef voor het kenmerk Hashed_Email een naam voor het aangepaste bericht `hashed_email`.

               * Geef voor het kenmerk Cookies het aangepaste bericht een naam `cookies`.

            1. Als u een aangepast veld wilt maken, gaat u naar [!DNL Source Key] veld, voert u de [!UICONTROL External Segment Key] die in het [segmenttoewijzingsgegevens](#map-data) in de vorige procedure.

               DSP gebruikt deze sleutel om uw segment te vullen.

            1. (Aanbevolen) Maak een updateactie om het segment vers te houden.

## Stap 5: Dupliceer de bestaande schakelaar in [!DNL Tealium] segmenten blijven delen {#duplicate-connector}

U kunt slechts één schakelaar per segment en één segment per schakelaar hebben.

1. In [!DNL Tealium]dupliceert u het segment waarvoor u een ander segment wilt maken en wijzigt u de naam van het nieuwe segment.

1. In [!DNL Tealium], dupliceren [de schakelaar u creeerde](#tealium-connector) in de vorige procedure en wijzig de naam van de nieuwe connector in &quot;`<original name>-copy`&quot; aan de nieuwe segmentnaam.

## Stap 6: Vergelijk het aantal universele id&#39;s met het aantal gehashte e-mailadressen {#compare-id-count}

De segmenten moeten binnen 24 uur in DSP beschikbaar zijn. Nadat DSP de segmentgegevens ontvangt, moet het aantal gebruikers binnen negen (9) uur zichtbaar zijn.

Verifieer in uw publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen plaatsingsinstellingen) dat het segment vult en het aantal universele id&#39;s vergelijkt met het aantal oorspronkelijke gehashte e-mailadressen.

De vertaalsnelheid van gehashte e-mailadressen naar universele id&#39;s moet groter zijn dan 90%; de vertaalsnelheid voor [!DNL RampIDs] met name 95 % als alle gehashte e - mailadressen uniek zijn . Als u bijvoorbeeld 100 gehashte e-mailadressen verzendt van het gegevensplatform van uw klant, moeten deze naar minstens 95 worden vertaald [!DNL RampIDs] of meer dan 90 andere typen universele id&#39;s. Een lager vertaaltarief is een kwestie. Voor meer informatie over hoe de segmenttellingen kunnen variëren, zie &quot;[Oorzaken voor gegevensvariaties tussen e-mailadressen en universele id&#39;s](#universal-ids-data-variances).&quot;

Segmenten worden elke 24 uur vernieuwd. Nochtans, verloopt de opneming in een segment na 30 dagen door gebrek of na een klant-gespecificeerde vervalperiode. Vernieuw de segmenten door ze te verplaatsen [!DNL Tealium] vóór de vervaldatum. Neem contact op met het accountteam van de Adobe om een vervaldatum van een aangepast segment aan te vragen.

Neem voor probleemoplossing contact op met uw accountteam van de Adobe of `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Ongeveer de Bronnen van het Publiek van de Eerste Partij](/help/dsp/audiences/sources/source-about.md)
>* [Bronnen voor publiek beheren om Universal ID-publiek te activeren](source-manage.md)
>* [Ondersteuning voor het activeren van Universal ID&#39;s](/help/dsp/audiences/universal-ids.md)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
