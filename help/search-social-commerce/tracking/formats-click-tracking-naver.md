---
title: Opmaak voor het bijhouden van klikken voor  [!DNL Naver]
description: Leer over de klik-volgende formaten voor  [!DNL Naver]  rekeningen.
exl-id: b438652e-6e98-4223-8169-2bfb37500670
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Opmaak voor het bijhouden van klikken op gesponsorde advertenties op [!DNL Naver]

De volgende basis-bestemmings-URL-indeling is van toepassing op gesponsorde advertenties:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=87&ev_cl={ef_uniqueid}&url=<the landing page>`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder in Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als tokendoorgeven is uitgeschakeld, vervangt u `cq?` after `<advertiser_ID>` with `c?` .
>
>* `<the landing page>` is een variabele die de URL op uw site vertegenwoordigt waarnaar eindgebruikers worden geleid.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer klik-volgende formaten URL voor de conversie het volgen dienst van Adobe Advertising &#x200B;](formats-click-tracking-about.md)
>* [&#x200B; formaten van identiteitskaart AMO &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
