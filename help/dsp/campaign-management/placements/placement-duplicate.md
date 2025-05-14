---
title: Plaatsen dupliceren
description: Leer hoe u een of meer stages dupliceert.
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: 860761bf65dd6ea35abbb3b04863d78c6461fe0f
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# Plaatsen dupliceren

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Dupliceer een of meer plaatsen om plaatsingen met gelijkaardige montages tot stand te brengen. U kunt:

* Meerdere duplicaten van plaatsingen maken
* Dubbele plaatsingen binnen de oorspronkelijke adverteerders en campagnes of binnen verschillende
* (Voor dubbele plaatsen binnen de originele campagnes) Naar keuze dupliceer de originele advertenties
* De status en vluchtdata van de nieuwe plaatsingen wijzigen

Zie &quot;[ wat niet ](#placement-not-duplicated)&quot;voor een lijst van plaatsingsmontages gedupliceerd is die niet worden gedupliceerd.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik op de naam van de campagne.

1. Klik in het submenu op **[!UICONTROL Placements]** .

1. Voer een van de volgende handelingen uit:

   * Als u één plaatsing wilt dupliceren, klikt u op **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** naast de pakketnaam.

   * Meerdere plaatsen dupliceren:

      1. Schakel het selectievakje naast elke plaatsing die u wilt dupliceren in.

      1. Klik op de werkbalk voor bulkacties op **[!UICONTROL Duplicate]** .

1. Geef de nieuwe plaatsingsinstellingen op:

   1. (Enkele plaatsen) Voer de nieuwe plaatsingsnaam in.

   1. Selecteer in het menu **[!UICONTROL Choose Package (Required)]** het bovenliggende pakket of **[!UICONTROL No package]*.

   1. (Optioneel) Wijzig de standaardinstellingen.

   De instellingen zijn van toepassing op alle geselecteerde plaatsingen.

   De nieuwe plaatsingen zijn standaard bedoeld voor het oorspronkelijke advertentietype, worden toegewezen aan de oorspronkelijke adverteerders en campagnes, hebben vluchtschema&#39;s die op de huidige dag beginnen, worden gepauzeerd en bevatten niet de originele advertenties.

   Wanneer u veelvoudige plaatsen creeert, worden de nieuwe plaatsingsnamen toegevoegd met een aantal, in opeenvolging, gebruikend de overeenkomst &lt;*original_placement_name #N*>, zoals &quot;Mijn Plaatsing #2.&quot;

1. Klik op **[!UICONTROL Submit]**.

## Wat is niet gedupliceerd {#placement-not-duplicated}

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

## Beste praktijken om de Nieuwe Plaatsen te vormen

>[!TIP]
>
>* De bulksbladen van het gebruik om [ veranderingen in veelvoudige campagnecomponenten in één keer aan te brengen ](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Het gebruik ad markeringsbladen aan [ uploadt veelvoudige derdeadvertenties ](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Onderbreek de nieuwe plaatsingen tot u bereid bent om hen te activeren.

* Overweeg het volgende en bewerk indien nodig de nieuwe plaatsingen:

   * Beschikt de rekening over voldoende financiële middelen om de nieuwe budgetten voor arbeidsbemiddeling te kunnen gebruiken?

   * Hebben de nieuwe stages andere budgetten nodig dan de vorige? Zijn er minimumbegrotingen nodig?

   * Upload creatieve producten, inclusief eventuele aangepaste wegingen en planningen, en koppel ze aan de plaatsingen.

   * Koppel indien nodig gebeurtenispixels aan de plaatsingen en advertenties.

   * Omvat geografische doelstellingen en plaatsing-niveau [!DNL DoubleVerify Authentic Brand Safety] segmenten zoals nodig aan de plaatsingen.

   * Voor programmatic gewaarborgde overeenkomsten, gebruik nieuwe deal IDs en creeer standaardplaatsingen.

   * Maak waar nodig nieuwe plaatsingen voor [!UICONTROL Simple Ad Serving] -deals.

>[!MORELIKETHIS]
>
>* [ Ongeveer het Beheer van de Plaatsing ](placement-about.md)
>* [ creeer een Plaatsing ](placement-create.md)
>* [ geeft Plaatsen ](placement-edit.md) uit
>* [ Mening het Logboek van de Verandering voor een Plaatsing ](placement-change-log.md)
>* [ Montages van de Plaatsing ](placement-settings.md)
