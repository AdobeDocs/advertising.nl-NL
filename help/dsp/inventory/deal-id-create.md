---
title: Handmatig id-details maken
description: Leer hoe te om details voor een overeenkomstenidentiteitskaart manueel in te gaan.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: a5be425ee34960cf58642cb850ae817998652f53
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Handmatig id-details maken

1. Klik in het hoofdmenu op **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Klik boven de datatabel op **[!UICONTROL Create]** en selecteer vervolgens **[!UICONTROL Deal ID]** .

1. Ga de [&#x200B; overeenkomstenmontages &#x200B;](deal-id-settings.md) in:

   1. In de [!UICONTROL Deal ID basics] sectie, specificeer de overeenkomstendetails en de adverteerders die tot de overeenkomst kunnen toegang hebben. Voor gegarandeerde deals moet u ook de geplande vluchtdata en het geschatte aantal indrukken specificeren, alleen voor traceringsdoeleinden.

      U kunt het afvangen van gewaarborgde overeenkomsten volgen door de &quot;Pacing van de Impressie Pacing&quot;uitgavenkolom van PG in de Inventaris > de mening van Overeenkomsten te omvatten.

   1. (Alleen gebruikers van beheerders; optioneel) Bewerk in de sectie [!UICONTROL Technical] de standaardinstellingen.

   1. Klik op **[!UICONTROL Save]**.

1. (Gegarandeerde overeenkomsten slechts) selecteer de advertenties voor de overeenkomst (of 1x1 pixel voor uitgever-beheerde advertenties) te gebruiken en creeer een standaard programmatic gewaarborgde plaatsing (PG).

   De standaardPG plaatsingen zorgen ervoor dat uw overeenkomst altijd een bod voor elke biedingsverzoek terugkeert. Als u geen standaardplaatsing van PG creeert, dan om het even welke plaatsen die de overeenkomst richten plaatsen geen biedingen tenzij zij opstelling correct zijn. U moet altijd een standaard-PG-plaatsing maken. In de [!UICONTROL Placements] mening, hebben de gebrek PG plaatsingen een [!UICONTROL Sub-type] kolomwaarde van &quot; [!UICONTROL PG Default]&quot;.

   U kunt naar keuze de overeenkomst als inventarisdoel in extra plaatsingen gebruiken maar moet hen opstelling correct om biedingen te plaatsen.

   1. In de [!UICONTROL Ad & Campaign Selection] montages, selecteer de advertenties voor de overeenkomst te gebruiken:

      1. Selecteer de adverteerder, de campagne en het type advertentie. Selecteer desgewenst een advertentiestatus waarmee de advertenties moeten worden gefilterd.

      1. Van de lijst van beschikbare advertenties, selecteer de controledoos naast elke advertentie om voor de overeenkomst te gebruiken.

         Voor elke door de uitgever beheerde advertentie wordt automatisch een pixel voor het bijhouden van de 1x1-beelden toegepast nadat een adverteerder en campagne zijn geselecteerd.

      1. Klik op **[!UICONTROL Apply]**.

   1. In het scherm met plaatsingsinstellingen:

      1. Voer de plaatsingsnaam in.

      1. (Facultatief) geef de [&#x200B; plaatsingsmontages &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md) uit, met inbegrip van het beschrijven van het standaardbod, dat automatisch met de waarde van CPM van de overeenkomst wordt bevolkt; het veranderen van de datumwaaier; of het vastmaken van meer advertenties.

      De overeenkomst wordt automatisch gericht in de sectie van de Streefcijfers van de Inventaris. Alle andere doelopties zijn niet van toepassing.

      1. Klik op **[!UICONTROL Create placement]**.

Nadat u de overeenkomst creeert, kunt u de overeenkomst als inventarisdoel voor veelvoudige plaatsen gebruiken.

>[!NOTE]
>
> U te hoeven niet om de overeenkomstenmarkering naar de uitgever voor controle te verzenden.

>[!TIP]
>
>* In de [!UICONTROL Inventory] > [!UICONTROL Deals] mening, toont de [!UICONTROL Pacing & Budget] kolom hoe de overeenkomst aan de gespecificeerde vluchtdatum en imperiatiedoel past.
>
>* Als de levering onderaan of overpakking is, contacteer uw uitgever om aan te passen hoeveel volume het door de overeenkomst verzendt.

>[!MORELIKETHIS]
>
>* [&#x200B; Hand de montages van overeenkomstidentiteitskaart &#x200B;](deal-id-settings.md)
>* [&#x200B; opstelling een programmatic gewaarborgde overeenkomst &#x200B;](programmatic-guaranteed-set-up.md)
>* [&#x200B; voorlegt een advertentie voor een programmatic gewaarborgde overeenkomst met  [!DNL FreeWheel]](freewheel-submit.md)
>* [&#x200B; Ongeveer programmatic gewaarborgde overeenkomsten &#x200B;](programmatic-guaranteed-about.md)
<!-- >* [Specify placements and ads for a private deal](deal-id-attach-placements.md)-->
