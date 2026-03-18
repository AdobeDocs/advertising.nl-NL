---
title: Voorbiedingsfilters op plaatsingsniveau en hoe deze te gebruiken
description: Verwijs naar de beschikbare voorbiedingsfilters op plaatsingsniveau en zie hoe u deze kunt gebruiken.
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: 4b7d525eb944545dfceaf4dec94199e188bb2ab2
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Voorbiedingsfilters op plaatsingsniveau en hoe deze te gebruiken

| Filter voor vooraf bieden | Beschrijving | Wanneer gebruikt u dit filter |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Hiermee stelt u een minimale voorspellingsdrempel in voor de waarschijnlijkheid dat een veiling een doorklikken tot gevolg kan hebben. Als u de drempel bijvoorbeeld instelt op 0,1%, biedt u alleen veilingen als de voorspelde waarschijnlijkheid van een klik groter is dan of gelijk is aan 0,1%.<br><br><b> Nota:</b> de Filters worden toegepast vóór optimalisatiedoelstellingen. Als gevolg hiervan kunnen zeer strikte filters uitgaven voorkomen. | Gebruik wanneer u een minimumKPI-doel voor doorkliktarief (CTR) hebt en uw budget niet wilt besteden wanneer CTR onder de drempel is. Dit filter kan vrij restrictief zijn, zodat is het belangrijk om realistische doelstellingen te plaatsen. Afhankelijk van andere beperkingen op de plaatsing, is een doel van 0,03 - 07% over het algemeen een goed uitgangspunt. U kunt dit naar wens op siteniveau optimaliseren om de metingen te verbeteren.<br><br> als uw doel minimaal CTR en best mogelijke CPM moet bereiken, dan is de geadviseerde opstelling een [!UICONTROL Click Through Rate] filter met het optimalisatiedoel &quot;[!UICONTROL Lowest CPM] te combineren.&quot; Als uw doel een maximum CPM zonder echt voordeel voor het overbereiken, en een minimum CTR is, dan kan het binden van een [!UICONTROL Click Through Rate] filter met het optimalisatiedoel &quot; [!UICONTROL Always Max Bid + Highest CTR]&quot;passender zijn. |
| [!UICONTROL 100% Completion Rate] | Hiermee stelt u een vereiste minimale voltooiingsfactor in waaraan moet worden voldaan voordat je op een afbeelding biedt. | Gebruik dit filter wanneer het belangrijkste doel van de campagne voltooiingspercentages is. Factor in andere het richten parameters, maar 65% is het geadviseerde beginnende percentage. |
| [!UICONTROL Player Size - Adobe] | Hiermee stelt u een vereiste minimale spelergrootte in met behulp van gegevens uit DSP. Je kunt op een indruk bieden wanneer aan de drempelwaarde voor [!UICONTROL Player Size] is voldaan. | Gebruik deze optie om te zorgen dat u de spelervoorraad voor een volledige aflevering aanbiedt met behulp van gegevens van DSP. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Hiermee stelt u een vereiste minimale spelergrootte in met behulp van gegevens uit [!DNL Moat] of [!DNL Integral Ad Science] ([!DNL IAS]). Je kunt op een indruk bieden wanneer aan de drempelwaarde voor [!UICONTROL Player Size] is voldaan. | Gebruik deze optie om ervoor te zorgen dat u de spelervoorraad voor volledige uitlevering aanbiedt met platformafmetingen [!DNL Moat] of [!DNL IAS] .<br><br><b> Nota:</b> gebruik dit filter slechts wanneer de campagne wordt gevormd om [!DNL Moat] of [!DNL IAS] gegevens te gebruiken. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Hiermee stelt u een minimaal weergavepercentage in met DSP-weergavegetallen en -metingen. Je kunt op een indruk bieden wanneer de opgegeven drempel is bereikt.<br><br><b> Nota&#39;s:</b><ul><li>Als de [!UICONTROL Viewability Sensitivity] instelling van de campagne &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]&quot; is, wordt de meetstandaard voor de [!DNL Media Rating Council] -weergave (MRC) gebruikt voor de campagne. Als de instelling [!UICONTROL Viewability Sensitivity] &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]&quot; is, wordt de meetstandaard voor de weergave van [!DNL GroupM] gebruikt voor de campagne.</li><li>Adobe-meetdefinities verschillen van definities van derden, zodat er kleine verschillen kunnen zijn met gegevens van derden.</li></ul> | U kunt het beste de optimalisatiedoelstelling en eventuele filterinstellingen vóór het bieden afstemmen op de instelling voor [!UICONTROL Viewability Sensitivity] van de campagne. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [&#x200B; hoe DSP Uw campagnes optimaliseert &#x200B;](optimization-how-dsp-optimizes-campaigns.md)
>* [&#x200B; de Montages van het Pakket &#x200B;](/help/dsp/campaign-management/packages/package-settings.md)
>* [&#x200B; Montages van de Plaatsing &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)
>* [&#x200B; Montages van de Campagne &#x200B;](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [&#x200B; Doelstellingen van de optimalisering en hoe te om hen te gebruiken &#x200B;](optimization-goals.md)
