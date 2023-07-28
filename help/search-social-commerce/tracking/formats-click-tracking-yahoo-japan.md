---
title: Opmaak voor het bijhouden van klikken voor [!DNL Yahoo! Japan Ads]
description: Meer informatie over de indelingen voor klikken en bijhouden voor [!DNL Yahoo! Japan Ads] rekeningen.
exl-id: 4584f2c4-8090-4931-bd44-0df42f350755
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Opmaak voor het bijhouden van klikken voor gesponsorde advertenties op [!DNL Yahoo! Japan Ads]

De volgende sjabloonindelingen voor het bijhouden van basis zijn van toepassing op gesponsorde advertenties:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

of als de optie voor automatische labeling is ingesteld voor het account in [!DNL Yahoo! Japan Ads]:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder binnen de Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als het doorgeven van token is uitgeschakeld, kunt u dit vervangen `cq?` na `<advertiser_ID>` with `c?`.
>
>* `<the landing page>` is een variabele die de URL op uw site vertegenwoordigt waarnaar eindgebruikers worden geleid.

>[!MORELIKETHIS]
>
>* [Over URL-indelingen voor het bijhouden van klikken voor de service Adobe Advertising converteren](formats-click-tracking-about.md)
>* [Opmaak voor de s\_kwcid-trackingcode](skwcid-tracking-parameter.md)
