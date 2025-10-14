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
   >Als u de logica van het publiekssegment uitgeeft, worden de gedetailleerde [&#x200B; gegevens van de publieksgrootte &#x200B;](audience-about.md) bijgewerkt in het juiste paneel.

   * (Facultatief) om **[!UICONTROL Audience Name]** uit te geven klik ![&#x200B; uitgeeft &#x200B;](/help/dsp/assets/edit.png) naast de publieksnaam, ga een unieke publieksnaam in, en klik dan **[!UICONTROL Apply]**.

   * (Optioneel) Ga als volgt te werk als u de segmentlogica handmatig wilt bewerken met behulp van segmenten die beschikbaar zijn op de tabbladen [[!UICONTROL Third Party Segments] , [!UICONTROL First Party Segments] , [!UICONTROL Adobe Segments] , [!UICONTROL Custom Segments] en [!UICONTROL Saved Audiences] &#x200B;](audience-settings.md) .

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

         * In een tekstredacteur, creeer manueel de segmentlogica gebruikend alfanumerieke segment IDs en [&#x200B; syntaxis Van Boole &#x200B;](audience-segment-logic-syntax.md), en kopieer het aan uw klembord.

      1. Klik op **[!UICONTROL paste in an audience rule to begin building]** , plak de bestaande segmentlogica in het invoerveld en klik op **[!UICONTROL Apply]** .

         >[!NOTE]
         >
         >Als het publiek reeds om het even welke segmentlogica omvat, beschrijft het kleven in nieuwe segmentlogica de bestaande logica.

1. Klik op **[!UICONTROL Save]**.

1. Klik in het bevestigingsbericht op **[!UICONTROL Continue]** .

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer het Beheer van het Publiek &#x200B;](audience-about.md)
>* [&#x200B; creeer een Herbruikbaar publiek &#x200B;](reusable-audience-create.md)
>* [&#x200B; dupliceer een Herbruikbaar publiek &#x200B;](reusable-audience-duplicate.md)
>* [&#x200B; Details van de Mening over een Herbruikbaar publiek &#x200B;](reusable-audience-view-details.md)
>* [&#x200B; deel een Herbruikbare Publiek &#x200B;](reusable-audience-share.md)
>* [&#x200B; de Uitvoer een Herbruikbaar publiek &#x200B;](reusable-audience-export.md)
>* [&#x200B; Kopieer de Sleutel van het Segment voor een Herbruikbaar publiek aan het Klembord &#x200B;](reusable-audience-clipboard.md)
>* [&#x200B; Schrap een Herbruikbaar publiek &#x200B;](reusable-audience-delete.md)
>* [&#x200B; Montages van het publiek &#x200B;](audience-settings.md)
>* [&#x200B; Syntaxis voor de Logica van het Segment van het Publiek &#x200B;](audience-segment-logic-syntax.md)
>* [&#x200B; Beschikbare Leveranciers van Gegevens van derden &#x200B;](third-party-data-providers.md)
