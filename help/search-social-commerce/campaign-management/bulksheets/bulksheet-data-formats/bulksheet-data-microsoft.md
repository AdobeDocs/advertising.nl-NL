---
title: Vereiste gegevens voor het bulkwerkblad [!DNL Microsoft Advertising] rekeningen
description: Verwijs naar de vereiste kopbalgebieden en gegevensgebieden in bulksbladen voor [!DNL Microsoft Advertising] rekeningen.
source-git-commit: 964ee8431d9f1d03b0c9eec8906ab5a0b7940222
workflow-type: tm+mt
source-wordcount: '7615'
ht-degree: 1%

---

# Aanhangsel - Vereiste gegevens voor het informatieblad voor [!DNL Microsoft Advertising] rekeningen

Om te creëren en bij te werken [!DNL Microsoft Advertising] Campagne gegevens in bulk, kunt u Onderzoek, Sociale, &amp; het bulksbladdossiers van de Handel gebruiken die specifiek voor worden geformatteerd [!DNL Microsoft Advertising] rekeningen. U kunt een van beide [bulkbladbestanden genereren voor bestaande accounts](../bulksheet-download.md) in de vereiste bestandsindeling of b) handmatig aanmaken (zie &quot;[Ondersteunde bestandsindelingen voor bulkbladbestanden](bulksheet-file-formats.md)&quot; voor algemene informatie over de ondersteunde bestandsindelingen).

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## Alle beschikbare gegevensvelden

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Veld | Beschrijving |
|----|----|
| Platform | (Opgenomen in gegenereerde bulksbladen ter informatie) Het advertentieplatform. Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Naam van account | De unieke naam die een advertentienetwerkaccount identificeert. Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | De unieke naam die een campagne voor een account identificeert. De maximumlengte is 128 tekens. |
| Campagnebudget | Het dagelijkse of maandelijkse campagnebudget, met of zonder monetaire symbolen en leestekens. Het mag niet minder zijn dan 0,05. |
| Kanaaltype | Het type kanaal dat de campagne als doel heeft: <i>Publiek</i>, <i>DynamicSearchAds</i>, <i>Zoeken</i>, of <i>Winkelen</i>. |
| Leveringsmethode | (Alleen campagnes met dagelijkse budgetten) Hoe snel u elke dag advertenties voor de campagne kunt weergeven:<ul><li><i>Standaard (gedistribueerd)</i> (de standaardinstelling voor nieuwe campagnes): Om uw advertenties over de dag te verspreiden.</li><li><i>Versneld:</i> Zo vaak mogelijk advertenties weergeven totdat uw budget is bereikt. Hierdoor worden uw advertenties mogelijk niet later op de dag weergegeven.</li></ul> |
| Campagneprioriteit | (Alleen winkelcampagnes) De prioriteit waarmee de campagne wordt gebruikt wanneer meerdere campagnes hetzelfde product adverteren: <i>Laag</i> (standaard voor nieuwe campagnes), <i>Normaal</i>, of <i>Hoog</i>.<br><br>Wanneer hetzelfde product in meer dan één campagne is opgenomen, gebruikt het advertentienetwerk eerst de campagneprioriteit om te bepalen welke campagne (en het bijbehorende bod) in aanmerking komt voor de advertentieveiling. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel. |
| Merchant ID | (Winkelcampagnes en publiekscampagnes die alleen zijn gekoppeld aan een commerciële feed) De klant-id van het zakelijke account waarvan de producten voor de campagne worden gebruikt. |
| Verkoopland | (Alleen koopcampagnes; alleen-lezen voor bestaande campagnes) Het land waar de campagneproducten worden verkocht. Omdat de producten met doellanden worden geassocieerd, bepaalt dit het plaatsen welke producten in de campagne worden geadverteerd. |
| Filter Productbereik | (Campagnes die het winkelnetwerk slechts gebruiken) De producten in uw handelaarrekening waarvoor productadvertenties voor de campagne kunnen worden gecreeerd. U kunt maximaal zeven productafmetingen en kenmerkcombinaties ingaan waarop om uw producten te filtreren, gebruikend het formaat dimensi=attribute. Scheid meerdere filters met een scheidingsteken &quot;>>&quot;. Voor een lijst met beschikbare productafmetingen raadpleegt u &quot;[Productfilters voor winkelcampagne](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;<br><br> Voorbeeld: &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> Als u de bestaande waarden wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| DSA-domeinnaam | (Campagnes van het type a) &quot;<i>DynamicSearchAds</i>&quot; of b) &quot;<i>Zoeken</i>&quot; als het element ExperimentId niet is ingesteld) De domeinnaam van de website die als doel moet dienen voor dynamische zoekopdrachten. De maximale lengte is 2.048 tekens. Als de domeinnaam `www`, het is afgesneden en niet gebruikt.<br><br>Voor bestaande campagnes, kunt u niet het domein uitgeven, maar u moet het omvatten om andere eigenschappen bij te werken. |
| DSA-domeintaal | (Campagnes van het type a) &quot;<i>DynamicSearchAds</i>&quot; of b) &quot;<i>Zoeken</i>&quot; als het element ExperimentId niet is ingesteld) De taal van de websitepagina&#39;s die moet worden gebruikt voor dynamische zoekopdrachten. De ondersteunde domeintalen zijn Nederlands, Engels, Frans, Duits, Italiaans, Spaans en Zweeds.<br><br>Voor bestaande campagnes, kunt u niet de taal uitgeven, maar u moet het omvatten om andere eigenschappen bij te werken. |
| Naam advertentiegroep | De unieke naam die een advertentiegroep identificeert. De maximumlengte is 128 tekens. Navolgende lege tekens worden niet opgeslagen (zoals &#39;Groep 1 toevoegen&#39; wordt opgeslagen als &#39;Groep 1 toevoegen&#39;). |
| Type advertentiegroep | (Campagnes op het onderzoeksnetwerk; alleen-lezen voor bestaande advertentiegroepen) Het type advertentiegroep: <i>Publiek</i> (alleen voor publiekscampagnes), <i>Dynamisch zoeken</i> (alleen voor dynamische zoekopdrachten) en <i>Zoekstandaard</i> (alleen voor responsieve zoekopdrachten en bestaande uitgevouwen tekstadvertenties). Sommige soorten campagnes kunnen veelvoudige advertentiegroep types omvatten. |
| Trefwoord | (Campagnes op het onderzoeksnetwerk slechts) het sleutelwoordkoord. De maximumlengte is 50 tekens.<br><br><b>Opmerkingen:</b><ul><li>Als u een trefwoord op advertentiegroep- of campagnereniveau wilt uitsluiten, stelt u het type Afstemmen in op `Negative`. Als de rij de naam van de advertentiegroep bevat, wordt het trefwoord uitgesloten voor de advertentiegroep. Als de rij niet de naam van de advertentiegroep omvat, wordt het sleutelwoord uitgesloten voor de volledige campagne.</li><li>Als u het trefwoord Microsoft Advertising wijzigt, wordt het bestaande trefwoord verwijderd en wordt een nieuw trefwoord met een nieuwe id gemaakt. Als u het overeenkomsttype wijzigt, wordt het bestaande trefwoord echter niet verwijderd.</li></ul> |
| Plaatsing | Vervangen |
| Publiek | De lijst voor het opnieuw op de markt brengen van onderzoeksadvertenties (RLSA) doelpubliek voor de campagne of de ad groep. |
| Doeltype | (Alleen RLSA-doelen) Het doeltype: <i>Opname</i> of <i>Uitsluiting</i>. |
| Automatische doelexpressie | Dynamische zoekdoelen voor de advertentiegroep. Gebruik voor alle doelen &quot;Alle webpagina&#39;s&quot;.<br><br>Als u maximaal drie dynamische zoekcriteria als doel wilt instellen, gebruikt u de indeling `<category>=<target>`, waarbij &lt;category> kan alle onderstaande rubrieken bevatten. Meerdere doelen samenvoegen voor een afzonderlijke categorie met &quot;`[blank space] and [blank space]`&quot; en voeg meerdere categorieën samen met &quot;`[blank space] and [blank space]`&quot;.<br><ul><li><i>Categorie:</i> Dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met een specifieke Google-inhoudscategorie.</li><li><i>URL:</i> Dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met een specifieke URL, waarbij de waarde overal in de URL kan worden opgenomen.</li><li><i>Paginatitel:</i> Dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met specifieke tekst in de paginatitel.</li><li><i>Pagina-inhoud:</i> Dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met specifieke inhoud.</li></ul>Voorbeeld: url=schoenen.example.com en page title=schoenen<br>Voorbeeld: Alle webpagina&#39;s |
| Locatie | Een geografische locatie waar advertenties voor de campagne of de ad-hocgroep moeten worden geplaatst; de waarden zijn niet hoofdlettergevoelig. Als u geen waarden voor de campagne of advertentiegroep invoert, worden alle locaties als doel ingesteld. Als u specifieke locaties als doel wilt instellen, voert u de locatie in met behulp van de code-indelingen voor Microsoft-publicatielocaties. Als u een locatielijst wilt downloaden, meldt u zich aan bij de Microsoft Advertising developer portal met de gegevens van uw advertentieaccount voor Microsoft Advertising. <b>Opmerking:</b> Als u een locatie wilt uitsluiten, plaatst u voor de locatiecode een minteken (`-`), zoals `-United States`. |
| Locatietype | Het type locatie, zoals Plaats, Land, MetroArea, PostalCode en Frame. Als u een locatielijst wilt downloaden, meldt u zich aan bij de Microsoft Advertising developer portal met de gegevens van uw advertentieaccount voor Microsoft Advertising. |
| Type afstemmen | (Alleen campagnes op het zoeknetwerk) De optie(s) voor trefwoordafstemming. Dit kan de optie voor trefwoordafstemming voor een dynamisch zoekdoel of een productgroep omvatten. Waarden zijn: <i>Breed</i> (standaard voor nieuwe trefwoorden), <i>Exact</i>, <i>Woorden</i>, <i>Inhoud</i> (automatisch instellen voor trefwoorden wanneer de advertentiegroep het inhoudsnetwerk aanwijst), <i>Negatief</i> (om een trefwoord uit te sluiten op het netwerk van inhoud), <i>Dynamisch ad-doel</i> (standaard voor nieuwe dynamische zoekdoelen), <i>Productgroep</i> (standaard voor nieuwe productgroepen), of <i>Negatieve productgroep</i> (om een productgroep uit te sluiten).  Een waarde voor of het gelijke type of sleutelwoordidentiteitskaart wordt vereist om een sleutelwoord met veelvoudige gelijke types uit te geven of te schrappen.<br><br>Kies voor Breedte overeenkomst aanpassen de optie &quot;Breed&quot; en voeg een `+` vóór elk woord binnen het vereiste trefwoord (zoals &quot;`+red +shoes`&quot; om zowel &quot;rood&quot; als &quot;schoenen&quot; te vereisen).<br><br>Als u het overeenkomsttype voor een Microsoft-trefwoord voor advertenties wijzigt, wordt het bestaande trefwoord niet verwijderd. |
| Max CPC | (Campagnes op het onderzoeksnetwerk) De maximumkosten per klik (CPC), die het hoogste bedrag voor een advertentieklik is dat op het sleutelwoord, de productgroep, of het dynamische onderzoeksdoel wordt gebaseerd, met of zonder monetaire symbolen en punctuatie.  Voor bestaande trefwoorden en productgroepen zijn de records in geoptimaliseerde portfolio&#39;s slechts één dag geldig en worden de updates tijdens de volgende optimalisatiecyclus overschreven. <b>Opmerking:</b> Je kunt geen biedingen instellen voor negatieve trefwoorden. |
| Max. inhoud CPC | (Alleen-lezen voor CPC-campagnes die zijn gemaakt voordat het inhoudsnetwerk in 2017 is afgekeurd) De maximale kosten voor inhoud per klik (CPC). Dit is het hoogste bedrag dat wordt betaald voor een advertentie via een netwerksite voor weergave, met of zonder monetaire symbolen en interpunctie. |
| Doelmethode publiek | (Publiek en groepen) Of:<ul><li><i>Doel en bod:</i> Alleen advertenties weergeven voor gebruikers die zijn gekoppeld aan doelgroepen die ook voldoen aan andere doelen voor de advertentiegroep.</li><li><i>Alleen bod:</i>Advertenties tonen zelfs aan mensen die niet met doelpubliek worden geassocieerd zolang zij andere doelstellingen op groepsniveau voldoen.</li></ul> U kunt de kans echter vergroten dat advertenties bij een bepaald publiek worden getoond door voor dat publiek hogere biedingen in te stellen. |
| Bovenliggende productgroepen | De hiërarchie van bovenliggende productgroepen.<br><br>Voorbeeld: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| Productgroepering | De productgroep (zoals &quot;brand=acme&quot; of &quot;Alle producten&quot;).<br><br><b>Opmerkingen:</b><ul><li>Wanneer een gespecificeerde productgroep niet in de hiërarchie van de Groepen van het Product van de Ouder bestaat, leidt het Onderzoek, Sociale, &amp; Handel tot om het even welke delen van de hiërarchie die nodig zijn.</li><li>Met Zoeken, Sociaal en Handel maakt u automatisch een groep Alle producten wanneer u een advertentiegroep maakt in een Google-winkelcampagne met een standaardbod ingesteld op het standaardbod van de advertentiegroep. Met Zoeken, Sociale media en Handel wordt automatisch een &quot;Everything Else&quot;-groep gemaakt met het standaardbod van de advertentiegroep op elk niveau van de hiërarchie van de productgroepen. U kunt deze standaardgroepen nog steeds expliciet maken en ze uitsluiten of hun biedingen wijzigen.</li><li>Elke advertentiegroep kan tot acht niveaus van productgroepen, met inbegrip van &quot;Alle Producten&quot;en zeven andere lagen omvatten.</li></ul> |
| Type partitie | Het partitietype voor de productgroep: <i>onderverdeling</i> (als het onderliggende productgroepen heeft) of <i>eenheid</i> (als het geen onderliggende productgroepen heeft). |
| Advertentitel, advertentietak 2-15 | (Alleen uitgevouwen tekstadvertenties, multimediadaden, responsieve advertenties en responsieve zoekadvertenties) De kopregels van een advertentie. De maximumlengte voor elk veld van de advertentie is 30 tekens of 15 double-byte tekens, inclusief alle dynamische tekst (zoals de waarden van trefwoorden). `{Param2}` en `{Param3}` dynamische substitutievariabelen en adverteerders).<br><br> Voor responsieve zoekadvertenties voegt u een advertentieklanker in in de volgende indeling, waarbij &#39;Standaardtekst&#39; een optionele waarde is die moet worden ingevoegd wanneer het invoerbestand geen geldige waarde bevat: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Voor uitgevouwen tekstadvertenties zijn Titel toevoegen en Titel 2 toevoegen vereist en Titel 3 toevoegen is optioneel. In Microsoft Advertising zijn uitgebreide tekstadvertenties in augustus 2022 vervangen. U kunt nu alleen rapporten hierover publiceren en deze verwijderen.<br><br>Voor multimediadaden, responsieve advertenties en responsieve zoekopdrachten zijn Advertentitel, Advertentitel 2 en Advertentitel 3 vereist en zijn alle andere titelvelden van de advertentie optioneel.<br><br>Als u de bestaande waarde voor een niet-vereist veld wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes).<br><br>Voor alle advertentietypen, behalve voor uitgevouwen tekstadvertenties, verwijdert het wijzigen van de advertentiekopie de bestaande advertentie en maakt een nieuwe advertentie met dezelfde eigenschappen. |
| Titel 1-15 Positie toevoegen | (Alleen responsieve zoekopdrachten; (optioneel) Een positie waarop de corresponderende advertentitel moet worden vastgezet: `[null]` (geen waarde waardoor de titel van de advertentie voor alle posities in aanmerking komt), 1, 2 of 3. Als Positie advertentie bijvoorbeeld de waarde 1 heeft, wordt Titel toevoegen alleen weergegeven in Positie 1. Standaard zijn alle advertentitels null (geen waarden). Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes).<br><br><b>Opmerking:</b> U kunt meerdere advertentitels vastzetten op dezelfde positie. In het advertentienetwerk wordt een van de advertentietitels gebruikt die op de positie zijn vastgezet. Titels die op positie 3 zijn vastgezet, worden mogelijk niet met de advertentie weergegeven. |
| Beschrijving regel 1-4 | (Tekstadvertenties, dynamische zoekadvertenties, multimedia-advertenties, responsieve zoekadvertenties en alleen verbeterde sitelinks op campageniveau) De hoofdtekst van een advertentie of sitelink.<br><br>Voor sitelinks kunt u desgewenst zowel Beschrijving regel 1 als Beschrijving regel 2 gebruiken om extra tekst op te nemen die het advertentienetwerk onder de koppelingstekst kan weergeven. Elk beschrijvingsveld kan maximaal 35 single-byte of 17 double-byte tekens bevatten.<br><br>Voor advertenties is de maximale lengte voor elk beschrijvingsveld 90 tekens of 45 double-byte tekens, inclusief alle dynamische tekst (zoals de waarden van trefwoorden en adverteerders).<br><br>Voor responsieve zoekadvertenties voegt u een advertentieklanker in in de volgende indeling, waarbij Standaardtekst een optionele waarde is die moet worden ingevoegd wanneer uw feed-bestand geen geldige waarde bevat: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Voor tekstadvertenties en dynamische zoekadvertenties is Beschrijving regel 1 vereist en Beschrijving regel 2 is optioneel.<br><br>Voor multimediaadvertenties, responsieve advertenties en responsieve zoekopdrachten zijn beschrijvingsregel 1 en beschrijvingsregel 2 vereist en beschrijvingsregel 3 en beschrijvingsregel 4 zijn optioneel.<br><br>Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes).<br><br><b>Opmerkingen:</b><ul><li>(Standaardtekstadvertenties) De gecombineerde titel en tekst moeten ten minste drie woorden lang zijn.</li><li>(Uitgebreide tekstadvertenties) Dit veld kan optioneel de opdracht {Param2} en {Param3} dynamische vervangingsvariabelen. In dat geval is de maximale lengte van de advertentietekst 300 single-byte of 150 double-byte tekens. In Microsoft Advertising zijn uitgebreide tekstadvertenties in augustus 2022 vervangen. U kunt nu alleen rapporten hierover publiceren en deze verwijderen.</li><li>(Dynamische zoekopdrachten) Dynamische vervangingstekst is niet toegestaan.</li><li>Voor alle advertentietypen, behalve uitgevouwen tekstadvertenties, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie.</li></ul> |
| Beschrijving regel 1-4 positie | (Alleen responsieve zoekopdrachten; (optioneel) Een positie waarop de desbetreffende beschrijving moet worden vastgezet: `[null]` (geen waarde waardoor de beschrijving voor alle posities in aanmerking komt), 1, 2 of 3. Als Beschrijving 1 Positie bijvoorbeeld de waarde 1 heeft, wordt Beschrijving 1 alleen weergegeven in Positie 1. Standaard zijn geen beschrijvingen vastgezet op een positie.<br><br>Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes).<br><br><b>Opmerking:</b> U kunt meerdere beschrijvingen vastzetten op dezelfde positie. Het advertentienetwerk zal één van de beschrijvingen gebruiken die aan de positie worden vastgezet. Beschrijvingen die op positie 2 zijn vastgezet, mogen niet met de advertentie worden getoond. |
| Bedrijfsnaam | (Alleen multimediaadvertenties) De bedrijfsnaam, met maximaal 25 tekens. |
| Aanbiedingslijn | (Alleen aanbiedingen voor producten) Een unieke promotielijn die in de zoekresultaten bij de aanbieding van het product moet worden gevoegd (zoals Nu gratis verzending). De maximumlengte is 45 tekens.<br><br>De promotielijn kan op verschillende plaatsen ten opzichte van de advertentie (zoals onder de advertentie) verschijnen, afhankelijk van waar de advertentie op de pagina wordt weergegeven. |
| URL weergeven | De URL die is opgenomen in de advertentie.<br><br>Voor uitgebreide dynamische zoekopdrachten genereert het advertentienetwerk deze waarde dynamisch vanuit het websitedomein en hoeft u geen waarde in te voeren.<br><br>Voor uitgevouwen tekstadvertenties en responsieve zoekopdrachten hoeft u geen waarde in te voeren. De weergave-URL wordt automatisch opgehaald uit het domein in de uiteindelijke URL. U kunt de URL desgewenst aanpassen met de velden Pad 1 en Pad 2.<br><br><b>Opmerkingen:</b><ul><li>(Accounts met definitieve URL&#39;s) De domeinnamen in de weergave-URL en de uiteindelijke URL moeten overeenkomen.</li><li>In Microsoft Advertising zijn uitgebreide tekstadvertenties in augustus 2022 vervangen. U kunt nu alleen rapporten hierover publiceren en deze verwijderen.</li></ul> |
| Pad 1 weergeven | (Alleen uitgevouwen tekstadvertenties, dynamische zoekadvertenties en responsieve zoekadvertenties) Tekst die aan de weergave-URL is toegevoegd en die automatisch uit de uiteindelijke URL wordt geëxtraheerd. Elk pad wordt voorafgegaan door een slash (/) in de URL. Een pad mag geen forward slash (/) of newline (\n) tekens bevatten. De maximumlengte voor elk pad is 15 tekens of 7 double-byte tekens.<br><br>Als u een advertentieklanter wilt invoegen, gebruikt u de volgende indelingen, waarbij &#39;Standaardtekst&#39; een optionele waarde is die moet worden ingevoegd wanneer uw feed-bestand geen geldige waarde bevat: `{CUSTOMIZER.Attribute name:Default text}`, zoals `{CUSTOMIZER.Discount:10%}`<br><br>Als bijvoorbeeld Pad 1 weergeven &quot;deals&quot; is, is de URL van de weergave &lt;display url=&quot;&quot;>/deals, zoals www.example.com/deals.<br><br>In Microsoft Advertising zijn uitgebreide tekstadvertenties in augustus 2022 vervangen. U kunt nu alleen rapporten hierover publiceren en deze verwijderen. |
| Pad 1 weergeven | (Alleen uitgebreide tekstadvertenties, dynamische zoekadvertenties en responsieve zoekopdrachten) Een extra weergavepad. zie de ingang voor de Weg van de Vertoning 1.<br><br>Voorbeeld: Als Weergavepad 1 &quot;deals&quot; is en Weergavepad 2 &quot;lokaal&quot; is, is de weergave-URL &lt;<i>URL weergeven</i>>/deals/local, zoals www.example.com/deals/local. |
| Begindatum | (Alleen verbeterde sitelinks) De eerste datum waarop biedingen mogen worden uitgebracht voor de sitelink, in de tijdzone van de adverteerder en in een van de volgende formaten: d/m/yyyy, m/d/jj, m-d-jjjj of m-d-jj. De standaard voor nieuwe verbeterde sitelinks is de huidige dag. <b>Opmerking:</b> Nieuwe verbeterde sitelinks kunnen alleen worden gemaakt in campagnes met bestaande verbeterde sitelinks of zonder sitelinks. |
| Einddatum | De laatste datum waarop de sitelink met advertenties kan worden weergegeven in de tijdzone van de adverteerder en in een van de volgende notaties: d/m/yyyy, m/d/jj, m-d-jjjj of m-d-jj. Voor een nieuwe sitelink is de standaardwaarde `[blank]` (dus geen einddatum). |
| Oproep tot actie | De oproep tot actie om op te nemen in de advertentie. Zie de [API-referentie voor een lijst met mogelijke waarden](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction), maar voer aanroepen van meerdere woorden naar handeling in als meerdere woorden (zoals &quot;Nu ophalen&quot; in plaats van &quot;Nu ophalen&quot;) in bulksbladen. |
| Oproep tot actie | De taal voor de vraag aan actieopties. Zie de [API-referentie voor een lijst met mogelijke talen](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| Basis-URL/Definitieve URL | De bestemmingspagina URL waarnaar de gebruikers van de onderzoeksmotor worden genomen wanneer zij uw advertentie klikken, met inbegrip van om het even welke toevoegingsparameters die voor de campagne of de rekening worden gevormd. Basis/definitieve URLs op het sleutelwoordniveau treedt die op het advertentieniveau en hoger met voeten.<br><br>Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| Doel-URL | (Ter informatie opgenomen in gegenereerde bulksbladen; (niet gepost aan de zoekmachine) Voor accounts met doel-URL&#39;s is dit de URL die een advertentie koppelt aan een basis-URL/bestemmingspagina op de website van de adverteerder (soms via een andere site die de klik bijhoudt en de gebruiker vervolgens doorstuurt naar de bestemmingspagina). Het omvat om het even welke toevoegingsparameters die voor de Onderzoek, Sociale, &amp; de campagne of de rekening van de Handel worden gevormd. Als u URL&#39;s voor bijhouden hebt gegenereerd, is dit gebaseerd op de volgende parameters in uw accountinstellingen en campagnemontages. Als u specifieke parameters voor zoekprogramma&#39;s hebt toegevoegd, kunnen deze worden vervangen door de equivalente parameters voor Zoeken, Sociale &amp; Handel.<br><br>Voor accounts met uiteindelijke URL&#39;s geeft deze kolom dezelfde waarde weer als de kolom Basis-URL/Definitieve URL. |
| Aangepast URL-parameters | Gegevens ter vervanging van de `{custom_code}` dynamische variabele wanneer de variabele is opgenomen in de volgende parameters voor de instellingen van de zoekaccount of campagne. Als u de aangepaste waarde in de URL voor bijhouden wilt invoegen, moet u het bestand met de opsommingstekens uploaden met de optie URL&#39;s voor bijhouden genereren. |
| Creatief type | De advertentievorm: <i>Dynamische zoekopdracht</i>, <i>Toegevoegde tekst uitgebreid</i>, <i>Uitgebreide advertentie voor dynamisch zoeken</i>, <i>Multimedia-advertentie</i>, <i>Productadvertentie</i> (winkeladvertenties), of <i>Responsieve zoekadvertentie</i>, of <i>Tekst en tekst</i>. De standaardinstelling voor nieuwe advertenties is <i>Tekst en tekst</i>. |
| Begindatum van groep toevoegen | De eerste datum waarop biedingen voor de advertentiegroep mogen worden geplaatst, in de tijdzone van de adverteerder en in een van de volgende formaten: d/m/yyyy, m/d/jj, m-d-jjjj of m-d-jj. Voor een nieuwe advertentiegroep is de standaardwaarde de huidige datum. |
| Einddatum van groep toevoegen | De laatste datum waarop biedingen voor de advertentiegroep mogen worden geplaatst, in de tijdzone van de adverteerder en in een van de volgende formaten: d/m/yyyy, m/d/jj, m-d-jjjj of m-d-jj. Voor een nieuwe advertentiegroep is de standaardwaarde [blank] (dus geen einddatum). |
| Sjabloon voor bijhouden | (Optioneel) De sjabloon voor reeksspatiëring, die alle parameters voor het omleiden en bijhouden van domeinen opgeeft en de laatste URL in een parameter insluit. De het volgen malplaatje op het meest korrelige niveau (met sleutelwoord als meest korrelig) treedt de waarden op alle hogere niveaus met voeten.<br><br>Voor het bijhouden van reclame-conversies voor Adobe, die wordt toegepast wanneer de instellingen voor de campagne &#39;EF omleiden&#39; en &#39;Automatisch uploaden&#39; bevatten, voegt Search, Social &amp; Commerce automatisch code voor omleiding en tekstspatiëring toe wanneer u de record opslaat.<br><br>Voer een waarde in voor omleidingen en bijhouden door derden.<br><br>Raadpleeg de documentatie bij Microsoft-advertenties voor een lijst met parameters die uiteindelijke URL&#39;s aangeven in trackingsjablonen.<br><br> Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| Achtervoegsel bestemmingspagina | Alle parameters die aan het einde van de uiteindelijke URL&#39;s moeten worden toegevoegd om informatie bij te houden. Voorbeeld: `param2=value1&param3=value2`<br><br>Zie &quot;[Opmaak voor het bijhouden van klikken voor [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).&quot;<br><br>De laatste URL-achtervoegsels op lagere niveaus overschrijven het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Als u een achtervoegsel op advertentieniveau of lager wilt configureren, gebruikt u de Microsoft Advertising Editor. |
| Netwerkstatus zoeken | Of u advertenties voor de advertentiegroep op verschillende elementen van het Zoeknetwerk wilt plaatsen:<ul><li><i>Alle:</i> Om advertenties op alle Bing onderzoeksnetwerken en syndicated onderzoekspartners te plaatsen.</li><li><i>OwnedAndOperatedOnly:</i>Als u alleen advertenties op Bing en Yahoo wilt plaatsen! websites.</li><li><i>SyndicatedSearchOnly:</i> Als u alleen advertenties op Bing en Yahoo wilt plaatsen! gesynchroniseerde zoekpartners.</li><li><i>Uit:</i> Om advertenties op het Netwerk van de Inhoud slechts (niet het Netwerk van het Onderzoek) te plaatsen.</li></ul> Voor nieuwe advertentiegroepen is de standaardwaarde Aan. |
| Inhoudsnetwerkstatus | Vervangen |
| Talen | De doeltaal voor advertenties in de advertentiegroep: Engels, Frans, Fins, Duits, Noors, Spaans of Zweeds. De standaardinstelling voor nieuwe campagnes is Engels.<br><br>Deze instelling bepaalt in welke landen en regio&#39;s uw advertentie kan worden weergegeven. Zorg ervoor dat u een taal kiest die compatibel is met de locatiedoelen van de campagne. |
| Begrotingstype | Of de begroting <i>Dagelijks</i> (de standaardwaarde) of <i>Maandelijks</i>.<br><br>Opmerking: Als u de campagne toewijst aan een geoptimaliseerde portfolio, wordt deze waarde automatisch ingesteld op Dagelijks. |
| Apparaat | Een apparaattype waarvoor biedaanpassingen worden uitgevoerd op campagne- of advertentieniveau: <i>smartphone</i>, <i>tablet</i>, of <i>desktop</i>. |
| Bodaanpassing | De bodaanpassing voor een opgegeven doeltype. Als het bod op het trefwoordniveau bijvoorbeeld 1 USD is en het bod voor smartphones 50% is, is het bod op de smartphone 1,50 USD. Standaard worden alle doelen geboden bij het bod op trefwoordniveau. Geldige percentages zijn:<ul><li>Smartphones en tablets: -100 (om niet te bieden op het apparaattype) en van -90 tot 900</li><li>Desktop: van 0 tot en met 900</li></ul> |
| Creatieve voorkeursapparaten | De apparaattypen waarop u de advertentie of sitelink wilt weergeven: <i>Alles</i> (de standaardwaarde) of <i>Mobiel</i>. Wanneer Mobiel is opgegeven, probeert het netwerk de advertentie of sitelink aan gebruikers van mobiele apparaten weer te geven in plaats van aan gebruikers van desktopcomputers of tablets. Anders, zal het netwerk de advertentie of sitelink op om het even welk apparatentype tonen. <b>Opmerking:</b> Het netwerk garandeert niet dat de advertentie op het voorkeurstype wordt weergegeven. |
| Param2 | De tekenreeks die als vervangende waarde moet worden gebruikt als de basis-URL van het trefwoord of de titel, beschrijving of basis-URL van de advertentie de volgende code bevat: `{Param2}` dynamische substitutiereeks. De maximumlengte is 70 tekens, maar houd rekening met de maximumlengte van het advertentie-element waarin u het element wilt gebruiken (de combinatie van Titel 1 en Titel 2 kan bijvoorbeeld maximaal 76 tekens bevatten). Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| Param3 | De tekenreeks die als vervangende waarde moet worden gebruikt als de basis-URL van het trefwoord of de titel, beschrijving of basis-URL van de advertentie de volgende code bevat: `{Param3}` dynamische substitutiereeks. De maximumlengte is 70 tekens, maar houd rekening met de maximumlengte van het advertentie-element waarin u het element wilt gebruiken (de combinatie van Titel 1 en Titel 2 kan bijvoorbeeld maximaal 76 tekens bevatten). Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| Koppelingsnaam | De sitelink-tekst. Het moet uniek zijn in de campagne. Als u Description1 en Description2 specificeert, dan kan de sitelink tekst tot 25 single-byte of 12 dubbel-byte karakters omvatten; anders kan de sitelink-tekst maximaal 35 single-byte of 17 double-byte tekens bevatten.<br><br>In Microsoft Advertising kunnen twee, vier of zes verbeterde sitelinks met beschrijvingen worden weergegeven, of vier of zes sitelinks in één rij zonder beschrijvingen, met een advertentie.<br><br>U kunt nieuwe verbeterde sitelinks alleen maken in campagnes met bestaande verbeterde sitelinks of zonder sitelinks. |
| Campagnestatus | De weergavestatus van de campagne: <i>Actief</i>, <i>Gepauzeerd</i>, of <i>Verwijderd</i> (alleen bestaande campagnes). Het gebrek voor nieuwe campagnes is Actief. Als u een actieve of gepauzeerde campagne wilt verwijderen, voert u de waarde in `Deleted`. |
| Status van advertentiegroep | De weergavestatus van de advertentiegroep: <i>Actief</i>, <i>Gepauzeerd</i>, of <i>Verwijderd</i> (alleen bestaande advertentiegroepen). De standaardinstelling voor nieuwe advertentiegroepen is Actief. Als u een actieve of gepauzeerde ad-groep wilt verwijderen, voert u de waarde in `Deleted`. |
| Trefwoordstatus | De weergavestatus van het trefwoord: <i>Actief</i>, <i>Gepauzeerd</i>, of <i>Verwijderd</i> (alleen bestaande trefwoorden). De standaardwaarde voor nieuwe trefwoorden is Actief. Als u een actief of gepauzeerd trefwoord wilt verwijderen, voert u de waarde in `Deleted`. <b>Opmerking:</b> Als u URL&#39;s bijhouden maakt voor een trefwoord met meerdere typen overeenkomsten, moet de status van het trefwoord voor elk type overeenkomst gelijk zijn. |
| Plaatsingsstatus | Vervangen |
| Advertentiestatus | De weergavestatus van de advertentie: <i>Actief</i>, <i>Verwijderd</i> (alleen bestaande advertenties), <i>Afgekeurd</i> (niet bewerkbaar), of <i>Gepauzeerd</i>. De standaardinstelling voor nieuwe advertenties is Actief. Als u een actieve of gepauzeerde advertentie wilt verwijderen, voert u de waarde in `Deleted`. |
| Doelstatus | De status van een dynamisch zoekdoel: <i>Actief</i>, <i>Gepauzeerd</i>, of <i>Verwijderd</i> (alleen bestaande streefcijfers). Het gebrek voor nieuwe doelstellingen is Actief. Als u een actief of gepauzeerd doel wilt verwijderen, voert u de waarde in `Deleted`. |
| Sitelink-status | De weergavestatus van de sitelink: <i>Actief</i> of <i>Verwijderd</i> (alleen bestaande sitelinks). De standaardinstelling voor nieuwe sitelinks is Actief. Als u een actieve sitelink wilt verwijderen, voert u de waarde in `Deleted`. |
| Locatiestatus | De status van het locatiedoel: <i>Actief</i> of <i>Verwijderd</i> (alleen bestaande locaties). Het gebrek voor nieuwe plaatsen is Actief. Als u een actieve locatie wilt verwijderen, voert u de waarde in `Deleted`. |
| Status van productgroep | De weergavestatus van de productgroep: <i>Actief</i> of <i>Verwijderd</i> (alleen bestaande productgroepen). De standaardwaarde voor nieuwe productgroepen is Actief. Als u een actieve productgroep wilt verwijderen, voert u de waarde in `Deleted`. |
| Doelstatus van apparaat | De status van het apparaatdoel op campagne- of advertentieniveau: <i>Actief</i> of <i>Verwijderd</i>. Voor nieuwe campagnes en advertentiegroepen, is het gebrek Actief. |
| RLSA-doelstatus | De status van de RLSA-doelstelling op campagne- of advertentieniveau of (alleen Google Ads)-uitsluiting: <i>Actief</i> of <i>Verwijderd</i> (alleen bestaande streefcijfers). De standaardinstelling voor nieuwe doelen of uitsluitingen is Actief. Als u een actief doel of een actieve uitsluiting wilt verwijderen, voert u de waarde in `Deleted`. |
| \[Advertiserspecifieke labelclassificatie\] | (Benoemd voor een advertentiespecifieke labelclassificatie, zoals &quot;Kleur&quot; voor een labelclassificatie genaamd Kleur) Een waarde voor de opgegeven classificatie die aan de entiteit is gekoppeld. U kunt per entiteit slechts één waarde per classificatie opnemen (zoals &quot;rood&quot; voor de labelclassificatie &quot;Kleur&quot; voor campagne A). De maximumlengte is 100 tekens en de waarde kan ASCII- en niet-ASCII-tekens bevatten.<br><br>De classificaties van het etiket en hun etiketwaarden worden toegepast op alle kindcomponenten; nieuwe componenten die later worden toegevoegd, worden automatisch aan het label gekoppeld. De etiketclassificaties voor productgroepen worden toegepast op het eenheidniveau (het meest korrelige).<br><br>Noch de classificatienaam noch de classificatiewaarde is hoofdlettergevoelig. |
| Restricties | Een beperking die aan de entiteit is toegewezen. U kunt slechts één beperking per entiteit toewijzen.<br><b>>Restricties worden overgeërfd door onderliggende entiteiten, zodat u geen waarden voor onderliggende entiteiten hoeft in te voeren, tenzij u de overgeërfde waarden wilt overschrijven. |
| Campagne-id | De unieke id die een bestaande campagne identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u de naam van de campagne wijzigt, tenzij de rij een &quot;AMO-id&quot; voor de campagne bevat. |
| Groep-id toevoegen | De unieke id die een bestaande advertentiegroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u de naam van de campagne wijzigt, tenzij de rij een &#39;AMO-id&#39; voor de advertentiegroep bevat. |
| Plaatsing-id | Vervangen |
| Trefwoord-id | De unieke id die een bestaand trefwoord identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Vereist slechts wanneer u het sleutelwoord verandert, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) een &quot;identiteitskaart van AMO.&quot; |
| ID advertentie | <p>De unieke id die een bestaande advertentie identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Voor responsieve zoekopdrachten is de ID van de advertentie of de AMO-id vereist om advertentiegegevens te bewerken of te verwijderen. Voor alle andere entiteitstypen is de AMO-id alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met eigenschappen bevat om de advertentie of b) een &quot;AMO-id&quot; te identificeren. Als u echter noch de ID van de advertentie, noch de AMO-id opneemt en de kolommen met de eigenschap advertentie overeenkomen met meerdere advertenties, verandert de status voor slechts een van de advertenties.</p><p><b>Opmerking:</b> Als u a) en bezitskolommen behalve Status voor een bestaande advertentie uitgeeft, of b) om het even welke gegevens voor een ontvankelijke onderzoeksadvertentie, en u omvat noch identiteitskaart van de Advertentie noch identiteitskaart AMO, dan wordt een nieuwe advertentie gecreeerd, en de bestaande advertentie wordt niet veranderd. </p> |
| Sitelink-id | De unieke id die een bestaande sitelink identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u de sitelink wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de sitelink te identificeren of b) een &quot;AMO-id&quot;. Nochtans, als u noch identiteitskaart Sitelink noch identiteitskaart AMO, en de bezitskolommen veelvoudige sitelinks aanpast, dan zal de status voor slechts één van de sitelinks veranderen.</p><p><b>Opmerking:</b> Als u de kolommen van de sitelink-eigenschap behalve Status voor een bestaande sitelink bewerkt en u noch de Sitelink-id noch de AMO-id opneemt, wordt een nieuwe sitelink gemaakt en wordt de bestaande sitelink niet gewijzigd. |
| Productgroep-id | De unieke id die een bestaande productgroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Dit is alleen vereist wanneer u de productgroep wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de productgroep te identificeren of b) een &quot;AMO-id&quot;. |
| Locatie-id | De unieke advertentie-id van Microsoft voor het locatiedoel. Als u een locatielijst wilt downloaden, meldt u zich aan bij de Microsoft Advertising developer portal met de gegevens van uw advertentieaccount voor Microsoft Advertising. Deze optie is alleen vereist wanneer u het doel van de locatie wijzigt of verwijdert, tenzij de rij een AMO-id voor het doel bevat. |
| Doel-id | De unieke id die een bestaand automatisch doel identificeert. Deze optie is alleen vereist wanneer u het automatische doel wijzigt of verwijdert, tenzij de rij een AMO-id voor het doel bevat. |
| RLSA doel-id | De unieke id die een bestaand RLSA-doel op campagne- of advertentieniveau identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u het doel of de uitsluiting wijzigt of verwijdert, tenzij de rij een &#39;AMO-id&#39; voor het doel bevat. |
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
| Kanaaltype | Vereist om een campagne te maken. |
| Leveringsmethode | Optioneel |
| Campagneprioriteit | Vereist om een winkelcampagne te maken. |
| Merchant ID | Vereist om een winkelcampagne te maken. |
| Verkoopland | Vereist om een winkelcampagne te maken. |
| Filter Productbereik | (Winkelcampagnes) Optioneel |
| DSA-domeinnaam | Vereist voor het maken van een campagne van het type a) &quot;DynamicSearchAds&quot; of b) &quot;Search&quot; wanneer het element ExperimentId niet is ingesteld) |
| DSA-domeintaal | Vereist voor het maken van een campagne van het type a) &quot;DynamicSearchAds&quot; of b) &quot;Search&quot; wanneer het element ExperimentId niet is ingesteld) |
| Sjabloon voor bijhouden | Optioneel |
| Achtervoegsel bestemmingspagina | <p>Optioneel |
| Begrotingstype | Vereist om een campagne te maken. |
| Apparaat | Optioneel |
| Bodaanpassing | Optioneel |
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
| Naam advertentiegroep | Vereist |
| Type advertentiegroep | Vereist om een advertentiegroep te maken. |
| Doelmethode publiek | Alleen vereist om publiek en groepen te maken. |
| Begindatum van groep toevoegen | Optioneel |
| Einddatum van groep toevoegen | Optioneel |
| Sjabloon voor bijhouden | Optioneel |
| Netwerkstatus zoeken | (Alleen campagnes op het zoeknetwerk) Optioneel |
| Talen | Optioneel |
| Apparaat | Optioneel |
| Bodaanpassing | Optioneel |
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
| Trefwoord | Vereist |
| Type afstemmen | Een waarde voor of het gelijke type of sleutelwoordidentiteitskaart wordt vereist om een sleutelwoord met veelvoudige gelijke types uit te geven of te schrappen. |
| Max CPC | Optioneel |
| Basis-URL/Definitieve URL | Optioneel |
| Aangepast URL-parameters | Optioneel |
| Sjabloon voor bijhouden | Optioneel |
| Param1 | Optioneel |
| Param2 | Optioneel |
| Trefwoordstatus | Alleen vereist om een trefwoord te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Restricties | Optioneel |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| Trefwoord-id | Vereist slechts wanneer u het sleutelwoord uitgeeft of schrapt, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) een &quot;identiteitskaart van AMO.&quot; |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Dynamisch zoeken en velden

>[!NOTE]
>
>Ondersteuning voor maken is niet beschikbaar.

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Creative (except RSA)]&quot; Rij in de [!UICONTROL Download Bulksheet] .

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist |
| Beschrijving regel 1-2 | Vereist om de beschrijving te bewerken. <b>Opmerking:</b> Als u voor dit advertentietype wijzigingen aanbrengt in de advertentie, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie. |
| Pad 1 weergeven | Vereist om het veld te bewerken. |
| Pad 2 weergeven | Vereist om het veld te bewerken. |
| Creatief type | Vereist om de status van een productadvertentie te maken of te bewerken. |
| Creatieve voorkeursapparaten | Optioneel |
| Advertentiestatus | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| ID advertentie | Deze optie is alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met ad-eigenschap bevat om de advertentie of b) een &quot;AMO-id&quot; te identificeren. Als u echter noch de ID van de advertentie, noch de AMO-id opneemt en de kolommen met de eigenschap advertentie komen overeen met meerdere advertenties, verandert de status voor slechts een van de advertenties. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Product (winkelen) en velden

Raadpleeg voor meer informatie over het maken van winkeladvertenties &quot;[Microsoft-reclamecampagnes implementeren](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/microsoft-shopping-campaigns.html).&quot;

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Creative (except RSA)]&quot; Rij in de [!UICONTROL Download Bulksheet] .

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist |
| Aanbiedingslijn | Optioneel |
| Basis-URL/Definitieve URL | Optioneel |
| Aangepast URL-parameters | Optioneel |
| Creatief type | Vereist om de status van een productadvertentie te maken of te bewerken. |
| Sjabloon voor bijhouden | Optioneel |
| Advertentiestatus | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Restricties | Optioneel |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| ID advertentie | Deze optie is alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met ad-eigenschap bevat om de advertentie of b) een &quot;AMO-id&quot; te identificeren. Als u echter noch de ID van de advertentie, noch de AMO-id opneemt en de kolommen met de eigenschap advertentie komen overeen met meerdere advertenties, verandert de status voor slechts een van de advertenties. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Responsief (multimedia) en velden

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Creative (except RSA)]&quot; Rij in de [!UICONTROL Download Bulksheet] .

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist |
| Advertentitel, advertentietak 2-15 | Voor responsieve advertenties zijn Advertentitel, Titel 2 en Titel 3 van Advertentie vereist om advertenties te maken. Alle andere velden voor de advertentie zijn optioneel. Als u de bestaande waarde voor een niet-vereist veld wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). <b>Opmerking:</b> Als u voor dit advertentietype wijzigingen aanbrengt in de advertentie, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie. |
| Beschrijving regel 1-4 | Beschrijvingsregel 1 en Beschrijving regel 2 zijn vereist om advertenties te maken en regel 3 en beschrijving 4 zijn optioneel. <b>Opmerking:</b> Als u voor dit advertentietype wijzigingen aanbrengt in de advertentie, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie. |
| Bedrijfsnaam | Vereist om een advertentie te maken of te verwijderen. |
| Oproep tot actie | Vereist om een advertentie te maken. |
| Oproep tot actie | Vereist om een advertentie te maken. |
| Basis-URL/Definitieve URL | Vereist om een advertentie te maken. |
| Creatief type | Optioneel. |
| Sjabloon voor bijhouden | Optioneel |
| Advertentiestatus | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
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
| Basis-URL/Definitieve URL | Vereist om een advertentie te maken. |
| Aangepast URL-parameters | Optioneel |
| Creatief type | Optioneel |
| Sjabloon voor bijhouden | Optioneel |
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
>Uitgebreide tekstadvertenties zijn afgekeurd. U kunt alleen bestaande tekstadvertenties verwijderen.

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist |
| Advertentietitel, en titel 2-3 | Alleen-lezen |
| Beschrijving regel 1-2 | Alleen-lezen |
| URL weergeven | Alleen-lezen |
| Pad 1 weergeven | Alleen-lezen |
| Pad 2 weergeven | Alleen-lezen |
| Basis-URL/Definitieve URL | Alleen-lezen |
| Aangepast URL-parameters | Alleen-lezen |
| Creatief type | Optioneel |
| Sjabloon voor bijhouden | Alleen-lezen |
| Creatieve voorkeursapparaten | Alleen-lezen |
| Advertentiestatus | Vereist |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| ID advertentie | Alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij een &quot;AMO-id&quot; bevat. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de advertentie-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Dynamische doelvelden (automatisch doel) voor zoeken

>[!NOTE]
>
>Ondersteuning voor maken is niet beschikbaar.

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist |
| Automatische doelexpressie | Vereist. |
| Type afstemmen | Optioneel |
| Max CPC | Optioneel |
| Aangepast URL-parameters | Optioneel |
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
| Type afstemmen | Vereist om een productgroep te maken. |
| Max CPC | Vereist om een productgroep te maken. |
| Bovenliggende productgroepen | Vereist |
| Productgroepering | Vereist |
| Type partitie | Vereist om een productgroep te maken. |
| Basis-URL/Definitieve URL | Vereist |
| Sjabloon voor bijhouden | Optioneel |
| Status van productgroep | Alleen vereist om een productgroep te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| Restricties | Optioneel |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel |
| Productgroep-id | Dit is alleen vereist wanneer u de productgroep wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de productgroep te identificeren of b) een &quot;AMO-id&quot;. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Sitemeelinktvelden op campagnereniveau

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Beschrijving regel 1 | Optioneel |
| Beschrijving regel 2 | Optioneel |
| Begindatum | Optioneel |
| Einddatum | Optioneel |
| Basis-URL/Definitieve URL | Vereist |
| Aangepast URL-parameters | Optioneel |
| Sjabloon voor bijhouden | Optioneel |
| Creatieve voorkeursapparaten | Optioneel |
| Koppelingsnaam | Vereist |
| Sitelink-status | Alleen vereist om een sitelink te verwijderen. |
| Campagne-id | Optioneel |
| Sitelink-id | Deze optie is alleen vereist wanneer u de sitelink wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de sitelink te identificeren of b) een &quot;AMO-id&quot;. Als u echter noch Sitelink-id, noch AMO-id opneemt en de eigenschappenkolommen overeenkomen met meerdere sitelinks, verandert de status voor slechts een van de sitelinks.<br><br><b>Opmerking:</b> Als u sitelink-eigenschapkolommen behalve Status voor een bestaande sitelink bewerkt en u niet de Sitelink-id of AMO-id opneemt, wordt een nieuwe sitelink gemaakt en wordt de bestaande sitelink niet gewijzigd. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Locatiedoelvelden

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Locatie | Vereist |
| Locatietype | Vereist om een doel te maken |
| Bodaanpassing | Optioneel |
| Locatiestatus | Alleen vereist om een locatiedoel te verwijderen. |
| Campagne-id | Optioneel |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de campagne-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Apparaatdoelvelden op campagnereniveau en op ad-groepniveau

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Apparaat | Vereist om een apparaatdoel te verwijderen. |
| Bodaanpassing | Optioneel |
| Naam advertentiegroep | Vereist voor apparaatdoelen op ad-groepsniveau. Niet van toepassing op apparaatdoelen op campagneniveau. |
| Doelstatus van apparaat | Alleen vereist om een apparaatdoel te verwijderen. |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel; alleen van toepassing op ad-group-apparaatdoelen. |
| AMO-id | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de apparaatdoel-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### De doelgebieden van RLSA van het campagne-niveau en van het ad groep

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| Naam van account | Vereist tenzij elke rij een &quot;AMO-id&quot; voor de entiteit bevat. |
| Campagnenaam | Vereist |
| Naam advertentiegroep | Vereist voor doelen op groepsniveau. Niet van toepassing op streefcijfers op campagneniveau. |
| Publiek | Vereist om een nieuw doel te creëren. |
| Doeltype | Optioneel |
| Bodaanpassing | Optioneel |
| RLSA-doelstatus | Vereist om een doel te schrappen. |
| Campagne-id | Optioneel |
| Groep-id toevoegen | Optioneel; alleen van toepassing op streefcijfers op ad-groepsniveau. |
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
