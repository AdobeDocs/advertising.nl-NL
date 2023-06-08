---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# Pad 1 en Pad 2 weergeven in bepaalde advertentie-instellingen

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Optioneel) Tekst die aan de weergave-URL wordt toegevoegd en die automatisch wordt opgehaald uit de uiteindelijke URL. Elk pad wordt voorafgegaan door een slash (`/`). Een pad mag geen schuine streep (`/`) of een nieuwe regel (`\n`) tekens. De maximumlengte voor elk pad is 15 tekens of 7 double-byte tekens.

Als u een advertentieklanter wilt invoegen, gebruikt u de volgende indelingen, waarbij `Default text` is een optionele waarde die moet worden ingevoegd wanneer uw feed geen geldige waarde bevat:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Als bijvoorbeeld Pad 1 weergeven &quot;deals&quot; is en Pad 2 weergeven &quot;lokaal&quot;, is de URL van de weergave `<display URL>/deals/local`, zoals www.example.com/deals/local.
