---
title: Maken [!DNL Google Ads] klant stemt doelgroep van [!DNL Adobe] publiek
description: Leer hoe u creeert [!DNL Google Ads] klanten komen hetzelfde publiek aan als uw bestaande Adobe Analytics- en Audience Manager-publiek.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# Maken [!DNL Google Ads] klantvriendelijkheid van Adobe Analytics en publiek van Audience Managers

*[!DNL Google Ads]accounts die alleen in aanmerking komen voor overeenkomst met klanten*

*Adverteerders met alleen de integratie Adobe Advertising-Adobe Audience Manager of Adobe Advertising-Adobe Analytics*

Geopende adverteerders kunnen [!DNL Google Ads] klant stemt publiek overeen gebruikend gebruiker - identiteitskaart van a) [!DNL Analytics] segmenten die worden gedeeld met Adobe Experience Cloud en b) de segmenten van de Audience Manager die Onderzoek, Sociale, &amp; Handel als bestemming hebben, met inbegrip van [!DNL Analytics] segmenten die worden gepubliceerd naar Adobe Experience Cloud en segmenten die worden gemaakt met de Adobe Experience Cloud Audience Library. Met Zoeken, Sociaal en Handel wordt automatisch een [!DNL Google] URL bijhouden naar elke URL [!DNL Analytics] of Audience Manager, zodat [!DNL Google] kan het publiek volgen.

Elk [!DNL Adobe] het publiek kan slechts voor één worden gebruikt [!DNL Google] publiek.

Elke nieuwe [!DNL Google] publiek heeft dezelfde naam als het origineel [!DNL Adobe] publiek. [!DNL Google] bepaalt hoe groot de doelgroep moet zijn.

>[!TIP]
>
>Voor segmentatie in real time, gebruik Audience Manager-gecreeerd publiek. Segmenten gemaakt in [!DNL Analytics] en gesynchroniseerd met Adobe Experience Cloud kunnen kleinere populaties hebben omdat ze alleen dagelijks gesynchroniseerd zijn; een surfer die voor een segment in aanmerking komt, mag pas de volgende dag in het segment worden opgenomen. Segmenten van [!DNL Analytics] hebben een gegevensbron van &quot;rapportreeks -.&quot;

>[!NOTE]
>
>Met Zoeken, Sociaal en Handel worden geen van de klantgegevens van uw [!DNL Adobe] segmenten die worden gebruikt voor het maken of bewerken van een [!DNL Google] publiek.

1. Vul de vereiste vereisten naar wens in:

   1. (Als u een publiek wilt maken met een vervolgkeuzelijst voor gebruikers-id&#39;s) Een [!DNL Adobe] de beheerder gebruiker of de rekeningsmanager moet de adverteerder-vlakke plaatsen selecteren om klant gelijke publiek toe te laten. De instellingen verschillen tussen adverteerders met Audience Manager en adverteerders met [!DNL Analytics] alleen.

   1. Implementeer de [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en) versie 2.0 of hoger.

   1. Gebruik de volgende tag zo hoog mogelijk op de webpagina&#39;s van de adverteerder waaruit het publiek moet worden bijgehouden

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      waar `Advertising_Cloud_UserID` Dit is de unieke gebruikersnaam die aan de adverteerder is toegewezen. Voorbeeld:  `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Indien nog niet voltooid) Een geautoriseerde gebruiker moet de account van de adverteerder configureren naar [synchroniseren met de organisatieaccount van de adverteerder in Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klik op de werkbalk boven de tabel met gegevens op ![Maken](/help/search-social-commerce/assets/add.png "Maken").

1. Selecteer het advertentienetwerk en de accountnaam en klik vervolgens op **[!UICONTROL Continue]**.

1. Geef de publieksinformatie op:

   1. In de **[!UICONTROL Data Source]** menu, selecteert u **[!UICONTROL Adobe Audience]**.

   1. Selecteer [!UICONTROL Adobe Audience] waarop de [!DNL Google] publiek.

      >[!NOTE]
      >
      >[!DNL Adobe] publiek dat al voor een andere [!DNL Google] publiek is niet beschikbaar.

      U kunt optioneel zoeken naar soorten publiek die een specifieke tekstreeks met minimaal drie tekens bevatten. Klik voor een passend publiek op **[!UICONTROL Include]** om het te selecteren.

      Als u meerdere [!DNL Adobe] publiek, vervolgens een aparte [!DNL Google] het publiek wordt voor elk gecreeerd.

   1. Selecteer **[!UICONTROL Audience Type]** maken: **[!UICONTROL Customer List_User ID]**.

      De adverteerders [!DNL Google Ads] account moet [in aanmerking komend voor aangepaste match](https://support.google.com/adspolicy/answer/6299717) en heeft ervoor gekozen [hermarketing van gebruikersnaam](https://support.google.com/google-ads/answer/9199250).

   1. Schakel het selectievakje in om aan te geven dat u akkoord gaat met de voorwaarden van het dialoogvenster [!DNL Adobe] en voegt beleid van de netwerkprivacy toe.

   1. Geef het aantal **[!UICONTROL Membership Days]**, dit is het aantal dagen dat de cookie van een gebruiker in het publiek blijft.

      Gebruik de tijdsduur waarvan u verwacht dat uw advertentie relevant is voor de gebruiker. De lijsten van het opmerken hebben een maximumduur van 540 dagen. Klantlijsten hebben geen maximale duur; Voer 10000 in om aan te geven dat het cookie nooit verloopt.

   1. Klik op **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] Het kan 24 uur duren voordat het bestand is verwerkt.
>
>* Zie [[!DNL Google Ads] documentatie over de werking en de beperkingen van klantenovereenkomsten](https://support.google.com/displayvideo/answer/9539301).


>[!MORELIKETHIS]
>
>* [Informatie over publiek](audience-about.md)
>* [Een [!DNL Google Ads] klant stemt publiek van een Adobe Campaign e-maillijst overeen](google-audience-from-campaign-email-list.md)
>* [Beheer klanten gelijke soorten publiek gebruikend de lijsten van klantengegevens](audience-from-customer-data-list.md)
>* [Dynamisch publiek voor opnieuw op de markt brengen beheren](audience-dynamic-remarketing-manage.md)

