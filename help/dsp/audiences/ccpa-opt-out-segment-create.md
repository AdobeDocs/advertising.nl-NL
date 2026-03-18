---
title: Een CCPA-opt-out-of-sales-segment maken en implementeren
description: Leer hoe u een segment maakt en implementeert om gebruikers-id's te traceren op basis van verzoeken van consumenten om te weigeren een product te verkopen.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 7cf17457ba777d2dfe9fc1607f9891a340da9031
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Een CCPA-opt-out-of-sales-segment maken en implementeren

U kunt een segment tot stand brengen om gebruikers IDs van consument van uit-verkoopverzoeken op uw website te volgen, volgens de Wet van de Privacy van de consument van Californië (CCPA). De gebruikers blijven in opt-out van CCPA-segmenten voor onbepaalde tijd.

Zodra de segmentpixel-tag is geïmplementeerd, begint Adobe Advertising namens de adverteerder een pool met id&#39;s te verzamelen.

>[!NOTE]
>
>* Voor informatie over hoe te om opting-uit-van-verkoop CCPA verzoeken aan Adobe Advertising mee te delen gebruikend Adobe Experience Platform Privacy Service API, zie [&#x200B; https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html &#x200B;](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* Om gebruikers te volgen die webpagina&#39;s voor doeleinden bezoeken die niet met het volgen van opting-uit-van-verkoop gebeurtenissen CCPA verwant zijn, evenals gebruikers die aan advertenties van Desktop, mobiel, en apparaten CTV worden blootgesteld, creeer a [&#x200B; douanesegment &#x200B;](/help/dsp/audiences/custom-segment-create.md).

1. Maak het segment:

   1. In het belangrijkste menu, klik **Soorten publiek > Segmenten**.

   1. Klik boven de gegevenstabel op **[!UICONTROL Create]** .

   1. Voer een uniek **[!UICONTROL Segment Name]** in.

      Aanbevolen segmentnaam: &quot;&lt; *Uw Naam Advertiser*> - CCPA uit Verkoop&quot;(zoals &quot;Acme - CCPA uit Verkoop&quot;)

   1. Selecteer [!UICONTROL Segment Type] voor **[!UICONTROL CCPA Opt-out of sale]** .

   1. Klik op **[!UICONTROL Save]**.

1. Kopieer en implementeer een pixeltag om het segment bij te houden:

   1. Ga terug naar **[!UICONTROL Audiences]** > **[!UICONTROL Segments]** .

   1. Houd de cursor in de segmentrij boven het nieuwe segment en klik op **[!UICONTROL Get pixel]** .

   1. Kopieer de afbeeldingspixel (beginnend met `<img src="https://rtd-tm.everesttech.net"` ) om gebruikers-id&#39;s van gebruikers van het bureaublad en mobiele bezoekers te verzamelen naar een webpagina.

   1. Geef de tag door aan de adverteerder of de websitecontactpersoon voor implementatie met behulp van het mechanisme dat het bedrijf gebruikt om CCPA-verzoeken om niet te verkopen (zoals het gebruik van een platform voor beheer van toestemming) bij te houden.

      De IT-afdeling of andere groep van de adverteerder moet mogelijk de implementatie van de tag plannen of hierover worden geïnformeerd.

      Nadat de pixel is geïmplementeerd, begint Adobe Advertising namens de adverteerder een pool met id&#39;s te verzamelen.

      Hoewel de keuze en logica van de implementatie bij de adverteerder liggen, ziet u hier een voorbeeld van hoe een adverteerder de pixel kan afvuren:

      1. Een consument landt op de homepage van de adverteerder.
      1. De consument zoekt en klikt op de knop CCPA-optie om de adverteerder te weigeren.
      1. De consument krijgt een lijst van dienstverleners te zien waarmee de adverteerder werkt.
      1. De consument schakelt het selectievakje uit om gegevens niet aan Adobe Advertising te verkopen.

         Deze actie brengt de pixel aan brand en om koekjesidentiteitskaart van de consument binnen het gespecificeerde &quot;[!UICONTROL CCPA Opt-out of sale]&quot;segment te verzamelen.

>[!MORELIKETHIS]
>
>* [&#x200B; de steun van Adobe Advertising voor de Wet van de Privacy van de Consumentenbescherming van Californië: De opt-out van de consument van verkoopsteun &#x200B;](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [&#x200B; Ongeveer [!UICONTROL CCPA Opt-out-of-Sale] Segmenten en Rapporten &#x200B;](ccpa-opt-out-about.md)
>* [&#x200B; wint consument op opt-out-of-verkoop rapporten &#x200B;](ccpa-opt-out-segment-report-retrieve.md)
>* [&#x200B; creeer en voer een Segment van de Douane uit &#x200B;](custom-segment-create.md)
>* [&#x200B; Ongeveer publieksbeheer &#x200B;](audience-about.md)
