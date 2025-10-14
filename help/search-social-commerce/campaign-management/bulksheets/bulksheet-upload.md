---
title: Upload een bulksheet of een gecorrigeerd foutbestand
description: Leer hoe u handmatig een bulksheet-bestand uploadt of het foutbestand voor de validatie van de landingspagina corrigeert.
exl-id: 44c76ca3-1d3e-43c2-868a-4868157d32b0
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---

# Upload een bulksheet of een gecorrigeerd foutbestand

U kunt bulksheet- dossiers, de gecorrigeerde dossiers van de het landende paginabevestiging, en andere gecorrigeerde foutendossiers van uw apparaat of netwerk voor [&#x200B; gesteunde advertentienetwerken &#x200B;](bulksheet-about.md#bulksheet-functionality-by-network) uploaden. Eventuele aangepaste kolommen in het bestand worden verwijderd wanneer u het bestand uploadt.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]** .

1. Klik in de werkbalk boven de gegevenstabel op **[!UICONTROL Upload Bulksheet]** .

1. Typ of selecteer informatie in de [[!UICONTROL Upload Bulksheet] instellingen &#x200B;](#bulksheet-upload-settings) .

1. Klik op **[!UICONTROL Apply]**.

Wanneer de taak begint, wordt het bestand weergegeven in de weergave [!UICONTROL Bulksheets] . Wanneer het bestand is voltooid, wordt een e-mailbericht verzonden met een koppeling naar het bestand. Afhankelijk van de hoeveelheid gecompileerde gegevens kan het e-mailbericht enkele minuten of langer duren. Als het genereren van het bestand echter mislukt, wordt een foutbestand weergegeven in de weergave [!UICONTROL Bulksheets] en wordt een e-mailmelding verzonden met een koppeling naar het foutbestand.

>[!NOTE]
>
>Als u de gegevens van het bulksblad op het advertentienetwerk post, kunt u de vooruitgang van het dossier in de [!UICONTROL Progress] kolom in de [!UICONTROL Bulksheets] mening volgen. Het duurt langer om grote hoeveelheden gegevens te verzenden.

## Instellingen voor bulksbladen en gecorrigeerde foutbestanden uploaden {#bulksheet-upload-settings}

| Parameter | Beschrijving |
|----|----|
| [!UICONTROL File to Upload] | Het bestand dat moet worden geüpload. Geef het bestand op door het volledige pad en de bestandsnaam in te voeren of door op <b>[!UICONTROL Browse]</b> te klikken om het bestand op uw apparaat of netwerk te zoeken.<br><br> de dossiers van het Blad kunnen tot 2.5 GB (ongeveer 2.5 miljoen rijen) zijn en moeten één van de volgende dossieruitbreidingen hebben: <i>[!UICONTROL .tsv]</i> (voor lusje-gescheiden waarden), <i>[!UICONTROL .txt]</i> (voor Unicode-Volgzame tekst ASCII), <i>[!UICONTROL .csv]</i> (voor komma-gescheiden waarden), of <i>[!UICONTROL .zip]</i> (voor samengeperste formaat van ZIP, dat aan een TSV- dossier) uitpakt. De dossier - naam kan niet de volgende karakters omvatten: `# % &amp; * | \ : &quot; &lt; &gt; . ? /`<br><br><b> Uiteinde:</b> voor gegevens die internationale karakters omvatten, gebruikdossiers in formaat TSV of TXT. |
| [!UICONTROL Single Account] | Geeft aan of het bestand van toepassing is op één account: <i>[!UICONTROL Yes]</i> (voor één account) of <i>[!UICONTROL No]</i> (voor meerdere accounts). |
| [!UICONTROL Account (Search Engine)] | (Wanneer het bestand van toepassing is op één account) Het account waarnaar de gegevens moeten worden geüpload. |
| [!UICONTROL Search Engine] | (Wanneer het bestand van toepassing is op meerdere accounts) Het advertentienetwerk waarop de gegevens moeten worden geüpload. |
| [!UICONTROL Scheduling] | Wanneer of als het bestand op het opgegeven ad-netwerk moet worden geplaatst:<ul><li><i>[!UICONTROL Post to ad network now]</i> (de standaardwaarde): hiermee worden de gegevens direct gepost.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Begint met het posten van de gegevens op de gespecificeerde datum en de tijd; het gebrek is morgen om 02:00 (2 a.m.). Om de datum te veranderen, ga een datum in het formaat DD/MM/JJJJ of D/M/JJJJ in of klik ![&#128279;](/help/search-social-commerce/assets/calendar.png " Kalender ") om de kalender te openen en [&#x200B; selecteer een datum &#x200B;](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md).  Als u de tijd wilt wijzigen, voert u de tijd in de notatie HH/MM of H/M in of selecteert u een tijd (met intervallen van 15 minuten) in de lijst.</li><li><i>[!UICONTROL Preview only]:</i> als u het bestand wilt uploaden naar Zoeken, Sociaal en Commerce zonder de gegevens naar het advertentienetwerk te posten, kunt u het bestand later nog steeds plaatsen. Wanneer het bulksbladbestand groter is dan 10 MB maar kleiner dan 2 GB, heeft het bestand de ZIP-indeling. U hoeft het bestand niet uit te pakken om het te posten.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Of trackingsjablonen en achtervoegsels van landingspagina&#39;s (voor toepasselijke advertentienetwerken) moeten worden opgenomen in accounts met trackingsjablonen, of doel-URL&#39;s met ingesloten trackingcodes in accounts met doel-URL&#39;s, voor alle trefwoorden, advertenties, plaatsingen, sitelinks en [!DNL Google Ads] -productgroepen in de post: <i>[!UICONTROL Yes]</i> (de standaardinstelling) of <i>[!UICONTROL No]</i> . Het maakt niet uit of de biedingseenheden zich in een portfolio bevinden.<br><br> als u <i>[!UICONTROL Yes]</i> selecteert, dan worden URLs geproduceerd volgens de parameters in de [!UICONTROL Tracking Methods] sectie van de relevante rekeningsmontages of campagnemontages. Als URL&#39;s worden bijgehouden, worden deze standaard alleen opnieuw gegenereerd als er nieuwe URL&#39;s nodig zijn (bijvoorbeeld als het trefwoordovereenkomende type, de advertentietekst of de volgparameters voor de relevante accounts zijn gewijzigd).<br><br> als u <i>[!UICONTROL No]</i> selecteert, dan kunt u het volgen URLs nog produceren later door het geuploade dossier manueel te posten.<br><br><b> Nota:</b> als de adverteerder de omzetting van Adobe Advertising het volgen gebruikt en de basis URL is veranderd, moet u nieuwe het volgen URLs produceren tenzij de rekening wordt gevormd om het volgen URLs automatisch te produceren en te uploaden. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Hiermee worden budgetwijzigingen toegestaan voor campagnes in geoptimaliseerde portfolio&#39;s op basis van gepubliceerde gegevens. Deze optie is standaard niet geselecteerd. Als u deze optie selecteert, zijn eventuele specifieke wijzigingen in het campagnebudget van toepassing totdat de optimalisatiefunctie bepaalt dat het budget opnieuw moet worden toegewezen (meestal bij de volgende biedcyclus).<br><br><b> Nota:</b> Om het even welke begrotingsveranderingen die uit de geposte gegevens voor campagnes in niet-geoptimaliseerde portefeuilles voortvloeien komen voor wanneer het dossier wordt gepost. De wijzigingen worden de volgende dag weergegeven in de weergaven van het campagnebeheer. |
| [!UICONTROL Enable bidding on ads within portfolios] | Wanneer de opgenomen campagnecomponenten in een geoptimaliseerde portefeuille zijn, treedt deze functie de optimaliseringsstrategie met voeten en staat biedingsveranderingen toe die op de gegevens in bulksheet tot een gespecificeerde einddatum worden gebaseerd. Als u deze optie selecteert, geeft u een einddatum tussen 1 en 7 dagen op in het veld **[!UICONTROL Hold bulksheet bids until]** . |

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer het beheren van campagnegegevens gebruikend bulksbladen &#x200B;](bulksheet-about.md)
>* [&#x200B; Download/creeer een bulksheet- dossier &#x200B;](bulksheet-download.md)
>* [&#x200B; Post bulksbladen of gecorrigeerde foutendossiers &#x200B;](bulksheet-post.md)
>* [&#x200B; bevestigt het landen pagina&#39;s in bulksheet dossiers &#x200B;](bulksheet-validate-landing-pages.md)
>* [&#x200B; de Uitvoer een geproduceerd of geupload bulksbladdossier &#x200B;](bulksheet-export.md)
