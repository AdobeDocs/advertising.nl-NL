---
title: Aangepaste doelen
description: Leer over douanedoelstellingen om uw succesgebeurtenissen te bepalen in pakketten die voor laagste CPA of hoogste ROAS worden geoptimaliseerd.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 0%

---

# Aangepaste doelen

De doelstellingen van de douane bepalen de succesgebeurtenissen die een adverteerder vereist om zijn bedrijfsdoelstellingen te ontmoeten. Elk pakket dat het optimalisatiedoel &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] of &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;gebruikt moet een douanedoel omvatten helpen het algemene optimalisatiedoel bereiken. U kunt douanedoelstellingen als *doelstellingen* in [!DNL Advertising Search, Social, & Commerce] tot stand brengen. De naam van elke doelstelling voor DSP moet vooraf worden bepaald met &quot;ADSP_&quot;.

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Elk douanedoel (doelstelling) bestaat uit één of meerdere omzettingsmetriek en de relatieve gewichten van die metriek. De beschikbare omzettingsmetriek omvat alle metriek die gebruikend de Adobe Advertising omzettingspixel en door Adobe Analytics wordt gevolgd. Alleen niet-mobiele gewichten worden in overweging genomen bij aangepaste DSP-doelen, maar worden gebruikt voor alle advertentietypen.

Stel dat drie conversiemetriek bijvoorbeeld relevant zijn voor een specifiek pakket in een van uw campagnes: &quot;PDF Download&quot; gewaardeerd op 20 USD, &quot;Email Signup&quot; gewaardeerd op 30 USD en &quot;Order Confirmation&quot; gewaardeerd op 40 USD. Als u gewicht wilt geven volgens de eenmalige monetaire waarde van de actie van de klant, dan zouden de relatieve gewichten van de metriek 1, 1.5, en 2 zijn.

Zodra u [&#x200B; een douanedoel &#x200B;](#custom-goal-create) creeert, kunt u [&#x200B; het aan een pakket &#x200B;](/help/dsp/campaign-management/packages/package-settings.md) voor het melden en algoritmische optimalisering toewijzen gebruikend Adobe Sensei.

De aanbevelingen van het gewicht worden automatisch geproduceerd voor DSP-toegeschreven metriek in doelstellingen, en kunnen alle gewichtsaanbevelingen met één klik toepassen. Alle gewichtswijzigingen in doelstellingen die vooraf zijn vastgesteld met &quot;ADSP_&quot; worden binnen twee dagen algoritmisch toegepast in DSP. Zie het hoofdstuk over &quot;Doelstellingen&quot; in het hoofdstuk over zoekopdrachten, sociale zaken en Commerce voor meer informatie over het gewicht.

## Een aangepast doel maken {#custom-goal-create}

Als u een aangepast doel wilt maken, moet de DSP-account vanuit de [!DNL Search, Social, & Commerce] -client-instellingen zijn gekoppeld aan een [!DNL Search, Social, & Commerce] -account met dezelfde Adobe Experience Cloud-organisatie-id. Als uw DSP-account niet is gekoppeld aan een [!DNL Search, Social, & Commerce] -account, neemt u contact op met uw Adobe-accountteam.

1. [&#x200B; Teken binnen aan het Onderzoek van Advertising, Sociale, &amp; Commerce &#x200B;](/help/search-social-commerce/getting-started/sign-in.md){target="_blank"}.

1. Zorg ervoor dat de meetgegevens die u in uw doel wilt opnemen, zijn bijgehouden, beschikbaar zijn in het product en een weergavenaam bevatten:

   1. Klik in het hoofdmenu op **[!UICONTROL Goals]** > **[!UICONTROL Conversions]** .

      De weergave Conversies wordt geopend in een nieuw browsertabblad.

   1. Bepaal de plaats van metrisch, en zorg ervoor dat **[!UICONTROL Show in UI and Reports]** voor metrisch wordt toegelaten.

      >[!NOTE]
      >
      >* [!DNL Analytics] aangepaste gebeurtenissen volgen deze naamgevingsconventie: `custom_event_[*event #*]_[*Analytics report suite ID*]` . Voorbeeld: `custom_event_16_examplersid`

   1. Als metrisch geen waarde in de **[!UICONTROL Display Name]** kolom heeft, dan klik in de cel, ga de vertoningsnaam in, en klik **[!UICONTROL Apply].**

1. [&#x200B; creeer het douanedoel als *doelstelling*](/help/search-social-commerce/new-ui/goals/objectives/objective-create.md){target="_blank"}. Overweeg het volgende:

   * Voor doelstellingen die voor pakketten Advertising DSP worden gebruikt, moet de objectieve naam met &quot;ADSP_&quot;zoals &quot;ADSP_Registrations worden vooraf bepaald.&quot; De prefix is niet hoofdlettergevoelig.

   * Alleen metriek opnemen die aan DSP worden toegewezen. Metrische gegevens die worden toegewezen aan Search, Social en Commerce of aan een ander advertentienetwerk, worden genegeerd.

   * Ten minste één metrische waarde moet het metrische type *[!UICONTROL Goal]* hebben.

   * DSP gebruikt de niet-mobiele gewichten voor alle advertenties. Alle opgegeven mobiele dikten worden genegeerd.

   >[!NOTE]
   >
   >* [!DNL Analytics] aangepaste gebeurtenissen volgen deze naamgevingsconventie: `custom_event_[*event #*]_[*Analytics report suite ID*]` . Voorbeeld: `custom_event_16_examplersid`
   >* [!DNL Analytics] -afmetingen en -segmenten zijn niet beschikbaar voor Adobe Advertising-optimalisatie.

   >[!TIP]
   >
   >Voor optimale prestaties, moeten de gecombineerde metriek in het douanedoel (doelstelling) minstens tien omzettingen per dag in totaal omvatten. Als dat niet het geval is, kunt u het beste aanvullende ondersteunende conversiemetriek, zoals productpagina&#39;s of het starten van de toepassing, aan het doel toevoegen. Zie [&#x200B; Beste praktijken voor de Bouw van een Doel van de Douane &#x200B;](#custom-goal-best-practices) voor richtlijnen.

In de het pakketmontages van DSP voor pakketten die het optimalisatiedoel &quot; [!UICONTROL Highest Return on Ad Spend (ROAS)"] of &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)] gebruiken,&quot;is de objectieve naam nu inbegrepen in de [!UICONTROL Custom Goals] lijst. Wanneer u het doel selecteert als het aangepaste doel voor een pakket, bevat de lijst van [!UICONTROL Conversion Metric] alle maatstaven voor het doel.

## Beste praktijken voor het Bouwen van een Doel van de Douane {#custom-goal-best-practices}

### Aangepaste doelen met één metrisch

De volgende voorbeelden tonen hoe u doelstellingen zou kunnen vormen die één enkele metrische omzetting richten.

#### Voorbeeld voor een Campagne met het &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;Doel van de Optimalisering

Als uw campagnedoel opbrengst ([!UICONTROL Highest Return on Ad Spend (ROAS)]) is, en de opbrengst van alle apparatentypes is even belangrijk voor u, dan omvat &quot;[!UICONTROL Revenue]&quot;metrisch met een niet-mobiel gewicht van één (1); het mobiele gewicht wordt genegeerd. Selecteer het metrische type *[!UICONTROL Goal]* .

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Een niet-mobiel gewicht van 1 (1) is gelijk aan de waarde 1 (1) voor elke $1 aan opbrengst die voor vertoningsadvertenties op om het even welk apparaat wordt gevolgd. Een conversie van € 250 met een niet-mobiel gewicht van 1 (1) wordt bijvoorbeeld gerapporteerd als $250 voor conversies. Als de omzettingsmetrische waarde een niet-mobiel gewicht van 0.5 wordt toegewezen, dan wordt $250 omzetting gemeld als $125 in Adobe Advertising ($250 Omzetting * 0.5 [!UICONTROL Non-mobile Weight] = $125).

#### Voorbeeld voor een Campagne met het &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;Doel van de Optimalisering

Als uw campagnedoel de laagste kosten per aanschaf (CPA) is en het slechts één succesgebeurtenis (zoals &quot;Toepassing voorlegt&quot;) vereist, dan omvat die één metrisch en specificeer metrisch type als *[!UICONTROL Goal]*. De beste manier is om het niet-mobiele gewicht in te stellen als één (1); het mobiele gewicht wordt genegeerd.

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Een niet-mobiel gewicht van één (1) is gelijk aan een waarde van één (1) voor elke omzetting die voor vertoningsadvertenties op om het even welk apparaat wordt gevolgd. Als bijvoorbeeld 10 omzettingen van Toepassing verzenden worden bijgehouden, worden 10 omzettingen van Toepassing verzenden gerapporteerd. Als de omzettingsmetrische waarde echter een niet-mobiel gewicht van 0,5 krijgt, worden de 10 omzettingen gerapporteerd als vijf (5) in Adobe Advertising (10 Omzettingen * 0,5 [!UICONTROL Non-mobile Weight] = 5).

### Aangepaste doelen met meerdere meetwaarden

Er zijn twee scenario&#39;s waarin u veelvoudige metriek in een douanedoel zou gebruiken:

* Uw campagnedoel heeft meerdere succesgebeurtenissen. U maakt bijvoorbeeld reclame voor meer dan één onsite actie (PDF Download, Contact met ons opnemen en Aanmelden via e-mail) en al deze acties dragen bij aan uw CPA-doel. Als het doel de drie verschillende metriek omvat, elk met niet-mobiele gewichten van één (1), dan behandelt het [!DNL Adobe Sensei] algoritme elk van de metriek en de types van gebruikersapparaten met gelijk belang. Als de verschillende meetwaarden verschillende kosten of belang hebben, dan past u hun relatieve gewichten dienovereenkomstig aan.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* De enige metrische conversie in uw douanedoel bereikt niet het minimum van 10 omzettingen per dag die voor geoptimaliseerde prestaties wordt vereist. Dit kan gebeuren door minimale dagelijkse pakketuitgaven of een beperkt aantal natuurlijke omzettingen. Het toevoegen van extra ondersteunende metriek aan het douanedoel kan u helpen de drempel 10-omzettingen-per-dag bereiken. Tien ondersteunende gebeurtenissen kunnen een pakket helpen aan de drempel van 10/dag te voldoen, zelfs als elk van hun gewichten onder één (1) is. Maar misschien hoeft u niet zoveel gebeurtenissen toe te voegen.

  Wanneer u ondersteunende metriek aan een douanedoel toevoegt, gewicht hen volgens hun relatieve belang aan de belangrijkste succesgebeurtenis, en houd in mening de hoeveelheid gegevenspunten. Op deze manier kan het Adobe Sensei-algoritme meerdere metingen in evenwicht brengen en optimaliseren naar uw doel.

  De volgende voorbeelddoelstelling omvat drie metriek, elk met een verschillend niet-mobiel gewicht: Toepassing dient = 1, het Begin van de Toepassing = 0.1, en Advertiser het Landing Pagina = 0.01 in. Dit betekent dat elke omzetting van de Toepassing voorlegt de zelfde waarde aan uw zaken zoals gemiddeld 10 omzettingen van het Begin van de Toepassing en 100 Advertiser het Landing van de Pagina omzettingen heeft.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Als, in plaats daarvan, u de bezoeken van de Pagina van het Aanlanden evenzeer aan de Verzending van de Toepassing gewogen, dan zou de natuurlijk hogere hoeveelheid landende paginabezoeken uw doel kunnen overweldigen en aan het landen paginabezoeken schuintrekken.<!--reword-->

>[!MORELIKETHIS]
>
>* [&#x200B; Doelstellingen van de optimalisering en hoe te om hen te gebruiken &#x200B;](optimization-goals.md)
>* [&#x200B; de Montages van het Pakket &#x200B;](/help/dsp/campaign-management/packages/package-settings.md)
> * [&#x200B; hoe DSP Uw campagnes optimaliseert &#x200B;](optimization-how-dsp-optimizes-campaigns.md)
