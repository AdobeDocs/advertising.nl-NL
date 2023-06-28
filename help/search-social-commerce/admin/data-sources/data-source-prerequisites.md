---
title: Vereisten voor het configureren van een [!DNL Google Analytics] gegevensbron
description: Leer over de stappen die u moet voltooien alvorens u vormt een [!DNL Google Analytics] gegevensbron.
role: User, Admin
exl-id: cbb2ad6d-8494-4fa4-928c-238b25bda3a6
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Vereisten voor het configureren van een [!DNL Google Analytics] gegevensbron

Voordat u een [!DNL Google Analytics] gegevensbron, moet u de de vraagkoordparameter van het Onderzoek, Sociale, &amp; van de Handel &quot;ef_id&quot;als primaire sleutel vestigen om gegevens van over te gaan [!DNL Google Analytics] om te zoeken, sociale zaken en handel. De primaire sleutel instellen voor elke [!DNL Google Analytics] de combinatie van account en eigenschap waarvoor u gegevens wilt synchroniseren. Het kan zijn dat andere personen in uw organisatie deze taken moeten uitvoeren. zie hieronder voor meer informatie .

Als de bestemmingspagina-URL&#39;s voor uw advertenties of trefwoorden nog geen omleidingen voor Zoeken, Sociale Zaken en Handel bevatten, voegt u deze eerst toe.

## Vereiste 1: Een token voor Zoeken, Sociale media en Handel (&quot;ef_id&quot;-queryreeks-parameter) implementeren in de URL&#39;s van de bestemmingspagina voor alle toepasselijke advertentierekeningen

Klik bij elke betaalde zoekopdracht op de relevante campagnes, een unieke `ef_id` moet worden gegenereerd en aan de URL van de bestemmingspagina worden toegevoegd als een queryreeks, zoals `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, waarbij `&ef_id=abcde:123456789:s` het toevoegsymbool is; `ef_id` sleutel, en `ef_id` waarde. Om een ef_id op te nemen, moeten de relevante rekeningen en de campagnes van de advertentienetwerken [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot; en de [!UICONTROL Redirect Type] &quot;[!UICONTROL Token].&quot;

Voor bestaande accounts en campagnes is de ef_id waarschijnlijk al geïmplementeerd.

Als de ef_id niet is opgenomen, vraagt u uw Adobe-accountteam om assistentie.

Wanneer alle voorwaarden worden voltooid, `ef_id` wordt gebruikt als primaire sleutel voor het doorgeven van gegevens van [!DNL Google Analytics] om te zoeken, sociale zaken en handel.

## Vereiste 2: Leg het token Search, Social &amp; Commerce (&quot;ef_id&quot;-parameter voor queryreeksen) vast in een aangepaste dimensie voor elk relevant item [!DNL Google Analytics] eigenschap

Herhaal de volgende taken voor elk [!DNL Google Analytics] de combinatie van account en eigenschap waarvoor u gegevens wilt synchroniseren. Zie [[!DNL Google Analytics] documentatie over het maken en implementeren van aangepaste afmetingen](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) voor hulp bij deze taken.

1. In [!DNL Google Analytics], maakt u een aangepaste dimensie met de naam &quot;`ef_id`&quot;. Bereik van de dimensie instellen op [!DNL User]en stelt de dimensie in op actief.

   >[!NOTE]
   >
   >Voor deze voorwaarde is bewerkingsmachtigingen voor de relevante eigenschappen vereist.

1. Werk uw [!DNL Google Analytics] volgende code om de waarde van de ef_id parameter van het vraagkoord te vangen wanneer het in de het landen pagina URL aanwezig is en het op te slaan in de ef_id douaneafmeting.

   >[!NOTE]
   >
   >ef_id zou slechts in het landen pagina URLs moeten zijn.

   Als de URL van de landingspagina bijvoorbeeld de URL is `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`, dan de waarde van de ef_id-dimensie in [!DNL Google Analytics] is `abcde:123456789:s`.

   >[!NOTE]
   >
   >Deze voorwaarde moet worden ingevuld door een gekwalificeerde ontwikkelaar.

>[!MORELIKETHIS]
>
>* [Over synchroniseren [!DNL Google Analytics] conversiemetingen](data-source-about.md)
>* [Een [!DNL Google Analytics] weergeven als gegevensbron](data-source-configure.md)
>* [Een [!DNL Google Analytics] gegevensbron](data-source-edit.md)
>* [Synchronisatie van een gegevensbron pauzeren](data-source-pause.md)
>* [Een [!DNL Google Analytics] gegevensbron](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] gegevensbroninstellingen](data-source-settings.md)
>* [Bijlage - beschikbaar [!DNL Google Analytics] cijfers](data-source-ga-metrics.md)
