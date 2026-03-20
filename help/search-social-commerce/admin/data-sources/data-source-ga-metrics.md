---
title: Beschikbare  [!DNL Google Analytics]  metriek
description: Verwijzing de  [!DNL Google Analytics]  metriek beschikbaar voor gegevensbronnen.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# Bijlage - Beschikbare [!DNL Google Analytics] metriek

De volgende maatstaven, behalve de vermelde uitsluitingen, zijn beschikbaar wanneer deze zijn ingeschakeld in de implementatie van de klant in [!DNL Google Analytics] .

<!--
 Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Categorie | Uitgesloten | Opmerkingen |
| ---- | ---- | ---- |
| \[Alles\] | Metriek met een gegevenstype &quot;PERCENT&quot; | De cijfers die als percentage worden voorgesteld worden altijd uitgesloten. |
| Gebruiker | ga :1dayUsers, ga :7dayUsers, ga :14dayUsers, ga :28dayUsers, ga :sessionsPerUser | — |
| Sessie | ga:uniqueDimensionCombinations | — |
| Goederen converteren | — | — |
| Pagina&#39;s bijhouden | ga :entrances, ga :timeOnPage, ga :exits | — |
| Interne zoekopdracht | — | De vriendschappelijke namen van alle metriek van Intern Onderzoek worden prepended met de waarde &quot;InternalSearch: &quot; |
| Gebeurtenissen bijhouden | — | — |
| Ecommerce | — | — |
| Sociale interacties | — | — |
| Uitzonderingen | — | — |
| Aangepaste variabelen of kolommen | ga :calcMetric_* | Berekende meetwaarden worden altijd uitgesloten. |

>[!MORELIKETHIS]
>
>* [ Ongeveer synchroniserend  [!DNL Google Analytics]  omzettingsmetriek ](data-source-about.md)
>* [ Vereisten om a  [!DNL Google Analytics]  gegevensbron ](data-source-prerequisites.md) te vormen
>* [ vorm a  [!DNL Google Analytics]  mening als gegevensbron ](data-source-configure.md)
>* [ geef a  [!DNL Google Analytics]  gegevensbron ](data-source-edit.md) uit
>* [ de synchronisatie van de pauze van een gegevensbron ](data-source-pause.md)
>* [ verklaart a  [!DNL Google Analytics]  gegevensbron ](data-source-reauthenticate.md) opnieuw voor authentiek
>* [[!DNL Google Analytics]  gegevensbronmontages ](data-source-settings.md)
