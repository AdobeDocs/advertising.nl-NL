---
source-git-commit: 92bf7768be91e75f029e1577c7f4e7e790c5a934
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---
# Fragmenten

## Sjabloonveld bijhouden voor Google Ads-entiteiten {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

**[!UICONTROL Tracking Template]:** (Optioneel) De URL voor reeksspatiëring of reeksspatiëring, die alle omleidingen en volgparameters van een extern domein opgeeft en ook de URL van de laatste/landingspagina in een URL insluit. [!DNL ValueTrack] parameter. Voorbeeld: `{lpurl}?source={network}&id=5` of `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` om een omleiding op te nemen.

Voor het bijhouden van Adoben Advertising voor conversie, die wordt toegepast wanneer de instellingen voor de campagne &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel vooraf fixeert automatisch zijn eigen omleiding en het volgen code wanneer u sparen het verslag.

* Zie voor ondersteunde parameters om de laatste URL in te sluiten de [[!DNL Google Ads] documentatie voor de ondersteunde [!DNL ValueTrack] formaten](https://support.google.com/google-ads/answer/6305348). (Ga naar de parameters &quot;het Volgen malplaatje slechts&quot;in de sectie over &quot;Beschikbaar [!DNL ValueTrack] Parameters.&quot;)

* U kunt optioneel URL-parameters en aangepaste parameters die zijn gedefinieerd voor de campagne opnemen, gescheiden door en-tekens (&amp;), zoals {lpurl}?matchtype={matchtype}&amp;apparaat={device}.

* U kunt desgewenst omleidingen en tekstspatiëring van derden toevoegen.

>[!NOTE]
>
>* Vermijd het gebruik van macro&#39;s, die niet worden vervangen door klikken van bronnen die parallelle tracking mogelijk maken. Als de adverteerder macro&#39;s moet gebruiken, moet het accountteam van de Adobe samenwerken met Klantenondersteuning of het implementatieteam om deze toe te voegen.
>* De volgende sjabloon op het meest granulaire niveau overschrijft de waarden op alle hogere niveaus. Als zowel de accountinstellingen als de trefwoordinstellingen bijvoorbeeld een waarde bevatten, wordt de trefwoordwaarde toegepast.
>* Als u een trackingsjabloon bijwerkt op advertentie-, sitelink- of trefwoordniveau, worden de relevante advertenties opnieuw verzonden voor revisie. U kunt de trackingsjablonen op account-, campagne- of advertentieniveau bijwerken zonder uw advertenties opnieuw ter goedkeuring in te dienen.

## Sjabloonveld bijhouden voor [!DNL Microsoft Advertising] entiteiten {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Optioneel) De URL voor reeksspatiëring of reeksspatiëring, die alle omleidingen en volgparameters van het niet-landende domein opgeeft en ook de URL van de laatste/landingspagina in een parameter insluit. Voorbeeld: `{lpurl}?source={network}&id=5` of `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` om een omleiding op te nemen.

Voor het bijhouden van Adoben Advertising voor conversie, die wordt toegepast wanneer de instellingen voor de campagne &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel vooraf fixeert automatisch zijn eigen omleiding en het volgen code wanneer u sparen het verslag.

* Zie voor ondersteunde parameters om de laatste URL in te sluiten de [[!DNL Microsoft Advertising] documentatie over parameters die de uiteindelijke URL aangeven](https://help.ads.microsoft.com/#apex/3/en/56799).

* U kunt optioneel URL-parameters en aangepaste parameters die zijn gedefinieerd voor de campagne opnemen, gescheiden door en-tekens (&amp;), zoals {lpurl}?matchtype={matchtype}&amp;apparaat={device}.

* U kunt desgewenst omleidingen en tekstspatiëring van derden toevoegen.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* De volgende sjabloon op het meest granulaire niveau overschrijft de waarden op alle hogere niveaus. Als zowel de accountinstellingen als de trefwoordinstellingen bijvoorbeeld een waarde bevatten, wordt de trefwoordwaarde toegepast.
>* U kunt de trackingsjablonen op elk niveau bijwerken zonder uw advertenties opnieuw ter goedkeuring in te dienen.

## Tekst en sjabloon - Opmerking waarin wordt uitgelegd hoe u een dynamische parameter invoegt {#inventory-feed-template-insert-dynamic-parameter}

Als u een kolomnaam of wijzigingengroep wilt invoegen als een dynamische parameter, klikt u in het invoerveld en vervolgens op een kolomnaam in de kolomlijst of een [wijzigingnaam](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) in de lijst Modifiers. Als u de [!DNL Param1] of [!DNL Param2] variabele, voer de waarde in `{param1:default text}` of `{param2:default text}`, waarbij &#39;standaardtekst&#39; tekst is die wordt gebruikt als de parameterkolom in het feed-bestand leeg is voor een advertentierij.

## Tekst en sjabloon - Opmerking waarin wordt uitgelegd hoe u een advertentieklanter invoegt {#inventory-feed-template-insert-ad-customizer}

Als u een advertentieklanter wilt invoegen, gebruikt u de volgende indelingen, waarbij `Default text` is een optionele waarde die moet worden ingevoegd wanneer uw feed geen geldige waarde bevat:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, zoals `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, zoals `{CUSTOMIZER.Discount:10%}`
