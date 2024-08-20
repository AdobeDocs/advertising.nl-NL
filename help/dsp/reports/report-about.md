---
title: Aangepaste rapporten
description: Leer over opties om douanerapporten manueel tot stand te brengen of pre-gevormde rapportmalplaatjes te gebruiken.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 81c9590d134214e1ed860c2f8116ff66882000be
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Aangepaste rapporten

Met aangepaste rapporten kunt u de inhoud en levering van uw rapportgegevens aanpassen aan de hand van de campagneafmetingen (zoals de adverteerder, plaatsing, sites of geos) en de maatstaven die het belangrijkst voor u zijn. U kunt:

* Vorm volledig de rapporten van de campagneprestaties op een korrelig niveau.
* Kies uit vooraf geconfigureerde rapportsjablonen en pas deze desgewenst verder aan.

U kunt rapporten eenmaal genereren, of ze plannen om dagelijks, wekelijks of maandelijks om 3:00 uur te worden gegenereerd in de opgegeven tijdzone. Zodra een rapport wordt geproduceerd, wordt het geleverd aan elke gespecificeerde e-mailontvanger of aan verbonden [ rapportbestemmingen ](/help/dsp/reports/report-destinations/report-destination-about.md) van de volgende types:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* FTP SSL (in bèta)

>[!NOTE]
>
>U kunt gegevens op bestelling op alle niveaus van een campagne (campagne, pakket, plaatsing, of advertentie) ook bekijken [ binnen de relevante mening van het campagnebeheer ](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Beschikbare rapporttypen

* **[!UICONTROL Custom]:** Dit rapport is een leeg malplaatje u kunt gebruiken om uw eigen douanerapport tot stand te brengen gebruikend de meeste dimensies en metriek. Rapporten [!UICONTROL Conversion] , [!UICONTROL Device] , [!UICONTROL Geo] en [!UICONTROL Site] zijn variaties van deze sjabloon met vooraf geselecteerde kolommen en dimensies voor hun respectievelijke gebruiksgevallen.

* Vooraf geconfigureerde rapportsjablonen

   * **[!UICONTROL Billing]:** gebruik dit rapport om zeer belangrijke het factureren metriek zoals uitgavenmetriek voor media het factureren door campagne te begrijpen. Gegevens zijn niet beschikbaar voor plaatsen die universele id&#39;s als doel hebben.

     >[!NOTE]
     >
     >Dit rapport bevat gegevens over het factureringssegment. Als een gebruiker of een apparaat een indruk krijgt die tot veelvoudige segmenten behoort, slechts wordt één factureerbare segment met de indruk gecrediteerd.

   * **[!UICONTROL Conversion]:** gebruik dit rapport om te begrijpen hoe uw campagnes worden uitgevoerd op basis van conversiemetriek die is vastgelegd met het bijhouden van Adoben Advertising conversie. Dit rapport bevat multi-touchattributie.

   * **[!UICONTROL Device]:** gebruik deze vooraf ingevulde sjabloon om belangrijke metriek per apparaat-gerelateerde afmetingen te zien.

   * **[!UICONTROL Frequency (by Impression)]:** gebruik dit rapport om de distributie te begrijpen van de beelden die aan unieke kijkers worden getoond (bijvoorbeeld, hoeveel unieke kijkers één indruk, twee beelden, drie beelden, etc. zagen. Gegevens zijn beschikbaar via plaatsing of campagne.

     >[!NOTE]
     >
     >* Gegevens zijn beschikbaar na 1 maart 2019.
     >* De frequentie wordt geschat op basis van een steekproef van gegevens.
     >* Voor sommige inventarisaties geven uitgevers geen apparaat-id door, waardoor het bijhouden van de frequentie wordt verhinderd. Dit rapport bevat alleen afbeeldingen waarvoor een apparaat-id beschikbaar was.

   * **[!UICONTROL Frequency (by App/Site)]:** gebruik dit rapport om te begrijpen hoeveel unieke gebruikers per app of per site zijn bereikt. U kunt ook zien hoeveel unieke gebruikers alleen via een bepaalde app of site (&quot;verschillende unieke gebruikers&quot;) zijn bereikt.

     >[!NOTE]
     >
     >* Gegevens zijn beschikbaar na 15 november 2018.
     >* Voor sommige privéinventarisaties geven uitgevers geen apparaat-id door, waardoor het bijhouden van de frequentie wordt verhinderd.

   * **[!UICONTROL Geo]**: Gebruik deze vooraf ingevulde sjabloon om de belangrijkste metriek op geografische afmetingen weer te geven.

   * **[!UICONTROL Margin]:** gebruik dit rapport om zeer belangrijke metriek zoals marge, winst, en andere uitgavenmetriek door campagne of plaatsing te zien. Gegevens zijn niet beschikbaar voor plaatsen die universele id&#39;s als doel hebben.

   * **[!UICONTROL Segment]:** gebruik dit vooraf ingevulde malplaatje om zeer belangrijke metriek door segment te zien.

     >[!NOTE]
     >
     >* Dit rapport is bedoeld om te tonen hoe de verschillende doelsegmenten presteren. Het gebruikt de gegevens van het segmentlidmaatschap. Wanneer een persoon of een apparaat dat tot twee of meer doelsegmenten behoort, de indruk krijgt, bevat dit rapport één rij voor elk segment. Daarom komen de totalen in dit rapport mogelijk niet overeen met de werkelijke levering.
     >* De metriek van de omzetting en de gegevens van het douanedoel voor segmenten zijn beschikbaar na 2 Augustus 2019. Alle andere gegevens voor segmenten zijn beschikbaar vanaf 1 juni 2018.

   * **[!UICONTROL Site]:** door gebrek, omvat standaardmetriek, totale media netto uitgaven, en totale factureerbare netto uitgaven door plaats.

   * **[!UICONTROL Household Reach & Frequency]:** gebruik dit rapport om beelden, bereik en frequentie voor één enkele afmeting over ad formaten op het niveau van het huishouden te zien die op IP adres, eerder dan op een apparaat/koekjesniveau wordt gebaseerd. Gebruik de inzichten om uw media mengeling te optimaliseren, prestaties te verbeteren, en mogelijkheden voor stijgende bereik te identificeren. Zie &quot;[ FAQs over de Rapporten van de Huishouden ](/help/dsp/reports/faq-household-report.md)&quot;voor meer informatie. Gegevens zijn niet beschikbaar voor plaatsen die universele id&#39;s als doel hebben.

   * **[!UICONTROL Household Conversions]:** gebruik dit rapport om mening-door omzettingen op het niveau van het huishouden te zien die op IP adres, eerder dan op een apparaat/koekjesniveau wordt gebaseerd. Gebruik de inzichten om campagneprestaties te meten en te optimaliseren. Zie &quot;[ FAQs over de Rapporten van de Huishouden ](/help/dsp/reports/faq-household-report.md)&quot;voor meer informatie. Gegevens zijn niet beschikbaar voor plaatsen die universele id&#39;s als doel hebben.

## Rapportage tussen accounts {#cross-account-reporting}

Om het even welke organisatie met veelvoudige DSP rekeningen kan naar keuze dwars-rekeningsgegevens in douanerapporten toelaten, volgens de behoeften van de organisatie. U kunt bijvoorbeeld Account A toegang geven tot de gegevens van Account B en Account B toegang geven tot de gegevens van Account C (maar niet van Account A). Neem contact op met het accountteam van de Adobe om deze functie in te schakelen en te configureren.

Zodra de eigenschap voor uw organisatie wordt toegelaten, kunt u [ ](report-settings.md) om het even welke volgende rapporttypes door rekening filtreren: [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], en [!UICONTROL Conversion].

Uw accountinstellingen op [!UICONTROL Settings] > [!UICONTROL Account] geven a) de andere accounts aan waarvan de gegevens beschikbaar zijn voor uw account en b) de andere accounts die toegang hebben tot de gegevens van uw account.

>[!MORELIKETHIS]
>
>* [ creeer een Rapport van de Douane ](/help/dsp/reports/report-create.md)
>* [ de Montages van het Rapport van de Douane ](/help/dsp/reports/report-settings.md)
>* [ Veelgestelde vragen over de Rapporten van de Huishouden ](/help/dsp/reports/faq-household-report.md)
>* [ Types van Rapporten van Prestaties in de Meningen van Campaign Management ](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [ Beschikbare Kolommen van het Rapport ](/help/dsp/reports/report-columns.md)
>* [ Over [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
