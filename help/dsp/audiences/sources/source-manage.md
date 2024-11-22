---
title: Bronnen voor publiek beheren om Universal ID-publiek te activeren
description: Leer hoe u een bron kunt maken en beheren om een publiek van uw klantgegevensplatform te importeren en deze om te zetten in segmenten met universele id's.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 3a641db6b145e67e6e1f1daca271dd524973e075
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 0%

---

# Bronnen voor publiek beheren om Universal ID-publiek te activeren

*eigenschap van Beta*

Creeer een bron in DSP voor elk eerste-partijpubliek in uw platform van klantengegevens dat u in segmenten wilt omzetten die gespecificeerde universele types van identiteitskaart bevatten. U kunt de segmenten importeren naar de DSP van uw organisatie of naar een advertentieaccount. Gegevenskosten worden toegepast op basis van de geselecteerde Universal ID-typen. Zodra u een bron creeert, worden de extra stappen vereist om het publiek van elk platform van klantengegevens in te voeren. Zie de nota aan het eind van de procedure om een bron tot stand te brengen.

U kunt de Universal ID-typen wijzigen waarnaar het bronpubliek wordt vertaald, en een logboek met de wijzigingen weergeven.

U kunt ook een bron verwijderen.

## Een Audience Source maken

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL Sources]** .

1. Klik op **[!UICONTROL Add Source]**.

1. In het [!UICONTROL Select a Type] menu, selecteer uw [ platform van klantengegevens ](source-about.md):

   * *[!UICONTROL RT-CDP]*: De [!DNL Adobe Real-Time CDP] .

   * *[!UICONTROL ActionIQ]*: Het [!DNL ActionIQ] klantgegevensplatform.

   * *[!UICONTROL Amperity]*: Het [!DNL Amperity] klantgegevensplatform.

   * *[!UICONTROL Optimizely]*: Het [!DNL Optimizely] klantgegevensplatform.

   * *[!UICONTROL Tealium CDP]*: (Alleen geconfigureerde gebruikers) Het [!DNL Tealium] -platform voor klantgegevens.

1. Geef de waarde [!UICONTROL Data Visibility Level] : *[!UICONTROL Advertiser]* of *[!UICONTROL Account]* op.

1. Ga de resterende [ bronmontages ](#source-settings) in.

   Bewaar een kopie van de gegenereerde [!UICONTROL Source Key] . U hebt de waarde later nodig.

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Nadat u een bron voor uw platform van klantengegevens creeert, zult u extra stappen moeten voltooien om uw publiek in te voeren. Zie het [ werkschema voor  [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md), <!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), --> het [ werkschema voor  [!DNL Amperity]](source-amperity.md), het [ werkschema voor  [!DNL Optimizely]](source-optimizely.md), en het [ werkschema voor  [!DNL Tealium]](source-tealium.md).

## De id-typen wijzigen voor een publiek-Source

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL Sources]** .

1. Plaats de cursor op de bronrij en klik op **[!UICONTROL Edit]** .

1. Verander [ IDs die voor de bron ](#source-settings) wordt geselecteerd.

1. Klik op **[!UICONTROL Save]**.

## Een Audience Source verwijderen

Het schrappen van een bron verwijdert de segmenten die door de bron worden vertaald.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL Sources]** .

1. Plaats de cursor op de bronrij en klik op **[!UICONTROL Delete]** .

1. Klik in het bevestigingsbericht op **[!UICONTROL Delete]** .

## Het Wijzigingslogboek weergeven voor een publiek-Source

U kunt details over veranderingen in een verslag van de publieksbron bekijken en naar keuze nota&#39;s aan het logboek vastmaken.

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL Sources]** .

1. Plaats de cursor op de bronrij en klik op **[!UICONTROL Change log]** .

1. (Optioneel) Een notitie toevoegen aan het wijzigingslogboek:

   1. Plaats de cursor op de bronrij en klik op **[!UICONTROL Add Notes]** .

   1. Voer de notitie in en klik op **[!UICONTROL Save]** .

      De maximumlengte is 256 tekens.

1. (Optioneel) Als u het logbestand in een groter detailscherm wilt openen, houdt u de cursor boven de bronrij en klikt u op **[!UICONTROL View Details]** .

## Source-instellingen voor publiek {#source-settings}

**[!UICONTROL Data Visibility Level]:** Of de segmenten aan één enkele adverteerder met toegang tot de rekening (*[!UICONTROL Advertiser]*) of aan alle adverteerders met toegang tot de rekening *[!UICONTROL Account]* beschikbaar zijn.

**[!UICONTROL Advertiser]:** (Advertiser-vlakke zicht slechts) de adverteerder voor wie de segmenten beschikbaar zijn. Selecteer een optie in de lijst met adverteerders die toegang hebben tot het account.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] slechts bronnen) de organisatie-ID van Adobe Experience Cloud voor de [!DNL Adobe Experience Platform] rekening.

**[!UICONTROL Convert PII to the following IDs]:** De types van identiteitskaart waaraan u uw persoonlijk identificeerbare informatie (PII) zult omzetten. Als u meerdere typen selecteert, wordt het gegenereerde segment gevuld met waarden voor elk geselecteerd id-type (bijvoorbeeld een [!DNL RampID] en een [!DNL Unified ID2.0] voor elk e-mailadres). Gegevensheffingen worden dienovereenkomstig toegepast.

Voor [!DNL RampID] en [!DNL Unified ID2.0] zoekt de leverancier elk e-mailadres om te controleren of er al een id bestaat en zet het adres om in een overeenkomende id, indien beschikbaar. Als er geen id voor het adres bestaat, wordt er een nieuwe id gemaakt.

>[!NOTE]
>
>U kunt slechts één type id in één plaatsing als doel instellen. Om prestaties door type van identiteitskaart te testen, [ creeer een afzonderlijke plaatsing ](/help/dsp/campaign-management/placements/placement-create.md) voor elk type van identiteitskaart in het segment.

* *[!DNL RampID]:* PII in a om te zetten [!DNL RampID]. U kunt [!DNL RampIDs] gebruiken voor het opnieuw toewijzen van gebruikers die zich aanmelden en voor [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) metingen.

* *[!DNL Unified ID2.0](Beta):* om PII in a [ Verenigde identiteitskaart 2.0 ](https://unifiedid.com) identiteitskaart voor het opnieuw richten van het programma-binnen gebruikers om te zetten.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** De serviceovereenkomst voor het converteren van PII naar universele id&#39;s. U of een andere gebruiker in de DSP account moet de voorwaarden één keer accepteren voordat u gegevens kunt converteren naar een nieuw id-type. Voor klanten met beheerde de dienstcontracten, zal uw Team van de Rekening van de Adobe uw toestemming krijgen en zal de termijnen namens uw organisatie goedkeuren. Om de termijnen te lezen, klik **>**. Schuif naar de onderkant van de voorwaarden en klik op **[!UICONTROL Accept]** om de voorwaarden te accepteren.

**[!UICONTROL Source Key]:** (Alleen-lezen; automatisch gegenereerd) De bronsleutel die u kunt gebruiken om een doelverbinding in het klantgegevensplatform te maken om een publiek naar Advertising DSP te sturen. U kunt de waarde naar het klembord kopiëren en deze in de instellingen voor de doelverbinding of in een bestand plakken.

>[!MORELIKETHIS]
>
>* [ Ongeveer de Bronnen van het Publiek van de Eerste Partij ](source-about.md)
>* [ Steun voor het Activeren van Universal IDs ](/help/dsp/audiences/universal-ids.md)
>* [ zet Gebruiker IDs van  [!DNL Adobe Real-Time CDP]  in Universal IDs ](/help/dsp/audiences/sources/source-adobe-rtcdp.md) om
>* [ zet Gebruiker IDs van  [!DNL Amperity]  in Universal IDs ](/help/dsp/audiences/sources/source-amperity.md) om
>* [ zet Gebruiker IDs van  [!DNL Optimizely]  in Universal IDs ](/help/dsp/audiences/sources/source-optimizely.md) om
>* [ zet Gebruiker IDs van  [!DNL Tealium]  in Universal IDs ](/help/dsp/audiences/sources/source-tealium.md) om
>* [ Ongeveer het Beheer van het Publiek ](/help/dsp/audiences/audience-about.md)
