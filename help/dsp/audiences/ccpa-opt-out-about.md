---
title: Info [!UICONTROL CCPA Opt-out-of-Sale] Segmenten en rapporten
description: Leer over het creëren van segmenten om IDs van uit-verkoopverzoeken te volgen CCPA en hoe te om rapporten van identiteitskaarts terug te winnen.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Info [!UICONTROL CCPA Opt-out-of-Sale] Segmenten en rapporten

U kunt gebruikers-id&#39;s bijhouden van een aanvraag voor een opt-out-of-sales (opt-out) voor de consument op uw website, op basis van de California Consumer Privacy Act (CCPA), door [tot oprichting en uitvoering van een CCPA-opt-out-of-sales-segment](ccpa-opt-out-segment-create.md). De gebruikers blijven in opt-out van CCPA-segmenten voor onbepaalde tijd.

Zodra de segmentpixel-tag is geïmplementeerd, begint de Adobe Advertising een pool met id&#39;s te verzamelen namens de adverteerder.

## Rapporten over verkoopverbod voor consumenten

Adobe Advertising genereert maandelijkse rapporten van id&#39;s die klanten hebben ingediend voor een aanvraag om niet te verkopen voor de account. De gegevens consolideren aanvragen die zijn vastgelegd met CCPA-opt-out-of-sales-segmenten die zijn gemaakt in DSP en alle aanvragen die via de Privacy Service-API zijn ingediend.  Rapporten worden gegenereerd op de eerste van elke maand voor de vorige maand. De maandelijkse gebruikerslijst voor juni is bijvoorbeeld beschikbaar op 1 juli.

Elk rapport is beschikbaar als een tekstbestand met tabs als scheidingsteken en gecomprimeerd in de GZIP-indeling. In de CCPA-opt-out-of-sales-segmenten vastgelegde gebruikers-id&#39;s worden per segment en per adverteerder geïdentificeerd.

U kunt [koppelingen naar de maandelijkse rapporten ophalen](ccpa-opt-out-segment-report-retrieve.md) die in de voorafgaande drie maanden zijn gemaakt, hetzij vanuit DSP, hetzij met behulp van de DSP [!DNL Trafficking API]. Elke koppeling is zeven dagen geldig, maar wordt telkens vernieuwd wanneer een klant probeert een koppeling op te halen.

>[!MORELIKETHIS]
>
>* [Adobe Advertising Support for the California Consumer Privacy Act: Consumer Opt-out Support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Een [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Rapporten over verkoopopties voor consumenten ophalen](ccpa-opt-out-segment-report-retrieve.md)
>* [Informatie over Audience Management](audience-about.md)
