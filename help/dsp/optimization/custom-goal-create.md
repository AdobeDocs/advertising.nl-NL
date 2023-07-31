---
title: Een aangepast doel maken
description: Een aangepast doel maken
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Een aangepast doel maken

U kunt aangepaste doelen maken als *doelstellingen* binnen [!DNL Advertising Search, Social, & Commerce].

Als u een aangepast doel wilt maken, moet de DSP-account zijn gekoppeld aan een [!DNL Search, Social, & Commerce] account met dezelfde Adobe Experience Cloud-organisatie-id, van binnen de [!DNL Search, Social, & Commerce] clientinstellingen. Als uw DSP niet is gekoppeld aan een [!DNL Search, Social, & Commerce] account, neemt u contact op met uw Adobe-accountteam.

>[!TIP]
>
>Zie de [aanbevolen procedures voor het maken van aangepaste doelen](custom-goal-best-practices.md) voor uiteinden op hoe te om uw douanedoelstellingen te vormen.

1. Aanmelden [!DNL Advertising Search, Social, & Commerce] at (gebruikers in Noord-Amerika) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) of (alle andere gebruikers) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Zorg ervoor dat de meetgegevens die u in uw doel wilt opnemen, zijn bijgehouden, beschikbaar zijn in het product en een weergavenaam bevatten:
   1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.
   1. Bepaal de plaats van metrisch, en zorg ervoor dat **[!UICONTROL Show in UI and Reports]** wordt toegelaten voor metrisch.
   1. Als metrisch geen waarde in metrisch heeft **[!UICONTROL Display Name]** , klikt u in de cel, voert u de weergavenaam in en klikt u op **[!UICONTROL Apply].**
1. Het aangepaste doel maken als een *doel*:
   1. Klik in het hoofdmenu op **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL Objectives]**.
   1. Klik op de werkbalk op **[!UICONTROL Create objective].**
   1. Voer de objectieve instellingen in:
      1. In de **[!UICONTROL Change Objective Name]** voert u de objectieve naam in.

         De objectieve naam wordt weergegeven in het [!UICONTROL Custom Goals] in de instellingen van het DSP pakket.

      1. Eigenschappen koppelen aan het doel:

         >[!NOTE]
         >
         > Alle omzettingsmetriek die voor de adverteerder worden gevolgd worden vermeld door gebrek in [!UICONTROL Available Properties] lijst.

         * Als u een CSV-bestand wilt importeren met conversiewaarden en de bijbehorende gewichten, klikt u op **[!UICONTROL Import]** en zoek het bestand dat u wilt importeren.

           De geïmporteerde conversiemetriek moet al bestaan voor de adverteerder. De namen zijn niet hoofdlettergevoelig.

           De geïmporteerde conversiemetriek vervangt de bestaande opgegeven eigenschappen.

         * Als u handmatig de eerste omzettingsmetrische waarde met de standaarddikte (1) wilt opgeven, selecteert u een waarde in een lijst met alle conversiemetriek die voor de adverteerder wordt bijgehouden.

         * Als u handmatig nog een metrische omzetting wilt toevoegen met de standaarddikte (1), klikt u op **[!UICONTROL +]** .

           >[!TIP]
           >
           > Als u naar metrische waarden in de lijst wilt zoeken, voert u een tekenreeks in vanuit een willekeurige locatie binnen de naam van de metrische waarde.

         * Als u handmatig meerdere conversiemetriek wilt toevoegen, klikt u op **[!UICONTROL Add Multiple Properties].** Voor elke metrische omzetting u wilt toevoegen, klik de metrische naam in [!UICONTROL Available Properties] en sleep deze naar de [!UICONTROL Added Properties] kolom. Wanneer u klaar bent met het toevoegen van metriek, klik **[!UICONTROL Add]**.

           >[!TIP]
           >
           >* Als u naar metrische waarden in de lijst wilt zoeken, voert u in het invoerveld een tekenreeks in vanuit de naam van de metrische waarde.
           >* Als u de lijst wilt filteren om metriek uit te sluiten die zijn uitgesloten in rapporten, selecteert u de optie **[!UICONTROL Hide properties excluded from reports].**

         * (Als het doel meerdere omzettingsmaatstaven bevat) Als u het gewicht van een metrische waarde wilt wijzigen ten opzichte van de andere metriek in het doel, voert u waarden in in het dialoogvenster **[!UICONTROL Weight]** veld(en)

      1. Klik onder aan de instellingen op **[!UICONTROL Save]**.

Wanneer u een doel hebt gemaakt, kunt u het als aangepast doel toewijzen aan een DSP pakket wanneer het optimalisatiedoel &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; of &quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>Voor optimale prestaties, moeten de gecombineerde metriek in het douanedoel (doelstelling) minstens tien omzettingen per dag in totaal omvatten. Als dat niet het geval is, kunt u het beste aanvullende ondersteunende conversiemetriek, zoals productpagina&#39;s of het starten van de toepassing, aan het doel toevoegen. Zie [Beste praktijken voor het Bouwen van een Doel van de Douane](custom-goal-best-practices.md) voor richtsnoeren.

>[!MORELIKETHIS]
>
>* [Aangepaste doelen](custom-goal-about.md)
>* [Beste praktijken voor het Bouwen van een Doel van de Douane](custom-goal-best-practices.md)
>* [Optimalisatiedoelstellingen en hoe deze te gebruiken](optimization-goals.md)
>* [Pakketinstellingen](/help/dsp/campaign-management/packages/package-settings.md)
> * [Hoe DSP uw campagnes optimaliseert](optimization-how-dsp-optimizes-campaigns.md)
