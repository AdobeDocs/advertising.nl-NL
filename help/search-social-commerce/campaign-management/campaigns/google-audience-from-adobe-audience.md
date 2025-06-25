---
title: Creeer  [!DNL Google Ads]  publiek van de klantengelijke van  [!DNL Adobe]  publiek
description: Leer hoe te om  [!DNL Google Ads]  publiek van de klantengelijke van uw bestaand publiek van Adobe Analytics en van Audience Manager tot stand te brengen.
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Maak [!DNL Google Ads] klantovereenkomsten van Adobe Analytics- en Audience Manager-publiek

*[!DNL Google Ads]accounts die alleen in aanmerking komen voor overeenkomst met klanten*

*Advertisers met slechts integratie Adobe Advertising-Adobe Audience Manager of Adobe Advertising-Adobe Analytics*

Opted-in-adverteerders kunnen [!DNL Google Ads] klantovereenkomsten maken met gebruikers-id&#39;s van a) [!DNL Analytics] -segmenten die worden gedeeld met Adobe Experience Cloud en b) Audience Manager-segmenten die Search, Social en Commerce als doel hebben, inclusief [!DNL Analytics] -segmenten die worden gepubliceerd naar Adobe Experience Cloud en segmenten die worden gemaakt met de Adobe Experience Cloud Audience Library. Met Zoeken, Sociaal en Commerce wordt automatisch een URL voor [!DNL Google] bijhouden naar elk [!DNL Analytics] - of Audience Manager-segment teruggezet, zodat [!DNL Google] het publiek kan volgen.

Elke [!DNL Adobe] -doelgroep kan voor slechts één [!DNL Google] -doelgroep worden gebruikt.

Elk nieuw publiek van [!DNL Google] heeft de zelfde naam zoals het originele publiek van [!DNL Adobe]. [!DNL Google] bepaalt hoe groot de doelgroep moet zijn.

>[!TIP]
>
>Gebruik voor realtime segmentatie een publiek dat door Audience Manager is gemaakt. Segmenten die zijn gemaakt in [!DNL Analytics] en gesynchroniseerd met Adobe Experience Cloud, hebben mogelijk kleinere populaties omdat ze alleen dagelijks worden gesynchroniseerd. Een surfer die in aanmerking komt voor een segment, wordt mogelijk pas de volgende dag in het segment opgenomen. Segmenten uit [!DNL Analytics] hebben een gegevensbron met de naam &quot;report suite - .&quot;

>[!NOTE]
>
>In Zoeken, Sociaal en Commerce worden geen gegevens van klanten uit uw [!DNL Adobe] -segmenten opgeslagen die worden gebruikt om een [!DNL Google] -publiek te maken of te bewerken.

1. Vul de vereiste vereisten naar wens in:

   1. (Als u een publiek met een vervolgkeuzelijst voor gebruikers-id wilt maken) Een [!DNL Adobe] admin-gebruiker of accountmanager moet de instelling op adverteerderniveau selecteren om ervoor te zorgen dat het publiek van de klant overeenkomt.

   1. Voer [ versie 2.0 uit van de Identiteitsdienst van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/id-service/using/home.html) of hoger.

   1. Gebruik de volgende tag zo hoog mogelijk op de webpagina&#39;s van de adverteerder waaruit het publiek moet worden bijgehouden

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      waarbij `Advertising_Cloud_UserID` de unieke numerieke gebruikersnaam is die aan de adverteerder is toegewezen.

      Voorbeeld: `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Als niet reeds voltooid) een erkende gebruiker moet de rekening van de adverteerder vormen aan [ synchronisatie met de de organisatierekening van de adverteerder in Adobe Experience Cloud ](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** . Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** .

1. In de toolbar boven de gegevenslijst, leidt de klik ![ ](/help/search-social-commerce/assets/add.png " tot ").

1. Selecteer het advertentienetwerk en de accountnaam en klik op **[!UICONTROL Continue]** .

1. Geef de publieksinformatie op:

   1. Selecteer **[!UICONTROL Adobe Audience]** in het menu **[!UICONTROL Data Source]** .

   1. Selecteer de [!UICONTROL Adobe Audience] waarop u de doelgroep van [!DNL Google] wilt baseren.

      >[!NOTE]
      >
      >[!DNL Adobe] publiek dat al voor een ander [!DNL Google] publiek wordt gebruikt, is niet beschikbaar.

      U kunt optioneel zoeken naar soorten publiek die een specifieke tekstreeks met minimaal drie tekens bevatten. Voor een passend publiek klikt u op **[!UICONTROL Include]** om het te selecteren.

      Als u meerdere [!DNL Adobe] soorten publiek selecteert, wordt voor elk publiek een apart publiek van [!DNL Google] gemaakt.

   1. Selecteer de lus **[!UICONTROL Audience Type]** die u wilt maken: **[!UICONTROL Customer List_User ID]** .

      De rekening van adverteerder [!DNL Google Ads] moet [ voor douanegelijke ](https://support.google.com/adspolicy/answer/6299717) verkiesbaar zijn en binnen voor [ gebruiker - identiteitskaart remarketing ](https://support.google.com/google-ads/answer/9199250) verkozen.

   1. Schakel het selectievakje in om aan te geven dat u akkoord gaat met de voorwaarden van het [!DNL Adobe] -beleid en het privacybeleid van het netwerk.

   1. Geef het aantal **[!UICONTROL Membership Days]** op. Dit is het aantal dagen dat de cookie van een gebruiker in het publiek blijft.

      Gebruik de tijdsduur waarvan u verwacht dat uw advertentie relevant is voor de gebruiker. De lijsten van het opmerken hebben een maximumduur van 540 dagen. De lijsten van de klant hebben geen maximumduur; om erop te wijzen dat het koekje nooit verloopt, ga 10000 in.

   1. Klik op **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] kan 24 uur duren voordat het bestand is verwerkt.
>
>* Zie [[!DNL Google Ads]  documentatie op hoe de klantengelijken werken en beperkingen ](https://support.google.com/displayvideo/answer/9539301) aanpassen.

>[!MORELIKETHIS]
>
>* [ Ongeveer publiek ](audience-about.md)
>* [ creeer a [!DNL Google Ads]  publiek van de klantengelijke van een e-maillijst van Adobe Campaign ](google-audience-from-campaign-email-list.md)
>* [ beheer klant gelijke publiek gebruikend de lijsten van klantengegevens ](audience-from-customer-data-list.md)
>* [ beheer dynamische remarketing publiek ](audience-dynamic-remarketing-manage.md)
