---
title: '[!DNL Adobe] [!DNL Audience Analytics]  voor Adobe Advertising-klanten'
description: Leer hoe u  [!DNL Adobe] [!DNL Audience Analytics] kunt gebruiken voor het maken van advertenties
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] voor Adobe Advertising-klanten

[[!DNL Adobe] [!DNL Audience Analytics] &#x200B;](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) is een integratie tussen Adobe Audience Manager en Adobe Analytics die klanten van Audience Manager toestaat om segmenten naar [!DNL Analytics] voor verrijkte inzichten over plaatsactiviteit te verzenden.

Adobe Advertising-klanten kunnen hiervan profiteren door [!DNL Audience Analytics] te gebruiken. Dankzij de integratie kunt u:

* Verzend Adobe Advertising-belichtingsgegevens rechtstreeks naar [!DNL Analytics] om het effect van de funnel-activiteiten op de activiteiten van de downstreamsite te bepalen.

* Bepaal de marketingkanalen en de toegangspunten van de site op basis van de blootstellingsadvertenties in de bovenste funnel.

* Laag de integratie met [!DNL Analytics for Advertising] om derde demografische segmenten van [&#x200B; Audience Manager  [!DNL Audience Marketplace] &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) met [!DNL Analytics for Advertising] gegevens voor meer inzicht over gebruikersprofielen op te nemen.

  [!DNL Audience Marketplace] biedt toegang tot gegevensfeeds van derden met abonnementmodellen voor activering, waarmee kopers gegevens naar een bestemming kunnen verzenden. Als de gegevens worden gebruikt binnen een [!DNL Analytics] -bestemming, worden geen activeringskosten toegepast.

* (Advertisers met Advertising DSP) Voeg extra blootstellingssegmenten toe voor holistische inzichten in het reisbeheer.

  Advertising DSP kan belichtingsgegevens naar Audience Manager verzenden als activeerbare signalen via de implementatie van Adobe Experience Platform- of Audience Manager-pixels die de indruk bijhouden. Door dezelfde gegevens naar [!DNL Analytics] te verzenden, kunt u geavanceerde gegevensanalyse uitvoeren. Zie &quot;[&#x200B; Overzicht van het verzenden van de media van DSP blootstellingsgegevens naar Adobe Audience Manager &#x200B;](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;voor meer informatie.

Voor meer informatie over [!DNL Audience Analytics], met inbegrip van zijn eerste vereisten en werkschema, zie &quot;[&#x200B; overzicht van Audience Analytics &#x200B;](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Voorbeelden van het gebruik van [!DNL Audience Analytics] -gegevens met Adobe Advertising-gegevens

Hieronder ziet u voorbeelden van het gebruik van de gecombineerde gegevens in [!DNL Analytics] [!DNL Analysis Workspace] .

### Zie de impact van de activiteiten van de bovenste funnel op de downstreamactiviteiten

Gebruik de blootstellingssegmenten van Audience Manager om de impact van de activiteit van de bovenste funnel-locatie op de activiteiten van de downstreamsite te zien. Neem Adobe Advertising- of externe macro-id&#39;s op in de volgende pixels om de impact op een gedetailleerd niveau te volgen, van het campagneniveau tot het niveau van de site waarop de gebruiker is weergegeven.

Belangrijkste voordelen:

* Houd de belichting door funnel/advertentietypen bij en gebruik [!DNL Audience Analytics] om de toegangspercentages te bepalen en om de volgende fase van de klantreis te overlappen.

* Bepaal de impact van de activiteiten van de bovenste funnel op de activiteiten van de downstreamsite.

* Verbind [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> en [!DNL Audience Analytics] gegevens om een holistische reis aan de plaats te bepalen.

<!-- (which includes the user's last exposure event) -->

Hieronder volgen voorbeelden van rapporten die u kunt maken in [!DNL Analysis Workspace] .

![&#x200B; zie het effect van de hogere activiteit van funnel op stroomafwaartse plaatsactiviteit &#x200B;](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Segmentgegevens van derden gebruiken voor analyse van gebruikersprofielen[!DNL Audience Analytics]

Gebruik Audience Manager-segmenten van derden voor een rijkere analyse van de manier waarop gebruikers met uw site communiceren. U kunt de informatie gebruiken om nieuw publiek van derde partijen te bepalen waarvoor om media te activeren, die op hoe de profielen van de derdesegmenten met zeer belangrijke prestatiesindicatoren voor de plaatsen van mediacampagnes verbinden.

>[!TIP]
> Gebruik de Audience Manager `Audiences ID` - en `Audiences Name` -afmetingen in [!DNL Analytics] , net als alle andere dimensies die [!DNL Analytics] verzamelt.

Hieronder volgen voorbeelden van rapporten die u kunt maken in [!DNL Analysis Workspace] .

![&#x200B; Gebruikend derdesegmenten om de analyse van het gebruikersprofiel te verrijken &#x200B;](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [&#x200B; de integratie van Adobe Advertising met Adobe Audience Manager &#x200B;](/help/integrations/audience-manager/overview.md)
