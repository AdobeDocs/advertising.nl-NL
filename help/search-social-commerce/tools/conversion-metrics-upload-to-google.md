---
title: Metrische gegevens voor het uploaden van zoekopdrachten, sociale gegevens en door Commerce bijgehouden conversies naar  [!DNL Google Ads]
description: Leer hoe u de conversiemetriek Zoeken, Sociaal en Commerce uploadt naar  [!DNL Google Ads] .
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Metrische gegevens voor het uploaden van zoekopdrachten, sociale gegevens en door Commerce bijgehouden conversies naar [!DNL Google Ads]

*Advertisers met [!DNL Google Ads] slechts rekeningen en de omzetting van Adobe Advertising het volgen*

Zoeken, sociale media en Commerce kunnen optioneel alle conversiemetriek die erin wordt bijgehouden uploaden naar [!DNL Google Ads] -campagnes die gebruikmaken van de service voor het bijhouden van conversies van Adobe Advertising. [!DNL Google Ads] Met deze optie zijn de conversies niet beschikbaar voor hybride optimalisatie. Als u uw omzettingen van Adobe voor hybride optimalisering wilt gebruiken, zie &quot;[ het uploaden van doelstellingen aan en netwerken ](objective-upload-to-networks.md) toelaten.&quot;

Dagelijkse uploads omvatten bijgehouden `gclid` waarde, de omzettingswaarde die gebruikend het adverteerder-vlakke attributiemodel wordt bepaald, en timestamp. Als het attributiemodel wordt bijgewerkt, dan gebruikt volgende uploadt het nieuwe model, maar het verleden gegevens wordt niet bijgewerkt om het nieuwe model te gebruiken.

>[!NOTE]
>
>De uploads bevatten geen conversiemetriek die vanuit feed-bestanden naar Adobe Advertising is geüpload.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]** .

1. Schakel het selectievakje naast **[!UICONTROL Upload Conversions to Google Ads]** in.

1. (Adverteerders die zaken doen in de Europese Economische Ruimte (EER) of het Verenigd Koninkrijk (VK); facultatief) Als u toestemming van gebruikers in de EER en het VK hebt verzameld om hun gegevens voor reclamedoeleinden te uploaden, selecteer dan het selectievakje naast **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klik op **[!UICONTROL Save]**.

1. (Als uw omzettingen op het niveau van de managerrekening worden gevolgd) [ voeg geloofsbrieven voor uw managerrekening ](/help/search-social-commerce/admin/manager-accounts.md) bij **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]** toe.

>[!MORELIKETHIS]
>
>* [ laat het uploaden van doelstellingen aan toe en netwerken ](objective-upload-to-networks.md)
