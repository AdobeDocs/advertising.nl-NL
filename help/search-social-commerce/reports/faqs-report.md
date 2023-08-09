---
title: Veelgestelde vragen over aangepaste rapporten
description: Leer antwoorden op veelgestelde vragen over prestatiesrapporten, met inbegrip van het oplossen van problemen van gegevenskwesties.
exl-id: 85707666-7c0f-4aa3-8c91-fb73ef6a5061
feature: Search Reports
source-git-commit: 2903bf783969b3e2d59c0933629cbb170c0a314c
workflow-type: tm+mt
source-wordcount: '3912'
ht-degree: 0%

---

# Veelgestelde vragen over aangepaste rapporten

## Algemene vragen

+++Wat als de datumwaaier voor het rapport begint alvorens rapportgegevens beschikbaar is?
Het rapport wordt gegenereerd, maar bevat alleen gegevens voor de datums waarvoor gegevens beschikbaar zijn. Voor meer informatie over wanneer de gegevens voor elk rapporttype beschikbaar zijn, zie &quot;[De gegevens die voor rapporten worden gebruikt](data-used-for-reports.md).&quot;
+++

+++Wat is het verschil tussen klik datum en transactie op datum-gebaseerde rapporten?
Wanneer u omzettingen per transactiedatum rapporteert, omvatten de gegevens transacties waarvan de transactiedatum tijdens de opgegeven tijdsperiode is opgetreden. Deze optie is het gebrek dat in basisrapporten en geavanceerde rapporten plaatst, en het toont u hoeveel opbrengst binnen de gespecificeerde tijdspanne werd verdiend.

Wanneer u omzettingen door klikdatum rapporteert, omvatten de gegevens transacties die uit een klik voortvloeiden die tijdens de gespecificeerde tijdspanne voorkwam. Wanneer een portefeuille significante vertragingen tussen kliks en transacties heeft, toont dit type van rapportering de historische opbrengst per klik voor de portefeuille, die u een idee geeft van welk opbrengstgedrag in tijd te verwachten.

![Rapport op klikdatum versus rapport op transactiedatum](/help/search-social-commerce/assets/click-date-vs-txn-date.png "Rapport op klikdatum versus rapport op transactiedatum")
+++

+++Wat gebeurt als ik het venster van de klikraadpleging of het venster van de imitatieraadpleging verander?
(Adverteerders met alleen de service Pixels-based conversion Tracking voor advertenties) Gegevens voor gebeurtenissen die het resultaat zijn van de eerste klik worden gedurende een langere of kortere periode verzameld.

Een adverteerder [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j) bepaalt het aantal dagen nadat een betaalde klik of een vertoningsindruk (respectievelijk) voorkomt waarin de gebeurtenis aan een omzetting kan worden toegeschreven. Het kan belangrijk zijn om een waarde te wijzigen in een langere of kortere periode voor adverteerders met bijzonder korte of lange &#39;click-to-Revenue&#39;-periodes of &#39;shadow-to-Revenue&#39;-perioden.

**Beste praktijken:** Zorg ervoor dat de terugkijkvensters langer zijn dan de klik-aan-opbrengst en vertoning beeld-aan-opbrengst tijden voor de meeste van uw sleutelwoorden of advertenties. Wanneer zij korter zijn, worden sommige omzettingen niet geassocieerd met de aanvankelijke klik of de indruk.
+++

+++Hoe weet ik welke omzettingen het resultaat zijn van een [!DNL Google Ads] extensie of productlijst toevoegen?
U kunt zien welke omzettingen het resultaat zijn van een klik op een [!DNL Google Ads] toevoegen (in plaats van op de advertentie zelf) of op een productlijst door een [!UICONTROL Transaction Report]. De [!UICONTROL Link Type] de kolomwaarde toont het type en de titel van een verbinding die werd geklikt:

* Objecten worden aangeboden als `pla:<product ID>`, zoals `pla:8525822`.

* Sitelinks worden weergegeven als `sl:<Sitelink text>`, zoals `sl:See Current Offers`.

  U kunt ook een sitelink identificeren als u de optie [!UICONTROL Tracking URL] in het rapport. De [!UICONTROL Tracking URL] voor een sitelink bevat het kenmerk `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>Conversies van [!DNL Google Ads] locaties en telefoonextensies worden opgenomen in de gegevens voor de advertenties die ze vergezellen . Ze worden niet afzonderlijk gerapporteerd.

+++

+++De &quot;[!UICONTROL Keyword]&quot; de kolom in mijn rapport bevat de waarde &quot;(adgroup content) &lt;*naam van groep*>.&quot;
Wanneer de rij gegevens bevat voor zoekcampagnes waarvoor inhoud is ingeschakeld, weergavecampagnes of sociale campagnes — die geen trefwoorden bevatten — wordt de rij [!UICONTROL Keyword] in plaats daarvan wordt de toepasselijke naam van de advertentiegroep weergegeven.
+++

+++Vanwege seizoensgebonden of marktveranderingen worden in mijn rapporten atypische gegevens weergegeven. Zal dit gevolgen hebben voor biedingen als de omstandigheden veranderen?
De optimaliseringscapaciteit bouwt zijn opbrengstmodellen voor elke biedingseenheid dagelijks om ervoor te zorgen dat het identificeert en onmiddellijk op trends reageert, en de modellen omvatten historische gegevens op lange termijn om seizoensgebonden prestaties te helpen voorspellen. De halfwaardetijd van het inkomstenmodel van de portefeuille<!-- add link to glossary? --> bepaalt ook hoe zwaar recente inkomstengegevens worden gewogen. De beste praktijk is om de halfwaardetijd tijdens een periode van atypische prestaties te verminderen maar te verhogen nadat het inkomstenmodel is aangepast. Als u vragen hebt over of het aanpassen van de halfwaardetijd noodzakelijk is, contacteer uw Team van de Rekening van de Adobe.

Als u niet wilt dat de gegevens voor de periode toekomstige biedingen beïnvloeden, dan kunt u verkiezen om die datums van het model uit te sluiten. Neem contact op met het accountteam van uw Adobe om de datums uit te sluiten.
+++

+++Kan ik een rapport maken over een specifieke accounteigenschap, zoals [!UICONTROL Device] of [!UICONTROL Objective Name]?
Voor verslagen van campagneentiteiten ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], en [!UICONTROL Product Group Report]), worden de metriekgegevens dynamisch samengevoegd door de bezitskolommen u in het rapport omvat. U kunt naar keuze de belangrijkste kolom voor het rapport verwijderen en slechts de bezitskolommen omvatten waarvoor u gegevens wilt samenvoegen.

Als u bijvoorbeeld een [!UICONTROL Keyword Report] die de [!UICONTROL Ad Group] en  De kolommen van het apparaat, dan, door gebrek, aggregeert het rapport metriek voor elk sleutelwoord door ad groep en apparatentype. Als u echter de [!UICONTROL Keyword] kolom alvorens u het rapport produceert, dan produceert het rapport dynamisch metriek voor de gespecificeerde ad groepen door apparatentype.

>[!NOTE]
>
>U kunt deze functie niet gebruiken om gegevens te aggregeren op basis van labelclassificaties. Alle kolommen met labelclassificatie in het rapport worden weggelaten. Gebruik in plaats daarvan de opdracht [Rapport voor labelclassificatie](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## Algemene gegevenskwesties

+++Rapporten die worden gegenereerd met verschillende toewijzingsregels geven verschillende totalen weer.
Als u een rapport veelvoudige tijden gebruikend de zelfde rapportparameters maar met verschillende attributenregels produceert, dan kunnen de gegevens om één van beide volgende redenen verschillen:

* Klik op datumgegevens als deze buiten het opgegeven datumbereik vallen.

  Als u de rapportparameter &quot;[!UICONTROL Conversions based on click date],&quot; is het opgegeven datumbereik van toepassing op de datum van de klik in plaats van op de datum van de transactie. Als in het rapport ook de toewijzingsregel &quot;Eerste gebeurtenis&quot; of &quot;Laatste gebeurtenis&quot; wordt gebruikt, kan de eerste of laatste gebeurtenis die tot de conversie heeft geleid, zich buiten het opgegeven datumbereik bevinden. Bijvoorbeeld, veronderstel dat een gebruiker Keyword_1 op 30 April klikte, Keyword_2 op 20 Mei klikte, en op 21 Mei omgezet. Als in het rapport de waarde &quot;[!UICONTROL First Event]&quot;- attributieregel en een datumbereik van 1-21 mei, dan wordt de eerste gebeurtenis (een klik op Keyword_1 op 30 april) niet in het rapport opgenomen. Als u het rapport uitvoert met hetzelfde datumbereik maar de waarde &quot;[!UICONTROL Last Event]&quot;- toewijzingsregel, dan wordt de conversie opgenomen in het rapport omdat de laatste klik binnen het opgegeven datumbereik heeft plaatsgevonden.

* Bij de selectie van het portfoliofilter worden enkele gebeurtenissen die tot de conversie leiden, uitgesloten.

  Als u een subset van portfolio&#39;s rapporteert, hoeft u mogelijk geen campagnes op te nemen die de gebeurtenis bevatten waaraan de conversie is toegewezen op basis van een van de toewijzingsregels. Bijvoorbeeld, veronderstel een gebruiker Keyword_1 van Portfolio_1 klikt, Keyword_2 van Portfolio_2 klikt, en dan omzet. Als in het rapport de waarde &quot;[!UICONTROL First Event]&quot;- toewijzingsregel, dan moet Portfolio_1 worden opgenomen om de conversie in het rapport op te nemen. Als het rapport echter de toewijzingsregel &quot;Laatste gebeurtenis&quot; gebruikt, moet Portfolio_2 worden opgenomen.

>[!TIP]
>
>Als u omzettingstotalen onder verschillende attribuutregels wilt vergelijken, dan looppas rapporten gebruikend de rapportparameter &quot;[!UICONTROL Conversions based on transaction date]&quot; en selecteert u alle advertentienetwerken of alle portfolio&#39;s. Als u geen andere filters instelt, moeten de totalen van de omzetting overeenkomen.

+++

+++Afzonderlijke gegevensvelden zijn onjuist, hoewel de totalen juist zijn.
Deze situatie kan zich voordoen wanneer de metrische formaten gehelen gebruiken:

* Als u een [aangepaste metrisch](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) met de notatie *Aantal decimalen met/uit* (waarin gegevens als gehele getallen worden weergegeven) en deze opnemen in een weergave of rapport waarin een gewogen toewijzingsregel voor conversie wordt gebruikt ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], of [!UICONTROL Even Distribution]), wordt de uitvoer weergegeven in gehele getallen, niet in decimalen. In dit geval zijn afzonderlijke gegevensvelden mogelijk onjuist, hoewel de totalen juist zijn. Als een volgorde bijvoorbeeld gelijk is verdeeld tussen drie gebeurtenissen, wordt één volgorde (in plaats van 0,33 volgorde) toegewezen aan elk van de drie gebeurtenissen. Om het probleem op te lossen, [de metrische indeling wijzigen](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) tot *Getal tot 2 decimale punten*.

* Op dezelfde manier als u opbrengst metrisch hebt die zoals in geheel wordt verzonden, dan komt de zelfde kwestie voor. (Het inkomstenformaat wordt gecontroleerd door de omzettingsmarkering die de gegevens indient.) Om het probleem op te lossen, [een aangepaste metrische waarde maken](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) uitsluitend bestaande uit de maatstaf van de ontvangsten en met het formaat *Getal tot 2 decimale punten*en neemt u deze op in weergaven en rapporten in plaats van de oorspronkelijke metrische waarde.
+++

+++Wanneer klik of de opbrengstgegevens ontbreken, hoe ik het verhinderen toekomstige biedingen te beïnvloeden?
Klik op gegevensproblemen als Zoeken, Sociaal en Handel niet synchroon is met het advertentienetwerk. Neem contact op met het accountteam van uw Adobe om de account handmatig te synchroniseren. Als klikgegevens een hele dag ontbreken, dan vraag uw Team van de Rekening van de Adobe om die dag van de kostenmodellen uit te sluiten.

Problemen met inkomstengegevens kunnen optreden als gevolg van een probleem met het bijhouden of doorvoeren van een bestand. Neem contact op met uw accountteam van Adobe om het probleem te onderzoeken. Als de opbrengstgegevens voor een volledige dag ontbreken, dan vraag uw Team van de Rekening van de Adobe om die dag van de opbrengstmodellen uit te sluiten.
+++

+++Monetaire gegevens worden in het verkeerde formaat weergegeven.
Standaard worden alle monetaire gegevens in rapporten weergegeven in de notatie voor Amerikaanse dollars (zoals 1.000,00). Als u de waarde wilt weergeven in de juiste valutanotatie (maar zonder valutasymbolen in CSV- en TSV-notaties), voegt u &quot;[!UICONTROL Currency]&quot;. Als het rapport gegevens bevat voor rekeningen met verschillende valuta&#39;s, dan kan &quot;[!UICONTROL Total]&quot; monetaire waarden zijn gewoon de som van alle getallen in de kolom, ongeacht de valuta.
+++

+++Waarom zie ik decimale waarden voor omzettings metrisch die een natuurlijk aantal (1, 2, etc.) zouden moeten zijn?
In de volgende gevallen kunt u decimale waarden zien:

* Als u het rapport met een andere parameter van de omzettingsattributieregel dan [!UICONTROL Last Event] of [!UICONTROL First Event]Vervolgens kunnen de inkomsten worden opgesplitst tussen meerdere gebeurtenissen in het conversiepad.

* In de [!UICONTROL Transaction Report], indien meerdere [biedingseenheden](/help/search-social-commerce/glossary.md#a-b) met verschillende overeenkomende typen dezelfde transactie-id hebben, worden de inkomsten voor de volgende id gesplitst volgens het aantal klikken op de opgegeven klikdatum.
+++

## Standaardprestatiewaarden

+++Klik gegevens ontbreken in rapporten.
Dit zijn algemene redenen voor het ontbreken van klikgegevens.

| Oorzaak | Detectie/analyse | Resolutie |
|---|---|---|
| Het proces dat klikgegevens van de advertentierekening terugwint ontbrak. | Er is geen systematische manier om dit probleem op te sporen, maar u kunt zien dat een campagne geen kosten toont of op informatie klikt, ook al heeft de advertentierekening geld uitgegeven. | Neem contact op met het accountteam van uw Adobe.<br><br>Als de gegevens meer dan 24 uur ontbreken, worden deze data van de kostenprognoses uitgesloten totdat de gegevens worden opgehaald. Uw Adobe-accountteam kan de datums uitsluiten. |
| Een factureringsprobleem tussen de adverteerder en het advertentienetwerk voorkomt dat de advertentierekening uitgaven. | Er is geen systematische manier om dit probleem op te sporen, maar u kunt zien dat een campagne geen kosten toont of op informatie klikt. | Als u weet dat een advertentierekening niet kon uitgeven wegens een factureringskwestie, dan sluit die data van de kostenramingen uit. Uw Adobe-accountteam kan de datums uitsluiten. |
+++

+++Prestatiegegevens zijn verschillend van gegevens in de ad netwerkredacteur.
Wanneer het advertentienetwerk updates naar vorige gegevens verzendt (vaak omdat zij klikfraude aan sommige kliks hebben toegeschreven), werkt het Onderzoek, Sociale, &amp; Handel niet de gegevens bij tenzij er meer dan een 5% discrepantie is en het Team van de Rekening van Adobe een verzoek indient.

Wanneer u de indruk vergelijkt die gegevens deelt die over een datumbereik zijn samengevoegd, kunnen de gegevens die in de rapporten Zoeken, Sociale Zaken en Handel worden vermeld, afwijken van de gegevens die in het advertentienetwerk worden gerapporteerd. Dit verschil is omdat de gegevens door API van het advertentienetwerk worden gemeld, die Onderzoek, Sociale, &amp; Handel gebruikt om gegevens in te trekken. Bijvoorbeeld: [!DNL Google Ads] gegevens:

* Voor het grootste deel van de indruk delen metriek, [!DNL Google Ads] Hiermee wordt het lage of het hoge uiteinde van de waarden aangegeven voor waarden die kleiner zijn dan 10% of groter dan 90%. Gegevens worden gerapporteerd als 0,0999 voor &lt;10% en 0,9001 voor >90%

* Als er een combinatie is van geplafonneerde en niet-geplafonneerde gegevens binnen het datumbereik, worden bij de imitatie bij Zoeken, Sociaal en Handel gegevens gedeeld met de waarden die ongewijzigd in de API worden verzonden. Bij rijen met &lt; 10% en 0,9001 bij rijen met >90% wordt 0,0999 gebruikt. Deze aggregatie kan resulteren in een afwijking van de [!DNL Google Ads] vooraf geaggregeerde gegevens omdat [!DNL Google Ads] U kunt werkelijke percentagewaarden gebruiken, zoals 7% of 97%.
+++

+++Prestatiegegevens in rapporten zijn anders dan gegevens in [!DNL Google Analytics].
De twee systemen meten verschillende gegevens, zodat zou u moeten verwachten om verschillende gegevens te zien. Bijvoorbeeld:

* Met Zoeken, Sociaal en Handel (en Google Ads) kunt u klikken, terwijl [!DNL Google Analytics] controleert bezoeken per 30 minieme browser zitting. Als een gebruiker bijvoorbeeld eenmaal op uw advertentie klikt, vervolgens op de knop Terug klikt en vervolgens opnieuw op de advertentie klikt, wordt met Zoeken, Sociale en Handel twee keer geklikt, maar [!DNL Google Analytics] registreert één bezoek.

* [!DNL Google Analytics] toont alle verkeersgegevens, terwijl Zoeken, Sociaal, &amp; Handel (en [!DNL Google Ads]) ongeldige kliks (zoals bovenmatige, herhaalde klikken).

* [!DNL Google Analytics] bevat klikgegevens en inkomstengegevens voor alle klikken. Met Zoeken, Sociaal en Handel kunt u geen klik- en inkomstengegevens bijhouden voor advertenties en trefwoorden met onjuiste of ontbrekende URL&#39;s.
+++

## Omzettingsmetriek

+++Mijn rapport toont geen omzettingsgegevens.
Het rapport bevat mogelijk geen conversiemetriek waarvoor conversies hebben plaatsgevonden.
+++

+++Opbrengst ontbreekt in rapporten.

**Adverteerders die conversietags voor Adoben Advertising gebruiken**

*Mogelijke oorzaken:*

* Trefwoorden of advertenties zijn toegevoegd zonder het voorvoegsel voor het bijhouden van de klik op Zoeken, Sociaal en Handel vooraf in te stellen op de trackingsjablonen of doel-URL&#39;s, of het voorvoegsel voor bijhouden is onjuist.

* De tag voor het bijhouden van conversies wordt niet correct geïmplementeerd op alle toepasselijke webpagina&#39;s of is bewerkt.

* De omzettingsmetriek die Onderzoek, Sociale, &amp; Handel volgen zijn uitgesloten van rapporten en daarom niet zichtbaar.

* De inkomstenparser voor de cliënt werd niet uitgevoerd.

*Mogelijke oplossing of oplossing:*

1. Controleer of de juiste kolommen zijn opgenomen in de rapporten- of gegevensweergaven. Als de correcte kolommen niet beschikbaar zijn om toe te voegen, dan moet u of uw Team van de Rekening van Adobe [de conversiemetriek beschikbaar stellen voor rapporten](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Controleer of de juiste codes voor het bijhouden van conversies zijn geïmplementeerd op alle toepasselijke webpagina&#39;s. Vraag zo nodig uw accountteam van Adobe om een testtransactie te maken voor elke toepasselijke conversietag en om de gegevens van de transactie vast te leggen, zoals de `transactionid` en gegevens uit de cookie (zoals de `trackingid`, `clickid`, enzovoort).

1. Als de [!UICONTROL Auto Upload] Deze optie is uitgeschakeld voor de campagne en u hebt trefwoorden of advertenties toegevoegd. Zorg er vervolgens voor dat u een trackingsjabloon of een doel-URL hebt gegenereerd die Zoeken, Sociale en Koophandel bevat en klik op Doorsturen voor elke sjabloon. Uw Adobe Account Team kan een intern rapport uitvoeren om te zien of klikken-volgende URLs (het volgen van malplaatjes of bestemmingsURLs) mist of misvormd.

   Indien nodig, genereert u tekstspatiëring door een bulksbladbestand met de juiste URL&#39;s te maken en het bestand naar de juiste account te posten met de opdracht **URL&#39;s voor bijhouden genereren** -optie.

   De doel-URL moet beginnen met &quot;http://pixel.everesttech.net&quot; of &quot;https://pixel.everesttech.net&quot;.

1. Als geen van deze stappen het probleem oplost, dan [Contact opnemen met de klantenservice](/help/search-social-commerce/get-help.md).

   Als de client niet is gestart of pas is gestart, controleert de klantenservice of er een inkomstenparser is ingesteld. Als de parser opstelling is, dan verifiëren zij als Onderzoek, Sociale, &amp; Handel om het even welke pixelomzettingen ontvangt en de kwestie problemen oplossen.

**Adverteerders die gegevens voor conversie verzenden**

*Mogelijke oorzaken:*

* Het voederbestand werd niet afgeleverd, het werd niet volledig geparseerd, of het voer bevatte transacties met wezen.

* De relevante omzettingsmetriek worden uitgesloten van rapporten en daarom niet zichtbaar.

>[!NOTE]
>
>De gegevens verschijnen over het algemeen niet in het gebruikersinterface tot 2-4 uur nadat het voer wordt ontvangen.

*Mogelijke oplossing of oplossing:*

1. Controleer of de juiste kolommen zijn opgenomen in de rapporten- of gegevensweergaven. Als de correcte kolommen niet beschikbaar zijn om toe te voegen, dan moet u of uw Team van de Rekening van Adobe [de conversiemetriek beschikbaar stellen voor rapporten](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Voer de [!UICONTROL Portfolio Report]. Als het leeg is, voert u de [!UICONTROL Campaign Report] en [!UICONTROL Search Engine Report] om na te gaan of de ontvangsten in deze verslagen voorkomen. Als dat het geval is, worden de campagnes mogelijk niet toegewezen aan de juiste portefeuille.

1. Controleer of het bestand naar de opbrengstserver is verzonden en of het bestand dezelfde indeling en naamgevingsconventie heeft gevolgd als vorige bestanden.

   Als de indeling of naamgevingsconventie voor bestanden is gewijzigd, corrigeert u het bestand en stuurt u het opnieuw.

1. Als het bestand is verzonden, [Contact opnemen met de klantenservice](/help/search-social-commerce/get-help.md).

   De klantenservice controleert of het bestand is ontvangen en geparseerd. Als het bestand zonder fouten is verwerkt, wordt gecontroleerd op verweesde transacties.
+++

+++Sommige geavanceerde rapporten bevatten geen omzettingsgegevens die door een adverteerdervoer worden verstrekt.
De [!UICONTROL Geo Distribution Report] en [!UICONTROL Domain Referral Report] gegevens te gebruiken die zijn vastgelegd via de service voor het bijhouden van Adoben Advertising en die alleen kunnen worden gegenereerd voor adverteerders met de service. De rapporten omvatten geen omzettingsgegevens die buiten het de omzettingsvolgsysteem van de Adobe Advertising worden gevolgd.
+++

+++inkomstengegevens verschillen van de eigen inkomstengegevens van de adverteerder.

**Adverteerders die conversietags voor Adoben Advertising gebruiken**

*Mogelijke oorzaken:*

* Bij zoeken, Sociale media en Handel worden inkomsten genegeerd wanneer de cookie verlopen of verwijderd is, maar de adverteerder kan dit als geldige inkomsten beschouwen.

* Het verkeer naar de pagina van de adverteerder kwam van een referentie of een organische onderzoek in plaats van van van een advertentie.

* De tag voor het bijhouden van conversies wordt niet correct geïmplementeerd op alle toepasselijke webpagina&#39;s of is bewerkt.

*Mogelijke oplossing of oplossing:*

1. Ga naar **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** en een [!UICONTROL Transaction Report]. Vergelijk de transacties die Search, Social &amp; Commerce hebben ontvangen met de gegevens van de adverteerder.

1. Als sommige transacties onjuist zijn of ontbreken, dan zorg ervoor dat de relevante het volgen van omzettingen markering op alle toepasselijke webpagina&#39;s wordt uitgevoerd en niet uitgegeven tenzij uw Team van de Rekening van de Adobe u adviseert om dit te doen. Een tag ontbreekt of wordt gewijzigd als de website onlangs is bijgewerkt.

   Zoek, Sociaal, &amp; Handel verwacht goed gevormde URLs (met parameters in naam-waarde paren) binnen `ef_transaction_properties` en binnen de `src` element van het `img` -tag.

1. Als u het probleem niet kunt bepalen en oplossen, dan [Contact opnemen met de klantenservice](/help/search-social-commerce/get-help.md).

   De zorg van de klant zal proberen om de ontbrekende transacties te identificeren en dan om op weestransacties en transacties te controleren die niet uit een advertentie kwamen (&quot;ongecorreleerde omzettingen&quot;).

**Adverteerders met gegevensdoorvoer voor conversie `ef_id` waarden**

Zie de mogelijke oorzaken en oplossingen voor pixelimplementaties hierboven.

**Adverteerders met de invoer van conversiegegevens gebruiken transactie-id&#39;s**

*Mogelijke oorzaken:*

* Bij zoeken, Sociaal en Handel worden inkomsten genegeerd wanneer het cookie verloopt of wordt verwijderd, maar de adverteerder kan dit als geldige inkomsten beschouwen.

* Het verkeer naar de pagina van de adverteerder kwam van een referentie of een organische onderzoek in plaats van van van een advertentie.

* Er is een offline conversie gerapporteerd voordat er een online transactie met dezelfde transactie-id heeft plaatsgevonden. De online transactie moet eerst plaatsvinden.

*Mogelijke oplossing of oplossing:*

1. Ga naar **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** en een [!UICONTROL Transaction Report]. Vergelijk de transacties die Search, Social &amp; Commerce hebben ontvangen met de de voedergegevens van de adverteerder.

1. Als een transactie in het feed-bestand ontbreekt in het rapport, controleert u of er een online transactie met dezelfde transactie-id (bijgehouden via de pixel) heeft plaatsgevonden vóór de offline conversie.

1. Als u het probleem niet kunt bepalen en oplossen, dan [Contact opnemen met de klantenservice](/help/search-social-commerce/get-help.md).

   De klantenservice controleert op fouten bij het parseren van gegevens en [verweesde transacties](/help/search-social-commerce/glossary.md#o-p).

**Adverteerders met andere soorten conversiegegevens**

*Mogelijke oorzaken:*

* Bij zoeken, Sociale media en Handel worden inkomsten genegeerd wanneer de cookie verlopen of verwijderd is, maar de adverteerder kan dit als geldige inkomsten beschouwen.

* Het verkeer naar de pagina van de adverteerder kwam van een referentie of een organische onderzoek in plaats van van van een advertentie.

* Er zijn [verweesde transacties](/help/search-social-commerce/glossary.md#o-p)Zoekopdrachten, sociale zaken en handel tellen dus niet alle inkomsten die het verdient.

* De adverteerder heeft een zoek-, sociaal en handelrapport gevalideerd op basis van een andere set gegevens dan die welke in de feed zijn verzonden.

* De transactie-id&#39;s (`ev_transid` waarden) zijn niet verzonden, zijn niet uniek of zijn onjuist.

* Het feed-bestand bevat dubbele id&#39;s voor bijhouden.

* Er zijn fouten opgetreden bij het parseren van het bestand.

* De deduping-logica van de adverteerder verschilt van de zoeklogica, de logica van sociale zaken en handel.

*Mogelijke oplossing of oplossing:*

1. Ga naar **[!UICONTROL Insights]&amp;[!UICONTROL Reports > Reports]** en een [!UICONTROL Transaction Report]. Vergelijk de transacties die Search, Social &amp; Commerce hebben ontvangen met de gegevens van de adverteerder.

1. Als sommige transacties onjuist zijn of ontbreken, dan zorg ervoor dat a) het voederdossier alle vereiste transactie IDs en geen dubbele het volgen IDs bevat en b) de transactie IDs uniek en correct is.

1. Als u het probleem niet kunt bepalen en oplossen, dan [Contact opnemen met de klantenservice](/help/search-social-commerce/get-help.md).

   De zorg van de klant zal op gegevens het ontleden fouten en wezen transacties controleren.
+++

+++Opbrengstgegevens verschillen van gegevens in Adobe Analytics Zie [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html).<!-- change link URL to relative link -->
+++

## Specifieke verslagen

+++Moet [!UICONTROL Portfolio Report] dezelfde cijfers tonen als de [!UICONTROL Portfolios] bekijken?
De [!UICONTROL Portfolio Report] en de [!UICONTROL Portfolios] de mening toont de zelfde gegevens wanneer alle filters voor de mening, de rapportparameters, en de gegevenskolommen voor de mening en het rapport het zelfde zijn. Als de [!UICONTROL Portfolios] in de weergave worden portfolio&#39;s weergegeven die &quot;[!UICONTROL All but inactive]&quot; voor het datumbereik &quot;[!UICONTROL Last 7 days]&quot; en met alleen de weergegeven standaardgegevenskolommen, en een [!UICONTROL Portfolio Report] bij gebruik van de standaardparameters worden identieke gegevens weergegeven. Als u een van de rapportparameters wijzigt of andere filters gebruikt in het dialoogvenster [!UICONTROL Portfolios] kunnen de gegevenswaarden anders zijn.
+++

+++De gegevens in mijn [!UICONTROL Portfolio Report] komt niet overeen met de gegevens in mijn [!UICONTROL Search Engine Report] of [!UICONTROL Search Engine Account Report].
De [!UICONTROL Portfolio Report] toont gegevens voor slechts de campagnes die aan de gespecificeerde portefeuilles worden toegewezen, maar [!UICONTROL Search Engine Report] en [!UICONTROL Search Engine Account Report] Dit kunnen ook gegevens bevatten voor campagnes die niet aan een portfolio zijn toegewezen.
+++

+++How is [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] anders dan op portefeuilleniveau [!UICONTROL Model Accuracy Report]?
(Alleen accountmanager van het Bureau, accountmanager van de Adobe en beheerders) De [!UICONTROL Forecast Accuracy Report] beschikbaar via [!UICONTROL Reports] > [!UICONTROL Model Accuracy] verstrekt de zelfde gegevens zoals het portefeuilleniveau [!UICONTROL Model Accuracy Report] behalve dat u het over veelvoudige portefeuilles kunt in werking stellen en u kunt de attributieregel veranderen. U kunt het rapport ook in werking stellen en plannen gebruikend douaneparameters, en u kunt het gebruiken om spreadsheetvoer tot stand te brengen. Bovendien [!UICONTROL Forecast Accuracy Report] nauwkeuriger is dan het verslag op portefeuilleniveau uit het verleden, omdat het de juistheid van de opbrengsten evalueert aan de hand van de historische doelstellingen voor de portefeuille in plaats van de huidige doelstelling, en het nauwkeuriger gegevens voor de toepasselijke tijdzone vertegenwoordigt.
+++

+++Gegevens op advertentieniveau zijn niet beschikbaar voor [!DNL Google Ads] dynamic search ad (DSA), performance max, smart shopping en [!DNL YouTube] campagnes.
De advertentienetwerken verstrekken niet het herkenningsteken noodzakelijk om opbrengst aan een individuele advertentie voor die campagnes toe te schrijven. Daarom zijn er geen prestatiegegevens op ad-niveau beschikbaar voor die typen campagnes in het dialoogvenster [!UICONTROL Ads] of in de [!UICONTROL Ad Variation Report]. Verwacht discrepanties tussen de totale ad-level gegevens voor een campagne en de totale gegevens voor de campagne.
+++

+++In de [!UICONTROL Transaction Report], hoe weet ik welke omzettingsmetrische waarde afkomstig is van een gegevenstoevoer of wordt bijgehouden door de Adobe Advertising die pixel volgt?
In een transactierapport kunt u zien of een inbegrepen metrisch omzettingspunt door de Adobe Advertising volgpixel werd gevolgd als u de douanekolom &quot;[!UICONTROL Tracking URL].&quot; URL&#39;s bijhouden met de pixel voor het bijhouden van de Adobe Advertising begint met &quot;`http://pixel.everesttech.net`.&quot;
+++

+++De gegevens in mijn [!UICONTROL Transaction Report] komt niet overeen met de gegevens in mijn [!UICONTROL Keyword Report].
Wanneer u beide rapporten genereert op portfolio, zijn de gegevens anders als u de [!UICONTROL Keyword Report] het gebruiken van historische gegevens (d.w.z., gebaseerd op de portefeuilleconfiguratie tijdens de gespecificeerde data) eerder dan het gebruiken van gegevens voor de huidige campagnes. Wanneer u de [!UICONTROL Transaction Report] per portfolio bevat het gegevens voor de huidige campagnes in het portfolio.
+++

## Werkbladfeeds

+++De output van het Rapport omvat een mengeling van datumwaaiers.
U kunt verschillende datumbereiken zien als de feed gegevens aggregeert met een ander niveau van gegevensaggregatie dan &quot;[!UICONTROL Daily].&quot;

Om het probleem op te lossen, werkt u de spreadsheetfeed bij en voegt u dagelijks geaggregeerde gegevens in. Deze taak omvat het bijwerken van het rapportmalplaatje, het produceren van een rapport gebruikend het malplaatje, het creëren van een douane [!DNL Microsoft® Excel] malplaatje gebruikend het rapport, en dan het bijwerken van de voedermontages om het nieuwe malplaatje van Excel te omvatten. Zie voor meer informatie &quot;[Invoerinstellingen voor spreadsheetrapporten bewerken](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

+++A-spreadsheetfeed resulteert in een interne fout.
Deze fout kan voorkomen als u de kolommen in het rapportmalplaatje verandert maar niet bijwerkt [!DNL Microsoft® Excel] dienovereenkomstig template.

Als u het probleem wilt verhelpen, werkt u de spreadsheetfeed bij en voegt u de nieuwe kolommen in. Deze taak omvat het bijwerken van het rapportmalplaatje, het produceren van een rapport gebruikend het malplaatje, het creëren van een douane [!DNL Excel] malplaatje gebruikend het rapport, en dan het bijwerken van de voedermontages om het nieuwe malplaatje van Excel te omvatten. Zie voor meer informatie &quot;[Invoerinstellingen voor spreadsheetrapporten bewerken](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

+++Wanneer ik een spreadsheetfeed probeer te openen in [!DNL Excel], [!DNL Excel] meldt een fout met betrekking tot &quot;onleesbare inhoud&quot; en er worden gegevens uit de herstelde inhoud verwijderd.
Wanneer de [!DNL Microsoft® Excel] de sjabloon sorteert gegevens niet op begindatum in oplopende volgorde, de spreadsheetfeed kan lege rijen bevatten. Met name: [!DNL Excel] meldt de fout &quot;Excel found unreadable content in &#39;&lt;*rapportnaam*>.xlsx.&#39; Wilt u de inhoud van het werkboek terugkrijgen? Als u de bron van dit werkboek vertrouwt, klik ja.&quot; Als u &quot;ja klikt,&quot;krijgt u het volgende bericht: &quot;Verwijderd Verslagen: De informatie van de cel van /xl/worksheets/sheet1.xml deel,&quot;en de spreadsheetvoer omvat lege rijen.

Als u het probleem wilt verhelpen, bewerkt u de [!DNL Excel] sjabloon gekoppeld aan feed om gegevens te sorteren op [!DNL Start date in Ascending (Oldest to Newest) order]en uploadt u de bijgewerkte sjabloon via de instellingen voor spreadsheetfeed. Zie voor meer informatie &quot;[Werkbladrapportfeeds bewerken](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++
