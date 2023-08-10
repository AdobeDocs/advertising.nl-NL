---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# Definitie van laatste URL-achtervoegsel

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** ([!DNL Google Ads] en [!DNL Microsoft Advertising] alleen accounts; optioneel) Alle parameters die aan het einde van de uiteindelijke URL&#39;s moeten worden toegevoegd om informatie bij te houden; bevatten alle parameters die uw bedrijf moet bijhouden. Voorbeeld:`param1=value1&param2=value2`

In accounts waarin Adobe Advertising conversie bijhouden wordt gebruikt, moet het achtervoegsel de klikidentificatie van het advertentienetwerk bevatten (`msclkid` for [!DNL Microsoft Advertising]; `gclid` for [!DNL Google Ads]).

Accounts met een Adobe Analytics-integratie moeten de [AMO-id](/help/integrations/analytics/ids.md) parameter. Als de account een AMO-id-implementatie aan de serverzijde heeft, wordt de parameter automatisch toegevoegd wanneer een gebruiker op een advertentie klikt; anders moet u deze hier handmatig toevoegen. Zie de [vereiste achtervoegselformaten voor [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) en [vereiste achtervoegselformaten voor [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Dit veld wordt niet bijgewerkt door de [!UICONTROL Auto Upload] instelling voor tekstspatiëring.
>* De laatste URL-achtervoegsels op lagere niveaus overschrijven het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Om een achtervoegsel op het niveau van de advertentiegroep of lager te vormen, gebruik de redacteur van het advertentienetwerk.
