---
title: Aangepaste doelen
description: Leer over douanedoelstellingen om uw succesgebeurtenissen te bepalen in pakketten die voor laagste CPA of hoogste ROAS worden geoptimaliseerd.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
source-git-commit: 290eea50fe3c52a534ad6ab4fcf6d857b13230aa
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 0%

---

# Aangepaste doelen

De doelstellingen van de douane bepalen de succesgebeurtenissen die een adverteerder vereist om zijn bedrijfsdoelstellingen te ontmoeten. Elk pakket dat het optimalisatiedoel gebruikt &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] of &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; moet een aangepast doel bevatten om het algemene optimalisatiedoel te helpen bereiken. U kunt aangepaste doelen maken als *doelstellingen* in [!DNL Advertising Search, Social, & Commerce]. De naam van elke doelstelling voor DSP moet worden voorafgegaan door &quot;ADSP_&quot;.

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Elk douanedoel (doelstelling) bestaat uit één of meerdere omzettingsmetriek en de relatieve gewichten van die metriek. De beschikbare omzettingsmetriek omvat alle metriek die gebruikend de Adobe Advertising omzettingspixel en door Adobe Analytics wordt gevolgd. Alleen niet-mobiele gewichten worden beschouwd als DSP aangepaste doelen, maar worden gebruikt voor alle advertentietypen.

Stel dat drie conversiemetriek bijvoorbeeld relevant zijn voor een specifiek pakket in een van uw campagnes: &quot;PDF downloaden&quot; met een waarde van 20 USD, &quot;E-mailaanmelding&quot; met een waarde van 30 USD en &quot;Bestelbevestiging&quot; met een waarde van 40 USD. Als u gewicht wilt geven volgens de eenmalige monetaire waarde van de actie van de klant, dan zouden de relatieve gewichten van de metriek 1, 1.5, en 2 zijn.

Eenmaal [een aangepast doel maken](#custom-goal-create), kunt u [toewijzen aan een pakket](/help/dsp/campaign-management/packages/package-settings.md) voor rapportage en algoritmische optimalisatie met Adobe Sensei.

De aanbevelingen van het gewicht worden automatisch geproduceerd voor DSP-toegeschreven metriek in doelstellingen, en kunnen alle gewichtsaanbevelingen met één klik toepassen. Alle gewichtswijzigingen in doelstellingen die vooraf zijn vastgesteld met &quot;ADSP_&quot; worden binnen twee dagen op algoritmische wijze in DSP toegepast. Raadpleeg voor meer informatie de aanbevelingen in het hoofdstuk Optimalisatiegids over &quot;(Beta) New Objectives&quot;, dat beschikbaar is in Search, Social &amp; Commerce.

## Een aangepast doel maken {#custom-goal-create}

Als u een aangepast doel wilt maken, moet de DSP-account zijn gekoppeld aan een [!DNL Search, Social, & Commerce] account met dezelfde Adobe Experience Cloud-organisatie-id, van binnen de [!DNL Search, Social, & Commerce] clientinstellingen. Als uw DSP niet is gekoppeld aan een [!DNL Search, Social, & Commerce] -account, neemt u contact op met het accountteam van de Adobe.

1. Aanmelden bij [!DNL Advertising Search, Social, & Commerce] at (gebruikers in Noord-Amerika) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) of (alle andere gebruikers) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. Zorg ervoor dat de meetgegevens die u in uw doel wilt opnemen, zijn bijgehouden, beschikbaar zijn in het product en een weergavenaam bevatten:

   1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. Bepaal de plaats van metrisch, en zorg ervoor dat **[!UICONTROL Show in UI and Reports]** wordt toegelaten voor metrisch.

      >[!NOTE]
      >
      >* [!DNL Analytics] aangepaste gebeurtenissen volgen deze naamgevingsconventie: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Voorbeeld: `custom_event_16_examplersid`

   1. Als metrisch geen waarde in metrisch heeft **[!UICONTROL Display Name]** , klikt u in de cel, voert u de weergavenaam in en klikt u op **[!UICONTROL Apply].**

1. Het aangepaste doel maken als een *doel*:

   1. Klik in het hoofdmenu op **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. Klik op de werkbalk op ![Maken](/help/dsp/assets/create-search-ui.png "Maken").

   1. Voer de objectieve instellingen in, inclusief de bijbehorende metriek en hun relatieve numerieke gewichten voor niet-mobiele apparaten, en sla het doel op. Overweeg het volgende:

      * Voor doelstellingen die voor pakketten Advertising DSP worden gebruikt, moet de objectieve naam met &quot;ADSP_&quot;zoals &quot;ADSP_Registrations worden vooraf bepaald.&quot; Het voorvoegsel is niet hoofdlettergevoelig.

      * Alleen metriek opnemen die aan DSP worden toegewezen. Metrische gegevens die worden toegewezen aan Search, Social en Commerce of aan een ander advertentienetwerk, worden genegeerd.

      * Minstens één metrisch moet metrisch type hebben *[!UICONTROL Goal]*.

      * DSP gebruikt de niet-mobiele dikten voor alle advertenties. Alle opgegeven mobiele dikten worden genegeerd.

      >[!NOTE]
      >
      >* [!DNL Analytics] aangepaste gebeurtenissen volgen deze naamgevingsconventie: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Voorbeeld: `custom_event_16_examplersid`
      >* [!DNL Analytics] de afmetingen en de segmenten zijn niet beschikbaar voor Adobe Advertising optimalisering.

      >[!TIP]
      >
      >Voor optimale prestaties, moeten de gecombineerde metriek in het douanedoel (doelstelling) minstens tien omzettingen per dag in totaal omvatten. Als dat niet het geval is, kunt u het beste aanvullende ondersteunende conversiemetriek, zoals productpagina&#39;s of het starten van de toepassing, aan het doel toevoegen. Zie [Beste praktijken voor het Bouwen van een Doel van de Douane](#custom-goal-best-practices) voor richtsnoeren.

In de DSP pakketinstellingen voor pakketten die het optimalisatiedoel gebruiken &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] of &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)],&quot; wordt de objectieve naam nu opgenomen in de [!UICONTROL Custom Goals] lijst. Wanneer u het doel selecteert als het aangepaste doel voor een pakket, wordt het [!UICONTROL Conversion Metric] de lijst bevat alle streefcijfers voor het doel .

## Beste praktijken voor het Bouwen van een Doel van de Douane {#custom-goal-best-practices}

### Aangepaste doelen met één metrisch

De volgende voorbeelden tonen hoe u doelstellingen zou kunnen vormen die één enkele metrische omzetting richten.

#### Voorbeeld van een campagne met de opdracht &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;Optimalisatiedoelstelling

Als het doel van uw campagne inkomsten is ([!UICONTROL Highest Return on Ad Spend (ROAS)]), en de opbrengst van alle apparatentypes is even belangrijk voor u, dan omvat &quot;[!UICONTROL Revenue]&quot; metrisch met een niet-mobiel gewicht van 1 (1); het mobiele gewicht wordt genegeerd. Selecteer het metrische type *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Een niet-mobiel gewicht van 1 (1) is gelijk aan de waarde 1 (1) voor elke $1 aan opbrengst die voor vertoningsadvertenties op om het even welk apparaat wordt gevolgd. Een conversie van € 250 met een niet-mobiel gewicht van 1 (1) wordt bijvoorbeeld gerapporteerd als $250 voor conversies. Als de omzettingsmetrische waarde een niet-mobiel gewicht van 0.5 wordt toegewezen, dan wordt $250 omzetting gemeld als $125 in Adobe Advertising ($250 Omzetting * 0.5 [!UICONTROL Non-mobile Weight] = $ 125).

#### Voorbeeld van een campagne met de opdracht &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;Optimalisatiedoelstelling

Als uw campagnedoel de laagste kosten per verwerving (CPA) is en het slechts één succesgebeurtenis (zoals &quot;Toepassing vereist voorlegt&quot;) vereist, dan omvat dat metrisch en specificeert metrisch type zoals *[!UICONTROL Goal]*. De beste manier is om het niet-mobiele gewicht in te stellen als één (1); het mobiele gewicht wordt genegeerd.

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Een niet-mobiel gewicht van één (1) is gelijk aan een waarde van één (1) voor elke omzetting die voor vertoningsadvertenties op om het even welk apparaat wordt gevolgd. Als bijvoorbeeld 10 omzettingen van Toepassing verzenden worden bijgehouden, worden 10 omzettingen van Toepassing verzenden gerapporteerd. Als aan de omzettingsmaatstaf echter een niet-mobiel gewicht van 0,5 wordt toegekend, worden de 10 omzettingen gerapporteerd als vijf (5) in Adobe Advertising (10 Omzettingen * 0,5 [!UICONTROL Non-mobile Weight] = 5).

### Aangepaste doelen met meerdere meetwaarden

Er zijn twee scenario&#39;s waarin u veelvoudige metriek in een douanedoel zou gebruiken:

* Uw campagnedoel heeft meerdere succesgebeurtenissen. U maakt bijvoorbeeld reclame voor meer dan één onsite actie (downloaden van PDF, contact met ons en aanmelden via e-mail) en al deze acties dragen bij aan uw CPA-doel. Als het doel de drie verschillende meeteenheden omvat, elk met een (1) niet-mobiel gewicht, dan [!DNL Adobe Sensei] het algoritme behandelt elk van de metriek en de types van gebruikersapparaat met gelijk belang. Als de verschillende meetwaarden verschillende kosten of belang hebben, dan past u hun relatieve gewichten dienovereenkomstig aan.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* De enige metrische conversie in uw douanedoel bereikt niet het minimum van 10 omzettingen per dag die voor geoptimaliseerde prestaties wordt vereist. Dit kan gebeuren door minimale dagelijkse pakketuitgaven of een beperkt aantal natuurlijke omzettingen. Het toevoegen van extra ondersteunende metriek aan het douanedoel kan u helpen de drempel 10-omzettingen-per-dag bereiken. Tien ondersteunende gebeurtenissen kunnen een pakket helpen aan de drempel van 10/dag te voldoen, zelfs als elk van hun gewichten onder één (1) is. Maar misschien hoeft u niet zoveel gebeurtenissen toe te voegen.

  Wanneer u ondersteunende metriek aan een douanedoel toevoegt, gewicht hen volgens hun relatieve belang aan de belangrijkste succesgebeurtenis, en houd in mening de hoeveelheid gegevenspunten. Op deze manier kan het Adobe Sensei-algoritme meerdere metingen in evenwicht brengen en optimaliseren naar uw doel.

  De volgende voorbeelddoelstelling omvat drie metriek, elk met een verschillend niet-mobiel gewicht: Toepassing dient = 1, het Begin van de Toepassing = 0.1, en Advertiser het Landing Pagina = 0.01 in. Dit betekent dat elke omzetting van de Toepassing voorlegt de zelfde waarde aan uw zaken zoals gemiddeld 10 omzettingen van het Begin van de Toepassing en 100 Advertiser het Landing van de Pagina omzettingen heeft.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Als u in plaats daarvan de Landing Page-bezoeken gelijkelijk aan Application Submits gewogen hebt, kan het natuurlijk hogere aantal landingspagina-bezoeken uw doel overweldigen en de pagina-bezoeken afschuinen.<!--reword-->

>[!MORELIKETHIS]
>
>* [Optimalisatiedoelstellingen en hoe deze te gebruiken](optimization-goals.md)
>* [Pakketinstellingen](/help/dsp/campaign-management/packages/package-settings.md)
> * [Hoe DSP uw campagnes optimaliseert](optimization-how-dsp-optimizes-campaigns.md)
