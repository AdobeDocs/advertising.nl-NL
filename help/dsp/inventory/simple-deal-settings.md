---
title: '[!UICONTROL Simple Ad Serving] Deal Settings'
description: Meer informatie over de beschikbare instellingen voor [!UICONTROL Simple Ad Serving] -deals.
feature: DSP Simple Ad Serving
exl-id: 20e23182-d3d0-457f-a821-0ad4770a138d
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] Deal Settings

## Nieuwe [!UICONTROL Simple Ad Serving] deals

### [!UICONTROL Select Ad Source]

| Parameter | Beschrijving |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | Het mediatype voor deze deal: *[!UICONTROL Video],* *[!UICONTROL Display],* of *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | De naam van de uitgever die deze voorraad verkoopt. Zoek naar een uitgever door minstens de eerste twee karakters in de naam in te gaan. Neem contact op met het accountteam van de Adobe als u een uitgever wilt toevoegen die niet in de lijst staat. |
| **[!UICONTROL Advertiser]** | Één enkele adverteerder in de rekening die tot deze overeenkomst kan toegang hebben. Selecteer ook de campagne en (naar keuze) het pakket waarin de overeenkomst beschikbaar is. |
| **[!UICONTROL Media Quality Assessment?]** | (Sommige gebruikers) Laat de advertentie toe om op een andere DSP voor derdecontrole te lopen. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | De enige optie is *[!UICONTROL Site Serve (Event Pixels)]* . |
| **[!UICONTROL Ad Creation]** | (Alleen nieuwe deals) Of:<ul><li>*[!UICONTROL Create New]:* om een advertentie voor deze overeenkomst tot stand te brengen.</li><li>*[!UICONTROL Select Ads]:* om een bestaande advertentie voor deze overeenkomst te gebruiken.</li></ul> |
| **[!UICONTROL Ad Type]** | Het advertentietype voor deze overeenkomst. Als u advertenties voor de overeenkomst gaat creëren, omvat de advertentiegrootte of de duur, zoals gevraagd. De beschikbare opties variëren per mediatype. |

{style="table-layout:auto"}

### [!UICONTROL Select Ad(s)]

(Wanneer u bestaande advertenties gebruikt) De advertenties om in de overeenkomst te omvatten. Schakel het selectievakje naast elke advertentie in die u wilt opnemen.

### [!UICONTROL Select & Upload [Media Type]]

(Nieuwe slechts advertenties) Screens om een nieuwe [ derdeadvertentie ](/help/dsp/campaign-management/ads/ad-create-multiple.md) tot stand te brengen.

### [!UICONTROL Feed Details]

| Parameter | Beschrijving |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | De kosten per 1000 beelden (CPM), zoals die in de tariefkaart voor uw contract worden weerspiegeld. Neem voor deze waarde contact op met het accountteam van de Adobe. <br><br> specificeer ook de munt voor de overeenkomst. Alle gebruikers kunnen USD selecteren, of, als het SSP extra valuta&#39;s steunt, de munt voor de DSP rekening. |
| **[!UICONTROL Third Party Billed Fees]** | (Optioneel) Een statische vergoeding voor derden die moet worden bijgehouden als niet-factureerbare kostprijs, en de valuta voor de transactie.<br><br> alle gebruikers kunnen USD selecteren, of, als SSP extra valuta&#39;s steunt, de munt voor de DSP rekening. **NOTA:** de Billable taksen worden weerspiegeld in [!UICONTROL Net CPM] metrisch. |
| **[!UICONTROL Third Party Fee Description]** | (Optioneel) Een beschrijving van de vergoedingen van derden. |
| **[!UICONTROL Flight Dates]** | De begin en einddata voor verkeer die deze overeenkomst gebruiken. De vluchtdata moeten worden opgenomen in de vluchtdata voor de campagne. De advertentietags retourneren alleen een reactie tijdens de opgegeven vlucht.<br><br> De beste manier om een afzonderlijke eenvoudige campagne voor het verzenden van advertenties te maken met een looptijd van een jaar en er trackingpixels in te bouwen. |
| **[!UICONTROL Impressions]** | (Facultatief) het geschatte aantal indrukkingen u verwacht om te lopen gebruikend deze overeenkomst. Deze waarde wordt alleen gebruikt voor traceringsdoeleinden en om te markeren wanneer de leveringsdoelen zijn bereikt. De uitgever beheert de werkelijke levering en levering. De beste manier is om een groot aantal afbeeldingen in te voeren om de tag actief te houden binnen DSP, zodat deze indien nodig kan worden vernieuwd of uitgebreid. |
| **[!UICONTROL Deal Name]** | De naam van de deal. Ga een naam in, of selecteer *[!UICONTROL Auto Generate Deal Name]* om DSP een naam te laten produceren die op de overeenkomstendetails wordt gebaseerd.<br><br> Voorbeeld van een automatisch gegenereerde naam: `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | (Alleen-lezen) De advertenties die deel uitmaken van de deal. Als u een advertentie wilt bewerken, klikt u op de advertentienaam. Als u een advertentie uit de deal wilt verwijderen, klikt u op **[!UICONTROL X]** naast de naam van de advertentie. |

{style="table-layout:auto"}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [ Over [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [ creeer a [!UICONTROL Simple Ad Serving] Overeenkomst ](simple-deal-create.md)
>* [ geeft [!UICONTROL Simple Ad Serving] Montages van de Overeenkomst ](simple-deal-edit.md) uit
>* [ Mening een Gedetailleerd Rapport voor een Overeenkomst ](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
