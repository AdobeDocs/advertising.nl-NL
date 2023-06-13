---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---
# Pad 1 en Pad 2 weergeven in bepaalde advertentie-instellingen

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Optioneel) Tekst die aan de weergave-URL wordt toegevoegd en die automatisch wordt opgehaald uit de uiteindelijke URL. Elk pad wordt voorafgegaan door een slash (`/`). Een pad mag geen schuine streep (`/`) of een nieuwe regel (`\n`) tekens. De maximumlengte voor elk pad is 15 tekens of 7 double-byte tekens.

Als u een advertentieklanter wilt invoegen, gebruikt u de volgende indelingen, waarbij `Default text` is een optionele waarde die moet worden ingevoegd wanneer uw feed geen geldige waarde bevat:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Als [!UICONTROL Display Path 1] is &quot;deals&quot; en [!UICONTROL Display Path 2] is &quot;lokaal&quot;, wordt de URL van de weergave `<display URL>/deals/local`, zoals www.example.com/deals/local.
