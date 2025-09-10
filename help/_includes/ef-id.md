---
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---
# Adobe Advertising EF-id&#39;s

De EF-id is een unieke token die Adobe Advertising gebruikt om activiteit te koppelen aan een online klik of belichting op het niveau van de afzonderlijke browser of het apparaat. EF-id&#39;s fungeren voornamelijk als sleutels voor het verzenden van [!DNL Analytics] -gegevens en Customer Journey Analytics-gegevens naar Adobe Advertising voor het melden en optimaliseren van biedingen binnen Adobe Advertising.

Voor [!DNL Analytics], wordt EF identiteitskaart opgeslagen in [ an  [!DNL Analytics] [!DNL eVar] ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) of [!DNL rVar] (gereserveerde [!DNL eVar]) dimensie (Adobe Advertising EF identiteitskaart).

Voor Customer Journey Analytics wordt de EF-id opgeslagen in de eigenschap `trackingIdentities` van het `conversionDetails` -object, dat deel uitmaakt van de [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] -eigenschap.
