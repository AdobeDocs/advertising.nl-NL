---
title: Conversie bijhouden met een EF-id-feed
description: Meer informatie over het gebruik van een EF-id-feed voor het bijhouden van conversiegegevens.
source-git-commit: 46e918418bf2e5c412efa8825dda22bc1953e439
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Conversie bijhouden met een EF-id-feed

In deze methode verzamelt Advertising Cloud een `ef_id` telkens wanneer een gebruiker klikt en adverteert en bij de landingspagina aankomt, en de adverteerder de `ef_id` waarde met de conversiegegevens en verstuurt deze in een gegevensfeed.

## Overzicht van implementatie

*Accountmanager van het Agentschap, [!DNL Adobe] alleen accountmanager en beheerdersgebruikersrollen*

1. De opties voor het bijhouden van accounts of campagnes gebruiken &quot;[!UICONTROL EF Redirect],&quot; het omleidingstype van &quot;[!UICONTROL Token],&quot; en &quot;[!UICONTROL Auto Upload]&quot; om automatisch een doel-URL of uiteindelijke URL te genereren met een Adobe Advertising-token (ef_id) voor elk trefwoord (voor reeksspatiëring) of advertentie (voor opvolging op advertentieniveau) in de account of campagne.

   >[!NOTE]
   >* Voor deze methode hoeft de adverteerder geen Adobe-tags voor conversie van advertenties te gebruiken.
   >* Als u van het omleidingstype voor een bestaande rekening of een campagne van schakelt [!UICONTROL Standard] tot [!UICONTROL Token], of vice versa, dan moet u alle toepasselijke het volgen URLs opnieuw produceren.

   De ef_id wordt gevuld en toegevoegd aan de bestemmingspagina-URL wanneer de eindgebruiker op de advertentie klikt en aan een server van de Advertising van Adobe wordt opnieuw gericht. De ef_id wordt vervolgens doorgegeven aan de adverteerder in de doel-URL of de laatste URL voor de advertentie of het trefwoord. Hier volgt een voorbeeld van een doel-URL die tijdens de omleiding wordt doorgegeven aan de adverteerder:

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. De adverteerder extraheert de ef_id uit de omleiding en slaat deze op met de relevante omzettingsgegevens die in het voederbestand moeten worden opgenomen. Verander ef ef_id niet of verander zijn geval.

1. (Optioneel, maar aanbevolen) De adverteerder kan een unieke transactie-id maken voor elke transactie die in het feed-bestand moet worden opgenomen.

1. De adverteerder uploadt een bestand met de [vereiste conversiegegevens](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) naar de aangewezen serverlocatie.

1. Technical Services parseert de conversiegegevens in de geüploade bestanden en uploadt de gegevens vervolgens naar Adobe Advertising. De Adobe Advertising volgt de gegevens dan tegen individuele sleutelwoorden, advertenties, en plaatsingen en leidt tot opbrengst het voorspellen voor elk.

1. Technische diensten valideert de verwerkte gegevens tegen de voedergegevens en controles voor om het even welk [verweesde transacties](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Bestandsvereisten voor de conversie van feed-bestanden](feed-file-requirements.md)
>* [Gegevensvereisten voor gegevensdoorvoer met EF-id&#39;s](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)


