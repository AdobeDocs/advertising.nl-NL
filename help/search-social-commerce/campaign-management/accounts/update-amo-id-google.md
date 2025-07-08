---
title: Werk identiteitskaart van AMO (s_kwcid) volgende code voor a  [!DNL Google Ads]  rekening bij
description: Leer hoe te aan de recentste het volgen code van identiteitskaart AMO voor a  [!DNL Google Ads]  rekening over te schakelen.
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# De trackingcode van de AMO-id (s_kwcid) voor een [!DNL Google Ads] -account bijwerken

*Advertisers met slechts integratie Adobe Advertising-Adobe Analytics*

*[!DNL Google Ads]alleen accounts*

De erfenis (voorafgaand aan Oktober 2019) formaat voor [ het volgen van identiteitskaart van AMO code ](/help/integrations/analytics/ids.md#amo-id-formats) voor bestaande [!DNL Google Ads] rekeningen steunt geen sommige eigenschappen in Analytics, zoals het melden bij de campagne en de groepsniveaus voor [!DNL Google Ads] prestaties maximumcampagnes, concepten en experimentatiecampagnes, en andere gebruiksgevallen waarin de zelfde combinatie ad+keyword+match in veelvoudige campagnes bestaat.

De huidige indeling bevat parameters voor campagne-id en groep-id:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

Voor een bestaande account die de oude indeling gebruikt, kunt u de huidige indeling wijzigen. Als u geen prestatiesmaximum campagnes of concepten en experimentatiecampagnes hebt, is het migreren dan aan het nieuwe formaat facultatief.

Alle nieuwe [!DNL Google Ads] accounts gebruiken automatisch de huidige indeling voor AMO-id&#39;s.

>[!NOTE]
>
>Deze optie is alleen beschikbaar voor accounts die de huidige indeling niet gebruiken.
>
>Nadat u een account hebt gemigreerd, worden alle klikgegevens, kosten en impliciete gegevens correct gerapporteerd na de wijziging. De doorklikgegevens die vóór de migratie zijn opgetreden, worden echter nog steeds toegewezen aan conversiegegevens die zijn gebaseerd op de oude indeling voor AMO-id.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]** . Klik in het submenu op **[!UICONTROL Live]** \> **[!UICONTROL Accounts]** .

1. Houd de curseur over de rekeningsnaam, klik ![ pijl dropdown pictogram ](/help/search-social-commerce/assets/arrow-dropdown-menu.png), en selecteer dan **[!UICONTROL Edit]**.

1. Klik op **[!UICONTROL Set Account Tracking]**.

1. Begin met de migratie:

   1. Klik op **[!UICONTROL S_KWCID FORMAT]** naast [!UICONTROL Account Tracking] in de **[!UICONTROL LEGACY S_KWCID FORMAT]** -instellingen.

   1. Klik op **[!UICONTROL Migrate to new s_kwcid format]**.

   1. Selecteer het selectievakje in het bevestigingsbericht en klik op **[!UICONTROL Continue]** .

   1. Klik op **[!UICONTROL Post]** in de accountinstellingen.

   Metagegevens voor de campagnes worden binnen een paar dagen bijgewerkt in [!DNL Analytics] . Het bijhouden wordt zonder onderbreking voortgezet, zodat er geen gegevens verloren gaan, maar de nieuwe volgcodes worden mogelijk pas in de rapportage opgenomen wanneer [!DNL Analytics] alle metagegevens ontvangt.

   >[!NOTE]
   >
   >Alle klikdoorhalingen die voorkwamen alvorens de migratie nog omzettingsgegevens rapporteerde die op het oude formaat worden gebaseerd.

1. Nadat u de migratie hebt gestart, werkt u desgewenst de instellingen voor het achtervoegsel van de bestemmingspagina (het zogenaamde &quot;laatste URL-achtervoegsel&quot; in sommige advertentienetwerken) bij:

   * Wanneer de functie [!UICONTROL Auto Upload] is ingeschakeld in de instellingen voor bijhouden, werkt Search, Social &amp; Commerce automatisch de code voor bijhouden bij in het achtervoegsel Landing Page voor dit account en de campagnes. Je hoeft niets te doen.

   * Wanneer de [!UICONTROL Auto Upload]&quot;eigenschap niet wordt toegelaten, en u gebruikt niet de [ server-kant AMO eigenschap van identiteitskaart ](/help/integrations/analytics/ids.md#amo-id-formats), dan moet u de AMO parameter van identiteitskaart in de het Bestaan montages van het Achtervoegsel van de Pagina manueel bijwerken. U kunt rekening en campagne-vlakke achtervoegsels manueel in de [ rekeningsmontages ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) veranderen en [ campagnemontages ](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) of door [ uploadend veranderingen in een bulksheet ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md). Als u een achtervoegsel wilt configureren op ad-groepsniveau of lager, gebruikt u de [!DNL Google Ads] -editor.

   * Als u de AMO-id opneemt in de Basis-URL-instelling voor een campagnecomponent, verplaatst u deze naar de desbetreffende instelling voor het achtervoegsel van de bestemmingspagina.

1. (Aanbevolen) Controleer de gegevens voor dit account in [!DNL Analytics] voordat u aanvullende accounts migreert.

>[!MORELIKETHIS]
>
>* [ beheer en netwerkrekeningen ](ad-network-account-manage.md)
>* [ Adobe Advertising IDs die door  [!DNL Analytics]](/help/integrations/analytics/ids.md) wordt gebruikt
>* [ Overzicht van  [!DNL Analytics for Advertising] ](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
