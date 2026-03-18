---
title: Voeg  [!DNL Analytics for Advertising]  macro's aan  [!DNL Google Campaign Manager 360]  toe en markeringen
description: Leer waarom en hoe te om  [!DNL Analytics for Advertising]  macro's aan uw  [!DNL Google Campaign Manager 360]  toe te voegen en markeringen
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: 0b95d99a1370a047642f8d1e4bbafe35ad5187f6
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# [!DNL Analytics for Advertising] macros toevoegen aan [!DNL Google Campaign Manager 360] -advertentietags

*Advertisers met slechts een integratie Adobe Advertising-Adobe Analytics*

*Toepasselijk op Advertising DSP slechts*

Als u advertentietags van [!DNL Google Campaign Manager 360] gebruikt voor uw Advertising DSP-advertenties, voegt u [!DNL Analytics for Advertising] -parameters toe aan de URL&#39;s van de bestemmingspagina met de [`%p` macro &#x200B;](https://support.google.com/campaignmanager/table/6096962) . De parameters registreren AMO-id (`s_kwcid`) en `ef_id` query-tekenreeksparameters in de bestemmingspagina-URL, zodat Adobe Advertising klikgegevens voor de advertenties naar Adobe Analytics kan verzenden.

Gebruik macro&#39;s voor weergave- en videoadvertenties van [!DNL Campaign Manager 360] voor de volgende typen [!DNL Analytics for Advertising] -implementaties:

* **Advertisers met de [!DNL Adobe] [!DNL Analytics for Advertising] code van JavaScript die op hun websites** wordt uitgevoerd: De code van JavaScript registreert reeds AMO identiteitskaart (`s_kwcid`) en `ef_id` parameters van het vraagkoord. Het gebruik van macro&#39;s breidt het bijhouden van wijzigingen echter uit om op klikken gebaseerde conversies op te nemen wanneer cookies van derden niet worden ondersteund. U kunt het beste de macro&#39;s in de volgende secties aan uw advertentietags toevoegen om aanvullende doorklikgegevens vast te leggen die niet zijn vastgelegd via de JavaScript-code.

>[!NOTE]
>
>De JavaScript-code is een oplossing om alleen op bijhouden te klikken als er nog cookies beschikbaar zijn. Wanneer de cookies zijn stopgezet, is het nodig de volgende macro&#39;s te implementeren.

* **Advertisers de van wie websites niet de [!DNL Analytics for Advertising] code van JavaScript gebruiken en in plaats daarvan op [!DNL Analytics] server-zij het door:sturen voor klikthrough slechts gegevens** (zonder om het even welke mening-door gegevens) baseren: De volgende macro&#39;s worden vereist om op-plaats klikactiviteit te melden die van advertenties wordt gedreven u door Adobe Advertising koopt.

## De macro&#39;s toevoegen aan uw [!DNL Google Campaign Manager 360] -advertenties

Voeg binnen [!DNL Google Campaign Manager 360] voor elk van uw weergave- en videoadvertenties aan de URL van de bestemmingspagina de volgende parameter toe: `%pamo=!;`

U kunt de URL van de bestemmingspagina op verschillende manieren opgeven. De volgende subsecties bevatten instructies voor elke optie.

Hieronder ziet u een voorbeeld van de URL van de landingspagina die is opgemaakt met het achtervoegsel.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>&#x200B;>* Als de bestemmingspagina-URL een hash-symbool (#) bevat, wat niet gebruikelijk is, plaatst u de parameter `amo` vóór het hashsymbool.
>* Als er geen andere parameters zijn opgenomen na de parameter `amo` , voegt u er vervolgens een parameter (bijvoorbeeld &amp;a=b) aan toe. Voorbeeld: `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Het URL-achtervoegsel van de landingspagina op advertentieniveau configureren

1. Zie de [&#x200B; instructies om de adverteerdereigenschappen &#x200B;](https://support.google.com/campaignmanager/answer/2829344) te openen.
1. Neem [!UICONTROL Landing page URL suffix] op in het veld `%pamo!;` in de instellingen van [!UICONTROL URL suffix] .

### Het URL-achtervoegsel van de landingspagina op campagneniveau configureren

1. Zie de [&#x200B; instructies om de campagneeigenschappen &#x200B;](https://support.google.com/campaignmanager/answer/2838056#set) te openen.
1. Neem [!UICONTROL Landing page URL suffix] op in het veld `%pamo!;` in de instellingen van [!UICONTROL URL suffix] .

### Het URL-achtervoegsel van de bestemmingspagina op creatief niveau configureren

1. Open de creatieve eigenschappen.
1. Neem in de instelling [!UICONTROL Click tags] `%pamo!;` op in de kolom [!UICONTROL Landing page] voor de kliktag.

## Hoe [!DNL Analytics for Advertising] macro&#39;s worden uitgebreid in DSP

Wanneer u in DSP een advertentie maakt die de parameter [!DNL Analytics for Advertising] (`amo`) bevat, worden de macro&#39;s `ef_id` en `s_kwcid` automatisch toegevoegd aan de klik-URL. U kunt het beste de tag in DSP controleren om te controleren of de macro&#39;s `ef_id` en `s_kwcid` aanwezig zijn.

Het volgende is een voorbeeld van a [!DNL Google Campaign Manager 360] [&#x200B; ins markering &#x200B;](https://support.google.com/campaignmanager/answer/6080468) aangezien het in DSP verschijnt.

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

Wanneer een gebruiker op de advertentie klikt, ziet [!DNL Google Campaign Manager 360] `%pamo` in het URL-achtervoegsel en wordt de waarde van de parameter `amo` dynamisch in de URL ingevoegd.

>[!MORELIKETHIS]
>
>* [&#x200B; Overzicht van  [!DNL Analytics for Advertising]](overview.md)
>* [&#x200B; Adobe Advertising IDs die door  [!DNL Analytics]](/help/integrations/analytics/ids.md) wordt gebruikt
>* [&#x200B; voeg  [!DNL Analytics for Advertising]  Macro&#39;s aan  [!DNL Flashtalking]  toe - Markeringen &#x200B;](macros-flashtalking.md)
