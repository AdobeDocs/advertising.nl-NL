---
title: Opmaak voor het bijhouden van klikken voor  [!DNL Yahoo! Japan Ads]
description: Leer over de klik-volgende formaten voor  [!DNL Yahoo! Japan Ads]  rekeningen.
exl-id: 79e45205-5c72-4612-9b60-36538e3c48c4
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Opmaak voor het bijhouden van klikken op gesponsorde advertenties op [!DNL Yahoo! Japan Ads]

De volgende sjabloonindelingen voor het bijhouden van basis zijn van toepassing op gesponsorde advertenties:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

of als de optie voor automatische labeling is ingesteld voor het account in [!DNL Yahoo! Japan Ads] :

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder in Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als tokendoorgeven is uitgeschakeld, vervangt u `cq?` after `<advertiser_ID>` with `c?` .
>
>* `<the landing page>` is een variabele die de URL op uw site vertegenwoordigt waarnaar eindgebruikers worden geleid.

>[!MORELIKETHIS]
>
>* [ Ongeveer klik-volgende formaten URL voor de conversie het volgen dienst van Adobe Advertising ](formats-click-tracking-about.md)
>* [ formaten van identiteitskaart AMO ](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
