---
title: '[!DNL Microsoft Advertising] conversiegegevens'
description: Leer over de types van  [!DNL Microsoft Advertising] - gevolgde omzettingsgegevens beschikbaar in Onderzoek, Sociale, & Commerce.
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: b8a34f3d85947536eb92ee481966f84694250f29
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] conversiegegevens in Zoeken, Sociaal en Commerce

Onderzoek, sociaal, &amp; Commerce synchroniseert automatisch alle omzettingen die door uw [[!DNL Microsoft Advertising]  universele gebeurtenis het volgen (UET) markeringen ](https://help.ads.microsoft.com/#apex/ads/en/53056) voor websiteomzettingen, met inbegrip van mening-door omzettingen, voor rapportering en optimalisering worden gevolgd.

Alle metriek zijn automatisch beschikbaar in de weergaven en basisrapporten van uw campagnebeheer en zijn ook beschikbaar voor gebruik in portfoliodoelstellingen voor het optimaliseren van [!DNL Microsoft Advertising] -campagnes.

## Beschikbare conversiegegevens

Onderzoek, sociaal, &amp; Commerce synchroniseert gegevens voor omzettingen waarvoor de &quot;[!DNL Include in 'Conversions']&quot;optie wordt toegelaten, trekkend de gegevens voor de laatste 35 dagen en dan trekkend veranderingen in de gegevens dagelijks door 09 :00-10: 00 in de tijdzone van de adverteerder. Historische gegevens kunnen van dag tot dag veranderen aangezien de nieuwe omzettingen voor elke klik worden gevolgd.

Twee metriek voor elke [[!DNL Microsoft Advertising] - gevolgde omzetting ](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (die u opstelling in [!DNL Microsoft Advertising]) zijn automatisch beschikbaar in Onderzoek, Sociale, &amp; Commerce, gebruikend de omzettingsnamen die in [!DNL Microsoft Advertising] worden gevormd. De meetgegevens voor elke omzetting omvatten:

* `<conversion-name>` — De conversiewaarde voor het trefwoord (zoals Aankoop).

  >[!TIP]
  >
  >Gebruik dit type metrische conversie in de doelstelling voor portefeuilles die [!DNL Microsoft Advertising] campagnes met de Maximale Waarde van de Omzetting en de Bodemstrategieën van het Doel van ROAS omvatten.

* `CT_<conversion-name>` — Het aantal (aantal) omzettingen, beginnend met het prefix &quot;CT_&quot; (zoals CT_Purchase).

  >[!TIP]
  >
  >Gebruik dit type metrische conversie in de doelstelling voor portfolio&#39;s die [!DNL Microsoft Advertising] -campagnes bevatten met de biedingsstrategieën Max Conversions en Target CPA.

De gegevens zijn beschikbaar op basis van de kliktijd en gebaseerd op de conversie-/transactietijd vanaf de datum waarop de functie voor de account is ingeschakeld.

[!DNL Microsoft Advertising] registreert elke omzetting door [ biedingseenheid ](/help/search-social-commerce/glossary.md#a-b), apparaat, en klik datum (niet omzettingsdatum). Attributie is gebaseerd op de standaardattributie die voor elke metrische waarde in [!DNL Microsoft Advertising] wordt geplaatst; de attributie van de Adobe Advertising wordt niet in rekening gebracht omdat de klik gebeurtenis-vlakke gegevens niet beschikbaar is.

>[!NOTE]
>
>* Als u meerdere accounts met dezelfde conversienamen hebt, ziet u mogelijk dubbele conversienamen in de Adobe Advertising. Als dit voorkomt, [ verander de vertoningsnaam ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) voor één van de dubbele metriek in [!UICONTROL Admin] > [!UICONTROL Conversions]. Rapportage is niet correct wanneer twee verschillende metriek de zelfde naam hebben.
>* Gegevens op het niveau van de biedingseenheid komen overeen met gegevens in het advertentienetwerk op hetzelfde niveau. Nochtans, kunnen de eigen omzettingsgegevens van het advertentienetwerk voor hogere niveaus extra omzettingen omvatten die niet aan de eenheden van het kindbod worden toegeschreven. Gegevens in Zoeken, Sociaal, &amp; Commerce worden altijd opgevoerd vanaf het niveau van de biedingseenheid, zodat, bijvoorbeeld, zou een campagne-vlakke rapport niet de zelfde totalen kunnen hebben zoals een campagne-vlakke rapport in het advertentienetwerk.
>* De variantie van gegevens is typisch minder na de ochtendsynchronisatie dan het later op de dag is, wanneer de extra omzettingen nog niet zijn gesynchroniseerd. We raden u aan &#39;s ochtends gegevens te valideren.
>* De gegevens zijn niet beschikbaar bij het publiek of het geografische plaatsniveau en daarom niet gebruikt om RLSA en plaats biodaanpassingen auto-te optimaliseren.

## Conversiegegevens in [!DNL Microsoft Advertising] vergelijken met gegevens in Zoeken, Sociaal en Commerce

Gebruik de volgende rapportinstellingen om vergelijkbare gegevens te valideren.

### In [!DNL Microsoft Advertising] te gebruiken rapportinstellingen

Genereer het rapport voor de geselecteerde omzettingsacties per dag en voeg gegevens voor alle advertentiestatussen toe.

### Rapportinstellingen voor Zoeken, Sociaal en Commerce

In Zoeken, Sociaal, &amp; Commerce, gebruik de mening of rapportoptie om omzettingen te bekijken die op de klikdatum (niet de transactiedatum) worden gebaseerd.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** .

1. Klik in de werkbalk boven de gegevenstabel op **[!UICONTROL Create Report]** , houd de cursor boven **[!UICONTROL Basic Reports]** en klik vervolgens op **[!UICONTROL Search Engine Account Report]** .

1. Geef in het [!UICONTROL Report Settings] -venster de volgende rapportinstellingen op:

   1. Selecteer **[!UICONTROL Click date]** in de sectie **[!UICONTROL Conversions Based]** on.

   1. Geef hetzelfde datumbereik op als dat u voor het [!DNL Microsoft Advertising] -rapport hebt gebruikt.

   1. Selecteer **[!UICONTROL Search Only]** in de sectie **[!UICONTROL Search/Content]** .

   1. Vouw in de sectie **[!UICONTROL Search Engine Hierarchy]** de sectie [!UICONTROL Microsoft Advertising] uit en selecteer de account.

   1. Open het tabblad [!UICONTROL Columns] en voeg de [!DNL Microsoft Advertising] -meetgegevens toe die u wilt vergelijken.

1. Klik op **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [ Overzicht van het uitvoeren van en netwerkrekeningen en campagnes ](campaign-implemention-overview.md)
>* [ Monitor en beheer de prestaties van uw campagnes van het advertentienetwerk ](monitor-performance-campaigns.md)
>* [ Mening de omzettingsmetriek die voor een adverteerder wordt gevolgd ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
