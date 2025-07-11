---
title: Instellingen voor doelgerichte ervaring
description: Zie beschrijvingen van alle montages voor gerichte en ervaringen.
feature: Creative Experiences
exl-id: cb6fd855-6534-4eac-b34b-323073d186be
source-git-commit: 4b780760e5a7a0c3d370054fce8b1c15fbc6802d
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 0%

---

# Instellingen voor doelgericht werken en ervaren

*Gesloten bèta*

## [!UICONTROL Experience basics] -sectie

**[!UICONTROL Ad Type]:** (Alleen-lezen voor bestaande ervaringen) Het type advertenties dat in de ervaring is opgenomen: *[!UICONTROL Standard Display]*, *[!UICONTROL Dynamic Display]* of *[!UICONTROL Video]* . Nadat u de ervaring hebt opgeslagen, kunt u het advertentietype niet meer wijzigen.

**[!UICONTROL Advertiser]:** (Alleen-lezen voor bestaande ervaringen) De adverteerder die een bod uitbrengt op de creatieve en doelcombinaties die in de ervaring zijn opgenomen. Wanneer u de ervaring hebt opgeslagen, kunt u de adverteerder niet meer wijzigen.

**[!UICONTROL Experience Name]:** Een unieke naam voor de ervaring. **Uiteinde:** gebruik een naam die u gemakkelijk kunt vinden wanneer u de ervaring als advertentie in Advertising DSP of andere DSP gebruikt.

**[!UICONTROL Creative Library]:** (Alleen-lezen voor bestaande ervaringen) Eén creatieve bibliotheek die u voor de ervaring kunt gebruiken. Nadat u de ervaring hebt opgeslagen, kunt u de bibliotheek niet meer wijzigen.

## [!UICONTROL Default creatives] -sectie

**\ [gespecificeerde Standaard creatieve creatieven \]:** de standaardcreatieve producten aan gebruik wanneer browser geen creatieve producten kan tonen die aan de ervaring worden toegewezen, zoals wanneer browser niet JavaScript-Toegelaten is of de advertentieserver kan niet de advertentie wegens vertragingen personaliseren. Voor een standaardweergave neemt u één creatieve afbeelding op per advertentiegrootte waarvoor de ervaring van toepassing is. Voor een video-ervaring van standaardkwaliteit neemt u één creatieve video op per advertentiegrootte waarvoor de ervaring geldt. Uw keuzes bepalen de creatieve formaten die voor de ervaring kunnen worden gebruikt.

Voor ervaringen met beslissingsboom die richten, kunt u de standaardcreatieven met creatieve bundels met creatieve bundels met creatieven van de zelfde grootte van binnen de beslissingsboom met voeten treden.<!-- verify -->

* Als u een creatieve standaardafbeelding met verschillende afmetingen wilt toevoegen, klikt u op **[!UICONTROL + Add Sizes]** en schakelt u het selectievakje naast de creatieve elementen in die u vanuit het rechterdeelvenster wilt toevoegen. Klik vervolgens op **[!UICONTROL Add Creatives]** .

* Om gebrek creatief te schrappen, de curseur over de creatieve duimnagel te houden en ![ Schrapping ](/help/creative/assets/delete.png " te klikken schrapt ").

* Om alle standaardcreatieven te schrappen, klik ![ Schrapping ](/help/creative/assets/delete.png " ") **[!UICONTROL Delete all]**.

* Om de ruit van Creatieven op het recht te tonen of te verbergen, klik ![ tonen/verbergen ](/help/creative/assets/hide-show-creatives.png " in het hogere recht van de juiste ruit.")

## [!UICONTROL Targeting] -sectie

**[!UICONTROL Targeting]:** (Alleen-lezen voor bestaande ervaringen) maakt het mogelijk om creatief te zoeken op basis van een beslissingsstructuur en het automatisch maken van tags. Nadat u de ervaring hebt opgeslagen, kunt u deze instelling niet meer wijzigen.

**[!UICONTROL Language Targeting]:** (Ervaring met alleen standaardadvertenties; optioneel; alleen-lezen voor bestaande ervaringen) Controleert de taalinstellingen van de browser van de gebruiker en geeft een creatief item weer in de opgegeven taal wanneer een creatief item in die taal beschikbaar is. Wanneer een creatief element in de door de browser opgegeven taal niet beschikbaar is, wordt in plaats daarvan de instelling [!UICONTROL Preferred language] gebruikt.

Nadat u de ervaring hebt opgeslagen, kunt u deze instelling niet meer wijzigen.

**[!UICONTROL Preferred language]:** (Ervaring met alleen standaardadvertenties; alleen-lezen voor bestaande ervaringen) De taal voor alle advertenties die uit de ervaring zijn gemaakt, behalve wanneer [!UICONTROL Language Targeting] is ingeschakeld. Nadat u de ervaring hebt opgeslagen, kunt u deze instelling niet meer wijzigen.

## [!UICONTROL Advanced] -sectie

**Pas van Gegevens:** (Read-only voor bestaande ervaringen; facultatief) om gebruikers te richten die op specifieke zeer belangrijke paren worden gebaseerd die DSP, de uitgever, of de partner in echt - tijd op indruk (zoals SKU=01234567890123 of Cart=empty) overgaat. U kunt maximaal vijf standaardsleutels van de gegevenspas (parameters) specificeren. Wanneer u opstelling richtend binnen de beslissingsboom, kunt u één niveau van gegevens omvatten gaat doelknopen over, naar keuze de sleutels aan, en specificeert de waarden aan doel voor elke knoop. Als u geen sleutels op dit gebied specificeert wanneer u de ervaring creeert, kunt u hen nog specificeren binnen de beslissingsboom.

Elke toets wordt toegevoegd als een macro in de tag advertentie, die u kunt genereren om te implementeren als een advertentie in uw DSP.

**Straal:** (Ervaringen met dynamische slechts advertenties; facultatief) een straal van een Verenigde Staten ZIP code die in het voederdossier aan doel wordt gespecificeerd; selecteer een straal van 0 mijl tot 200 mijl. Het voederdossier dat wordt gebruikt om de dynamische advertenties voor de ervaring tot stand te brengen moet een [!UICONTROL ZIP] kolom <!-- or a user-named column mapped to a ZIP column --> met een waarde voor elke productrij in het dossier omvatten. Bijvoorbeeld, voor een straal van 10 mijl, kan een advertentie voor een product beschikbaar in 95110 aan gebruikers binnen 10 mijl van 95110 worden getoond (die door het IP adres van de gebruiker wordt bepaald).

**pixel van RT:** (read-only voor bestaande ervaringen; facultatief) A [!UICONTROL Creative] die pixel aan potentieel doel opnieuw richt. Wanneer u het richten binnen de beslissingsboom plaatst, kunt u één niveau van de knopen van het pixeldoel van RT omvatten. Voor elke knoop, zult u de pixel aan doel en de waarden voor de attributen van de pixel specificeren die worden vereist om de creatieven in de toegewezen creatieve bundels te tonen. Als u geen pixel op dit gebied specificeert wanneer u de ervaring creeert, kunt u nog binnen de beslissingsboom specificeren.<!-- May move this to just within the decision tree. -->

**Etiket:**<!-- should be "Labels" --> (Facultatief) om het even welke [!DNL Creative] - specifieke etiketten om op de ervaring van toepassing te zijn. U kunt ervaringen filteren op label in de weergave Ervaringen en de [!UICONTROL Experience Label] -dimensie opnemen in de [!UICONTROL Custom Creative Report] .

* Om bestaande etiketten te selecteren, klik ![ neer ](/help/creative/assets/chevron-down.png " "), en selecteer de controledoos naast elk etiket om toe te passen.

* Als u naar bestaande labels wilt zoeken, voert u een tekenreeks in de labelnaam in.

* Om een nieuw etiket tot stand te brengen om toe te passen, open de lijst, **+ voegt Etiket** toe, gaat een nieuwe etiketnaam op het [!UICONTROL Label] gebied in, en klikt dan **creeert**.

* Als u een label wilt verwijderen, schakelt u het selectievakje naast de labelnaam uit.

**het Volgen URL van de Indrukking:** (Facultatief) een derde indruk-volgende URL om aan de het landen pagina URL voor om het even welke die advertentie van de ervaring wordt gecreeerd toe te voegen. U kunt maximaal vijf URL&#39;s opnemen. Om extra URL toe te voegen, klik ![ pictogram ** ](/help/creative/assets/create.png) en ga URL in.[!UICONTROL Add More]

Zodra u URL ingaat, zijn alle [ beschikbare macro&#39;s ](/help/creative/creative-macros.md) en de gegevens waarmee zij worden vervangen vermeld verder onderaan de pagina. Om één van de macro&#39;s in URL op te nemen, houd de curseur over de macrobeschrijving en klik ![ Exemplaar aan klembord ](/help/creative/assets/copy-to-clipboard.png " Exemplaar aan klembord "), en kleef dan de macro waar u het op het gebied URL wilt.

>[!NOTE]
>
>* In [!DNL Creative] worden automatisch eigen imitatie-trackingtags vooraf toegewezen aan de URL van de bestemmingspagina.
>* U kunt [ dit URL voor om het even welk creatief in de ervaring ](experience-tracking-urls-targeting.md) met voeten treden.
>* U kunt ook JavaScript-code voor imitatie van derden invoeren in het veld [!UICONTROL Client JS]

**klik het Volgen URL:** (Facultatief) (Facultatief) een derde klik-volgende URL om aan de het landen pagina URL toe te voegen. U kunt maximaal vijf URL&#39;s opnemen. Om extra URL toe te voegen, klik ![ pictogram ** ](/help/creative/assets/create.png) en ga URL in.[!UICONTROL Add More]

Zodra u URL ingaat, zijn alle [ beschikbare macro&#39;s ](/help/creative/creative-macros.md) en de gegevens waarmee zij worden vervangen vermeld verder onderaan de pagina. Om één van de macro&#39;s in URL op te nemen, houd de curseur over de macrobeschrijving en klik ![ Exemplaar aan klembord ](/help/creative/assets/copy-to-clipboard.png " Exemplaar aan klembord "), en kleef dan de macro waar u het op het gebied URL wilt.

>[!NOTE]
>
>* In [!DNL Creative] worden automatisch eigen imitatie-trackingtags vooraf toegewezen aan de URL van de bestemmingspagina.
>* U kunt [ dit URL voor om het even welk creatief in de ervaring ](experience-tracking-urls-targeting.md) met voeten treden.

**Cliënt JS:** (Facultatief) om het even welke volgend:

* (Wanneer de adverteerder een leverancier van OBA-compatibiliteit voor de advertenties gebruikt) JavaScript-code die verwijst naar de advertentie-overlay waarmee gebruikers kunnen weigeren zich online te richten op gedragingen (OBA).

* Eventuele JavaScript-code voor het bijhouden van de indruk die door derden wordt bijgevoegd bij de landingspagina. **Nota:** U kunt een derde ook ingaan indruk-volgende URL op het [!UICONTROL Impression Tracking URL] gebied.

>[!MORELIKETHIS]
>
>* [ creeer een ervaring met beslissingsboom richtend ](experience-create-targeting.md)
>* [ geef een ervaring met beslissingsboom uit richtend ](experience-edit-targeting.md)
>* [ Beschikbare macro&#39;s voor het volgen URLs ](/help/creative/creative-macros.md)
