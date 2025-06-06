---
title: Voeg een doelknooppunt toe aan het uiteindelijke niveau in een ervaring
description: Leer hoe u een doelnode toevoegt aan het uiteindelijke doelniveau van een advertentie.
feature: Creative Experiences
exl-id: 3ff657d5-bad1-47f4-a3ec-9ea678fd3c9d
source-git-commit: 05bcaa63779856cfea2f9cd3a0ab5d5e9d3d472a
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Voeg een doelknooppunt toe aan het uiteindelijke niveau in een ervaring

*Ervaringen met beslissingsboom richtend slechts*
*Gesloten bèta*

Wanneer u een doelknoop aan het bodem-meest niveau in de ervaring toevoegt — of het de wortel &quot;Al&quot;knoop, een doel-specifieke knoop, of een &quot;Al Else&quot;knoop is — u bepaalt direct het doel en te hoeven niet om een sibling knoop tot stand te brengen. Als u een knooppunt op het onderste niveau toevoegt, maakt u het doelknooppunt en een extra knooppunt &quot;All Else&quot; op hetzelfde niveau.

>[!NOTE]
>
>Om een doelknoop tussen bestaande niveaus van een besluitvormingsboom op te nemen, zie &quot;[ een doelknoop tussen knopen in een ervaring ](experience-target-node-add-inner.md) opnemen.&quot;

<!-- 1. [ways to get to the decision tree] -->

1. Onder de knoop waarbij u het doel wilt opnemen, ![ ](/help/creative/assets/add.png " toevoegen ") klikken, en dan selecteren **[!UICONTROL Insert New Target]**.

1. Geef de doelen op:

   * Selecteer **[!UICONTROL Adobe Audience]** voor Adobe Audience-doelen en voer de volgende handelingen uit:

      1. Klik op **[!UICONTROL Click to Browse]** om de [!UICONTROL Audience Targeting] -opties te openen, open het tabblad **[!UICONTROL Adobe Segments]** , geef een of meer van de [!DNL Adobe] publieksdoelen van de adverteerder op en klik op **[!UICONTROL Create]** .

      1. (Optioneel) Als u meerdere doelknooppunten wilt maken wanneer meerdere soorten publiek zijn opgegeven, selecteert u **[!UICONTROL Split targets to create nodes]** .

         Met deze functie maakt u een afzonderlijk doelknooppunt (met afzonderlijke creatieve bundels) voor elk opgegeven publiek. Als u de doelen niet splitst, moet de gebruiker bij alle opgegeven doelgroepen horen (een [!DNL Boolean] `AND` -instructie).

      1. Klik op **[!UICONTROL Apply]**.

   * Voor geografische doelen selecteert u één geografische categorie (zoals [!UICONTROL Geo: Country]) en voert u de volgende handelingen uit:

      1. Klik op **[!UICONTROL Click to Browse]** om de [!UICONTROL Geo Targeting] -opties te openen, geef een of meer geografische doelen op en klik op **[!UICONTROL Save]** .

         Postcodedoelen hebben opties voor bulkbewerking. Als u meerdere postcodes wilt plakken, klikt u op de tab **[!UICONTROL Paste postal codes]** , selecteert u het land, plakt of voert u postcodes in die door komma&#39;s of op afzonderlijke regels zijn gescheiden, en klikt u op **[!UICONTROL Include All]** . Om een inbegrepen zip codedoel te verwijderen, houd de curseur over het doel en klik ![ verwijder ](/help/creative/assets/delete.png " ") **[!UICONTROL Remove]**.

      1. (Optioneel) Als u meerdere doelknooppunten wilt maken wanneer meerdere geografische doelen zijn opgegeven, selecteert u **[!UICONTROL Split targets to create nodes]** .

         Met deze functie maakt u een afzonderlijk doelknooppunt (met afzonderlijke creatieve bundels) voor elk opgegeven geografische doel. Als u de doelen niet splitst, moet de gebruiker tot alle opgegeven locaties behoren (een [!DNL Boolean] `AND` -instructie).

      1. Klik op **[!UICONTROL Apply]**.

   * Selecteer **[!UICONTROL Data Pass]** voor een gegevensdoorvoerdoel, pas desgewenst de gegevensdoorvoersleutel aan, voer één gegevensdoorvoerwaarde in en klik op **[!UICONTROL Apply]** .

   Een standaardwaarde voor de sleutel in het zeer belangrijk-waardepaar wordt reeds geplaatst op het **[!UICONTROL Data Pass]** gebied in de [!UICONTROL Advanced] sectie van de [ ervaringsmontages ](experience-settings-targeting.md). U kunt de toets desgewenst aanpassen.

   * Selecteer **[!UICONTROL RT Pixel]** als u een pixeldoel opnieuw wilt toewijzen, selecteer één nieuwe doelpixel en de waarden voor de kenmerken van een pixel die nodig zijn om de creatieve elementen weer te geven. Klik vervolgens op **[!UICONTROL Apply]** .

     De attributen voor het opnieuw richten pixel worden gevormd in [ het opnieuw richten pixelmontages ](/help/creative/pixels/retargeting-pixel-manage.md).

   * Ga als volgt te werk voor apparaatdoelen:

      1. Selecteer één doelcategorie (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** of **[!UICONTROL Device: Browser]** ) en selecteer vervolgens de doelen.

      1. (Optioneel) Als u meerdere doelknooppunten wilt maken wanneer meerdere geografische doelen zijn opgegeven, selecteert u **[!UICONTROL Split targets to create nodes]** .

         Met deze functie maakt u een afzonderlijk doelknooppunt (met afzonderlijke creatieve bundels) voor elk opgegeven geografische doel. Als u de doelen niet splitst, moet de gebruiker tot alle opgegeven locaties behoren (een [!DNL Boolean] `AND` -instructie).

      1. Klik op **[!UICONTROL Apply]**.

1. Voer een van de volgende handelingen uit:

   * (Facultatief) [ wijst creatieve personen ](experience-assign-creative-bundles.md) aan de nieuwe doelknoop en aan de &quot;Al Else&quot;knoop toe.

   * (Optioneel) U kunt de ervaring als volgt opslaan:

      1. Klik op **[!UICONTROL Save]** en vervolgens op **[!UICONTROL OK]** .

      1. (Als elk knooppunt op het laagste niveau niet ten minste één creatief knooppunt bevat): Voer een van de volgende handelingen uit:

         * Klik op **[!UICONTROL Save as Draft]** om de ervaring zonder alle vereiste creatieve bundels op te slaan.

           U kunt geen ad-tag maken voor een conceptervaring.

         * Klik op **[!UICONTROL Assign Default Creatives]** als u de standaard creatieve waarde wilt toewijzen aan elk doel waaraan nog geen creatieve bundel is toegewezen. Klik op **[!UICONTROL Save]** en **[!UICONTROL OK]** nadat u de bijgewerkte structuur hebt bekeken waaraan de standaardcreatieven zijn toegewezen.

         * Klik op **[!UICONTROL Continue Edit]** als u de beslissingstructuur wilt blijven bewerken.

>[!MORELIKETHIS]
>
>* [ neem een doelknoop tussen knopen ](experience-target-node-add-inner.md) op
>* [ voeg een sibling doelknoop tussen knopen ](experience-target-node-add-sibling.md) toe
>* [ de kindknopen en creatieven van het Exemplaar aan een andere knoop op het zelfde niveau ](experience-target-node-copy.md)
>* [ wijs creatieve elementen aan een definitieve knoop toe ](experience-assign-creative-bundles.md)
>* [ Schrap een doelknoop of creatieve bladknoop ](/help/creative/experiences/experience-target-node-delete.md)
>* [ creeer een ervaring met beslissingsboom richtend ](experience-create-targeting.md)
>* [ geef een ervaring met beslissingsboom uit richtend ](experience-edit-targeting.md)
>* [ gerichte ervaringsmontages ](experience-settings-targeting.md)
