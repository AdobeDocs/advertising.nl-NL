---
title: "Gebruikersnamen converteren van [!DNL ActionIQ] naar universele id's"
description: "Leer hoe u DSP kunt inschakelen om uw [!DNL ActionIQ] eerste-partijsegmenten."
feature: DSP Audiences
source-git-commit: ecab6e81575128718156bb0bde1a5ea33a21d5f0
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# Gebruikersnamen converteren van [!DNL ActionIQ] naar universele id&#39;s

*Beta, functie*

Gebruik de DSP integratie met de [!DNL ActionIQ] het gegevensplatform van de klant om uw gehakte e-mailadressen in universele identiteitskaart voor gerichte reclame om te zetten.

Er zijn <!-- NN --> stappen om gegevens te delen van [!DNL ActionIQ] met DSP:

1. [Een publieksbron maken in DSP](#source-create).

1. ?

## Stap 1: Een publieksbron maken in DSP {#source-create}

1. [Een publieksbron maken](source-create.md) om soorten publiek te importeren naar uw DSP account of een advertentieaccount, met de [Universal ID-indelingen](source-about.md) waarnaar u de gebruikers-id&#39;s wilt converteren.

1. Nadat u de publieksbron creeert, deel de sleutel van de broncode met [!DNL ActionIQ] gebruiker.

1. Nadat u alle stappen hebt uitgevoerd, controleert u het bestand in de publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen plaatsingsinstellingen) dat het segment binnen 24 uur vult. Vergelijk het aantal universele id&#39;s met het aantal originele hashed-e-mailadressen.

   De vertaalsnelheid van gehashte e-mailadressen naar universele id&#39;s moet groter zijn dan 90%. Als u bijvoorbeeld 100 gehashte e-mailadressen verzendt van het gegevensplatform van uw klant, moeten deze worden vertaald naar meer dan 90 universele id&#39;s. Een vertaalsnelheid van 90% of minder is een probleem. Voor meer informatie over hoe de segmenttellingen kunnen variëren, zie &quot;[Oorzaken voor gegevensvariaties tussen e-mailadressen en universele id&#39;s](#universal-ids-data-variances).&quot;

   Neem voor probleemoplossing contact op met uw accountteam van de Adobe of `adcloud-support@adobe.com`.

Segmenten worden elke 24 uur vernieuwd.

## Stap 2:

>[!MORELIKETHIS]
>
>* [Ongeveer de Bronnen van het Publiek van de Eerste Partij](/help/dsp/audiences/sources/source-about.md)
>* [Een doelbron maken om Universal ID-publiek te activeren](source-create.md)
>* [Broninstellingen voor publiek](source-settings.md)
>* [Gebruikersnamen converteren van [!DNL Adobe Real-Time CDP] naar universele id&#39;s](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Gebruikersnamen converteren van [!DNL Tealium] naar universele id&#39;s](/help/dsp/audiences/sources/source-tealium.md)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
