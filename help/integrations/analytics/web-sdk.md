---
title: Met de [!DNL Last Event Service] JavaScript-bibliotheek met [!DNL Web SDK]
description: Leer de stappen om over te schakelen van het gebruiken van [!DNL Analytics] [!DNL visitorAPI] aan de [!DNL Experience Platform] [!DNL Web SDK] bibliotheek voor [!DNL Analytics for Advertising] uitvoering.
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 7501c1f8f6477a4ee6de64c64d52b1aafaf16994
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Met de [!DNL Last Event Service] JavaScript-bibliotheek met Adobe Experience Platform [!DNL Web SDK]

*Adverteerders met alleen Adobe Advertising-Adobe Analytics-integratie*

Als uw organisatie de oudere Adobe Analytics gebruikt `visitorAPI.js` bibliotheek voor gegevensverzameling, kunt u naar keuze schakelen om de [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) bibliotheek (`alloy.js`), waardoor u via de [!DNL Edge Network].

De [!DNL Analytics for Advertising] [!DNL Last Event Service] De bibliotheek van JavaScript, ongewijzigd, registreert mening-door en klik-door gebeurtenissen en stitseert hen aan de bijbehorende omzettingen gebruikend een extra identiteitskaart (`SDID`). De [!DNL Web SDK] bibliotheek, echter, levert geen [!DNL stitch ID]. Als u de opdracht [!DNL Web SDK] for [!DNL Analytics for Advertising], moet u 1) wijzigen [!DNL Last Event Service] -tags die u op uw webpagina&#39;s gebruikt en 2) uw [!DNL Web SDK] `sendEvent` opdrachten dienovereenkomstig.

## Stap 1: Bewerk uw [!DNL Last Event Service] Tags om een `[!DNL StitchID]`

In de [!DNL Analytics for Advertising] [!DNL Last Event Service] -tag die u gebruikt op uw webpagina&#39;s, voegt u code toe om de `[!DNL StitchID]` met de willekeurige id-generator die in de bibliotheek is gebundeld.

**Oudere tag:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

**Nieuwe tag:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

## Stap 2: gebruik [!DNL Web SDK] om de [!DNL StitchID] als XDM-gegevens voor [!DNL Analytics]

Voeg de volgende eigenschap in uw [!DNL Web SDK] `sendEvent` opdracht om de [!DNL StitchID] tot [!DNL Experience Edge] als [!DNL Experience Data Model] (XDM) gegevens voor [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] gebruikt de waarde als een `SDID`.

**Toe te voegen eigenschap:**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**Voorbeeld:**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [Overzicht van [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-code voor [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
