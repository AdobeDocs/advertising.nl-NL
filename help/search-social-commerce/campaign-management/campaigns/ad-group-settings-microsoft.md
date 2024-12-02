---
title: '[!DNL Microsoft Advertising] ad-groepinstellingen'
description: Verwijs de montages voor  [!DNL Microsoft Advertising]  en groepen.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] ad-groepinstellingen

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Een naam van een advertentiegroep die binnen de campagne uniek is. De maximumlengte is 128 tekens.

**[!UICONTROL Status]:** de vertoningsstatus van de advertentiegroep: *Actieve* of *Gepauzeerde*. Het gebrek voor nieuwe advertentiegroepen is Actief **.

**[!UICONTROL Ad Language]:** (de campagnes van het Onderzoek) de doeltaal voor advertenties.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** (Zoekadvertenties) Hoe en waar u advertenties in de advertentiegroep plaatst:

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* (de standaardinstelling): om biedingen voor advertenties op het zoeknetwerk te plaatsen.

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]:* om biedingen voor advertenties op gesynchroniseerde partnersites te plaatsen.

* *[!UICONTROL Content network]:* Afgekeurd

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** Afgekeurd

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Publiek en groepen) Of:

* *[!UICONTROL Target and Bid]:* om alleen advertenties weer te geven aan gebruikers die zijn gekoppeld aan doelgroepen die ook voldoen aan andere doelen voor de advertentiegroep.

* *[!UICONTROL Bid Only]:* om zelfs advertenties aan mensen te tonen die niet met doelpubliek worden geassocieerd zolang zij andere doelstellingen op het niveau van de ad groep voldoen. U kunt de kans echter vergroten dat advertenties bij een bepaald publiek worden getoond door voor dat publiek hogere biedingen in te stellen.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Voor [!DNL Microsoft Advertising] advertentiegroepen in het publieksnetwerk, biodmodifiers voor plaatsdoelstellingen worden niet geoptimaliseerd in standaardportefeuilles met &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;het plaatsen.

**[!UICONTROL Genre]:** (De groepen van de Advertentie in [!UICONTROL Audience CTV Video] campagnes; beschikbaar in V.S., CA, BR, MX, UK, DE, ES, FR, IT, AU, MY, en TH <!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->) de doelgenres, die de shows en de kanalen bepalen waarop uw advertenties verschijnen:

* *[!UICONTROL All genres]:* (het gebrek) richt alle genres.

* *[!UICONTROL Select From Below List]:* hiermee worden geselecteerde genres als doel opgegeven. Maak een keuze in de lijst met alle beschikbare genres.

De positie van de aangesloten tv (CTV) is afhankelijk van de videokwaliteit en het aantal biedingen. Zie de [ technische vereisten voor CTV advertenties ](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (Publiek en groepen; optioneel) Specifieke genders die als doel moeten worden opgenomen of uitgesloten: *[!UICONTROL Male]*, *[!UICONTROL Female]* en *[!UICONTROL Unknown]* . Standaard worden alle genders als doelgroep gebruikt. Uitsluitingen hebben altijd voorrang op insluitingen.

* Selecteer geen waarden als u alle waarden als doel wilt instellen.

* Om een waarde te omvatten, klik eens de aangrenzende cirkel zodat een blauw controleteken (![ omvat ](/help/search-social-commerce/assets/include.png " ")) verschijnt. U kunt het aantal biedingen optioneel verhogen of verlagen met een bepaald percentage voor elk van de beoogde geslachten.

* Om een waarde uit te sluiten, klik tweemaal de aangrenzende cirkel zodat een rood controleteken (![ sluit ](/help/search-social-commerce/assets/exclude.png " uit ")) verschijnt.

**[!UICONTROL Age]:** (Publiek en groepen; optioneel) Specifieke leeftijdscategorieën die als doel moeten worden opgenomen of uitgesloten: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]* en *[!UICONTROL Unknown]* . Standaard worden alle leeftijden als doelgroep gebruikt. Uitsluitingen hebben altijd voorrang op insluitingen.

* Selecteer geen waarden als u alle waarden als doel wilt instellen.

* Om een waarde te omvatten, klik eens de aangrenzende cirkel zodat een blauw controleteken (![ omvat ](/help/search-social-commerce/assets/include.png " ")) verschijnt. U kunt het aantal biedingen voor elke beoogde leeftijd optioneel met een bepaald percentage verhogen of verlagen.

* Om een waarde uit te sluiten, klik tweemaal de aangrenzende cirkel zodat een rood controleteken (![ sluit ](/help/search-social-commerce/assets/exclude.png " uit ")) verschijnt.

**[!UICONTROL Industry]:** (Publiek en groepen; facultatief) specifieke industrieën om als doelstellingen op te nemen of uit te sluiten. Standaard zijn alle industrieën gericht. Uitsluitingen hebben altijd voorrang op insluitingen.

* Selecteer geen waarden als u alle waarden als doel wilt instellen.

* Om een waarde te omvatten, klik eens de aangrenzende cirkel zodat een blauw controleteken (![ omvat ](/help/search-social-commerce/assets/include.png " ")) verschijnt. U kunt biedingen voor elke beoogde sector optioneel met een bepaald percentage verhogen of verlagen.

* Om een waarde uit te sluiten, klik tweemaal de aangrenzende cirkel zodat een rood controleteken (![ sluit ](/help/search-social-commerce/assets/exclude.png " uit ")) verschijnt.

**[!UICONTROL Job Function Targets]:** (Publiek en groepen; facultatief) specifieke baanfuncties om als doelstellingen te omvatten of uit te sluiten. Standaard worden alle functies geactiveerd. Uitsluitingen hebben altijd voorrang op insluitingen.

* Selecteer geen waarden als u alle waarden als doel wilt instellen.

* Om een waarde te omvatten, klik eens de aangrenzende cirkel zodat een blauw controleteken (![ omvat ](/help/search-social-commerce/assets/include.png " ")) verschijnt. U kunt de biedingen optioneel met een bepaald percentage verhogen of verlagen voor elke betreffende taakfunctie.

* Om een waarde uit te sluiten, klik tweemaal de aangrenzende cirkel zodat een rood controleteken (![ sluit ](/help/search-social-commerce/assets/exclude.png " uit ")) verschijnt.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** (Optioneel) Het aantal keren dat een klant advertenties van de advertentiegroep kan ontvangen. Voer een waarde in en selecteer de tijdeenheid (*[!UICONTROL Hour]* , *[!UICONTROL Day]* of *[!UICONTROL Week]* ).

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campagnes op de vertoning/het inheemse netwerk slechts; facultatief) Plaatsen op het vertoningsnetwerk waarop u uw advertenties niet wilt worden getoond. Voer een geldige URL in, bijvoorbeeld www.example.com. Als u meerdere tekenreeksen wilt opgeven, scheidt u deze met komma&#39;s of voert u ze op afzonderlijke regels in.

Voor informatie over beschikbaarheid, zie [!DNL Microsoft Advertising] hulp aan &quot;[ verhinderen advertenties op specifieke websites ](https://help.ads.microsoft.com/#apex/bae/en/14061/0) verschijnen.&quot;

>[!MORELIKETHIS]
>
>* [ beheer en groepen ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
