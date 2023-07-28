---
title: Implementeren [!DNL Naver] accounts met alleen traceren
description: Leer hoe u traceercampagnes instelt voor uw [!DNL Naver] accounts zodat u de prestaties van advertenties die u rechtstreeks via het advertentienetwerk koopt, kunt bijhouden, rapporteren en visualiseren.
exl-id: 8013d4e8-0b4f-41a7-9c1b-10c55349930f
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# Implementeren [!DNL Naver] accounts met alleen traceren

*[!DNL Naver]alleen accounts*

U kunt volgcampagnes voor uw [!DNL Naver] accounts zodat u de prestaties van advertenties die u rechtstreeks via het advertentienetwerk koopt, kunt bijhouden, rapporteren en visualiseren. Met Zoeken, Sociale media en Handel worden geen gegevens gesynchroniseerd met het advertentienetwerk, wordt het bijhouden van gegevens automatisch geüpload en worden geen biedingen voor het account geplaatst.

Bij het bijhouden van campagnes worden uw bestaande campagnes, groepen en trefwoorden gerepliceerd. Zodra u de rekeningsstructuur in Onderzoek, Sociale, &amp; Handel en het volgen aan de originele campagnes binnen het advertentienetwerk hebt gecreeerd, kunt u dagelijkse metriek van het netwerkverkeer voor uw sleutelwoorden of advertenties uploaden. Met Zoeken, Sociaal en Handel kunt u uw conversies vervolgens aan uw advertenties en trefwoorden toewijzen.

U kunt prestatiesmetriek over al uw campagnes en voor om het even welke individuele campagne, ad groep, of sleutelwoord/advertentie volgen. U kunt ook informatie over hen in het meest basisch, geavanceerd, en hulprapporten, samen met gegevens voor uw andere advertentienetwerken omvatten. Ondersteuning voor het exporteren van metriek naar Adobe Analytics is niet beschikbaar, maar Zoeken, Sociaal en Handel kan wel worden gesynchroniseerd [cijfers die je bijhoudt [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) in Search, Social, &amp; Commerce.

>[!NOTE]
>
>U kunt geen volgcampagnes toevoegen aan een portfolio voor optimalisatie.

1. Trainingscampagnes maken in Zoeken, Sociale Zaken en Handel:

   1. Maken [dummy-netwerkaccountgegevens](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Als u veelvoudige rekeningen binnen één enkel ad netwerk hebt, dan consolideer hen in één rekening in [!UICONTROL Accounts] weergeven.

      [!DNL Naver] biedt geen API-ondersteuning voor het uploaden van trackingparameters naar het advertentienetwerk. Nochtans, kunt u het volgen parameters produceren gebruikend bulksbladen en manueel hen toevoegen binnen het advertentienetwerk (per Stap 2). Als u de volgende parameters wilt genereren, moet u &quot;[!UICONTROL EF Redirect]&quot;. U kunt optioneel alle gewenste toevoegingsparameters toevoegen.

      De parameter voor zoeken, sociale zaken en handel wordt automatisch opgenomen `ev_cl={ef_uniqueid}` in URL&#39;s die worden bijgehouden, wordt deze gegenereerd in bulksbladen voor de account. Deze unieke id wordt gebruikt om de gegevens van de campagne aan te passen aan de kosten en op de gegevens te klikken die u uploadt.

   1. Campagnes instellen om te volgen:

      1. Maak binnen het advertentienetwerk een bulksbladbestand met alle entiteiten en hun vereiste bovenliggende entiteiten die u wilt bijhouden bij Zoeken, Sociale media en Handel voor de account.

         U kunt gegevens over trefwoorden opnemen, zoals de bovenliggende campagnes en ad-groups.

      1. Bewerk indien nodig het bulksbladbestand, zodat dit volgt op Zoeken, Sociaal en Handel [bulksheet-indeling vereist voor [!DNL Naver] rekeningen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. In Zoeken, Sociale &amp; Handel, [uploadt het bulksbladbestand](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >Opmerking: de gegevens worden niet via Zoeken, Sociale Zaken en Handel op de account van het advertentienetwerk geplaatst.

1. Tekstspatiëring instellen voor de campagnes:

   1. In Zoeken, Sociale &amp; Handel, [een nieuw bulksbladbestand downloaden](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) met de optie &quot;[!UICONTROL Generate Tracking URLs].&quot;

   De &quot;[!UICONTROL Generate Tracking URLs]Met de optie &quot; wordt de [!UICONTROL Destination URL] veld voor elk trefwoord met de trackingcode Zoeken, Sociaal en Handel vooraf ingesteld op de [!UICONTROL Base URL] waarde.

   Hieronder ziet u een voorbeeld van de doel-URL met tekstspatiëring:

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. De [!UICONTROL Destination URL] waarden in het gedownloade bulkbladbestand naar de relevante trefwoordinstellingen in het netwerk.

      U kunt URLs aan de relevante entiteiten toevoegen door het dossier aan het netwerk binnen de redacteur van het ad netwerk te uploaden. In dat geval, kunt u sommige kolommen, volgens de gegevensvereisten van het netwerk moeten verwijderen. Anders moet u de URL&#39;s handmatig invoeren in het netwerk.

1. Download regelmatig klik- en kostengegevens die dagelijks van het advertentienetwerk worden geaggregeerd voor de trefwoorden of advertenties op groepsniveau die u bijhoudt, en vervolgens [uploaden klik en kostengegevens](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) om te zoeken, sociale zaken en handel in de [vereiste indeling](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Neem de volledige accounthiërarchie en alle gegevens op die u wilt opnemen. Zoeken, Sociaal en Handel komen overeen met de geüploade gegevens met gegevens in bestaande campagnes.

1. (Optioneel) Als u servicetags voor conversie van Adobe Advertising naar webpagina&#39;s gebruikt om conversies bij te houden die niet op het advertentienetwerk worden bijgehouden, stuurt u feed-bestanden met dagelijks geaggregeerde conversiegegevens naar uw traceringscampagnes.

   Neem voor meer informatie contact op met uw Adobe-accountteam.

Alle geüploade volggegevens zijn beschikbaar via [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] binnen de [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups], en [!UICONTROL Keywords] weergaven. Het is ook beschikbaar voor rapporten in [!UICONTROL Insights & Reports] weergeven.

>[!MORELIKETHIS]
>
>* [Aanhangsel - Vereiste gegevens voor het informatieblad voor [!DNL Naver] rekeningen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Verkeer en conversie uploaden voor [!DNL Naver] accounts met alleen traceren](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Metrische gegevensvereisten voor [!DNL Naver] accounts met alleen traceren](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Opmaak voor het bijhouden van klikken voor [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
