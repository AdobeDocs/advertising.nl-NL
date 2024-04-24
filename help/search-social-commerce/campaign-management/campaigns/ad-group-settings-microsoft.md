---
title: '[!DNL Microsoft® Advertising] ad group settings'
description: Verwijs naar de instellingen voor [!DNL Microsoft® Advertising] ad groepen.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 2407d29fb4061e6b3181b86c335c52a8384c4ca3
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] groepsinstellingen toevoegen

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Een naam van een advertentiegroep die uniek is in de campagne. De maximumlengte is 128 tekens.

**[!UICONTROL Status]:** De weergavestatus van de advertentiegroep: *Actief* of *Gepauzeerd*. De standaardwaarde voor nieuwe advertentiegroepen is *Actief*.

**[!UICONTROL Ad Language]:** (Zoekcampagnes) De doeltaal voor advertenties.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** (Zoekadvertenties) Hoe en waar u advertenties in de advertentiegroep plaatst:

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! websites]* (de standaardinstelling): Biedingen voor advertenties plaatsen op het zoeknetwerk.

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! syndicated search partners]:* Biedt voor advertenties op gesynchroniseerde partnersites.

* *[!UICONTROL Content network]:* Vervangen

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** Vervangen

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Publiek en groepen) Of:

* *[!UICONTROL Target and Bid]:* Alleen advertenties weergeven voor gebruikers die zijn gekoppeld aan doelgroepen die ook voldoen aan andere doelen voor de advertentiegroep.

* *[!UICONTROL Bid Only]:* Advertenties tonen zelfs aan mensen die niet met doelpubliek worden geassocieerd zolang zij andere doelstellingen op groepsniveau voldoen. U kunt de kans echter vergroten dat advertenties bij een bepaald publiek worden getoond door voor dat publiek hogere biedingen in te stellen.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Voor [!DNL Microsoft® Advertising] en groepen in het publieksnetwerk, biodmodifiers voor plaatsdoelstellingen worden niet geoptimaliseerd in standaardportefeuilles met &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot; instellen.

**[!UICONTROL Genre]:** (Groepen toevoegen in [!UICONTROL Audience CTV Video] campagnes; beschikbaar in de V.S., CA, BR, MX, UK, DE, ES, FR, IT, AU, MY en TH<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->) De doelgenres, die de shows en kanalen bepalen waarop uw advertenties verschijnen:

* *[!UICONTROL All genres]:* (De standaardinstelling) Hiermee worden alle genres als doel ingesteld.

* *[!UICONTROL Select From Below List]:* Hiermee worden de geselecteerde genres als doel opgegeven. Maak een keuze in de lijst met alle beschikbare genres.

De positie van de aangesloten tv (CTV) is afhankelijk van de videokwaliteit en het aantal biedingen. Zie de [technische vereisten voor CTV-advertenties](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (Publiek en groepen; facultatief) specifieke geslachten om als doel op te nemen of uit te sluiten: *[!UICONTROL Male]*, *[!UICONTROL Female]*, en *[!UICONTROL Unknown]*. Standaard worden alle genders als doelgroep gebruikt. Uitsluitingen hebben altijd voorrang op insluitingen.

* Selecteer geen waarden als u alle waarden als doel wilt instellen.

* Als u een waarde wilt opnemen, klikt u eenmaal op de cirkel naast de waarde, zodat een blauw vinkje (![Inclusief](/help/search-social-commerce/assets/include.png "Inclusief")) wordt weergegeven. U kunt het aantal biedingen optioneel verhogen of verlagen met een bepaald percentage voor elk van de beoogde geslachten.

* Als u een waarde wilt uitsluiten, klikt u tweemaal op de cirkel naast de waarde, zodat een rood vinkje (![Uitsluiten](/help/search-social-commerce/assets/exclude.png "Uitsluiten")) wordt weergegeven.

**[!UICONTROL Age]:** (Publiek en groepen; facultatief) specifieke leeftijdscategorieën die als streefcijfers moeten worden opgenomen of uitgesloten: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]*, en *[!UICONTROL Unknown]*. Standaard worden alle leeftijden als doelgroep gebruikt. Uitsluitingen hebben altijd voorrang op insluitingen.

* Selecteer geen waarden als u alle waarden als doel wilt instellen.

* Als u een waarde wilt opnemen, klikt u eenmaal op de cirkel naast de waarde, zodat een blauw vinkje (![Inclusief](/help/search-social-commerce/assets/include.png "Inclusief")) wordt weergegeven. U kunt het aantal biedingen voor elke beoogde leeftijd optioneel met een bepaald percentage verhogen of verlagen.

* Als u een waarde wilt uitsluiten, klikt u tweemaal op de cirkel naast de waarde, zodat een rood vinkje (![Uitsluiten](/help/search-social-commerce/assets/exclude.png "Uitsluiten")) wordt weergegeven.

**[!UICONTROL Industry]:** (Publiek en groepen; facultatief) specifieke bedrijfstakken om als streefcijfers op te nemen of uit te sluiten. Standaard zijn alle industrieën gericht. Uitsluitingen hebben altijd voorrang op insluitingen.

* Selecteer geen waarden als u alle waarden als doel wilt instellen.

* Als u een waarde wilt opnemen, klikt u eenmaal op de cirkel naast de waarde, zodat een blauw vinkje (![Inclusief](/help/search-social-commerce/assets/include.png "Inclusief")) wordt weergegeven. U kunt biedingen voor elke beoogde sector optioneel met een bepaald percentage verhogen of verlagen.

* Als u een waarde wilt uitsluiten, klikt u tweemaal op de cirkel naast de waarde, zodat een rood vinkje (![Uitsluiten](/help/search-social-commerce/assets/exclude.png "Uitsluiten")) wordt weergegeven.

**[!UICONTROL Job Function Targets]:** (Publiek en groepen; facultatief) specifieke functies om als doelen op te nemen of uit te sluiten. Standaard worden alle functies geactiveerd. Uitsluitingen hebben altijd voorrang op insluitingen.

* Selecteer geen waarden als u alle waarden als doel wilt instellen.

* Als u een waarde wilt opnemen, klikt u eenmaal op de cirkel naast de waarde, zodat een blauw vinkje (![Inclusief](/help/search-social-commerce/assets/include.png "Inclusief")) wordt weergegeven. U kunt de biedingen optioneel met een bepaald percentage verhogen of verlagen voor elke betreffende taakfunctie.

* Als u een waarde wilt uitsluiten, klikt u tweemaal op de cirkel naast de waarde, zodat een rood vinkje (![Uitsluiten](/help/search-social-commerce/assets/exclude.png "Uitsluiten")) wordt weergegeven.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** (Optioneel) Het aantal keren dat een klant advertenties van de advertentiegroep ontvangt. Voer een waarde in en selecteer de tijdeenheid (*[!UICONTROL Hour]*, *[!UICONTROL Day]*, of *[!UICONTROL Week]*).

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Alleen campagnes op het scherm/native netwerk; optioneel) Sites op het weergavenetwerk waarop u uw advertenties niet wilt weergeven. Voer een geldige URL in, bijvoorbeeld www.example.com. Als u meerdere tekenreeksen wilt opgeven, scheidt u deze met komma&#39;s of voert u ze op afzonderlijke regels in.

Voor informatie over beschikbaarheid, zie [!DNL Microsoft® Advertising] Help bij &quot;[Voorkomen dat advertenties op bepaalde websites worden weergegeven](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

>[!MORELIKETHIS]
>
>* [Adroepen beheren](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
