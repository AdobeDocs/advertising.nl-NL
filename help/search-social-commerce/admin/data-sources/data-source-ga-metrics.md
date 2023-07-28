---
title: Beschikbaar [!DNL Google Analytics] cijfers
description: Verwijs naar de [!DNL Google Analytics] gegevens beschikbaar voor gegevensbronnen.
role: User, Admin
exl-id: f7ac93e3-1aed-4165-ae65-7966ca192c84
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Bijlage - beschikbaar [!DNL Google Analytics] cijfers

De volgende metriek, behalve de vermelde uitsluitingen, zijn beschikbaar wanneer zij in de implementatie van de klant in [!DNL Google Analytics].

<!-- Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Categorie | Uitgesloten | Opmerkingen |
| ---- | ---- | ---- |
| \[Alles\] | Metriek met een gegevenstype &quot;PERCENT&quot; | De cijfers die als percentage worden voorgesteld worden altijd uitgesloten. |
| Gebruiker | ga:1 dagGebruikers, ga:7 dagenGebruikers, ga:14 dagenGebruikers, ga:28 dagenGebruikers, ga:sessiesPerGebruiker | — |
| Sessie | ga:uniqueDimensionCombinations | — |
| Goederen converteren | — | — |
| Pagina&#39;s bijhouden | ga:ingangen, ga:timeOnPage, ga:afsluiten | — |
| Interne zoekopdracht | — | De vriendschappelijke namen van alle metriek van Intern Onderzoek worden prepended met de waarde &quot;InternalSearch: &quot; |
| Gebeurtenissen bijhouden | — | — |
| Ecommerce | — | — |
| Sociale interacties | — | — |
| Uitzonderingen | — | — |
| Aangepaste variabelen of kolommen | ga:calcMetric_* | Berekende meetwaarden worden altijd uitgesloten. |

>[!MORELIKETHIS]
>
>* [Over synchroniseren [!DNL Google Analytics] conversiemetingen](data-source-about.md)
>* [Vereisten voor het configureren van een [!DNL Google Analytics] gegevensbron](data-source-prerequisites.md)
>* [Een [!DNL Google Analytics] weergeven als gegevensbron](data-source-configure.md)
>* [Een [!DNL Google Analytics] gegevensbron](data-source-edit.md)
>* [Synchronisatie van een gegevensbron pauzeren](data-source-pause.md)
>* [Een [!DNL Google Analytics] gegevensbron](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] gegevensbroninstellingen](data-source-settings.md)
