---
title: Vereiste bulkbladgegevens voor  [!DNL Microsoft Advertising]  rekeningen
description: Verwijzing de vereiste kopbalgebieden en gegevensgebieden in bulksbladen voor  [!DNL Microsoft Advertising]  rekeningen.
exl-id: 2a5f0e7b-f020-4cca-9b77-807c2ee5c273
feature: Search Bulksheets
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '6928'
ht-degree: 0%

---

# Bijlage - Vereiste bulksbladgegevens voor [!DNL Microsoft Advertising] -accounts

Als u [!DNL Microsoft Advertising] -campagnegegevens bulksgewijs wilt maken en bijwerken, kunt u de bulkbladbestanden Zoeken, Sociaal en Commerce gebruiken die specifiek zijn opgemaakt voor [!DNL Microsoft Advertising] -accounts. U kunt of a) [&#x200B; bulkbladdossiers voor bestaande rekeningen &#x200B;](../bulksheet-download.md) in het vereiste dossierformaat of b) manueel tot hen leiden (zie &quot;[&#x200B; Ondersteunde Formaten van het Dossier van het Bulksblad &#x200B;](bulksheet-file-formats.md)&quot;voor algemene informatie over de gesteunde dossierformaten).

Elk bulksheet moet de kopbalgebieden en overeenkomstige gegevensgebieden omvatten die voor de [&#x200B; worden vereist specifieke verrichtingen u &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) (zoals het creëren van een advertentie) wilt uitvoeren. Als een veld niet vereist is, kunt u het weglaten uit de koptekst- en gegevensrijen. Alle aangepaste kolommen worden verwijderd wanneer u het bulkbladbestand uploadt.

Hieronder volgt een tabel met alle beschikbare gegevensvelden en aanvullende tabellen die aangeven welke velden vereist zijn om gegevens voor afzonderlijke entiteiten (zoals campagnes en trefwoorden) toe te voegen, te bewerken of te verwijderen.

## Alle beschikbare gegevensvelden {#bulksheet-fields-all-microsoft}

In de volgende tabel worden alle beschikbare gegevensvelden beschreven.

Voor de gegevensgebieden relevant voor rekeningsentiteiten, zie &quot;[&#x200B; Gebieden die worden vereist om, elke rekeningscomponent &#x200B;](#bulksheet-fields-per-component-microsoft) tot stand te brengen uit te geven of te schrappen.&quot;

| Veld | Beschrijving |
|----|----|
| [!UICONTROL Platform] | (Opgenomen in gegenereerde bulksbladen ter informatie) Het advertentieplatform. Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Acct Name] | De unieke naam die een advertentienetwerkaccount identificeert. Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | De unieke naam die een campagne voor een account identificeert. De maximumlengte is 128 tekens. |
| [!UICONTROL Campaign Budget] | Het dagelijkse of maandelijkse campagnebudget, met of zonder monetaire symbolen en leestekens. Het mag niet minder zijn dan 0,05. |
| [!UICONTROL Channel Type] | Het type kanaal dat de campagne als doel heeft: <i>[!UICONTROL Audience]</i>, <i>[!UICONTROL DynamicSearchAds]</i>, <i>[!UICONTROL Search]</i> of <i>[!UICONTROL Shopping]</i> . |
| [!UICONTROL Delivery Method] | (Alleen campagnes met dagelijkse budgetten) Hoe snel u elke dag advertenties voor de campagne kunt weergeven:<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (de standaardinstelling voor nieuwe campagnes): uw advertenties over de dag verspreiden.</li><li><i>[!UICONTROL Accelerated]:</i> om uw advertenties zo vaak mogelijk weer te geven tot uw budget is bereikt. Hierdoor worden uw advertenties mogelijk niet later op de dag weergegeven.</li></ul> |
| [!UICONTROL Campaign Priority] | (Alleen voor winkelcampagnes) De prioriteit waarmee de campagne wordt gebruikt wanneer meerdere campagnes adverteren voor hetzelfde product: <i>[!UICONTROL Low]</i> (de standaardinstelling voor nieuwe campagnes), <i>[!UICONTROL Medium]</i> of <i>[!UICONTROL High]</i> .<br><br> wanneer het zelfde product in meer dan één campagne inbegrepen is, gebruikt het advertentienetwerk eerst de campagneprioriteit om te bepalen welke campagne (en bijbehorende bieding) voor de advertentievieiling verkiesbaar is. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel. |
| [!UICONTROL Merchant ID] | (Winkelcampagnes en publiekscampagnes die alleen zijn gekoppeld aan een commerciële feed) De klant-id van het zakelijke account waarvan de producten voor de campagne worden gebruikt. |
| [!UICONTROL Sales Country] | (Alleen winkelcampagnes; alleen-lezen voor bestaande campagnes) Het land waar de producten van de campagne worden verkocht. Omdat de producten met doellanden worden geassocieerd, bepaalt dit het plaatsen welke producten in de campagne worden geadverteerd. |
| [!UICONTROL Product Scope Filter] | (Campagnes die het winkelnetwerk slechts gebruiken) De producten in uw handelaarrekening waarvoor productadvertenties voor de campagne kunnen worden gecreeerd. U kunt maximaal zeven productafmetingen en kenmerkcombinaties ingaan waarop om uw producten te filtreren, gebruikend het formaat dimensi=attribute. Scheid meerdere filters met een scheidingsteken &quot;>>&quot;. Voor een lijst van beschikbare productafmetingen, zie &quot;[&#x200B; het Verkopen de filters van het campagneproduct &#x200B;](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;<br><br> Voorbeeld: &quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br> om de bestaande waarden te schrappen, gebruik de waarde `[delete]` (met inbegrip van de steunen). |
| [!UICONTROL DSA Domain Name] | (Campagnes van type a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; of b) &quot;<i>[!UICONTROL Search]</i>&quot; wanneer het [!DNL ExperimentId] element niet wordt geplaatst) De domeinnaam van de website aan doel voor dynamische onderzoeksadvertenties. De maximale lengte is 2.048 tekens. Als de domeinnaam `www` bevat, wordt deze bijgesneden en niet gebruikt.<br><br> voor bestaande campagnes, kunt u niet het domein uitgeven, maar u moet het omvatten om andere eigenschappen bij te werken. |
| [!UICONTROL DSA Domain Language] | (Campagnes van type a) &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot; of b) &quot;<i>[!UICONTROL Search]</i>&quot; wanneer het [!DNL ExperimentId] element niet wordt geplaatst) De taal van de websitepagina&#39;s aan doel voor dynamische onderzoeksadvertenties. De ondersteunde domeintalen zijn [!UICONTROL Dutch], [!UICONTROL English], [!UICONTROL French], [!UICONTROL German], [!UICONTROL Italian], [!UICONTROL Spanish] en [!UICONTROL Swedish] .<br><br> voor bestaande campagnes, kunt u niet de taal uitgeven, maar u moet het omvatten om andere eigenschappen bij te werken. |
| [!UICONTROL Ad Group Name] | De unieke naam die een advertentiegroep identificeert. De maximumlengte is 128 tekens. Navolgende lege tekens worden niet opgeslagen (zoals &#39;Groep 1 toevoegen&#39; wordt opgeslagen als &#39;Groep 1 toevoegen&#39;). |
| [!UICONTROL Ad Group Type] | (Campagnes op het zoeknetwerk; alleen-lezen voor bestaande advertentiegroepen) Het type advertentiegroep: <i>[!UICONTROL Audience]</i> (alleen voor publiekscampagnes), <i>[!UICONTROL Search Dynamic]</i> (alleen voor dynamische zoekadvertenties) en <i>[!UICONTROL Search Standard]</i> (alleen voor responsieve zoekadvertenties en bestaande uitgevouwen tekstadvertenties). Sommige soorten campagnes kunnen veelvoudige advertentiegroep types omvatten. |
| [!UICONTROL Keyword] | (Campagnes op het onderzoeksnetwerk slechts) het sleutelwoordkoord. De maximumlengte is 50 tekens.<br><br><b> Nota&#39;s:</b><ul><li>Als u een trefwoord op advertentiegroep- of campagnereniveau wilt uitsluiten, stelt u de [!UICONTROL Match Type] in op `Negative` . Als de rij de naam van de advertentiegroep bevat, wordt het trefwoord uitgesloten voor de advertentiegroep. Als de rij niet de naam van de advertentiegroep omvat, wordt het sleutelwoord uitgesloten voor de volledige campagne.</li><li>Als u het trefwoord [!DNL Microsoft Advertising] wijzigt, wordt het bestaande trefwoord verwijderd en wordt een nieuw trefwoord met een nieuwe id gemaakt. Als u het overeenkomsttype wijzigt, wordt het bestaande trefwoord echter niet verwijderd.</li></ul> |
| Plaatsing | Vervangen |
| [!UICONTROL Audience] | De lijst voor het opnieuw op de markt brengen van onderzoeksadvertenties (RLSA) doelpubliek voor de campagne of de ad groep. |
| [!UICONTROL Target Type] | (RLSA richt slechts) het doeltype: <i>[!UICONTROL Inclusion]</i> of <i>[!UICONTROL Exclusion]</i>. |
| [!UICONTROL Auto Target Expression] | Dynamische zoekdoelen voor de advertentiegroep. Voor alle doelstellingen, gebruik &quot;[!UICONTROL All Web Pages]&quot;.<br><br> om tot drie dynamische onderzoekscriteria te richten, gebruik het formaat `<category>=<target>`, waar &lt;category> om het even welke hieronder categorieën kan omvatten. Verbind veelvoudige doelstellingen voor een individuele categorie met &quot;`[blank space] and [blank space]`&quot;en sluit zich bij veelvoudige categorieën aan &quot;`[blank space] and [blank space]`&quot;.<br><ul><li><i> Categorie:</i> om dynamische onderzoeksadvertenties voor geïndexeerde pagina&#39;s met een specifieke de inhoudscategorie van Google te tonen.</li><li><i> URL:</i> om dynamische onderzoeksadvertenties voor geïndexeerde pagina&#39;s met specifieke URL te tonen, waar de waarde overal binnen URL kan worden omvat.</li><li><i> Titel van de Pagina:</i> om dynamische onderzoeksadvertenties voor geïndexeerde pagina&#39;s met specifieke tekst in de paginatitel te tonen.</li><li><i> Inhoud van de Pagina:</i> om dynamische onderzoeksadvertenties voor geïndexeerde pagina&#39;s met specifieke inhoud te tonen.</li></ul>Voorbeeld: url=shoes.example.com en page title=schoeisel <br> Voorbeeld: Alle Pagina&#39;s van het Web |
| [!UICONTROL Location] | Een geografische locatie waar advertenties voor de campagne of advertentiegroep moeten worden geplaatst. De waarden zijn niet hoofdlettergevoelig. Als u geen waarden voor de campagne of advertentiegroep invoert, worden alle locaties als doel ingesteld. Als u specifieke locaties als doel wilt instellen, voert u de locatie in met behulp van de notaties voor de [!DNL Microsoft Advertising] -locatiecode. Als u een locatielijst wilt downloaden, meldt u zich aan bij de [!DNL Microsoft Advertising] -ontwikkelaarportal met de referenties van uw [!DNL Microsoft Advertising] -advertentieaccount. <b> Nota:</b> om een plaats uit te sluiten, ga de plaatscode met een minus teken (`-`), zoals `-United States` vooraf. |
| [!UICONTROL Location Type] | Het type locatie, zoals Plaats, Land, MetroArea, PostalCode en Frame. Als u een locatielijst wilt downloaden, meldt u zich aan bij de [!DNL Microsoft Advertising] -ontwikkelaarportal met de referenties van uw [!DNL Microsoft Advertising] -advertentieaccount. |
| [!UICONTROL Match Type] | (Alleen campagnes op het zoeknetwerk) De optie(s) voor trefwoordafstemming. Dit kan de optie voor trefwoordafstemming voor een dynamisch zoekdoel of een productgroep omvatten. Waarden zijn onder andere : <i>[!UICONTROL Broad]</i> (de standaardwaarde voor nieuwe trefwoorden), <i>[!UICONTROL Exact]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Content]</i> (automatisch ingesteld voor trefwoorden wanneer de advertentiegroep het inhoudsnetwerk als doel instelt), <i>[!UICONTROL Negative]</i> (om een trefwoord uit te sluiten in het inhoudsnetwerk), <i>[!UICONTROL Dynamic Ad Target]</i> (de standaardwaarde voor nieuwe dynamische zoekdoelen), <i>[!UICONTROL Product Group]</i> (de standaardwaarde voor nieuwe productgroepen) of <i>[!UICONTROL Negative Product Group]</i> (om een productgroep uit te sluiten).  Een waarde voor of het gelijke type of sleutelwoordidentiteitskaart wordt vereist om een sleutelwoord met veelvoudige gelijke types uit te geven of te schrappen.<br><br> voor Brede Modifier van de Overeenkomst, kies &quot;Breed&quot;en neem a `+` vóór om het even welk woord binnen het sleutelwoord op dat (zoals &quot; `+red +shoes`&quot;wordt vereist om zowel &quot;rood&quot;als &quot;schoenen&quot; te vereisen).<br><br> Veranderend het gelijke type voor a [!DNL Microsoft Advertising] sleutelwoord schrapt niet het bestaande sleutelwoord. |
| [!UICONTROL Max CPC] | (Campagnes op het onderzoeksnetwerk) De maximumkosten per klik (CPC), die het hoogste bedrag voor een advertentieklik is dat op het sleutelwoord, de productgroep, of het dynamische onderzoeksdoel wordt gebaseerd, met of zonder monetaire symbolen en punctuatie.  Voor bestaande trefwoorden en productgroepen zijn de records in geoptimaliseerde portfolio&#39;s slechts één dag geldig en worden de updates tijdens de volgende optimalisatiecyclus overschreven. <b> Nota:</b> u kunt geen biedingen voor negatieve sleutelwoorden plaatsen. |
| [!UICONTROL Max Content CPC] | (Alleen-lezen voor CPC-campagnes die zijn gemaakt voordat het inhoudsnetwerk in 2017 is afgekeurd) De maximale kosten voor inhoud per klik (CPC). Dit is het hoogste bedrag dat wordt betaald voor een advertentie via een netwerksite voor weergave, met of zonder monetaire symbolen en interpunctie. |
| [!UICONTROL Audience Target Method] | (Publiek en groepen) Of:<ul><li><i>[!UICONTROL Target and Bid]:</i> om alleen advertenties weer te geven aan gebruikers die zijn gekoppeld aan doelgroepen die ook voldoen aan andere doelen voor de advertentiegroep.</li><li><i>[!UICONTROL Bid Only]:</i> om advertenties zelfs aan mensen te tonen die niet met doelpubliek worden geassocieerd zolang zij andere ad groep-vlakke doelstellingen voldoen.</li></ul> U kunt de kans echter vergroten dat advertenties bij een bepaald publiek worden getoond door voor dat publiek hogere biedingen in te stellen. |
| [!UICONTROL Parent Product Groupings] | De hiërarchie van bovenliggende productgroepen.<br><br> Voorbeeld: `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | De productgroep (zoals &quot;brand=acme&quot; of &quot;Alle producten&quot;).<br><br><b> Nota&#39;s:</b><ul><li>Wanneer een gespecificeerde productgroep niet in de hiërarchie van de Groepen van het Product van de Ouder bestaat, leidt het Onderzoek, Sociaal, &amp; Commerce tot om het even welke delen van de hiërarchie die nodig zijn.</li><li>Met Zoeken, Sociaal en Commerce wordt automatisch een groep [!UICONTROL All Products] gemaakt wanneer u een advertentiegroep maakt in een winkelcampagne met een standaardbod ingesteld op het standaardbod van de advertentiegroep. Met Zoeken, Sociaal en Commerce wordt automatisch een groep [!UICONTROL Everything Else] gemaakt met het standaardbod voor de advertentiegroep op elk niveau van de hiërarchie van de productgroepen. U kunt deze standaardgroepen nog steeds expliciet maken en ze uitsluiten of hun biedingen wijzigen.</li><li>Elke ad groep kan tot acht niveaus van productgroepen, met inbegrip van &quot;[!UICONTROL All Products]&quot;en zeven andere lagen omvatten.</li></ul> |
| [!UICONTROL Partition Type] | Het partitietype voor de productgroep: <i>[!UICONTROL subdivision]</i> (wanneer deze onderliggende productgroepen heeft) of <i>[!UICONTROL unit]</i> (wanneer deze geen onderliggende productgroepen heeft). |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] -[!UICONTROL Ad Title 15] | (Alleen uitgevouwen tekstadvertenties, multimediadaden, responsieve advertenties en responsieve zoekadvertenties) De kopregels van een advertentie. De maximumlengte voor elk veld van de advertentie is 30 karakters of 15 dubbel-byte karakters, met inbegrip van om het even welke dynamische teksten (zoals de waarden van sleutelwoorden, `{Param2}` en `{Param3}` dynamische vervangingsvariabelen, en adverteerders).<br><br> Voor responsieve zoekadvertenties voegt u een advertentieklanker in met de volgende indeling, waarbij &#39;Standaardtekst&#39; een optionele waarde is die moet worden ingevoegd wanneer het bestand met de feed geen geldige waarde bevat: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br> Voor uitgebreide tekstadvertenties zijn Titel en Titel 2 van advertentie vereist en [!UICONTROL Ad Title 3] is optioneel. [!DNL Microsoft Advertising] heeft in augustus 2022 uitgebreide tekstadvertenties vervangen en u kunt deze nu alleen melden en verwijderen.<br><br> Voor multimediadaden, responsieve advertenties en responsieve zoekopdrachten zijn [!UICONTROL Ad Title] , [!UICONTROL Ad Title 2] en [!UICONTROL Ad Title 3] vereist en zijn alle andere titelvelden van de advertentie optioneel.<br><br> om de bestaande waarde voor een niet vereist gebied te schrappen, gebruik de waarde `[delete]` (met inbegrip van de steunen).<br><br> voor alle advertentietypes behalve uitgebreide tekstadvertenties, schrapt het veranderen van het advertentiekopie de bestaande advertentie en leidt tot een nieuwe advertentie met de zelfde eigenschappen. |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | (Alleen responsieve zoekopdrachten; optioneel) Een positie waarop de bijbehorende advertentietak moet worden vastgezet: `[null]` (geen waarde, waardoor de titel van de advertentie voor alle posities in aanmerking komt), 1, 2 of 3. Als [!UICONTROL Ad Title Position] bijvoorbeeld de waarde 1 heeft, kan [!UICONTROL Ad Title] alleen op positie 1 worden weergegeven. Standaard zijn alle advertentitels null (geen waarden). Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (inclusief de vierkante haakjes).<br><br><b> Nota:</b> u kunt veelvoudige advertentietitels aan de zelfde positie vastzetten. In het advertentienetwerk wordt een van de advertentietitels gebruikt die op de positie zijn vastgezet. Titels die op positie 3 zijn vastgezet, worden mogelijk niet met de advertentie weergegeven. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | (Tekstadvertenties, dynamische zoekadvertenties, multimedia-advertenties, responsieve zoekadvertenties en alleen verbeterde sitelinks op campageniveau) De hoofdtekst van een advertentie of sitelink.<br><br> voor sitelinks, gebruik naar keuze zowel [!UICONTROL Description Line 1] als [!UICONTROL Description Line 2] om extra tekst te omvatten die het advertentienetwerk onder de verbindingstekst kan tonen. Elk beschrijvingsveld kan maximaal 35 single-byte of 17 double-byte tekens bevatten.<br><br> voor advertenties, is de maximumlengte voor elk beschrijvingsgebied 90 karakters of 45 dubbel-byte karakters, met inbegrip van om het even welke dynamische teksten (zoals de waarden van sleutelwoorden en adverteerders).<br><br> voor ontvankelijke onderzoeksadvertenties, neem een adverteerder op gebruikend het volgende formaat, waar Standaard tekst een facultatieve waarde is op te nemen wanneer uw voederdossier geen geldige waarde omvat: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br> voor tekstadvertenties en dynamische onderzoeksadvertenties, is Regel 1 van de Beschrijving vereist en [!UICONTROL Description Line 2] is facultatief.<br><br> Voor multimediadaden, responsieve advertenties en responsieve zoekopdrachten zijn [!UICONTROL Description Line 1] en [!UICONTROL Description Line 2] vereist en zijn [!UICONTROL Description Line 3] en [!UICONTROL Description Line 4] optioneel.<br><br> om de bestaande waarde te schrappen, gebruik de waarde `[delete]` (met inbegrip van de steunen).<br><br><b> Nota&#39;s:</b><ul><li>(Standaardtekstadvertenties) De gecombineerde titel en tekst moeten ten minste drie woorden lang zijn.</li><li>(Uitgebreide tekstadvertenties) In dit veld kunnen optioneel de variabelen {Param2} en {Param3} dynamic substitution worden opgenomen. In dat geval is de maximale lengte van de advertentietekst 300 single-byte of 150 double-byte tekens. [!DNL Microsoft Advertising] heeft in augustus 2022 uitgebreide tekstadvertenties vervangen en u kunt deze nu alleen melden en verwijderen.</li><li>(Dynamische zoekopdrachten) Dynamische vervangingstekst is niet toegestaan.</li><li>Voor alle advertentietypen, behalve uitgevouwen tekstadvertenties, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie.</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | (Alleen responsieve zoekopdrachten; optioneel) Een positie waarop de corresponderende beschrijving moet worden vastgezet: `[null]` (geen waarde, waardoor de beschrijving in aanmerking komt voor alle posities), 1, 2 of 3. Als [!UICONTROL Description 1 Position] bijvoorbeeld de waarde 1 heeft, kan Beschrijving 1 alleen op Positie 1 worden weergegeven. Standaard zijn geen beschrijvingen vastgezet op een positie.<br><br> om de bestaande waarde te schrappen, gebruik de waarde `[delete]` (met inbegrip van de steunen).<br><br><b> Nota:</b> u kunt veelvoudige beschrijvingen aan de zelfde positie vastzetten. Het advertentienetwerk gebruikt één van de beschrijvingen die aan de positie worden vastgezet. Beschrijvingen die op positie 2 zijn vastgezet, mogen niet met de advertentie worden getoond. |
| [!UICONTROL Business Name] | (Alleen multimediaadvertenties) De bedrijfsnaam, met maximaal 25 tekens. |
| [!UICONTROL Promotion Line] | (Alleen aanbiedingen voor producten) Een unieke promotielijn die in de zoekresultaten bij de aanbieding van het product moet worden opgenomen (zoals Nu gratis verzending). De maximumlengte is 45 tekens.<br><br> de bevorderingslijn kan in verschillende plaatsen met betrekking tot de advertentie (zoals onder de advertentie) afhankelijk van verschijnen waar de advertentie op de pagina verschijnt. |
| [!UICONTROL Display URL] | De URL die is opgenomen in de advertentie.<br><br> voor uitgebreide dynamische onderzoeksadvertenties, produceert het advertentienetwerk deze waarde dynamisch van het websitedomein, en u te hoeven om geen waarde in te gaan.<br><br> voor uitgebreide tekstadvertenties en ontvankelijke onderzoeksadvertenties, te hoeven u om geen waarde in te gaan. De weergave-URL wordt automatisch opgehaald uit het domein in de uiteindelijke URL. U kunt de URL desgewenst aanpassen met de velden Pad 1 en Pad 2.<br><br><b> Nota&#39;s:</b><ul><li>(Accounts met definitieve URL&#39;s) De domeinnamen in de weergave-URL en de uiteindelijke URL moeten overeenkomen.</li><li>[!DNL Microsoft Advertising] heeft in augustus 2022 uitgebreide tekstadvertenties vervangen en u kunt deze nu alleen melden en verwijderen.</li></ul> |
| [!UICONTROL Display Path 1] | (Alleen uitgevouwen tekstadvertenties, dynamische zoekadvertenties en responsieve zoekadvertenties) Tekst die aan de weergave-URL is toegevoegd en die automatisch uit de uiteindelijke URL wordt geëxtraheerd. Elk pad wordt voorafgegaan door een slash (/) in de URL. Een pad mag geen forward slash (/) of newline (\n) tekens bevatten. De maximumlengte voor elk pad is 15 tekens of 7 double-byte tekens.<br><br> om een advertentieklanker op te nemen, gebruik de volgende formaten, waar &quot;Standaardtekst&quot;een facultatieve waarde is om op te nemen wanneer uw voederdossier geen geldige waarde omvat: `{CUSTOMIZER.Attribute name:Default text}`, zoals `{CUSTOMIZER.Discount:10%}`<br><br> bijvoorbeeld, als [!UICONTROL Display Path 1] &quot;overeenkomsten is,&quot;dan zou de vertoning URL &lt;display URL>/deals, zoals www.example.com/deals zijn.<br><br>[!DNL Microsoft Advertising] heeft in augustus 2022 uitgebreide tekstadvertenties vervangen en u kunt deze nu alleen melden en verwijderen. |
| [!UICONTROL Display Path 1] | (Alleen uitgebreide tekstadvertenties, dynamische zoekadvertenties en responsieve zoekadvertenties) Een extra weergavepad. Zie de vermelding voor [!UICONTROL Display Path 1] .<br><br> Voorbeeld: Als [!UICONTROL Display Path 1] &quot;overeenkomsten&quot;is en [!UICONTROL Display Path 2] &quot;lokaal is,&quot;dan zou de vertoning URL &lt; <i> vertoning URL </i>>/deals/local, zoals www.example.com/deals/local zijn. |
| [!UICONTROL Start Date] | (Alleen verbeterde sitelinks) De eerste datum waarop biedingen voor de sitelink mogen worden ingediend, in de tijdzone van de adverteerder en in een van de volgende formaten: m/d/jjjj, m/d/jj, m-d-jjjj of m-d-jj. De standaard voor nieuwe verbeterde sitelinks is de huidige dag. <b> Nota:</b> Nieuwe verbeterde sitelinks kan slechts in campagnes met bestaande verbeterde sitelinks of geen sitelinks worden gecreeerd. |
| [!UICONTROL End Date] | De laatste datum waarop de sitelink met advertenties kan worden weergegeven in de tijdzone van de adverteerder en in een van de volgende notaties: m/d/jjjj, m/d/jj, m-d-jjjj of m-d-jj. Voor een nieuwe sitelink is de standaardwaarde `[blank]` (dat wil zeggen, geen einddatum). |
| [!UICONTROL Call To Action] | De call to action die in de advertentie moet worden opgenomen. Zie de [&#x200B; API verwijzing voor een lijst van mogelijke waarden &#x200B;](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction), maar ga multi-woordvraag aan actie als veelvoudige woorden (zoals &quot;Bet nu&quot;in plaats van &quot;BetNow&quot;) in bulksbladen in. |
| [!UICONTROL Call To Action Language] | De taal voor de call to action-opties. Zie de [&#x200B; API verwijzing voor een lijst van mogelijke talen &#x200B;](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename). |
| [!UICONTROL Base URL/Final URL] | De bestemmingspagina URL waarnaar de gebruikers van de onderzoeksmotor worden genomen wanneer zij uw advertentie klikken, met inbegrip van om het even welke toevoegingsparameters die voor de campagne of de rekening worden gevormd. Basis/definitieve URLs op het sleutelwoordniveau treedt die op het advertentieniveau en hoger met voeten.<br><br> om de bestaande waarde te schrappen, gebruik de waarde `[delete]` (met inbegrip van de steunen). |
| [!UICONTROL Destination URL] | (Opgenomen in gegenereerde bulksbladen voor informatiedoeleinden; niet gepost naar het zoekprogramma) Voor accounts met bestemmings-URL&#39;s is dit de URL die een advertentie koppelt aan een basis-URL/bestemmingspagina op de website van de adverteerder (soms via een andere site die de klik bijhoudt en de gebruiker vervolgens omleidt naar de bestemmingspagina). Het bevat alle toevoegingsparameters die zijn geconfigureerd voor de campagne of account voor Zoeken, Sociaal zoeken en Commerce. Als u URL&#39;s voor bijhouden hebt gegenereerd, is dit gebaseerd op de volgende parameters in uw accountinstellingen en campagnemontages. Als u specifieke parameters voor zoekprogramma&#39;s hebt toegevoegd, kunnen deze worden vervangen door de equivalente parameters voor Zoeken, Sociaal en Commerce.<br><br> voor rekeningen met definitieve URLs, toont deze kolom de zelfde waarde zoals de Basis URL/Definitieve kolom URL. |
| [!UICONTROL Custom URL Param] | Gegevens die de dynamische variabele `{custom_code}` moeten vervangen wanneer de variabele is opgenomen in de volgende parameters voor de instellingen van de zoekaccount of campagne. Als u de aangepaste waarde in de URL voor bijhouden wilt invoegen, moet u het bestand met de opsommingstekens uploaden met de optie URL&#39;s voor reeksspatiëring genereren. |
| [!UICONTROL Creative Type] | De advertentievorm: <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i> (winkeladvertenties), of <i>[!UICONTROL Responsive Search Ad]</i>, of <i>[!UICONTROL Text ad]</i> . De standaardwaarde voor nieuwe advertenties is <i>[!UICONTROL Text ad]</i> . |
| [!UICONTROL Ad Group Start Date] | De eerste datum waarop biedingen voor de advertentiegroep mogen worden ingediend, in de tijdzone van de adverteerder en in een van de volgende formaten: m/d/jjjj, m/d/jj, m-d-jjjj of m-d-jj. Voor een nieuwe advertentiegroep is de standaardwaarde de huidige datum. |
| [!UICONTROL Ad Group End Date] | De laatste datum waarop biedingen voor de advertentiegroep mogen worden ingediend, in de tijdzone van de adverteerder en in een van de volgende formaten: m/d/jjjj, m/d/jj, m-d-jjjj of m-d-jj. Voor een nieuwe advertentiegroep, is het gebrek [ leeg ] (namelijk geen einddatum). |
| [!UICONTROL Tracking Template] | (Optioneel) De sjabloon voor reeksspatiëring, die alle parameters voor het omleiden en bijhouden van domeinen opgeeft en de laatste URL in een parameter insluit. De het volgen malplaatje op het meest korrelige niveau (met sleutelwoord als meest korrelig) treedt de waarden op alle hogere niveaus met voeten.<br><br> voor het omzetten van Adobe Advertising volgen, die wordt toegepast wanneer de campagnemontages &quot; [!UICONTROL EF Redirect]&quot;en &quot;[!UICONTROL Auto Upload] omvatten,&quot;Onderzoek, Sociale, &amp; Commerce voegt automatisch omleiding en het volgen code toe wanneer u sparen het verslag.<br><br> voor derdeomleiding en het volgen, ga een waarde in.<br><br> voor een lijst van parameters om definitieve URLs in het volgen malplaatjes aan te geven, zie de [!DNL Microsoft Advertising] documentatie.<br><br> Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (inclusief de vierkante haakjes). |
| [!UICONTROL Landing Page Suffix] | Alle parameters die aan het einde van de uiteindelijke URL&#39;s moeten worden toegevoegd om informatie bij te houden. Voorbeeld: `param2=value1&param3=value2`<br><br> zie &quot;[&#x200B; klik-volgende formaten voor  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).&quot;<br><br> definitieve URL achtervoegsels op lagere niveaus treden het rekening-vlakke achtervoegsel met voeten. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Als u een achtervoegsel wilt configureren op ad-groepsniveau of lager, gebruikt u de [!DNL Microsoft Advertising] -editor. |
| Netwerkstatus zoeken | Of u advertenties voor de advertentiegroep op verschillende elementen van het Zoeknetwerk wilt plaatsen:<ul><li><i> allen:</i> om advertenties op alle het onderzoeksnetwerken van de Bing en gesynchroniseerde onderzoekspartners te plaatsen.</li><li><i> OwnedAndOperatedOnly:</i> om advertenties slechts op Bing en Yahoo te plaatsen! websites.</li><li><i> SyndicatedSearchOnly:</i> om advertenties slechts op Bing en Yahoo te plaatsen! gesynchroniseerde zoekpartners.</li><li><i> weg:</i> om advertenties op het Netwerk van de Inhoud slechts (niet het Netwerk van het Onderzoek) te plaatsen.</li></ul> Voor nieuwe advertentiegroepen is de standaardwaarde Aan. |
| [!UICONTROL Content Network Status] | Vervangen |
| [!UICONTROL Languages] | De doeltaal voor advertenties in de advertentiegroep: [!UICONTROL English], [!UICONTROL French], [!UICONTROL Finnish], [!UICONTROL German], [!UICONTROL Norwegian], [!UICONTROL Spanish] of [!UICONTROL Swedish] . De standaardwaarde voor nieuwe campagnes is [!UICONTROL English].<br><br> dit het plaatsen bepaalt de landen en de gebieden waarin uw advertentie kan worden getoond. Zorg ervoor dat u een taal kiest die compatibel is met de locatiedoelen van de campagne. |
| [!UICONTROL Budget Type] | Geeft aan of het budget <i>[!UICONTROL Daily]</i> (de standaardwaarde) of <i>[!UICONTROL Monthly]</i> is.<br><br> Nota: Als u de campagne aan een geoptimaliseerde portefeuille toewijst, wordt deze waarde automatisch geplaatst aan [!UICONTROL Daily]. |
| [!UICONTROL Device] | Een apparaattype waarvoor biedaanpassingen worden uitgevoerd op campagne- of advertentieniveau: <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i> of <i>[!UICONTROL desktop]</i> . |
| [!UICONTROL Bid Adjustment] | De bodaanpassing voor een opgegeven doeltype. Als het bod op het trefwoordniveau bijvoorbeeld 1 USD is en het bod voor smartphones 50% is, is het bod op de smartphone 1,50 USD. Standaard worden alle doelen geboden bij het bod op trefwoordniveau. Geldige percentages zijn:<ul><li>Smartphones en tablets: -100 (om niet te bieden voor het apparaattype) en van -90 tot 900</li><li>Desktop: van 0 tot 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | De apparaattypen waarop u de advertentie of sitelink wilt weergeven: <i>[!UICONTROL All]</i> (de standaardinstelling) of <i>[!UICONTROL Mobile]</i> . Wanneer Mobiel is opgegeven, probeert het netwerk de advertentie of sitelink aan gebruikers van mobiele apparaten weer te geven in plaats van aan gebruikers van desktopcomputers of tablets. Anders geeft het netwerk de advertentie of de sitelink weer op elk apparaattype. <b> Nota:</b> het netwerk waarborgt niet dat het de advertentie op het aangewezen apparatentype zal tonen. |
| [!UICONTROL Param2] | De tekenreeks die als vervangende waarde moet worden gebruikt als de basis-URL van het trefwoord of de titel, beschrijving of basis-URL van de advertentie de `{Param2}` dynamische vervangingstekenreeks bevat. De maximumlengte is 70 tekens, maar houd rekening met de maximumlengte van de advertentie-elementen waarin u deze gebruikt (de combinatie van Titel 1 en Titel 2 kan bijvoorbeeld maximaal 76 tekens bevatten). Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (inclusief de vierkante haakjes). |
| [!UICONTROL Param3] | De tekenreeks die als vervangende waarde moet worden gebruikt als de basis-URL van het trefwoord of de titel, beschrijving of basis-URL van de advertentie de `{Param3}` dynamische vervangingstekenreeks bevat. De maximumlengte is 70 tekens, maar houd rekening met de maximumlengte van de advertentie-elementen waarin u deze gebruikt (de combinatie van Titel 1 en Titel 2 kan bijvoorbeeld maximaal 76 tekens bevatten). Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (inclusief de vierkante haakjes). |
| [!UICONTROL Link Name] | De sitelink-tekst. Het moet uniek zijn in de campagne. Als u Description1 en Description2 specificeert, dan kan de sitelink tekst tot 25 single-byte of 12 dubbel-byte karakters omvatten; anders, kan de sitelink tekst tot 35 single-byte of 17 dubbel-byte karakters omvatten.<br><br>[!DNL Microsoft Advertising] kan twee, vier of zes verbeterde sitelinks met beschrijvingen weergeven, of vier of zes sitelinks in één rij zonder beschrijvingen, met een advertentie.<br><br> u kunt nieuwe verbeterde sitelinks slechts in campagnes met bestaande verbeterde sitelinks of geen sitelinks tot stand brengen. |
| [!UICONTROL Campaign Status] | De weergavestatus van de campagne: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande campagnes). De standaardwaarde voor nieuwe campagnes is [!UICONTROL Active]. Voer de waarde `Deleted` in om een actieve of gepauzeerde campagne te verwijderen. |
| [!UICONTROL Ad Group Status] | De weergavestatus van de advertentiegroep: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande advertentiegroepen). De standaardwaarde voor nieuwe advertentiegroepen is [!UICONTROL Active] . Als u een actieve of gepauzeerde advertentiegroep wilt verwijderen, voert u de waarde `Deleted` in. |
| [!UICONTROL Keyword Status] | De weergavestatus van het trefwoord: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande trefwoorden). De standaardwaarde voor nieuwe trefwoorden is [!UICONTROL Active] . Voer de waarde `Deleted` in om een actief of gepauzeerd trefwoord te verwijderen. <b> Nota:</b> als u het volgen URLs voor een sleutelwoord met veelvoudige gelijke types creeert, dan moet de sleutelwoordstatus voor elk overeenkomstentype het zelfde zijn. |
| [!UICONTROL Placement Status] | Vervangen |
| [!UICONTROL Ad Status] | De weergavestatus van de advertentie: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> (alleen bestaande advertenties), <i>[!UICONTROL Disapproved]</i> (niet bewerkbaar) of <i>[!UICONTROL Paused]</i> . De standaardwaarde voor nieuwe advertenties is [!UICONTROL Active] . Voer de waarde `Deleted` in om een actieve of gepauzeerde advertentie te verwijderen. |
| [!UICONTROL Target Status] | De status van een dynamisch zoekdoel: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande doelen). De standaardwaarde voor nieuwe doelen is [!UICONTROL Active] . Voer de waarde `Deleted` in om een actief of gepauzeerd doel te verwijderen. |
| [!UICONTROL Sitelink Status] | De weergavestatus van de sitelink: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande sitelinks). De standaardwaarde voor nieuwe sitelinks is [!UICONTROL Active] . Voer de waarde `Deleted` in om een actieve sitelink te verwijderen. |
| [!UICONTROL Location Status] | De status van het doel van de locatie: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande locaties). De standaardwaarde voor nieuwe locaties is [!UICONTROL Active] . Voer de waarde `Deleted` in om een actieve locatie te verwijderen. |
| [!UICONTROL Product Group Status] | De weergavestatus van de productgroep: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande productgroepen). De standaardwaarde voor nieuwe productgroepen is [!UICONTROL Active] . Voer de waarde `Deleted` in om een actieve productgroep te verwijderen. |
| [!UICONTROL Device Target Status] | De status van het apparaatdoel op campagne- of advertentieniveau: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i> . Voor nieuwe campagnes en advertentiegroepen is de standaardwaarde [!UICONTROL Active] . |
| [!UICONTROL RLSA Target Status] | De status van het RLSA-doel op campagne- of advertentieniveau of (alleen Google Ads)-uitsluiting: <i>[!UICONTROL Active]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande doelen). De standaardwaarde voor nieuwe doelen of uitsluitingen is [!UICONTROL Active] . Voer de waarde `Deleted` in om een actief doel of een actieve uitsluiting te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | (Benoemd voor een advertentiespecifieke labelclassificatie, zoals &quot;Kleur&quot; voor een labelclassificatie genaamd Kleur) Een waarde voor de opgegeven classificatie die aan de entiteit is gekoppeld. U kunt per entiteit slechts één waarde per classificatie opnemen (zoals &quot;rood&quot; voor de labelclassificatie &quot;Kleur&quot; voor campagne A). De maximumlengte is 100 tekens en de waarde kan ASCII- en niet-ASCII-tekens bevatten.<br><br> de classificaties van het Etiket en hun etiketwaarden worden toegepast op alle kindcomponenten; de nieuwe componenten die later worden toegevoegd worden automatisch geassocieerd met het etiket. De etiketclassificaties voor productgroepen worden toegepast op het eenheidniveau (het meest korrelige).<br><br> Noch is de classificatienaam noch de classificatiewaarde case-sensitive. |
| [!UICONTROL Constraints] | Een beperking die aan de entiteit is toegewezen. U kunt slechts één beperking per entiteit toewijzen.<br><b>>Beperkingen worden overgeërfd door onderliggende entiteiten, zodat u geen waarden voor onderliggende entiteiten hoeft in te voeren, tenzij u de overgeërfde waarden wilt overschrijven. |
| [!UICONTROL Campaign ID] | De unieke id die een bestaande campagne identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u de campagnenaam verandert, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor de campagne omvat. |
| [!UICONTROL Ad Group ID] | De unieke id die een bestaande advertentiegroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u de campagnenaam verandert, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor de advertentiegroep omvat. |
| [!UICONTROL Placement ID] | Vervangen |
| [!UICONTROL Keyword ID] | De unieke id die een bestaand trefwoord identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u het sleutelwoord verandert, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) &quot; [!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>De unieke id die een bestaande advertentie identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Voor responsieve zoekopdrachten is de id van de advertentie of de AMO-id vereist om advertentiegegevens te bewerken of te verwijderen. Voor alle andere entiteittypes, wordt identiteitskaart van AMO vereist slechts wanneer u de advertentiestatus verandert, tenzij de rij a) voldoende kolommen van het ad bezit omvat om de advertentie of b) te identificeren &quot;[!UICONTROL AMO ID]&quot;. Als u echter noch de kolommen [!UICONTROL Ad ID] noch [!UICONTROL AMO ID] opneemt en de kolommen met de eigenschap ad overeenkomen met meerdere advertenties, verandert de status voor slechts een van de advertenties.</p><p><b> Nota:</b> als u a) en bezitskolommen behalve Status voor een bestaande advertentie of b) om het even welke gegevens voor een ontvankelijke onderzoeksadvertentie uitgeeft, en u omvat noch [!UICONTROL Ad ID] noch [!UICONTROL AMO ID], dan wordt een nieuwe advertentie gecreeerd, en de bestaande advertentie wordt niet veranderd. </p> |
| [!UICONTROL Sitelink ID] | De unieke id die een bestaande sitelink identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u verandert of de sitelink schrapt, tenzij de rij a) voldoende bezitskolommen omvat om sitelink of b) te identificeren &quot;[!UICONTROL AMO ID]&quot;. Als u echter geen [!UICONTROL Sitelink ID] of [!UICONTROL AMO ID] opneemt en de eigenschapskolommen overeenkomen met meerdere sitelinks, verandert de status voor slechts een van de sitelinks.</p><p><b> Nota:</b> als u sitelink bezitskolommen behalve Status voor bestaande sitelink uitgeeft, en u noch [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID] omvat, dan wordt een nieuwe sitelink gecreeerd, en bestaande sitelink wordt niet veranderd. |
| [!UICONTROL Product Group ID] | De unieke id die een bestaande productgroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u verandert of de productgroep schrapt, tenzij de rij a) voldoende bezitskolommen omvat om de productgroep te identificeren of b) &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| Locatie-id | De unieke [!DNL Microsoft Advertising] -id voor het doel van de locatie. Als u een locatielijst wilt downloaden, meldt u zich aan bij de [!DNL Microsoft Advertising] -ontwikkelaarportal met de referenties van uw [!DNL Microsoft Advertising] -advertentieaccount. Vereist slechts wanneer u verandert of het plaatsdoel schrapt, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor het doel omvat. |
| [!UICONTROL Target ID] | De unieke id die een bestaand automatisch doel identificeert. Vereist slechts wanneer u verandert of het autodoel schrapt, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor het doel omvat. |
| [!UICONTROL RLSA Target ID] | De unieke id die een bestaand RLSA-doel op campagne- of advertentieniveau identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u het doel of de uitsluiting verandert of schrapt, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor het doel omvat. |
| [!UICONTROL AMO ID] | (In gegenereerde bulksbladen) Een door Adobe gegenereerde unieke id voor een gesynchroniseerde entiteit. Voor responsieve zoekopdrachten is de AMO-id vereist om advertenties te bewerken of te verwijderen, tenzij u de advertentie-id opneemt. Als u gegevens voor alle andere entiteitstypen met een AMO-id wilt bewerken, moet de AMO-id de gegevens bewerken of verwijderen, tenzij u de id van de entiteit en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |
| [!UICONTROL EF Error Message] | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van het advertentienetwerk met betrekking tot gegevens in de rij; foutberichten worden opgenomen in [!UICONTROL EF Errors] -bestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| [!UICONTROL SE Error Message] | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van het advertentienetwerk met betrekking tot gegevens in de rij; foutberichten worden opgenomen in [!UICONTROL SE Errors] -bestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| [!UICONTROL Exemption Request] | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van de namen en tekst van alle Google-advertentiebeleidsregels die een advertentie schendt. |
| [!UICONTROL Retail Hash] | (Ter informatie opgenomen in bulksbladen die zijn gegenereerd met Advanced Campaign Management) Een alfanumerieke hash-code (zoals f9639f40cdf56524b541e5dacf55a991) die aangeeft dat het item is gegenereerd met de weergave Geavanceerd (ACM). |

[^1 ]: [!DNL Excel] zet grote aantallen in wetenschappelijke aantekening (zoals 2.12E+09 voor 2115585666) om wanneer het dossier opent. Als u cijfers in de standaardnotatie wilt weergeven, selecteert u een willekeurige cel in de kolom en klikt u in de formulebalk.

## Velden vereist voor het maken, bewerken of verwijderen van elk accountonderdeel {#bulksheet-fields-per-component-microsoft}

De volgende secties bevatten de velden die relevant zijn voor specifieke rekeningentiteiten.

>[!NOTE]
>
>Wanneer een veld niet van toepassing is op een handeling, wordt een waarde die in het veld is ingevoerd, genegeerd.

### Campagnevelden

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist. De unieke naam die een campagne voor een account identificeert. |
| [!UICONTROL Campaign Budget] | Vereist om een campagne te maken. Een dagelijkse uitgavenlimiet voor de campagne, met of zonder monetaire symbolen en leestekens. Deze waarde overschrijft, maar kan het budget van de account niet overschrijden. |
| [!UICONTROL Channel Type] | Vereist om een campagne te maken. |
| [!UICONTROL Delivery Method] | Optioneel |
| [!UICONTROL Campaign Priority] | Vereist voor het maken van een winkelcampagne. |
| [!UICONTROL Merchant ID] | Vereist voor het maken van een winkelcampagne. |
| [!UICONTROL Sales Country] | Vereist voor het maken van een winkelcampagne. |
| [!UICONTROL Product Scope Filter] | (Winkelcampagnes) Optioneel |
| [!UICONTROL DSA Domain Name] | Vereist om een campagne van type a) &quot;[!UICONTROL DynamicSearchAds]&quot;of b) &quot; [!UICONTROL Search]&quot;tot stand te brengen wanneer het [!DNL ExperimentId] element niet wordt geplaatst) |
| [!UICONTROL DSA Domain Language] | Vereist om een campagne van type a) &quot;[!UICONTROL DynamicSearchAds]&quot;of b) &quot; [!UICONTROL Search]&quot;tot stand te brengen wanneer het [!DNL ExperimentId] element niet wordt geplaatst) |
| [!UICONTROL Tracking Template] | Optioneel |
| [!UICONTROL Landing Page Suffix] | <p>Optioneel |
| [!UICONTROL Budget Type] | Vereist om een campagne te maken. |
| [!UICONTROL Device] | Optioneel |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL Campaign Status] | Alleen vereist om een campagne te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Constraints] | Optioneel |
| [!UICONTROL Campaign ID] | Vereist slechts wanneer u de campagnenaam verandert, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor de campagne omvat. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Groepsvelden toevoegen

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
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
| [!UICONTROL Ad Group ID] | Vereist slechts wanneer u de naam van de advertentiegroep verandert, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor de advertentiegroep omvat. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Trefwoordvelden

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
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
| [!UICONTROL Keyword ID] | Vereist slechts wanneer u het sleutelwoord uitgeeft of schrapt, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) &quot; [!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Dynamisch zoeken en velden

>[!NOTE]
>
>Ondersteuning voor maken is niet beschikbaar.

Gebruik voor dit advertentietype de rij &quot;[!UICONTROL Creative (except RSA)]&quot; in het dialoogvenster [!UICONTROL Download Bulksheet] .

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Vereist om de beschrijving te bewerken. <b> Nota:</b> voor dit advertentietype, schrapt het veranderen en het exemplaar de bestaande advertentie en leidt tot nieuwe. |
| [!UICONTROL Display Path 1] | Vereist om het veld te bewerken. |
| [!UICONTROL Display Path 2] | Vereist om het veld te bewerken. |
| [!UICONTROL Creative Type] | Vereist om de status van een productadvertentie te maken of te bewerken. |
| [!UICONTROL Creative Preferred Devices] | Optioneel |
| [!UICONTROL Ad Status] | Vereist om een advertentie te verwijderen. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel |
| [!UICONTROL Ad ID] | Vereist slechts wanneer u de advertentiestatus verandert, tenzij de rij a&rpar; voldoende en bezitskolommen omvat om de advertentie te identificeren of b&rpar; &quot;[!UICONTROL AMO ID]&quot;. Als u echter noch de kolommen [!UICONTROL Ad ID] noch [!UICONTROL AMO ID] opneemt en de kolommen met de eigenschap ad overeenkomen met meerdere advertenties, verandert de status voor slechts een van de advertenties. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Product (winkelen) en velden

Voor meer informatie over het creëren van het winkelen adverteert, zie &quot;[&#x200B; voert  [!DNL Microsoft Advertising]  het winkelen campagnes &#x200B;](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/microsoft-shopping-campaigns.html?lang=nl-NL) uit.&quot;

Gebruik voor dit advertentietype de rij &quot;[!UICONTROL Creative (except RSA)]&quot; in het dialoogvenster [!UICONTROL Download Bulksheet] .

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
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
| [!UICONTROL Ad ID] | Vereist slechts wanneer u de advertentiestatus verandert, tenzij de rij a) voldoende kolom van het ad-bezit omvat om de advertentie of b) te identificeren &quot;[!UICONTROL AMO ID]&quot;. Als u echter noch de kolommen [!UICONTROL Ad ID] noch [!UICONTROL AMO ID] opneemt en de kolommen met de eigenschap ad overeenkomen met meerdere advertenties, verandert de status voor slechts een van de advertenties. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Responsief (multimedia) en velden

Gebruik voor dit advertentietype de rij &quot;[!UICONTROL Creative (except RSA)]&quot; in het dialoogvenster [!UICONTROL Download Bulksheet] .

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] -[!UICONTROL Ad Title 15] | Voor responsieve advertenties zijn [!UICONTROL Ad Title] , [!UICONTROL Ad Title 2] en [!UICONTROL Ad Title 3] vereist om advertenties te maken. Alle andere titelvelden zijn optioneel. Als u de bestaande waarde voor een niet-vereist veld wilt verwijderen, gebruikt u de waarde `[delete]` (inclusief de haakjes). <b> Nota:</b> voor dit advertentietype, schrapt het veranderen en het exemplaar de bestaande advertentie en leidt tot nieuwe. |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | [!UICONTROL Description Line 1] en [!UICONTROL Description Line 2] zijn vereist om advertenties te maken en [!UICONTROL Description Line 3] en [!UICONTROL Description Line 4] zijn optioneel. <b> Nota:</b> voor dit advertentietype, schrapt het veranderen en het exemplaar de bestaande advertentie en leidt tot nieuwe. |
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
| [!UICONTROL Ad ID] | Vereist slechts wanneer u de advertentiestatus verandert, tenzij de rij a) voldoende kolom van het ad-bezit omvat om de advertentie of b) te identificeren &quot;[!UICONTROL AMO ID]&quot;. Als u echter noch de kolommen [!UICONTROL Ad ID] noch [!UICONTROL AMO ID] opneemt en de kolommen met de eigenschap ad overeenkomen met meerdere advertenties, verandert de status voor slechts een van de advertenties. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Responsieve zoekopdrachten en velden

Gebruik voor dit advertentietype de rij &quot;[!UICONTROL Responsive Search Ad]&quot; in het dialoogvenster [!UICONTROL Download Bulksheet] .

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] -[!UICONTROL Ad Title 15] | Voor responsieve zoekopdrachten zijn [!UICONTROL Ad Title] , [!UICONTROL Ad Title 2] en [!UICONTROL Ad Title 3] vereist om een advertentie te maken. Alle andere titelvelden zijn optioneel. Als u de bestaande waarde voor een niet-vereist veld wilt verwijderen, gebruikt u de waarde `[delete]` (inclusief de haakjes). |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | Optioneel |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | Voor responsieve zoekadvertenties zijn [!UICONTROL Description Line 1] en [!UICONTROL Description Line 2] vereist om een advertentie te maken en zijn [!UICONTROL Description Line 3] en [!UICONTROL Description Line 4] optioneel. Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (inclusief de vierkante haakjes). |
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
| [!UICONTROL Ad ID] | Vereist om advertenties uit te geven of te schrappen tenzij de rij &quot;[!UICONTROL AMO ID]&quot;omvat. |
| [!UICONTROL AMO ID] | Je moet advertenties bewerken of verwijderen, tenzij je de advertentie-id opneemt. |

### Tekst en velden

Gebruik voor dit advertentietype de rij &quot;[!UICONTROL Creative (except RSA)]&quot; in het dialoogvenster [!UICONTROL Download Bulksheet] .

>[!NOTE]
>
>Uitgebreide tekstadvertenties zijn vervangen. U kunt alleen bestaande tekstadvertenties verwijderen.

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2] -[!UICONTROL Ad Title 3] | Alleen-lezen |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | Alleen-lezen |
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
| [!UICONTROL Ad ID] | Vereist slechts wanneer u de advertentiestatus verandert, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;omvat. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de advertentie-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Dynamische doelvelden (automatisch doel) voor zoeken

>[!NOTE]
>
>Ondersteuning voor maken is niet beschikbaar.

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
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
| [!UICONTROL Target ID] | Vereist slechts wanneer u verandert of het autodoel schrapt, tenzij de rij &quot;[!UICONTROL AMO ID]&quot;voor het doel omvat. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Velden voor productgroepen kopen

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
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
| [!UICONTROL Product Group ID] | Vereist slechts wanneer u verandert of de productgroep schrapt, tenzij de rij a) voldoende bezitskolommen omvat om de productgroep te identificeren of b) &quot; [!UICONTROL AMO ID]&quot;. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Sitemeelinktvelden op campagnereniveau

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
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
| [!UICONTROL Sitelink ID] | Vereist slechts wanneer u de sitelink verandert of schrapt, tenzij de rij a) voldoende bezitskolommen omvat om sitelink of b) te identificeren &quot;[!UICONTROL AMO ID]&quot;. Als u echter geen [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID] opneemt en de eigenschapskolommen overeenkomen met meerdere sitelinks, verandert de status voor slechts een van de sitelinks.<br><br><b> Nota:</b> als u sitelink bezitskolommen behalve Status voor bestaande sitelink uitgeeft, en u of [!UICONTROL Sitelink ID] noch [!UICONTROL AMO ID] omvat, dan wordt een nieuwe sitelink gecreeerd, en bestaande sitelink wordt niet veranderd. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de entiteit-id en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Locatiedoelvelden

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Location] | Vereist |
| [!UICONTROL Location Type] | Vereist om een doel te maken |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL Location Status] | Alleen vereist om een locatiedoel te verwijderen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de campagne-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### Apparaatdoelvelden op campagnereniveau en op ad-groepniveau

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Device] | Vereist om een apparaatdoel te verwijderen. |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL Ad Group Name] | Vereist voor apparaatdoelen op ad-groepsniveau. Niet van toepassing op apparaatdoelen op campagneniveau. |
| [!UICONTROL Device Target Status] | Alleen vereist om een apparaatdoel te verwijderen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel; alleen van toepassing op ad-group-apparaatdoelen. |
| [!UICONTROL AMO ID] | Vereist om de gegevens te bewerken of te verwijderen, tenzij u de apparaatdoel-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |

### De doelgebieden van RLSA van het campagne-niveau en van het ad groep

Voor een beschrijving van elk gegevensgebied, zie &quot;[&#x200B; Alle beschikbare gegevensgebieden &#x200B;](#bulksheet-fields-all-microsoft).&quot;

| Veld | Vereist? |
| ---- | ---- |
| [!UICONTROL Acct Name] | Vereist tenzij elke rij &quot;[!UICONTROL AMO ID]&quot;voor de entiteit omvat. |
| [!UICONTROL Campaign Name] | Vereist |
| [!UICONTROL Ad Group Name] | Vereist voor doelen op groepsniveau. Niet van toepassing op streefcijfers op campagneniveau. |
| [!UICONTROL Audience] | Vereist om een nieuw doel te creëren. |
| [!UICONTROL Target Type] | Optioneel |
| [!UICONTROL Bid Adjustment] | Optioneel |
| [!UICONTROL RLSA Target Status] | Vereist om een doel te schrappen. |
| [!UICONTROL Campaign ID] | Optioneel |
| [!UICONTROL Ad Group ID] | Optioneel; alleen van toepassing op streefcijfers op ad-groepsniveau. |
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
