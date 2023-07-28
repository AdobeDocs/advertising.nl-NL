---
title: Tekst en responsieve zoek- en sjablooninstellingen voor voorraadfeeds
description: Verwijs naar de montages voor tekst en ontvankelijke onderzoek en malplaatjes voor inventarisvoer.
exl-id: ee3956f9-4367-40e4-bdb3-f04a8da9a5f1
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '3317'
ht-degree: 0%

---

# Tekst en responsieve zoek- en sjablooninstellingen voor voorraadfeeds


*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

>[!NOTE]
>
>* De volgende tekens zijn gereserveerd voor het aangeven van kolomnamen en wijzigingsnamen in de sjabloon en zijn daarom niet toegestaan als tekst in alle kenmerkvelden:  `[ ] < > `
>* In [!DNL Yandex templates], kunt u de dynamische parameters gebruiken `{param1}` en `{param2}` alleen in URL&#39;s, en u kunt geen dynamische prijstoevoeging in beschrijvingen van advertenties gebruiken.

## \[Boven alle tabbladen\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Deelvenster Links\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

**[!UICONTROL Map Only]:** (Optioneel) Hiermee kunt u alle nieuwe advertentiegroepen toewijzen (niet beschikbaar voor [!DNL Yandex]), trefwoorden en advertenties aan bestaande campagnes in plaats van campagnes te maken. Selecteer de toewijzingsmethode als u deze optie inschakelt.

Gebruiken [!UICONTROL Map Only] op campagnereniveau is een bestaande accountstructuur vereist die nauw verbonden is met de producttaxonomie en eenvoudig kan worden toegewezen aan de gegevensinvoer .

**[!UICONTROL Map Method]:** (Wanneer [!UICONTROL Map Only] is ingeschakeld voor de campagne) De methode waarmee nieuwe advertentiegroepen (niet beschikbaar voor [!DNL Yandex]), trefwoorden en advertenties worden toegewezen aan bestaande campagnes:

* *[!UICONTROL Contains Anywhere]:* Hiermee worden gegevens toegevoegd aan een bestaande campagne waarvan de naam de opgegeven tekenreeks bevat, als deze bestaat.

* *[!UICONTROL Contains Exactly]:* Hiermee worden gegevens toegevoegd aan een bestaande campagne waarvan de naam de opgegeven tekenreeks bevat, als deze bestaat.

* *[!UICONTROL Exactly Matches]* (standaard): voegt gegevens toe aan een bestaande campagne met dezelfde naam, als deze bestaat.

Wanneer geen gelijke wordt gevonden, worden alle gegevens voor de campagne genegeerd. Als er meerdere overeenkomende campagnes zijn gevonden, worden de trefwoorden en advertenties aan alle toegewezen.

**[!UICONTROL Campaign Tracking Template]:** (Accounts met alleen final/advanced URLs; optioneel) The campagne-level tracking template, that specifies all off-landing domain redirects and tracking parameters and embed the final URL in a parameter. Deze waarde overschrijft de instelling op accountniveau, maar sjablonen bijhouden op meer granulaire niveaus (met trefwoord als meest korrelige) overschrijven deze waarde.

* Voor het bijhouden van Adoben Advertising voor conversie, die wordt toegepast wanneer de instellingen voor de campagne &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel voegt automatisch omleiding en volgende code toe wanneer u sparen het verslag.

* De uiteindelijke URL insluiten:

   * ([!DNL Google Ads] en [!DNL Microsoft® Advertising] alleen) Voor een lijst met parameters die de uiteindelijke URL&#39;s aangeven in trackingsjablonen, raadpleegt u ([!DNL Microsoft® Advertising] alleen) [[!DNL Microsoft® Advertising] documentatie](https://help.ads.microsoft.com/#apex/3/en/56799/2) of ([!DNL Google Ads] alleen) de &quot;Volgsjabloon alleen&quot;-parameters in de sectie &quot;Beschikbaar [!DNL ValueTrack] Parameters&quot; in de [[!DNL Google Ads] documentatie](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] alleen) De parameter gebruiken `!{unescapedurl}` om de URL van de landingspagina aan te geven.

   * U kunt optioneel URL-parameters en aangepaste parameters die zijn gedefinieerd voor de campagne opnemen, gescheiden door en-tekens (&amp;), zoals `{lpurl}?matchtype={matchtype}&device={device}`.

* Voer een waarde in voor omleidingen en bijhouden door derden.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]:** (In [!DNL Google Ads] en [!DNL Yandex] campagne-instellingen) De netwerken waarop advertenties moeten worden geplaatst:

* *[!UICONTROL Search]:* Biedt voor gesponsorde zoekopdrachten.

  ([!DNL Google Ads] campagnes) Biedingen opnemen in aanbiedingen voor [!DNL Google Ads] zoekpartners, schakel het selectievakje in naast **[!UICONTROL Search partners]**.

* *[!UICONTROL Content]:* Biedt voor plaatsingen op (weergave)netwerklijsten met inhoud. **Opmerking:** U kunt geen plaatsingen tot stand brengen gebruikend het malplaatje. Wanneer u deze optie selecteert, maakt u plaatsingen voor elke advertentiegroep en geeft u op welke pagina&#39;s in het weergavenetwerk u als doel voor elke advertentiegroep instelt met behulp van <!-- insert link --> bolletjes of <!-- insert links --> en groepeer en plaatsingsmontages in [!UICONTROL Search] > [!UICONTROL Campaigns] weergaven.

**[!UICONTROL Languages]:** ([!DNL Google Ads] (alleen zoeken en weergeven in netwerken) Een of meer doeltalen voor advertenties in de campagne.

[!DNL Google Ads] bepaalt de taal van een gebruiker van de gebruiker [!DNL Google] taalinstelling of de taal van de zoekquery, de huidige pagina of onlangs weergegeven pagina&#39;s op de [!DNL Google Display Network].

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Alleen accounts met definitieve/geavanceerde URL&#39;s) De sjabloon voor reeksspatiëring op advertentieniveau, die alle parameters voor het omleiden en volgen van domeinen opgeeft en de laatste URL in een parameter insluit.

Voor het bijhouden van Adoben Advertising voor conversie, die wordt toegepast wanneer de instellingen voor de campagne &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel voegt automatisch omleiding en volgende code toe wanneer u sparen het verslag.

Voer een waarde in voor omleidingen en bijhouden door derden. De URL van de landingspagina aangeven:

* Voor Yahoo! Japan Adds-accounts, parameter gebruiken {lpurl}.

* Voor parameters die beschikbaar zijn voor Microsoft® Advertising- en Google Ads-accounts raadpleegt u de [[!DNL Microsoft® Advertising] documentatie](https://help.ads.microsoft.com/#apex/3/en/56799) of de parameters van het &quot;Volgsjabloon slechts&quot;in de sectie over &quot;Beschikbaar [!DNL ValueTrack] Parameters&quot; in de [[!DNL Google Ads] documentatie](https://support.google.com/google-ads/answer/6305348).

Deze waarde negeert de instellingen op account- en campagnereniveau, maar het bijhouden van sjablonen op meer granulaire niveaus (met trefwoord als meest korrelige) overschrijft deze waarde.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]:** Trefwoorden voor de opgegeven advertentiegroep (of campagne voor [!DNL Yandex] accounts), die kunnen bestaan uit een willekeurige combinatie van statische tekst, kolommen in het opgegeven bestand en modifiers. Kolomnamen en modifiers worden vervangen door werkelijke gegevens wanneer het opgegeven voederbestand via de sjabloon wordt doorgegeven.

Als u een kolomnaam of wijzigingengroep wilt invoegen als een dynamische parameter, klikt u in het invoerveld en vervolgens op een kolomnaam in de kolomlijst of een [wijzigingnaam](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) in de lijst Modifiers. Als u meerdere trefwoorden of meerdere overeenkomende typen voor hetzelfde trefwoord wilt opgeven, voert u deze op aparte regels in. Gebruik de volgende syntaxis voor het overeenkomende type met trefwoorden rond de kolomnaam om het overeenkomende type op te geven:

* Voor [!DNL Google Ads], [!DNL Microsoft® Advertising], en [!DNL Yahoo! Japan Ads] sjablonen:

   * Voor dynamische parameters: brede overeenkomst = `[keyword]`, Brede matchmodifier voor de eerste term in de [!UICONTROL Keyword] kolom (bijvoorbeeld +blue suede schoenen) = `+[keyword]`, Brede overeenkomst Modifier voor elke termijn in de kolom van het Sleutelwoord (zoals +blue +suede +schoenen) = `+[keyword]+`, Phrase Match = `"[keyword]"`, Exacte overeenkomst = `[[keyword]]`

   * Voor statische trefwoorden: brede overeenkomst = `keyword`, Brede overeenkomende modifier = `+keyword`, of Phrase Match = `"keyword"`

     U kunt hier geen statische trefwoorden invoeren die exact overeenkomen met de standaard overeenkomende syntaxis omdat ze tussen haakjes staan (`[]`), zoals dynamische parameters.

* Voor [!DNL Yandex] sjablonen:

   * Voor dynamische parameters: voeg de kolomnaam in, zoals `[keyword]`. Als u overeenkomende typen wilt aangeven, gebruikt u de opdracht [[!DNL Yandex]-specifieke syntaxis](https://yandex.com/support/direct/keywords/symbols-and-operators.html). **Opmerking:** Gebruik voor brede overeenkomsten de volgende syntaxis: Brede overeenkomst Modifier voor de eerste term in de kolom Trefwoord (zoals +blue suede schoenen) = `+[keyword]`, Brede overeenkomst Modifier voor elke termijn in de kolom van het Sleutelwoord (zoals +blue +suede +schoenen) = `+[keyword]+`

   * Voor statische trefwoorden: alleen zoektrefwoorden worden ondersteund. Gebruik de [[!DNL Yandex]-specifieke syntaxis](https://yandex.com/support/direct/keywords/symbols-and-operators.html) voor het trefwoord. Haakjes (`[]`) om de woordvolgorde aan te geven, wordt niet ondersteund.

>[!NOTE]
>
>* U kunt handmatig meerdere wijzigingwaarden opnemen in het veld Trefwoorden door met komma&#39;s gescheiden waarden tussen haakjes in te sluiten voor of na een trefwoordparameter (maar niet op beide plaatsen). Bijvoorbeeld: `(cheap, discount, affordable)[product]` produceert drie afzonderlijke advertenties voor elk product.
>* Als u geen overeenkomend type specificeert, dan wordt het standaard gelijke type &quot;breed&quot;gebruikt.
* Negatieve overeenkomsten worden niet ondersteund.
* Google-trefwoorden voor brede overeenkomsten hebben nu hetzelfde gedrag als woordcombinaties die overeenkomen voor bepaalde talen en u kunt geen nieuwe trefwoorden voor brede overeenkomsten maken. Zie de [[!DNL Google Ads] documentatie](https://support.google.com/google-ads/answer/10286719) voor meer informatie .

**[!UICONTROL Map Only]:** Hiermee voegt u nieuwe advertenties toe aan advertentiegroepen (of aan campagnes voor [!DNL Yandex] accounts) waarin de opgegeven trefwoorden worden gevonden, in plaats van nieuwe trefwoorden te maken. Schakel het selectievakje in om deze optie in te schakelen. Wanneer deze optie wordt toegelaten, zijn om het even welk Param 1 en Paragraaf 2 variabelen in de gespecificeerde sleutelwoorden niet van toepassing omdat de sleutelwoorden bestaan.

**[!UICONTROL Keyword Final URL]:** (Accounts met final/advanced URLs; optioneel) De bestemmingspagina-URL waarnaar netwerkgebruikers worden geleid wanneer zij op uw advertentie klikken. De URL moet hetzelfde domein bevatten als de URL van de weergave en alle parameters in de uiteindelijke URL moeten overeenkomen met de parameters in de URL van de bestemmingspagina na de advertentie. Het kan omleidingen binnen het landende paginadomein of subdomain bevatten maar geen omleidingen buiten het landende paginadomein.

Als u een [!DNL Google Merchant Center] Geef deze waarde op in het veld &quot;[!DNL Link]&quot;, en voeg dan die kolom op dit gebied in.

>[!NOTE]
>
* Als u het volgen URLs produceert wanneer u gegevens die door het malplaatje worden verspreid post, worden het volgen parameters toegevoegd aan deze waarde die op de rekening het volgen montages wordt gebaseerd.
* ([!DNL Google Ads] accounts) Vermijd het gebruik van macro&#39;s, die niet worden vervangen door klikken van bronnen die parallelle tracking mogelijk maken. Als de adverteerder macro&#39;s moet gebruiken, moet het Adobe-accountteam samenwerken met Klantenondersteuning of het implementatieteam om deze toe te voegen.

**[!UICONTROL Keyword Tracking Template]:** (Accounts met final/advanced URLs; optional) The tracking template, that specifies all off-landing domain redirects and tracking parameters and embed the final URL in a parameter. De volgende malplaatje op het meest korrelige niveau (met sleutelwoord als meest korrelige) treedt waarden op alle andere niveaus met voeten.

* Voor het bijhouden van Adoben Advertising voor conversie, die wordt toegepast wanneer de instellingen voor de campagne &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel voegt automatisch omleiding en volgende code toe wanneer u sparen het verslag.

* U kunt desgewenst omleidingen en reeksspatiëring van derden invoeren.

* De URL van de landingspagina aangeven:

   * ([!DNL Google Ads] en [!DNL Microsoft® Advertising] alleen) Voor een lijst met parameters die de uiteindelijke URL&#39;s aangeven in trackingsjablonen, raadpleegt u ([!DNL Microsoft® Advertising] alleen) [[!DNL Microsoft® Advertising] documentatie](https://help.ads.microsoft.com/#apex/3/en/56799) of ([!DNL Google Ads] alleen) de &quot;Volgsjabloon alleen&quot;-parameters in de sectie &quot;Beschikbaar [!DNL ValueTrack] Parameters&quot; in de [[!DNL Google Ads] documentatie](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] alleen) De parameter gebruiken `!{lpurl}` om de URL van de landingspagina aan te geven.

**[!UICONTROL Param 1]**, **[!UICONTROL Param 2]\[[!DNL Google Ads] sjablonen\]:** ([!DNL Google Ads] alleen sjablonen) De kolom in het opgegeven bestand die de [!DNL Google Ads] `{param1}` of `{param2}` Deze variabele kunt u in de advertentie opnemen of URL weergeven voor elke advertentie die met de sjabloon is gemaakt. Als u de dynamische parameter wilt invoegen, klikt u in het invoerveld en klikt u op een kolomnaam in de kolomlijst. De kolomnaam wordt vervangen door de werkelijke gegevens wanneer het voederbestand via de sjabloon wordt doorgegeven.

Als u een van beide parameters gebruikt, kunt u de parameter alleen op nieuwe trefwoorden toepassen of de waarden van bestaande trefwoorden bijwerken die niet op basis van de sjabloon zijn gemaakt:

* **[!UICONTROL Do Not Apply to Existing Keywords]** (de standaardwaarde): voegt eenvoudig de waarde van de parameter in voor nieuwe trefwoorden die met de sjabloon worden gemaakt.

* **[!UICONTROL Apply to Existing Keywords: Constant]:** Naast het creëren van nieuwe sleutelwoorden van het voer, werkt het Onderzoek, Sociale, &amp; Handel ook de waarde van de parameter voor alle bestaande sleutelwoorden in de ad groep bij die niet gebruikend het malplaatje werden gecreeerd. Voer één numerieke waarde in die voor al deze trefwoorden wordt gebruikt. De sjabloon moet ten minste één trefwoord bevatten.

* **[!UICONTROL Apply to Existing Keywords: Min]:** Naast het creëren van nieuwe sleutelwoorden van het voer, werkt het Onderzoek, Sociale, &amp; Handel ook de waarde van de parameter voor alle bestaande sleutelwoorden in de ad groep bij die niet gebruikend het malplaatje werden gecreeerd zolang het voederdossier numerieke waarden voor de parameter, met maximaal één decimaalteken maar zonder komma&#39;s, muntsymbolen of codes, of andere karakters bevat. De minimumwaarde voor de parameter in het feed-bestand wordt gebruikt voor alle bestaande trefwoorden. Als het feed-bestand bijvoorbeeld [!UICONTROL Param1] waarden van 21500 en 22000, dan [!UICONTROL Param1] De waarden voor de bestaande trefwoorden worden gewijzigd in 21500. De sjabloon moet ten minste één trefwoord bevatten. **Tip:** Gebruik deze optie alleen als u strak georiënteerde ad-hocgroepen hebt, zodat het logisch is dat trefwoorden dezelfde waarde hebben.

De gegevensvelden in het feed-bestand mogen maximaal 25 tekens hebben en mogen alleen bestaan uit numerieke gegevens met de volgende niet-numerieke tekens:

* (Wanneer u &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot; parameter) Alleen tot één decimaalteken.

* (Wanneer u niet de &quot;[!UICONTROL Apply to Existing Keywords: Min]&quot;parameter):

   * De waarde kan worden voorafgegaan of toegevoegd met een valutasymbool of -code. Zo zijn £ 2.000,00 en GBP 2000 geldig.

   * De waarde kan een komma (,) of punt (.) bevatten als scheidingsteken, met een optionele punt (.) of komma (,) voor fractionele waarden. 1,000,00 en 2,000,10 zijn bijvoorbeeld geldig.

   * De waarde kan worden voorafgegaan of worden toegevoegd met een percentageteken (%), plus-teken (+) of minteken (-). 20%, 208+ en -42,32 zijn bijvoorbeeld geldig.

   * Twee getallen kunnen worden ingesloten met een slash. 4/1 en 0.95/0.45 zijn bijvoorbeeld geldig.

**[!UICONTROL Param 2]\[[!DNL Microsoft® Advertising] sjablonen\]:** ([!DNL Microsoft® Advertising] (alleen sjablonen) De tekenreeks die als vervangingswaarde in een advertentie moet worden gebruikt als de titel, tekst, weergave-URL of laatste URL de waarde `{Param2}` dynamische vervangingsreeks. De maximumlengte is 70 tekens, maar houd rekening met de maximumlengte van het advertentie-element waarin u het element gebruikt (een advertentitel kan bijvoorbeeld maximaal 25 tekens bevatten).

**[!UICONTROL Param 3]:** ([!DNL Microsoft® Advertising] (alleen sjablonen) De tekenreeks die als vervangingswaarde in een advertentie moet worden gebruikt als de titel, tekst, weergave-URL of laatste URL de waarde `{Param3}` dynamische vervangingsreeks. De maximumlengte is 70 tekens, maar houd rekening met de maximumlengte van het advertentie-element waarin u het element gebruikt (een advertentitel kan bijvoorbeeld maximaal 25 tekens bevatten).

**[!UICONTROL Initial Bid (<Match Type or Ad Type>)]:** Het eerste bod voor elk trefwoord met het opgegeven overeenkomende type of advertentietype.

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]:** ([!DNL Google Ads] en [!DNL Microsoft® Advertising] (alleen campagnes) Het type advertenties: *[!UICONTROL Expanded Search Ads]* of *[!UICONTROL Responsive Search Ads]*.

**[!UICONTROL Prefill]:** (Optioneel) Hiermee worden alle alternatieve velden en kopieervelden vooraf gevuld met tekst uit de oorspronkelijke velden en de oorspronkelijke velden.

### [!UICONTROL Headlines]

**[!UICONTROL Pin]:** (Alleen voor responsieve zoekopdrachten) De advertingspositie waar de titel/titel moet worden ingevoegd (bijvoorbeeld &quot;[!UICONTROL Pinned at position 1]&quot;). De standaardwaarde is [!UICONTROL Unpinned].

Voor elke positie moet ten minste één titel beschikbaar zijn. Als u meerdere titels vastzet op dezelfde positie, bevat de laatste en altijd een van deze titels op de opgegeven positie. Titels die op positie 3 zijn vastgezet, worden mogelijk niet met de advertentie weergegeven.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]**, **[!UICONTROL Headline 3]:** (Alleen voor responsieve zoekopdrachten) De titels van de advertentie (koppen). Elke variatie in advertentie moet ten minste drie, en ten hoogste 15, en titels bevatten. Het advertentienetwerk toont advertenties met maximaal drie koppen. De maximumlengte voor elke titel is 30 tekens, inclusief alle dynamische tekst (zoals de waarden van trefwoorden en adverteerders).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]:** (Bestaande Microsoft® Advertising Standard text ads only; read-only) De titel, of eerste regel, van een advertentie. Microsoft® Advertising heeft het maken en bewerken van standaard tekstadvertenties vervangen.

**[!UICONTROL Headline 1]**, **[!UICONTROL Headline 2]:** ([!DNL Google Ads] en [!DNL Yahoo! Japan Ads] (alleen uitgevouwen/uitgebreide tekst en sjablonen) De kop van een advertentie. De maximumlengte voor elke regel (nadat dynamische parameters zijn vervangen) is 30 tekens of 15 double-byte tekens.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]:** ([!DNL Google Ads] alleen uitgevouwen tekst en sjablonen; optioneel) Een derde kopregel voor een advertentie. De maximumlengte (nadat dynamische parameters zijn vervangen) is 30 tekens of 15 double-byte tekens.

**[!UICONTROL Title]:** ([!DNL Yandex] alleen) De titel, of eerste regel, van een advertentie. Het maximum aantal tekens is 33.

**[!UICONTROL Title Part 1]**, **[!UICONTROL Title Part 2]:** (Alleen advertenties in Microsoft® Advertising Uitgebreide text) De kop van een advertentie. De maximumlengte voor elke regel (nadat dynamische parameters zijn vervangen) is 30 tekens of 15 double-byte tekens.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]:** (Alleen advertenties in Microsoft® Advertising Uitgebreide text) De hoofdtekst van een advertentie. De maximumlengte (nadat dynamische parameters zijn vervangen) is 80 tekens of 40 double-byte tekens (zoals Chinees, Japans en Koreaans).

### [!UICONTROL Descriptions]

**[!UICONTROL Description]:** De hoofdtekst van de advertentie.

* (Google voegt uitgebreide tekst en sjablonen toe) De maximumlengte (nadat eventuele dynamische parameters zijn vervangen) is 90 tekens of 45 double-byte tekens.

* (Yahoo!) Sjablonen voor advertenties in Japan) De maximumlengte (nadat dynamische parameters zijn vervangen) is 80 tekens of 40 double-byte tekens.

* (Yandex-sjablonen) De maximumlengte (nadat dynamische parameters zijn vervangen) is 75 tekens en één woord mag niet meer dan 22 tekens bevatten.

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]:** (Alleen voor responsieve zoekopdrachten) De advertingspositie waar de beschrijving moet worden opgenomen (bijvoorbeeld &quot;[!UICONTROL Pinned at position 1]&quot;). De standaardwaarde is [!UICONTROL Unpinned]. Voor elke positie moet ten minste één beschrijving beschikbaar zijn.

Als u meerdere beschrijvingen op dezelfde positie vastzet, wordt in de laatste en altijd een van deze beschrijvingen op de opgegeven positie geplaatst. Beschrijvingen die op positie 2 zijn vastgezet, mogen niet met de advertentie worden getoond.

**[!UICONTROL Description 1]**, **[!UICONTROL Description 2]:** (Alleen responsieve zoekadvertenties) De beschrijvingen van de advertentie. Elke advertentievariatie moet ten minste twee en maximaal vier beschrijvingen bevatten. Het advertentienetwerk toont advertenties met maximaal twee beschrijvingen; ga minstens twee in. De maximale lengte voor elke beschrijving is 90 tekens, inclusief alle dynamische tekst (zoals de waarden van trefwoorden en adverteerders).

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]:** (Google heeft alleen tekst en sjablonen uitgevouwen; optioneel) Een tweede regel van de advertentie. De maximumlengte (nadat dynamische parameters zijn vervangen) is 90 tekens of 45 double-byte tekens.

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Alleen uitgevouwen tekst en responsieve zoekopdrachten; optioneel) Een of twee URL-paden die na de basis-URL worden ingevoegd. Zij zouden het product of de dienst in de advertentie meer in detail moeten beschrijven. Als u bijvoorbeeld een [!UICONTROL Display Path 1] van &quot;Shoes&quot; en [!UICONTROL Display Path 2] van &quot;Outdoor&quot; naar de basis-URL www.example.com, is de URL www.example.com/Shoes/Outdoor. De maximumlengte (nadat dynamische parameters zijn vervangen) voor elk veld is 15 tekens of 7 double-byte tekens.

Voor responsieve zoekadvertenties voegt u een advertentieklanker in met de volgende indelingen, waarbij `Default text` is een optionele waarde die moet worden ingevoegd wanneer uw feed geen geldige waarde bevat:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, zoals `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft® Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, zoals `{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]:** (Bestaande [!DNL Microsoft® Advertising] en [!DNL Yahoo! Japan Ads] alleen standaardtekstadvertenties; alleen-lezen) De URL die in een advertentie wordt weergegeven.

[!DNL Microsoft® Advertising] en [!DNL Yahoo! Japan Ads] hebben het maken en bewerken van standaardtekstadvertenties vervangen.

**[!UICONTROL Base URL]:** (Accounts with destination URLs only) The page to which users are take. Het kan herrichtings- en volgcode van derden bevatten. Als u de service voor het bijhouden van Adoben Advertising voor conversie gebruikt en de instellingen voor de campagne het gebruik van de opdracht [!UICONTROL EF Redirect] en het toevoegen van het volgen op het advertentieniveau, dan voegt het Onderzoek, Sociale, &amp; Handel automatisch zijn eigen redirection en het volgen code aan de advertentie toe.

Als u een kolomnaam of wijzigingengroep wilt invoegen als een dynamische parameter, klikt u in het invoerveld en vervolgens op een kolomnaam in de kolomlijst of een [wijzigingnaam](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) in de [!UICONTROL Modifiers] lijst.

**[!UICONTROL Final URL]:** (Accounts met final/advanced URLs) De bestemmingspagina-URL waarnaar gebruikers worden geleid wanneer zij op uw advertentie klikken. De URL moet hetzelfde domein bevatten als de URL van de weergave en alle parameters in de uiteindelijke URL moeten overeenkomen met de parameters in de URL van de bestemmingspagina na de advertentie. Het kan omleidingen binnen het landende paginadomein of subdomain bevatten maar geen omleidingen buiten het landende paginadomein.

Als u een [!DNL Google Merchant] De feed centreren en deze waarde opnemen in het veld &quot;[!UICONTROL Link]&quot;, en voeg dan die kolom op dit gebied in.

>[!NOTE]
>
* Als u het volgen URLs produceert wanneer u gegevens die door het malplaatje worden verspreid post, dan worden het volgen parameters toegevoegd aan deze waarde die op de rekening het volgen montages wordt gebaseerd.
* ([!DNL Google Ads] accounts ) Gebruik geen macro&#39;s, die niet worden vervangen door klikken op bronnen die parallelle tracking mogelijk maken. Als de adverteerder macro&#39;s moet gebruiken, moet het Adobe Account Team met de Klantenondersteuning of het implementatieteam samenwerken om deze toe te voegen.

**[!UICONTROL Tracking Template]:** (Accounts met final/advanced URLs; optional) The tracking template, that specifies all off-landing domain redirects and tracking parameters and embed the final URL in a parameter. De volgende malplaatje op het meest korrelige niveau (met sleutelwoord als meest korrelige) treedt waarden op alle andere niveaus met voeten.

Voor het bijhouden van Adoben Advertising voor conversie, die wordt toegepast wanneer de instellingen voor de campagne &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel voegt automatisch omleiding en volgende code toe wanneer u sparen het verslag.

Voer een waarde in voor omleidingen en bijhouden door derden. De URL van de landingspagina aangeven:

* Voor Yahoo! Japan Adds-accounts, parameter gebruiken {lpurl}.

* Voor parameters die beschikbaar zijn voor Microsoft® Advertising- en Google Ads-accounts raadpleegt u de [[!DNL Microsoft® Advertising] documentatie](https://help.ads.microsoft.com/#apex/3/en/56799) of de parameters van het &quot;Volgsjabloon slechts&quot;in de sectie over &quot;Beschikbaar [!DNL ValueTrack] Parameters&quot; in de [[!DNL Google Ads] documentatie](https://support.google.com/google-ads/answer/6305348).

**\[Alternatieve advertentievelden onder de oorspronkelijke advertentievelden\]:** (Optioneel) Een alternatieve set advertentiekopieën voor een advertentie, die kan worden gebruikt als een van de regels in het origineel en de kopie de maximaal toegestane lengte overschrijdt zodra dynamische parameters zijn ingevuld met gegevens tijdens de propagatie.

>[!NOTE]
>
* Als de [!UICONTROL Prefill] is geselecteerd, worden de alternatieve velden vooraf ingevuld met de oorspronkelijke velden en kunt u deze naar wens bewerken.
* Alleen de velden voor het kopiëren van de advertentie die de maximale lengte overschrijden, worden vervangen door de alternatieve waarde. Als bijvoorbeeld alleen een oorspronkelijke kop of titel te lang is, gebruiken de gegenereerde en de variatie de alternatieve kop of titel en de oorspronkelijke beschrijvingen. Zorg er daarom voor dat de alternatieve advertentie-kopie zinvol is wanneer deze wordt gecombineerd met het origineel en de kopie.
* Als het origineel en de kopie voldoen aan de lengtevereisten van het zoekprogramma, wordt de alternatieve advertentiekopie verwijderd.

**\[Component\] [!UICONTROL Ad Label Classifications] > \[Classificatie en waarde van label\]:** (Optioneel) Waarden voor maximaal vijf bestaande labelclassificaties die worden toegewezen aan de advertentievariaties die worden gemaakt of bewerkt met de sjabloon. Voor elk campagnecomponent waaraan u etiketclassificaties wilt toewijzen:

1. Klik op het selectievakje.

1. Configureer de waarden voor labelclassificatie voor de sjabloon voor ad-variatie:

   * Ga als volgt te werk voor elke labelclassificatie en -waarde die aan het onderdeel moet worden toegewezen:

      1. Klik op **[!UICONTROL Add Label Classification]**.

      1. Selecteer de bestaande labelclassificatie en selecteer vervolgens een bestaande waarde of voer een nieuwe waarde in.

         De maximumlengte voor elke waarde is 100 tekens en kan ASCII- en niet-ASCII-tekens bevatten.

         Als u een kolomnaam als een dynamische parameter voor een labelclassificatiewaarde wilt invoegen, klikt u in het invoerveld (het tweede veld) en vervolgens op een kolomnaam in de kolomlijst.

         U kunt slechts één waarde per classificatie per campagnecomponent opnemen. Een campagne kan bijvoorbeeld Color=Red hebben, maar niet Color=Red en Color=Blue.

         * Als u een bestaande labelclassificatiewaarde wilt wijzigen, selecteert u of voert u een nieuwe waarde in.

         * Als u een bestaande labelclassificatiewaarde wilt verwijderen, klikt u op **[!UICONTROL X]** naast de waarde.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
* [Informatie over het automatiseren en beheren van voorraden](../inventory-feeds-about.md)
* [Wijzigingstoetsen beheren](../modifiers-manage.md)
* [Invoerbestanden voor inventarisgegevens beheren](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
* [Doorvoergegevens doorgeven via sjablonen](../feed-data-propagate.md)
* [Campagnegegevens van voorraadfeeds aan advertentienetwerken posten](../propagated-data-post.md)
