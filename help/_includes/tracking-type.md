---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# Het veld Type bijhouden in de account- en campagne-instellingen

**[!UICONTROL Tracking Type]:** De methode waarmee URL&#39;s worden gegenereerd:

* *[!UICONTROL EF Redirect]* (de standaardinstelling): Voor klanten die de service voor het bijhouden van Adobe-advertenties willen gebruiken. Deze methode genereert unieke id&#39;s voor het bijhouden van klikken en leidt gebruikers om naar de advertentieserver van Adobe voor traceringsdoeleinden voordat ze naar de landingspagina van de client worden verzonden.

   Deze methode heeft standaardopties voor bijhouden die u naar keuze kunt aanpassen en u kunt ook parameters opgeven die aan elke URL moeten worden toegevoegd.

* *[!UICONTROL No EF Redirect]:* Voor klanten die alleen hun eigen code voor het bijhouden van klikken willen gebruiken. Zoeken, Sociaal en Handel biedt geen id&#39;s voor het bijhouden van klikken of codes voor omleiding. Voor accounts met doel-URL&#39;s is elke doel-URL gelijk aan de basis-URL.

   **Opmerkingen:**

   * Deze waarde kan alleen worden gewijzigd door de accountmanager van het Adobe-bureau, de accountmanager en de beheerder.
   * Als u de methode voor bijhouden wijzigt, moet u de URL&#39;s voor het bijhouden van een account opnieuw genereren.
   * De opties voor bijhouden op campagnereniveau hebben voorrang op instellingen op accountniveau.
