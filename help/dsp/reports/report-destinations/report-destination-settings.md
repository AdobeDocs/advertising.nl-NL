---
title: Doelinstellingen rapporteren
description: Zie de details die voor uw rapportbestemmingen, door bestemmingstype worden vereist.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Doelinstellingen rapporteren

De details die voor niet-e-mailrapportbestemmingen worden vereist variëren door bestemmingstype.

>[!NOTE]
>
> U kunt uw douanerapporten aan e-mailontvangers ook leveren, die geen opgeslagen rapportbestemming vereisen. U kunt e-mailontvangers, in plaats van opgeslagen doelen, binnen de rapportinstellingen opgeven.

## [!UICONTROL S3]

**[!UICONTROL Name]:** Een naam om u te helpen de bestemming identificeren.

**[!UICONTROL S3 Bucket URL]:** De volledige weg aan de omslag op het [!DNL Amazon Simple Storage Service] (S3) emmertje aan wie het rapport wordt geupload. Voorbeeld: `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** Sleutelidentiteitskaart van de Toegang aan het ([!DNL Amazon S3]) emmer (die door [!DNL Amazon] wordt verstrekt).

**[!UICONTROL Secret Access Key]:** De Geheime Sleutel van de Toegang tot het ([!DNL Amazon S3]) emmertje (die door [!DNL Amazon] wordt verstrekt).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** Een naam om u te helpen de bestemming identificeren.

**[!UICONTROL Server]:** De hostnaam voor de server.

**[!UICONTROL Port]:** Het poortnummer dat op de server moet worden gebruikt. De standaardwaarde is *[!UICONTROL 21]* .

**[!UICONTROL Username]:** De gebruikersnaam om u aan te melden bij de server.

**[!UICONTROL Password]:** Het wachtwoord om u aan te melden bij de server.

**[!UICONTROL Path (Optional)]:** De serverweg waaraan de dossiers worden geupload.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** Een naam om u te helpen de bestemming identificeren.

**[!UICONTROL Server]:** De hostnaam voor de server.

**[!UICONTROL Port]:** Het poortnummer dat op de server moet worden gebruikt. De standaardwaarde is *[!UICONTROL 21]* .

**[!UICONTROL Username]:** De gebruikersnaam om u aan te melden bij de server.

**[!UICONTROL Password]:** Het wachtwoord om u aan te melden bij de server.

**[!UICONTROL Path (Optional)]:** De serverweg waaraan de dossiers worden geupload.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** Een naam om u te helpen de bestemming identificeren.

**[!UICONTROL Server]:** De hostnaam voor de server.

**[!UICONTROL Port]:** Het poortnummer dat op de server moet worden gebruikt. De standaardwaarde is *[!UICONTROL 21]* .

**[!UICONTROL Username]:** De gebruikersnaam om u aan te melden bij de server.

**[!UICONTROL Password]:** Het wachtwoord om u aan te melden bij de server.

**[!UICONTROL Path (Optional)]:** De serverweg waaraan de dossiers worden geupload.

>[!MORELIKETHIS]
>
>* [ Over [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [ Maak een [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [ Bewerk a [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [ Verwijderen a [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)
