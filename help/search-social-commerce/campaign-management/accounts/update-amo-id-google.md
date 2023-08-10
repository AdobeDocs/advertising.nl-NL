---
title: De trackingcode van de AMO-id (s\_kwcid) bijwerken voor een [!DNL Google Ads] account
description: Leer hoe u overschakelt naar de nieuwste trackingcode voor AMO-id's voor een [!DNL Google Ads] account.
exl-id: 82168ee6-43bb-4b8d-882d-5254a1abcb09
feature: Search Campaign Management
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# De s_kwcid-trackingcode bijwerken voor een [!DNL Google Ads] account

*Adverteerders die alleen Adobe Advertising-Adobe Analytics-integratie hebben*

*[!DNL Google Ads]alleen accounts*

De oudere indeling voor de s\_kwcid-trackingcode voor bestaande [!DNL Google Ads] accounts bieden geen ondersteuning voor bepaalde functies in Analytics, zoals rapportage op campagne- en advertentieniveau voor [!DNL Google Ads] maximale prestaties voor campagnes, concepten en experimentatiecampagnes en andere gebruiksgevallen waarin dezelfde combinatie van het type ad+keyword+match in meerdere campagnes bestaat.

De meest recente indeling bevat parameters voor campagne-id en groep-id:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

U kunt de nieuwe indeling wijzigen voor al uw bestaande accounts of voor al uw bestaande accounts afzonderlijk. Als u geen prestatiesmaximum campagnes of concepten en experimentatiecampagnes hebt, is het migreren dan aan het nieuwe formaat facultatief.

Alle nieuwe [!DNL Google Ads] accounts gebruiken automatisch de nieuwe notatie s\_kwcid.

>[!NOTE]
>
>Nadat u een account hebt gemigreerd, worden alle klikgegevens, kosten en impliciete gegevens correct gerapporteerd na de wijziging. De doorklikgegevens die vóór de migratie zijn opgetreden, worden echter nog steeds toegewezen aan conversiegegevens die zijn gebaseerd op de oude s\_kwcid-indeling.

1. Klik in het hoofdmenu op **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klik in het submenu op **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.
1. Houd de cursor boven de accountnaam en klik op ![pijlvervolgkeuzepictogram](/help/search-social-commerce/assets/arrow-dropdown-menu.png)en selecteer vervolgens **[!UICONTROL Edit]**.
1. Klik op **[!UICONTROL Set Account Tracking]**.
1. Begin met de migratie:

   1. Volgende tot **[!UICONTROL S_KWCID FORMAT]** , klikt u op **[!UICONTROL LEGACY S_KWCID FORMAT]**.
   1. Klik op **[!UICONTROL Migrate to new s_kwcid format]**.
   1. Selecteer in het bevestigingsbericht het selectievakje en klik op **[!UICONTROL Continue]**.
   1. Klik in de accountinstellingen op **[!UICONTROL Post]**.

   Metagegevens voor de campagnes worden binnen een paar dagen bijgewerkt in Analytics. Het bijhouden wordt zonder onderbreking voortgezet, zodat er geen gegevens verloren gaan, maar de nieuwe volgcodes worden mogelijk pas in de rapportage opgenomen als Analytics alle metagegevens ontvangt.

   >[!NOTE]
   >
   >Alle klikdoorhalingen die voorkwamen alvorens de migratie nog omzettingsgegevens zal melden die op het oude formaat worden gebaseerd.

1. Nadat u de migratie hebt gestart, werkt u desgewenst de instellingen voor het achtervoegsel van de bestemmingspagina (het zogenaamde &quot;laatste URL-achtervoegsel&quot; in sommige advertentienetwerken) bij:

   * Wanneer de [!UICONTROL Auto Upload]De functie &quot; is ingeschakeld in de instellingen voor bijhouden, Zoeken, Sociale zaken en Handel werkt automatisch de code voor bijhouden bij in het achtervoegsel Landing Page voor dit account en de bijbehorende campagnes. Je hoeft niets te doen.
   * Wanneer de [!UICONTROL Auto Upload]De functie &#39;&#39; is niet ingeschakeld en u gebruikt de parameter s-kwcid aan de serverzijde niet. Vervolgens moet u de parameter s\_kwcid handmatig bijwerken in de instellingen voor het achtervoegsel voor de landingspagina. U kunt achtervoegsels op account- en campagnereniveau handmatig wijzigen in de account- en campagne-instellingen of door wijzigingen te uploaden in een bulksheet. Om een achtervoegsel op het niveau van de ad groep of lager te vormen, gebruik [!DNL Google Ads] editor.
   * Als u s\_kwcid in het Basis URL plaatsen voor om het even welke campagnecomponent, dan verplaats het naar het relevante het Bestanden plaatsen van het Achtervoegsel van de Pagina.

1. (Aanbevolen) Controleer de gegevens voor dit account in Analytics voordat u aanvullende accounts migreert.

>[!MORELIKETHIS]
>
>* [Netwerkaccounts beheren](ad-network-account-manage.md)
>* [De parameter voor het bijhouden van AMO-id&#39;s](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md)
>* [Overzicht van [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
