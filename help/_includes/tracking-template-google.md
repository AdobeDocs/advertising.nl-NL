---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---
# Sjabloonveld bijhouden voor Google Ads-entiteiten

<!-- Search CRUD and bulk edit of Google entity settings -->

**[!UICONTROL Tracking Template]:** (Optioneel) De URL voor reeksspatiëring of reeksspatiëring, die alle omleidingen en volgparameters van een extern domein opgeeft en ook de URL van de laatste/landingspagina insluit in een [!DNL ValueTrack] parameter. Voorbeeld: `{lpurl}?source={network}&id=5` of `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` om een omleiding op te nemen.

Voor het bijhouden van reclame-conversies voor Adobe, die wordt toegepast wanneer de instellingen voor de campagne &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel vooraf fixeert automatisch zijn eigen omleiding en het volgen code wanneer u sparen het verslag.

* Voor ondersteunde parameters om de laatste URL in te sluiten, raadpleegt u de [[!DNL Google Ads] documentation for the supported [!DNL ValueTrack] formaten](https://support.google.com/google-ads/answer/6305348). (Ga naar de parameters &quot;het Volgen malplaatje slechts&quot;in de sectie over &quot;Beschikbaar [!DNL ValueTrack] Parameters.&quot;)

* U kunt optioneel URL-parameters en aangepaste parameters die zijn gedefinieerd voor de campagne opnemen, gescheiden door en-tekens (&amp;), zoals {lpurl}?matchtype={matchtype}&amp;device={device}.

* U kunt desgewenst omleidingen en tekstspatiëring van derden toevoegen.

>[!NOTE]
>
>* Vermijd het gebruik van macro&#39;s, die niet worden vervangen door klikken van bronnen die parallelle tracking mogelijk maken. Als de adverteerder macro&#39;s moet gebruiken, moet het accountteam van Adobe samenwerken met de klantenondersteuning of het implementatieteam om deze toe te voegen.
>* De het volgen malplaatje op het meest korrelige niveau treedt de waarden op alle hogere niveaus met voeten. Als zowel de accountinstellingen als de trefwoordinstellingen bijvoorbeeld een waarde bevatten, wordt de trefwoordwaarde toegepast.
>* Als u een trackingsjabloon bijwerkt op advertentie-, sitelink- of trefwoordniveau, worden de relevante advertenties opnieuw verzonden voor revisie. U kunt de trackingsjablonen op account-, campagne- of advertentieniveau bijwerken zonder uw advertenties opnieuw ter goedkeuring in te dienen.
