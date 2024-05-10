---
title: Verwachte gegevensvariaties tussen [!DNL Analytics] en Adobe Advertising
description: Verwachte gegevensvariaties tussen [!DNL Analytics] en Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '3205'
ht-degree: 0%

---

# Verwachte gegevensvariaties tussen [!DNL Analytics] en Adobe Advertising

*Adverteerders met alleen Adobe Advertising-Adobe Analytics-integratie*

Adverteerders met de [!DNL Analytics for Advertising] <!-- (A4AdC) --> betaalde reclame via Adobe Advertising en Adobe Analytics. Wanneer u media, campagnes en kanalen bijhoudt via meerdere systemen, komen dezelfde gegevenssets van verschillende systemen zelden volledig overeen. In dit document wordt uitgelegd hoe u gegevens voor media die via Adobe Advertising worden verhandeld, moet vergelijken met gegevens in de verschillende systemen waarin de media worden bijgehouden [!DNL Analytics].

>[!NOTE]
>
>Dit document is gericht op Adobe Advertising en Analytics, maar veel van de belangrijkste punten zijn ook overdraagbaar aan andere het volgen oplossingen.

## Attribuutverschillen in vergelijkbare rapporten

### Potentieel Verschillende LookbackVensters en Modellen van de Attributie

De [!DNL Analytics for Advertising] integratie gebruikt twee variabelen ([!DNL eVars] of [!DNL rVars] \[gereserveerd [!DNL eVars]]\) om de [EF-id en AMO-id](ids.md). Deze variabelen worden gevormd met één enkel raadplegingsvenster (de tijd waarbinnen klik-productie en mening-productie worden toegeschreven) en een attributiemodel. Tenzij anders gespecificeerd, worden de variabelen gevormd om het gebrek aan te passen, klikt de adverteerder-vlakke raadplegingsvenster en attributiemodel in Adobe Advertising.

Nochtans, zijn de raadplegingsvensters en attribuutmodellen configureerbaar in beide Analytics (via [!DNL eVars]) en in Adobe Advertising. Verder is het attributiemodel in Adobe Advertising niet alleen op adverteerderniveau (voor optimalisatie van biedingen), maar ook in afzonderlijke gegevensweergaven en -rapporten (alleen voor rapportagedoeleinden) configureerbaar. Een organisatie kan bijvoorbeeld de voorkeur geven aan het toewijzingsmodel voor gelijkmatige distributie voor optimalisatie, maar de laatste aanraakkenmerk gebruiken voor rapporten in DSP of [!DNL Advertising Search, Social, & Commerce]. Als u toewijzingsmodellen wijzigt, wordt het aantal toegewezen conversies gewijzigd.

Als een terugkijkvenster of attributenmodel van het rapport in één product en niet in andere wordt gewijzigd, dan tonen de zelfde rapporten van elk systeem verschillende gegevens:

* **Voorbeeld van verschillen die worden veroorzaakt door verschillende terugkijkvensters:**

  Stel dat de Adobe Advertising een terugkijkvenster van 60 dagen heeft klikken en [!DNL Analytics] heeft een terugkijkvenster van 30 dagen. En stel dat een gebruiker naar de site komt via een advertentie, bladeren en vervolgens terugkeren op dag 45 en converteert. De Adobe Advertising kenmerkt de omzetting aan het aanvankelijke bezoek omdat de omzetting binnen het 60 dagraadplegingsvenster voorkwam. [!DNL Analytics], nochtans, kan niet de omzetting aan het aanvankelijke bezoek toeschrijven omdat de omzetting voorkwam nadat het terugkijkvenster van 30 dagen was verlopen. In dit voorbeeld rapporteert Adobe Advertising een hoger aantal conversies dan [!DNL Analytics] wel.

  ![Voorbeeld van een conversie die wel in Adobe Advertising maar niet [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Voorbeeld van discrepanties veroorzaakt door verschillende attributiemodellen:**

  Veronderstel een gebruiker met drie verschillende Adobe Advertising advertenties alvorens om te zetten, met opbrengst als omzettingstype in wisselwerking staat. Als een rapport van de Adobe Advertising een gelijk distributiemodel voor attributie gebruikt, dan attributen het de opbrengst gelijkelijk over alle advertenties. Indien [!DNL Analytics] gebruikt het laatste aanraakattributiemodel, maar geeft de opbrengst aan de laatste advertentie. In het volgende voorbeeld kent de Adobe Advertising een zelfs 10 USD van de 30 USD aan inkomsten toe die aan elk van de drie advertenties worden opgenomen, terwijl [!DNL Analytics] Alle 30 USD aan inkomsten wordt toegeschreven aan de laatste advertentie van de gebruiker. Wanneer u rapporten van Adobe Advertising en [!DNL Analytics], kunt u de impact van het verschil in attributie verwachten.

  ![Verschillende aan Adoben Advertising toegerekende opbrengsten en [!DNL Analytics] op basis van verschillende toerekeningsmodellen](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>De beste praktijken moeten de zelfde raadplegingsvensters en attributenmodel in zowel Adobe Advertising als gebruiken [!DNL Analytics]. Werk zo nodig samen met het accountteam van de Adobe om de huidige instellingen te identificeren en de configuraties synchroon te houden.

Deze zelfde concepten zijn op een andere gelijkaardige kanalen van toepassing die verschillende raadplegingsvensters of attributiemodellen gebruiken.

#### Verschillende Lookback Vensters voor het Volgen van mening-door {#impression-lookback}

In Adobe Advertising, is de attributie gebaseerd op kliks en impressies, en u kunt verschillende raadplegingsvensters voor kliks en voor impressies vormen. In [!DNL Analytics], nochtans, is de attributie gebaseerd op klikdoorhalingen en mening-door, en u hebt niet de optie om verschillende attributievensters voor klikdoorhalingen en mening-doorhalingen te plaatsen; het volgen voor elk begint bij het aanvankelijke plaatsbezoek. Een indruk kan zich voordoen op dezelfde dag of meerdere dagen voordat een view-through plaatsvindt, en dit kan van invloed zijn op de plaats waar het toewijzingsvenster in elk systeem start.

Doorgaans vindt het merendeel van de doorkijkconversies snel genoeg plaats, zodat beide systemen krediet kunnen toewijzen. Nochtans, kunnen sommige omzettingen buiten het venster van de de imitatie van de Adobe Advertising terugblik maar binnen voorkomen [!DNL Analytics] terugkijkvenster; dergelijke omzettingen worden toegeschreven aan mening binnen [!DNL Analytics] maar niet in de Adobe Advertising.

In het volgende voorbeeld, veronderstel een bezoeker een advertentie op Dag 1 werd gediend, een mening-door bezoek (namelijk bezocht de de landende pagina van de advertentie zonder eerder de advertentie) op Dag 2, en op Dag 45 omgezet. In dit geval, zou de Adobe Advertising de gebruiker van Dagen 1-14 (gebruikend een raadpleging van 14 dagen) volgen, [!DNL Analytics] zou de gebruiker bijhouden vanaf dagen 2-61 (met een 60-daagse terugzoekactie), en de conversie op dag 45 zou worden toegeschreven aan de advertentie binnen [!DNL Analytics] maar niet binnen de Adobe Advertising.

![Voorbeeld van een doorkijkconversie die wordt toegewezen in [!DNL Analytics] maar geen Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png)

Een andere oorzaak van discrepanties is dat, in Adobe Advertising, u mening-door omzettingen een douane kunt toewijzen *doorkijkgewicht* die gerelateerd is aan het gewicht dat wordt toegewezen aan een klikconversie. Het standaardgewicht van de weergave-door is 40%. Dit betekent dat een doorkijkconversie wordt geteld als 40% van de waarde van een klikconversie. [!DNL Analytics] geen dergelijke weging van doorkijkomzettingen biedt. Zo wordt bijvoorbeeld een inkooporder van 100 dollar opgenomen in [!DNL Analytics] wordt verdisconteerd tot 40 USD in Adobe Advertising als je het standaard view-through gewicht gebruikt — een verschil van 60 USD.

Houd rekening met deze verschillen bij het vergelijken van doorkijkconversies tussen Adobe Advertising en [!DNL Analytics] rapporten.

#### Beschikbare kenmerkmodellen

| Attributie Adobe Advertising | [!DNL Analytics] Attributie | [!DNL eVar]/[!DNL rVar] Toewijzing |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | nvt | nvt |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>Niet gebruiken* |
| [!UICONTROL Weight Last Event More] | nvt | nvt |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | nvt |
| nvt | [!UICONTROL J-Shaped] | nvt |
| nvt | [!UICONTROL Inverse-J] | nvt |
| nvt | [!UICONTROL Custom] | nvt |
| nvt | [!UICONTROL Participation] | nvt |
| nvt | [!UICONTROL Algorithmic] | nvt |

>[!NOTE]
>
>Voor lineaire allocatie, [!DNL Analytics] attributen success events across all all [!DNL eVar] waarden binnen één bezoek, gebruik zo lineaire toewijzing met een [!DNL eVar] verlopen van &quot;Visit&quot;. Voor reclame leidt het gebruik van lineaire toewijzing echter tot een niet echt lineaire toewijzing en tot minder dan ideale rapportage. Als een bezoeker bijvoorbeeld met drie advertenties communiceert voordat hij of zij in drie afzonderlijke bezoeken gaat omwisselen, wordt alleen de advertentie die tijdens het laatste bezoek werd getoond aan de conversie toegeschreven, niet aan alle drie advertenties.
>
>Bovendien voorkomt het schakelen van conversie naar of van &quot;Lineair&quot; dat historische gegevens worden weergegeven, wat kan leiden tot onjuiste gegevens in rapporten. Zo zou lineaire toewijzing inkomsten kunnen verdelen over een aantal verschillende [!DNL eVar] waarden. Als u de toewijzing wijzigt in &quot;Recentste&quot;, wordt 100% van die inkomsten gekoppeld aan de meest recente enkele waarde. Deze koppeling kan tot onjuiste conclusies leiden.
>
>Om verwarring te voorkomen [!DNL Analytics] maakt historische gegevens niet beschikbaar in de rapportinterface. U kunt de historische gegevens weergeven als u de [!DNL eVar] terug naar de eerste toewijzingsinstelling, maar deze mag niet worden gewijzigd [!DNL eVar] de montages van de toewijzing eenvoudig om tot historische gegevens toegang te hebben. Adobe raadt u aan een nieuwe [!DNL eVar] wanneer u een nieuwe toewijzingsinstelling wilt toepassen voor gegevens die al worden vastgelegd, in plaats van toewijzingsinstellingen te wijzigen voor een [!DNL eVar] die reeds over een aanzienlijke hoeveelheid historische gegevens beschikt.

Zie een lijst met [!DNL Analytics] attributiemodellen en de bijbehorende definities op [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Als u bent aangemeld [!DNL Search, Social, & Commerce], kunt u een lijst vinden

* (Gebruikers in Noord-Amerika) [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* (Alle andere gebruikers) [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Attributie van gebeurtenisdatum in Adobe Advertising

In Adobe Advertising, kunt u omzettingsgegevens of door de bijbehorende klikdatum/gebeurtenisdatum (de datum van de klik of de impliciete gebeurtenis) of door de transactiedatum (omzettingsdatum) melden. Het concept van click/gebeurtenisdatumrapportage bestaat niet in [!DNL Analytics]; alle omzettingen bijgehouden in [!DNL Analytics] per transactiedatum worden gerapporteerd. Dientengevolge kan dezelfde conversie met verschillende data in Adobe Advertising worden gerapporteerd en [!DNL Analytics]. Neem bijvoorbeeld een gebruiker die op 1 januari op een advertentie klikt en deze op 5 januari omzet. Als u de omzettingsgegevens door gebeurtenisdatum in Adobe Advertising bekijkt, dan wordt de omzetting gemeld op 1 Januari, toen de klik voorkwam. In [!DNL Analytics], wordt dezelfde conversie gerapporteerd op 5 januari.

![Voorbeeld van een conversie die aan verschillende datums wordt toegeschreven](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attributie in [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] rapportage](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) staat u toe om regels te vormen om verschillende marketing kanalen te identificeren die op verschillende aspecten van klapinformatie worden gebaseerd. U kunt Adobe Advertising-gevolgde kanalen volgen ([!UICONTROL Display Click Through], [!UICONTROL Display View Through], en [!UICONTROL Paid Search]) als [!DNL Marketing Channels] door de `ef_id` query string parameter om het kanaal te identificeren. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Maar hoewel de [!DNL Marketing Channels] in rapporten kunnen Adobe Advertising kanalen worden bijgehouden, de gegevens komen mogelijk om verschillende redenen niet overeen met de rapporten van de Adobe Advertising. Zie de volgende secties voor meer informatie.

>[!NOTE]
>
> De volgende kernconcepten zijn ook van toepassing op elke multikanaaltracering waarbij campagnes worden gebruikt die niet in de Adobe Advertising worden bijgehouden, zoals de [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) variable (ook wel &#39;Tracking code&#39; of &#39;[!DNL eVar] 0&quot;) en aangepast [!DNL eVar] bijhouden.

### Mogelijke verschillen in Attributiemodellen in [!DNL Marketing Channels]

Meeste [!DNL Marketing Channels] rapporten worden gevormd met [!UICONTROL Last Touch] attributie, waarvoor het laatst ontdekte marketingkanaal 100% van de omzetwaarde krijgt toegewezen. Verschillende toewijzingsmodellen gebruiken voor de [!DNL Marketing Channels] rapporten en verslagen van de Adobe Advertising leiden tot discrepanties in toegeschreven omzettingen.

### Een potentieel verschillend Lookback Venster in [!DNL Marketing Channels]

Het terugzoekvenster voor [!DNL Marketing Channels] kan worden aangepast. In Adobe Advertising, is het venster van de klikraadpleging configureerbaar, hoewel een vast venster van 60 dagen gemeenschappelijk is. Als de twee producten verschillende raadplegingsvensters gebruiken, kunt u gegevensdiscrepanties verwachten.

### Verschillende kanaalkenmerken in [!DNL Marketing Channels]

Adobe Advertising rapporteert dat alleen betaalde media die via Adobe Advertising worden verhandeld (betaalde zoekopdracht naar [!DNL Advertising Search, Social, & Commerce] advertenties en display voor advertenties DSP advertenties), terwijl [!DNL Marketing Channels] in rapporten kunnen alle digitale kanalen worden bijgehouden . Dit kan tot een discrepantie in het kanaal leiden waarvoor een omzetting wordt toegeschreven.

Betaalde zoekopdrachten en natuurlijke zoekkanalen hebben bijvoorbeeld vaak een symbiotische relatie, waarbij elk kanaal het andere kanaal helpt. De [!DNL Marketing Channels] het rapport kenmerkt sommige omzettingen aan natuurlijk onderzoek die de Adobe Advertising niet omdat het geen natuurlijk onderzoek volgt.

Neem bijvoorbeeld ook een klant die een advertentie weergeeft, op een betaalde zoekadvertentie klikt, in een e-mailbericht klikt en vervolgens een bestelling van 30 USD plaatst. Zelfs als Adobe Advertising en [!DNL Marketing Channels] beide methoden maken gebruik van het laatste aanraakattributiemodel en de conversie wordt nog steeds anders toegewezen aan beide. Adobe Advertising heeft geen toegang tot de [!UICONTROL Email] kanaal, zodat zou het betaalde onderzoek naar de omzetting crediteren. [!DNL Marketing Channels]heeft echter toegang tot alle drie de kanalen, zodat het krediet [!UICONTROL Email] voor de conversie.

![Voorbeeld van verschillende conversietoewijzing in Adobe Advertising versus [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Voor meer uitleg over de reden waarom de meetwaarden kunnen variëren, raadpleegt u &quot;[Waarom kanaalgegevens kunnen variëren tussen Adobe Advertising en [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).&quot;

## Gegevensverschillen in Adobe Analytics [!DNL Paid Search Detection]

De [verouderd [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) functie in [!DNL Analytics] staat bedrijven toe [regels vaststellen voor het volgen van betaald en biologisch zoekverkeer](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) voor specifieke zoekprogramma&#39;s. De [!DNL Paid Search Detection] de regels gebruiken zowel een vraagkoord als het verwijzende domein om betaald en natuurlijk onderzoeksverkeer te identificeren. De [!DNL Paid Search Detection] rapporten maken deel uit van de grotere groep [Methoden zoeken](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) rapporten, die verlopen wanneer een opgegeven gebeurtenis (zoals Afhandeling winkelen winkelen winkelen) plaatsvindt of het bezoek afloopt.

Hier volgt de interface voor het maken van een [!DNL Paid Search Detection] regelset:

![Voorbeeld van een regel voor betaalde zoekopdracht in [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

Het resultaat [!DNL Paid Search Detection] de rapporten bevatten [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine], en [!UICONTROL Natural Search Keywords] rapporten.

Let op de volgende twee beperkingen met gegevens in [!DNL Paid Search Detection] rapporten:

* De [!UICONTROL Paid Search Keywords] en [!UICONTROL Natural Search Keywords] In rapporten worden de zoekopdrachten weergegeven die worden aangegeven door de verwijzende URL&#39;s, niet de trefwoorden waarop gebruikers bieden. Adobe Advertising en [!DNL Analytics] de rapporten tonen de daadwerkelijke sleutelwoorden, zodat verwacht niet hen om zich aan te sluiten bij [!DNL Paid Search Detection] trefwoordrapporten.

* Wanneer de [!DNL Paid Search Detection] oorspronkelijk is gemaakt, was de oorspronkelijke zoekquery (de tekenreeks die de gebruiker in de zoekbalk in het zoekprogramma heeft ingevoerd) gemakkelijker beschikbaar voor adverteerders via de verwijzende URL. Vandaag, verduisteren de onderzoeksmotoren grotendeels de onderzoeksvraag, en [!DNL Paid Search Detection] trefwoordrapporten zijn van beperkte waarde omdat de meeste querygegevens onder &quot;unspecified&quot; vallen.

  Met [!DNL Analytics for Advertising], kunnen adverteerders betaalde trefwoorden nog steeds bijhouden in [!DNL Analytics]. Het verwijzende domein informeert de motorrapporten die de onderzoeksmotor het verkeer drijven. Aangezien de accountgegevens die specifiek zijn voor de adverteerder niet aan het verwijzende domein zijn gekoppeld, wordt al het verkeer weergegeven onder de zoekfunctie. Adverteerders met meerdere accounts in hetzelfde zoekprogramma moeten naar Adobe Advertising verwijzen of [!DNL Analytics] rapportage voor rekeningspecifieke rapportage.

### Waarom configureren [!DNL Paid Search Detection]?

De [!DNL Paid Search Detection] Met rapporten kunt u natuurlijk zoekverkeer in het dialoogvenster [[!DNL Analytics Marketing Channels] rapporten](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). Het scheiden van betaald onderzoeksverkeer tegenover natuurlijk onderzoeksverkeer is een grote manier om de waarde te begrijpen die de natuurlijke opsporing aan het volledige marketing ecosysteem brengt.

## Doorklikgegevens valideren voor [!DNL Analytics for Advertising] {#data-validation}

Voor uw integratie moet u uw doorklikgegevens valideren om ervoor te zorgen dat alle pagina&#39;s op uw site de doorklikbewerkingen correct bijhouden.

In [!DNL Analytics], een van de eenvoudigste manieren om te valideren [!DNL Analytics for Advertising] het volgen moet kliks aan instanties vergelijken gebruikend &quot;klikt aan [!UICONTROL AMO ID Instances]&quot; berekende metrische waarde, die als volgt wordt berekend:

```
Clicks to [!UICONTROL AMO ID Instances] = ([!UICONTROL AMO ID Instances] / Adobe Advertising Clicks)
```

[!UICONTROL AMO ID Instances] geeft het aantal keren weer dat [AMO-id&#39;s](ids.md) worden bijgehouden op de site. Elke keer dat op een advertentie wordt geklikt, wordt een AMO-id (`s_kwcid`) wordt toegevoegd aan de URL van de bestemmingspagina. Het aantal [!UICONTROL AMO ID Instances]Dit is dus hetzelfde als het aantal klikken en kan worden gevalideerd tegen het aantal klikken. Doorgaans wordt een 80% overeenkomende verhouding weergegeven voor [!DNL Search, Social, & Commerce] en een 30% gelijke tarief voor [!DNL DSP] verkeer (wanneer gefilterd om slechts klik-door te omvatten [!UICONTROL AMO ID Instances]). Het verschil in verwachtingen tussen onderzoek en vertoning kan door het verwachte verkeersgedrag worden verklaard. Zoekopdracht legt de intentie vast en daarom zijn gebruikers gewoonlijk van plan om op de zoekresultaten van hun zoekopdracht te klikken. Gebruikers die een weergave- of onlinevideo zien, zullen echter vaker onbedoeld op de advertentie klikken en dan van de site naar de site stuiteren of het nieuwe venster dat wordt geladen verlaten voordat de paginageactiviteit wordt bijgehouden.

In rapporten van de Adobe Advertising, kunt u klikken aan instanties op een vergelijkbare manier vergelijken gebruikend &quot;[!UICONTROL ef_id_instances]&quot; metrisch in plaats van [!UICONTROL AMO ID Instances]:

```
Clicks to [EF ID Instances = (ef_id_instances / Clicks)
```

Zorg dat de AMO-id en de EF-id goed overeenkomen. Verwacht echter niet dat de AMO-id en de EF-id allemaal op dezelfde manier overeenkomen. Dit verschil kan leiden tot kleine verschillen in het totaal [!UICONTROL AMO ID Instances] en [!UICONTROL EF ID Instances]. Indien het totaal [!UICONTROL AMO ID Instances] in [!DNL Analytics] verschillen van [!UICONTROL EF ID Instances] in Adobe Advertising met meer dan 1%, echter, contacteer uw Team van de Rekening van de Adobe voor hulp.

Zie voor meer informatie over de AMO-id en EF-id [Adobe Advertising-id&#39;s gebruikt door Analytics](ids.md).

Hieronder ziet u een voorbeeld van een werkruimte waarin u kliks naar instanties kunt bijhouden.

![Voorbeeld van een werkruimte om kliks naar instanties bij te houden](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## Gegevenssets vergelijken in [!DNL Analytics for Advertising] Telling in Adobe Advertising

De [AMO-id](ids.md) (s_kwcid de parameter van het vraagkoord wordt gebruikt voor het melden in [!DNL Analytics]en de [EF-id](ids.md) wordt gebruikt voor rapportage in Adobe Advertising. Omdat het verschillende waarden zijn, is het mogelijk dat één waarde is beschadigd of niet is toegevoegd aan de landingspagina.

Stel dat we de volgende bestemmingspagina hebben:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

waarbij de EF-id &quot;`test_ef_id`&quot; en de AMO-id &quot;`test_amo_id`.&quot;

Als een omleiding van de site plaatsvindt, kan de URL er als volgt uitzien:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

waarbij de EF-id &quot;`test_ef_id`&quot; en de AMO-id &quot;`test_amo_id#redirectAnchorTag`.&quot;

In dit voorbeeld worden door het toevoegen van de ankertag onverwachte tekens aan de AMO-id toegevoegd. Dit leidt tot een waarde die Analytics niet herkent. Deze AMO-id zou niet geclassificeerd worden en conversies die eraan gekoppeld zijn, vallen onder &quot;[!UICONTROL unspecified]&quot; of &quot;[!UICONTROL none]&quot; in [!DNL Analytics] rapporten.

Gelukkig, terwijl de kwesties als dit gemeenschappelijk zijn, resulteren zij typisch niet in een hoog percentage van discrepantie. Als u echter een grote discrepantie tussen AMO-id&#39;s constateert in [!DNL Analytics] en EF IDs in Adobe Advertising, contacteer uw Team van de Rekening van de Adobe voor hulp.

## Andere metrische overwegingen

### Het verschil tussen klikken en bezoeken {#clicks-vs-visits}

Ze lijken op elkaar, maar klikken en bezoeken geven verschillende gegevens weer:

* **Klik:** [!DNL DSP] of het zoekprogramma neemt een klik op wanneer een bezoeker op een advertentie op de website van een uitgever klikt.

* **Bezoek:** [!DNL Analytics] definieert een [bezoek](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) als een reeks pagina&#39;s die door een gebruiker worden weergegeven, eindigend volgens een van de verschillende criteria, zoals 30 minuten inactiviteit.

Een klik kan per definitie leiden tot meerdere bezoeken.

Bekijk het volgende voorbeeld: gebruiker 1 en gebruiker 2 hebben beide toegang tot een site door op een advertentie voor een Adobe Advertising te klikken. Gebruiker 1 geeft vier pagina&#39;s weer en verlaat vervolgens de dag, zodat de eerste klik resulteert in één bezoek. Gebruiker 2 geeft twee pagina&#39;s weer, verlaat voor een lunch van 45 minuten, retourneert, bekijkt nog twee pagina&#39;s en verlaat vervolgens. In dit geval leidt de eerste klik tot twee bezoeken.

![Voorbeeld van het verschil tussen klikken en bezoeken](/help/integrations/assets/a4adc-visits-example.png)

### Het verschil tussen klikken en klik-door

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Klik en klik-door zijn twee verschillende metriek:

* **Klik:** [!DNL DSP] of het zoekprogramma neemt een klik op wanneer een bezoeker op een advertentie op de website van een uitgever klikt.

* **Doorklikken:** [!DNL Analytics] registreert een klikthrough wanneer de bezoeker op de bestemmingswebsite, de landingspagina laadt, en [!DNL Analytics] verzoek onder aan pagina verzendt de gegevens naar [!DNL Analytics].

Klikken en doorklikken kunnen sterk verschillen als gevolg van een ongeluk en klikken. We hebben gezien dat de meeste klikken op weergaveadvertenties per ongeluk gebeuren. Deze bezoekers raakten op de knop Terug voordat de landingspagina wordt geladen, dus [!DNL Analytics] kan geen klik-door registreren. Dit geldt met name voor advertenties waarin een onbedoelde klik waarschijnlijker is, zoals mobiele advertenties, videobanden en advertenties die het scherm vullen en moeten worden gesloten voordat de gebruiker de pagina kan bekijken.

Sites die op mobiele apparaten worden geladen, zullen ook minder vaak een doorklik tot gevolg hebben vanwege een lagere bandbreedte of een lagere verwerkingscapaciteit, waardoor het langer duurt om bestemmingspagina&#39;s te laden. Het is niet ongebruikelijk voor 50-70% van kliks om niet in klikproductie te resulteren. In mobiele omgevingen kan het verschil oplopen tot 90% vanwege de combinatie van een langzamere browser en de hogere kans dat de gebruiker per ongeluk op de advertentie klikt terwijl de pagina wordt doorgeschoven of de advertentie wordt gesloten.

De klikgegevens kunnen ook worden geregistreerd in milieu&#39;s die klikdoorgangen met de huidige volgende mechanismen (zoals kliks die naar, of van, een mobiele app gaan) niet kunnen registreren of waarvoor de adverteerder slechts één het volgen benadering (bijvoorbeeld, met mening-door JavaScript benadering, browsers die derdekoekjes houden klikken, maar niet klikken-door) opstelde. Een zeer belangrijke reden dat de Adobe aanbeveelt zowel de klik URL het volgen als mening-door JavaScript het volgen benaderingen op te stellen is dekking van volgbare klikthrough te maximaliseren.

### Het gebruiken van de Metriek van het Verkeer van de Adobe Advertising voor Dimensionen niet van de Adobe Advertising

Adobe Advertising biedt Analytics met [reclamespecifieke verkeersmaatstaven en de daarmee verband houdende afmetingen van [!DNL DSP] en [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). De Adobe Advertising-verstrekte metriek is van toepassing slechts op de gespecificeerde afmetingen van de Adobe Advertising, en de gegevens zijn niet beschikbaar voor andere dimensies in [!DNL Analytics].

Als u bijvoorbeeld de [!UICONTROL Adobe Advertising Clicks] en [!UICONTROL Adobe Advertising Cost] metriek door Rekening, die een dimensie van de Adobe Advertising is, dan het totaal [!UICONTROL Adobe Advertising Clicks] en [!UICONTROL Adobe Advertising Cost] worden per account weergegeven.

![Voorbeeld van Adobe Advertising metriek in een rapport gebruikend een dimensie van de Adobe Advertising](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Als u echter de [!UICONTROL Adobe Advertising Clicks] en [!UICONTROL Adobe Advertising Cost] metriek door een op-pagina afmeting (zoals Pagina), waarvoor de Adobe Advertising geen gegevens verstrekt, toen [!UICONTROL Adobe Advertising Clicks] en [!UICONTROL Adobe Advertising Cost] voor elke pagina is nul (0).

![Voorbeeld van meetgegevens voor Adoben Advertising in een rapport met een niet-ondersteunde dimensie](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Gebruiken [!UICONTROL AMO ID Instances] als plaatsvervanger voor Klikken met Dimensionen zonder Adobe Advertising

Omdat u het niet kunt gebruiken [!UICONTROL AMO Clicks] met onsite afmetingen, wilt u misschien een equivalent aan klikken. Mogelijk bent u geneigd Visit te gebruiken als een vervanging, maar dit is niet de beste optie, omdat elke bezoeker meerdere bezoeken kan hebben. (Zie &quot;[Het verschil tussen klikken en bezoeken](#clicks-vs-visits).&quot; In plaats daarvan raden we u aan [!UICONTROL AMO ID Instances], dit is het aantal keren dat de AMO-id wordt vastgelegd. while [!UICONTROL AMO ID Instances] niet overeenkomen [!UICONTROL AMO Clicks] zij zijn precies de beste optie om klikverkeer op de plaats te meten. Zie voor meer informatie &quot;[Doorklikgegevens valideren voor [!DNL Analytics for Advertising]](#data-validation).&quot;

![Voorbeeld van [!UICONTROL AMO ID Instances] in plaats van [!UICONTROL Adobe Advertising Clicks] voor een niet-ondersteunde dimensie](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Overzicht van [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising-id&#39;s gebruikt door [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Adoben Advertising in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Gegevens in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Waarom gegevens kunnen verschillen tussen Adobe Advertising en [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
