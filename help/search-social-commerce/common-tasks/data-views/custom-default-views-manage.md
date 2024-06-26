---
title: Standaard- en aangepaste weergaven beheren
description: Leer hoe u uw standaardweergaven en aangepaste weergaven aanpast.
exl-id: 1f240760-6186-471f-bf1a-3e0ee13ce550
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '2835'
ht-degree: 0%

---

# Standaard- en aangepaste weergaven beheren

Met de standaardweergaven en aangepaste weergaven kunt u de prestatiegegevens aanpassen die worden weergegeven in de gegevensweergaven van de zoekcampagne. Tot de weergave-instellingen behoren de kolommen die moeten worden opgenomen, de filters, het datumbereik, de conversieattributie-instellingen en andere geavanceerde instellingen. U kunt de instellingen tijdelijk toepassen of ze opslaan. (Uitzondering: u kunt filters niet opslaan voor standaardweergaven.) Elke standaardweergave en standaardweergave is van toepassing op een specifieke entiteitsweergave (zoals [!UICONTROL Campaigns]) en alleen specifieke adverteerderaccount. Elke universele aangepaste weergave is van toepassing op de verschillende weergaven van entiteiten voor een specifieke adverteerder en kan daarom geen eigenschapskolommen (zoals de naam of status van een entiteit) bevatten, die per entiteitstype variëren.

De standaardweergaven worden standaard weergegeven wanneer u zich aanmeldt. U kunt aanvullende aangepaste weergaven maken en deze op elk gewenst moment toepassen. U kunt desgewenst elke aangepaste weergave delen die u maakt met alle andere gebruikers die de gegevens van de adverteerder kunnen bekijken. In uw weergaveoverzichten is elke weergave die een andere persoon deelt cursief, zoals &quot;*Prestatiecampagnes*.&quot; Alleen de persoon die een aangepaste weergave maakt, kan deze verwijderen.

Elke weergave is beschikbaar als een sneltoets in het dialoogvenster [!UICONTROL Custom Views] in het linkerdeelvenster.

## Een standaardweergave of aangepaste weergave toepassen

* (Standaardweergaven) Klik op **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]** \> **\[type entiteit\]**.

* (Aangepaste weergaven) In het navigatievenster aan de linkerkant:

   1. Klik in het linkerdeelvenster op de knop **[!UICONTROL Custom Views]** om het uit te vouwen.

      Weergaven worden gesorteerd op de toepasselijke entiteit.

   1. Vouw de beschikbare menu&#39;s uit.

      &quot;[!UICONTROL Universal Views]&quot; bevat aangepaste weergaven die in alle entiteitsweergaven kunnen worden gebruikt. Alle andere aangepaste weergaven worden gegroepeerd op type entiteit.

   1. Klik op de naam van de weergave.

      Als de mening universeel is of op de huidige entiteit van toepassing is, dan wordt de gegevenslijst opnieuw getoond volgens de meningsconfiguratie. Als de weergave op een andere entiteit van toepassing is, worden de gegevens voor de betreffende entiteit weergegeven volgens de weergaveconfiguratie.

## Een aangepaste weergave maken {#create-custom-view}

Aangepaste weergaven zijn alleen van toepassing op de weergaven voor campagnebeheer.

>[!NOTE]
>
>Naast de weergave-instellingen die u opgeeft voor de aangepaste weergave, wordt de huidige sorteervolgorde van kolommen ook opgeslagen.

1. Klik rechts van de werkbalk boven de gegevenstabel op de naam van de huidige weergave (die mogelijk &quot;[!UICONTROL Default]&quot;).

1. Geef de [aangepaste weergave-instellingen](#view-settings):

   1. (Optioneel) De gegevensinstellingen beschikbaar stellen in alle entiteitsweergaven (voor [!UICONTROL Campaigns], [!UICONTROL Ads], enzovoort) selecteert u **[!UICONTROL Universal View]**.

      Nadat u deze optie hebt in- of uitgeschakeld, kunt u de wijziging niet opslaan in de bestaande weergave, maar kunt u wel een nieuwe weergave maken met de wijziging.

   1. (Optioneel) Als u de weergave beschikbaar wilt maken voor alle andere gebruikers die de gegevens van de adverteerder kunnen bekijken, verplaatst u de **[!UICONTROL Shared]** schuifregelaar naar *[!UICONTROL Yes]*.

   1. (Optioneel) Op de **[!UICONTROL Columns]** wijzigt u de kolommen die beschikbaar zijn voor het tabblad, de volgorde waarin deze staan en hoe u de rijen wilt sorteren.

   1. (Optioneel) Klik op de knop **[!UICONTROL Filters]** en geeft u vervolgens op welke filters u wilt toepassen.

      Het toepassen van filters keert rijen slechts terug wanneer de waarde voor metrisch aan gespecificeerde criteria voldoet, al dan niet metrisch is inbegrepen als kolom in het rapport.

   1. (Optioneel) Klik op de knop **[!UICONTROL Date]** en wijzigt u de standaarddatuminstellingen.

   1. (Optioneel) Klik op de knop **[!UICONTROL Additional Settings]** en wijzigt u de instellingen.

1. Klik op **[!UICONTROL Save as New]**.

1. Voer de naam van de nieuwe weergave in en klik op **[!UICONTROL Save]**.

   >[!TIP]
   >
   >Gebruik een naam die u helpt het tabblad en de informatie te identificeren waarop het van toepassing is (zoals &quot;Gepauzeerde campagnes&quot; of &quot;Hoogste 50 advertenties&quot;).

### Een standaardweergave of aangepaste weergave bewerken

1. Open de weergave-instellingen:

   * (Als u de weergave al hebt toegepast) Klik rechts van de werkbalk boven de datatabel op de naam van de huidige weergave (die mogelijk &quot;[!UICONTROL Default]&quot;).

   * (Aangepaste weergaven die niet worden toegepast) Klik in het linkerdeelvenster op ![Aangepaste weergaven](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Aangepaste weergaven") om de [!UICONTROL Custom Views] -menu. Klik op de naam van de aangepaste weergave.

1. Bewerk de [weergave-instellingen](#view-settings):

   1. (Optioneel) De gegevensinstellingen in- of uitschakelen in alle weergaven van zoekentiteiten (voor [!UICONTROL Campaigns], [!UICONTROL Ad Groups], enzovoort), selecteert of deselecteert u **[!UICONTROL Universal View]**.

      U kunt de wijziging niet opslaan in de bestaande weergave, maar u kunt wel een nieuwe weergave maken met de wijziging.

   1. (Optioneel; alleen aangepaste weergaven die u hebt gemaakt) Als de weergave nog niet openbaar is, stelt u deze beschikbaar voor alle andere gebruikers die de gegevens van de adverteerder kunnen bekijken door de **[!UICONTROL Shared]** schuifregelaar naar *[!UICONTROL Yes]*.

   1. (Optioneel) Op de **[!UICONTROL Columns]** wijzigt u de kolommen die beschikbaar zijn voor het tabblad, de volgorde waarin deze staan en hoe u de rijen wilt sorteren.

   1. (Optioneel) Klik op de knop **[!UICONTROL Filters]** en bewerkt u vervolgens de filters die u wilt toepassen.

      Het toepassen van filters keert rijen slechts terug wanneer de waarde voor metrisch aan gespecificeerde criteria voldoet, al dan niet metrisch is inbegrepen als kolom in het rapport.

      >[!NOTE]
      >
      >U kunt wijzigingen in filters toepassen, maar niet opslaan in de standaardweergave-instellingen.

   1. (Optioneel) Klik op de knop **[!UICONTROL Date]** en wijzigt u de standaarddatuminstellingen.

   1. (Optioneel) Klik op de knop **[!UICONTROL Additional Settings]** en wijzigt u de instellingen.

1. Pas de instellingen toe of sla deze op:

   * Klik op **[!UICONTROL Apply]**.

     De instellingen worden toegepast op het tabblad totdat u de beheerweergave op het hoogste niveau verlaat of (indien van toepassing) [gegevens voor een andere adverteerder bekijken](/help/search-social-commerce/common-tasks/change-advertiser.md).

   * (Voor standaardweergaven en aangepaste weergaven die u hebt gemaakt) Als u de instellingen wilt opslaan in de huidige weergave, klikt u op **[!UICONTROL Save]**.

   * Als u de instellingen in een nieuwe, aangepaste weergave wilt opslaan, klikt u op **[!UICONTROL Save As]**. In de [!UICONTROL Enter New Custom View Name] voert u de naam van de nieuwe weergave in en klikt u op **[!UICONTROL Save]**.

## Een standaardweergave herstellen naar de standaardinstellingen van het systeem

Als u de standaardweergave-instellingen herstelt, verwijdert u alle instellingen die u hebt opgeslagen en past u de standaardinstellingen van het systeem opnieuw toe.

De standaardinstellingen van het systeem variëren per tabblad. Voor de meeste lusjes, toont de systeemstandaardmening gegevens voor de vorige dag voor punten in toegelaten rekeningen en die actief zijn (bijvoorbeeld, slechts actieve en groepen in actieve campagnes), met de gegevens die door kosten worden gesorteerd, en met omzettingsgegevens die op transactiedatum worden gebaseerd.

1. Klik in het linkerdeelvenster op ![Aangepaste weergaven](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Aangepaste weergaven") om de [!UICONTROL Custom Views] -menu.

   Weergaven worden gesorteerd op de toepasselijke entiteit.

1. Klik naast de weergavenaam op ![Standaardinstellingen herstellen](/help/search-social-commerce/assets/revert.png "Standaardinstellingen herstellen").

## Een aangepaste weergave verwijderen

U kunt elke aangepaste weergave verwijderen die u hebt gemaakt.

Als u een aangepaste weergave verwijdert die op het huidige tabblad is toegepast, wordt de aangepaste weergave op het tabblad weergegeven totdat u zich buiten de weergaveset bevindt (bijvoorbeeld vanuit weergaven in het deelvenster [!UICONTROL Search] aan de [!UICONTROL Reports] (indien van toepassing) wanneer u [gegevens voor een andere adverteerder bekijken](/help/search-social-commerce/common-tasks/change-advertiser.md).

1. Klik in het linkerdeelvenster op ![Aangepaste weergaven](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Aangepaste weergaven") om de [!UICONTROL Custom Views] -menu.

1. Plaats de cursor boven de naam van de aangepaste weergave en klik vervolgens op ![Verwijderen](/help/search-social-commerce/assets/delete.png "Verwijderen").

1. Klik in het bevestigingsbericht **[!UICONTROL Continue]**.

## Standaardinstellingen en aangepaste weergave-instellingen {#view-settings}

| **Tab** | **Veld** | **Beschrijving** |
| --- | --- | --- |
| [Boven alle tabbladen] | Naam | Een unieke naam voor de weergave. U kunt de naam van een standaardweergave niet bewerken. <p><b>Tip:</b> Gebruik een naam die u helpt het tabblad en de informatie te identificeren waarop het van toepassing is (zoals &quot;Gepauzeerde campagnes&quot; of &quot;Hoogste 50 advertenties&quot;). |
|   | Universele weergave | Hiermee maakt u de gegevensinstellingen beschikbaar in alle entiteitweergaven (voor campagnes, advertenties, enzovoort). De universele meningen kunnen metrische en etiketclassificatiekolommen - maar niet bezitskolommen (zoals entiteitsnaam en status) omvatten omdat zij door entiteitstype - evenals alle andere meningsattributen verschillen. Eventuele filtercriteria worden toegepast op de entiteitsweergave, indien van toepassing, en worden anders genegeerd. Alle metrische filters worden plaatselijk geëvalueerd (bijvoorbeeld, voor kliks \> 1000, tonen de meningen van Campagnes campagnes met meer dan 1000 klikken, en de mening van Groepen van de Advertentie toont ad groepen met meer dan 1000 klikken).<p>De eigenschapkolommen voor een universele weergave worden uit de standaardweergave van de entiteit gehaald. In de standaardweergave-instellingen kunt u de standaardeigenschapkolommen voor een bepaalde entiteit wijzigen.<p>Nadat u deze optie hebt in- of uitgeschakeld, kunt u de wijziging niet opslaan in de bestaande weergave, maar kunt u wel een nieuwe weergave maken met de wijziging. |
|   | Delen | (Alleen aangepaste weergaven; optioneel) Hiermee maakt u de weergave beschikbaar voor alle andere gebruikers die de gegevens van de adverteerder kunnen bekijken. Andere gebruikers kunnen de weergave niet bewerken of verwijderen, maar kunnen wel een nieuwe weergave maken op basis van de instellingen. In uw weergavelijsten is elke weergave die door een andere persoon wordt gedeeld cursief, zoals &quot;_Prestatiecampagnes_.&quot; |
| Kolommen | Geselecteerde kolommen en volgorde | De kolommen met gegevens die worden weergegeven en hun volgorde:<ul><li> (Als u een kolom wilt toevoegen) Klik in de lijst Beschikbare kolommen op een kolomnaam en sleep deze naar de lijst Geselecteerde kolommen en volgorde of klik op ![pijl-rechts](/help/search-social-commerce/assets/chevron-right.png) om het daar te verplaatsen.</li><li>(Als u de horizontale positie van een kolom wilt wijzigen) Klik in de lijst Geselecteerde kolommen en volgorde op de kolomnaam en sleep deze naar de gewenste positie of klik op ![pijl-omhoog](/help/search-social-commerce/assets/chevron-up.png) of ![pijl-omlaag](/help/search-social-commerce/assets/chevron-down.png) om het daar te verplaatsen. De bovenste kolomnaam wordt weergegeven in de linkerkolom.</li><li>(Als u een kolom wilt verwijderen) Klik in de lijst Geselecteerde kolommen en volgorde op een kolomnaam en sleep deze naar de lijst Beschikbare kolommen of klik op ![pijl-links](/help/search-social-commerce/assets/chevron-left.png) om het daar te verplaatsen.</li></ul><b>Gegevens filteren</b><p>Als u alleen een specifiek type gegevens wilt weergeven, klikt u op een van de pictogrammen naast de lijst:<ul><li>![eigenschappenpictogram](/help/search-social-commerce/assets/properties-icon.png) voor eigenschapnamen en id&#39;s voor zoekcomponenten, zoals Status</li><li>![verkeerspictogram](/help/search-social-commerce/assets/traffic-metrics-icon.png) voor standaardverkeersmetriek, zoals indrukken en klikken</li><li>![ontvangpictogram](/help/search-social-commerce/assets/revenue-metrics-icon.png) (voor conversiemetriek die voor de adverteerder wordt bijgehouden, inclusief conversie- en locatiegegevens die via Analytics zijn gesynchroniseerd)</li><li>![aangepast pictogram](/help/search-social-commerce/assets/custom-metrics-icon.png) (voor maateenheden die door de adverteerder zijn gemaakt)</li><li>![classificatiepictogram](/help/search-social-commerce/assets/classifications-icon.png) (voor labelindelingen).</li></ul> <b>Aanvullende opmerkingen:</b><ul><li>Zie &#39;Een aangepaste metrisch maken&#39;, &#39;Een aangepaste metrisch bewerken&#39; en &#39;Een aangepaste metrisch verwijderen&#39; als u nieuwe metrische gegevens wilt toevoegen, maken of bewerken.</li><li>Als het rapport gegevens voor rekeningen met verschillende valuta&#39;s omvat, dan zijn de totalen niet inbegrepen voor op monetair-gebaseerde kolommen (zoals Kosten en CPC).</li><li>U kunt [Bewerk tijdelijk de kolomset in het menu met kolomkoppen](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md), en [de kolomset bewerken en sorteren op basis van de [!UICONTROL Columns] pictogram](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![Kolommen, pictogram](/help/search-social-commerce/assets/custom-columns.png "Kolommen, pictogram")).</li></ul> |
|   | Sorteren op | De kolom waarmee de gegevens moeten worden gesorteerd. De standaardwaarde is verschillend voor elk rapporttype. |
|   | Sorteervolgorde | Of de gegevens moeten worden gesorteerd **Oplopend** of **Aflopend** bestelling. Verplaats de schuifregelaar om een optie te selecteren. |
| Filters | [Filterdefinities] | (Optioneel) Filters die op gegevens moeten worden toegepast. Wanneer filters worden toegepast, worden alleen rijen geretourneerd wanneer de waarde voor een kolom aan opgegeven criteria voldoet.<p>Voor elk filter dat moet worden toegepast:<ol><li>Selecteer een kolomnaam in het menu Filter toevoegen. De lijst omvat alle beschikbare kolommen en wordt gesorteerd door kolomtype, met bezitskolommen eerst.</li><li>Het filter in de kolom definiëren</li></ol>(Filters met invoervelden) Selecteer een operator in het tweede menu en voer de toepasselijke waarde in. Waarden zijn niet hoofdlettergevoelig. Klikken ![controlepictogram](/help/search-social-commerce/assets/select.png) als je klaar bent.<p>Als u bijvoorbeeld de kolom &quot;Kliks&quot; hebt geselecteerd en alleen rijen met meer dan 100 klikken wilt retourneren, selecteert u _\>_ en betreden `100` in het invoerveld.<p>Afhankelijk van het gegevenstype kunnen de beschikbare operatoren <i>groter dan</i>, <i>minder dan</i>, <i>equals</i>, <i>contains</i>, <i>bevat niet</i>, <i>begint met</i>, <i>eindigt met</i>,<i>geen waarde</i>, of <i>has value</i> <i>voor</i>, <i>na</i>,of <i>geen datum</i>.<p>(Filters zonder invoervelden) Klik op ![pijl omlaag](/help/search-social-commerce/assets/arrow-down-expand.png) naast het menu Lijstitems selecteren en selecteer vervolgens de selectievakjes naast elke waarde die u wilt opnemen. Klikken ![controlepictogram](/help/search-social-commerce/assets/select.png) als je klaar bent.<p><b>Opmerkingen:</b><ul><li>U kunt wijzigingen in filters toepassen, maar niet opslaan in de standaardweergave-instellingen.</li><li>U kunt ook [de toepasselijke filters tijdelijk wijzigen](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) in de weergave.</li></ul> |
|   | Inclusief rijen met alleen prestatiegegevens | (Alleen in de weergaven Groepen, Trefwoord, Productgroepen, Plaatsen en Automatische doelen toevoegen) <p>Hiermee worden alleen rijen opgenomen met prestatiegegevens gedurende de opgegeven datums. Deze optie is standaard geselecteerd om de laadtijd van de pagina te verkorten. <p><b>Waarschuwing</b>: Als u de selectie van de optie ongedaan maakt en de weergave veel entiteiten zonder prestatiegegevens bevat, duurt het langer om de gegevens weer te geven.<p> <b>Opmerking</b>: U kunt wijzigingen in filters toepassen, maar niet opslaan in de standaardweergave-instellingen. In standaardweergaven worden altijd alleen entiteiten met prestatiegegevens weergegeven. |
| Datum | Datumbereik | (Als Inclusief datumbereik is geselecteerd)<p>Het datumbereik waarvoor gegevens moeten worden gegenereerd. Kies één optie:<ul><li><i>[Vooraf ingesteld bereik]</i>: Een lijst met veelvoorkomende tijdtoenamen, variërend van <i>Vandaag</i> tot <i>Afgelopen 180 dagen</i>. Kies een optie in de lijst. De standaardwaarde is <i>Gisteren</i>. Opmerking: <i>Vorige maand</i>, <i>Laatste 3 maanden</i>, en <i>Laatste 6 maanden</i> gegevens voor de voorafgaande kalendermaanden weergeven.</li><li><i>Aangepast datumbereik:</i> Geef de begin- en einddatum op. Voer datums in in de notatie MM/DD/JJJJ of M/D/JJJJ, of klik op ![kalenderpictogram](/help/search-social-commerce/assets/calendar.png) naast een veld en selecteer een datum.</li></ul> |
|   | Vergelijking | Vergelijkt gegevens voor het opgegeven datumbereik met gegevens voor een tweede datumbereik. Wanneer u deze optie selecteert, worden er twee extra kolommen toegevoegd voor elke gewone gegevenskolom. Bijvoorbeeld, in plaats van slechts één kolom voor &quot;Inpressies,&quot;omvat het rapport kolommen voor &quot;Waaier 1 van Inpressies,&quot;Waaier 2 van de Indrukken,&quot;en &quot;Verschil van Impressies.&quot;<p><b>Opmerkingen:</b><ul><li>De verschilkolom wordt niet getoond voor afgeleide metriek.</li><li>Rapporten die grote datumbereiken vergelijken, kunnen langer duren om te genereren.</li></ul> |
|   | Vergelijkingsindeling | Hoe te om het verschil tussen gegevens in de twee geselecteerde datumwaaiers in uit te drukken &quot;[_Gegevensveld_] Verschil&quot;. Kies één optie:<ul><li><i>Variantie</i> (standaard): geeft het verschil weer als een numerieke waarde.</li><li><i>% wijzigen</i>: geeft het verschil weer als een percentage.</li></ul> |
| Aanvullende instellingen | Standaardinstellingen gebruiken | Past de attributie-instellingen toe die zijn opgegeven in de conversie-attributie-instellingen op adverteerderniveau. |
|   | Attributieregel | (Adverteerders met de Adobe Advertising alleen service voor het bijhouden van pixelconversies) Op het tabblad Hoe kunt u conversiegegevens — mogelijk over meerdere advertentiekanalen en portfolio&#39;s — toewijzen in een reeks gebeurtenissen die tot conversie leiden. Standaard is de regel die is opgegeven in de conversie-attributie-instellingen op adverteerderniveau geselecteerd.<ul><li> <i>Eerste gebeurtenis</i>: Kenmerkt de omzetting aan de eerste betaalde klik in de reeks binnen het klikterugkijkvenster van de adverteerder of, als er geen betaalde kliks voorkwamen, aan de laatste indruk binnen het venster van de de imitatieraadpleging van de adverteerder.</li><li><i>Dikte eerste gebeurtenis meer</i>: Kenmerkt de omzetting aan alle gebeurtenissen in de reeks die binnen het de klikterugkijkvenster van de adverteerder en het venster van de impresraadpleging voorkwamen, maar geeft het meeste gewicht aan de eerste gebeurtenis en opeenvolgend minder gewicht aan de volgende gebeurtenissen. Wanneer de conversie wordt voorafgegaan door zowel betaalde klikken als indrukken, wordt het opgegeven gewicht waarmee de indruk wordt overschreven, verder toegepast op de afbeeldingen. Wanneer de conversie alleen wordt voorafgegaan door indrukken, worden de indrukkingen gewogen volgens het doorkijkgewicht van de adverteerder in plaats van volgens het gewicht dat de indruk overschrijft.</li><li><i>Even verdelen</i>: Kenmerkt de omzetting gelijk aan elke gebeurtenis in de reeks die binnen het klikterugkijkvenster van de adverteerder en het venster van de imitatieraadpleging voorkwam. Wanneer de conversie wordt voorafgegaan door zowel betaalde klikken als indrukken, wordt het opgegeven gewicht waarmee de indruk wordt overschreven, verder toegepast op de afbeeldingen. Wanneer de conversie alleen wordt voorafgegaan door indrukken, worden de indrukkingen gewogen volgens het doorkijkgewicht van de adverteerder in plaats van volgens het gewicht dat de indruk overschrijft.</li><li><i>Dikte laatste gebeurtenis meer</i>: Kenmerkt de omzetting aan alle gebeurtenissen in de reeks die binnen het de klikterugkijkvenster van de adverteerder en het venster van de impresuslookback voorkwamen, maar geeft het meeste gewicht aan de laatste gebeurtenis en opeenvolgend minder gewicht aan de voorafgaande gebeurtenissen. Wanneer de conversie wordt voorafgegaan door zowel betaalde klikken als indrukken, wordt het opgegeven gewicht waarmee de indruk wordt overschreven, verder toegepast op de afbeeldingen. Wanneer de conversie alleen wordt voorafgegaan door indrukken, worden de indrukkingen gewogen volgens het doorkijkgewicht van de adverteerder in plaats van volgens het gewicht dat de indruk overschrijft.</li><li><i>Laatste gebeurtenis</i> (standaard): hiermee wordt de omzetting in de laatst betaalde klik in de reeks binnen het klikterugkijkvenster van de adverteerder of, als er geen betaalde kliks optraden, aan de laatste indruk binnen het imitatievenster van de adverteerder toegeschreven.</li><li><i>U-gevormd</i>: Kenmerkt de omzetting aan alle gebeurtenissen in de reeks die binnen het de klikterugkijkvenster van de adverteerder en het venster van de impresuslookback voorkwamen, maar geeft het meeste gewicht aan de eerste gebeurtenis en laatste gebeurtenissen, met opeenvolgend minder gewicht aan de gebeurtenissen in het midden van de omzettingsweg. Wanneer de conversie wordt voorafgegaan door zowel betaalde klikken als indrukken, wordt het opgegeven gewicht waarmee de indruk wordt overschreven, verder toegepast op de afbeeldingen. Wanneer de conversie alleen wordt voorafgegaan door indrukken, worden de indrukkingen gewogen volgens het doorkijkgewicht van de adverteerder in plaats van volgens het gewicht dat de indruk overschrijft.</li></ul><p><b>Opmerkingen:</b><ul><li>Alle attributieregels naast Last Event zijn alleen beschikbaar voor adverteerders met Adobe Advertising klik bijhouden en conversie via Adobe Advertising of Adobe Analytics (met integratie van Analytics).</li><li>De regels van het attribuut zijn op kliks op betaalde advertenties in om het even welk kanaal van toepassing. Ze zijn niet van toepassing op afbeeldingen voor betaalde zoekopdrachten, die niet op gebeurtenisniveau kunnen worden bijgehouden.</li><li>Wanneer u conversiegegevens rapporteert met een toewijzingsregel behalve een van de regels voor laatste gebeurtenis, kunnen de gebeurtenissen die de conversie hebben veroorzaakt zich voordoen in meerdere portfolio&#39;s. In dat geval bevat de weergave alleen gegevens voor de conversie wanneer de advertenties of trefwoorden in die portfolio&#39;s in de weergave zijn opgenomen.</li><li>Voor standaardmeningen, adviseren wij dat u de standaardattributieregel houdt, die wordt gebruikt om te berekenen [objectieve waarde](/help/search-social-commerce/glossary.md#o-p) (voorheen &quot;gewogen inkomsten&quot; genoemd) voor elke biedeenheid tijdens de optimalisatie van de inschrijvingen.</li></ul> |
|   | Conversies op basis van | Conversiegegevens rapporteren:<ul><li><i>Transactiedatum</i> (de standaardinstelling): transacties waarvan de transactiedatum tijdens de opgegeven tijdsperiode is opgetreden, bekijken. Dit geeft aan hoeveel inkomsten binnen de opgegeven periode zijn verdiend.</li><li><i>Klikdatum</i>: U kunt als volgt de transacties weergeven die het resultaat zijn van een klik die tijdens de opgegeven periode is opgetreden. Wanneer een portfolio aanzienlijke vertraging heeft tussen klikken en transacties, is deze optie handig voor het berekenen van de historische opbrengst per klik voor de portfolio, die het inkomstengedrag aangeeft dat in de loop der tijd moet worden verwacht. |
