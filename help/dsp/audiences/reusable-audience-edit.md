---
title: Een herbruikbaar publiek bewerken
description: Leer hoe u een herbruikbaar publiek kunt bewerken.
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
source-git-commit: 0afe1d9985c1451c28943aaa17c7d6f8a73a95ef
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Een herbruikbaar publiek bewerken

Wanneer u een publiek uitgeeft dat in om het even welke plaatsen of ander herbruikbaar publiek wordt gebruikt, worden de veranderingen onmiddellijk toegepast op die plaatsen en het publiek.<!-- verify -->

>[!NOTE]
>
>(Adverteerders voor wie DSP gehashte e-mailadressen in de segmenten van de RampID van LiveRampID omzet) De segmenten van eerste partij RampID die niet aan een actieve, geplande, of gepauzeerde plaatsing in bijlage zijn worden gepauzeerd. Het segment wordt in de segmentlijst genoteerd als &quot;Automatisch gepauzeerd&quot;.

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL All audiences]** .

1. Plaats de cursor op de personenrij en klik op **[!UICONTROL Edit]** .

1. Bewerk de publieksinstellingen op een van de volgende manieren:

   >[!NOTE]
   >
   >Als u de logica van het publiekssegment uitgeeft, worden de gedetailleerde [ gegevens van de publieksgrootte ](audience-about.md) bijgewerkt in het juiste paneel.

   * (Facultatief) om **[!UICONTROL Audience Name]** uit te geven klik ![ uitgeeft ](/help/dsp/assets/edit.png) naast de publieksnaam, ga een unieke publieksnaam in, en klik dan **[!UICONTROL Apply]**.

   * (Optioneel) Ga als volgt te werk als u de segmentlogica handmatig wilt bewerken met behulp van segmenten die beschikbaar zijn op de tabbladen [[!UICONTROL Third Party Segments] , [!UICONTROL First Party Segments] , [!UICONTROL Adobe Segments] , [!UICONTROL Custom Segments] en [!UICONTROL Saved Audiences] ](audience-settings.md) .

      * Een segment toevoegen aan een bestaande segmentgroep:

      1. Klik op de segmentgroep in het rechterdeelvenster.

      1. (Optioneel) Wijzig desgewenst de groeplogica in *[!UICONTROL Include Any]* , *[!UICONTROL Include All]* of *[!UICONTROL Exclude All]* .

         *[!UICONTROL Exclude All]* is niet beschikbaar voor de eerste segmentgroep. Voor een publiek dat alleen uitsluitingen bevat, bouwt u dit publiek op als *[!UICONTROL Include Any]* en selecteert u vervolgens binnen een plaatsing dat publiek in het menu Uitgesloten soorten publiek.

      1. Zoek het nieuwe segment in het linkerdeelvenster en selecteer het selectievakje naast de segmentnaam.

         De segmentgroep wordt automatisch bijgewerkt met het nieuwe segment.

   * Een nieuwe segmentgroep toevoegen:

      1. Klik op **[!UICONTROL + New Group]** in het rechterdeelvenster.

      1. (Optioneel) Wijzig desgewenst de logica tussen de vorige groep en de nieuwe groep in *[!UICONTROL And]* of *[!UICONTROL Or]* .

      1. Zoek de segmenten voor de nieuwe groep in het linkerdeelvenster en selecteer de selectievakjes naast de segmentnamen.

      1. (Optioneel) Wijzig desgewenst de groeplogica in *[!UICONTROL Include Any]* , *[!UICONTROL Include All]* of *[!UICONTROL Exclude All]* .

   * Segmentlogica van een bestaand publiek gebruiken:

      1. Kopieer de segmentlogica van het bestaande publiek op een van de volgende manieren:

         * Houd in de weergave Alle soorten publiek de cursor boven de publiekstrij en klik vervolgens op **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]** .

         * In de montages voor het bestaande publiek, bij de bovenkant van het paneel van de segmentlogica, klik **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * In een tekstredacteur, creeer manueel de segmentlogica gebruikend alfanumerieke segment IDs en [ syntaxis Van Boole ](audience-segment-logic-syntax.md), en kopieer het aan uw klembord.

      1. Klik op **[!UICONTROL paste in an audience rule to begin building]** , plak de bestaande segmentlogica in het invoerveld en klik op **[!UICONTROL Apply]** .

         >[!NOTE]
         >
         >Als het publiek reeds om het even welke segmentlogica omvat, beschrijft het kleven in nieuwe segmentlogica de bestaande logica.

1. Klik op **[!UICONTROL Save]**.

1. Klik in het bevestigingsbericht op **[!UICONTROL Continue]** .

>[!MORELIKETHIS]
>
>* [ Ongeveer het Beheer van het Publiek ](audience-about.md)
>* [ creeer een Herbruikbaar publiek ](reusable-audience-create.md)
>* [ dupliceer een Herbruikbaar publiek ](reusable-audience-duplicate.md)
>* [ Details van de Mening over een Herbruikbaar publiek ](reusable-audience-view-details.md)
>* [ deel een Herbruikbare Publiek ](reusable-audience-share.md)
>* [ de Uitvoer een Herbruikbaar publiek ](reusable-audience-export.md)
>* [ Kopieer de Sleutel van het Segment voor een Herbruikbaar publiek aan het Klembord ](reusable-audience-clipboard.md)
>* [ Schrap een Herbruikbaar publiek ](reusable-audience-delete.md)
>* [ Montages van het publiek ](audience-settings.md)
>* [ Syntaxis voor de Logica van het Segment van het Publiek ](audience-segment-logic-syntax.md)
>* [ Beschikbare Leveranciers van Gegevens van derden ](third-party-data-providers.md)
