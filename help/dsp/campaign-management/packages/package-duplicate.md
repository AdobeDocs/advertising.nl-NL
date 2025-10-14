---
title: Een pakket dupliceren
description: Leer hoe u een pakket dupliceert.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 860761bf65dd6ea35abbb3b04863d78c6461fe0f
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Een pakket dupliceren

Dupliceer een pakket om een pakket met gelijkaardige montages tot stand te brengen. U kunt:

* Het pakket dupliceren binnen de oorspronkelijke adverteerder en campagne of binnen verschillende

* U kunt desgewenst de plaatsen in het pakket dupliceren

* (Voor gedupliceerde pakketten in de oorspronkelijke campagnes) Dupliceer optioneel de oorspronkelijke advertenties en de gebeurtenispixels op plaatsingsniveau

* De vluchtdatums van het nieuwe pakket wijzigen

Zie &quot;[&#x200B; wat niet &#x200B;](#package-not-duplicated)&quot;voor een lijst van plaatsingsmontages gedupliceerd is die niet worden gedupliceerd.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik op de naam van de campagne om de weergave [!UICONTROL Packages] te openen.

1. Klik naast de pakketnaam op **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** .

1. Geef de nieuwe pakketinstellingen op:

   1. Voer de nieuwe pakketnaam in.

   1. (Optioneel) Wijzig de standaardinstellingen.

      Standaard:

      * Het nieuwe pakket wordt toegewezen aan de oorspronkelijke adverteerder en campagne.

      * Het nieuwe pakket wordt actief op de huidige dag.<!-- and the flight continues for NN  days. -->

      * Plaatsen in het originele pakket worden gekopieerd naar het nieuwe pakket.

      * De advertenties en de gebeurtenispixels op plaatsingsniveau worden niet naar het nieuwe pakket gekopieerd.

1. Klik op **[!UICONTROL Submit]**.

## Wat is niet gedupliceerd {#package-not-duplicated}

Alle instellingen van de originele plaatsingen worden gedupliceerd, behalve:

* Instellingen Experimenteren
* Minimumbegrotingen op plaatsingsniveau
* (Als u de vluchtdatums wijzigt) Aangepaste en geplande planning
* (Als u geen advertenties koppelt) Aangepaste weging en planning
* Standaardplaatsingen voor door het programma gegarandeerde deals en plaatsingen voor [!UICONTROL Simple Ad Serving] -deals
* (Als u plaatsingen naar een andere campagne kopieert):
   * Geo-doelen
   * Gebeurtenispixels
   * Adds
   * Placement-level [!DNL DoubleVerify Authentic Brand Safety] segmenten (die de adverteerders-vlakke segmenten met voeten treden)

## Beste praktijken om het Nieuwe Pakket te vormen

>[!TIP]
>
>* De bulksbladen van het gebruik om [&#x200B; veranderingen in veelvoudige campagnecomponenten in één keer aan te brengen &#x200B;](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Het gebruik ad markeringsbladen aan [&#x200B; uploadt veelvoudige derdeadvertenties &#x200B;](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Onderbreek het nieuwe pakket totdat u het kunt activeren.

* Overweeg het volgende en bewerk het nieuwe pakket indien nodig:

   * Beschikt de rekening over voldoende financiële middelen om het nieuwe budget te dekken?

   * Heeft het nieuwe pakket een andere begroting nodig dan het vorige pakket?

   * Zijn er minimumbudgetten nodig voor een van de stages?

   * Upload creatieve producten, inclusief eventuele aangepaste wegingen en planningen, en koppel ze aan de plaatsingen.

   * Koppel indien nodig gebeurtenispixels aan de plaatsingen en advertenties.

   * Omvat geografische doelstellingen en plaatsing-niveau [!DNL DoubleVerify Authentic Brand Safety] segmenten zoals nodig aan plaatsingen.

   * Voor programmatic gewaarborgde overeenkomsten, gebruik nieuwe deal IDs en creeer standaardplaatsingen.

   * Maak waar nodig nieuwe plaatsingen voor [!UICONTROL Simple Ad Serving] -deals.

* Voor pakketten die aangepaste optimalisatiedoelstellingen gebruiken, gebruik [[!UICONTROL Linked Package for Optimization Learnings Carryover] plaatsend &#x200B;](/help/dsp/campaign-management/packages/package-settings.md) voor elk pakket om de historische gegevens van de vorige campagne als input voor het optimaliseren van het pakket te gebruiken.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer het Beheer van het Pakket &#x200B;](package-about.md)
>* [&#x200B; creeer een Pakket &#x200B;](package-create.md)
>* [&#x200B; geef een Pakket &#x200B;](package-edit.md) uit
>* [&#x200B; Mening het Logboek van de Verandering voor een Pakket &#x200B;](package-change-log.md)
>* [&#x200B; de Montages van het Pakket &#x200B;](package-settings.md)
