---
title: Een [!DNL Google Analytics] gegevensbron
description: Leer hoe u een [!DNL Google Analytics] gegevensbron als u het bijbehorende wachtwoord verandert of het certificaat verloopt.
role: User, Admin
exl-id: 9233e004-8607-444a-ba99-f63cb83a8b7a
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# Een [!DNL Google Analytics] gegevensbron

*Beheerders van agentschappen, accountmanagers van het Bureau, accountmanagers van Adobe en alleen beheerders*

Als u het wachtwoord wijzigt voor het e-mailaccount dat wordt gebruikt voor een gegevensbron, of als de [!DNL OAuth] Het certificaat voor de account verloopt. Vervolgens worden alle open verbindingen met de e-mailaccount gesloten en moet u opnieuw verifiëren om de synchronisatie van gegevens te hervatten.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Schakel het selectievakje in naast de gegevensbron die u opnieuw wilt verifiëren.

1. Klik op de werkbalk boven de tabel met gegevens op ![Bewerken](/help/search-social-commerce/assets/edit.png "Bewerken").

1. Bewerk de [gegevensbroninstellingen](data-source-settings.md):

   1. In de [!UICONTROL Connect to Google Analytics] , voert u de volgende handelingen uit.

      1. (Indien nodig) Voer een nieuw e-mailadres in voor toegang tot gegevens voor deze gegevensbron. Het e-mailadres moet bij een [!DNL Google] -account en beschikken over &quot;Lezen en analyseren&quot;-machtigingen voor de [!DNL Google Analytics] account. Zie de [instructies voor het toewijzen van gebruikersmachtigingen in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Alleen specifieke [!DNL Google Analytics] De eigenschappen en de meningen zijn beschikbaar binnen Onderzoek, Sociale, &amp; Handel, login gebruikend een e-mailadres dat toegang tot slechts die eigenschappen en meningen heeft.

   1. Schakel het selectievakje in om Zoeken, Sociale media en Handel toegang te geven tot statistieken voor de account.

   1. Klik op **[!UICONTROL Re-Authenticate]**.

1. Klik op **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Over synchroniseren [!DNL Google Analytics] conversiemetingen](data-source-about.md)
>* [Vereisten voor het configureren van een [!DNL Google Analytics] gegevensbron](data-source-prerequisites.md)
>* [Een [!DNL Google Analytics] weergeven als gegevensbron](data-source-configure.md)
>* [Een [!DNL Google Analytics] gegevensbron](data-source-edit.md)
>* [Synchronisatie van een gegevensbron pauzeren](data-source-pause.md)
>* [[!DNL Google Analytics] gegevensbroninstellingen](data-source-settings.md)
>* [Bijlage - beschikbaar [!DNL Google Analytics] cijfers](data-source-ga-metrics.md)
