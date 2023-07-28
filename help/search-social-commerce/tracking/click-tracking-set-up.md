---
title: Op cookie gebaseerde klik bijhouden instellen
description: Leer hoe u kliktrackinglabels instelt en valideert.
exl-id: 340aec08-a1a5-4aa5-b666-9c819c1709d0
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Op cookie gebaseerde klik bijhouden instellen

Voor Onderzoek, Sociale, &amp; Handel om kliks te volgen, moeten de volgende elementen worden gevormd en worden bevestigd.

1. (Het Team van de Rekening van Adobe) Opstelling adverteerder als pixelklant.

1. [Geef de juiste opties voor bijhouden op voor elk van de advertentienetwerkaccounts en campagnes van de adverteerder](#set-up-click-tracking-options).

1. Indien nodig [URL&#39;s genereren en uploaden](#generate-upload-tracking-urls) voor sommige campagneelementen.

1. [Valideer de indeling van een paar van de klikken die URL&#39;s bijhouden en test deze om te controleren of de juiste bestemmingspagina wordt geopend](#validate-tracking-urls).

## Opties instellen voor het bijhouden van advertenties voor netwerkaccounts en campagnes {#set-up-click-tracking-options}

*Accountmanager van het Agentschap, [!DNL Adobe] alleen accountmanager en beheerdersgebruikersrollen*

1. Voer voor elke advertentie-netwerkaccount de volgende handelingen uit:

   1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]>[!UICONTROL Accounts]**.

   1. Houd de cursor boven de accountnaam en klik op ![Menupictogram](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menupictogram")en selecteer vervolgens **[!UICONTROL Edit]**.

   1. Klik op **[!UICONTROL Set Account Tracking]**.

   1. Voor de [!UICONTROL Tracking Type] instellen, selecteren **[!UICONTROL EF Redirect]**.

   1. (Als u Zoeken, Sociaal, &amp; Handel wilt toestaan om gegevens uit te wisselen met Adobe Analytics of om conversies te volgen die plaatsvinden in [!DNL Apple Safari]) Selecteer de [!UICONTROL Redirect Type] option **[!UICONTROL Token]**.

   1. (Optioneel) Schakel de optie **[!UICONTROL Auto Upload]** optie om automatisch nieuwe het volgen URLs aan het advertentienetwerk te uploaden de volgende tijd dat Onderzoek, Sociale, &amp; Handel met het synchroniseert. Deze waarde wordt overgeërfd als standaardwaarde voor alle campagnes in de account, maar kan op campagneniveau worden overschreven.

1. Ga voor elke campagne als volgt te werk:

   1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

   1. Houd de cursor boven de naam van de campagne en klik op ![Menupictogram](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menupictogram")en selecteer vervolgens **[!UICONTROL Edit]**.

   1. Klik op **[!UICONTROL Set Campaign Tracking]**. Selecteer vervolgens de optie om **[!UICONTROL Override Account Tracking]**.

   1. Voor de [!UICONTROL Tracking Type] instellen, selecteren **[!UICONTROL EF Redirect]**.

   1. (Als u Zoeken, Sociaal, &amp; Handel wilt toestaan om gegevens uit te wisselen met Adobe Analytics of om conversies te volgen die plaatsvinden in [!DNL Apple Safari]) Selecteer de [!UICONTROL Redirect Type] option **[!UICONTROL Token]**.

   1. (Optioneel) Schakel de optie **[!UICONTROL Auto Upload]** optie om automatisch nieuwe het volgen URLs aan het advertentienetwerk te uploaden de volgende tijd dat Onderzoek, Sociale, &amp; Handel met het synchroniseert. Deze waarde wordt overgeërfd als standaardwaarde voor alle campagnes in de account, maar kan op campagneniveau worden overschreven.

## URL&#39;s voor bijhouden genereren en uploaden {#generate-upload-tracking-urls}

Zie &quot;[Wanneer en hoe te om klik-volgende URLs te produceren](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

### De indeling van URL&#39;s die klikken bijhouden testen {#validate-tracking-urls}

Valideer dat de juiste landingspagina wordt geopend voor de URL voor het bijhouden van klikken.

1. Een advertentie simuleren door verkeer naar de testomgeving van de adverteerder te sturen:

   1. Plak in een teksteditor een URL voor het bijhouden van klikken, wijzig de URL van de bestemmingspagina zodat deze naar dezelfde pagina verwijst in de staging-omgeving van de adverteerder en plak vervolgens de nieuwe URL in de adresbalk van uw browser en druk op de knop **[!DNL Enter]** toets.

   1. Zoek de cookie in de opgeslagen cookies van uw browser.

   1. Voltooi een transactie op de testsite en controleer of de succespagina de juiste pixel in werking stelt. De werkelijke parameters die door de pixel worden bijgehouden, variëren per adverteerder en URL bijhouden. In het volgende voorbeeld wil de adverteerder het aantal nieuwe toepassingen en het bedrag van nieuwe inkomsten bijhouden:

      Voor een nieuwe eindgebruiker (met een vers cookie) moet de volgende pixel worden geactiveerd:

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      Als de cookie niet vers is, moet de volgende pixel worden geactiveerd:

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. Herhaal deze bewerking voor meerdere klik op URL&#39;s bijhouden in het domein.

1. Herhaal Stap 1 voor elk domein, gebruikend een verschillende het landen pagina dienovereenkomstig.

1. Bevestig zo nodig dat Search, Social en Commerce de pixels voor de transactie-id&#39;s kunnen zien (`ev_transid`) die tijdens de test worden gegenereerd.

>[!MORELIKETHIS]
>
>* [Wanneer en hoe te om klik-volgende URLs te produceren](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
