---
title: "Gebruikersnamen converteren van [!DNL ActionIQ] naar universele id's"
description: "Leer hoe u DSP kunt inschakelen om uw [!DNL ActionIQ] eerste-partijsegmenten."
feature: DSP Audiences
source-git-commit: 4292083dac92860854dca30f7897e1b0279f68ec
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Gebruikersnamen converteren van [!DNL ActionIQ] naar universele id&#39;s

*Beta-functie*

Gebruik de DSP integratie met de [!DNL ActionIQ] het gegevensplatform van de klant om uw gehakte e-mailadressen in universele identiteitskaart voor gerichte reclame om te zetten.

Er zijn <!-- NN --> stappen om gegevens te delen van [!DNL ActionIQ] met DSP:

1. [Een publieksbron maken in DSP](#source-create).

1. ?

## Stap 1: Een publieksbron maken in DSP {#source-create}

1. [Een publieksbron maken](source-manage.md) om soorten publiek te importeren naar uw DSP account of een advertentieaccount, met de [Universal ID-indelingen](source-about.md) waarnaar u de gebruikers-id&#39;s wilt converteren.

1. Nadat u de publieksbron creeert, deel de sleutel van de broncode met [!DNL ActionIQ] gebruiker.

1. 
   <!-- ActionIQ-specific step(s) -->

1. Verifieer in uw publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen plaatsingsinstellingen) dat het segment vult en het aantal universele id&#39;s vergelijkt met het aantal oorspronkelijke gehashte e-mailadressen.

   De segmenten moeten binnen 24 uur in DSP beschikbaar zijn. Nadat DSP de segmentgegevens ontvangt, moet het aantal gebruikers binnen negen (9) uur zichtbaar zijn.

   De vertaalsnelheid van gehashte e-mailadressen naar universele id&#39;s moet groter zijn dan 90%; de vertaalsnelheid voor [!DNL RampIDs] met name 95 % als alle gehashte e - mailadressen uniek zijn . Als u bijvoorbeeld 100 gehashte e-mailadressen verzendt van het gegevensplatform van uw klant, moeten deze naar minstens 95 worden vertaald [!DNL RampIDs] of meer dan 90 andere typen universele id&#39;s. Een lager vertaaltarief is een kwestie. Voor meer informatie over hoe de segmenttellingen kunnen variëren, zie &quot;[Oorzaken voor gegevensvariaties tussen e-mailadressen en universele id&#39;s](#universal-ids-data-variances).&quot;

   Neem voor probleemoplossing contact op met uw accountteam van de Adobe of `adcloud-support@adobe.com`.

Segmenten worden elke 24 uur vernieuwd.

## Stap 2:

>[!MORELIKETHIS]
>
>* [Ongeveer de Bronnen van het Publiek van de Eerste Partij](/help/dsp/audiences/sources/source-about.md)
>* [Bronnen voor publiek beheren om Universal ID-publiek te activeren](source-manage.md)
>* [Gebruikersnamen converteren van [!DNL Adobe Real-Time CDP] naar universele id&#39;s](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Gebruikersnamen converteren van [!DNL Tealium] naar universele id&#39;s](/help/dsp/audiences/sources/source-tealium.md)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
