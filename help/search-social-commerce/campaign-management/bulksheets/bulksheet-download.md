---
title: Een bulkbladbestand downloaden/maken
description: Leer hoe u bulksheet-bestanden kunt maken door accountgegevens voor uw advertentienetwerken te downloaden.
exl-id: a3fcef52-3d36-462e-a975-c741d003326e
feature: Search Bulksheets
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 0%

---

# Een bulkbladbestand downloaden/maken

U kunt bulksbladen tot stand brengen gebruikend douanemontages voor één of meerdere rekeningen op één of meerdere [&#x200B; gesteunde advertentienetwerken &#x200B;](bulksheet-about.md#bulksheet-functionality-by-network). Opsommingstekens bevatten gegevens in Zoeken, Sociaal en Commerce.

Voor gesynchroniseerde campagnes kunt u optioneel synchroniseren met het advertentienetwerk voordat u de gegevens downloadt om ervoor te zorgen dat recente gegevenswijzigingen aan de zijde van het advertentienetwerk worden opgenomen. Voor alle advertentienetwerken, kunt u naar keuze nieuwe klik-volgende URLs produceren om in het dossier te omvatten.

>[!NOTE]
>
>U kunt ook [&#x200B; tot een bulksheet dossier leiden dat op de zichtbare kolommen in een mening van het campagnebeheer &#x200B;](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md) wordt gebaseerd.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]** .

1. Klik in de werkbalk op **[!UICONTROL Download Bulksheet]** .

1. Specificeer de [&#x200B; montages van het bulksblad &#x200B;](#bulksheet-download-settings):

1. Voer op het tabblad **[!UICONTROL Selections]** gegevens in de velden in of selecteer deze.

1. (Optioneel) Klik op het tabblad **[!UICONTROL Rows and Columns]** , geef de accountcomponenten en componentstatussen op waarvoor u rijen in het bulksblad wilt opnemen en geef vervolgens de kolommen op die u voor elke geselecteerde component wilt opnemen.

   Voor een lijst van beschikbare bulksbladrijen, zie &quot;[&#x200B; de rijen van het Bulksblad door netwerk &#x200B;](#bulksheet-rows-by-ad-network) toe te voegen.&quot;

1. (Optioneel) Klik op het tabblad **[!UICONTROL Filters]** en geef vervolgens criteria op voor specifieke campagnes, en groepen, advertenties/creatieven, trefwoorden, plaatsingen en andere entiteiten die u wilt opnemen in het bulksblad:

   1. Selecteer een parameter (entiteitsnaam of identiteitskaart; of om het even welk element van een advertentie, sleutelwoord, of plaatsing), selecteer een exploitant, en ga dan de toepasselijke waarde in. Bijvoorbeeld, om slechts advertenties met &quot;schoenen&quot;in de titel voor een [!DNL Google Ads] rekening terug te keren, selecteer *Titel*, selecteer *[!UICONTROL contains]*, en ga dan `shoes` op het inputgebied in.

   1. (Als u aanvullende filters wilt toepassen) Klik voor elk extra filter op **[!UICONTROL +Add Filter]** , selecteer **[!UICONTROL AND]** of **[!UICONTROL OR]** , selecteer een advertentie-element of trefwoord en een operator en voer vervolgens de toepasselijke waarde in.

1. Klik op **[!UICONTROL Download]**.

Wanneer de taak begint, toont het venster een bericht maar open blijft zodat kunt u extra bulksbladen blijven tot stand brengen als u wilt. Alle opgegeven filters en uitsluitingen die van toepassing zijn op nieuwe accounts die u selecteert, blijven behouden. Wanneer de taak begint, wordt het bestand weergegeven in de weergave Opsommingstekens. Wanneer het bestand is gemaakt, ontvangt u een e-mailbericht met een koppeling naar het bestand. Afhankelijk van de hoeveelheid gegevens die wordt gecompileerd, kan het een paar minuten of langer duren. Als het genereren van het bestand echter mislukt, wordt een foutbestand weergegeven in de weergave Opsommingstekens en ontvangt u een e-mailmelding met een koppeling naar het foutbestand.

## Downloadinstellingen voor werkbladen {#bulksheet-download-settings}

| Tab | Parameter | Beschrijving |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | De accounts, campagnes of advertentiegroepen waarnaar de gegevens moeten worden geüpload:<ul><li>Als u een account en alle bijbehorende campagnes en advertentiegroepen wilt selecteren, schakelt u het selectievakje naast de naam van de account in en klikt u op >> om de account naar de kolom [!UICONTROL Selected Filters] te verplaatsen.</li><li>Als u afzonderlijke campagnes of advertentiegroepen wilt selecteren, klikt u naast de account om deze uit te vouwen. Klik (indien nodig) naast de campagne of de groep om de campagne of de groep uit te vouwen, selecteer het selectievakje naast de naam van de campagne of de groep en klik vervolgens op >> om deze naar de kolom [!UICONTROL Selected Filters] te verplaatsen. Als u bijvoorbeeld alleen gegevens wilt ophalen voor Campagne 1 in Account 1, vouwt u Account 1 uit, schakelt u het selectievakje naast Campagne 1 in en verplaatst u het vervolgens naar de kolom [!UICONTROL Selected Filters] .</li></ul><b> Nota&#39;s:</b><ul><li>Eén enkel bulksblad kan van toepassing zijn op meerdere accounts in meerdere advertentienetwerken. De netwerk-specifieke kolommen van de extra zijn geëtiketteerd in bulksbladen met de naam van het advertentienetwerk (zoals &quot;Mobiele Dragers (de Advertentie van Google)&quot;).</li><li>Als u wilt zien welk type component een item is, houdt u de cursor erop.</li><li>Voor campagnes staat de eerste letter van de naam van het advertentienetwerk tussen haakjes achter de accountnaam (zoals &quot;Acme Realty (G)&quot; voor een [!DNL Google Ads] account).</li><li>Standaard worden alleen actieve en ingeschakelde accounts en hun actieve componenten weergegeven. Om gepauzeerde en geschrapte componenten te bekijken, klik ![&#x200B; neer pijl &#x200B;](/help/search-social-commerce/assets/arrow-down-expand.png " neer pijl ") naast [!UICONTROL Show] en selecteer ** [!UICONTROL All]. |
| | [!UICONTROL Generate Tracking URLs] | (Optioneel) Bevat volgsjablonen en achtervoegsels van bestemmingspagina&#39;s (voor toepasselijke advertentienetwerken) in accounts met trackingsjablonen, of doel-URL&#39;s met ingesloten trackingcodes in accounts met doel-URL&#39;s, voor trefwoorden, advertenties, plaatsaanduidingen, sitelinks en [!DNL Google Ads] -productgroepen in het bulksblad. Deze optie is standaard geselecteerd.<br><br> wanneer deze optie wordt geselecteerd, wordt URLs geproduceerd volgens de parameters in de [!UICONTROL Campaign Tracking] sectie van de rekeningsmontages of campagnemontages. Als er al URL&#39;s worden bijgehouden, worden deze standaard niet opnieuw gegenereerd, tenzij er nieuwe URL&#39;s nodig zijn (bijvoorbeeld als het trefwoordtype, de advertentietekst of de trackingparameters van de account zijn gewijzigd).<br><br><b> Nota&#39;s:</b><ul><li>Als de adverteerder gebruikmaakt van het bijhouden van Adobe Advertising-conversies en de desbetreffende account niet is geconfigureerd voor het automatisch genereren en uploaden van URL&#39;s voor bijhouden, moet u nieuwe URL&#39;s genereren wanneer de basis-URL&#39;s zijn gewijzigd.</li><li>Als u deze optie niet selecteert, kunt u later nog URL&#39;s voor bijhouden genereren wanneer u het bestand uploadt of post.</li></ul> |
| | [!UICONTROL Perform Pre-sync] | (Optioneel) Hiermee wordt Zoekopdrachten, sociale gegevens en Commerce geïnstrueerd om de bestanden te synchroniseren met de opgegeven campagnes om ervoor te zorgen dat alle gegevens gelijk zijn. Deze optie is standaard niet geselecteerd.<br><b> Nota:</b> Onderzoek, Sociale, &amp; Commerce synchroniseert automatisch met het advertentienetwerk eens per dag, wanneer het een nieuwe campagne op het advertentienetwerk ontdekt, en telkens als u campagnegegevens van binnen Onderzoek, Sociale, &amp; Commerce verandert. Selecteer deze optie als u denkt dat recente wijzigingen in campagne- of accountgegevens rechtstreeks zijn aangebracht in het advertentienetwerk of met de bureaubladeditor van het advertentienetwerk. Het maken van werkbladen duurt langer als u deze optie selecteert. |
| | [!UICONTROL Bulksheet Name] | De naam van het nieuwe bulksblad en het bestandstype. Standaard wordt het bestand gemaakt in een indeling met tabgescheiden waarden en krijgt het de volgende naam:<ul><li>(voor alle accounts van het advertentienetwerk) `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(voor enkelvoudige accounts) `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>(voor meerdere accounts) `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv` .</li></ul>U kunt de naam van het bestand wijzigen. De naam mag de volgende tekens niet bevatten: `# % & * \| \ : : < > . ? or /` .<br><br> naar keuze, verander het dossiertype. De opties zijn *[!UICONTROL .tsv]* (voor door tabs gescheiden waarden), *[!UICONTROL .txt]* (voor ASCII-tekst die compatibel is met Unicode), *[!UICONTROL .csv]* (voor door komma&#39;s gescheiden waarden) of *[!UICONTROL .zip]* (voor gecomprimeerde ZIP-indeling die wordt uitgepakt naar een TSV-bestand).<br><br><b> Uiteinde:</b> voor bulksbladen die internationale karakters omvatten, gebruik TSV of formaat TXT. |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | De entiteiten, en hun overeenkomstige status, om in het bulksblad op te nemen, met één gegevensrij per ingang. Als u bijvoorbeeld actieve campagnes opneemt, bevat het blad één rij per actieve campagne. Alleen geselecteerde entiteiten met de geselecteerde status worden opgenomen. De standaardwaarden worden vooraf geselecteerd op basis van het opgegeven advertentienetwerk. Standaard worden alleen actieve instanties van de geselecteerde entiteiten opgenomen. Voor een lijst van beschikbare bulksbladrijen, zie &quot;[&#x200B; de rijen van het Bulksblad door netwerk &#x200B;](#bulksheet-rows-by-ad-network) toe te voegen.&quot;<br><br> om entiteiten toe te voegen of te verwijderen, selecteer of ontruim de controlevakjes naast de entiteiten, respectievelijk. Als u statussen voor een entiteit wilt toevoegen of verwijderen, klikt u naast het statusmenu en schakelt u respectievelijk de selectievakjes naast de entiteiten in of uit. |
| | [!UICONTROL Cascading Status Hierarchy] | Filtert het werkingsgebied van kindentiteiten aan die met de gespecificeerde ouderentiteitstatus, gebruikend EN. Bijvoorbeeld, als u &quot;Actieve Campagne,&quot;Actieve Adgroup,&quot;en &quot;Actief Sleutelwoord selecteert,&quot;dan omvat bulksheet slechts actieve sleutelwoorden in actieve en groepen in actieve campagnes.<br><br> als u deze optie niet selecteert, dan wordt de ouderstatus niet overwogen, en de filter gebruikt OF verrichting. Bijvoorbeeld, als u &quot;Actieve Campagne,&quot;Actieve Adgroup,&quot;en &quot;Actief Sleutelwoord selecteert,&quot;dan omvat het bulksblad alle actieve campagnes; alle actieve ad groepen, ongeacht de status van de oudercampagne; en alle actieve sleutelwoorden, ongeacht de oudercampagne en status van de advertentiegroep. |
| | [!UICONTROL Bulksheet Columns] | De kolommen die moeten worden opgenomen in het gedownloade bulksbladbestand:<ul><li>*[!UICONTROL AMO ID]*: (Vereist als &quot;[!UICONTROL SE ID]&quot; niet is geselecteerd) Bevat een door [!DNL Adobe] gegenereerde unieke id voor elke entiteit/rij. Search, Social &amp; Commerce gebruikt de waarde om te bepalen welke identiteit moet worden bewerkt, maar plaatst deze niet op het advertentienetwerk. Later kunt u gegevens voor de entiteit bewerken met de id [!UICONTROL AMO ID] in plaats van de id&#39;s van de entiteit en de bovenliggende entiteit.</li><li>*[!UICONTROL SE ID]*: (Vereist als &quot;[!UICONTROL AMO ID]&quot;niet wordt geselecteerd) omvat het unieke herkenningsteken van het advertentienetwerk voor elke inbegrepen kolom en zijn ouderentiteiten. Als u later gegevens voor een entiteit bewerkt met [!UICONTROL SE ID] als id, moet u ook rijen voor de bovenliggende entiteiten (inclusief de [!UICONTROL SE ID] -waarden) opnemen.</li><li>*[!UICONTROL Platform]*: neemt [!UICONTROL Platform column] aan het begin van elke rij op om het advertentieplatform aan te geven (zoals &quot;Baidu&quot;).</li><li>*[!UICONTROL Acct Name]*: (Vereist als &quot;[!UICONTROL AMO ID]&quot; niet is geselecteerd) Bevat de naam van de advertentienetwerkaccount voor elke entiteit/rij.</li><li>\[Kolommen die moeten worden opgenomen\]: als u alle, geen of alleen geselecteerde kolommen wilt opnemen die relevant zijn voor elke geselecteerde entiteit in de sectie [!UICONTROL Bulksheet Rows] . Om de individuele kolommen relevant voor een entiteit te zien, klik ![&#x200B; Juiste pijlpunt &#x200B;](/help/search-social-commerce/assets/compressed-item.png " Juiste pijlpunt ") naast de entiteitnaam. Standaard worden alle relevante kolommen opgenomen voor elke geselecteerde rij entiteiten. Schakel het selectievakje naast een entiteit of naast een afzonderlijke kolom uit om deze uit te sluiten van de lijst met opsommingstekens.</li></ul><br><br><b> Uiteinde:</b> zorg ervoor dat u adequate kolommen omvat om het punt in elke rij van het bulkbladdossier te identificeren. Stel bijvoorbeeld dat u trefwoordrijen opneemt per de kiezer van [!UICONTROL Bulksheet Rows] , maar dat u alle kolommen met betrekking tot trefwoorden uitsluit. Het resulterende opsommingsteken bevat één rij voor elke trefwoordinstantie. Nochtans, aangezien geen sleutelwoordverwante kolommen inbegrepen zijn — zelfs niet identiteitskaart van AMO of identiteitskaart van SE — kunt u niet identificeren welke sleutelwoordinstantie tot een specifieke rij behoort, en u kunt niet bulksheet gebruiken om gegevens bij te werken tenzij u manueel de aangewezen kolom en de waarden van identiteitskaart toevoegt. |
| [!UICONTROL Filters] | | Criteria voor specifieke campagnes, en groepen, advertenties/creatieve personen, trefwoorden en/of plaatsen die in het bulksblad moeten worden opgenomen:<ol><li>Selecteer een parameter (entiteitsnaam of identiteitskaart; of om het even welk element van creatief, sleutelwoord, of plaatsing), selecteer een exploitant, en ga dan de toepasselijke waarde in.<br> bijvoorbeeld, om slechts advertenties met &quot;schoenen&quot;in de titel voor een [!DNL Google Ads] rekening terug te keren, selecteer *[!UICONTROL Headline]*, selecteer *[!UICONTROL contains]*, en ga dan `shoes` op het inputgebied in.</li><li>(Als u aanvullende filters wilt toepassen) Klik voor elk extra filter op **[!UICONTROL +Add Filter]** , selecteer **[!UICONTROL AND]** of **[!UICONTROL OR]** , selecteer een advertentie-element of trefwoord en een operator en voer vervolgens de toepasselijke waarde in.</li></ul> |

## Opsommingstekstrijen per ad-netwerk {#bulksheet-rows-by-ad-network}

| Opsommingstekenrij | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | Yandex | Notities |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | — |
| [!UICONTROL Adgroup] | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | Ja | — |
| [!UICONTROL Creative] *of* [!UICONTROL Creative (except RSA)] | Ja | Ja | Ja | — | — | Ja | Ja | Ja | Ja | ([!DNL Google  Ads]) Gebruik deze optie voor alle advertentietypen, behalve voor responsieve zoekopdrachten, die beschikbaar zijn in de [!UICONTROL Responsive Search Ad] -rij. |
| [!UICONTROL Responsive Search Ad] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | Ja | Ja | Ja | Ja | Ja | — | Ja | Ja | Ja | Alleen gebruiken voor niet-negatieve trefwoorden. Als u negatieve trefwoorden wilt zien die op campagne- of advertentieniveau zijn gemaakt, gebruikt u de rij [!UICONTROL Campaign Negative Keyword] of [!UICONTROL Adgroup Negative Keyword] (indien beschikbaar). |
| [!UICONTROL Promoted Pin] | — | — | — | — | Ja | — | — | — | — | — |
| [!UICONTROL Placement] | — | Ja | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | Ja | Ja | — | — | — | — | — | — | Wordt gebruikt voor dynamische zoekdoelen voor een advertentiegroep. |
| [!UICONTROL Shopping Product Group] | — | Ja | Ja | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | Ja | Ja | — | — | — | — | Ja | — | — |
| [!UICONTROL Campaign Negative Keyword] | Ja | Ja | Ja | — | — | — | Ja | Ja | — | Gebruik deze optie alleen voor negatieve trefwoorden die op campagne- of advertentieniveau zijn gemaakt. Als u niet-negatieve trefwoorden wilt zien, gebruikt u de [!UICONTROL Keyword] -rij (indien beschikbaar). |
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
>* [&#x200B; Ongeveer het beheren van campagnegegevens gebruikend bulksbladen &#x200B;](bulksheet-about.md)
>* [&#x200B; Post bulksbladen of gecorrigeerde foutendossiers &#x200B;](bulksheet-post.md)
>* [&#x200B; bevestigt het landen pagina&#39;s in bulksheet dossiers &#x200B;](bulksheet-validate-landing-pages.md)
>* [&#x200B; de Uitvoer een geproduceerd of geupload bulksbladdossier &#x200B;](bulksheet-export.md)
