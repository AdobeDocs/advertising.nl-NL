---
title: Creatieve bundels beheren
description: Meer informatie over xxxx.
feature: Creative Bundles
exl-id: a9ed4e8f-db93-46d5-9231-2b3bb0aa072a
source-git-commit: a07af2b3a49d47f5e4ec276ab82520df46d6068a
workflow-type: tm+mt
source-wordcount: '1359'
ht-degree: 0%

---

# Creatieve bundels beheren

*Gesloten bèta*

<!--
**I'll probably split this up into multiple pages since the creative-related topics are separate**
-->

Bundels zijn groepen creatieve elementen die u als eenheid aan een ervaring kunt toevoegen. Nadat u een bundelcontainer hebt gemaakt, kunt u creatieve elementen aan de bundel koppelen. Standaardbundels kunnen alleen standaardadvertenties bevatten en dynamische bundels kunnen alleen dynamische advertenties bevatten. U kunt de landingspagina&#39;s, de beeld-volgtags, en klik-volgmarkeringen voor alle creatieve binnen een bundel met voeten treden die aan een ervaring van binnen de ervaring beslissingsboom wordt toegewezen, zonder de basiscreatieven te beïnvloeden.

[!DNL Creative] roteert door de creatieve elementen in de bundel zoals gespecificeerd voor elke ervaring waaraan de bundel wordt toegewezen. U kunt desgewenst toestaan dat [!DNL Creative] de advertentie-elementen optimaliseert voor elke ervaring op basis van prestaties met behulp van algoritme en rotatie, die door Adobe Sensei wordt aangedreven.

Om de optimalisatie van advertentie-elementen tussen bundels in een advertentiervaring mogelijk te maken, kan elke bundel slechts één van elke combinatie \[creatieve grootte + taal\] bevatten. Als een bundel bijvoorbeeld één creatieve 250 x 250 met de standaardtaal &quot;Frans&quot; bevat, kunt u geen tweede creatieve 250 x 250 met de standaardtaal &quot;Frans&quot; toevoegen. Als u meerdere creatieven van dezelfde grootte in dezelfde taal hebt, voegt u deze dan afzonderlijk toe aan de ervaring.

Creatieve producten die aan bundels zijn gekoppeld, zijn nog steeds beschikbaar als afzonderlijke creatieve producten. U kunt één creatieve bundel toevoegen aan meerdere bundels. Als u instellingen bewerkt voor een creatief object dat aan een bundel is gekoppeld, worden de wijzigingen doorgegeven aan de bundel. Alle aangepaste openingspagina&#39;s, codes voor het bijhouden van de indruk en aanklikcodes die zijn geconfigureerd voor de creatieve toepassingen in een bepaalde ervaring, worden echter altijd voor deze ervaring gebruikt.

<!-- multiselect only to duplicate and delete -->

## Een bundel maken voor een creatieve bibliotheek

U kunt een creatief element toevoegen aan meerdere bundels.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** .

1. Klik op de naam van de bibliotheek.

1. Klik op de tab **[!UICONTROL Bundles]** .

1. Klik rechtsboven op **[!UICONTROL Create]** > **[!UICONTROL Bundles]** > **[!UICONTROL Bundle]** .

1. Ga uniek **[!UICONTROL Bundle Name]** en **[!UICONTROL Bundle Type]in:** *Standaard* (voor standaardcreatieven) of *Dynamisch* (voor dynamische creatieve producten.

1. Klik op **[!UICONTROL Create]**.

## Creatieve elementen in een bundel weergeven

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** .

1. (Facultatief) [ pas de mening ](/help/creative/introduction/customize-data-views.md) aan om specifieke bibliotheken te omvatten.

1. Klik op de naam van de bibliotheek.

1. Klik op de tab **[!UICONTROL Bundles]** .

1. Klik op de bundelkaart of rij om alle creatieve elementen in de bundel weer te geven.

## Bundels dupliceren

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** .

1. (Facultatief) [ pas de mening ](/help/creative/introduction/customize-data-views.md) aan om specifieke bibliotheken te omvatten.

1. Klik op de naam van de bibliotheek.

1. Klik op de tab **[!UICONTROL Bundles]** .

1. Selecteer de bundels die u wilt dupliceren:

   * Een enkele bundel dupliceren:

      * Klik in de kaartweergave op **[!UICONTROL ...]** naast de bundelnaam en klik vervolgens op **[!UICONTROL Duplicate]** .

      * Houd in de tabelweergave de cursor boven de rij en klik op **[!UICONTROL Duplicate]** .

   * Als u een of meer bundels wilt dupliceren, schakelt u het selectievakje in voor elke bundel die u wilt dupliceren. Klik op de werkbalk voor bulkacties op **[!UICONTROL Duplicate].**

     Als u alle rijen wilt selecteren, schakelt u het selectievakje Algemeen linksboven in.

   De nieuwe bundels worden genoemd `<original name> (copy) # 1` (of het volgende aantal in de opeenvolging). Als u bijvoorbeeld twee duplicaten van &quot;Testbundel&quot; maakt, krijgen de duplicaten de naam &quot;Testbundel (kopie) # 1&quot; en &quot;Testbundel (kopie) # 2&quot;.

## Een bundelnaam bewerken

Wijzigingen in een bundelnaam worden doorgegeven in alle bijbehorende ervaringen.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** .

1. Klik op de naam van de bibliotheek.

1. Klik op de tab **[!UICONTROL Bundles]** .

1. Selecteer de bundel:

   * Klik in de kaartweergave op **[!UICONTROL ...]** naast de naam van de bibliotheek en klik vervolgens op **[!UICONTROL Edit]** .

   * Houd in de tabelweergave de cursor boven de rij en klik op **[!UICONTROL Edit]** .

1. Bewerk de **[!UICONTROL Bundle Name]** .

   De [!UICONTROL Bundle Name] moet uniek zijn.

1. Klik op **[!UICONTROL Update]**. <!-- inconsistent with "Edit" for creative libraries and creatives -->

## Creatieve elementen aan een bundel koppelen

U kunt [ bestaande standaardcreatieven ](/help/creative/creative-libraries/creative-libraries-about.md) aan een standaardbundel vastmaken en bestaande dynamische creatieve elementen <!-- [existing dynamic creatives](creative-dynamic-manage.md) --> aan een dynamische bundel vastmaken. Als u een creatief element aan een bundel koppelt, maakt u het creatieve materiaal beschikbaar in alle ervaringen waaraan het bundel is toegewezen. Elke bundel kan slechts één van elke combinatie \[creatieve grootte + taal\] bevatten.

>[!NOTE]
>
>U kunt creatieve elementen aan bundels van de StandaardAdvertenties en de Dynamische meningen van Advertenties [&#128279;](creative-attach-detach-bundles.md) ook vastmaken.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** .

1. (Facultatief) [ pas de mening ](/help/creative/introduction/customize-data-views.md) aan om specifieke bibliotheken te omvatten.

1. Klik op de naam van de bibliotheek.

1. Klik op de tab **[!UICONTROL Bundles]** .

1. Selecteer de bundel:

   * Klik in de kaartweergave op **[!UICONTROL ...]** naast de bundelnaam en klik vervolgens op **[!UICONTROL Attach Creatives]** .

   * Houd in de tabelweergave de cursor boven de rij en klik op **[!UICONTROL Attach Creatives]** .

   Elke creatieve waarde die in aanmerking komt voor het bundeltype, wordt in het rechterframe weergegeven. Creatieve elementen die al aan de bundel zijn gekoppeld, worden wel vermeld, maar kunnen niet worden geselecteerd.

1. (Facultatief) schakelaar tussen de standaardlijstmening en een kaartmening van de beschikbare bundels door ![&#128279;](/help/creative/assets/card-view-button.png " de mening van de Kaart van 0&rbrace; te klikken ") om de kaartmening te openen of ![Tabel-/lijstweergave](/help/creative/assets/table-view-button.png "Tabelweergave") om aan de lijstmening terug te keren.

1. Selecteer in het rechterframe het selectievakje naast de creatieve elementen die u aan de bundel wilt koppelen en klik op **[!UICONTROL Attach Creative to Bundle]** .

## Creatieve elementen loskoppelen van een bundel {#bundle-detach-creatives}

Als u een creatief element loskoppelt uit een bundel, wordt de koppeling tussen de twee verwijderd, zodat de creatieve elementen niet meer worden gebruikt voor ervaringen die op de bundel zijn gericht.

Als u een creatief element loskoppelt uit de bundel, wordt het creatieve element niet verwijderd uit het tabblad Creative in uw creatieve bibliotheek.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** .

1. (Facultatief) [ pas de mening ](/help/creative/introduction/customize-data-views.md) aan om specifieke bibliotheken te omvatten.

1. Klik op de naam van de bibliotheek.

1. Klik op de tab **[!UICONTROL Bundles]** .

1. Klik op de bundelkaart of rij om alle creatieve elementen in de bundel weer te geven.

1. Selecteer de creatieve elementen die u van de bundel wilt loskoppelen:

   * Een enkele creatieve bewerking loskoppelen:

      * Klik in de kaartweergave op **[!UICONTROL ...]** naast de naam van het origineel en klik vervolgens op **[!UICONTROL Detach]** .

      * Houd in de tabelweergave de cursor boven de rij en klik op **[!UICONTROL Detach]** .

   * Als u een of meer creatieve items wilt loskoppelen, schakelt u het selectievakje in voor elke creatieve optie die u wilt loskoppelen. Klik op de werkbalk voor bulkacties op **[!UICONTROL Detach]** .

     Als u alle rijen wilt selecteren, schakelt u het selectievakje Algemeen linksboven in.

## Eén creatieve voorvertoning in een bundel weergeven

U kunt een voorvertoning weergeven van een creatieve afbeelding, zoals hyperlinks, terwijl de gebruiker deze ziet.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** .

1. (Facultatief) [ pas de mening ](/help/creative/introduction/customize-data-views.md) aan om specifieke bibliotheken te omvatten.

1. Klik op de naam van de bibliotheek.

1. Klik op de tab **[!UICONTROL Bundles]** .

1. Klik op de bundelkaart of rij om alle creatieve elementen in de bundel weer te geven.

1. Selecteer de creatieve:

   * Klik in de kaartweergave op **[!UICONTROL ...]** naast de naam van het origineel en klik vervolgens op **[!UICONTROL Preview]** .

   * Houd in de tabelweergave de cursor boven de rij en klik op **[!UICONTROL Preview]** .

1. (Optioneel) Als u het formaat van de afbeelding wilt wijzigen binnen het scherm, selecteert u een optie in de lijst van **[!UICONTROL Zoom]** , van 10% tot 100% van de afbeeldingsgrootte.

<!-- Not there as of 1/22/24:  1. (Flexible HTML5 creatives; optional) To show all frames for the creative, select **Show frames**. -->

1. (Optioneel) Als u de openingspagina voor de creatieve projecten wilt openen, klikt u op de creatieve pagina.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Facultatief) om creatief te downloaden, klik ![ Download ](/help/creative/assets/download.png " ").

   Het bestand wordt gedownload volgens de normale procedure van uw browser.

## Alle creatieve elementen in een bundel voorvertonen

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** .

1. Klik op de naam van de bibliotheek.

1. Klik op de tab **[!UICONTROL Bundles]** .

1. Selecteer de bundel:

   * Klik in de kaartweergave op **[!UICONTROL ...]** naast de bundelnaam en klik vervolgens op **[!UICONTROL Preview]** .

   * Houd in de tabelweergave de cursor boven de rij en klik op **[!UICONTROL Preview]** .

1. (Optioneel) Als u de creatieve elementen wilt filteren op taal, selecteert u een optie in de lijst **[!UICONTROL Language]** en klikt u vervolgens op **[!UICONTROL Preview]** rechtsboven in de voorvertoning.

1. (Optioneel) Als u de creatieve elementen wilt filteren op grootte, selecteert u een optie in de lijst **[!UICONTROL Size]** en klikt u vervolgens op **[!UICONTROL Preview]** rechtsboven in de voorvertoning.

1. (Optioneel) Als u het formaat van de afbeeldingen in het scherm wilt wijzigen, selecteert u een optie in de lijst van **[!UICONTROL Zoom]** , van 10% tot 100% van de afbeeldingsgrootte.

1. (Optioneel) Als u de openingspagina voor een creatieve pagina wilt openen, klikt u op de knop Creatief.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Optioneel) U kunt als volgt een demo-URL delen zodat andere personen zonder aanmelding bij [!DNL Creative] een voorvertoning van de creatieve documenten kunnen weergeven:

   1. Klik ![&#128279;](/help/creative/assets/share.png " Aandeel 1&rbrace; van het Aandeel ") in het hogere recht van de voorproef.

   1. Klik in het dialoogvenster [!UICONTROL Share Demo URL] op **[!UICONTROL Copy]** om de URL naar het klembord te kopiëren, zodat u deze met iemand anders kunt delen.

<!-- Not there as of 1/22/25:

## Edit the landing page and tracking tags for the creatives in a standard creative bundle

*Standard creative bundles only*

[Verify and edit all this, including the command names and where they're available. This is supposed to be a single and bulk action from within the right frame when you've open bundle details for a single bundle -- not from the Bundles table view.]

This procedure customizes the landing page, impression-tracking tags, and click-tracking tags for the creatives only within the context of the bundle. It doesn't change the settings for the base creative in [!UICONTROL Creative Libraries].

The custom URL and tags are applied to a creative when the bundle is assigned to an experience and the creative is served for the experience.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle name.

1. In the right pane, XXXXXXXXXXXX.

1. 

1. Edit any of the following settings: **[!UICONTROL Landing Page]**, **[!UICONTROL Click Tags]**, **[!UICONTROL Impression Tags]**.[Verify, and is can you do this for only one creative or is multiselect available?]

1.

 -->

## Bundels verwijderen

U kunt bundels schrappen die niet aan a [ levende ](/help/creative/experiences/experience-about.md#experience-statuses-experience-statuses) ervaring worden toegewezen. Als een bundel aan een levende ervaring wordt toegewezen, dan [ verwijder de bundel uit de beslissingsboom ](/help/creative/experiences/experience-target-node-delete.md) voor de ervaring alvorens u verdergaat.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]** .

1. (Facultatief) [ pas de mening ](/help/creative/introduction/customize-data-views.md) aan om specifieke bibliotheken te omvatten.

1. Klik op de naam van de bibliotheek.

1. Klik op de tab **[!UICONTROL Bundles]** .

1. Selecteer de te verwijderen bundels:

   * Eén bundel verwijderen:

      * Klik in de kaartweergave op **[!UICONTROL ...]** naast de bundelnaam en klik vervolgens op **[!UICONTROL Delete]** .

      * Houd in de tabelweergave de cursor boven de rij en klik op **[!UICONTROL Delete]** .

   * Als u een of meer bundels wilt verwijderen, schakelt u het selectievakje in voor elke bundel die u wilt verwijderen. Klik op de werkbalk voor bulkacties op **[!UICONTROL Delete].**

     Als u alle rijen wilt selecteren, schakelt u het selectievakje Algemeen linksboven in.

1. Klik in het bevestigingsbericht op **[!UICONTROL Delete].**

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [ wijs creatieve bundels aan een definitieve knoop in een ervaring toe en unassign ](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [ Voorproef creatieve ](/help/creative/creative-libraries/creative-preview.md)
>* [ voeg standaardcreatieve creatieve bibliotheek ](/help/creative/creative-libraries/creative-add-standard.md) toe
>* [ beheer creatieve bibliotheken ](/help/creative/creative-libraries/creative-library-manage.md)
>* [ Ongeveer uw creatieve bibliotheken ](/help/creative/creative-libraries/creative-libraries-about.md)
