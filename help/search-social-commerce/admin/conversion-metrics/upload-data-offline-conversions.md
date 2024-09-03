---
title: Offline conversiegegevens uploaden voor verbeterde conversies
description: Leer hoe te om eerste-partij, off-line omzettingsgegevens aan kaart te uploaden  [!DNL Google Ads]  verbeterde omzettingen voor lood.
feature: Conversions
source-git-commit: c3cb1549adeb7b621c1b426c53da9bb09eddcbdc
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Offline conversiegegevens uploaden voor verbeterde conversies

*[!DNL Google Ads]alleen accounts*

<!-- Tweak metadata title/description and heading -->

U kunt uw eerste-partij, off-line omzettingsgegevens - met inbegrip van gehakt e-mailadressen en telefoonaantallen - uploaden om aan uw bestaande [[!DNL Google Ads]  verbeterde omzettingen voor lood ](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) in kaart te brengen. Alle geüploade gegevens worden in realtime gesynchroniseerd met [!DNL Google Ads] .

## Gegevens uploaden voor [!DNL Google Ads] verbeterde conversies voor leads

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]** en klik vervolgens op de tab **[!UICONTROL Upload]** .

1. Selecteer het advertentienetwerk, en dan de rekening.

1. (Facultatief) om een malplaatje met alle [ vereiste gegevensgebieden ](#enhanced-conversions-leads-data) in [!DNL Microsoft Excel] formaat te downloaden, klik **[!UICONTROL View Template]**, en download dan het dossier volgens de normale procedure van uw browser.

   U kunt het bestand bewerken om de gegevens op te nemen en uw wijzigingen op te slaan. Vervolgens uploadt u het bestand in de volgende stap.

1. Klik op **[!UICONTROL Choose File]** en selecteer een bestand dat u wilt uploaden van uw apparaat of netwerk.

## Vereiste gegevens voor geüploade bestanden {#enhanced-conversions-leads-data}

### Gegevens boven de tabel

`Parameters:TimeZone=insert_timezone`

Ga timezone van de rekening of in deze plaats of in &quot;[!UICONTROL Conversion Time]&quot;kolom voor elke rij in. Gebruik of a) het [ gesteunde formaat van identiteitskaart van de tijdzone ](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) of b) de GMT compensatie, zoals die door + of - en het 4-cijfertijdverschil (zoals - 0500 voor New York) wordt vermeld.

### Tabelkolommen en -waarden

| Kolom | Beschrijving |
| ------ | ----------- |
| E-mail | Het e-mailadres van de gebruiker, dat moet worden gehasht gebruikend het algoritme SHA-256. Elke rij moet een e-mailwaarde of een waarde van het Aantal van de Telefoon bevatten. |
| Telefoonnummer | Het telefoonnummer van de gebruiker, dat moet worden hashed gebruikend het algoritme SHA-256. De code moet een landcode bevatten en mag streepjes en andere symbolen bevatten. Elke rij moet een e-mailwaarde of een waarde van het Aantal van de Telefoon bevatten. |
| Conversienaam | (Vereist) De naam van de conversieactie. |
| Conversietijd | (Vereist) de tijd de omzettingsgebeurtenis in a [ gesteunde tijdformaat ](https://support.google.com/google-ads/answer/7014069#prepare_data) voorkwam. Als u niet timezone identiteitskaart van de rekening in `Parameters:TimeZone=insert_timezone` lijn boven de gegevenslijst omvat, dan omvat timezone voor elke rij gebruikend of a) het [ gesteunde formaat van timezone ID ](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) of b) de GMT compensatie, zoals die door + of - en het 4-cijfertijdverschil (zoals - 0500 voor New York) wordt vermeld. |
| Conversiewaarde | (Vereist) De numerieke conversiewaarde. |
| Conversievaluta | De valutacode voor de conversiegebeurtenis. |
| Gebruikersgegevens toevoegen | (Van toepassing op gegevens die betrekking hebben op gebruikers in de Europese Economische Ruimte (EER) of het Verenigd Koninkrijk (VK)) Geeft aan of er toestemming is gegeven voor het verzenden van gebruikersgegevens naar [!DNL Google] voor persoonlijke doeleinden. Waarden kunnen `Granted`, `Denied` of \[null\] (die als `Unspecified` naar [!DNL Google Ads] wordt verzonden) zijn. **Nota:** [!DNL Google Ads] dwingt momenteel geen toestemming voor verbeterde omzettingen voor lood af, maar het kan dit in de toekomst doen. |
| Ad Personalization | (Van toepassing op gegevens die betrekking hebben op gebruikers in de Europese Economische Ruimte (EER) of het Verenigd Koninkrijk (VK)) Geeft aan of er toestemming is gegeven voor het verzenden van gebruikersgegevens naar [!DNL Google] voor reclamedoeleinden. Waarden kunnen `Granted`, `Denied` of \[null\] (die als `Unspecified` naar [!DNL Google Ads] wordt verzonden) zijn. **Nota:** [!DNL Google Ads] dwingt momenteel geen toestemming voor verbeterde omzettingen voor lood af, maar het kan dit in de toekomst doen. |

>[!MORELIKETHIS]
>
>* [ creeer een omzettingsactie voor a  [!DNL Google Ads]  verbeterde omzetting voor lood ](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [ voer  [!DNL Google Ads]  verbeterde omzettingen voor lood ](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md) uit
>* [ uploadt Onderzoek, Sociale, &amp; Commerce-Gecontroleerde omzettingsmetriek aan  [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
