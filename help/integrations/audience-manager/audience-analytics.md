---
title: '[!DNL Adobe] [!DNL Audience Analytics]  voor klanten van de Adobe Advertising'
description: Leer hoe u  [!DNL Adobe] [!DNL Audience Analytics] kunt gebruiken voor het maken van advertenties
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] voor klanten van de Adobe Advertising

[[!DNL Adobe] [!DNL Audience Analytics] ](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) is een integratie tussen Adobe Audience Manager en Adobe Analytics die Audience Manager klanten toestaat om segmenten naar [!DNL Analytics] voor verrijkte inzichten over plaatsactiviteit te verzenden.

Adobe Advertising klanten kunnen baat hebben bij het gebruik van [!DNL Audience Analytics] . Dankzij de integratie kunt u:

* Verstuur de blootstellingsgegevens van de Adobe Advertising rechtstreeks naar [!DNL Analytics] om het effect van de activiteit van de bovenste trechter op de activiteit van de downstreamsite te bepalen.

* Bepaal de marketingkanalen en de toegangspunten van de site op basis van de blootstellingsadvertenties van de bovenste trechter.

* Laag de integratie met [!DNL Analytics for Advertising] om derde demografische segmenten van [ Audience Manager  [!DNL Audience Marketplace] ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) met [!DNL Analytics for Advertising] gegevens voor meer inzicht over gebruikersprofielen op te nemen.

  [!DNL Audience Marketplace] biedt toegang tot gegevensfeeds van derden met abonnementmodellen voor activering, waarmee kopers gegevens naar een bestemming kunnen verzenden. Als de gegevens worden gebruikt binnen een [!DNL Analytics] -bestemming, worden geen activeringskosten toegepast.

* (Advertisers met Advertising DSP) Voeg extra blootstellingssegmenten toe voor holistische inzichten in het reisbeheer.

  Advertising DSP kan belichtingsgegevens naar Audience Manager verzenden als activeerbare signalen via de implementatie van Adobe Experience Platform of Audience Manager-tracking pixels. Door dezelfde gegevens naar [!DNL Analytics] te verzenden, kunt u geavanceerde gegevensanalyse uitvoeren. Zie &quot;[ Overzicht van de Integratie van de Gegevens van de Media van de Adobe Advertising met Adobe Audience Manager ](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;voor meer informatie.

Voor meer informatie over [!DNL Audience Analytics], met inbegrip van zijn eerste vereisten en werkschema, zie &quot;[ overzicht van het Audience Analytics ](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Voorbeelden van het gebruik van [!DNL Audience Analytics] -gegevens met Adobe Advertising-gegevens

Hieronder ziet u voorbeelden van het gebruik van de gecombineerde gegevens in [!DNL Analytics] [!DNL Analysis Workspace] .

### Zie de impact van de Activiteit van het hoger personeel op de downstreamactiviteit

Gebruik de blootstellingssegmenten van de Audience Manager om de impact van de activiteit van de bovenste schoorsteenlocatie op de activiteiten van de downstreamlocatie te zien. Neem Adobe Advertising- of externe macro-id&#39;s op in de volgende pixels om de impact op een gedetailleerd niveau te volgen, van het campagmeniveau tot het niveau van de site waarop de gebruiker is weergegeven.

Belangrijkste voordelen:

* De blootstelling van het spoor door trechter/advertentietypes en gebruik [!DNL Audience Analytics] om ingangstarieven te bepalen en met de volgende fase van de klantenreis te overlappen.

* Bepaal de impact van de activiteit van de bovenste trechter op de activiteiten van de downstreamlocatie.

* Verbind [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> en [!DNL Audience Analytics] gegevens <!-- (which includes the user's last exposure event) --> om een holistische reis aan de plaats te bepalen.

Hieronder volgen voorbeelden van rapporten die u kunt maken in [!DNL Analysis Workspace] .

![ zie het effect van bovenkanaalactiviteit op stroomafwaartse plaatsactiviteit ](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### [!DNL Audience Analytics] Segmentgegevens van derden gebruiken voor analyse gebruikersprofiel

De segmenten van de Audience Manager van de derde van het gebruik voor een rijkere analyse van hoe de gebruikers met uw plaats interactie aangaan. U kunt de informatie gebruiken om nieuw publiek van derde partijen te bepalen waarvoor om media te activeren, die op hoe de profielen van de derdesegmenten met zeer belangrijke prestatiesindicatoren voor de plaatsen van mediacampagnes verbinden.

>[!TIP]
> Gebruik de Audience Manager `Audiences ID` en `Audiences Name` afmetingen in [!DNL Analytics] , net als alle andere dimensies die [!DNL Analytics] verzamelt.

Hieronder volgen voorbeelden van rapporten die u kunt maken in [!DNL Analysis Workspace] .

![ Gebruikend derdesegmenten om de analyse van het gebruikersprofiel te verrijken ](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [ Integraties van de Adobe Advertising met Adobe Audience Manager ](/help/integrations/audience-manager/overview.md)
