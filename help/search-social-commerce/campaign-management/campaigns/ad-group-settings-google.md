---
title: "[!DNL Google Ads] ad group settings"
description: Verwijs naar de instellingen voor [!DNL Google Ads] ad groepen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# [!DNL Google Ads] groepsinstellingen

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** Een naam van een advertentiegroep die uniek is in de campagne. De maximumlengte is 255 double-byte tekens.

**[!UICONTROL Status]:** De weergavestatus van de advertentiegroep: *Actief* of *Gepauzeerd*. De standaardinstelling voor nieuwe advertentiegroepen is *Actief*.

**[!UICONTROL Ad Group Type]:** (Alleen uitgebreide dynamische zoekopdrachten en campagnes) Het type advertentiegroep:

* *[!UICONTROL Search Standard]* (de standaardinstelling): Voor standaardadvertenties.

* *[!UICONTROL Search Dynamic]:* Voor dynamische zoekopdrachten.

**[!UICONTROL Ad Rotation Mode]:** Hoe vaak [!DNL Google Ads] levert uw actieve advertenties in relatie tot elkaar binnen de advertentiegroep:

* *[!UICONTROL Optimize]:* In Google Ads worden advertenties geprezen die naar verwachting beter zullen worden uitgevoerd dan andere advertenties in de advertentiegroep. Deze advertenties komen vaker op de advertentie in en in de loop van de tijd wordt één advertentie bevoordeeld. Dit is mogelijk inconsistent met uw zakelijke en optimalisatiedoelstellingen.

* *[!UICONTROL Rotate forever]:*   Elk van je advertenties komt een even aantal keren op de advertentieviekplaats terecht, zodat Search, Social &amp; Commerce je advertenties niet alleen op doorkliksnelheid maar ook op conversies kan scoren.

* *[!UICONTROL Use campaign setting]*(de standaardinstelling voor nieuwe advertentiegroepen): Gebruikt de bestaande instelling voor campagneniveau en rotatie. **Opmerking:** De instelling op campagneniveau is niet zichtbaar in Zoeken, Sociale Zaken en Handel.

Als de campagne gebruikmaakt van een strategie voor een slim bod (bijvoorbeeld [!UICONTROL Target CPA], [!UICONTROL Target ROAS], of [!UICONTROL Enhanced CPC]), dan [!DNL Google Ads] stelt de optie automatisch in op &quot;[!UICONTROL Optimize].&quot;

**[!UICONTROL Custom Bid Level]:** (Campagnes die slechts het vertoningsnetwerk richten) hoe te om te bieden: door *[!UICONTROL Ad Group]* (standaard), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Belangen en Opmerking in Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (website), *[!UICONTROL Unknown]*, of *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Als je op trefwoord biedt, maak je trackingsjablonen op trefwoordniveau. Als je op plaatsing biedt, maak je ook trackingsjablonen op plaatsingsniveau. Voor alle andere dimensies maakt u volgsjablonen op advertentieniveau.
>* Wanneer u op leeftijd, geslacht, interesse en lijst of verticaal biedt voor campagnes in portfolio&#39;s, optimaliseert de optimalisatiefunctie de biedingen voor de dimensie niet. Bovendien wordt alle toewijzing toegepast op de advertentiegroep.
>* Advertenties op het onderzoeksnetwerk gebruiken altijd sleutelwoordbiedingen.


## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Campagnes met [!UICONTROL Target CPA] biedingen; (facultatief) de streefkosten per verwerving (CPA) voor de advertentiegroep. Deze waarde heeft voorrang op het doel op campagneniveau.

**[!UICONTROL Target ROAS]:** (Campagnes met [!UICONTROL Target ROAS] biedingen; (optioneel) Het doelrendement op advertentie-uitgaven (ROAS) voor de advertentiegroep, als percentage. Deze waarde heeft voorrang op het doel op campagneniveau.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Campagnes op slechts het onderzoeksnetwerk, en bestaand, read-only [!DNL Gmail] campagnes op het vertoningsnetwerk) Of:

* *[!UICONTROL Target and Bid]:* Alleen advertenties weergeven voor gebruikers die zijn gekoppeld aan doelgroepen die ook voldoen aan andere doelen voor de advertentiegroep.

* *[!UICONTROL Bid Only]:* Advertenties tonen zelfs aan mensen die niet met doelpubliek worden geassocieerd zolang zij andere doelstellingen op groepsniveau voldoen. U kunt de kans echter vergroten dat advertenties bij een bepaald publiek worden getoond door voor dat publiek hogere biedingen in te stellen.

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
>* [Advertentiegroepen beheren](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)

