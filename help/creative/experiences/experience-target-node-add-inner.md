---
title: Een doelknooppunt toevoegen tussen knooppunten in een ervaring
description: Leer hoe u een doelknooppunt tussen doelknooppunten in een advertentie kunt toevoegen.
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# Een doelknooppunt toevoegen tussen knooppunten in een ervaring

*Ervaringen met beslissingsboom richtend slechts*
*Gesloten bèta*

Wanneer u een doelknoop tussen bestaande niveaus opneemt, behoudt de nieuwe doelknoop alle bestaande kinddoelstellingen en creatieven, en de nieuwe knoop wordt aanvankelijk geroepen &quot;allen.&quot; U kunt optioneel het nieuwe knooppunt behouden zonder meer specifieke doelen toe te voegen.

Om een specifiek doel te bepalen, voeg een extra sibling doelknoop op het zelfde niveau toe, specificeer het nieuwe doel, en wijs dan creatief aan enkel dat doel toe. Dit leidt tot de nieuwe doelknoop en beweegt alle kinddoelstellingen en creatieven die eerder aan &quot;allen&quot;aan een nieuwe &quot;Al anders&quot;knoop op het zelfde niveau werden toegewezen. Op deze manier worden de bestaande onderliggende vertakkingen niet beïnvloed door de toevoeging van het nieuwe doel, omdat alleen het nieuwe knooppunt op hetzelfde niveau de nieuwe doelgegevens bevat.

>[!NOTE]
>
>Om een doelknoop aan het bodemniveau van een besluitvormingsboom toe te voegen, zie &quot;[ een doelknoop aan het definitieve niveau in een ervaring ](experience-target-node-add-final.md) toevoegen.&quot;

<!-- 1. [ways to get to the decision tree] -->

1. Onder de knoop waarbij u het doel wilt opnemen, ![ ](/help/creative/assets/add.png " toevoegen ") klikken, en dan selecteren **[!UICONTROL Insert New Target]**.

1. Voer een van de volgende handelingen uit:

   * Als knooppunten op hetzelfde niveau nog niet bestaan, gaat u als volgt te werk:

      1. Selecteer het doeltype en klik op **[!UICONTROL Apply]** :

         * Selecteer **[!UICONTROL Adobe Audience]** voor doelwitten van publiek Adobe.

         * Voor geografische doelen selecteert u één geografische categorie (zoals [!UICONTROL Geo: Country]).

         * Selecteer **[!UICONTROL Data Pass]** voor gegevensdoorvoerdoelen.

         * Voor het opnieuw richten van pixeldoelstellingen, uitgezochte ** [!UICONTROL RT Pixel].

         * Selecteer één doelcategorie (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** of **[!UICONTROL Device: Browser]** ) voor apparaatdoelen.

   * Als knooppunten op hetzelfde niveau al bestaan, gaat u als volgt te werk:

      * Ga als volgt te werk voor doelgroepen voor publiek Adobe:

         1. Klik op **[!UICONTROL Click to Browse]** om de [!UICONTROL Audience Targeting] -opties te openen, open het tabblad **[!UICONTROL Adobe Segments]** , geef een of meer van de [!DNL Adobe] publieksdoelen van de adverteerder op en klik op **[!UICONTROL Create]**<!-- Why not "Save" like for the other node types/use cases? -->.

         1. (Optioneel) Als u meerdere doelknooppunten wilt maken wanneer meerdere soorten publiek zijn opgegeven, selecteert u **[!UICONTROL Split targets to create nodes]** .

            Hiermee wordt een afzonderlijk doelknooppunt (met afzonderlijke creatieve bundels) voor elk opgegeven publiek gemaakt. Als u de doelen niet splitst, moet de gebruiker bij alle opgegeven doelgroepen horen.

         1. Klik op **[!UICONTROL Apply]**.

      * Ga als volgt te werk voor geografische doelen:

         1. Klik op **[!UICONTROL Click to Browse]** om de [!UICONTROL Geo Targeting] -opties te openen, geef een of meer geografische doelen op en klik op **[!UICONTROL Save]** .

            Postcodedoelen hebben opties voor bulkbewerking. Als u meerdere postcodes wilt plakken, klikt u op de tab **[!UICONTROL Paste postal codes]** , selecteert u het land, plakt of voert u postcodes in die door komma&#39;s of op afzonderlijke regels zijn gescheiden, en klikt u op **[!UICONTROL Include All]** . Om een inbegrepen zip codedoel te verwijderen, houd de curseur over het doel en klik ![ verwijder ](/help/creative/assets/delete.png " ") **[!UICONTROL Remove]**.

         1. (Optioneel) Als u meerdere doelknooppunten wilt maken wanneer meerdere geografische doelen zijn opgegeven, selecteert u **[!UICONTROL Split targets to create nodes]** .

            Hierdoor wordt een afzonderlijk doelknooppunt (met afzonderlijke creatieve bundels) gemaakt voor elk opgegeven geografische doel. Als u de doelen niet splitst, moet de gebruiker tot alle opgegeven locaties behoren.

         1. Klik op **[!UICONTROL Apply]**.

      * Voer voor een gegevensdoorvoerdoel één waarde voor de gegevensdoorloop in en klik op **[!UICONTROL Apply]** .

        De sleutel voor het zeer belangrijk-waardepaar wordt reeds geplaatst op het **[!UICONTROL Data Pass]** gebied in de [!UICONTROL Advanced] sectie van de [ ervaringsmontages ](experience-settings-targeting.md).

      * Selecteer voor een heroriënterend pixeldoel één herrichtingspixel dat u wilt gebruiken en de vereiste waarden voor de kenmerken van een pixel die aanwezig moeten zijn om de creatieve elementen weer te geven. Klik vervolgens op **[!UICONTROL Apply]** .

        De attributen voor het opnieuw richten pixel worden gevormd in [ het opnieuw richten pixelmontages ](/help/creative/pixels/retargeting-pixel-manage.md).

      * Ga als volgt te werk voor apparaatdoelen:

         1. Selecteer de doelen.

         1. (Optioneel) Als u meerdere doelknooppunten wilt maken wanneer meerdere geografische doelen zijn opgegeven, selecteert u **[!UICONTROL Split targets to create nodes]** .

            Hierdoor wordt een afzonderlijk doelknooppunt (met afzonderlijke creatieve bundels) gemaakt voor elk opgegeven geografische doel. Als u de doelen niet splitst, moet de gebruiker tot alle opgegeven locaties behoren.

         1. (Optioneel) Als u meerdere doelknooppunten wilt maken wanneer meerdere geografische doelen zijn opgegeven, selecteert u **[!UICONTROL Split targets to create nodes]** .

         1. Klik op **[!UICONTROL Apply]**.

1. Voer een van de volgende handelingen uit:

   * (Facultatief) [ wijst creatieve personen ](experience-assign-creative-bundles.md) aan de nieuwe doelknoop en aan de &quot;Al Else&quot;knoop toe.

   * (Facultatief) [ voeg een sibling doelknoop ](experience-target-node-add-sibling.md) toe die een doel van het gespecificeerde type zal omvatten.

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
>* [ voeg een sibling doelknoop tussen knopen ](experience-target-node-add-sibling.md) toe
>* [ de kindknopen en creatieven van het Exemplaar aan een andere knoop op het zelfde niveau ](experience-target-node-copy.md)
>* [ wijs creatieve elementen aan een definitieve knoop toe ](experience-assign-creative-bundles.md)
>* [ Schrap een doelknoop of creatieve bladknoop ](/help/creative/experiences/experience-target-node-delete.md)
>* [ creeer een ervaring met beslissingsboom richtend ](experience-create-targeting.md)
>* [ geef een ervaring met beslissingsboom uit richtend ](experience-edit-targeting.md)
>* [ gerichte ervaringsmontages ](experience-settings-targeting.md)
