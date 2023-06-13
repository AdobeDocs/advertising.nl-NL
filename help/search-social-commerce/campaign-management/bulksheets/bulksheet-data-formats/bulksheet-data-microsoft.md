---
title: Vereiste gegevens voor het bulkwerkblad [!DNL Microsoft Advertising] rekeningen
description: Verwijs naar de vereiste kopbalgebieden en gegevensgebieden in bulksbladen voor [!DNL Microsoft Advertising] rekeningen.
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '6595'
ht-degree: 1%

---

# Aanhangsel - Vereiste gegevens voor het informatieblad voor [!DNL Microsoft Advertising] rekeningen

Om te creëren en bij te werken [!DNL Microsoft Advertising] Campagne gegevens in bulk, kunt u Onderzoek, Sociale, &amp; het bulksbladdossiers van de Handel gebruiken die specifiek voor worden geformatteerd [!DNL Microsoft Advertising] rekeningen. U kunt een van beide [bulkbladbestanden genereren voor bestaande accounts](../bulksheet-download.md) in de vereiste bestandsindeling of b) handmatig aanmaken (zie &quot;[Ondersteunde bestandsindelingen voor bulkbladbestanden](bulksheet-file-formats.md)&quot; voor algemene informatie over de ondersteunde bestandsindelingen).

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## Alle beschikbare gegevensvelden

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Veld | Beschrijving |
|----|----|
| [!UICONTROL Platform] | (Opgenomen in gegenereerde bulksbladen ter informatie) Het advertentieplatform. Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Acct Name] | De unieke naam die een advertentienetwerkaccount identificeert. Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | De unieke naam die een campagne voor een account identificeert. De maximumlengte is 128 tekens. |
| [!UICONTROL Campaign Budget] | Het dagelijkse of maandelijkse campagnebudget, met of zonder monetaire symbolen en leestekens. Het mag niet minder zijn dan 0,05. |
| [!UICONTROL Channel Type] | Het type kanaal dat de campagne als doel heeft: <i>[!UICONTROL Audience]</i>, <i>[!UICONTROL DynamicSearchAds]</i>, <i>[!UICONTROL Search]</i>, of <i>[!UICONTROL Shopping]</i>. |
| [!UICONTROL Delivery Method] | (Alleen campagnes met dagelijkse budgetten) Hoe snel u elke dag advertenties voor de campagne kunt weergeven:<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (de standaardinstelling voor nieuwe campagnes): Om uw advertenties over de dag te verspreiden.</li><li><i>[!UICONTROL Accelerated]:</i> Zo vaak mogelijk advertenties weergeven totdat uw budget is bereikt. Hierdoor worden uw advertenties mogelijk niet later op de dag weergegeven.</li></ul> |
| [!UICONTROL Campaign Priority] | (Alleen winkelcampagnes) De prioriteit waarmee de campagne wordt gebruikt wanneer meerdere campagnes hetzelfde product adverteren: <i>[!UICONTROL Low]</i> (standaard voor nieuwe campagnes), <i>[!UICONTROL Medium]</i>, of <i>[!UICONTROL High]</i>.<br><br>Wanneer hetzelfde product in meer dan één campagne is opgenomen, gebruikt het advertentienetwerk eerst de campagneprioriteit om te bepalen welke campagne (en het bijbehorende bod) in aanmerking komt voor de advertentieveiling. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel. |
| [!UICONTROL Merchant ID] | (Winkelcampagnes en publiekscampagnes die alleen zijn gekoppeld aan een commerciële feed) De klant-id van het zakelijke account waarvan de producten voor de campagne worden gebruikt. |
| [!UICONTROL Sales Country] | (Alleen koopcampagnes; alleen-lezen voor bestaande campagnes) Het land waar de campagneproducten worden verkocht. Omdat de producten met doellanden worden geassocieerd, bepaalt dit het plaatsen welke producten in de campagne worden geadverteerd. |
| [!UICONTROL Product Scope Filter] | (Campagnes die het winkelnetwerk slechts gebruiken) De producten in uw handelaarrekening waarvoor productadvertenties voor de campagne kunnen worden gecreeerd. U kunt maximaal zeven productafmetingen en kenmerkcombinaties ingaan waarop om uw producten te filtreren, gebruikend het formaat dimensi=attribute. Scheid meerdere filters met een scheidingsteken &quot;>>&quot;. Voor een lijst met beschikbare productafmetingen raadpleegt u &quot;[Productfilters voor winkelcampagne](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;<br><br> Voorbeeld: &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> Als u de bestaande waarden wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| [!UICONTROL DSA Domain Name] | (Campagnes van het type a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; of b) &quot;<i>[!UICONTROL Search]</i>&quot; wanneer de [!DNL ExperimentId] -element is niet ingesteld) De domeinnaam van de website die als doel moet dienen voor dynamische zoekopdrachten. De maximale lengte is 2.048 tekens. Als de domeinnaam `www`, het is afgesneden en niet gebruikt.<br><br>Voor bestaande campagnes, kunt u niet het domein uitgeven, maar u moet het omvatten om andere eigenschappen bij te werken. |
| [!UICONTROL DSA Domain Language] | (Campagnes van het type a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; of b) &quot;<i>[!UICONTROL Search]</i>&quot; wanneer de [!DNL ExperimentId] -element is niet ingesteld) De taal van de websitepagina&#39;s die moet worden gebruikt voor dynamische zoekopdrachten. De ondersteunde domeintalen zijn [!UICONTROL Dutch], [!UICONTROL English], [!UICONTROL French], [!UICONTROL German], [!UICONTROL Italian], [!UICONTROL Spanish], en [!UICONTROL Swedish].<br><br>Voor bestaande campagnes, kunt u niet de taal uitgeven, maar u moet het omvatten om andere eigenschappen bij te werken. |
| [!UICONTROL Ad Group Name] | De unieke naam die een advertentiegroep identificeert. De maximumlengte is 128 tekens. Navolgende lege tekens worden niet opgeslagen (zoals &#39;Groep 1 toevoegen&#39; wordt opgeslagen als &#39;Groep 1 toevoegen&#39;). |
| [!UICONTROL Ad Group Type] | (Campagnes op het onderzoeksnetwerk; alleen-lezen voor bestaande advertentiegroepen) Het type advertentiegroep: <i>[!UICONTROL Audience]</i> (alleen voor publiekscampagnes), <i>[!UICONTROL Search Dynamic]</i> (alleen voor dynamische zoekopdrachten) en <i>[!UICONTROL Search Standard]</i> (alleen voor responsieve zoekopdrachten en bestaande uitgevouwen tekstadvertenties). Sommige soorten campagnes kunnen veelvoudige advertentiegroep types omvatten. |
| [!UICONTROL Keyword] | (Campagnes op het onderzoeksnetwerk slechts) het sleutelwoordkoord. De maximumlengte is 50 tekens.<br><br><b>Opmerkingen:</b><ul><li>Als u een trefwoord op advertentiegroep- of campagnereniveau wilt uitsluiten, stelt u de optie [!UICONTROL Match Type] tot `Negative`. Als de rij de naam van de advertentiegroep bevat, wordt het trefwoord uitgesloten voor de advertentiegroep. Als de rij niet de naam van de advertentiegroep omvat, wordt het sleutelwoord uitgesloten voor de volledige campagne.</li><li>Een [!DNL Microsoft Advertising] trefwoord verwijdert het bestaande trefwoord en maakt een nieuw trefwoord met een nieuwe id. Als u het overeenkomsttype wijzigt, wordt het bestaande trefwoord echter niet verwijderd.</li></ul> |
| Plaatsing | Vervangen |
| [!UICONTROL Audience] | De lijst voor het opnieuw op de markt brengen van onderzoeksadvertenties (RLSA) doelpubliek voor de campagne of de ad groep. |
| [!UICONTROL Target Type] | (Alleen RLSA-doelen) Het doeltype: <i>[!UICONTROL Inclusion]</i> of <i>[!UICONTROL Exclusion]</i>. |
| [!UICONTROL Auto Target Expression] | Dynamische zoekdoelen voor de advertentiegroep. Gebruik voor alle doelen &quot;[!UICONTROL All Web Pages].&quot;<br><br>Als u maximaal drie dynamische zoekcriteria als doel wilt instellen, gebruikt u de indeling `<category>=<target>`, waarbij &lt;category> kan alle onderstaande rubrieken bevatten. Meerdere doelen samenvoegen voor een afzonderlijke categorie met &quot;`[blank space] and [blank space]`&quot; en voeg meerdere categorieën samen met &quot;`[blank space] and [blank space]`&quot;.<br><ul><li><i>Categorie:</i> Dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met een specifieke Google-inhoudscategorie.</li><li><i>URL:</i> Dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met een specifieke URL, waarbij de waarde overal in de URL kan worden opgenomen.</li><li><i>Paginatitel:</i> Dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met specifieke tekst in de paginatitel.</li><li><i>Pagina-inhoud:</i> Dynamische zoekopdrachten weergeven voor geïndexeerde pagina&#39;s met specifieke inhoud.</li></ul>Voorbeeld: url=schoenen.example.com en page title=schoenen<br>Voorbeeld: Alle webpagina&#39;s |
| [!UICONTROL Location] | Een geografische locatie waar advertenties voor de campagne of de ad-hocgroep moeten worden geplaatst; de waarden zijn niet hoofdlettergevoelig. Als u geen waarden voor de campagne of advertentiegroep invoert, worden alle locaties als doel ingesteld. Als u specifieke locaties als doel wilt instellen, voert u de locatie in met de [!DNL Microsoft Advertising] notaties voor locatiecode. Als u een locatielijst wilt downloaden, meldt u zich aan bij de [!DNL Microsoft Advertising] ontwikkelaarsportal met uw [!DNL Microsoft Advertising] referenties van reclameaccount. <b>Opmerking:</b> Als u een locatie wilt uitsluiten, plaatst u voor de locatiecode een minteken (`-`), zoals `-United States`. |
| [!UICONTROL Location Type] | Het type locatie, zoals Plaats, Land, MetroArea, PostalCode en Frame. Als u een locatielijst wilt downloaden, meldt u zich aan bij de [!DNL Microsoft Advertising] ontwikkelaarsportal met uw [!DNL Microsoft Advertising] referenties van reclameaccount. |
| [!UICONTROL Match Type] | (Alleen campagnes op het zoeknetwerk) De optie(s) voor trefwoordafstemming. Dit kan de optie voor trefwoordafstemming voor een dynamisch zoekdoel of een productgroep omvatten. Waarden zijn: <i>[!UICONTROL Broad]</i> (standaard voor nieuwe trefwoorden), <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Content]</i> (automatisch instellen voor trefwoorden wanneer de advertentiegroep het inhoudsnetwerk aanwijst), <i>[!UICONTROL Negative]</i> (om een trefwoord uit te sluiten op het netwerk van inhoud), <i>[!UICONTROL Dynamic Ad Target]</i> (standaard voor nieuwe dynamische zoekdoelen), <i>[!UICONTROL Product Group]</i> (standaard voor nieuwe productgroepen), of <i>[!UICONTROL Negative Product Group]</i> (om een productgroep uit te sluiten).  Een waarde voor of het gelijke type of sleutelwoordidentiteitskaart wordt vereist om een sleutelwoord met veelvoudige gelijke types uit te geven of te schrappen.<br><br>Kies voor Breedte overeenkomst aanpassen de optie &quot;Breed&quot; en voeg een `+` vóór elk woord binnen het vereiste trefwoord (zoals &quot;`+red +shoes`&quot; om zowel &quot;rood&quot; als &quot;schoenen&quot; te vereisen).<br><br>Het overeenkomentype voor een [!DNL Microsoft Advertising] Het bestaande trefwoord wordt niet verwijderd. |
| [!UICONTROL Max CPC] | (Campagnes op het onderzoeksnetwerk) De maximumkosten per klik (CPC), die het hoogste bedrag voor een advertentieklik is dat op het sleutelwoord, de productgroep, of het dynamische onderzoeksdoel wordt gebaseerd, met of zonder monetaire symbolen en punctuatie.  Voor bestaande trefwoorden en productgroepen zijn de records in geoptimaliseerde portfolio&#39;s slechts één dag geldig en worden de updates tijdens de volgende optimalisatiecyclus overschreven. <b>Opmerking:</b> Je kunt geen biedingen instellen voor negatieve trefwoorden. |
| [!UICONTROL Max Content CPC] | (Alleen-lezen voor CPC-campagnes die zijn gemaakt voordat het inhoudsnetwerk in 2017 is afgekeurd) De maximale kosten voor inhoud per klik (CPC). Dit is het hoogste bedrag dat wordt betaald voor een advertentie via een netwerksite voor weergave, met of zonder monetaire symbolen en interpunctie. |
| [!UICONTROL Audience Target Method] | (Publiek en groepen) Of:<ul><li><i>[!UICONTROL Target and Bid]:</i> Alleen advertenties weergeven voor gebruikers die zijn gekoppeld aan doelgroepen die ook voldoen aan andere doelen voor de advertentiegroep.</li><li><i>[!UICONTROL Bid Only]:</i>Advertenties tonen zelfs aan mensen die niet met doelpubliek worden geassocieerd zolang zij andere doelstellingen op groepsniveau voldoen.</li></ul> U kunt de kans echter vergroten dat advertenties bij een bepaald publiek worden getoond door voor dat publiek hogere biedingen in te stellen. |
| [!UICONTROL Parent Product Groupings] | De hiërarchie van bovenliggende productgroepen.<br><br>Voorbeeld: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | De productgroep (zoals &quot;brand=acme&quot; of &quot;Alle producten&quot;).<br><br><b>Opmerkingen:</b><ul><li>Wanneer een gespecificeerde productgroep niet in de hiërarchie van de Groepen van het Product van de Ouder bestaat, leidt het Onderzoek, Sociale, &amp; Handel tot om het even welke delen van de hiërarchie die nodig zijn.</li><li>Met Zoeken, Sociaal, en Handel wordt automatisch een &quot;[!UICONTROL All Products]&quot; groeperen wanneer u een advertentiegroep maakt in een winkelcampagne met een standaardbod ingesteld op het standaardbod van de advertentiegroep. Met Zoeken, Sociaal, en Handel wordt automatisch een &quot;[!UICONTROL Everything Else]&quot; groeperen met het standaardbod van de advertentiegroep op elk niveau van de hiërarchie van de productgroepen. U kunt deze standaardgroepen nog steeds expliciet maken en ze uitsluiten of hun biedingen wijzigen.</li><li>Elke advertentiegroep kan maximaal acht lagen productgroepen bevatten, waaronder &quot;[!UICONTROL All Products]&quot; en zeven andere lagen.</li></ul> |
| [!UICONTROL Partition Type] | Het partitietype voor de productgroep: <i>[!UICONTROL subdivision]</i> (als het onderliggende productgroepen heeft) of <i>[!UICONTROL unit]</i> (als het geen onderliggende productgroepen heeft). |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | (Alleen uitgevouwen tekstadvertenties, multimediadaden, responsieve advertenties en responsieve zoekadvertenties) De kopregels van een advertentie. De maximumlengte voor elk veld van de advertentie is 30 tekens of 15 double-byte tekens, inclusief alle dynamische tekst (zoals de waarden van trefwoorden). `{Param2}` en `{Param3}` dynamische substitutievariabelen en adverteerders).<br><br> Voor responsieve zoekadvertenties voegt u een advertentieklanker in in de volgende indeling, waarbij &#39;Standaardtekst&#39; een optionele waarde is die moet worden ingevoegd wanneer het invoerbestand geen geldige waarde bevat: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Voor uitgebreide tekstadvertenties zijn Titel toevoegen en Titel 2 toevoegen vereist, en [!UICONTROL Ad Title 3] is optioneel. [!DNL Microsoft Advertising] vervangen uitgebreide tekstadvertenties in augustus 2022, en u kunt nu alleen rapporteren over en deze verwijderen.<br><br>Voor multimediadaden, responsieve advertenties en responsieve zoekopdrachten, [!UICONTROL Ad Title], [!UICONTROL Ad Title 2], en [!UICONTROL Ad Title 3] zijn vereist en alle andere titelvelden zijn optioneel.<br><br>Als u de bestaande waarde voor een niet-vereist veld wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes).<br><br>Voor alle advertentietypen, behalve voor uitgevouwen tekstadvertenties, verwijdert het wijzigen van de advertentiekopie de bestaande advertentie en maakt een nieuwe advertentie met dezelfde eigenschappen. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | (Alleen responsieve zoekopdrachten; (optioneel) Een positie waarop de corresponderende advertentitel moet worden vastgezet: `[null]` (geen waarde waardoor de titel van de advertentie voor alle posities in aanmerking komt), 1, 2 of 3. Als [!UICONTROL Ad Title Position] heeft een waarde van 1, dan [!UICONTROL Ad Title] alleen op positie 1 worden weergegeven. Standaard zijn alle advertentitels null (geen waarden). Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes).<br><br><b>Opmerking:</b> U kunt meerdere advertentitels vastzetten op dezelfde positie. In het advertentienetwerk wordt een van de advertentietitels gebruikt die op de positie zijn vastgezet. Titels die op positie 3 zijn vastgezet, worden mogelijk niet met de advertentie weergegeven. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | (Tekstadvertenties, dynamische zoekadvertenties, multimedia-advertenties, responsieve zoekadvertenties en alleen verbeterde sitelinks op campageniveau) De hoofdtekst van een advertentie of sitelink.<br><br>Voor sitelinks kunt u optioneel beide gebruiken [!UICONTROL Description Line 1] en [!UICONTROL Description Line 2] om extra tekst op te nemen die het advertentienetwerk onder de koppelingstekst kan tonen. Elk beschrijvingsveld kan maximaal 35 single-byte of 17 double-byte tekens bevatten.<br><br>Voor advertenties is de maximale lengte voor elk beschrijvingsveld 90 tekens of 45 double-byte tekens, inclusief alle dynamische tekst (zoals de waarden van trefwoorden en adverteerders).<br><br>Voor responsieve zoekadvertenties voegt u een advertentieklanker in in de volgende indeling, waarbij Standaardtekst een optionele waarde is die moet worden ingevoegd wanneer uw feed-bestand geen geldige waarde bevat: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>Voor tekstadvertenties en dynamische zoekadvertenties is Beschrijving regel 1 vereist en [!UICONTROL Description Line 2] is optioneel.<br><br>Voor multimediadaden, responsieve advertenties en responsieve zoekopdrachten, [!UICONTROL Description Line 1] en [!UICONTROL Description Line 2] verplicht zijn, en [!UICONTROL Description Line 3] en [!UICONTROL Description Line 4] zijn optioneel.<br><br>Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes).<br><br><b>Opmerkingen:</b><ul><li>(Standaardtekstadvertenties) De gecombineerde titel en tekst moeten ten minste drie woorden lang zijn.</li><li>(Uitgebreide tekstadvertenties) Dit veld kan optioneel de opdracht {Param2} en {Param3} dynamische vervangingsvariabelen. In dat geval is de maximale lengte van de advertentietekst 300 single-byte of 150 double-byte tekens. [!DNL Microsoft Advertising] vervangen uitgebreide tekstadvertenties in augustus 2022, en u kunt nu alleen rapporteren over en deze verwijderen.</li><li>(Dynamische zoekopdrachten) Dynamische vervangingstekst is niet toegestaan.</li><li>Voor alle advertentietypen, behalve uitgevouwen tekstadvertenties, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie.</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Alleen responsieve zoekopdrachten; (optioneel) Een positie waarop de desbetreffende beschrijving moet worden vastgezet: `[null]` (geen waarde waardoor de beschrijving voor alle posities in aanmerking komt), 1, 2 of 3. Als [!UICONTROL Description 1 Position] heeft een waarde van 1, dan zal Beschrijving 1 slechts in Positie 1 verschijnen. Standaard zijn geen beschrijvingen vastgezet op een positie.<br><br>Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes).<br><br><b>Opmerking:</b> U kunt meerdere beschrijvingen vastzetten op dezelfde positie. Het advertentienetwerk zal één van de beschrijvingen gebruiken die aan de positie worden vastgezet. Beschrijvingen die op positie 2 zijn vastgezet, mogen niet met de advertentie worden getoond. |
| [!UICONTROL Business Name] | (Alleen multimediaadvertenties) De bedrijfsnaam, met maximaal 25 tekens. |
| [!UICONTROL Promotion Line] | (Alleen aanbiedingen voor producten) Een unieke promotielijn die in de zoekresultaten bij de aanbieding van het product moet worden gevoegd (zoals Nu gratis verzending). De maximumlengte is 45 tekens.<br><br>De promotielijn kan op verschillende plaatsen ten opzichte van de advertentie (zoals onder de advertentie) verschijnen, afhankelijk van waar de advertentie op de pagina wordt weergegeven. |
| [!UICONTROL Display URL] | De URL die is opgenomen in de advertentie.<br><br>Voor uitgebreide dynamische zoekopdrachten genereert het advertentienetwerk deze waarde dynamisch vanuit het websitedomein en hoeft u geen waarde in te voeren.<br><br>Voor uitgevouwen tekstadvertenties en responsieve zoekopdrachten hoeft u geen waarde in te voeren. De weergave-URL wordt automatisch opgehaald uit het domein in de uiteindelijke URL. U kunt de URL desgewenst aanpassen met de velden Pad 1 en Pad 2.<br><br><b>Opmerkingen:</b><ul><li>(Accounts met definitieve URL&#39;s) De domeinnamen in de weergave-URL en de uiteindelijke URL moeten overeenkomen.</li><li>[!DNL Microsoft Advertising] vervangen uitgebreide tekstadvertenties in augustus 2022, en u kunt nu alleen rapporteren over en deze verwijderen.</li></ul> |
| [!UICONTROL Display Path 1] | (Alleen uitgevouwen tekstadvertenties, dynamische zoekadvertenties en responsieve zoekadvertenties) Tekst die aan de weergave-URL is toegevoegd en die automatisch uit de uiteindelijke URL wordt geëxtraheerd. Elk pad wordt voorafgegaan door een slash (/) in de URL. Een pad mag geen forward slash (/) of newline (\n) tekens bevatten. De maximumlengte voor elk pad is 15 tekens of 7 double-byte tekens.<br><br>Als u een advertentieklanter wilt invoegen, gebruikt u de volgende indelingen, waarbij &#39;Standaardtekst&#39; een optionele waarde is die moet worden ingevoegd wanneer uw feed-bestand geen geldige waarde bevat: `{CUSTOMIZER.Attribute name:Default text}`, zoals `{CUSTOMIZER.Discount:10%}`<br><br>Als [!UICONTROL Display Path 1] is &quot;deals&quot;, wordt de URL van de weergave &lt;display url=&quot;&quot;>/deals, zoals www.example.com/deals.<br><br>[!DNL Microsoft Advertising] vervangen uitgebreide tekstadvertenties in augustus 2022, en u kunt nu alleen rapporteren over en deze verwijderen. |
| [!UICONTROL Display Path 1] | (Alleen uitgebreide tekstadvertenties, dynamische zoekadvertenties en responsieve zoekopdrachten) Een extra weergavepad. zie de vermelding voor [!UICONTROL Display Path 1].<br><br>Voorbeeld: Indien [!UICONTROL Display Path 1] is &quot;deals&quot; en [!UICONTROL Display Path 2] is &quot;lokaal&quot;, dan is de weergave-URL &lt;<i>URL weergeven</i>>/deals/local, zoals www.example.com/deals/local. |
| [!UICONTROL Start Date] | (Alleen verbeterde sitelinks) De eerste datum waarop biedingen mogen worden uitgebracht voor de sitelink, in de tijdzone van de adverteerder en in een van de volgende formaten: d/m/yyyy, m/d/jj, m-d-jjjj of m-d-jj. De standaard voor nieuwe verbeterde sitelinks is de huidige dag. <b>Opmerking:</b> Nieuwe verbeterde sitelinks kunnen alleen worden gemaakt in campagnes met bestaande verbeterde sitelinks of zonder sitelinks. |
| [!UICONTROL End Date] | De laatste datum waarop de sitelink met advertenties kan worden weergegeven in de tijdzone van de adverteerder en in een van de volgende notaties: d/m/yyyy, m/d/jj, m-d-jjjj of m-d-jj. Voor een nieuwe sitelink is de standaardwaarde `[blank]` (dus geen einddatum). |
| [!UICONTROL Call To Action] | De oproep tot actie om op te nemen in de advertentie. Zie de [API-referentie voor een lijst met mogelijke waarden](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction), maar voer aanroepen van meerdere woorden naar handeling in als meerdere woorden (zoals &quot;Nu ophalen&quot; in plaats van &quot;Nu ophalen&quot;) in bulksbladen. |
| [!UICONTROL Call To Action Language] | De taal voor de vraag aan actieopties. Zie de [API-referentie voor een lijst met mogelijke talen](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| [!UICONTROL Base URL/Final URL] | De bestemmingspagina URL waarnaar de gebruikers van de onderzoeksmotor worden genomen wanneer zij uw advertentie klikken, met inbegrip van om het even welke toevoegingsparameters die voor de campagne of de rekening worden gevormd. Basis/definitieve URLs op het sleutelwoordniveau treedt die op het advertentieniveau en hoger met voeten.<br><br>Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| [!UICONTROL Destination URL] | (Ter informatie opgenomen in gegenereerde bulksbladen; (niet gepost aan de zoekmachine) Voor accounts met doel-URL&#39;s is dit de URL die een advertentie koppelt aan een basis-URL/bestemmingspagina op de website van de adverteerder (soms via een andere site die de klik bijhoudt en de gebruiker vervolgens doorstuurt naar de bestemmingspagina). Het omvat om het even welke toevoegingsparameters die voor de Onderzoek, Sociale, &amp; de campagne of de rekening van de Handel worden gevormd. Als u URL&#39;s voor bijhouden hebt gegenereerd, is dit gebaseerd op de volgende parameters in uw accountinstellingen en campagnemontages. Als u specifieke parameters voor zoekprogramma&#39;s hebt toegevoegd, kunnen deze worden vervangen door de equivalente parameters voor Zoeken, Sociale &amp; Handel.<br><br>Voor accounts met uiteindelijke URL&#39;s geeft deze kolom dezelfde waarde weer als de kolom Basis-URL/Definitieve URL. |
| [!UICONTROL Custom URL Param] | Gegevens ter vervanging van de `{custom_code}` dynamische variabele wanneer de variabele is opgenomen in de volgende parameters voor de instellingen van de zoekaccount of campagne. Als u de aangepaste waarde in de URL voor bijhouden wilt invoegen, moet u het bestand met de opsommingstekens uploaden met de optie URL&#39;s voor bijhouden genereren. |
| [!UICONTROL Creative Type] | De advertentievorm: <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i> (winkeladvertenties), of <i>[!UICONTROL Responsive Search Ad]</i>, of <i>[!UICONTROL Text ad]</i>. De standaardinstelling voor nieuwe advertenties is <i>[!UICONTROL Text ad]</i>. |
| [!UICONTROL Ad Group Start Date] | De eerste datum waarop biedingen voor de advertentiegroep mogen worden geplaatst, in de tijdzone van de adverteerder en in een van de volgende formaten: d/m/yyyy, m/d/jj, m-d-jjjj of m-d-jj. Voor een nieuwe advertentiegroep is de standaardwaarde de huidige datum. |
| [!UICONTROL Ad Group End Date] | De laatste datum waarop biedingen voor de advertentiegroep mogen worden geplaatst, in de tijdzone van de adverteerder en in een van de volgende formaten: d/m/yyyy, m/d/jj, m-d-jjjj of m-d-jj. Voor een nieuwe advertentiegroep is de standaardwaarde [blank] (dus geen einddatum). |
| [!UICONTROL Tracking Template] | (Optioneel) De sjabloon voor reeksspatiëring, die alle parameters voor het omleiden en bijhouden van domeinen opgeeft en de laatste URL in een parameter insluit. De het volgen malplaatje op het meest korrelige niveau (met sleutelwoord als meest korrelig) treedt de waarden op alle hogere niveaus met voeten.<br><br>Voor het bijhouden van reclame-conversies voor Adobe, die wordt toegepast wanneer de instellingen voor de campagne &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel voegt automatisch omleiding en volgende code toe wanneer u sparen het verslag.<br><br>Voer een waarde in voor omleidingen en bijhouden door derden.<br><br>Voor een lijst met parameters die uiteindelijke URL&#39;s aangeven in trackingsjablonen raadpleegt u de [!DNL Microsoft Advertising] documentatie.<br><br> Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| [!UICONTROL Landing Page Suffix] | Alle parameters die aan het einde van de uiteindelijke URL&#39;s moeten worden toegevoegd om informatie bij te houden. Voorbeeld: `param2=value1&param3=value2`<br><br>Zie &quot;[Opmaak voor het bijhouden van klikken voor [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).&quot;<br><br>De laatste URL-achtervoegsels op lagere niveaus overschrijven het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Om een achtervoegsel op het niveau van de ad groep of lager te vormen, gebruik [!DNL Microsoft Advertising] editor. |
| Netwerkstatus zoeken | Of u advertenties voor de advertentiegroep op verschillende elementen van het Zoeknetwerk wilt plaatsen:<ul><li><i>Alle:</i> Om advertenties op alle Bing onderzoeksnetwerken en syndicated onderzoekspartners te plaatsen.</li><li><i>OwnedAndOperatedOnly:</i>Als u alleen advertenties op Bing en Yahoo wilt plaatsen! websites.</li><li><i>SyndicatedSearchOnly:</i> Als u alleen advertenties op Bing en Yahoo wilt plaatsen! gesynchroniseerde zoekpartners.</li><li><i>Uit:</i> Om advertenties op het Netwerk van de Inhoud slechts (niet het Netwerk van het Onderzoek) te plaatsen.</li></ul> Voor nieuwe advertentiegroepen is de standaardwaarde Aan. |
| [!UICONTROL Content Network Status] | Vervangen |
| [!UICONTROL Languages] | De doeltaal voor advertenties in de advertentiegroep: [!UICONTROL English], [!UICONTROL French], [!UICONTROL Finnish], [!UICONTROL German], [!UICONTROL Norwegian], [!UICONTROL Spanish], of [!UICONTROL Swedish]. De standaardinstelling voor nieuwe campagnes is [!UICONTROL English].<br><br>Deze instelling bepaalt in welke landen en regio&#39;s uw advertentie kan worden weergegeven. Zorg ervoor dat u een taal kiest die compatibel is met de locatiedoelen van de campagne. |
| [!UICONTROL Budget Type] | Of de begroting <i>[!UICONTROL Daily]</i> (de standaardwaarde) of <i>[!UICONTROL Monthly]</i>.<br><br>Opmerking: Als u de campagne toewijst aan een geoptimaliseerde portfolio, wordt deze waarde automatisch ingesteld op [!UICONTROL Daily]. |
| [!UICONTROL Device] | Een apparaattype waarvoor biedaanpassingen worden uitgevoerd op campagne- of advertentieniveau: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i>, of <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | De bodaanpassing voor een opgegeven doeltype. Als het bod op het trefwoordniveau bijvoorbeeld 1 USD is en het bod voor smartphones 50% is, is het bod op de smartphone 1,50 USD. Standaard worden alle doelen geboden bij het bod op trefwoordniveau. Geldige percentages zijn:<ul><li>Smartphones en tablets: -100 (om niet te bieden op het apparaattype) en van -90 tot 900</li><li>Desktop: van 0 tot en met 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | De apparaattypen waarop u de advertentie of sitelink wilt weergeven: <i>[!UICONTROL All]</i> (de standaardwaarde) of <i>[!UICONTROL Mobile]</i>. Wanneer Mobiel is opgegeven, probeert het netwerk de advertentie of sitelink aan gebruikers van mobiele apparaten weer te geven in plaats van aan gebruikers van desktopcomputers of tablets. Anders, zal het netwerk de advertentie of sitelink op om het even welk apparatentype tonen. <b>Opmerking:</b> Het netwerk garandeert niet dat de advertentie op het voorkeurstype wordt weergegeven. |
| [!UICONTROL Param2] | De tekenreeks die als vervangende waarde moet worden gebruikt als de basis-URL van het trefwoord of de titel, beschrijving of basis-URL van de advertentie de volgende code bevat: `{Param2}` dynamische substitutiereeks. De maximumlengte is 70 tekens, maar houd rekening met de maximumlengte van het advertentie-element waarin u het element wilt gebruiken (de combinatie van Titel 1 en Titel 2 kan bijvoorbeeld maximaal 76 tekens bevatten). Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| [!UICONTROL Param3] | De tekenreeks die als vervangende waarde moet worden gebruikt als de basis-URL van het trefwoord of de titel, beschrijving of basis-URL van de advertentie de volgende code bevat: `{Param3}` dynamische substitutiereeks. De maximumlengte is 70 tekens, maar houd rekening met de maximumlengte van het advertentie-element waarin u het element wilt gebruiken (de combinatie van Titel 1 en Titel 2 kan bijvoorbeeld maximaal 76 tekens bevatten). Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| [!UICONTROL Link Name] | De sitelink-tekst. Het moet uniek zijn in de campagne. Als u Description1 en Description2 specificeert, dan kan de sitelink tekst tot 25 single-byte of 12 dubbel-byte karakters omvatten; anders kan de sitelink-tekst maximaal 35 single-byte of 17 double-byte tekens bevatten.<br><br>[!DNL Microsoft Advertising] U kunt twee, vier of zes verbeterde sitelinks met beschrijvingen weergeven, of vier of zes sitelinks in één rij zonder beschrijvingen, met een advertentie.<br><br>U kunt nieuwe verbeterde sitelinks alleen maken in campagnes met bestaande verbeterde sitelinks of zonder sitelinks. |
| [!UICONTROL Campaign Status] | De weergavestatus van de campagne: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, of <i>[!UICONTROL Deleted]</i> (alleen bestaande campagnes). De standaardinstelling voor nieuwe campagnes is [!UICONTROL Active]. Als u een actieve of gepauzeerde campagne wilt verwijderen, voert u de waarde in `Deleted`. |
| [!UICONTROL Ad Group Status] | De weergavestatus van de advertentiegroep: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, of <i>[!UICONTROL Deleted]</i> (alleen bestaande advertentiegroepen). De standaardinstelling voor nieuwe advertentiegroepen is [!UICONTROL Active]. Als u een actieve of gepauzeerde ad-groep wilt verwijderen, voert u de waarde in `Deleted`. |
| [!UICONTROL Keyword Status] | De weergavestatus van het trefwoord: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, of <i>[!UICONTROL Deleted]</i> (alleen bestaande trefwoorden). De standaardwaarde voor nieuwe trefwoorden is [!UICONTROL Active]. Als u een actief of gepauzeerd trefwoord wilt verwijderen, voert u de waarde in `Deleted`. <b>Opmerking:</b> Als u URL&#39;s bijhouden maakt voor een trefwoord met meerdere typen overeenkomsten, moet de status van het trefwoord voor elk type overeenkomst gelijk zijn. |
| [!UICONTROL Placement Status] | Vervangen |
| [!UICONTROL Ad Status] | De weergavestatus van de advertentie: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (alleen bestaande advertenties), <i>[!UICONTROL Disapproved]</i> (niet bewerkbaar), of <i>[!UICONTROL Paused]</i>. De standaardinstelling voor nieuwe advertenties is [!UICONTROL Active]. Als u een actieve of gepauzeerde advertentie wilt verwijderen, voert u de waarde in `Deleted`. |
| [!UICONTROL Target Status] | De status van een dynamisch zoekdoel: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, of <i>[!UICONTROL Deleted]</i> (alleen bestaande streefcijfers). De standaardinstelling voor nieuwe doelen is [!UICONTROL Active]. Als u een actief of gepauzeerd doel wilt verwijderen, voert u de waarde in `Deleted`. |
| [!UICONTROL Sitelink Status] | De weergavestatus van de sitelink: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande sitelinks). De standaardinstelling voor nieuwe sitelinks is [!UICONTROL Active]. Als u een actieve sitelink wilt verwijderen, voert u de waarde in `Deleted`. |
| [!UICONTROL Location Status] | De status van het locatiedoel: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande locaties). De standaardinstelling voor nieuwe locaties is [!UICONTROL Active]. Als u een actieve locatie wilt verwijderen, voert u de waarde in `Deleted`. |
| [!UICONTROL Product Group Status] | De weergavestatus van de productgroep: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande productgroepen). De standaardwaarde voor nieuwe productgroepen is [!UICONTROL Active]. Als u een actieve productgroep wilt verwijderen, voert u de waarde in `Deleted`. |
| [!UICONTROL Device Target Status] | De status van het apparaatdoel op campagne- of advertentieniveau: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i>. Voor nieuwe campagnes en advertentiegroepen is de standaardwaarde [!UICONTROL Active]. |
| [!UICONTROL RLSA Target Status] | De status van de RLSA-doelstelling op campagne- of advertentieniveau of (alleen Google Ads)-uitsluiting: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande streefcijfers). De standaardinstelling voor nieuwe doelen of uitsluitingen is [!UICONTROL Active]. Als u een actief doel of een actieve uitsluiting wilt verwijderen, voert u de waarde in `Deleted`. |
| \[Advertiserspecifieke labelclassificatie\] | (Benoemd voor een advertentiespecifieke labelclassificatie, zoals &quot;Kleur&quot; voor een labelclassificatie genaamd Kleur) Een waarde voor de opgegeven classificatie die aan de entiteit is gekoppeld. U kunt per entiteit slechts één waarde per classificatie opnemen (zoals &quot;rood&quot; voor de labelclassificatie &quot;Kleur&quot; voor campagne A). De maximumlengte is 100 tekens en de waarde kan ASCII- en niet-ASCII-tekens bevatten.<br><br>De classificaties van het etiket en hun etiketwaarden worden toegepast op alle kindcomponenten; nieuwe componenten die later worden toegevoegd, worden automatisch aan het label gekoppeld. De etiketclassificaties voor productgroepen worden toegepast op het eenheidniveau (het meest korrelige).<br><br>Noch de classificatienaam noch de classificatiewaarde is hoofdlettergevoelig. |
| [!UICONTROL Constraints] | Een beperking die aan de entiteit is toegewezen. U kunt slechts één beperking per entiteit toewijzen.<br><b>>Restricties worden overgeërfd door onderliggende entiteiten, zodat u geen waarden voor onderliggende entiteiten hoeft in te voeren, tenzij u de overgeërfde waarden wilt overschrijven. |
| [!UICONTROL Campaign ID] | De unieke id die een bestaande campagne identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Alleen vereist wanneer u de naam van de campagne wijzigt, tenzij de rij de waarde &quot;[!UICONTROL AMO ID]&quot; voor de campagne . |
| [!UICONTROL Ad Group ID] | De unieke id die een bestaande advertentiegroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Alleen vereist wanneer u de naam van de campagne wijzigt, tenzij de rij de waarde &quot;[!UICONTROL AMO ID]&quot; voor de advertentiegroep. |
| [!UICONTROL Placement ID] | Vervangen |
| [!UICONTROL Keyword ID] | De unieke id die een bestaand trefwoord identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Vereist slechts wanneer u het sleutelwoord verandert, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>De unieke id die een bestaande advertentie identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Voor responsieve zoekopdrachten is de ID van de advertentie of de AMO-id vereist om advertentiegegevens te bewerken of te verwijderen. Voor alle andere entiteitstypen is de AMO-id alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met eigenschappen bevat om de advertentie of b) en &quot;[!UICONTROL AMO ID]&quot;.&quot; Als u echter geen van de [!UICONTROL Ad ID] noch [!UICONTROL AMO ID]en de kolommen met de eigenschap ad-eigenschap komen overeen met meerdere advertenties, verandert de status voor slechts een van de advertenties.</p><p><b>Opmerking:</b> Als u a) en bezitskolommen behalve Status voor een bestaande advertentie uitgeeft, of b) om het even welke gegevens voor een ontvankelijke onderzoeksadvertentie, en u omvat noch [!UICONTROL Ad ID] noch [!UICONTROL AMO ID], wordt er een nieuwe advertentie gemaakt en de bestaande advertentie wordt niet gewijzigd. </p> |
| [!UICONTROL Sitelink ID] | De unieke id die een bestaande sitelink identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Dit is alleen vereist wanneer u de sitelink wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de sitelink te identificeren of b) en &quot;[!UICONTROL AMO ID]&quot;.&quot; Als u echter geen van beide opties opneemt [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID]en de eigenschapskolommen overeenkomen met meerdere sitelinks, verandert de status voor slechts een van de sitelinks.</p><p><b>Opmerking:</b> Als u eigenschapkolommen sitelink bewerkt, behalve Status voor een bestaande sitelink, en u geen van beide kolommen [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID], wordt er een nieuwe sitelink gemaakt en de bestaande sitelink wordt niet gewijzigd. |
| [!UICONTROL Product Group ID] | De unieke id die een bestaande productgroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Dit is alleen vereist wanneer u de productgroep wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de productgroep te identificeren of b) en &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| Locatie-id | De unieke [!DNL Microsoft Advertising] id voor het locatiedoel. Als u een locatielijst wilt downloaden, meldt u zich aan bij de [!DNL Microsoft Advertising] ontwikkelaarsportal met uw [!DNL Microsoft Advertising] referenties van reclameaccount. Deze optie is alleen vereist wanneer u het doel van de locatie wijzigt of verwijdert, tenzij de rij een &quot;[!UICONTROL AMO ID]&quot; voor het doel. |
| [!UICONTROL Target ID] | De unieke id die een bestaand automatisch doel identificeert. Alleen vereist wanneer u het automatische doel wijzigt of verwijdert, tenzij de rij een &quot;[!UICONTROL AMO ID]&quot; voor het doel. |
| [!UICONTROL RLSA Target ID] | De unieke id die een bestaand RLSA-doel op campagne- of advertentieniveau identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u het doel of de uitsluiting wijzigt of verwijdert, tenzij de rij een &quot;[!UICONTROL AMO ID]&quot; voor het doel. |
| [!UICONTROL AMO ID] | (In gegenereerde bulksbladen) Een unieke id die door Adobe wordt gegenereerd voor een gesynchroniseerde entiteit. Voor responsieve zoekopdrachten is de AMO-id vereist om advertenties te bewerken of te verwijderen, tenzij u de advertentie-id opneemt. Als u gegevens voor alle andere entiteitstypen met een AMO-id wilt bewerken, moet de AMO-id de gegevens bewerken of verwijderen, tenzij u de id van de entiteit en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |
| [!UICONTROL EF Error Message] | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van het advertentienetwerk betreffende gegevens in de rij; foutberichten worden opgenomen in [!UICONTROL EF Errors] bestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| [!UICONTROL SE Error Message] | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van het advertentienetwerk betreffende gegevens in de rij; foutberichten worden opgenomen in [!UICONTROL SE Errors] bestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| [!UICONTROL Exemption Request] | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van de namen en tekst van het advertentiebeleid van Google dat een advertentie schendt. |
| [!UICONTROL Retail Hash] | (Ter informatie opgenomen in bulksbladen die zijn gegenereerd met Advanced Campaign Management) Een alfanumerieke hash-code (zoals f9639f40cdf56524b541e5dacf55a991) die aangeeft dat het item is gegenereerd met de weergave Geavanceerd (ACM). |

<table style="table-layout:auto">

[^1]: [!DNL Excel] grote getallen worden omgezet in wetenschappelijke notaties (zoals 2.12E+09 voor 2115585666) wanneer het bestand wordt geopend. Als u cijfers in de standaardnotatie wilt weergeven, selecteert u een willekeurige cel in de kolom en klikt u in de formulebalk.

## Velden vereist voor het maken, bewerken of verwijderen van elk accountonderdeel

### Campagnevelden

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist | De unieke naam die een campagne voor een account identificeert. |
| [!UICONTROL Campaign Budget] | Vereist om een campagne te maken. | Een dagelijkse uitgavenlimiet voor de campagne, met of zonder monetaire symbolen en leestekens. Deze waarde overschrijft, maar kan het budget van de account niet overschrijden. |
| [!UICONTROL Channel Type] | Vereist om een campagne te maken. |
| [!UICONTROL Delivery Method] | Optioneel |
| [!UICONTROL Campaign Priority] | Vereist om een winkelcampagne te maken. |
| [!UICONTROL Merchant ID] | Vereist om een winkelcampagne te maken. |
| [!UICONTROL Sales Country] | Vereist om een winkelcampagne te maken. |
| [!UICONTROL Product Scope Filter] | (Winkelcampagnes) Optioneel |
| [!UICONTROL DSA Domain Name] | Vereist voor het maken van een campagne van het type a) &quot;[!UICONTROL DynamicSearchAds]&quot; of b) &quot;[!UICONTROL Search]&quot; wanneer de [!DNL ExperimentId] element niet ingesteld) |
| [!UICONTROL DSA Domain Language] | Vereist voor het maken van een campagne van het type a) &quot;[!UICONTROL DynamicSearchAds]&quot; of b) &quot;[!UICONTROL Search]&quot; wanneer de [!DNL ExperimentId] element niet ingesteld) |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Landing Page Suffix] | <p>Optioneel |
| [!UICONTROL Budget Type] | Vereist om een campagne te maken. |
| [!UICONTROL Device] | Optioneel |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL Campaign Status] | Alleen vereist om een campagne te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Campaign ID] | Alleen vereist wanneer u de naam van de campagne wijzigt, tenzij de rij de waarde &quot;[!UICONTROL AMO ID]&quot; voor de campagne . |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Groepsvelden toevoegen

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Ad Group Type] | Vereist om een advertentiegroep te maken. |
| [!UICONTROL Audience Target Method] | Alleen vereist om publiek en groepen te maken. |
| [!UICONTROL Ad Group Start Date] | Optioneel |
| [!UICONTROL Ad Group End Date] | Optioneel |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Search Network Status] | (Alleen campagnes op het zoeknetwerk) Optioneel |
| [!UICONTROL Languages] | Optioneel |
| [!UICONTROL Device] | Optioneel |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL Ad Group Status] | Alleen vereist om een advertentiegroep te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Ad Group ID] | Alleen vereist wanneer u de naam van de advertentiegroep wijzigt, tenzij de rij een &quot;[!UICONTROL AMO ID]&quot; voor de advertentiegroep. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Trefwoordvelden

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Keyword] | Vereist |
| [!UICONTROL Match Type] | Een waarde voor of het gelijke type of sleutelwoordidentiteitskaart wordt vereist om een sleutelwoord met veelvoudige gelijke types uit te geven of te schrappen. |
| [!UICONTROL Max CPC] | Optioneel |
| [!UICONTROL Base URL/Final URL] | Optioneel |
| [!UICONTROL Custom URL Param] | Optioneel |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Param1] | Optioneel |
| [!UICONTROL Param2] | Optioneel |
| [!UICONTROL Keyword Status] | Alleen vereist om een trefwoord te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Keyword ID] | Vereist slechts wanneer u het sleutelwoord uitgeeft of schrapt, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Dynamisch zoeken en velden

>[!NOTE]
>
>Ondersteuning voor maken is niet beschikbaar.

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Creative (except RSA)]&quot; Rij in de [!UICONTROL Download Bulksheet] .

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Vereist om de beschrijving te bewerken. <b>Opmerking:</b> Als u voor dit advertentietype wijzigingen aanbrengt in de advertentie, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie. |
| [!UICONTROL Display Path 1] | Vereist om het veld te bewerken. |
| [!UICONTROL Display Path 2] | Vereist om het veld te bewerken. |
| [!UICONTROL Creative Type] | Vereist om de status van een productadvertentie te maken of te bewerken. |
| [!UICONTROL Creative Preferred Devices] | Optioneel |
| [!UICONTROL Ad Status] | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Ad ID] | Dit is alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met ad-eigenschap bevat om de advertentie of b) en &quot;[!UICONTROL AMO ID].&quot; Als u echter geen van de [!UICONTROL Ad ID] noch [!UICONTROL AMO ID]en de kolommen met de eigenschap ad-eigenschap komen overeen met meerdere advertenties. De status voor slechts een van de advertenties verandert dan. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Product (winkelen) en velden

Raadpleeg voor meer informatie over het maken van winkeladvertenties &quot;[Implementeren [!DNL Microsoft Advertising] winkelcampagnes](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/microsoft-shopping-campaigns.html).&quot;

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Creative (except RSA)]&quot; Rij in de [!UICONTROL Download Bulksheet] .

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Promotion Line] | Optioneel |
| [!UICONTROL Base URL/Final URL] | Optioneel |
| [!UICONTROL Custom URL Param] | Optioneel |
| [!UICONTROL Creative Type] | Vereist om de status van een productadvertentie te maken of te bewerken. |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Ad Status] | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Ad ID] | Dit is alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met ad-eigenschap bevat om de advertentie of b) en &quot;[!UICONTROL AMO ID].&quot; Als u echter geen van de [!UICONTROL Ad ID] noch [!UICONTROL AMO ID]en de kolommen met de eigenschap ad-eigenschap komen overeen met meerdere advertenties. De status voor slechts een van de advertenties verandert dan. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Responsief (multimedia) en velden

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Creative (except RSA)]&quot; Rij in de [!UICONTROL Download Bulksheet] .

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Voor responsieve advertenties: [!UICONTROL Ad Title], [!UICONTROL Ad Title 2], en [!UICONTROL Ad Title 3] zijn vereist voor het maken van advertenties en alle andere velden voor advertentietitels zijn optioneel. Als u de bestaande waarde voor een niet-vereist veld wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). <b>Opmerking:</b> Als u voor dit advertentietype wijzigingen aanbrengt in de advertentie, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | [!UICONTROL Description Line 1] en [!UICONTROL Description Line 2] zijn vereist voor het maken van advertenties, en [!UICONTROL Description Line 3] en [!UICONTROL Description Line 4] zijn optioneel. <b>Opmerking:</b> Als u voor dit advertentietype wijzigingen aanbrengt in de advertentie, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie. |
| [!UICONTROL Business Name] | Vereist om een advertentie te maken of te verwijderen. |
| [!UICONTROL Call To Action] | Vereist om een advertentie te maken. |
| [!UICONTROL Call To Action Language] | Vereist om een advertentie te maken. |
| [!UICONTROL Base URL/Final URL] | Vereist om een advertentie te maken. |
| [!UICONTROL Creative Type] | Optioneel. |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Ad Status] | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Ad ID] | Dit is alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij a) voldoende kolommen met ad-eigenschap bevat om de advertentie of b) en &quot;[!UICONTROL AMO ID].&quot; Als u echter geen van de [!UICONTROL Ad ID] noch [!UICONTROL AMO ID]en de kolommen met de eigenschap ad-eigenschap komen overeen met meerdere advertenties. De status voor slechts een van de advertenties verandert dan. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Responsieve zoekopdrachten en velden

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Responsive Search Ad]&quot; Rij in de [!UICONTROL Download Bulksheet] .

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | Voor responsieve zoekadvertenties: [!UICONTROL Ad Title], [!UICONTROL Ad Title 2], en [!UICONTROL Ad Title 3] zijn vereist om een advertentie te maken en alle andere velden voor advertentietoldaties zijn optioneel. Als u de bestaande waarde voor een niet-vereist veld wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Optioneel |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Voor responsieve zoekadvertenties: [!UICONTROL Description Line 1] en [!UICONTROL Description Line 2] zijn vereist om een advertentie te maken, en [!UICONTROL Description Line 3] en [!UICONTROL Description Line 4] zijn optioneel. Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | Optioneel |
| [!UICONTROL Display Path 1] | Optioneel |
| [!UICONTROL Display Path 2] | Optioneel |
| [!UICONTROL Base URL/Final URL] | Vereist om een advertentie te maken. |
| [!UICONTROL Custom URL Param] | Optioneel |
| [!UICONTROL Creative Type] | Optioneel |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Ad Status] | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Ad ID] | Vereist om advertenties te bewerken of te verwijderen, tenzij de rij een &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Je moet advertenties bewerken of verwijderen, tenzij je de advertentie-id opneemt. |

### Tekst en velden

Voor dit advertentietype gebruikt u &quot;[!UICONTROL Creative (except RSA)]&quot; Rij in de [!UICONTROL Download Bulksheet] .

>[!NOTE]
>
>Uitgebreide tekstadvertenties zijn afgekeurd. U kunt alleen bestaande tekstadvertenties verwijderen.

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | Alleen-lezen |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] Alleen-lezen |
| [!UICONTROL Display URL] | Alleen-lezen |
| [!UICONTROL Display Path 1] | Alleen-lezen |
| [!UICONTROL Display Path 2] | Alleen-lezen |
| [!UICONTROL Base URL/Final URL] | Alleen-lezen |
| [!UICONTROL Custom URL Param] | Alleen-lezen |
| [!UICONTROL Creative Type] | Optioneel |
| [!UICONTROL Tracking Template] | Alleen-lezen |
| [!UICONTROL Creative Preferred Devices] | Alleen-lezen |
| [!UICONTROL Ad Status] | Vereist |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Ad ID] | Alleen vereist wanneer u de advertentiestatus wijzigt, tenzij de rij een &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de advertentie-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Dynamische doelvelden (automatisch doel) voor zoeken

>[!NOTE]
>
>Ondersteuning voor maken is niet beschikbaar.

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Auto Target Expression] | Vereist. |
| [!UICONTROL Match Type] | Optioneel |
| [!UICONTROL Max CPC] | Optioneel |
| [!UICONTROL Custom URL Param] | Optioneel |
| [!UICONTROL Target Status] | Vereist om een doel te verwijderen |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Target ID] | Alleen vereist wanneer u het automatische doel wijzigt of verwijdert, tenzij de rij een &quot;[!UICONTROL AMO ID]&quot; voor het doel. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Velden voor productgroepen kopen

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Match Type] | Vereist om een productgroep te maken. |
| [!UICONTROL Max CPC] | Vereist om een productgroep te maken. |
| [!UICONTROL Parent Product Groupings] | Vereist |
| [!UICONTROL Product Grouping] | Vereist |
| [!UICONTROL Partition Type] | Vereist om een productgroep te maken. |
| [!UICONTROL Base URL/Final URL] | Vereist |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Product Group Status] | Alleen vereist om een productgroep te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Product Group ID] | Dit is alleen vereist wanneer u de productgroep wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de productgroep te identificeren of b) en &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Sitemeelinktvelden op campagnereniveau

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| Beschrijving regel 1 | Optioneel |
| [!UICONTROL Description Line 2] | Optioneel |
| [!UICONTROL Start Date] | Optioneel |
| [!UICONTROL End Date] | Optioneel |
| [!UICONTROL Base URL/Final URL] | Vereist |
| [!UICONTROL Custom URL Param] | Optioneel |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Creative Preferred Devices] | Optioneel |
| [!UICONTROL Link Name] | Vereist |
| [!UICONTROL Sitelink Status] | Alleen vereist om een sitelink te verwijderen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Sitelink ID] | Dit is alleen vereist wanneer u de sitelink wijzigt of verwijdert, tenzij de rij a) voldoende eigenschapskolommen bevat om de sitelink te identificeren of b) en &quot;[!UICONTROL AMO ID].&quot; Als u echter geen van beide opties opneemt [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID]  en de bezitskolommen passen veelvoudige sitelinks aan, dan zal de status voor slechts één van de sitelinks veranderen.<br><br><b>Opmerking:</b> Als u de kolommen van de sitelink-eigenschap behalve Status voor een bestaande sitelink bewerkt, en u neemt geen van beide kolommen [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID], wordt er een nieuwe sitelink gemaakt en de bestaande sitelink wordt niet gewijzigd. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Locatiedoelvelden

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Location] | Vereist |
| [!UICONTROL Location Type] | Vereist om een doel te maken |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL Location Status] | Alleen vereist om een locatiedoel te verwijderen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de campagne-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Apparaatdoelvelden op campagnereniveau en op ad-groepniveau

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Device] | Vereist om een apparaatdoel te verwijderen. |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL Ad Group Name] | Vereist voor apparaatdoelen op ad-groepsniveau. Niet van toepassing op apparaatdoelen op campagneniveau. |
| [!UICONTROL Device Target Status] | Alleen vereist om een apparaatdoel te verwijderen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel; alleen van toepassing op ad-group-apparaatdoelen. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de apparaatdoel-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### De doelgebieden van RLSA van het campagne-niveau en van het ad groep

| Veld | Vereist? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij een &quot; bevat[!UICONTROL AMO ID]&quot; voor de entiteit. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist voor doelen op groepsniveau. Niet van toepassing op streefcijfers op campagneniveau. |
| [!UICONTROL Audience] | Vereist om een nieuw doel te creëren. |
| [!UICONTROL Target Type] | Optioneel |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL RLSA Target Status] | Vereist om een doel te schrappen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel; alleen van toepassing op streefcijfers op ad-groepsniveau. |
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
