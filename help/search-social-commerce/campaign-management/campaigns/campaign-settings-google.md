---
title: '[!DNL Google Ads] campagne-instellingen'
description: Verwijs de montages voor  [!DNL Google Ads]  campagnes.
exl-id: 19973286-b7c8-496e-8b87-767cda6e3542
feature: Search Campaign Management
source-git-commit: c1085fe1b065cef95beabba2cb2ea391bd7ef3e8
workflow-type: tm+mt
source-wordcount: '2582'
ht-degree: 0%

---

# [!DNL Google Ads] campagne-instellingen

## \[Scherm Campagne maken\]

**[!UICONTROL Campaign Type]:** (Alleen beschikbaar tijdens het maken van campagnes) Waar u advertenties wilt plaatsen en welke soorten advertenties de campagne kan bevatten:

* *[!UICONTROL Search Network Only]:* toont advertenties op het onderzoeksnetwerk, dat [!DNL Google] onderzoeksresultaten en, naar keuze, onderzoekspartsites omvat. U moet trefwoorden opgeven voor elke advertentiegroep.

* *[!UICONTROL Search with Display Select]:* toont advertenties op het onderzoeksnetwerk (dat [!DNL Google] onderzoeksresultaten en, naar keuze, onderzoekspartsites omvat) en toont potentieel advertenties op de plaatsen van het vertoningsnetwerk. Op het weergavenetwerk geeft [!DNL Google Ads] uw advertenties selectief weer met automatische biedingen, ongeacht de biedstrategie van de campagne. Geef voor zoekadvertenties trefwoorden op voor elke advertentiegroep. Geef voor weergaveadvertenties plaatsingen op en geef desgewenst trefwoorden op voor elke advertentiegroep.

* *[!UICONTROL Shopping Network]:* toont productadvertenties, die [!DNL Google] automatisch genereert op basis van uw producten in [!DNL Google Merchant Center] on [!DNL Google Shopping] , het gebied naast [!DNL Google] zoekresultaten (apart van tekstadvertenties) en (optioneel) zoekpartnerwebsites. Voor elke advertentiegroep in de campagne kunt u productgroepen opgeven die u wilt adverteren.

* *[!UICONTROL Display Network Only]:* toont advertenties op het vertoningsnetwerk. Voor elke advertentiegroep moet u plaatsingen specificeren en kunt naar keuze sleutelwoorden specificeren.

* *[!UICONTROL Performance Max]:* toont en optimaliseert omzettingen voor uw advertenties over kanalen gebruikend [!DNL Google Ads] slimme het bieden. Binnen de instellingen voor de campagne moet u een of meer elementgroepen opgeven, zoals afbeeldingen, logo&#39;s, kopregels, beschrijvingen, optionele video&#39;s en publiekssignalen. [!DNL Google Ads] combineert automatisch de elementen om advertenties te leveren op basis van het kanaal (zoals [!DNL YouTube] , [!DNL Gmail] of [!DNL Search] ).

  **Nota&#39;s:**

   * Alleen de vereiste instellingen zijn beschikbaar. Meld u aan bij de [!DNL Google Ads] -editor voor optionele instellingen.

   * Koppelingen naar [!DNL Google Merchant Center] productfeeds worden niet ondersteund.

   * Ondersteuning voor aanbiedingsgroepen is niet beschikbaar. Meld u aan bij de [!DNL Google Ads] editor om gegevens voor lijstgroepen te beheren en weer te geven.

   * Hybride optimalisatie wordt ondersteund. De doelstellingen van de biedstrategie en de campagnebegrotingen worden vastgesteld op het campagneniveau.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Een campagnenaam die binnen de rekening uniek is.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

**[!UICONTROL Audience Target Method]:** (Bestaande, alleen-lezen Gmail campagnes) Of:

* *[!UICONTROL Target and Bid]* Alleen advertenties weergeven voor gebruikers die zijn gekoppeld aan doelgroepen die ook voldoen aan andere doelen voor de advertentiegroep.

* *[!UICONTROL Bid Only]:* om zelfs advertenties aan mensen te tonen die niet met doelpubliek worden geassocieerd zolang zij andere doelstellingen op het niveau van de ad groep voldoen. U kunt de kans echter vergroten dat advertenties bij een bepaald publiek worden getoond door voor dat publiek hogere biedingen in te stellen.

**[!UICONTROL Status]:** De vertoningsstatus van de campagne: *Actieve* of *Gepauzeerde*. Het gebrek voor nieuwe advertentiecampagnes is *Actief*.

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Search Partners]:** (Campagnes die slechts het onderzoeksnetwerk, met inbegrip van het winkelen campagnes richten) toont uw advertenties op de netwerken van de onderzoekspartner van het advertentienetwerk. Deze optie is standaard ingesteld op *[!UICONTROL Off]* .

**[!UICONTROL AI Max Enabled]:** (Campagnes die slechts het onderzoeksnetwerk richten; read-only) Of de [[!UICONTROL AI Max] eigenschap ](https://support.google.com/google-ads/answer/15910366) wordt toegelaten: *[!UICONTROL On]* of *[!UICONTROL Off]*.

**[!UICONTROL AI Max Bundling]:** (Campagnes die alleen op het zoeknetwerk gericht zijn; campagnes met de AI Max-functie ingeschakeld; alleen-lezen) Of bundeling vereist is: *[!UICONTROL Not Required]*, *[!UICONTROL Required]*, *[!UICONTROL Unknown]* of *[!UICONTROL Unspecified]* .

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

**[!UICONTROL Google Recommended Budget]:** (Optioneel; van toepassing op campagnes met alle vereiste instellingen en alleen voor advertentiegroepen) Klik op **[!UICONTROL Show Recommendation]** om het budget weer te geven dat [!DNL Google Ads] aanbeveelt. Voor complexe campagnes kan het tot 40 seconden duren voordat de aanbeveling wordt gegenereerd.

Voor maximale prestaties en zoekcampagnes zijn de volgende instellingen vereist voor aanbevelingen:

* type biedingsstrategie
* uiteindelijke URL
* middelengroepen

Voor zoekcampagnes zijn ook de volgende aanvullende instellingen vereist voor aanbevelingen:

* streefdoel biedingsstrategie
* land
* taal
* een opgenomen of uitgesloten locatie
* trefwoorden

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** De biedstrategie voor de campagne:

* *[!UICONTROL Enhanced CPC]:* Afgekeurd. [!DNL Google Ads] begon automatisch veranderend bestaande [ verbeterde CPC biedingsstrategieën ](https://support.google.com/google-ads/answer/2464964) aan hand CPC op 15 Maart 2025.

* *[!UICONTROL Manual CPC]* (standaard): (Niet beschikbaar voor maximale prestatiecampagnes) gebruikt het CPC-model (cost per click). U kunt desgewenst toestaan het advertentienetwerk om biedingen voor de campagne te veranderen:

   * **[!UICONTROL Enable Enhanced CPC]** (standaard uitgeschakeld): dit is hetzelfde als het gebruik van de optie &quot;[!UICONTROL Enhanced CPC]&quot;, die is afgekeurd. [!DNL Google Ads] begon automatisch veranderend bestaande [ verbeterde CPC biedingsstrategieën ](https://support.google.com/google-ads/answer/2464964) aan hand CPC op 15 Maart 2025.

* *[!UICONTROL Maximize Clicks]:* (Onderzoek, vertoning, en het winkelen campagnes) het advertentienetwerk — niet Onderzoek, Sociale, &amp; Commerce — optimaliseert biedingen om kliks te maximaliseren. Voer desgewenst een **[!UICONTROL Max CPC]** (kosten per klik) in om ervoor te zorgen dat het advertentienetwerk niet meer betaalt dan een bepaald bedrag voor elke klik. **Voorzichtigheid:** wanneer u een campagne met deze strategie aan een portefeuille toevoegt, worden de biedingen gedreven door klikgewicht, niet door het portefeuilledoel.

* *[!UICONTROL Maximize Conversion Value]:* (Onderzoek, prestaties maximum, en slimme het winkelen campagnes) het advertentienetwerk — niet Onderzoek, Sociale, &amp; Commerce — optimaliseert biedingen om omzetwaarde te maximaliseren. Voer desgewenst een **[!UICONTROL Target Return on Ad Spend]** (ROAS) in als een percentage. **Nota:** gebruik deze optie voor campagnes in hybride portefeuilles maar niet standaardportefeuilles. In hybride portefeuilles, optimaliseert Onderzoek, Sociale, &amp; Commerce het campagne-niveau of (indien beschikbaar) en groep-vlakke ROAS van het Doel.

* *[!UICONTROL Maximize Conversions]:* (Onderzoek, vertoning, en prestaties maximumcampagnes) het advertentienetwerk — niet Onderzoek, Sociale, &amp; Commerce — optimaliseert biedingen om omzettingen te maximaliseren. Voer desgewenst een **[!UICONTROL Target CPA]** (kostprijs per aankoop) in. **Nota:** gebruik deze optie voor campagnes in hybride portefeuilles maar niet standaardportefeuilles. In hybride portefeuilles, optimaliseert het Onderzoek, Sociale, &amp; Commerce campagne-niveau of (indien beschikbaar) en groep-vlakke Doel CPA.

* *[!UICONTROL Target CPA]:* (Weergavecampagnes) Het advertentienetwerk — niet Zoeken, Sociaal, &amp; Commerce — optimaliseert biedingen op basis van een optioneel **[!UICONTROL Target CPA]** (kosten per aankoop). Dit is het gemiddelde bedrag van 30 dagen dat u voor een aankoop (conversie) wilt betalen. **Nota:** gebruik deze optie voor campagnes in hybride portefeuilles (maar niet standaardportefeuilles) met om het even welke uitgavenstrategie behalve [!UICONTROL Weekly] of [!UICONTROL Google Target CPA]. In hybride portefeuilles, optimaliseert het Onderzoek, Sociale, &amp; Commerce campagne-niveau of (indien beschikbaar) en groep-vlakke Doel CPA.

  Gemiddelde positie en CPC-biedgegevens zijn niet beschikbaar voor campagnes met deze biedstrategie.

* *[!UICONTROL Target Impression Share]:* (Zoekcampagnes) Het advertentienetwerk — niet Zoeken, Sociaal, &amp; Commerce — optimaliseert biedingen om een doel te bereiken dat de indruk deelt en toevoegt positie. Voer desgewenst een **[!UICONTROL Target Impression Share]** in als een percentage, de **[!UICONTROL Target Ad Position]** en een **[!UICONTROL Max CPC]** (kosten per klik). **Nota:** deze optie wordt niet gesteund in portefeuilles.

* *[!UICONTROL Target Return on Ad Spend]:* (Weergave- en winkelcampagnes) Het advertentienetwerk — niet Zoeken, Sociaal en Commerce — optimaliseert biedingen op basis van een opgegeven **[!UICONTROL Target ROAS]** (rendement op advertentie-uitgaven), opgegeven als een percentage. **Nota:** gebruik deze optie voor campagnes in hybride portefeuilles (maar niet standaardportefeuilles) met om het even welke uitgavenstrategie behalve [!UICONTROL Weekly] of [!UICONTROL Google Target ROAS]. In hybride portefeuilles, optimaliseert Onderzoek, Sociale, &amp; Commerce het campagne-niveau of (indien beschikbaar) en groep-vlakke ROAS van het Doel.

  Gemiddelde positie en CPC-biedgegevens zijn niet beschikbaar voor campagnes met deze biedstrategie.

* *[!UICONTROL Viewable CPM]:* (Alleen bestaande, alleen-lezen [!DNL Gmail] campagnes) Het advertentienetwerk — niet Zoeken, Sociaal en Commerce — biedt alleen biedingen op advertenties die zijn gemeten als zichtbaar. **Nota:** De optimalisering voor deze strategie wordt niet gesteund in om het even welk type van portefeuille.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Alleen winkelcampagnes; alleen-lezen voor bestaande campagnes) Het land waarin
de producten van de campagne worden verkocht . Omdat de producten met doellanden worden geassocieerd, bepaalt dit het plaatsen welke producten in de campagne worden geadverteerd.

<!-- **[!UICONTROL Campaign Priority]:** -->

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Local Inventory Ads]:** (Alleen winkelcampagnes; adverteerders die al deelnemen aan het lokale winkelprogramma met [!DNL Google Merchant Center] winkels in de VS, het VK, DE, FR, JP en AU; optioneel) [!DNL Google Ads] staat toe om automatisch uw lokale inventarisgegevens toe te voegen aan uw winkeladvertenties op Google.com.

**Uiteinde:** als u dit het plaatsen gebruikt, sluit geen lokale advertenties in het [!UICONTROL Inventory Filter] plaatsen uit.

**Nota:** Lokale inventarisadvertenties vereisen twee extra voer aan [!DNL Google Merchant Center] - met uw lokale productgegevens en een andere met uw lokale productinventaris. Zie de [!DNL Google Ads] documentatie voor meer informatie over [ lokale het winkelen advertenties ](https://www.google.com/retail/local-inventory-ads/).

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Onderzoek en vertoningsnetwerken slechts) Één of meerdere doeltalen voor advertenties in de campagne.

[!DNL Google Ads] bepaalt de taal van een gebruiker op basis van de taalinstelling [!DNL Google] van de gebruiker of de taal van de zoekquery, de huidige pagina of onlangs weergegeven pagina&#39;s op de [!DNL Google Display Network] .

**[!UICONTROL Location Targets]:** Specifieke geografische locaties voor gebruikers die moeten worden opgenomen in of uitgesloten als doelen. Standaard zijn alle locaties aangewezen. U kunt gebruikers in om het even welke combinatie plaatsen omvatten en uitsluiten. Uitsluitingen hebben altijd voorrang op insluitingen.

* Selecteer geen locaties om alle locaties als doel in te stellen.

* Specifieke locaties als doel instellen of uitsluiten:

   * (Landen, staten, metropolitane gebieden, of steden) klik **[!UICONTROL Location Target]** (![ Doel van het Doel van de Plaats ](/help/search-social-commerce/assets/location-target.png " het Doel van de Plaats ")) en bepaal de plaats om van de plaatsen te omvatten en uit te sluiten:

      * Om een plaats en zijn kindplaatsen te omvatten, klik eens de aangrenzende cirkel zodat een blauw controleteken (![ omvat ](/help/search-social-commerce/assets/include.png " ")) verschijnt.

      * Om een plaats uit te sluiten, klik tweemaal de aangrenzende cirkel zodat een rood controleteken (![ sluit ](/help/search-social-commerce/assets/exclude.png " uit ")) verschijnt.

      * Als u een locatie wilt uitbreiden naar de subcomponenten (zoals de staten, metropolitane gebieden of steden in de VS), klikt u op de naam van de locatie.

      * Als u naar een locatie wilt zoeken, typt of plakt u ten minste de eerste drie tekens van de locatie in het invoerveld. Klik in de zoekresultaten op **[!UICONTROL Include]** naast een locatie die u wilt opnemen of op **[!UICONTROL Exclude]** naast een locatie die u wilt uitsluiten.

   * (De plaatsen dichtbij een adres; omvatten slechts doelstellingen) klikken **[!UICONTROL Radius Target]** (![ het Doel van het Straal ](/help/search-social-commerce/assets/radius-target.png " van het Doel van de Straal ")), en klikken dan **[!UICONTROL Address]**. Voer het adres en de straal in mijl of kilometers rond het te richten adres in, en klik vervolgens op **[!UICONTROL Add]**.

   * (Plaatsen dichtbij geografische coördinaten; omvat slechts doelstellingen) klik **[!UICONTROL Radius Target]** (![ het Doel van het Straal ](/help/search-social-commerce/assets/radius-target.png " van het Doel van de Straal ")), en klik dan **[!UICONTROL Coordinate]**. Voer de breedte en lengte en de straal in mijl of kilometers rond de te richten locatie in en klik op **[!UICONTROL Add]** .

* (Voer een waarde voor de bodaanpassing in voor een opgenomen doellocatie.)

* 0%: als u de biedingen voor advertenties op deze locatie niet wilt aanpassen.

* \[Overige waarden van -90% tot 300%\]: het bod voor advertenties op deze locatie verhogen of verlagen.

**Nota:**

* Zoeken, Sociaal en Commerce biedt geen automatische correcties voor biedingen voor de volgende locatiedoelen vanwege beperkingen in de gegevens die [!DNL Google Ads] biedt voor het toewijzen van overboekingslocaties aan locatiedoelen:

   * Straal

   * Sommige locaties onder het niveau van de staat/provincie/regio/provincie/prefectuur waarvoor [!DNL Google Ads] geen bovenliggende locatie in de URL van de surfer verzendt, inclusief luchthavens en congresdistricten van de VS.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL Advanced Device Options]

**[!UICONTROL Mobile Carriers]:** (Alleen netwerk weergeven) Specifieke mobiele carriers die u wilt gebruiken; de dragers worden gesorteerd
per land. Als u niets selecteert, worden alle doelgroepen gebruikt.

**[!UICONTROL Mobile Carriers]:** (Alleen netwerk weergeven) Specifieke besturingssystemen die als doel moeten worden ingesteld. Als u niets selecteert, worden alle doelgroepen gebruikt.

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

## [!UICONTROL Customer Acquisition Goals]

**[!UICONTROL Customer Acquisition]:** (De maximum en onderzoekscampagnes van Prestaties slechts) hoe te om biedingen voor nieuwe klanten en bestaande klanten toe te wijzen:

* *[!UICONTROL Bid equally for new and existing customers]*

* *[!UICONTROL Bid higher for new customers than for existing customers]*

  **Nota:** om dit het plaatsen te gebruiken, moet u het nieuwe doel van de klantenverwerving voor de [!DNL Google Ads] rekening of, indien van toepassing, voor de managerrekening eerst activeren. Het doel bepaalt de in aanmerking komende bestaande klantenlijsten en de extra omzettingswaarde voor nieuwe klanten in de omzettingsmontages. Zie Stappen 1-2 in de [!DNL Google Ads] hulp &quot;[ activeert het nieuwe doel van de klantenverwerving ](https://support.google.com/google-ads/answer/14007601).&quot;

* *[!UICONTROL Only bid for new customers]*

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

**[!UICONTROL Track Product Group]:** (alleen voor [!UICONTROL EF Redirect] ) Niet geïmplementeerd

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (per elementgroep)

**[!UICONTROL Asset Group Name]:** De naam van de elementgroep. Koppelingen naar [!DNL Google Merchant Center] productfeeds worden niet ondersteund.

**[!UICONTROL Asset Group Status]:** De status van de elementgroep: *[!UICONTROL Active]* of *[!UICONTROL Paused]* .

**[!UICONTROL Final URL]:** De laatste URL voor alle advertenties die zijn gemaakt op basis van de elementgroep. <!-- For campaigns created within Search, Social, & Commerce, final URL expansion is automatically enabled for the campaign, and Google Ads replaces this value with a more relevant landing page based on the user's search query and intent, and also customizes the headline based on the landing page content. You can disable final URL expansion, or exclude specific URLs from expansion, from within the [!DNL Google Ads] editor. -->

**[!UICONTROL Images]:** Tot 15 afbeeldingen voor de advertentie, waaronder de volgende formaten: 1) ten minste drie vierkante afbeeldingen, 2) ten minste drie liggende afbeeldingen en 3) ten minste één staande afbeelding. Zie de [[!DNL Google Ads]  beeldspecificaties ](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). U kunt afbeeldingen uploaden of ze selecteren vanuit uw [!UICONTROL Asset Library] , maar niet in beide bewerkingen.

* Afbeeldingen uploaden:

   1. Klik op het tabblad [!UICONTROL Upload from Device] op **[!UICONTROL +]** en selecteer afbeeldingen van uw apparaat of netwerk.

   1. Voor elke afbeelding:

      1. Selecteer de hoogte-breedteverhouding.

      1. Sleep het uitsnijdvak naar de gewenste plaats om het zichtbare gedeelte van de afbeelding te selecteren en wijzig zo nodig de grootte van het zichtbare gedeelte van de afbeelding.

      1. (Optioneel) Selecteer aanvullende hoogte-breedteverhoudingen en wijzig desgewenst de positie en de grootte van de afbeelding voor elke geselecteerde hoogte-breedteverhouding.

         Er wordt één element gemaakt voor elke geselecteerde hoogte-breedteverhouding.

      1. Klik op **[!UICONTROL Proceed]**.

   1. Wanneer u klaar bent met het opgeven van afbeeldingen, klikt u op **[!UICONTROL Upload]** .

* Als u afbeeldingen in uw [!UICONTROL Asset Library] wilt selecteren, klikt u op **[!UICONTROL Asset Library]** en selecteert u de afbeeldingen.

**[!UICONTROL Logos]:** minstens één vierkant (1 :1) embleem en één landschaps (4 :1) embleem. U kunt maximaal vijf van elke grootte opnemen. Zie de [[!DNL Google Ads]  logospecificaties ](https://support.google.com/google-ads/answer/10724492?hl=en&ref_topic=10631992#zippy=,audience-signal-inputs,video-specifications,image-specifications). U kunt afbeeldingen uploaden of ze selecteren vanuit uw [!UICONTROL Asset Library] , maar niet in beide bewerkingen.

* Afbeeldingen uploaden:

   1. Klik op het tabblad [!UICONTROL Upload from Device] op **[!UICONTROL +]** en selecteer afbeeldingen van uw apparaat of netwerk.

   1. Voor elke afbeelding:

      1. Selecteer de hoogte-breedteverhouding.

      1. Sleep het uitsnijdvak naar de gewenste plaats om het zichtbare gedeelte van de afbeelding te selecteren en wijzig zo nodig de grootte van het zichtbare gedeelte van de afbeelding.

      1. (Optioneel) Selecteer aanvullende hoogte-breedteverhoudingen en wijzig desgewenst de positie en de grootte van de afbeelding voor elke geselecteerde hoogte-breedteverhouding.

         Er wordt één element gemaakt voor elke geselecteerde hoogte-breedteverhouding.

      1. Klik op **[!UICONTROL Proceed]**.

   1. Wanneer u klaar bent met het opgeven van afbeeldingen, klikt u op **[!UICONTROL Upload]** .

* Als u afbeeldingen in uw [!UICONTROL Asset Library] wilt selecteren, klikt u op **[!UICONTROL Asset Library]** en selecteert u de afbeeldingen.

**[!UICONTROL Videos]:** (Optioneel) Ten minste één en maximaal vijf [!DNL YouTube] video&#39;s met een lengte van ten minste 10 seconden. U kunt URL&#39;s invoeren of ze selecteren in uw [!UICONTROL Asset Library] , maar niet in beide bewerkingen.

* URL&#39;s invoeren:

   1. Voer op het tabblad [!UICONTROL Enter Video Url] een URL in.

   1. (Optioneel) Als u nog een URL wilt toevoegen, klikt u op **[!UICONTROL + Add]** en voert u de URL in.

* Als u video&#39;s wilt selecteren in uw [!UICONTROL Asset Library] , klikt u op **[!UICONTROL Asset Library]** en selecteert u de video&#39;s.

**[!UICONTROL Headlines]:** minstens drie, en tot vijf, korte koppen met een maximum van 30 karakters elk. Ten minste één kop moet ten minste 15 tekens lang zijn. Als de optie op campagnereniveau is ingesteld om de uiteindelijke URL-uitbreiding in te schakelen binnen [!DNL Google Ads] , vervangt [!DNL Google Ads] deze waarde door een aangepaste kop op basis van de inhoud van de bestemmingspagina.

U kunt tekst invoeren of elementen selecteren in uw [!UICONTROL Asset Library], maar niet in beide bewerkingen.

* U voert als volgt tekst in:

   1. Voer op het tabblad [!UICONTROL Enter Text] de tekst in.

   1. (Optioneel) Als u nog een tekenreeks wilt toevoegen, klikt u op **[!UICONTROL + Add]** en voert u de tekenreeks in.

* Als u elementen wilt selecteren in uw [!UICONTROL Asset Library] , klikt u op **[!UICONTROL Asset Library]** en selecteert u de elementen.

**[!UICONTROL Long Headlines]:** minstens één, en tot vijf, lange kopregels met een maximum van 90 karakters elk. U kunt tekst invoeren of elementen selecteren in uw [!UICONTROL Asset Library], maar niet in beide bewerkingen.

* U voert als volgt tekst in:

   1. Voer op het tabblad [!UICONTROL Enter Text] de tekst in.

   1. (Optioneel) Als u nog een tekenreeks wilt toevoegen, klikt u op **[!UICONTROL + Add]** en voert u de tekenreeks in.

* Als u elementen wilt selecteren in uw [!UICONTROL Asset Library] , klikt u op **[!UICONTROL Asset Library]** en selecteert u de elementen.

**[!UICONTROL Descriptions]:** minstens twee, en tot vier, beschrijvingen met een maximum van 90 karakters elk. Ten minste één beschrijving moet ten minste 30 tekens lang zijn. U kunt tekst invoeren of elementen selecteren in uw [!UICONTROL Asset Library], maar niet in beide bewerkingen.

* U voert als volgt tekst in:

   1. Voer op het tabblad [!UICONTROL Enter Text] de tekst in.

   1. (Optioneel) Als u nog een tekenreeks wilt toevoegen, klikt u op **[!UICONTROL + Add]** en voert u de tekenreeks in.

* Als u elementen wilt selecteren in uw [!UICONTROL Asset Library] , klikt u op **[!UICONTROL Asset Library]** en selecteert u de elementen.

**[!UICONTROL Call to Action]:** De call to action die in de advertentie moet worden opgenomen. Standaard is *[!UICONTROL Automated]* geselecteerd en selecteert [!DNL Google Ads] de call to action. U kunt desgewenst een andere actie kiezen.

**[!UICONTROL Business Name]:** De bedrijfsnaam, met een maximum van 25 karakters.

**[!UICONTROL Audience Signal]:** (Optioneel) [!DNL Google Ads] publiek dat als publiekssignalen voor de campagne moet worden gebruikt. [!DNL Google Ads] computerleermodellen gebruiken het publiek om vergelijkbare websurfers te vinden die u als doel wilt gebruiken en kunnen ook advertenties aan het publiek tonen die niet als signalen worden opgegeven om u te helpen uw prestatiedoelen te bereiken. Kies het publiek dat het meest waarschijnlijk wordt omgezet.

>[!NOTE]
>De signalen van het publiek zijn verschillend van [ campagne-niveau en ad groep-vlakke publieksdoelstellingen ](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

**[!UICONTROL Primary Status]:** (Alleen-lezen veld voor bestaande elementgroepen in maximale prestatiecampagnes) Waarom de elementengroep op volledige capaciteit wordt of wordt gebruikt. Hierbij wordt rekening gehouden met de status van de activagroep en met andere signalen, zoals beleids- en kwaliteitsgoedkeuringen. De waarden kunnen *IN AANMERKING KOMEND,* *BEPERKT,* *NIET_ELIGIBLE,* *BEHANDELD,* *PENDING,* *VERWIJDERD,* *ONBEKEND,* of *ONBEKEND omvatten.*<!-- GGL also has a Primary Status field for campaigns; if we ever sync that, then we'll need to distinguish between them. -->

**[!UICONTROL Primary Status Reason]:** (Alleen-lezen veld voor bestaande elementgroepen in maximale prestatiecampagnes) Aanvullende informatie over de primaire status van de elementgroep. De waarden kunnen *ASSET_GROUP_DISAPPED,* *ASSET_GROUP_LIMITED,* *ASSET_GROUP_PAUSED,* *ASSET_GROUP_REMOVED,* *ASSET_GROUP_UNDER_REVIEW,* *CAMPAUW omvatten N_ENDED,* *CAMPAIGN_PAUSED,* *CAMPAIGN_PENDING,* *CAMPAIGN_REMOVED,* *ONBEKEND,* of *NIET GESPECIFICEERD.*}

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Of *[!UICONTROL Use account conversion goals for this campaign]* (de standaardwaarde) of *[!UICONTROL Use campaign specific conversion goals]*. Als u ervoor kiest om omzettingsdoelstellingen voor de campagne te specificeren, dan uitgezochte standaarddoelstellingen en/of creeer een douanedoel voor de campagne.

De doelstellingen worden gesynchroniseerd dagelijks, zodat kunnen de bestaande doelstellingen die in de vorige 24 uren worden gecreeerd niet worden vermeld. Om de lijst bij te werken, [ synchroniseert manueel de gegevens van het advertentienetwerk ](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Om een doel van de douaneomzetting tot stand te brengen, klik **[!UICONTROL + Add custom goal]**, ga de naam van het douanedoel in, selecteer de [ omzettingsacties ](https://support.google.com/google-ads/answer/6032150) om in het douanedoel te omvatten, en klik dan **[!UICONTROL Save]**. **Nota:** Elke campagne kan slechts één douanedoel hebben.

>[!TIP]
>
>Als de campagne deel uitmaakt van een hybride portfolio, kunt u het beste campagnedoelen gebruiken die overeenkomen met de conversiedoelstellingen in de doelstelling van de portfolio. Het opnemen van aanvullende conversiedoelstellingen kan van invloed zijn op de prestaties van het portfolio.
>
>Nochtans, voor campagnes in hybride portefeuilles waarvoor u [ doelstellingen aan het advertentienetwerk ](/help/search-social-commerce/tools/objective-upload-to-networks.md) uploadt, doe het volgende binnen de redacteur van het advertentienetwerk in plaats van hier: a) voeg het geuploade Onderzoek toe, Sociale, &amp; de portefeuilledoelstelling van Commerce (die met &quot;O_ACS_OBJ&quot;begint) als omzettingsactie voor de campagne, en b) voeg om het even welke campagnedoelstellingen toe die [!DNL Google]-gevolgde omzettingen omvatten omdat de netwerk-sporen zijn Niet geüpload naar het advertentienetwerk met het doel.

>[!MORELIKETHIS]
>
>* [ beheert campagnes ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
