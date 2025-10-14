---
title: Advertentieschema's voor plaatsingen bewerken
description: Leer hoe u de advertentieschema's voor de advertenties wijzigt die bij plaatsingen horen.
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: 18c68edec80a80d236df138c05fba8d857c9ed9e
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Advertentieschema&#39;s voor plaatsingen bewerken

## Advertentieschema&#39;s voor een of meer plaatsen bewerken

U kunt de geplande vliegdatums en de ad-rotatie wijzigen voor advertenties die aan meerdere plaatsen zijn gekoppeld met behulp van een [!DNL Microsoft Excel] -spreadsheet. Elke advertentie kan actief zijn tijdens meerdere vluchten.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik op de naam van de campagne.

1. Klik in het submenu op **[!UICONTROL Placements]** .

1. Schakel het selectievakje in naast elke plaatsing waarvan u de advertentiegegevens wilt downloaden.

1. Klik op de werkbalk voor bulkacties op **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]** .

1. Wanneer het bestand beschikbaar is, klikt u op **[!UICONTROL Download]** in het bericht boven aan de browserpagina om een werkbladbestand (in XLSX-indeling) te downloaden volgens de normale procedure van uw browser.

   ![&#x200B; Klaar bericht van de Download &#x200B;](/help/dsp/assets/download-ready.png " Download Klaar bericht ")

1. Open het gedownloade bestand, bewerk de vluchtinformatievelden voor elke advertentierij die u in de vlucht wilt opnemen en sla het bijgewerkte bestand op:

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** (zoals [!UICONTROL Flight 1 Start Date] en [!UICONTROL Flight 1 End Date] ): de eerste en laatste datums van de vlucht. Gebruik de notatie YYYY-MM-DD voor elke datum. Alle advertenties met lege vliegdatumvelden worden behandeld als niet-deelnemende advertenties.

   * **[!UICONTROL Flight N Weight]** (zoals [!UICONTROL Flight 1 Weight] ): De advertenties voor een vlucht roteren. Voer een waarde in:

      * Voer `[!UICONTROL Even]` in als u de advertenties voor een vlucht gelijkmatig wilt roteren.

      * Als u de advertenties voor een vlucht ongelijk wilt roteren, voert u het relatieve gewicht in waarmee u elke advertentie wilt roteren, als een percentage (bijvoorbeeld `40` voor 40%). Het totale gewicht van de vlucht moet gelijk zijn aan 100.

1. Upload de bewerkte sjabloon voor advertentieschema:

   1. Schakel het selectievakje naast elke toepasselijke plaatsing in.

   1. Klik op de werkbalk voor bulkacties op **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]** en geef op welk bestand u wilt uploaden.

## Het advertentieschema voor één plaatsing bewerken

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

U kunt de geplande vliegdatums en de ad-rotatie wijzigen voor de advertenties die aan een plaatsing zijn gekoppeld. Elke advertentie kan actief zijn tijdens meerdere vluchten.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik op de naam van de campagne.

1. Klik in het submenu op **[!UICONTROL Placements]** .

1. Klik naast de plaatsingsnaam op **[!UICONTROL ...]** > **[!UICONTROL Ads]** > **[!UICONTROL Ad schedule]** .

1. Voer een van de volgende handelingen uit:

   * Als u een vlucht wilt toevoegen, klikt u op **[!UICONTROL Add Flight]** en geeft u vervolgens de begin- en einddatum op.

   * Als u een bestaande vlucht aan een advertentie wilt toevoegen, klikt u op **[!UICONTROL +]** in de rij met toevoegingen voor de vluchtkolom.

   * Als u een bestaande vlucht uit een advertentie wilt verwijderen, klikt u op **[!UICONTROL x]** in de rij met toevoegingen voor de vluchtkolom.

      * (Als meerdere advertenties dezelfde vlucht hebben) Als u de advertenties ongelijk wilt roteren, klikt u op **[!UICONTROL Even Rotation]** in de vluchtinformatie en voert u vervolgens het relatieve gewicht in waarmee u elke advertentie wilt roteren, als een percentage.

        Het totale gewicht moet 100 zijn.

1. Klik in de rechterbovenhoek op **[!UICONTROL Continue]** .

1. Controleer de vlieggegevens en klik op **[!UICONTROL Save & Finish]** .

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer het Beheer van de Plaatsing &#x200B;](placement-about.md)
>* [&#x200B; geeft Plaatsen &#x200B;](placement-edit.md) uit
>* [&#x200B; Mening het Logboek van de Verandering voor een Plaatsing &#x200B;](placement-change-log.md)
>* [&#x200B; Montages van de Plaatsing &#x200B;](placement-settings.md)
