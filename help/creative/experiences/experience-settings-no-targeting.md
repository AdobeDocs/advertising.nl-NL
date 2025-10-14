---
title: Instellingen voor niet-doelgerichte ervaringen
description: Zie beschrijvingen van alle montages voor en ervaringen zonder beslissingsboom het richten.
feature: Creative Experiences
exl-id: aeeca035-8ae2-4173-827a-b8690d228549
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '1126'
ht-degree: 0%

---

# Instellingen voor niet-doelgerichte ervaringen

## [!UICONTROL Experience basics] -sectie

**[!UICONTROL Ad Type]:** (Alleen-lezen voor bestaande ervaringen) Het type advertenties dat in de ervaring is opgenomen: *[!UICONTROL Standard Display]*, *[!UICONTROL Dynamic Display]* of *[!UICONTROL Video]* . Nadat u de ervaring hebt opgeslagen, kunt u het advertentietype niet meer wijzigen.

**[!UICONTROL Advertiser]:** (Alleen-lezen voor bestaande ervaringen) De adverteerder die een bod uitbrengt op de creatieve producten die in de ervaring zijn opgenomen. Wanneer u de ervaring hebt opgeslagen, kunt u de adverteerder niet meer wijzigen.

**[!UICONTROL Experience Name]:** Een unieke naam voor de ervaring. **Uiteinde:** gebruik een naam die u gemakkelijk kunt vinden wanneer u de ervaring als advertentie in Advertising DSP of andere DSP gebruikt.

**[!UICONTROL Creative Library]:** (Alleen-lezen voor bestaande ervaringen) Eén creatieve bibliotheek die u voor de ervaring kunt gebruiken. Nadat u de ervaring hebt opgeslagen, kunt u de bibliotheek niet meer wijzigen.

## [!UICONTROL Default creatives] -sectie

**\ [gespecificeerde Standaard creatieve creatieven \]:** de standaardcreatieve producten aan gebruik wanneer browser geen creatieve producten kan tonen die aan de ervaring worden toegewezen, zoals wanneer browser niet JavaScript-Toegelaten is of de advertentieserver kan niet de advertentie wegens vertragingen personaliseren. Voor een standaardweergave neemt u één creatieve afbeelding op per advertentiegrootte waarvoor de ervaring van toepassing is. Voor een video-ervaring van standaardkwaliteit neemt u één creatieve video op per advertentiegrootte waarvoor de ervaring geldt. Uw keuzes bepalen de creatieve formaten die voor de ervaring kunnen worden gebruikt.

Voor ervaringen zonder doelgericht gebruik van beslissingsstructuren kunt u de standaardcreatieven negeren met creatieven van dezelfde grootte binnen [!UICONTROL Tag Manager] .

* Als u een creatieve standaardafbeelding met verschillende afmetingen wilt toevoegen, klikt u op **[!UICONTROL + Add Sizes]** en schakelt u het selectievakje naast de creatieve elementen in die u vanuit het rechterdeelvenster wilt toevoegen. Klik vervolgens op **[!UICONTROL Add Creatives]** .

* Om gebrek creatief te schrappen, de curseur over de creatieve duimnagel te houden en ![&#x200B; Schrapping &#x200B;](/help/creative/assets/delete.png " te klikken schrapt ").

* Om alle standaardcreatieven te schrappen, klik ![&#x200B; Schrapping &#x200B;](/help/creative/assets/delete.png " ") **[!UICONTROL Delete all]**.

* Om de ruit van Creatieven op het recht te tonen of te verbergen, klik ![&#x200B; tonen/verbergen &#x200B;](/help/creative/assets/hide-show-creatives.png " in het hogere recht van de juiste ruit.")

## [!UICONTROL Targeting] -sectie

**[!UICONTROL Targeting]:** (Read-only voor bestaande ervaringen) niet van toepassing wanneer u het richten niet toelaat gebruikend een besluitvormingsboom; houd deze optie onbruikbaar. **Nota:** Zodra u sparen een ervaring zonder het richten, kunt u niet het richten later toevoegen.

**[!UICONTROL Language Targeting]:** (Ervaring met alleen standaardadvertenties; optioneel; alleen-lezen voor bestaande ervaringen) Controleert de taalinstellingen van de browser van de gebruiker en geeft een creatief item weer in de opgegeven taal wanneer een creatief item in die taal beschikbaar is. Wanneer een creatief element in de door de browser opgegeven taal niet beschikbaar is, wordt in plaats daarvan de instelling [!UICONTROL Preferred language] gebruikt. Nadat u de ervaring hebt opgeslagen, kunt u deze instelling niet meer wijzigen.

**[!UICONTROL Preferred language]:** (Ervaring met alleen standaardadvertenties; alleen-lezen voor bestaande ervaringen) De taal voor alle advertenties die uit de ervaring zijn gemaakt, behalve wanneer [!UICONTROL Language Targeting] is ingeschakeld. Nadat u de ervaring hebt opgeslagen, kunt u deze instelling niet meer wijzigen.

## [!UICONTROL Advanced] -sectie

**Pas van Gegevens:** (Ervaringen met dynamische slechts advertenties; facultatief) om gebruikers te richten die op specifieke zeer belangrijke paren worden gebaseerd die DSP, de uitgever, of de partner in echt - tijd op indruk (zoals SKU=01234567890123 of Cart=empty) overgaat. U kunt tot vijf sleutels van de gegevenspas (parameters) specificeren.<!-- May move this to just within the decision tree. -->

Wanneer u een advertentietag voor een specifieke creatieve grootte creeert, wordt elke sleutel die op dit gebied wordt gespecificeerd toegevoegd als macro in de markering. Voer de waarde in voor elk sleutelwaardepaar in de tag voordat u de tag als advertentie in de DSP implementeert.

**Straal:** (Ervaringen met dynamische slechts advertenties; facultatief) een straal van een Verenigde Staten ZIP code die in het voederdossier aan doel wordt gespecificeerd; selecteer een straal van 0 mijl tot 200 mijl. Het voederdossier dat wordt gebruikt om de dynamische advertenties voor de ervaring tot stand te brengen moet een [!UICONTROL ZIP] kolom <!-- or a user-named column mapped to a ZIP column --> met een waarde voor elke productrij in het dossier omvatten. Bijvoorbeeld, voor een straal van 10 mijl, kan een advertentie voor een product beschikbaar in 95110 aan gebruikers binnen 10 mijl van 95110 worden getoond (die door het IP adres van de gebruiker wordt bepaald).

**pixel van RT:** (Ervaringen met dynamische slechts advertenties; facultatief) A [!UICONTROL Creative] die pixel opnieuw richt aan potentieel doel. Wanneer u het richten binnen de beslissingsboom plaatst, kunt u één niveau van de knopen van het pixeldoel van RT omvatten. Voor elke knoop, zult u de pixel aan doel en de waarden voor de attributen van de pixel specificeren die worden vereist om de creatieven in de toegewezen creatieve bundels te tonen. Als u geen pixel op dit gebied specificeert, kunt u nog binnen de beslissingsboom specificeren.<!-- From R: "the RT Pixel should be via the content selection in the Dynamic ad setup." Clarify. I do see "Datapass" (oneword) in the dynamic ad settings, but I'm not sure how that setting and this experience-level one work together. -->

**[!UICONTROL Label]:**<!-- should be "Labels" --> (Optioneel) Alle [!DNL Creative] -specifieke labels die u op de ervaring wilt toepassen. U kunt ervaringen filteren op label in de weergave Ervaringen en de [!UICONTROL Experience Label] -dimensie opnemen in de [!UICONTROL Custom Creative Report] .

* Om bestaande etiketten te selecteren, klik ![&#x200B; neer &#x200B;](/help/creative/assets/chevron-down.png " "), en selecteer de controledoos naast elk etiket om toe te passen.

* Als u naar bestaande labels wilt zoeken, voert u een tekenreeks in de labelnaam in.

* Om een nieuw etiket tot stand te brengen om toe te passen, open de lijst, **+ voegt Etiket** toe, gaat een nieuwe etiketnaam op het [!UICONTROL Label] gebied in, en klikt dan **creeert**.

* Als u een label wilt verwijderen, schakelt u het selectievakje naast de labelnaam uit.

**[!UICONTROL Impression Tracking URL]:** (Optioneel) Een URL voor het bijhouden van de indruk door derden die u aan de URL van de bestemmingspagina wilt toevoegen voor een advertentie die u uit de ervaring hebt gemaakt. U kunt maximaal vijf URL&#39;s opnemen. Om extra URL toe te voegen, klik ![&#x200B; pictogram ** &#x200B;](/help/creative/assets/create.png) en ga URL in.[!UICONTROL Add More]

Zodra u URL ingaat, zijn alle [&#x200B; beschikbare macro&#39;s &#x200B;](/help/creative/creative-macros.md) en de gegevens waarmee zij worden vervangen vermeld verder onderaan de pagina. Om één van de macro&#39;s in URL op te nemen, houd de curseur over de macrobeschrijving en klik ![&#x200B; Exemplaar aan klembord &#x200B;](/help/creative/assets/copy-to-clipboard.png " Exemplaar aan klembord "), en kleef dan de macro waar u het op het gebied URL wilt.

>[!NOTE]
>
>* In [!DNL Creative] worden automatisch eigen imitatie-trackingtags vooraf toegewezen aan de URL van de bestemmingspagina.
>* U kunt deze URL overschrijven voor elke creatieve functie in de ervaring.
>* U kunt ook JavaScript-code voor imitatie van derden invoeren in het veld [!UICONTROL Client JS]

**[!UICONTROL Click Tracking URL]:** (Optioneel) (Optioneel) Een URL voor het bijhouden van klikken door derden die wordt toegevoegd aan de URL van de bestemmingspagina. U kunt maximaal vijf URL&#39;s opnemen. Om extra URL toe te voegen, klik ![&#x200B; pictogram &#x200B;](/help/creative/assets/create.png) **[!UICONTROL Add More]** en ga URL in.

Zodra u URL ingaat, zijn alle [&#x200B; beschikbare macro&#39;s &#x200B;](/help/creative/creative-macros.md) en de gegevens waarmee zij worden vervangen vermeld verder onderaan de pagina. Om één van de macro&#39;s in URL op te nemen, houd de curseur over de macrobeschrijving en klik ![&#x200B; Exemplaar aan klembord &#x200B;](/help/creative/assets/copy-to-clipboard.png " Exemplaar aan klembord "), en kleef dan de macro waar u het op het gebied URL wilt.

>[!NOTE]
>
>* In [!DNL Creative] worden automatisch eigen imitatie-trackingtags vooraf toegewezen aan de URL van de bestemmingspagina.
>* U kunt dit URL voor om het even welke creatieve <!-- creative bundle for targeted experiences --> in de ervaring met voeten treden.

**[!UICONTROL Client JS]:** (Optioneel) Een van de volgende opties:

* (Wanneer de adverteerder een leverancier van OBA-compatibiliteit voor de advertenties gebruikt) JavaScript-code die verwijst naar de advertentie-overlay waarmee gebruikers kunnen weigeren zich online te richten op gedragingen (OBA).

* Eventuele JavaScript-code voor het bijhouden van de indruk die door derden wordt bijgevoegd bij de landingspagina. **Nota:** U kunt een derde ook ingaan indruk-volgende URL op het [!UICONTROL Impression Tracking URL] gebied.

>[!MORELIKETHIS]
>
>* [&#x200B; creeer een ervaring zonder beslissingsboom richtend &#x200B;](experience-create-no-targeting.md)
>* [&#x200B; geef een ervaring zonder beslissingsboom uit richtend &#x200B;](experience-edit-no-targeting.md)
>* [&#x200B; Beschikbare macro&#39;s voor het volgen URLs &#x200B;](/help/creative/creative-macros.md)
>* [&#x200B; creeer manueel een ad markering voor een toepasselijke creatieve grootte &#x200B;](experience-tag-create-manually.md)
>* [&#x200B; wijs creatieve elementen aan een ad markering voor ervaringen toe zonder zich te richten &#x200B;](experience-tag-assign-creatives.md)
>* [&#x200B; pas het volgen URLs voor een ervaring aan zonder zich &#x200B;](experience-tracking-urls-no-targeting.md) te richten
>* [&#x200B; pas creatieve optimalisering en het plannen voor een ervaring aan zonder zich &#x200B;](experience-optimization-scheduling-no-targeting.md) te richten
