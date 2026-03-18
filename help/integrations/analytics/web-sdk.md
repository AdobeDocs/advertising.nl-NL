---
title: Het gebruiken van de  [!DNL Last Event Service]  bibliotheek van JavaScript met  [!DNL Web SDK]
description: Leer de stappen om van het gebruiken van de  [!DNL Analytics] [!DNL visitorAPI] bibliotheek aan de  [!DNL Experience Platform] [!DNL Web SDK] bibliotheek voor uw  [!DNL Analytics for Advertising]  implementatie over te schakelen.
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# De [!DNL Last Event Service] JavaScript-bibliotheek gebruiken met Adobe Experience Platform [!DNL Web SDK]

*Advertisers met slechts een integratie Adobe Advertising-Adobe Analytics*

Als uw organisatie de erfenisAdobe Analytics `visitorAPI.js` bibliotheek voor gegevensinzameling gebruikt, kunt u naar keuze schakelen aan het gebruiken van [ Adobe Experience Platform  [!DNL Web SDK] ](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) bibliotheek (`alloy.js`), die u toestaat om met de diverse diensten van Experience Cloud door [!DNL Edge Network] in wisselwerking te staan.

In de [!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript-bibliotheek, &#39;as-is&#39;, worden de gebeurtenissen view-through en click-through vastgelegd en worden deze met een aanvullende id (`SDID`) aan de bijbehorende conversies gekoppeld. De [!DNL Web SDK] -bibliotheek levert echter geen [!DNL stitch ID] . Als u de tag [!DNL Web SDK] for [!DNL Analytics for Advertising] wilt gebruiken, moet u 1) de tag [!DNL Last Event Service] die u gebruikt op uw webpagina&#39;s wijzigen en 2) de opdrachten [!DNL Web SDK] `sendEvent` dienovereenkomstig.

## Stap 1: bewerk de tag [!DNL Last Event Service] om een `[!DNL StitchID]` -element te genereren

Voeg in de tag [!DNL Analytics for Advertising] [!DNL Last Event Service] die u op uw webpagina&#39;s gebruikt code toe om de `[!DNL StitchID]` te genereren met behulp van de willekeurige id-generator die in de bibliotheek is gebundeld.

**Verouderde markering:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

**Nieuwe markering:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

## Stap 2: Gebruik [!DNL Web SDK] om de [!DNL StitchID] als XDM-gegevens voor [!DNL Analytics] te verzenden

Voeg de volgende eigenschap in de opdracht [!DNL Web SDK] `sendEvent` in om de gegevens [!DNL StitchID] naar [!DNL Experience Edge] as [!DNL Experience Data Model] (XDM) voor [!DNL Analytics] te verzenden. <!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] gebruikt de waarde als een `SDID` .

**Bezit om toe te voegen:**

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
>* [ Overzicht van  [!DNL Analytics for Advertising]](overview.md)
>* [ code van JavaScript voor  [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
