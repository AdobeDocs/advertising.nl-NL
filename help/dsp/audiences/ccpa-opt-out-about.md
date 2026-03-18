---
title: Informatie over [!UICONTROL CCPA Opt-out-of-Sale] segmenten en rapporten
description: Leer over het creëren van segmenten om IDs van uit-verkoopverzoeken te volgen CCPA en hoe te om rapporten van identiteitskaarts terug te winnen.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 7cf17457ba777d2dfe9fc1607f9891a340da9031
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# Informatie over [!UICONTROL CCPA Opt-out-of-Sale] segmenten en rapporten

U kunt gebruikers IDs van de consument van opt-out-of-verkoop verzoeken op uw website, per de Wet van de Privacy van de consument van Californië (CCPA) volgen, door [&#x200B; het creëren en het uitvoeren van een opt-out van-van-verkoop CCPA segment &#x200B;](ccpa-opt-out-segment-create.md). De gebruikers blijven in opt-out van CCPA-segmenten voor onbepaalde tijd.

Zodra de segmentpixel-tag is geïmplementeerd, begint Adobe Advertising namens de adverteerder een pool met id&#39;s te verzamelen.

## Verslagen over de opt-out van de verkoop voor consumenten

Adobe Advertising genereert maandelijkse rapporten met id&#39;s die klanten hebben ingediend voor een aanvraag om te weigeren te verkopen voor de account. De gegevens consolideren aanvragen die zijn vastgelegd met CCPA-opt-out-of-sales-segmenten die in DSP zijn gemaakt en alle aanvragen die via de Privacy Service API zijn ingediend.  Rapporten worden gegenereerd op de eerste van elke maand voor de vorige maand. De maandelijkse gebruikerslijst voor juni is bijvoorbeeld beschikbaar op 1 juli.

Elk rapport is beschikbaar als een tekstbestand met tabs als scheidingsteken en gecomprimeerd in de GZIP-indeling. In de CCPA-opt-out-of-sales-segmenten vastgelegde gebruikers-id&#39;s worden per segment en per adverteerder geïdentificeerd.

U kunt [&#x200B; verbindingen aan de maandelijkse rapporten &#x200B;](ccpa-opt-out-segment-report-retrieve.md) terugwinnen die in de vorige drie maanden, of van binnen DSP of door DSP [!DNL Trafficking API] werden gecreeerd te gebruiken. Elke koppeling is zeven dagen geldig, maar wordt telkens vernieuwd wanneer een klant probeert een koppeling op te halen.

>[!MORELIKETHIS]
>
>* [&#x200B; de steun van Adobe Advertising voor de Wet van de Privacy van de Consumentenbescherming van Californië: De opt-out van de consument van verkoopsteun &#x200B;](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [&#x200B; creeer en voer a [!UICONTROL CCPA Opt-Out-of-Sale] Segment &#x200B;](ccpa-opt-out-segment-create.md) uit
>* [&#x200B; wint consument op opt-out-of-verkoop rapporten &#x200B;](ccpa-opt-out-segment-report-retrieve.md)
>* [&#x200B; Ongeveer publieksbeheer &#x200B;](audience-about.md)
