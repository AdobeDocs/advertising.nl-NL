---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---
# Veld Parameters toevoegen in account- en campagne-instellingen

**[!UICONTROL Append Parameters]:** (Optioneel) Eventuele aanvullende volgparameters die aan de basis-URL&#39;s moeten worden toegevoegd.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. De toevoegingsparameters op adverteerderniveau worden standaard opgenomen op het accountniveau en het campagneniveau, maar u kunt een van beide overschrijven.

U kunt elke statische tekstreeks gebruiken, inclusief parameters voor tekstspatiëring van derden, of een van de [ondersteunde tracking-parameters](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md), die een geschikte gegevenswaarde in de basis-URL invoegt.

Scheid meerdere parameters met komma&#39;s of ampersands (&amp;). Geneste haakjes worden niet ondersteund.

**Opmerkingen:**

* Wijzigingen in toevoegingsparameters worden niet door de [!UICONTROL Auto Upload] optie. Als u de toevoegingsparameters voor bestaande basis-URL&#39;s wijzigt, worden er niet automatisch nieuwe URL&#39;s gegenereerd. Voeg de nieuwe parameters toe door een bulksbladbestand voor de account of campagne te downloaden en het [!UICONTROL Base URL/Final URL] velden, en uploaden en posten van het bulksblad.

* (Voeg netwerken met parallelle tracking toe) Gebruik geen macro&#39;s, die niet worden vervangen door klikken van bronnen die parallelle tracking mogelijk maken. Als de adverteerder macro&#39;s moet gebruiken, moet het accountteam van Adobe samenwerken met de klantenondersteuning of het implementatieteam om deze toe te voegen.

* (Adverteerders met een Adobe Advertising-Adobe Analytics-integratie) Om een `s_kwcid` parameter voor het verzenden van gegevens over Zoeken, Sociale Zaken en Handel naar [!DNL Analytics], zie de [en netwerkspecifieke indelingen](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md). Het is niet nodig om de parameter voor [!DNL Google Ads] en [!DNL Microsoft Advertising] accounts met een server-side s\_kwcid-implementatie.
