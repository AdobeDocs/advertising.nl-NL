---
title: Historische gegevens verzamelen voor AMO-id's en EF-id's voor gebruik in Adobe Customer Journey Analytics
description: Leer hoe u historische gegevens voor gereserveerde variabelen in Adobe Analytics kunt verzamelen voor toekomstig gebruik in Adobe Customer Journey Analytics
feature: Integration with Adobe Analytics
exl-id: 1f8fa139-f146-426b-b0c4-079f8e2de56c
source-git-commit: c1701505be0a1efa6db15edcf21adf80880bad8b
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 0%

---

# Historische gegevens verzamelen voor AMO-id&#39;s en EF-id&#39;s voor gebruik in Adobe Customer Journey Analytics

*Advertisers met [!DNL Analytics for Advertising] en slechts Adobe Customer Journey Analytics*

<!-- Solution built but not tested. Move to the CJA chapter once it's available?  If so, then create a redirect. -->

Als u gereserveerde variabelen gebruikt om [&#x200B; identiteitskaart van AMO en EF identiteitskaart &#x200B;](ids.md) voor uw [!DNL Analytics for Advertising] integratie te vangen, dan kunt u uw gegevens voor de integratie tussen Adobe Advertising en [&#x200B; Adobe Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-overview) voorbereiden, die volgende-generatie [!DNL analytics] oplossing van Adobe is, door uw gereserveerde variabelen voor AMO identiteitskaart en EF identiteitskaart in [&#x200B; norm  [!DNL eVars] te kopiëren &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/components/dimensions/evar) zo spoedig mogelijk. Zo kunt u historische gegevens voor de AMO-id&#39;s en EF-id&#39;s verzamelen zodra u de taak hebt voltooid. Uw Adobe-accountteam zal u laten weten of u gereserveerde variabelen gebruikt en deze taak moet voltooien.

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## Waarom moet ik historische gegevens verzamelen voor Customer Journey Analytics?

Met Customer Journey Analytics kunt u gegevens van Adobe Experience Platform synchroniseren naar [!DNL Workspace] . Op dit moment verzendt [!DNL Analytics Data Connector] naar Experience Platform geen gegevens voor gereserveerde variabelen van [!DNL Analytics] naar Experience Platform. Dientengevolge, zijn de gegevens voor AMO IDs en EF IDs die door gereserveerde variabelen worden gevangen niet beschikbaar binnen Customer Journey Analytics. <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertising bouwt een oplossing om de gegevens automatisch naar Customer Journey Analytics te verzenden. Zodra de oplossing is vrijgegeven, zal Adobe Advertising gegevens voor uw AMO-id en EF-id voor gebruik in Customer Journey Analytics verzenden, maar er zullen geen historische gegevens voor de releasedatum bestaan.

Nochtans, kunt u beginnen gegevens voor uw AMO IDs en EF IDs <!-- [!DNL rVars] --> eerder te verzamelen door een eenvoudige [[!DNL Analytics]  verwerkingsregel &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules) te creëren om uw AMO IDs en EF IDs <!-- [!DNL rVars] --> in [!DNL eVars] nu te kopiëren. Zodra u de verwerkingsregel hebt gemaakt, begint u gegevens voor uw AMO-id&#39;s en EF-id&#39;s op te nemen <!-- [!DNL rVars] --> zodra deze nieuwe gebeurtenissen bijhouden. De historische gegevens zijn dan beschikbaar in Customer Journey Analytics zodra de oplossing beschikbaar is.

>[!NOTE]
>
>* Met ingang van 28 februari 2025 worden doorklikgegevens bijgehouden, maar geen doorkijkgegevens.
>* De regels van de verwerking worden toegepast slechts op nieuwe gegevens die worden ontvangen. Ze werken niet met terugwerkende kracht om gegevens uit het verleden te verzamelen.

## Kopieer de gereserveerde variabelen voor AMO-id&#39;s en EF-id&#39;s naar [!DNL eVars]

Deze stap is handmatig en moet worden uitgevoerd voor elk rapportpakket dat AMO-id&#39;s en EF-id&#39;s <!-- [!DNL rVars] --> bijhoudt die u in de toekomst met Adobe Advertising wilt integreren.

1. [&#x200B; creeer een verwerkingsregel &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) met de volgende montages:

   * Selecteer de rapportsuite waarvoor u AMO ID- en EF-ID <!-- [!DNL rVar] -->-gegevens naar Experience Platform wilt migreren voor gebruik door Customer Journey Analytics.

   * Gebruik voor de [!UICONTROL Rule Title] een beschrijvende naam, zoals &#39;AMO-id kopiëren en EF-id kopiëren naar Vars.&#39;

   * Voeg in de sectie [!UICONTROL Always Execute] twee handelingen toe om de nieuwe eVars te maken:

      * Voor `AMO ID` :

         1. Selecteer **overschrijven de waarde van**.
         1. Selecteer *\ &lt;the new/unused eVar\>*.
         1. Selecteer **de Parameter van het Koord van de Vraag**.
         1. Voer `s_kwcid` in.

        Voorbeeld: ```Overwrite the value of rVar10 with Query String Parameter s_kwcid```

      * Voor `EF ID` :

         1. Selecteer **overschrijven de waarde van**.
         1. Selecteer *\ &lt;the new/unused eVar\>*.
         1. Selecteer **de Parameter van het Koord van de Vraag**.
         1. Voer `ef_id` in.

        Voorbeeld: `Overwrite the value of rVar11 with Query String Parameter ef_id`

   * Gebruik voor de [!UICONTROL Reason for rule] een beschrijvende notitie, zoals &quot;AMO-id en EF-id worden via Adobe Analytics-connector naar AEP verzonden.&quot;

1. Valideer de opgeslagen verwerkingsregel.

   Nadat u de verwerkingsregel hebt opgeslagen, moeten de gegevens voor de `AMO ID` en de `AMO EF ID` <!-- the existing reserved variables --> identiek zijn aan de gegevens voor de twee nieuwe Vars waarnaar ze worden gekopieerd.

   Als de nieuwe eVar `eVar142` bijvoorbeeld wordt toegewezen aan `amo.s_kwcid(Context Data)` , moeten de gegevens voor de `eVar142` en de `AMO ID` identiek zijn.

Voor meer informatie over hoe de verwerkingsregels worden toegepast, zie &quot;[&#x200B; hoe de verwerkingsregels &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about) werken.&quot;

>[!MORELIKETHIS]
>
>* [&#x200B; Overzicht van  [!DNL Analytics for Advertising]](overview.md)
