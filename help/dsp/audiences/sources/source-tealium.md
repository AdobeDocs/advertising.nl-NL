---
title: Workflow voor het gebruik van de DSP integratie met [!DNL Tealium]
description: Leer hoe u DSP kunt inschakelen om uw [!DNL Tealium] eerste-partijsegmenten.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Workflow voor het gebruik van de DSP integratie met [!DNL Tealium]

U kunt de gegevens van de eerste partij van uw organisatie delen via de [!DNL Tealium] het gegevensplatform van de klant gebruiken [!DNL Amazon Web Services] (AWS) brandslangaansluiting. Er zijn vier stappen om gegevens van Tealium met DSP te delen:

1. [Een publieksbron maken in DSP](#source-create).

1. [Segmenttoewijzingsgegevens voorbereiden en delen](#map-data).

1. [Verbindingen maken in [!DNL Tealium] segmentgegevens delen](#tealium-connector).

1. [De bestaande connector dupliceren in [!DNL Tealium] segmenten blijven delen](#duplicate-connector).

## Stap 1: Een publieksbron maken in DSP {#source-create}

* [Een publieksbron maken](source-create.md) om soorten publiek in uw DSP of een adverteerderaccount te importeren en de broncodesleutel met de [!DNL Tealium] gebruiker.

## Stap 2: Voorbereiden en delen van segmenttoewijzingsgegevens {#map-data}

1. De adverteerder moet segmenttoewijzingsgegevens voorbereiden en delen:

   1. De adverteerder moet de gegevens binnen [!DNL Tealium]:

      1. De e-mailadressen voor het publiek van de adverteerder moeten worden gehasht met het SHA-256-algoritme.

      1. De kolom met gehashte e-mailadressen moet worden toegewezen aan het kenmerk van het type bezoeker-id.

      1. Het publiek moet worden gemaakt met de `Tealium_visitor_id` kenmerk. De juiste verrijking moet worden toegepast om de doelgroep te activeren. Zie de [[!DNL Tealium] documentatie over kenmerken van bezoekersidentiteitskaart](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

   1. De adverteerder moet segment-kaartgegevens aan het Team van de Rekening van de Adobe geven om de segmenten in DSP tot stand te brengen. Gebruik de volgende kolomnamen en -waarden in een bestand met door komma&#39;s gescheiden waarden:

      * **Sleutel extern segment:** De externe segmentsleutel, die u later in de actiemontages voor de schakelaar binnen zult specificeren [!DNL Tealium]. De aanbevolen naamgevingsconventie is &quot;`<DSP source key>_<Tealium segment name>`,&quot; zoals &quot;57bf424dc10_koffiedrinkers.&quot;

      * **Segmentnaam:** De segmentnaam.

      * **Segmentbeschrijving:** Het doel of de regel van het segment, of allebei.

      * **Bovenliggende id:** Leeg houden

      * **Video CPM:** 0

      * **CPM weergeven:** 0

      * **Segmentvenster:** Het segment time-to-live.

## Stap 3: Maak connectors in [!DNL Tealium] segmentgegevens delen {#tealium-connector}

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

            1. Als u een aangepast veld wilt maken, gaat u naar [!DNL Source Key] veld, voert u de [!UICONTROL External Segment Key] die was opgenomen in de segmenttoewijzingsgegevens in [Stap 2](#map-data).

               DSP gebruikt deze sleutel om uw segment te vullen.

            1. (Aanbevolen) Maak een updateactie om het segment vers te houden.

## Stap 4: Dupliceer de bestaande schakelaar in [!DNL Tealium] segmenten blijven delen {#duplicate-connector}

U kunt slechts één schakelaar per segment en één segment per schakelaar hebben.

1. In [!DNL Tealium]dupliceert u het segment waarvoor u een ander segment wilt maken en wijzigt u de naam van het nieuwe segment.

1. In [!DNL Tealium], dupliceer de connector die u hebt gemaakt in [Stap 3](#tealium-connector)en wijzig de naam van de nieuwe connector in &quot;`<original name>-copy`&quot; aan de nieuwe segmentnaam.

>[!MORELIKETHIS]
>
>* [Ongeveer het Activeren van Authenticated Segmenten van de Bronnen van het Publiek](/help/dsp/audiences/sources/source-about.md)
>* [Creeer een Bron van het Publiek om Eerste Publiek te activeren](source-create.md)
>* [Broninstellingen voor publiek](source-settings.md)
>* [Workflow voor het gebruik van de DSP integratie met [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
