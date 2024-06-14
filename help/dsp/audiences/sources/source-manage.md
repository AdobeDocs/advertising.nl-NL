---
title: Bronnen voor publiek beheren om Universal ID-publiek te activeren
description: Leer hoe u een bron kunt maken en beheren om een publiek van uw klantgegevensplatform te importeren en deze om te zetten in segmenten met universele id's.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 02ed538a48a4ba0323f9b75938ee6b007c6e0fd7
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 0%

---

# Bronnen voor publiek beheren om Universal ID-publiek te activeren

*Beta, functie*

Creeer een bron in DSP voor elk eerste-partijpubliek in uw platform van klantengegevens dat u in segmenten wilt omzetten die gespecificeerde universele types van identiteitskaart bevatten. U kunt de segmenten importeren naar de DSP van uw organisatie of naar een advertentieaccount. Gegevenskosten worden toegepast op basis van de geselecteerde Universal ID-typen. Zodra u een bron creeert, worden de extra stappen vereist om het publiek van elk platform van klantengegevens in te voeren. Zie de nota aan het eind van de procedure om een bron tot stand te brengen.

U kunt de Universal ID-typen wijzigen waarnaar het bronpubliek wordt vertaald, en een logboek met de wijzigingen weergeven.

U kunt ook een bron verwijderen.

## Een doelbron maken

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Klik op **[!UICONTROL Add Source]**.

1. In de [!UICONTROL Select a Type] selecteert u uw [klantgegevensplatform](source-about.md):

   * *[!UICONTROL RT-CDP]*: De [!DNL Adobe Real-Time Customer Data Platform].

   * *[!UICONTROL ActionIQ]*: De [!DNL ActionIQ] klantgegevensplatform.

   * *[!UICONTROL Amperity]*: De [!DNL Amperity] klantgegevensplatform.

   * *[!UICONTROL Optimizely]*: De [!DNL Optimizely] klantgegevensplatform.

   * *[!UICONTROL Tealium CDP]*: (Alleen geconfigureerde gebruikers) De [!DNL Tealium] klantgegevensplatform.

1. Geef de [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* of *[!UICONTROL Account]*.

1. Geef de resterende gegevens op [broninstellingen](#source-settings).

   Bewaar een kopie van het dialoogvenster [!UICONTROL Source Key] dat wordt gegenereerd. U hebt de waarde later nodig.

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Nadat u een bron voor uw platform van klantengegevens creeert, zult u extra stappen moeten voltooien om uw publiek in te voeren. Zie de [workflow voor [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md),<!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), --> de [workflow voor [!DNL Amperity]](source-amperity.md)de [workflow voor [!DNL Optimizely]](source-optimizely.md)en de [workflow voor [!DNL Tealium]](source-tealium.md).

## Wijzig de types van identiteitskaart voor een Bron van het Publiek

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Plaats de cursor op de bronrij en klik op **[!UICONTROL Edit]**.

1. Wijzig de [Id&#39;s geselecteerd voor de bron](#source-settings).

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

## Broninstellingen voor publiek {#source-settings}

**[!UICONTROL Data Visibility Level]:** Of de segmenten beschikbaar zijn voor één adverteerder met toegang tot de account (*[!UICONTROL Advertiser]*) of aan alle adverteerders die toegang hebben tot de account *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Alleen de zichtbaarheid op advertentieniveau) De adverteerder voor wie de segmenten beschikbaar zijn. Selecteer een optie in de lijst met adverteerders die toegang hebben tot het account.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] alleen bronnen) De Adobe Experience Cloud-organisatie-id voor de [!DNL Adobe Experience Platform] account.

**[!UICONTROL Convert PII to the following IDs]:** De id-typen waarnaar u uw persoonlijk identificeerbare gegevens (PII) converteert. Als u meerdere typen selecteert, wordt het gegenereerde segment gevuld met waarden voor elk geselecteerd id-type (zoals een [!DNL RampID] en [!DNL Unified ID2.0] voor elk e-mailadres). Gegevensheffingen worden dienovereenkomstig toegepast.

Voor [!DNL RampID] en [!DNL Unified ID2.0], zoekt de leverancier elk e-mailadres op om te zien of er al een id bestaat en zet het adres om in een overeenkomstige id, indien beschikbaar. Als er geen id voor het adres bestaat, wordt er een nieuwe id gemaakt.

>[!NOTE]
>
>U kunt slechts één type id in één plaatsing als doel instellen. Prestaties testen op ID-type [een aparte plaatsing maken](/help/dsp/campaign-management/placements/placement-create.md) voor elk type ID in het segment.

* *[!DNL RampID]:* PII omzetten in een [!DNL RampID]. U kunt [!DNL RampIDs] voor het opnieuw richten van login gebruikers en voor [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) meting.

* *[!DNL Unified ID2.0](Beta):* PII omzetten in een [Unified ID 2.0](https://unifiedid.com) ID voor het opnieuw richten van login gebruikers.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** De serviceovereenkomst voor de conversie van PII naar universele id&#39;s. U of een andere gebruiker in de DSP account moet de voorwaarden één keer accepteren voordat u gegevens kunt converteren naar een nieuw id-type. Voor klanten met beheerde de dienstcontracten, zal uw Team van de Rekening van de Adobe uw toestemming krijgen en zal de termijnen namens uw organisatie goedkeuren. Als u de voorwaarden wilt lezen, klikt u op **>**. Als u de voorwaarden wilt accepteren, schuift u naar de onderkant van de voorwaarden en klikt u op **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Alleen-lezen; automatisch gegenereerd) De bronsleutel die u kunt gebruiken om een doelverbinding te maken in het platform met klantgegevens om het publiek naar DSP te duwen. U kunt de waarde naar het klembord kopiëren en deze in de instellingen voor de doelverbinding of in een bestand plakken.

>[!MORELIKETHIS]
>
>* [Ongeveer de Bronnen van het Publiek van de Eerste Partij](source-about.md)
>* [Ondersteuning voor het activeren van Universal ID&#39;s](/help/dsp/audiences/universal-ids.md)
>* [Gebruikersnamen converteren van [!DNL Adobe Real-Time CDP] naar universele id&#39;s](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Gebruikersnamen converteren van [!DNL Amperity] naar universele id&#39;s](/help/dsp/audiences/sources/source-amperity.md)
>* [Gebruikersnamen converteren van [!DNL Optimizely] naar universele id&#39;s](/help/dsp/audiences/sources/source-optimizely.md)
>* [Gebruikersnamen converteren van [!DNL Tealium] naar universele id&#39;s](/help/dsp/audiences/sources/source-tealium.md)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
