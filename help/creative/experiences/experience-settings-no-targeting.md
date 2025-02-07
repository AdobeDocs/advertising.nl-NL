---
title: Instellingen voor niet-doelgerichte ervaringen
description: Zie beschrijvingen van alle montages voor en ervaringen zonder beslissingsboom het richten.
feature: Creative Experiences
source-git-commit: fbf663b38282f48facab57efaf5533892642a252
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---

# Instellingen voor niet-doelgerichte ervaringen

*Gesloten bèta*

## [!UICONTROL Experience basics] -sectie

**[!UICONTROL Advertiser]:** (Alleen-lezen voor bestaande ervaringen) De adverteerder die een bod uitbrengt op de creatieve producten die in de ervaring zijn opgenomen. Wanneer u de ervaring hebt opgeslagen, kunt u de adverteerder niet meer wijzigen.

**[!UICONTROL Experience Name]:** Een unieke naam voor de ervaring. **Uiteinde:** gebruik een naam die gemakkelijk zal zijn te vinden wanneer u de ervaring als advertentie in Advertising DSP of andere DSP gebruikt.

**[!UICONTROL Creative Library]:** (Alleen-lezen voor bestaande ervaringen) Eén creatieve bibliotheek die u voor de ervaring kunt gebruiken. Nadat u de ervaring hebt opgeslagen, kunt u de bibliotheek niet meer wijzigen.

## [!UICONTROL Default creatives] -sectie

**\ [gespecificeerde Standaard creatieve creatieven \]:** de standaardbeeldcreatieve producten aan gebruik wanneer browser geen creatieve producten kan tonen die aan de ervaring worden toegewezen, zoals wanneer browser niet JavaScript-Toegelaten is of de advertentieserver kan niet de advertentie wegens vertragingen personaliseren. Voeg één creatieve afbeelding toe per advertentiegrootte waarvoor de ervaring geldt. Uw keuzes bepalen de creatieve formaten die voor de ervaring kunnen worden gebruikt. <!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. -->

Voor ervaringen zonder doelgericht gebruik van beslissingsstructuren kunt u de standaardcreatieven negeren met creatieven van dezelfde grootte binnen [!UICONTROL Tag Manager] . <!-- verify -->

* Als u een creatieve standaardafbeelding met verschillende afmetingen wilt toevoegen, klikt u op **[!UICONTROL + Add Sizes]** en schakelt u het selectievakje naast de creatieve elementen in die u vanuit het rechterdeelvenster wilt toevoegen. Klik vervolgens op **[!UICONTROL Add Creatives]** .

* Om gebrek creatief te schrappen, de curseur over de creatieve duimnagel te houden en ![ Schrapping ](/help/creative/assets/delete.png " te klikken schrapt ").

* Om alle standaardcreatieven te schrappen, klik ![ Schrapping ](/help/creative/assets/delete.png " ") **[!UICONTROL Delete all]**.

* Om de ruit van Creatieven op het recht te tonen of te verbergen, klik ](/help/creative/assets/hide-show-creatives.png " tonen/verbergen ") in het hogere recht van de juiste ruit.![

## [!UICONTROL Targeting] -sectie

**[!UICONTROL Targeting]:** (Read-only voor bestaande ervaringen) niet van toepassing wanneer u het richten niet wilt toelaten gebruikend een besluitvormingsboom; houd deze optie gehandicapt.

**[!UICONTROL Dynamic ads]:** (Alleen-lezen voor bestaande ervaringen) geeft aan dat de ervaring dynamische advertenties bevat. **Nota:** een ervaring kan of alle standaardadvertenties of alle dynamische advertenties omvatten.

**[!UICONTROL Language Targeting]:** (Ervaring met alleen standaardadvertenties; optioneel; alleen-lezen voor bestaande ervaringen) Controleert de taalinstellingen van de browser van de gebruiker en geeft een creatief item weer in de opgegeven taal wanneer een creatief item in die taal beschikbaar is. Wanneer een creatief element in de door de browser opgegeven taal niet beschikbaar is, wordt in plaats daarvan de instelling [!UICONTROL Preferred language] gebruikt. Nadat u de ervaring hebt opgeslagen, kunt u deze instelling niet meer wijzigen.

**[!UICONTROL Preferred language]:** (Ervaring met alleen standaardadvertenties; alleen-lezen voor bestaande ervaringen) De taal voor alle advertenties die uit de ervaring zijn gemaakt, behalve wanneer [!UICONTROL Language Targeting] is ingeschakeld. Nadat u de ervaring hebt opgeslagen, kunt u deze instelling niet meer wijzigen.

## [!UICONTROL Advanced] -sectie

**Voldoende Gegevens:** (Ervaringen met dynamische slechts advertenties; facultatief) om gebruikers te richten die op specifieke zeer belangrijke paren worden gebaseerd die de DSP, de uitgever, of de partner in echt - tijd op indruk overgaat. U kunt tot vijf sleutels van de gegevenspas (parameters) specificeren.<!-- May move this to just within the decision tree. -->

Wanneer u later een advertentietag voor een specifieke creatieve grootte creeert, wordt elke sleutel die op dit gebied wordt gespecificeerd toegevoegd als macro in de markering. U moet de waarde voor elk sleutel-waardepaar binnen de markering ingaan alvorens u de markering als advertentie in uw DSP uitvoert.

**Straal:** (Ervaringen met dynamische slechts advertenties; facultatief) een gebruikersstraal aan doel. Selecteer een straal van 0 mijl tot 200 mijl.<!-- Does this end up in the ad tag parameters? -->

**pixel van RT:** (Ervaringen met dynamische slechts advertenties; facultatief) A [!UICONTROL Creative] die pixel opnieuw richt aan potentieel doel. Wanneer u het richten binnen de beslissingsboom plaatst, kunt u één niveau van de knopen van het pixeldoel van RT omvatten en het pixel specificeren om voor elke knoop evenals de vereiste waarden voor de attributen van de pixel te richten die moeten aanwezig zijn om de creatieve creatieve bundels te tonen. Als u geen pixel op dit gebied specificeert, kunt u nog binnen de beslissingsboom specificeren.&lt;!— Van R: &quot;de pixel van RT zou via de inhoudselectie in Dynamische en opstelling moeten zijn&quot; — verduidelijk. Ik zie &quot;Datapass&quot; (één woord) in de dynamische advertentie-instellingen, maar ik weet niet hoe die instelling en deze ervaringsniveau één samenwerken. —>

**[!UICONTROL Label]:** <!-- should be "Labels" --> (Optioneel) Alle [!DNL Creative] -specifieke labels die u op de ervaring wilt toepassen. U kunt ervaringen door etiket in de mening van Ervaringen <!-- sic --> filtreren.

* Om bestaande etiketten te selecteren, klik ![ neer ](/help/creative/assets/chevron-down.png " "), en selecteer de controledoos naast elk etiket om toe te passen.

* Als u naar bestaande labels wilt zoeken, voert u een tekenreeks in de labelnaam in.

* Om een nieuw etiket tot stand te brengen om toe te passen, open de lijst, **+ voegt Etiket** toe, gaat een nieuwe etiketnaam op het [!UICONTROL Label] gebied in, en klikt dan **creeert**.

* Als u een label wilt verwijderen, schakelt u het selectievakje naast de labelnaam uit.

**[!UICONTROL Impression Tracking URL]:** (Optioneel) Een URL voor het bijhouden van de indruk door derden die u aan de URL van de bestemmingspagina wilt toevoegen voor een advertentie die u uit de ervaring hebt gemaakt. U kunt maximaal vijf URL&#39;s opnemen. Om extra URL toe te voegen, klik ](/help/creative/assets/create.png) pictogram ** [!UICONTROL Add More] en ga URL in.![

Nadat u een URL hebt ingevoerd, worden alle beschikbare macro&#39;s en de gegevens waarmee deze worden vervangen verderop op in de pagina weergegeven. Om één van de macro&#39;s in URL op te nemen, houd de curseur over de macrobeschrijving en klik ![ Exemplaar aan klembord ](/help/creative/assets/copy-to-clipboard.png " Exemplaar aan klembord "), en kleef dan de macro waar u het op het gebied URL wilt.

>[!NOTE]
>
>* In [!DNL Creative] worden automatisch eigen imitatie-trackingtags vooraf toegewezen aan de URL van de bestemmingspagina.
>* U kunt deze URL overschrijven voor elke creatieve functie in de ervaring.
>* U kunt ook JavaScript-code voor imitatie van derden invoeren in het veld [!UICONTROL Client JS]

**[!UICONTROL Click Tracking URL]:** (Optioneel) (Optioneel) Een URL voor het bijhouden van klikken door derden die wordt toegevoegd aan de URL van de bestemmingspagina. U kunt maximaal vijf URL&#39;s opnemen. Om extra URL toe te voegen, klik ![ pictogram ](/help/creative/assets/create.png) **[!UICONTROL Add More]** en ga URL in.

Nadat u een URL hebt ingevoerd, worden alle beschikbare macro&#39;s en de gegevens waarmee deze worden vervangen verderop op in de pagina weergegeven. Om één van de macro&#39;s in URL op te nemen, houd de curseur over de macrobeschrijving en klik ![ Exemplaar aan klembord ](/help/creative/assets/copy-to-clipboard.png " Exemplaar aan klembord "), en kleef dan de macro waar u het op het gebied URL wilt.

>[!NOTE]
>
>* In [!DNL Creative] worden automatisch eigen imitatie-trackingtags vooraf toegewezen aan de URL van de bestemmingspagina.
>* U kunt dit URL voor om het even welke creatieve <!-- creative bundle for targeted experiences --> in de ervaring met voeten treden.

**[!UICONTROL Client JS]:** (Optioneel) Een van de volgende opties:

* (Wanneer de adverteerder een leverancier van OBA-compatibiliteit voor de advertenties gebruikt) JavaScript-code die verwijst naar de advertentie-overlay waarmee gebruikers kunnen weigeren zich online te richten op gedragingen (OBA).

* Eventuele JavaScript-code voor het bijhouden van de indruk die door derden wordt bijgevoegd bij de landingspagina. **Nota:** U kunt een derde ook een beeld-volgende URL op het [!UICONTROL Impression Tracking URL] gebied ingaan.

>[!MORELIKETHIS]
>
>* [ creeer een ervaring zonder beslissingsboom richtend ](experience-create-no-targeting.md)
>* [ geef een ervaring zonder beslissingsboom uit richtend ](experience-edit-no-targeting.md)
>* [ creeer manueel een ad markering voor een toepasselijke creatieve grootte ](experience-tag-create-manually.md)
>* [ wijs creatieve elementen aan een ad markering voor ervaringen toe zonder zich te richten ](experience-tag-assign-creatives.md)
>* [ pas het volgen URLs voor een ervaring aan zonder zich ](experience-tracking-urls-no-targeting.md) te richten
>* [ pas creatieve optimalisering en het plannen voor een ervaring aan zonder zich ](experience-optimization-scheduling-no-targeting.md) te richten
