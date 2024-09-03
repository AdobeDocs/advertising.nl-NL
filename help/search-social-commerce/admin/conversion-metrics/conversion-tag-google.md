---
title: Een conversietag maken voor  [!DNL Google Ads]
description: Leer hoe te om a  [!DNL Google Ads]  omzettingsmarkering tot stand te brengen.
feature: Conversions
exl-id: 214611f0-bd38-499e-a7de-3a5878995fb5
source-git-commit: 2c20d2138ee797b6ed2f27d9baa9eda7d413da8d
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Een conversietag maken voor [!DNL Google Ads]

U kunt conversietags maken voor nieuwe conversies die moeten worden bijgehouden voor afzonderlijke [!DNL Google Ads] -accounts, niet die op beheerdersniveau worden bijgehouden.

Als u conversietags voor bestaande conversies wilt genereren, gebruikt u de editor van het advertentienetwerk.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]** , dat wordt geopend op de tab **[!UICONTROL Summary]** .

1. In de toolbar boven de gegevenslijst, leidt de klik ![ ](/help/search-social-commerce/assets/add.png " tot ").

1. Specificeer de [ montages van de omzettingsmarkering ](#conversion-tag-settings-google).

   1. Selecteer het account en selecteer het type conversie.

   1. Klik op **[!UICONTROL Next]**.

   1. Geef de conversieopties op.

   1. Klik op **[!UICONTROL Generate]**.

1. Kopieer de conversietag en implementeer deze op de websites waarvan u de metrische conversie wilt bijhouden.

   Zie &quot;Installing the [!DNL Google] markering&quot;in [!DNL Google Ads] hulp aan &quot;[ 2. Opstelling uw markering van Google ](https://support.google.com/google-ads/answer/12215519).&quot;

1. Klik op **[!UICONTROL Done].**

Nadat u de tags aan uw website hebt toegevoegd en deze hebt geactiveerd, worden de conversies door [!DNL Google Ads] vastgelegd op de website. Met Zoeken, Sociaal en Commerce worden de conversies dagelijks gesynchroniseerd. Voor meer informatie over de gegevens die worden gesynchroniseerd, zie &quot;[[!DNL Google Ads]  omzettingsgegevens in Onderzoek, Sociale, &amp; Commerce ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Instellingen voor conversietag {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** De toepasselijke Google Ads-account.

**[!UICONTROL Type of Conversion]:** Het type conversie naar track: *[!UICONTROL Click on a webpage element]* , *[!UICONTROL Calls to a phone number on your website]* of *[!UICONTROL Clicks to your number on your mobile website]* . **Nota:** *[!UICONTROL Import conversion]* wordt gebruikt voor een verschillend doel; zie &quot;[ een omzettingsactie voor a  [!DNL Google Ads]  verbeterde omzetting voor lood ](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) creëren.&quot;

**[!UICONTROL Conversion Name]:** Een unieke naam voor de metrische conversie.

**\[Conversiecategorie\]:** De conversiecategorie. De beschikbare categorieën variëren per conversietype. Voor *[!UICONTROL Calls to a phone number on your website]* en *[!UICONTROL Clicks to your number on your mobile website]*, &quot; [!UICONTROL Phone Call Lead]&quot;wordt geselecteerd door gebrek.

**\[Type handeling\]:** Of het doel een *[!UICONTROL Primary action used for bidding optimization]* of een *[!UICONTROL Secondary action not used for bidding optimization]* is.

**[!UICONTROL Value]:** hoe te om de [ waarde van elke omzetting ](https://support.google.com/google-ads/answer/3419241) te meten:

* *[!UICONTROL Use the same value for each conversion],* die u vereist om een munt te selecteren en de waarde voor elke omzetting in te gaan.

* *[!UICONTROL Use a different value for each conversion],* die u vereist om een munt te selecteren en een standaardwaarde voor elke omzetting in te gaan. U kunt de standaardwaarde in de tag wijzigen met een transactiespecifieke waarde wanneer u de tag implementeert op een specifieke webpagina.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [ hoeveel omzettingen per klik of interactie te tellen ](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* of *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Het maximumaantal dagen na een advertentietransactie waarvoor omzettingen worden geregistreerd. Voor zoek-, weergave- en winkelcampagnes kan het venster 1-90 dagen lang zijn. Selecteer een getal of selecteer **[!UICONTROL Custom]** en voer een getal in.

**[!UICONTROL View Through Conversion Window]:** Het maximumaantal dagen nadat een gebruiker uw advertenties bekijkt waarvoor mening-door omzettingen worden geregistreerd. Voor zoek-, weergave- en winkelcampagnes kan het venster 1-90 dagen lang zijn. Selecteer een getal of selecteer **[!UICONTROL Custom]** en voer een getal in.

**[!UICONTROL Attribution Model]:** [ hoeveel krediet elke ad interactie ](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138) krijgt: *[!UICONTROL Data driven]* of *[!UICONTROL Last click]*. **Nota:** de acties van de Omzetting die eerder de nu-niet gestaafde *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]*, of *[!UICONTROL Position based]* modellen gebruikten nu het *[!UICONTROL Data driven]* model.

>[!MORELIKETHIS]
>
>* [ upload off-line omzettingsgegevens voor verbeterde omzettingen ](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [[!DNL Google Ads]  omzettingsgegevens in Onderzoek, Sociale, &amp; Commerce ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
