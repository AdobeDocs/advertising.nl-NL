---
title: Een bulkbladbestand downloaden/maken
description: Leer hoe u bulksheet-bestanden kunt maken door accountgegevens voor uw advertentienetwerken te downloaden.
source-git-commit: 313e63fdbe3f9c0853dfef0ed29148d5119e482c
workflow-type: tm+mt
source-wordcount: '1756'
ht-degree: 0%

---

# Een bulkbladbestand downloaden/maken

U kunt bulksbladen maken met behulp van aangepaste instellingen voor een of meer accounts op een of meer [ondersteunde advertentienetwerken](bulksheet-about.md#bulksheet-functionality-by-network). De bulksbladen omvatten gegevens binnen Onderzoek, Sociale, &amp; Handel.

Voor gesynchroniseerde campagnes kunt u optioneel synchroniseren met het advertentienetwerk voordat u de gegevens downloadt om ervoor te zorgen dat recente gegevenswijzigingen aan de zijde van het advertentienetwerk worden opgenomen. Voor alle advertentienetwerken, kunt u naar keuze nieuwe klik-volgende URLs produceren om in het dossier te omvatten.

>[!NOTE]
>
>U kunt ook [een bulksbladbestand maken op basis van de zichtbare kolommen in een campagnebeheerweergave](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md).

1. Klik in het hoofdmenu op **[!UICONTROL Search]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**.

1. Klik op de werkbalk op **[!UICONTROL Download Bulksheet]**.

1. Geef de [instellingen voor bulkpagina](#bulksheet-download-settings):

1. Op de **[!UICONTROL Selections]** op, voert u gegevens in de velden in of selecteert u deze.

1. (Optioneel) Klik op de knop **[!UICONTROL Rows and Columns]** geeft u de accountcomponenten en de componentstatus op waarvoor u rijen in het bulksblad wilt opnemen en geeft u vervolgens de kolommen op die u voor elke geselecteerde component wilt opnemen.

   Zie &quot;[Opsommingstekstrijen per ad-netwerk](#bulksheet-rows-by-ad-network).&quot;

1. (Optioneel) Klik op de knop **[!UICONTROL Filters]** en geeft vervolgens criteria op voor specifieke campagnes, en groepen, advertenties/creatieve personen, trefwoorden, plaatsingen en andere entiteiten die in het bulksblad moeten worden opgenomen:

   1. Selecteer een parameter (naam van entiteit of ID; of een element van een advertentie, trefwoord of plaatsing), selecteert u een operator en voert u vervolgens de toepasselijke waarde in. Als u bijvoorbeeld alleen advertenties met &quot;schoenen&quot; in de kop wilt retourneren voor een [!DNL Google Ads] account, selecteren *Titel*, selecteert u *[!UICONTROL contains]* en vervolgens voert u `shoes` in het invoerveld.

   1. (Als u aanvullende filters wilt toepassen) Klik voor elk extra filter op **[!UICONTROL +Add Filter]**, selecteert u **[!UICONTROL AND]** of **[!UICONTROL OR]** selecteert u een advertentie-element of trefwoord en een operator en voert u vervolgens de toepasselijke waarde in.

1. Klik op **[!UICONTROL Download]**.

Wanneer de taak begint, toont het venster een bericht maar open blijft zodat kunt u extra bulksbladen blijven tot stand brengen als u wilt. Alle opgegeven filters en uitsluitingen die van toepassing zijn op nieuwe accounts die u selecteert, blijven behouden. Wanneer de taak begint, wordt het bestand weergegeven in de weergave Opsommingstekens. Wanneer het bestand is gemaakt, ontvangt u een e-mailmelding met een koppeling naar het bestand. afhankelijk van de hoeveelheid gegevens die wordt verzameld, kan de kennisgeving enkele minuten of langer duren. Als het genereren van het bestand echter mislukt, wordt een foutbestand weergegeven in de weergave Opsommingstekens en ontvangt u een e-mailmelding met een koppeling naar het foutbestand.

## Downloadinstellingen voor werkbladen {#bulksheet-download-settings}

| Tab | Parameter | Beschrijving |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | De accounts, campagnes of advertentiegroepen waarnaar de gegevens moeten worden geüpload:<ul><li>Als u een account en alle bijbehorende campagnes en advertentiegroepen wilt selecteren, schakelt u het selectievakje naast de naam van de account in en klikt u op >> om de account naar de [!UICONTROL Selected Filters] kolom.</li><li>Als u afzonderlijke campagnes of advertentiegroepen wilt selecteren, klikt u naast de account om deze uit te vouwen. Klik (indien nodig) naast de campagne of de groep om de campagne uit te vouwen, selecteer het selectievakje naast de naam van de campagne of de advertentiegroep en klik vervolgens op >> om deze naar de [!UICONTROL Selected Filters] kolom. Als u bijvoorbeeld alleen gegevens wilt ophalen voor Campagne 1 in Account 1, vouwt u Account 1 uit, schakelt u het selectievakje naast Campagne 1 in en verplaatst u het vervolgens naar de [!UICONTROL Selected Filters] kolom.</li></ul><b>Opmerkingen:</b><ul><li>Eén enkel bulksblad kan van toepassing zijn op meerdere accounts in meerdere advertentienetwerken. De netwerk-specifieke kolommen van de extra zijn geëtiketteerd in bulksbladen met de naam van het advertentienetwerk (zoals &quot;Mobiele Dragers (de Advertentie van Google)&quot;).</li><li>Als u wilt zien welk type component een item is, houdt u de cursor erop.</li><li>Voor campagnes, is de eerste brief van de naam van het advertentienetwerk tussen haakjes na de rekeningsnaam (zoals &quot;Acme Realty (G)&quot;voor a [!DNL Google Ads] account).</li><li>Standaard worden alleen actieve en ingeschakelde accounts en hun actieve componenten weergegeven. Als u gepauzeerde en verwijderde componenten wilt weergeven, klikt u op ![Pijl-omlaag](/help/search-social-commerce/assets/arrow-down-expand.png "Pijl-omlaag") naast [!UICONTROL Show] en selecteer **[!UICONTROL All]. |
| | [!UICONTROL Generate Tracking URLs] | (Optioneel) Bevat volgsjablonen en achtervoegsels van landingspagina&#39;s (voor toepasselijke advertentienetwerken) in accounts met trackingsjablonen, of doel-URL&#39;s met ingesloten trackingcodes in accounts met doel-URL&#39;s, voor trefwoorden, advertenties, plaatsingen, sitelinks en [!DNL Google Ads] productgroepen in het bulksblad. Deze optie is standaard geselecteerd.<br><br>Wanneer deze optie is geselecteerd, worden de URL&#39;s gegenereerd volgens de parameters in het dialoogvenster [!UICONTROL Campaign Tracking] van de instellingen van de account of de campagne. Als er al URL&#39;s worden bijgehouden, worden deze standaard niet opnieuw gegenereerd, tenzij er nieuwe URL&#39;s nodig zijn (bijvoorbeeld als het trefwoordtype, de advertentietekst of de trackingparameters van de account zijn gewijzigd).<br><br><b>Opmerkingen:</b><ul><li>Als de adverteerder het volgen van de omzetting van de Adobe Advertising gebruikt en de relevante rekening niet wordt gevormd om het volgen URLs automatisch te produceren en te uploaden, dan moet u nieuwe het volgen URLs produceren wanneer de basis URLs is veranderd.</li><li>Als u deze optie niet selecteert, kunt u later nog URL&#39;s voor bijhouden genereren wanneer u het bestand uploadt of post.</li></ul> |
| | [!UICONTROL Perform Pre-sync] | (Optioneel) Hiermee wordt Zoekopdrachten, sociale zaken en handel geïnstrueerd zijn bestanden te synchroniseren met de opgegeven campagnes om ervoor te zorgen dat alle gegevens gelijk zijn. Deze optie is standaard niet geselecteerd.<br><b>Opmerking:</b> Het onderzoek, Sociale, &amp; Handel synchroniseert automatisch met het advertentienetwerk eens per dag, wanneer het een nieuwe campagne op het advertentienetwerk ontdekt, en telkens als u campagnegegevens van binnen Onderzoek, Sociale, &amp; Handel verandert. Selecteer deze optie als u denkt dat recente wijzigingen in campagne- of accountgegevens rechtstreeks zijn aangebracht in het advertentienetwerk of met de bureaubladeditor van het advertentienetwerk. Het maken van werkbladen duurt langer als u deze optie selecteert. |
| | [!UICONTROL Bulksheet Name] | De naam van het nieuwe bulksblad en het bestandstype. Standaard wordt het bestand gemaakt in een indeling met tabgescheiden waarden en krijgt het de volgende naam:<ul><li>(voor alle rekeningen voor het advertentienetwerk) `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(voor enkelvoudige rekeningen) `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(voor meerdere accounts) `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`.</li></ul>U kunt de naam van het bestand wijzigen. De naam mag de volgende tekens niet bevatten: `# % &amp; * | \ : &quot; &lt; &gt; . ? or /`.<br><br>Wijzig desgewenst het bestandstype. De opties omvatten *[!UICONTROL .tsv]* (voor door tabs gescheiden waarden), *[!UICONTROL .txt]* (voor ASCII-tekst die compatibel is met Unicode), *[!UICONTROL .csv]* (voor door komma&#39;s gescheiden waarden), of *[!UICONTROL .zip]* (voor gecomprimeerde ZIP-indeling, die wordt uitgepakt naar een TSV-bestand).<br><br><b>Tip:</b> Voor bulksbladen die internationale karakters omvatten, gebruik TSV of formaat TXT. |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | De entiteiten, en hun overeenkomstige status, om in het bulksblad op te nemen, met één gegevensrij per ingang. Als u bijvoorbeeld actieve campagnes opneemt, bevat het bulksblad één rij per actieve campagne. Alleen geselecteerde entiteiten met de geselecteerde status worden opgenomen. De standaardwaarden worden vooraf geselecteerd op basis van het opgegeven advertentienetwerk. Standaard worden alleen actieve instanties van de geselecteerde entiteiten opgenomen. Zie &quot;[Opsommingstekstrijen per ad-netwerk](#bulksheet-rows-by-ad-network).&quot;<br><br>Als u entiteiten wilt toevoegen of verwijderen, schakelt u respectievelijk de selectievakjes naast de entiteiten in of uit. Als u statussen voor een entiteit wilt toevoegen of verwijderen, klikt u naast het statusmenu en schakelt u respectievelijk de selectievakjes naast de entiteiten in of uit. |
| | [!UICONTROL Cascading Status Hierarchy] | Filtert het werkingsgebied van kindentiteiten aan die met de gespecificeerde ouderentiteitstatus, gebruikend EN. Bijvoorbeeld, als u &quot;Actieve Campagne,&quot;Actieve Adgroup,&quot;en &quot;Actief Sleutelwoord selecteert,&quot;dan omvat bulksheet slechts actieve sleutelwoorden in actieve en groepen in actieve campagnes.<br><br>Als u deze optie niet selecteert, dan wordt de ouderstatus niet overwogen, en de filter gebruikt OF verrichting. Bijvoorbeeld, als u &quot;Actieve Campagne,&quot;Actieve Adgroup,&quot;en &quot;Actief Sleutelwoord selecteert,&quot;dan omvat bulksheet alle actieve campagnes; alle actieve ad-hocgroepen, ongeacht de status van de bovenliggende campagne; en alle actieve trefwoorden, ongeacht de status van de bovenliggende campagne en de advertentiegroep. |
| | [!UICONTROL Bulksheet Columns] | De kolommen die moeten worden opgenomen in het gedownloade bulksbladbestand:<ul><li>*[!UICONTROL AMO ID]*: (Vereist als &quot;[!UICONTROL SE ID]&quot; is niet geselecteerd) Bevat een [!DNL Adobe]-generated unique identifier for each entity/row. Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post het niet aan het advertentienetwerk. Later kunt u gegevens voor de entiteit bewerken met de opdracht [!UICONTROL AMO ID] als de id, in plaats van de id van de entiteit en de moederentiteit.</li><li>*[!UICONTROL SE ID]*: (Vereist als &quot;[!UICONTROL AMO ID]&quot; is niet geselecteerd) Bevat de unieke id van het advertentienetwerk voor elke opgenomen kolom en de bovenliggende entiteiten. Later, als u gegevens voor om het even welke entiteit uitgeeft gebruikend [!UICONTROL SE ID] als id, dan moet u ook rijen voor de ouderentiteiten (met inbegrip van hun omvatten [!UICONTROL SE ID] waarden).</li><li>*[!UICONTROL Platform]*: Bevat een [!UICONTROL Platform column] aan het begin van elke rij om het advertentieplatform aan te geven (zoals &quot;Baidu&quot;).</li><li>*[!UICONTROL Acct Name]*: (Vereist als &quot;[!UICONTROL AMO ID]&quot; is niet geselecteerd) Bevat de naam van de advertentienetwerkaccount voor elke entiteit/rij.</li><li>\[Kolommen die moeten worden opgenomen\]: Alle, geen of alleen geselecteerde kolommen opnemen die relevant zijn voor elke geselecteerde entiteit in het dialoogvenster [!UICONTROL Bulksheet Rows] sectie. Klik op ![Rechterpijlpunt](/help/search-social-commerce/assets/compressed-item.png "Rechterpijlpunt") naast de entiteitsnaam. Standaard worden alle relevante kolommen opgenomen voor elke geselecteerde rij entiteiten. Schakel het selectievakje naast een entiteit of naast een afzonderlijke kolom uit om deze uit te sluiten van de lijst met opsommingstekens.</li></ul><br><br><b>Tip:</b> Zorg ervoor dat u de juiste kolommen opneemt om het item in elke rij van het bulkbladbestand te identificeren. Stel bijvoorbeeld dat u trefwoordrijen opneemt per [!UICONTROL Bulksheet Rows] , maar u sluit alle kolommen met betrekking tot trefwoorden uit. Het resulterende opsommingsteken bevat één rij voor elke trefwoordinstantie. Nochtans, aangezien geen sleutelwoordverwante kolommen inbegrepen zijn — zelfs niet identiteitskaart van AMO of identiteitskaart van SE — kunt u niet identificeren welke sleutelwoordinstantie tot een specifieke rij behoort, en u kunt niet bulksheet gebruiken om gegevens bij te werken tenzij u manueel de aangewezen kolom en de waarden van identiteitskaart toevoegt. |
| [!UICONTROL Filters] | | Criteria voor specifieke campagnes, en groepen, advertenties/creatieve personen, trefwoorden en/of plaatsen die in het bulksblad moeten worden opgenomen:<ol><li>Selecteer een parameter (naam van entiteit of ID; of een element van een creatieve waarde, trefwoord of plaatsing), selecteert u een operator en voert u vervolgens de toepasselijke waarde in.<br>Als u bijvoorbeeld alleen advertenties met &quot;schoenen&quot; in de kop wilt retourneren voor een [!DNL Google Ads] account, selecteren *[!UICONTROL Headline]*, selecteert u *[!UICONTROL contains]* en vervolgens voert u `shoes` in het invoerveld.</li><li>(Als u aanvullende filters wilt toepassen) Klik voor elk extra filter op **[!UICONTROL +Add Filter]**, selecteert u **[!UICONTROL AND]** of **[!UICONTROL OR]** selecteert u een advertentie-element of trefwoord en een operator en voert u vervolgens de toepasselijke waarde in.</li></ul> |

## Opsommingstekstrijen per ad-netwerk {#bulksheet-rows-by-ad-network}

| Opsommingstekenrij | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft® Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | Yandex | Notities |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | — |
| [!UICONTROL Adgroup] | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | — |
| [!UICONTROL Creative] *of* [!UICONTROL Creative (except RSA)] | Ja | Ja | Ja | — | — | Ja | Ja | Ja | Ja | ([!DNL Google  Ads]) Gebruik voor alle advertentietypen, behalve voor responsieve zoekopdrachten, die beschikbaar zijn in de [!UICONTROL Responsive Search Ad] rij. |
| [!UICONTROL Responsive Search Ad] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | Ja | Ja | Ja | Ja | Ja | — | Ja | Ja | Ja | Alleen gebruiken voor niet-negatieve trefwoorden. Als u negatieve trefwoorden wilt zien die op campagne- of advertentieniveau zijn gemaakt, gebruikt u de opdracht [!UICONTROL Campaign Negative Keyword] of [!UICONTROL Adgroup Negative Keyword] rij indien beschikbaar. |
| [!UICONTROL Promoted Pin] | — | — | — | — | Ja | — | — | — | — | — |
| [!UICONTROL Placement] | — | Ja | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | Ja | Ja | — | — | — | — | — | — | Wordt gebruikt voor dynamische zoekdoelen voor een advertentiegroep. |
| [!UICONTROL Shopping Product Group] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Campaign Negative Keyword] | Ja | Ja | Ja | — | — | — | Ja | Ja | — | Gebruik deze optie alleen voor negatieve trefwoorden die op campagne- of advertentieniveau zijn gemaakt. Als u niet-negatieve trefwoorden wilt zien, gebruikt u de opdracht [!UICONTROL Keyword] rij indien beschikbaar. |
| [!UICONTROL Campaign Negative Website] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Adgroup Site Link] | — | Ja | — | — | — | — | — | Ja | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | Ja | — |
| [!UICONTROL Adgroup Negative Keyword] | Ja | Ja | Ja | — | — | — | Ja | Ja | — | — |
| [!UICONTROL Adgroup Negative Website] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | Ja | Ja | Ja | — | — | — | Ja | Ja | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Campaign Device Target] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Adgroup Device Target] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Campaign RLSA Target] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | Ja | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | Ja | — | — | — | — | — | — | — | — |

>[!MORELIKETHIS]
>
>* [Campagnegegevens beheren met behulp van bulksbladen](bulksheet-about.md)
>* [Kolommen of gecorrigeerde foutbestanden plaatsen](bulksheet-post.md)
>* [Openingspagina&#39;s in bulkbladbestanden valideren](bulksheet-validate-landing-pages.md)
>* [Een gegenereerd of geüpload bulksbladbestand exporteren](bulksheet-export.md)
