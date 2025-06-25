---
title: Kolommen of gecorrigeerde foutbestanden plaatsen
description: Leer hoe u bladbestanden met opsommingstekens op uw advertentienetwerken kunt plaatsen.
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# Kolommen of gecorrigeerde foutbestanden plaatsen

U kunt bestaande bulksheet- dossiers of gecorrigeerde foutendossiers aan de relevante rekeningen voor [ gesteunde advertentienetwerken ](bulksheet-about.md#bulksheet-functionality-by-network) posten. Als het bestand de ZIP-indeling heeft, hoeft u het niet eerst uit te pakken.

Opsommingenbladbestanden en foutbestanden worden 30 dagen na het uploaden of genereren automatisch verwijderd.

>[!NOTE]
>U kunt ook een bestand met opsommingstekens of een foutbestand plaatsen wanneer u het bestand uploadt.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]** .

1. Schakel het selectievakje in naast elk bestand dat u wilt plaatsen.

1. Klik in de werkbalk boven de gegevenstabel op **[!UICONTROL Post]** .

1. Typ of selecteer in het dialoogvenster informatie in de [[!UICONTROL Post Bulksheet] instellingen ](#bulksheet-post-settings) en klik op **[!UICONTROL Post]** .

   Dezelfde instellingen gelden voor alle bestanden die u plaatst.

Wanneer de taak begint, worden de status en de geplande postdatum voor de rij gewijzigd in de [!UICONTROL Bulksheets] weergave. Wanneer het bestand wordt gepost, wordt een e-mailbericht verzonden met een koppeling naar het bestand. Afhankelijk van de hoeveelheid gecompileerde gegevens kan het e-mailbericht enkele minuten of langer duren. Als een van de gegevens echter niet kan worden gepost, wordt een foutbestand weergegeven in de weergave [!UICONTROL Bulksheets] en wordt een e-mailmelding verzonden met een koppeling naar het foutbestand.

>[!NOTE]
>
>* Het duurt langer om grote hoeveelheden gegevens te verzenden. U kunt de voortgang van het bestand volgen in de kolom [!UICONTROL Progress] in de [!UICONTROL Bulksheets] -weergave.
>* Alle geposte gegevens zijn onderworpen aan het redactionele proces van het netwerk.
>* Voordat het bulksbladbestand wordt gepost, kunt u het posten annuleren.

## Post-instellingen voor bulksbladen en gecorrigeerde foutbestanden {#bulksheet-post-settings}

| Parameter | Beschrijving |
|----|----|
| [!UICONTROL Account (Search Engine)] | De advertentienetwerkrekening waarvoor de gegevens worden gepost. Als u veelvoudige dossiers gelijktijdig of één dossier post dat op veelvoudige rekeningen van toepassing is, is de waarde <i> Geselecteerde Meerdere Rekeningen </i>.<br><br> de eerste brief van de naam van het advertentienetwerk is tussen haakjes na de rekeningsnaam (zoals &quot;Acme Realty (G)&quot;voor een [!DNL Google Ads] rekening). |
| [!UICONTROL Scheduling] | Wanneer post het dossier aan het gespecificeerde ad netwerk:<ul><li><i>[!UICONTROL Post to ad network now]</i> (de standaardwaarde): hiermee worden de gegevens direct gepost.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Begint met het posten van de gegevens op de gespecificeerde datum en de tijd; het gebrek is morgen om 02:00 (2 a.m.). Om de datum te veranderen, ga een datum in het formaat DD/MM/JJJJ of D/M/JJJJ in of klik ![&#128279;](/help/search-social-commerce/assets/calendar.png " Kalender ") om de kalender te openen en [ selecteer een datum ](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md).  Als u de tijd wilt wijzigen, voert u de tijd in de notatie HH/MM of H/M in of selecteert u een tijd (met intervallen van 15 minuten) in de lijst.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Of trackingsjablonen en achtervoegsels van landingspagina&#39;s (voor toepasselijke advertentienetwerken) moeten worden opgenomen in accounts met trackingsjablonen, of doel-URL&#39;s met ingesloten trackingcodes in accounts met doel-URL&#39;s, voor alle trefwoorden, advertenties, plaatsingen, sitelinks en [!DNL Google Ads] -productgroepen in de post: <i>[!UICONTROL Yes]</i> (de standaardinstelling) of <i>[!UICONTROL No]</i> . Het maakt niet uit of de biedingseenheden zich in een portfolio bevinden.<br><br> als u <i>[!UICONTROL Yes]</i> selecteert, dan worden URLs geproduceerd volgens de parameters in de [!UICONTROL Tracking Methods] sectie van de relevante rekeningsmontages of campagnemontages. Als URL&#39;s worden bijgehouden, worden deze standaard alleen opnieuw gegenereerd als er nieuwe URL&#39;s nodig zijn (bijvoorbeeld als het trefwoordovereenkomende type, de advertentietekst of de volgparameters voor de relevante accounts zijn gewijzigd).<br><br> als u <i>[!UICONTROL No]</i> selecteert, dan kunt u het volgen URLs nog produceren later door het geuploade dossier manueel te posten.<br><br><b> Nota:</b> als de adverteerder de omzetting van Adobe Advertising het volgen gebruikt en de basis URL is veranderd, moet u nieuwe het volgen URLs produceren tenzij de rekening wordt gevormd om het volgen URLs automatisch te produceren en te uploaden. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Hiermee worden budgetwijzigingen toegestaan voor campagnes in geoptimaliseerde portfolio&#39;s op basis van gepubliceerde gegevens. Deze optie is standaard niet geselecteerd. Als u deze optie selecteert, zijn eventuele specifieke wijzigingen in het campagnebudget van toepassing totdat de optimalisatiefunctie bepaalt dat het budget opnieuw moet worden toegewezen (meestal bij de volgende biedcyclus).<br><br><b> Nota:</b> Om het even welke begrotingsveranderingen die uit de geposte gegevens voor campagnes in niet-geoptimaliseerde portefeuilles voortvloeien komen voor wanneer het dossier wordt gepost. De wijzigingen worden de volgende dag weergegeven in de weergaven van het campagnebeheer. |
| [!UICONTROL Enable bidding on ads within portfolios] | Wanneer de opgenomen campagnecomponenten in een geoptimaliseerde portefeuille zijn, treedt deze functie de optimaliseringsstrategie met voeten en staat biedingsveranderingen toe die op de gegevens in bulksheet tot een gespecificeerde einddatum worden gebaseerd. Als u deze optie selecteert, geeft u een einddatum tussen 1 en 7 dagen op in het veld **[!UICONTROL Hold bulksheet bids until]** . |

>[!MORELIKETHIS]
>
>* [ Ongeveer het beheren van campagnegegevens gebruikend bulksbladen ](bulksheet-about.md)
>* [ Download/creeer een bulksheet- dossier ](bulksheet-download.md)
>* [ uploadt bulksbladen of gecorrigeerde foutendossiers ](bulksheet-upload.md)
>* [ bevestigt het landen pagina&#39;s in bulksheet dossiers ](bulksheet-validate-landing-pages.md)
>* [ de Uitvoer een geproduceerd of geupload bulksbladdossier ](bulksheet-export.md)
