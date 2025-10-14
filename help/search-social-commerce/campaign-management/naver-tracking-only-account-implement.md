---
title: Voer  [!DNL Naver]  het volgen-slechts rekeningen uit
description: Leer hoe te opstelling het volgen campagnes voor uw  [!DNL Naver]  rekeningen zodat u, prestaties voor de advertenties kunt volgen rapporteren en visualiseren u direct van het advertentienetwerk koopt.
exl-id: acbaf4f0-eb55-4788-bc84-c3181d635f1d
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# [!DNL Naver] Alleen-trackingaccounts implementeren

*[!DNL Naver]alleen accounts*

U kunt traceringscampagnes voor uw [!DNL Naver] -accounts maken, zodat u de prestaties voor advertenties die u rechtstreeks via het advertentienetwerk koopt, kunt bijhouden, rapporteren en visualiseren. Met Zoeken, Sociaal en Commerce worden gegevens niet gesynchroniseerd met het advertentienetwerk, worden gegevens automatisch geüpload en worden geen biedingen voor het account geplaatst.

Bij het bijhouden van campagnes worden uw bestaande campagnes, groepen en trefwoorden gerepliceerd. Nadat u de accountstructuur hebt gemaakt in Zoeken, Sociaal en Commerce en de oorspronkelijke campagnes in het advertentienetwerk hebt bijgehouden, kunt u dagelijkse netwerkverkeersmetingen uploaden voor uw trefwoorden of advertenties. Zoeken, Sociaal en Commerce kunnen uw conversies vervolgens aan uw advertenties en trefwoorden toewijzen.

U kunt prestatiesmetriek over al uw campagnes en voor om het even welke individuele campagne, ad groep, of sleutelwoord/advertentie volgen. U kunt ook informatie over hen in het meest basisch, geavanceerd, en hulprapporten, samen met gegevens voor uw andere advertentienetwerken omvatten. Steun voor het uitvoeren van de metriek naar Adobe Analytics is niet beschikbaar, maar het Onderzoek, Sociale, &amp; Commerce kan [&#x200B; metriek synchroniseren u binnen  [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) in Onderzoek, Sociale, &amp; Commerce volgt.

>[!NOTE]
>
>U kunt geen volgcampagnes toevoegen aan een portfolio voor optimalisatie.

1. Campagnes voor bijhouden maken in Zoeken, Sociaal en Commerce:

   1. Creeer [&#x200B; dummy details van de netwerkrekening &#x200B;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Als u meerdere accounts in één advertentienetwerk hebt, consolideert u deze vervolgens in één account in de weergave [!UICONTROL Accounts] .

      [!DNL Naver] biedt geen API-ondersteuning voor het uploaden van trackingparameters naar het advertentienetwerk. Nochtans, kunt u het volgen parameters produceren gebruikend bulksbladen en manueel hen toevoegen binnen het advertentienetwerk (per Stap 2). Om de volgende parameters te produceren, moet u de &quot;[!UICONTROL EF Redirect]&quot;het volgen methode gebruiken. U kunt optioneel alle gewenste toevoegingsparameters toevoegen.

      Zoeken, Sociaal en Commerce neemt de parameter `ev_cl={ef_uniqueid}` automatisch op in URL&#39;s die worden opgehaald in de bulksbladen voor de account. Deze unieke id wordt gebruikt om de gegevens van de campagne aan te passen aan de kosten en op de gegevens te klikken die u uploadt.

   1. Campagnes instellen om te volgen:

      1. Maak binnen het advertentienetwerk een bulksbladbestand met alle entiteiten en de vereiste bovenliggende entiteiten die u wilt bijhouden bij Zoeken, Sociaal en Commerce.

         U kunt gegevens over trefwoorden opnemen, zoals de bovenliggende campagnes en ad-groups.

      1. Bewerk het bulksbladdossier, indien nodig, zodat het het Onderzoek, Sociale, &amp; formaat van het Commerce [&#x200B; bulksheet volgt dat voor  [!DNL Naver]  wordt vereist rekeningen &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. In Onderzoek, Sociaal, &amp; Commerce, [&#x200B; uploadt het bulksbladdossier &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >Opmerking: met Zoeken, Sociaal en Commerce worden de gegevens niet op de netwerkaccount van de advertentie geplaatst.

1. Tekstspatiëring instellen voor de campagnes:

   1. In Onderzoek, Sociaal, &amp; Commerce, [&#x200B; download een nieuw bulksheet dossier &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) gebruikend de optie aan &quot;[!UICONTROL Generate Tracking URLs].&quot;

   Als u de optie &quot;[!UICONTROL Generate Tracking URLs]&quot; gebruikt, wordt in het veld [!UICONTROL Destination URL] voor elk trefwoord de code Zoeken, Sociaal en Commerce-tracking toegevoegd, die vooraf aan de waarde [!UICONTROL Base URL] is ingesteld.

   Hieronder ziet u een voorbeeld van de doel-URL met tekstspatiëring:

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Kopieer de [!UICONTROL Destination URL] -waarden in het gedownloade bulksbladbestand naar de relevante trefwoordinstellingen in het netwerk.

      U kunt URLs aan de relevante entiteiten toevoegen door het dossier aan het netwerk binnen de redacteur van het ad netwerk te uploaden. In dat geval, kunt u sommige kolommen, volgens de gegevensvereisten van het netwerk moeten verwijderen. Anders moet u de URL&#39;s handmatig invoeren in het netwerk.

1. Periodiek download klik en kostengegevens die dagelijks van het advertentienetwerk voor de sleutelwoorden of ad groep-vlakke merkadvertenties worden samengevoegd die u volgt, en dan [&#x200B; uploadt de klik en kostengegevens &#x200B;](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) aan Onderzoek, Sociale, &amp; Commerce in het [&#x200B; vereiste formaat &#x200B;](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Neem de volledige accounthiërarchie en alle gegevens op die u wilt opnemen. Zoeken, Sociaal en Commerce komen overeen met de geüploade gegevens met gegevens in bestaande campagnes.

1. (Optioneel) Als u tags van de service voor het bijhouden van Adobe Advertising-conversies op uw webpagina&#39;s gebruikt om conversies bij te houden die niet op het advertentienetwerk worden bijgehouden, stuurt u feed-bestanden met dagelijks geaggregeerde conversiegegevens die u wilt toevoegen aan uw traceringscampagnes.

   Neem voor meer informatie contact op met uw Adobe-accountteam.

Alle geüploade volggegevens zijn beschikbaar via [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] in de weergaven [!UICONTROL Accounts] , [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] en [!UICONTROL Keywords] . Deze is ook beschikbaar voor rapporten in de weergave [!UICONTROL Insights & Reports] .

>[!MORELIKETHIS]
>
>* [&#x200B; Bijlage - Vereiste bulksheet- gegevens voor  [!DNL Naver]  rekeningen &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [&#x200B; Upload verkeer en omzettingsmetriek voor  [!DNL Naver]  het volgen-slechts rekeningen &#x200B;](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [&#x200B; Metrische gegevensvereisten voor  [!DNL Naver]  het volgen-slechts rekeningen &#x200B;](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [&#x200B; klik-volgende formaten voor  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
