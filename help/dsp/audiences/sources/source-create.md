---
title: Een doelbron maken om Universal ID-publiek te activeren
description: Leer hoe u een bron kunt maken om een publiek te importeren van uw klantgegevensplatform en deze om te zetten in segmenten met universele id's.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 16a796e02150b00c77c825d7f54c6e390c85214a
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Een doelbron maken om Universal ID-publiek te activeren

*Beta, functie*

Creeer een bron in DSP voor elk eerste-partijpubliek in uw platform van klantengegevens dat u in segmenten wilt omzetten die gespecificeerde universele types van identiteitskaart bevatten. U kunt de segmenten importeren naar de DSP van uw organisatie of naar een advertentieaccount. Gegevenskosten worden toegepast op basis van de geselecteerde Universal ID-typen.

Er zijn aanvullende stappen vereist om het publiek van elk klantgegevensplatform te kunnen innemen. Zie de opmerking aan het einde van de procedure.

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Klik op **[!UICONTROL Add Source]**.

1. In de [!UICONTROL Select a Type] -menu, selecteert u uw klantgegevensplatform:

   * *[!UICONTROL RT-CDP]*: [De [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*: De [[!DNL ActionIQ] klantgegevensplatform](source-about.md).

   * *[!UICONTROL Tealium CDP]*: (Alleen geconfigureerde gebruikers) De [[!DNL Tealium] klantgegevensplatform](source-about.md).

1. Geef de [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* of *[!UICONTROL Account]*.

1. Geef de resterende gegevens op [broninstellingen](source-settings.md).

   Bewaar een kopie van het dialoogvenster [!UICONTROL Source Key] dat wordt gegenereerd. U hebt de waarde later nodig.

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Nadat u een bron voor uw platform van klantengegevens creeert, zult u extra stappen moeten voltooien. Zie de [workflow voor het importeren van soorten publiek uit [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> en de [workflow voor het importeren van soorten publiek uit [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Broninstellingen voor publiek](source-settings.md)
>* [Ongeveer de Bronnen van het Publiek van de Eerste Partij](source-about.md)
>* [Adobe Advertising Cloud DSP-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
