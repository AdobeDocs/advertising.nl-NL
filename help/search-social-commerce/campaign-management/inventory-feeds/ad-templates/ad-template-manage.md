---
title: Advertentiesjablonen beheren voor voorraadfeeds
description: Meer informatie over het beheren van advertentiesjablonen waarmee je voorraadgegevens kunnen worden verwerkt om de accountstructuur te beheren en dynamische advertenties te leveren.
exl-id: b0e540cf-8735-4812-9df5-58f488a25ba5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# Advertentiesjablonen beheren voor voorraadfeeds

*[!DNL Google Ads], [!DNL Microsoft Advertising] , [!DNL Yahoo! Japan Ads] (alleen acties verwijderen) en [!DNL Yandex] alleen accounts*

Voor of nadat u gegevens hebt geüpload, kunt u specifieke advertentiesjablonen maken voor de zoekmachine waarmee uw gegevens kunnen worden verwerkt. U kunt sjablonen maken voor tekstadvertenties en uitgebreide/uitgebreide tekstadvertenties, [!DNL Google Ads] en [!DNL Microsoft Advertising] responsieve zoekadvertenties en voor [!DNL Google Ads] - en [!DNL Microsoft Advertising] winkeladvertenties.

U kunt elke sjabloon aan één feed-bestand, [!DNL Google Merchant Center] -account of [!DNL Microsoft Merchant Center] -account koppelen en u kunt meerdere sjablonen aan hetzelfde feed-bestand of dezelfde account koppelen. Een advertentiesjabloon kan variabelen bevatten, die worden vervangen door feitelijke gegevenskolommen uit een geüpload bestand of een account. In de meeste gevallen, kunnen de variabelen ook [&#x200B; een bepalingsgroep &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) omvatten u opstelling in Onderzoek, Sociaal, &amp; Commerce om veelvoudige advertenties, sleutelwoorden, campagnes, of ad groepen voor elke toepasselijke rij in het gegevensdossier tot stand te brengen. Met de sjabloonopties kunt u een nieuwe accountstructuur (campagnes, groepen en trefwoorden) voor de advertenties maken of de advertenties toewijzen aan de bestaande accountstructuur.

U kunt optioneel nieuwe sjablonen maken door bestaande sjablonen te klonen en bestaande sjablonen te bewerken.

Zodra u een malplaatje creeert en het met een dossier van de gegevensvoer of een bedrijfscentrum rekening associeert, kunt u de gegevens in het dossier door het malplaatje verspreiden om campagnegegevens en rekeningsstructuur tot stand te brengen, naar keuze creërend een bulksbladdossier voor overzicht of voor directe post aan het advertentienetwerk.

Elke sjabloon kan worden geactiveerd, gepauzeerd of verwijderd. De gegevens van het voer kunnen automatisch worden verspreid slechts door actieve malplaatjes. U kunt gegevens echter handmatig doorgeven via een gepauzeerde sjabloon.

## Een voedersjabloon maken, klonen of bewerken

Maak aparte sjablonen voor tekst en uitgebreide/uitgebreide tekstadvertenties, responsieve zoekopdrachten, [!DNL Google Ads] winkeladvertenties en [!DNL Microsoft Advertising] winkeladvertenties.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** , dat wordt geopend op de tab [!UICONTROL Templates] .

1. Voer een van de volgende handelingen uit:

   * Als u een geheel nieuwe sjabloon wilt maken, klikt u op **[!UICONTROL Create/Clone]** in de werkbalk boven de datatabel en selecteert u vervolgens de toepasselijke advertentienetwerken.

   * Een bestaande sjabloon klonen:

      1. Schakel het selectievakje in naast de sjabloon die u wilt kopiëren.

      1. Klik in de werkbalk boven de datatabel op **[!UICONTROL Create/Clone]** en selecteer vervolgens het toepasselijke advertentienetwerk.

   * (Om een bestaand malplaatje uit te geven) naast de malplaatjenaam, klik ![&#x200B; Mening/geef montages &#x200B;](/help/search-social-commerce/assets/settings.png " Mening uit/geef montages ").

1. Specificeer de montages voor de [&#x200B; tekst en malplaatje &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md), [[!DNL Google Ads]  het winkelen en malplaatje &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md), of [[!DNL Microsoft Advertising]  het winkelen en malplaatje &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md):

   1. Geef boven aan het venster met sjablooninstellingen de naam van de sjabloon en het toepasselijke account op.

      Wanneer u een bestaande sjabloon kloont, wijzigt u de naam van de nieuwe sjabloon zodat de advertenties die op basis van de nieuwe sjabloon worden gemaakt, niet worden gekoppeld aan advertenties die op basis van de bronsjabloon worden gemaakt.

   1. (Optioneel) Geef in de linkerkolom het bestand met de productfeed of de zakelijke account op waarvan de gegevens via de sjabloon worden doorgegeven:

      * (Voor de dossiers van de productvoer) om een eerder-geupload dossier te selecteren, klik ![&#x200B; neer pijl &#x200B;](/help/search-social-commerce/assets/arrow-down-dropdown.png " neer pijl ") en selecteer een dossier van de lijst van beschikbare voederdossiers. Als u een nieuw bestand wilt uploaden, geeft u het bestand op door het volledige pad en de bestandsnaam in te voeren of door op **[!UICONTROL Browse]** te klikken om het bestand op uw apparaat of netwerk te zoeken. Klik vervolgens op **[!UICONTROL Upload]** .

      * (Voor een gesynchroniseerde zakelijke account) Selecteer de naam van de account.

      De kolommen voor het geselecteerde bestand of account worden weergegeven.

   1. Geef op het tabblad **[!UICONTROL Account Structure]** de instellingen voor de accountstructuur op.

   1. (Alleen tekstadvertenties) Klik op de tab **[!UICONTROL Keywords]** en geef de trefwoordinstellingen op.

   1. (Alleen tekst en responsieve zoekopdrachten) Klik op het tabblad **[!UICONTROL Ads]** en voer een van de volgende handelingen uit:

      >[!NOTE]
      >
      >* U kunt maximaal vier variatiesjablonen per standaardtekst en -sjabloon, vijf en variatiesjablonen per uitgebreide/uitgebreide tekst en sjabloon en drie en variatiesjablonen per responsieve zoekopdracht en sjabloon opnemen.
      >* Elke advertentiegroep kan maximaal drie ingeschakelde responsieve zoekadvertenties bevatten.
      >* U kunt bestaande standaardtekst en -variaties niet bewerken en bestaande sjablonen genereren niet langer standaardtekstadvertenties.
      >* Als u een advertentievariatiesjabloon verandert, dan kunnen de bestaande advertenties worden geschrapt en de nieuwe degenen kunnen worden gecreeerd wanneer u gegevens door het malplaatje verspreidt, [&#x200B; afhankelijk van het advertentietype en ad netwerk &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md).

      * Ga als volgt te werk om een advertentievariatie toe te voegen:

         1. Klik op **[!UICONTROL Add Ad Variation]** om een tekstadvertentie te maken, op **[!UICONTROL Add ETA Variation]** om een uitgebreide/uitgebreide tekstadvertentie te maken of op **[!UICONTROL Add RSA Variation]** om een responsieve tekstadvertentie te maken.

            Nadat u het advertentietype hebt opgegeven, kunt u alleen dat advertentietype met de sjabloon maken.

         1. Geef de advertentie-instellingen op.

            Voor responsieve zoekopdrachten kunt u 3-15 kopregels en 2-4 beschrijvingen opnemen.

         1. (Optioneel) Als u alle alternatieve en kopieervelden vooraf wilt vullen met tekst uit de oorspronkelijke en gekopieerde velden, schakelt u het selectievakje naast **[!UICONTROL Prefill]** in.

         1. (Optioneel) Als u nog een set toevoegingen aan een advertentie wilt toevoegen, die kan worden gebruikt als een van de regels in het origineel en de kopie de maximumlengte overschrijdt wanneer dynamische parameters tijdens de propagatie worden vervangen door gegevens, klikt u op **[!UICONTROL Add Alternate]** en voegt u vervolgens de alternatieve waarden toe.

            >[!NOTE]
            >
            >* Als de optie [!UICONTROL Prefill] is geselecteerd, worden de oorspronkelijke velden vooringevuld in de andere velden en kunt u deze naar wens bewerken.
            >* Alleen de velden voor het kopiëren van de advertentie die de maximale lengte overschrijden, worden vervangen door de alternatieve waarde. Als bijvoorbeeld alleen een originele kop of titel te lang is, gebruiken de gegenereerde en de variatie de alternatieve kop of titel en de oorspronkelijke beschrijvingen. Zorg er daarom voor dat de alternatieve advertentie-kopie zinvol is wanneer deze wordt gecombineerd met het origineel en de kopie.
            >* Als het origineel en de kopie voldoen aan de lengtevereisten van het zoekprogramma, wordt de alternatieve advertentiekopie verwijderd.
            >* U kunt maximaal vier alternatieven opgeven voor elk veld voor een advertentie-kopie.

         * Ga als volgt te werk om een advertentievariatie te bewerken:

            1. Bewerk de advertentie-instellingen.

               Voor responsieve zoekopdrachten kunt u 3-15 kopregels en 2-4 beschrijvingen opnemen.

            1. (Optioneel) Als u alle alternatieve en kopieervelden vooraf wilt vullen met tekst uit de oorspronkelijke en gekopieerde velden, schakelt u het selectievakje naast **[!UICONTROL Prefill]** in.

            1. (Optioneel) Als u nog een set toevoegingen aan een advertentie wilt toevoegen, die kan worden gebruikt als een van de regels in het origineel en de kopie de maximumlengte overschrijdt wanneer dynamische parameters tijdens de propagatie worden vervangen door gegevens, klikt u op **[!UICONTROL Add Alternate]** en voegt u vervolgens de alternatieve waarden toe.

               >[!NOTE]
               >
               >* Als de optie [!UICONTROL Prefill] is geselecteerd, worden de oorspronkelijke velden vooringevuld in de andere velden en kunt u deze naar wens bewerken.
               >* Alleen de velden voor het kopiëren van de advertentie die de maximale lengte overschrijden, worden vervangen door de alternatieve waarde. Als bijvoorbeeld alleen een originele kop of titel te lang is, gebruiken de gegenereerde en de variatie de alternatieve kop of titel en de oorspronkelijke beschrijvingen. Zorg er daarom voor dat de alternatieve advertentie-kopie zinvol is wanneer deze wordt gecombineerd met het origineel en de kopie.
               >* Als het origineel en de kopie voldoen aan de lengtevereisten van het zoekprogramma, wordt de alternatieve advertentiekopie verwijderd.
               >* U kunt maximaal vier alternatieven opgeven voor elk veld voor een advertentie-kopie.

         * Als u een advertentievariatie wilt verwijderen, klikt u op **[!UICONTROL Remove ETA Variation]** (voor uitgebreide/uitgebreide tekstadvertenties) of op **[!UICONTROL Remove RSA Variation]** (voor responsieve zoekadvertenties) naast de advertentievariatie, al naar gelang van toepassing.

   1. (Alleen winkelsjablonen) Klik op het tabblad **[!UICONTROL Product Groups]** en geef vervolgens informatie op over de productgroepen die u als doel wilt instellen.

   1. (Optioneel) Klik op de tab **[!UICONTROL Feed Filters]** en geef op welke rijen in het voederbestand u wilt doorgeven.

   1. (Optioneel) Klik op **[!UICONTROL Label Classifications tab]** en geef de waarden voor de labelclassificatie op die u wilt toewijzen aan de verschillende campagnecomponenten die worden gemaakt:

      1. Klik op het selectievakje naast **[!DNL \[Component\] Label Classifications]** .

      1. Ga als volgt te werk voor elke labelclassificatie die aan de component moet worden toegewezen:

         1. Klik op **[!UICONTROL Add Label Classification]**.

         1. Selecteer de labelclassificatie en selecteer vervolgens een bestaande waarde of voer een nieuwe waarde in.

1. Sla de sjabloon op:

   * Als u de sjabloon gewoon wilt opslaan, klikt u op **[!UICONTROL Save]** en vervolgens nogmaals op **[!UICONTROL Save]** .

   * Als u de sjabloon wilt opslaan en het opgegeven gegevensbestand wilt doorgeven, klikt u op **[!UICONTROL Save]** en vervolgens op **[!UICONTROL Save & Propagate]** .

## De status van voedersjablonen wijzigen

U kunt elke gepauzeerde sjabloon voor gegevensinvoer activeren of een actieve sjabloon voor gegevensinvoer pauzeren.

>[!NOTE]
>
>U kunt gegevens manueel verspreiden door een gepauzeerde malplaatje, maar het gegeven wordt niet automatisch verspreid door het.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** , dat wordt geopend op de tab [!UICONTROL Templates] .

1. Schakel het selectievakje in naast elke sjabloon waarvan u de status wilt wijzigen.

1. Klik in de werkbalk boven de datatabel op **[!UICONTROL Change Status]** en klik vervolgens op **[!UICONTROL Activate]** of **[!UICONTROL Pause]** .

## Feed-sjablonen verwijderen

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** , dat wordt geopend op de tab [!UICONTROL Templates] .

1. Schakel het selectievakje in naast elke sjabloon die u wilt verwijderen.

1. Klik in de werkbalk boven de gegevenstabel op **[!UICONTROL Delete]** .

1. Klik in het bevestigingsbericht op **[!UICONTROL Yes]** .

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer automatiserend en beheer gebruikend inventarisvoer &#x200B;](../inventory-feeds-about.md)
>* [&#x200B; Tekst en ontvankelijke onderzoek en malplaatjemontages &#x200B;](template-text-rsa.md)
>* [[!DNL Google Ads]  het winkelen en malplaatjemontages &#x200B;](template-google-shopping.md)
>* [[!DNL Microsoft Advertising]  het winkelen en malplaatjemontages &#x200B;](template-microsoft-shopping.md)
>* [&#x200B; doorgeven voedergegevens door malplaatjes &#x200B;](../feed-data-propagate.md)
