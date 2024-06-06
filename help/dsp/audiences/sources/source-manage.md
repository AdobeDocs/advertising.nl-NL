---
title: Bronnen voor publiek maken en beheren om universeel ID-publiek te activeren
description: Leer hoe u een bron kunt maken en beheren om een publiek van uw klantgegevensplatform te importeren en deze om te zetten in segmenten met universele id's.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---

# Een doelbron maken om Universal ID-publiek te activeren

*Beta, functie*

Creeer een bron in DSP voor elk eerste-partijpubliek in uw platform van klantengegevens dat u in segmenten wilt omzetten die gespecificeerde universele types van identiteitskaart bevatten. U kunt de segmenten importeren naar de DSP van uw organisatie of naar een advertentieaccount. Gegevenskosten worden toegepast op basis van de geselecteerde Universal ID-typen.

Er zijn aanvullende stappen vereist om het publiek van elk klantgegevensplatform te kunnen innemen. Zie de opmerking aan het einde van de procedure.

## Een doelbron maken

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

## Wijzig de types van identiteitskaart voor een Bron van het Publiek

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Plaats de cursor op de bronrij en klik op **[!UICONTROL Edit]**.

1. Wijzig de [Id&#39;s geselecteerd voor de bron](source-settings.md).

1. Klik op **[!UICONTROL Save]**.

## Een doelbron verwijderen

Als u een bron verwijdert, verwijdert u de segmenten die door de bron zijn vertaald.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Plaats de cursor op de bronrij en klik op **[!UICONTROL Delete]**.

1. Klik in het bevestigingsbericht **[!UICONTROL Delete]**.

## Bekijk het Logboek van de Verandering voor een Bron van het Publiek

U kunt details over veranderingen in een verslag van de publieksbron bekijken en naar keuze nota&#39;s aan het logboek vastmaken.

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Plaats de cursor op de bronrij en klik op **[!UICONTROL Change log]**.

1. (Optioneel) Een notitie toevoegen aan het wijzigingslogboek:

   1. Plaats de cursor op de bronrij en klik op **[!UICONTROL Add Notes]**.

   1. Voer de notitie in en klik op **[!UICONTROL Save]**.

      De maximumlengte is 256 tekens.

1. (Optioneel) Als u het logbestand in een groter detailscherm wilt openen, houdt u de cursor boven de bronrij en klikt u op **[!UICONTROL View Details]**.

>[!MORELIKETHIS]
>
>* [Broninstellingen voor publiek](source-settings.md)
>* [Ongeveer de Bronnen van het Publiek van de Eerste Partij](source-about.md)
>* [Adobe Advertising Cloud DSP-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
