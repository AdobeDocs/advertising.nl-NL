---
title: Een conversietag maken voor [!DNL Google Ads]
description: Leer hoe u een [!DNL Google Ads] conversietag.
feature: Conversions
source-git-commit: 8f08151013ec63df14843733a0c83badcceba4c3
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Een conversietag maken voor [!DNL Google Ads]

U kunt conversietags maken voor nieuwe conversies die voor afzonderlijke conversies moeten worden bijgehouden [!DNL Google Ads] accounts, niet bijgehouden op het niveau van een beheerdersaccount.

Als u conversietags voor bestaande conversies wilt genereren, gebruikt u de editor van het advertentienetwerk.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

1. Klik op de werkbalk boven de tabel met gegevens op ![Maken](/help/search-social-commerce/assets/add.png "Maken").

1. Geef de [instellingen voor conversietags](#conversion-tag-settings-google).

   1. Selecteer het account en selecteer het type conversie.

   1. Klik op **[!UICONTROL Next]**.

   1. Geef de conversieopties op.

   1. Klik op **[!UICONTROL Generate]**.

1. Kopieer de conversietag en implementeer deze op de websites waarvan u de metrische conversie wilt bijhouden.

   Zie &quot;De installatie van de [!DNL Google] -tag&quot; in de [!DNL Google Ads] Help bij &quot;[2. De Google-tag instellen](https://support.google.com/google-ads/answer/12215519).&quot;

1. Klik op **[!UICONTROL Done].**

Nadat u de tags aan uw website hebt toegevoegd en deze hebt geactiveerd, [!DNL Google Ads] registreert omzettingen op de website. Met Zoeken, Sociaal en Handel worden de conversies dagelijks gesynchroniseerd. Zie voor meer informatie over de gesynchroniseerde gegevens &quot;[[!DNL Google Ads] conversiegegevens in Zoeken, Sociaal, &amp; Handel](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Instellingen voor conversietag {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** De toepasselijke Google Ads-account.

**[!UICONTROL Type of Conversion]:** Het type conversie naar track: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]*, of *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]:** Een unieke naam voor de metrische conversie.

**\[Doelcategorie\]:** De conversiecategorie. De beschikbare categorieën variëren per conversietype. Voor *[!UICONTROL Calls to a phone number on your website]* en *[!UICONTROL Clicks to your number on your mobile website]*, &quot;[!UICONTROL Phone Call Lead]&quot; is standaard geselecteerd.

**\[Type handeling\]:** Of het doel een *[!UICONTROL Primary action used for bidding optimization]* of *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Hoe wordt de [waarde van elke conversie](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],* waarvoor u een valuta moet selecteren en de waarde voor elke conversie moet invoeren.

* *[!UICONTROL Use a different value for each conversion],* waarvoor u een valuta moet selecteren en een standaardwaarde voor elke conversie moet opgeven. U kunt de standaardwaarde in de tag wijzigen met een transactiespecifieke waarde wanneer u de tag implementeert op een specifieke webpagina.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Hoeveel omzettingen per klik of interactie moeten tellen](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* of *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Het maximumaantal dagen na een advertentietransactie waarvoor omzettingen worden geregistreerd. Voor zoek-, weergave- en winkelcampagnes kan het venster 1-90 dagen lang zijn. Selecteer een nummer of selecteer **[!UICONTROL Custom]** en voert u een getal in.

**[!UICONTROL View Through Conversion Window]:** Het maximumaantal dagen nadat een gebruiker advertenties bekijkt waarvoor doorkijkconversies worden opgenomen. Voor zoek-, weergave- en winkelcampagnes kan het venster 1-90 dagen lang zijn. Selecteer een nummer of selecteer **[!UICONTROL Custom]** en voert u een getal in.

**[!UICONTROL Attribution Model]:** [Hoeveel krediet elke advertentieinteractie krijgt](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*, *[!UICONTROL Last click]*, *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]*, of *[!UICONTROL Position based]*.

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] conversiegegevens in Zoeken, Sociaal, &amp; Handel](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
