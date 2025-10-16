---
title: '[!DNL Google Ads] ad-groepinstellingen'
description: Verwijs de montages voor  [!DNL Google Ads]  en groepen.
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
source-git-commit: 345c2af5363ca10412f3809700e281af5b06897f
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# [!DNL Google Ads] ad-groepinstellingen

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Een naam van een advertentiegroep die binnen de campagne uniek is. De maximumlengte is 255 double-byte tekens.

**[!UICONTROL Status]:** de vertoningsstatus van de advertentiegroep: *Actieve* of *Gepauzeerde*. Het gebrek voor nieuwe advertentiegroepen is Actief **.

**[!UICONTROL Ad Group Type]:** (Uitgebreide dynamische onderzoek en campagnes slechts) het type van ad groep:

* *[!UICONTROL Search Standard]* (de standaardwaarde): voor standaardadvertenties.

* *[!UICONTROL Search Dynamic]:* voor dynamische zoekopdrachten.

**[!UICONTROL Ad Rotation Mode]:** Hoe vaak [!DNL Google Ads] levert u uw actieve advertenties in relatie tot elkaar in de advertentiegroep:

* *[!UICONTROL Optimize]:* Google Ads geeft advertenties de voorkeur die naar verwachting beter zullen presteren dan andere advertenties in de advertentiegroep. Deze advertenties komen vaker op de advertentie in en in de loop van de tijd wordt één advertentie bevoordeeld. Dit is mogelijk inconsistent met uw zakelijke en optimalisatiedoelstellingen.

* *[!UICONTROL Rotate forever]:*   Elk van je advertenties komt een even aantal keren in de advertentievieiling terecht, zodat Search, Social en Commerce je advertenties niet alleen op doorkliksnelheid maar ook op conversies kunnen scoren.

* *[!UICONTROL Use campaign setting]* (de standaardinstelling voor nieuwe advertentiegroepen): gebruikt de bestaande instelling op campagnereniveau en rotatie. **Nota:** het campagne-niveau plaatsen is niet zichtbaar in Onderzoek, Sociaal, &amp; Commerce.

Als de campagne gebruikmaakt van een strategie voor slim bieden (zoals [!UICONTROL Target CPA] , [!UICONTROL Target ROAS] ), stelt [!DNL Google Ads] automatisch de optie in op &quot; [!UICONTROL Optimize]&quot;.

**[!UICONTROL Custom Bid Level]:** (Campagnes die alleen op het weergavenetwerk zijn gericht) Hoe u kunt bieden: door *[!UICONTROL Ad Group]* (de standaardinstelling), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Interesten en opmerkingen in Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (website), *[!UICONTROL Unknown]* of *[!UICONTROL Vertical]* .

>[!NOTE]
>
>* Als je op trefwoord biedt, maak je trackingsjablonen op trefwoordniveau. Als je op plaatsing biedt, maak je ook trackingsjablonen op plaatsingsniveau. Voor alle andere dimensies maakt u volgsjablonen op advertentieniveau.
>* Wanneer u op leeftijd, geslacht, interesse en lijst of verticaal biedt voor campagnes in portfolio&#39;s, optimaliseert de optimalisatiefunctie de biedingen voor de dimensie niet. Bovendien wordt alle toewijzing toegepast op de advertentiegroep.
>* Advertenties op het onderzoeksnetwerk gebruiken altijd sleutelwoordbiedingen.

**[!UICONTROL AI Max Search Term Matching]:** (Campagnes die het onderzoeksnetwerk richten en waarvoor de [ AI Max eigenschap ](https://support.google.com/google-ads/answer/15910366) en de campagne-vlakke gelijke eigenschap van de onderzoeksterm wordt toegelaten; read-only) of de ad groep-vlakke zoekterm aanpassing wordt toegelaten: *[!UICONTROL Disabled]* of *[!UICONTROL Enabled]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Campagnes with [!UICONTROL Target CPA] bidding; optioneel) De doelkosten per aankoop (CPA) voor de advertentiegroep. Deze waarde heeft voorrang op het doel op campagneniveau.

**[!UICONTROL Target ROAS]:** (Campagnes with [!UICONTROL Target ROAS] bidding; optioneel) Het doelrendement op advertentie-uitgaven (ROAS) voor de advertentiegroep, als percentage. Deze waarde heeft voorrang op het doel op campagneniveau.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Campagnes op slechts het onderzoeksnetwerk, en bestaande, read-only [!DNL Gmail] campagnes op het vertoningsnetwerk) Of:

* *[!UICONTROL Target and Bid]:* om alleen advertenties weer te geven aan gebruikers die zijn gekoppeld aan doelgroepen die ook voldoen aan andere doelen voor de advertentiegroep.

* *[!UICONTROL Bid Only]:* om zelfs advertenties aan mensen te tonen die niet met doelpubliek worden geassocieerd zolang zij andere doelstellingen op het niveau van de ad groep voldoen. U kunt de kans echter vergroten dat advertenties bij een bepaald publiek worden getoond door voor dat publiek hogere biedingen in te stellen.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

>[!MORELIKETHIS]
>
>* [ beheer en groepen ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
