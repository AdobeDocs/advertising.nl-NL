---
title: Gebruikersbeheer
description: Leer hoe te.
feature: Search Introduction
source-git-commit: 5a4c608d8c8371c24cf220cc5eed9a39989dc850
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# (Nieuwe gebruikersinterface) Gebruikersbeheer voor Zoeken, Sociale &amp; Handel

Sommige gebruikers kunnen de toegang tot de nieuwe gebruikersinterface voor Zoeken, Sociale media en Commerce beheren met de Adobe Admin Console, de centrale locatie voor het beheer van alle Adobe-rechten en gebruikersbeheer. Gebruikers worden gecategoriseerd als eindgebruikers of beheerders. Uw Adobe-accountteam geeft een melding als u een beheerder bent. Als u een beheerder bent, zie de volgende secties om uw toestemmingen en werkschema&#39;s voor het beheren van gebruikers te identificeren.<!-- How can you see what your user role is, or will your Adobe Account Team tell you? -->

## Relevante typen beheerders

Admin Console biedt meerdere typen beheerders, maar alleen de volgende beheerderstypen en machtigingen zijn relevant voor Zoeken, Sociaal en Commerce.

**Admin van het Systeem:** Super gebruiker voor de organisatie. Een systeembeheerder kan alle beheertaken in Admin Console voor de organisatie uitvoeren en kan beheerfunctionaliteit delegeren aan andere gebruikers (productbeheerders).&lt;!—, de beheerders van het productprofiel, en de beheerders van de gebruikersgroep.  — Ik denk dat het ALLEEN PRODUCT-BEHEERS VOOR ONS is?  Verifiëren. —>

**Admin van het Product:** beheert toegang tot een specifiek [!DNL Adobe] product (zoals Onderzoek, Sociale, &amp; Commerce) en hun rechten van gebruikers op dat product. Productbeheerders kunnen productprofielen voor het product maken, gebruikers en gebruikersgroepen maken (maar niet verwijderen), gebruikers en gebruikersgroepen toevoegen aan of verwijderen uit productprofielen en andere productbeheerders toevoegen aan of verwijderen uit het product.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Standaardproductprofielen

De profielen van het product, die aan rollen gelijkaardig zijn, geven gebruikers de recht met de specifieke diensten voor een specifiek product.

De nieuwe gebruikersinterface voor Zoeken, Sociale &amp; Handel heeft de volgende standaardproductprofielen, die verschillende ondergroepen van eigenschappen en de diensten verstrekken. U kunt de standaardproductprofielen niet bewerken of verwijderen. Systeembeheerders kunnen echter desgewenst aanvullende productprofielen met verschillende subsets met machtigingen maken en beheren.

* **BasisOptimalisering:** Dit profiel verstrekt de volgende functionaliteit:

   * Doelstellingen: Volledige toegang

   * Simulaties: volledige toegang

   * Portfolio-groepen: volledige toegang

   * Portfolio&#39;s: Toegang tot portfolioinstellingen voor doelstellingen, campagnes en uitgavenbeheer maken/bewerken; alleen-lezen toegang tot de overige portfolioinstellingen.

   * Campagnes: Read-only toegang tot campagnemontages (geen creeer, geef uit, of schrapt eigenschappen zijn beschikbaar); volledige toegang tot beperking en portefeuilletaken <!-- Is that the correct wording? -->

   * Groepen toevoegen: Alleen-lezen toegang tot instellingen van advertentiegroep (er zijn geen functies beschikbaar voor maken, bewerken of verwijderen); volledige toegang tot restricties en portfoliotoewijzingen <!-- Is that the correct wording? -->

  Dit toegangsniveau heeft de voorkeur voor gebruikers die nog steeds aan het leren zijn om Zoeken, Sociale media en Commerce te gebruiken.

* **Deskundige Optimalisering:** Dit profiel verstrekt de volgende functionaliteit:

   * Doelstellingen: Volledige toegang

   * Simulaties: volledige toegang

   * Portfolio-groepen: volledige toegang

   * Portfolio&#39;s: volledige toegang

   * Campagnes: Read-only toegang tot de campagnemijst (geen campagneverwezenlijking, het uitgeven, of het schrappen van eigenschappen zijn nog beschikbaar); volledige toegang tot beperking en portefeuilletaken <!-- Is that the correct wording? -->

   * Advertentiegroepen: Alleen-lezen toegang tot de lijst met advertentiegroepen (er zijn nog geen functies voor het maken, bewerken of verwijderen van campagnes beschikbaar); volledige toegang tot restricties en portfoliotoewijzingen <!-- Is that the correct wording? -->

  Dit toegangsniveau wordt aanbevolen voor ervaren gebruikers van Zoeken, Sociaal en Commerce.

* **read-only:** Dit profiel verstrekt de volgende functionaliteit:

   * Doelstellingen: alleen-lezen toegang

   * Simulaties: alleen-lezen toegang

   * Portfolio-groepen: alleen-lezen toegang

   * Portfolio&#39;s: alleen-lezen toegang

   * Campagnes: Alleen-lezen toegang

   * Toegevoegde groepen: alleen-lezen toegang

* **Admin:** Dit profiel verleent volledige toegang tot alle beschikbare functionaliteit en staat gebruikers toe om nieuwe cliëntinstanties tot stand te brengen. Wijs dit recht niet aan iedereen toe tenzij u een juiste bedrijfsrechtvaardiging hebt.

<!-- Do I need to include this? If so, adjust wording as needed

## Product-specific instances

 -->

## Taken voor beheerders

### Meld u aan bij Adobe Admin Console en open deze voor Zoeken, Sociaal en Commerce

>[!PREREQUISITES]
>
>U moet beheerderstoegang hebben&lt;!— wat voor soort? Productbeheerder, systeembeheerder, maar ik ben zeker ook de beheerder van het productprofiel of de beheerder van de gebruikersgroep (die een interne groep — controle zou kunnen zijn) —> aan Onderzoek, Sociale, &amp; Commerce.

1. Ga naar https://adminconsole.adobe.com/enterprise/.

1. (Als u niet bent aangemeld bij Experience Cloud) Meld u aan bij Experience Cloud:

   1. Voer uw [!DNL Adobe] -id in en klik op **[!UICONTROL Continue]** .

   1. Selecteer of **&#x200B; [!UICONTROL Personal Account]&quot;of &#x200B;** [!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Selecteer de toepasselijke Experience Cloud-organisatie.

   1. Klik onder Product &amp; de Diensten, &quot;[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]&quot;.

   De productpagina wordt standaard geopend op het tabblad [!UICONTROL Product profiles] voor Zoeken, Sociaal en Commerce. Extra tabbladen zijn [!UICONTROL Users] en [!UICONTROL Product Admins] .

### Workflow voor systeembeheerders

1. [ Teken binnen aan Adobe Admin Console en open het aan Onderzoek, Sociale, &amp; Commerce ](#open-admin-console).

1. Het product en gebruikersbeheer van de delegatie door [ toevoegend productbeheerders ](https://helpx.adobe.com/nl/enterprise/using/admin-roles.html#enterprise).

<!-- what else? -->

### Workflow voor productbeheerders

1. [ Teken binnen aan Adobe Admin Console en open het aan Onderzoek, Sociale, &amp; Commerce ](#open-admin-console).

1. Zoals nodig, creeer eind - gebruikers [ individueel ](https://helpx.adobe.com/nl/enterprise/using/manage-users-individually.html) of [ in bulk ](https://helpx.adobe.com/nl/enterprise/using/bulk-upload-users.html).

1. (Facultatief) creeer [ gebruikersgroepen ](https://helpx.adobe.com/nl/enterprise/using/user-groups.html) voor elke productinstantie en wijs gebruikers aan elke gebruikersgroep toe.

   Als het exemplaar vele gebruikers heeft, creeer gebruikersgroepen om ervoor te zorgen dat de gebruikers de juiste profielen op hun niveau van deskundigheid worden toegewezen. (Zie Stap 4 voor het toewijzen van gebruikersgroepen aan productprofielen.) U kunt gebruikersgroepen tot stand brengen die op de branche, gebruikerstoegangsbehoeften, gebruikershuurdatum, of andere criteria worden gebaseerd.

   >[!IMPORTANT]
   >
   >Gebruikersgroepnamen moeten duidelijk aangeven welke rechten aan de groep gebruikers moeten worden toegewezen. Als u bijvoorbeeld een gebruikersgroep wilt maken met de rechten Alleen-lezen, neemt u &quot;Alleen-lezen&quot; op in de naam van de gebruikersgroep, zoals &quot;Acme_Uk_ReadOnly&quot; of &quot;Acme_ReadOnly&quot;.

1. (Facultatief) [ creeer de profielen van het douaneproduct ](https://helpx.adobe.com/nl/enterprise/using/manage-product-profiles.html) met bepaalde toestemmingsreeksen.

   Aangepaste profielen zijn een aanvulling op de vier standaardproductprofielen die al beschikbaar zijn.

   Elk productprofiel voor een organisatie moet een unieke naam hebben. Als uw organisatie meerdere instanties Search, Social en Commerce gebruikt (bijvoorbeeld Acme_US en Acme_JP), kunt u een productprofielnaam niet in meerdere exemplaren dupliceren. **Beste praktijken:** gebruik de noemende overeenkomst `<Name>_<Instance>,` zoals &quot;Simulation_Only_JP.&quot;

1. [ wijs elke gebruiker of gebruikersgroep aan het relevante productprofiel ](https://helpx.adobe.com/nl/enterprise/using/manage-product-profiles.html) manueel of in bulk toe.

## Volledige handleiding voor gebruikersbeheer en aanvullende koppelingen

* Voor meer informatie over gebruikersbeleid dat Adobe Admin Console gebruikt, zie &quot;[ de Gids van het Beleid van de Onderneming &amp; van Teams van Adobe ](https://helpx.adobe.com/nl/enterprise/admin-guide.html),&quot;met inbegrip van het [ overzicht van Admin Console ](https://helpx.adobe.com/nl/enterprise/using/admin-console.html).

* Admin Console: [ https://adminconsole.adobe.com](https://adminconsole.adobe.com)
