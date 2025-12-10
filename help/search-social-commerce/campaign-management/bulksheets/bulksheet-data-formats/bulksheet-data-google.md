---
title: Vereiste bulkbladgegevens voor  [!DNL Google Ads]  rekeningen
description: Verwijzing de vereiste kopbalgebieden en gegevensgebieden in bulksbladen voor  [!DNL Google Ads]  rekeningen.
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '7898'
ht-degree: 0%

---

# Bijlage - Vereiste bulksbladgegevens voor [!DNL Google Ads] -accounts

Als u [!DNL Google Ads] -campagnegegevens bulksgewijs wilt maken en bijwerken, kunt u de bulkbladbestanden Zoeken, Sociaal en Commerce gebruiken die specifiek zijn opgemaakt voor [!DNL Google Ads] -accounts. U kunt of a) [&#x200B; bulkbladdossiers voor bestaande rekeningen &#x200B;](../bulksheet-download.md) in het vereiste dossierformaat of b) manueel tot hen leiden (zie &quot;[&#x200B; Ondersteunde Formaten van het Dossier van het Bulksblad &#x200B;](bulksheet-file-formats.md)&quot;voor algemene informatie over de gesteunde dossierformaten).

Elk bulksheet moet de kopbalgebieden en overeenkomstige gegevensgebieden omvatten die voor de [&#x200B; worden vereist specifieke verrichtingen u &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (zoals het creëren van een advertentie) wilt uitvoeren. Als een veld niet vereist is, kunt u het weglaten uit de koptekst- en gegevensrijen. Alle aangepaste kolommen worden verwijderd wanneer u het bulkbladbestand uploadt.

Hieronder volgt een tabel met alle beschikbare gegevensvelden en aanvullende tabellen die aangeven welke velden vereist zijn om gegevens voor afzonderlijke entiteiten (zoals campagnes en trefwoorden) toe te voegen, te bewerken of te verwijderen.

## Alle beschikbare gegevensvelden {#bulksheet-fields-all-google}

In de volgende tabel worden alle beschikbare gegevensvelden beschreven.

Voor de gegevensgebieden relevant voor rekeningsentiteiten, zie &quot;[&#x200B; Gebieden die worden vereist om, elke rekeningscomponent &#x200B;](#bulksheet-fields-per-component-google) tot stand te brengen uit te geven of te schrappen.&quot;

>[!NOTE]
>
>* De waarden in alle tekstkolommen zijn hoofdlettergevoelig.
>* Wanneer u een nieuwe record maakt en geen waarden opneemt voor alle vereiste gegevensvelden, worden aan sommige van deze velden de opgegeven standaardwaarden toegewezen.
>* Voor gebieden die hieronder niet worden gespecificeerd, wordt de standaardwaarde voor het advertentienetwerk gebruikt.
>* Voor een lijst van beschikbare bulksbladrijen in de [!UICONTROL Download Bulksheet] dialoog, zie &quot;[&#x200B; de rijen van het Blad door netwerk &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network) toe te voegen.&quot;

| Veld | Beschrijving |
| ---- | ---- |
| [!UICONTROL Platform] | (Opgenomen in gegenereerde bulksbladen ter informatie) Het advertentieplatform. Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Acct Name] | De unieke naam die een advertentienetwerkaccount identificeert. Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | De unieke naam die een campagne voor een account identificeert. |
| [!UICONTROL Campaign Budget] | Een dagelijkse uitgavenlimiet voor de campagne, met of zonder monetaire symbolen en leestekens. Deze waarde overschrijft, maar kan het budget van de account niet overschrijden. |
| [!UICONTROL Delivery Method] | <p>Hoe snel om advertenties voor de campagne elke dag te tonen:</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> (de standaardinstelling voor nieuwe campagnes): uw advertenties over de dag verspreiden.</p></li><li><p><i>[!UICONTROL Accelerated]:</i> (Verouderd in oktober 2019) Om uw advertenties zo vaak mogelijk weer te geven totdat uw budget is bereikt. Hierdoor worden uw advertenties mogelijk niet later op de dag weergegeven.</p></li></ul> |
| [!UICONTROL Channel Type] | <p>De kanalen waarop advertenties moeten worden geplaatst. Geef een of meer opties op:</p><ul><li><p><i>[!UICONTROL Search]</i> (de standaardinstelling voor nieuwe campagnes): advertenties plaatsen op het [!DNL Google Ads] zoeknetwerk (inclusief [!DNL Google Ads] zoek- en zoekpartnerwebsites) en optioneel ook op het [!DNL Google Ads] weergavenetwerk. <b> Nota:</b> campagnes die zowel het onderzoeksnetwerk als het vertoningsnetwerk richten kunnen niet aan een portefeuille voor biodoptimalisering worden toegevoegd.</p></li><li><p><i>[!UICONTROL Display]</i>: als u advertenties alleen op het [!DNL Google Ads] -weergavenetwerk wilt plaatsen.</p></li><li><p><i>[!UICONTROL Shopping]</i>: winkeladvertenties plaatsen op [!DNL Google Ads] shopping network (in bepaalde landen) en het [!DNL Google Ads] zoeknetwerk (inclusief [!DNL Google Ads] zoek- en zoekpartnerwebsites). Om het winkelen advertenties tot stand te brengen, moet u producten in a [!DNL Google Merchant Center] rekening hebben en [&#x200B; Onderzoek, Sociaal, &amp; Commerce toestaan om gegevens van de rekening &#x200B;](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md) te downloaden. Zie &quot;[&#x200B; uitvoeren  [!DNL Google Ads]  het winkelen campagnes &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot;voor meer informatie over het proces om het winkelen advertenties te creëren.</p></li></ul> |
| [!UICONTROL Networks] | <p>Waar moet ik advertenties plaatsen? Geef een of meer opties op:</p><ul><li><p><i>[!UICONTROL Google Search]</i>: Gesponsorde zoekopdrachten in alleen het Google Search Network.</p></li><li><p><i>[!UICONTROL Search Partners]</i>: gesponsorde zoekopdrachten bij zoekpartners van Google.</p></li><li><p><i>[!UICONTROL Content]</i>: als u biedingen wilt plaatsen voor de weergave van netwerklijsten.</p></li><li><p><i>[!UICONTROL All]</i> (de standaardinstelling voor nieuwe campagnes): hiermee wordt Google Search (Zoeken in partners), Search (zoekpartners) en Content (Inhoud) bedoeld.</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>(Alleen zoeken in netwerk; alleen van toepassing op uitgebreide dynamische zoekadvertenties) Het hoofddomein (zoals example.com) of subdomein (zoals shoes.example.com) van de website waarvan de inhoud die het advertentienetwerk gebruikt om uw dynamische zoekadvertenties als doel in te stellen.<br><br><b> Nota&#39;s:</b></p><ul><li><p>Uitgebreide dynamische zoekopdrachten zijn gericht op website-inhoud in plaats van op trefwoorden.</p></li><li><p>Uw domein moet door de biologische onderzoeksindex van het advertentienetwerk worden geïndexeerd om worden gericht.</p></li><li><p>Als u geen domein opgeeft, moet u voor elke advertentiegroep dynamische zoekdoelen maken, die al uw websitepagina&#39;s of een subset daarvan als doel hebben.</p></li></ul> |
| [!UICONTROL DSA Domain Language] | (Alleen netwerk zoeken; alleen van toepassing op uitgebreide dynamische zoekopdrachten) De taal voor het opgegeven websitedomein. <b> Nota:</b> als het domein pagina&#39;s in veelvoudige talen bevat en u alle hen wilt richten, creeer een afzonderlijke campagne voor elke taal. |
| [!UICONTROL GDN Custom Bid Level] | (Campagnes die alleen op het weergavenetwerk zijn gericht) Hoe kunt u bieden: door <i>[!UICONTROL Ad Group]</i> (de standaardwaarde), <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i> (website) of <i>[!UICONTROL None]</i> (om de bestaande waarde opnieuw in te stellen). Andere afmetingen (<i> Leeftijd </i>, <i> Geslacht </i>, <i> Rente en Lijst </i>, <i> Onderwerp </i>, en <i> Verticaal </i>) zijn beschikbaar bij de [!DNL Google Ads] interface. Als u de [!DNL Google Ads] interface hebt gebruikt om het bieden door een andere afmeting te vormen, wordt die waarde getoond, maar u kunt niet die dimensies selecteren of ingaan hier.</p><p><b> Nota:</b></p><ul><li><p>Als je op trefwoord biedt, maak je trackingsjablonen op trefwoordniveau. Als je op plaatsing biedt, maak je ook trackingsjablonen op plaatsingsniveau. Voor alle andere dimensies maakt u volgsjablonen op advertentieniveau.</p></li><li><p>Wanneer u biedt met een niet-ondersteunde dimensie (leeftijd, geslacht, interesse en lijst of onderwerp), optimaliseert Zoeken, Sociaal en Commerce biedingen niet voor de dimensie en wordt alle toewijzing toegepast op de advertentiegroep.</p></li><li><p>Advertenties op het onderzoeksnetwerk gebruiken altijd sleutelwoordbiedingen.</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>(Alleen voor winkelcampagnes) De prioriteit waarmee de campagne wordt gebruikt wanneer meerdere campagnes adverteren voor hetzelfde product: <i>[!UICONTROL Low]</i> (de standaardinstelling voor nieuwe campagnes), <i>[!UICONTROL Medium]</i> of <i>[!UICONTROL High]</i> .</p><p>Wanneer hetzelfde product in meer dan één campagne is opgenomen, gebruikt het advertentienetwerk eerst de campagneprioriteit om te bepalen welke campagne (en het bijbehorende bod) in aanmerking komt voor de advertentieveiling. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel. |
| [!UICONTROL Has EU Political Ads] | (Van toepassing op campagnes die gericht zijn op het publiek in de Europese Unie (EU)) Of de campagne al dan niet politieke reclame per behoefte bevat voor advertenties die in de Europese Unie worden bediend krachtens EU-Verordening 2024/90: <i>[!UICONTROL Yes]</i> of <i>[!UICONTROL No]</i> . |
| [!UICONTROL Merchant ID] | (Winkelcampagnes en publiekscampagnes die alleen zijn gekoppeld aan een commerciële feed) De klant-id van het zakelijke account waarvan de producten voor de campagne worden gebruikt. |
| [!UICONTROL Sales Country] | (Alleen winkelcampagnes; alleen-lezen voor bestaande campagnes) Het land waar de producten van de campagne worden verkocht. Omdat de producten met doellanden worden geassocieerd, bepaalt dit het plaatsen welke producten in de campagne worden geadverteerd. |
| [!UICONTROL Product Scope Filter] | (Campagnes die alleen het [!DNL Google Ads] shopping network gebruiken) De producten in uw [!DNL Google Merchant Center] -account waarvoor winkeladvertenties voor de campagne kunnen worden gemaakt. U kunt maximaal zeven productafmetingen en kenmerkcombinaties ingaan waarop om uw producten te filtreren, gebruikend het formaat dimensi=attribute. Scheid meerdere filters met een scheidingsteken &quot;>>&quot;. Voor een lijst van beschikbare productafmetingen, zie &quot;[&#x200B; het Verkopen de filters van het campagneproduct &#x200B;](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;</p><p>Voorbeeld: &quot;Categorie L1=dieren>>Categorie L2=pet-benodigdheden>>Merk=Acme-dierenbenodigdheden&quot;</p><p>Om de bestaande waarden te schrappen, gebruik de waarde <code>[ schrapt ]</code> (inclusief de haakjes).</p> |
| [!UICONTROL Languages] | <p>(Alleen zoek- en weergavenetwerken) De doeltalen voor advertenties in de campagne.</p><p>Als u geen waarde voor dit veld of het veld [!UICONTROL Geo Targeting] voor een nieuwe campagne opgeeft, wordt de standaardtaal bepaald door de valuta die voor de account is opgegeven, behalve dat campagnes met valuta&#39;s die niet aan specifieke talen zijn toegewezen (bijvoorbeeld EUR), zijn gericht op alle talen. Als u geen waarde voor dit gebied ingaat maar een waarde op het [!UICONTROL Geo Targeting] gebied voor een nieuwe campagne ingaat, is dit gebrek aan <i>[!UICONTROL All]</i>. Als u dit veld leeg laat voor een bestaande campagne, blijft de bestaande waarde behouden.</p><p>Om alle talen te richten, ga <span style="font-style: italic;"> &lt;i [!UICONTROL >All]</i></span> in. Om specifieke talen te richten, ga waarden in die door puntkomma&#39;s worden gescheiden gebruikend of <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] taalnamen </a> (zoals <i> Engels;Japans </i>, die met de correcte numerieke codes) of numerieke codes (zoals <i> 1000 worden vervangen;1005 </i>). De waarden zijn niet hoofdlettergevoelig.</p> |
| [!UICONTROL Location] | Een geografische locatie waar advertenties voor de campagne moeten worden geplaatst of waar advertenties moeten worden uitgesloten. Als u geen waarden voor dit veld of het veld Talen voor een nieuwe campagne invoert, bepaalt de valuta die voor de account is opgegeven de standaardlocaties, behalve dat campagnes met valuta&#39;s die niet aan specifieke locaties zijn toegewezen (bijvoorbeeld EUR), op alle locaties worden gericht. Als u geen waarde voor dit gebied ingaat maar een waarde op het [!UICONTROL Languages] gebied voor een nieuwe campagne ingaat, dan blijft dit aan <i>[!UICONTROL All]</i> in gebreke. Als u dit veld leeg laat voor een bestaande campagne, blijft de bestaande waarde behouden.</p><p>Om een specifieke plaats te richten, gebruik één van [[!DNL Google Ads]  plaatsnamen &#x200B;](https://developers.google.com/adwords/api/docs/appendix/geotargeting) (die met de correcte numerieke code) of plaatscodes worden vervangen:</p><ul><li><p>Landen/gebieden: Ga de land/gebiedsnamen (zoals <i> Verenigde Staten;Japan </i>) of de numerieke codes (zoals <i> in 2840;2392 </i>).</p></li><li><p>Staten/provincies/regio&#39;s: Ga de staat/provincie/gebiedsnamen met de verwante land/gebiedsafkortingen (zoals <i> Tokio, JP;New York, de V.S. </i>) of de numerieke codes (zulke <i> 20636;21167 </i>) in.</p></li><li><p>Niet-Amerikaanse steden: ga de stad, staat/provincie/regio naam, en land/gebiedsafkortingen (zoals <i> Adachi, Tokio, JP;Kita, Tokio, JP </i>), of de numerieke codes (zoals <i> 1028850;1009293 </i>) in</p></li><li><p>De metro van de V.S. gebieden: ga de plaatsnamen, staatsnamen, en landafkortingen (zoals <i> Buffalo NY, de V.S.;New York NY, de V.S. </i>) of de numerieke codes (zoals <i> 514;501 </i>) in.</p></li></ul><p>Om een plaats uit te sluiten, ga de plaatsnaam of de code met een minteken (`-`), zoals <i> - Japan </i> vooraf.</p><p><b> Nota:</b> de waarden zijn niet case-sensitive.</p> |
| [!UICONTROL Location Type] | (Wanneer u een Plaats omvat) het [&#x200B; plaatstype &#x200B;](https://developers.google.com/google-ads/api/data/geotargets). |
| [!UICONTROL Device] | Een apparaattype waarvoor biedaanpassingen worden uitgevoerd op campagne- of advertentieniveau: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> of <i>[!UICONTROL desktop]</i> . |
| [!UICONTROL Bid Adjustment] | <p>(Wanneer u een doel [!UICONTROL Location] , [!UICONTROL Device] of [!UICONTROL RLSA] opneemt, geeft aan of de biedingen voor advertenties op een specifieke locatie, op een specifiek apparaattype of met een specifiek doelpubliek moeten worden aangepast:</p><ul><li><p>Voer 0 in om het trefwoordniveaubod te gebruiken (verschil van 0%). Voor nieuwe doelen kunt u deze ook leeg laten.</p></li><li><p>Als u een ander bod voor dit doel wilt gebruiken, voert u het percentage in waarmee u de biedingen wilt verhogen of verlagen.</p></li><ul><li><p>Voor locatie en doelstellingen RLSA, omvatten de geldige percentages van -90 tot 900.</p></li><li><p>Voor correcties bij het bieden van een apparaat zijn geldige percentages:</p></li><ul><li><p>(Campagnes)-100 (om niet te bieden voor advertenties op het apparaattype) of van -90 tot 900.</p></li><li><p>(Toevoegingsgroepen) -100 voor smartphones en tablets (om niet te bieden voor het apparaattype) en van -90 tot 900 voor alle apparaattypen.</p></li></ul></ul><li><p>(Bestaande campagnes en advertentiegroepen) Laat dit leeg als u de bestaande correctie voor biedingen wilt gebruiken.</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | (Opgenomen in gegenereerde bulksbladen ter informatie) De alleen-lezen-bodaanpassing die Adobe aanbeveelt voor een locatiedoel op campagnereniveau of een RLSA. Deze wordt alleen berekend wanneer de campagne zich in een portfolio bevindt met een doel dat gebruikmaakt van gewogen conversiemetriek (niet de [!UICONTROL Maximize Clicks] -doelstelling) en de campagne ten minste twee locatiedoelen bevat of RLSA&#39;s met ten minste vijf klikken of 5 USD aan kosten in de afgelopen 90 dagen.</p><p>Als u een plaatsdoel of RLSA manueel wilt uitgeven om de geadviseerde waarde te gebruiken, wacht minstens twee weken nadat u het plaatsdoel of RLSA creeert om voor voldoende gegevensinzameling toe te staan, en verandert niet de waarde meer dan eens per week. |
| [!UICONTROL Device Targets] | <p>(Alleen verouderde campagnetypen) De apparaten waarop de advertentie kan worden weergegeven: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Smartphones]</i> of <i>[!UICONTROL Tablets]</i> . Voor nieuwe campagnes is de standaardwaarde <i>[!UICONTROL All]</i> .</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | (Alleen verouderde campagnetypen; van toepassing wanneer de apparaatdoelen &#39;smartphones&#39; of &#39;Tablets&#39; bevatten) De besturingssystemen waarop de advertentie kan worden weergegeven: <i>[!UICONTROL All]</i>, <i>[!UICONTROL Android]</i>, <i>[!UICONTROL iOS]</i> of <i>[!UICONTROL Palm]</i> . Voor nieuwe campagnes is de standaardwaarde <i>[!UICONTROL All]</i> .</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>(Verouderde campagneretypen slechts; van toepassing wanneer [!UICONTROL Device Targets] &quot;[!UICONTROL All]&quot;of &quot;[!UICONTROL Smartphones]&quot;) Mobiele dragers omvat waaraan smartphones kunnen worden aangesloten: <i>[!UICONTROL All]</i>, of één of meerdere dragers die door &lt;c <i> dragercode </i>> worden vermeld, &lt; <i> landcode </i>> (zoals T-Mobile, US) gebruikend de lijst van <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank"> beschikbare dragers en codes voor [!DNL Google Ads]</a>. Scheid meerdere dragers met puntkomma&#39;s (zoals T-Mobile,US;T-Mobile,GB). Voor nieuwe campagnes is de standaardwaarde <i>[!UICONTROL All]</i> .</p> |
| [!UICONTROL Ad Group Name] | <p>De unieke naam die een advertentiegroep identificeert. De maximumlengte is 255 tekens. Witte tekens die naast elkaar staan, worden niet opgeslagen (zoals &#39;Groep 1 toevoegen&#39; wordt bijvoorbeeld opgeslagen als &#39;Groep 1 toevoegen&#39;). Dit veld is niet van toepassing op sitelinks op campagneniveau of apparaatdoelen op campagneniveau.</p> |
| [!UICONTROL Ad Group Type] | <p>Het type advertentiegroep: <i>[!UICONTROL Demand Gen]</i> (alleen voor verbruiksgerichte campagnes), <i>[!UICONTROL Display]</i> (voor weergavecampagnes), <i>[!UICONTROL Search Dynamic]</i> (voor uitgebreide dynamische zoekadvertenties), <i>[!UICONTROL Search Standard]</i> (voor zoekadvertenties), <i>[!UICONTROL Shopping Product]</i> (voor winkelproductadvertenties), <i>[!UICONTROL Shopping Showcase]</i> (maken en bewerken niet ondersteund) of <i>[!UICONTROL Unknown]</i> .</p> |
| [!UICONTROL Max CPC] | <p>(Alleen CPC-campagnes) De maximale kosten per klik (CPC). Dit is het hoogste bedrag dat wordt betaald voor een advertentie op het advertentienetwerk, met of zonder monetaire symbolen en interpunctie. U kunt waarden instellen voor advertentiegroepen en trefwoorden, productgroepen en dynamische zoekdoelen. De standaardinstelling voor een nieuw trefwoord wordt overgenomen van het niveau van de advertentiegroep. Voor productgroepen kunt u waarden instellen voor de laagste niveau van de productgroep. De standaardinstelling voor een nieuwe laag wordt overgenomen van de bovenliggende laag.</p><p>Voor bestaande productgroepen en dynamische zoekdoelen in geoptimaliseerde portfolio&#39;s zijn updates slechts één dag effectief en worden ze tijdens de volgende optimalisatiecyclus overschreven.</p> |
| [!UICONTROL Max Content CPC] | <p>(Alleen CPC-campagnes) De maximale kosten voor inhoud per klik (CPC). Dit is het hoogste bedrag dat wordt betaald voor een advertentie via een netwerksite voor weergave, met of zonder monetaire symbolen en interpunctie. U kunt waarden instellen en bewerken op het niveau van de advertentiegroep in campagnes die niet op plaatsing zijn gericht.</p> |
| [!UICONTROL Audience Target Method] | <p>(Alleen campagnes op het zoeknetwerk en bestaande, alleen-lezen [!DNL Gmail] campagnes op het weergavenetwerk) Of:</p><ul><li><p><i>[!UICONTROL Target and Bid]</i>: alleen advertenties weergeven voor gebruikers die zijn gekoppeld aan doelgroepen die ook voldoen aan andere doelen voor de advertentiegroep.</p></li><li><p><i>[!UICONTROL Bid Only]</i>: Advertenties zelfs aan mensen tonen die niet met doelpubliek worden geassocieerd zolang zij andere doelstellingen op het niveau van de groep voldoen.</p><p>U kunt de kans echter vergroten dat advertenties bij een bepaald publiek worden getoond door voor dat publiek hogere biedingen in te stellen.</p></li></ul> |
| [!UICONTROL Keyword] | De trefwoordtekenreeks. De maximumlengte is 80 tekens en niet meer dan 10 woorden en mag alleen letters, cijfers en de volgende speciale tekens bevatten: spatie `# $ & _ - " [ ] ' + . / :`</p><p><b> Nota:</b></p><ul><li><p>Als u een trefwoord op advertentiegroep- of campagnereniveau wilt uitsluiten, stelt u de [!UICONTROL Match Type] in op <i>[!UICONTROL Negative]</i> . Als de rij de naam van de advertentiegroep bevat, wordt het trefwoord uitgesloten voor de advertentiegroep. Als de rij niet de naam van de advertentiegroep omvat, wordt het sleutelwoord uitgesloten voor de volledige campagne.</p></li><li><p>Als u het trefwoord [!DNL Google Ads] of het type overeenkomst wijzigt, wordt het bestaande trefwoord verwijderd en wordt een nieuw trefwoord gemaakt.</p></li></ul> |
| [!UICONTROL Placement] | (Campagnes die inhoud gebruiken stemmen slechts overeen) Een plaatsing in het vertoningsnetwerk waarop uw advertenties kunnen worden getoond. Geef een van de volgende opties op:</p><ul><li><p>Website: Voer een geldige URL in. Het kan een top-level domein, eerste-vlakke subdomein, of domein met één enkele foldernaam zijn. De URL kan geen vraagteken (?) bevatten. Voorbeelden:<code><br /> www.example.com<br /> example.com <br /> autos.example.com <br /> example.com/widgets</code></p></li><li><p>Een advertingspositie op een specifieke pagina: Gebruik de indeling `<URL> >> <location,sublocation>` (zoals `finance.google.com >> Company pages,Top right` ).</p></li><li><p>Een onderwerpcategorie: gebruik de syntaxis `<category::<category> > <subcategory>` enzovoort (zoals `category::Industries > Energy & Utilities > Oil & Gas` ).</p></li></ul><p><b> Nota:</b> om een plaatsing op de advertentiegroep of campagnemaniveau uit te sluiten, plaats [!UICONTROL Match Type] aan <i>[!UICONTROL Negative]</i>. Als de rij de naam van de advertentiegroep bevat, wordt de plaatsing uitgesloten voor de advertentiegroep. Als de rij de naam van de advertentiegroep niet bevat, wordt de plaatsing uitgesloten voor de gehele campagne.</p> |
| [!UICONTROL Auto Target Expression] | <p>(Vereist wanneer campagne die aan &quot;[!UICONTROL Use my website contents to target my ads]&quot;plaatst niet wordt toegelaten; facultatief anders) Dynamische onderzoeksdoelstellingen voor de advertentiegroep.</p><p>Gebruik voor alle doelen een sterretje (*).</p><p>Als u maximaal drie dynamische zoekcriteria als doel wilt instellen, gebruikt u de indeling `<category>=<target>` , waarin `<category>` een van de onderstaande categorieën kan bevatten. Sluit zich bij veelvoudige doelstellingen voor een individuele categorie met &quot;\ [lege ruimte \] en \ [lege ruimte \]&quot;aan en sluit zich bij veelvoudige categorieën met &quot;[ lege ruimte ] en [ lege ruimte ]&quot;.</p><ul><li><p><i>[!UICONTROL Category]</i>: uitgebreide dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met een specifieke [!DNL Google Ads] -inhoudscategorie.</p></li><li><p><i>[!UICONTROL URL]</i>: als u uitgebreide dynamische zoekopdrachten wilt weergeven voor geïndexeerde pagina&#39;s met een specifieke URL, waarbij de waarde overal in de URL kan worden opgenomen.</p></li><li><p><i>[!UICONTROL Page Title]</i>: uitgebreide dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met specifieke tekst in de paginatitel.</p></li><li><p><i>[!UICONTROL Page Content]</i>: uitgebreide dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met specifieke inhoud.</p></li></ul><p>Voorbeeld: url=shoes.example.com en page title=schoeisel</p> |
| [!UICONTROL Parent Product Groupings] | De hiërarchie van bovenliggende productgroepen.<br><br> Voorbeeld: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>De productgroep (zoals &quot;brand=acme&quot; of &quot;Alle producten&quot;).</p><p><b> Nota:</b></p><ul><li><p>Wanneer een opgegeven productgroep niet bestaat in de hiërarchie van [!UICONTROL Parent Product Groupings] , maken Zoeken, Sociaal en Commerce alle benodigde onderdelen van de hiërarchie.</p></li><li><p>Met Zoeken, Sociaal en Commerce wordt automatisch een groep [!UICONTROL All Products] gemaakt wanneer u een advertentiegroep maakt in een [!DNL Google Ads] -winkelcampagne met een standaardbod ingesteld op het standaardbod voor een advertentiegroep. Met Zoeken, Sociaal en Commerce wordt automatisch een groep [!UICONTROL Everything Else] gemaakt met het standaardbod voor de advertentiegroep op elk niveau van de hiërarchie van de productgroep. U kunt deze standaardgroepen nog steeds expliciet maken en ze uitsluiten of hun biedingen wijzigen.</p></li><li><p>Elke ad groep kan tot acht niveaus van productgroepen, met inbegrip van &quot;[!UICONTROL All Products]&quot;en zeven andere lagen omvatten.</p></li></ul> |
| [!UICONTROL Partition Type] | Het verdelingstype voor de productgroep: <i> onderverdeling </i> (wanneer het kindproductgroepen) of <i> eenheid </i> heeft (wanneer het geen kindproductgroepen heeft). |
| [!UICONTROL Match Type] | <p>Voor dynamische zoekdoelen of productgroepen: de optie voor trefwoordafstemming voor het dynamische zoekdoel of de dynamische productgroep: <i>[!UICONTROL Dynamic Ad Target]</i> (de standaardinstelling voor nieuwe dynamische zoekdoelen), <i>[!UICONTROL Product Group]</i> (de standaardinstelling voor nieuwe productgroepen) of <i>[!UICONTROL Negative Product Group]</i> (om een productgroep uit te sluiten).</p><p>Voor trefwoorden: de optie voor trefwoordafstemming voor het trefwoord: <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Exact]</i> of <i>[!UICONTROL Negative]</i> (om een trefwoord of een plaatsing op het weergavenetwerk uit te sluiten); productgroepen die worden gebruikt met winkeladvertenties hebben het overeenkomende type <i>[!UICONTROL Product Group]</i> . Als u <i>[!UICONTROL Negative]</i> gebruikt, moet u ook het overeenkomstype opnemen dat moet worden uitgesloten (bijvoorbeeld &#39;Negatieve zin&#39;).</p><p>Voor nieuwe trefwoorden is de standaardwaarde <i>[!UICONTROL Broad]</i> . Een waarde voor het type van gelijke of sleutelwoordidentiteitskaart wordt vereist slechts om een sleutelwoord met veelvoudige gelijke types uit te geven.</p><p><b> Nota:</b></p><ul><li><p>Identieke typen zijn niet van toepassing op uitgebreide dynamische zoekadvertenties, die geen trefwoorden gebruiken.</p></li><li><p>Als u het overeenkomsttype voor een trefwoord [!DNL Google Ads] wijzigt, wordt het bestaande trefwoord verwijderd en wordt een nieuw trefwoord gemaakt.</p></li><li><p>Kies bij Breedte overeenkomende modifier &quot;Breed&quot; en voeg een + in vóór elk woord in het trefwoord waarvoor nauwe varianten vereist zijn (zoals &quot;+red +schoenen&quot; om nauwe varianten van zowel &quot;rood&quot; als &quot;schoenen&quot; te vereisen). <b> Nota:</b> de Brede overeenkomstenbepalingen hebben nu het zelfde passende gedrag zoals woordgelijke voor sommige talen, en u hebt geen nieuwe brede gelijkewijzigingstrefwoorden kunnen tot stand brengen sinds Juli 2021. Zie [[!DNL Google Ads]  documentatie &#x200B;](https://support.google.com/google-ads/answer/7042511) voor meer informatie.</p> |
| [!UICONTROL First Page Bid] | (Opgenomen in gegenereerde bulksbladen ter informatie) Het bod dat vereist is om een advertentie op de eerste pagina van de zoekresultaten te plaatsen. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| [!UICONTROL Quality Score] | (Opgenomen in gegenereerde opsommingstekens ter informatie) De huidige kwaliteitsscore die de zoekfunctie aan het trefwoord heeft toegewezen. Deze waarde wordt niet naar het advertentienetwerk gepost.) |
| [!UICONTROL Creative Preferred Devices] | (Tekstadvertenties, uitgebreide dynamische zoekadvertenties en verbeterde sitelinks; optioneel) De apparaattypen waarop u de advertentie liever weergeeft: <i>[!UICONTROL All]</i> (de standaardinstelling) of <i>[!UICONTROL Mobile]</i> . Wanneer <i>[!UICONTROL Mobile]</i> is opgegeven, probeert het netwerk de advertentie weer te geven aan gebruikers van mobiele apparaten in plaats van aan gebruikers van desktopcomputers of tablets. Anders, toont het netwerk de advertentie op om het even welk apparatentype.</p><p><b> Nota:</b></p><ul><li><p>Alleen beheerders en gebruikers van [!DNL Adobe] accountmanagers kunnen deze instelling bewerken.</p></li><li><p>Het netwerk garandeert niet dat de advertentie op het voorkeurstype wordt weergegeven.</p></li><li><p>Nieuwe verbeterde sitelinks kunnen alleen worden gemaakt in campagnes met bestaande verbeterde sitelinks of zonder sitelinks.</p></li></ul> |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] -15 | (Alleen uitgevouwen tekstadvertenties en responsieve zoekadvertenties) De kopregels van een advertentie, elk gescheiden door een verticale pipe (&vert;). De maximumlengte voor elk veld van de advertentitel is 30 karakters of 15 dubbel-byte karakters, met inbegrip van om het even welke dynamische teksten (zoals de waarden van sleutelwoorden en adverteerders).</p><p>Voor responsieve zoekopdrachten zijn [!UICONTROL Ad Title] , [!UICONTROL Ad Title 2] en [!UICONTROL Ad Title 3] vereist en zijn alle andere titelvelden optioneel. Om de bestaande waarde voor een niet vereist gebied te schrappen, gebruik de waarde <code>[ schrapt ]</code> (inclusief de haakjes).</p><p>Voeg voor responsieve zoekadvertenties een advertentieklanker in met de volgende indeling: <code>{CUSTOMIZER.AdCustomizerName:DefaultText}</code>, zoals <code>{CUSTOMIZER.Discount :10%}</code></p><p>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen, die in juni 2022 door [!DNL Google Ads] zijn vervangen. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>(De Responsieve onderzoeksadvertenties slechts; facultatief) Een positie waarop om de overeenkomstige advertentietolatie te speld: `[null]` (geen waarde, die de advertentietolkje voor alle posities), <i> 1 </i>, <i> 2 </i>, of <i> 3 </i> in aanmerking komt. Als [!UICONTROL Ad Title Position] bijvoorbeeld de waarde 1 heeft, wordt Titel toevoegen alleen weergegeven in Positie 1. Standaard zijn alle advertentitels null (geen waarden).</p><p>Om de bestaande waarde te schrappen, gebruik de waarde <code>[ schrapping ]</code> (inclusief de haakjes).</p><p><b> Nota:</b> u kunt veelvoudige advertentietitels aan de zelfde positie vastzetten. In het advertentienetwerk wordt een van de advertentietitels gebruikt die op de positie zijn vastgezet. Titels die op positie 3 zijn vastgezet, worden mogelijk niet met de advertentie weergegeven.</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>(Alleen uitgebreide dynamische zoekopdrachten, uitgevouwen tekstadvertenties en responsieve zoekadvertenties) De hoofdtekst van een advertentie. De maximumlengte voor elk beschrijvingsveld is 90 tekens of 45 double-byte tekens, inclusief alle dynamische tekst (zoals de waarden van trefwoorden en adverteerders).</p><p>Voeg voor responsieve zoekadvertenties een advertentieklanker in met de volgende indeling: `{CUSTOMIZER.AdCustomizerName:DefaultText}` , zoals `{CUSTOMIZER.Discount:10%}`</p><p>Gebruik [!UICONTROL Description Line 1] en [!UICONTROL Description Line 2] alleen voor uitgebreide dynamische zoekopdrachten. <b> Nota:</b> voor dit advertentietype, schrapt het veranderen en het exemplaar de bestaande advertentie en leidt tot nieuwe.</p><p>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen, die in juni 2022 door [!DNL Google Ads] zijn vervangen.</p><p>Voor responsieve zoekopdrachten zijn [!UICONTROL Description Line 1] en [!UICONTROL Description Line 2] vereist en [!UICONTROL Description Line 3] en [!UICONTROL Description Line 4] zijn optioneel. Om de bestaande waarde te schrappen, gebruik de waarde <code>[ schrapping ]</code> (inclusief de haakjes).</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (De Responsieve onderzoeksadvertenties slechts; facultatief) Een positie waarop om de overeenkomstige beschrijving te speld: `[null]` (geen waarde, die de beschrijving geschikt voor alle posities) maakt, <i> 1 </i>, <i> 2 </i>, of <i> 3 </i>. Als [!UICONTROL Description 1 Position] bijvoorbeeld de waarde 1 heeft, wordt [!UICONTROL Description 1] alleen weergegeven in Positie 1. Standaard zijn geen beschrijvingen vastgezet op een positie.</p><p>Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (inclusief de vierkante haakjes).</p><p><b> Nota:</b> u kunt veelvoudige beschrijvingen aan de zelfde positie vastzetten. Het advertentienetwerk gebruikt één van de beschrijvingen die aan de positie worden vastgezet. Beschrijvingen die op positie 2 zijn vastgezet, mogen niet met de advertentie worden getoond. |
| [!UICONTROL Display URL] | De URL die is opgenomen in de advertentie.<br><br> voor uitgebreide dynamische onderzoeksadvertenties, [!DNL Google Ads] produceert deze waarde dynamisch van het websitedomein, en u te hoeven om geen waarde in te gaan.<br><br> voor ontvankelijke onderzoeksadvertenties, te hoeven u geen waarde in te gaan. De weergave-URL wordt automatisch opgehaald uit het domein in de uiteindelijke URL. U kunt de URL desgewenst aanpassen met de velden Pad 1 en Pad 2.<br><br> u kunt niet tot stand brengen of uitgeven, maar u kunt schrappen, uitgebreide tekstadvertenties, die [!DNL Google Ads] in juni 2022 verving.<br><br><b> Nota:</b> (Rekeningen met definitieve URLs) De domeinnamen in de vertoning URL en definitieve URL moeten aanpassen.</p> |
| [!UICONTROL Display Path 1] | <p>(Uitgebreide tekstadvertenties <span> en ontvankelijke onderzoeksadvertenties </span> slechts)</p><p>(Optioneel) Tekst die wordt toegevoegd aan de weergave-URL en die automatisch wordt opgehaald uit de uiteindelijke URL. Het wordt voorafgegaan in de URL door een slash (/). Een pad mag geen forward slash (/) of newline (\n) tekens bevatten. De maximumlengte is 15 tekens of 7 double-byte tekens.</p><p>Als u een advertentieklanter wilt invoegen, gebruikt u de volgende indelingen, waarbij `Default text` een optionele waarde is die moet worden ingevoegd wanneer uw feed-bestand geen geldige waarde bevat:&lt; `{CUSTOMIZER.AdCustomizerName:Default text}`, zoals `{CUSTOMIZER.Discount:10%}`</p><p>Bijvoorbeeld, als [!UICONTROL Display Path 1] &quot;overeenkomsten is,&quot;dan is de vertoning URL &lt; <i> vertoning URL </i>>/deals, zoals www.example.com/deals.</p><p>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen, die in juni 2022 door [!DNL Google Ads] zijn vervangen.</p> |
| [!UICONTROL Display Path 2] | Een tweede weergavepad. Zie de vermelding voor [!UICONTROL Display Path 1] .<br><br> Voorbeeld: Als [!UICONTROL Display Path 1] &quot;overeenkomsten&quot;is en [!UICONTROL Display Path 2] &quot;lokaal is,&quot;dan is de vertoning URL &lt; <i> vertoning URL </i>>/deals/local, zoals www.example.com/deals/local.</p><p>U kunt geen tekstadvertenties maken of bewerken, maar u kunt wel tekstadvertenties verwijderen, die in juni 2022 door [!DNL Google Ads] zijn vervangen.</p> |
| [!UICONTROL Promotion Line] | (Alleen advertenties voor aanbiedingen van producten) Een optionele promotielijn die in de zoekresultaten bij de aanbieding van het product moet worden gevoegd. De maximumlengte is 45 tekens.</p><p>De promotielijn kan op verschillende plaatsen ten opzichte van de advertentie (zoals onder de advertentie) verschijnen, afhankelijk van waar de advertentie op de pagina wordt weergegeven. |
| [!UICONTROL Link Name] | <p>De sitelink-tekst. Het kan maximaal 25 tekens bevatten.</p><p>Voor nieuwe sitelinks moet u de naam van de campagne opnemen in de sitelink-rij. Voor sitelinks op advertentieniveau moet u ook de naam van de advertentiegroep opnemen.</p><p><b> Nota:</b> Bestaande teksten van 35 karakters worden nog getoond in advertenties op Desktops en tablets maar niet op mobiele apparaten.</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | (Bestaande app installeert slechts advertenties) Het werkende systeem waarop de mobiele toepassing loopt: <i> Android™ </i> of <i> ios </i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | (Alleen bestaande installatieladingen voor apps) <p>De toepassings-id of pakketnaam. |
| [!UICONTROL Mobile App Name (Google Adwords)] | (Alleen voor bestaande installatiemonsters) De naam van de toepassing. |
| [!UICONTROL Start Date] | <p>(Verbeterde sitelinks slechts) de eerste datum waarop de biedingen voor sitelink, in de de tijdzone van de adverteerder en in één van de volgende formaten kunnen worden geplaatst: <i> m/d/yyyy </i>, <i> m/d/yy </i>, <i> m-d-yyyy </i>, of <i> m-d-yy </i>. De standaard voor nieuwe verbeterde sitelinks is de huidige dag.</p><p><b> Nota:</b> Nieuwe verbeterde sitelinks kan slechts in campagnes met bestaande verbeterde sitelinks of geen sitelinks worden gecreeerd.</p> |
| [!UICONTROL End Date] | <p>(Alleen verbeterde sitelinks) De laatste datum waarop biedingen voor de sitelink mogen worden uitgebracht, in de tijdzone van de adverteerder en in een van de volgende formaten:  <i> m/d/jjjj </i>, <i> m/d/jj </i>, <i> m-d-jjjj </i>, of <i> m-d-jj </i>. De standaardwaarde is geen (geen einddatum).</p><p><b> Nota:</b> Nieuwe verbeterde sitelinks kan slechts in campagnes met bestaande verbeterde sitelinks of geen sitelinks worden gecreeerd.</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | (Alleen bestaande installatieladingen voor apps)</p><p>(Optioneel) Hiermee voorkomt u dat [!DNL Google Ads] de advertentie weergeeft aan tabletgebruikers. De waarden kunnen <i> ja </i> en <i> nr </i> omvatten. |
| [!UICONTROL Landing Page Suffix] | Alle parameters die aan het einde van de uiteindelijke URL&#39;s moeten worden toegevoegd om informatie bij te houden. Voorbeeld: `param2=value1&param3=value2`<br><br> zie &quot;[&#x200B; klik-volgende formaten voor  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md).&quot;<br><br> definitieve URL achtervoegsels op lagere niveaus treden het rekening-vlakke achtervoegsel met voeten. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Als u een achtervoegsel wilt configureren op ad-groepsniveau of lager, gebruikt u de [!DNL Google Ads] -editor. |
| [!UICONTROL Tracking Template] | De volgende sjabloon, die alle parameters voor het omleiden en volgen van domeinen buiten de landing opgeeft en de laatste URL in een parameter [!DNL ValueTrack] insluit. De het volgen malplaatje op het meest korrelige niveau (met sleutelwoord als meest korrelig) treedt de waarden op alle hogere niveaus met voeten.<br><br> voor het omzetten van Adobe Advertising volgen, die wordt toegepast wanneer de campagnemontages &quot; [!UICONTROL EF Redirect]&quot;en &quot;[!UICONTROL Auto Upload] omvatten,&quot;Onderzoek, Sociale, &amp; Commerce voegt automatisch zijn eigen omleiding en het volgen code toe wanneer u sparen het verslag.<br><br> voor derdeomleiding en het volgen, ga een waarde in. Voor een lijst van [!DNL ValueTrack] parameters om definitieve URLs in het volgen malplaatjes te wijzen, zie de &quot;Volgend malplaatje slechts&quot;parameters in de sectie over &quot;Beschikbare [!DNL ValueTrack] Parameters&quot;in de [[!DNL Google Ads]  documentatie &#x200B;](https://support.google.com/google-ads/answer/2375447).<br><br> om de bestaande waarde te schrappen, gebruik de waarde `[delete]` (met inbegrip van de steunen). |
| [!UICONTROL Base URL/Final URL] | De bestemmingspagina URL waarnaar de gebruikers van de onderzoeksmotor worden genomen wanneer zij uw advertentie klikken, met inbegrip van om het even welke toevoegingsparameters die voor de campagne of de rekening worden gevormd. Basis/definitieve URLs op het sleutelwoordniveau treedt die op het advertentieniveau en hoger met voeten.<br><br> om de bestaande waarde te schrappen, gebruik de waarde `[delete]` (met inbegrip van de steunen). |
| [!UICONTROL Destination URL] | (Opgenomen in gegenereerde bulksbladen voor informatiedoeleinden; niet gepost naar het zoekprogramma) Voor accounts met bestemmings-URL&#39;s is dit de URL die een advertentie koppelt aan een basis-URL/bestemmingspagina op de website van de adverteerder (soms via een andere site die de klik bijhoudt en de gebruiker vervolgens omleidt naar de bestemmingspagina). Het bevat alle toevoegingsparameters die zijn geconfigureerd voor de campagne of account voor Zoeken, Sociaal zoeken en Commerce. Als u URL&#39;s voor bijhouden hebt gegenereerd, is dit gebaseerd op de volgende parameters in uw accountinstellingen en campagnemontages. Als u specifieke parameters voor zoekprogramma&#39;s hebt toegevoegd, kunnen deze worden vervangen door de equivalente parameters voor Zoeken, Sociaal en Commerce.<br><br> voor rekeningen met definitieve URLs, toont deze kolom de zelfde waarde zoals de Basis URL/Definitieve kolom URL. |
| [!UICONTROL Custom URL Param] | Gegevens die de dynamische variabele `{custom_code}` moeten vervangen wanneer de variabele is opgenomen in de volgende parameters voor de instellingen van de zoekaccount of campagne. Als u de aangepaste waarde in de URL voor bijhouden wilt invoegen, moet u het bestand met de opsommingstekens uploaden met de optie URL&#39;s voor reeksspatiëring genereren. |
| [!UICONTROL Creative Type] | De advertentieformaat: <i>[!UICONTROL Text ad]</i>, <i>[!UICONTROL Expanded text ad]</i>, <i>[!UICONTROL Demand Gen Carousel Ad]</i> (carrouseladvertenties met meerdere afbeeldingen), <i>[!UICONTROL Demand Gen Image Ad (single-image ads)]</i>, <i>[!UICONTROL Demand Gen Product Ad]</i> en <i>[!UICONTROL Demand Gen Video Ad]</i>, <i>[!UICONTROL Dynamic search ad]</i> (afgekeurd advertentietype), <i>[!UICONTROL Expanded Dynamic Search ad]</i>, &lt; [!UICONTROL i>Display ad]</i>, <i>[!UICONTROL App Install ad]</i> (afgekeurd), <i>[!UICONTROL Image]</i>, <i>[!UICONTROL Product ad<]/i> (winkeladvertenties) of <i>[!UICONTROL Responsive search ad]</i> . De standaardwaarde voor nieuwe advertenties is <i>[!UICONTROL Text ad]</i> .<br><br> vereist om de status van een productadvertentie tot stand te brengen of uit te geven. |
| [!UICONTROL Param1] | <p>De numerieke waarde van de parameter `{param1}` ad, die kan worden opgenomen in de advertentie- of weergave-URL voor elke advertentie in het bulksbladbestand. De maximumlengte is 25 tekens en u kunt de volgende niet-numerieke tekens opnemen:</p><ul><li><p>De waarde kan worden voorafgegaan of toegevoegd met een valutasymbool of -code. `£2.000,00` en `2000GBP` zijn bijvoorbeeld geldig.</p></li><li><p>De waarde kan een komma (`,`) of een punt (`.`) als separator, met een facultatieve punt (`.`) of een komma (`,`) voor fractionele waarden omvatten. `1,000.00` en `2.000,10` zijn bijvoorbeeld geldig.</p></li><li><p>De waarde kan met een percententeken (`%`), plus teken (`+`), of minteken (`- `) worden vooraf bepaald of worden toegevoegd. `20%` , `208+` en `-42.32` zijn bijvoorbeeld geldig.</p></li><li><p>Twee getallen kunnen worden ingesloten met een slash. `4/1` en `0.95/0.45` zijn bijvoorbeeld geldig.</p></li></ul><p>Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (inclusief de vierkante haakjes).</p> |
| [!UICONTROL Param2] | De numerieke waarde van de parameter `{param2}` ad, die kan worden opgenomen in de advertentie- of weergave-URL voor elke advertentie in het bulksbladbestand. Zie de ingang voor Param1 voor meer informatie. |
| [!UICONTROL Audience] | De lijst voor opnieuw op de markt brengen voor onderzoeksadvertenties (RLSA) richt publiek of uitgesloten publiek voor de campagne of de ad groep. Geef op of dit een doel of een uitsluiting is in het veld &quot;Doeltype&quot;. |
| [!UICONTROL Target Type] | (Wanneer een Publiek wordt gespecificeerd) Of de gespecificeerde publiek een <i> Insluiting </i> (doel) of <i> Uitsluiting </i> is. |
| [!UICONTROL Campaign Status] | De weergavestatus van de campagne: <i>[!UICONTROL Active]</i> , <i>[!UICONTROL Paused]</i> , <i>[!UICONTROL Ended]</i> (niet bewerkbaar) of <i>[!UICONTROL Deleted]</i> (alleen bestaande campagnes). De standaardwaarde voor nieuwe campagnes is <i>[!UICONTROL Active]</i>. Voer de waarde <i>[!UICONTROL Deleted]</i> in om een actieve of gepauzeerde campagne te verwijderen. |
| [!UICONTROL Ad Group Status] | De weergavestatus van de advertentiegroep: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande advertentiegroepen). De standaardwaarde voor nieuwe advertentiegroepen is [!UICONTROL Active] . Als u een actieve of gepauzeerde advertentiegroep wilt verwijderen, voert u de waarde `Deleted` in. |
| [!UICONTROL Keyword Status] | De weergavestatus van het trefwoord: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande trefwoorden). De standaardwaarde voor nieuwe trefwoorden is [!UICONTROL Active] . Voer de waarde <i>[!UICONTROL Deleted]</i> in om een actief of gepauzeerd trefwoord te verwijderen. |
| [!UICONTROL Ad Status] | De weergavestatus van de advertentie: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (alleen bestaande advertenties), <i>[!UICONTROL Disapproved]</i> (niet bewerkbaar) of <i>[!UICONTROL Paused]</i> . De standaardwaarde voor nieuwe advertenties is [!UICONTROL Active] . Voer de waarde <i>[!UICONTROL Deleted]</i> in om een actieve of gepauzeerde advertentie te verwijderen. |
| [!UICONTROL Placement Status] | De status van de plaatsing van de website: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande advertenties). Het gebrek voor nieuwe websites is Actief <i>.</i> Voer de waarde <i>[!UICONTROL Deleted]</i> in om een actieve of gepauzeerde plaatsing te verwijderen. |
| [!UICONTROL Target Status] | De status van een dynamisch zoekdoel: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande doelen). Het gebrek voor nieuwe doelstellingen is Actief <i>.</i> Voer de waarde <i>[!UICONTROL Deleted]</i> in om een actief of gepauzeerd doel te verwijderen. |
| [!UICONTROL Product Group Status] | De weergavestatus van de productgroep: <i>[!UICONTROL Active]</i> <span> of </span> <i>[!UICONTROL Deleted]</i> (alleen bestaande productgroepen). De standaardwaarde voor nieuwe productgroepen is <i>[!UICONTROL Active]</i> . Voer de waarde <i>[!UICONTROL Deleted]</i> in om een actieve productgroep te verwijderen. |
| [!UICONTROL Sitelink Status] | De vertoningsstatus van sitelink: <i> Actieve of Geschrapte </i> (bestaande slechts sitelinks). De standaardwaarde voor nieuwe sitelinks is <i>[!UICONTROL Active]</i> . Voer de waarde <i>[!UICONTROL Deleted]</i> in om een actieve sitelink te verwijderen. |
| [!UICONTROL Location Status] | De status van het doel van de locatie: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande locaties). De standaardwaarde voor nieuwe locaties is [!UICONTROL Active] . Voer de waarde <i>[!UICONTROL Deleted]</i> in om een actieve locatie te verwijderen. |
| [!UICONTROL RLSA Target Status] | De status van het RLSA-doel of -uitsluiting op campagne- of advertentieniveau: <i>[!UICONTROL Active]</i> of [!UICONTROL Deleted]</i> (alleen bestaande doelen). De standaardwaarde voor nieuwe doelen of uitsluitingen is <i>[!UICONTROL Active]</i> . Voer de waarde <i>[!UICONTROL Deleted]</i> in om een actief doel of een actieve uitsluiting te verwijderen. |
| [!UICONTROL Device Target Status] | <p>De status van het apparaatdoel op campagne- of advertentieniveau: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i> . Voor nieuwe campagnes en advertentiegroepen is de standaardwaarde <i>[!UICONTROL Active]</i> .</p> |
| \[Advertiserspecifieke labelclassificatie\] | (Benoemd voor een advertentiespecifieke labelclassificatie, zoals &quot;Kleur&quot; voor een labelclassificatie genaamd Kleur) Een waarde voor de opgegeven classificatie die aan de entiteit is gekoppeld. U kunt per entiteit slechts één waarde per classificatie opnemen (zoals &quot;rood&quot; voor de labelclassificatie &quot;Kleur&quot; voor campagne A). De maximumlengte is 100 tekens en de waarde kan ASCII- en niet-ASCII-tekens bevatten.<br><br> de classificaties van het Etiket en hun etiketwaarden worden toegepast op alle kindcomponenten; de nieuwe componenten die later worden toegevoegd worden automatisch geassocieerd met het etiket. De etiketclassificaties voor productgroepen worden toegepast op het eenheidniveau (het meest korrelige).<br><br> Noch is de classificatienaam noch de classificatiewaarde case-sensitive. |
| [!UICONTROL Constraints] | Een beperking die aan de entiteit is toegewezen. U kunt slechts één beperking per entiteit toewijzen.<br><b>>Beperkingen worden overgeërfd door onderliggende entiteiten, zodat u geen waarden voor onderliggende entiteiten hoeft in te voeren, tenzij u de overgeërfde waarden wilt overschrijven. |
| [!UICONTROL Campaign ID] | De unieke id die een bestaande campagne identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u de campagnenaam verandert, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor de campagne omvat. |
| [!UICONTROL Ad Group ID] | De unieke id die een bestaande advertentiegroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u de campagnenaam verandert, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor de advertentiegroep omvat. |
| [!UICONTROL Keyword ID] | De unieke id die een bestaand trefwoord identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u het sleutelwoord verandert, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) &quot; [!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>De unieke id die een bestaande advertentie identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Voor responsieve zoekopdrachten is de id van de advertentie of de AMO-id vereist om advertentiegegevens te bewerken of te verwijderen. Voor alle andere entiteittypes, wordt identiteitskaart van de Advertentie vereist slechts wanneer u de advertentiestatus verandert, tenzij de rij a) voldoende kolommen van het ad bezit omvat om de advertentie of b) te identificeren &quot;[!UICONTROL AMO ID]&quot;.&quot; Als u echter noch de kolommen [!UICONTROL Ad ID] noch [!UICONTROL AMO ID] opneemt en de kolommen met de eigenschap ad overeenkomen met meerdere advertenties, verandert de status voor slechts een van de advertenties.</p><p><b> Nota:</b> als u a) en bezitskolommen behalve Status voor een bestaande advertentie of b) om het even welke gegevens voor een ontvankelijke onderzoeksadvertentie uitgeeft, en u omvat noch [!UICONTROL Ad ID] noch [!UICONTROL AMO ID], dan wordt een nieuwe advertentie gecreeerd, en de bestaande advertentie wordt niet veranderd.</p> |
| [!UICONTROL Placement ID] | De unieke id die een plaatsing van een website identificeert. Vereist slechts wanneer u verandert of de plaatsing schrapt, tenzij de rij a) voldoende bezitskolommen omvat om de plaatsing te identificeren of b) &quot; [!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Target ID] | De unieke id die een bestaand automatisch doel identificeert. Vereist slechts wanneer u verandert of het autodoel schrapt, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor het doel omvat. |
| [!UICONTROL Product Group ID] | De unieke id die een bestaande productgroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u verandert of de productgroep schrapt, tenzij de rij a) voldoende bezitskolommen omvat om de productgroep te identificeren of b) &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Sitelink ID] | De unieke id die een bestaande sitelink identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u verandert of de sitelink schrapt, tenzij de rij a) voldoende bezitskolommen omvat om sitelink of b) te identificeren &quot;[!UICONTROL AMO ID]&quot;. Als u echter geen [!UICONTROL Sitelink ID] of [!UICONTROL AMO ID] opneemt en de eigenschapskolommen overeenkomen met meerdere sitelinks, verandert de status voor slechts een van de sitelinks.</p><p><b> Nota:</b> als u sitelink bezitskolommen behalve Status voor bestaande sitelink uitgeeft, en u noch [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID] omvat, dan wordt een nieuwe sitelink gecreeerd, en bestaande sitelink wordt niet veranderd. |
| [!UICONTROL RLSA Target ID] | De unieke id die een bestaand RLSA-doel of -uitsluiting op campagne- of advertentieniveau identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u het doel of de uitsluiting verandert of schrapt, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor het doel omvat. |
| [!UICONTROL Device Target ID] | <p>De unieke id die een bestaand doel of een bestaande uitsluiting op campagnereniveau of op ad-groepsniveau aangeeft. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u verandert of het doel schrapt, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor het doel omvat.</p> |
| [!UICONTROL AMO ID] | (In gegenereerde bulksbladen) Een door Adobe gegenereerde unieke id voor een gesynchroniseerde entiteit. Voor responsieve zoekopdrachten is de AMO-id vereist om advertenties te bewerken of te verwijderen, tenzij u de advertentie-id opneemt. Als u gegevens voor alle andere entiteitstypen met een AMO-id wilt bewerken, moet de AMO-id de gegevens bewerken of verwijderen, tenzij u de id van de entiteit en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |
| [!UICONTROL EF Error Message] | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van het advertentienetwerk met betrekking tot gegevens in de rij; foutberichten worden opgenomen in [!UICONTROL EF Errors] -bestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| [!UICONTROL SE Error Message] | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van het advertentienetwerk met betrekking tot gegevens in de rij; foutberichten worden opgenomen in [!UICONTROL SE Errors] -bestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| [!UICONTROL Exemption Request] | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van de namen en tekst van alle [!DNL Google Ads] -advertentiebeleidsregels die door een advertentie worden overtreden. |
| [!UICONTROL Retail Hash] | (Ter informatie opgenomen in bulksbladen die zijn gegenereerd met Advanced Campaign Management) Een alfanumerieke hash-code (zoals f9639f40cdf56524b541e5dacf55a991) die aangeeft dat het item is gegenereerd met de weergave Geavanceerd (ACM). |

[^1 ]: [!DNL Excel] zet grote aantallen in wetenschappelijke aantekening (zoals 2.12E+09 voor 2115585666) om wanneer het dossier opent. Als u cijfers in de standaardnotatie wilt weergeven, selecteert u een willekeurige cel in de kolom en klikt u in de formulebalk.

## Velden vereist voor het maken, bewerken of verwijderen van elk accountonderdeel {#bulksheet-fields-per-component-google}

De volgende secties bevatten de velden die relevant zijn voor specifieke rekeningentiteiten.

>[!NOTE]
>
>Wanneer een veld niet van toepassing is op een handeling, wordt een waarde die in het veld is ingevoerd, genegeerd.

### Campagnevelden

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Campaign Budget] | Vereist om een campagne te maken. |
| [!UICONTROL Delivery Method] | Vereist om een campagne te maken. |
| [!UICONTROL Channel Type] | Vereist om een campagne te maken. |
| [!UICONTROL Networks] | Vereist om een campagne te maken. |
| [!UICONTROL DSA Domain Name] | Vereist om een campagne met dynamische onderzoeksadvertenties op het onderzoeksnetwerk tot stand te brengen. |
| [!UICONTROL DSA Domain Language] | Vereist om een campagne met dynamische onderzoeksadvertenties op het onderzoeksnetwerk tot stand te brengen. |
| [!UICONTROL Campaign Priority] | Vereist voor het maken van een winkelcampagne. |
| [!UICONTROL Has EU Political Ads] | Vereist om een campagne te maken. |
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
| [!UICONTROL Campaign ID] | Vereist slechts wanneer u de campagnenaam verandert, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor de campagne omvat. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Groepsvelden toevoegen

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
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
| [!UICONTROL Ad Group ID] | Vereist slechts wanneer u de naam van de advertentiegroep verandert, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor de advertentiegroep omvat. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Trefwoordvelden

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
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
| [!UICONTROL Keyword ID] | Vereist slechts wanneer u het sleutelwoord uitgeeft of schrapt, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) &quot; [!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Plaatsingsvelden

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
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
| [!UICONTROL Placement ID] | Vereist slechts wanneer u uitgeeft of de plaatsing schrapt, tenzij de rij a) voldoende bezitskolommen omvat om de plaatsing te identificeren of b) &quot; [!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Uitgebreide dynamische zoekopdracht

Dit advertentietype wordt nu &#39;&#39;dynamic search ad&#39;&#39; in [!DNL Google Ads] genoemd. Voor meer informatie over het creëren van dynamische onderzoeksadvertenties, zie &quot;[&#x200B;  [!DNL Google Ads]  dynamische onderzoeksadvertenties &#x200B;](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-dynamic-search-ads.html?lang=nl-NL) uitvoeren.&quot;

Gebruik voor dit advertentietype de rij &quot;[!UICONTROL Creative (except RSA)]&quot; in het dialoogvenster [!UICONTROL Download Bulksheet] .

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Creative Preferred Devices] | Optioneel |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Vereist om een advertentie te maken of de beschrijving te bewerken. <b> Nota:</b> voor dit advertentietype, schrapt het veranderen en het exemplaar de bestaande advertentie en leidt tot nieuwe. |
| [!UICONTROL Display URL] | Vereist |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Creative Type] | Vereist om de status van een productadvertentie te maken of te bewerken. |
| [!UICONTROL Ad Status] | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Ad ID] | Vereist slechts wanneer u de advertentiestatus verandert, tenzij de rij a) voldoende kolom van het ad-bezit omvat om de advertentie of b) te identificeren &quot;[!UICONTROL AMO ID]&quot;. Als u echter noch de kolommen [!UICONTROL Ad ID] noch [!UICONTROL AMO ID] opneemt en de kolommen met de eigenschap ad overeenkomen met meerdere advertenties, verandert de status voor slechts een van de advertenties. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Aanbiedings-/winkeladvertentievelden

Voor meer informatie over het creëren van het winkelen adverteert, zie &quot;[&#x200B; voert  [!DNL Google Ads]  het winkelen campagnes &#x200B;](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-shopping-campaigns.html?lang=nl-NL) uit.&quot;

Gebruik voor dit advertentietype de rij &quot;[!UICONTROL Creative (except RSA)]&quot; in het dialoogvenster [!UICONTROL Download Bulksheet] .

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
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
| [!UICONTROL Ad ID] | Vereist slechts wanneer u de advertentiestatus verandert, tenzij de rij a) voldoende kolom van het ad-bezit omvat om de advertentie of b) te identificeren &quot;[!UICONTROL AMO ID]&quot;. Als u echter noch de kolommen [!UICONTROL Ad ID] noch [!UICONTROL AMO ID] opneemt en de kolommen met de eigenschap ad overeenkomen met meerdere advertenties, verandert de status voor slechts een van de advertenties. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Responsieve zoekopdrachten en velden

Gebruik voor dit advertentietype de rij &quot;[!UICONTROL Responsive Search Ad]&quot; in het dialoogvenster [!UICONTROL Download Bulksheet] .

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] -15 | Voor responsieve zoekopdrachten zijn [!UICONTROL Ad Title] , [!UICONTROL Ad Title 2] en [!UICONTROL Ad Title 3] vereist om een advertentie te maken. Alle andere titelvelden zijn optioneel. Als u de bestaande waarde voor een niet-vereist veld wilt verwijderen, gebruikt u de waarde `[delete]` (inclusief de haakjes). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Optioneel |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Voor responsieve zoekadvertenties zijn [!UICONTROL Description Line 1] en [!UICONTROL Description Line 2] vereist om een advertentie te maken en zijn [!UICONTROL Description Line 3] en [!UICONTROL Description Line 4] optioneel. Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (inclusief de vierkante haakjes). |
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
| [!UICONTROL Ad ID] | Vereist om advertenties uit te geven of te schrappen tenzij de rij &quot;[!UICONTROL AMO ID]&quot;omvat. |
| [!UICONTROL AMO ID] | Je moet advertenties bewerken of verwijderen, tenzij je de advertentie-id opneemt. |

### Tekst en velden

Gebruik voor dit advertentietype de rij &quot;[!UICONTROL Creative (except RSA)]&quot; in het dialoogvenster [!UICONTROL Download Bulksheet] .

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

>[!NOTE]
>
>Uitgebreide tekstadvertenties zijn in juni 2022 afgekeurd. U kunt alleen bestaande tekstadvertenties verwijderen.

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Creative Preferred Devices] | Alleen-lezen |
| [!UICONTROL Ad Title], Advertentie Titel 2-3 | Alleen-lezen |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Alleen-lezen |
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
| [!UICONTROL Ad ID] | Vereist slechts wanneer u de advertentiestatus verandert, tenzij de rij a&rpar; voldoende en bezitskolommen omvat om de advertentie te identificeren of b&rpar; &quot;[!UICONTROL AMO ID]&quot;. Als u echter noch de kolommen [!UICONTROL Ad ID] noch [!UICONTROL AMO ID] opneemt en de kolommen met de eigenschap ad overeenkomen met meerdere advertenties, verandert de status voor slechts een van de advertenties. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Dynamische doelvelden (automatisch doel) voor zoeken

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Max CPC] | Optioneel |
| [!UICONTROL Auto Target Expression] | Vereist slechts wanneer campagne die aan &quot;[!UICONTROL Use my website contents to target my ads]&quot;plaatst niet wordt toegelaten. |
| [!UICONTROL Match Type] | Optioneel |
| [!UICONTROL Target Status] | Vereist om een doel te verwijderen |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Target ID] | Vereist slechts wanneer u verandert of het autodoel schrapt, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor het doel omvat. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Velden voor productgroepen kopen

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
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
| [!UICONTROL Product Group ID] | Vereist slechts wanneer u verandert of de productgroep schrapt, tenzij de rij a) voldoende bezitskolommen omvat om de productgroep te identificeren of b) &quot; [!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Sitemelinktvelden op campagnereniveau en op groepsniveau

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
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
| [!UICONTROL Sitelink ID] | Vereist slechts wanneer u de sitelink verandert of schrapt, tenzij de rij a) voldoende bezitskolommen omvat om sitelink of b) te identificeren &quot;[!UICONTROL AMO ID]&quot;. Als u echter geen [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID] opneemt en de eigenschapskolommen overeenkomen met meerdere sitelinks, verandert de status voor slechts een van de sitelinks.<br><br><b> Nota:</b> als u sitelink bezitskolommen behalve [!UICONTROL Status] voor bestaande sitelink uitgeeft, en u of [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID] omvat, dan wordt een nieuwe sitelink gecreeerd, en bestaande sitelink wordt niet veranderd. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Locatiedoel

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Location] | Vereist |
| [!UICONTROL Location Type] | Optioneel |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL Location Status] | Alleen vereist om een locatiedoel te verwijderen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u [!UICONTROL Campaign ID] opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Apparaatdoelvelden op campagnereniveau en op ad-groepniveau

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Device] | Vereist voor het maken of bewerken van een apparaatdoel. |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL Ad Group Name] | Vereist voor apparaatdoelen op ad-groepsniveau. Niet van toepassing op apparaatdoelen op campagneniveau. |
| [!UICONTROL Device Target Status] | Alleen vereist om een apparaatdoel te verwijderen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel; alleen van toepassing op ad-group-apparaatdoelen. |
| [!UICONTROL Device Target ID] | Vereist slechts wanneer u verandert of het doel schrapt, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor het doel omvat. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de apparaatdoel-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Campagne- en ad-group-niveau RLSA-doel-/uitsluitingsvelden

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-google).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL Ad Group Name] | Vereist voor streefcijfers en uitsluitingen op groepsniveau. Niet van toepassing op streefcijfers en uitsluitingen op campagneniveau. |
| [!UICONTROL Audience] | Vereist om een nieuw doel of een nieuwe uitsluiting te creëren. |
| [!UICONTROL Target Type] | Vereist om een nieuw doel of een nieuwe uitsluiting te creëren. |
| [!UICONTROL RLSA Target Status] | Alleen vereist om een doel of uitsluiting te verwijderen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel; alleen van toepassing op streefcijfers en uitsluitingen op ad-groepsniveau. |
| [!UICONTROL RLSA Target ID] | Vereist slechts wanneer u verandert of het doel schrapt, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor het doel omvat. |
| [!UICONTROL AMO ID] | Vereist om de gegevens uit te geven of te schrappen tenzij u identiteitskaart van het Doel RLSA omvat.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

>[!MORELIKETHIS]
>
>* [&#x200B; Bijlage - de fouten van het Bulksheet &#x200B;](../bulksheet-errors.md)
>* [&#x200B; Verrichtingen u in bulksbladen kunt uitvoeren &#x200B;](bulksheet-operations.md)
>* [&#x200B; Ondersteunde formaten van het bulkbladdossier &#x200B;](bulksheet-file-formats.md)
>* [&#x200B; Download/creeer een bulksheet- dossier &#x200B;](../bulksheet-download.md)
>* [&#x200B; klik-volgende formaten voor  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [&#x200B; upload een bulksheet- dossier of verbeterd foutendossier &#x200B;](../bulksheet-upload.md)
