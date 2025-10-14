---
title: Veelgestelde vragen over aangepaste rapporten
description: Meer informatie over aangepaste rapporten, waaronder rapporten van het huishouden en analytische rapporten over het omzetpad.
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
source-git-commit: a1ece707f43af4a6a3fc5573e41c75622f9b502f
workflow-type: tm+mt
source-wordcount: '1178'
ht-degree: 0%

---

# Veelgestelde vragen over aangepaste rapporten

## Huishoudelijke rapporten

### Het [!UICONTROL Household Reach & Frequency] -rapport

#### Hoe verschillen [!UICONTROL Household Reach & Frequency] -rapporten van andere aangepaste rapporten?

De rapportmetingen van [!UICONTROL Household Reach & Frequency] bereiken, de indruk, en de frequentie over diverse dimensies op een huisniveau dat op IP adres wordt gebaseerd. De andere aangepaste rapporten worden gegenereerd op apparaat- of cookieniveau.

Zelfs als er bijvoorbeeld één indruk wordt gemaakt op drie apparaten binnen één huishouden, is de unieke maatstaf van het huishouden bereikt er één.

##### Ondersteunde afmetingen

Het [!UICONTROL Household Reach & Frequency] rapport steunt [&#x200B; volgende afmetingen &#x200B;](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot;[!UICONTROL Package], &quot;[!UICONTROL Placement],&quot;&quot;[!UICONTROL Site/Apps]&quot; (die geen toegang tot overlappende metriek) verleent, &quot;[!UICONTROL Media Type], &quot;[!UICONTROL Feed Type], &quot;[!UICONTROL Device],&quot;&quot;[!UICONTROL Publisher], &quot;[!UICONTROL Audience],&quot;&quot;[!UICONTROL Creative Length],&quot; en gebruiker-gecreeerde plaatsing &quot;[!UICONTROL Tags].&quot; |

##### Ondersteunde metriek

De [&#x200B; beschikbare metriek &#x200B;](/help/dsp/reports/report-columns.md) omvatten:

* Overlap metriek: [!UICONTROL Frequency Overlap] , [!UICONTROL Measurable Impressions (Overlap)] en [!UICONTROL Unique Household (Overlap)] .

  Overlap-meetwaarden zijn de waarden die alleen voorkomen voor de gerapporteerde dimensie of combinatie van dimensies, en niet voor andere dimensies. <!-- For example, it might show the ?? -->

* Niet-overlappende metriek: [!UICONTROL Frequency] , [!UICONTROL Incremental Household Reached] , [!UICONTROL % Incremental Household Reached] , [!UICONTROL Impressions] , [!UICONTROL Measurable Impressions] en [!UICONTROL Unique Household Reached]

De metriek van de omzetting en douanedoelstellingen worden niet gesteund.

#### Wat is het verschil tussen de overlap en de niet-overlap cijfers?

In de volgende afbeelding ziet u drie meeteenheden (Unieke waarde voor huishoudens bereikt, Incrementele huishoudens bereikt en Incrementele huishoudens (overlapping)) voor drie campagnes (A, B en C).

![&#x200B; Illustratie van huisoverlap metriek &#x200B;](/help/dsp/assets/household-overlap-metrics-illustration.png " Illustratie van huisoverlap metriek ")

* Unieke huishoudens die zijn bereikt (totaal), geven de unieke huishoudens aan die door elk van de campagnes zijn bereikt of het totale oppervlak van elk van de cirkels. In de figuur is het unieke huishouden bereikt door A = het incrementele huishouden bereikt door A + (A+B) + (A+C) + (A+B+C)

* Het incrementele huishouden dat is bereikt is het unieke huishouden dat slechts door een campagne is bereikt. In de cijfers zijn de incrementele huishoudens die door A, B, C zijn bereikt, de incrementele huishoudens die door A, B, C zijn bereikt.

* Het incrementele huishouden (overlapping) is de unieke huishouden die wordt bereikt door de campagne of combinatie van campagnes. In de figuur is de incrementele huishouding bereikt door A, C A+C.

#### Workflow

Volg de normale stappen om [&#x200B; tot een douanerapport &#x200B;](report-create.md) te leiden.

Het [!UICONTROL Household Reach & Frequency] -rapport kan slechts één dimensie bevatten. Het kan ook a) metriek door om het even welke afmeting behalve Plaats/Apps of b) niet-overlappende metriek omvatten, maar niet allebei.

#### Wat zijn enkele beperkingen van het [!UICONTROL Household Reach & Frequency] -rapport?

Rapporten met overlappende metrische outputsnijpunten van maximaal drie waarden. Als u bijvoorbeeld de maatstaf [!UICONTROL Unique Household (Overlap)] voor 10 plaatsen gebruikt, kunt u de unieke huishoudens zien die worden bereikt door individuele plaatsingen, gemeenschappelijke huishoudens die worden bereikt door een combinatie van twee plaatsingen en gemeenschappelijke huishoudens die worden bereikt door combinaties van drie plaatsingen. Je ziet geen gewone huishoudens die door vier of meer plaatsen worden bereikt.

Voor dimensies buiten campagne, pakket, of plaatsing, steunt het rapport tot 10 waarden in elke dimensie. Als u bijvoorbeeld een [!UICONTROL Unique Household Reached] -rapport wilt genereren voor de [!UICONTROL Audience] -dimensie, moet het aantal unieke doelgroepen kleiner zijn dan of gelijk zijn aan 10. Als u meer dan 10 uniek publiek omvat, dan wordt een leeg rapport geproduceerd.

#### Waarom verschillen de frequentie en unieke bereikwaarden tussen mijn [!UICONTROL Custom] -rapporten en het [!UICONTROL Household Reach & Frequency] -rapport?

Deze metriek in [!UICONTROL Household] rapporten wordt berekend gebruikend de daadwerkelijke telling van IP adressen, terwijl de metriek in het [!UICONTROL Custom] rapport geschatte aantallen gebruikt die gebruikend modellen worden berekend. De afwijking moet echter minder dan 10% bedragen.

#### Hoe configureer ik het rapport voor de [!UICONTROL Placement Tags] -dimensie?

Om markeringen voor de plaatsing tot stand te brengen, [&#x200B; open de plaatsingsmontages &#x200B;](/help/dsp/campaign-management/placements/placement-edit.md) en ga waarden op het [&#x200B; gebied van de Markeringen van de Plaatsing &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md) in.

Wanneer een plaatsing veelvoudige markeringen omvat, beschouwt het rapport het volledige koord als één markering. Het rapport bevat één rij voor elke unieke tekenreeks.

### Het [!UICONTROL Household Conversions] -rapport

#### Welke toewijzingsmethoden worden ondersteund in het [!UICONTROL Household Conversions] -rapport?

Er worden twee typen toewijzingsmethoden ondersteund:

* [!UICONTROL Unique]: telt het aantal keren dat een waarde voor de dimensie (zoals een apparaat of plaatsing) zich op het pad naar conversie bevond.

* [!UICONTROL Multi-Touch Attribution (MTA)]: distribueert het krediet van elke omzetting op de frequentie van voorkomen van de afmetingswaarde (zoals een apparaat of plaatsing) op de weg aan omzetting. Als er bijvoorbeeld in totaal 10 indrukken waren vóór de conversie, met 8 op CTV en 2 op Mobile, wordt 80% van het krediet (0,8) aan CTV-schermen en 0,2 aan Mobiel gegeven.

#### Hoe verschilt de rapportage van omrekeningen van huishoudens van de rapportage van de doorkijkcijfers van de tv in Adobe Analytics?

* In [!DNL Analytics] toont het [!DNL CTV View-Through Conversion] -rapport het aantal conversies waarvoor een CTV-indruk het laatste aanraakpunt vóór de conversie was. Het DSP [!UICONTROL Household Conversions] -rapport daarentegen toont het aantal unieke huishoudens dat vóór de conversie aan een CTV-indruk werd blootgesteld op een willekeurig punt binnen het gedefinieerde terugzoekvenster.

* In [!DNL Analytics] wijst attributielogica uitsluitend conversies toe aan het laatste aanraakpunt van Adobe Advertising. Het DSP [!UICONTROL Household Conversions] -rapport ondersteunt daarentegen aanvullende attributiemodellen *[!UICONTROL Unique]* en *[!UICONTROL Multi-Touch Attribution (MTA)]* .

* De rapportgegevens van [!DNL Analytics] zijn bijzonder waardevol om door marketing kanalen, de metriek van de plaatsovereenkomst, etc. te analyseren. Het DSP [!UICONTROL Household Conversions] -rapport biedt gedetailleerdere inzichten doordat conversiegegevens kunnen worden gesplitst in verschillende dimensies, zoals het mediatype en de uitgever.

### [!UICONTROL Household Reach & Frequency] en [!UICONTROL Household Conversions] Rapporten versus gegevens van [!DNL Advanced Measurement Services]

Voor geavanceerde rapportering over huishouden-gebaseerd bereik en frequentie of omzettingen, kan het [[!DNL Strategic Advertising Consulting]  team &#x200B;](/help/dsp/introduction/advanced-measurement-services.md) hoogst klantgerichte rapporten samen met holistische strategische aanbevelingen verstrekken. Neem voor meer informatie over [!DNL Advanced Measurement Services] contact op met uw Adobe-accountteam.

#### Als ik [!DNL Advanced Measurement Services] al gebruik, waarom zou ik [!UICONTROL Household Reach & Frequency] en [!UICONTROL Household Conversions] rapporten moeten gebruiken?

In de rapporten [!UICONTROL Household Reach & Frequency] en [!UICONTROL Household Conversions] kunnen clients het bereik, de frequentie en de conversiemetriek op het niveau van het huishouden zelfstandig in real-time ophalen.

#### Kan ik zowel de [!UICONTROL Household Reach & Frequency] als [!UICONTROL Household Conversions] rapporten en [!DNL Advanced Measurement Services] gebruiken?

Het ideale geval is om zowel het [!UICONTROL Household] -rapport als de [!DNL Advanced Measurement Services] -services voor rapportage en advies samen te gebruiken. Beschouw het [!UICONTROL Household] -rapport als transactie, dat bedoeld is om dagelijkse optimalisaties te informeren, en [!DNL Advanced Measurement Services] als strategischer, dat bedoeld is om holistische lessen te informeren en overgangen te maken die verband houden met overkoepelende bedrijfsdoelstellingen.

## Analyserapporten van pad voor conversie

### Hoe verhoudt het rapport Pad naar conversie zich tot rapporten die zijn gemaakt door [!DNL Advanced Measurement Services] en Adobe Analytics Analysis Workspace?

| | Pad naar omzettingsrapport | Geavanceerd halo-effect Metingsservices bij zoekrapportage | Rapporten in Analysis Workspace |
| --- | --- | --- |---|
| Klantenwaarde | Genereer een zelf-bediende douanerapport om te begrijpen welke wegen van de ad reis tot meer omzettingen leidden om optimalisering te bevorderen | Begrijp de invloed van de tactiek van de Verbonden TV (CTV) op onderzoek klikt | Begrijp de invloed van uw holistische investering van Adobe Advertising, naast andere marketing kanalen, op onderzoeksklikjes |
| Huishoudelijk niveau | Ja | Ja | Nee |
| Wordt CTV ondersteund? | Ja | Ja | Ja |
| Attributiemethode | De laatste aanraakgebeurtenis (indruk of klik) moet zich in het venster van het lookboek bevinden. | Uniques | Laatste aanraking |
| | Interactiepunten die meer dan 30 dagen vóór de laatste aanraakgebeurtenis liggen, worden in overweging genomen voor het conversiepad. | (CTV ontvangt krediet, ongeacht de locatie van de blootstelling aan kleuren-tv&#39;s in het pad naar klikken van de gebruiker) | (CTV krijgt krediet als de indruk de laatste gebeurtenis in het terugkijkvenster is EN er geen betaalde klik van andere formaten of vóór of na blootstelling CTV is) |
| Rapportageniveau | korrelig | korrelig | Breed |
| | (Kanaaltype, Creative/Advertentie, Trefwoord, Paden, Lengte, Tijd-aan-Omzetting) | (Tactische tv, CTV-app/uitgever) | (Adobe Advertising en andere marketingkanalen) |
| Marketingkanalen | DSP + Zoeken (van Zoeken, Sociaal en Commerce) | DSP + Zoeken (van Zoeken, Sociaal en Commerce) | Marketingkanalen die niet worden bijgehouden door de Adobe Advertising klikken via EF-id (zoals Organic Search, Organic Social, Email en Affiliate) |
| Ondersteunde omzettingsstatistieken | Metrisch bijgehouden met Adobe Advertising-gebeurtenispixel (AMO-id) en Adobe Analytics-tracking | Klikken (geen conversies) | Metrische gegevens bijgehouden met gebruik van Adobe Analytics tracking |

Voor meer informatie over het Geavanceerde Effect van de Halo van de Diensten van de Meting van de Meting op het Onderzoek die, zie &quot;[&#x200B; Geavanceerde Diensten van de Meting &#x200B;](/help/dsp/introduction/advanced-measurement-services.md) melden.&quot;

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer de Rapporten van de Douane &#x200B;](/help/dsp/reports/report-about.md)
>* [&#x200B; creeer een Rapport van de Douane &#x200B;](/help/dsp/reports/report-create.md)
>* [&#x200B; geef een Rapport van de Douane uit &#x200B;](/help/dsp/reports/report-edit.md)
>* [&#x200B; de Montages van het Rapport van de Douane &#x200B;](/help/dsp/reports/report-settings.md)
>* [&#x200B; Beschikbare Kolommen van het Rapport &#x200B;](/help/dsp/reports/report-columns.md)
