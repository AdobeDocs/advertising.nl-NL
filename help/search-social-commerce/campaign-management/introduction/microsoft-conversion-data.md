---
title: '[!DNL Microsoft Advertising] conversiegegevens'
description: Meer informatie over de typen [!DNL Microsoft Advertising]-tracked conversion data available in Search, Social, & Commerce.
source-git-commit: 0d7a7b63b31f85b3befb3217fc43bcb229b370f0
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] conversiegegevens in Zoeken, Sociaal, &amp; Handel

Met Zoeken, Sociaal en Handel worden automatisch alle conversies gesynchroniseerd die door uw [Microsoft-tags voor Universal Event tracking (UET) voor advertenties](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) voor websiteconversies, met inbegrip van doorkijkconversies, voor rapportage en optimalisatie.

Alle metriek zijn automatisch beschikbaar in uw weergaven voor campagnebeheer en basisrapporten en zijn ook beschikbaar voor gebruik in portfoliodoelstellingen voor optimalisatie van Microsoft-advertentiecampagnes.

## Beschikbare conversiegegevens

Met Zoeken, Sociaal en Handel worden gegevens gesynchroniseerd voor conversies waarvoor &quot;[!DNL Include in 'Conversions']&quot; optie is ingeschakeld, waarbij de gegevens de laatste 35 dagen worden opgehaald en vervolgens dagelijks wijzigingen in de gegevens worden doorgevoerd tegen 09:00-10:00 in de tijdzone van de adverteerder. Historische gegevens kunnen van dag tot dag veranderen aangezien de nieuwe omzettingen voor elke klik worden gevolgd.

Twee transactieeigenschappen voor elk [[!DNL Microsoft Advertising]-trackconversie](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (die u hebt ingesteld in [!DNL Microsoft Advertising]) automatisch beschikbaar zijn in Zoeken, Sociale Zaken, &amp; Handel, gebruikend de omzettingsnamen die in worden gevormd [!DNL Microsoft Advertising]. De transactieeigenschappen voor elke omzetting omvatten:

* `<conversion-name>` — De conversiewaarde voor het trefwoord (zoals Aankoop).

  >[!TIP]
  >
  >Gebruik dit type eigenschap in de doelstelling voor portfolio&#39;s die [!DNL Microsoft Advertising] campagnes met de Maximale Waarde van de Omzetting en de Bodemstrategieën van het Doel ROAS.

* `CT_<conversion-name>` — Het aantal (aantal) omzettingen, beginnend met het prefix &quot;CT_&quot; (zoals CT_Purchase).

  >[!TIP]
  >
  >Gebruik dit type eigenschap in de doelstelling voor portfolio&#39;s die [!DNL Microsoft Advertising] campagnes met de Maximale Conversies en de Bodemstrategieën van Doel CPA.

De gegevens zijn beschikbaar op basis van de kliktijd en gebaseerd op de conversie-/transactietijd vanaf de datum waarop de functie voor de account is ingeschakeld.

[!DNL Microsoft Advertising] registreert elke omzetting door [biedingseenheid](/help/search-social-commerce/glossary.md#a-b), apparaat en klik op datum (geen omzettingsdatum). Attributie is gebaseerd op de standaardattributie-instelling voor elke metrische waarde in [!DNL Microsoft Advertising]; De attributie van de Adobe Advertising wordt niet in rekening gebracht omdat de klik gebeurtenis-vlakke gegevens niet beschikbaar is.

>[!NOTE]
>
>* Als u meerdere accounts met dezelfde conversienamen hebt, ziet u mogelijk dubbele conversienamen in de Adobe Advertising. Als dit gebeurt, [de weergavenaam wijzigen](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) voor een van de dubbele meetwaarden in [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. Rapportage is niet correct wanneer twee verschillende metriek de zelfde naam hebben.
>* Gegevens op het niveau van de biedingseenheid komen overeen met gegevens in het advertentienetwerk op hetzelfde niveau. Nochtans, kunnen de eigen omzettingsgegevens van het advertentienetwerk voor hogere niveaus extra omzettingen omvatten die niet aan de eenheden van het kindbod worden toegeschreven. Gegevens in Zoeken, Sociaal, &amp; Handel worden altijd opgevoerd vanaf het niveau van de biedingseenheid, zodat, bijvoorbeeld, zou een campagne-vlakke rapport niet de zelfde totalen kunnen hebben zoals een campagne-vlakke rapport in het advertentienetwerk.
>* De variantie van gegevens is typisch minder na de ochtendsynchronisatie dan het later op de dag is, wanneer de extra omzettingen nog niet zijn gesynchroniseerd. We raden u aan &#39;s ochtends gegevens te valideren.
>* De gegevens zijn niet beschikbaar bij het publiek of het geografische plaatsniveau en daarom niet gebruikt om RLSA en plaats biodaanpassingen auto-te optimaliseren.

## Conversiegegevens vergelijken in [!DNL Microsoft Advertising] met gegevens in Zoeken, Sociale &amp; Handel

Gebruik de volgende rapportinstellingen om vergelijkbare gegevens te valideren.

### Rapportinstellingen voor gebruik in [!DNL Microsoft Advertising]

Genereer het rapport voor de geselecteerde omzettingsacties per dag en voeg gegevens voor alle advertentiestatussen toe.

### Rapportinstellingen die moeten worden gebruikt in Zoeken, Sociale Zaken en Handel

In Onderzoek, Sociale, &amp; Handel, gebruik de mening of rapportoptie om omzettingen te bekijken die op de klikdatum (niet de transactiedatum) worden gebaseerd.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Create Report]**, houd de cursor boven **[!UICONTROL Basic Reports]** en klik vervolgens op **[!UICONTROL Search Engine Account Report]**.

1. In de [!UICONTROL Report Settings] Geef de volgende rapportinstellingen op:

   1. In de **[!UICONTROL Conversions Based]** in sectie selecteert u **[!UICONTROL Click date]**.

   1. Geef hetzelfde datumbereik op als dat u hebt gebruikt voor het dialoogvenster [!DNL Microsoft Advertising] verslag.

   1. In de **[!UICONTROL Search/Content]** sectie, selecteert u **[!UICONTROL Search Only]**.

   1. In de **[!UICONTROL Search Engine Hierarchy]** in, vouwt u de [!UICONTROL Microsoft Advertising] en selecteer de account.

   1. Open de [!UICONTROL Columns] en voegt u de [!DNL Microsoft Advertising] maatstaven die u wilt vergelijken.

1. Klik op **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Overzicht van het uitvoeren van en netwerkrekeningen en campagnes](campaign-implemention-overview.md)
>* [De prestaties van uw advertentienetwerkcampagnes bewaken en beheren](monitor-performance-campaigns.md)
>* [De transactieeigenschappen weergeven die voor een adverteerder zijn bijgehouden](/help/search-social-commerce/admin/transaction-properties/transaction-property-view-tracked.md)
