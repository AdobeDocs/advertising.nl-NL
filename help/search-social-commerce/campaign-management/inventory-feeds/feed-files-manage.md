---
title: Bestanden voor de invoer van voorraadgegevens beheren
description: Leer hoe te om de montages te vormen die controleren hoe de voedergegevens worden verwerkt.
exl-id: 73d372de-2673-4190-94cf-2f07f4ce2493
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 0%

---

# Bestanden voor de invoer van voorraadgegevens beheren

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

Als u uw eigen feed-gegevens verzendt, moet u bestanden met uw productgegevens uploaden om op dynamische wijze op basis van uw productgegevens een campagnestructuur, advertenties en trefwoorden te maken. U kunt hen dan associëren met ad-netwerk-specifieke advertentiesjablonen en de gegevens door de malplaatjes verwerken, uiteindelijk het posten van de gegevens aan relevante ad netwerken. U kunt meerdere sjablonen aan een feed-bestand koppelen, maar elke sjabloon kan aan slechts één feed-bestand worden gekoppeld.

>[!NOTE]
>
>Upload geen bestanden als u gegevens rechtstreeks van een bedrijfscentrum gebruikt.

U kunt gegevensdoorvoerbestanden op een van de volgende manieren uploaden en verwerken:

* **Automatisch FTP gebruiken:** U kunt bestanden rechtstreeks uploaden naar een FTP-map. De service controleert elke twee uur of er nieuwe bestanden zijn. Nadat u een dossier voor het eerst uploadt, kunt u het met een ad netwerk-specifieke malplaatje associëren. Later worden alle bestanden die u met dezelfde naam uploadt, automatisch aan dezelfde sjabloon gekoppeld. Afhankelijk van hoe u [de instellingen voor de feed-gegevens configureren](feed-settings-manage.md), kan Zoeken, Sociaal, &amp; Handel de voedergegevens automatisch verspreiden door alle toepasselijke malplaatjes en naar keuze de resulterende campagne en advertentiegegevens aan de relevante advertentienetwerken posten.

  Neem contact op met het Adobe-accountteam als u een FTP-map wilt instellen voor het opslaan en automatisch verwerken van gegevensbestanden.

* **Handmatige verwerking:** U kunt handmatig [feed-bestanden uploaden](#feed-file-upload) van de [!UICONTROL Advanced] (ACM). Nadat u een feed-bestand aan een of meer ad-netwerkspecifieke bestanden hebt gekoppeld [sjablonen](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md), kunt u campagne- en advertentiegegevens genereren door [het verspreiden van de voedergegevens door de malplaatjes](feed-data-propagate.md) volgens de [gegevensinstellingen van feed](feed-settings-manage.md). U kunt naar keuze voorproef de geproduceerde gegevens binnen de meningen van de campagnehiërarchie, een bulksbladdossier voor overzicht produceren, of een bulksbladdossier voor directe post aan het ad netwerk produceren. Als u de gegevens niet onmiddellijk plaatst, kunt u [voorvertonen](propagated-data-view.md) en [plaatsen](propagated-data-post.md) later. U kunt [het bestaande feed-bestand vervangen door een nieuw bestand](#feed-file-replace) zonder bestaande sjabloonkoppelingen te verliezen.

## Vereisten voor een bestand met feed

Er zijn geen specifieke gegevensvelden vereist in een afzonderlijk bestand, maar voor elk bestand is het volgende vereist:

* De eerste regel in het bestand moet kolomnamen bevatten (ook wel *koppen*), die overeenkomen met de dynamische parameters in de bijbehorende sjablonen. De overige regels moeten gegevens bevatten die overeenkomen met de kolomnamen. Elke gegevensregel (rij) mag slechts op één accountcomponent betrekking hebben, zoals één campagne of één advertentie. De waarden op alle regels moeten door tabs of komma&#39;s van elkaar worden gescheiden. Zie de [CSV-voorbeeldbestand](#example-csv-feed-file) en [CSV-voorbeeldbestand](#example-tsv-feed-file) hieronder.

* Het bestand kan elke grootte hebben, maar moet een van de volgende bestandsextensies hebben: `.tsv` (voor tabgescheiden waarden), `.txt` (for [!DNL Unicode]-compatibele ASCII-tekst), `.csv` (voor door komma&#39;s gescheiden waarden), of `.zip` (voor één bestand in gecomprimeerde ZIP-indeling dat wordt uitgepakt naar een TSV-bestand).

* De bestandsnaam is hoofdlettergevoelig en kan de volgende tekens niet bevatten: `# % & * | \ : " < > . ? /`

* Als u bestanden in een FTP-map deponeert, moet u voor elke versie van het bestand dezelfde bestandsnaam gebruiken.

* ([!DNL Google Ads] alleen sjablonen) Als uw sjabloon de parameter Param2 of Param2 in tekstadvertenties gebruikt, moeten de bijbehorende gegevensvelden in het feed-bestand numerieke gegevens bevatten, zonder monetaire symbolen.

* Als u bestaande accountcomponenten wilt bijwerken, neemt u de naam van de bestaande campagne op (en de onderdelen ervan, indien van toepassing). Als de bestaande structuur niet wordt gespecificeerd, dan worden de nieuwe componenten gecreeerd.

### Voorbeeld van een voederbestand met komma&#39;s als scheidingsteken {#example-csv-feed-file}

```
Product Category,Product Name,Discount Percentage
electronics,iPods,10
apparel,Shirts,15
shoes,Clarks,20
```

### Voorbeeld van een feed met tabs als scheidingsteken {#example-tsv-feed-file}

```
Product Category<TAB>Product Name<TAB>Discount Percentage
electronics<TAB>iPods<TAB>10
apparel<TAB>Shirts<TAB>15
shoes<TAB>Clarks<TAB>20
```

## Aanbevolen procedures

* Gebruik bestanden in de indeling TSV of TXT voor gegevens die internationale tekens bevatten.

* Voor een herhaalbaar proces met beperkte handmatige revisie of bewerking stelt u als volgt feed-bestanden en de bijbehorende gegevens over de accountstructuur in:

   * Kolommen en rijen opnemen die voldoende gegevens bevatten om een accountstructuur te maken of een toewijzing te maken aan de bestaande accountstructuur. In het ideale geval gebruikt u een bestaande accountstructuur die nauw verbonden is met de producttaxonomie en waaraan de voedergegevens gemakkelijk kunnen worden toegewezen.

   * Beschrijvingen opnemen die kort genoeg zijn om te gebruiken in een advertentie.

   * Gebruik consistente gegevenspatronen en naamgevingsconventies in alle productrijen.

   * Alle voorafgaande spaties en afsluitende spaties verwijderen.

   * Verwijder onjuiste tekens.

## Een feed-bestand weergeven of downloaden

U kunt elk hoofdbestand openen of downloaden dat handmatig of met FTP is geüpload.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, die voor de [!UICONTROL Templates] tab.

1. Zoek het feed-bestand:

1. Zoek in de lijst met sjablonen een sjabloon die het feed-bestand gebruikt.

1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Feeds]** om een lijst met alle feed-bestanden te openen.

1. Klik op de naam van het feed-bestand.

1. Open of sla het bestand op volgens de normale procedure van uw browser.

Raadpleeg de online Help van uw browser voor meer informatie.

## Een feed-bestand handmatig uploaden {#feed-file-upload}

>[!NOTE]
> Als u een sjabloon koppelt aan een handmatig geüpload bestand, maar u uploadt via FTP een ander bestand met dezelfde naam, bestandsextensie en grammaticale hoofdletters/kleine letters, wordt het FTP-bestand gebruikt wanneer u de gegevens via de sjabloon doorgeeft. mijnbestand.csv vervangt bijvoorbeeld mijnbestand.csv, maar mijnbestand.CSV niet.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, die voor de [!UICONTROL Templates] tab.

1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Feeds]**.

1. Klik boven de gegevenstabel op **[!UICONTROL Upload]**.

1. Geef het te uploaden bestand op door het volledige pad en de bestandsnaam in te voeren of door te klikken op **[!UICONTROL Browse]** om het bestand op uw apparaat of netwerk te zoeken.

1. Klik op **[!UICONTROL Upload].

Alle velden in het bestand worden gevalideerd. Items met een ongeldige veldlengte kunt u later pas posten nadat u de waarden hebt gecorrigeerd. Alle kolomnamen in het bestand worden beschikbaar in sjablonen als dynamische parameters.

## Een feed-bestand vervangen {#feed-file-replace}

Wanneer u een feed-bestand vervangt — zelfs als het nieuwe bestand een andere bestandsnaam of extensie heeft — blijven alle bestaande sjabloonkoppelingen behouden. Het nieuwe dossier wordt gebruikt wanneer u gegevens door alle malplaatjes verspreidt die oorspronkelijk met het vorige dossier werden geassocieerd.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, die voor de [!UICONTROL Templates] tab.

1. Voer een van de volgende handelingen uit:

   * In de [!UICONTROL Feed] kolom voor een toepasselijke sjabloon, klikt u op ![Meer opties](/help/search-social-commerce/assets/options.png "Meer opties") en selecteert u **[!UICONTROL Re-upload]**.

   * Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Feeds]**. Schakel in de lijst met feed-bestanden het selectievakje naast de bestaande bestandsnaam in. Klik boven de gegevenstabel op **[!UICONTROL Upload]**.

   >[!NOTE]
   >
   >De bron van het feed-bestand (&quot;[!UICONTROL FTP]&quot; of &quot;&amp;mdash&quot; voor handmatig geüploade bestanden) is opgenomen in de [!UICONTROL Source] kolom.

1. Geef het te uploaden bestand op door het volledige pad en de bestandsnaam in te voeren of door te klikken op **[!UICONTROL Browse]** om het bestand op uw apparaat of netwerk te zoeken.

Zelfs als het nieuwe bestand een andere bestandsnaam of extensie heeft, wordt het bestaande bestand overschreven door het nieuwe bestand.

1. Klik op **[!UICONTROL Re-Upload]**.

Alle velden in het bestand worden gevalideerd. Items met een ongeldige veldlengte kunt u later pas posten nadat u de waarden hebt gecorrigeerd. Alle kolomnamen in het bestand worden beschikbaar in sjablonen als dynamische parameters.

## Feed-bestanden verwijderen

U kunt alle feed-bestanden verwijderen die handmatig of via FTP zijn geüpload. Wanneer u een voederdossier schrapt, is het niet meer verbonden met om het even welke malplaatjes.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, die voor de [!UICONTROL Templates] tab.

1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Feeds]**.

1. Schakel het selectievakje in naast elk bestand dat u wilt verwijderen.

1. Klik boven de gegevenstabel op **[!UICONTROL Delete]**.

1. Klik in het bevestigingsbericht **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [Informatie over voorraadfeeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Doorvoergegevens doorgeven via sjablonen](feed-data-propagate.md)
>* [Gegevens weergeven die zijn gegenereerd uit feeds](propagated-data-view.md)
>* [Uit feeds gegenereerde gegevens bewerken](propagated-data-edit.md)
>* [Gegevens van de post campagne die van voer aan advertentienetwerken worden geproduceerd](propagated-data-post.md)
>* [Een publicatietaak voor de gegevens van de inventarisfeed stoppen](stop-job.md)
>* [Statussen van gegevens die zijn gegenereerd uit feeds](propagated-data-status.md)
