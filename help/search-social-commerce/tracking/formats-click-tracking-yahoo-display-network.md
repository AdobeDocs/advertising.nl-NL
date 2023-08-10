---
title: Opmaak voor het bijhouden van klikken voor [!DNL Yahoo! Display Network]
description: Meer informatie over de indelingen voor klikken en bijhouden voor [!DNL Yahoo! Display Network] rekeningen.
exl-id: 62ea592c-9138-4a8e-9616-c8f2475fea26
feature: Search Tracking
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# Opmaak voor het bijhouden van klikken voor gesponsorde advertenties op [!DNL Yahoo! Display Network]

De volgende basis-bestemmings-URL-indeling is van toepassing op gesponsorde advertenties:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=86&ev_cl={ef_uniqueid}&url=<the landing page>`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=86&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

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
>* [Opmaak voor de trackingcode van de AMO-id](skwcid-tracking-parameter.md)
