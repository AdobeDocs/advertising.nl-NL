---
title: Voeg  [!DNL Analytics for Advertising]  Macro's aan  [!DNL Flashtalking]  toe en Markeringen
description: Leer waarom en hoe te om  [!DNL Analytics for Advertising]  macro's aan uw  [!DNL Flashtalking]  toe te voegen en markeringen
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: a69bef9d249514f5c494cff8d706b9df792eaf23
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# [!DNL Analytics for Advertising] Macro&#39;s toevoegen aan [!DNL Flashtalking] Tags toevoegen

*Advertisers met slechts een integratie Adobe Advertising-Adobe Analytics*

*Organisaties zonder een direct partnerschap met [!DNL Flashtalking] slechts*

*Toepasselijk op Advertising DSP slechts*

Als u advertentietags van [!DNL Flashtalking] gebruikt voor Advertising DSP-advertenties, moet u volgparameters toevoegen aan de URL&#39;s van de bestemmingspagina. Als u het Advertising DSP-partnerschap met [!DNL Flashtalking] wilt gebruiken, voegt u Analytics voor Advertising-parameters toe aan de URL&#39;s van de bestemmingspagina. De parameters registreren AMO-id (`s_kwcid`) en `ef_id` query-tekenreeksparameters in de bestemmingspagina-URL, zodat Adobe Advertising klikgegevens voor de advertenties naar Adobe Analytics kan verzenden.

>[!NOTE]
>
>Als uw organisatie een directe samenwerking met [!DNL Flashtalking] heeft, dan is deze procedure niet noodzakelijk voor u. In plaats daarvan, login aan uw [!DNL Flashtalking] rekening en volg de [!DNL Flashtalking] steundocumentatie in [ https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros ](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros) om gegeven-pas macro&#39;s te gebruiken om `s_kwcid` en `ef_id` het volgen parameters te volgen.

Gebruik macro&#39;s voor weergave- en videoadvertenties van [!DNL Flashtalking] voor de volgende typen [!DNL Analytics for Advertising] -implementaties:

* **Advertisers met de [!DNL Adobe] [!DNL Analytics for Advertising] code van JavaScript die op hun websites** wordt uitgevoerd: De code van JavaScript registreert reeds AMO identiteitskaart (`s_kwcid`) en `ef_id` parameters van het vraagkoord. Het gebruik van macro&#39;s breidt het bijhouden van wijzigingen echter uit om op klikken gebaseerde conversies op te nemen wanneer cookies van derden niet worden ondersteund. U kunt het beste de macro&#39;s in de volgende secties aan uw advertentietags toevoegen om aanvullende doorklikgegevens vast te leggen die niet zijn vastgelegd via de JavaScript-code.

  >[!NOTE]
  >
  >De JavaScript-code is een oplossing om alleen op bijhouden te klikken als er nog cookies beschikbaar zijn. Wanneer de cookies zijn stopgezet, is het nodig de volgende macro&#39;s te implementeren.

* **Advertisers de van wie websites niet de [!DNL Analytics for Advertising] code van JavaScript gebruiken en in plaats daarvan op [!DNL Analytics] server-zij het door:sturen voor klikthrough slechts gegevens** (zonder om het even welke mening-door gegevens) baseren: De volgende macro&#39;s worden vereist om op-plaats klikactiviteit te melden die van advertenties wordt gedreven u door Adobe Advertising koopt.

## Ad-tags weergeven

Voeg binnen de instellingen voor [!DNL Flashtalking] ad-tag de volgende macro toe aan het einde van de doorklikURL in het veld `Clicktag` :

```
[ftqs:[AdobeAMO]]
```

Als het de eerste of enige querytekenreeks na de basis-URL is, scheidt u deze van de basis-URL met een `?` . Als de basis-URL meerdere querytekenreeksen bevat, begint de eerste tekenreeks met een `?` en elke volgende tekenreeks met een `&` .

Voorbeelden:

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Video-advertentietags

Voeg binnen de instellingen voor [!DNL Flashtalking] ad-tag de volgende macro toe aan het einde van de doorklikURL in het veld `Clicktag` :

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Als het de eerste of enige querytekenreeks na de basis-URL is, scheidt u deze van de basis-URL met een `?` . Als de basis-URL meerdere querytekenreeksen bevat, begint de eerste tekenreeks met een `?` en elke volgende tekenreeks met een `&` .

Voorbeelden:

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [ Overzicht van  [!DNL Analytics for Advertising]](overview.md)
>* [ Adobe Advertising IDs die door  [!DNL Analytics]](/help/integrations/analytics/ids.md) wordt gebruikt
>* [ voeg  [!DNL Analytics for Advertising]  Macro&#39;s aan  [!DNL Google Campaign Manager 360]  toe - Markeringen ](/help/integrations/analytics/macros-google-campaign-manager.md)

