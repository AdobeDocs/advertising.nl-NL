---
title: Advertentiesjablonen beheren voor voorraadfeeds
description: Meer informatie over het beheren van advertentiesjablonen waarmee je voorraadgegevens kunnen worden verwerkt om de accountstructuur te beheren en dynamische advertenties te leveren.
exl-id: b26fc32a-76bc-470a-8ce5-fbaad4b3ca71
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '1415'
ht-degree: 0%

---

# Advertentiesjablonen beheren voor voorraadfeeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

Voor of nadat u gegevens hebt geüpload, kunt u specifieke advertentiesjablonen maken voor de zoekmachine waarmee uw gegevens kunnen worden verwerkt. U kunt sjablonen maken voor tekstadvertenties en uitgebreide/uitgebreide tekstadvertenties. [!DNL Google Ads] en [!DNL Microsoft® Advertising] responsieve zoekopdrachten en voor [!DNL Google Ads] en [!DNL Microsoft® Advertising] winkeladvertenties.

U kunt elke sjabloon aan één feed-bestand koppelen. [!DNL Google Merchant Center] rekening, of [!DNL Microsoft® Merchant Center] en u kunt meerdere sjablonen koppelen aan hetzelfde feed-bestand of dezelfde account. Een advertentiesjabloon kan variabelen bevatten, die worden vervangen door feitelijke gegevenskolommen uit een geüpload bestand of een account. In de meeste gevallen kunnen de variabelen ook [een wijziginggroep](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) als u meerdere advertenties, trefwoorden, campagnes of advertentiegroepen voor elke toepasselijke rij in het gegevensbestand wilt maken. Met de sjabloonopties kunt u een nieuwe accountstructuur (campagnes, groepen en trefwoorden) voor de advertenties maken of de advertenties toewijzen aan de bestaande accountstructuur.

U kunt optioneel nieuwe sjablonen maken door bestaande sjablonen te klonen en bestaande sjablonen te bewerken.

Zodra u een malplaatje creeert en het met een dossier van de gegevensvoer of een bedrijfscentrum rekening associeert, kunt u de gegevens in het dossier door het malplaatje verspreiden om campagnegegevens en rekeningsstructuur tot stand te brengen, naar keuze creërend een bulksbladdossier voor overzicht of voor directe post aan het advertentienetwerk.

Elke sjabloon kan worden geactiveerd, gepauzeerd of verwijderd. De gegevens van het voer kunnen automatisch worden verspreid slechts door actieve malplaatjes. U kunt gegevens echter handmatig doorgeven via een gepauzeerde sjabloon.

## Een voedersjabloon maken, klonen of bewerken

Maak aparte sjablonen voor tekst en uitgebreide/uitgebreide tekstadvertenties, responsieve zoekopdrachten, [!DNL Google Ads] winkeladvertenties, en [!DNL Microsoft® Advertising] winkeladvertenties.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, die voor de [!UICONTROL Templates] tab.

1. Voer een van de volgende handelingen uit:

   * Als u een geheel nieuwe sjabloon wilt maken, klikt u op **[!UICONTROL Create/Clone]** in de toolbar boven de gegevenslijst, en selecteer dan het toepasselijke advertentienetwerk.

   * Een bestaande sjabloon klonen:

      1. Schakel het selectievakje in naast de sjabloon die u wilt kopiëren.

      1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Create/Clone]** en selecteert u vervolgens het toepasselijke advertentienetwerk.

   * (Als u een bestaande sjabloon wilt bewerken) Klik naast de sjabloonnaam op ![Instellingen weergeven/bewerken](/help/search-social-commerce/assets/settings.png "Instellingen weergeven/bewerken").

1. Geef de instellingen op voor de [tekst en sjabloon](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md), [[!DNL Google Ads] winkelsjabloon](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md), of [[!DNL Microsoft® Advertising] winkelsjabloon](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md):

   1. Geef boven aan het venster met sjablooninstellingen de naam van de sjabloon en het toepasselijke account op.

      Wanneer u een bestaande sjabloon kloont, wijzigt u de naam van de nieuwe sjabloon zodat de advertenties die op basis van de nieuwe sjabloon worden gemaakt, niet worden gekoppeld aan advertenties die op basis van de bronsjabloon worden gemaakt.

   1. (Optioneel) Geef in de linkerkolom het bestand met de productfeed of de zakelijke account op waarvan de gegevens via de sjabloon worden doorgegeven:

      * (Voor bestanden met productfeed) Als u een eerder geüpload bestand wilt selecteren, klikt u ![Pijl-omlaag](/help/search-social-commerce/assets/arrow-down-dropdown.png "Pijl-omlaag") en selecteer een bestand in de lijst met beschikbare feed-bestanden. Als u een nieuw bestand wilt uploaden, geeft u het bestand op door het volledige pad en de volledige bestandsnaam in te voeren of door op **[!UICONTROL Browse]** om het bestand op uw apparaat of netwerk te zoeken en klik vervolgens op **[!UICONTROL Upload]**.

      * (Voor een gesynchroniseerde zakelijke account) Selecteer de naam van de account.

      De kolommen voor het geselecteerde bestand of account worden weergegeven.

   1. Op de **[!UICONTROL Account Structure]** geeft u de instellingen voor de accountstructuur op.

   1. (Alleen tekstadvertenties) Klik op de knop **[!UICONTROL Keywords]** en geeft u de trefwoordinstellingen op.

   1. (Alleen tekst en responsieve zoekopdrachten) Klik op de knop **[!UICONTROL Ads]** en voer een van de volgende handelingen uit:

      >[!NOTE]
      >
      >* U kunt maximaal vier variatiesjablonen per standaardtekst en -sjabloon, vijf en variatiesjablonen per uitgebreide/uitgebreide tekst en sjabloon en drie en variatiesjablonen per responsieve zoekopdracht en sjabloon opnemen.
      >* Elke advertentiegroep kan maximaal drie ingeschakelde responsieve zoekadvertenties bevatten.
      >* U kunt bestaande standaardtekst en -variaties niet bewerken en bestaande sjablonen genereren niet langer standaardtekstadvertenties.
      >* Als u een advertentiesjabloon wijzigt, kunnen bestaande advertenties worden verwijderd en kunnen nieuwe advertenties worden gemaakt wanneer u gegevens via de sjabloon verspreidt, [afhankelijk van het advertentietype en het advertentienetwerk](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md).

      * Ga als volgt te werk om een advertentievariatie toe te voegen:

         1. Klikken **[!UICONTROL Add Ad Variation]** om een tekstadvertentie te maken, **[!UICONTROL Add ETA Variation]** om een uitgebreide/uitgebreide tekstadvertentie te maken, of **[!UICONTROL Add RSA Variation]** om een responsieve tekstadvertentie te maken.

            Nadat u het advertentietype hebt opgegeven, kunt u alleen dat advertentietype met de sjabloon maken.

         1. Geef de advertentie-instellingen op.

            Voor responsieve zoekopdrachten kunt u 3-15 kopregels en 2-4 beschrijvingen opnemen.

         1. (Optioneel) Als u alle alternatieve velden wilt voorvullen en kopiëren met tekst uit de oorspronkelijke velden en de kopieervelden, schakelt u het selectievakje naast **[!UICONTROL Prefill]**.

         1. (Optioneel) Als u nog een set toevoegingen aan een advertentie wilt toevoegen, die kan worden gebruikt als een van de regels in het origineel en de kopie de maximumlengte overschrijdt wanneer dynamische parameters tijdens de propagatie worden vervangen door gegevens, klikt u op **[!UICONTROL Add Alternate]** en voeg vervolgens de alternatieve waarden toe.

            >[!NOTE]
            >
            >* Als de [!UICONTROL Prefill] is geselecteerd, worden de alternatieve velden vooraf ingevuld met de oorspronkelijke velden en kunt u deze naar wens bewerken.
            >* Alleen de velden voor het kopiëren van de advertentie die de maximale lengte overschrijden, worden vervangen door de alternatieve waarde. Als bijvoorbeeld alleen een originele kop of titel te lang is, gebruiken de gegenereerde en de variatie de alternatieve kop of titel en de oorspronkelijke beschrijvingen. Zorg er daarom voor dat de alternatieve advertentie-kopie zin heeft wanneer deze wordt gecombineerd met het origineel en de kopie.
            >* Als het origineel en de kopie voldoen aan de lengtevereisten van het zoekprogramma, wordt de alternatieve advertentiekopie verwijderd.
            >* U kunt maximaal vier alternatieven opgeven voor elk veld voor een advertentie-kopie.

         * Ga als volgt te werk om een advertentievariatie te bewerken:

            1. Bewerk de advertentie-instellingen.

               Voor responsieve zoekopdrachten kunt u 3-15 kopregels en 2-4 beschrijvingen opnemen.

            1. (Optioneel) Als u alle alternatieve velden wilt voorvullen en kopiëren met tekst uit de oorspronkelijke velden en de kopieervelden, schakelt u het selectievakje naast **[!UICONTROL Prefill]**.

            1. (Optioneel) Als u nog een set toevoegingen aan een advertentie wilt toevoegen, die kan worden gebruikt als een van de regels in het origineel en de kopie de maximumlengte overschrijdt wanneer dynamische parameters tijdens de propagatie worden vervangen door gegevens, klikt u op **[!UICONTROL Add Alternate]** en voeg vervolgens de alternatieve waarden toe.

               >[!NOTE]
               >
               >* Als de [!UICONTROL Prefill] is geselecteerd, worden de alternatieve velden vooraf ingevuld met de oorspronkelijke velden en kunt u deze naar wens bewerken.
               >* Alleen de velden voor het kopiëren van de advertentie die de maximale lengte overschrijden, worden vervangen door de alternatieve waarde. Als bijvoorbeeld alleen een originele kop of titel te lang is, gebruiken de gegenereerde en de variatie de alternatieve kop of titel en de oorspronkelijke beschrijvingen. Zorg er daarom voor dat de alternatieve advertentie-kopie zin heeft wanneer deze wordt gecombineerd met het origineel en de kopie.
               >* Als het origineel en de kopie voldoen aan de lengtevereisten van het zoekprogramma, wordt de alternatieve advertentiekopie verwijderd.
               >* U kunt maximaal vier alternatieven opgeven voor elk veld voor een advertentie-kopie.

         * Om een advertentievariatie te verwijderen, klik **[!UICONTROL Remove ETA Variation]** (voor uitgebreide/uitgebreide tekstadvertenties) of **[!UICONTROL Remove RSA Variation]** (voor responsieve zoekopdrachten) naast de advertentie, al naar gelang het geval.

   1. (Alleen winkelsjablonen) Klik op de knop **[!UICONTROL Product Groups]** en geeft u vervolgens informatie op over de productgroepen waarvoor u wilt kiezen.

   1. (Optioneel) Klik op de knop **[!UICONTROL Feed Filters]** en geeft u vervolgens op welke rijen in het feed-bestand moeten worden doorgegeven.

   1. (Optioneel) Klik op de knop **[!UICONTROL Label Classifications tab]** en geef vervolgens de classificatiewaarden voor labels op die worden toegewezen aan de verschillende campagnecomponenten die worden gemaakt:

      1. Klik op het selectievakje naast **[!DNL \[Component\] Label Classifications]**.

      1. Ga als volgt te werk voor elke labelclassificatie die aan de component moet worden toegewezen:

         1. Klik op **[!UICONTROL Add Label Classification]**.

         1. Selecteer de labelclassificatie en selecteer vervolgens een bestaande waarde of voer een nieuwe waarde in.

1. Sla de sjabloon op:

   * Als u de sjabloon gewoon wilt opslaan, klikt u op **[!UICONTROL Save]** en klik vervolgens op **[!UICONTROL Save]** opnieuw.

   * Als u de sjabloon wilt opslaan en het opgegeven gegevensbestand wilt doorgeven, klikt u op **[!UICONTROL Save]** en klik vervolgens op **[!UICONTROL Save & Propagate]**.

## De status van voedersjablonen wijzigen

U kunt elke gepauzeerde sjabloon voor gegevensinvoer activeren of een actieve sjabloon voor gegevensinvoer pauzeren.

>[!NOTE]
>
>U kunt gegevens manueel verspreiden door een gepauzeerde malplaatje, maar het gegeven wordt niet automatisch verspreid door het.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, die voor de [!UICONTROL Templates] tab.

1. Schakel het selectievakje in naast elke sjabloon waarvan u de status wilt wijzigen.

1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Change Status]** en klik vervolgens op **[!UICONTROL Activate]** of **[!UICONTROL Pause]**.

## Feed-sjablonen verwijderen

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, die voor de [!UICONTROL Templates] tab.

1. Schakel het selectievakje in naast elke sjabloon die u wilt verwijderen.

1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Delete]**.

1. Klik in het bevestigingsbericht **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [Informatie over het automatiseren en beheren van voorraden](../inventory-feeds-about.md)
>* [Tekst en responsieve zoek- en sjablooninstellingen](template-text-rsa.md)
>* [[!DNL Google Ads] winkelen en sjablooninstellingen](template-google-shopping.md)
>* [[!DNL Microsoft® Advertising] winkelen en sjablooninstellingen](template-microsoft-shopping.md)
>* [Doorvoergegevens doorgeven via sjablonen](../feed-data-propagate.md)
