---
title: Aangepaste doelen
description: Leer over douanedoelstellingen om uw succesgebeurtenissen te bepalen in pakketten die voor laagste CPA of hoogste ROAS worden geoptimaliseerd.
feature: DSP Optimization
exl-id: 806450b9-ce32-4f5c-a2ac-ba8e435ce36d
source-git-commit: d1ebb6a12a04b969ba8558912c3ac76bb1632b3c
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Aangepaste doelen

De doelstellingen van de douane bepalen de succesgebeurtenissen die een adverteerder vereist om zijn bedrijfsdoelstellingen te ontmoeten. Elk pakket dat de optimalisatiedoelstellingen gebruikt &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; of &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot; moet een aangepast doel bevatten dat zal helpen het algemene optimalisatiedoel te bereiken. U kunt aangepaste doelen maken als *doelstellingen* in [!DNL Advertising Search, Social, & Commerce].

![aangepaste doelen](/help/dsp/assets/objective-goals.png)

Elk douanedoel bestaat uit één of meerdere omzettingsmetriek en de relatieve gewichten van die metriek. De beschikbare omzettingsmetriek omvat alle metriek die gebruikend de Adobe Advertising omzettingspixel en door Adobe Analytics wordt gevolgd.

>[!NOTE]
>
>* [!DNL Analytics] de afmetingen en de segmenten zijn niet beschikbaar voor Adobe Advertising optimalisering.
>* Om de gebeurtenissen van Analytics in DSP te gebruiken, werk met uw Team van de Rekening van Adobe om een adverteerder-vlakke integratie te vormen.
>* [!DNL Analytics] aangepaste gebeurtenissen volgen deze naamgevingsconventie: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Voorbeeld: `custom_event_16_examplersid`

Stel dat drie conversiemetriek bijvoorbeeld relevant zijn voor een specifiek pakket in een van uw campagnes: &quot;PDF downloaden&quot; met een waarde van 20 USD, &quot;E-mailaanmelding&quot; met een waarde van 30 USD en &quot;Bestelbevestiging&quot; met een waarde van 40 USD. Als u gewicht wilt geven volgens de eenmalige monetaire waarde van de actie van de klant, dan zouden de relatieve gewichten van de eigenschappen 1, 2, en 1.5 zijn.

Zie de [aanbevolen procedures voor het maken van aangepaste doelen](custom-goal-best-practices.md) voor uiteinden op hoe te om uw douanedoelstellingen te vormen.

Eenmaal [een aangepast doel maken](custom-goal-create.md), kunt u [toewijzen aan een pakket](/help/dsp/campaign-management/packages/package-settings.md) voor rapportage en algoritmische optimalisatie met Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Een aangepast doel maken](custom-goal-create.md)
>* [Beste praktijken voor het Bouwen van een Doel van de Douane](custom-goal-best-practices.md)
>* [Optimalisatiedoelstellingen en hoe deze te gebruiken](optimization-goals.md)
>* [Pakketinstellingen](/help/dsp/campaign-management/packages/package-settings.md)
> * [Hoe DSP uw campagnes optimaliseert](optimization-how-dsp-optimizes-campaigns.md)
