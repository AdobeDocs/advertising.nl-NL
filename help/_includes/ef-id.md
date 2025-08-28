---
source-git-commit: 47b5d399d4a5daa8832456abc32fff68e694abe9
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---
# Adobe Advertising EF-id&#39;s

## Adobe Advertising EF-id&#39;s

De EF-id is een unieke token die Adobe Advertising gebruikt om activiteit te koppelen aan een online klik of advertentie. EF identiteitskaart wordt opgeslagen in [ een  [!DNL Analytics] [!DNL eVar] ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=nl-NL) of [!DNL rVar] (gereserveerde [!DNL eVar]) afmeting (Adobe Advertising EF identiteitskaart) en volgt elke en klik of blootstelling op individuele browser of apparatenniveau. EF-id&#39;s fungeren voornamelijk als sleutels voor het verzenden van [!DNL Analytics] -gegevens naar Adobe Advertising voor rapportage en optimalisatie van biedingen in Adobe Advertising.

### EF-ID-indelingen {#ef-id-formats}

>[!NOTE]
>
>EF-id&#39;s zijn hoofdlettergevoelig. Als een [!DNL Analytics] -implementatie het bijhouden van URL&#39;s in kleine letters dwingt, herkent Adobe Advertising de EF-id niet. Dit is van invloed op Adobe Advertising-biedingen en -rapporten, maar heeft geen invloed op Adobe Advertising-rapportage binnen [!DNL Analytics] .

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
