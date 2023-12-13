---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---
# Trackingsjabloonveld voor Microsoft-advertentie-entiteiten

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Optioneel; niet beschikbaar voor alle entiteiten) De URL voor het bijhouden van het sjabloon of de URL voor het bijhouden van de gegevens, waarmee alle omleidingen en volgparameters van het niet-landende domein worden opgegeven en ook de URL van de laatste/landingspagina wordt ingesloten in een parameter. Voorbeeld: `{lpurl}?source={network}&id=5` of `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` om een omleiding op te nemen.

Voor het bijhouden van Adoben Advertising voor conversie, die wordt toegepast wanneer de instellingen voor de campagne &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel vooraf fixeert automatisch zijn eigen omleiding en het volgen code wanneer u sparen het verslag.

* Zie voor ondersteunde parameters om de laatste URL in te sluiten de [[!DNL Microsoft Advertising] documentatie over parameters die de uiteindelijke URL aangeven](https://help.ads.microsoft.com/#apex/3/en/56799).

* U kunt optioneel URL-parameters en aangepaste parameters die zijn gedefinieerd voor de campagne opnemen, gescheiden door en-tekens (&amp;), zoals {lpurl}?matchtype={matchtype}&amp;apparaat={device}.

* U kunt desgewenst omleidingen en tekstspatiëring van derden toevoegen.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* De volgende sjabloon op het meest granulaire niveau overschrijft de waarden op alle hogere niveaus. Als zowel de accountinstellingen als de trefwoordinstellingen bijvoorbeeld een waarde bevatten, wordt de trefwoordwaarde toegepast.
>* U kunt de trackingsjablonen op elk niveau bijwerken zonder uw advertenties opnieuw ter goedkeuring in te dienen.
