---
title: Standaard- en aangepaste weergaven beheren
description: Leer hoe u uw standaardweergaven en aangepaste weergaven aanpast.
exl-id: 1f240760-6186-471f-bf1a-3e0ee13ce550
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 17dfff36a3f3b62be0d8c24d24b222d43cd97d4a
workflow-type: tm+mt
source-wordcount: '2917'
ht-degree: 0%

---

# Standaard- en aangepaste weergaven beheren

<!-- Doesn't include instructions for legacy Portfolios or Reports views -->

Met de standaardweergaven en aangepaste weergaven kunt u de prestatiegegevens aanpassen die worden weergegeven in de gegevensweergaven van de zoekcampagne. Tot de weergave-instellingen behoren de kolommen die moeten worden opgenomen, de filters, het datumbereik, de conversieattributie-instellingen en andere geavanceerde instellingen. U kunt de instellingen tijdelijk toepassen of ze opslaan. (Uitzondering: u kunt filters niet opslaan voor standaardweergaven.) Elke standaardweergave en standaardweergave is alleen van toepassing op een specifieke weergave (zoals [!UICONTROL Portfolios] of [!UICONTROL Campaigns] ) en een specifieke advertentieaccount. In de oudere gebruikersinterface is elke universele aangepaste weergave van toepassing op verschillende entiteitsweergaven voor een specifieke adverteerder en kan deze daarom geen eigenschapskolommen (zoals entiteitsnaam of -status) opnemen, die per entiteitstype verschillen.

De standaardweergaven worden standaard weergegeven wanneer u zich aanmeldt. U kunt aanvullende aangepaste weergaven maken en deze op elk gewenst moment toepassen. U kunt desgewenst elke aangepaste weergave delen die u maakt met alle andere gebruikers die de gegevens van de adverteerder kunnen bekijken.<!-- I no longer see this in the legacy CM views - why? --> in uw meningslijsten, elke mening die een andere persoon deelt is cursief, zoals &quot;*best-presterende Campagnes*.&quot; Alleen de persoon die een aangepaste weergave maakt, kan deze verwijderen.

In de oudere gebruikersinterface is elke weergave beschikbaar als een sneltoets in de sectie [!UICONTROL Custom Views] van het linkerdeelvenster.

## Een standaardweergave of aangepaste weergave toepassen

### (Nieuwe UI) Pas een gebrek of douanemening op een beheersmening toe

1. Boven de gegevenslijst, klik de naam van de momenteel-toegepaste mening (![ Mening ](/help/search-social-commerce/assets/view.png " Mening ")).

1. Klik zo nodig op een van de tabbladen ( [!UICONTROL All Views] , [!UICONTROL Private] , [!UICONTROL Shared by Me] en [!UICONTROL From Others] ) om de weergave te zoeken.

1. Plaats de cursor op de naam van de weergave en klik op **[!UICONTROL Apply]** .

### (Verouderde UI) Pas een gebrek of douanemening op een mening van het campagnebeheer toe

* (Standaardweergaven) Klik in het hoofdmenu op **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]** . In submenus, klik **[!UICONTROL Live]** \> **\ [entiteittype \]**.

* (Aangepaste weergaven) In het navigatievenster aan de linkerkant:

   1. Klik in het linkerdeelvenster op het menu **[!UICONTROL Custom Views]** om het uit te vouwen.

      Weergaven worden gesorteerd op de toepasselijke entiteit.

   1. Vouw de beschikbare menu&#39;s uit.

      &quot;[!UICONTROL Universal Views]&quot;omvat douanemeningen die over alle entiteitmeningen kunnen worden gebruikt. Alle andere aangepaste weergaven worden gegroepeerd op type entiteit.

   1. Klik op de naam van de weergave.

      Als de mening universeel is of op de huidige entiteit van toepassing is, dan wordt de gegevenslijst opnieuw getoond volgens de meningsconfiguratie. Als de weergave op een andere entiteit van toepassing is, worden de gegevens voor de betreffende entiteit weergegeven volgens de weergaveconfiguratie.

## Een aangepaste weergave maken {#create-custom-view}

<!--
## (New UI) Create a custom view from management views
-->

## (Verouderde gebruikersinterface) Een aangepaste weergave maken op basis van weergaven voor campagnebeheer

Aangepaste weergaven zijn alleen van toepassing op de weergaven voor campagnebeheer.

>[!NOTE]
>
>Naast de weergave-instellingen die u opgeeft voor de aangepaste weergave, wordt de huidige sorteervolgorde van kolommen ook opgeslagen.

1. Op de rechterkant van de toolbar boven de gegevenslijst, klik de naam van de huidige mening (die &quot;[!UICONTROL Default]&quot;zou kunnen zijn).

1. Specificeer de [ montages van de douanemening ](#view-settings):

   1. (Optioneel) Selecteer [!UICONTROL Campaigns] als u de gegevensinstellingen in alle entiteitsweergaven beschikbaar wilt maken (bijvoorbeeld [!UICONTROL Ads] , **[!UICONTROL Universal View]** , enzovoort).

      Nadat u deze optie hebt in- of uitgeschakeld, kunt u de wijziging niet opslaan in de bestaande weergave, maar kunt u wel een nieuwe weergave maken met de wijziging.

   1. (Optioneel) Als u de weergave beschikbaar wilt maken voor alle andere gebruikers die de gegevens van de adverteerder kunnen weergeven, verplaatst u de schuifregelaar **[!UICONTROL Shared]** naar *[!UICONTROL Yes]* .

   1. (Optioneel) Wijzig op het tabblad **[!UICONTROL Columns]** de kolommen die beschikbaar zijn voor het tabblad, hun volgorde en hoe u de rijen wilt sorteren.

   1. (Optioneel) Klik op de tab **[!UICONTROL Filters]** en geef de filters op die u wilt toepassen.

      Het toepassen van filters keert rijen slechts terug wanneer de waarde voor metrisch aan gespecificeerde criteria voldoet, al dan niet metrisch is inbegrepen als kolom in het rapport.

   1. (Optioneel) Klik op het tabblad **[!UICONTROL Date]** en wijzig de standaarddatuminstellingen.

   1. (Optioneel) Klik op de tab **[!UICONTROL Additional Settings]** en wijzig de instellingen.

1. Klik op **[!UICONTROL Save as New]**.

1. Voer de naam van de nieuwe weergave in en klik op **[!UICONTROL Save]** .

   >[!TIP]
   >
   >Gebruik een naam die u helpt het tabblad en de informatie te identificeren waarop het van toepassing is (zoals &quot;Gepauzeerde campagnes&quot; of &quot;Hoogste 50 advertenties&quot;).

### Een standaardweergave of aangepaste weergave bewerken

1. Open de weergave-instellingen:

   * (Als u reeds de mening) op de rechterkant van de toolbar boven de gegevenslijst hebt toegepast, klik de naam van de huidige mening (die &quot;[!UICONTROL Default]&quot;zou kunnen zijn).

   * (De meningen van de Douane die niet worden toegepast) in het linkerpaneel, klik ![ de Mening van de Douane ](/help/search-social-commerce/assets/custom-views-left-rail_icon.png " om het ") menu uit te breiden. [!UICONTROL Custom Views] Klik op de naam van de aangepaste weergave.

1. Bewerk de [ meningsmontages ](#view-settings):

   1. (Optioneel) U kunt de gegevensinstellingen in- of uitschakelen in alle weergaven van de zoekentiteit (bijvoorbeeld [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] ) door **[!UICONTROL Universal View]** in of uit te schakelen.

      U kunt de wijziging niet opslaan in de bestaande weergave, maar u kunt wel een nieuwe weergave maken met de wijziging.

   1. (Optioneel; alleen aangepaste weergaven die u hebt gemaakt) Als de weergave nog niet openbaar is, stelt u deze beschikbaar voor alle andere gebruikers die de gegevens van de adverteerder kunnen weergeven door de schuifregelaar **[!UICONTROL Shared]** naar *[!UICONTROL Yes]* te verplaatsen.

   1. (Optioneel) Wijzig op het tabblad **[!UICONTROL Columns]** de kolommen die beschikbaar zijn voor het tabblad, hun volgorde en hoe u de rijen wilt sorteren.

   1. (Optioneel) Klik op de tab **[!UICONTROL Filters]** en bewerk vervolgens de filters die u wilt toepassen.

      Het toepassen van filters keert rijen slechts terug wanneer de waarde voor metrisch aan gespecificeerde criteria voldoet, al dan niet metrisch is inbegrepen als kolom in het rapport.

      >[!NOTE]
      >
      >U kunt wijzigingen in filters toepassen, maar niet opslaan in de standaardweergave-instellingen.

   1. (Optioneel) Klik op het tabblad **[!UICONTROL Date]** en wijzig de standaarddatuminstellingen.

   1. (Optioneel) Klik op de tab **[!UICONTROL Additional Settings]** en wijzig de instellingen.

1. Pas de instellingen toe of sla deze op:

   * Klik op **[!UICONTROL Apply]** als u de instellingen tijdelijk wilt toepassen zonder ze op te slaan in de weergave.

     De montages worden toegepast op het lusje tot u zich vanaf de top-level beheersmening of (indien van toepassing) [ meningsgegevens voor een andere adverteerder ](/help/search-social-commerce/common-tasks/change-advertiser.md) beweegt.

   * (Voor standaardweergaven en aangepaste weergaven die u hebt gemaakt) Klik op **[!UICONTROL Save]** om de instellingen op te slaan in de huidige weergave.

   * Klik op **[!UICONTROL Save As]** om de instellingen op te slaan in een nieuwe, aangepaste weergave. Voer in het [!UICONTROL Enter New Custom View Name] -venster de naam van de nieuwe weergave in en klik op **[!UICONTROL Save]** .

## Een standaardweergave herstellen naar de standaardinstellingen van het systeem

Als u de standaardweergave-instellingen herstelt, verwijdert u alle instellingen die u hebt opgeslagen en past u de standaardinstellingen van het systeem opnieuw toe.

De standaardinstellingen van het systeem variëren per tabblad. Voor de meeste lusjes, toont de systeemstandaardmening gegevens voor de vorige dag voor punten in toegelaten rekeningen en die actief zijn (bijvoorbeeld, slechts actieve en groepen in actieve campagnes), met de gegevens die door kosten worden gesorteerd, en met omzettingsgegevens die op transactiedatum worden gebaseerd.

1. In het linkerpaneel, klik ![ de Mening van de Douane van 0} ](/help/search-social-commerce/assets/custom-views-left-rail_icon.png " om het ") menu uit te breiden.[!UICONTROL Custom Views]

   Weergaven worden gesorteerd op de toepasselijke entiteit.

1. Naast de meningsnaam, klik ![ herstellen aan standaardmontages ](/help/search-social-commerce/assets/restore.png " herstellen aan standaardmontages ").

## Een aangepaste weergave verwijderen

U kunt elke aangepaste weergave verwijderen die u hebt gemaakt.

Als u een douanemening schrapt die op het huidige lusje wordt toegepast, blijft het lusje de douanemening tonen tot u zich buiten de meningsreeks (bijvoorbeeld, van meningen binnen het [!UICONTROL Search] menu aan het [!UICONTROL Reports] menu) of (wanneer toepasselijk) beweegt wanneer u [ meningsgegevens voor een andere adverteerder ](/help/search-social-commerce/common-tasks/change-advertiser.md) bekijkt.

1. In het linkerpaneel, klik ![ de Mening van de Douane van 0} ](/help/search-social-commerce/assets/custom-views-left-rail_icon.png " om het ") menu uit te breiden.[!UICONTROL Custom Views]

1. Houd de curseur over de naam van de douanemening, en klik dan ![ Schrapping ](/help/search-social-commerce/assets/delete.png " ").

1. Klik in het bevestigingsbericht op **[!UICONTROL Continue]** .

## Standaardinstellingen en aangepaste weergave-instellingen {#view-settings}

| **Lusje** | **Gebied** | **Beschrijving** |
| --- | --- | --- |
| [ Boven alle lusjes ] | Naam | Een unieke naam voor de weergave. U kunt de naam van een standaardweergave niet bewerken.<p><b> Uiteinde:</b> gebruik een naam die u helpt het lusje en de informatie identificeren waarop het van toepassing is (zoals &quot;Gepauzeerde Campagnes&quot;of &quot;Hoogste 50 Advertentie&quot;). |
|   | Universele weergave | Hiermee maakt u de gegevensinstellingen beschikbaar in alle entiteitweergaven (voor campagnes, advertenties, enzovoort). De universele meningen kunnen metrische en etiketclassificatiekolommen - maar niet bezitskolommen (zoals entiteitsnaam en status) omvatten omdat zij door entiteitstype - evenals alle andere meningsattributen verschillen. Eventuele filtercriteria worden toegepast op de entiteitsweergave, indien van toepassing, en worden anders genegeerd. Alle metrische filters worden plaatselijk geëvalueerd (bijvoorbeeld, voor kliks \> 1000, tonen de meningen van Campagnes campagnes met meer dan 1000 klikken, en de mening van Groepen van de Advertentie toont ad groepen met meer dan 1000 klikken).<p>De eigenschapkolommen voor een universele weergave worden uit de standaardweergave van de entiteit gehaald. In de standaardweergave-instellingen kunt u de standaardeigenschapkolommen voor een bepaalde entiteit wijzigen.<p>Nadat u deze optie hebt in- of uitgeschakeld, kunt u de wijziging niet opslaan in de bestaande weergave, maar kunt u wel een nieuwe weergave maken met de wijziging. |
|   | Delen | (Alleen aangepaste weergaven; optioneel) Hiermee maakt u de weergave beschikbaar voor alle andere gebruikers die de gegevens van de adverteerder kunnen bekijken. Andere gebruikers kunnen de weergave niet bewerken of verwijderen, maar ze kunnen wel een nieuwe weergave maken op basis van de instellingen. In uw meningslijsten, wordt elke mening die een andere persoon deelt cursief, zoals &quot;_best-presterende Campagnes_.&quot; |
| Kolommen | Geselecteerde kolommen en volgorde | De kolommen met gegevens die worden weergegeven en hun volgorde:<ul><li> (Om een kolom toe te voegen) in de Beschikbare lijst van Kolommen, klik een kolomnaam, en dan of sleep het in de Geselecteerde Kolommen &amp; het Bestel- lijst of klik ![ juiste pijl ](/help/search-social-commerce/assets/chevron-right.png) om het daar te bewegen.</li><li>(Om de horizontale positie van een kolom) in de Geselecteerde Kolommen &amp; het Bestel- lijst te veranderen, klik de kolomnaam, en of sleep het dan aan de gewenste positie of klik ![ omhoog pijl ](/help/search-social-commerce/assets/chevron-up.png) of ![ benedenpijl ](/help/search-social-commerce/assets/chevron-down.png) om het daar te bewegen. De bovenste kolomnaam wordt weergegeven in de linkerkolom.</li><li>(Om een kolom) in de Geselecteerde Kolommen &amp; het Bestel- lijst te verwijderen, klik een kolomnaam, en dan of sleep het in de Beschikbare lijst van Kolommen of klik ![ verlaten pijl ](/help/search-social-commerce/assets/chevron-left.png) om het daar te bewegen.</li></ul><b> gegevens van de Filter </b><p>Als u alleen een specifiek type gegevens wilt weergeven, klikt u op een van de pictogrammen naast de lijst:<ul><li>![ eigenschappen pictogram ](/help/search-social-commerce/assets/properties-icon.png) voor bezitsnamen en identiteitskaarts voor onderzoekscomponenten, zoals Status</li><li>![ verkeerspictogram ](/help/search-social-commerce/assets/traffic-metrics-icon.png) voor standaardverkeersmetriek, zoals impressies en kliks</li><li>![ opbrengstpictogram ](/help/search-social-commerce/assets/revenue-metrics-icon.png) (voor omzettingsmetriek die voor adverteerder, met inbegrip van omzetting en de metriek van de plaatsovereenkomst wordt bijgehouden die van Analytics wordt gesynchroniseerd)</li><li>![ douanepictogram ](/help/search-social-commerce/assets/custom-metrics-icon.png) (voor douane afgeleide metriek die door adverteerder wordt gecreeerd)</li><li>![ classificatiepictogram ](/help/search-social-commerce/assets/classifications-icon.png) (voor etiketclassificaties).</li></ul> <b> Extra nota&#39;s:</b><ul><li>Zie &#39;Een aangepaste metrisch maken&#39;, &#39;Een aangepaste metrisch bewerken&#39; en &#39;Een aangepaste metrisch verwijderen&#39; als u nieuwe metrische gegevens wilt toevoegen, maken of bewerken.</li><li>Als het rapport gegevens voor rekeningen met verschillende valuta&#39;s omvat, dan zijn de totalen niet inbegrepen voor op monetair-gebaseerde kolommen (zoals Kosten en CPC).</li><li>U kunt [ tijdelijk de kolom uitgeven die van het menu van de kolomrubriek ](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md) wordt geplaatst, en [ uitgeeft en de kolomreeks van het [!UICONTROL Columns] pictogram ](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md) sorteert. (![ pictogram van Kolommen ](/help/search-social-commerce/assets/custom-columns.png " pictogram van Kolommen ")).</li></ul> |
|   | Sorteren op | De kolom waarmee de gegevens moeten worden gesorteerd. De standaardwaarde is verschillend voor elk rapporttype. |
|   | Sorteervolgorde | Of om de gegevens in **Te sorteren die** of **** orde stijgen. Verplaats de schuifregelaar om een optie te selecteren. |
| Filters | [ definities van de Filter ] | (Optioneel) Filters die op gegevens moeten worden toegepast. Wanneer filters worden toegepast, worden alleen rijen geretourneerd wanneer de waarde voor een kolom aan opgegeven criteria voldoet.<p>Voor elk filter dat moet worden toegepast:<ol><li>Selecteer een kolomnaam in het menu Filter toevoegen. De lijst omvat alle beschikbare kolommen en wordt gesorteerd door kolomtype, met bezitskolommen eerst.</li><li>Het filter in de kolom definiëren</li></ol>(Filters met invoervelden) Selecteer een operator in het tweede menu en voer de toepasselijke waarde in. Waarden zijn niet hoofdlettergevoelig. Klik ![ controlepictogram ](/help/search-social-commerce/assets/select.png) wanneer u wordt gedaan.<p>Bijvoorbeeld, als u de kolom &quot;van Klikken&quot;hebt geselecteerd en slechts rijen met meer dan 100 klikken wilt terugkeren, dan selecteer _\>_ en ga `100` op het inputgebied in.<p>Afhankelijk van het gegevenstype, kunnen de beschikbare exploitanten <i> groter dan </i> omvatten, <i> minder dan </i>, <i> gelijken </i>, <i> bevat </i>, <i> bevat niet </i>, <i> begint met </i>, <i> beëindigt met </i>, <i> geen waarde </i>, of <i>} heeft waarde </i> <i> vóór </i>, <i> na </i>, of <i> geen datum </i>.<p>(Filters zonder inputgebieden) klik ![ pijl neer ](/help/search-social-commerce/assets/arrow-down-expand.png) naast het Uitgezochte menu van lijstpunten, en selecteer dan de controledozen naast elke te omvatten waarde. Klik ![ controlepictogram ](/help/search-social-commerce/assets/select.png) wanneer u wordt gedaan.<p><b> Nota&#39;s:</b><ul><li>U kunt wijzigingen in filters toepassen, maar niet opslaan in de standaardweergave-instellingen.</li><li>U kunt ook [ tijdelijk de toepasselijke filters ](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) binnen de mening veranderen.</li></ul> |
|   | Inclusief rijen met alleen prestatiegegevens | (Alleen in de weergaven Groepen, Trefwoord, Productgroepen, Plaatsen en Automatische doelen toevoegen) <p>Hiermee worden alleen rijen opgenomen met prestatiegegevens gedurende de opgegeven datums. Deze optie is standaard geselecteerd om de laadtijd van de pagina te verkorten. <p><b> Waarschuwing </b>: Als u de optie schrapt en de mening vele entiteiten zonder prestatiesgegevens omvat, duurt het langer om te worden getoond.<p> <b> Nota </b>: U kunt veranderingen in filters op uw standaardmeningsmontages toepassen maar niet opslaan. In standaardweergaven worden altijd alleen entiteiten met prestatiegegevens weergegeven. |
| Datum | Datumbereik | (Als Inclusief datumbereik is geselecteerd)<p>Het datumbereik waarvoor gegevens moeten worden gegenereerd. Kies één optie:<ul><li><i>[ vooraf ingestelde waaier ]</i>: Een lijst van gemeenschappelijke tijdtoename, die zich van <i> vandaag </i> aan <i> Laatste 180 Dagen </i> uitstrekken. Kies één van de lijst; het gebrek is <i> Gisteren </i>. Nota: <i> Vorige Maand </i>, <i> Laatste 3 Maanden </i>, en <i> Laatste 6 Maanden </i> tonen gegevens voor de vorige kalendermaanden.</li><li><i> de Waaier van de Datum van de Douane:</i> specificeer de begindatum en einddatum. Ga data in het formaat MM/DD/JJJJ of M/D/JJJJ in, of klik ![ kalenderpictogram ](/help/search-social-commerce/assets/calendar.png) naast een gebied en selecteer een datum.</li></ul> |
|   | Vergelijking | Vergelijkt gegevens voor het opgegeven datumbereik met gegevens voor een tweede datumbereik. Wanneer u deze optie selecteert, worden er twee extra kolommen toegevoegd voor elke gewone gegevenskolom. Bijvoorbeeld, in plaats van slechts één kolom voor &quot;Inpressies,&quot;omvat het rapport kolommen voor &quot;Waaier 1 van Inpressies,&quot;Waaier 2 van de Indrukken,&quot;en &quot;Verschil van Impressies.&quot;<p><b> Nota&#39;s:</b><ul><li>De verschilkolom wordt niet getoond voor afgeleide metriek.</li><li>Rapporten die grote datumbereiken vergelijken, kunnen langer duren om te genereren.</li></ul> |
|   | Vergelijkingsindeling | Hoe te om het verschil tussen gegevens in de twee geselecteerde datumwaaiers in &quot;[_het gebied van Gegevens_] Verschil&quot;kolom uit te drukken. Kies één optie:<ul><li><i> Variantie </i> (het gebrek): Toont het verschil als numerieke waarde.</li><li><i>% verandering </i>: toont het verschil als percentage.</li></ul> |
| Aanvullende instellingen | Standaardinstellingen gebruiken | Past de attributie-instellingen toe die zijn opgegeven in de conversie-attributie-instellingen op adverteerderniveau. |
|   | Attributieregel | (Adverteerders met alleen de Adobe Advertising-service voor het bijhouden van pixelconversies) Op het tabblad Hoe kunt u conversiegegevens — mogelijk over meerdere advertentiekanalen en portfolio&#39;s — toewijzen in een reeks gebeurtenissen die tot conversie leiden. Standaard is de regel die is opgegeven in de conversie-attributie-instellingen op adverteerderniveau geselecteerd.<ul><li> <i> Eerste Gebeurtenis </i>: Attributes de omzetting aan de eerste betaalde klik in de reeks binnen het de klikterugkijkvenster van de adverteerder of, als geen betaalde kliks voorkwam, aan de laatste indruk binnen het venster van de imitatieraadpleging van de adverteerder.</li><li><i> Eerste Gebeurtenis van het Gewicht Meer </i>: Attributes de omzetting aan alle gebeurtenissen in de reeks die binnen het de klikterugkijkvenster van de adverteerder en het venster van de impresraadpleging voorkwamen, maar geeft het meeste gewicht aan de eerste gebeurtenis en opeenvolgend minder gewicht aan de volgende gebeurtenissen. Wanneer de conversie wordt voorafgegaan door zowel betaalde klikken als indrukken, wordt het opgegeven gewicht waarmee de indruk wordt overschreven, verder toegepast op de afbeeldingen. Wanneer de conversie alleen wordt voorafgegaan door indrukken, worden de indrukkingen gewogen volgens het doorkijkgewicht van de adverteerder in plaats van volgens het gewicht dat de indruk overschrijft.</li><li><i> Zelfs Distributie </i>: Attributen evenzeer de omzetting aan elke gebeurtenis in de reeks die binnen het de klikterugkijkvenster van de adverteerder en het venster van de imitatieraadpleging voorkwam. Wanneer de conversie wordt voorafgegaan door zowel betaalde klikken als indrukken, wordt het opgegeven gewicht waarmee de indruk wordt overschreven, verder toegepast op de afbeeldingen. Wanneer de conversie alleen wordt voorafgegaan door indrukken, worden de indrukkingen gewogen volgens het doorkijkgewicht van de adverteerder in plaats van volgens het gewicht dat de indruk overschrijft.</li><li><i> Dikte Laatste Gebeurtenis meer </i>: Attributes de omzetting aan alle gebeurtenissen in de reeks die binnen het de klikterugkijkvenster van de adverteerder en het venster van de imitatieraadpleging voorkwamen, maar geeft het meeste gewicht aan de laatste gebeurtenis en opeenvolgend minder gewicht aan de voorafgaande gebeurtenissen. Wanneer de conversie wordt voorafgegaan door zowel betaalde klikken als indrukken, wordt het opgegeven gewicht waarmee de indruk wordt overschreven, verder toegepast op de afbeeldingen. Wanneer de conversie alleen wordt voorafgegaan door indrukken, worden de indrukkingen gewogen volgens het doorkijkgewicht van de adverteerder in plaats van volgens het gewicht dat de indruk overschrijft.</li><li><i> Laatste Gebeurtenis </i> (het gebrek): Attributes de omzetting aan de laatste betaalde klik in de reeks binnen het de klikterugkijkvenster van de adverteerder of, als geen betaalde kliks voorkwam, aan de laatste indruk binnen het de impotraadpleging van de adverteerder venster.</li><li><i> u-vormig </i>: Attributes de omzetting aan alle gebeurtenissen in de reeks die binnen het de klikterugkijkvenster en de venster van de impresraadpleging van de adverteerder voorkwamen, maar geeft het meeste gewicht aan de eerste gebeurtenis en laatste gebeurtenissen, met opeenvolgend minder gewicht aan de gebeurtenissen in het midden van de omzettingsweg. Wanneer de conversie wordt voorafgegaan door zowel betaalde klikken als indrukken, wordt het opgegeven gewicht waarmee de indruk wordt overschreven, verder toegepast op de afbeeldingen. Wanneer de conversie alleen wordt voorafgegaan door indrukken, worden de indrukkingen gewogen volgens het doorkijkgewicht van de adverteerder in plaats van volgens het gewicht dat de indruk overschrijft.</li></ul><p><b> Nota&#39;s:</b><ul><li>Alle toewijzingsregels behalve Laatste gebeurtenis zijn alleen beschikbaar voor adverteerders met Adobe Advertising klik bijhouden en de conversie wordt bijgehouden vanuit Adobe Advertising of Adobe Analytics (met integratie van Analytics).</li><li>De regels van het attribuut zijn op kliks op betaalde advertenties in om het even welk kanaal van toepassing. Ze zijn niet van toepassing op afbeeldingen voor betaalde zoekopdrachten, die niet op gebeurtenisniveau kunnen worden bijgehouden.</li><li>Wanneer u conversiegegevens rapporteert met een toewijzingsregel behalve een van de regels voor laatste gebeurtenis, kunnen de gebeurtenissen die de conversie hebben veroorzaakt zich voordoen in meerdere portfolio&#39;s. In dat geval bevat de weergave alleen gegevens voor de conversie wanneer de advertenties of trefwoorden in die portfolio&#39;s in de weergave zijn opgenomen.</li><li>Voor standaardmeningen, adviseren wij dat u de standaardattributieregel houdt, die wordt gebruikt om de [ objectieve waarde ](/help/search-social-commerce/glossary.md#o-p) (vroeger genoemd &quot;gewogen opbrengst&quot;) voor elke biedingseenheid tijdens biedingsoptimalisering te berekenen.</li></ul> |
|   | Conversies op basis van | Conversiegegevens rapporteren:<ul><li><i> de datum van de Transactie </i> (het gebrek): Om transacties te zien waarvan transactiedatum tijdens de gespecificeerde tijdspanne voorkwam. Dit geeft aan hoeveel inkomsten binnen de opgegeven periode zijn verdiend.</li><li><i> klik datum </i>: Om transacties te zien die uit een klik resulteerden die tijdens de gespecificeerde tijdspanne voorkwam. Wanneer een portfolio aanzienlijke vertraging heeft tussen klikken en transacties, is deze optie handig voor het berekenen van de historische opbrengst per klik voor de portfolio, die het inkomstengedrag aangeeft dat in de loop der tijd moet worden verwacht. |
