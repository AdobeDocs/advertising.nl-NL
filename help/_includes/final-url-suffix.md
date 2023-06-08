---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# Definitie van laatste URL-achtervoegsel

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** ([!DNL Google Ads] en [!DNL Microsoft Advertising] alleen rekeningen; (facultatief) om het even welke parameters om aan het eind van definitieve URLs aan spoorinformatie toe te voegen; omvat alle parameters die uw zaken moeten volgen. Voorbeeld:`param1=value1&param2=value2`

In accounts die gebruikmaken van het bijhouden van Adobe-advertenties, moet het achtervoegsel de klikidentificatie van het advertentienetwerk bevatten (`msclkid` for [!DNL Microsoft Advertising]; `gclid` for [!DNL Google Ads]).

Accounts met een Adobe Analytics-integratie moeten de parameter s_kwcid gebruiken. Als de rekening een server-kant s_kwcid implementatie heeft, dan wordt de parameter automatisch toegevoegd wanneer een gebruiker een advertentie klikt; anders, moet u het hier manueel toevoegen. Zie de [vereiste achtervoegselformaten voor [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) en [vereiste achtervoegselformaten voor [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Dit veld wordt niet bijgewerkt door de [!UICONTROL Auto Upload] instelling voor tekstspatiëring.
>* De laatste URL-achtervoegsels op lagere niveaus overschrijven het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Om een achtervoegsel op het niveau van de advertentiegroep of lager te vormen, gebruik de redacteur van het ad netwerk.

