---
title: Een campagne dupliceren
description: Leer hoe u een campagne dupliceert.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 051658d822253e5d0cac56e3d59e99386c68fb71
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Een campagne dupliceren

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Dupliceer een campagne om een nieuwe campagne met vergelijkbare instellingen te maken. U kunt:

* De campagne dupliceren voor de oorspronkelijke adverteerder of voor een andere

* Dupliceer optioneel de originele pakketten en plaatsen

* De vluchtdata van de nieuwe campagne wijzigen

Zie &quot;[ wat niet ](#campaign-not-duplicated)&quot;voor een lijst van plaatsingsmontages gedupliceerd is die niet worden gedupliceerd.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik naast de naam van de campagne op **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** .

1. Geef de nieuwe instellingen voor de campagne op:

   1. Voer de nieuwe naam van de campagne en de eindvluchtdatum in.

   1. (Optioneel) Wijzig de standaardinstellingen.

      De nieuwe campagne wordt standaard toegewezen aan de oorspronkelijke adverteerder, heeft een vliegschema dat op de huidige dag begint en de originele pakketten en plaatsen bevat.

1. Klik op **[!UICONTROL Submit]**.

## Wat is niet gedupliceerd {#campaign-not-duplicated}

Alle instellingen van de originele plaatsingen worden gedupliceerd, behalve:

* Instellingen Experimenteren
* (Als u de vluchtdatums wijzigt) Aangepaste en geplande planning
* (Als u geen advertenties koppelt) Aangepaste weging en planning
* Standaardplaatsingen voor door het programma gegarandeerde deals en plaatsingen voor [!UICONTROL Simple Ad Serving] -deals
* (Als u plaatsingen naar een andere campagne kopieert):
   * Geo-doelen
   * Gebeurtenispixels
   * Adds
   * Placement-level [!DNL DoubleVerify Authentic Brand Safety] segmenten (die de adverteerders-vlakke segmenten met voeten treden)

## Beste praktijken om de Nieuwe Campagne te vormen

>[!TIP]
>
>* De bulksbladen van het gebruik om [ veranderingen in veelvoudige campagnecomponenten in één keer aan te brengen ](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Het gebruik ad markeringsbladen aan [ uploadt veelvoudige derdeadvertenties ](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Onderbreek de nieuwe campagne totdat u deze kunt activeren.

* Overweeg het volgende en bewerk indien nodig de nieuwe campagnemontages:

   * Beschikt de rekening over voldoende middelen om de nieuwe campagnebegroting op te nemen?

   * Heeft de nieuwe campagne een andere begroting nodig dan de vorige campagne?

   * Upload creatieve producten, inclusief eventuele aangepaste wegingen en planningen, en koppel ze aan de plaatsingen.

   * Koppel indien nodig gebeurtenispixels aan de plaatsingen en advertenties.

   * Omvat geografische doelstellingen en plaatsing-niveau [!DNL DoubleVerify Authentic Brand Safety] segmenten zoals nodig aan plaatsingen.

   * Voor programmatic gewaarborgde overeenkomsten, gebruik nieuwe deal IDs en creeer standaardplaatsingen.

   * Maak waar nodig nieuwe plaatsingen voor [!UICONTROL Simple Ad Serving] -deals.

* Voor prestatiecampagnes (d.w.z., campagnes met pakketten die de doelstellingen van de douaneoptimalisering gebruiken), gebruik [[!UICONTROL Linked Package for Optimization Learnings Carryover] het plaatsen ](/help/dsp/campaign-management/packages/package-settings.md) voor elk pakket om de historische gegevens van de vorige campagne als input voor het optimaliseren van het pakket te gebruiken.

>[!MORELIKETHIS]
>
>* [ Ongeveer het Beheer van de Campagne ](campaign-about.md)
>* [ creeer een Campagne ](campaign-create.md)
>* [ geef een Campagne ](campaign-edit.md) uit
>* [ Mening het Logboek van de Verandering voor een Campagne ](campaign-change-log.md)
>* [ Montages van de Campagne ](campaign-settings.md)
