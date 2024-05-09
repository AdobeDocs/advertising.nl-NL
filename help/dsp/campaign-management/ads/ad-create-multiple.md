---
title: Meerdere externe advertenties maken
description: Leer hoe u meerdere advertenties van derden tegelijk kunt maken.
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Meerdere externe advertenties maken

U kunt maximaal 500 advertenties van derden tegelijk maken door tags te uploaden die verwijzen naar creatieve elementen die worden gehost op externe advertentieservers. U kunt overtrekpixels opnemen voor de advertenties.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

U kunt beide uploaden [!DNL DoubleClick] en [!DNL Flashtalking] met de meegeleverde sjabloon of een handmatig ingevuld bestand.

>[!TIP]
>
> U kunt het beste advertenties van derden gebruiken die veilig via HTTPS worden aangeboden. URL&#39;s die via HTTPS worden aangeboden, beginnen met &quot;https.&quot;

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

1. Klik op de naam van de campagne waarin u de advertentie wilt opnemen.

1. Klik boven de gegevenstabel op **[!UICONTROL Create]**. Klik in het gedeelte Typen toevoegen van het menu op **[!UICONTROL Bulk upload ads]**.

1. Selecteer de advertentieserver waarop de advertentie wordt gehost: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]*, of *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] en [!DNL Flashtalking] advertenties) Selecteer het type code dat u voor elk video-element en elk weergaveelement wilt gebruiken. De beschikbare opties variëren per advertentieserver.

1. (Toevoegen op alle advertentieservers behalve [!DNL DoubleClick] en [!DNL Flashtalking]) Klik **[!UICONTROL Download this template]** om een sjabloon te downloaden in [!DNL Microsoft Excel] spreadsheetindeling (XLSX), die u kunt vullen met advertentiegegevens en lokaal kunt opslaan. De vereiste kolommen bevatten [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag], en [!UICONTROL Ad Types].

1. Klikken **[!UICONTROL Upload]** en selecteer een bestand in de indeling .xlsx of .xls van uw apparaat of netwerk.

   Voor [!DNL DoubleClick] en [!DNL Flashtalking] adverteert, uploadt u onbewerkte tagbladen van de advertentieserver. Voor andere advertentieservers, gebruik het malplaatje u in Stap 3 downloadde.

1. Klik op **[!UICONTROL Start Building Ads]**.

1. Bekijk de details en status van elke advertentie:

   1. (Universeel video-advertenties gebruiken [!DNL Google] of [!DNL Flashtalking] tags) Klik op de knop **[!UICONTROL Ad Type]** veld en selecteer **[!UICONTROL Universal Video]**.

   1. (Universal Video Adads) Voor elke nieuwe advertentie klikt u op ![bewerken](/help/dsp/assets/edit.png), selecteert u de [toepasselijke video-indeling](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)en klik vervolgens op **Opslaan**.

   1. Controleer de status van elke advertentie, die is gebaseerd op validatiecontroles van de geüploade tag.

   1. (Optioneel) Voer een van de volgende handelingen uit voor elke advertentie:

      * Als u een voorvertoning van een advertentie wilt weergeven, klikt u op ![play](/help/dsp/assets/play.png) in de advertentierij.

      * Klik op ![bewerken](/help/dsp/assets/edit.png), bewerkt u de details en klikt u op **Opslaan**.

      * Als u een advertentie wilt verwijderen, klikt u op **[!UICONTROL X]** in de advertentierij.

1. Klikken **[!UICONTROL Create *N *Advertentie(s)]**.

1. Voer een van de volgende handelingen uit:

   * Klik op **[!UICONTROL Done]**.

   * (Als een advertentie wordt afgewezen; optioneel) Als u de advertentierecord wilt bewerken en de advertentie opnieuw ter controle wilt verzenden:

      1. Klik op de advertentienaam.

      1. Bewerk de advertentie-instellingen.

      1. Klik op **[!UICONTROL Save & submit for review]**.

>[!NOTE]
>
>Universele video-advertenties kunnen alleen worden gekoppeld aan universele video-opnamen.

>[!MORELIKETHIS]
>
>* [Over Advertentiebeheer](ad-about.md)
>* [Ad-specificaties](ad-specs.md)
>* [Eén advertentie maken](ad-create.md)
>* [Video: hoe te om te bulken uploadt de Markeringen van de Advertentie van derden](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)
>* [Veelgestelde vragen over Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
