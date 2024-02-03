---
source-git-commit: 24aa1afe9611ca6ae46795c9bca2964e1d9c4f97
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---
# Apparaatveld in GGL- en MS-campagne- en ad-groepinstellingen

**[!UICONTROL Devices]:** (Optioneel; niet beschikbaar voor [!DNL Google Ads] maximale prestatiecampagnes of [!DNL Microsoft Advertising] video- of CTV-videobads) Bodaanpassingen configureren voor verschillende apparaattypen, als percentages van het bod op trefwoordniveau. Als het bod op het trefwoordniveau bijvoorbeeld 1 USD is en het bod voor smartphones 50% is, is het bod op de smartphone 1,50 USD. Standaard worden geen waarden ingevoerd (Bodaanpassing=0) en alle apparaten worden bij het trefwoordbod opgegeven.

Voor [!DNL Google Ads]Geldige percentages kunnen -100 voor smartphones en tablets bevatten (om niet te bieden voor het apparaattype) en van -90 tot 900 voor alle apparaattypen.

Voor [!DNL Microsoft Advertising]Geldige percentages kunnen zijn:

* Smartphones en tablets: -100 (om niet te bieden voor het apparaattype) en van -90 tot 900
* Desktop: van 0 tot 900

>[!NOTE]
>* De instellingen op advertentieniveau op groepsniveau overschrijven de instellingen op campagnereniveau. Nochtans, als u een apparaat op campagneniveau uitsluit, dan kunt u niet de uitsluiting op het niveau van de ad groep met voeten treden.
>* Als u deze campagne toewijst aan een standaard geoptimaliseerde portfolio, bepaalt Search, Social &amp; Commerce automatisch het basisbod op trefwoordniveau om het portfolio te helpen zijn doel te bereiken. Het advertentienetwerk past dan het bod zoals gespecificeerd voor verschillende apparatentypes aan.
>* (Voor alle campagnes/advertentiegroepen, behalve voor [!DNL Microsoft Advertising] ad groepen in het publieksnetwerk) Als u deze campagne toewijst aan een standaard geoptimaliseerde portefeuille die aan &quot;[!UICONTROL Auto-optimize Bid Adjustment Values],&quot; wijzigt de optimalisatiefunctie de opgegeven apparaatbodaanpassingen op ad-groepsniveau, zolang de ideale waarde die wordt berekend, binnen de minimum- en maximumwaarden valt die zijn opgegeven in de portfolioinstellingen en de advertentiegroep biedt voor het apparaattype niet uit.
