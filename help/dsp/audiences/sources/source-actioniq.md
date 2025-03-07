---
title: Zet Gebruiker IDs van  [!DNL ActionIQ]  in Universele IDs om
description: Leer hoe te om DSP toe te laten om uw  [!DNL ActionIQ]  eerste-partijsegmenten in te voeren.
feature: DSP Audiences
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Gebruikersnamen converteren van [!DNL ActionIQ] naar universele id&#39;s

*eigenschap van Beta*

Gebruik de DSP integratie met het [!DNL ActionIQ] -klantgegevensplatform om uw gehashte e-mailadressen om te zetten in universele id&#39;s voor gerichte advertenties.

Er zijn <!-- NN --> stappen om gegevens van [!DNL ActionIQ] met DSP te delen:

1. [ creeer een publieksbron in DSP ](#source-create).

1. ?

## Stap 1: Een publieksbron maken in DSP {#source-create}

1. [ creeer een publieksbron ](source-manage.md) om publiek in uw DSP rekening of een adverteerderrekening in te voeren, specificerend de [ universele formaten van identiteitskaart ](source-about.md) waarnaar u uw gebruikersidentificatiecodes wilt omzetten.

1. Nadat u de publieksbron hebt gemaakt, deelt u de broncodesleutel met de [!DNL ActionIQ] -gebruiker.

## Stap 2:

## Stap 3:

1. Controleer in uw publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen de plaatsingsinstellingen) of het segment vult en vergelijk het aantal universele id&#39;s met het aantal oorspronkelijke gehashte e-mailadressen.

   De segmenten moeten binnen 24 uur in DSP beschikbaar zijn. Nadat DSP de segmentgegevens ontvangt, moet het aantal gebruikers binnen negen (9) uur zichtbaar zijn. Voor informatie over aanvaardbare identiteitskaart vertaaltarieven en waarom de segmenttellingen kunnen variëren, zie &quot;[ Varianties van Gegevens tussen E-mail IDs en Universele IDs ](#universal-ids-data-variances).&quot;

Segmenten worden elke 24 uur vernieuwd.

## Problemen oplossen

Om vertaaltarief en gebruikerstellingskwesties problemen op te lossen, zie &quot;[ Steun voor het Activeren van Universal IDs ](/help/dsp/audiences/universal-ids.md).&quot;

Neem contact op met het accountteam van de Adobe of `adcloud-support@adobe.com` om problemen met de conversieprocedure op te lossen.

>[!MORELIKETHIS]
>
>* [ Ongeveer de Bronnen van het Publiek van de Eerste Partij ](/help/dsp/audiences/sources/source-about.md)
>* [ beheert de Bronnen van het Publiek om Universele Soorten van identiteitskaart ](source-manage.md) te activeren
>* [ zet Gebruiker IDs van  [!DNL Adobe Real-Time CDP]  in Universal IDs ](/help/dsp/audiences/sources/source-adobe-rtcdp.md) om
>* [ zet Gebruiker IDs van  [!DNL Tealium]  in Universal IDs ](/help/dsp/audiences/sources/source-tealium.md) om
>* [ Ongeveer het Beheer van het Publiek ](/help/dsp/audiences/audience-about.md)
