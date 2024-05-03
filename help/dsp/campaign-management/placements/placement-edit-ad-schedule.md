---
title: Advertentieschema's voor plaatsingen bewerken
description: Leer hoe u de advertentieschema's voor de advertenties wijzigt die bij plaatsingen horen.
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Advertentieschema&#39;s voor plaatsingen bewerken

## Advertentieschema&#39;s voor een of meer plaatsen bewerken

U kunt de geplande vliegdatums en de ad-rotatie wijzigen voor advertenties die zijn gekoppeld aan meerdere plaatsen met behulp van een [!DNL Microsoft Excel] spreadsheet. Elke advertentie kan actief zijn tijdens meerdere vluchten.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

1. Klik op de naam van de campagne.

1. Klik in het submenu op **[!UICONTROL Placements]**.

1. Schakel het selectievakje in naast elke plaatsing waarvan u de advertentiegegevens wilt downloaden.

1. Klik op de werkbalk voor bulkacties op **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. Klik op **[!UICONTROL Download]** in het bericht boven aan de browserpagina om een werkbladbestand (in XLSX-indeling) te downloaden volgens de normale procedure van uw browser.

   ![Klaar-melding downloaden](/help/dsp/assets/download-ready.png "Klaar-melding downloaden")

1. Open het gedownloade bestand, bewerk de vluchtinformatievelden voor elke advertentierij die u in de vlucht wilt opnemen en sla het bijgewerkte bestand op:

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** (zoals [!UICONTROL Flight 1 Start Date] en [!UICONTROL Flight 1 End Date]): De eerste en laatste vluchtdata. Gebruik de notatie YYYY-MM-DD voor elke datum. Alle advertenties met lege vliegdatumvelden worden behandeld als niet-deelnemende advertenties.

   * **[!UICONTROL Flight N Weight]** (zoals [!UICONTROL Flight 1 Weight]): Hoe draait u de advertenties voor een vlucht. Voer een waarde in:

      * Als u de advertenties voor een vlucht gelijkmatig wilt roteren, voert u `[!UICONTROL Even]`.

      * Als u de advertenties voor een vlucht ongelijk wilt roteren, voert u het relatieve gewicht in waarmee u elke advertentie wilt roteren, als een percentage (bijvoorbeeld `40` voor 40%). Het totale gewicht van de vlucht moet gelijk zijn aan 100.

1. Upload de bewerkte sjabloon voor advertentieschema:

   1. Schakel het selectievakje naast elke toepasselijke plaatsing in.

   1. Klik op de werkbalk voor bulkacties op **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]** en geeft u het bestand op dat u wilt uploaden.

## Het advertentieschema voor één plaatsing bewerken

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

U kunt de geplande vliegdatums en de ad-rotatie wijzigen voor de advertenties die aan een plaatsing zijn gekoppeld. Elke advertentie kan actief zijn tijdens meerdere vluchten.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

1. Klik op de naam van de campagne.

1. Klik in het submenu op **[!UICONTROL Placements]**.

1. Klik naast de plaatsingsnaam op  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

1. Voer een van de volgende handelingen uit:

   * Om een vlucht toe te voegen, klik **[!UICONTROL Add Flight]** en geeft u vervolgens de begin- en einddatum op.

   * Als u een bestaande vlucht wilt toevoegen aan een advertentie, klikt u op **[!UICONTROL +]** in de rij ad voor de vluchtkolom.

   * Als u een bestaande vlucht uit een advertentie wilt verwijderen, klikt u op **[!UICONTROL x]** in de rij ad voor de vluchtkolom.

      * (Als meerdere advertenties dezelfde vlucht hebben) Als u de advertenties ongelijk wilt roteren, klikt u op **[!UICONTROL Even Rotation]** in de vluchtinformatie, en voert vervolgens het relatieve gewicht in waarmee elke advertentie moet worden geroteerd, als percentage.

        Het totale gewicht moet 100 zijn.

1. Klik rechtsboven op **[!UICONTROL Continue]**.

1. Bekijk de vlieggegevens en klik vervolgens op **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Info over Plaatsingsbeheer](placement-about.md)
>* [Plaatsen bewerken](placement-edit.md)
>* [Het Wijzigingslogboek voor een plaatsing weergeven](placement-change-log.md)
>* [Plaatsingsinstellingen](placement-settings.md)
