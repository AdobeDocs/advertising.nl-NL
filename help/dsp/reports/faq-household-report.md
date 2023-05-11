---
title: Veelgestelde vragen over de [!UICONTROL Household] Rapport
description: Meer informatie over de [!UICONTROL Household] rapport, met inbegrip van hoe het van andere rapporten en het oplossen van problemen verschilt.
source-git-commit: 95f81dafbe13f40487bad47f7dd41a6c80c589ee
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Veelgestelde vragen over de [!UICONTROL Household] Rapport

## Hoe wordt [!UICONTROL Household] bereik en frequentie rapporten anders dan andere aangepaste rapporten?

De [!UICONTROL Household] de rapportmaatregelen bereiken, de indruk, en de frequentie over diverse dimensies op het niveau van het huishouden gebaseerd op IP adres. De andere aangepaste rapporten worden gegenereerd op apparaat- of cookieniveau.

Zelfs als er bijvoorbeeld één indruk wordt gemaakt op drie apparaten binnen één huishouden, is de unieke maatstaf van het huishouden bereikt er één.

### Ondersteunde Dimension

De [!UICONTROL Household] het verslag steunt [volgende afmetingen](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot; &quot;[!UICONTROL Package],&quot; &quot;[!UICONTROL Placement],&quot; &quot;[!UICONTROL Site/Apps]&quot; (wat geen toegang tot overlappende meetgegevens biedt), &quot;[!UICONTROL Media Type],&quot; &quot;[!UICONTROL Feed Type],&quot; &quot;[!UICONTROL Device],&quot; &quot;[!UICONTROL Publisher],&quot; &quot;[!UICONTROL Audience],&quot; &quot;[!UICONTROL Creative Length],&quot; en door de gebruiker gemaakte plaatsing &quot;[!UICONTROL Tags].&quot; |

### Ondersteunde metriek

De [beschikbare cijfers](/help/dsp/reports/report-columns.md) omvatten:

* Maten overlappen: [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)], en [!UICONTROL Unique Household (Overlap)].

   Overlap-meetwaarden zijn de waarden die alleen voorkomen voor de gerapporteerde dimensie of combinatie van dimensies, en niet voor andere dimensies. <!-- For example, it might show the ?? -->

* Niet-overlappende cijfers: [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions], en [!UICONTROL Unique Household Reached]

De metriek van de omzetting en douanedoelstellingen worden niet gesteund.

## Wat is het verschil tussen de overlap en de niet-overlap cijfers?

In de volgende afbeelding ziet u drie meeteenheden (Unieke waarde voor huishoudens bereikt, Incrementele huishoudens bereikt en Incrementele huishoudens (overlapping)) voor drie campagnes (A, B en C).

![Afbeelding van de maatstaven voor overlap tussen huishoudens](/help/dsp/assets/household-overlap-metrics-illustration.png "Afbeelding van de maatstaven voor overlap tussen huishoudens")

* Unieke huishoudens die zijn bereikt (totaal), geven de unieke huishoudens aan die door elk van de campagnes zijn bereikt of het totale oppervlak van elk van de cirkels. In de figuur is het unieke huishouden bereikt door A = het incrementele huishouden bereikt door A + (A+B) + (A+C) + (A+B+C)

* Het incrementele huishouden dat is bereikt is het unieke huishouden dat slechts door een campagne is bereikt. In de cijfers zijn de incrementele huishoudens die door A, B, C zijn bereikt, de incrementele huishoudens die door A, B, C zijn bereikt.

* Het incrementele huishouden (overlapping) is de unieke huishouden die wordt bereikt door de campagne of combinatie van campagnes. In de figuur is de incrementele huishouding bereikt door A, C A+C.

## Workflow

Voer de normale stappen uit om [een aangepast rapport maken](report-create.md).

De [!UICONTROL Household] het rapport kan slechts één dimensie bevatten . Het kan ook a) metriek door om het even welke afmeting behalve Plaats/Apps of b) niet-overlappende metriek omvatten, maar niet allebei.

## Wat zijn enkele beperkingen van de [!UICONTROL Household] rapporteren? 

Rapporten met overlappende metrische outputsnijpunten van maximaal drie waarden. Als u bijvoorbeeld de metrische [!UICONTROL Unique Household (Overlap)] voor 10 stages kunt u de unieke huishoudens zien die door individuele stages worden bereikt , gemeenschappelijke huishoudens die door een combinatie van twee stages worden bereikt , en gemeenschappelijke huishoudens die door combinaties van drie stages worden bereikt . Je ziet geen gewone huishoudens die door vier of meer plaatsen worden bereikt.

Voor dimensies buiten campagne, pakket, of plaatsing, steunt het rapport tot 10 waarden in elke dimensie. Als u bijvoorbeeld een [!UICONTROL Unique Household Reached] verslag voor de [!UICONTROL Audience] , moet het aantal unieke doelgroepen kleiner zijn dan of gelijk zijn aan 10. Als u meer dan 10 uniek publiek omvat, dan wordt een leeg rapport geproduceerd.

## Waarom zijn de frequentie en de unieke bereikwaarden verschillend tussen mijn [!UICONTROL Custom] en de [!UICONTROL Household] rapporteren?

Deze waarden in [!UICONTROL Household] de rapporten worden berekend gebruikend de daadwerkelijke telling van IP adressen, terwijl de metriek in [!UICONTROL Custom] het rapportgebruik geschatte aantallen berekend gebruikend modellen. De afwijking moet echter minder dan 10% bedragen.

## Hoe vorm ik het rapport voor [!UICONTROL Placement Tags] dimensie?

Als u labels voor de plaatsing wilt maken, [de plaatsingsinstellingen openen](/help/dsp/campaign-management/placements/placement-edit.md) en voert u waarden in in het dialoogvenster [Plaatsingslabels, veld](/help/dsp/campaign-management/placements/placement-settings.md).
 
Wanneer een plaatsing veelvoudige markeringen omvat, beschouwt het rapport het volledige koord als één markering. Het rapport bevat één rij voor elke unieke tekenreeks.

## [!UICONTROL Household] Gegevens rapporteren vs. [!DNL Advanced Measurement Services]

Voor geavanceerde rapportage over het bereik en de frequentie van huishoudens, [[!DNL Strategic Advertising Consulting] team](/help/dsp/introduction/advanced-measurement-services.md) kan zeer klantgerichte rapporten samen met holistische strategische aanbevelingen verstrekken. Meer informatie over [!DNL Advanced Measurement Services], neemt u contact op met uw Adobe-accountteam.

### Als ik al gebruik [!DNL Advanced Measurement Services], waarom moet ik de [!UICONTROL Household] rapporteren?

De [!UICONTROL Household] het rapport machtigt cliënten om het bereik en de frequentiemetriek op het niveau van het huishouden autonoom in real time te trekken.

### Mag ik beide [!UICONTROL Household] verslag en [!DNL Advanced Measurement Services]? 

Het ideale gebruiksscenario is om beide [!UICONTROL Household] en de [!DNL Advanced Measurement Services] gezamenlijke rapportage- en adviesdiensten. Neem de [!UICONTROL Household] rapporteren als transactie, bedoeld om optimalisaties van dag tot dag te informeren, en [!DNL Advanced Measurement Services] als meer strategisch, bedoeld om holistische lessen te informeren en overnames te maken in verband met overkoepelende bedrijfsdoelstellingen.

>[!MORELIKETHIS]
>
>* [Aangepaste rapporten](/help/dsp/reports/report-about.md)
>* [Een aangepast rapport maken](/help/dsp/reports/report-create.md)
>* [Een aangepast rapport bewerken](/help/dsp/reports/report-edit.md)
>* [Instellingen voor aangepaste rapporten](/help/dsp/reports/report-settings.md)
>* [Beschikbare rapportkolommen](/help/dsp/reports/report-columns.md)

