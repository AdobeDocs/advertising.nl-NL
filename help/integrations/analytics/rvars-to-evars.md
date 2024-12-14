---
title: Historische gegevens verzamelen voor AMO-id's en EF-id's voor gebruik in Adobe Customer Journey Analytics
description: Leer hoe u historische gegevens voor gereserveerde variabelen in Adobe Analytics kunt verzamelen voor toekomstig gebruik in Adobe Customer Journey Analytics
feature: Integration with Adobe Analytics
source-git-commit: 4cd58fd995b3df9fb7837077108207ce910157c1
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Historische gegevens verzamelen voor AMO-id&#39;s en EF-id&#39;s voor gebruik in Adobe Customer Journey Analytics

*Advertisers met [!DNL Analytics for Advertising] en slechts Adobe Customer Journey Analytics*

Als u gereserveerde variabelen gebruikt om [ identiteitskaart van AMO en EF identiteitskaart ](ids.md) voor uw [!DNL Analytics for Advertising] integratie te vangen, dan kunt u voor een toekomstige integratie tussen Adobe Advertising en [ Adobe Customer Journey Analytics ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) voorbereiden, die volgende-generatie [!DNL analytics] oplossing van Adobe is, door uw gereserveerde variabelen voor AMO identiteitskaart en EF identiteitskaart in [ norm  [!DNL eVars] te kopiëren ](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar) zo spoedig mogelijk. Zo kunt u historische gegevens voor de AMO-id&#39;s en EF-id&#39;s verzamelen zodra u de taak hebt voltooid. Het accountteam van de Adobe laat u weten of u gereserveerde variabelen gebruikt en deze taak moet voltooien.

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## Waarom moet ik Historische Gegevens voor Customer Journey Analytics verzamelen?

Met Customer Journey Analytics kunt u gegevens van Adobe Experience Platform synchroniseren naar Adobe Analytics Analysis Workspace. Op dit moment verzendt [!DNL Analytics Data Connector] naar Experience Platform geen gegevens voor gereserveerde variabelen van [!DNL Analytics] naar Experience Platform. Dientengevolge, zijn de gegevens voor AMO IDs en EF IDs die door gereserveerde variabelen worden gevangen momenteel niet beschikbaar binnen Customer Journey Analytics. <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertising is van plan een toekomstige implementatie met Customer Journey Analytics te maken. Zodra de implementatie is vrijgegeven, moet u bij uw [!DNL Analytics for Advertising] -integratie nog steeds doorklikgegevens en (DSP gebruikers) doorkijkgegevens verzamelen met [!DNL Analytics] tracking, maar u kunt uw gegevens bekijken in zowel 1\) [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) --> als 2\) Customer Journey Analytics <!-- (Analysis Workspace using data from Experience Platform)--> als uw organisatie beide producten heeft. Wanneer de functie wordt vrijgegeven, begint het Experience Platform gegevens voor uw AMO-id en EF-id te verzamelen voor gebruik in de Customer Journey Analytics, maar er zullen geen historische gegevens bestaan vóór de releasedatum.

Nochtans, kunt u beginnen gegevens voor uw AMO IDs en EF IDs <!-- [!DNL rVars] --> eerder te verzamelen door een eenvoudige [[!DNL Analytics]  verwerkingsregel ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules) te creëren om uw AMO IDs en EF IDs <!-- [!DNL rVars] --> in [!DNL eVars] nu te kopiëren. Zodra u de verwerkingsregel hebt gemaakt, begint u gegevens voor uw AMO-id&#39;s en EF-id&#39;s op te nemen <!-- [!DNL rVars] --> zodra deze nieuwe gebeurtenissen bijhouden. De historische gegevens zijn dan beschikbaar binnen de Customer Journey Analytics zodra de implementatie beschikbaar is.

>[!NOTE]
>
>De regels van de verwerking worden toegepast slechts op nieuwe gegevens die worden ontvangen. Ze werken niet met terugwerkende kracht om gegevens uit het verleden te verzamelen.

## Kopieer de gereserveerde variabelen voor AMO-id&#39;s en EF-id&#39;s naar [!DNL eVars]

Deze stap is handmatig en moet worden uitgevoerd voor elke rapportsuite die AMO-id&#39;s en EF-id&#39;s <!-- [!DNL rVars] --> bijhoudt die u in de toekomst met Adobe Advertising wilt integreren.

1. [ creeer een verwerkingsregel ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) met de volgende montages:

   * Selecteer de rapportsuite waarvoor u AMO ID- en EF ID <!-- [!DNL rVar] -->-gegevens naar het Experience Platform wilt migreren voor gebruik door Customer Journey Analytics.

   * Gebruik voor de [!UICONTROL Rule Title] een beschrijvende naam, zoals &#39;AMO-id kopiëren en EF-id kopiëren naar Vars.&#39;

   * Voeg in de sectie [!UICONTROL Always Execute] twee handelingen toe om de nieuwe eVars te maken:

      * Voor `AMO ID`: ```Overwrite value of <new/unused eVar> with amo.s_kwcid(Context Data)```

      * Voor `EF ID`: ```Overwrite value of <new/unused eVar> With amo.ef_id(Context Data)```

   * Gebruik voor de [!UICONTROL Reason for rule] een beschrijvende notitie, zoals &quot;AMO-id en EF-id worden via Adobe Analytics Connector naar AEP verzonden.&quot;

1. Valideer de opgeslagen verwerkingsregel.

   Nadat u de verwerkingsregel hebt opgeslagen, moeten de gegevens voor de `AMO ID` en de `AMO EF ID` <!-- the existing reserved variables --> identiek zijn aan de gegevens voor de twee nieuwe Vars waarnaar ze worden gekopieerd.

   Als de nieuwe eVar `eVar142` bijvoorbeeld wordt toegewezen aan `amo.s_kwcid(Context Data)` , moeten de gegevens voor de `eVar142` en de `AMO ID` identiek zijn.

Voor meer informatie over hoe de verwerkingsregels worden toegepast, zie &quot;[ hoe de verwerkingsregels ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about) werken.&quot;

>[!MORELIKETHIS]
>
>* [ Overzicht van  [!DNL Analytics for Advertising]](overview.md)