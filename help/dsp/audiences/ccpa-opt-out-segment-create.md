---
title: Creeer en voer een CCPA uit Opt-uit-van-Verkoop segment
description: Leer hoe u een segment maakt en implementeert om gebruikers-id's te traceren op basis van verzoeken van consumenten om te weigeren een product te verkopen.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# Creeer en voer een CCPA uit Opt-uit-van-Verkoop segment

U kunt een segment tot stand brengen om gebruikers IDs van consument van uit-verkoopverzoeken op uw website te volgen, volgens de Wet van de Privacy van de consument van Californië (CCPA). De gebruikers blijven in opt-out van CCPA-segmenten voor onbepaalde tijd.

Zodra de segmentpixel-tag is geïmplementeerd, begint de Adobe Advertising een pool met id&#39;s te verzamelen namens de adverteerder.

>[!NOTE]
>
>* Voor informatie over hoe te om CCPA mee te delen - uit-van-verkoop verzoeken aan Adobe Advertising gebruikend Adobe Experience Platform Privacy Service API, zie [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html?lang=nl-NL](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html?lang=nl-NL).
>* Als u gebruikers wilt volgen die webpagina&#39;s bezoeken voor doeleinden die geen verband houden met het volgen van CCPA-opt-out-of-sale gebeurtenissen, en gebruikers die worden blootgesteld aan advertenties van desktop-, mobiele en CTV-apparaten, maakt u een [aangepast segment](/help/dsp/audiences/custom-segment-create.md).

1. Maak het segment:

   1. Klik in het hoofdmenu op **Soorten publiek > Segmenten**.

   1. Klik boven de gegevenstabel op **[!UICONTROL Create]**.

   1. Voer een unieke waarde in **[!UICONTROL Segment Name]**.

      Aanbevolen segmentnaam: &quot;&lt;*De naam van uw adverteerder*> - CCPA niet meer in de handel&quot; (zoals &quot;Acme - CCPA niet meer in de handel&quot;)

   1. Voor de [!UICONTROL Segment Type], selecteert u **[!UICONTROL CCPA Opt-out of sale]**.

   1. Klik op **[!UICONTROL Save]**.

1. Kopieer en implementeer een pixeltag om het segment bij te houden:

   1. Terug naar **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Houd de cursor in de segmentrij boven het nieuwe segment en klik op **[!UICONTROL Get pixel]**.

   1. De afbeeldingspixel kopiëren (beginnen met `<img src="https://rtd-tm.everesttech.net"`) om gebruikers-id&#39;s van bezoekers van het bureaublad en mobiele apparaten te verzamelen op een webpagina.

   1. Geef de tag door aan de adverteerder of de websitecontactpersoon voor implementatie met behulp van het mechanisme dat het bedrijf gebruikt om CCPA-verzoeken om niet te verkopen (zoals het gebruik van een platform voor beheer van toestemming) bij te houden.

      De IT-afdeling of andere groep van de adverteerder moet mogelijk de implementatie van de tag plannen of hierover worden geïnformeerd.

      Zodra de pixel wordt uitgevoerd, begint de Adobe Advertising een pool van IDs namens de adverteerder te verzamelen.

      Hoewel de keuze en logica van de implementatie bij de adverteerder liggen, ziet u hier een voorbeeld van hoe een adverteerder de pixel kan afvuren:

      1. Een consument landt op de homepage van de adverteerder.
      1. De consument zoekt en klikt op de knop CCPA-optie om de adverteerder te weigeren.
      1. De consument krijgt een lijst van dienstverleners te zien waarmee de adverteerder werkt.
      1. De consument schakelt het selectievakje uit om gegevens niet aan de Adobe Advertising te verkopen.

         Deze actie activeert de pixel om in brand te steken en de koekjesidentiteitskaart van de consument binnen gespecificeerde te verzamelen &quot;[!UICONTROL CCPA Opt-out of sale]&quot; segment.

>[!MORELIKETHIS]
>
>* [Adobe Advertising Support for the California Consumer Privacy Act: Consumer Opt-out Support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Info [!UICONTROL CCPA Opt-out-of-Sale] Segmenten en rapporten](ccpa-opt-out-about.md)
>* [Rapporten over verkoopopties voor consumenten ophalen](ccpa-opt-out-segment-report-retrieve.md)
>* [Een aangepast segment maken en implementeren](custom-segment-create.md)
>* [Informatie over Audience Management](audience-about.md)
