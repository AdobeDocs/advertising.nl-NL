---
title: Voeg een doelknooppunt toe aan het uiteindelijke niveau in een ervaring
description: Leer hoe u een doelnode toevoegt aan het uiteindelijke doelniveau van een advertentie.
feature: Creative Experiences
exl-id: 3ff657d5-bad1-47f4-a3ec-9ea678fd3c9d
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---

# Voeg een doelknooppunt toe aan het uiteindelijke niveau in een ervaring

*Ervaringen met beslissingsboom richtend slechts*

Wanneer u een doelknoop aan het bodem-meest niveau in de ervaring toevoegt — of het de wortel &quot;Al&quot;knoop, een doel-specifieke knoop, of een &quot;Al Else&quot;knoop is — u bepaalt direct het doel en te hoeven niet om een sibling knoop tot stand te brengen. Als u een knooppunt op het onderste niveau toevoegt, maakt u het doelknooppunt en een extra knooppunt &quot;All Else&quot; op hetzelfde niveau.

>[!NOTE]
>
>Om een doelknoop tussen bestaande niveaus van een besluitvormingsboom op te nemen, zie &quot;[&#x200B; een doelknoop tussen knopen in een ervaring &#x200B;](experience-target-node-add-inner.md) opnemen.&quot;

<!-- 1. [ways to get to the decision tree] -->

1. Onder de knoop waarbij u het doel wilt opnemen, ![&#x200B; &#x200B;](/help/creative/assets/add.png " toevoegen ") klikken, en dan selecteren **[!UICONTROL Insert New Target]**.

1. Geef de doelen op:

   * Selecteer **[!UICONTROL Audience]** voor doelgroepen, klik op **[!UICONTROL Click to Browse]** om de [!UICONTROL Audience Targeting] -opties te openen en voer de volgende handelingen uit:

      * Als u het eerste segment wilt toevoegen, zoekt u het segment in het linkerdeelvenster en schakelt u het selectievakje naast de segmentnaam in.

      * Een segment toevoegen aan een bestaande segmentgroep:

         1. Klik op de segmentgroep in het rechterdeelvenster.

         1. (Optioneel) Wijzig desgewenst de groeplogica in *[!UICONTROL Include Any]* , *[!UICONTROL Include All]* of *[!UICONTROL Exclude All]* .

            *[!UICONTROL Exclude All]* is niet beschikbaar voor de eerste segmentgroep. Voor een publiek dat alleen uitsluitingen bevat, maakt u dit publiek op als *[!UICONTROL Include Any]* en sluit u dat publiek uit wanneer u het toevoegt aan een plaatsing in uw DSP.

         1. Zoek het nieuwe segment in het linkerdeelvenster en selecteer het selectievakje naast de segmentnaam.

            De segmentgroep wordt automatisch bijgewerkt met het nieuwe segment.

      * Een nieuwe segmentgroep toevoegen:

         1. Klik op **[!UICONTROL + New Group]** in het rechterdeelvenster.

         1. (Optioneel) Wijzig desgewenst de logica tussen de vorige groep en de nieuwe groep in *[!UICONTROL And]* of *[!UICONTROL Or]* .

         1. Zoek de segmenten voor de nieuwe groep in het linkerdeelvenster en selecteer de selectievakjes naast de segmentnamen.

         1. (Optioneel) Wijzig desgewenst de groeplogica in *[!UICONTROL Include Any]* , *[!UICONTROL Include All]* of *[!UICONTROL Exclude All]* .

      1. Klik op **[!UICONTROL Create]**.

      1. Klik op **[!UICONTROL Apply]**.

   * Voor geografische doelen selecteert u één geografische categorie (zoals [!UICONTROL Geo: Country]) en voert u de volgende handelingen uit:

      1. Klik op **[!UICONTROL Click to Browse]** om de [!UICONTROL Geo Targeting] -opties te openen, geef een of meer geografische doelen op en klik op **[!UICONTROL Save]** .

         Postcodedoelen hebben opties voor bulkbewerking. Als u meerdere postcodes wilt plakken, klikt u op de tab **[!UICONTROL Paste postal codes]** , selecteert u het land, plakt of voert u postcodes in die door komma&#39;s of op afzonderlijke regels zijn gescheiden, en klikt u op **[!UICONTROL Include All]** . Om een inbegrepen zip codedoel te verwijderen, houd de curseur over het doel en klik ![&#x200B; verwijder &#x200B;](/help/creative/assets/delete.png " ") **[!UICONTROL Remove]**.

      1. (Optioneel) Als u meerdere doelknooppunten wilt maken wanneer meerdere geografische doelen zijn opgegeven, selecteert u **[!UICONTROL Split targets to create nodes]** .

         Met deze functie maakt u een afzonderlijk doelknooppunt (met afzonderlijke creatieve bundels) voor elk opgegeven geografische doel. Als u de doelen niet splitst, moet de gebruiker tot alle opgegeven locaties behoren (een [!DNL Boolean] `AND` -instructie).

      1. Klik op **[!UICONTROL Apply]**.

   * Selecteer **[!UICONTROL Data Pass]** voor een gegevensdoorvoerdoel, pas desgewenst de gegevensdoorvoersleutel aan, voer één gegevensdoorvoerwaarde in en klik op **[!UICONTROL Apply]** .

   Een standaardwaarde voor de sleutel in het zeer belangrijk-waardepaar wordt reeds geplaatst op het **[!UICONTROL Data Pass]** gebied in de [!UICONTROL Advanced] sectie van de [&#x200B; ervaringsmontages &#x200B;](experience-settings-targeting.md). U kunt de toets desgewenst aanpassen.

   * Selecteer **[!UICONTROL RT Pixel]** als u een pixeldoel opnieuw wilt toewijzen, selecteer één nieuwe doelpixel en de waarden voor de kenmerken van een pixel die nodig zijn om de creatieve elementen weer te geven. Klik vervolgens op **[!UICONTROL Apply]** .

     De attributen voor het opnieuw richten pixel worden gevormd in [&#x200B; het opnieuw richten pixelmontages &#x200B;](/help/creative/pixels/retargeting-pixel-manage.md).

   * Ga als volgt te werk voor apparaatdoelen:

      1. Selecteer één doelcategorie (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** of **[!UICONTROL Device: Browser]** ) en selecteer vervolgens de doelen.

      1. (Optioneel) Als u meerdere doelknooppunten wilt maken wanneer meerdere geografische doelen zijn opgegeven, selecteert u **[!UICONTROL Split targets to create nodes]** .

         Met deze functie maakt u een afzonderlijk doelknooppunt (met afzonderlijke creatieve bundels) voor elk opgegeven geografische doel. Als u de doelen niet splitst, moet de gebruiker tot alle opgegeven locaties behoren (een [!DNL Boolean] `AND` -instructie).

      1. Klik op **[!UICONTROL Apply]**.

1. (Optioneel) Geef een aangepaste vertakkingsnaam op voor een door de gebruiker gedefinieerde vertakking.

   Door gebrek, user-defined takken worden geëtiketteerd met de toegepaste doelstellingen.

   U kunt geen aangepaste vertakkingsnaam maken voor een vertakking Alles of Iedereen anders.

   1. Plaats de cursor op het doelknooppunt en klik op **[!UICONTROL ...]** > **[!UICONTROL Edit Name]** .

   1. Voer de **[!UICONTROL Node Name]** in en klik op **[!UICONTROL Save]** .

1. Voer een van de volgende handelingen uit:

   * (Facultatief) [&#x200B; wijst creatieve personen &#x200B;](experience-assign-creative-bundles.md) aan de nieuwe doelknoop en aan de &quot;Al Else&quot;knoop toe.

   * (Optioneel) U kunt de ervaring als volgt opslaan:

      1. Klik op **[!UICONTROL Save]** en vervolgens op **[!UICONTROL OK]** .

      1. (Als elk knooppunt op het laagste niveau niet ten minste één creatief knooppunt bevat): Voer een van de volgende handelingen uit:

         * Klik op **[!UICONTROL Save as Draft]** om de ervaring zonder alle vereiste creatieve bundels op te slaan.

           U kunt geen ad-tag maken voor een conceptervaring.

         * Klik op **[!UICONTROL Assign Default Creatives]** als u de standaard creatieve waarde wilt toewijzen aan elk doel waaraan nog geen creatieve bundel is toegewezen. Klik op **[!UICONTROL Save]** en **[!UICONTROL OK]** nadat u de bijgewerkte structuur hebt bekeken waaraan de standaardcreatieven zijn toegewezen.

         * Klik op **[!UICONTROL Continue Edit]** als u de beslissingstructuur wilt blijven bewerken.

>[!MORELIKETHIS]
>
>* [&#x200B; neem een doelknoop tussen knopen &#x200B;](experience-target-node-add-inner.md) op
>* [&#x200B; voeg een sibling doelknoop tussen knopen &#x200B;](experience-target-node-add-sibling.md) toe
>* [&#x200B; de kindknopen en creatieven van het Exemplaar aan een andere knoop op het zelfde niveau &#x200B;](experience-target-node-copy.md)
>* [&#x200B; wijs creatieve elementen aan een definitieve knoop toe &#x200B;](experience-assign-creative-bundles.md)
>* [&#x200B; Schrap een doelknoop of creatieve bladknoop &#x200B;](/help/creative/experiences/experience-target-node-delete.md)
>* [&#x200B; creeer een ervaring met beslissingsboom richtend &#x200B;](experience-create-targeting.md)
>* [&#x200B; geef een ervaring met beslissingsboom uit richtend &#x200B;](experience-edit-targeting.md)
>* [&#x200B; gerichte ervaringsmontages &#x200B;](experience-settings-targeting.md)
