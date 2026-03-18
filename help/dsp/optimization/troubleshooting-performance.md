---
title: Problemen oplossen
description: Verwijzing gemeenschappelijke prestatieskwesties en zie hoe te om hen problemen op te lossen.
feature: DSP Optimization
exl-id: b87f8556-1908-40c1-9f98-fbdc6d9b59b1
source-git-commit: 4b7d525eb944545dfceaf4dec94199e188bb2ab2
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Problemen oplossen

| Probleem | Mogelijke oorzaak | Te nemen handelingen |
| --- | --- | --- |
| Geen uitgaven voor plaatsing | De plaatsing bevat geen advertenties en/of de advertenties zijn niet actief. | Controleer of alle verwachte advertenties zijn gekoppeld aan de plaatsing en zijn goedgekeurd en actief.<br><br> ook, zie of omvat de plaatsing een douane advertentieschema, die de vliegperiode voor elke advertentie kan beperken. Als u het advertentieschema voor een plaatsing wilt weergeven vanuit de weergave Plaatsen, klikt u op **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]** naast de plaatsingsnaam. |
| | De betrokken datums vallen niet binnen de geconfigureerde vluchtdatums. | Controleer of de vluchtdatums geldig zijn op de campagne, het pakket en het plaatsingsniveau &#x200B; s. |
| | Het begrotingsdoel is bereikt en/of is niet hoog genoeg. | Controleer de budgetinstellingen op de campagne-, pakket- en plaatsingsniveaus. |
| | De rekening heeft niet genoeg financiering. | Ga naar **[!UICONTROL Settings]** > **[!UICONTROL Account]** en bekijk de hoeveelheid [!UICONTROL Usable Funds] om te zien of uw account voldoende is gefinancierd. Neem contact op met uw Adobe-accountteam als u meer middelen wilt toevoegen. |
| | Er is geen voorraad beschikbaar. | Controleer of de opgegeven inventarisbronnen ([!UICONTROL Public], [!UICONTROL Private] of [!UICONTROL On Demand]):<ul><li>Correcte instelling.</li><li>Actief en via veilingen verzenden.</li><li>Compatibel met het toepasselijke advertentie- en plaatsingstype.</li></ul><br> als de inventarisbronnen allen geldig en actief zijn, dan richt extra of alle inventarisbronnen wanneer mogelijk. |
| | Er zijn geen gebruikers beschikbaar. | Controleer of de opgegeven doelgroepen voldoende actieve gebruikers bevatten. Als ze dat niet doen, breidt u de doelen uit door meer publiek toe te voegen. |
| Lage uitgaven voor plaatsing | In het gedeelte [!UICONTROL Non Bids] van het rapport voor de plaatsingsdiagnose worden mogelijke redenen getoond waarom er geen bod is uitgebracht. | [ herzie het [!UICONTROL Non Bids] rapport ](/help/dsp/campaign-management/reports/placement-diagnostics.md) om te begrijpen waarom de plaatsing niet bood.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
| | De plaatsing gebruikt [ pre-bid filters ](/help/dsp/campaign-management/placements/placement-settings.md) die het bieden beperken. | Verlaag de drempelwaarden van de filters voor het vooraf bieden met 5% om de balans tussen besteding en prestaties te beoordelen. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br> houd in mening dat het gebruiken van veelvoudige plaatsingsdoelstellingen, zoals voorbiedingsfilters, geo&#39;s, inventaris, en publiek, het bieden en uitgeven cumulatief kan beperken. |
| | De prijs van de plaatsing is laag. | Verhoog [!UICONTROL Max Bid] om de winsnelheid te verbeteren.<br><br><b> NOTA:</b> de prijzen van de Inventaris kunnen variëren gebaseerd op het richten van de plaatsing.<br><br> het 10%-win tarief wordt beschouwd als gezond. |
| | Er is een laag aantal voorraden beschikbaar. | Indien mogelijk aanvullende of alle inventarisbronnen als doel instellen.<br><br> houd in mening dat het gebruiken van veelvoudige plaatsingsdoelstellingen, zoals voorbiedingsfilters, geo&#39;s, inventaris, en publiek, het bieden en uitgeven cumulatief kan beperken. |
| | Er zijn weinig gebruikers beschikbaar. | Controleer of de opgegeven doelgroepen voldoende actieve gebruikers bevatten. Als ze dat niet doen, breidt u de doelen uit door meer publiek toe te voegen.<br><br> houd in mening dat het gebruiken van veelvoudige plaatsingsdoelstellingen, zoals voorbiedingsfilters, geo&#39;s, inventaris, en publiek, het bieden en uitgeven cumulatief kan beperken. |
| | Het pakket bevat een groot aantal actieve plaatsingen. | Het aantal actieve stages binnen het pakket verminderen of het totale budget voor het pakket verhogen.<br><br> als het pakket vele plaatsen maar niet genoeg begroting heeft, kan DSP niet genoeg begroting aan elke plaatsing toewijzen. Elke plaatsing moet de mogelijkheid hebben om ten minste 2 USD/dag te besteden. Als uw pakket bijvoorbeeld een budget van 10 dollar per dag heeft, kunt u het beste vijf of minder plaatsen opnemen. &#x200B; |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [ Montages van de Plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md)
>* [ de Montages van het Pakket ](/help/dsp/campaign-management/packages/package-settings.md)
>* [ Montages van de Campagne ](/help/dsp/campaign-management/campaigns/campaign-settings.md)
