---
title: Veelgestelde vragen over Adobe Advertising-conversie- en pagina-weergavetags
description: Zie een vergelijking van de Adobe Advertising-conversie en de labels voor het bijhouden van de paginaweergave.
exl-id: 2e5ef792-e0f5-4409-bd37-87d9fab1265f
feature: Search Tracking
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Veelgestelde vragen over Adobe Advertising-conversie- en pagina-weergavetags

Het volgende is van toepassing op de volgende tags voor Adobe Advertising-conversie en tags voor het bijhouden van de paginaweergave.

| | JS-tags met ECID | JS versie 3-tags | Tags JS versie 2 | Afbeeldingslabels |
| ---- | ---- | ---- | ---- | ---- |
| Kan worden gebruikt op dezelfde webpagina als een andere JS-versie | — | — | — | nvt |
| Hiermee kunnen meerdere tags met dezelfde gebruikers-id&#39;s voor adverteerders op dezelfde webpagina worden gebruikt | Ja | Ja | Ja | — |
| Hiermee kunt u meerdere tags met verschillende gebruikers-id&#39;s voor adverteerders op dezelfde webpagina gebruiken | Ja | Ja | — | — |
| Wordt gebruikt door de Adobe Advertising-extensie voor Adobe Experience Platform en is compatibel met andere tags die zijn gegenereerd met Experience Platform | Ja | Ja | — | — |
| Hiermee kunnen alle conversies die afkomstig zijn van [!DNL Apple Safari] en [!DNL Mozilla Firefox] worden bijgehouden bij gebruik met de conversietoewijzingstag Adobe Advertising JavaScript | Ja | Ja | Ja | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Voor alle nieuwe implementaties wordt JavaScript versie 3 gebruikt.
>* De markering van JavaScript met ECID gebruikt de [&#x200B; identiteitskaart van Adobe Experience Cloud (ECID) Dienst &#x200B;](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=nl-NL) evenals erfenis ef_id en gsurferid om omzettingen te meten. Deze recentste markering leidt [&#x200B; eerste-partijExperience Cloud s_ecid koekjes &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html?lang=nl-NL) en verstrekt strakkere integratie met andere producten van Experience Cloud.
>* Gebruik alleen JavaScript Version 2-tags als deze al zijn geïmplementeerd op de webpagina&#39;s van de adverteerder.
>* De beste manier is om JavaScript-tags te gebruiken in plaats van afbeeldingstags, tenzij de site een beleid heeft tegen het gebruik ervan.
>* JavaScript-tags zijn vereist voor adverteerders die hun doelgroep willen maken voor in Adobe Experience Cloud gemaakte, in Adobe Audience Manager gemaakte of vanuit Audience Manager of Adobe Analytics naar Adobe Experience Cloud gepubliceerde soorten publiek.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer conversie-volgende markeringen van Adobe Advertising &#x200B;](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [&#x200B; produceer een Adobe Advertising omzettingsmarkering &#x200B;](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [&#x200B; Formaat van de conversie van JavaScript volgmerkversie 3 &#x200B;](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [&#x200B; Formaat van de conversie van JavaScript volgmerkversie 2 &#x200B;](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [&#x200B; Formaat van beeldomzetting volgende markeringen &#x200B;](/help/search-social-commerce/tracking/format-conversion-tag-image.md)

<!--
 add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
