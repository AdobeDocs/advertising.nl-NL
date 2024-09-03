---
title: '[!DNL Google Ads] conversiegegevens'
description: Leer over de types van  [!DNL Google Ads] - gevolgde omzettingsgegevens beschikbaar in Onderzoek, Sociale, & Commerce.
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# [!DNL Google Ads] conversiegegevens in Zoeken, Sociaal en Commerce

Met Zoeken, Sociaal en Commerce worden automatisch [!DNL Google Ads] bijgehouden conversiegegevens gesynchroniseerd voor al uw campagnes op de [!DNL Google Ads] -netwerken voor zoeken en winkelen naar Zoeken, Sociaal en Commerce voor rapportage en optimalisatie.

Alle metriek zijn automatisch beschikbaar in uw meningen van het campagnebeheer en basisrapporten, en zijn ook beschikbaar om in portefeuilledoelstellingen voor optimalisering te gebruiken.

## Beschikbare conversiegegevens

Onderzoek, sociaal, &amp; Commerce synchroniseert gegevens voor omzettingen waarvoor de &quot;[!DNL Include in 'Conversions']&quot;optie wordt toegelaten, trekkend de gegevens voor de laatste 35 dagen en dan trekkend veranderingen in de gegevens dagelijks door 09 :00-10: 00 in de tijdzone van de adverteerder. Historische gegevens kunnen van dag tot dag veranderen aangezien de nieuwe omzettingen voor elke klik worden gevolgd.

Maximaal drie metriek voor elke [[!DNL Google Ads] bijgehouden conversie ](https://support.google.com/google-ads/answer/4677036) (die u instelt in [!DNL Google Ads] ) zijn automatisch beschikbaar in Zoeken, Sociaal en Commerce, met gebruik van de conversienamen die zijn geconfigureerd in [!DNL Google Ads] . De meetgegevens voor elke omzetting omvatten:

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — (Wanneer u dit bijhoudt) De omzettingswaarde voor het trefwoord, te beginnen met het voorvoegsel &quot;GGL&quot; (zoals Aankoop GL).

* `GGL_CT*` — Het aantal (aantal) conversies, beginnend met het voorvoegsel &quot;GGL_CT&quot; (zoals GGL_CT_Purchase).

* `GGL_XD_CT*` — (Indien beschikbaar voor het conversietype, wanneer u deze bijhoudt) Het aantal (aantal) apparaatomzettingen, zoals gemeten door Google, beginnend met het voorvoegsel &quot;GGL_XD_CT_&quot; (zoals GL_XD_CT_Purchase).

[!DNL Google Ads] registreert elke omzetting door [ biedingseenheid ](/help/search-social-commerce/glossary.md#a-b), apparaat, en klik datum (niet omzettingsdatum). Attributie is gebaseerd op de standaardattributie die voor elke metrische waarde in [!DNL Google Ads] wordt geplaatst; de attributie van de Adobe Advertising wordt niet in rekening gebracht omdat de klik gebeurtenis-vlakke gegevens niet beschikbaar is.

>[!NOTE]
>
>* Als u meerdere accounts met dezelfde conversienamen hebt, ziet u mogelijk dubbele conversienamen in de Adobe Advertising. Als dit voorkomt, [ verander de vertoningsnaam ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) voor één van de dubbele metriek in [!UICONTROL Admin] > [!UICONTROL Conversions]. Rapportage is niet correct wanneer twee verschillende metriek de zelfde naam hebben.
>* Gegevens op het niveau van de biedingseenheid komen overeen met gegevens in [!DNL Google Ads] op hetzelfde niveau. De eigen conversiegegevens van [!DNL Google Ads] voor hogere niveaus kunnen echter aanvullende conversies bevatten die niet aan de onderliggende bodeenheden worden toegewezen. Gegevens in Zoeken, Sociaal, &amp; Commerce worden altijd opgevoerd vanaf het niveau van de biedingseenheid, zodat een campagnerapport bijvoorbeeld mogelijk niet dezelfde totalen heeft als een campagnerapport in Google Ads.
>* De variantie van gegevens is typisch minder na de ochtendsynchronisatie dan het later op de dag is, wanneer de extra omzettingen nog niet zijn gesynchroniseerd. We raden u aan &#39;s ochtends gegevens te valideren.
>* Conversiegegevens zijn niet beschikbaar voor advertenties [!DNL Google Display Network] , [!DNL Gmail] , [!DNL Mobile App] en [!DNL YouTube] . Filter deze typen advertenties uit wanneer u gegevens in [!DNL Google Ads] vergelijkt met gegevens in Zoeken, Sociaal en Commerce.
>* Gegevens voor [!DNL Google Ads] -conversies zijn niet beschikbaar voor het publiek of de geografische locatie en worden daarom niet gebruikt voor het automatisch optimaliseren van RLSA- en locatieblokaanpassingen.

## Conversiegegevens in [!DNL Google Ads] vergelijken met gegevens in Zoeken, Sociaal en Commerce

Als u gegevens in Zoeken, Sociaal, &amp; Commerce met die in [!DNL Google Ads] vergelijkt, gebruik de mening of rapportoptie om omzettingen te bekijken die op de klikdatum (niet de transactiedatum) worden gebaseerd.

Gebruik de volgende rapportinstellingen om vergelijkbare gegevens te valideren.

### In [!DNL Google Ads] te gebruiken rapportinstellingen

Genereer het rapport voor de geselecteerde omzettingsacties per dag en voeg gegevens voor alle advertentiestatussen toe.

<!-- 

1. In the main toolbar, select **[!DNL Reports] > [!DNL Report]**.

1. Select **[!DNL + Custom] > [!DNL Table]**.

1. From the left pane, specify the rows and columns in the report:
   
   1. Search for the **[!DNL Day]** field and it drag to the [!DNL Row] section.

   1. Search for the **[!DNL All conv].** field and it drag to the [!DNL Column] section.

   1. Search for the **[!DNL Conversion action]** field and it drag to the [!DNL Column] section.

1. In the report settings toolbar, select **[!DNL Filter] > [!DNL Ad status]**, and then select all boxes.

1. In the report settings toolbar, select **[!DNL Download] > [!DNL Excel .csv]**.

-->

### Rapportinstellingen voor Zoeken, Sociaal en Commerce

In Zoeken, Sociaal, &amp; Commerce, gebruik de mening of rapportoptie om omzettingen te bekijken die op de klikdatum (niet de transactiedatum) worden gebaseerd.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** .

1. Klik in de werkbalk boven de gegevenstabel op **[!UICONTROL Create Report]** , houd de cursor boven **[!UICONTROL Basic Reports]** en klik vervolgens op **[!UICONTROL Search Engine Account Report]** .

1. Geef in het [!UICONTROL Report Settings] -venster de volgende rapportinstellingen op:

   1. Selecteer **[!UICONTROL Click date]** in de sectie **[!UICONTROL Conversions Based]** on.

   1. Geef hetzelfde datumbereik op als dat u voor het [!DNL Google Ads] -rapport hebt gebruikt.

   1. Selecteer **[!UICONTROL Search Only]** in de sectie **[!UICONTROL Search/Content]** .

   1. Vouw in de sectie **[!UICONTROL Search Engine Hierarchy]** de sectie [!UICONTROL Google Adwords] uit en selecteer de account.

   1. Open het tabblad [!UICONTROL Columns] en voeg de [!DNL Google Ads] -metriek (te beginnen met &quot;GGL&quot;) toe die u wilt vergelijken.

1. Klik op **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [ Overzicht van het uitvoeren van en netwerkrekeningen en campagnes ](campaign-implemention-overview.md)
>* [ Monitor en beheer de prestaties van uw campagnes van het advertentienetwerk ](monitor-performance-campaigns.md)
>* [ Mening de omzettingsmetriek die voor een adverteerder wordt gevolgd ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [ creeer een omzettingsmarkering voor  [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)
>* [ upload off-line omzettingsgegevens voor verbeterde omzettingen ](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
