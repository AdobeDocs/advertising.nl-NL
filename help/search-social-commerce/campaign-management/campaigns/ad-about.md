---
title: Advertenties beheren
description: Meer informatie over advertenties in Zoeken, Sociaal en Commerce, inclusief de beschikbare advertentietypen.
exl-id: 01bd211d-fe6b-4329-90e1-0e54d626c125
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Over advertenties

*[!DNL Google Ads], [!DNL Microsoft Advertising] , [!DNL Yahoo! Japan Ads] , [!DNL Yandex] en alleen bestaande [!DNL Baidu] accounts*

Een advertentie kan worden weergegeven op een doelwebsite (voor inhoud of op plaatsing gerichte campagnes); wanneer een gebruiker naar een van de trefwoorden in de advertentiegroep zoekt (voor zoekcampagnes) of naar inhoud op uw website (dynamische zoekadvertenties in [!DNL Google Ads] alleen-zoekcampagnes); of wanneer een gebruiker een zoekopdracht uitvoert die relevant is voor een van de items in de [!DNL Google Merchant Center] - of [!DNL Microsoft Merchant Center] productfeed (advertenties in [!DNL Google Ads] of productadvertenties in [!DNL Microsoft Advertising] campagnes).

## Beschikbare advertentietypen

U kunt ondersteunde advertentietypen voor advertentiegroepen maken en beheren in een gesynchroniseerde advertentie-netwerkaccount:

* **de advertenties van de Tekst of uitgebreide tekstadvertenties** voor een advertentiegroep in een campagne die het onderzoeksnetwerk richt. Tekstadvertenties kunnen optionele volgparameters bevatten die de parameters op advertentieniveau of op campagnereniveau overschrijven. Afhankelijk van het advertentienetwerk, kunt u of uitgebreide/uitgebreide tekstadvertenties of standaardtekstadvertenties tot stand brengen.

* Interdevice, inheemse **publieksadvertenties** voor [!DNL Microsoft Advertising] campagnes op [!DNL Microsoft Audience Network]. U hebt twee opties voor publieksadvertenties, op basis van de campagne-instellingen:

   * Als de campagne aan een winkelcentrum wordt verbonden, dan laat het advertentienetwerk automatisch advertenties op diervoeder-gebaseerde advertenties voor de campagne produceren, gebruikend de productinformatie van de opslag. U hoeft geen op feed gebaseerde advertenties voor de campagne te maken, maar u moet ad-groups maken met een gebruikerstoewijzing.

   * Als de campagne niet is gekoppeld aan een commercieel gecentreerde account, maakt u op afbeeldingen gebaseerde publieksadvertenties met de responsieve advertentievorm, die meerdere tekst- en afbeeldingselementen bevat. Het advertentienetwerk verzamelt de advertenties met behulp van de meest effectieve combinaties van advertentie-elementen en geeft deze weer op sites als [!DNL MSN] , [!DNL Outlook.com] en [!DNL Microsoft Edge] .

* **vraag-slechts advertenties** voor [!DNL Google Ads] campagnes op het onderzoeksnetwerk. Alleen-aanroepbare advertenties zijn tekstadvertenties die een telefoonnummer bevatten. U kunt optioneel een [!DNL Google Ads]-toegewezen door:sturen aantal voor geavanceerde vraag gebruiken meldend.

* **Uitgebreide dynamische onderzoeksadvertenties** (nu genoemd enkel &quot;dynamische onderzoeksadvertenties&quot;op de advertentienetwerken) voor [!DNL Google Ads] en [!DNL Microsoft Advertising] dynamische onderzoek en groepen in onderzoekscampagnes. Dynamische zoekadvertenties gebruiken inhoud van uw website in plaats van trefwoorden om te bepalen wanneer u uw advertenties wilt weergeven. Het advertentienetwerk genereert dynamisch de kop, kiest de bestemmingspagina-URL en de weergave-URL en genereert automatisch de laatste URL.

  U kunt de pagina&#39;s in uw websites definiëren waarvan de inhoud wordt gebruikt om uw dynamische zoekadvertenties te activeren door specifieke dynamische zoekdoelen voor de advertentiegroep in te stellen. Voor [!DNL Google Ads] kunt u dynamische zoekdoelen maken in Zoeken, Sociaal en Commerce. Voor [!DNL Microsoft Advertising] moet u deze doelen maken binnen [!DNL Microsoft Advertising] . In [!DNL Google Ads] campagnes, kunt u naar keuze een websitedomein en een taal in de sectie &quot;[!DNL DSA Options]&quot;van de campagne specificeren in plaats van, of naast, het creëren van dynamische onderzoeksdoelstellingen.

  Wanneer de zoekterm van een gebruiker exact overeenkomt met een trefwoord in een van uw op trefwoorden gebaseerde campagnes, wordt een advertentie uit de op trefwoorden gebaseerde campagne weergegeven in plaats van een dynamische zoekadvertentie. Het advertentienetwerk toont een dynamische onderzoeksadvertentie in plaats van een sleutelwoord-gericht en wanneer de het onderzoekstermijn van de gebruiker een brede gelijke of woordgroep aan één van uw sleutelwoorden en uw dynamische onderzoeksadvertentie heeft een hogere rang.

  Voor meer informatie over dynamische onderzoeksadvertenties, zie de [[!DNL Google Ads]  documentatie &#x200B;](https://support.google.com/google-ads/answer/2471185) en [[!DNL Microsoft Advertising]  documentatie &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Multimedia advertenties** voor [!DNL Microsoft Advertising] onderzoekscampagnes. Multimedia-advertenties zijn grote afbeeldingsadvertenties die worden weergegeven op de prominente posities in de mainline en zijbalk en die slechts één multimediadad per pagina bevatten. Ze kunnen meerdere tekst- en afbeeldingselementen bevatten, zoals responsieve advertenties, en het advertentienetwerk verzamelt de advertenties met behulp van de meest effectieve combinaties van advertentie-elementen. Multimedia-advertenties vervangen uw tekst en plaatsingen niet.

* Promotielijnen voor **[!DNL Microsoft Advertising]product(shopping) advertenties** op het winkelnetwerk. Voor winkeladvertenties worden producten in de bestaande [!DNL Microsoft Merchant Center] -productfeed gebruikt in plaats van trefwoorden om te bepalen hoe en waar u uw advertenties wilt weergeven. De URL van de advertentiekopie- en landingspagina wordt automatisch gegenereerd op basis van uw productinformatie in de feed, maar u kunt optioneel promotielijnen instellen die worden opgenomen voor de advertentiegroep.

  U kunt bepalen welke producten worden weergegeven met uw [!DNL Microsoft Advertising] winkeladvertenties door afzonderlijke productgroepen voor de advertentiegroep in te stellen, vanuit de weergave [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] .

  Voor meer informatie over het werkschema voor product/het winkelen advertenties, zie &quot;[&#x200B; uitvoeren  [!DNL Microsoft Advertising]  het winkelen campagnes &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md).&quot;  Voor extra informatie over productadvertenties, zie de [&#x200B; documentatie van Advertising van Microsoft &#x200B;](https://help.ads.microsoft.com/#apex/3/en/51082).

* Responsieve zoekopdrachten voor [!DNL Google Ads] - en [!DNL Microsoft Advertising] -campagnes op het zoeknetwerk. Het advertentienetwerk assembleert dynamisch op tekst gebaseerde responsieve zoekadvertenties van een reeks advertentietitels en beschrijvingen, die combinaties begunstigen die goed samen presteren. De advertentie bevat maximaal drie kopregels, twee beschrijvingen en een aanpasbare URL uit de basis-URL en optionele velden path1 en path2. U kunt desgewenst titels en beschrijvingen vastzetten op specifieke posities.

>[!NOTE]
>
>[!DNL Google Ads] verstrekt geen gegevens buiten zijn inheemse redacteurs over de tekstcombinaties die als advertenties werden getoond. Voor meer informatie over het melden voor elke tekstcombinatie, zie de [&#x200B; documentatie van Google Ads &#x200B;](https://support.google.com/google-ads/answer/7684791).

## De weergave [!UICONTROL Ads]

U kunt advertenties maken, bewerken en de status ervan wijzigen in de weergave [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads] .

## Prestatiegegevens op advertentieniveau

Gegevens op ad-niveau zijn beschikbaar voor de meeste advertentietypen.

Deze functie is echter niet beschikbaar voor [!DNL Google Ads] dynamische zoekopdrachten en (DSA), maximale prestaties, slim winkelen en [!DNL YouTube] -campagnes. Verwacht discrepanties tussen de totale ad-level gegevens voor een campagne en de totale gegevens voor de campagne.

| Toevoegen van netwerk-/campagne-/advertentietype | Beschikbaarheid van gegevens |
|---|---|
| [!DNL Google Ads] dynamic search ad (DSA) | Campagne, ad groep |
| [!DNL Google Ads] maximale prestaties | Campagne |
| [!DNL Google Ads] winkelen, slim winkelen | Campagne, ad groep |
| [!DNL Google Ads] [!DNL YouTube] | Campagne, ad groep |

>[!MORELIKETHIS]
>
>* [&#x200B; beheert advertenties &#x200B;](ad-manage.md)
