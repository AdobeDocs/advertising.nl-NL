---
title: Bekijk de Sites, Advertenties, Frequentie, en Details van de Inventaris voor een Plaatsing
description: Leer hoe u de beoogde sites, advertenties, frequentie en inventarisgegevens voor een plaatsing bekijkt.
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 0f022babeab6c044949760cedc103323eb0cc950
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Bekijk de Sites, Advertenties, Frequentie, en Details van de Inventaris voor een Plaatsing

Voor elke plaatsing, kunt u a (detailmening [) [!UICONTROL Inspector] openen, die van alle gerichte plaatsen, advertenties, en overeenkomsten in een plaatsing een lijst maakt. &#x200B;](placement-details-view.md) Het omvat ook frequentiegegevens voor de plaatsing. U kunt de gegevens optioneel vanuit elk tabblad exporteren.

![&#x200B; de inspecteur van de Plaatsing &#x200B;](/help/dsp/assets/placement-inspector.png)

## Informatie in de Placement [!UICONTROL Inspector] {#placement-inspector}

* **[!UICONTROL Sites]:** Alle sites waarop de plaatsing indrukken heeft.

  Het tabblad [!UICONTROL Sites] bevat zoek- en filterfuncties, dezelfde standaard- en aangepaste kolomweergaveopties die beschikbaar zijn op de hoofdpagina en een [!UICONTROL Exclude] -knop in elke rij, zodat u een site snel van de plaatsing kunt uitsluiten.

* **[!UICONTROL Ads]:** Alle advertenties in de plaatsing.

  Het tabblad [!UICONTROL Ads] bevat zoek- en filterfuncties, dezelfde standaard- en aangepaste kolomweergaveopties die beschikbaar zijn op de hoofdpagina, en knoppen voor snelle actie in elke rij, zoals [!UICONTROL View Ad Approvals] .

* **[!UICONTROL Frequency]:** Gegevens voor elk advertentieniveau voor de plaatsing, die omvatten:
   * het ad-frequentieniveau (bijvoorbeeld &quot;1&quot; voor alle gevallen waarin gebruikers een advertentie één keer zagen)
   * het geschatte unieke aantal apparaten/browsers of personen (afhankelijk van de opgegeven [!UICONTROL Cross Device Level] voor de campagne) die op het opgegeven frequentieniveau afdrukken hebben ontvangen
   * het geschatte aantal indrukkingen op het opgegeven frequentieniveau
   * de geschatte gemiddelde frequentie voor het gespecificeerde frequentieniveau. Deze waarde is gelijk aan (Geschatte Impressies)/(Geschatte Uniques).

* **[!UICONTROL Inventory]:** Informatie over alle overeenkomsten die op de plaatsing betrekking hebben.

  Op het tabblad [!UICONTROL Inventory] kunt u snel problemen oplossen door prestatiestatistieken zoals [!UICONTROL Auctions] , [!UICONTROL Bids] en [!UICONTROL Win Rate] weer te geven. Het tabblad bevat zoek- en filterfuncties, dezelfde standaard- en aangepaste kolomweergaveopties die beschikbaar zijn op de hoofdpagina, en snelle actieknoppen in elke rij, inclusief [!UICONTROL Edit] , [!UICONTROL View Report] en [[!UICONTROL Auction Insights] voor meer informatie over het oplossen van problemen &#x200B;](/help/dsp/inventory/private-deal-auction-insights.md) .

## De [!UICONTROL Placement Inspector] openen {#inspector-open}

1. Open de weergave Plaatsen voor de bovenliggende campagne of het bovenliggende pakket:

   * Alle plaatsen in de bovenliggende campagne weergeven:

      1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

      1. Klik op de naam van de campagne.

      1. Klik op de tab **[!UICONTROL Placements]** .

   * Alle plaatsen in het bovenliggende pakket weergeven:

      1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

      1. Klik op de naam van de campagne.

      1. Klik op de tab **[!UICONTROL Packages]** .

      1. Klik op de naam van het bovenliggende pakket.

1. Plaats de cursor op de plaatsingsrij en klik op **[!UICONTROL ...]** > **[!UICONTROL Analyze]** > **[!UICONTROL Inspector]** .

1. (Facultatief) [&#x200B; verander de kolommening &#x200B;](campaign-data-views-manage.md#column-view-change) zoals nodig om de vereiste metriek te bekijken.

1. (Facultatief) om de gegevens over om het even welk lusje uit te voeren, klik ![&#x200B; Meer &#x200B;](/help/search-social-commerce/assets/more.png " ") in het hogere recht, en klik dan **[!UICONTROL Export]**.

   De gegevens worden opgeslagen in de standaarddownloadmap van uw browser als een rapport in XLSM-indeling.

## Een advertentie verwijderen uit een advertentie uit de [!UICONTROL Placement Inspector] {#remove-ads-placement-inspector}

1. [&#x200B; open [!UICONTROL Placement Inspector]](#inspector-open).

1. Klik op de tab **[!UICONTROL Ads]** .

1. Klik naast de naam van de advertentie op **[!UICONTROL ...]** > **[!UICONTROL Detach]** .

## Probleeminventarisatie

| Probleem | Mogelijke oorzaak | Te nemen handelingen |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | De uitgever is niet begonnen met het verzenden van biedaanvragen. | Contacteer de uitgever om de overeenkomst te activeren. |
| | De overeenkomst werd opstelling verkeerd, zoals door een onjuiste externe overeenkomstenidentiteitskaart in te gaan. | Bevestig de overeenkomstendetails en geef de overeenkomst uit. |
| [!UICONTROL Auctions but no Bids] | De plaatsing richt zich niet op de inkomende biedingsverzoeken voor de overeenkomst. <br><br> Bijvoorbeeld, zou een plaatsing zich op een aardrijkskunde kunnen richten die niet voor de overeenkomst in aanmerking komt. | Bewerk indien nodig de plaatsingsdoelen om te voorkomen dat problemen bij de plaatsing onder de aandacht worden gebracht. |
| | De plaatsing heeft geen actieve advertentie met het vereiste media type voor de overeenkomst. | Maak een advertentie met het juiste mediatype en koppel deze aan de plaatsing. |
| | De plaatsing heeft geen toereikend budget. | Verhoog het budget voor plaatsing zodat u op inkomende aanvragen kunt bieden. |
| | De datums van de plaatsingsvlucht overlappen niet met de data van de beeldlevering voor de overeenkomst. | Bewerk indien nodig de vluchtdatums van de plaatsing. |
| [!UICONTROL Low Win Rate] | Het maximumbod van de plaatsing (ondergrens of vast) is lager dan het minimum dat door de transactie wordt vereist. | Verhoog indien nodig de plaatsing [!UICONTROL Max Bid]. |
| | De plaatsing gebruikt vooraf geboden filters die het bieden beperken. | Verlaag de drempelwaarden van de filters vóór het bod om meer biedingen mogelijk te maken. |
| | De doelgerichtheid van het publiek voor de plaatsing is te beperkt. | Controleer of de opgegeven doelgroepen voldoende actieve gebruikers hebben en vouw zo mogelijk het publiek uit. |

>[!MORELIKETHIS]
>
>* [&#x200B; Types van Rapporten van Prestaties in de Meningen van het Beheer van de Campagne &#x200B;](campaign-reports-about.md)
>* [&#x200B; beheert Uw Kijken van Gegevens van de Campagne &#x200B;](campaign-data-views-manage.md)
