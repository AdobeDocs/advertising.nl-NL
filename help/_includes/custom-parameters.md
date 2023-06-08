---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---
# Veld Aangepaste parameters in instellingen voor GGL- en MS-campagnes, instellingen voor lidstaten en groepen, en MS-multimedia en responsieve advertentie-instellingen

**[!UICONTROL Custom Parameters]:** (facultatief; alleen van toepassing op publiekscampagnes voor [!DNL Microsoft Advertising]) Naam- en waardeparen voor maximaal drie aangepaste parameters. De maximale lengte voor namen is 16 alfanumerieke tekens. de maximumlengte voor waarden is 200 tekens, inclusief ingesloten parameters.

U kunt uw namen van douaneparameters in het volgen malplaatjes voor de entiteit en zijn kindentiteiten omvatten. Wanneer een gebruiker op een relevante advertentie klikt, vervangt het ad-netwerk de parameternaam door de gedefinieerde parameterwaarde. Als u bijvoorbeeld een klantparameter maakt `{_color}=red` en uw sjabloon voor bijhouden bevat `http://tracker.example.com/?color={_color}&u={lpurl}`wordt vervolgens &quot;rood&quot; ingevoegd in de kleurparameter wanneer een gebruiker op een advertentie klikt.

Aangepaste parameters bij de advertentiegroep of ([!DNL Microsoft Advertising] alleen) overschrijf op ad-level-niveau aangepaste parameters met dezelfde naam.
