---
title: Toevoegen [!DNL Analytics for Advertising] Macro's naar [!DNL Flashtalking] Labels toevoegen
description: Ontdek waarom en hoe u kunt toevoegen [!DNL Analytics for Advertising] macro's voor uw [!DNL Flashtalking] advertentietags
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: c7821f112757f695a6ab9da1fffb014b822e1ff3
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Toevoegen [!DNL Analytics for Advertising] Macro&#39;s naar [!DNL Flashtalking] Labels toevoegen

*Adverteerders met alleen Adobe Advertising-Adobe Analytics-integratie*

*Alleen van toepassing op DSP*

Als u tags ad gebruikt van [!DNL Flashtalking] Voeg voor advertenties DSP advertenties Analytics voor advertentieparameters toe aan de URL&#39;s van de bestemmingspagina. De parameters registreren AMO-id (`s_kwcid`) en `ef_id` query-tekenreeksparameters in de URL van de bestemmingspagina, zodat Adobe Advertising klikgegevens voor de advertenties naar Adobe Analytics kan verzenden.

Macro&#39;s gebruiken voor [!DNL Flashtalking] weergave- en videoadvertenties voor de volgende typen [!DNL Analytics for Advertising] implementaties:

* **Adverteerders met de [!DNL Adobe] [!DNL Analytics for Advertising] JavaScript-code geïmplementeerd op hun websites**: In de JavaScript-code wordt de AMO-id al vastgelegd (`s_kwcid`) en `ef_id` querytekenreeksparameters. Het gebruik van macro&#39;s breidt het bijhouden van wijzigingen echter uit om op klikken gebaseerde conversies op te nemen wanneer cookies van derden niet worden ondersteund. U kunt het beste de macro&#39;s in de volgende secties aan uw advertentietags toevoegen om aanvullende doorklikgegevens vast te leggen die niet door de JavaScript-code worden vastgelegd.

>[!NOTE]
>
>De JavaScript-code is een oplossing om alleen op bijhouden te klikken als er nog cookies beschikbaar zijn. Wanneer de cookies zijn stopgezet, is het nodig de volgende macro&#39;s te implementeren.

* **Adverteerders van wie de websites de [!DNL Analytics for Advertising] JavaScript-code en vertrouwen in plaats daarvan op [!DNL Analytics] server-kant het door:sturen voor klik-door gegevens slechts** (zonder doorkijkgegevens): de volgende macro&#39;s zijn vereist om klikactiviteiten ter plaatse te melden die worden aangestuurd door advertenties die u via de Adobe Advertising koopt.

## Ad-tags weergeven

Binnen de [!DNL Flashtalking] voeg de volgende macro toe aan het einde van de doorklikURL in het dialoogvenster `Clicktag` veld:

```
[ftqs:[AdobeAMO]]
```

Als het de eerste of enige querytekenreeks na de basis-URL is, scheidt u deze van de basis-URL met een `?`. Als de basis-URL meerdere querytekenreeksen bevat, begint de eerste tekenreeks met een `?` en elke volgende tekenreeks met een `&`.

Voorbeelden:

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Video-advertentietags

Binnen de [!DNL Flashtalking] voeg de volgende macro toe aan het einde van de doorklikURL in het dialoogvenster `Clicktag` veld:

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Als het de eerste of enige querytekenreeks na de basis-URL is, scheidt u deze van de basis-URL met een `?`. Als de basis-URL meerdere querytekenreeksen bevat, begint de eerste tekenreeks met een `?` en elke volgende tekenreeks met een `&`.

Voorbeelden:

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Overzicht van [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising-id&#39;s gebruikt door [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Toevoegen [!DNL Analytics for Advertising] Macro&#39;s naar [!DNL Google Campaign Manager 360] Labels toevoegen](/help/integrations/analytics/macros-google-campaign-manager.md)

