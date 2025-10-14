---
title: Een herbruikbaar publiek maken
description: Leer hoe u een herbruikbaar publiek kunt maken dat bestaat uit doelsegmenten en andere opgeslagen soorten publiek.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: 0afe1d9985c1451c28943aaa17c7d6f8a73a95ef
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Een herbruikbaar publiek maken

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

U kunt herbruikbare soorten publiek opslaan en beheren. Dit zijn groepen publiekssegmenten en zelfs andere opgeslagen soorten publiek, die u kunt gebruiken als doelen of uitsluitingen voor meerdere plaatsen.

>[!NOTE]
>
>(Adverteerders voor wie DSP gehashte e-mailadressen in de segmenten van de RampID van LiveRampID omzet) De segmenten van eerste partij RampID die niet aan een actieve, geplande, of gepauzeerde plaatsing in bijlage zijn worden gepauzeerd. Het segment wordt in de segmentlijst genoteerd als &quot;Automatisch gepauzeerd&quot;.

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]** .

1. Klik boven de gegevenstabel op **[!UICONTROL Create]** .

1. Voer een uniek **[!UICONTROL Audience Name]** in.

1. (Optioneel) Schakel de optie uit die u wilt **[!UICONTROL Share with all advertisers in my account]** gebruiken.

   Wanneer u een publiek deelt, wordt het publiek beschikbaar als doel of uitsluiting voor alle adverteerders binnen de account. De afzonderlijke segmenten in het publiek zijn echter alleen beschikbaar voor gebruikers waarop de segmenten worden gedeeld. Als u bijvoorbeeld een publiek deelt dat Adobe Analytics-segmenten bevat, met een adverteerder die niet is toegewezen aan dezelfde [!DNL Analytics] -account, wordt het segment niet voorvertoond in dat publiek voor die adverteerder. Alleen de segmenten die voor die adverteerder beschikbaar zijn, worden in het publiek voorvertoond.

1. Klik op **[!UICONTROL Save]**.

1. Het publiek opbouwen:

   >[!NOTE]
   >
   >Aangezien u het publiek bouwt, worden de gedetailleerde [&#x200B; gegevens van de publieksgrootte &#x200B;](audience-about.md) bijgewerkt in het juiste paneel

   * Ga als volgt te werk om de segmentlogica handmatig te maken met behulp van segmenten die beschikbaar zijn op de tabbladen [[!UICONTROL Third Party Segments] , [!UICONTROL First Party Segments] , [!UICONTROL Adobe Segments] , [!UICONTROL Custom Segments] en [!UICONTROL Saved Audiences] &#x200B;](audience-settings.md) .

      * Als u het eerste segment wilt toevoegen, zoekt u het segment in het linkerdeelvenster en schakelt u het selectievakje naast de segmentnaam in.

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

1. Klik op **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer het Beheer van het Publiek &#x200B;](audience-about.md)
>* [&#x200B; Montages van het publiek &#x200B;](audience-settings.md)
>* [&#x200B; Syntaxis voor de Logica van het Segment van het Publiek &#x200B;](audience-segment-logic-syntax.md)
>* [&#x200B; Beschikbare Leveranciers van Gegevens van derden &#x200B;](third-party-data-providers.md)
>* [&#x200B; creeer en voer een Segment van de Douane uit &#x200B;](custom-segment-create.md)
>* [&#x200B; creeer en voer a [!UICONTROL CCPA Opt-Out-of-Sale] Segment &#x200B;](ccpa-opt-out-segment-create.md) uit
>* [&#x200B; Montages van de Plaatsing &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)
