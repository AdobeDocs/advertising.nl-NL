---
title: Veelgestelde vragen over aangepaste rapporten
description: Leer antwoorden op veelgestelde vragen over prestatiesrapporten, met inbegrip van het oplossen van problemen van gegevenskwesties.
exl-id: 1232efce-25eb-48d8-a3fb-f57711fa14e5
feature: Search Reports
source-git-commit: c0f8f8c2886ea821dd7705446a727054b66ad3bc
workflow-type: tm+mt
source-wordcount: '3922'
ht-degree: 0%

---

# Veelgestelde vragen over aangepaste rapporten

## Algemene vragen

+++Wat als de datumwaaier voor het rapport begint alvorens rapportgegevens beschikbaar is?
Het rapport wordt gegenereerd, maar bevat alleen gegevens voor de datums waarvoor gegevens beschikbaar zijn. Voor meer informatie over wanneer het gegeven voor elk rapporttype beschikbaar is, zie &quot;[ Gegevens die voor Rapporten ](data-used-for-reports.md) worden gebruikt.&quot;
+++

+++Wat is het verschil tussen klik datum en transactie op datum-gebaseerde rapporten?
Wanneer u omzettingen per transactiedatum rapporteert, omvatten de gegevens transacties waarvan de transactiedatum tijdens de opgegeven tijdsperiode is opgetreden. Deze optie is het gebrek dat in basisrapporten en geavanceerde rapporten plaatst, en het toont u hoeveel opbrengst binnen de gespecificeerde tijdspanne werd verdiend.

Wanneer u omzettingen door klikdatum rapporteert, omvatten de gegevens transacties die uit een klik voortvloeiden die tijdens de gespecificeerde tijdspanne voorkwam. Wanneer een portefeuille significante vertragingen tussen kliks en transacties heeft, toont dit type van rapportering de historische opbrengst per klik voor de portefeuille, die u een idee geeft van welk opbrengstgedrag in tijd te verwachten.

![ Rapport door datum tegenover rapport te klikken door transactiedatum ](/help/search-social-commerce/assets/click-date-vs-txn-date.png " Rapport door datum tegenover rapport door transactiedatum ") te klikken
+++

+++Wat gebeurt als ik het venster van de klikraadpleging of het venster van de imitatieraadpleging verander?
(Adverteerders met alleen Advertising-service voor het bijhouden van pixelconversies) Gegevens voor gebeurtenissen die het resultaat zijn van de eerste klik worden gedurende een langere of kortere periode verzameld.

Een adverteerder [ klikt raadplegingsvenster ](/help/search-social-commerce/glossary.md#c-d) en [ het venster van de imitatieraadpleging ](/help/search-social-commerce/glossary.md#i-j) bepaalt het aantal dagen na een betaalde klik of een vertoningsindruk (respectievelijk) komt voor waarin de gebeurtenis aan een omzetting kan worden toegeschreven. Het kan belangrijk zijn om een waarde te wijzigen in een langere of kortere periode voor adverteerders met bijzonder korte of lange &#39;click-to-Revenue&#39;-periodes of &#39;shadow-to-Revenue&#39;-perioden.

**Beste praktijken:** zorg ervoor dat de raadplegingsvensters langer zijn dan de klik-aan-opbrengst en vertoning beeld-aan-opbrengst tijden voor het grootste deel van uw sleutelwoorden of advertenties. Wanneer zij korter zijn, worden sommige omzettingen niet geassocieerd met de aanvankelijke klik of de indruk.
+++

+++Hoe weet ik welke omzettingen het resultaat zijn van een [!DNL Google Ads] extensie of productvermelding?
U kunt zien welke conversies het resultaat zijn van een klik op een [!DNL Google Ads] ad-extensie (in plaats van op de advertentie zelf) of op een product-aanbieding door een [!UICONTROL Transaction Report] te genereren. De kolomwaarde [!UICONTROL Link Type] toont het type en de titel van een koppeling waarop is geklikt:

* Productaanbiedingen worden aangeboden als `pla:<product ID>`, zoals `pla:8525822` .

* Sitelinks worden weergegeven als `sl:<Sitelink text>`, zoals `sl:See Current Offers` .

  U kunt ook een sitelink identificeren als u de kolom [!UICONTROL Tracking URL] in het rapport opneemt. De [!UICONTROL Tracking URL] voor een sitelink bevat het kenmerk `&ev_ltx=sl:<link-name>` .

>[!NOTE]
>
>Conversies van [!DNL Google Ads] -locaties en telefoonextensies worden opgenomen in de gegevens voor de advertenties die ze vergezellen. Ze worden niet afzonderlijk gerapporteerd.

+++

+++De &quot;[!UICONTROL Keyword]&quot;kolom in mijn rapport omvat een waarde &quot;(adgroup inhoud) &lt; *naam van de ad groep*>.&quot;
Wanneer de rij gegevens voor inhoud-toegelaten onderzoekscampagnes, vertoningscampagnes, of sociale campagnes omvat — die geen sleutelwoorden omvatten — de [!UICONTROL Keyword] kolom toont in plaats daarvan de toepasselijke naam van de advertentiegroep.
+++

+++Vanwege seizoensgebonden of marktveranderingen worden in mijn rapporten atypische gegevens weergegeven. Heeft dit gevolgen voor biedingen als de omstandigheden veranderen?
De optimaliseringscapaciteit bouwt zijn opbrengstmodellen voor elke biedingseenheid dagelijks om ervoor te zorgen dat het identificeert en onmiddellijk op trends reageert, en de modellen omvatten historische gegevens op lange termijn om seizoensgebonden prestaties te helpen voorspellen. De het inkomstenmodel van de portefeuille het plaatsen van de halfwaardetijd <!-- add link to glossary? --> bepaalt ook hoe zwaar recente opbrengstgegevens worden gewogen. De beste praktijk is om de halfwaardetijd tijdens een periode van atypische prestaties te verminderen maar te verhogen nadat het inkomstenmodel is aangepast. Als u vragen hebt over of het aanpassen van de halfwaardetijd noodzakelijk is, contacteer uw Team van de Rekening van de Adobe.

Als u niet wilt dat de gegevens voor de periode toekomstige biedingen beïnvloeden, dan kunt u verkiezen om die datums van het model uit te sluiten. Neem contact op met het accountteam van de Adobe om de datums uit te sluiten.
+++

+++Kan ik een rapport maken over de metrische waarde van een specifieke accounteigenschap, zoals [!UICONTROL Device] of [!UICONTROL Objective Name] ?
Voor rapporten van campagneentiteiten ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], en [!UICONTROL Product Group Report]), worden de metrieke gegevens dynamisch bijeengevoegd door de bezitskolommen u in het rapport omvat. U kunt naar keuze de belangrijkste kolom voor het rapport verwijderen en slechts de bezitskolommen omvatten waarvoor u gegevens wilt samenvoegen.

Als u bijvoorbeeld een [!UICONTROL Keyword Report] genereert die de apparaatkolommen [!UICONTROL Ad Group] en  bevat, worden in het rapport standaard de metriek voor elk trefwoord geaggregeerd op ad-groep en apparaattype. Nochtans, als u de [!UICONTROL Keyword] kolom verwijdert alvorens u het rapport produceert, dan produceert het rapport dynamisch metriek voor de gespecificeerde ad groepen door apparatentype.

>[!NOTE]
>
>U kunt deze functie niet gebruiken om gegevens te aggregeren op basis van labelclassificaties. Alle kolommen met labelclassificatie in het rapport worden weggelaten. In plaats daarvan, gebruik het [ Rapport van de Classificatie van het Etiket ](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## Algemene gegevenskwesties

+++Rapporten die worden gegenereerd met verschillende toewijzingsregels geven verschillende totalen weer.
Als u een rapport veelvoudige tijden gebruikend de zelfde rapportparameters maar met verschillende attributenregels produceert, dan kunnen de gegevens om één van beide volgende redenen verschillen:

* Klik op datumgegevens als deze buiten het opgegeven datumbereik vallen.

  Als u de rapportparameter &quot;[!UICONTROL Conversions based on click date] gebruikt,&quot;dan is de gespecificeerde datumwaaier op de datum van de klik in plaats van de datum van de transactie van toepassing. Als in het rapport ook de toewijzingsregel &quot;Eerste gebeurtenis&quot; of &quot;Laatste gebeurtenis&quot; wordt gebruikt, kan de eerste of laatste gebeurtenis die tot de conversie heeft geleid, zich buiten het opgegeven datumbereik bevinden. Bijvoorbeeld, veronderstel dat een gebruiker Keyword_1 op 30 April klikte, Keyword_2 op 20 Mei klikte, en op 21 Mei omgezet. Als het rapport &quot;[!UICONTROL First Event]&quot;attributieregel en een datumwaaier van 1 Mei-21 gebruikt, dan is de eerste gebeurtenis (een klik op Keyword_1 op 30 april) niet inbegrepen in het rapport. Als u het rapport met de zelfde datumwaaier maar gebruikend &quot;[!UICONTROL Last Event]&quot;attributieregel in werking stelt, dan is de omzetting inbegrepen in het rapport omdat de laatste klik binnen de gespecificeerde datumwaaier voorkwam.

* Bij de selectie van het portfoliofilter worden enkele gebeurtenissen die tot de conversie leiden, uitgesloten.

  Als u een subset van portfolio&#39;s rapporteert, hoeft u mogelijk geen campagnes op te nemen die de gebeurtenis bevatten waaraan de conversie is toegewezen op basis van een van de toewijzingsregels. Bijvoorbeeld, veronderstel een gebruiker Keyword_1 van Portfolio_1 klikt, Keyword_2 van Portfolio_2 klikt, en dan omzet. Als het rapport &quot;[!UICONTROL First Event]&quot;attributieregel gebruikt, dan moet Portfolio_1 voor de omzetting worden omvat die in het rapport moet worden omvat. Nochtans, als het rapport de &quot;Laatste gebeurtenisattributieregel&quot;gebruikt, dan moet Portfolio_2 worden omvat.

>[!TIP]
>
>Als u omzettingstotalen onder verschillende attributieregels wilt vergelijken, dan looppas rapporten gebruikend de rapportparameter &quot;[!UICONTROL Conversions based on transaction date]&quot;en selecteer alle ad netwerken of alle portefeuilles. Als u geen andere filters instelt, moeten de totalen van de omzetting overeenkomen.

+++

+++Afzonderlijke gegevensvelden zijn onjuist, hoewel de totalen juist zijn.
Deze situatie kan zich voordoen wanneer de metrische formaten gehelen gebruiken:

* Als u a [ douane metrische ](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) met het formaat *Aantal met Decimale Punten* (die gegevens als gehelen) toont en het in een mening of een rapport omvat die een gewogen omzettingsattributieregel ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], of [!UICONTROL Even Distribution]) gebruikt, dan wordt de output getoond in gehelen, niet decimalen. In dit geval zijn afzonderlijke gegevensvelden mogelijk onjuist, hoewel de totalen juist zijn. Als een volgorde bijvoorbeeld gelijk is verdeeld tussen drie gebeurtenissen, wordt één volgorde (in plaats van 0,33 volgorde) toegewezen aan elk van de drie gebeurtenissen. Om de kwestie op te lossen, [ verander het metrische formaat ](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) in *Aantal in 2 Decimale Punten*.

* Op dezelfde manier als u opbrengst metrisch hebt die zoals in geheel wordt verzonden, dan komt de zelfde kwestie voor. (Het inkomstenformaat wordt gecontroleerd door de omzettingsmarkering die de gegevens indient.) Om de kwestie op te lossen, [ creeer een douane metrisch ](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) die enkel uit opbrengst metrisch en met het formaat *Aantal aan 2 Decimale Punten* bestaat, en omvat het in meningen en rapporten eerder dan origineel metrisch.
+++

+++Wanneer klik of de opbrengstgegevens ontbreken, hoe ik het verhinderen toekomstige biedingen te beïnvloeden?
Klik op gegevensproblemen als Zoeken, Sociaal en Commerce niet synchroon is met het advertentienetwerk. Neem contact op met het accountteam van de Adobe om de account handmatig te synchroniseren. Als klikgegevens een hele dag ontbreken, dan vraag uw Team van de Rekening van de Adobe om die dag van de kostenmodellen uit te sluiten.

Problemen met inkomstengegevens kunnen optreden als gevolg van een probleem met het bijhouden of doorvoeren van een bestand. Neem contact op met het accountteam van de Adobe om het probleem te onderzoeken. Als de opbrengstgegevens voor een volledige dag ontbreken, dan vraag uw Team van de Rekening van de Adobe om die dag van de opbrengstmodellen uit te sluiten.
+++

+++Monetaire gegevens worden in het verkeerde formaat weergegeven.
Standaard worden alle monetaire gegevens in rapporten weergegeven in de notatie voor Amerikaanse dollars (zoals 1.000,00). Om de waarde in het correcte muntformaat (maar zonder om het even welke muntsymbolen in Csv en Vv formaten) te tonen, voeg de &quot;[!UICONTROL Currency]&quot;kolom aan het rapport toe. Als het rapport gegevens voor rekeningen met verschillende valuta&#39;s omvat, dan zijn om het even welke &quot;[!UICONTROL Total]&quot;monetaire waarden eenvoudig de som alle aantallen in de kolom, ongeacht munt.
+++

+++Waarom zie ik decimale waarden voor omzettings metrisch die een natuurlijk aantal (1, 2, etc.) zouden moeten zijn?
In de volgende gevallen kunt u decimale waarden zien:

* Als u het rapport uitvoert met een andere parameter voor de omzettingstoewijzingsregel dan [!UICONTROL Last Event] of [!UICONTROL First Event] , kunnen de opbrengsten worden gesplitst tussen meerdere gebeurtenissen in het conversiepad.

* In [!UICONTROL Transaction Report], als de veelvoudige [ biedingseenheden ](/help/search-social-commerce/glossary.md#a-b) met verschillende gelijke types zelfde transactie identiteitskaart hebben, dan wordt de opbrengst voor het volgen identiteitskaart verdeeld volgens het aantal klikken op de gespecificeerde klikdatum.
+++

## Standaardprestatiewaarden

+++Klik gegevens ontbreken in rapporten.
Dit zijn algemene redenen voor het ontbreken van klikgegevens.

| Oorzaak | Detectie/analyse | Resolutie |
|---|---|---|
| Het proces dat klikgegevens van de advertentierekening terugwint ontbrak. | Er is geen systematische manier om dit probleem op te sporen, maar u kunt zien dat een campagne geen kosten toont of op informatie klikt, ook al heeft de advertentierekening geld uitgegeven. | Neem contact op met het accountteam van de Adobe.<br><br> als het gegeven meer dan 24 uren mist, dan sluit die data van de kostenramingen uit tot de gegevens worden teruggewonnen. Uw accountteam van de Adobe kan de datums uitsluiten. |
| Een factureringsprobleem tussen de adverteerder en het advertentienetwerk voorkomt dat de advertentierekening uitgaven. | Er is geen systematische manier om dit probleem op te sporen, maar u kunt zien dat een campagne geen kosten toont of op informatie klikt. | Als u weet dat een advertentierekening niet kon uitgeven wegens een factureringskwestie, dan sluit die data van de kostenramingen uit. Uw accountteam van de Adobe kan de datums uitsluiten. |

+++

+++Prestatiegegevens zijn verschillend van gegevens in de ad netwerkredacteur.
Wanneer het advertentienetwerk updates naar vorige gegevens verzendt (vaak omdat zij klikfraude aan sommige kliks hebben toegeschreven), werkt het Onderzoek, Sociale, &amp; Commerce niet de gegevens bij tenzij er meer dan een 5% discrepantie is en het Team van de Rekening van de Adobe een verzoek indient.

Wanneer u de indruk vergelijkt dat gedeelde gegevens over een datumbereik zijn samengevoegd, kunnen de gegevens die door de rapporten Zoeken, Sociaal en Commerce worden gerapporteerd, afwijken van de gegevens die door het advertentienetwerk worden gerapporteerd. Dit verschil is te wijten aan de manier waarop de gegevens worden gerapporteerd door de API van het advertentienetwerk, die door Search, Social &amp; Commerce wordt gebruikt om gegevens aan te trekken. Bijvoorbeeld voor [!DNL Google Ads] data:

* Voor de meeste indruk deelt u metriek. In [!DNL Google Ads] wordt de lage of hoge waarde van waarden die voor waarden van minder dan 10% of meer dan 90% worden gerapporteerd, afgekapt. Gegevens worden gerapporteerd als 0,0999 voor &lt;10% en 0,9001 voor >90%

* Wanneer er een combinatie van geplafonneerde en niet-geplafonneerde gegevens binnen het datumbereik is, worden bij de indruk Zoeken, Sociaal en Commerce gegevens gedeeld met de waarden die ongewijzigd in de API worden verzonden. Bij rijen met &lt; 10% en 0,9001 wordt 0,0999 gebruikt voor rijen met > 90%. Deze samenvoeging kan resulteren in een verschil met de [!DNL Google Ads] vooraf geaggregeerde gegevens omdat [!DNL Google Ads] werkelijke percentagewaarden kan gebruiken, zoals 7% of 97%.
+++

+++Prestatiegegevens in rapporten zijn verschillend van gegevens in [!DNL Google Analytics].
De twee systemen meten verschillende gegevens, zodat zou u moeten verwachten om verschillende gegevens te zien. Bijvoorbeeld:

* Met Zoeken, Sociaal en Commerce (en Google Ads) kunt u klikken, terwijl met [!DNL Google Analytics] bezoeken per browsersessie van 30 minuten worden bijgehouden. Als een gebruiker bijvoorbeeld eenmaal op uw advertentie klikt, vervolgens op de knop Terug klikt en vervolgens opnieuw op de advertentie klikt, worden twee keer op de advertentie geklikt met de opdracht Zoeken, Sociaal en Commerce, maar wordt één bezoek vastgelegd door [!DNL Google Analytics] .

* [!DNL Google Analytics] geeft alle verkeersgegevens weer, terwijl met de filters Zoeken, Sociaal en Commerce (en [!DNL Google Ads] ) ongeldige kliks worden gefilterd (zoals te vaak klikken).

* [!DNL Google Analytics] bevat klikgegevens en inkomstengegevens voor alle klikken. Zoeken, sociale media en Commerce kunnen klikgegevens en inkomstengegevens voor advertenties en trefwoorden met onjuiste of ontbrekende URL&#39;s niet bijhouden.
+++

## Omzettingsmetriek

+++Mijn rapport toont geen omzettingsgegevens.
Het rapport bevat mogelijk geen conversiemetriek waarvoor conversies hebben plaatsgevonden.
+++

+++Opbrengst ontbreekt in rapporten.

**Advertisers die de markeringen van de Adobe Advertising omzettingen gebruiken**

*Mogelijke oorzaken:*

* Trefwoorden of advertenties zijn toegevoegd zonder het voorvoegsel voor het bijhouden van de zoekopdracht, sociaal en Commerce-klik toe te voegen aan de trackingsjablonen of doel-URL&#39;s, of het voorvoegsel voor bijhouden is onjuist.

* De tag voor het bijhouden van conversies wordt niet correct geïmplementeerd op alle toepasselijke webpagina&#39;s of is bewerkt.

* De omzettingsmetriek die Onderzoek, Sociaal, &amp; Commerce volgt zijn uitgesloten van rapporten en daarom niet zichtbaar.

* De inkomstenparser voor de cliënt werd niet uitgevoerd.

*Mogelijke oplossing of werk-rond:*

1. Controleer of de juiste kolommen zijn opgenomen in de rapporten- of gegevensweergaven. Als de correcte kolommen niet beschikbaar zijn om toe te voegen, dan moet u of uw Team van de Rekening van de Adobe [ de omzettingsmetriek beschikbaar maken aan rapporten ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Controleer of de juiste codes voor het bijhouden van conversies zijn geïmplementeerd op alle toepasselijke webpagina&#39;s. Vraag indien nodig uw accountteam van de Adobe om een testtransactie te maken voor elke toepasselijke code voor het bijhouden van conversies en om de gegevens van de transactie vast te leggen, zoals de `transactionid` en de gegevens van het cookie (zoals de `trackingid` , `clickid` , enzovoort).

1. Als de optie [!UICONTROL Auto Upload] is uitgeschakeld voor de campagne en u trefwoorden of advertenties hebt toegevoegd, moet u een trackingsjabloon of doel-URL met Zoeken, Sociaal zoeken en Commerce op Doorsturen klikken voor elke sjabloon. Het accountteam van uw Adobe kan een intern rapport uitvoeren om te controleren of een klik-volgende URL&#39;s (trackingsjablonen of doel-URL&#39;s) ontbreken of onjuist zijn geformuleerd.

   Indien noodzakelijk, produceer het volgen door een bulksbladdossier met correcte URLs te creëren, en post het dossier aan de aangewezen rekening gebruikend **het Volgen URLs** optie produceert.

   De doel-URL moet beginnen met &quot;http://pixel.everesttech.net&quot; of &quot;https://pixel.everesttech.net&quot;.

1. Als geen van deze stappen de kwestie oplost, dan [ contacteer de Zorg van de Klant ](/help/search-social-commerce/get-help.md).

   Als de client niet is gestart of pas is gestart, controleert de klantenservice of er een inkomstenparser is ingesteld. Als de parser is ingesteld, verifiëren ze of Search, Social en Commerce pixelomzettingen ontvangen en het probleem oplossen.

**Advertisers die de voer van omzettingsgegevens verzenden**

*Mogelijke oorzaken:*

* Het voederbestand werd niet afgeleverd, het werd niet volledig geparseerd, of het voer bevatte transacties met wezen.

* De relevante omzettingsmetriek worden uitgesloten van rapporten en daarom niet zichtbaar.

>[!NOTE]
>
>De gegevens verschijnen over het algemeen niet in het gebruikersinterface tot 2-4 uur nadat het voer wordt ontvangen.

*Mogelijke oplossing of werk-rond:*

1. Controleer of de juiste kolommen zijn opgenomen in de rapporten- of gegevensweergaven. Als de correcte kolommen niet beschikbaar zijn om toe te voegen, dan moet u of uw Team van de Rekening van de Adobe [ de omzettingsmetriek beschikbaar maken aan rapporten ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md).

1. Voer de lus [!UICONTROL Portfolio Report] uit. Als deze leeg is, voert u de instructies [!UICONTROL Campaign Report] en [!UICONTROL Search Engine Report] uit om te controleren of de opbrengsten in die rapporten worden weergegeven. Als dat het geval is, worden de campagnes mogelijk niet toegewezen aan de juiste portefeuille.

1. Controleer of het bestand naar de opbrengstserver is verzonden en of het bestand dezelfde indeling en naamgevingsconventie heeft gevolgd als vorige bestanden.

   Als de indeling of naamgevingsconventie voor bestanden is gewijzigd, corrigeert u het bestand en stuurt u het opnieuw.

1. Als het dossier werd verzonden, dan [ contacteer de Zorg van de Klant ](/help/search-social-commerce/get-help.md).

   De klantenservice controleert of het bestand is ontvangen en geparseerd. Als het bestand zonder fouten is verwerkt, controleren ze op verweesde transacties.
+++

+++Sommige geavanceerde rapporten bevatten geen omzettingsgegevens die door een adverteerdervoer worden verstrekt.
De [!UICONTROL Geo Distribution Report] en [!UICONTROL Domain Referral Report] gebruiken gegevens die zijn vastgelegd via de service voor het bijhouden van Adoben Advertising en kunnen alleen worden gegenereerd voor adverteerders met de service. De rapporten omvatten geen omzettingsgegevens die buiten het de omzettingsvolgsysteem van de Adobe Advertising worden gevolgd.
+++

+++inkomstengegevens verschillen van de eigen inkomstengegevens van de adverteerder.

**Advertisers die de markeringen van de Adobe Advertising omzettingen gebruiken**

*Mogelijke oorzaken:*

* Zoeken, Sociaal en Commerce negeert inkomsten wanneer de cookie verlopen of verwijderd is, maar de adverteerder beschouwt deze mogelijk als geldige inkomsten.

* Het verkeer naar de pagina van de adverteerder kwam van een referentie of een organische onderzoek in plaats van van van een advertentie.

* De tag voor het bijhouden van conversies wordt niet correct geïmplementeerd op alle toepasselijke webpagina&#39;s of is bewerkt.

*Mogelijke oplossing of werk-rond:*

1. Ga naar **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** en genereren een [!UICONTROL Transaction Report] . Vergelijk de transacties die Search, Social &amp; Commerce heeft ontvangen met de gegevens van de adverteerder.

1. Als sommige transacties onjuist zijn of ontbreken, dan zorg ervoor dat de relevante het volgen van omzettingsmarkering op alle toepasselijke webpagina&#39;s wordt uitgevoerd en niet werd uitgegeven tenzij uw Team van de Rekening van de Adobe u adviseerde dit te doen. Een tag ontbreekt of wordt gewijzigd als de website onlangs is bijgewerkt.

   Search, Social &amp; Commerce verwacht goed gevormde URL&#39;s (met parameters in naam-waardeparen) binnen de `ef_transaction_properties` -variabele en binnen het `src` -element van de `img` -tag.

1. Als u niet de kwestie kunt bepalen en oplossen, dan [ contacteer de Zorg van de Klant ](/help/search-social-commerce/get-help.md).

   De zorg van de klant zal proberen om de ontbrekende transacties te identificeren en dan om op weestransacties en transacties te controleren die niet uit een advertentie kwamen (&quot;ongecorreleerde omzettingen&quot;).

**Advertisers met de voer van omzettingsgegevens gebruikend `ef_id` waarden**

Zie de mogelijke oorzaken en oplossingen voor pixelimplementaties hierboven.

**Advertisers met de voer van omzettingsgegevens gebruikend transactie IDs**

*Mogelijke oorzaken:*

* Zoeken, Sociaal en Commerce negeert inkomsten wanneer de cookie vervalt of wordt verwijderd, maar de adverteerder kan dit als geldige inkomsten beschouwen.

* Het verkeer naar de pagina van de adverteerder kwam van een referentie of een organische onderzoek in plaats van van van een advertentie.

* Er is een offline conversie gerapporteerd voordat er een online transactie met dezelfde transactie-id heeft plaatsgevonden. De online transactie moet eerst plaatsvinden.

*Mogelijke oplossing of werk-rond:*

1. Ga naar **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** en genereren een [!UICONTROL Transaction Report] . Vergelijk de transacties die Search, Social en Commerce hebben ontvangen met de feedbackgegevens van de adverteerder.

1. Als een transactie in het feed-bestand ontbreekt in het rapport, controleert u of er een online transactie met dezelfde transactie-id (bijgehouden via de pixel) heeft plaatsgevonden vóór de offline conversie.

1. Als u niet de kwestie kunt bepalen en oplossen, dan [ contacteer de Zorg van de Klant ](/help/search-social-commerce/get-help.md).

   De zorg van de klant zal voor gegevens het ontleden fouten en [ wezen transacties ](/help/search-social-commerce/glossary.md#o-p) controleren.

**Advertisers met andere soorten de voer van omzettingsgegevens**

*Mogelijke oorzaken:*

* Zoeken, Sociaal en Commerce negeert inkomsten wanneer de cookie verlopen of verwijderd is, maar de adverteerder beschouwt deze mogelijk als geldige inkomsten.

* Het verkeer naar de pagina van de adverteerder kwam van een referentie of een organische onderzoek in plaats van van van een advertentie.

* Er zijn [ verweesde transacties ](/help/search-social-commerce/glossary.md#o-p), zodat het Onderzoek, Sociaal, &amp; Commerce niet alle opbrengst telt die het zou moeten.

* De adverteerder heeft een zoek-, sociaal en Commerce-rapport gevalideerd op basis van een andere set gegevens dan die welke in de feed zijn verzonden.

* De transactie IDs (`ev_transid` waarden) werd niet verzonden, is niet uniek, of is onjuist.

* Het feed-bestand bevat dubbele id&#39;s voor bijhouden.

* Er zijn fouten opgetreden bij het parseren van het bestand.

* De deduping-logica van de adverteerder verschilt van de zoeklogica, de sociale logica en de Commerce-logica.

*Mogelijke oplossing of werk-rond:*

1. Ga naar **[!UICONTROL Insights]&amp;[!UICONTROL Reports > Reports]** en genereer een [!UICONTROL Transaction Report] . Vergelijk de transacties die Search, Social &amp; Commerce heeft ontvangen met de gegevens van de adverteerder.

1. Als sommige transacties onjuist zijn of ontbreken, dan zorg ervoor dat a) het voederdossier alle vereiste transactie IDs en geen dubbele het volgen IDs bevat en b) de transactie IDs uniek en correct is.

1. Als u niet de kwestie kunt bepalen en oplossen, dan [ contacteer de Zorg van de Klant ](/help/search-social-commerce/get-help.md).

   De zorg van de klant zal op gegevens het ontleden fouten en wezen transacties controleren.
+++

+++Opbrengstgegevens verschillen van gegevens in Adobe Analytics
Zie [ https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html ](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html).<!-- change link URL to relative link -->
+++

## Specifieke verslagen

+++Moet de [!UICONTROL Portfolio Report] dezelfde figuren weergeven als de [!UICONTROL Portfolios] -weergave?
De weergaven [!UICONTROL Portfolio Report] en [!UICONTROL Portfolios] tonen dezelfde gegevens wanneer alle filters voor de weergave, de rapportparameters en de gegevenskolommen voor de weergave en het rapport hetzelfde zijn. Bijvoorbeeld, als de [!UICONTROL Portfolios] mening portefeuilles toont die &quot; [!UICONTROL All but inactive]&quot;voor de datumwaaier &quot; [!UICONTROL Last 7 days]&quot;en met slechts de getoonde standaardgegevenskolommen zijn, dan toont a [!UICONTROL Portfolio Report] gebruikend de standaardparameters identieke gegevens. Als u een van de rapportparameters wijzigt of andere filters gebruikt in de weergave [!UICONTROL Portfolios] , kunnen de gegevenswaarden verschillen.
+++

+++De gegevens in mijn [!UICONTROL Portfolio Report] komen niet overeen met de gegevens in mijn [!UICONTROL Search Engine Report] of [!UICONTROL Search Engine Account Report] .
In [!UICONTROL Portfolio Report] worden alleen gegevens weergegeven voor de campagnes die zijn toegewezen aan de opgegeven portfolio&#39;s, maar de [!UICONTROL Search Engine Report] en [!UICONTROL Search Engine Account Report] kunnen ook gegevens bevatten voor campagnes die niet zijn toegewezen aan een portfolio.
+++

+++Hoe verschilt [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] van het portfolio-niveau [!UICONTROL Model Accuracy Report] ?
(Alleen accountmanager, accountmanager voor Adoben en gebruikers van beheerders) [!UICONTROL Forecast Accuracy Report] beschikbaar via [!UICONTROL Reports] > [!UICONTROL Model Accuracy] levert dezelfde gegevens als op portfolioniveau [!UICONTROL Model Accuracy Report] , maar u kunt deze uitvoeren in meerdere portfolio&#39;s en u kunt de toewijzingsregel wijzigen. U kunt het rapport ook in werking stellen en plannen gebruikend douaneparameters, en u kunt het gebruiken om spreadsheetvoer tot stand te brengen. Bovendien is [!UICONTROL Forecast Accuracy Report] nauwkeuriger dan het oude portefeuillerapport omdat het de opbrengstnauwkeurigheid gebruikend de historische doelstellingen voor de portefeuille eerder dan het huidige doel evalueert, en het nauwkeuriger gegevens voor de toepasselijke tijdzone vertegenwoordigt.
+++

+++Gegevens op advertentieniveau zijn niet beschikbaar voor [!DNL Google Ads] dynamische zoekopdrachten en (DSA), maximale prestaties, slim winkelen en [!DNL YouTube] -campagnes.
De advertentienetwerken verstrekken niet het herkenningsteken noodzakelijk om opbrengst aan een individuele advertentie voor die campagnes toe te schrijven. Hierdoor zijn prestatiegegevens op ad-niveau niet beschikbaar voor die typen campagnes in de [!UICONTROL Ads] -weergave of in [!UICONTROL Ad Variation Report] . Verwacht discrepanties tussen de totale ad-level gegevens voor een campagne en de totale gegevens voor de campagne.
+++

+++In [!UICONTROL Transaction Report], hoe weet ik welke omzettingsmetrische waarde van een gegevensvoer of door de Adobe Advertising volgende pixel is wordt gevolgd?
In een transactierapport, kunt u vertellen of inbegrepen omzettingsmetrisch door de Adobe Advertising volgende pixel werd gevolgd als u de douanekolom &quot;[!UICONTROL Tracking URL]&quot;omvat. Het volgen van URLs met de Adobe Advertising het volgen pixel begint met &quot;`http://pixel.everesttech.net`&quot;.
+++

+++De gegevens in mijn [!UICONTROL Transaction Report] komen niet overeen met de gegevens in mijn [!UICONTROL Keyword Report] .
Wanneer u beide rapporten per portfolio genereert, zijn de gegevens anders als u de [!UICONTROL Keyword Report] genereert met behulp van historische gegevens (dat wil zeggen, gebaseerd op de portfolioconfiguratie tijdens de opgegeven datums) in plaats van gegevens voor de huidige campagnes. Wanneer u de [!UICONTROL Transaction Report] per portfolio genereert, bevat deze gegevens voor de huidige campagnes in het portfolio.
+++

## Werkbladfeeds

+++De output van het Rapport omvat een mengeling van datumwaaiers.
U kunt verschillende datumwaaiers zien als de voer gegevens gebruikend om het even welk niveau van de gegevenssamenvoeging buiten &quot;[!UICONTROL Daily]&quot;samenvoegt.

Om het probleem op te lossen, werkt u de spreadsheetfeed bij en voegt u dagelijks geaggregeerde gegevens in. Deze taak omvat het bijwerken van het rapportmalplaatje, het produceren van een rapport gebruikend het malplaatje, het creëren van een douane [!DNL Microsoft Excel] malplaatje gebruikend het rapport, en dan het bijwerken van de voedermontages om het nieuwe malplaatje van Excel te omvatten. Voor meer informatie, zie &quot;[ spreadsheetrapportvoedermontages ](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md) uitgeven.&quot;
+++

+++A-spreadsheetfeed resulteert in een interne fout.
Deze fout kan optreden als u de kolommen in de rapportsjabloon wijzigt, maar de sjabloon [!DNL Microsoft Excel] niet dienovereenkomstig bijwerkt.

Als u het probleem wilt verhelpen, werkt u de spreadsheetfeed bij en voegt u de nieuwe kolommen in. Deze taak omvat het bijwerken van het rapportmalplaatje, het produceren van een rapport gebruikend het malplaatje, het creëren van een douane [!DNL Excel] malplaatje gebruikend het rapport, en dan het bijwerken van de voedermontages om het nieuwe malplaatje van Excel te omvatten. Voor meer informatie, zie &quot;[ spreadsheetrapportvoedermontages ](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md) uitgeven.&quot;
+++

+++Wanneer ik een spreadsheetfeed probeer te openen in [!DNL Excel] , geeft [!DNL Excel] een foutmelding weer dat de inhoud niet kan worden gelezen en worden gegevens uit de herstelde inhoud verwijderd.
Wanneer de [!DNL Microsoft Excel] -sjabloon gegevens niet op begindatum in oplopende volgorde sorteert, kan de spreadsheetfeed lege rijen bevatten. Met name, [!DNL Excel] meldt de fout &quot;Excel gevonden onleesbare inhoud in &quot;&lt; *rapportnaam*>.xlsx.&quot; Wilt u de inhoud van het werkboek terugkrijgen? Als u de bron van dit werkboek vertrouwt, klik ja.&quot; Als u &quot;ja klikt,&quot;krijgt u het volgende bericht: &quot;Verwijderd Verslagen: De informatie van de cel van /xl/worksheets/sheet1.xml deel,&quot;en de spreadsheetvoer omvat lege rijen.

Als u het probleem wilt verhelpen, bewerkt u de [!DNL Excel] -sjabloon die aan de feed is gekoppeld, om gegevens op [!DNL Start date in Ascending (Oldest to Newest) order] te sorteren. Vervolgens uploadt u de bijgewerkte sjabloon via de instellingen voor de spreadsheetfeed. Voor meer informatie, zie &quot;[ spreadsheetrapportvoer ](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md) uitgeven.&quot;
+++
