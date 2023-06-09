---
title: Vereiste gegevens voor het bulkwerkblad [!DNL Google Ads] rekeningen
description: Verwijs naar de vereiste kopbalgebieden en gegevensgebieden in bulksbladen voor [!DNL Google Ads] rekeningen.
source-git-commit: a1201866bab44b260c6e1e68ba215162504e618f
workflow-type: tm+mt
source-wordcount: '8662'
ht-degree: 1%

---

# Aanhangsel - Vereiste gegevens voor het informatieblad voor [!DNL Google Ads] rekeningen

Om te creëren en bij te werken [!DNL Google Ads] Campagne gegevens in bulk, kunt u Onderzoek, Sociale, &amp; het bulksbladdossiers van de Handel gebruiken die specifiek voor worden geformatteerd [!DNL Google Ads] rekeningen. U kunt een van beide [bulkbladbestanden genereren voor bestaande accounts](../bulksheet-download.md) in de vereiste bestandsindeling of b) handmatig aanmaken (zie &quot;[Ondersteunde bestandsindelingen voor bulkbladbestanden](bulksheet-file-formats.md)&quot; voor algemene informatie over de ondersteunde bestandsindelingen).

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## Alle beschikbare gegevensvelden

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Veld | Beschrijving |
| ---- | ---- |
| Platform | (Opgenomen in gegenereerde bulksbladen ter informatie) Het advertentieplatform. Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Naam van account | De unieke naam die een advertentienetwerkaccount identificeert. Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | De unieke naam die een campagne voor een account identificeert. |
| Campagnebudget | Een dagelijkse uitgavenlimiet voor de campagne, met of zonder monetaire symbolen en leestekens. Deze waarde overschrijft, maar kan het budget van de account niet overschrijden. |
| Leveringsmethode | <p>Hoe snel om advertenties voor de campagne elke dag te tonen:</p><ul><li><p><i>Standaard (gedistribueerd)</i> (de standaardinstelling voor nieuwe campagnes): Om uw advertenties over de dag te verspreiden.</p></li><li><p><i>Versneld:</i> (Verouderd in oktober 2019) Je advertenties zo vaak mogelijk weergeven totdat je budget is bereikt. Hierdoor worden uw advertenties mogelijk niet later op de dag weergegeven.</p></li></ul> |
| Kanaaltype | <p>De kanalen waarop advertenties moeten worden geplaatst. Geef een of meer opties op:</p><ul><li class="p"><p><span style="font-style: italic;"><i>Zoeken</i></span> (de standaardinstelling voor nieuwe campagnes): Advertenties plaatsen op het Google-zoeknetwerk (met inbegrip van de zoek- en zoekpartnerwebsites van Google) en eventueel ook op het Google-weergavenetwerk. <b>Opmerking:</b> Campagnes die zowel het onderzoeksnetwerk als het vertoningsnetwerk richten kunnen niet aan een portefeuille voor bieding worden toegevoegd optimalisering.</p></li><li class="p"><p><span style="font-style: italic;"><i>Weergave</i></span>: Advertenties alleen op het Google-weergavenetwerk plaatsen.</p></li><li class="p"><p><span style="font-style: italic;"><i>Winkelen</i></span>: Winkeladvertenties plaatsen op Google Shopping (in bepaalde landen) en het Google-zoeknetwerk (waaronder websites van Google-zoekers en Google-zoekpartners). Als je winkeladvertenties wilt maken, moet je producten hebben in een Google Merchant Center-account en [toestaan dat Search, Social en Commerce gegevens downloaden van de account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Zie &quot;[Implementeren [!DNL Google Ads] winkelcampagnes](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)&quot; voor meer informatie over het proces van het maken van winkeladvertenties .</p></li></ul> |
| Netwerken | <p>Waar plaatsen van advertenties? Geef een of meer opties op:</p><ul><li class="p"><p><span style="font-style: italic;"><i>Google Search</i></span>: Gesponsorde zoekopdrachten in alleen het Google Search Network.</p></li><li class="p"><p><span style="font-style: italic;"><i>Partners zoeken</i></span>: Gesponsorde zoekaanbiedingen op zoekpartners van Google.</p></li><li class="p"><p><span style="font-style: italic;"><i>Inhoud</i></span>: Biedingen plaatsen voor de weergave van netwerklijsten.</p></li><li class="p"><p><span style="font-style: italic;"><i>Alles</i></span> (de standaardinstelling voor nieuwe campagnes): Doet Google-zoekopdrachten, zoekpartners en inhoud.</p></li></ul> |
| DSA-domeinnaam | <p>(Alleen zoeknetwerk; (alleen van toepassing op uitgebreide dynamische zoekadvertenties) Het hoofddomein (zoals example.com) of subdomein (zoals schoenen.voorbeeld.com) van de website waarvan de inhoud die het advertentienetwerk gebruikt om uw dynamische zoekadvertenties te richten.<br><br><b>Opmerkingen:</b></p><ul><li><p>Uitgebreide dynamische zoekopdrachten zijn gericht op website-inhoud in plaats van op trefwoorden.</p></li><li><p>Uw domein moet door de biologische onderzoeksindex van het advertentienetwerk worden geïndexeerd om worden gericht.</p></li><li><p>Als u geen domein opgeeft, moet u voor elke advertentiegroep dynamische zoekdoelen maken, die al uw websitepagina&#39;s of een subset daarvan als doel hebben.</p></li></ul> |
| DSA-domeintaal | (Alleen zoeknetwerk; (alleen van toepassing op uitgebreide dynamische zoekadvertenties) De taal voor het opgegeven websitedomein. <b>Opmerking:</b> Als het domein pagina&#39;s in veelvoudige talen bevat en u wilt elk van hen richten, creeer een afzonderlijke campagne voor elke taal. |
| Aangepast biedingsniveau GDN | (Campagnes die slechts het vertoningsnetwerk richten) hoe te om te bieden: door <span style="font-style: italic;"><i>Advertentiegroep</i></span> (standaard), <span style="font-style: italic;"><i>Trefwoord</i></span>, <span style="font-style: italic;"><i>Plaatsing</i></span> (website), of <span style="font-style: italic;"><i>Geen</i></span> (om de bestaande waarde opnieuw in te stellen). Overige afmetingen (<span style="font-style: italic;"><i>Leeftijd</i></span>, <span style="font-style: italic;"><i>Geslacht</i></span>, <span style="font-style: italic;"><i>Rente en lijst</i></span>, <span style="font-style: italic;"><i>Onderwerp</i></span>, en <span style="font-style: italic;"><i>Verticaal</i></span>) zijn beschikbaar via de interface Google Ads. Als u de interface Google Ads hebt gebruikt om biedingen op een andere dimensie te configureren, wordt die waarde weergegeven, maar kunt u die dimensies hier niet selecteren of invoeren.</p><p><b>Opmerking:</b></p><ul><li><p>Als je op trefwoord biedt, maak je trackingsjablonen op trefwoordniveau. Als je op plaatsing biedt, maak je ook trackingsjablonen op plaatsingsniveau. Voor alle andere dimensies maakt u volgsjablonen op advertentieniveau.</p></li><li><p>Wanneer u biedt met een niet-ondersteunde dimensie (leeftijd, geslacht, interesse en lijst of onderwerp), optimaliseert Zoeken, Sociaal en Handel biedingen niet voor de dimensie en wordt alle toewijzing toegepast op de advertentiegroep.</p></li><li><p>Advertenties op het onderzoeksnetwerk gebruiken altijd sleutelwoordbiedingen.</p></li></ul> |
| Campagneprioriteit | <p>(Alleen winkelcampagnes) De prioriteit waarmee de campagne wordt gebruikt wanneer meerdere campagnes hetzelfde product adverteren:  <span style="font-style: italic;"><i>Laag</i></span> (standaard voor nieuwe campagnes), <span style="font-style: italic;"><i>Normaal</i></span>, of <span style="font-style: italic;"><i>Hoog</i></span>.</p><p>Wanneer hetzelfde product in meer dan één campagne is opgenomen, gebruikt het advertentienetwerk eerst de campagneprioriteit om te bepalen welke campagne (en het bijbehorende bod) in aanmerking komt voor de advertentieveiling. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel. |
| Merchant ID | (Winkelcampagnes en publiekscampagnes die alleen zijn gekoppeld aan een commerciële feed) De klant-id van het zakelijke account waarvan de producten voor de campagne worden gebruikt. |  |
| Verkoopland | (Alleen koopcampagnes; alleen-lezen voor bestaande campagnes) Het land waar de campagneproducten worden verkocht. Omdat de producten met doellanden worden geassocieerd, bepaalt dit het plaatsen welke producten in de campagne worden geadverteerd. |
| Filter Productbereik | (Campagnes die het winkelnetwerk van Google slechts gebruiken) De producten in uw Google Merchant Center rekening waarvoor winkeladvertenties voor de campagne kunnen worden gecreeerd. U kunt maximaal zeven productafmetingen en kenmerkcombinaties ingaan waarop om uw producten te filtreren, gebruikend het formaat dimensi=attribute. Scheid meerdere filters met een scheidingsteken &quot;>>&quot;. Voor een lijst met beschikbare productafmetingen raadpleegt u &quot;[Productfilters voor winkelcampagne](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;</p><p>Voorbeeld: &quot;Categorie L1=dieren>>Categorie L2=pet-benodigdheden>>Merk=Acme-dierenbenodigdheden&quot;</p><p>Als u de bestaande waarden wilt verwijderen, gebruikt u de waarde <span class="Code">[delete]</span> (met inbegrip van de haakjes).</p> |
| Talen | <p>(Alleen zoek- en weergavenetwerken) De doeltalen voor advertenties in de campagne.</p><p>Als u geen waarde voor of dit gebied of het Geo Targeting gebied voor een nieuwe campagne ingaat, bepaalt de munt die voor de rekening wordt gespecificeerd de standaardtalen, behalve dat campagnes met valuta die niet aan specifieke talen (bijvoorbeeld, EUR) worden in kaart gebracht aan alle talen worden gericht. Als u geen waarde voor dit gebied ingaat maar een waarde op het Geo Targeting gebied voor een nieuwe campagne ingaat, is dit gebrek aan <span style="font-style: italic;"><i>Alles</i></span>. Als u dit veld leeg laat voor een bestaande campagne, blijft de bestaande waarde behouden.</p><p>Als u alle talen als doel wilt instellen, voert u <span style="font-style: italic;"><i>Alles</i></span>. Als u specifieke talen als doel wilt instellen, voert u waarden in die door puntkomma&#39;s worden gescheiden. Hiervoor gebruikt u <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">Google-taalnamen</a> (zoals <span style="font-style: italic;"><i>Engels;Japans</i></span>, die wordt vervangen door de juiste numerieke codes) of door numerieke codes (zoals <span style="font-style: italic;"><i>1000;1005</i></span>). De waarden zijn niet hoofdlettergevoelig.</p> |
| Locatie | Een geografische locatie waar advertenties voor de campagne moeten worden geplaatst of waar advertenties moeten worden uitgesloten. Als u geen waarden voor dit veld of het veld Talen voor een nieuwe campagne invoert, bepaalt de valuta die voor de account is opgegeven de standaardlocaties, behalve dat campagnes met valuta&#39;s die niet aan specifieke locaties zijn toegewezen (bijvoorbeeld EUR), op alle locaties worden gericht. Als u voor dit veld geen waarde opgeeft, maar een waarde opgeeft in het veld [!UICONTROL Languages] veld voor een nieuwe campagne, dan is dit standaard <i>Alles</i>. Als u dit veld leeg laat voor een bestaande campagne, blijft de bestaande waarde behouden.</p><p>Als u een specifieke locatie als doel wilt instellen, gebruikt u een van de volgende [Google-locatienamen](https://developers.google.com/adwords/api/docs/appendix/geotargeting) (die worden vervangen door de juiste numerieke code) of locatiecodes:</p><ul><li><p>Landen/gebieden: Voer de naam van het land of gebied in (bijvoorbeeld <span style="font-style: italic;"><i>Verenigde Staten;Japan</i></span>) of de numerieke codes (zoals <span style="font-style: italic;"><i>2840;2392</i></span>).</p></li><li><p>Staten/provincies/regio&#39;s: Geef de naam van de staat/provincie/regio op met de bijbehorende afkortingen voor land/gebied (zoals <span style="font-style: italic;"><i>Tokyo, JP;New York, VS</i></span>) of de numerieke codes (zoals <span style="font-style: italic;"><i>20636;2167</i></span>).</p></li><li><p>Niet-Amerikaanse steden: Voer de naam van de stad, de naam van de provincie/regio en de afkortingen land/gebied in (zoals <span style="font-style: italic;"><i>Adachi, Tokio, JP;Kita, Tokio, JP</i></span>), of de numerieke codes (zoals <span style="font-style: italic;"><i>1028850;1009293</i></span>)</p></li><li><p>Amerikaanse metrogebieden: Voer de namen van steden, staten en landen in (zoals <span style="font-style: italic;"><i>Buffalo NY, VS;New York NY, VS</i></span>) of de numerieke codes (zoals <span style="font-style: italic;"><i>514;501</i></span>).</p></li></ul><p>Als u een locatie wilt uitsluiten, plaatst u een minteken (-) vóór de naam of code van de locatie, zoals <span style="font-style: italic;"><i>-Japan</i></span>.</p><p><b>Opmerking:</b> De waarden zijn niet hoofdlettergevoelig.</p> |
| Locatietype | (Wanneer u een locatie opneemt) De [locatietype](https://developers.google.com/google-ads/api/data/geotargets). |
| Apparaat | Een apparaattype waarvoor biedaanpassingen worden uitgevoerd op campagne- of advertentieniveau: <i>smartphone</i>, <i>tablet</i>, of <i>desktop</i>. |
| Bodaanpassing | <p>(Wanneer u een Locatie, Apparaat, of doel RLSA omvat) Of om biedingen voor advertenties in een specifieke plaats, op een specifiek apparatentype, of met een specifiek publieksdoel aan te passen:</p><ul><li><p>Voer 0 in om het trefwoordniveaubod te gebruiken (verschil van 0%). Voor nieuwe doelen kunt u deze ook leeg laten.</p></li><li><p>Als u een ander bod voor dit doel wilt gebruiken, voert u het percentage in waarmee u de biedingen wilt verhogen of verlagen.</p></li><ul><li><p>Voor locatie en doelstellingen RLSA, omvatten de geldige percentages van -90 tot 900.</p></li><li><p>Voor correcties bij het bieden van een apparaat zijn geldige percentages:</p></li><ul><li><p>(Campagnes)-100 (om niet te bieden voor advertenties op het apparaattype) of van -90 tot 900.</p></li><li><p>(Toevoegingsgroepen) -100 voor smartphones en tablets (om niet te bieden voor het apparaattype) en van -90 tot 900 voor alle apparaattypen.</p></li></ul></ul><li><p>(Bestaande campagnes en advertentiegroepen) Laat dit leeg als u de bestaande correctie voor biedingen wilt gebruiken.</p></li></ul> |
| Adobe Rec Bodaanpassing | (Opgenomen in gegenereerde bulksbladen ter informatie) De alleen-lezen-bodaanpassing die Adobe aanbeveelt voor een locatiedoel op campagnereniveau of een RLSA. Deze wordt alleen berekend wanneer de campagne zich in een portefeuille met een gewogen inkomstendoelstelling bevindt (niet de doelstelling Klikken maximaliseren) en de campagne ten minste twee locatiedoelen of RLSA&#39;s bevat met ten minste vijf klikken of 5 USD aan kosten in de afgelopen 90 dagen.</p><p>Als u een plaatsdoel of RLSA manueel wilt uitgeven om de geadviseerde waarde te gebruiken, wacht minstens twee weken nadat u het plaatsdoel of RLSA creeert om voor voldoende gegevensinzameling toe te staan, en verandert niet de waarde meer dan eens per week. |
| Apparaatdoelen | <p>(Alleen oudere campagnetypen) De apparaten waarop de advertentie kan worden weergegeven: <span style="font-style: italic;"><i>Alles</i></span>, <span style="font-style: italic;"><i>Computers</i></span>, <span style="font-style: italic;"><i>Smartphones</i></span>, of <span style="font-style: italic;"><i>Tablets</i></span>. Voor nieuwe campagnes is de standaardwaarde <span style="font-style: italic;"><i>Alles</i></span>.</p> |
| Apparaatbesturingssysteemdoelen (Google Adwords) | (Alleen verouderde campagnetypen; van toepassing wanneer de doelstellingen van het Apparaat &quot;Smartphones&quot;of &quot;Tablets&quot;omvatten de werkende systemen waarop de advertentie kan worden getoond: <span style="font-style: italic;"><i>Alles</i></span>, <span style="font-style: italic;"><i>Android</i></span>, <span style="font-style: italic;"><i>iOS</i></span>, of <span style="font-style: italic;"><i>Palm</i></span>. Voor nieuwe campagnes is de standaardwaarde <span style="font-style: italic;"><i>Alles</i></span>.</p> |
| Mobiele dragers (Google Adwords) | <p>(Alleen verouderde campagnetypen; Van toepassing wanneer de doelstellingen van het Apparaat &quot;Alle&quot;of &quot;Smartphones&quot;) Mobiele dragers omvatten waaraan smartphones kunnen worden aangesloten: <span style="font-style: italic;"><i>Alles</i></span>of een of meer door &lt;c span=&quot;&quot; id=&quot;2&quot; translate=&quot;no&quot; />code van drager</i></span>>,&lt;<span style="font-style: italic;"><i>landcode</i></span>> (zoals T-Mobile, VS) met de lijst van <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">beschikbare dragers en codes voor Google Ads</a>. <span style="font-style: italic;"><i> Scheid meerdere dragers van elkaar met puntkomma&#39;s (zoals T-Mobile,US;T-Mobile,GB). Voor nieuwe campagnes is de standaardwaarde <span style="font-style: italic;"><i>Alles</i></span>.</p> |
| Naam advertentiegroep | <p>De unieke naam die een advertentiegroep identificeert. De maximale lengte is 255 tekens. Er worden geen navolgende lege tekens opgeslagen (zoals &#39;Groep 1 toevoegen&#39; wordt opgeslagen als &#39;Groep 1 toevoegen&#39;). Dit veld is niet van toepassing op sitelinks op campagneniveau of apparaatdoelen op campagneniveau.</p> |
| Type advertentiegroep | <p>Het type advertentiegroep: <span class="Option">Detectie</span> (alleen voor opsporingscampagnes), <span class="Option">Weergave</span> (voor weergavecampagnes), <span class="Option">Dynamisch zoeken</span> (voor uitgebreide dynamische zoekadvertenties), <span class="Option">Zoekstandaard</span> (voor zoekadvertenties), <span class="Option">Winkelproduct</span> (voor winkeladvertenties), <span class="Option">Showcase voor winkelen</span> (maken en bewerken wordt niet ondersteund), of <span class="Option">Onbekend</span>.</p> |
| Max CPC | <p>(Alleen CPC-campagnes) De maximale kosten per klik (CPC). Dit is het hoogste bedrag dat wordt betaald voor een advertentie op het advertentienetwerk, met of zonder monetaire symbolen en interpunctie. U kunt waarden instellen voor advertentiegroepen en trefwoorden, productgroepen en dynamische zoekdoelen. De standaardinstelling voor een nieuw trefwoord wordt overgenomen van het niveau van de advertentiegroep. Voor productgroepen kunt u waarden instellen voor de laagste productgroepniveau. de standaardinstelling voor een nieuwe laag wordt overgenomen van de bovenliggende laag.</p><p>Voor bestaande productgroepen en dynamische zoekdoelen in geoptimaliseerde portfolio&#39;s zijn updates slechts één dag effectief en worden ze tijdens de volgende optimalisatiecyclus overschreven.</p><p><b>Opmerking:</b> Gebruik voor plaatsing het veld Max Placement CPC.</p> |
| Max. inhoud CPC | <p>(Alleen CPC-campagnes) De maximale kosten voor inhoud per klik (CPC). Dit is het hoogste bedrag dat wordt betaald voor een advertentie via een netwerksite voor weergave, met of zonder monetaire symbolen en interpunctie. U kunt waarden instellen en bewerken op het niveau van de advertentiegroep in campagnes die niet op plaatsing zijn gericht.</p> |
| Doelmethode publiek | <p>(Campagnes op slechts het onderzoeksnetwerk, en bestaande, read-only Gmail campagnes op het vertoningsnetwerk) Of:</p><ul><li><p><span style="font-style: italic;"><i>Doel en bod</i></span>: Alleen advertenties weergeven voor gebruikers die zijn gekoppeld aan doelgroepen die ook voldoen aan andere doelen voor de advertentiegroep.</p></li><li><p><span style="font-style: italic;"><i>Alleen bieden</i></span>: Advertenties tonen zelfs aan mensen die niet met doelpubliek worden geassocieerd zolang zij andere doelstellingen op groepsniveau voldoen.</p><p>U kunt de kans echter vergroten dat advertenties bij een bepaald publiek worden getoond door voor dat publiek hogere biedingen in te stellen.</p></li></ul> |
| Trefwoord | De trefwoordtekenreeks. De maximumlengte is 80 tekens en niet meer dan 10 woorden en kan alleen letters, cijfers en de volgende speciale tekens bevatten: spatie `# $ & _ - " [ ] ' + . / :`</p><p><b>Opmerking:</b></p><ul><li><p>Als u een trefwoord op advertentiegroep- of campagnereniveau wilt uitsluiten, stelt u het type Afstemmen in op <span style="font-style: italic;"><i>Negatief</i></span>. Als de rij de naam van de advertentiegroep bevat, wordt het trefwoord uitgesloten voor de advertentiegroep. Als de rij niet de naam van de advertentiegroep omvat, wordt het sleutelwoord uitgesloten voor de volledige campagne.</p></li><li><p>Als u een Google Ads-trefwoord of -match-type wijzigt, wordt het bestaande trefwoord verwijderd en wordt een nieuw trefwoord gemaakt.</p></li></ul> |
| Plaatsing | (Campagnes die inhoud gebruiken stemmen slechts overeen) Een plaatsing in het vertoningsnetwerk waarop uw advertenties kunnen worden getoond. Geef een van de volgende opties op:</p><ul><li class="p"><p>Website: Voer een geldige URL in. Het kan een top-level domein, eerste-vlakke subdomein, of domein met één enkele foldernaam zijn. De URL kan geen vraagteken (?) bevatten. Voorbeelden:<span class="Code"><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</span></p></li><li class="p"><p>Een advertingspositie op een specifieke pagina: De indeling gebruiken `<URL> >> <location,sublocation>` (zoals `finance.google.com >> Company pages,Top right`).</p></li><li class="p"><p>Een onderwerpcategorie: De syntaxis gebruiken `<category::<category> > <subcategory>` enzovoort (zoals `category::Industries > Energy & Utilities > Oil & Gas`).</p></li></ul><p><b>Opmerking:</b> Als u een plaatsing op advertentiegroep- of campagnereniveau wilt uitsluiten, stelt u het Type afstemmen in op <span style="font-style: italic;"><i>Negatief</i></span>. Als de rij de naam van de advertentiegroep bevat, wordt de plaatsing uitgesloten voor de advertentiegroep. Als de rij de naam van de advertentiegroep niet bevat, wordt de plaatsing uitgesloten voor de gehele campagne.</p> |
| Automatische doelexpressie | <p>(Vereist als de instelling voor de campagne &quot;De inhoud van mijn website gebruiken om mijn advertenties te activeren&quot; niet is ingeschakeld; (anders optioneel) Dynamische zoekdoelen voor de advertentiegroep.</p><p>Gebruik voor alle doelen een sterretje (*).</p><p>Als u maximaal drie dynamische zoekcriteria als doel wilt instellen, gebruikt u de indeling `<category>=<target>`, waarbij `<category>` kan alle onderstaande rubrieken bevatten. Meerdere doelen samenvoegen voor een afzonderlijke categorie met &quot;\[spatie\]&quot; en \[spatie\]&quot; en meerdere categorieën samenvoegen met &quot;[spatie] en [spatie]&quot;.</p><ul><li class="p"><p><span style="font-style: italic;"><i>Categorie</i></span>: Uitgebreide dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met een specifieke Google-inhoudscategorie.</p></li><li class="p"><p><span style="font-style: italic;"><i>URL</i></span>: Uitgebreide dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met een specifieke URL, waarbij de waarde overal in de URL kan worden opgenomen.</p></li><li class="p"><p><span style="font-style: italic;"><i>Paginatitel</i></span>: Uitgebreide dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met specifieke tekst in de paginatitel.</p></li><li class="p"><p><span style="font-style: italic;"><i>Pagina-inhoud</i></span>: Uitgebreide dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met specifieke inhoud.</p></li></ul><p>Voorbeeld: url=schoenen.example.com en page title=schoenen</p> |
| Bovenliggende productgroepen | De hiërarchie van bovenliggende productgroepen.<br><br>Voorbeeld: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| Productgroepering | <p>De productgroep (zoals &quot;brand=acme&quot; of &quot;Alle producten&quot;).</p><p><b>Opmerking:</b></p><ul><li><p>Wanneer een gespecificeerde productgroep niet in de hiërarchie van de Groepen van het Product van de Ouder bestaat, leidt het Onderzoek, Sociale, &amp; Handel tot om het even welke delen van de hiërarchie die nodig zijn.</p></li><li><p>Met Zoeken, Sociaal en Handel maakt u automatisch een groep Alle producten wanneer u een advertentiegroep maakt in een Google-winkelcampagne met een standaardbod ingesteld op het standaardbod van de advertentiegroep. Met Zoeken, Sociale media en Handel wordt automatisch een &quot;Everything Else&quot;-groep gemaakt met het standaardbod van de advertentiegroep op elk niveau van de hiërarchie van de productgroepen. U kunt deze standaardgroepen nog steeds expliciet maken en ze uitsluiten of hun biedingen wijzigen.</p></li><li><p>Elke advertentiegroep kan tot acht niveaus van productgroepen, met inbegrip van &quot;Alle Producten&quot;en zeven andere lagen omvatten.</p></li></ul> |
| Type partitie | Het partitietype voor de productgroep: <i>onderverdeling</i> (als het onderliggende productgroepen heeft) of <i>eenheid</i> (als het geen onderliggende productgroepen heeft). |
| Type afstemmen | <p>Voor dynamisch zoekdoel of productgroepen: De optie voor trefwoordafstemming voor het dynamische zoekdoel of de productgroep: <i>Dynamisch ad-doel</i> (standaard voor nieuwe dynamische zoekdoelen), <i>Productgroep</i> (standaard voor nieuwe productgroepen) of <i>Negatieve productgroep</i> (om een productgroep uit te sluiten).</p><p>Voor trefwoorden: De optie voor trefwoordafstemming voor het trefwoord: <span style="font-style: italic;"><i>Breed</i></span>, <span style="font-style: italic;"><i>Woorden</i></span>, <span style="font-style: italic;"><i>Exact</i></span>, of <span style="font-style: italic;"><i>Negatief</i></span> (om een trefwoord of een plaatsing op het weergavenetwerk uit te sluiten); productgroepen die voor winkeladvertenties worden gebruikt, hebben een overeenkomend type <span style="font-style: italic;"><i>Productgroep</i></span>. Als u <span style="font-style: italic;"><i>Negatief</i></span>, moet u ook het type opnemen dat moet worden uitgesloten (bijvoorbeeld Negatieve zin).</p><p>Voor nieuwe trefwoorden is de standaardwaarde <span style="font-style: italic;"><i>Breed</i></span>. Een waarde voor het type van gelijke of sleutelwoordidentiteitskaart wordt vereist slechts om een sleutelwoord met veelvoudige gelijke types uit te geven.</p><p><b>Opmerking:</b></p><ul><li><p>Identieke typen zijn niet van toepassing op uitgebreide dynamische zoekadvertenties, die geen trefwoorden gebruiken.</p></li><li><p>Als u het overeenkomsttype voor een Google Ads-trefwoord wijzigt, wordt het bestaande trefwoord verwijderd en wordt een nieuw trefwoord gemaakt.</p></li><li><p>Kies bij Breedte overeenkomende modifier &quot;Breed&quot; en voeg een + in vóór elk woord in het trefwoord waarvoor nauwe varianten vereist zijn (zoals &quot;+red +schoenen&quot; om nauwe varianten van zowel &quot;rood&quot; als &quot;schoenen&quot; te vereisen). <b>Opmerking:</b> Brede overeenkomende wijzigingstoetsen hebben nu hetzelfde gedrag als woordovereenkomst voor sommige talen en u kunt sinds juli 2021 geen nieuwe trefwoorden voor brede overeenkomsten maken. Zie [Google-documentatie](https://support.google.com/google-ads/answer/7042511) voor meer informatie .</p> |
| Eerste paginabod | (Opgenomen in gegenereerde bulksbladen ter informatie) Het bod dat vereist is om een advertentie op de eerste pagina van de zoekresultaten te plaatsen. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| Kwaliteitsscore | (Opgenomen in gegenereerde opsommingstekens ter informatie) De huidige kwaliteitsscore die de zoekfunctie aan het trefwoord heeft toegewezen. Deze waarde wordt niet naar het advertentienetwerk gepost.) |
| Creatieve voorkeursapparaten | (Tekstadvertenties, uitgebreide dynamische zoekopdrachten en verbeterde sitelinks; (optioneel) De apparaattypen waarop u de advertentie wilt weergeven: <span style="font-style: italic;"><i>Alles</i></span> (de standaardwaarde) of <i>Mobiel</i>. Wanneer <i>Mobiel</i> wordt opgegeven, probeert het netwerk de advertentie voor gebruikers van mobiele apparaten weer te geven in plaats van voor gebruikers van desktops of tablets. Anders, toont het netwerk de advertentie op om het even welk apparatentype.</p><p><b>Opmerking:</b></p><ul><li><p>Alleen beheerder en [!DNL Adobe] gebruikers van accountmanagers kunnen deze instelling bewerken.</p></li><li><p>Het netwerk garandeert niet dat de advertentie op het voorkeurstype wordt weergegeven.</p></li><li><p>Nieuwe verbeterde sitelinks kunnen alleen worden gemaakt in campagnes met bestaande verbeterde sitelinks of zonder sitelinks.</p></li></ul> |
| Advertentitel, advertentietak 2-15 | (Alleen uitgebreide tekstadvertenties en responsieve zoekadvertenties) De kopregels van een advertentie, elk gescheiden door een verticale pipe ( | ). De maximumlengte voor elk veld van de advertentitel is 30 karakters of 15 dubbel-byte karakters, met inbegrip van om het even welke dynamische teksten (zoals de waarden van sleutelwoorden en adverteerders).</p><p>Voor responsieve zoekadvertenties zijn Advertentitel, Advertentitel 2 en Advertentitel 3 vereist, en alle andere velden van de advertentitel zijn optioneel. Als u de bestaande waarde voor een niet-vereist veld wilt verwijderen, gebruikt u de waarde <code>[delete]</code> (met inbegrip van de haakjes).</p><p>Voor responsieve zoekadvertenties voegt u een advertentieklanker in met de volgende indelingen:</p><ul><li><p>Google-advertenties: `{CUSTOMIZER.AdCustomizerName:DefaultText}`, zoals `{CUSTOMIZER.Discount:10%}`</p></li><li><p><span>Microsoft® Advertising: `{CUSTOMIZER.Attribute name:default text}`, zoals `{CUSTOMIZER.Discount:10%}`</span></p></li></ul><p>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen, die in juni 2022 door Google Ads zijn vervangen. |
| Titel 1-15 Positie toevoegen | <p>(Alleen responsieve zoekopdrachten; (optioneel) Een positie waarop de corresponderende advertentitel moet worden vastgezet: `[null]` (geen waarde waardoor de titel van de advertentie voor alle posities in aanmerking komt), <i>1</i>, <i>2</i>, of <i>3</i>. Als Positie advertentie bijvoorbeeld de waarde 1 heeft, wordt Titel toevoegen alleen weergegeven in Positie 1. Standaard zijn alle advertentitels null (geen waarden).</p><p>Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde <code>[delete]</code> (met inbegrip van de haakjes).</p><p><b>Opmerking:</b> U kunt meerdere advertentitels vastzetten op dezelfde positie. In het advertentienetwerk wordt een van de advertentietitels gebruikt die op de positie zijn vastgezet. Titels die op positie 3 zijn vastgezet, worden mogelijk niet met de advertentie weergegeven.</p> |
| Beschrijving regel 1-4 | <p>(Alleen uitgebreide dynamische zoekadvertenties, uitgevouwen tekstadvertenties en responsieve zoekadvertenties) De hoofdtekst van een advertentie. De maximumlengte voor elk beschrijvingsveld is 90 tekens of 45 double-byte tekens, inclusief alle dynamische tekst (zoals de waarden van trefwoorden en adverteerders).</p><p>Voor responsieve zoekadvertenties voegt u een advertentieklanker in met de volgende indelingen:</p><ul><li><p>Google-advertenties: `{CUSTOMIZER.AdCustomizerName:DefaultText}`, zoals `{CUSTOMIZER.Discount:10%}`</p></li><li><p><span>Microsoft® Advertising: `{CUSTOMIZER.Attribute name:default text}`, zoals `{CUSTOMIZER.Discount:10%}`</span></p></li></ul><p>Gebruik voor uitgebreide dynamische zoekopdrachten alleen Regel 1 en Beschrijving regel 2. <b>Opmerking:</b> Als u voor dit advertentietype wijzigingen aanbrengt in de advertentie, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie.</p><p>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen, die in juni 2022 door Google Ads zijn vervangen.</p><p>Voor responsieve zoekopdrachten zijn beschrijvingsregel 1 en beschrijvingsregel 2 vereist en regel 3 en beschrijving 4 zijn optioneel. Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde <code>[delete]</code> (met inbegrip van de haakjes).</p> |
| Beschrijving regel 1-4 positie | (Alleen responsieve zoekopdrachten; (optioneel) Een positie waarop de desbetreffende beschrijving moet worden vastgezet: `[null]` (geen waarde waardoor de beschrijving voor alle posities in aanmerking komt), <i>1</i>, <i>2</i>, of <i>3</i>. Als Beschrijving 1 Positie bijvoorbeeld de waarde 1 heeft, wordt Beschrijving 1 alleen weergegeven in Positie 1. Standaard zijn geen beschrijvingen vastgezet op een positie.</p><p>Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes).</p><p><b>Opmerking:</b> U kunt meerdere beschrijvingen vastzetten op dezelfde positie. Het advertentienetwerk gebruikt één van de beschrijvingen die aan de positie worden vastgezet. Beschrijvingen die op positie 2 zijn vastgezet, mogen niet met de advertentie worden getoond. |
| URL weergeven | De URL die is opgenomen in de advertentie.<br><br>Voor uitgebreide dynamische zoekadvertenties genereert Google Ads deze waarde dynamisch vanuit het websitedomein en hoeft u geen waarde in te voeren.<br><br>Voor responsieve zoekopdrachten hoeft u geen waarde in te voeren. De weergave-URL wordt automatisch opgehaald uit het domein in de uiteindelijke URL. U kunt de URL desgewenst aanpassen met de velden Pad 1 en Pad 2.<br><br>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen, die in juni 2022 door Google Ads zijn vervangen.<br><br><b>Opmerking:</b> (Accounts met definitieve URL&#39;s) De domeinnamen in de weergave-URL en de uiteindelijke URL moeten overeenkomen.</p> |
| Pad 1 weergeven | <p>(Uitgebreide tekstadvertenties<span> en responsieve zoekadvertenties</span> alleen)</p><p>(Optioneel) Tekst die wordt toegevoegd aan de weergave-URL en die automatisch wordt opgehaald uit de uiteindelijke URL. Het is voorafgegaan in URL door een voorwaartse schuine streep (/). Een pad mag geen forward slash (/) of newline (\n) tekens bevatten. De maximumlengte is 15 tekens of 7 double-byte tekens.</p><p>Als u een advertentieklanter wilt invoegen, gebruikt u de volgende indelingen, waarbij `Default text` is een optionele waarde die moet worden ingevoegd wanneer uw feed geen geldige waarde bevat:</p><ul><li><p>Google-advertenties: `{CUSTOMIZER.AdCustomizerName:Default text}`, zoals `{CUSTOMIZER.Discount:10%}`</p></li><li><p>Microsoft® Advertising: `{CUSTOMIZER.Attribute name:Default text}`, zoals `{CUSTOMIZER.Discount:10%}`</p></li></ul><p>Als Display Path 1 bijvoorbeeld &#39;deals&#39; is, is de weergave-URL &lt;<i>URL weergeven</i>>/deals, zoals www.example.com/deals.</p><p>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen, die in juni 2022 door Google Ads zijn vervangen.</p> |
| Pad 2 weergeven | een tweede weergavepad; zie de ingang voor de Weg van de Vertoning 1.<br><br>Voorbeeld: Als Weergavepad 1 &quot;deals&quot; is en Weergavepad 2 &quot;lokaal&quot; is, is de weergave-URL &lt;<i>URL weergeven</i>>/deals/local, zoals www.example.com/deals/local.</p><p>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen, die in juni 2022 door Google Ads zijn vervangen.</p> |
| Aanbiedingslijn | (Alleen Google-aanbiedingen) Een optionele promotielijn die in de zoekresultaten bij de aanbieding van het product moet worden gevoegd. De maximumlengte is 45 tekens.</p><p>De promotielijn kan op verschillende plaatsen ten opzichte van de advertentie (zoals onder de advertentie) verschijnen, afhankelijk van waar de advertentie op de pagina wordt weergegeven. |
| Koppelingsnaam | <p>De sitelink-tekst. Het kan maximaal 25 tekens bevatten.</p><p>Voor nieuwe sitelinks moet u de naam van de campagne opnemen in de sitelink-rij. Voor sitelinks op advertentieniveau moet u ook de naam van de advertentiegroep opnemen.</p><p><b>Opmerking:</b> Bestaande tekst van 35 tekens wordt nog wel weergegeven in advertenties op desktops en tablets, maar niet op mobiele apparaten.</p> |
| Mobile App-Platform (Google-trefwoorden) | (Alleen voor bestaande installatielocaties voor apps) Het besturingssysteem waarop de mobiele toepassing wordt uitgevoerd: <i>Android™</i> of <i>ios</i>. |
| Mobiele app-id (Google Adwords) | (Alleen bestaande installatieladingen voor apps) <p>De toepassings-id of pakketnaam. |
| Mobiele toepassingsnaam (Google-trefwoorden) | (Alleen voor bestaande installatiemonsters) De naam van de toepassing. |
| Begindatum | <p>(Alleen verbeterde sitelinks) De eerste datum waarop biedingen mogen worden uitgebracht voor de sitelink, in de tijdzone van de adverteerder en in een van de volgende formaten: <span style="font-style: italic;"><i>d/m/yyyy</i></span>, <span style="font-style: italic;"><i>d/m/yy</i></span>, <span style="font-style: italic;"><i>d-m-yyyy</i></span>, of <span style="font-style: italic;"><i>d-m-yy</i></span>. De standaard voor nieuwe verbeterde sitelinks is de huidige dag.</p><p><b>Opmerking:</b> Nieuwe verbeterde sitelinks kunnen alleen worden gemaakt in campagnes met bestaande verbeterde sitelinks of zonder sitelinks.</p> |
| Einddatum | <p>(Alleen verbeterde sitelinks) De laatste datum waarop biedingen voor de sitelink mogen worden uitgebracht, in de tijdzone van de adverteerder en in een van de volgende formaten:  <span style="font-style: italic;"><i>d/m/yyyy</i></span>, <span style="font-style: italic;"><i>d/m/yy</i></span>, <span style="font-style: italic;"><i>d-m-yyyy</i></span>, of <span style="font-style: italic;"><i>d-m-yy</i></span>. De standaardwaarde is geen (geen einddatum).</p><p><b>Opmerking:</b> Nieuwe verbeterde sitelinks kunnen alleen worden gemaakt in campagnes met bestaande verbeterde sitelinks of zonder sitelinks.</p> |
| Tablet uitsluiten (Google Adwords) | (Alleen bestaande installatieladingen voor apps)</p><p>(Optioneel) Hiermee voorkomt u dat Google Ads de advertentie weergeeft aan tabletgebruikers. Waarden kunnen <i>ja</i> en <i>nee</i>. |
| Achtervoegsel bestemmingspagina | Alle parameters die aan het einde van de uiteindelijke URL&#39;s moeten worden toegevoegd om informatie bij te houden. Voorbeeld: `param2=value1&param3=value2`<br><br>Zie &quot;[Opmaak voor het bijhouden van klikken voor [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md).&quot;<br><br>De laatste URL-achtervoegsels op lagere niveaus overschrijven het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Als u een achtervoegsel wilt configureren op ad-groepsniveau of lager, gebruikt u de Google Ads-editor. |
| Sjabloon voor bijhouden | Het volgende malplaatje, dat alle off-landing domein specificeert richt en het volgen parameters en bedt definitieve URL in een parameter ValueTrack in. De het volgen malplaatje op het meest korrelige niveau (met sleutelwoord als meest korrelig) treedt de waarden op alle hogere niveaus met voeten.<br><br>Voor het bijhouden van reclame-conversies voor Adobe, die wordt toegepast wanneer de instellingen voor de campagne &#39;EF-omleiding&#39; en &#39;Automatisch uploaden&#39; bevatten, voegt Search, Social &amp; Commerce automatisch zijn eigen omleidings- en trackingcode toe wanneer u de record opslaat.<br><br>Voer een waarde in voor omleidingen en bijhouden door derden. Voor een lijst van parameters ValueTrack om definitieve URLs in het volgen malplaatjes aan te geven, zie de &quot;het Volgen malplaatje&quot;parameters in de sectie over &quot;Beschikbare Parameters ValueTrack&quot;in <a href="https://support.google.com/google-ads/answer/2375447?hl=en" target="_blank">Google Ads-documentatie</a>.<br><br>Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| Basis-URL/Definitieve URL | De bestemmingspagina URL waarnaar de gebruikers van de onderzoeksmotor worden genomen wanneer zij uw advertentie klikken, met inbegrip van om het even welke toevoegingsparameters die voor de campagne of de rekening worden gevormd. Basis/definitieve URLs op het sleutelwoordniveau treedt die op het advertentieniveau en hoger met voeten.<br><br>Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| Doel-URL | (Ter informatie opgenomen in gegenereerde bulksbladen; (niet gepost aan de zoekmachine) Voor accounts met doel-URL&#39;s is dit de URL die een advertentie koppelt aan een basis-URL/bestemmingspagina op de website van de adverteerder (soms via een andere site die de klik bijhoudt en de gebruiker vervolgens doorstuurt naar de bestemmingspagina). Het omvat om het even welke toevoegingsparameters die voor de Onderzoek, Sociale, &amp; de campagne of de rekening van de Handel worden gevormd. Als u URL&#39;s voor bijhouden hebt gegenereerd, is dit gebaseerd op de volgende parameters in uw accountinstellingen en campagnemontages. Als u specifieke parameters voor zoekprogramma&#39;s hebt toegevoegd, kunnen deze worden vervangen door de equivalente parameters voor Zoeken, Sociale &amp; Handel.<br><br>Voor accounts met uiteindelijke URL&#39;s geeft deze kolom dezelfde waarde weer als de kolom Basis-URL/Definitieve URL. |
| Aangepast URL-parameters | Gegevens ter vervanging van de `{custom_code}` dynamische variabele wanneer de variabele is opgenomen in de volgende parameters voor de instellingen van de zoekaccount of campagne. Als u de aangepaste waarde in de URL voor bijhouden wilt invoegen, moet u het bestand met de opsommingstekens uploaden met de optie URL&#39;s voor bijhouden genereren. |
| Creatief type | De advertentievorm: <i>Tekst en tekst</i>, <i>Uitgebreide tekst en</i>, <i>Dynamisch zoeken en</i> (afgekeurd advertentietype), <i>Uitgebreide dynamische zoekopdracht</i>, <i>Advertentie weergeven</i>, <i>App Install-advertentie</i> (afgekeurd), <i>Afbeelding</i> <i>Productadvertentie</i> (winkeladvertenties), of <i>Responsieve zoekopdracht</i>. De standaardinstelling voor nieuwe advertenties is <i>Tekst en tekst</i>.<br><br>Vereist om de status van een productadvertentie te maken of te bewerken. |
| Param1 | <p>De numerieke waarde van de `{param1}` ad parameter, die kan worden opgenomen in de advertentie-kopie of weergave-URL voor elke advertentie in het bulksbladbestand. De maximumlengte is 25 tekens en u kunt de volgende niet-numerieke tekens opnemen:</p><ul><li><p>De waarde kan worden voorafgegaan of toegevoegd met een valutasymbool of -code. Bijvoorbeeld: `£2.000,00` en `2000GBP` zijn geldig.</p></li><li><p>De waarde kan een komma (`,`) of punt (`.`) als scheidingsteken, met een optionele punt (`.`) of komma (`,`) voor fractionele waarden. Bijvoorbeeld: `1,000.00` en `2.000,10` zijn geldig.</p></li><li><p>De waarde kan worden voorafgegaan of met een percentageteken worden toegevoegd (`%`), plusteken (`+`), of minteken (`- `). Bijvoorbeeld: `20%`, `208+`, en `-42.32` zijn geldig.</p></li><li><p>Twee getallen kunnen worden ingesloten met een slash. Bijvoorbeeld: `4/1` en `0.95/0.45` zijn geldig.</p></li></ul><p>Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes).</p> |
| Param2 | De numerieke waarde van de `{param2}` ad parameter, die kan worden opgenomen in de advertentie-kopie of weergave-URL voor elke advertentie in het bulksbladbestand. Zie de ingang voor Param1 voor meer informatie. |
| Publiek | De lijst voor opnieuw op de markt brengen voor onderzoeksadvertenties (RLSA) richt publiek of uitgesloten publiek voor de campagne of de ad groep. Geef op of dit een doel of een uitsluiting is in het veld &quot;Doeltype&quot;. |
| Doeltype | (Wanneer een publiek wordt gespecificeerd) Of het gespecificeerde publiek een publiek is <i>Opname</i> (doel) of <i>Uitsluiting</i>. |
| Campagnestatus | De weergavestatus van de campagne: <i>Actief</i>, <i>Gepauzeerd</i>, <i>Beëindigd</i> (niet bewerkbaar), of <i>Verwijderd</i> (alleen bestaande campagnes). De standaardinstelling voor nieuwe campagnes is <i>Actief</i>. Als u een actieve of gepauzeerde campagne wilt verwijderen, voert u de waarde in <i>Verwijderd</i>. |
| Status van advertentiegroep | De weergavestatus van de advertentiegroep: <i>Actief</i>, <i>Gepauzeerd</i>, of <i>Verwijderd</i> (alleen bestaande advertentiegroepen). De standaardinstelling voor nieuwe advertentiegroepen is Actief. Als u een actieve of gepauzeerde ad-groep wilt verwijderen, voert u de waarde in `Deleted`. |
| Trefwoordstatus | De weergavestatus van het trefwoord: <i>Actief</i>, <i>Gepauzeerd</i>, of <i>Verwijderd</i> (alleen bestaande trefwoorden). De standaardwaarde voor nieuwe trefwoorden is Actief. Als u een actief of gepauzeerd trefwoord wilt verwijderen, voert u de waarde in <i>Verwijderd</i>. |
| Advertentiestatus | De weergavestatus van de advertentie: <i>Actief</i>, <i>Verwijderd</i> (alleen bestaande advertenties), <i>Afgekeurd</i> (niet bewerkbaar), of <i>Gepauzeerd</i>. De standaardinstelling voor nieuwe advertenties is Actief. Als u een actieve of gepauzeerde advertentie wilt verwijderen, voert u de waarde in <i>Verwijderd</i>. |
| Plaatsingsstatus | De status van de plaatsing van de website: <span style="font-style: italic;"><i>Actief</i></span>, <span style="font-style: italic;"><i>Gepauzeerd</i></span>, of <span style="font-style: italic;"><i>Verwijderd</i></span> (alleen bestaande advertenties). De standaardinstelling voor nieuwe websites is <span style="font-style: italic;"><i>Actief.</i></span> Als u een actieve of gepauzeerde plaatsing wilt verwijderen, voert u de waarde in <span style="font-style: italic;"><i>Verwijderd</i></span>. |
| Doelstatus | De status van een dynamisch zoekdoel: <span style="font-style: italic;"><i>Actief</i></span>, <span style="font-style: italic;"><i>Gepauzeerd</i></span>, of <span style="font-style: italic;"><i>Verwijderd</i></span> (alleen bestaande streefcijfers). De standaardinstelling voor nieuwe doelen is <span style="font-style: italic;"><i>Actief.</i></span> Als u een actief of gepauzeerd doel wilt verwijderen, voert u de waarde in <span style="font-style: italic;"><i>Verwijderd</i></span>. |
| Status van productgroep | De weergavestatus van de productgroep: <span style="font-style: italic;"><i>Actief</i></span> <span>of</span> <span style="font-style: italic;"><i>Verwijderd</i></span> (alleen bestaande productgroepen). De standaardwaarde voor nieuwe productgroepen is <span style="font-style: italic;"><i>Actief</i></span>. Als u een actieve productgroep wilt verwijderen, voert u de waarde in <span style="font-style: italic;"><i>Verwijderd</i></span>. |
| Sitelink-status | De weergavestatus van de sitelink: <span style="font-style: italic;"><i>Actief of verwijderd</i></span> (alleen bestaande sitelinks). De standaardinstelling voor nieuwe sitelinks is <span style="font-style: italic;"><i>Actief</i></span>. Als u een actieve sitelink wilt verwijderen, voert u de waarde in <span style="font-style: italic;"><i>Verwijderd</i></span>. |
| Locatiestatus | De status van het locatiedoel: <i>Actief</i> of <i>Verwijderd</i> (alleen bestaande locaties). Het gebrek voor nieuwe plaatsen is Actief. Als u een actieve locatie wilt verwijderen, voert u de waarde in <i>Verwijderd</i>. |
| RLSA-doelstatus | De status van de RLSA-doelstelling op campagne- of advertentieniveau of (alleen Google Ads)-uitsluiting: <span style="font-style: italic;"><i>Actief of verwijderd</i></span> (alleen bestaande streefcijfers). De standaardinstelling voor nieuwe doelen of uitsluitingen is <span style="font-style: italic;"><i>Actief</i></span>. Als u een actief doel of een actieve uitsluiting wilt verwijderen, voert u de waarde in <span style="font-style: italic;"><i>Verwijderd</i></span>. |
| Doelstatus van apparaat | <p>De status van het apparaatdoel op campagne- of advertentieniveau: <span class="Option">Actief</span> of <span class="Option">Verwijderd</span>. Voor nieuwe campagnes en advertentiegroepen is de standaardwaarde <span class="Option">Actief</span>.</p> |
| \[Advertiserspecifieke labelclassificatie\] | (Benoemd voor een advertentiespecifieke labelclassificatie, zoals &quot;Kleur&quot; voor een labelclassificatie genaamd Kleur) Een waarde voor de opgegeven classificatie die aan de entiteit is gekoppeld. U kunt per entiteit slechts één waarde per classificatie opnemen (zoals &quot;rood&quot; voor de labelclassificatie &quot;Kleur&quot; voor campagne A). De maximumlengte is 100 tekens en de waarde kan ASCII- en niet-ASCII-tekens bevatten.<br><br>De classificaties van het etiket en hun etiketwaarden worden toegepast op alle kindcomponenten; nieuwe componenten die later worden toegevoegd, worden automatisch aan het label gekoppeld. De etiketclassificaties voor productgroepen worden toegepast op het eenheidniveau (het meest korrelige).<br><br>Noch de classificatienaam noch de classificatiewaarde is hoofdlettergevoelig. |
| Restricties | Een beperking die aan de entiteit is toegewezen. U kunt slechts één beperking per entiteit toewijzen.<br><b>>Restricties worden overgeërfd door onderliggende entiteiten, zodat u geen waarden voor onderliggende entiteiten hoeft in te voeren, tenzij u de overgeërfde waarden wilt overschrijven. |
| Campagne-id | De unieke id die een bestaande campagne identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u de naam van de campagne wijzigt, tenzij de rij een &quot;AMO-id&quot; voor de campagne bevat. |
| Groep-id toevoegen | De unieke id die een bestaande advertentiegroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u de naam van de campagne wijzigt, tenzij de rij een &#39;AMO-id&#39; voor de advertentiegroep bevat. |
| Trefwoord-id | De unieke id die een bestaand trefwoord identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Vereist slechts wanneer u het sleutelwoord verandert, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) een &quot;identiteitskaart van AMO.&quot; |
| ID advertentie | <p>De unieke id die een bestaande advertentie identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Voor responsieve zoekopdrachten is de ID van de advertentie of de AMO-id vereist om advertentiegegevens te bewerken of te verwijderen. Voor alle andere entiteitstypen is de advertentie-id alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met eigenschappen bevat om de advertentie of b) een &quot;AMO-id&quot; te identificeren. Als u echter noch de ID van de advertentie, noch de AMO-id opneemt en de kolommen met de eigenschap advertentie komen overeen met meerdere advertenties, verandert de status voor slechts een van de advertenties.</p><p><b>Opmerking:</b> Als u a) en bezitskolommen behalve Status voor een bestaande advertentie uitgeeft, of b) om het even welke gegevens voor een ontvankelijke onderzoeksadvertentie, en u omvat noch identiteitskaart van de Advertentie noch identiteitskaart AMO, dan wordt een nieuwe advertentie gecreeerd, en de bestaande advertentie wordt niet veranderd.</p> |
| Plaatsing-id | De unieke id die een plaatsing van een website identificeert. Deze optie is alleen vereist wanneer u de plaatsing wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de plaatsing te identificeren of b) een &quot;AMO-id&quot;. |
| Doel-id | De unieke id die een bestaand automatisch doel identificeert. Deze optie is alleen vereist wanneer u het automatische doel wijzigt of verwijdert, tenzij de rij een AMO-id voor het doel bevat. |
| Productgroep-id | De unieke id die een bestaande productgroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Dit is alleen vereist wanneer u de productgroep wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de productgroep te identificeren of b) een &quot;AMO-id&quot;. |
| Sitelink-id | De unieke id die een bestaande sitelink identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u de sitelink wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de sitelink te identificeren of b) een &quot;AMO-id&quot;. Als u echter geen Sitelink-id of AMO-id opneemt en de eigenschapskolommen overeenkomen met meerdere sitelinks, verandert de status voor slechts een van de sitelinks.</p><p><b>Opmerking:</b> Als u de kolommen van de sitelink-eigenschap behalve Status voor een bestaande sitelink bewerkt en u noch de Sitelink-id noch de AMO-id opneemt, wordt een nieuwe sitelink gemaakt en wordt de bestaande sitelink niet gewijzigd. |
| RLSA doel-id | De unieke id die een bestaand RLSA-doel op campagne- of advertentieniveau of (alleen Google Ads) uitsluiting identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u het doel of de uitsluiting wijzigt of verwijdert, tenzij de rij een &#39;AMO-id&#39; voor het doel bevat. |
| Apparaatdoel-id | <p>De unieke id die een bestaand doel of een bestaande uitsluiting op campagnereniveau of op ad-groepsniveau aangeeft. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u het doel wijzigt of verwijdert, tenzij de rij een AMO-id voor het doel bevat.</p> |
| AMO-id | (In gegenereerde bulksbladen) Een unieke id die door Adobe wordt gegenereerd voor een gesynchroniseerde entiteit. Voor responsieve zoekopdrachten is de AMO-id vereist om advertenties te bewerken of te verwijderen, tenzij u de advertentie-id opneemt. Als u gegevens voor alle andere entiteitstypen met een AMO-id wilt bewerken, moet de AMO-id de gegevens bewerken of verwijderen, tenzij u de id van de entiteit en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |
| EF-foutbericht | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van het advertentienetwerk betreffende gegevens in de rij; foutberichten worden opgenomen in EF-foutbestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| Foutbericht SE | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van het advertentienetwerk betreffende gegevens in de rij; foutberichten worden opgenomen in de bestanden met SE-fouten. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| Vrijstellingsverzoek | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van de namen en tekst van het advertentiebeleid van Google dat een advertentie schendt. |
| Retail Hash | (Ter informatie opgenomen in bulksbladen die zijn gegenereerd met Advanced Campaign Management) Een alfanumerieke hash-code (zoals f9639f40cdf56524b541e5dacf55a991) die aangeeft dat het item is gegenereerd met de weergave Geavanceerd (ACM). |

<table style="table-layout:auto">

[^1]: [!DNL Excel] grote getallen worden omgezet in wetenschappelijke notaties (zoals 2.12E+09 voor 2115585666) wanneer het bestand wordt geopend. Als u cijfers in de standaardnotatie wilt weergeven, selecteert u een willekeurige cel in de kolom en klikt u in de formulebalk.

## Velden vereist voor het maken, bewerken of verwijderen van elk accountonderdeel

### Campagnevelden

| Veld | Vereist? |
| ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist | De unieke naam die een campagne voor een account identificeert. |
| Campagnebudget | Vereist om een campagne te maken. | Een dagelijkse uitgavenlimiet voor de campagne, met of zonder monetaire symbolen en leestekens. Deze waarde overschrijft, maar kan het budget van de account niet overschrijden. |
| Leveringsmethode | Vereist om een campagne te maken. |
| Kanaaltype | Vereist om een campagne te maken. |
| Netwerken | Vereist om een campagne te maken. |
| DSA-domeinnaam | Vereist om een campagne op het onderzoeksnetwerk tot stand te brengen die dynamische onderzoeksadvertenties zal hebben. |
| DSA-domeintaal | Vereist om een campagne op het onderzoeksnetwerk tot stand te brengen die dynamische onderzoeksadvertenties zal hebben. |
| Campagneprioriteit | Vereist om een winkelcampagne te maken. |
| Merchant ID | Vereist om een winkelcampagne te maken. |
| Verkoopland | Vereist om een winkelcampagne te maken. |
| Filter Productbereik | (Winkelcampagnes) Optioneel |
| Talen | Optioneel |
| Apparaatdoelen | Optioneel |
| Apparaatbesturingssysteemdoelen (Google Adwords) | Optioneel |
| Mobiele dragers (Google Adwords) | Optioneel |
| Doelmethode publiek | n.v.t. |
| Achtervoegsel bestemmingspagina | Optioneel |
| Sjabloon voor bijhouden | Optioneel |
| Campagnestatus | Alleen vereist om een campagne te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Restricties | Optioneel |
| Campagne-id | Deze optie is alleen vereist wanneer u de naam van de campagne wijzigt, tenzij de rij een &quot;AMO-id&quot; voor de campagne bevat. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Groepsvelden toevoegen

| Veld | Vereist? |
| ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Netwerken | n.v.t. |
| Aangepast biedingsniveau GDN | Optioneel |
| Naam advertentiegroep | Vereist |
| Type advertentiegroep | Vereist om een advertentiegroep te maken. |
| Max CPC | Optioneel |
| Max. inhoud CPC | Optioneel |
| Doelmethode publiek | Vereist |
| Sjabloon voor bijhouden | Optioneel |
| Status van advertentiegroep | Alleen vereist om een advertentiegroep te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Restricties | Optioneel |
| Groep-id toevoegen | Alleen vereist wanneer u de naam van de advertentiegroep wijzigt, tenzij de rij een &quot;AMO-id&quot; voor de advertentiegroep bevat. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Trefwoordvelden

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist |
| Max CPC | Optioneel |
| Trefwoord | Vereist |
| Type afstemmen | Een waarde voor of het gelijke type of sleutelwoordidentiteitskaart wordt vereist om een sleutelwoord met veelvoudige gelijke types uit te geven of te schrappen. |
| Sjabloon voor bijhouden | Optioneel |
| Basis-URL/Definitieve URL | Optioneel |
| Aangepast URL-parameters | Optioneel |
| Param1 | Optioneel |
| Param2 | Optioneel |
| Trefwoordstatus | Alleen vereist om een trefwoord te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Restricties | Optioneel |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| Trefwoord-id | Vereist slechts wanneer u het sleutelwoord uitgeeft of schrapt, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) een &quot;identiteitskaart van AMO.&quot; |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Plaatsingsvelden

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist |
| Max Placement CPC (Google Adwords) | Optioneel |
| Max Placement CPM (Google Adwords) | Optioneel |
| Plaatsing | Vereist |
| Type afstemmen | Vereist |
| Sjabloon voor bijhouden | Optioneel |
| Basis-URL/Definitieve URL | Optioneel |
| Aangepast URL-parameters | Optioneel |
| Plaatsingsstatus | Optioneel: Maken of bewerken<br><br>Vereist: Verwijderen |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Restricties | Optioneel |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| Plaatsing-id | Deze optie is alleen vereist wanneer u de plaatsing bewerkt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de plaatsing te identificeren of b) een &quot;AMO-id&quot;. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Uitgebreide dynamische zoekopdracht

Dit advertentietype wordt nu &#39;&#39;dynamic search ad&#39;&#39; genoemd in [!DNL Google Ads]. Ga voor meer informatie over het maken van dynamische zoekadvertenties naar &quot;[Implementeren [!DNL Google Ads] dynamische zoekadvertenties](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-dynamic-search-ads.html).&quot;

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Creative (except RSA)]&quot; Rij in de [!UICONTROL Download Bulksheet] .

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist |
| Creatieve voorkeursapparaten | Optioneel |
| Beschrijving regel 1-2 | Vereist om een advertentie te maken of de beschrijving te bewerken. <b>Opmerking:</b> Als u voor dit advertentietype wijzigingen aanbrengt in de advertentie, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie. |
| URL weergeven | Vereist |
| Sjabloon voor bijhouden | Optioneel |
| Creatief type | Vereist om de status van een productadvertentie te maken of te bewerken. |
| Advertentiestatus | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| ID advertentie | Deze optie is alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met ad-eigenschap bevat om de advertentie of b) een &quot;AMO-id&quot; te identificeren. Als u echter noch de ID van de advertentie, noch de AMO-id opneemt en de kolommen met de eigenschap advertentie komen overeen met meerdere advertenties, verandert de status voor slechts een van de advertenties. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Aanbiedings-/winkeladvertentievelden

Raadpleeg voor meer informatie over het maken van winkeladvertenties &quot;[Google Ads-winkelcampagnes implementeren](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-shopping-campaigns.html).&quot;

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Creative (except RSA)]&quot; Rij in de [!UICONTROL Download Bulksheet] .

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist |
| Aanbiedingslijn | Optioneel |
| Sjabloon voor bijhouden | Optioneel |
| Basis-URL/Definitieve URL | Optioneel |
| Aangepast URL-parameters | Optioneel |
| Creatief type | Vereist om de status van een productadvertentie te maken of te bewerken. |
| Advertentiestatus | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Restricties | Optioneel |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| ID advertentie | Deze optie is alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met ad-eigenschap bevat om de advertentie of b) een &quot;AMO-id&quot; te identificeren. Als u echter noch de ID van de advertentie, noch de AMO-id opneemt en de kolommen met de eigenschap advertentie komen overeen met meerdere advertenties, verandert de status voor slechts een van de advertenties. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Responsieve zoekopdrachten en velden

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Responsive Search Ad]&quot; Rij in de [!UICONTROL Download Bulksheet] .

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist | |
| Advertentitel, advertentietak 2-15 | Voor responsieve zoekadvertenties zijn Advertentitel, Advertentitel 2 en Advertentitel 3 vereist om een advertentie te maken, en alle andere advertentievelden zijn optioneel. Als u de bestaande waarde voor een niet-vereist veld wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| Titel 1-15 Positie toevoegen | Optioneel |
| Beschrijving regel 1-4 | Voor responsieve zoekadvertenties zijn Beschrijving regel 1 en Beschrijving regel 2 vereist om een advertentie te maken, en Beschrijving regel 3 en Beschrijving regel 4 zijn optioneel. Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| Beschrijving regel 1-4 positie | Optioneel |
| Pad 1 weergeven | Optioneel |
| Pad 2 weergeven | Optioneel |
| Sjabloon voor bijhouden | Optioneel |
| Basis-URL/Definitieve URL | Vereist om een advertentie te maken. |
| Aangepast URL-parameters | Optioneel |
| Creatief type | Optioneel |
| Advertentiestatus | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| ID advertentie | Vereist om advertenties te bewerken of te verwijderen, tenzij de rij een &quot;AMO-id&quot; bevat. |
| AMO-id | Je moet advertenties bewerken of verwijderen, tenzij je de advertentie-id opneemt. |

### Tekst en velden

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Creative (except RSA)]&quot; Rij in de [!UICONTROL Download Bulksheet] .

>[!NOTE]
>
>Uitgebreide tekstadvertenties zijn in juni 2022 afgekeurd. U kunt alleen bestaande tekstadvertenties verwijderen.

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist |
| Creatieve voorkeursapparaten | Alleen-lezen |
| Advertentietitel, en titel 2-3 | Alleen-lezen |
| Beschrijving regel 1-2 | Alleen-lezen |
| URL weergeven | Alleen-lezen |
| Pad 1 weergeven | Alleen-lezen |
| Pad 2 weergeven | Alleen-lezen |
| Sjabloon voor bijhouden | Alleen-lezen |
| Basis-URL/Definitieve URL | Alleen-lezen |
| Aangepast URL-parameters | Alleen-lezen |
| Creatief type | Optioneel |
| Advertentiestatus | Vereist |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| ID advertentie | Deze optie is alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met ad-eigenschap bevat om de advertentie of b) een &quot;AMO-id&quot; te identificeren. Als u echter noch de ID van de advertentie, noch de AMO-id opneemt en de kolommen met de eigenschap advertentie komen overeen met meerdere advertenties, verandert de status voor slechts een van de advertenties. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Dynamische doelvelden (automatisch doel) voor zoeken

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist |
| Max CPC | Optioneel |
| Automatische doelexpressie | Vereist als de instelling voor de campagne &quot;Mijn website-inhoud gebruiken om mijn advertenties te activeren&quot; niet is ingeschakeld. anders facultatief. |
| Type afstemmen | Optioneel |
| Doelstatus | Vereist om een doel te verwijderen |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Restricties | Optioneel |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| Doel-id | Deze optie is alleen vereist wanneer u het automatische doel wijzigt of verwijdert, tenzij de rij een AMO-id voor het doel bevat. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Velden voor productgroepen kopen

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist |
| Max CPC | Vereist om een productgroep te maken. |
| Bovenliggende productgroepen | Vereist |
| Productgroepering | Vereist |
| Type partitie | Vereist om een productgroep te maken. |
| Type afstemmen | Optioneel |
| Sjabloon voor bijhouden | Optioneel |
| Basis-URL/Definitieve URL | Vereist |
| Status van productgroep | Alleen vereist om een productgroep te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Restricties | Optioneel |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| Productgroep-id | Dit is alleen vereist wanneer u de productgroep wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de productgroep te identificeren of b) een &quot;AMO-id&quot;. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Sitemelinktvelden op campagnereniveau en op groepsniveau

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist voor sitelinks op advertentieniveau. Niet van toepassing op sitelinks op campagneniveau. |
| Creatieve voorkeursapparaten | Optioneel |
| Koppelingsnaam | Vereist |
| Begindatum | Optioneel |
| Einddatum | Optioneel |
| Sjabloon voor bijhouden | Optioneel |
| Basis-URL/Definitieve URL | Vereist |
| Sitelink-status | Alleen vereist om een sitelink te verwijderen. |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| Sitelink-id | Deze optie is alleen vereist wanneer u de sitelink wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de sitelink te identificeren of b) een &quot;AMO-id&quot;. Als u echter noch Sitelink-id, noch AMO-id opneemt en de eigenschappenkolommen overeenkomen met meerdere sitelinks, verandert de status voor slechts een van de sitelinks.<br><br><b>Opmerking:</b> Als u sitelink-eigenschapkolommen behalve Status voor een bestaande sitelink bewerkt en u niet de Sitelink-id of AMO-id opneemt, wordt een nieuwe sitelink gemaakt en wordt de bestaande sitelink niet gewijzigd. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Locatiedoelvelden

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Locatie | Vereist |
| Locatietype | Optioneel |
| Bodaanpassing | Optioneel |
| Locatiestatus | Alleen vereist om een locatiedoel te verwijderen. |
| Campagne-id | Optioneel |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de campagne-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Apparaatdoelvelden op campagnereniveau en op ad-groepniveau

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Apparaat | Vereist voor het maken of bewerken van een apparaatdoel. |
| Bodaanpassing | Optioneel |
| Naam advertentiegroep | Vereist voor apparaatdoelen op ad-groepsniveau. Niet van toepassing op apparaatdoelen op campagneniveau. |
| Doelstatus van apparaat | Alleen vereist om een apparaatdoel te verwijderen. |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel; alleen van toepassing op ad-group-apparaatdoelen. |
| Apparaatdoel-id | Deze optie is alleen vereist wanneer u het doel wijzigt of verwijdert, tenzij de rij een AMO-id voor het doel bevat. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de apparaatdoel-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Campagne- en ad-group-niveau RLSA-doel-/uitsluitingsvelden

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Bodaanpassing | Optioneel |
| Naam advertentiegroep | Vereist voor streefcijfers en uitsluitingen op groepsniveau. Niet van toepassing op streefcijfers en uitsluitingen op campagneniveau. |
| Publiek | Vereist om een nieuw doel of een nieuwe uitsluiting te creëren. |
| Doeltype | Vereist om een nieuw doel of een nieuwe uitsluiting te creëren. |
| RLSA-doelstatus | Alleen vereist om een doel of uitsluiting te verwijderen. |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel; alleen van toepassing op streefcijfers en uitsluitingen op ad-groepsniveau. |
| RLSA doel-id | Deze optie is alleen vereist wanneer u het doel wijzigt of verwijdert, tenzij de rij een AMO-id voor het doel bevat. |
| AMO-id | Vereist om de gegevens uit te geven of te schrappen tenzij u identiteitskaart van het Doel RLSA omvat.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

>[!MORELIKETHIS]
>
>* [Bijlage - Fouten in bladbladen](../bulksheet-errors.md)
>* [Bewerkingen die u kunt uitvoeren in bulksbladen](bulksheet-operations.md)
>* [Ondersteunde bestandsindelingen voor bulksbladen](bulksheet-file-formats.md)
>* [Een bulkbladbestand downloaden/maken](../bulksheet-download.md)
>* [Opmaak voor het bijhouden van klikken voor [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Een bulksbladbestand of gecorrigeerd foutbestand uploaden](../bulksheet-upload.md)
