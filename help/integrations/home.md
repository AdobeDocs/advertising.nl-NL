---
title: Nieuwe functies
description: Meer informatie over updates van de integratie tussen Adobe Advertising en andere producten en services in Adobe Experience Cloud.
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
source-git-commit: ae93aff0056e58fd4427620d2eab76330a73039c
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# Nieuwe functies

De volgende functies zijn nieuw of onlangs gewijzigd.

| Datum | Functie | Beschrijving | Voor meer informatie |
| ---- | ------- | ----------- | -------------------- |
| 26 maart 2025 | [!DNL Adobe Analytics for Advertising] | (Adverteerders met de optie Zoeken, Sociaal en Commerce; [!DNL Microsoft Advertising] accounts en [!DNL Adobe Analytics for Advertising] ) Voor accounts met de optie [!UICONTROL Auto Upload] tracking is de indeling van de parameter AMO ID in de achtervoegsels van de bestemmingspagina voor alle typen campagnes bijgewerkt naar de meest recente indeling. Eerder werden de maximale prestatiecampagnes voor de meeste accounts gemigreerd naar de nieuwe indeling.<br><br> voor rekeningen zonder de [!UICONTROL Auto Upload] het volgen optie die niet reeds aan het nieuwe formaat waren gemigreerd, nochtans, moet u elk het landende paginaachtervoegsel manueel bijwerken om het nieuwe formaat van identiteitskaart van AMO te omvatten.<br><br> Huidige indeling: `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}` | Zie &quot;[ Overzicht van  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)&quot;en [ de formaten van identiteitskaart van AMO ](/help/integrations/analytics/ids.md#amo-id-formats).&quot; |
| 13 november 2024 | [!DNL Analytics for Advertising] | (Adverteerders met [!DNL Analytics for Advertising] en Adobe Customer Journey Analytics) Als u gereserveerde variabelen gebruikt om uw AMO-id&#39;s en EF-id&#39;s vast te leggen, kunt u zich voorbereiden op een toekomstige integratie tussen Adobe Advertising en Adobe Customer Journey Analytics door de gereserveerde variabelen voor de AMO-id en de EF-id zo snel mogelijk naar de standaard-id [!DNL eVars] te kopiëren. Hierdoor kunnen historische gegevens voor de AMO-id&#39;s en EF-id&#39;s worden verzameld zodra u de taak hebt voltooid. De historische gegevens zijn beschikbaar voor toekomstig gebruik. Uw Adobe-accountteam zal u laten weten of u gereserveerde variabelen gebruikt en deze taak moet voltooien. | Zie &quot;[ Historische Gegevens voor AMO IDs en EF IDs voor Gebruik in Adobe Customer Journey Analytics ](/help/integrations/analytics/rvars-to-evars.md) verzamelen.&quot; |
| Release 29 oktober 2024 | [!DNL Adobe Analytics for Advertising] | (Adverteerders met [!DNL Adobe Analytics for Advertising] - en [!DNL Microsoft Advertising] max. campagnes voor prestaties) Gegevens op groepsniveau voor de maximale prestaties zijn nu beschikbaar in Adobe Analytics wanneer u een nieuwe AMO-id-parameter ([!DNL s_kwcid] ) implementeert in URL&#39;s voor de maximale prestatiecampagnes, die geen advertenties en trefwoorden bevatten. Voor de meeste accounts met maximale prestatiecampagnes is het bijhouden al gemigreerd naar de nieuwe indeling. Voor accounts met maximale prestatiecampagnes zonder de optie [!UICONTROL Auto Upload] bijhouden die nog niet naar de nieuwe indeling zijn gemigreerd, moet u echter elk achtervoegsel van de bestemmingspagina handmatig bijwerken en de nieuwe indeling voor AMO-id opnemen.<br><br> de gegevens van Adobe Analytics voor uw prestaties maximumcampagnes zijn ook beschikbaar in Onderzoek, Sociale, &amp; Commerce. | Zie het nieuwe [ formaat van identiteitskaart van AMO ](/help/integrations/analytics/ids.md#amo-id-formats) en [ wanneer en hoe te om de parameter aan uw het volgen URLs ](/help/integrations/analytics/ids.md#amo-id-implement) toe te voegen. |
| 16 december 2023 | Help | In een nieuw document wordt uitgelegd hoe u A/B-tests instelt in [!DNL Target] voor doorklikverkeer van advertenties in Zoeken, Sociaal en Commerce en hoe u tips geeft voor het meten en visualiseren van uw tests in [!DNL Analytics] . | Zie &quot;[ A/B Tests in Adobe Target voor Onderzoek, Sociale, &amp; Advertenties van Commerce ](/help/integrations/target/ab-tests-search.md) vormen.&quot; |
| 8 augustus 2023 | [!DNL Analytics for Advertising] | Sommige metriek voor succesgebeurtenissen van [!DNL Analytics], zoals standaard, aangepaste en gereserveerde conversiemetriek en verkeersmetriek, zijn automatisch beschikbaar in DSP en in Zoeken, Sociaal en Commerce. Nu kunt u ook uw eigen succesmaatstaven configureren op basis van uw bestaande [!DNL Analytics] [!DNL eVars] - en [!DNL props] -methoden door gegevens op [!DNL eVar] - en [!DNL prop] -niveau te importeren in een aangepaste succesgebeurtenis. | Zie &quot;[ de Metriek van de Omzetting van Adobe Analytics  [!DNL eVars]  en  [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md).&quot; |
| 13 juli 2023 | Rapportage | (DSP-gebruikers met [!DNL Analytics for Advertising] ) Doorzichtopzettingen voor CTV-plaatsingen (connected TV) worden nu opgenomen in conversiegegevens die beschikbaar zijn in Adobe Analytics. | Zie de sectie over &quot;Voorbeelden van hoe te om de Integratie&quot;in &quot;[ Overzicht van  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples) te gebruiken.&quot; |
| 1 november 2022 | Help | In een nieuw document wordt uitgelegd hoe u doorklikken en doorzien van signalen kunt implementeren tussen Advertising DSP en Adobe Target, hoe u een A/B-testactiviteit instelt in [!DNL Target] voor uw DSP-advertenties en hoe u Adobe Analytics Analysis Workspace kunt instellen om de testgegevens weer te geven. | Zie &quot;[ A/B Tests in Adobe Target voor Advertising DSP Advertentie ](/help/integrations/target/ab-tests-dsp.md) vormen.&quot; |
| 17 augustus 2022 | Help | In een nieuw hoofdstuk worden alle manieren beschreven waarop Adobe Advertising is geïntegreerd met Adobe Audience Manager. | Zie het hoofdstuk op &quot;Integratie met Adobe Audience Manager,&quot;met inbegrip van een overzicht van &quot;[ Integraties van Adobe Advertising met Adobe Audience Manager ](/help/integrations/audience-manager/overview.md).&quot; |
| 27 april 2021 | [!DNL Analytics for Advertising] | Leer waarom en hoe u [!DNL Analytics for Advertising] macro&#39;s toevoegt aan uw [!DNL Google Campaign Manager 360] -advertentietags om klikgegevens naar Adobe Analytics te verzenden. | Zie &quot;[ toevoegt  [!DNL Analytics for Advertising]  Macro&#39;s aan  [!DNL Google Campaign Manager 360]  en Codes ](/help/integrations/analytics/macros-google-campaign-manager.md).&quot; |
| 19 april 2021 | [!DNL Analytics for Advertising] | Leer waarom en hoe u macro&#39;s toevoegt aan uw [!DNL Flashtalking] -advertentietags om klikgegevens naar Adobe Analytics te verzenden. | Zie &quot;[ toevoegt  [!DNL Analytics for Advertising]  Macro&#39;s aan  [!DNL Flashtalking]  en Codes ](/help/integrations/analytics/macros-flashtalking.md).&quot; |
| 27 oktober 2021 | [!DNL Analytics for Advertising] | Als uw organisatie van het gebruiken van de erfenisAdobe Analytics `visitorAPI.js` bibliotheek aan de [ Adobe Experience Platform  [!DNL Web SDK] ](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=nl-NL) bibliotheek (`alloy.js`) voor gegevensinzameling wil schakelen, moet u sommige veranderingen aanbrengen om identiteitskaart het stitching toe te laten. | Zie &quot;[ Gebruikend de  [!DNL Last Event Service]  Bibliotheek van JavaScript met Adobe Experience Platform  [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md).&quot; |
| 26 mei 2021 | Help | Het hoofdstuk &quot;[!DNL Analytics for Advertising]&quot; bevat nu een subhoofdstuk over &quot;Werken in [!DNL Analytics Marketing Channels]&quot;. | Zie: &quot;[ Grondbeginselen van de Marketing Kanalen ](/help/integrations/analytics/marketing-channels/mc-overview.md),&quot;[ Gebruikend Adobe Advertising IDs om  [!DNL Analytics Marketing Channels]  Verwerkingsregels ](/help/integrations/analytics/marketing-channels/mc-ids.md) tot stand te brengen,&quot; [ Gebruikend  [!DNL Analytics Marketing Channels]  met de Gegevens van Adobe Advertising ](/help/integrations/analytics/marketing-channels/mc-ac-data.md),&quot; en &quot;[ waarom de Gegevens van het Kanaal tussen Adobe Advertising en  [!DNL Analytics Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md) kunnen variëren.&quot; |
| 26 mei 2021 | Help | Er is een koppeling toegevoegd naar alle videozelfstudies over [!DNL Analytics for Advertising] . | Zie: &quot;[ videoleerprogramma&#39;s over de integratie van Adobe Advertising ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html?lang=nl-NL).&quot; |

{style="table-layout:auto"}

<!-- At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe Experience Cloud products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
