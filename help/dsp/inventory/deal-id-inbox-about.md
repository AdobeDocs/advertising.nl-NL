---
title: Over de [!UICONTROL Deal ID Inbox]
description: Leer over de [!UICONTROL Deal ID inbox] eigenschap, die u toestaat om privé overeenkomsten goed te keuren u reeds met uitgevers op  [!DNL FreeWheel], [!DNL Google Authorized Buyers]  (vroeger gekend als  [!DNL AdX]), and [!DNL Magnite DV+]  (vroeger  [!DNL Rubicon]) hebt onderhandeld.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: 394a281c9b9d7eeab939f4c58508ec1f34eba67c
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Over de [!UICONTROL Deal ID Inbox]

Met Advertising DSP [!UICONTROL Deal ID inbox] kunt u snel deals instellen die DSP van uitgevers heeft geïmporteerd via leveranciers (SSPs), zodat u niet elke deal handmatig hoeft in te stellen. U kunt de gegarandeerde en niet-gegarandeerde privé-voorraadtransacties accepteren die u al met uitgevers hebt onderhandeld op [!DNL FreeWheel] , [!DNL Google Authorized Buyers] (voorheen bekend als [!DNL AdX] ) en [!DNL Magnite DV+] (voorheen [!DNL Rubicon] ) van de [!UICONTROL Deal ID inbox] .

>[!NOTE]
>
>Advertising DSP is de eerste DSP die met de [!DNL FreeWheel] API wordt geïntegreerd.

In [!UICONTROL Deal ID inbox], kunt u de details van de overeenkomst zien aangezien uw uitgever hen ziet, uw overeenkomstenopstelling versnelt, en handingangsfouten vermijdt.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP vernieuwt automatisch alle details van de deal dagelijks om 4:30 uur EST. Ook worden alle [!DNL FreeWheel] -deals vernieuwd en worden bestaande deals vanuit [!DNL Google] en [!DNL Magnite DV+] uur bijgewerkt. U kunt de overeenkomstendetails ook manueel verfrissen om nieuwe overeenkomsten op elk ogenblik te bevolken.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->

>[!NOTE]
>
>Voor programmatic gegarandeerde deals via [!DNL Google Authorized Buyers] moet u ten minste 90% van uw budget leveren, anders verliest uw account de toegang tot [!DNL Google] -deals in de [!UICONTROL Deal ID inbox] .

## De [!UICONTROL Deal ID Inbox] implementeren

Als u uw deals in de [!UICONTROL Deal ID inbox] wilt ontvangen, moet uw SSP-account de DSP-account van uw organisatie toewijzen aan uw SSP-account. DSP kan de accountnamen van de organisatie delen met de relevante SSP&#39;s. Neem contact op met uw Adobe-accountteam voor instructies.

Geef de uitgever tijdens de onderhandelingen over deals de deal door aan de koper in plaats van aan de bovenliggende DSP-account. De overeenkomstenherkenningsteken kan een naam of een identiteitskaart, afhankelijk van SSP zijn.

## Handelingen die u kunt uitvoeren

* **de overeenkomsten van het Overzicht** om te verifiëren dat SSP de correcte uitgever, vluchtdata, CPM, en andere overeenkomstendetails heeft verzonden. Als de uitgever een fout heeft gemaakt, contacteer hen buiten DSP zodat kunnen zij de overeenkomst verbeteren en opnieuw verzenden.

* **keurt overeenkomsten** na het herzien goed, en zij verschijnen niet meer in [!UICONTROL Deal ID inbox]. Accepteerde deals worden weergegeven in [!UICONTROL Inventory] > [!UICONTROL Deals] en zijn gereed om zich te richten binnen de plaatsen van adverteerders.

* **negeer overeenkomsten** die niet nodig zijn of ongevraagd zijn. Genegeerde deals worden verplaatst naar het tabblad [!UICONTROL Ignored Deals] in [!UICONTROL Deal ID inbox] , dat als archief fungeert. DSP waarschuwt geen SSPs en uitgevers wanneer u een overeenkomst negeert.

* **wijzigt details voor reeds-toegelaten overeenkomsten** van [!UICONTROL Inventory] > [!UICONTROL Deals] (niet in [!UICONTROL Deal ID inbox]). Op dezelfde manier zijn adverteerders die wijzigingen in deals verzenden, verantwoordelijk voor de implementatie van deze wijzigingen in [!UICONTROL Inventory] > [!UICONTROL Deals] omdat de wijzigingen van de SSP&#39;s door [!UICONTROL Deal ID inbox] niet worden gesynchroniseerd nadat deals zijn ingesteld.

## Welke types van Overeenkomsten kunnen niet worden goedgekeurd?

Wanneer een overeenkomstenlijst niet a ![ omvat Accepteer ](/help/dsp/assets/accept.png) pictogram of een [!UICONTROL Accept] knoop, kunt u niet het van [!UICONTROL Deal ID inbox] goedkeuren. In plaats daarvan, kunt u [ de details van identiteitskaart van de overeenkomst manueel ](/help/dsp/inventory/deal-id-create.md) tot stand brengen.

U kunt de volgende typen overeenkomsten niet accepteren:

* [!DNL Google] -deals die niet in USD staan.

* [!DNL Magnite DV+] -deals die niet in USD staan

* [!DNL FreeWheel] -deals die zich niet in uw accountvaluta bevinden.

* Overeenkomsten die een einddatum vóór vandaag hebben.

* Oude [!DNL Magnite DV+] deals die zijn gelabeld als &#39;meerdere mediatypen&#39;.

De overeenkomstendetails omvatten de reden dat de overeenkomst niet beschikbaar is te aanvaarden.

>[!MORELIKETHIS]
>
>* [ keurt een Overeenkomst in identiteitskaart Inbox van de Overeenkomst goed ](deal-id-inbox-accept.md)
>* [ Overzicht van de Eigenschappen van de Inventaris ](inventory-overview.md)
