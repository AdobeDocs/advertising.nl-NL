---
title: Reauthenticate a [!DNL Google Analytics]  gegevensbron
description: Leer hoe te om a  [!DNL Google Analytics]  gegevensbron opnieuw voor authentiek te verklaren als u het bijbehorende wachtwoord verandert of het certificaat verloopt.
role: User, Admin
exl-id: 624f0f0e-3f2f-45b1-b3dc-c1b107b4736f
feature: Search Admin, Search Data Sources
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Een [!DNL Google Analytics] -gegevensbron opnieuw verifiëren

*de Beheerders van het Agentschap, de Managers van de Rekening van het Agentschap, de Managers van de Rekening van Adobe, en slechts Beheerders*

Als u het wachtwoord wijzigt voor het e-mailaccount dat wordt gebruikt voor een gegevensbron, of als het [!DNL OAuth] -certificaat voor de account vervalt, worden alle open verbindingen met de e-mailaccount gesloten en moet u opnieuw verifiëren of u de synchronisatie van gegevens wilt hervatten.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]** .

1. Schakel het selectievakje in naast de gegevensbron die u opnieuw wilt verifiëren.

1. In de toolbar boven de gegevenslijst, geeft de klik ![ ](/help/search-social-commerce/assets/edit.png " uit ").

1. Bewerk de [ montages van de gegevensbron ](data-source-settings.md):

   1. Ga als volgt te werk in de sectie [!UICONTROL Connect to Google Analytics] .

      1. (Indien nodig) Voer een nieuw e-mailadres in voor toegang tot gegevens voor deze gegevensbron. Het e-mailadres moet zijn geregistreerd bij een [!DNL Google] -account en de machtiging &quot;Lezen en analyseren&quot; hebben voor de [!DNL Google Analytics] -account. Zie de [ instructies voor het toewijzen van gebruikerstoestemmingen in  [!DNL Google Analytics] ](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Meld u aan met een e-mailadres dat alleen toegang heeft tot die eigenschappen en weergaven, om ervoor te zorgen dat alleen specifieke [!DNL Google Analytics] -eigenschappen en -weergaven beschikbaar zijn in Zoeken, Sociaal en Commerce.

   1. Schakel het selectievakje in om Zoeken, Sociaal en Commerce toegang te geven tot gegevens voor het account.

   1. Klik op **[!UICONTROL Re-Authenticate]**.

1. Klik op **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [ Ongeveer synchroniserend  [!DNL Google Analytics]  omzettingsmetriek ](data-source-about.md)
>* [ Vereisten om a  [!DNL Google Analytics]  gegevensbron ](data-source-prerequisites.md) te vormen
>* [ vorm a  [!DNL Google Analytics]  mening als gegevensbron ](data-source-configure.md)
>* [ geef a  [!DNL Google Analytics]  gegevensbron ](data-source-edit.md) uit
>* [ de synchronisatie van de pauze van een gegevensbron ](data-source-pause.md)
>* [[!DNL Google Analytics]  gegevensbronmontages ](data-source-settings.md)
>* [ Bijlage - Beschikbare  [!DNL Google Analytics]  metriek ](data-source-ga-metrics.md)
