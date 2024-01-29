---
title: Bekijk de Sites, Advertenties, Frequentie, en Details van de Inventaris voor een Plaatsing
description: Leer hoe u de beoogde sites, advertenties, frequentie en inventarisgegevens voor een plaatsing bekijkt.
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# Bekijk de Sites, Advertenties, Frequentie, en Details van de Inventaris voor een Plaatsing

Voor elke plaatsing kunt u [openen a (detailweergave) [!UICONTROL Inspector])](placement-details-view.md), waarin alle doelsites, advertenties en plaatsingsovereenkomsten worden vermeld. Het omvat ook frequentiegegevens voor de plaatsing. U kunt de gegevens optioneel vanuit elk tabblad exporteren.

![Plaatsingscontrole](/help/dsp/assets/placement-inspector.png)

## Informatie in de plaats [!UICONTROL Inspector] {#placement-inspector}

* **[!UICONTROL Sites]:** Alle sites waarop de plaatsing indrukt.

  De [!UICONTROL Sites] tab bevat zoek- en filterfuncties, dezelfde standaard- en aangepaste kolomweergaveopties die beschikbaar zijn op de hoofdpagina, en een [!UICONTROL Exclude] in elke rij zodat u een site snel van de plaatsing kunt uitsluiten.

* **[!UICONTROL Ads]:** Alle advertenties in de plaatsing.

  De [!UICONTROL Ads] tab bevat zoek- en filterfuncties, dezelfde standaard- en aangepaste kolomweergaveopties die beschikbaar zijn op de hoofdpagina, en snelle actieknoppen in elke rij, zoals [!UICONTROL Pause] (zodat u snel een advertentie kunt pauzeren).

* **[!UICONTROL Frequency]:** Gegevens voor elk ad-frequentieniveau voor de plaatsing, waaronder:
   * het ad-frequentieniveau (bijvoorbeeld &quot;1&quot; voor alle gevallen waarin gebruikers een advertentie één keer zagen)
   * het geschatte unieke aantal apparaten/browsers of personen (afhankelijk van het opgegeven aantal [!UICONTROL Cross Device Level] voor de campagne) die indrukken hebben gekregen op het opgegeven frequentieniveau
   * het geschatte aantal indrukkingen op het opgegeven frequentieniveau
   * de geschatte gemiddelde frequentie voor het gespecificeerde frequentieniveau. Deze waarde is gelijk aan (Geschatte Impressies)/(Geschatte Uniques).

* **[!UICONTROL Inventory]:** Informatie over alle overeenkomsten waarop de plaatsing betrekking heeft.

  De [!UICONTROL Inventory] het lusje laat snelle het oplossen van problemen door prestatiesstatistieken te tonen, zoals [!UICONTROL Auctions], [!UICONTROL Bids], en [!UICONTROL Win Rate]. Het tabblad bevat zoek- en filterfuncties, dezelfde standaard- en aangepaste kolomweergaveopties die beschikbaar zijn op de hoofdpagina, en knoppen voor snelle actie in elke rij, waaronder [!UICONTROL Edit], [!UICONTROL View Report], en [[!UICONTROL Auction Insights] voor verdere probleemoplossing](/help/dsp/inventory/private-deal-auction-insights.md).

## Open de [!UICONTROL Placement Inspector]

1. Open de weergave Plaatsen voor de bovenliggende campagne of het bovenliggende pakket:

   * Alle plaatsen in de bovenliggende campagne weergeven:

      1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

      1. Klik op de naam van de campagne.

      1. Klik op de knop **[!UICONTROL Placements]** tab.

   * Alle plaatsen in het bovenliggende pakket weergeven:

      1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

      1. Klik op de naam van de campagne.

      1. Klik op de knop **[!UICONTROL Packages]** tab.

      1. Klik op de naam van het bovenliggende pakket.

1. Plaats de cursor op de plaatsingsrij en klik op **[!UICONTROL More]** en klik vervolgens op een optie:

   * Klik op **[!UICONTROL Sites]**.

   * Als u alle advertenties in de plaatsing wilt weergeven, klikt u op **[!UICONTROL Ads]**.

   * Als u de frequentiegegevens voor de plaatsing wilt weergeven, klikt u op **[!UICONTROL Frequency]**.

   * Als u alle overeenkomsten wilt weergeven die de plaatsingsdoelen hebben, klikt u op **[!UICONTROL Inventory]**.

1. (Optioneel) [De kolomweergave wijzigen](campaign-data-views-manage.md#column-view-change) om de vereiste maatstaven weer te geven.

1. (Optioneel) Als u de gegevens op een willekeurig tabblad wilt exporteren, klikt u op ![Meer](/help/search-social-commerce/assets/more.png "Meer") in de rechterbovenhoek en klik vervolgens op **[!UICONTROL Export]**.

   De gegevens worden opgeslagen in de standaarddownloadmap van uw browser als een rapport in XLSM-indeling.

## Probleeminventarisatie

| Probleem | Mogelijke oorzaak | Te nemen handelingen |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | De uitgever is niet begonnen met het verzenden van biedaanvragen. | Contacteer de uitgever om de overeenkomst te activeren. |
| | De overeenkomst werd opstelling verkeerd, zoals door een onjuiste externe overeenkomstenidentiteitskaart in te gaan. | Bevestig de overeenkomstendetails en geef de overeenkomst uit. |
| [!UICONTROL Auctions but no Bids] | De plaatsing richt zich niet op de inkomende biedingsverzoeken voor de overeenkomst. <br><br> Bijvoorbeeld, zou een plaatsing zich op een geografie kunnen richten die niet voor de overeenkomst in aanmerking komt. | Bewerk indien nodig de plaatsingsdoelen om te voorkomen dat problemen bij de plaatsing onder de aandacht worden gebracht. |
| | De plaatsing heeft geen actieve advertentie met het vereiste media type voor de overeenkomst. | Maak een advertentie met het juiste mediatype en koppel deze aan de plaatsing. |
| | De plaatsing heeft geen toereikend budget. | Verhoog het budget voor plaatsing zodat u op inkomende aanvragen kunt bieden. |
| | De datums van de plaatsingsvlucht overlappen niet met de data van de beeldlevering voor de overeenkomst. | Bewerk indien nodig de vluchtdatums van de plaatsing. |
| [!UICONTROL Low Win Rate] | Het maximumbod van de plaatsing (ondergrens of vast) is lager dan het minimum dat door de transactie wordt vereist. | De plaatsing verhogen [!UICONTROL Max Bid] indien nodig. |
| | De plaatsing gebruikt vooraf geboden filters die het bieden beperken. | Verlaag de drempelwaarden van de filters vóór het bod om meer biedingen mogelijk te maken. |
| | De doelgerichtheid van het publiek voor de plaatsing is te beperkt. | Controleer of de opgegeven doelgroepen voldoende actieve gebruikers hebben en vouw zo mogelijk het publiek uit. |

>[!MORELIKETHIS]
>
>* [Typen prestatierapporten in Campaign Management-weergaven](campaign-reports-about.md)
>* [De weergave van uw Campagnegegevens beheren](campaign-data-views-manage.md)
