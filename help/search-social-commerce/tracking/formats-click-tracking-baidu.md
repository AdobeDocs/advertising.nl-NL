---
title: Opmaak voor het bijhouden van klikken voor  [!DNL Baidu]
description: Leer over de klik-volgende formaten voor  [!DNL Baidu]  rekeningen.
exl-id: 4f4ed518-aa25-4a29-b263-c01f78b69b92
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# Opmaak voor het bijhouden van klikken op gesponsorde advertenties op [!DNL Baidu]

De volgende basis-bestemmings-URL-indeling is van toepassing op gesponsorde advertenties:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder in Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als tokendoorgeven is uitgeschakeld, vervangt u `cq?` after `<advertiser_ID>` with `c?` .
>
>* `<campaignID>` is een variabele voor de numerieke campagne-id.
>
>* `<the landing page>` is een variabele die de URL op uw site vertegenwoordigt waarnaar eindgebruikers worden geleid.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer klik-volgende formaten URL voor de conversie het volgen dienst van Adobe Advertising &#x200B;](formats-click-tracking-about.md)
>* [&#x200B; Vormen van identiteitskaart AMO &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
