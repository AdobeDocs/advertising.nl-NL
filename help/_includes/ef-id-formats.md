---
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---
# Adobe Advertising EF-id&#39;s

>[!NOTE]
>
>EF-id&#39;s zijn hoofdlettergevoelig. Als een [!DNL Analytics] - of Customer Journey Analytics-implementatie URL-tracking in kleine letters forceert, herkent Adobe Advertising de EF-id niet. Dit is van invloed op Adobe Advertising-biedingen en -rapporten, maar heeft geen invloed op Adobe Advertising-rapportage binnen [!DNL Analytics] of Customer Journey Analytics.

#### [!DNL Google Ads] zoekopdrachten

```
{gclid}:G:s
```

waarbij:

* `gclid` is de [!DNL Google Click ID] (GCLID).
* `s` is het netwerktype (&quot;s&quot; voor onderzoek).

#### [!DNL Microsoft Advertising] zoekopdrachten

```
{msclkid}:G:s
```

waarbij:

* `msclkid` is de [!DNL Microsoft Click ID] (MSCLKID).
* `s` is het netwerktype (&quot;s&quot; voor onderzoek).

#### Advertenties en zoekadvertenties weergeven op andere zoekmachines

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

waarbij:

* &lt;*identiteitskaart van de bezoeker van Adobe Advertising*> is een unieke identiteitskaart per bezoeker (zoals UWKVaAABCkJ0mDt). Ook geroepen *surfer identiteitskaart*.

* &lt;*timestamp*> is de tijd in formaat YYYMMDDHHMMSS (zoals 20190821192533 voor Jaar 2019, Maand 08, Dag 21, Tijd 19 :25: 33).

* &lt;*kanaaltype*> is het kanaaltype verantwoordelijk voor de klik of de blootstelling:

   * `d` voor een klik op een DSP-advertentie (klik-via tonen)
   * `i` voor een indruk van een DSP-advertentie (display view-through)
   * `s` voor een klik op een zoekadvertentie (doorzoekklik).

Voorbeeld `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`
