# Création d'un rapport de rétrofacturation pour Azure Purview

Nous allons voir comment utiliser les informations d'Azure Log Analytics afin de créer un rapport permettant la retrofacturation d'utilisation des scans.

## Pre requis

- Un compte [Azure Purview](https://docs.microsoft.com/fr-fr/azure/purview/create-catalog-portal)
- Un espace de travail [Azure Log Analytics](https://docs.microsoft.com/fr-fr/azure/azure-monitor/logs/quick-create-workspace)
- [Power BI Desktop](https://www.microsoft.com/fr-fr/download/details.aspx?id=58494) 
- Optinonel : une licence Power BI Pro ou Premium


## Configuration d'Azure Purview

Dans un premier temps, nous allons configuer Azure Purview afin d'envoyer les informations de télémétries à Azure Log Analytics

Depuis le portail Azure, cherchez et sélectionnez votre compte Azure Purview
Cliquez sur **"Diagnostic settings"**, puis sur **"+ Add diagnostic setting"**

![sparkle](Pictures/001.png)

Dans la fenêtre "Diagnostic setting", dans la partie "Category details" cochez les cases :
- ScanStatusLogEvent
- AllMetrics

Puis dans la partie "Destination details" cochez la case **"Send to Log Analytics workspace"** et resneignez les information de votre espace de travail Azure Log analytics.

Cliquez sur le bouton **"Save"**

![sparkle](Pictures/002.png)

