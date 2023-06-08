---
title: Opmaak voor het bijhouden van klikken voor [!DNL Baidu]
description: Meer informatie over de indelingen voor klikken en bijhouden voor [!DNL Baidu] rekeningen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Opmaak voor het bijhouden van klikken voor gesponsorde advertenties op [!DNL Baidu]

De volgende basis-bestemmings-URL-indeling is van toepassing op gesponsorde advertenties:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder in Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als het doorgeven van token is uitgeschakeld, kunt u dit vervangen `cq?` na `<advertiser_ID>` with `c?`.
>
>* `<campaignID>` is een variabele voor de numerieke campagne-id.
>
>* `<the landing page>` is een variabele die de URL op uw site vertegenwoordigt waarnaar eindgebruikers worden geleid.


>[!MORELIKETHIS]
>
>* [Over het bijhouden van klikken op URL-indelingen voor de service voor het bijhouden van Adobe-advertenties](formats-click-tracking-about.md)
>* [Opmaak voor de s\_kwcid-trackingcode](skwcid-tracking-parameter.md)

