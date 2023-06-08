---
title: "[!DNL Google Ads] conversiegegevens"
description: Meer informatie over de typen [!DNL Google Ads]-tracked conversion data available in Search, Social, & Commerce.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# [!DNL Google Ads] conversiegegevens in Zoeken, Sociaal, &amp; Handel

Automatisch synchroniseren bij Zoeken, Sociale media en Handel [!DNL Google Ads]-tracked conversion data for all your campagnes on the [!DNL Google Ads] zoek- en winkelnetwerken naar Zoeken, Sociale Zaken en Handel voor rapportage en optimalisatie. Met Zoeken, Sociaal en Handel worden gegevens gesynchroniseerd voor conversies waarvoor &quot;[!DNL Include in 'Conversions']&quot; optie is ingeschakeld, waarbij de gegevens de laatste 30 dagen worden opgehaald en vervolgens dagelijks wijzigingen in de gegevens worden doorgevoerd.

## Beschikbare conversiegegevens

Tot drie transactieeigenschappen voor elk [[!DNL Google Ads]-trackconversie](https://support.google.com/google-ads/answer/4677036) (die u hebt ingesteld in [!DNL Google Ads]) automatisch beschikbaar zijn in Zoeken, Sociale Zaken, &amp; Handel, gebruikend de omzettingsnamen die in worden gevormd [!DNL Google Ads]. De transactieeigenschappen voor elke omzetting omvatten:

* `GGL*` — (Wanneer u het volgt) De som omzettingswaarden voor het sleutelwoord, die met het prefix &quot;GL&quot;beginnen (zoals Aankoop GL).

* `GGL_CT*` — Het aantal (aantal) conversies, beginnend met het voorvoegsel &quot;GGL_CT&quot; (zoals GGL_CT_Purchase).

* `GGL_XD_CT*` — (Indien beschikbaar voor het conversietype, wanneer u deze bijhoudt) Het aantal (aantal) apparaatoverschrijvingen, zoals gemeten door Google, beginnend met het voorvoegsel &quot;GGL_XD_CT_&quot; (zoals GGL_XD_CT_Purchase).

De gegevens zijn beschikbaar vanaf de datum waarop de functie is ingeschakeld voor de account en worden dagelijks bijgewerkt met 09:00-10:00 in de tijdzone van de adverteerder.

[!DNL Google Ads] registreert elke omzetting door [biedingseenheid](/help/search-social-commerce/glossary.md#a-b), apparaat en klik op datum (geen omzettingsdatum). Attributie is gebaseerd op de standaardattributie-instelling voor elke metrische waarde in [!DNL Google Ads]; De Adobe-advertentiekenmerken worden niet meegerekend omdat gegevens op gebeurtenisniveau niet beschikbaar zijn. Elke dag, trekt Onderzoek, Sociale, &amp; Handel omzettingsgegevens voor de vorige 30 dagen en berekent dan om het even welke stijgende omzettingen sinds de vorige dag, gebruikend de klikdatum van [!DNL Google Ads] en de voorafgaande dag aan te wijzen als de transactiedatum. Als gevolg hiervan kunnen historische gegevens van dag tot dag veranderen wanneer voor elke klik nieuwe omzettingen worden bijgehouden. Als u gegevens in Search, Social &amp; Commerce vergelijkt met die in [!DNL Google Ads]gebruikt u de optie Weergave of Rapport om &quot;[!UICONTROL Conversions by: Click date]&quot; (niet op transactiedatum).

Alle metriek zijn automatisch beschikbaar in uw meningen van het campagnebeheer en basisrapporten, en zijn ook beschikbaar om in portefeuilledoelstellingen voor optimalisering te gebruiken.

>[!NOTE]
>
>* Als u meerdere accounts met dezelfde conversienamen hebt, ziet u mogelijk dubbele conversienamen in Adobe Advertising. Als dit gebeurt, [de weergavenaam wijzigen](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) voor een van de dubbele meetwaarden in [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. Rapportage is niet correct wanneer twee verschillende metriek de zelfde naam hebben.
>* Gegevens op het niveau van de biedingseenheid komen overeen met gegevens in [!DNL Google Ads] op hetzelfde niveau. Maar [!DNL Google Ads]De eigen omzettingsgegevens voor hogere niveaus kunnen extra omzettingen omvatten die niet aan de eenheden van het kindbod worden toegeschreven. Gegevens in Zoeken, Sociaal, &amp; Handel worden altijd opgevoerd vanaf het niveau van de biedingseenheid, zodat bijvoorbeeld een campagnerapport mogelijk niet dezelfde totalen heeft als een campagnerapport in Google Ads.
>* De variantie van gegevens is typisch minder na de ochtendsynchronisatie dan het later op de dag is, wanneer de extra omzettingen nog niet zijn gesynchroniseerd. We raden u aan &#39;s ochtends gegevens te valideren.
>* Conversiegegevens zijn niet beschikbaar voor [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App], en [!DNL YouTube] advertenties. Filter deze typen advertenties uit wanneer u gegevens vergelijkt in [!DNL Google Ads] met gegevens in Zoeken, Sociaal, &amp; Handel.
>* Gegevens voor [!DNL Google Ads] conversies zijn niet beschikbaar op het niveau van het publiek of de geografische locatie en worden daarom niet gebruikt voor automatische optimalisatie van RLSA- en locatiewijzigingen.


## Conversiegegevens vergelijken in [!DNL Google Ads] met gegevens in Zoeken, Sociale &amp; Handel

Gebruik de volgende rapportinstellingen om vergelijkbare gegevens te valideren.

### Rapportinstellingen voor gebruik in [!DNL Google Ads]

1. Selecteer in de hoofdwerkbalk de optie **[!DNL Reports]>[!DNL Report]**.

1. Selecteren **[!DNL + Custom]>[!DNL Table]**.

1. Geef in het linkervenster de rijen en kolommen in het rapport op:

   1. Zoeken naar **[!DNL Day]** veld en wordt naar het [!DNL Row] sectie.

   1. Zoeken naar **[!DNL All conv].** veld en wordt naar het [!DNL Column] sectie.

   1. Zoeken naar **[!DNL Conversion action]** veld en wordt naar het [!DNL Column] sectie.

1. Selecteer op de werkbalk met rapportinstellingen de optie **[!DNL Filter]>[!DNL Ad status]** en selecteert u vervolgens alle vakken.

1. Selecteer op de werkbalk met rapportinstellingen de optie **[!DNL Download]>[!DNL Excel .csv]**.

### Rapportinstellingen die moeten worden gebruikt in Zoeken, Sociale Zaken en Handel

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Create Report]**, houd de cursor boven **[!UICONTROL Basic Reports]** en klik vervolgens op **[!UICONTROL Search Engine Account Report]**.

1. In de [!UICONTROL Report Settings] Geef de volgende rapportinstellingen op:

   1. In de **[!UICONTROL Conversions Based]** in sectie selecteert u **[!UICONTROL Click date]**.

   1. Geef hetzelfde datumbereik op als dat u hebt gebruikt voor het dialoogvenster [!DNL Google Ads] verslag.

   1. In de **[!UICONTROL Search/Content]** sectie, selecteert u **[!UICONTROL Search Only]**.

   1. In de **[!UICONTROL Search Engine Hierarchy]** in, vouwt u de [!UICONTROL Google Adwords] en selecteer de account.

   1. Open de [!UICONTROL Columns] en voegt u de [!DNL Google Ads] maateenheden (te beginnen met &quot;GGL&quot;) die u wilt vergelijken.

1. Klik op **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Informatie over campagnebeheer in Zoeken, Sociale Zaken en Handel](campaign-management-about.md)
>* [Overzicht van het uitvoeren van en netwerkrekeningen en campagnes](campaign-implemention-overview.md)
>* [De prestaties van uw advertentienetwerkcampagnes bewaken en beheren](monitor-performance-campaigns.md)

