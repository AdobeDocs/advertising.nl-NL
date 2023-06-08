---
title: Veelgestelde vragen over conversie van Adobe-advertenties en labels voor het bijhouden van paginaweergaven
description: Zie een vergelijking van de conversie van Adobe-advertenties en de labels voor het bijhouden van de paginaweergave.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Veelgestelde vragen over conversie van Adobe-advertenties en labels voor het bijhouden van paginaweergaven

Het volgende is van toepassing op Adobe-tags voor conversie van advertenties en codes voor het bijhouden van paginaweergaven.

|  | JS-tags met ECID | JS versie 3-tags | Tags JS versie 2 | Afbeeldingslabels |
| ---- | ---- | ---- | ---- | ---- |
| Kan worden gebruikt op dezelfde webpagina als een andere JS-versie | — | — | — | n.v.t. |
| Hiermee kunnen meerdere tags met dezelfde gebruikers-id&#39;s voor adverteerders op dezelfde webpagina worden gebruikt | Ja | Ja | Ja | — |
| Hiermee kunt u meerdere tags met verschillende gebruikers-id&#39;s voor adverteerders op dezelfde webpagina gebruiken | Ja | Ja | Nee | Nee |
| Wordt gebruikt door de extensie Adobe Advertising voor Adobe Experience Platform en is compatibel met andere tags die zijn gegenereerd met Experience Platform | Ja | Ja | — | — |
| Hiermee worden alle conversies toegestaan die afkomstig zijn van [!DNL Apple Safari] en [!DNL Mozilla Firefox] moet worden bijgehouden bij gebruik met de conversietag JavaScript-conversie Adobe Advertising. | Ja | Ja | Ja | — |

<!-- add link to page on conversion mapping tag above? -->

>[!NOTE]
>
>* Alle nieuwe implementaties gebruiken JavaScript versie 3.
>* De JavaScript-tag met ECID gebruikt de [Adobe Experience Cloud ID-service (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) en de verouderde ef_id en gsurferid om omzettingen te meten. Deze nieuwste tag maakt [first-party Experience Cloud s_ecid cookies](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-first-party.html) en zorgt voor een betere integratie met andere Experience Cloud-producten.
>* Gebruik alleen JavaScript versie 2-tags als deze al zijn geïmplementeerd op de webpagina&#39;s van de adverteerder.
>* De beste manier is om JavaScript-tags te gebruiken in plaats van afbeeldingstags, tenzij de site een beleid heeft tegen het gebruik ervan.
>* JavaScript-tags zijn vereist voor adverteerders die doelgroepen willen maken die in Adobe Experience Cloud zijn gemaakt, in Adobe Audience Manager zijn gemaakt of vanuit Audience Manager of Adobe Analytics naar Adobe Experience Cloud zijn gepubliceerd.


>[!MORELIKETHIS]
>
>* [Informatie over conversietags voor Adobe-advertenties](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Een conversietag voor Adobe-advertenties genereren](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Indeling van JavaScript-tags voor conversie bijhouden versie 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Indeling van JavaScript-tags voor bijhouden van conversie versie 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Opmaak van trackingtags voor afbeeldingsconversie](/help/search-social-commerce/tracking/format-conversion-tag-image.md)


<!-- add if I keep the file:  
>* The Adobe Advertising JavaScript conversion mapping tag
-->
