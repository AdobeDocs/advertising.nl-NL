---
title: Klikgegevens verzamelen en gegevens weergeven via Advertising DSP-campagnes
description: Leer hoe u op een cookie gebaseerde indruk vastlegt en op gebeurtenissen klikt vanuit Advertising DSP-advertenties met Audience Manager-pixels
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Media-belichtingsgegevens verzamelen via Advertising DSP-campagnes

*Advertisers met slechts Advertising DSP*

*Advertisers met slechts een integratie Adobe Advertising-Adobe Audience Manager*

In dit document wordt uitgelegd hoe u Advertising DSP-advertenties kunt labelen om op cookies gebaseerde indruk vast te leggen en op gebeurtenissen kunt klikken met Audience Manager-pixels. Ook worden extra taken uitgevoerd die nodig zijn om de gegevens te kunnen gebruiken.

De gebeurtenispixels leggen geen gebeurtenissen vast die plaatsvinden in omgevingen zonder cookie, zoals mobiele apps en aangesloten tv (CTV).

## Stap 1: Een gegevensbron instellen in Audience Manager {#set-up-data-source}

In Audience Manager, creeer a [ gegevensbron ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) voor de indruk van DSP en klik gegevens. Omvat gegevensbron identiteitskaart [ in elke gebeurtenismarkering ](#implement-dsp-pixels) zodat alle gevolgde gebeurtenissen aan de gegevensbron worden toegeschreven.

>[!NOTE]
> Het is mogelijk om alle indruk te verzamelen en gegevens voor reclamecampagnes te klikken die op veelvoudige DSPs binnen één enkele gegevensbron lopen.

## Stap 2: Importeer de indruk en klik op gebeurtenispixels op webpagina&#39;s {#implement-dsp-pixels}

Adverteerders kunnen gebeurtenislabels voor hun eigen merken maken en implementeren. Neem indien nodig contact op met uw Adobe Audience Manager-consultant of uw Adobe-accountteam voor ondersteuning.

>[!NOTE]
>
>Als uw organisatie [!DNL Analytics] tracking gebruikt, is het mogelijk dat u geen Audience Manager-functie voor bijhouden van klikken nodig hebt. Adobe Analytics vangt signalen vast en kan hen naar Audience Manager door [ server-kant door:sturen ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html) verzenden.

### Pixelsyntaxis

Gebeurtenispixels moeten de volgende parameters bevatten.

**Indruk-volgende pixel:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

met [ facultatieve extra parameters ](#parameters) vooraf bepaald met `&`

**klik-volgende pixel:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

met [ facultatieve extra parameters ](#parameters) vooraf bepaald met `&`

Waarbij:

* `[Audience Manager customer domain]` is de domeinnaam die de indruk wekt of op gebeurtenissen klikt naar [!DNL Adobe] .

* `[source id]` is identiteitskaart voor de [ gegevensbron ](#set-up-data-source) waarin u de indruk van DSP volgt en gegevens klikt.

* `[redirect URL]` is de dubbelgecodeerde omleidings-URL. Als u een online coderingsprogramma gebruikt, zoals www.urlencoder.org, voert u de tekenreeks uit via de codeermodule en codeert u het resultaat opnieuw.

* `${TM_CAMPAIGN_ID_NUM}` is de numerieke campagne-id in DSP. Als u een afzonderlijke campagne-id wilt coderen in plaats van de DSP-macro te gebruiken, zoekt u de id in de campagne-instellingen.

* Elke [ parameter ](#key-value-pairs) wordt vooraf bepaald met `&` en is in het formaat `d_parameter=parameter_id`, waar `parameter` door het zeer belangrijke waardepaar voor het nieuwe gebied wordt vervangen. Voorbeeld: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parameters als sleutelwaardeparen {#parameters}

**Formaat:** `d_parameter=parameter_id`

     waar:
    
    * de parameter vooraf bepaald door ` &amp; ` 
    
    * ` parameter ` wordt vervangen door het zeer belangrijk-waardepaar voor het nieuwe gebied 
    
     Voorbeeld: `&amp;d_placement=$ {TM_PLACEMENT_ID_NUM} ` 

Beide types van pixel kunnen extra parameters als *zeer belangrijk-waardeparen* bevatten om eigenschappen te verzamelen of campagnemetagegevens (zoals een plaatsingsnaam of een campagnenaam) voor andere rapporten te verstrekken. Een zeer belangrijk-waardepaar bestaat uit twee verwante elementen: a *sleutel*, die een constante is die de gegevensreeks bepaalt, en a *waarde*, die een variabele is die tot de reeks behoort.

In het zeer belangrijk-waardepaar, kan de waardevariabele of hard-gecodeerde identiteitskaart of a *macro* zijn, die een kleine eenheid van met alle accomodatie code is die dynamisch met de overeenkomstige waarden wordt vervangen wanneer de ad markering voor campagne en gebruiker het volgen laadt. Voor op campagne betrekking hebbende parameters, kunt u [ macro&#39;s van DSP ](/help/dsp/campaign-management/macros.md) in plaats van de macro&#39;s van Audience Manager gebruiken om campagneattributen samen met de overeenkomstige indruk te verzenden of gegevens aan Audience Manager te klikken, gebruikend één enkel pixel over alle advertenties. De DSP-macro&#39;s die u in de gebeurtenispixels invoegt, moeten de juiste waarden zijn voor de sleutelwaardeparen die u in de pixels opneemt. Voor de `d_placement` -toets gebruikt u bijvoorbeeld de DSP-macro `${TM_PLACEMENT_ID_NUM}` als waarde voor het vastleggen van plaatsings-id&#39;s die door de Adobe Advertising-macro zijn gegenereerd.

Voor een lijst van macro&#39;s die Audience Manager voor de pixel van de impeilingsgebeurtenis steunt, zie &quot;[ het Vangst van de Gegevens van de Indrukking van de Campagne via de Vraag van het Pixel ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

Voor een lijst van macro&#39;s die Audience Manager voor de pixel van de klikgebeurtenis steunt, zie &quot;[ het Vangst Campagne Gegevens van de Klik via de Vraag van het Pixel ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* De beste manier is om de campagne, plaatsing, creatieve (advertentie) en site-id&#39;s op te nemen, zodat u de campagnerekenmerken kunt gebruiken om Audience Manager-kenmerken te maken.
>* Voor het maken van Audience Optimization-rapporten zijn aanvullende parameters vereist.
>* In de zeer belangrijk-waardeparen, vervang de waarden met de relevante [ macro&#39;s van DSP ](/help/dsp/campaign-management/macros.md) zodat kunt u één enkele pixel over alle reclame in alle campagnes gebruiken. Wijzig bijvoorbeeld `d_campaign=[%campaignID%]` in `d_campaign=${TM_CAMPAIGN_ID_NUM}` om campagne-id&#39;s vast te leggen die zijn gegenereerd door de Adobe Advertising-macro.
>* Indien nodig kunt u uw eigen parameters met gecodeerde waarden maken. Voorbeeld: `d_DSP=AdCloud`

Voorbeeld van een pixel van een impressiegebeurtenis:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Waar moeten de pixels worden toegevoegd?

#### Pixel voor het bijhouden van indrukking

Koppel een pixel voor het bijhouden van een impressie aan alle advertenties in uw [!DNL DSP] -campagnes. U kunt dit op de volgende plaatsen doen:

* Op plaatsingsniveau, dat de pixel door gebrek op alle advertenties in de plaatsing toepast. Voeg in het gedeelte Bijhouden van de plaatsingsinstellingen de pixel toe in het [[!UICONTROL Event pixels] veld ](/help/dsp/campaign-management/placements/placement-settings.md) .

* Op advertentieniveau, dat om het even welke plaatsing-vlakke gebeurtenispixel met voeten treedt. In de advertentiemontages, [ creeer een gebeurtenispixel op het [!UICONTROL Pixel] lusje ](/help/dsp/campaign-management/ads/ad-edit.md).

* (Voor advertenties op een externe advertentieserver) Op advertentieniveau in de advertentieserver.

#### Klikken en pixel bijhouden

Voeg in de advertentieserver de pixel van de klikgebeurtenis in (met de gecodeerde URL toegevoegd) waar u normaal de klikdoorklikURL van de advertentie invoegt.

## Stap 3: Taken na de implementatie

Zodra de gebeurtenislabels worden uitgevoerd, stromen de gegevens in de servers van de gegevensinzameling van Audience Manager. Voer de volgende taken uit voordat u de gegevens in rapporten kunt gebruiken.

### Een [!DNL Amazon S3] emmertje en gegevensbron maken

Zodra uw gegevens op de servers van Audience Manager zijn, moet u een [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) emmertje, en dan een gegevensbron tot stand brengen, waarnaar alle pixelgegevens worden verzonden. Contacteer uw consultant van Audience Manager of [ de Zorg van de Klant ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) als u steun nodig hebt.

### Audience Manager-kenmerken en -segmenten maken

Uw gebeurtenisgegevens stromen in Audience Manager als [ ongebruikte signalen ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). Creëer manueel [ regel-gebaseerde treinstellen ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) van de ingebedde gegevens, en creeer dan [ segmenten ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) gebruikend die eigenschappen, alvorens u de gegevens in rapporten kunt gebruiken.

Voorbeeld dat gegevens op gebruikersniveau vult voor gebruikers die worden blootgesteld aan een bepaalde creatieve functie in DSP:

1. De gebeurtenis identificeren als `d_event = imp` .
1. Identificeer de creatieve id in de DSP-campagne en wijs deze vervolgens toe als `d_creative=[Creative ID]` .

![ het aanmaakscherm van het Beetje ](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [ Macro&#39;s van DSP ](/help/dsp/campaign-management/macros.md)
>* [ Overzicht van het verzenden van de media van DSP blootstellingsgegevens naar Adobe Audience Manager ](overview.md)
>* [ Gevallen van het Gebruik ](use-cases.md)
