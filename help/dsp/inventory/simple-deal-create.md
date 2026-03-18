---
title: Een [!UICONTROL Simple Ad Serving] -deal maken
description: Leer hoe u een tekstspatiëringspixel maakt voor een [!UICONTROL Simple Ad Serving] -deal.
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 4264d6032a8d31004e66fd4ee033d9ecd51918c8
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Een [!UICONTROL Simple Ad Serving] -deal maken

1. Klik in het hoofdmenu op **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Klik boven de datatabel op **[!UICONTROL Create]** en selecteer vervolgens **[!UICONTROL Simple Ad Serving]** .

1. Ga de [ overeenkomstenmontages ](simple-deal-settings.md) in:

   1. Geef in de sectie [!UICONTROL Select Ad Source] informatie op over de uitgever, de adverteerder en de campagne, en het type advertentie. Klik vervolgens op **[!UICONTROL Next]** .

   1. Geef in de sectie [!UICONTROL Select Ad(s)] een advertentie op die u als proxy wilt gebruiken in DSP:

      1. Voer een van de volgende handelingen uit:

         * Selecteer voor bestaande advertenties de advertenties die u wilt gebruiken.

         * Voor nieuwe advertenties, creeer een volmacht [ derde advertentie ](/help/dsp/campaign-management/ads/ad-create-multiple.md).

      >[!NOTE]
      > DSP heeft geen advertenties die u opgeeft. De uitgever dient de advertentie.

      1. Klik op **[!UICONTROL Next]**.

   1. Bewerk in Details feed de gegevens van de feed en klik op **[!UICONTROL Next]** .

      DSP produceert automatisch een plaatsing, genoemd &quot;SAS Plaatsing - &lt;*overeenkomstennaam*>,&quot;voor de advertentie. In de plaatsing, wordt de overeenkomst automatisch gericht in de [!UICONTROL Inventory Targets] sectie. Alle andere doelopties zijn niet van toepassing.

1. Verzend de pixels voor het bijhouden van gebeurtenissen naar de uitgever voor implementatie op een van de volgende manieren:

   * (Optioneel) Verzend vanuit het scherm [!UICONTROL Activate Tag with Publisher] de tag deal naar de uitgever.

     Wanneer u de vorige stappen hebt uitgevoerd, genereert DSP een e-mailbericht dat u naar de uitgever kunt verzenden. Het bericht omvat de overeenkomstendetails, een verbinding waarvan om de overeenkomstenmarkering terug te winnen, en een vergunningscode voor de verbinding.

      1. Herzie de overeenkomstendetails, en doe dan één van beiden van het volgende:

         * Als u de gegevens in een e-mailbericht in een e-mailtoepassing op uw apparaat wilt plakken, klikt u op **[!UICONTROL Email & Done]** en selecteert u de e-mailtoepassing. Het veld [!UICONTROL CC:] wordt vooraf gevuld met een [!DNL Adobe] -ondersteuningsadres. U kunt het bericht dan naar het aangewezen contact voor de uitgever verzenden.

         * Klik op **[!UICONTROL Copy Email]om de gegevens naar het klembord te kopiëren.** U kunt de inhoud vervolgens handmatig in een e-mailbericht plakken en naar de juiste contactpersoon voor de uitgever verzenden. U moet een kopie (CC:) naar `publisher-support-global@adobe.com` opnemen. Klik op **[!UICONTROL Email & Done]** wanneer u het bericht hebt gekopieerd.

      1. (Indien nodig) Neem contact op met de uitgever om te controleren of de tag de juiste macro&#39;s bevat, zodat de tag met de advertentieserver van de uitgever werkt kan worden.

   * (Optioneel) Stuur de pixels voor het bijhouden van gebeurtenissen handmatig naar de uitgever:

      1. In de overeenkomstenrij binnen de [!UICONTROL Deals] mening, klik ![ het menu van Opties ](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         De gebeurtenispixels omvatten een [!UICONTROL Clickthrough] pixel en een [!UICONTROL Impression] pixel. Video- en audioadvertenties bevatten ook gebeurtenispixels op kwartaalbasis voltooid (van [!UICONTROL 25% Complete] tot [!UICONTROL 100% Complete] ).

      1. Kopieer de pixels voor het bijhouden van gebeurtenissen en geef deze door aan uw uitgever.

>[!MORELIKETHIS]
>
>* [ Over [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] Instellingen ](simple-deal-settings.md)
>* [ Mening een Gedetailleerd Rapport voor een Overeenkomst ](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
