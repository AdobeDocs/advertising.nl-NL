---
title: '[!DNL Google Ads] campagne-instellingen'
description: Verwijs naar de instellingen voor [!DNL Google Ads] campagnes.
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: fd5a78a0eb2982ee85ca2d2b6a3cd79a0821d965
workflow-type: tm+mt
source-wordcount: '2424'
ht-degree: 0%

---

# [!DNL Google Ads] campagne-instellingen

## \[Scherm Campagne maken\]

**[!UICONTROL Campaign Type]:** (Alleen beschikbaar tijdens het maken van campagnes) Waar kunt u advertenties plaatsen en welke advertentietypes de campagne kan bevatten:

* *[!UICONTROL Search Network Only]:* Toont advertenties op het onderzoeksnetwerk, dat omvat [!DNL Google] zoekresultaten en, optioneel, zoekpartnersites. U moet trefwoorden opgeven voor elke advertentiegroep.

* *[!UICONTROL Search with Display Select]:* Toont advertenties op het onderzoeksnetwerk (dat omvat [!DNL Google] de onderzoeksresultaten en, naar keuze, de plaatsen van de onderzoekspartner) en tonen potentieel advertenties op de plaatsen van het vertoningsnetwerk. Op het weergavenetwerk [!DNL Google Ads] geeft je advertenties selectief weer met automatische biedingen, ongeacht de biedstrategie van de campagne. Geef voor zoekadvertenties trefwoorden op voor elke advertentiegroep. Geef voor weergaveadvertenties plaatsingen op en geef desgewenst trefwoorden op voor elke advertentiegroep.

* *[!UICONTROL Shopping Network]:* Geeft productadvertenties weer, die [!DNL Google] wordt automatisch gegenereerd op basis van uw producten in [!DNL Google Merchant Center] op [!DNL Google Shopping], het gebied naast [!DNL Google] zoekresultaten (apart van tekstadvertenties) en (optioneel) zoekpartnerwebsites. Voor elke advertentiegroep in de campagne kunt u productgroepen opgeven die u wilt adverteren.

* *[!UICONTROL Display Network Only]:* Toont advertenties op het weergavenetwerk. Voor elke advertentiegroep moet u plaatsingen specificeren en kunt naar keuze sleutelwoorden specificeren.

* *[!UICONTROL Performance Max]:* Hiermee toont en optimaliseert u omzettingen voor uw advertenties via kanalen [!DNL Google Ads] slim bieden. Binnen de instellingen voor de campagne moet u een of meer elementgroepen opgeven, zoals afbeeldingen, logo&#39;s, kopregels, beschrijvingen, optionele video&#39;s en publiekssignalen. [!DNL Google Ads] combineert automatisch de elementen om advertenties te bedienen op basis van het kanaal (zoals [!DNL YouTube], [!DNL Gmail], of [!DNL Search]).

  **Opmerkingen:**

   * Alleen de vereiste instellingen zijn beschikbaar. Meld u aan bij de [!DNL Google Ads] editor.

   * Koppelingen naar [!DNL Google Merchant Center] productfeeds worden niet ondersteund.

   * Ondersteuning voor aanbiedingsgroepen is niet beschikbaar. Als u gegevens voor aanbiedingsgroepen wilt beheren en weergeven, meldt u zich aan bij de [!DNL Google Ads] editor.

   * Hybride optimalisatie wordt ondersteund. De doelstellingen van de biedstrategie en de campagnebegrotingen worden vastgesteld op het campagneniveau.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Een campagnenaam die uniek is binnen de account.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:**(Alleen bestaande alleen-lezen Gmail-campagnes) Of:

* *[!UICONTROL Target and Bid]* Alleen advertenties weergeven voor gebruikers die zijn gekoppeld aan doelgroepen die ook voldoen aan andere doelen voor de advertentiegroep.

* *[!UICONTROL Bid Only]:*  Advertenties tonen zelfs aan mensen die niet met doelpubliek worden geassocieerd zolang zij andere doelstellingen op groepsniveau voldoen. U kunt de kans echter vergroten dat advertenties bij een bepaald publiek worden getoond door voor dat publiek hogere biedingen in te stellen.

**[!UICONTROL Status]:** De weergavestatus van de campagne: *Actief* of *Gepauzeerd*. De standaardwaarde voor nieuwe advertentiecampagnes is *Actief*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Campagnes die het onderzoeksnetwerk slechts, met inbegrip van het winkelen campagnes richten) toont uw advertenties op de netwerken van de onderzoekspartner van het advertentienetwerk. Deze optie is standaard *[!UICONTROL Off]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** De biedstrategie voor de campagne:

* *[!UICONTROL Enhanced CPC]:* (Niet beschikbaar voor maximale of bestaande prestaties, alleen-lezen [!DNL Gmail] campagnes) Gebruikt het verbeterde kosten-per-klik (eCPC) model van het advertentienetwerk, dat het advertentienetwerk toestaat om de kosten-per-klikbod (CPC) voor elke veiling automatisch te veranderen in een poging om omzettingen te maximaliseren, gebruikend omzetting(en) binnen het advertentienetwerk (niet in Onderzoek, Sociale, &amp; Commerce), terwijl het proberen om uw gemiddelde CPC onder uw maximum te houden.

Wanneer u een campagne met eCPC toevoegt aan een geoptimaliseerde portefeuille van Zoeken, Sociale, &amp; Commerce, optimaliseert het Onderzoek, Sociale, &amp; Commerce de basisbiedingen en — wanneer &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; optie is ingeschakeld — het campagnebudget. Het advertentienetwerk optimaliseert alle biedingsaanpassingen en kan de door Zoeken, Sociale en Commerce gegenereerde biedingen wijzigen op het moment van de gebruikersquery op basis van eigen gegevens en inzichten. **Let op:** Gebruik eCPC-campagnes alleen in portfolio&#39;s wanneer de totale conversies die op het advertentienetwerk worden bijgehouden, overeenkomen met de portfoliodoelstelling. <!-- Note to self: Within the ad network UI, you specify conversion goals either a) all conversion actions you've set to be included in "Conversions" at the account level or b) one or more individual conversions to use for optimization -->

* *[!UICONTROL Manual CPC]* (standaard): (Niet beschikbaar voor maximale prestatiecampagnes) Gebruikt het CPC-model (cost per click). U kunt desgewenst toestaan het advertentienetwerk om biedingen voor de campagne te veranderen:

   * **[!UICONTROL Enable Enhanced CPC]** (standaard uitgeschakeld): dit is hetzelfde als het gebruik van &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Maximize Clicks]:* (Zoeken, weergeven en winkelen) Het advertentienetwerk — niet Zoeken, Sociaal en Commerce — optimaliseert biedingen om klikmogelijkheden te maximaliseren. Voer desgewenst een **[!UICONTROL Max CPC]** (kosten per klik) om ervoor te zorgen dat het advertentienetwerk niet meer dan een specifiek bedrag voor elke klik betaalt. **Let op:** Wanneer u een campagne met deze strategie toevoegt aan een portfolio, worden de biedingen bepaald door het gewicht van de klik en niet door het doel van het portfolio.

* *[!UICONTROL Maximize Conversion Value]:* (Zoeken, maximale prestaties en slimme winkelcampagnes) Het advertentienetwerk — niet Zoeken, Sociaal en Commerce — optimaliseert biedingen om de conversiewaarde te maximaliseren. Voer desgewenst een **[!UICONTROL Target Return on Ad Spend]** (ROAS) als een percentage. **Opmerking:** Gebruik deze optie voor campagnes in hybride portefeuilles maar niet standaardportefeuilles.

* *[!UICONTROL Maximize Conversions]:* (Zoek-, weergave- en maximale prestatiecampagnes) Het advertentienetwerk — niet Zoeken, Sociaal en Commerce — optimaliseert biedingen om conversies te maximaliseren. Voer desgewenst een **[!UICONTROL Target CPA]** (kosten per overname). **Opmerking:** Gebruik deze optie voor campagnes in hybride portefeuilles maar niet standaardportefeuilles.

* *[!UICONTROL Target CPA]:* (Weergavecampagnes; bestaande zoekcampagnes) Het advertentienetwerk — niet Zoeken, Sociaal en Commerce — optimaliseert biedingen op basis van een optionele **[!UICONTROL Target CPA]** (kosten per overname), dat is het gemiddelde bedrag van 30 dagen dat u voor een overname (omzetting) wilt betalen. **Opmerking:** Gebruik deze optie voor campagnes in hybride portefeuilles (maar niet standaardportefeuilles) met om het even welke uitgavenstrategie behalve [!UICONTROL Weekly] of [!UICONTROL Google Target CPA].

  Gemiddelde positie en CPC-biedgegevens zijn niet beschikbaar voor campagnes met deze biedstrategie.

  Voor nieuwe zoekcampagnes: [!DNL Google Ads] heeft deze biedstrategie vervangen door [!UICONTROL Maximize Conversions] strategie met behulp van een [!UICONTROL Target CPA] waarde. Voor bestaande zoekcampagnes met deze strategie kunt u alleen de doelwaarde bewerken. Hierdoor verandert de strategie in de [!UICONTROL Maximize Conversions] strategie met behulp van de opgegeven [!UICONTROL Target CPA] waarde.

* *[!UICONTROL Target Impression Share]:* (Zoekcampagnes) Het advertentienetwerk — niet Zoeken, Sociaal, en Commerce — optimaliseert biedingen om een doel te bereiken dat de indruk wordt gedeeld en geplaatst. Voer desgewenst een **[!UICONTROL Target Impression Share]** als een percentage **[!UICONTROL Target Ad Position]** en **[!UICONTROL Max CPC]** (kosten per klik). **Opmerking:** Deze optie wordt niet ondersteund in portfolio&#39;s.

* *[!UICONTROL Target Return on Ad Spend]:*  (Weergeven en winkelen; bestaande zoekcampagnes) Het advertentienetwerk — niet Zoeken, Sociaal en Commerce — optimaliseert biedingen op basis van een opgegeven **[!UICONTROL Target ROAS]** (Retourneren bij advertentie-uitgaven), opgegeven als een percentage. **Opmerking:** Gebruik deze optie voor campagnes in hybride portefeuilles (maar niet standaardportefeuilles) met om het even welke uitgavenstrategie behalve [!UICONTROL Weekly] of [!UICONTROL Google Target ROAS].

  Gemiddelde positie en CPC-biedgegevens zijn niet beschikbaar voor campagnes met deze biedstrategie.

  Voor nieuwe zoekcampagnes: [!DNL Google Ads] heeft deze biedstrategie vervangen door [!UICONTROL Maximize Conversion Value] strategie met behulp van een [!UICONTROL Target Return on Ad Spend value]. Voor bestaande zoekcampagnes met deze strategie kunt u alleen de doelwaarde bewerken. Hierdoor verandert de strategie in de [!UICONTROL Maximize Conversion Value] strategie met behulp van de opgegeven [!UICONTROL Target Return on Ad Spend] waarde.

* *[!UICONTROL Viewable CPM]:* (Bestaand, alleen-lezen) [!DNL Gmail] alleen campagnes) Het advertentienetwerk — niet Zoeken, Sociaal, en Commerce — biedt alleen biedingen op advertenties die zijn gemeten als zichtbaar. **Opmerking:** Optimalisatie voor deze strategie wordt in geen enkel type portfolio ondersteund.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Alleen winkelcampagnes; alleen-lezen voor bestaande campagnes) Het land waar de producten van de campagne worden verkocht. Omdat de producten met doellanden worden geassocieerd, bepaalt dit het plaatsen welke producten in de campagne worden geadverteerd.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Alleen winkelcampagnes; adverteerders nemen al deel aan het lokale winkelprogramma met [!DNL Google Merchant Center] winkels in de VS, het Verenigd Koninkrijk, de, FR, JP en AU; facultatief) staat [!DNL Google Ads] om automatisch uw lokale inventarisgegevens toe te voegen aan uw winkeladvertenties op Google.com.

**Tip:** Als u deze instelling gebruikt, sluit dan lokale advertenties in het dialoogvenster [!UICONTROL Inventory Filter] instellen.

**Opmerking:** Lokale voorraadadvertenties vereisen twee extra feeds aan [!DNL Google Merchant Center] — één met uw lokale productgegevens en een andere met uw lokale productvoorraad. Zie de [!DNL Google Ads] documentatie voor meer informatie over [lokale winkeladvertenties](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Alleen netwerken zoeken en weergeven) Een of meer doeltalen voor advertenties in de campagne.

[!DNL Google Ads] bepaalt de taal van een gebruiker van de gebruiker [!DNL Google] taalinstelling of de taal van de zoekquery, de huidige pagina of onlangs weergegeven pagina&#39;s op de [!DNL Google Display Network].

**[!UICONTROL Location Targets]:** Specifieke geografische locaties van gebruikers die moeten worden opgenomen in of uitgesloten als doelen. Standaard zijn alle locaties aangewezen. U kunt gebruikers in om het even welke combinatie plaatsen omvatten en uitsluiten. Uitsluitingen hebben altijd voorrang op insluitingen.

* Selecteer geen locaties om alle locaties als doel in te stellen.

* Specifieke locaties als doel instellen of uitsluiten:

   * (Landen, staten, metropolitane gebieden of steden) Klik op **[!UICONTROL Location Target]** (![Locatiedoel](/help/search-social-commerce/assets/location-target.png "Locatiedoel")) en zoek de locaties die u wilt opnemen en uitsluiten:

      * Als u een locatie en de onderliggende locaties wilt opnemen, klikt u eenmaal op de aangrenzende cirkel, zodat een blauw vinkje (![Inclusief](/help/search-social-commerce/assets/include.png "Inclusief")) wordt weergegeven.

      * Als u een locatie wilt uitsluiten, klikt u tweemaal op de aangrenzende cirkel, zodat een rood vinkje (![Uitsluiten](/help/search-social-commerce/assets/exclude.png "Uitsluiten")) wordt weergegeven.

      * Als u een locatie wilt uitbreiden naar de subcomponenten (zoals de staten, metropolitane gebieden of steden in de VS), klikt u op de naam van de locatie.

      * Als u naar een locatie wilt zoeken, typt of plakt u ten minste de eerste drie tekens van de locatie in het invoerveld. Klik in de zoekresultaten op **[!UICONTROL Include]** naast een locatie die moet worden opgenomen of **[!UICONTROL Exclude]** naast een locatie die moet worden uitgesloten.

   * (Locaties bij een adres; alleen inbegrepen doelen) Klik **[!UICONTROL Radius Target]** (![Straal](/help/search-social-commerce/assets/radius-target.png "Straal")) en klik vervolgens op **[!UICONTROL Address]**. Ga het adres en de straal in mijl of kilometers rond het te richten adres in, en klik dan **[!UICONTROL Add]**.

   * (Locaties bij geografische coördinaten; alleen inbegrepen doelen) Klik **[!UICONTROL Radius Target]** (![Straal](/help/search-social-commerce/assets/radius-target.png "Straal")) en klik vervolgens op **[!UICONTROL Coordinate]**. Voer de breedte en lengte en de straal in mijl of kilometers rond de te richten locatie in en klik vervolgens op **[!UICONTROL Add]**.

* (Voer een waarde voor de bodaanpassing in voor een opgenomen doellocatie.)

* 0%: als u de biedingen voor advertenties op deze locatie niet wilt aanpassen.

* \[Overige waarden van -90% tot 300%\]: het bod voor advertenties op deze locatie verhogen of verlagen.

**Opmerking:**

* Zoeken, sociaal en Commerce biedt geen automatische correcties voor biedingen voor de volgende locatiedoelen vanwege beperkingen in de gegevens die [!DNL Google Ads] voorziet in het toewijzen van locaties aan locatiedoelen:

   * Straal

   * Enkele locaties onder het niveau van de staat/provincie/regio/provincie/prefectuur waarvoor [!DNL Google Ads] verzendt geen ouderplaats in URL van de surfer, met inbegrip van luchthavens en de districten van het Amerikaanse Congres.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Alleen netwerk weergeven) Specifieke mobiele vervoerders die als doel dienen; de vervoerders worden gesorteerd op land. Als u niets selecteert, worden alle doelgroepen gebruikt.

**[!UICONTROL Mobile Carriers]:** (Alleen netwerk weergeven) Specifieke besturingssystemen waarop u zich wilt richten. Als u niets selecteert, worden alle doelgroepen gebruikt.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

## [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (Voor [!UICONTROL EF Redirect] alleen) Niet geïmplementeerd

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (per elementgroep)

**[!UICONTROL Asset Group Name]:** De naam van de elementgroep. Koppelingen naar [!DNL Google Merchant Center] productfeeds worden niet ondersteund.

**[!UICONTROL Asset Group Status]:** De status van de activagroep: *[!UICONTROL Active]* of *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** De laatste URL voor alle advertenties die zijn gemaakt op basis van de elementgroep. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Tot 15 afbeeldingen voor de advertentie, waaronder de volgende formaten: 1) ten minste drie vierkante afbeeldingen, 2) ten minste drie liggende afbeeldingen en 3) ten minste één staande afbeelding. Zie de [[!DNL Google Ads] afbeeldingsspecificaties](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). U kunt afbeeldingen uploaden of ze selecteren vanuit uw [!UICONTROL Asset Library] — maar niet beide in dezelfde handeling.

* Afbeeldingen uploaden:

   1. Op de [!UICONTROL Upload from Device] tabblad, klikt u op **[!UICONTROL +]** en selecteer afbeeldingen van uw apparaat of netwerk.

   1. Voor elke afbeelding:

      1. Selecteer de hoogte-breedteverhouding.

      1. Sleep het uitsnijdvak naar de gewenste plaats om het zichtbare gedeelte van de afbeelding te selecteren en wijzig zo nodig de grootte van het zichtbare gedeelte van de afbeelding.

      1. (Optioneel) Selecteer aanvullende hoogte-breedteverhoudingen en wijzig desgewenst de positie en de grootte van de afbeelding voor elke geselecteerde hoogte-breedteverhouding.

         Er wordt één element gemaakt voor elke geselecteerde hoogte-breedteverhouding.

      1. Klik op **[!UICONTROL Proceed]**.

   1. Wanneer u klaar bent met het opgeven van afbeeldingen, klikt u op **[!UICONTROL Upload]**.

* Als u afbeeldingen wilt selecteren in uw [!UICONTROL Asset Library], klikt u op **[!UICONTROL Asset Library]** en selecteert u de afbeeldingen.

**[!UICONTROL Logos]:** Ten minste één vierkant (1:1) logo en één landschaps (4:1) logo. U kunt maximaal vijf van elke grootte opnemen. Zie de [[!DNL Google Ads] logo-specificaties](https://support.google.com/google-ads/answer/10724492?hl=en&amp;ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). U kunt afbeeldingen uploaden of ze selecteren vanuit uw [!UICONTROL Asset Library] — maar niet beide in dezelfde handeling.

* Afbeeldingen uploaden:

   1. Op de [!UICONTROL Upload from Device] tabblad, klikt u op **[!UICONTROL +]** en selecteer afbeeldingen van uw apparaat of netwerk.

   1. Voor elke afbeelding:

      1. Selecteer de hoogte-breedteverhouding.

      1. Sleep het uitsnijdvak naar de gewenste plaats om het zichtbare gedeelte van de afbeelding te selecteren en wijzig zo nodig de grootte van het zichtbare gedeelte van de afbeelding.

      1. (Optioneel) Selecteer aanvullende hoogte-breedteverhoudingen en wijzig desgewenst de positie en de grootte van de afbeelding voor elke geselecteerde hoogte-breedteverhouding.

         Er wordt één element gemaakt voor elke geselecteerde hoogte-breedteverhouding.

      1. Klik op **[!UICONTROL Proceed]**.

   1. Wanneer u klaar bent met het opgeven van afbeeldingen, klikt u op **[!UICONTROL Upload]**.

* Als u afbeeldingen wilt selecteren in uw [!UICONTROL Asset Library], klikt u op **[!UICONTROL Asset Library]** en selecteert u de afbeeldingen.

**[!UICONTROL Videos]:** (Optioneel) Ten minste één en ten hoogste vijf, [!DNL YouTube] video&#39;s die minstens 10 seconden lang zijn. U kunt URL&#39;s invoeren of ze selecteren in uw [!UICONTROL Asset Library] — maar niet beide in dezelfde handeling.

* URL&#39;s invoeren:

   1. Op de [!UICONTROL Enter Video Url] voert u een URL in.

   1. (Optioneel) Als u nog een URL wilt toevoegen, klikt u op **[!UICONTROL + Add]** en voer de URL in.

* Om video&#39;s van uw te selecteren [!UICONTROL Asset Library], klikt u op **[!UICONTROL Asset Library]** en selecteer de video&#39;s.

**[!UICONTROL Headlines]:** Minimaal drie en maximaal vijf korte kopregels met elk maximaal 30 tekens. Ten minste één kop moet ten minste 15 tekens lang zijn. Als de optie op campagnereniveau om de uiteindelijke uitbreiding van URL in te schakelen is ingesteld binnen [!DNL Google Ads]vervolgens [!DNL Google Ads] vervangt deze waarde door een aangepaste kop op basis van de inhoud van de bestemmingspagina.

U kunt tekst invoeren of elementen selecteren in uw [!UICONTROL Asset Library] — maar niet beide in dezelfde handeling.

* U voert als volgt tekst in:

   1. Op de [!UICONTROL Enter Text] voert u de tekst in.

   1. (Optioneel) Klik op **[!UICONTROL + Add]** en voer de tekenreeks in.

* Elementen selecteren uit uw [!UICONTROL Asset Library], klikt u op **[!UICONTROL Asset Library]** en selecteert u de elementen.

**[!UICONTROL Long Headlines]:** Minstens één, en tot vijf, lange kopregels met een maximum van 90 karakters elk. U kunt tekst invoeren of elementen selecteren in uw [!UICONTROL Asset Library] — maar niet beide in dezelfde handeling.

* U voert als volgt tekst in:

   1. Op de [!UICONTROL Enter Text] voert u de tekst in.

   1. (Optioneel) Klik op **[!UICONTROL + Add]** en voer de tekenreeks in.

* Elementen selecteren uit uw [!UICONTROL Asset Library], klikt u op **[!UICONTROL Asset Library]** en selecteert u de elementen.

**[!UICONTROL Descriptions]:** Ten minste twee, en maximaal vier, beschrijvingen met elk maximaal 90 tekens. Ten minste één beschrijving moet ten minste 30 tekens lang zijn. U kunt tekst invoeren of elementen selecteren in uw [!UICONTROL Asset Library] — maar niet beide in dezelfde handeling.

* U voert als volgt tekst in:

   1. Op de [!UICONTROL Enter Text] voert u de tekst in.

   1. (Optioneel) Klik op **[!UICONTROL + Add]** en voer de tekenreeks in.

* Elementen selecteren uit uw [!UICONTROL Asset Library], klikt u op **[!UICONTROL Asset Library]** en selecteert u de elementen.

**[!UICONTROL Call to Action]:** De oproep tot actie om op te nemen in de advertentie. Standaard, *[!UICONTROL Automated]* is geselecteerd, en [!DNL Google Ads] Hiermee selecteert u de aanroep van de handeling. U kunt desgewenst een andere actie kiezen.

**[!UICONTROL Business Name]:** De firmanaam, met een maximum van 25 karakters.

**[!UICONTROL Audience Signal]:** (Optioneel) [!DNL Google Ads] publiek dat als publiekssignalen voor de campagne moet worden gebruikt. [!DNL Google Ads] computerleermodellen gebruiken het publiek om gelijkaardige Web surfers aan doel te vinden en kunnen ook advertenties aan publiek tonen die niet als signalen worden gespecificeerd om u te helpen uw prestatiesdoelstellingen ontmoeten. Kies het publiek dat het meest waarschijnlijk wordt omgezet.

>[!NOTE]
>De signalen van het publiek zijn verschillend van [doelgroepen op campagnereniveau en op groepsniveau](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Add new asset group]:** Hiermee kunt u een andere elementgroep opgeven.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Of *[!UICONTROL Use account conversion goals for this campaign]* (de standaardwaarde) of *[!UICONTROL Use campaign specific conversion goals]*. Als u ervoor kiest om omzettingsdoelstellingen voor de campagne te specificeren, dan uitgezochte standaarddoelstellingen en/of creeer een douanedoel voor de campagne.

De doelstellingen worden gesynchroniseerd dagelijks, zodat kunnen de bestaande doelstellingen die in de vorige 24 uren worden gecreeerd niet worden vermeld. Om de lijst bij te werken, [de netwerkgegevens van de advertentie handmatig synchroniseren](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Als u een aangepast conversiedoel wilt maken, klikt u op **[!UICONTROL + Add custom goal]**, voert u de naam van het aangepaste doel in en selecteert u [conversiehandelingen](https://support.google.com/google-ads/answer/6032150) om in het douanedoel te omvatten, en dan te klikken **[!UICONTROL Save]**. **Opmerking:** Elke campagne kan slechts één aangepast doel hebben.

>[!TIP]
>
>Voor campagnes in hybride portefeuilles waarvoor u doelstellingen aan het advertentienetwerk uploadt, is de beste praktijk om campagne-vlakke doelstellingen te gebruiken die de omzettingsdoelstellingen in de doelstelling van de portefeuille aanpassen. Als de campagnedoelstellingen echter [!DNL Google]-tracked omzettingen, dan voeg hen binnen toe [!DNL Google Ads] editor omdat ze niet opnieuw worden geüpload naar het advertentienetwerk met het doel. Daarnaast moet de [!DNL Google Ads] redacteur, verwijder de de omzettingsacties van de campagne als rekening standaarddoelstellingen door hen als secundaire (niet primaire) doelstellingen te merken.

<!-- Check on this:
>If the campaign is part of a hybrid portfolio, then use only conversion goals that are included in the portfolio's objective for the campaign. Including additional conversion goals may impact portfolio performance.
>
>The objective may include conversion goals or other conversions that aren't included for the campaign, but the campaign can't include conversion goals that aren't included in the objective.
-->

>[!MORELIKETHIS]
>
>* [Campagnes beheren](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)

