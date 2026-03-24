---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---
# Veld automatisch uploaden in account- en campagne-instellingen

**[!UICONTROL Auto Upload]:** (Voor gesynchroniseerde campagnes met [!UICONTROL EF Redirect] slechts) uploadt automatisch het volgende aan het advertentienetwerk de volgende tijd Onderzoek, Sociale, &amp; Commerce synchroniseert met het: a) Onderzoek, Sociale, &amp; Commerce het volgen parameters voor het volgen van malplaatjes en de zelfde parameters toevoegden aan definitieve URLs of b) nieuwe bestemmings URLs ingebed met het het volgen van Onderzoek, Sociale, &amp; Commerce code. Voor adverteerders met een [&#x200B; Adobe Advertising-Adobe Analytics integratie &#x200B;](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) en een server-kantAMO identiteitskaart (s_kwcid) configuratie, omvat de upload ook [&#x200B; parameters van identiteitskaart van AMO &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id) voor uw [!DNL Google Ads] en [!DNL Microsoft Advertising] rekeningen. De standaardinstelling op accountniveau wordt overgenomen van de instellingen voor bijhouden van adverteerders. U kunt de instelling op accountniveau op campagneniveau overschrijven.

**Nota:** het Volgen URLs wordt dagelijks bijgewerkt slechts voor entiteiten die uit synchronisatie (namelijk nieuwe entiteiten zijn die werden toegevoegd en bestaande entiteiten waarvan eigenschappen zijn veranderd). Als u deze instelling wijzigt van uitgeschakeld in ingeschakeld voor een bestaande adverteerder/account/campagne, worden URL&#39;s die worden bijgehouden niet bijgewerkt voor bestaande entiteiten die al gesynchroniseerd zijn. Als u de URL&#39;s van bestaande, synchrone entiteiten wilt bijhouden, neemt u contact op met uw Adobe-accountteam en vraagt u een eenmalig, handmatig synchronisatieproces. Het automatische uploadproces zal toekomstige veranderingen behandelen.
