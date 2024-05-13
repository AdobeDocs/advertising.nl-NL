---
title: Wanneer worden accountcomponenten gemaakt of verwijderd door voorraadfeeds?
description: Leer welke situaties accountcomponenten maken en verwijderen wanneer u voorraadfeeds plaatst.
exl-id: 39a3cc2c-f956-4a89-a69d-687a27a38a1e
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---

# Wanneer worden accountcomponenten gemaakt of verwijderd door voorraadfeeds?

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

Wanneer een dossier van de inventarisvoer door een malplaatje wordt verspreid, worden de rekeningscomponenten gecreeerd en als volgt geschrapt.

>[!NOTE]
>
>Er worden nooit dubbele advertenties gemaakt in een advertentiegroep.

| Scenario | Voorbeeld | Handeling |
|----|----|----|
| De gegevens van het voer omvatten een nieuwe waarde voor een kolom die in een campagnenaam, een groepsnaam, een sleutelwoord, of een productgroep wordt gebruikt. | Vorige bestanden:<br>Campaign=Hats<br>Campaign=Ghandschoenen<br><br>Nieuw bestand:<br>Campaign=Shoes | Er wordt een nieuwe campagne, advertentiegroep, trefwoord of productgroep gemaakt als deze niet bestaat op het advertentienetwerk. |
| Diervoedergegevens bevatten een nieuwe waarde voor een kolom die in een advertentie wordt gebruikt. | Vorig bestand: een advertentie inclusief prijs=20<br><br>Nieuw bestand: voor dezelfde advertentie is price=10 | Wanneer de advertentie wordt gekopieerd voor [!DNL Microsoft Advertising] uitgebreide tekstadvertenties, [!DNL Yahoo! Japan ads], of [!DNL Yandex] advertenties worden gewijzigd, de bestaande advertentie wordt verwijderd en er wordt een nieuwe advertentie gemaakt.<br><br>Wanneer een advertentiekopie wordt gewijzigd voor andere advertentietypes of wanneer de toepasselijke kolom voor een [!DNL Google Ads] ad, parameter ({param1} of {param2}) in een advertentie, wordt de bestaande advertentie bijgewerkt. |
| De malplaatjemontages voor de campagne, en de groep, het sleutelwoord, of de productgroep veranderden sinds de laatste propagatie. | Vorige instelling:Trefwoord=[Trefwoord]<br><br>Nieuwe instelling: Trefwoord=&lt;color>[Trefwoord] | Er wordt een nieuwe campagne, advertentiegroep, trefwoord of productgroep gemaakt als deze niet bestaat op het advertentienetwerk. |
| De malplaatjemontages voor een advertentie veranderden sinds de laatste propagatie. | Vorige instelling: beschrijving toevoegen=&quot;Kopen [categorie] nu.&quot;<br><br>Nieuwe instelling: beschrijving toevoegen=&quot;Kopen [merk] nu.&quot; | Wanneer de advertentie wordt gekopieerd voor [!DNL Microsoft Advertising] uitgebreide tekstadvertenties, [!DNL Yahoo! Japan ads], of [!DNL Yandex] advertenties worden gewijzigd, de bestaande advertentie wordt verwijderd en er wordt een nieuwe advertentie gemaakt.<br><br>Wanneer een advertentiekopie wordt gewijzigd voor andere advertentietypes of wanneer de verandering op een verandering in kolom wijst die voor één wordt gebruikt [!DNL Google Ads] ad, parameter ({param1} of {param2}) in een advertentie, wordt de bestaande advertentie bijgewerkt. |
| Nieuwe voedergegevens omvatten geen rij voor een bestaande campagne of een advertentiegroep. | nvt | De bestaande campagnes en advertentiegroepen blijven ongewijzigd. |
| Nieuwe feed-gegevens bevatten geen rij voor een bestaande advertentiegroep, advertentie, trefwoord of productgroep. | nvt | De bestaande advertentiegroep, advertentie, trefwoord of productgroep blijft &#39;as-is&#39;, wordt gepauzeerd of verwijderd volgens de instructies [gegevensinstellingen van feed](feed-settings-manage.md#feed-data-settings). |
| Nieuwe voedergegevens voor een bestaande ouderproductgroep omvatten geen rijen voor zijn bestaande kindproductgroepen. | nvt | De bestaande bovenliggende productgroep blijft ongewijzigd of wordt verwijderd volgens de [gegevensinstellingen van feed](feed-settings-manage.md#feed-data-settings). <b>Opmerking:</b> Als de montages van voedergegevens worden gevormd om ontbrekende lijnpunten te pauzeren, dan wordt de ouderproductgroep nog geschrapt omdat u geen productgroepen kunt pauzeren. |
| De nieuwe voedergegevens omvatten een rij voor een advertentiegroep, een advertentie, een sleutelwoord, of een productgroep die a) in vorige gegevens was maar b) sindsdien werd weggelaten en volgens [gegevensinstellingen van feed](feed-settings-manage.md#feed-data-settings). | nvt | De bestaande advertentiegroep, advertentie, trefwoord of productgroep wordt opnieuw geactiveerd, zonder dat er geschiedenis of kwaliteitsscore verloren gaat. |
| De nieuwe voedergegevens omvatten een rij voor een advertentiegroep, een advertentie, een sleutelwoord, of een productgroep die a) in vorige gegevens was maar b) sindsdien werd weggelaten en volgens [gegevensinstellingen van feed](feed-settings-manage.md#feed-data-settings). | nvt | Er wordt een nieuwe advertentiegroep, advertentie, trefwoord of productgroep gemaakt. |
| U hebt de optie op campagne- of advertentieniveau uitgeschakeld naar &quot;[!UICONTROL Delete negative keywords when omitted from list].&quot; | De negatieve trefwoordenlijst bevat &quot;coupe&quot; en &quot;sport car&quot;.<br><br>De ad-groep bevat al het negatieve trefwoord &quot;SUV&quot;. | Eventuele negatieve trefwoorden die niet in de lijst staan, blijven ongewijzigd. |
| U hebt de optie op campagne- of advertentieniveau ingeschakeld op &quot;[!UICONTROL Delete negative keywords when omitted from list],&quot; en negatieve trefwoorden die niet in de lijst staan, bestaan. | De negatieve trefwoordenlijst bevat &quot;coupe&quot; en &quot;sport car&quot;.<br><br>De ad-groep bevat al het negatieve trefwoord &quot;SUV&quot;. | Eventuele niet-opgegeven negatieve trefwoorden die eerder met de sjabloon zijn gemaakt, worden verwijderd wanneer een feed-bestand via de sjabloon wordt doorgegeven. Niet-opgegeven negatieve trefwoorden die op andere manieren zijn gemaakt (bijvoorbeeld in normale bulksbladen, [!UICONTROL Campaigns] weergaven (of in de advertentie-editor van het advertentienetwerk) blijven ongewijzigd. | | De geplande einddatum voor de componenten van een gepost voederdossier komt voor. | nvt | De bestaande campagnes blijven ongewijzigd. De bestaande advertentiegroepen, advertenties en trefwoorden blijven ongewijzigd, worden gepauzeerd of verwijderd volgens de [gegevensinstellingen van feed](feed-settings-manage.md#feed-data-settings). |
| Het voorraadniveau van een artikel daalt tot onder het in de [gegevensinstellingen van feed](feed-settings-manage.md#feed-data-settings). | Vorig bestand: stock=10<br><br>Nieuw bestand: stock=0 | De bestaande campagnes blijven ongewijzigd. De bestaande advertentiegroepen, advertenties, trefwoorden en productgroepen worden gepauzeerd of verwijderd volgens de [gegevensinstellingen van feed](feed-settings-manage.md#feed-data-settings). |
| Het voorraadniveau van een artikel ligt weer boven het in de [gegevensinstellingen van feed](feed-settings-manage.md#feed-data-settings). | Vorig bestand: stock=0<br><br> Nieuw bestand: stock=10 | Wanneer de bestaande advertenties, trefwoorden of productgroepen zijn gepauzeerd, worden ze opnieuw geactiveerd, zonder dat er geschiedenis of kwaliteitsscore verloren gaat. Als er geen advertenties, trefwoorden of productgroepen bestaan (bijvoorbeeld als deze eerder zijn verwijderd omdat het voorraadniveau onder het minimum lag), worden er nieuwe gemaakt. |

>[!MORELIKETHIS]
>
>* [Informatie over het automatiseren en beheren van voorraden](inventory-feeds-about.md)
