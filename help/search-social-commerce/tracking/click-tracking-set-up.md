---
title: Op cookie gebaseerde klik bijhouden instellen
description: Leer hoe u kliktrackinglabels instelt en valideert.
exl-id: 3f2b09bc-9794-41d1-89fc-0d239bad2fb1
feature: Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Op cookie gebaseerde klik bijhouden instellen

Als u wilt dat zoekopdrachten, sociale gegevens en Commerce bijhouden, moeten de volgende elementen zijn geconfigureerd en gevalideerd.

1. (Adobe-accountteam) Stel de adverteerder in als een pixelklant.

1. [ specificeer de correcte het volgen opties voor elk van de adverteerders rekeningen van het advertentienetwerk en campagnes ](#set-up-click-tracking-options).

1. Indien noodzakelijk, [ produceert het volgen URLs en uploadt hen ](#generate-upload-tracking-urls) voor sommige campagneelementen.

1. [ bevestigt het formaat van een paar klik volgende URLs, en test hen om te bevestigen dat de correcte het landen pagina ](#validate-tracking-urls) opent.

## Opties instellen voor het bijhouden van advertenties voor netwerkaccounts en campagnes {#set-up-click-tracking-options}

*de rekeningsmanager van het Agentschap, [!DNL Adobe] rekeningsmanager, en slechts de rollen van de beheerdergebruiker*

1. Voer voor elke advertentie-netwerkaccount de volgende handelingen uit:

   1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** . Klik in de submenu&#39;s op **[!UICONTROL Live]>[!UICONTROL Accounts]** .

   1. Houd de curseur over de rekeningsnaam, het pictogram van het Menu ![&#128279;](/help/search-social-commerce/assets/arrow-dropdown-menu.png " pictogram van het Menu ") klikken, en dan selecteren **[!UICONTROL Edit]**.

   1. Klik op **[!UICONTROL Set Account Tracking]**.

   1. Selecteer **[!UICONTROL EF Redirect]** voor de instelling [!UICONTROL Tracking Type] .

   1. (Als u Zoeken, Sociaal en Commerce wilt toestaan gegevens uit te wisselen met Adobe Analytics of conversies wilt bijhouden die plaatsvinden in [!DNL Apple Safari] ) selecteert u de optie [!UICONTROL Redirect Type] **[!UICONTROL Token]** .

   1. (Optioneel) Schakel de optie **[!UICONTROL Auto Upload]** in om automatisch nieuwe URL&#39;s voor tekstspatiëring te uploaden naar het advertentienetwerk wanneer u deze URL&#39;s de volgende keer synchroniseert met Zoeken, Sociaal en Commerce. Deze waarde wordt overgeërfd als standaardwaarde voor alle campagnes in de account, maar kan op campagneniveau worden overschreven.

1. Ga voor elke campagne als volgt te werk:

   1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** . Klik in de submenu&#39;s op **[!UICONTROL Live]>[!UICONTROL Campaigns]** .

   1. Houd de curseur over de campagnenaam, het pictogram van het Menu ![&#128279;](/help/search-social-commerce/assets/arrow-dropdown-menu.png " pictogram van het Menu ") klikken, en dan selecteren **[!UICONTROL Edit]**.

   1. Klik op **[!UICONTROL Set Campaign Tracking]**. Selecteer vervolgens de optie die u wilt **[!UICONTROL Override Account Tracking]** gebruiken.

   1. Selecteer **[!UICONTROL EF Redirect]** voor de instelling [!UICONTROL Tracking Type] .

   1. (Als u Zoeken, Sociaal en Commerce wilt toestaan gegevens uit te wisselen met Adobe Analytics of conversies wilt bijhouden die plaatsvinden in [!DNL Apple Safari] ) selecteert u de optie [!UICONTROL Redirect Type] **[!UICONTROL Token]** .

   1. (Optioneel) Schakel de optie **[!UICONTROL Auto Upload]** in om automatisch nieuwe URL&#39;s voor tekstspatiëring te uploaden naar het advertentienetwerk wanneer u deze URL&#39;s de volgende keer synchroniseert met Zoeken, Sociaal en Commerce. Deze waarde wordt overgeërfd als standaardwaarde voor alle campagnes in de account, maar kan op campagneniveau worden overschreven.

## URL&#39;s voor bijhouden genereren en uploaden {#generate-upload-tracking-urls}

Zie &quot;[ wanneer en hoe te om klik-volgende URLs ](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) te produceren.&quot;

### De indeling van URL&#39;s die klikken bijhouden testen {#validate-tracking-urls}

Valideer dat de juiste landingspagina wordt geopend voor de URL voor het bijhouden van klikken.

1. Een advertentie simuleren door verkeer naar de testomgeving van de adverteerder te sturen:

   1. Plak in een teksteditor een URL voor het bijhouden van klikken, wijzig de URL van de bestemmingspagina zodat deze naar dezelfde pagina verwijst in de staging-omgeving van de adverteerder en plak vervolgens de nieuwe URL in de adresbalk van uw browser en druk op **[!DNL Enter]** .

   1. Zoek de cookie in de opgeslagen cookies van uw browser.

   1. Voltooi een transactie op de testsite en controleer of de succespagina de juiste pixel in werking stelt. De werkelijke parameters die door de pixel worden bijgehouden, variëren per adverteerder en URL bijhouden. In het volgende voorbeeld wil de adverteerder het aantal nieuwe toepassingen en het bedrag van nieuwe inkomsten bijhouden:

      Voor een nieuwe eindgebruiker (met een vers cookie) moet de volgende pixel worden geactiveerd:

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      Als de cookie niet vers is, moet de volgende pixel worden geactiveerd:

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. Herhaal deze bewerking voor meerdere klik op URL&#39;s bijhouden in het domein.

1. Herhaal Stap 1 voor elk domein, gebruikend een verschillende het landen pagina dienovereenkomstig.

1. Bevestig zo nodig dat Search, Social en Commerce de pixels kunnen zien voor de transactie-id&#39;s (`ev_transid`) die tijdens het testen worden gegenereerd.

>[!MORELIKETHIS]
>
>* [ wanneer en hoe te om klik-volgende URLs te produceren ](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
