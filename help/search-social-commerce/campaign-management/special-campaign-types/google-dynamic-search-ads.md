---
title: Implementeren [!DNL Google Ads] dynamische zoekadvertenties
description: Meer informatie over de workflow voor het instellen van [!DNL Google Ads] dynamische zoekopdrachten.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Implementeren [!DNL Google Ads] dynamische zoekadvertenties

*[!DNL Google Ads]alleen-zoekcampagnes met creatief of alleen-trefwoord- en creatief bijhouden*

Dynamische zoekadvertenties gebruiken inhoud van uw website in plaats van trefwoorden om te bepalen wanneer u uw advertenties wilt weergeven. U kunt de pagina&#39;s in uw websites definiëren waarvan de inhoud wordt gebruikt om uw dynamische zoekadvertenties te activeren door afzonderlijke dynamische zoekdoelen voor de advertentiegroep in te stellen of door een instelling op campageniveau te kiezen om uw advertenties te richten met behulp van de inhoud van uw website.

U kunt dynamische zoekopdrachten afzonderlijk instellen of met behulp van bulksbladen. De volgende instructies bevatten koppelingen naar het maken van afzonderlijke entiteiten.

## Stappen die moeten worden ingesteld [!DNL Google Ads] dynamische zoekadvertenties

1. [Een campagne maken](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) voor dynamische zoekopdrachten:

   1. Stel aanvankelijk het campagnebudget in op 10% van uw dagelijkse uitgaven voor de zoekcampagne.

      U kunt het budget later verhogen nadat de advertenties hun waarde hebben bewezen.

   1. (Als u [!DNL Google Ads] om uw dynamische zoekadvertenties weer te geven op basis van de inhoud van uw website) Geef het hoofddomein en de taal voor het domein op in het dialoogvenster [!UICONTROL DSA Options] sectie van de campagnemontages.

      >[!NOTE]
      >
      >Uw domein moet door worden geïndexeerd [!DNL Google Ads] biologische zoekindex die moet worden aangewezen. Ook, als het domein pagina&#39;s in veelvoudige talen bevat en u alle hen wilt richten, creeer een afzonderlijke campagne voor elke taal.

      Als u uw websitedomein niet gebruikt om uw advertenties te richten, creeer dan dynamische onderzoeksdoelstellingen (zie Stap 4) voor elke advertentiegroep. U kunt de doelen maken [individueel](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) of gebruiken [bulkgoederen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

   1. Zorg ervoor dat de campagne zich richt op het zoekkanaal en alleen op de [!DNL Google Ads] zoeknetwerk (niet het weergavenetwerk). Deze instellingen zijn beschikbaar via de [!UICONTROL Networks and Devices] tab.

   1. (Optioneel) Trefwoorden uitsluiten op het tabblad [!UICONTROL Negatives] tab.

   1. (Optioneel) Configureer een sjabloon voor bijhouden op campagneniveau, dat de sjabloon voor bijhouden op accountniveau overschrijft, maar op lagere niveaus kan worden overschreven.

      (Adverteerders met Adobe Analytics zonder server-side tracking) Als u tracering voor de reverse feed van Zoeken, Sociale &amp; Handel naar Analytics wilt opnemen, voegt u de s_kwcid-trackingcode toe aan de parameters voor toevoegen op accountniveau, waarmee de code aan de uiteindelijke URL wordt toegevoegd. Zie &quot;[De parameter s_kwcid tracking](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md).&quot;

1. [Een advertentiegroep maken](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) binnen de campagne, met inbegrip van de volgende stappen:

   1. Stel de [!UICONTROL Ad Group Type] tot **[!UICONTROL Search Dynamic].**

   1. Stel het standaardbod voor alle advertenties in.

      U kunt het standaardbod voor afzonderlijke dynamische zoekdoelen overschrijven als u deze configureert.

   1. (Optioneel) Configureer een volgsjabloon op ad-groepsniveau, dat eventuele volgsjablonen op hogere niveaus overschrijft, maar op advertentieniveau kan worden overschreven.

      Als u het bijhouden van Adobe Analytics op campagnereniveau hebt toegevoegd en u wilt deze voor de advertentiegroep opnemen, voegt u deze hier toe. Zie stap 1e.

1. [Maak elke dynamische zoekadvertentie](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) in de advertentiegroep.

   [!DNL Google Ads] Hiermee worden de kop, de weergave-URL en de bestemmingspagina-URL voor elke advertentie dynamisch gegenereerd. U kunt optioneel omleidingen en tekstspatiëring toevoegen aan de sjabloon voor reeksspatiëring op advertentieniveau, die de volgsjablonen op hogere niveaus overschrijft.
Als u het bijhouden van Adobe Analytics&#39;s op hogere niveaus wilt overschrijven met het bijhouden van advertenties, voegt u deze hier toe. Zie de stappen 1e en 2c.

1. (Vereist wanneer u niet het worteldomein en de taal voor het domein in de sectie van Opties DSA van de campagnemontages omvat; anders optioneel) Maken [dynamische zoekdoelen](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) voor de advertentiegroep. U kunt optioneel het advertentieniveau overschrijven met biedingen op doelniveau.

   De doelen bepalen of het advertentienetwerk alle pagina&#39;s of een subset van de pagina&#39;s in uw website gebruikt om uw dynamische zoekadvertenties te richten. Om de prestaties het best te volgen, vorm uw campagne met één ad groep per dynamisch onderzoeksdoel, en omvat een ad groep die alle criteria richt.

1. Zo nodig [de campagne-instellingen bewerken](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) het campagnebudget aanpassen en het verkeer verfijnen door extra trefwoorden van de campagne uit te sluiten.
