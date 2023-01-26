---
title: Problemen oplossen
description: Verwijzing gemeenschappelijke prestatieskwesties en zie hoe te om hen problemen op te lossen.
feature: DSP Optimization
exl-id: b87f8556-1908-40c1-9f98-fbdc6d9b59b1
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Problemen oplossen

| Probleem | Mogelijke oorzaak | Te nemen handelingen |
| --- | --- | --- |
| Geen uitgaven voor plaatsing | De plaatsing bevat geen advertenties en/of de advertenties zijn niet actief. | Controleer of alle verwachte advertenties zijn gekoppeld aan de plaatsing en zijn goedgekeurd en actief.<br><br>Zie ook of de plaatsing een aangepast advertentieschema bevat, waardoor de vliegperiode voor elke advertentie kan worden beperkt. Klik op  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]** naast de plaatsingsnaam. |
|  | De betrokken datums vallen niet binnen de geconfigureerde vluchtdatums. | Controleer of de vluchtdatums geldig zijn op de campagne, het pakket en het plaatsingsniveau &#x200B; s. |
|  | Het begrotingsdoel is bereikt en/of is niet hoog genoeg. | Controleer de budgetinstellingen op de campagne-, pakket- en plaatsingsniveaus. |
|  | De rekening heeft niet genoeg financiering. | Ga naar **[!UICONTROL Settings]** > **[!UICONTROL Account]** en bekijk de hoeveelheid [!UICONTROL Usable Funds]. Neem contact op met uw [!DNL Adobe] accountteam. |
|  | Er is geen voorraad beschikbaar. | Controleren of de opgegeven inventarisbronnen ([!UICONTROL Public], [!UICONTROL Private], of [!UICONTROL On Demand]) zijn:<ul><li>Correcte instelling.</li><li>Actief en via veilingen verzenden.</li><li>Compatibel met het toepasselijke advertentie- en plaatsingstype.</li></ul><br>Als de inventarisbronnen allemaal geldig en actief zijn, richt u zich waar mogelijk op aanvullende of alle inventarisbronnen. |
|  | Er zijn geen gebruikers beschikbaar. | Controleer of de opgegeven doelgroepen voldoende actieve gebruikers bevatten. Als ze dat niet doen, breidt u de doelen uit door meer publiek toe te voegen. |
| Lage uitgaven voor plaatsing | De [!UICONTROL Non Bids] in het rapport voor plaatsingsdiagnostiek worden mogelijke redenen getoond waarom er geen bod is uitgebracht. | [Controleer de [!UICONTROL Non Bids] verslag](/help/dsp/campaign-management/reports/placement-diagnostics.md) om te begrijpen waarom de plaatsing niet heeft geboden.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | De plaatsing gebruikt [filters voor vooraf bieden](/help/dsp/campaign-management/placements/placement-settings.md) die limiet voor biedingen. | Verlaag de drempelwaarden van de filters voor het vooraf bieden met 5% om de balans tussen besteding en prestaties te beoordelen. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Houd er rekening mee dat het gebruik van meerdere plaatsingsdoelen, zoals voorbiedingsfilters, geo&#39;s, voorraad en soorten publiek, het bieden en uitgeven van objecten cumulatief kan beperken. |
|  | De prijs van de plaatsing is laag. | De [!UICONTROL Max Bid] verbetering van het win - winpercentage .<br><br><b>OPMERKING:</b> De inventarisprijzen kunnen variëren afhankelijk van de doelgerichtheid van de plaatsing.<br><br>Een 10%-win-percentage wordt als gezond beschouwd. |
|  | Er is een laag aantal voorraden beschikbaar. | Indien mogelijk aanvullende of alle inventarisbronnen als doel instellen.<br><br>Houd er rekening mee dat het gebruik van meerdere plaatsingsdoelen, zoals voorbiedingsfilters, geo&#39;s, voorraad en soorten publiek, het bieden en uitgeven van objecten cumulatief kan beperken. |
|  | Er zijn weinig gebruikers beschikbaar. | Controleer of de opgegeven doelgroepen voldoende actieve gebruikers bevatten. Als ze dat niet doen, breidt u de doelen uit door meer publiek toe te voegen.<br><br>Houd er rekening mee dat het gebruik van meerdere plaatsingsdoelen, zoals voorbiedingsfilters, geo&#39;s, voorraad en soorten publiek, het bieden en uitgeven van objecten cumulatief kan beperken. |
|  | Het pakket bevat een groot aantal actieve plaatsingen. | Het aantal actieve stages binnen het pakket verminderen of het totale budget verhogen.<br><br>Als het pakket veel plaatsen maar niet genoeg budget heeft, kan DSP mogelijk niet genoeg budget aan elke plaatsing toewijzen. Elke plaatsing moet de mogelijkheid hebben om ten minste 2 USD/dag te besteden. Als uw pakket bijvoorbeeld een budget van 10 dollar per dag heeft, kunt u het beste vijf of minder plaatsen opnemen. &#x200B; |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Plaatsingsinstellingen](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Pakketinstellingen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Campagne-instellingen](/help/dsp/campaign-management/campaigns/campaign-settings.md)

