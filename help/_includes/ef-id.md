---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---
# Adobe Advertising EF-id&#39;s

## Adobe Advertising EF-id&#39;s

De EF-id is een unieke token die Adobe Advertising gebruikt om activiteit te koppelen aan een online klik of belichting op het niveau van de afzonderlijke browser of het apparaat. EF-id&#39;s fungeren voornamelijk als sleutels voor het verzenden van [!DNL Analytics] -gegevens en Customer Journey Analytics-gegevens naar Adobe Advertising voor het melden en optimaliseren van biedingen binnen Adobe Advertising.

Voor [!DNL Analytics], wordt EF identiteitskaart opgeslagen in [ an  [!DNL Analytics] [!DNL eVar] ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) of [!DNL rVar] (gereserveerde [!DNL eVar]) dimensie (Adobe Advertising EF identiteitskaart).

Voor Customer Journey Analytics, wordt EF identiteitskaart opgeslagen in het `trackingIdentities` bezit van het `conversionDetails` voorwerp, dat deel van [ uitmaakt [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension).

### EF-id-indelingen {#ef-id-formats}

Zie de [ formaten voor EF de afmetingspunten van identiteitskaart ](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-ef-id#dimension-items) in de &quot;Gids van de Componenten van Adobe Analytics.&quot;

>[!NOTE]
>
>EF-id&#39;s zijn hoofdlettergevoelig. Als een [!DNL Analytics] - of Customer Journey Analytics-implementatie URL-tracking in kleine letters forceert, herkent Adobe Advertising de EF-id niet. Dit is van invloed op Adobe Advertising-biedingen en -rapporten, maar heeft geen invloed op Adobe Advertising-rapportage binnen [!DNL Analytics] of Customer Journey Analytics.

<!-- Legacy content:

#### [!DNL Google Ads] search ads

```
{gclid}:G:s
```

where:

* `gclid` is the [!DNL Google Click ID] (GCLID).
* `s` is the network type ("s" for search).

#### [!DNL Microsoft Advertising] search ads

```
{msclkid}:G:s
```

where:

* `msclkid` is the [!DNL Microsoft Click ID] (MSCLKID).
* `s` is the network type ("s" for search).

#### Display ads and search ads on other search engines 

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

where:

* <*Adobe Advertising visitor ID*> is a unique ID per visitor (such as UhKVaAAABCkJ0mDt). Also called the *surfer ID*.

* <*timestamp*> is the time in the format YYYYMMDDHHMMSS (such as 20190821192533 for Year 2019, Month 08, Day 21, Time 19:25:33).

* <*channel type*> is the channel type responsible for the click or exposure:

    * `d` for a click on a DSP display ad (display click-through)
    * `i` for an impression of a DSP display ad (display view-through)
    * `s` for a click on a Search ad (search click-through).

Example `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

-->
