---
title: Upload een bulksheet of een gecorrigeerd foutbestand
description: Leer hoe u handmatig een bulksheet-bestand uploadt of het foutbestand voor de validatie van de landingspagina corrigeert.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Upload een bulksheet of een gecorrigeerd foutbestand

U kunt bulkbladbestanden uploaden, gecorrigeerde foutbestanden voor de validatie van landingspagina&#39;s en andere gecorrigeerde foutbestanden van uw apparaat of netwerk voor [ondersteunde advertentienetwerken](bulksheet-about.md#bulksheet-functionality-by-network). Eventuele aangepaste kolommen in het bestand worden verwijderd wanneer u het bestand uploadt.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Upload Bulksheet]**.

1. Voer gegevens in of selecteer deze in het dialoogvenster [[!UICONTROL Upload Bulksheet] instellingen](#bulksheet-upload-settings).

1. Klik op **[!UICONTROL Apply]**.

Wanneer de taak begint, wordt het bestand weergegeven in het dialoogvenster [!UICONTROL Bulksheets] weergeven. Wanneer het bestand is voltooid, wordt een e-mailbericht verzonden met een koppeling naar het bestand. Afhankelijk van de hoeveelheid gecompileerde gegevens kan het e-mailbericht enkele minuten of langer duren. Als het genereren van het bestand echter mislukt, wordt een foutbestand weergegeven in het dialoogvenster [!UICONTROL Bulksheets] en er wordt een e-mailmelding verzonden met een koppeling naar het foutbestand.

>[!NOTE]
>
>Als u de gegevens van het bulksblad op het advertentienetwerk plaatst, kunt u de vooruitgang van het dossier in volgen [!UICONTROL Progress] in de [!UICONTROL Bulksheets] weergeven. Het duurt langer om grote hoeveelheden gegevens te verzenden.

## Instellingen voor bulksbladen en gecorrigeerde foutbestanden uploaden {#bulksheet-upload-settings}

| Parameter | Beschrijving |
|----|----|
| [!UICONTROL File to Upload] | Het bestand dat moet worden geüpload. Geef het bestand op door het volledige pad en de bestandsnaam in te voeren of door op <b>[!UICONTROL Browse]</b> om het bestand op uw apparaat of netwerk te zoeken.<br><br>Bulksheet-bestanden kunnen maximaal 2,5 GB (ongeveer 2,5 miljoen rijen) bevatten en moeten een van de volgende bestandsextensies hebben: <i>[!UICONTROL .tsv]</i> (voor door tabs gescheiden waarden), <i>[!UICONTROL .txt]</i> (voor ASCII-tekst die compatibel is met Unicode), <i>[!UICONTROL .csv]</i> (voor door komma&#39;s gescheiden waarden), of <i>[!UICONTROL .zip]</i> (voor gecomprimeerde ZIP-indeling, die wordt uitgepakt naar een TSV-bestand). De bestandsnaam mag de volgende tekens niet bevatten: `# % &amp; * | \ : &quot; &lt; &gt; . ? /`<br><br><b>Tip:</b> Gebruik bestanden in de indeling TSV of TXT voor gegevens die internationale tekens bevatten. |
| [!UICONTROL Single Account] | Geeft aan of het bestand op één account van toepassing is: <i>[!UICONTROL Yes]</i> (voor één rekening) of <i>[!UICONTROL No]</i>(voor meerdere accounts). |
| [!UICONTROL Account (Search Engine)] | (Wanneer het bestand van toepassing is op één account) Het account waarnaar de gegevens moeten worden geüpload. |
| [!UICONTROL Search Engine] | (Wanneer het bestand van toepassing is op meerdere accounts) Het advertentienetwerk waarop de gegevens moeten worden geüpload. |
| [!UICONTROL Scheduling] | Wanneer of als het bestand op het opgegeven ad-netwerk moet worden geplaatst:<ul><li><i>[!UICONTROL Post to ad network now]</i> (de standaardinstelling): Begint de gegevens onmiddellijk te posten.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Begint de gegevens op de opgegeven datum en tijd te publiceren; de standaardwaarde is morgen om 2.00 uur (2.00 uur). Als u de datum wilt wijzigen, voert u een datum in in de notatie DD/MM/JJJJ of D/M/JJJJ of klikt u op ![Kalender](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md "Kalender") de kalender te openen en [selecteer een datum](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Als u de tijd wilt wijzigen, voert u de tijd in de notatie HH/MM of H/M in of selecteert u een tijd (met intervallen van 15 minuten) in de lijst.</li><li><i>[!UICONTROL Preview only]:</i> Het bestand uploaden naar Zoeken, Sociale Zaken en Handel zonder de gegevens naar het advertentienetwerk te verzenden. u kunt het bestand nog steeds later plaatsen. Als het bestand met de opsommingstekens groter is dan 10 MB maar kleiner dan 2 GB, heeft het bestand de ZIP-indeling. U hoeft het bestand niet uit te pakken om het te posten.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Of trackingsjablonen en achtervoegsels van landingspagina&#39;s (voor toepasselijke advertentienetwerken) moeten worden opgenomen in accounts met trackingsjablonen, of doel-URL&#39;s met ingesloten trackingcodes in accounts met doel-URL&#39;s, voor alle trefwoorden, advertenties, plaatsingen, sitelinks en [!DNL Google Ads] productgroepen in de post : <i>[!UICONTROL Yes]</i> (de standaardwaarde) of <i>[!UICONTROL No]</i>. Het maakt niet uit of de biedingseenheden zich in een portfolio bevinden.<br><br>Als u <i>[!UICONTROL Yes]</i>, worden de URL&#39;s gegenereerd volgens de parameters in het dialoogvenster [!UICONTROL Tracking Methods] van de relevante account-instellingen of campagne-instellingen. Als URL&#39;s worden bijgehouden, worden deze standaard alleen opnieuw gegenereerd als er nieuwe URL&#39;s nodig zijn (bijvoorbeeld als het trefwoordovereenkomende type, de advertentietekst of de volgparameters voor de relevante accounts zijn gewijzigd).<br><br>Als u <i>[!UICONTROL No]</i>, kunt u URL&#39;s voor bijhouden nog steeds later genereren door het geüploade bestand handmatig te posten.<br><br><b>Opmerking:</b> Als de adverteerder Adobe Advertising tracking gebruikt en de basis-URL is gewijzigd, moet u nieuwe URL&#39;s voor bijhouden genereren, tenzij het account is geconfigureerd voor het automatisch genereren en uploaden van URL&#39;s voor bijhouden. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Hiermee worden budgetwijzigingen toegestaan voor campagnes in geoptimaliseerde portfolio&#39;s op basis van gepubliceerde gegevens. Deze optie is standaard niet geselecteerd. Als u deze optie selecteert, zijn eventuele specifieke wijzigingen in het campagnebudget van toepassing totdat de optimalisatiefunctie bepaalt dat het budget opnieuw moet worden toegewezen (meestal bij de volgende biedcyclus).<br><br><b>Opmerking:</b> Eventuele begrotingswijzigingen die voortvloeien uit de geposte gegevens voor campagnes in niet-geoptimaliseerde portfolio&#39;s, treden op wanneer het bestand wordt gepost. Wijzigingen worden de volgende dag weergegeven in de weergaven van het campagnebeheer. |
| [!UICONTROL Enable bidding on ads within portfolios] | Wanneer de opgenomen campagnecomponenten in een geoptimaliseerde portefeuille zijn, treedt deze functie de optimaliseringsstrategie met voeten en staat biedingsveranderingen toe die op de gegevens in bulksheet tot een gespecificeerde einddatum worden gebaseerd. Als u deze optie selecteert, geeft u een einddatum tussen 1 en 7 dagen op in het dialoogvenster **[!UICONTROL Hold bulksheet bids until]** veld. |

>[!MORELIKETHIS]
>
>* [Campagnegegevens beheren met behulp van bulksbladen](bulksheet-about.md)
>* [Een bulkbladbestand downloaden/maken](bulksheet-download.md)
>* [Kolommen of gecorrigeerde foutbestanden plaatsen](bulksheet-post.md)
>* [Openingspagina&#39;s in bulkbladbestanden valideren](bulksheet-validate-landing-pages.md)
>* [Een gegenereerd of geüpload bulksbladbestand exporteren](bulksheet-export.md)

