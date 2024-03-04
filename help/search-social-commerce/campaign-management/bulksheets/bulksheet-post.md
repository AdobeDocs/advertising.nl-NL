---
title: Kolommen of gecorrigeerde foutbestanden plaatsen
description: Leer hoe u bladbestanden met opsommingstekens op uw advertentienetwerken kunt plaatsen.
exl-id: 49b930ba-71b3-442d-a162-67cf7ae14e14
feature: Search Bulksheets
source-git-commit: 6b3c876f17d0e30dcce69048bb4041fc8cd29902
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# Kolommen of gecorrigeerde foutbestanden plaatsen

U kunt bestaande bulkbladbestanden of gecorrigeerde foutbestanden op de desbetreffende accounts plaatsen voor [ondersteunde advertentienetwerken](bulksheet-about.md#bulksheet-functionality-by-network). Als het bestand de ZIP-indeling heeft, hoeft u het niet eerst uit te pakken.

Opsommingenbladbestanden en foutbestanden worden 30 dagen na het uploaden of genereren automatisch verwijderd.

>[!NOTE]
>U kunt ook een bestand met opsommingstekens of een foutbestand plaatsen wanneer u het bestand uploadt.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Schakel het selectievakje in naast elk bestand dat u wilt plaatsen.

1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Post]**.

1. Typ of selecteer in het dialoogvenster informatie in het dialoogvenster [[!UICONTROL Post Bulksheet] instellingen](#bulksheet-post-settings)en klik vervolgens op **[!UICONTROL Post]**.

   Dezelfde instellingen gelden voor alle bestanden die u plaatst.

Wanneer de taak begint, worden de status en de geplande postdatum voor de rij gewijzigd in de [!UICONTROL Bulksheets] weergeven. Wanneer het bestand wordt gepost, wordt een e-mailbericht verzonden met een koppeling naar het bestand. Afhankelijk van de hoeveelheid gecompileerde gegevens kan het e-mailbericht enkele minuten of langer duren. Als een van de gegevens niet kan worden gepost, echter, dan is een foutendossier vermeld op [!UICONTROL Bulksheets] en er wordt een e-mailmelding verzonden met een koppeling naar het foutbestand.

>[!NOTE]
>
>* Het duurt langer om grote hoeveelheden gegevens te verzenden. U kunt de voortgang van het bestand volgen in het dialoogvenster [!UICONTROL Progress] in de [!UICONTROL Bulksheets] weergeven.
>* Alle geposte gegevens zijn onderworpen aan het redactionele proces van het netwerk.
* Voordat het bulksbladbestand wordt gepost, kunt u het posten annuleren.

## Post-instellingen voor bulksbladen en gecorrigeerde foutbestanden {#bulksheet-post-settings}

| Parameter | Beschrijving |
|----|----|
| [!UICONTROL Account (Search Engine)] | De advertentienetwerkrekening waarvoor de gegevens worden gepost. Als u meerdere bestanden tegelijk plaatst of één bestand dat van toepassing is op meerdere accounts, is de waarde <i>Meerdere accounts geselecteerd</i>.<br><br>De eerste letter van de naam van het advertentienetwerk staat tussen haakjes achter de accountnaam (zoals &quot;Acme Realty (G)&quot; voor een [!DNL Google Ads] account). |
| [!UICONTROL Scheduling] | Wanneer post het dossier aan het gespecificeerde ad netwerk:<ul><li><i>[!UICONTROL Post to ad network now]</i> (de standaardinstelling): hiermee worden de gegevens direct gepost.</li><li><i>[!UICONTROL Post to ad network on \[specified date\] \[specified time\]]:</i> Begint de gegevens op de opgegeven datum en tijd te posten; de standaardwaarde is morgen om 2.00 uur (2.00 uur). Als u de datum wilt wijzigen, voert u een datum in in de notatie DD/MM/JJJJ of D/M/JJJJ of klikt u op ![Kalender](/help/search-social-commerce/assets/calendar.png "Kalender") de kalender te openen en [selecteer een datum](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Als u de tijd wilt wijzigen, voert u de tijd in de notatie HH/MM of H/M in of selecteert u een tijd (met intervallen van 15 minuten) in de lijst.</li></ul> |
| [!UICONTROL Generate Tracking URLs] | Of trackingsjablonen en achtervoegsels van landingspagina&#39;s (voor toepasselijke advertentienetwerken) moeten worden opgenomen in accounts met trackingsjablonen, of doel-URL&#39;s met ingesloten trackingcodes in accounts met doel-URL&#39;s, voor alle trefwoorden, advertenties, plaatsingen, sitelinks en [!DNL Google Ads] productgroepen in de post : <i>[!UICONTROL Yes]</i> (de standaardwaarde) of <i>[!UICONTROL No]</i>. Het maakt niet uit of de biedingseenheden zich in een portfolio bevinden.<br><br>Als u <i>[!UICONTROL Yes]</i>, worden de URL&#39;s gegenereerd volgens de parameters in het dialoogvenster [!UICONTROL Tracking Methods] van de relevante account-instellingen of campagne-instellingen. Als URL&#39;s worden bijgehouden, worden deze standaard alleen opnieuw gegenereerd als er nieuwe URL&#39;s nodig zijn (bijvoorbeeld als het trefwoordovereenkomende type, de advertentietekst of de volgparameters voor de relevante accounts zijn gewijzigd).<br><br>Als u <i>[!UICONTROL No]</i>, kunt u URL&#39;s voor bijhouden nog steeds later genereren door het geüploade bestand handmatig te posten.<br><br><b>Opmerking:</b> Als de adverteerder het bijhouden van Adoben Advertising gebruikt en de basis-URL is gewijzigd, moet u nieuwe URL&#39;s voor bijhouden genereren, tenzij de account is geconfigureerd voor het automatisch genereren en uploaden van URL&#39;s voor bijhouden. |
| [!UICONTROL Enable budget changes on optimized campaigns] | Hiermee worden budgetwijzigingen toegestaan voor campagnes in geoptimaliseerde portfolio&#39;s op basis van gepubliceerde gegevens. Deze optie is standaard niet geselecteerd. Als u deze optie selecteert, zijn eventuele specifieke wijzigingen in het campagnebudget van toepassing totdat de optimalisatiefunctie bepaalt dat het budget opnieuw moet worden toegewezen (meestal bij de volgende biedcyclus).<br><br><b>Opmerking:</b> Eventuele begrotingswijzigingen die voortvloeien uit de geposte gegevens voor campagnes in niet-geoptimaliseerde portfolio&#39;s, treden op wanneer het bestand wordt gepost. De wijzigingen worden de volgende dag weergegeven in de weergaven van het campagnebeheer. |
| [!UICONTROL Enable bidding on ads within portfolios] | Wanneer de opgenomen campagnecomponenten in een geoptimaliseerde portefeuille zijn, treedt deze functie de optimaliseringsstrategie met voeten en staat biedingsveranderingen toe die op de gegevens in bulksheet tot een gespecificeerde einddatum worden gebaseerd. Als u deze optie selecteert, geeft u een einddatum tussen 1 en 7 dagen op in het dialoogvenster **[!UICONTROL Hold bulksheet bids until]** veld. |

>[!MORELIKETHIS]
>
>* [Campagnegegevens beheren met behulp van bulksbladen](bulksheet-about.md)
>* [Een bulkbladbestand downloaden/maken](bulksheet-download.md)
>* [Bulksbladen of gecorrigeerde foutbestanden uploaden](bulksheet-upload.md)
>* [Openingspagina&#39;s in bulkbladbestanden valideren](bulksheet-validate-landing-pages.md)
>* [Een gegenereerd of geüpload bulksbladbestand exporteren](bulksheet-export.md)
