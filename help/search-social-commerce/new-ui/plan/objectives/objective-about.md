---
title: (Nieuwe interface) Informatie over doelstellingen
description: Leer over doelstellingen om uw bedrijfsdoelstellingen te ontmoeten.
feature: Search Objectives, Search Optimization
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# (Nieuwe interface) Informatie over doelstellingen

*eigenschap van Beta*

De doelstellingen zijn doelstellingen die een adverteerder plaatst om zijn bedrijfsdoelstellingen te ontmoeten, zoals om winsten te maximaliseren of een specifiek verkoopdoel te bereiken. Zowel Advertising Search, Social, en Commerce als Advertising DSP gebruiken doelstellingen:

* Elk portfolio met zoekopdrachten, sociale gegevens en Commerce moet een doel hebben, zodat de optimalisatiefunctie klikmodellen en inkomstenmodellen voor het portfolio kan maken.

* In DSP worden doelstellingen weergegeven als aangepaste doelen voor DSP-accounts die zijn gekoppeld aan accounts in het vak Zoeken, Sociaal en Commerce. Elk pakket dat de optimalisatiedoelstellingen &quot;Hoogste Rendement op Advertentie (ROAS)&quot;of &quot;Laagste Kosten per Acquisition (CPA)&quot;gebruikt moet een douanedoel omvatten dat de algemene optimaliseringsdoelstelling helpt bereiken.

Een doel bestaat uit de conversiemetriek die moet worden bijgehouden en geoptimaliseerd, en de relatieve gewichten van die metriek. Stel dat een onlinetijdschrift met twee onlineabonnementsniveaus en één niveau voor gedrukte abonnementen en de doelstelling &quot;winstmaximalisatie&quot; drie cijfers heeft: &quot;basis online abonnementen&quot; gewaardeerd op 20 USD, &quot;premium online abonnementen&quot; gewaardeerd op 40 USD en &quot;printabonnementen&quot; gewaardeerd op 30 USD. Als het tijdschrift gewicht wil geven volgens de eenmalige monetaire waarde van het abonnement, dan zouden de relatieve gewichten van de meetwaarden respectievelijk 1, 2 en 1,5 zijn.

Voor elke metrische waarde in het doel kunt u:

* Configureer afzonderlijke dikten voor conversies van mobiele apparaten.

* Label de metrische waarde als [!UICONTROL Goal] metrisch of [!UICONTROL Assist] metrisch.

* Pas gewichtaanbevelingen op de metriek toe.

>[!NOTE]
>* (Onderzoek, Sociaal, &amp; Commerce) U kunt een doelstelling met een portefeuille associëren wanneer u [ de portefeuille ](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md) creeert of door later [ de portefeuillemontages ](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md) te wijzigen.
>* (Advertisers met de rekeningen van DSP die met Onderzoek, Sociale, &amp; rekeningen van Commerce verbonden zijn) in Advertising DSP, kunt u een doelstelling als a [ douaneoptimalisatiedoel ](/help/dsp/campaign-management/packages/package-settings.md) voor een pakket met pakket-vlakke het passen selecteren.
>* U kunt hetzelfde doel gebruiken voor meerdere zoek-, sociale en Commerce-portfolio&#39;s en/of meerdere DSP-pakketten.
>* De meetgegevens voor elk doel in de weergave [!UICONTROL Objectives] bevatten geen gegevens van DSP.

## Beschikbare cijfers

U kunt het volgende opnemen in uw doelstellingen:

* De cijfers die Adobe Advertising volgen gebruikend het [ conversie volgende pixel van Adobe Advertising ](/help/search-social-commerce/tracking/conversion-tracking-advertising.md).

* [ Advertiser-Gecontroleerde metriek van de dossiers van de omzetvoer ](/help/search-social-commerce/tracking/conversion-tracking-about.md).<!-- Search only, or might DSP-only clients also have these? -->

* (Advertisers met [!DNL Adobe Analytics for Advertising]) [ de metriek van de Omzetting en van de plaatsovereenkomst die van Adobe Analytics ](/help/integrations/analytics/overview.md) wordt gesynchroniseerd.

  In Onderzoek, Sociale, &amp; Commerce, worden de volgende [ metriek van de plaatstoezegging ](/help/integrations/analytics/analytics-data-in-advertising.md) automatisch in de portefeuille het bieden algoritmen in aanmerking genomen: `timespent_secs_1stvisit`, `timespent_secs_total`, `pageviews_1stvisit`, `pageviews_total`, en `bounces`.

* [!DNL Google] metrics: <!-- Search only, or might DSP-only clients also have these? -->

   * [[!DNL Google Ads] -tracked conversions ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) van gesynchroniseerde [!DNL Google Ads] accounts.

   * (Advertisers met [[!DNL Google Analytics]  integraties ](/help/search-social-commerce/admin/data-sources/data-source-about.md)) de meningen van de Pagina, Zittingen, het Tarief van de Stuiting (berekend als grenzen/zittingen), en Duur van de Zitting.

     In Zoeken, Sociaal en Commerce worden deze meetgegevens automatisch meegenomen in de algoritmen voor het bieden van portfolio&#39;s.

## Optie om doelstellingen te uploaden naar advertentienetwerken

U kunt naar keuze [ de doelstellingen voor de portefeuilles van de rekening aan  [!DNL Google Ads]  en/of  [!DNL Microsoft Advertising]  als omzettingen ](/help/search-social-commerce/tools/objective-upload-to-networks.md) uploaden zodat u hen voor campagne- of groep-vlakke optimalisering kunt gebruiken. Wanneer u deze optie inschakelt, geven Search, Social en Commerce de gewogen inkomstengegevens op EF-ID-niveau (klik op ID) door aan het advertentienetwerk. Het laat om het even welke ad netwerk-gevolgde metriek weg.

>[!MORELIKETHIS]
>
>* [ creeer een doel ](objective-create.md)
>* [ geef een doelstelling ](objective-edit.md) uit
>* [ Schrap een doelstelling ](objective-delete.md)
>* [ pas gewichtaanbevelingen op een doelstelling toe ](objective-apply-weight-recommendations.md)
>* [ Objectieve montages ](objective-settings.md)
