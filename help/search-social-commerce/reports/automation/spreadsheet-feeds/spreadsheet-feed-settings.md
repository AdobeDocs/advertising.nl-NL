---
title: Feed-instellingen voor werkbladrapporten
description: Meer informatie over de instellingen voor spreadsheetfeeds.
exl-id: 9a7e0a21-5db4-4829-a191-cacaa51f6cb6
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Feed-instellingen voor werkbladrapporten

| Veld | Beschrijving |
|---|---|
| [!UICONTROL Feed Name] | Een naam voor de spreadsheetfeed. |
| [!UICONTROL Report Template] | Het rapportmalplaatje dat de vereiste rapportgegevens specificeert; selecteer één u gebruikte om tot de [!DNL Excel] sjabloon. Alle basisierapportsjablonen worden weergegeven.<br><br><b>Opmerking:</b> Als u het rapportmalplaatje verandert dat voor het rapport wordt gebruikt, of u werkt de kolommen in het malplaatje bij, dan moet u een nieuw creëren en uploaden [!DNL Excel] sjabloon. |
| [!UICONTROL Excel Template] | De speciaal geformatteerde [!DNL Excel] malplaatje dat u in .XLSX formaat creeerde, dat op gegevens wordt toegepast die in het rapportmalplaatje worden gespecificeerd. Geef het te uploaden bestand op door het volledige pad en de bestandsnaam in te voeren of door te klikken op <b>[!UICONTROL Browse]</b> om het bestand op uw apparaat of netwerk te zoeken. |
| [!UICONTROL Back Fill From] | De begindatum waarvoor bestaande gegevens over de [!UICONTROL RAW] tab wordt vernieuwd, weergegeven door een aantal dagen in het verleden. Voer een waarde in van maximaal 90 dagen. De standaardwaarde is zeven (7) dagen.<br><br>Als de waarde bijvoorbeeld 7 is en vandaag 7 maart, worden de bestaande gegevens over de [!UICONTROL RAW] tab die begint met 1 maart, wordt vernieuwd (tot de einddatum die is opgegeven door de [!UICONTROL Back Fill Until] parameter). Bestaande rijen met gegevens voor datums vóór 1 maart worden niet verwijderd, maar niet vernieuwd. |
| [!UICONTROL Back Fill Until] | De einddatum waarvoor bestaande gegevens over de [!UICONTROL RAW] tab wordt vernieuwd, weergegeven door een aantal dagen in het verleden. De standaardwaarde is één (1) dag.<br><br>Als deze waarde bijvoorbeeld 1 is en vandaag 7 maart, worden de bestaande gegevens over de [!UICONTROL RAW] tab wordt vernieuwd tot 6 maart (en begint met de startdatum die door de [!UICONTROL Back Fill From] parameter). Als deze waarde 1 is, wordt [!UICONTROL Back Fill Until] parameter is 7, en vandaag is het 7 maart, dan de bestaande gegevens over [!UICONTROL RAW] wordt vernieuwd van 1 maart tot en met 6 maart. In beide voorbeelden worden bestaande rijen met gegevens voor datums na 6 maart niet verwijderd, maar niet vernieuwd. |
| [!UICONTROL Email Recipients] | E-mailadressen waarop om berichten te verzenden telkens als het rapport wordt verfrist, of telkens als het rapport wordt in werking gesteld wanneer het malplaatje een programma omvat. Standaard wordt het adres van uw gebruikersaccount ingevoerd. Als u meerdere adressen wilt opgeven, scheidt u deze met komma&#39;s, spaties of nieuwe regels. |
| [!UICONTROL Schedule Time] | Het tijdstip waarop spreadsheetfeeds worden vernieuwd: om 8.00 uur of op een willekeurig uur tussen 10.00 en 23.00 uur in de tijdzone van de adverteerder. De standaardwaarde voor nieuwe spreadsheetfeeds is 10:00.<br><br><b>Opmerking:</b> Om prestatiesredenen, kunt u spreadsheetvoer bij 09:00 niet verfrissen, wanneer andere rapporten worden geproduceerd. |
| [!UICONTROL Email Notification] | (Wanneer e-mailontvangers zijn opgegeven) Wat moet u in e-mailmeldingen opnemen voor een opgegeven adres:<ul><li><i>Voeding bijvoegen</i> — Een kopie van het voltooide rapport in XLSX-indeling verzenden. Als het bestand groter is dan 10 MB, bevat het bericht geen bijlage.</li><li><i>Alleen kennisgeving</i> (het gebrek) — om slechts een bericht van de rapportvoltooiing of mislukking, met een verbinding naar het rapport te verzenden.</li></ul> |

>[!MORELIKETHIS]
>
>* [Info over werkbladrapportfeeds](spreadsheet-feed-about.md)
>* [Een feed voor een spreadsheetrapport maken](spreadsheet-feed-create.md)
>* [Een [!DNL Excel] sjabloon voor een spreadsheetrapportfeed](spreadsheet-feed-create-excel-template.md)
>* [Invoerinstellingen voor spreadsheetrapporten bewerken](spreadsheet-feed-edit.md)
>* [Een feed-bestand voor een spreadsheetrapport weergeven of opslaan](spreadsheet-feed-view-or-save.md)
>* [Werkbladrapportfeeds handmatig vernieuwen](spreadsheet-feed-refresh.md)
>* [feeds voor spreadsheetrapporten verwijderen](spreadsheet-feed-delete.md)
