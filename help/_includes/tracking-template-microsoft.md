---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---
# Trackingsjabloonveld voor Microsoft-advertentie-entiteiten

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Optioneel) De URL voor reeksspatiëring of reeksspatiëring, die alle omleidingen en volgparameters van het niet-landende domein opgeeft en ook de URL van de laatste/landingspagina in een parameter insluit. Voorbeeld: `{lpurl}?source={network}&id=5` of `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` om een omleiding op te nemen.

Voor het bijhouden van reclame-conversies voor Adobe, die wordt toegepast wanneer de instellingen voor de campagne &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel vooraf fixeert automatisch zijn eigen omleiding en het volgen code wanneer u sparen het verslag.

* Voor ondersteunde parameters om de laatste URL in te sluiten, raadpleegt u de [[!DNL Microsoft Advertising] documentatie over parameters die de uiteindelijke URL aangeven](https://help.ads.microsoft.com/#apex/3/en/56799).

* U kunt naar keuze URL parameters en om het even welke douaneparameters omvatten die voor de campagne worden bepaald, door ampersands (&amp;), zoals {lpurl} worden gescheiden?matchtype={matchtype}&amp;device={device}.

* U kunt desgewenst omleidingen en tekstspatiëring van derden toevoegen.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* De het volgen malplaatje op het meest korrelige niveau treedt de waarden op alle hogere niveaus met voeten. Als zowel de accountinstellingen als de trefwoordinstellingen bijvoorbeeld een waarde bevatten, wordt de trefwoordwaarde toegepast.
>* U kunt de trackingsjablonen op elk niveau bijwerken zonder uw advertenties opnieuw ter goedkeuring in te dienen.

