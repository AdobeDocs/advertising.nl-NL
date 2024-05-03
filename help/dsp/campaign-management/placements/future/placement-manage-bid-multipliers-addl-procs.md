---
title: Bodmultiplicatoren voor plaatsen beheren
description: Meer informatie over het maken en bewerken van biedingsvermenigvuldigers voor opgegeven plaatsingsdoelen.
feature: DSP Placements
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---

# Bodmultiplicatoren voor plaatsen beheren


<!--

See if any of these procedures are implemented; may need to be edited and/or re-worded based on functionality/UI

-->

Met deze functie kun je de biedvermenigvuldigingsfactoren voor je bestaande plaatsingsdoelen wijzigen.

Als u de geselecteerde doelen voor uw plaatsing wilt wijzigen, raadpleegt u &quot;[Plaatsen bewerken](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

## Bodvermenigvuldigers voor een of meer plaatsen beheren

Voor alle geselecteerde plaatsen, kunt u of manueel waarden uitgeven of een spreadsheet met waarden uploaden.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

1. Klik op de naam van de campagne.

1. Klik in het submenu op **[!UICONTROL Placements]**.

1. Schakel het selectievakje in naast elke plaatsing waarvan u de biedvermenigvuldigingsfactoren wilt beheren.

1. Klik op de werkbalk voor bulkacties op **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Pas de bodvermenigvuldigers voor het in aanmerking komende doel handmatig aan of door een CSV-bestand met doelwaarden te uploaden:

   * Als u de waarden voor de bodvermenigvuldiger handmatig wilt aanpassen, gaat u naar elk doelspecifiek tabblad ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], en[!UICONTROL Brand Safety]) en bewerkt u de bestaande waarden voor de plaatsingsdoelen.

   Dezelfde wijzigingen worden aangebracht op alle geselecteerde plaatsen.

   * U kunt als volgt een CSV-bestand met waarden voor de vermenigvuldigingsfactor van het bod uploaden waarmee de bestaande waarden worden overschreven:

     >[!NOTE]
     >
     >Als u een veld leeg laat, worden alle waarden voor dat doeltype verwijderd.<!-- Verify and re-word if needed. I'm not sure if you'll be able to have multiple data rows (one per placement) or if there will be only one data row applicable for all. -->

      1. Klikken **[!UICONTROL CSV Edit]** rechtsboven.

      1. (a) klikken **[!UICONTROL Download Template]** en bewerk de waarden voor de biedvermenigvuldiger of b) bewerk een eerder gedownloade sjabloon. Sla het bewerkte bestand op uw apparaat of netwerk op.

      1. (a) sleep het bewerkte bestand naar het vak of b) klik in het vak om het bestand van uw apparaat of netwerk te selecteren.

   1. Klik op **[!UICONTROL Upload]**.

   Standaard is de biedvermenigvuldiger voor een doel 1,00, wat betekent dat het bod niet voor dat doel is aangepast. Waarden kunnen variëren van 0,10 tot 10,00. Een biedwijziging van 0,5 verlaagt bijvoorbeeld een bod van USD 6 naar USD 3 (0,5 x 6). U kunt een berichtvermenigvuldiger (met andere waarden dan 1,00) instellen voor een [beperkt aantal streefcijfers](#bid-multiplier-limits-by-target).

   Wanneer een veiling in aanmerking komt voor meerdere biedmodifiers, worden alle toepasselijke biedmodifiers vermenigvuldigd.

   Met biedopties wordt het bod nooit hoger dan het maximumbod.

1. Klik op **[!UICONTROL Save]**.

—>

## Upload een spreadsheet om de Bodvermenigvuldigers voor één enkele Plaatsing te beheren<!-- Is this still going to exist independently, or will you just do this via the "Bid Multiplier" option in the main context menu for placements? If both options, then reword headings for distinction -->

Wijzigingen in het geüploade bestand overschrijven de bestaande waarden voor de vermenigvuldigingsfactor voor het bod.<!-- what if you delete a row? -->

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

1. Klik op de naam van de campagne.

1. Klik in het submenu op **[!UICONTROL Placements]**.

1. Klik naast de plaatsingsnaam op  **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. 
   <!-- Verify the rest of these steps. -->

1. (a) klikken **[!UICONTROL Download Template]** en bewerk de waarden voor de biedvermenigvuldiger of b) bewerk een eerder gedownloade sjabloon. Sla het bewerkte bestand op uw apparaat of netwerk op.

   Standaard is de biedvermenigvuldiger voor een doel 1,00, wat betekent dat het bod niet voor dat doel is aangepast. Waarden kunnen variëren van 0,10 tot 10,00. Een biedwijziging van 0,5 verlaagt bijvoorbeeld een bod van USD 6 naar USD 3 (0,5 x 6). U kunt een berichtvermenigvuldiger (met andere waarden dan 1,00) instellen voor een [beperkt aantal streefcijfers](#bid-multiplier-limits-by-target).

   Wanneer een veiling in aanmerking komt voor meerdere biedmodifiers, worden alle toepasselijke biedmodifiers vermenigvuldigd.

   Met biedopties wordt het bod nooit hoger dan het maximumbod.

1. (a) sleep het bewerkte bestand naar het vak of b) klik in het vak om het bestand van uw apparaat of netwerk te selecteren.

1. Klik op **[!UICONTROL Upload]**.

1. Klik op **[!UICONTROL Save]**.

## Doeltypen die in aanmerking komen voor biedvermenigvuldigingsfactoren {#bid-multiplier-by-target}

hier niet gedupeerd

## Maximum aantal biedvermenigvuldigers per doeltype {#bid-multiplier-limits-by-target}

hier niet gedupeerd

<!--

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit Placements](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
 -->
