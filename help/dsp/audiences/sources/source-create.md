---
title: Creeer een Bron van het Publiek om Eerste Publiek te activeren
description: Leer hoe u een bron kunt maken voor het importeren van soorten publiek naar uw account of een adverteerderaccount.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---

# Creeer een Bron van het Publiek om Eerste Publiek te activeren

<!-- Will this remain for admin users/Adobe Account Team users only? -->

Maak een bron in DSP om gebruikers van de eerste partij naar uw DSP of een adverteerderaccount te importeren.

Voor extra die stappen worden vereist om segmenten van specifieke platforms van klantgegevens in te voeren, zie [de publiekspecifieke activeringsworkflows](source-about.md)

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Klik op **[!UICONTROL Add Source]**.

1. In de [!UICONTROL Select a Type] selecteert u het type bron.

   * *[!UICONTROL RT-CDP]*: [De [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   <!-- * *[!UICONTROL ActionIQ]*: The [[!DNL ActionIQ] customer data platform](source-about.md). -->

   * *[!UICONTROL Tealium CDP]*: De [[!DNL Tealium] klantgegevensplatform](source-about.md).

1. Geef de [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* of *[!UICONTROL Account]*.

1. Geef de resterende gegevens op [broninstellingen](source-settings.md).

   Bewaar een kopie van het dialoogvenster [!UICONTROL Source Key] dat wordt gegenereerd. U hebt de waarde later nodig.

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Nadat u een bron voor uw platform van klantengegevens creeert, moet u extra stappen voltooien. Zie de [activeringsworkflow voor [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> en de [activeringsworkflow voor [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Broninstellingen voor publiek](source-settings.md)
>* [Ongeveer het Activeren van Authenticated Segmenten van de Bronnen van het Publiek](source-about.md)
>* [Activeer Erkende Segmenten van de Universele Partners van identiteitskaart](source-universal-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
