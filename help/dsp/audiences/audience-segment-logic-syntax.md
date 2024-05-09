---
title: Syntaxis voor Audience Segment Logic
description: Verwijs naar de syntaxis u kunt gebruiken om de logica voor publiekssegmenten te bepalen.
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Syntaxis voor Audience Segment Logic

Wanneer u herbruikbare soorten publiek maakt, kunt u de segmentlogica handmatig definiëren met alfanumerieke segment-id&#39;s (sleutels) en de volgende syntaxis:

* () om een groep aan te geven
* `||` for [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; voor [!DNL AND]
* ! for [!DNL NOT] (uitsluiten)

>[!NOTE]
>
>* Alle gespecificeerde segmentgroepen zijn inbegrepen tenzij zij door worden voorafgegaan ! (exclusief deze).
>* U kunt [zoek segmentidentiteitskaart voor een publiek](reusable-audience-clipboard.md) van [!UICONTROL Audiences] > [!UICONTROL All audiences].

De volgende logica:

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

means (in normale Engelse taal)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>In plaatsingsmontages, kunt u opgeslagen publiek of als publiek gebruiken om uitdrukkelijk te richten of als afzonderlijke publiek om van het richten uit te sluiten. Zorg ervoor uw segmentlogica het doel voor het gebruiken van het publiek weerspiegelt.

>[!MORELIKETHIS]
>
>* [Kopieer de segmentsleutel voor een herbruikbaar publiek naar het klembord](reusable-audience-clipboard.md)
>* [Informatie over Audience Management](audience-about.md)
>* [Een herbruikbaar publiek maken](reusable-audience-create.md)
>* [Instellingen voor publiek](audience-settings.md)
>* [Beschikbare gegevensleveranciers van derden](third-party-data-providers.md)
