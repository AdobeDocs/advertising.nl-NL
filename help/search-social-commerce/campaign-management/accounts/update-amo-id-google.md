---
title: De trackingcode van de AMO-id (s_kwcid) bijwerken voor een [!DNL Google Ads] account
description: Leer hoe u overschakelt naar de nieuwste trackingcode voor AMO-id's voor een [!DNL Google Ads] account.
exl-id: 82168ee6-43bb-4b8d-882d-5254a1abcb09
feature: Search Campaign Management
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# De trackingcode van de AMO-id (s_kwcid) bijwerken voor een [!DNL Google Ads] account

*Adverteerders die alleen Adobe Advertising-Adobe Analytics-integratie hebben*

*[!DNL Google Ads]alleen accounts*

De oudere indeling voor de [Code voor bijhouden AMO-id](/help/integrations/analytics/ids.md#amo-id-formats) voor bestaande [!DNL Google Ads] accounts bieden geen ondersteuning voor bepaalde functies in Analytics, zoals rapportage op campagne- en advertentieniveau voor [!DNL Google Ads] maximale prestaties voor campagnes, concepten en experimentatiecampagnes en andere gebruiksgevallen waarin dezelfde combinatie van het type ad+keyword+match in meerdere campagnes bestaat.

De meest recente indeling bevat parameters voor campagne-id en groep-id:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

U kunt de nieuwe indeling wijzigen voor al uw bestaande accounts of voor al uw bestaande accounts afzonderlijk. Als u geen prestatiesmaximum campagnes of concepten en experimentatiecampagnes hebt, is het migreren dan aan het nieuwe formaat facultatief.

Alle nieuwe [!DNL Google Ads] accounts gebruiken automatisch de nieuwe indeling voor AMO-id.

>[!NOTE]
>
>Nadat u een account hebt gemigreerd, worden alle klikgegevens, kosten en impliciete gegevens correct gerapporteerd na de wijziging, maar eventuele doorklikgegevens die vóór de migratie zijn opgetreden, worden nog steeds toegewezen aan conversiegegevens die zijn gebaseerd op de oude indeling voor AMO-id.

1. Klik in het hoofdmenu op **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klik in het submenu op **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Houd de cursor boven de accountnaam en klik op ![pijlvervolgkeuzepictogram](/help/search-social-commerce/assets/arrow-dropdown-menu.png)en selecteer vervolgens **[!UICONTROL Edit]**.

1. Klik op **[!UICONTROL Set Account Tracking]**.

1. Begin met de migratie:

   1. Volgende tot **[!UICONTROL S_KWCID FORMAT]** , klikt u op **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. Klik op **[!UICONTROL Migrate to new s_kwcid format]**.

   1. Selecteer in het bevestigingsbericht het selectievakje en klik op **[!UICONTROL Continue]**.

   1. Klik in de accountinstellingen op **[!UICONTROL Post]**.

   Metagegevens voor de campagnes worden bijgewerkt in [!DNL Analytics] binnen een paar dagen. Het bijhouden wordt zonder onderbreking voortgezet, zodat er geen gegevens verloren gaan, maar de rapportage geeft mogelijk pas de nieuwe volgcodes weer totdat [!DNL Analytics] ontvangt alle metagegevens.

   >[!NOTE]
   >
   >Alle klikdoorhalingen die voorkwamen alvorens de migratie nog omzettingsgegevens zal melden die op het oude formaat worden gebaseerd.

1. Nadat u de migratie hebt gestart, werkt u desgewenst de instellingen voor het achtervoegsel van de bestemmingspagina (het zogenaamde &quot;laatste URL-achtervoegsel&quot; in sommige advertentienetwerken) bij:

   * Wanneer de [!UICONTROL Auto Upload]De functie &quot; is ingeschakeld in de instellingen voor bijhouden, Zoeken, Sociale zaken en Handel werkt automatisch de code voor bijhouden bij in het achtervoegsel Landing Page voor dit account en de bijbehorende campagnes. Je hoeft niets te doen.

   * Wanneer de [!UICONTROL Auto Upload]De functie &quot; is niet ingeschakeld en u gebruikt de [AMO ID-functie aan serverzijde](/help/integrations/analytics/ids.md#amo-id-formats)Vervolgens moet u de parameter AMO ID handmatig bijwerken in de instellingen voor het achtervoegsel van de bestemmingspagina. U kunt achtervoegsels op account- en campagnereniveau handmatig wijzigen in de account- en campagne-instellingen of door wijzigingen te uploaden in een bulksheet. Om een achtervoegsel op het niveau van de ad groep of lager te vormen, gebruik [!DNL Google Ads] editor.

   * Als u de AMO-id opneemt in de Basis-URL-instelling voor een campagnecomponent, verplaatst u deze naar de desbetreffende instelling voor het achtervoegsel van de bestemmingspagina.

1. (Aanbevolen) Controleer de gegevens voor dit account in [!DNL Analytics] voordat je aanvullende accounts migreert.

>[!MORELIKETHIS]
>
>* [Netwerkaccounts beheren](ad-network-account-manage.md)
>* [Adobe Advertising-id&#39;s gebruikt door [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Overzicht van [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
