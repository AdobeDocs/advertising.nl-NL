---
title: Een herbruikbaar publiek maken
description: Leer hoe u een herbruikbaar publiek kunt maken dat bestaat uit doelsegmenten en andere opgeslagen soorten publiek.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Een herbruikbaar publiek maken

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

U kunt herbruikbare soorten publiek opslaan en beheren. Dit zijn groepen publiekssegmenten en zelfs andere opgeslagen soorten publiek, die u kunt gebruiken als doelen of uitsluitingen voor meerdere plaatsen.

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Klik boven de gegevenstabel op **[!UICONTROL Create]**.

1. Voer een unieke waarde in **[!UICONTROL Audience Name]**.

1. (Optioneel) Schakel de optie uit om **[!UICONTROL Share with all advertisers in my account]**.

   Wanneer u een publiek deelt, wordt het publiek beschikbaar als doel of uitsluiting voor alle adverteerders binnen de account. De afzonderlijke segmenten in het publiek zijn echter alleen beschikbaar voor gebruikers waarop de segmenten worden gedeeld. Bijvoorbeeld, als u een publiek deelt dat de segmenten van Adobe Analytics met een adverteerder bevat die niet aan het zelfde in kaart wordt gebracht [!DNL Analytics] -account, dan wordt het segment niet voorvertoond in dat publiek voor die adverteerder. Alleen de segmenten die voor die adverteerder beschikbaar zijn, worden in het publiek voorvertoond.

1. Klik op **[!UICONTROL Save]**.

1. Het publiek opbouwen:

   >[!NOTE]
   >
   >Tijdens het samenstellen van het publiek, gedetailleerd [gegevens over doelgrootte](audience-about.md) wordt bijgewerkt in het rechterdeelvenster

   * Om de segmentlogica manueel te creëren, gebruikend segmenten beschikbaar op [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments], en [!UICONTROL Saved Audiences] tabs](audience-settings.md), doet u het volgende.

      * Als u het eerste segment wilt toevoegen, zoekt u het segment in het linkerdeelvenster en schakelt u het selectievakje naast de segmentnaam in.

      * Een segment toevoegen aan een bestaande segmentgroep:

         1. Klik op de segmentgroep in het rechterdeelvenster.

         1. (Optioneel) Wijzig de logica van de groep in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, of *[!UICONTROL Exclude All]*, indien nodig.

            *[!UICONTROL Exclude All]* is niet beschikbaar aan de eerste segmentgroep. Voor een publiek dat alleen uitsluitingen bevat, bouwt u dit publiek als *[!UICONTROL Include Any]* en selecteer vervolgens binnen een plaatsing dat publiek in het menu Uitgesloten soorten publiek.

         1. Zoek het nieuwe segment in het linkerdeelvenster en selecteer het selectievakje naast de segmentnaam.

            De segmentgroep wordt automatisch bijgewerkt met het nieuwe segment.

      * Een nieuwe segmentgroep toevoegen:

         1. Klikken **[!UICONTROL + New Group]** in het rechterdeelvenster.

         1. (Optioneel) Wijzig de logica tussen de vorige groep en de nieuwe groep in *[!UICONTROL And]* of *[!UICONTROL Or]*, indien nodig.

         1. Zoek de segmenten voor de nieuwe groep in het linkerdeelvenster en selecteer de selectievakjes naast de segmentnamen.

         1. (Optioneel) Wijzig de logica van de groep in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, of *[!UICONTROL Exclude All]*, indien nodig.

   * Segmentlogica van een bestaand publiek gebruiken:

      1. Kopieer de segmentlogica van het bestaande publiek op een van de volgende manieren:

         * Houd in de weergave Alle soorten publiek de cursor boven de personenrij en klik vervolgens op **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Klik in de instellingen voor het bestaande publiek boven aan het deelvenster voor segmentlogica op **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Maak in een teksteditor handmatig de segmentlogica met alfanumerieke segment-id&#39;s en [Booleaanse syntaxis](audience-segment-logic-syntax.md)en kopieer deze naar het klembord.

      1. Klikken **[!UICONTROL paste in an audience rule to begin building]** plakt u de bestaande segmentlogica in het invoerveld en klikt u vervolgens op **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Als het publiek reeds om het even welke segmentlogica omvat, beschrijft het kleven in nieuwe segmentlogica de bestaande logica.

1. Klik op **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Informatie over Audience Management](audience-about.md)
>* [Instellingen voor publiek](audience-settings.md)
>* [Syntaxis voor Audience Segment Logic](audience-segment-logic-syntax.md)
>* [Beschikbare gegevensleveranciers van derden](third-party-data-providers.md)
>* [Een aangepast segment maken en implementeren](custom-segment-create.md)
>* [Een [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Plaatsingsinstellingen](/help/dsp/campaign-management/placements/placement-settings.md)
