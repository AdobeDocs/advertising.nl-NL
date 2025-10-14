---
title: Verwachte Variaties van Gegevens tussen  [!DNL Analytics]  en Adobe Advertising
description: Verwachte Variaties van Gegevens tussen  [!DNL Analytics]  en Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 6470ed471c60477bf19cf9b125f0250136f31511
workflow-type: tm+mt
source-wordcount: '3358'
ht-degree: 0%

---

# Verwachte gegevensvariaties tussen [!DNL Analytics] en Adobe Advertising

*Advertisers met Adobe Advertising-Adobe Analytics slechts Integratie*

Adverteerders met de [!DNL Analytics for Advertising] <!-- (A4AdC) --> -integratietrack betalen reclame via Adobe Advertising en Adobe Analytics. Wanneer u media, campagnes en kanalen bijhoudt via meerdere systemen, komen dezelfde gegevenssets van verschillende systemen zelden volledig overeen. In dit document wordt uitgelegd hoe u gegevens voor media die via Adobe Advertising worden verhandeld, moet vergelijken met gegevens in de verschillende systemen waarin de media worden bijgehouden in [!DNL Analytics] .

>[!NOTE]
>
>Dit document is gericht op Adobe Advertising en Analytics, maar veel van de belangrijkste punten zijn ook overdraagbaar aan andere het volgen oplossingen.

## Attribuutverschillen in vergelijkbare rapporten

### Potentieel Verschillende LookbackVensters en Modellen van de Attributie

De [!DNL Analytics for Advertising] integratie gebruikt twee variabelen ([!DNL eVars] of [!DNL rVars] \ [gereserveerde [!DNL eVars]] \) om [&#x200B; EF identiteitskaart en identiteitskaart van AMO &#x200B;](ids.md) te vangen. Deze variabelen worden gevormd met één enkel raadplegingsvenster (de tijd waarbinnen klik-productie en mening-productie worden toegeschreven) en een attributiemodel. Tenzij anders gespecificeerd, worden de variabelen gevormd om het gebrek aan te passen, klikt de adverteerder-vlakke raadplegingsvenster en attributiemodel in Adobe Advertising.

De terugkijkvensters en attributiemodellen kunnen echter zowel in Analytics (via [!DNL eVars]) als in Adobe Advertising worden geconfigureerd. Verder is het attributiemodel in Adobe Advertising niet alleen op adverteerderniveau (voor optimalisatie van biedingen), maar ook in afzonderlijke gegevensweergaven en -rapporten (alleen voor rapportagedoeleinden) configureerbaar. Een organisatie kan bijvoorbeeld de voorkeur geven aan het toewijzingsmodel voor gelijkmatige verdeling voor optimalisatie, maar de laatste aanraakkenmerk gebruiken voor rapporten in Advertising DSP of [!DNL Advertising Search, Social, & Commerce] . Als u toewijzingsmodellen wijzigt, wordt het aantal toegewezen conversies gewijzigd.

Als een terugkijkvenster of attributenmodel van het rapport in één product en niet in andere wordt gewijzigd, dan tonen de zelfde rapporten van elk systeem verschillende gegevens:

* **Voorbeeld van discrepanties die door verschillende raadplegingsvensters worden veroorzaakt:**

  Stel dat de Adobe Advertising een terugkijkvenster van 60 dagen heeft en [!DNL Analytics] een terugkijkvenster van 30 dagen heeft. En stel dat een gebruiker naar de site komt via een advertentie, bladeren en vervolgens terugkeren op dag 45 en converteert. De Adobe Advertising kenmerkt de omzetting aan het aanvankelijke bezoek omdat de omzetting binnen het 60 dagraadplegingsvenster voorkwam. [!DNL Analytics] kan de conversie echter niet toewijzen aan het eerste bezoek omdat de conversie heeft plaatsgevonden nadat het terugzoekvenster van 30 dagen is verlopen. In dit voorbeeld rapporteert Adobe Advertising een hoger aantal conversies dan [!DNL Analytics].

  ![&#x200B; Voorbeeld van een omzetting die in Adobe Advertising maar niet wordt toegeschreven [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Voorbeeld van discrepanties die door verschillende attributiemodellen worden veroorzaakt:**

  Veronderstel dat een gebruiker met drie verschillende Adobe Advertising adverteert alvorens om te zetten, met opbrengst als omzettingstype in wisselwerking staat. Als een rapport van de Adobe Advertising een gelijk distributiemodel voor attributie gebruikt, dan attributen het de opbrengst gelijkelijk over alle advertenties. Als [!DNL Analytics] echter het laatste aanraakattributiemodel gebruikt, wordt de opbrengst toegewezen aan de laatste advertentie. In het volgende voorbeeld kent Adobe Advertising zelfs 10 USD van de 30 USD aan inkomsten toe die aan elk van de drie advertenties worden vastgelegd, terwijl [!DNL Analytics] alle 30 USD aan inkomsten toewijst aan de laatste advertentie die de gebruiker heeft gezien. Wanneer u rapporten van Adobe Advertising en [!DNL Analytics] vergelijkt, kunt u het effect van het verschil in attributie verwachten te zien.

  ![&#x200B; Verschillende die opbrengst aan Adobe Advertising wordt toegeschreven en [!DNL Analytics] op verschillende attributiemodellen &#x200B;](/help/integrations/assets/a4adc-attribution-example.png) wordt gebaseerd

>[!IMPORTANT]
>
>De beste manier is om dezelfde terugzoekvensters en toewijzingsmodel te gebruiken in zowel Adobe Advertising als [!DNL Analytics] . Werk zo nodig samen met het accountteam van de Adobe om de huidige instellingen te identificeren en de configuraties synchroon te houden.

Deze zelfde concepten zijn op een andere gelijkaardige kanalen van toepassing die verschillende raadplegingsvensters of attributiemodellen gebruiken.

#### Verschillende Lookback Vensters voor het Volgen van mening-door {#impression-lookback}

In Adobe Advertising, is de attributie gebaseerd op kliks en impressies, en u kunt verschillende raadplegingsvensters voor kliks en voor impressies vormen. In [!DNL Analytics], echter, is de attributie gebaseerd op klikproductie en mening-productie, en u hebt niet de optie om verschillende attributievensters voor klikproductie en mening-doorheen te plaatsen; het volgen voor elk begint bij het aanvankelijke plaatsbezoek. Een indruk kan zich voordoen op dezelfde dag of meerdere dagen voordat een view-through plaatsvindt, en de timing kan van invloed zijn op de plaats waar het toewijzingsvenster in elk systeem start.

Doorgaans vindt het merendeel van de doorkijkconversies snel genoeg plaats, zodat beide systemen krediet kunnen toewijzen. Er kunnen echter conversies optreden buiten het Adobe Advertising-imitatievenster, maar binnen het [!DNL Analytics] lookback-venster. Dergelijke conversies worden toegeschreven aan de view-through in [!DNL Analytics] , maar niet aan de Adobe Advertising.

Stel dat een bezoeker op dag 1 een advertentie heeft ontvangen, op dag 2 een doorkijkbezoek heeft uitgevoerd (dat wil zeggen, de landingspagina van de advertentie heeft bezocht zonder eerder op de advertentie te klikken) en op dag 45 is omgezet. In dit geval houdt de Adobe Advertising de gebruiker van Dagen 1-14 bij (met een 14-daagse terugzoekactie), [!DNL Analytics] volgt de gebruiker van Dagen 2-61 (met een 60-daagse terugzoekactie) en de conversie op Dag 45 wordt binnen [!DNL Analytics] maar niet binnen de Adobe Advertising aan de advertentie toegewezen.

![&#x200B; Voorbeeld van een mening-door omzetting die in [!DNL Analytics] maar niet Adobe Advertising wordt toegeschreven &#x200B;](/help/integrations/assets/a4adc-viewthrough-example.png)

Een verdere oorzaak van discrepanties is dat, in Adobe Advertising, u mening-door omzettingen een douane *mening-door gewicht* kunt toewijzen dat met betrekking tot het gewicht is dat aan een op klik-gebaseerde omzetting wordt toegeschreven. Het standaardgewicht van de weergave-door is 40%. Dit betekent dat een doorkijkconversie wordt geteld als 40% van de waarde van een klikconversie. [!DNL Analytics] biedt niet een dergelijke weging van doorkijkconversies. Zo, bijvoorbeeld, wordt een 100 USD opbrengstorde die in [!DNL Analytics] wordt gevangen gedisconteerd aan 40 USD in Adobe Advertising als u het standaardmening-door gewicht gebruikt - een verschil van 60 USD.

Houd rekening met deze verschillen bij het vergelijken van doorkijkconversies tussen Adobe Advertising- en [!DNL Analytics] -rapporten.

#### Beschikbare kenmerkmodellen

| Attributie Adobe Advertising | [!DNL Analytics] Attributie | [!DNL eVar]/[!DNL rVar] Toewijzing |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | nvt | nvt |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br> Niet gebruiken* |
| [!UICONTROL Weight Last Event More] | nvt | nvt |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | nvt |
| nvt | [!UICONTROL J-Shaped] | nvt |
| nvt | [!UICONTROL Inverse-J] | nvt |
| nvt | [!UICONTROL Custom] | nvt |
| nvt | [!UICONTROL Participation] | nvt |
| nvt | [!UICONTROL Algorithmic] | nvt |

>[!NOTE]
>
>Voor lineaire toewijzing kent [!DNL Analytics] succesgebeurtenissen in gelijke mate toe aan alle [!DNL eVar] -waarden binnen één bezoek. Gebruik dus lineaire toewijzing met een [!DNL eVar] -vervaldatum van &quot;Visit&quot;. Voor reclame leidt het gebruik van lineaire toewijzing echter tot een niet echt lineaire toewijzing en tot minder dan ideale rapportage. Als een bezoeker bijvoorbeeld met drie advertenties communiceert voordat hij of zij in drie afzonderlijke bezoeken gaat omwisselen, wordt alleen de advertentie die tijdens het laatste bezoek werd getoond aan de conversie toegeschreven, niet aan alle drie advertenties.
>
>Bovendien voorkomt het schakelen van conversie naar of van &quot;Lineair&quot; dat historische gegevens worden weergegeven, wat kan leiden tot onjuiste gegevens in rapporten. Met lineaire toewijzing kunt u bijvoorbeeld de omzet verdelen over een aantal verschillende [!DNL eVar] -waarden. Als u de toewijzing wijzigt in &quot;Recentste&quot;, wordt 100% van die inkomsten gekoppeld aan de meest recente enkele waarde. Deze koppeling kan tot onjuiste conclusies leiden.
>
>Om verwarring te voorkomen maakt [!DNL Analytics] historische gegevens niet beschikbaar in de rapportinterface. U kunt de historische gegevens weergeven als u de [!DNL eVar] terugzet naar de eerste toewijzingsinstelling, maar u mag de toewijzingsinstellingen van [!DNL eVar] niet wijzigen om alleen toegang te krijgen tot historische gegevens. Adobe raadt u aan een nieuwe [!DNL eVar] te gebruiken wanneer u een nieuwe toewijzingsinstelling wilt toepassen voor gegevens die al worden opgenomen, in plaats van toewijzingsinstellingen te wijzigen voor een [!DNL eVar] die al een aanzienlijke hoeveelheid historische gegevens bevat.

Zie een lijst van [!DNL Analytics] attributiemodellen en hun definities in [&#x200B; https://experienceleague.adobe.com/nl/docs/analytics/analyze/analysis-workspace/attribution/models &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/analyze/analysis-workspace/attribution/models).

Als u bent aangemeld bij [!DNL Search, Social, & Commerce] , kunt u een lijst vinden

* (Gebruikers in Noord-Amerika) [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm` &#x200B;](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* (Alle andere gebruikers) [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm` &#x200B;](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Attributie van gebeurtenisdatum in Adobe Advertising

In Adobe Advertising, kunt u omzettingsgegevens of door de bijbehorende klikdatum/gebeurtenisdatum (de datum van de klik of de impliciete gebeurtenis) of door de transactiedatum (omzettingsdatum) melden. Het concept van rapportage van click/gebeurtenisdatum bestaat niet in [!DNL Analytics]. Alle conversies die in [!DNL Analytics] worden bijgehouden, worden gerapporteerd op transactiedatum. Als gevolg hiervan kan dezelfde conversie met verschillende datums in Adobe Advertising en [!DNL Analytics] worden gerapporteerd. Neem bijvoorbeeld een gebruiker die op 1 januari op een advertentie klikt en deze op 5 januari omzet. Als u de omzettingsgegevens door gebeurtenisdatum in Adobe Advertising bekijkt, dan wordt de omzetting gemeld op 1 Januari, toen de klik voorkwam. In [!DNL Analytics] wordt dezelfde conversie gerapporteerd op 5 januari.

![&#x200B; Voorbeeld van een omzetting die aan verschillende data wordt toegeschreven &#x200B;](/help/integrations/assets/a4adc-conversions-based-on.png)

## Kenmerk in [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels]  het melden &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html?lang=nl-NL) staat u toe om regels te vormen om verschillende marketing kanalen te identificeren die op verschillende aspecten van klapinformatie worden gebaseerd. U kunt kanalen met Adobe Advertising als [!UICONTROL Display Click Through], [!UICONTROL Display View Through] en [!UICONTROL Paid Search]) [!DNL Marketing Channels] bijhouden door het kanaal te identificeren aan de hand van de parameter van de queryreeks `ef_id` . <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Hoewel in de [!DNL Marketing Channels] -rapporten wel Adobe Advertising kanalen kunnen worden bijgehouden, komen de gegevens mogelijk om verschillende redenen niet overeen met de rapporten van de Adobe Advertising. Zie de volgende secties voor meer informatie.

>[!NOTE]
>
> De volgende kernconcepten zijn ook op om het even welk multi-kanaalvolgen van toepassing dat campagnes impliceert die niet in Adobe Advertising worden gevolgd, zoals [`campaign` &#x200B;](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html?lang=nl-NL) variabele (die ook als &quot;het Volgen code&quot;dimensie of &quot;[!DNL eVar] 0&quot;wordt bekend) en douane [!DNL eVar] het volgen.

### Mogelijke verschillen in attributiemodellen in [!DNL Marketing Channels]

De meeste [!DNL Marketing Channels] -rapporten zijn geconfigureerd met [!UICONTROL Last Touch] -attributie, waaraan het laatst gedetecteerde marketingkanaal 100% van de conversiewaarde is toegewezen. Het gebruik van verschillende toewijzingsmodellen voor de rapporten en Adoben Advertising van [!DNL Marketing Channels] leidt tot discrepanties in toegewezen conversies.

### Een potentieel verschillend Lookback Venster in [!DNL Marketing Channels]

Het terugzoekvenster voor [!DNL Marketing Channels] kan worden aangepast. In Adobe Advertising, is het venster van de klikraadpleging configureerbaar, hoewel een vast venster van 60 dagen gemeenschappelijk is. Als de twee producten verschillende raadplegingsvensters gebruiken, kunt u gegevensdiscrepanties verwachten.

### Verschillende kanaalkenmerken in [!DNL Marketing Channels]

In Adobe Advertising-rapporten worden alleen betaalde media vastgelegd die via Adobe Advertising worden verhandeld (betaalde zoekopdracht naar [!DNL Advertising Search, Social, & Commerce] advertenties en weergave voor Advertising DSP-advertenties), terwijl in [!DNL Marketing Channels] alle digitale kanalen kunnen worden getraceerd. Dit kan tot een discrepantie in het kanaal leiden waarvoor een omzetting wordt toegeschreven.

Betaalde zoekopdrachten en natuurlijke zoekkanalen hebben bijvoorbeeld vaak een symbiotische relatie, waarbij elk kanaal het andere kanaal helpt. Het rapport [!DNL Marketing Channels] geeft bepaalde omzettingen aan een natuurlijke zoekopdracht die de Adobe Advertising niet volgt omdat deze geen natuurlijke zoekopdracht bijhoudt.

Neem bijvoorbeeld ook een klant die een advertentie weergeeft, op een betaalde zoekadvertentie klikt, in een e-mailbericht klikt en vervolgens een bestelling van 30 USD plaatst. Zelfs als Adobe Advertising en [!DNL Marketing Channels] beide het laatste aanraakattributiemodel gebruiken, wordt de conversie nog steeds anders toegewezen aan beide. Adobe Advertising heeft geen toegang tot het [!UICONTROL Email] -kanaal. Betaalde zoekopdracht naar de conversie wordt daarom naar behoren uitgevoerd. [!DNL Marketing Channels] heeft echter toegang tot alle drie kanalen, zodat [!UICONTROL Email] wordt gecrediteerd voor de conversie.

![&#x200B; Voorbeeld van verschillende omzettingsattributie in Adobe Advertising tegenover [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Voor meer verklaring van waarom de metriek kan variëren, zie &quot;[&#x200B; waarom de Gegevens van het Kanaal tussen Adobe Advertising en  [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md) kunnen variëren.&quot;

## Gegevensverschillen in Adobe Analytics [!DNL Paid Search Detection]

De [&#x200B; erfenis  [!DNL Paid Search Detection] &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html?lang=nl-NL) eigenschap in [!DNL Analytics] staat bedrijven toe [&#x200B; regels te bepalen om betaald en biologisch onderzoeksverkeer &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html?lang=nl-NL) voor gespecificeerde onderzoeksmotoren te volgen. De [!DNL Paid Search Detection] regels gebruiken zowel een vraagkoord als het verwijzende domein om betaald en natuurlijk onderzoeksverkeer te identificeren. De [!DNL Paid Search Detection] rapporten maken deel uit van de grotere groep van [&#x200B; het Vinden Methoden &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html?lang=nl-NL) rapporten, die of verlopen wanneer een gespecificeerde gebeurtenis (zoals een Controle van het Kunst) voorkomt of het bezoek beëindigt.

Hieronder ziet u de interface voor het maken van een [!DNL Paid Search Detection] -regelset:

![&#x200B; Voorbeeld van een Paid die regel van de Detectie van het Onderzoek in [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png) wordt geplaatst

De resulterende [!DNL Paid Search Detection] -rapporten bevatten de [!UICONTROL Paid Search Engine] , [!UICONTROL Paid Search Keywords] , [!UICONTROL Natural Search Engine] en [!UICONTROL Natural Search Keywords] -rapporten.

Houd rekening met de volgende twee beperkingen met gegevens in [!DNL Paid Search Detection] -rapporten:

* In de rapporten [!UICONTROL Paid Search Keywords] en [!UICONTROL Natural Search Keywords] worden de zoekquery&#39;s weergegeven die worden geïdentificeerd door de verwijzende URL&#39;s, niet de trefwoorden waarop gebruikers bieden. In Adobe Advertising- en [!DNL Analytics] -rapporten worden de werkelijke trefwoorden weergegeven. Zorg er dus niet voor dat deze uitlijnen met de trefwoordrapporten van [!DNL Paid Search Detection] .

* Toen de functie [!DNL Paid Search Detection] oorspronkelijk werd gemaakt, was de oorspronkelijke zoekquery (de tekenreeks die de gebruiker in de zoekbalk in het zoekprogramma had ingevoerd) gemakkelijker beschikbaar voor adverteerders via de verwijzende URL. Tegenwoordig vervagen zoekprogramma&#39;s de zoekquery grotendeels en zijn de trefwoordrapporten van [!DNL Paid Search Detection] van beperkte waarde omdat de meeste querygegevens onder &quot;niet opgegeven&quot; vallen.

  Met [!DNL Analytics for Advertising] kunnen adverteerders betaalde trefwoorden nog steeds bijhouden in [!DNL Analytics] . Het verwijzende domein informeert de motorrapporten die de onderzoeksmotor het verkeer drijven. Aangezien de accountgegevens die specifiek zijn voor de adverteerder niet aan het verwijzende domein zijn gekoppeld, wordt al het verkeer weergegeven onder de zoekfunctie. Adverteerders met meerdere accounts in hetzelfde zoekprogramma moeten naar Adobe Advertising of [!DNL Analytics] rapportage voor accountspecifieke rapportage verwijzen.

### Waarom [!DNL Paid Search Detection] configureren?

De [!DNL Paid Search Detection] rapporten staan u toe om natuurlijk onderzoeksverkeer in de [[!DNL Analytics Marketing Channels]  rapporten &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html?lang=nl-NL) te identificeren. Het scheiden van betaald onderzoeksverkeer tegenover natuurlijk onderzoeksverkeer is een grote manier om de waarde te begrijpen die de natuurlijke opsporing aan het volledige marketing ecosysteem brengt.

## Doorklikgegevens valideren voor [!DNL Analytics for Advertising] {#data-validation}

Voor uw integratie moet u uw doorklikgegevens valideren om ervoor te zorgen dat alle pagina&#39;s op uw site de doorklikbewerkingen correct bijhouden.

In [!DNL Analytics] is een van de eenvoudigste manieren om [!DNL Analytics for Advertising] tracking te valideren het vergelijken van instanties met klikken met behulp van de berekende metrische waarde &#39;AMO ID Instances to Clicks&#39;, die als volgt wordt berekend:

```
AMO ID Instances to Clicks = ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

[!UICONTROL AMO ID Instances] vertegenwoordigt het aantal tijden dat [&#x200B; AMO IDs &#x200B;](ids.md) op de plaats wordt gevolgd. Telkens wanneer op een advertentie wordt geklikt, wordt een parameter van AMO ID (`s_kwcid`) toegevoegd aan de bestemmingspagina URL. Het aantal [!UICONTROL AMO ID Instances] is daarom gelijk aan het aantal klikken en kan worden gevalideerd tegen klikken en neerzetten. Doorgaans ziet u een 85% overeenkomende frequentie voor [!DNL Search, Social, & Commerce] en een 30% overeenkomende frequentie voor [!DNL DSP] -verkeer (wanneer gefilterd om alleen doorklikken [!UICONTROL AMO ID Instances] op te nemen). Het verschil in verwachtingen tussen onderzoek en vertoning kan door het verwachte verkeersgedrag worden verklaard. Zoekopdracht legt de intentie vast en daarom zijn gebruikers gewoonlijk van plan om op de zoekresultaten van hun zoekopdracht te klikken. Gebruikers die een weergave- of onlinevideo zien, zullen echter vaker onbedoeld op de advertentie klikken en dan van de site naar de site stuiteren of het nieuwe venster dat wordt geladen verlaten voordat de paginageactiviteit wordt bijgehouden.

In rapporten van de Adobe Advertising, kunt u instanties vergelijken om te klikken gebruikend metrisch &quot;[!UICONTROL EF ID Instances]&quot;in plaats van [!UICONTROL AMO ID Instances]:

```
EF ID Instances to Clicks = ([!UICONTROL EF ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

Verwacht weliswaar dat de AMO-id en de EF-id een hoge equivalentie hebben, maar verwacht niet dat deze gelijk zijn aan 100%, omdat de AMO-id en de EF-id fundamenteel verschillende gegevens bijhouden. Dit verschil kan leiden tot kleine verschillen in het totaal [!UICONTROL AMO ID Instances] en [!UICONTROL EF ID Instances] . Als het totaal [!UICONTROL AMO ID Instances] in [!DNL Analytics] meer dan 1% verschilt van [!UICONTROL EF ID Instances] Adobe Advertising, neemt u contact op met het accountteam van de Adobe voor hulp.

Voor meer informatie over AMO identiteitskaart en EF identiteitskaart, zie [&#x200B; Adobe Advertising IDs die door Analytics &#x200B;](ids.md) wordt gebruikt.

<!--  Need to create a new report to show tracking instances to clicks, instead of clicks to instances as shown, and replace this screenshot.

The following is an example of a workspace to track clicks to instances.

![Example of a workspace to track clicks to instances to clicks](/help/integrations/assets/a4adc-clicks-to-instances-example.png)
-->

### Problemen oplossen met verschillen tussen klikken en instanties

Als de verhouding tussen [!UICONTROL EF ID Instances] en klikken lager is dan 85%, controleert u het volgende:

* Ontbreekt u klik het volgen voor de rekening of op om het even welk subniveau, of hebt u dubbele klik het volgen (bijvoorbeeld, op zowel de rekening als campagnemaniveaus)?

  In Onderzoek, Sociaal, &amp; Commerce, [&#x200B; download een bulksheet &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) voor de rekening om het volgen URLs te controleren.

  In [!DNL Analytics] kunt u ook zien of de AMO-id en EF IF consistent worden toegevoegd met de berekende metrische waarde &quot;[!DNL AMO ID] to [!DNL EF ID]&quot;. Deze wordt als volgt berekend:

  ```
  [!DNL AMO ID] to [!DNL EF ID] = ([!UICONTROL AMO ID] / [!DNL EF ID])
  ```

  Een waarde groter dan 100% geeft aan dat er meer EF-id&#39;s ontbreken dan AMO-id&#39;s.

* Heeft de landingspagina een laadprobleem, zodat de AMO-id en EF-id niet worden vastgelegd?

* Is de URL van de bestemmingspagina omgeleid zodat de AMO-id en EF-id verloren gaan?

* Gebruiken alle bestemmingspagina&#39;s de gevormde rapportreeks?

>[!NOTE]
>
>In theorie is het mogelijk dat één instantie meerdere klikken heeft. Controleer of er op verschillende apparaten (zoals bureaublad, mobiel en tablet) is geklikt.

## Gegevenssets vergelijken in [!DNL Analytics for Advertising] versus in Adobe Advertising

[&#x200B; identiteitskaart van AMO &#x200B;](ids.md) (s_kwcid parameter van het vraagkoord) wordt gebruikt voor het melden in [!DNL Analytics], en [&#x200B; EF identiteitskaart &#x200B;](ids.md) (ef_id parameter van het vraagkoord) wordt gebruikt voor het melden in Adobe Advertising. Omdat het verschillende waarden zijn, is het mogelijk dat één waarde is beschadigd of niet is toegevoegd aan de landingspagina.

Stel dat we de volgende bestemmingspagina hebben:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

waar EF identiteitskaart &quot;`test_ef_id`&quot;is en AMO identiteitskaart &quot;`test_amo_id` is.&quot;

Als een omleiding van de site plaatsvindt, kan de URL er als volgt uitzien:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

waar EF identiteitskaart &quot;`test_ef_id`&quot;is en AMO identiteitskaart &quot;`test_amo_id#redirectAnchorTag` is.&quot;

In dit voorbeeld worden door het toevoegen van de ankertag onverwachte tekens aan de AMO-id toegevoegd. Dit leidt tot een waarde die Analytics niet herkent. Deze AMO-id zou niet geclassificeerd worden en conversies die eraan gekoppeld zijn, vallen onder &quot;[!UICONTROL unspecified]&quot; of &quot;[!UICONTROL none]&quot; in [!DNL Analytics] -rapporten.

Gelukkig, terwijl de kwesties als dit gemeenschappelijk zijn, resulteren zij typisch niet in een hoog percentage van discrepantie. Als u echter een grote discrepantie tussen AMO-id&#39;s in [!DNL Analytics] en EF-id&#39;s in de Adobe Advertising opmerkt, neemt u contact op met het accountteam van de Adobe voor hulp.

## Andere metrische overwegingen

### Het verschil tussen klikken en bezoeken {#clicks-vs-visits}

Ze lijken op elkaar, maar klikken en bezoeken geven verschillende gegevens weer:

* **klik:** [!DNL DSP] of de onderzoeksmotor registreert een klik wanneer een bezoeker een advertentie op de website van een uitgever klikt.

* **Bezoek:** [!DNL Analytics] bepaalt a [&#x200B; bezoek &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=nl-NL) als reeks paginameningen door een gebruiker, die volgens één van verscheidene criteria, zoals 30 minuten van inactiviteit beëindigt.

Een klik kan per definitie leiden tot meerdere bezoeken.

Bekijk het volgende voorbeeld: gebruiker 1 en gebruiker 2 hebben beide toegang tot een site door op een advertentie voor een Adobe Advertising te klikken. Gebruiker 1 geeft vier pagina&#39;s weer en verlaat vervolgens de dag, zodat de eerste klik resulteert in één bezoek. Gebruiker 2 geeft twee pagina&#39;s weer, verlaat voor een lunch van 45 minuten, retourneert, bekijkt nog twee pagina&#39;s en verlaat vervolgens. In dit geval leidt de eerste klik tot twee bezoeken.

![&#x200B; Voorbeeld van het verschil tussen kliks en bezoeken &#x200B;](/help/integrations/assets/a4adc-visits-example.png)

### Het verschil tussen klikken en klik-door

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Klik en klik-door zijn twee verschillende metriek:

* **klik:** [!DNL DSP] of de onderzoeksmotor registreert een klik wanneer een bezoeker een advertentie op de website van een uitgever klikt.

* **klik-door:** [!DNL Analytics] registreert een klik-door wanneer de bezoeker op de bestemmingswebsite, de het landen pagina laadt, en het [!DNL Analytics] verzoek bij de bodem van de pagina verzendt de gegevens naar [!DNL Analytics].

Klikken en doorklikken kunnen sterk verschillen als gevolg van een ongeluk en klikken. We hebben gezien dat de meeste klikken op weergaveadvertenties per ongeluk gebeuren. Deze bezoekers raakten op de knop Terug voordat de landingspagina wordt geladen, zodat [!DNL Analytics] geen doorklikgegevens kan opnemen. Dit geldt met name voor advertenties waarin een onbedoelde klik waarschijnlijker is, zoals mobiele advertenties, videobanden en advertenties die het scherm vullen en moeten worden gesloten voordat de gebruiker de pagina kan bekijken.

Sites die op mobiele apparaten worden geladen, zullen ook minder vaak een doorklik tot gevolg hebben vanwege een lagere bandbreedte of een lagere verwerkingscapaciteit, waardoor het langer duurt om bestemmingspagina&#39;s te laden. Het is niet ongebruikelijk voor 50-70% van kliks om niet in klikproductie te resulteren. In mobiele omgevingen kan het verschil oplopen tot 90% vanwege de combinatie van een langzamere browser en de hogere kans dat de gebruiker per ongeluk op de advertentie klikt terwijl de pagina wordt doorgeschoven of de advertentie wordt gesloten.

De klikgegevens kunnen ook worden geregistreerd in milieu&#39;s die klikdoorgangen met de huidige volgende mechanismen (zoals kliks die naar, of van, een mobiele app) gaan niet kunnen registreren of waarvoor de adverteerder slechts één het volgen benadering (bijvoorbeeld, met de mening-door benadering van JavaScript, browsers die derdekoekjes houden klikken, maar niet klikken-door) opstelde. Een zeer belangrijke reden dat de Adobe aanbeveelt zowel de klik URL het volgen als mening-door JavaScript het volgen benaderingen op te stellen is dekking van trackable klikthrough te maximaliseren.

### Het gebruiken van de Metriek van het Verkeer van de Adobe Advertising voor Dimensionen niet van de Adobe Advertising

De Adobe Advertising verstrekt Analytics met [&#x200B; reclame-specifieke verkeersmetriek en de verwante dimensies van  [!DNL DSP]  en  [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). De door de Adobe Advertising opgegeven meetgegevens zijn alleen van toepassing op de opgegeven Adobe Advertising en de gegevens zijn niet beschikbaar voor andere dimensies in [!DNL Analytics] .

Als u bijvoorbeeld de waarden [!UICONTROL Adobe Advertising Clicks] en [!UICONTROL Adobe Advertising Cost] per account bekijkt (dit is een Adobe Advertising-dimensie), worden het totaal [!UICONTROL Adobe Advertising Clicks] en [!UICONTROL Adobe Advertising Cost] per account weergegeven.

![&#x200B; Voorbeeld van metriek van de Adobe Advertising in een rapport gebruikend een dimensie van de Adobe Advertising &#x200B;](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Als u echter de metriek [!UICONTROL Adobe Advertising Clicks] en [!UICONTROL Adobe Advertising Cost] op paginagrootte (zoals Pagina) bekijkt, waarvoor Adobe Advertising geen gegevens levert, zijn de [!UICONTROL Adobe Advertising Clicks] en [!UICONTROL Adobe Advertising Cost] voor elke pagina nul (0).

![&#x200B; Voorbeeld van metriek van de Adobe Advertising in een rapport gebruikend een niet gestaafde afmeting &#x200B;](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### [!UICONTROL AMO ID Instances] gebruiken als vervanging voor klikken met Dimensionen zonder Adobe Advertising

Omdat u [!UICONTROL AMO Clicks] niet kunt gebruiken met onsite afmetingen, is het verstandig om een equivalent te zoeken voor klikken. Mogelijk bent u geneigd Visit te gebruiken als een vervanging, maar dit is niet de beste optie, omdat elke bezoeker meerdere bezoeken kan hebben. (Zie &quot;[&#x200B; het Verschil tussen Klik en Bezoek &#x200B;](#clicks-vs-visits).&quot; In plaats daarvan raden we u aan [!UICONTROL AMO ID Instances] te gebruiken. Dit is het aantal keren dat de AMO-id wordt vastgelegd. Hoewel [!UICONTROL AMO ID Instances] niet [!UICONTROL AMO Clicks] exact overeenkomen, zijn ze de beste optie voor het meten van het klikken op de site. Voor meer informatie, zie &quot;[&#x200B; Klik-door de Bevestiging van Gegevens voor  [!DNL Analytics for Advertising]](#data-validation).&quot;

![&#x200B; Voorbeeld van [!UICONTROL AMO ID Instances] in plaats van [!UICONTROL Adobe Advertising Clicks] voor een niet gestaafde afmeting &#x200B;](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [&#x200B; Overzicht van  [!DNL Analytics for Advertising]](overview.md)
>* [&#x200B; Adobe Advertising IDs die door  [!DNL Analytics]](/help/integrations/analytics/ids.md) wordt gebruikt
>* [&#x200B; Metriek van de Adobe Advertising in Analysis Workspace &#x200B;](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics]  Gegevens in Adobe Advertising &#x200B;](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [&#x200B; waarom de Gegevens tussen Adobe Advertising en  [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md) kunnen variëren
