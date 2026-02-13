---
title: Een herbruikbaar publiek maken met Generative AI
description: Leer hoe u herbruikbare soorten publiek kunt maken in Adobe Advertising DSP met behulp van de AI-ondersteunde publieksagent. Beschrijf uw doelpubliek in natuurlijk-taalherinneringen; de agent stelt derdesegmenten voor en bouwt publieksuitdrukkingen voor gebruik als doelstellingen of uitsluitingen.
feature: DSP Audiences
hidefromtoc: true
hide: true
source-git-commit: 86053178969de362dda0c135ff8c85b9ec9f674e
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 0%

---

# Een herbruikbaar publiek maken met Generative AI

*eigenschap van Beta*

*Vragen in slechts de Engelse taal*

<!-- I thought it was all segment types? -->

<!-- Redo the legacy file to include the new info. It's probably cleanest to keep it as two separate procedures (gen AI and manually) rather than one big, long procedure. -->

Gebruik de AI-ondersteunde publieksagent om nieuwe, herbruikbare soorten publiek te maken met behulp van alle segmenten van derden die voor u beschikbaar zijn, volgens de aangegeven vereisten. U kunt uw publiek gebruiken als doelen of uitsluitingen voor meerdere plaatsen.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>Deze functie bevindt zich in de bètamodus en kan worden gewijzigd. Zorg ervoor dat de gegenereerde publieksexpressie het gewenste publiek vertegenwoordigt voordat u het publiek maakt en deze voor uw plaatsingen gebruikt.

1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]** .

1. Klik boven de gegevenstabel op **[!UICONTROL Create]** .

1. Voer een uniek **[!UICONTROL Audience Name]** in.

1. (Optioneel) Schakel de optie uit die u wilt **[!UICONTROL Share with all advertisers in my account]** gebruiken.

   Wanneer u een publiek deelt, wordt het publiek beschikbaar als doel of uitsluiting voor alle adverteerders binnen de account. De afzonderlijke segmenten in het publiek zijn echter alleen beschikbaar voor gebruikers waarop de segmenten worden gedeeld.

1. Klik op **[!UICONTROL Save]**.

1. Het publiek opbouwen:

   Voor gebruikers met bètamachtigingen is de optie AI de standaardinstelling. Om [ het publiek te assembleren zelf ](/help/dsp/audiences/reusable-audience-create.md), klik de &quot;Schakelaar aan handwijze&quot;knoop bij de bodem.

   1. Voer een of meer aanwijzingen in om de publiekskenmerken te beschrijven die u wilt opnemen en uitsluiten. Om elke herinnering voor te leggen, klik ![ voorlegt herinnering ](/help/dsp/assets/submit-prompt.png " voorlegt herinnering ").

      Voor meer informatie, zie &quot;[ het Schrijven van Herinneringen ](#writing-prompts)&quot; en &quot;[ Beste praktijken voor het Creëren van een Korf van de Publiek ](#audience-brief-best-practices).&quot;

      Aangezien de AI agent relevante segmenten vindt, leidt het tot een publieksuitdrukking die op uw criteria wordt gebaseerd. Het vraagt ook om uw goedkeuring alvorens passende segmenten te zoeken om het publiek samen te stellen.

      U kunt optioneel het verzoek negeren en aanvullende publiekscriteria blijven opgeven.

   1. Wanneer de AI agent een publieksuitdrukking voorstelt die adequaat uw publiek beschrijft, vertel de AI agent om met het assembleren van het publiek te werk te gaan.

      U kunt &quot;te werk gaan&quot;, &quot;OK&quot;, &quot;OK&quot;, &quot;ja&quot; of een ander vergelijkbaar woord invoeren.

1. (Indien nodig) Geef aanvullende criteria op. Wanneer de AI agent een publieksuitdrukking voorstelt die aan elk van uw criteria voldoet, vertel de AI agent om met het assembleren van het publiek te werk te gaan.

1. Wanneer u tevreden bent met het samengestelde publiek, klikt u op **[!UICONTROL Create]** om het opgegeven publiek te maken.

   >[!NOTE]
   >
   >U kunt het publiek later niet uitgeven gebruikend de agent AI. In plaats daarvan, [ geef manueel de publieksuitdrukking uit ](/help/dsp/audiences/reusable-audience-edit.md).

## Schrijfverzoeken {#writing-prompts}

### Wat zou een herinnering moeten omvatten?

* Gebruik duidelijke, beschrijvende taal om het doelpubliek te beschrijven.

  Over het algemeen zijn aanwijzingen niet hoofdlettergevoelig en is leestekens alleen nodig voor meer duidelijkheid.

* Ben specifiek en verstrek details over alle publiekskenmerken die u en om het even welke eigenschappen wilt omvatten die u specifiek wilt uitsluiten. Hoe meer details u verstrekt, des te groter de kans dat u de resultaten zult krijgen die aan uw behoeften voldoen.

* Identificeer plaatsen, apparatentypes, en gegevensleveranciers om te omvatten of uit te sluiten.

* U kunt desgewenst meer informatie verstrekken om uw criteria en de gegenereerde publieksexpressie te verfijnen voordat u het publiek opslaat.

* Leer over het veroorzaken door experimenteren.

  De publieksagent slaat niet automatisch een gegenereerde publieksexpressie op als een publiek. U kunt een publiek alleen opslaan door op de knop [!UICONTROL Create] te klikken. Deze knop bevindt zich buiten het gebied met de vraag, zodat u alle wijzigingen ongedaan kunt maken die u niet wilt behouden.

Zie &quot;[ Beste praktijken voor het Creëren van een Kort van het Publiek ](#audience-brief-best-practices)&quot;voor verdere manieren om herinneringen voor publiek te optimaliseren.

<!-- I think these are happening later:

DSP uses "smart" defaults based on the user's previous audiences (all user-created audiences or only ones created via AI prompting?)

you can use a predefined prompt (fill in the blanks, and some fields might have selectors where you can choose values)

Over time, DSP XXXX defaults [clarify this]

 onsider starting by asking for a general template, which contains placeholder values that you can replace with your desired values. The default template is something like "Create a xxx with NNN xxx."

you can give thumbs up or down to [what exactly?]. Verify what info is carried over from session to session and what starts from scratch.

-->

### Wat kunt u niet in een herinnering omvatten?

* Verwijzingen naar bestaande publieksuitdrukkingen.

* Tekst in talen behalve Engels.

### Voorbeelden van antwoorden van AI-agents en hoe ze moeten reageren

Wanneer de AI agent een reactie van u nodig heeft, kunt u antwoorden gebruikend sleutelwoorden in het verzoek of gebruikend gemeenschappelijke termijnen die gelijkwaardig zijn.

#### Antwoord van AI-agent waarmee u een vraag stelt

`If you are okay with the proposed expression, I can start searching third party segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

Uw bevestigende antwoorden: &quot;ga verder,&quot; &quot;oké&quot;, &quot;ok&quot;, &quot;ja&quot; of een ander vergelijkbaar woord

U kunt het verzoek ook negeren en aanvullende publiekscriteria blijven opgeven.

#### Antwoord van de AI-agent waarin u wordt gevraagd uit meerdere opties te kiezen

```
Would you like to:
1) Proceed with this expression,
2) Get maximum reach alternatives, or
3) Modify the expression manually?
```

Uw antwoord: `1`, `proceed`, `2`, `maximum reach` enzovoort.

U kunt het verzoek ook negeren en aanvullende publiekscriteria blijven opgeven.

## Beste praktijken voor het Creëren van een Kort van het Publiek {#audience-brief-best-practices}

Een publieksnotatie is een strategische beschrijving die het doelpubliek voor een campagne definieert. Een goed opgemaakte samenvatting helpt de DSP-publieksagent de meest relevante segmenten te identificeren om uw doelgroep samen te stellen.

### Essentiële componenten van een effectief publiek

#### Kenmerken publiek

Neem zoveel mogelijk kenmerktypen op uit de volgende lijst in uw overzicht. Wees specifiek over kenmerken die u wilt uitsluiten.

<!-- What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **Demographics**

  Omvat kenmerken zoals leeftijd, geslacht, huwelijkse staat, samenstelling van het huishouden (gezinsgrootte, aanwezigheid van kinderen, multi-generationele huishoudens).

* **Sociaal-economische Indicatoren**

  Vormt financiële capaciteit door middel van inkomensgroepen (HHI), onderwijsniveau, beroep/functie-titels, arbeidsstatus en de status van huiseigenaar.

* **Geografische Parameters**

  Definieert het bereik van de locatie, inclusief land/landen, regio (EMEA, APAC, NA), bevolkingsdichtheid (stedelijk/voorstedelijk/landelijk).

* **Belangen &amp; Affinities**

  Identificeert passies en voorkeur zoals hobby&#39;s (sport, kunst, buitenactiviteiten), media consumptiepatronen, merkaffiniteiten, en levensstijlactiviteiten (reizen, dineren, entertainment).

* **Psychographics**

  Hiermee legt u denkbeelden en waarden vast, waaronder aspiraties (statuszoeken, zelfverbetering), kernwaarden (duurzaamheid, innovatie, traditie), persoonlijkheidskenmerken (risiconemers, vroege adopters) en aankoopmotieven.

* **Signalen van het Gedrag**

  Waarneembare acties, zoals gedrag bij aankopen (frequentie van winkelen, kanaalvoorkeuren, merkloyaliteit), online gedrag (websitebezoeken, betrokkenheid bij inhoud, sociale media-activiteit) en offlinegedrag (bezoeken aan winkels, deelname aan evenementen, lidmaatschap).

* **In-Market Intent**

  Identificeert koopbereidheid door product/de dienstcategorieën die worden onderzocht, aankoopchronologie (onmiddellijk, op korte termijn, op lange termijn), en relevante levensgebeurtenissen die aankoopbesluiten teweegbrengen.

* **Stadium van het Leven**

  Actuele fase van het begrip, met inbegrip van de loopbaanfase (student, instapniveau, middelbare carrière, uitvoerend, gepensioneerd), de gezinsfase (nieuwigheden, nieuwe ouders, lege nesters) en belangrijke overgangen in het leven.

### Voorbeeld van een goedgestructureerde hoornvlieg voor een prospectieve campagne

Hieronder ziet u een voorbeeld van een uitgebreide publieksnotatie voor een campagne om het bewustzijn te vergroten en te experimenteren voor een premiumpakket-abonnementsservice:

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [ dupliceer een Herbruikbaar publiek ](/help/dsp/audiences/reusable-audience-duplicate.md)
>* [ geef een Herbruikbare Publiek ](/help/dsp/audiences/reusable-audience-edit.md) uit
>* [ Details van de Mening over een Herbruikbaar publiek ](/help/dsp/audiences/reusable-audience-view-details.md)
>* [ deel een Herbruikbare Publiek ](/help/dsp/audiences/reusable-audience-share.md)
>* [ de Uitvoer een Herbruikbaar publiek ](/help/dsp/audiences/reusable-audience-export.md)
>* [ Kopieer de Sleutel van het Segment voor een Herbruikbaar publiek aan het Klembord ](/help/dsp/audiences/reusable-audience-clipboard.md)
>* [ Schrap een Herbruikbaar publiek ](/help/dsp/audiences/reusable-audience-delete.md)
