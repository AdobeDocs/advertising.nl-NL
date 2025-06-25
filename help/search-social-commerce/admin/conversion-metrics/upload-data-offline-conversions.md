---
title: Offline conversiegegevens uploaden voor verbeterde conversies
description: Leer hoe te om eerste-partij te uploaden, off-line omzettingsgegevens aan kaart  [!DNL Google Ads]  verbeterde omzettingen voor lood en  [!DNL Microsoft Advertising]  verbeterde omzettingen.
feature: Conversions
exl-id: 5c5dfbb8-3b17-4973-8012-fc7f0e97e33b
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# Offline conversiegegevens uploaden voor verbeterde conversies

*[!DNL Google Ads]en [!DNL Microsoft Advertising] alleen accounts*

U kunt uw eerste-partij, off-line omzettingsgegevens - met inbegrip van gehakt e-mailadressen en telefoonaantallen - uploaden om aan uw bestaande [[!DNL Google Ads]  verbeterde omzettingen voor lood ](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) en [[!DNL Microsoft Advertising]  verbeterde omzettingen ](https://help.ads.microsoft.com/#apex/ads/en/60178) in kaart te brengen. Alle geüploade gegevens worden in realtime gesynchroniseerd met het advertentienetwerk.

## Gegevens uploaden voor verbeterde conversies

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]** en klik vervolgens op de tab **[!UICONTROL Upload]** .

1. Selecteer het advertentienetwerk, en dan de rekening.

1. (Facultatief) om een malplaatje met alle [ vereiste gegevensgebieden ](#enhanced-conversions-leads-data) in [!DNL Microsoft Excel] formaat te downloaden, klik **[!UICONTROL View Template]**, en download dan het dossier volgens de normale procedure van uw browser.

   U kunt het bestand bewerken om de gegevens op te nemen en uw wijzigingen op te slaan. Vervolgens uploadt u het bestand in de volgende stap.

1. Klik op **[!UICONTROL Choose File]** en selecteer een bestand dat u wilt uploaden van uw apparaat of netwerk.

## Vereiste gegevens voor geüploade bestanden {#enhanced-conversions-leads-data}

### Gegevens boven de tabel

`Parameters:TimeZone=insert_timezone`

Ga de tijdzone van de rekening of in deze plaats of in &quot;[!UICONTROL Conversion Time]&quot;kolom voor elke rij in. Gebruik of a \) ([!DNL Google Ads only]) het [ gesteunde formaat van identiteitskaart van de tijdzone ](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) of b\) de GMT compensatie, zoals die door + of - en het 4-cijfertijdverschil (zoals - 0500 voor New York, +0100 voor Berlijn, of +0000 voor Greenwich Gemiddelde Tijd) wordt vermeld.

### Tabelkolommen en -waarden voor [!DNL Google Ads]

| Kolom | Beschrijving |
| ------ | ----------- |
| E-mail | Het e-mailadres van de gebruiker, dat moet worden gehasht gebruikend het algoritme SHA-256. Elke rij moet een e-mailwaarde of een waarde van het Aantal van de Telefoon bevatten. |
| Telefoonnummer | Het telefoonnummer van de gebruiker, dat moet worden hashed gebruikend het algoritme SHA-256. De code moet een landcode bevatten en mag streepjes en andere symbolen bevatten. Elke rij moet een e-mailwaarde of een waarde van het Aantal van de Telefoon bevatten. |
| Conversienaam | (Vereist) De naam van de conversieactie. |
| Conversietijd | (Vereist) de tijd de omzettingsgebeurtenis in a [ gesteunde tijdformaat ](https://support.google.com/google-ads/answer/7014069#prepare_data) voorkwam. Als u geen identiteitskaart van de tijdzone van de rekening in `Parameters:TimeZone=insert_timezone` lijn boven de gegevenslijst omvat, dan omvat de tijdzone voor elke rij gebruikend of a\) het [ gesteunde formaat van identiteitskaart van de tijdzone ](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) of b\) de GMT compensatie, zoals die door + of - en het 4-cijfertijdverschil (zoals - 0500 voor New York, +0100 voor Berlijn, of 0 wordt vermeld 000 voor Greenwich Mean Time). |
| Conversiewaarde | (Vereist) De numerieke conversiewaarde. |
| Conversievaluta | De valutacode voor de conversiegebeurtenis. |
| Gebruikersgegevens toevoegen | (Van toepassing op gegevens die betrekking hebben op gebruikers in de Europese Economische Ruimte (EER) of het Verenigd Koninkrijk (VK)) Geeft aan of er toestemming is gegeven voor het verzenden van gebruikersgegevens naar [!DNL Google] voor persoonlijke doeleinden. Waarden kunnen `Granted`, `Denied` of \[null\] (die als `Unspecified` naar [!DNL Google Ads] wordt verzonden) zijn. **Nota:** [!DNL Google Ads] dwingt momenteel geen toestemming voor verbeterde omzettingen voor lood af, maar het kan dit in de toekomst doen. |
| Ad Personalization | (Van toepassing op gegevens die betrekking hebben op gebruikers in de Europese Economische Ruimte (EER) of het Verenigd Koninkrijk (VK)) Geeft aan of er toestemming is gegeven voor het verzenden van gebruikersgegevens naar [!DNL Google] voor reclamedoeleinden. Waarden kunnen `Granted`, `Denied` of \[null\] (die als `Unspecified` naar [!DNL Google Ads] wordt verzonden) zijn. **Nota:** [!DNL Google Ads] dwingt momenteel geen toestemming voor verbeterde omzettingen voor lood af, maar het kan dit in de toekomst doen. |

### Tabelkolommen en -waarden voor [!DNL Microsoft Advertising]

Voor meer instructies voor het gebruiken van het malplaatje, zie [ https://help.ads.microsoft.com/#apex/3/56852 ](https://help.ads.microsoft.com/#apex/3/56852).

| Kolom | Beschrijving |
| ------ | ----------- |
| Conversienaam | (Vereist) De naam van het omzettingsdoel. |
| Conversietijd | (Vereist) Het tijdstip waarop de conversiegebeurtenis heeft plaatsgevonden. Als u de tijdzone-id van de account niet opneemt in de `Parameters:TimeZone=insert_timezone` -regel boven de datatabel, neemt u de tijdzone voor elke rij op met behulp van de GMT-verschuiving, zoals aangegeven door + of - en het 4-cijferige tijdverschil (zoals -0500 voor New York, +0100 voor Berlijn of +000 voor Greenwich Mean Time). Voor een lijst van tijdstreken voor diverse steden, zie [ https://learn.microsoft.com/en-us/advertising/guides/time-zones ](https://learn.microsoft.com/en-us/advertising/guides/time-zones), maar zorg ervoor dat u het formaat gebruikt hier in plaats van het formaat in de lijst van de tijdzone wordt gespecificeerd. |
| Conversiewaarde | (Vereist) De numerieke conversiewaarde. |
| Conversievaluta | De valutacode voor de conversiegebeurtenis. |
| Microsoft Click ID | De bijbehorende unieke klikidentificatie [!DNL Microsoft] (MSCLKID). Dit veld is mogelijk leeg voor verbeterde offlineconversies. |
| Onderbroken e-mailadres | Het e-mailadres van de gebruiker, dat moet worden gehasht gebruikend het algoritme SHA-256. Voor verbeterde offlineconversies, moet elke rij of een Gehakt waarde van het E-mailadres of een Gehakt waarde van het Aantal van de Telefoon omvatten. |
| Telefoonnummer met hashing | Het telefoonnummer van de gebruiker, dat moet worden hashed gebruikend het algoritme SHA-256. De code moet een landcode bevatten en mag streepjes en andere symbolen bevatten. Voor verbeterde offlineconversies, moet elke rij of een Gehakt waarde van het E-mailadres of een Gehakt waarde van het Aantal van de Telefoon omvatten. |

>[!MORELIKETHIS]
>
>* [ voer  [!DNL Google Ads]  verbeterde omzettingen voor lood ](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md) uit
>* [ voert  [!DNL Microsoft Advertising]  verbeterde off-line omzettingen uit ](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* ([!DNL Google Ads only]) [ creeer een omzettingsactie voor a  [!DNL Google Ads]  verbeterde omzetting voor lood ](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [ uploadt Onderzoek, Sociale, &amp; Commerce-Gecontroleerde omzettingsmetriek aan  [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
