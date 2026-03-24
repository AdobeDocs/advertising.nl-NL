---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---
# Veld Parameters toevoegen in account- en campagne-instellingen

**[!UICONTROL Append Parameters]:** (Facultatief) om het even welke extra het volgen parameters om aan basis URLs toe te voegen.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. De toevoegingsparameters op adverteerderniveau worden standaard opgenomen op het accountniveau en het campagneniveau, maar u kunt een van beide overschrijven.

U kunt om het even welk statisch tekstkoord, met inbegrip van derde volgende parameters, of om het even welke [&#x200B; gesteunde volgende parameters &#x200B;](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md) gebruiken, die een aangewezen gegevenswaarde in basisURL opnemen.

Scheid meerdere parameters met komma&#39;s of ampersands (&amp;). Geneste haakjes worden niet ondersteund.

**Nota&#39;s:**

* Wijzigingen in toevoegingsparameters worden niet bestuurd door de optie [!UICONTROL Auto Upload] . Als u de toevoegingsparameters voor bestaande basis-URL&#39;s wijzigt, worden er niet automatisch nieuwe URL&#39;s gegenereerd. Voeg de nieuwe parameters toe door een bulksbladbestand voor de account of campagne te downloaden, de [!UICONTROL Base URL/Final URL] -velden bij te werken en het bulksheet vervolgens te uploaden en te plaatsen.

* (Voeg netwerken met parallelle tracking toe) Gebruik geen macro&#39;s, die niet worden vervangen door klikken van bronnen die parallelle tracking mogelijk maken. Als de adverteerder macro&#39;s moet gebruiken, moet het Adobe-accountteam samenwerken met Customer Support of het implementatieteam om deze toe te voegen.

* (Advertisers met een integratie Adobe Advertising-Adobe Analytics) om een parameter van identiteitskaart van AMO te omvatten om Onderzoek, Sociale, &amp; gegevens van Commerce naar [!DNL Analytics] te verzenden, zie [&#x200B; ad netwerk-specifieke formaten &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items). U hoeft de parameter voor [!DNL Google Ads] - en [!DNL Microsoft Advertising] -accounts niet handmatig toe te voegen met een AMO ID-implementatie aan de serverzijde.
