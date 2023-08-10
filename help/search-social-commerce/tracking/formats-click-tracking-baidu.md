---
title: Opmaak voor het bijhouden van klikken voor [!DNL Baidu]
description: Meer informatie over de indelingen voor klikken en bijhouden voor [!DNL Baidu] rekeningen.
exl-id: a57ff0cf-0bcf-4d55-9a86-7551db8a08e7
feature: Search Tracking
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
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
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder binnen de Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als het doorgeven van token is uitgeschakeld, kunt u dit vervangen `cq?` na `<advertiser_ID>` with `c?`.
>
>* `<campaignID>` is een variabele voor de numerieke campagne-id.
>
>* `<the landing page>` is een variabele die de URL op uw site vertegenwoordigt waarnaar eindgebruikers worden geleid.

>[!MORELIKETHIS]
>
>* [Over URL-indelingen voor het bijhouden van klikken voor de service Adobe Advertising converteren](formats-click-tracking-about.md)
>* [Opmaak voor de trackingcode van de AMO-id](amo-id-tracking-parameter.md)
