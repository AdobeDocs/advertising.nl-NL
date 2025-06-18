---
title: Voeg een sibling doelknoop tussen knopen in een ervaring toe
description: Leer hoe te om een sibling knoop aan om het even welke knoop toe te voegen die een doel heeft of op het zelfde niveau zoals een knoop met een doel is.
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
source-git-commit: 8961833c854ed41e4cca69787a5dc70dce2f203c
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Voeg een sibling doelknoop tussen knopen in een ervaring toe

*Ervaringen met beslissingsboom richtend slechts*
*Gesloten bèta*

U kunt een sibling knoop aan om het even welke knoop toevoegen die een doel heeft of op het zelfde niveau zoals een knoop met een doel is.

<!-- 1. Open the decision tree:


In a new experience


In an existing experience,
 -->

1. Boven de knoop waaraan u de sibling knoop wilt toevoegen, ![ ](/help/creative/assets/add.png " toevoegen ") klikken, en dan selecteren **[!UICONTROL Insert Sibling Target]**.

1. Geef de doelen op:

   * Ga als volgt te werk voor Adobe Audience-doelen:

      1. Klik op **[!UICONTROL Click to Browse]** om de [!UICONTROL Audience Targeting] -opties te openen, open het tabblad **[!UICONTROL Adobe Segments]** , geef een of meer van de [!DNL Adobe] publieksdoelen van de adverteerder op en klik op **[!UICONTROL Save]** .

      1. (Optioneel) Als u meerdere doelknooppunten wilt maken wanneer meerdere soorten publiek zijn opgegeven, selecteert u **[!UICONTROL Split targets to create nodes]** .

         Met deze functie maakt u een afzonderlijk doelknooppunt (met afzonderlijke creatieve bundels) voor elk opgegeven publiek. Als u de doelen niet splitst, moet de gebruiker bij alle opgegeven doelgroepen horen (een [!DNL Boolean] `AND` -instructie).

      1. Klik op **[!UICONTROL Apply]**.

   * Ga als volgt te werk voor geografische doelen:

      1. Klik op **[!UICONTROL Click to Browse]** om de [!UICONTROL Geo Targeting] -opties te openen, geef een of meer geografische doelen op en klik op **[!UICONTROL Save]** .

         Postcodedoelen hebben opties voor bulkbewerking. Als u meerdere postcodes wilt plakken, klikt u op de tab **[!UICONTROL Paste postal codes]** , selecteert u het land, plakt of voert u postcodes in die door komma&#39;s of op afzonderlijke regels zijn gescheiden, en klikt u op **[!UICONTROL Include All]** . Om een inbegrepen zip codedoel te verwijderen, houd de curseur over het doel en klik ![ verwijder ](/help/creative/assets/delete.png " ") **[!UICONTROL Remove]**.

      1. (Optioneel) Als u meerdere doelknooppunten wilt maken wanneer meerdere geografische doelen zijn opgegeven, selecteert u **[!UICONTROL Split targets to create nodes]** .

         Met deze functie maakt u een afzonderlijk doelknooppunt (met afzonderlijke creatieve bundels) voor elk opgegeven geografische doel. Als u de doelen niet splitst, moet de gebruiker tot alle opgegeven locaties behoren (een [!DNL Boolean] `AND` -instructie).

      1. Klik op **[!UICONTROL Apply]**.

   * Voor gegevensdoorvoerdoelen past u desgewenst de gegevensdoorvoersleutel aan, voert u één waarde voor de gegevensdoorloop in en klikt u op **[!UICONTROL Apply]** .

     Een standaardwaarde voor de sleutel in het zeer belangrijk-waardepaar wordt reeds geplaatst op het **[!UICONTROL Data Pass]** gebied in de [!UICONTROL Advanced] sectie van de [ ervaringsmontages ](experience-settings-targeting.md). U kunt de toets desgewenst aanpassen.

   * Als u pixeldoelen opnieuw wilt toewijzen, selecteert u de opnieuw te gebruiken pixel en de vereiste waarden voor de kenmerken van een pixel die aanwezig moeten zijn om de creatieve elementen weer te geven. Klik vervolgens op **[!UICONTROL Apply]** .

     De attributen voor het opnieuw richten pixel worden gevormd in [ het opnieuw richten pixelmontages ](/help/creative/pixels/retargeting-pixel-manage.md).

   * Ga als volgt te werk voor apparaatdoelen:

      1. Selecteer de doelen.

      1. (Optioneel) Als u meerdere doelknooppunten wilt maken wanneer meerdere geografische doelen zijn opgegeven, selecteert u **[!UICONTROL Split targets to create nodes]** .

         Met deze functie maakt u een afzonderlijk doelknooppunt (met afzonderlijke creatieve bundels) voor elk opgegeven geografische doel. Als u de doelen niet splitst, moet de gebruiker tot alle opgegeven locaties behoren (een [!DNL Boolean] `AND` -instructie).

      1. Klik op **[!UICONTROL Apply]**.

1. (Optioneel) Geef een aangepaste vertakkingsnaam op voor een door de gebruiker gedefinieerde vertakking.

   Door gebrek, user-defined takken worden geëtiketteerd met de toegepaste doelstellingen.

   U kunt geen aangepaste vertakkingsnaam maken voor een vertakking Alles of Iedereen anders.

   1. Plaats de cursor op het doelknooppunt en klik op **[!UICONTROL ...]** > **[!UICONTROL Edit Name]** .

   1. Voer de **[!UICONTROL Node Name]** in en klik op **[!UICONTROL Save]** .

1. Voer een van de volgende handelingen uit:

   * (Facultatief) [ wijst creatieve personen ](experience-assign-creative-bundles.md) aan de nieuwe doelknoop toe.

   * (Optioneel) U kunt de ervaring als volgt opslaan:

      1. Klik op **[!UICONTROL Save]** en vervolgens op **[!UICONTROL OK]** .

      1. (Als elk knooppunt op het laagste niveau niet ten minste één creatief knooppunt bevat): Voer een van de volgende handelingen uit:

         * Klik op **[!UICONTROL Save as Draft]** om de ervaring zonder alle vereiste creatieve bundels op te slaan.

           U kunt geen ad-tag maken voor een conceptervaring.

         * Klik op **[!UICONTROL Assign Default Creatives]** als u de standaard creatieve waarde wilt toewijzen aan elk doel waaraan nog geen creatieve bundel is toegewezen. Klik op **[!UICONTROL Save]** en **[!UICONTROL OK]** nadat u de bijgewerkte structuur hebt bekeken waaraan de standaardcreatieven zijn toegewezen.

         * Klik op **[!UICONTROL Continue Edit]** als u de beslissingstructuur wilt blijven bewerken.

>[!MORELIKETHIS]
>
>* [ voeg een doelknoop aan het definitieve niveau toe ](experience-target-node-add-final.md)
>* [ neem een doelknoop tussen knopen ](experience-target-node-add-inner.md) op
>* [ de kindknopen en creatieven van het Exemplaar aan een andere knoop op het zelfde niveau ](experience-target-node-copy.md)
>* [ wijs creatieve elementen aan een definitieve knoop toe ](experience-assign-creative-bundles.md)
>* [ Schrap een doelknoop of creatieve bladknoop ](/help/creative/experiences/experience-target-node-delete.md)
>* [ creeer een ervaring met beslissingsboom richtend ](experience-create-targeting.md)
>* [ geef een ervaring met beslissingsboom uit richtend ](experience-edit-targeting.md)
>* [ gerichte ervaringsmontages ](experience-settings-targeting.md)
