---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---
# Het veld Achtervoegsel van bestemmingspagina wordt weergegeven in instellingen voor GGL- en MS-accounts, instellingen voor campagne en enkele advertentie-instellingen

**[!UICONTROL Landing Page Suffix]:** ([!DNL Google Ads] en [!DNL Microsoft Advertising] alleen rekeningen; (facultatief) om het even welke parameters om aan het eind van definitieve URLs aan spoorinformatie toe te voegen; omvat alle parameters die uw zaken moeten volgen. Voorbeeld: `param1=value1&param2=value2`

Accounts die Adobe Advertising conversion tracking gebruiken, moeten de klikidentificatie van het advertentienetwerk bevatten (`gclid` for [!DNL Google Ads] of `msclkid` for [!DNL Microsoft Advertising]) in het achtervoegsel.

Accounts met een Adobe Analytics-integratie moeten de parameter s_kwcid gebruiken. Als de rekening een server-kant s_kwcid implementatie heeft, dan wordt de parameter automatisch toegevoegd wanneer een gebruiker een advertentie klikt; anders, moet u het hier manueel toevoegen. Zie de [vereiste achtervoegselformaten voor Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md) en [vereiste achtervoegselformaten voor Microsoft Advertising](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

**Opmerkingen:**

* Dit veld wordt niet bijgewerkt door de [!UICONTROL Auto Upload] instelling voor tekstspatiëring.

* Achtervoegsels op lagere niveaus van de bestemmingspagina hebben voorrang op het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Om een achtervoegsel op het niveau van de advertentiegroep of lager te vormen, gebruik de redacteur van het ad netwerk.
