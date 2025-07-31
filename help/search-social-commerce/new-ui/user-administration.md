---
title: (Nieuwe gebruikersinterface) Gebruikersbeheer
description: Leer hoe u gebruikerstoegang beheert.
feature: Search Introduction
source-git-commit: c198b5ea2f8ef125b1a5d25616158d57950ce3b0
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 0%

---

# (Nieuwe gebruikersinterface) Gebruikersbeheer voor Zoeken, Sociale &amp; Handel

Sommige gebruikers kunnen toegang tot het nieuwe Onderzoek, Sociale, &amp; gebruikersinterface van Commerce beheren gebruikend [ Adobe Admin Console ](https://helpx.adobe.com/nl/enterprise/using/admin-console.html), die de centrale plaats voor het beheren van alle rechten van Adobe en gebruikersbeheer is. Gebruikers worden gecategoriseerd als eindgebruikers of beheerders. Uw Adobe-accountteam geeft een melding als u een beheerder bent. Als u een beheerder bent, zie de volgende secties om uw toestemmingen en werkschema&#39;s voor het beheren van gebruikers te identificeren.

## Typen beheerders

Admin Console biedt meerdere typen beheerders. De volgende beheerderstypen en machtigingen zijn vereist voor Zoeken, Sociaal en Commerce. U kunt extra types toevoegen als u wenst om gebruikerbeheerstaken te delegeren.

**beheerder van het Systeem:** Super gebruiker die alle producten voor de organisatie, met inbegrip van alle cliëntinstanties voor de organisatie beheert. (Clientinstanties zijn hetzelfde als oudere adverteerderaccounts, met een of meer exemplaren per organisatie-id). Een systeembeheerder kan alle beheerstaken in Admin Console voor de organisatie uitvoeren en kan beheerfunctionaliteit aan andere gebruikers voor om het even welke producten van de organisatie delegeren.

**Admin van het Product:** beheert toegang tot een specifiek [!DNL Adobe] product (zoals Onderzoek, Sociale, &amp; Commerce) en de gebruikersrechten aan dat product. Productbeheerders kunnen productprofielen voor het product maken, gebruikers en gebruikersgroepen voor het product maken (maar niet verwijderen), gebruikers en gebruikersgroepen toevoegen aan of verwijderen uit productprofielen en andere productbeheerders toevoegen aan of verwijderen uit het product.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Standaardproductprofielen

De profielen van het product, die aan rollen gelijkaardig zijn, geven gebruikers de recht met de specifieke diensten voor een specifiek product.

De nieuwe gebruikersinterface voor Zoeken, Sociale &amp; Handel heeft de volgende standaardproductprofielen, die verschillende ondergroepen van eigenschappen en de diensten verstrekken. U kunt de productmachtigingen voor de standaardproductprofielen niet bewerken of de standaardproductprofielen verwijderen. Productbeheerders, productprofielbeheerders en systeembeheerders kunnen echter zo nodig aanvullende productprofielen met verschillende subsets van beschikbare machtigingen maken en beheren.

* **[!UICONTROL Basic Optimization]:** Dit profiel biedt de volgende functionaliteit:

   * [!UICONTROL Objectives]: volledige toegang

   * [!UICONTROL Simulations]: volledige toegang

   * [!UICONTROL Portfolio Groups]: volledige toegang

   * [!UICONTROL Portfolios]: Maak/bewerk toegang tot portfolioinstellingen voor [!UICONTROL Objectives] , [!UICONTROL Campaigns] en Spend [!UICONTROL Management] ; alleen-lezen toegang tot de overige portfolioinstellingen.

   * [!UICONTROL Campaigns]: Alleen-lezen toegang tot campagne-instellingen (er zijn geen functies voor maken, bewerken of verwijderen beschikbaar); volledige toegang tot restricties en portfoliotoewijzingen

   * [!UICONTROL Ad Groups]: Alleen-lezen toegang tot instellingen van een advertentiegroep (er zijn geen functies voor maken, bewerken of verwijderen beschikbaar); volledige toegang tot restricties en portfoliotoewijzingen

  Dit toegangsniveau heeft de voorkeur voor gebruikers die nog steeds aan het leren zijn om Zoeken, Sociale media en Commerce te gebruiken.

* **[!UICONTROL Expert Optimization]:** Dit profiel biedt de volgende functionaliteit:

   * [!UICONTROL Objectives]: volledige toegang

   * [!UICONTROL Simulations]: volledige toegang

   * [!UICONTROL Portfolio Groups]: volledige toegang

   * [!UICONTROL Portfolios]: volledige toegang

   * [!UICONTROL Campaigns]: Alleen-lezen toegang tot de lijst met campagnes (er zijn nog geen functies voor het maken, bewerken of verwijderen van campagnes beschikbaar); volledige toegang tot restricties en portfoliotoewijzingen

   * [!UICONTROL Ad Groups]: Alleen-lezen toegang tot de lijst met advertentiegroepen (er zijn nog geen functies voor het maken, bewerken of verwijderen van campagnes beschikbaar); volledige toegang tot restricties en portfoliotoewijzingen

  Dit toegangsniveau wordt aanbevolen voor ervaren gebruikers van Zoeken, Sociaal en Commerce.

* **[!UICONTROL Read-Only]:** Dit profiel biedt de volgende functionaliteit:

   * [!UICONTROL Objectives]: alleen-lezen toegang

   * [!UICONTROL Simulations]: alleen-lezen toegang

   * [!UICONTROL Portfolio Groups]: alleen-lezen toegang

   * [!UICONTROL Portfolios]: alleen-lezen toegang

   * [!UICONTROL Campaigns]: alleen-lezen toegang

   * [!UICONTROL Ad Groups]: alleen-lezen toegang

* **[!UICONTROL Admin]:** Dit profiel verleent volledige toegang tot alle beschikbare functionaliteit en staat gebruikers toe om nieuwe cliëntinstanties (het zelfde als erfenisadverteerderrekeningen, met één of meerdere instanties per organisatieidentiteitskaart) tot stand te brengen. Wijs dit recht niet aan iedereen toe tenzij u een juiste bedrijfsrechtvaardiging hebt.

## Taken voor beheerders

### Meld u aan bij Adobe Admin Console en open deze voor Zoeken, Sociaal en Commerce

>[!PREREQUISITES]
>
>U moet een bepaald type beheerder toegang hebben tot Zoeken, Sociaal en Commerce om u aan te melden bij Admin Console.

1. Ga naar https://adminconsole.adobe.com/enterprise/.

1. (Als u niet bent aangemeld bij Experience Cloud) Meld u aan bij Experience Cloud:

   1. Voer uw [!DNL Adobe] -id in en klik op **[!UICONTROL Continue]** .

   1. Selecteer of ** [!UICONTROL Personal Account]&quot;of **[!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Selecteer de toepasselijke Experience Cloud-organisatie.

      Admin Console wordt geopend voor de tab [!UICONTROL Overview] .

   1. Klik onder [!UICONTROL Product & services] op &quot;[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]&quot;.

      De productpagina wordt geopend op het tabblad [!UICONTROL Product profiles] voor Zoeken, Sociaal en Commerce. Extra tabbladen zijn [!UICONTROL Users] en [!UICONTROL Product Admins] .

### Workflow voor systeembeheerders

Volg deze workflow voor elke client-instantie van Zoeken, Sociaal en Commerce.

1. [ Teken binnen aan Adobe Admin Console en open het aan Onderzoek, Sociale, &amp; Commerce ](#open-admin-console).

1. (Facultatief) [ voeg een andere systeembeheerder ](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise) als steun toe.

1. Het product en gebruikersbeheer van de delegatie door [ toevoegend productbeheerders ](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise).

### Workflow voor productbeheerders

Volg deze workflow voor elke client-instantie van Zoeken, Sociaal en Commerce.

1. [ Teken binnen aan Adobe Admin Console en open het aan Onderzoek, Sociale, &amp; Commerce ](#open-admin-console).

1. Zoals nodig, creeer eind - gebruikers [ individueel ](https://helpx.adobe.com/enterprise/using/manage-users-individually.html) of [ in bulk ](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. (Facultatief) creeer [ gebruikersgroepen ](https://helpx.adobe.com/enterprise/using/user-groups.html) voor de instantie en wijs gebruikers aan elke gebruikersgroep toe.

   Als het exemplaar vele gebruikers heeft, creeer gebruikersgroepen om ervoor te zorgen dat de gebruikers de juiste profielen op hun niveau van deskundigheid worden toegewezen. (Zie Stap 4 voor het toewijzen van gebruikersgroepen aan productprofielen.) U kunt gebruikersgroepen tot stand brengen die op de branche, gebruikerstoegangsbehoeften, gebruikershuurdatum, of andere criteria worden gebaseerd.

   >[!IMPORTANT]
   >
   >Gebruikersgroepnamen moeten duidelijk aangeven welke rechten aan de groep gebruikers moeten worden toegewezen. Als u bijvoorbeeld een gebruikersgroep wilt maken met de rechten Alleen-lezen, neemt u &quot;Alleen-lezen&quot; op in de naam van de gebruikersgroep, zoals &quot;Acme_Uk_ReadOnly&quot; of &quot;Acme_ReadOnly&quot;.

1. (Facultatief) [ creeer de profielen van het douaneproduct ](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) met bepaalde toestemmingsreeksen.

   Aangepaste profielen zijn een aanvulling op de vier standaardproductprofielen die al beschikbaar zijn.

   Elk productprofiel voor een organisatie moet een unieke naam hebben. Als uw organisatie meerdere instanties Search, Social en Commerce gebruikt (bijvoorbeeld Acme_US en Acme_JP), kunt u een productprofielnaam niet in meerdere exemplaren dupliceren. **Beste praktijken:** gebruik de noemende overeenkomst `<Name>_<Instance>,` zoals &quot;Simulation_Only_JP.&quot;

   **Voorzichtigheid:** de toestemmingen van het Product zijn zeer korrelig. Wees voorzichtig wanneer u aangepaste productprofielen configureert of wanneer u de functionaliteit weglaat die u wilt opnemen.

1. [ wijs elke gebruiker of gebruikersgroep aan het relevante productprofiel ](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) manueel of in bulk toe.

## Volledige handleiding voor gebruikersbeheer en aanvullende koppelingen

* Voor meer informatie over gebruikersbeleid dat Adobe Admin Console gebruikt, zie &quot;[ de Gids van het Beleid van de Onderneming &amp; van Teams van Adobe ](https://helpx.adobe.com/enterprise/admin-guide.html),&quot;met inbegrip van het [ overzicht van Admin Console ](https://helpx.adobe.com/nl/enterprise/using/admin-console.html).

* Admin Console: [ https://adminconsole.adobe.com](https://adminconsole.adobe.com)
