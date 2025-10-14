---
title: Creeer een omzettingsactie voor a [!DNL Google Ads]  verbeterde omzetting voor lood
description: Leer hoe te om a  [!DNL Google Ads]  omzettingsactie voor een verbeterde omzetting voor lood tot stand te brengen.
feature: Conversions
exl-id: faf4a6de-e82f-4afd-bda5-2602fb45aee5
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Een conversieactie maken voor een [!DNL Google Ads] verbeterde conversie voor leads

*[!DNL Google Ads]alleen accounts*

U kunt conversieacties maken voor [!DNL Google Ads] verbeterde conversies voor leads die moeten worden bijgehouden voor afzonderlijke [!DNL Google Ads] -accounts, niet voor conversies die worden bijgehouden op het niveau van een beheeraccount.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]** , waarmee u het tabblad **[!UICONTROL Summary]** opent.

1. In de toolbar boven de gegevenslijst, leidt de klik ![&#x200B; &#x200B;](/help/search-social-commerce/assets/add.png " tot ").

1. Specificeer de [&#x200B; montages van de omzettingsactie &#x200B;](#conversion-action-settings-google).

   1. Selecteer de account en selecteer het conversietype: *[!UICONTROL Import conversion]* .

   1. Klik op **[!UICONTROL Next]**.

   1. Geef de opties voor de conversieactie op.

   1. Klik op **[!UICONTROL Generate]**.

1. Lees de informatie over hoe u een trackingtag maakt voor de verbeterde conversie voor leads en klik vervolgens op **[!UICONTROL Next]** .

   Maak de conversietag en implementeer deze zo nodig op de websites waarvan u de conversiemetrisch wilt bijhouden. Zie het volgende voor instructies:

   * Om de [!DNL Google] markering te gebruiken, zie de [!DNL Google Ads] instructies om &quot;te vormen [!DNL Google] markeringsmontages&quot;in &quot;[&#x200B; Opstelling verbeterde omzettingen voor lood met de  [!DNL Google]  markering &#x200B;](https://support.google.com/google-ads/answer/11347292).&quot;

   * Om [!DNL Google Tag Manager] te gebruiken, zie de [!DNL Google Ads] instructies om &quot;[!DNL Google] markeringsmontages&quot;te vormen en &quot;uw opstelling te verifiëren en de container&quot;in &quot;[&#x200B; Opstelling verbeterde omzettingen voor lood met  [!DNL Google Tag Manager] te publiceren &#x200B;](https://support.google.com/google-ads/answer/11021502?#configure).&quot;

1. Klik op **[!UICONTROL Done].**

Nadat u de conversieactie hebt gemaakt en een trackingtag voor conversie hebt geïmplementeerd, kunt u de offlineconversiegegevens uploaden die uw organisatie vastlegt en deze koppelen aan de conversieactie. Zie &quot;[&#x200B; off-line omzettingsgegevens voor verbeterde omzettingen &#x200B;](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) uploaden.&quot;

## Instellingen voor conversieactie {#conversion-action-settings-google}

**[!UICONTROL Select an Account]:** De toepasselijke Google Ads-account.

**[!UICONTROL Type of Conversion]:** Het type conversie naar track: Selecteren *[!UICONTROL Import conversion]* . Alle andere typen worden gebruikt om conversietags (geen conversieacties) te maken voor andere typen conversies.

**[!UICONTROL Conversion Name]:** Een unieke naam voor de conversieactie.

**\ [de Categorie van de Omzetting \]:** de omzettingscategorie, zoals *Gekwalificeerde lood* of *login*.

**\[Type handeling\]:** Of het doel een *[!UICONTROL Primary action used for bidding optimization]* of een *[!UICONTROL Secondary action not used for bidding optimization]* is.

**[!UICONTROL Value]:** hoe te om de [&#x200B; waarde van elke omzetting &#x200B;](https://support.google.com/google-ads/answer/13064207) te meten:

* *[!UICONTROL Use the same value for each conversion],* die u vereist om een munt te selecteren en de waarde voor elke omzetting in te gaan.

* *[!UICONTROL Use a different value for each conversion],* die u vereist om een munt te selecteren en een standaardwaarde voor elke omzetting in te gaan. U kunt de standaardwaarde in de tag wijzigen met een transactiespecifieke waarde wanneer u de tag implementeert op een specifieke webpagina.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [&#x200B; hoeveel omzettingen per klik of interactie te tellen &#x200B;](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* of *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Het maximumaantal dagen na een advertentietransactie waarvoor omzettingen worden geregistreerd. Voor zoek-, weergave- en winkelcampagnes kan het venster 1-90 dagen lang zijn. Selecteer een getal of selecteer **[!UICONTROL Custom]** en voer een getal in.

**[!UICONTROL View Through Conversion Window]:** Het maximumaantal dagen nadat een gebruiker uw advertenties bekijkt waarvoor mening-door omzettingen worden geregistreerd. Voor zoek-, weergave- en winkelcampagnes kan het venster 1-90 dagen lang zijn. Selecteer een getal of selecteer **[!UICONTROL Custom]** en voer een getal in.

**[!UICONTROL Attribution Model]:** [&#x200B; hoeveel krediet elke ad interactie &#x200B;](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138) krijgt: *[!UICONTROL Data driven]* of *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [&#x200B; upload off-line omzettingsgegevens voor verbeterde omzettingen &#x200B;](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [&#x200B; voer  [!DNL Google Ads]  verbeterde omzettingen voor lood &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md) uit
