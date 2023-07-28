---
title: Vereiste gegevens voor het bulkwerkblad [!DNL Google Ads] rekeningen
description: Verwijs naar de vereiste kopbalgebieden en gegevensgebieden in bulksbladen voor [!DNL Google Ads] rekeningen.
exl-id: 1e35f503-c2fe-459c-ad13-6b8cf65be67e
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '7839'
ht-degree: 1%

---

# Aanhangsel - Vereiste gegevens voor het informatieblad voor [!DNL Google Ads] rekeningen

Om te creëren en bij te werken [!DNL Google Ads] Campagne gegevens in bulk, kunt u Onderzoek, Sociale, &amp; de bulksbladdossiers van de Handel gebruiken die specifiek voor worden geformatteerd [!DNL Google Ads] rekeningen. U kunt een van beide [bulkbladbestanden genereren voor bestaande accounts](../bulksheet-download.md) in de vereiste bestandsindeling of b) handmatig aanmaken (zie &quot;[Ondersteunde bestandsindelingen voor bulkbladbestanden](bulksheet-file-formats.md)&quot; voor algemene informatie over de ondersteunde bestandsindelingen).

Elk bulksblad moet de koptekstvelden en de bijbehorende gegevensvelden bevatten die zijn vereist voor de [specifieke bewerkingen die u wilt uitvoeren](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (zoals een advertentie maken). Als een veld niet vereist is, kunt u het weglaten uit de koptekst- en gegevensrijen. Alle aangepaste kolommen worden verwijderd wanneer u het bulkbladbestand uploadt.

Hieronder volgt een tabel met alle beschikbare gegevensvelden en aanvullende tabellen die aangeven welke velden vereist zijn om gegevens voor afzonderlijke entiteiten (zoals campagnes en trefwoorden) toe te voegen, te bewerken of te verwijderen.

## Alle beschikbare gegevensvelden {#bulksheet-fields-all-google}

In de volgende tabel worden alle beschikbare gegevensvelden beschreven.

Voor de gegevensvelden die relevant zijn voor rekeningentiteiten, zie &quot;[Velden vereist voor het maken, bewerken of verwijderen van elk accountonderdeel](#bulksheet-fields-per-component-google).&quot;

>[!NOTE]
>
>* De waarden in alle tekstkolommen zijn hoofdlettergevoelig.
>* Wanneer u een nieuwe record maakt en geen waarden opneemt voor alle vereiste gegevensvelden, worden aan sommige van deze velden de opgegeven standaardwaarden toegewezen.
>* Voor gebieden die hieronder niet worden gespecificeerd, wordt de standaardwaarde voor het advertentienetwerk gebruikt.
>* Voor een lijst met beschikbare rijen voor opsommingstekens in het dialoogvenster [!UICONTROL Download Bulksheet] dialoogvenster, zie &quot;[Opsommingstekstrijen per ad-netwerk](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network).&quot;

| Veld | Beschrijving |
| ---- | ---- |
| [!UICONTROL Platform] | (Opgenomen in gegenereerde bulksbladen ter informatie) Het advertentieplatform. Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Acct Name] | De unieke naam die een advertentienetwerkaccount identificeert. Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | De unieke naam die een campagne voor een account identificeert. |
| [!UICONTROL Campaign Budget] | Een dagelijkse uitgavenlimiet voor de campagne, met of zonder monetaire symbolen en leestekens. Deze waarde overschrijft, maar kan het budget van de account niet overschrijden. |
| [!UICONTROL Delivery Method] | <p>Hoe snel om advertenties voor de campagne elke dag te tonen:</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> (de standaardinstelling voor nieuwe campagnes): uw advertenties over de dag verspreiden.</p></li><li><p><i>[!UICONTROL Accelerated]:</i> (Verouderd in oktober 2019) Je advertenties zo vaak mogelijk weergeven totdat je budget is bereikt. Hierdoor worden uw advertenties mogelijk niet later op de dag weergegeven.</p></li></ul> |
| [!UICONTROL Channel Type] | <p>De kanalen waarop advertenties moeten worden geplaatst. Geef een of meer opties op:</p><ul><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Search]</i></span> (de standaardinstelling voor nieuwe campagnes): advertenties plaatsen op de [!DNL Google Ads] zoeknetwerk (inclusief [!DNL Google Ads] zoek- en zoekpartnerwebsites) en eventueel ook op de [!DNL Google Ads] weergavenetwerk. <b>Opmerking:</b> Campagnes die zowel het onderzoeksnetwerk als het vertoningsnetwerk richten kunnen niet aan een portefeuille voor bieding worden toegevoegd optimalisering.</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Display]</i></span>: Als u alleen advertenties op de [!DNL Google Ads] weergavenetwerk.</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Shopping]</i></span>: Winkeladvertenties plaatsen op [!DNL Google Ads] winkelnetwerk ( in bepaalde landen ) en [!DNL Google Ads] zoeknetwerk (inclusief [!DNL Google Ads] websites van partners zoeken en zoeken). Als u winkeladvertenties wilt maken, moet u producten in een [!DNL Google Merchant Center] rekening en [toestaan dat Search, Social en Commerce gegevens downloaden van de account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Zie &quot;[Implementeren [!DNL Google Ads] winkelcampagnes](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)&quot; voor meer informatie over het proces van het maken van winkeladvertenties .</p></li></ul> |
| [!UICONTROL Networks] | <p>Waar moet ik advertenties plaatsen? Geef een of meer opties op:</p><ul><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Google Search]</i></span>: Gesponsorde zoekopdrachten in alleen het Google Search Network.</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Search Partners]</i></span>: Gesponsorde zoekaanbiedingen op zoekpartners van Google.</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Content]</i></span>: Als u biedingen wilt plaatsen voor de weergave van netwerklijsten.</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL All]</i></span> (het gebrek voor nieuwe campagnes): Doet het Onderzoek van Google, de Partners van het Onderzoek, en Inhoud.</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>(Alleen zoeken in netwerk; alleen van toepassing op uitgebreide dynamische zoekadvertenties) Het hoofddomein (zoals example.com) of subdomein (zoals shoes.example.com) van de website waarvan de inhoud die het advertentienetwerk gebruikt om uw dynamische zoekadvertenties als doel in te stellen.<br><br><b>Opmerkingen:</b></p><ul><li><p>Uitgebreide dynamische zoekopdrachten zijn gericht op website-inhoud in plaats van op trefwoorden.</p></li><li><p>Uw domein moet door de biologische onderzoeksindex van het advertentienetwerk worden geïndexeerd om worden gericht.</p></li><li><p>Als u geen domein opgeeft, moet u voor elke advertentiegroep dynamische zoekdoelen maken, die al uw websitepagina&#39;s of een subset daarvan als doel hebben.</p></li></ul> |
| [!UICONTROL DSA Domain Language] | (Alleen netwerk zoeken; alleen van toepassing op uitgebreide dynamische zoekopdrachten) De taal voor het opgegeven websitedomein. <b>Opmerking:</b> Als het domein pagina&#39;s in veelvoudige talen bevat en u wilt elk van hen richten, creeer een afzonderlijke campagne voor elke taal. |
| [!UICONTROL GDN Custom Bid Level] | (Campagnes die slechts het vertoningsnetwerk richten) hoe te om te bieden: door <span style="font-style: italic;"><i>[!UICONTROL Ad Group]</i></span> (standaard), <span style="font-style: italic;"><i>[!UICONTROL Keyword]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Placement]</i></span> (website), of <span style="font-style: italic;"><i>[!UICONTROL None]</i></span> (om de bestaande waarde opnieuw in te stellen). Overige afmetingen (<span style="font-style: italic;"><i>Leeftijd</i></span>, <span style="font-style: italic;"><i>Geslacht</i></span>, <span style="font-style: italic;"><i>Rente en lijst</i></span>, <span style="font-style: italic;"><i>Onderwerp</i></span>, en <span style="font-style: italic;"><i>verticaal</i></span>) zijn beschikbaar via de [!DNL Google Ads] interface. Als u de [!DNL Google Ads] interface om het bieden door een andere afmeting te vormen, wordt die waarde getoond, maar u kunt niet die dimensies selecteren of ingaan hier.</p><p><b>Opmerking:</b></p><ul><li><p>Als je op trefwoord biedt, maak je trackingsjablonen op trefwoordniveau. Als je op plaatsing biedt, maak je ook trackingsjablonen op plaatsingsniveau. Voor alle andere dimensies maakt u volgsjablonen op advertentieniveau.</p></li><li><p>Wanneer u biedt met een niet-ondersteunde dimensie (leeftijd, geslacht, interesse en lijst of onderwerp), optimaliseert Zoeken, Sociaal en Handel biedingen niet voor de dimensie en wordt alle toewijzing toegepast op de advertentiegroep.</p></li><li><p>Advertenties op het onderzoeksnetwerk gebruiken altijd sleutelwoordbiedingen.</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>(Alleen winkelcampagnes) De prioriteit waarmee de campagne wordt gebruikt wanneer meerdere campagnes hetzelfde product adverteren:  <span style="font-style: italic;"><i>[!UICONTROL Low]</i></span> (standaard voor nieuwe campagnes), <span style="font-style: italic;"><i>[!UICONTROL Medium]</i></span>, of <span style="font-style: italic;"><i>[!UICONTROL High]</i></span>.</p><p>Wanneer hetzelfde product in meer dan één campagne is opgenomen, gebruikt het advertentienetwerk eerst de campagneprioriteit om te bepalen welke campagne (en het bijbehorende bod) in aanmerking komt voor de advertentieveiling. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel. |
| [!UICONTROL Merchant ID] | (Winkelcampagnes en publiekscampagnes die alleen zijn gekoppeld aan een commerciële feed) De klant-id van het zakelijke account waarvan de producten voor de campagne worden gebruikt. |  |
| [!UICONTROL Sales Country] | (Alleen winkelcampagnes; alleen-lezen voor bestaande campagnes) Het land waar de producten van de campagne worden verkocht. Omdat de producten met doellanden worden geassocieerd, bepaalt dit het plaatsen welke producten in de campagne worden geadverteerd. |
| [!UICONTROL Product Scope Filter] | (Campagnes die het [!DNL Google Ads] het winkelnetwerk slechts) de producten in uw [!DNL Google Merchant Center] account waarvoor winkeladvertenties voor de campagne kunnen worden gemaakt. U kunt maximaal zeven productafmetingen en kenmerkcombinaties ingaan waarop om uw producten te filtreren, gebruikend het formaat dimensi=attribute. Scheid meerdere filters met een scheidingsteken &quot;>>&quot;. Voor een lijst met beschikbare productafmetingen raadpleegt u &quot;[Productfilters voor winkelcampagne](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;</p><p>Voorbeeld: &quot;Categorie L1=dieren>>Categorie L2=pet-benodigdheden>>Merk=Acme-dierenbenodigdheden&quot;</p><p>Gebruik de waarde om de bestaande waarden te verwijderen <span class="Code">[delete]</span> (inclusief de haakjes).</p> |
| [!UICONTROL Languages] | <p>(Alleen zoek- en weergavenetwerken) De doeltalen voor advertenties in de campagne.</p><p>Als u geen waarde voor of dit gebied of [!UICONTROL Geo Targeting] in het veld voor een nieuwe campagne worden de standaardtalen bepaald door de valuta die voor de account is opgegeven, behalve dat campagnes met valuta&#39;s die niet aan specifieke talen zijn toegewezen (bijvoorbeeld EUR), op alle talen zijn gericht. Als u voor dit veld geen waarde opgeeft, maar een waarde opgeeft in het veld [!UICONTROL Geo Targeting] veld voor een nieuwe campagne, standaard ingesteld op <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>. Als u dit veld leeg laat voor een bestaande campagne, blijft de bestaande waarde behouden.</p><p>Als u alle talen als doel wilt instellen, voert u <span style="font-style: italic;">&lt;i span=&quot;&quot; id=&quot;1&quot; translate=&quot;no&quot; />. [!UICONTROL >All]</i></span> Als u specifieke talen als doel wilt instellen, voert u waarden in die door puntkomma&#39;s worden gescheiden. Hiervoor gebruikt u <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] taalnamen</a> (zoals <span style="font-style: italic;"><i>Engels;Japans</i></span>, die wordt vervangen door de juiste numerieke codes) of door numerieke codes (zoals <span style="font-style: italic;"><i>1000;1005</i></span>). De waarden zijn niet hoofdlettergevoelig.</p> |
| [!UICONTROL Location] | Een geografische locatie waar advertenties voor de campagne moeten worden geplaatst of waar advertenties moeten worden uitgesloten. Als u geen waarden voor dit veld of het veld Talen voor een nieuwe campagne invoert, bepaalt de valuta die voor de account is opgegeven de standaardlocaties, behalve dat campagnes met valuta&#39;s die niet aan specifieke locaties zijn toegewezen (bijvoorbeeld EUR), op alle locaties worden gericht. Als u voor dit veld geen waarde opgeeft, maar een waarde opgeeft in het veld [!UICONTROL Languages] veld voor een nieuwe campagne, dan is dit standaard <i>[!UICONTROL All]</i>. Als u dit veld leeg laat voor een bestaande campagne, blijft de bestaande waarde behouden.</p><p>Als u een specifieke locatie als doel wilt instellen, gebruikt u een van de volgende [[!DNL Google Ads] locatienamen](https://developers.google.com/adwords/api/docs/appendix/geotargeting) (die worden vervangen door de juiste numerieke code) of locatiecodes:</p><ul><li><p>Landen/gebieden: geef de naam van het land/gebied op (bijvoorbeeld <span style="font-style: italic;"><i>Verenigde Staten;Japan</i></span>) of de numerieke codes (zoals <span style="font-style: italic;"><i>2840;2392</i></span>).</p></li><li><p>Staten/provincies/regio&#39;s: geef de naam van de staat/provincie/regio op met de bijbehorende afkortingen voor land/gebied (zoals <span style="font-style: italic;"><i>Tokio, JP;New York, VS</i></span>) of de numerieke codes (zoals <span style="font-style: italic;"><i>20636;2167</i></span>).</p></li><li><p>Niet-Amerikaanse steden: voer de naam van de stad, de naam van de provincie/regio en de afkortingen land/gebied in (zoals <span style="font-style: italic;"><i>Adachi, Tokio, JP;Kita, Tokio, JP</i></span>), of de numerieke codes (zoals <span style="font-style: italic;"><i>1028850;1009293</i></span>)</p></li><li><p>Amerikaanse metro-gebieden: voer de namen van steden, staten en landen in (zoals <span style="font-style: italic;"><i>Buffalo NY, VS;New York NY, VS</i></span>) of de numerieke codes (zoals <span style="font-style: italic;"><i>514;501</i></span>).</p></li></ul><p>Als u een locatie wilt uitsluiten, plaatst u een minteken (`-`), zoals <span style="font-style: italic;"><i>-Japan</i></span>.</p><p><b>Opmerking:</b> De waarden zijn niet hoofdlettergevoelig.</p> |
| [!UICONTROL Location Type] | (Wanneer u een locatie opneemt) De [locatietype](https://developers.google.com/google-ads/api/data/geotargets). |
| [!UICONTROL Device] | Een apparaattype waarvoor biedaanpassingen worden uitgevoerd op campagne- of advertentieniveau: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i>, of <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | <p>(Wanneer u een [!UICONTROL Location], [!UICONTROL Device], of [!UICONTROL RLSA] target) Of u de biedingen voor advertenties op een specifieke locatie, op een specifiek apparaattype of met een specifiek doelpubliek wilt aanpassen:</p><ul><li><p>Voer 0 in om het trefwoordniveaubod te gebruiken (verschil van 0%). Voor nieuwe doelen kunt u deze ook leeg laten.</p></li><li><p>Als u een ander bod voor dit doel wilt gebruiken, voert u het percentage in waarmee u de biedingen wilt verhogen of verlagen.</p></li><ul><li><p>Voor locatie en doelstellingen RLSA, omvatten de geldige percentages van -90 tot 900.</p></li><li><p>Voor correcties bij het bieden van een apparaat zijn geldige percentages:</p></li><ul><li><p>(Campagnes)-100 (om niet te bieden voor advertenties op het apparaattype) of van -90 tot 900.</p></li><li><p>(Toevoegingsgroepen) -100 voor smartphones en tablets (om niet te bieden voor het apparaattype) en van -90 tot 900 voor alle apparaattypen.</p></li></ul></ul><li><p>(Bestaande campagnes en advertentiegroepen) Laat dit leeg als u de bestaande correctie voor biedingen wilt gebruiken.</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | (Opgenomen in gegenereerde bulksbladen ter informatie) De alleen-lezen-bodaanpassing die Adobe aanbeveelt voor een locatiedoel op campagnereniveau of een RLSA. Deze wordt alleen berekend wanneer de campagne zich in een portfolio met een gewogen inkomstendoelstelling bevindt (niet de [!UICONTROL Maximize Clicks] (doelstelling) en de campagne bevat ten minste twee locatiedoelen of RLSA&#39;s met ten minste vijf klikken of 5 USD aan kosten in de afgelopen 90 dagen.</p><p>Als u een plaatsdoel of RLSA manueel wilt uitgeven om de geadviseerde waarde te gebruiken, wacht minstens twee weken nadat u het plaatsdoel of RLSA creeert om voor voldoende gegevensinzameling toe te staan, en verandert niet de waarde meer dan eens per week. |
| [!UICONTROL Device Targets] | <p>(Alleen verouderde campagnetypen) De apparaten waarop de advertentie kan worden weergegeven: <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Computers]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Smartphones]</i></span>, of <span style="font-style: italic;"><i>[!UICONTROL Tablets]</i></span>. Voor nieuwe campagnes is de standaardwaarde <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>.</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | (Alleen oudere campagnetypen; van toepassing wanneer de apparaatdoelen &quot;Smartphones&quot; of &quot;Tablets&quot; bevatten) De besturingssystemen waarop de advertentie kan worden weergegeven: <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Android]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL iOS]</i></span>, of <span style="font-style: italic;"><i>[!UICONTROL Palm]</i></span>. Voor nieuwe campagnes is de standaardwaarde <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>.</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>(Alleen oudere campagneretypen; van toepassing wanneer de [!UICONTROL Device Targets] include &quot;[!UICONTROL All]&quot; of &quot;[!UICONTROL Smartphones]&quot;) Mobiele dragers waarop de smartphones kunnen worden aangesloten: <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>of een of meer door &lt;c span=&quot;&quot; id=&quot;4&quot; translate=&quot;no&quot; />code van drager</i></span>>,&lt;<span style="font-style: italic;"><i>landcode</i></span>> (zoals T-Mobile, VS) met de lijst van <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">beschikbare vervoerders en codes voor [!DNL Google Ads]</a>. <span style="font-style: italic;"><i> Scheid meerdere dragers met puntkomma&#39;s (zoals T-Mobile,US;T-Mobile,GB). Voor nieuwe campagnes is de standaardwaarde <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>.</p> |
| [!UICONTROL Ad Group Name] | <p>De unieke naam die een advertentiegroep identificeert. De maximumlengte is 255 tekens. Witte tekens die naast elkaar staan, worden niet opgeslagen (zoals &#39;Groep 1 toevoegen&#39; wordt bijvoorbeeld opgeslagen als &#39;Groep 1 toevoegen&#39;). Dit veld is niet van toepassing op sitelinks op campagneniveau of apparaatdoelen op campagneniveau.</p> |
| [!UICONTROL Ad Group Type] | <p>Het type advertentiegroep: <i>[!UICONTROL Discovery]</i> (alleen voor opsporingscampagnes), <i>[!UICONTROL Display]</i> (voor weergavecampagnes) <i>[!UICONTROL Search Dynamic]</i> (voor uitgebreide dynamische zoekopdrachten), <i>[!UICONTROL Search Standard]</i> (voor zoekopdrachten), <i>[!UICONTROL Shopping Product]</i> (voor winkeladvertenties), <i>[!UICONTROL Shopping Showcase]</i> (maken en bewerken wordt niet ondersteund), of <i>[!UICONTROL Unknown]</i>.</p> |
| [!UICONTROL Max CPC] | <p>(Alleen CPC-campagnes) De maximale kosten per klik (CPC). Dit is het hoogste bedrag dat wordt betaald voor een advertentie op het advertentienetwerk, met of zonder monetaire symbolen en interpunctie. U kunt waarden instellen voor advertentiegroepen en trefwoorden, productgroepen en dynamische zoekdoelen. De standaardinstelling voor een nieuw trefwoord wordt overgenomen van het niveau van de advertentiegroep. Voor productgroepen kunt u waarden instellen voor de laagste niveau van de productgroep. De standaardinstelling voor een nieuwe laag wordt overgenomen van de bovenliggende laag.</p><p>Voor bestaande productgroepen en dynamische zoekdoelen in geoptimaliseerde portfolio&#39;s zijn updates slechts één dag effectief en worden ze tijdens de volgende optimalisatiecyclus overschreven.</p> |
| [!UICONTROL Max Content CPC] | <p>(Alleen CPC-campagnes) De maximale kosten voor inhoud per klik (CPC). Dit is het hoogste bedrag dat wordt betaald voor een advertentie via een netwerksite voor weergave, met of zonder monetaire symbolen en interpunctie. U kunt waarden instellen en bewerken op het niveau van de advertentiegroep in campagnes die niet op plaatsing zijn gericht.</p> |
| [!UICONTROL Audience Target Method] | <p>(Alleen campagnes op het zoeknetwerk en bestaande, alleen-lezen [!DNL Gmail] campagnes op het vertoningsnetwerk) Of:</p><ul><li><p><span style="font-style: italic;"><i>[!UICONTROL Target and Bid]</i></span>: alleen advertenties weergeven voor gebruikers die zijn gekoppeld aan doelgroepen die ook voldoen aan andere doelen voor de advertentiegroep.</p></li><li><p><span style="font-style: italic;"><i>[!UICONTROL Bid Only]</i></span>: Om zelfs advertenties te tonen aan mensen die niet geassocieerd zijn met doelpubliek zolang ze voldoen aan andere doelen op groepsniveau.</p><p>U kunt de kans echter vergroten dat advertenties bij een bepaald publiek worden getoond door voor dat publiek hogere biedingen in te stellen.</p></li></ul> |
| [!UICONTROL Keyword] | De trefwoordtekenreeks. De maximumlengte is 80 tekens en niet meer dan 10 woorden en kan alleen letters, cijfers en de volgende speciale tekens bevatten: spatie `# $ & _ - " [ ] ' + . / :`</p><p><b>Opmerking:</b></p><ul><li><p>Als u een trefwoord op advertentiegroep- of campagnereniveau wilt uitsluiten, stelt u de optie [!UICONTROL Match Type] tot <span style="font-style: italic;"><i>[!UICONTROL Negative]</i></span>. Als de rij de naam van de advertentiegroep bevat, wordt het trefwoord uitgesloten voor de advertentiegroep. Als de rij niet de naam van de advertentiegroep omvat, wordt het sleutelwoord uitgesloten voor de volledige campagne.</p></li><li><p>Een [!DNL Google Ads] het bestaande trefwoord of het overeenkomende type wordt verwijderd en er wordt een nieuw trefwoord gemaakt.</p></li></ul> |
| [!UICONTROL Placement] | (Campagnes die inhoud gebruiken stemmen slechts overeen) Een plaatsing in het vertoningsnetwerk waarop uw advertenties kunnen worden getoond. Geef een van de volgende opties op:</p><ul><li class="p"><p>Website: Voer een geldige URL in. Het kan een top-level domein, eerste-vlakke subdomein, of domein met één enkele foldernaam zijn. De URL kan geen vraagteken (?) bevatten. Voorbeelden:<span class="Code"><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</span></p></li><li class="p"><p>Een advertingspositie op een specifieke pagina: De indeling gebruiken `<URL> >> <location,sublocation>` (zoals `finance.google.com >> Company pages,Top right`).</p></li><li class="p"><p>Een onderwerpcategorie: de syntaxis gebruiken `<category::<category> > <subcategory>` enzovoort (zoals `category::Industries > Energy & Utilities > Oil & Gas`).</p></li></ul><p><b>Opmerking:</b> Als u een plaatsing op advertentiegroep- of campagnereniveau wilt uitsluiten, stelt u de optie [!UICONTROL Match Type] tot <span style="font-style: italic;"><i>[!UICONTROL Negative]</i></span>. Als de rij de naam van de advertentiegroep bevat, wordt de plaatsing uitgesloten voor de advertentiegroep. Als de rij de naam van de advertentiegroep niet bevat, wordt de plaatsing uitgesloten voor de gehele campagne.</p> |
| [!UICONTROL Auto Target Expression] | <p>(Vereist als de instelling voor de campagne &quot;[!UICONTROL Use my website contents to target my ads]&quot; is niet ingeschakeld; anders optioneel) Dynamische zoekdoelen voor de advertentiegroep.</p><p>Gebruik voor alle doelen een sterretje (*).</p><p>Als u maximaal drie dynamische zoekcriteria als doel wilt instellen, gebruikt u de indeling `<category>=<target>`, waarbij `<category>` kan een van de onderstaande rubrieken bevatten. Meerdere doelen samenvoegen voor een afzonderlijke categorie met &quot;\[spatie\]&quot; en \[spatie\]&quot; en meerdere categorieën samenvoegen met &quot;[spatie] en [spatie]&quot;.</p><ul><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Category]</i></span>: Uitgebreide dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met een specifieke [!DNL Google Ads] inhoudscategorie.</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL URL]</i></span>: Hiermee geeft u uitgebreide dynamische zoekopdrachten voor geïndexeerde pagina&#39;s met een specifieke URL weer, waarbij de waarde overal in de URL kan worden opgenomen.</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Page Title]</i></span>: Hiermee geeft u uitgebreide dynamische zoekadvertenties weer voor geïndexeerde pagina&#39;s met specifieke tekst in de paginatitel.</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Page Content]</i></span>: Hiermee geeft u uitgebreide dynamische zoekadvertenties weer voor geïndexeerde pagina&#39;s met specifieke inhoud.</p></li></ul><p>Voorbeeld: url=shoes.example.com en page title=schoeisel</p> |
| [!UICONTROL Parent Product Groupings] | De hiërarchie van bovenliggende productgroepen.<br><br>Voorbeeld: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>De productgroep (zoals &quot;brand=acme&quot; of &quot;Alle producten&quot;).</p><p><b>Opmerking:</b></p><ul><li><p>Wanneer een opgegeven productgroep niet bestaat in het dialoogvenster [!UICONTROL Parent Product Groupings] de hiërarchie, het Onderzoek, de Sociale, &amp; Handel leidt tot om het even welke delen van de hiërarchie die nodig zijn.</p></li><li><p>Met Zoeken, Sociaal, en Handel wordt automatisch een &quot;[!UICONTROL All Products]&quot; groeperen wanneer u een advertentiegroep maakt in een [!DNL Google Ads] Winkelcampagne met een standaardbod ingesteld op het standaardbod van de advertentiegroep. Met Zoeken, Sociaal, en Handel wordt automatisch een &quot;[!UICONTROL Everything Else]&quot; groeperen met het standaardbod van de advertentiegroep op elk niveau van de hiërarchie van de productgroep. U kunt deze standaardgroepen nog steeds expliciet maken en ze uitsluiten of hun biedingen wijzigen.</p></li><li><p>Elke advertentiegroep kan maximaal acht lagen productgroepen bevatten, waaronder &quot;[!UICONTROL All Products]&quot; en zeven andere lagen.</p></li></ul> |
| [!UICONTROL Partition Type] | Het partitietype voor de productgroep: <i>onderverdeling</i> (als het onderliggende productgroepen heeft) of <i>eenheid</i> (als het geen onderliggende productgroepen heeft). |
| [!UICONTROL Match Type] | <p>Voor dynamisch zoekdoel of productgroepen: de optie voor trefwoordafstemming voor het dynamische zoekdoel of de dynamische productgroep: <i>[!UICONTROL Dynamic Ad Target]</i> (standaard voor nieuwe dynamische zoekdoelen), <i>[!UICONTROL Product Group]</i> (standaard voor nieuwe productgroepen) of <i>[!UICONTROL Negative Product Group]</i> (om een productgroep uit te sluiten).</p><p>Voor trefwoorden: de optie voor trefwoordafstemming voor het trefwoord: <span style="font-style: italic;"><i>[!UICONTROL Broad]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Phrase]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Exact]</i></span>, of <span style="font-style: italic;"><i>[!UICONTROL Negative]</i></span> (om een trefwoord of een plaatsing op het weergavenetwerk uit te sluiten); productgroepen die worden gebruikt met winkeladvertenties, hebben een overeenkomend type <span style="font-style: italic;"><i>[!UICONTROL Product Group]</i></span>. Als u <span style="font-style: italic;"><i>[!UICONTROL Negative]</i></span>, moet u ook het type opnemen dat moet worden uitgesloten (bijvoorbeeld Negatieve zin).</p><p>Voor nieuwe trefwoorden is de standaardwaarde <span style="font-style: italic;"><i>[!UICONTROL Broad]</i></span>. Een waarde voor het type van gelijke of sleutelwoordidentiteitskaart wordt vereist slechts om een sleutelwoord met veelvoudige gelijke types uit te geven.</p><p><b>Opmerking:</b></p><ul><li><p>Identieke typen zijn niet van toepassing op uitgebreide dynamische zoekadvertenties, die geen trefwoorden gebruiken.</p></li><li><p>Het overeenkomentype voor een [!DNL Google Ads] verwijdert het bestaande trefwoord en maakt een nieuw trefwoord.</p></li><li><p>Kies bij Breedte overeenkomende modifier &quot;Breed&quot; en voeg een + in vóór elk woord in het trefwoord waarvoor nauwe varianten vereist zijn (zoals &quot;+red +schoenen&quot; om nauwe varianten van zowel &quot;rood&quot; als &quot;schoenen&quot; te vereisen). <b>Opmerking:</b> Brede overeenkomende wijzigingstoetsen hebben nu hetzelfde gedrag als woordovereenkomst voor sommige talen en u kunt sinds juli 2021 geen nieuwe trefwoorden voor brede overeenkomsten maken. Zie [[!DNL Google Ads] documentatie](https://support.google.com/google-ads/answer/7042511) voor meer informatie .</p> |
| [!UICONTROL First Page Bid] | (Opgenomen in gegenereerde bulksbladen ter informatie) Het bod dat vereist is om een advertentie op de eerste pagina van de zoekresultaten te plaatsen. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| [!UICONTROL Quality Score] | (Opgenomen in gegenereerde opsommingstekens ter informatie) De huidige kwaliteitsscore die de zoekfunctie aan het trefwoord heeft toegewezen. Deze waarde wordt niet naar het advertentienetwerk gepost.) |
| [!UICONTROL Creative Preferred Devices] | (Tekstadvertenties, uitgebreide dynamische zoekopdrachten en verbeterde sitelinks; optioneel) De apparaattypen waarop u de advertentie wilt weergeven: <span style="font-style: italic;"><i>[!UICONTROL All]</i></span> (de standaardwaarde) of <i>[!UICONTROL Mobile]</i>. Wanneer <i>[!UICONTROL Mobile]</i> wordt opgegeven, probeert het netwerk de advertentie voor gebruikers van mobiele apparaten weer te geven in plaats van voor gebruikers van desktops of tablets. Anders, toont het netwerk de advertentie op om het even welk apparatentype.</p><p><b>Opmerking:</b></p><ul><li><p>Alleen beheerder en [!DNL Adobe] gebruikers van accountmanagers kunnen deze instelling bewerken.</p></li><li><p>Het netwerk garandeert niet dat de advertentie op het voorkeurstype wordt weergegeven.</p></li><li><p>Nieuwe verbeterde sitelinks kunnen alleen worden gemaakt in campagnes met bestaande verbeterde sitelinks of zonder sitelinks.</p></li></ul> |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | (Alleen uitgebreide tekstadvertenties en responsieve zoekadvertenties) De kopregels van een advertentie, elk gescheiden door een verticale pipe ( | ). De maximumlengte voor elk veld van de advertentitel is 30 karakters of 15 dubbel-byte karakters, met inbegrip van om het even welke dynamische teksten (zoals de waarden van sleutelwoorden en adverteerders).</p><p>Voor responsieve zoekopdrachten [!UICONTROL Ad Title], [!UICONTROL Ad Title 2], en [!UICONTROL Ad Title 3] zijn vereist en alle andere titelvelden zijn optioneel. Als u de bestaande waarde voor een niet-vereist veld wilt verwijderen, gebruikt u de waarde <code>[delete]</code> (inclusief de haakjes).</p><p>Voeg voor responsieve zoekadvertenties een advertentieklanker in met de volgende indeling: `{CUSTOMIZER.AdCustomizerName:DefaultText}`, zoals `{CUSTOMIZER.Discount:10%}`</p><p>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen en uitbreiden, die [!DNL Google Ads] afgeschaft in juni 2022. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>(Alleen responsieve zoekopdrachten; optioneel) Een positie waarop de bijbehorende advertentietak moet worden vastgezet: `[null]` (geen waarde waardoor de titel van de advertentie voor alle posities in aanmerking komt), <i>1</i>, <i>2</i>, of <i>3</i>. Als [!UICONTROL Ad Title Position] heeft een waarde van 1, dan verschijnt de Titel van de Advertentie slechts in Positie 1. Standaard zijn alle advertentitels null (geen waarden).</p><p>Gebruik de waarde om de bestaande waarde te verwijderen <code>[delete]</code> (inclusief de haakjes).</p><p><b>Opmerking:</b> U kunt meerdere advertentitels vastzetten op dezelfde positie. In het advertentienetwerk wordt een van de advertentietitels gebruikt die op de positie zijn vastgezet. Titels die op positie 3 zijn vastgezet, worden mogelijk niet met de advertentie weergegeven.</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>(Alleen uitgebreide dynamische zoekopdrachten, uitgevouwen tekstadvertenties en responsieve zoekadvertenties) De hoofdtekst van een advertentie. De maximumlengte voor elk beschrijvingsveld is 90 tekens of 45 double-byte tekens, inclusief alle dynamische tekst (zoals de waarden van trefwoorden en adverteerders).</p><p>Voeg voor responsieve zoekadvertenties een advertentieklanker in met de volgende indeling: `{CUSTOMIZER.AdCustomizerName:DefaultText}`, zoals `{CUSTOMIZER.Discount:10%}`</p><p>Gebruik voor uitgebreide dynamische zoekopdrachten [!UICONTROL Description Line 1] en [!UICONTROL Description Line 2] alleen. <b>Opmerking:</b> Als u voor dit advertentietype wijzigingen aanbrengt in de advertentie, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie.</p><p>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen en uitbreiden, die [!DNL Google Ads] afgeschaft in juni 2022.</p><p>Voor responsieve zoekopdrachten [!UICONTROL Description Line 1] en [!UICONTROL Description Line 2] verplicht zijn, en [!UICONTROL Description Line 3] en [!UICONTROL Description Line 4] zijn optioneel. Gebruik de waarde om de bestaande waarde te verwijderen <code>[delete]</code> (inclusief de haakjes).</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Alleen responsieve zoekopdrachten; optioneel) Een positie waarop de bijbehorende beschrijving moet worden vastgezet: `[null]` (geen waarde waardoor de beschrijving voor alle posities in aanmerking komt), <i>1</i>, <i>2</i>, of <i>3</i>. Als [!UICONTROL Description 1 Position] heeft een waarde van 1, dan [!UICONTROL Description 1] alleen op positie 1 wordt weergegeven. Standaard zijn geen beschrijvingen vastgezet op een positie.</p><p>Gebruik de waarde om de bestaande waarde te verwijderen `[delete]` (inclusief de haakjes).</p><p><b>Opmerking:</b> U kunt meerdere beschrijvingen vastzetten op dezelfde positie. Het advertentienetwerk gebruikt één van de beschrijvingen die aan de positie worden vastgezet. Beschrijvingen die op positie 2 zijn vastgezet, mogen niet met de advertentie worden getoond. |
| [!UICONTROL Display URL] | De URL die is opgenomen in de advertentie.<br><br>Voor uitgebreide dynamische zoekopdrachten [!DNL Google Ads] Hiermee wordt deze waarde dynamisch gegenereerd vanuit het websitedomein. U hoeft geen waarde in te voeren.<br><br>Voor responsieve zoekopdrachten hoeft u geen waarde in te voeren. De weergave-URL wordt automatisch opgehaald uit het domein in de uiteindelijke URL. U kunt de URL desgewenst aanpassen met de velden Pad 1 en Pad 2.<br><br>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen en uitbreiden, die [!DNL Google Ads] afgeschaft in juni 2022.<br><br><b>Opmerking:</b> (Accounts met definitieve URL&#39;s) De domeinnamen in de weergave-URL en de uiteindelijke URL moeten overeenkomen.</p> |
| [!UICONTROL Display Path 1] | <p>(Uitgebreide tekstadvertenties<span> en responsieve zoekopdrachten</span> alleen)</p><p>(Optioneel) Tekst die wordt toegevoegd aan de weergave-URL en die automatisch wordt opgehaald uit de uiteindelijke URL. Het wordt voorafgegaan in de URL door een slash (/). Een pad mag geen forward slash (/) of newline (\n) tekens bevatten. De maximumlengte is 15 tekens of 7 double-byte tekens.</p><p>Als u een advertentieklanter wilt invoegen, gebruikt u de volgende indelingen, waarbij `Default text` is een optionele waarde die moet worden ingevoegd wanneer uw feed-bestand geen geldige waarde bevat:&lt; `{CUSTOMIZER.AdCustomizerName:Default text}`, zoals `{CUSTOMIZER.Discount:10%}`</p><p>Als [!UICONTROL Display Path 1] is &quot;deals&quot;, dan is de weergave-URL &lt;<i>URL weergeven</i>>/deals, zoals www.example.com/deals.</p><p>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen en uitbreiden, die [!DNL Google Ads] afgeschaft in juni 2022.</p> |
| [!UICONTROL Display Path 2] | Een tweede weergavepad. Zie de vermelding voor [!UICONTROL Display Path 1].<br><br>Voorbeeld: if [!UICONTROL Display Path 1] is &quot;deals&quot; en [!UICONTROL Display Path 2] is &quot;lokaal&quot;, dan is de weergave-URL &lt;<i>URL weergeven</i>>/deals/local, zoals www.example.com/deals/local.</p><p>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen en uitbreiden, die [!DNL Google Ads] afgeschaft in juni 2022.</p> |
| [!UICONTROL Promotion Line] | (Alleen advertenties voor aanbiedingen van producten) Een optionele promotielijn die in de zoekresultaten bij de aanbieding van het product moet worden gevoegd. De maximumlengte is 45 tekens.</p><p>De promotielijn kan op verschillende plaatsen ten opzichte van de advertentie (zoals onder de advertentie) verschijnen, afhankelijk van waar de advertentie op de pagina wordt weergegeven. |
| [!UICONTROL Link Name] | <p>De sitelink-tekst. Het kan maximaal 25 tekens bevatten.</p><p>Voor nieuwe sitelinks moet u de naam van de campagne opnemen in de sitelink-rij. Voor sitelinks op advertentieniveau moet u ook de naam van de advertentiegroep opnemen.</p><p><b>Opmerking:</b> Bestaande tekst van 35 tekens wordt nog wel weergegeven in advertenties op desktops en tablets, maar niet op mobiele apparaten.</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | (Alleen voor bestaande installatielocaties voor apps) Het besturingssysteem waarop de mobiele toepassing wordt uitgevoerd: <i>Android™</i> of <i>ios</i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | (Alleen bestaande installatieladingen voor apps) <p>De toepassings-id of pakketnaam. |
| [!UICONTROL Mobile App Name (Google Adwords)] | (Alleen voor bestaande installatiemonsters) De naam van de toepassing. |
| [!UICONTROL Start Date] | <p>(Alleen verbeterde sitelinks) De eerste datum waarop biedingen mogen worden uitgebracht voor de sitelink, in de tijdzone van de adverteerder en in een van de volgende formaten: <span style="font-style: italic;"><i>d/m/yyyy</i></span>, <span style="font-style: italic;"><i>d/m/yy</i></span>, <span style="font-style: italic;"><i>d-m-yyyy</i></span>, of <span style="font-style: italic;"><i>d-m-yy</i></span>. De standaard voor nieuwe verbeterde sitelinks is de huidige dag.</p><p><b>Opmerking:</b> Nieuwe verbeterde sitelinks kunnen alleen worden gemaakt in campagnes met bestaande verbeterde sitelinks of zonder sitelinks.</p> |
| [!UICONTROL End Date] | <p>(Alleen verbeterde sitelinks) De laatste datum waarop biedingen voor de sitelink mogen worden uitgebracht, in de tijdzone van de adverteerder en in een van de volgende formaten:  <span style="font-style: italic;"><i>d/m/yyyy</i></span>, <span style="font-style: italic;"><i>d/m/yy</i></span>, <span style="font-style: italic;"><i>d-m-yyyy</i></span>, of <span style="font-style: italic;"><i>d-m-yy</i></span>. De standaardwaarde is geen (geen einddatum).</p><p><b>Opmerking:</b> Nieuwe verbeterde sitelinks kunnen alleen worden gemaakt in campagnes met bestaande verbeterde sitelinks of zonder sitelinks.</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | (Alleen bestaande installatieladingen voor apps)</p><p>(Optioneel) Voorkomen [!DNL Google Ads] van het weergeven van de advertentie naar tabletgebruikers. Waarden kunnen <i>ja</i> en <i>nee</i>. |
| [!UICONTROL Landing Page Suffix] | Alle parameters die aan het einde van de uiteindelijke URL&#39;s moeten worden toegevoegd om informatie bij te houden. Voorbeeld: `param2=value1&param3=value2`<br><br>Zie &quot;[Opmaak voor het bijhouden van klikken voor [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md).&quot;<br><br>De laatste URL-achtervoegsels op lagere niveaus overschrijven het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Om een achtervoegsel op het niveau van de ad groep of lager te vormen, gebruik [!DNL Google Ads] editor. |
| [!UICONTROL Tracking Template] | De volgende sjabloon, die alle buiten-landingsdomein omleidt en het volgen parameters specificeert en definitieve URL in een inbedt [!DNL ValueTrack] parameter. De het volgen malplaatje op het meest korrelige niveau (met sleutelwoord als meest korrelig) treedt de waarden op alle hogere niveaus met voeten.<br><br>Voor het bijhouden van Adoben Advertising voor conversie, die wordt toegepast wanneer de instellingen voor de campagne &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel voegt automatisch zijn eigen omleiding en volgcode toe wanneer u sparen het verslag.<br><br>Voer een waarde in voor omleidingen en bijhouden door derden. Voor een lijst met [!DNL ValueTrack] parameters om definitieve URLs in het volgen malplaatjes aan te geven, zie de &quot;het Volgen malplaatjes slechts&quot;parameters in de sectie over &quot;Beschikbaar [!DNL ValueTrack] Parameters&quot; in de [[!DNL Google Ads] documentatie](https://support.google.com/google-ads/answer/2375447).<br><br>Gebruik de waarde om de bestaande waarde te verwijderen `[delete]` (inclusief de haakjes). |
| [!UICONTROL Base URL/Final URL] | De bestemmingspagina URL waarnaar de gebruikers van de onderzoeksmotor worden genomen wanneer zij uw advertentie klikken, met inbegrip van om het even welke toevoegingsparameters die voor de campagne of de rekening worden gevormd. Basis/definitieve URLs op het sleutelwoordniveau treedt die op het advertentieniveau en hoger met voeten.<br><br>Gebruik de waarde om de bestaande waarde te verwijderen `[delete]` (inclusief de haakjes). |
| [!UICONTROL Destination URL] | (Opgenomen in gegenereerde bulksbladen voor informatiedoeleinden; niet gepost naar het zoekprogramma) Voor accounts met bestemmings-URL&#39;s is dit de URL die een advertentie koppelt aan een basis-URL/bestemmingspagina op de website van de adverteerder (soms via een andere site die de klik bijhoudt en de gebruiker vervolgens omleidt naar de bestemmingspagina). Het omvat om het even welke toevoegingsparameters die voor de Onderzoek, Sociale, &amp; de campagne of de rekening van de Handel worden gevormd. Als u URL&#39;s voor bijhouden hebt gegenereerd, is dit gebaseerd op de volgende parameters in uw accountinstellingen en campagnemontages. Als u specifieke parameters voor zoekprogramma&#39;s hebt toegevoegd, kunnen deze worden vervangen door de equivalente parameters voor Zoeken, Sociale &amp; Handel.<br><br>Voor accounts met uiteindelijke URL&#39;s geeft deze kolom dezelfde waarde weer als de kolom Basis-URL/Definitieve URL. |
| [!UICONTROL Custom URL Param] | Gegevens ter vervanging van de `{custom_code}` dynamische variabele wanneer de variabele is opgenomen in de volgende parameters voor de instellingen van de zoekaccount of campagne. Als u de aangepaste waarde in de URL voor bijhouden wilt invoegen, moet u het bestand met de opsommingstekens uploaden met de optie URL&#39;s voor reeksspatiëring genereren. |
| [!UICONTROL Creative Type] | De advertentievorm: <i>[!UICONTROL Text ad]</i>, <i>[!UICONTROL Expanded text ad]</i>, <i>[!UICONTROL Dynamic search ad]</i> (afgekeurd ad type), <i>[!UICONTROL Expanded Dynamic Search ad]</i>, &lt;[!UICONTROL i>Display ad]</i>, <i>[!UICONTROL App Install ad]</i> (afgekeurd) <i>[!UICONTROL Image]</i>, <i>[!UICONTROL Product ad<]/i> (winkeladvertenties), of <i>[!UICONTROL Responsive search ad]</i>. De standaardwaarde voor nieuwe advertenties is <i>[!UICONTROL Text ad]</i>.<br><br>Vereist om de status van een productadvertentie te maken of te bewerken. |
| [!UICONTROL Param1] | <p>De numerieke waarde van de `{param1}` ad parameter, die kan worden opgenomen in de advertentie-kopie of weergave-URL voor elke advertentie in het bulksbladbestand. De maximumlengte is 25 tekens en u kunt de volgende niet-numerieke tekens opnemen:</p><ul><li><p>De waarde kan worden voorafgegaan of toegevoegd met een valutasymbool of -code. Bijvoorbeeld: `£2.000,00` en `2000GBP` zijn geldig.</p></li><li><p>De waarde kan een komma (`,`) of punt (`.`) als scheidingsteken, met een optionele punt (`.`) of komma (`,`) voor fractionele waarden. Bijvoorbeeld: `1,000.00` en `2.000,10` zijn geldig.</p></li><li><p>De waarde kan worden voorafgegaan of met een percentageteken worden toegevoegd (`%`), plusteken (`+`), of minteken (`- `). Bijvoorbeeld: `20%`, `208+`, en `-42.32` zijn geldig.</p></li><li><p>Twee getallen kunnen worden ingesloten met een slash. Bijvoorbeeld: `4/1` en `0.95/0.45` zijn geldig.</p></li></ul><p>Gebruik de waarde om de bestaande waarde te verwijderen `[delete]` (inclusief de haakjes).</p> |
| [!UICONTROL Param2] | De numerieke waarde van de `{param2}` ad parameter, die kan worden opgenomen in de advertentie-kopie of weergave-URL voor elke advertentie in het bulksbladbestand. Zie de ingang voor Param1 voor meer informatie. |
| [!UICONTROL Audience] | De lijst voor opnieuw op de markt brengen voor onderzoeksadvertenties (RLSA) richt publiek of uitgesloten publiek voor de campagne of de ad groep. Geef op of dit een doel of een uitsluiting is in het veld &quot;Doeltype&quot;. |
| [!UICONTROL Target Type] | (Wanneer een publiek wordt gespecificeerd) Of het gespecificeerde publiek is <i>Opname</i> (doel) of <i>Uitsluiting</i>. |
| [!UICONTROL Campaign Status] | De weergavestatus van de campagne: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i> (niet bewerkbaar), of <i>[!UICONTROL Deleted]</i> (alleen bestaande campagnes). De standaardwaarde voor nieuwe campagnes is <i>[!UICONTROL Active]</i>. Voer de waarde in om een actieve of gepauzeerde campagne te verwijderen <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | De weergavestatus van de advertentiegroep: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, of <i>[!UICONTROL Deleted]</i> (alleen bestaande advertentiegroepen). De standaardwaarde voor nieuwe advertentiegroepen is [!UICONTROL Active]. Als u een actieve of gepauzeerde ad-groep wilt verwijderen, voert u de waarde in `Deleted`. |
| [!UICONTROL Keyword Status] | De weergavestatus van het trefwoord: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, of <i>[!UICONTROL Deleted]</i> (alleen bestaande trefwoorden). De standaardwaarde voor nieuwe trefwoorden is [!UICONTROL Active]. Voer de waarde in om een actief of gepauzeerd trefwoord te verwijderen <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | De weergavestatus van de advertentie: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (alleen bestaande advertenties), <i>[!UICONTROL Disapproved]</i> (niet bewerkbaar), of <i>[!UICONTROL Paused]</i>. De standaardwaarde voor nieuwe advertenties is [!UICONTROL Active]. Voer de waarde in om een actieve of gepauzeerde advertentie te verwijderen <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Placement Status] | De status van de plaatsing van de website: <span style="font-style: italic;"><i>[!UICONTROL Active]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Paused]</i></span>, of <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span> (alleen bestaande advertenties). De standaardwaarde voor nieuwe websites is <span style="font-style: italic;"><i>Actief.</i></span> Voer de waarde in om een actieve of gepauzeerde plaatsing te verwijderen <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span>. |
| [!UICONTROL Target Status] | De status van een dynamisch zoekdoel: <span style="font-style: italic;"><i>[!UICONTROL Active]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Paused]</i></span>, of <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span> (alleen bestaande streefcijfers). De standaardinstelling voor nieuwe doelen is <span style="font-style: italic;"><i>Actief.</i></span> Voer de waarde in om een actief of gepauzeerd doel te verwijderen <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span>. |
| [!UICONTROL Product Group Status] | De weergavestatus van de productgroep: <span style="font-style: italic;"><i>[!UICONTROL Active]</i></span> <span>of</span> <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span> (alleen bestaande productgroepen). De standaardwaarde voor nieuwe productgroepen is <span style="font-style: italic;"><i>[!UICONTROL Active]</i></span>. Voer de waarde in om een actieve productgroep te verwijderen <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span>. |
| [!UICONTROL Sitelink Status] | De weergavestatus van de sitelink: <span style="font-style: italic;"><i>Actief of verwijderd</i></span> (alleen bestaande sitelinks). De standaardinstelling voor nieuwe sitelinks is <span style="font-style: italic;"><i>[!UICONTROL Active]</i></span>. Voer de waarde in om een actieve sitelink te verwijderen <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span>. |
| [!UICONTROL Location Status] | De status van het locatiedoel: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande locaties). De standaardwaarde voor nieuwe locaties is [!UICONTROL Active]. Voer de waarde in om een actieve locatie te verwijderen <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL RLSA Target Status] | De status van het doel of de uitsluiting van de RLSA op campagne- of advertentieniveau: <span style="font-style: italic;"><i>[!UICONTROL Active]</i> of [!UICONTROL Deleted]</i></span> (alleen bestaande streefcijfers). De standaardwaarde voor nieuwe doelen of uitsluitingen is <span style="font-style: italic;"><i>[!UICONTROL Active]</i></span>. Voer de waarde in om een actief doel of een actieve uitsluiting te verwijderen <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span>. |
| [!UICONTROL Device Target Status] | <p>De status van het apparaatdoel op campagne- of advertentieniveau: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i>. Voor nieuwe campagnes en advertentiegroepen is de standaardwaarde <i>[!UICONTROL Active]</i>.</p> |
| \[Advertiserspecifieke labelclassificatie\] | (Benoemd voor een advertentiespecifieke labelclassificatie, zoals &quot;Kleur&quot; voor een labelclassificatie genaamd Kleur) Een waarde voor de opgegeven classificatie die aan de entiteit is gekoppeld. U kunt per entiteit slechts één waarde per classificatie opnemen (zoals &quot;rood&quot; voor de labelclassificatie &quot;Kleur&quot; voor campagne A). De maximumlengte is 100 tekens en de waarde kan ASCII- en niet-ASCII-tekens bevatten.<br><br>De classificaties van het etiket en hun etiketwaarden worden toegepast op alle kindcomponenten; de nieuwe componenten die later worden toegevoegd worden automatisch geassocieerd met het etiket. De etiketclassificaties voor productgroepen worden toegepast op het eenheidniveau (het meest korrelige).<br><br>Noch de classificatienaam noch de classificatiewaarde is hoofdlettergevoelig. |
| [!UICONTROL Constraints] | Een beperking die aan de entiteit is toegewezen. U kunt slechts één beperking per entiteit toewijzen.<br><b>>Restricties worden overgeërfd door onderliggende entiteiten, zodat u geen waarden voor onderliggende entiteiten hoeft in te voeren, tenzij u de overgeërfde waarden wilt overschrijven. |
| [!UICONTROL Campaign ID] | De unieke id die een bestaande campagne identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Alleen vereist wanneer u de naam van de campagne wijzigt, tenzij de rij de waarde &quot;[!UICONTROL AMO ID]&quot; voor de campagne . |
| [!UICONTROL Ad Group ID] | De unieke id die een bestaande advertentiegroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Alleen vereist wanneer u de naam van de campagne wijzigt, tenzij de rij de waarde &quot;[!UICONTROL AMO ID]&quot; voor de advertentiegroep. |
| [!UICONTROL Keyword ID] | De unieke id die een bestaand trefwoord identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Vereist slechts wanneer u het sleutelwoord verandert, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>De unieke id die een bestaande advertentie identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Voor responsieve zoekopdrachten is de ID van de advertentie of de AMO-id vereist om advertentiegegevens te bewerken of te verwijderen. Voor alle andere entiteitstypen is de advertentie-id alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met eigenschappen bevat om de advertentie te identificeren of b) en &quot;[!UICONTROL AMO ID]&quot;.&quot; Als u echter geen van de [!UICONTROL Ad ID] noch [!UICONTROL AMO ID]en de kolommen met de eigenschap ad-eigenschap komen overeen met meerdere advertenties. De status voor slechts een van de advertenties verandert dan.</p><p><b>Opmerking:</b> Als u a) en bezitskolommen behalve Status voor een bestaande advertentie uitgeeft, of b) om het even welke gegevens voor een ontvankelijke onderzoeksadvertentie, en u omvat noch [!UICONTROL Ad ID] noch [!UICONTROL AMO ID], wordt er een nieuwe advertentie gemaakt en de bestaande advertentie wordt niet gewijzigd.</p> |
| [!UICONTROL Placement ID] | De unieke id die een plaatsing van een website identificeert. Dit is alleen vereist wanneer u de plaatsing wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de plaatsing te identificeren, of b) en &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Target ID] | De unieke id die een bestaand automatisch doel identificeert. Alleen vereist wanneer u het automatische doel wijzigt of verwijdert, tenzij de rij een &quot;[!UICONTROL AMO ID]&quot; voor het doel. |
| [!UICONTROL Product Group ID] | De unieke id die een bestaande productgroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Dit is alleen vereist wanneer u de productgroep wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de productgroep te identificeren of b) en &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Sitelink ID] | De unieke id die een bestaande sitelink identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Dit is alleen vereist wanneer u de sitelink wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de sitelink te identificeren of b) en &quot;[!UICONTROL AMO ID]&quot;.&quot; Als u echter geen van beide opties opneemt [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID]en de eigenschapskolommen overeenkomen met meerdere sitelinks. De status voor slechts een van de sitelinks wordt dan gewijzigd.</p><p><b>Opmerking:</b> Als u eigenschapkolommen sitelink bewerkt, behalve Status voor een bestaande sitelink, en u geen van beide kolommen [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID], wordt er een nieuwe sitelink gemaakt en de bestaande sitelink wordt niet gewijzigd. |
| [!UICONTROL RLSA Target ID] | De unieke id die een bestaand RLSA-doel of -uitsluiting op campagne- of advertentieniveau identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u het doel of de uitsluiting wijzigt of verwijdert, tenzij de rij een &quot;[!UICONTROL AMO ID]&quot; voor het doel. |
| [!UICONTROL Device Target ID] | <p>De unieke id die een bestaand doel of een bestaande uitsluiting op campagnereniveau of op ad-groepsniveau aangeeft. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Alleen vereist wanneer u het doel wijzigt of verwijdert, tenzij de rij een &quot;[!UICONTROL AMO ID]&quot; voor het doel.</p> |
| [!UICONTROL AMO ID] | (In gegenereerde bulksbladen) Een unieke id die door Adobe wordt gegenereerd voor een gesynchroniseerde entiteit. Voor responsieve zoekopdrachten is de AMO-id vereist om advertenties te bewerken of te verwijderen, tenzij u de advertentie-id opneemt. Als u gegevens voor alle andere entiteitstypen met een AMO-id wilt bewerken, moet de AMO-id de gegevens bewerken of verwijderen, tenzij u de id van de entiteit en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |
| [!UICONTROL EF Error Message] | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van het advertentienetwerk met betrekking tot gegevens in de rij; foutberichten worden opgenomen in [!UICONTROL EF Errors] bestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| [!UICONTROL SE Error Message] | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van het advertentienetwerk met betrekking tot gegevens in de rij; foutberichten worden opgenomen in [!UICONTROL SE Errors] bestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| [!UICONTROL Exemption Request] | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van de namen en tekst van [!DNL Google Ads] reclamebeleid dat een advertentie schendt. |
| [!UICONTROL Retail Hash] | (Ter informatie opgenomen in bulksbladen die zijn gegenereerd met Advanced Campaign Management) Een alfanumerieke hash-code (zoals f9639f40cdf56524b541e5dacf55a991) die aangeeft dat het item is gegenereerd met de weergave Geavanceerd (ACM). |

<table style="table-layout:auto">

[^1]: [!DNL Excel] grote getallen worden omgezet in wetenschappelijke notaties (zoals 2.12E+09 voor 2115585666) wanneer het bestand wordt geopend. Als u cijfers in de standaardnotatie wilt weergeven, selecteert u een willekeurige cel in de kolom en klikt u in de formulebalk.

## Velden vereist voor het maken, bewerken of verwijderen van elk accountonderdeel {#bulksheet-fields-per-component-google}

De volgende secties bevatten de velden die relevant zijn voor specifieke rekeningentiteiten.

>[!NOTE]
>
>Wanneer een veld niet van toepassing is op een handeling, wordt een waarde die in het veld is ingevoerd, genegeerd.

### Campagnevelden

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Campaign Budget] | Vereist om een campagne te maken. |
| [!UICONTROL Delivery Method] | Vereist om een campagne te maken. |
| [!UICONTROL Channel Type] | Vereist om een campagne te maken. |
| [!UICONTROL Networks] | Vereist om een campagne te maken. |
| [!UICONTROL DSA Domain Name] | Vereist om een campagne op het onderzoeksnetwerk tot stand te brengen die dynamische onderzoeksadvertenties zal hebben. |
| [!UICONTROL DSA Domain Language] | Vereist om een campagne op het onderzoeksnetwerk tot stand te brengen die dynamische onderzoeksadvertenties zal hebben. |
| [!UICONTROL Campaign Priority] | Vereist voor het maken van een winkelcampagne. |
| [!UICONTROL Merchant ID] | Vereist voor het maken van een winkelcampagne. |
| [!UICONTROL Sales Country] | Vereist voor het maken van een winkelcampagne. |
| [!UICONTROL Product Scope Filter] | (Winkelcampagnes) Optioneel |
| [!UICONTROL Languages] | Optioneel |
| [!UICONTROL Device Targets] | Optioneel |
| [!UICONTROL Device Targets (Google Adwords)] | Optioneel |
| [!UICONTROL Mobile Carriers (Google Adwords)] | Optioneel |
| [!UICONTROL Audience Target Method] | nvt |
| [!UICONTROL Landing Page Suffix] | Optioneel |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Campaign Status] | Alleen vereist om een campagne te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Campaign ID] | Alleen vereist wanneer u de naam van de campagne wijzigt, tenzij de rij de waarde &quot;[!UICONTROL AMO ID]&quot; voor de campagne . |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Groepsvelden toevoegen

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Networks] | nvt |
| [!UICONTROL GDN Custom Bid Level] | Optioneel |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Ad Group Type] | Vereist om een advertentiegroep te maken. |
| [!UICONTROL Max CPC] | Optioneel |
| [!UICONTROL Max Content CPC] | Optioneel |
| [!UICONTROL Audience Target Method] | Vereist |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Ad Group Status] | Alleen vereist om een advertentiegroep te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Ad Group ID] | Alleen vereist wanneer u de naam van de advertentiegroep wijzigt, tenzij de rij een &quot;[!UICONTROL AMO ID]&quot; voor de advertentiegroep. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Trefwoordvelden

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Max CPC] | Optioneel |
| [!UICONTROL Keyword] | Vereist |
| [!UICONTROL Match Type] | Een waarde voor of het gelijke type of sleutelwoordidentiteitskaart wordt vereist om een sleutelwoord met veelvoudige gelijke types uit te geven of te schrappen. |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Base URL/Final URL] | Optioneel |
| [!UICONTROL Custom URL Param] | Optioneel |
| [!UICONTROL Param1] | Optioneel |
| [!UICONTROL Param2] | Optioneel |
| [!UICONTROL Keyword Status] | Alleen vereist om een trefwoord te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Keyword ID] | Vereist slechts wanneer u het sleutelwoord uitgeeft of schrapt, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Plaatsingsvelden

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Max Placement CPC (Google Adwords)] | Optioneel |
| [!UICONTROL Max Placement CPM (Google Adwords)] | Optioneel |
| [!UICONTROL Placement] | Vereist |
| [!UICONTROL Match Type] | Vereist |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Base URL/Final URL] | Optioneel |
| [!UICONTROL Custom URL Param] | Optioneel |
| [!UICONTROL Placement Status] | Alleen vereist om een plaatsing te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Placement ID] | Dit is alleen vereist wanneer u de plaatsing bewerkt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de plaatsing te identificeren, of b) en &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Uitgebreide dynamische zoekopdracht

Dit advertentietype wordt nu &#39;dynamic search ad&#39; genoemd in [!DNL Google Ads]. Ga voor meer informatie over het maken van dynamische zoekadvertenties naar &quot;[Implementeren [!DNL Google Ads] dynamische zoekopdrachten](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-dynamic-search-ads.html).&quot;

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Creative (except RSA)]&quot; Rij in de [!UICONTROL Download Bulksheet] in.

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Creative Preferred Devices] | Optioneel |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Vereist om een advertentie te maken of de beschrijving te bewerken. <b>Opmerking:</b> Als u voor dit advertentietype wijzigingen aanbrengt in de advertentie, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie. |
| [!UICONTROL Display URL] | Vereist |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Creative Type] | Vereist om de status van een productadvertentie te maken of te bewerken. |
| [!UICONTROL Ad Status] | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Ad ID] | Dit is alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met ad-eigenschap bevat om de advertentie of b) en &quot;[!UICONTROL AMO ID].&quot; Als u echter geen van de [!UICONTROL Ad ID] noch [!UICONTROL AMO ID]en de kolommen met de eigenschap ad-eigenschap komen overeen met meerdere advertenties. De status voor slechts een van de advertenties verandert dan. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Aanbiedings-/winkeladvertentievelden

Raadpleeg voor meer informatie over het maken van winkeladvertenties &quot;[Implementeren [!DNL Google Ads] winkelcampagnes](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-shopping-campaigns.html).&quot;

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Creative (except RSA)]&quot; Rij in de [!UICONTROL Download Bulksheet] in.

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Promotion Line] | Optioneel |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Base URL/Final URL] | Optioneel |
| [!UICONTROL Custom URL Param] | Optioneel |
| [!UICONTROL Creative Type] | Vereist om de status van een productadvertentie te maken of te bewerken. |
| [!UICONTROL Ad Status] | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Ad ID] | Dit is alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met ad-eigenschap bevat om de advertentie of b) en &quot;[!UICONTROL AMO ID].&quot; Als u echter geen van de [!UICONTROL Ad ID] noch [!UICONTROL AMO ID]en de kolommen met de eigenschap ad-eigenschap komen overeen met meerdere advertenties. De status voor slechts een van de advertenties verandert dan. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Responsieve zoekopdrachten en velden

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Responsive Search Ad]&quot; Rij in de [!UICONTROL Download Bulksheet] in.

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | Voor responsieve zoekopdrachten [!UICONTROL Ad Title], [!UICONTROL Ad Title 2], en [!UICONTROL Ad Title 3] zijn vereist om een advertentie te maken en alle andere velden voor advertentietoldaties zijn optioneel. Als u de bestaande waarde voor een niet-vereist veld wilt verwijderen, gebruikt u de waarde `[delete]` (inclusief de haakjes). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Optioneel |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Voor responsieve zoekopdrachten [!UICONTROL Description Line 1] en [!UICONTROL Description Line 2] zijn vereist om een advertentie te maken, en [!UICONTROL Description Line 3] en [!UICONTROL Description Line 4] zijn optioneel. Gebruik de waarde om de bestaande waarde te verwijderen `[delete]` (inclusief de haakjes). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Optioneel |
| [!UICONTROL Display Path 1] | Optioneel |
| [!UICONTROL Display Path 2] | Optioneel |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Base URL/Final URL] | Vereist om een advertentie te maken. |
| [!UICONTROL Custom URL Param] | Optioneel |
| [!UICONTROL Creative Type] | Optioneel |
| [!UICONTROL Ad Status] | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Ad ID] | Vereist om advertenties te bewerken of te verwijderen, tenzij de rij een &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Je moet advertenties bewerken of verwijderen, tenzij je de advertentie-id opneemt. |

### Tekst en velden

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Creative (except RSA)]&quot; Rij in de [!UICONTROL Download Bulksheet] in.

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

>[!NOTE]
>
>Uitgebreide tekstadvertenties zijn in juni 2022 afgekeurd. U kunt alleen bestaande tekstadvertenties verwijderen.

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Creative Preferred Devices] | Alleen-lezen |
| [!UICONTROL Ad Title], en Titel 2-3 | Alleen-lezen |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Alleen-lezen |
| [!UICONTROL Display URL] | Alleen-lezen |
| [!UICONTROL Display Path 1] | Alleen-lezen |
| [!UICONTROL Display Path 2] | Alleen-lezen |
| [!UICONTROL Tracking Template] | Alleen-lezen |
| [!UICONTROL Base URL/Final URL] | Alleen-lezen |
| [!UICONTROL Custom URL Param] | Alleen-lezen |
| [!UICONTROL Creative Type] | Optioneel |
| [!UICONTROL Ad Status] | Vereist |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Ad ID] | Dit is alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met ad-eigenschap bevat om de advertentie of b) en &quot;[!UICONTROL AMO ID].&quot; Als u echter geen van de [!UICONTROL Ad ID] noch [!UICONTROL AMO ID]en de kolommen met de eigenschap ad-eigenschap komen overeen met meerdere advertenties. De status voor slechts een van de advertenties verandert dan. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Dynamische doelvelden (automatisch doel) voor zoeken

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Max CPC] | Optioneel |
| [!UICONTROL Auto Target Expression] | Alleen vereist als de instelling voor de campagne op &quot;[!UICONTROL Use my website contents to target my ads]&quot; is niet ingeschakeld. |
| [!UICONTROL Match Type] | Optioneel |
| [!UICONTROL Target Status] | Vereist om een doel te verwijderen |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Target ID] | Alleen vereist wanneer u het automatische doel wijzigt of verwijdert, tenzij de rij een &quot;[!UICONTROL AMO ID]&quot; voor het doel. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Velden voor productgroepen kopen

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Max CPC] | Vereist om een productgroep te maken. |
| [!UICONTROL Parent Product Groupings] | Vereist |
| [!UICONTROL Product Grouping] | Vereist |
| [!UICONTROL Partition Type] | Vereist om een productgroep te maken. |
| [!UICONTROL Match Type] | Optioneel |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Base URL/Final URL] | Vereist |
| [!UICONTROL Product Group Status] | Alleen vereist om een productgroep te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Product Group ID] | Dit is alleen vereist wanneer u de productgroep wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de productgroep te identificeren of b) en &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Sitemelinktvelden op campagnereniveau en op groepsniveau

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist voor sitelinks op advertentieniveau. Niet van toepassing op sitelinks op campagneniveau. |
| [!UICONTROL Creative Preferred Devices] | Optioneel |
| [!UICONTROL Link Name] | Vereist |
| [!UICONTROL Start Date] | Optioneel |
| [!UICONTROL End Date] | Optioneel |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Base URL/Final URL] | Vereist |
| [!UICONTROL Sitelink Status] | Alleen vereist om een sitelink te verwijderen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Sitelink ID] | Dit is alleen vereist wanneer u de sitelink wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de sitelink te identificeren of b) en &quot;[!UICONTROL AMO ID].&quot; Als u echter geen van beide opties opneemt [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID]  en de bezitskolommen passen veelvoudige sitelinks aan, dan zal de status voor slechts één van de sitelinks veranderen.<br><br><b>Opmerking:</b> Als u eigenschapkolommen sitelink bewerkt, behalve [!UICONTROL Status] voor een bestaande sitelink, en u omvat noch [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID], wordt er een nieuwe sitelink gemaakt en de bestaande sitelink wordt niet gewijzigd. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Locatiedoel

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Location] | Vereist |
| [!UICONTROL Location Type] | Optioneel |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL Location Status] | Alleen vereist om een locatiedoel te verwijderen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL AMO ID] | De gegevens moeten worden bewerkt of verwijderd, tenzij u de [!UICONTROL Campaign ID].<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Apparaatdoelvelden op campagnereniveau en op ad-groepniveau

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Device] | Vereist voor het maken of bewerken van een apparaatdoel. |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL Ad Group Name] | Vereist voor apparaatdoelen op ad-groepsniveau. Niet van toepassing op apparaatdoelen op campagneniveau. |
| [!UICONTROL Device Target Status] | Alleen vereist om een apparaatdoel te verwijderen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel; alleen van toepassing op ad-group-apparaatdoelen. |
| [!UICONTROL Device Target ID] | Alleen vereist wanneer u het doel wijzigt of verwijdert, tenzij de rij een &quot;[!UICONTROL AMO ID]&quot; voor het doel. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de apparaatdoel-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Campagne- en ad-group-niveau RLSA-doel-/uitsluitingsvelden

Voor een beschrijving van elk gegevensveld raadpleegt u &quot;[Alle beschikbare gegevensvelden](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL Ad Group Name] | Vereist voor streefcijfers en uitsluitingen op groepsniveau. Niet van toepassing op streefcijfers en uitsluitingen op campagneniveau. |
| [!UICONTROL Audience] | Vereist om een nieuw doel of een nieuwe uitsluiting te creëren. |
| [!UICONTROL Target Type] | Vereist om een nieuw doel of een nieuwe uitsluiting te creëren. |
| [!UICONTROL RLSA Target Status] | Alleen vereist om een doel of uitsluiting te verwijderen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel; alleen van toepassing op streefcijfers en uitsluitingen op ad-groepsniveau. |
| [!UICONTROL RLSA Target ID] | Alleen vereist wanneer u het doel wijzigt of verwijdert, tenzij de rij een &quot;[!UICONTROL AMO ID]&quot; voor het doel. |
| [!UICONTROL AMO ID] | Vereist om de gegevens uit te geven of te schrappen tenzij u identiteitskaart van het Doel RLSA omvat.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

>[!MORELIKETHIS]
>
>* [Bijlage - Fouten in bladbladen](../bulksheet-errors.md)
>* [Bewerkingen die u kunt uitvoeren in bulksbladen](bulksheet-operations.md)
>* [Ondersteunde bestandsindelingen voor bulksbladen](bulksheet-file-formats.md)
>* [Een bulkbladbestand downloaden/maken](../bulksheet-download.md)
>* [Opmaak voor het bijhouden van klikken voor [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Een bulksbladbestand of gecorrigeerd foutbestand uploaden](../bulksheet-upload.md)
