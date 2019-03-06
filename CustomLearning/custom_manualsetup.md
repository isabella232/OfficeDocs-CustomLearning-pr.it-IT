---
author: pkrebs
ms.author: pkrebs
title: Configurazione della web part autonoma
ms.date: 02/10/2019
description: Installazione di Web part manuale per l'apprendimento personalizzato per Office 365
ms.openlocfilehash: 650e6c12ebe8ca7fedc6edc107b5822c48ead99a
ms.sourcegitcommit: b6617bbbaee0784d6216e96052c2469f97cf51e9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2019
ms.locfileid: "30411876"
---
# <a name="stand-alone-web-part-setup"></a>Configurazione della web part autonoma

L'apprendimento personalizzato offre una configurazione di Web part autonoma e manuale per le organizzazioni che dispongono già di un sito di comunicazione moderno di SharePoint Online definito dedicato all'allenamento o che desiderano solo configurare la Web part di apprendimento personalizzata in modo autonomo. sito di comunicazione. Si noti che la configurazione manuale richiede un'esperienza di utilizzo di Windows PowerShell e di SharePoint Online Management Shell. I passaggi per una configurazione manuale della web part di apprendimento personalizzata come indicato di seguito:

- Verificare che siano stati soddisfatti tutti i prerequisiti.
- Installare il file customlearning. sppkg nel catalogo delle app tenant di Office 365.
- ProVisioning/identificare un sito di comunicazione moderno che funga da apprendimento personalizzato per il sito Home di Office 365.
- Eseguire uno script di PowerShell che configurerà il tenant con gli elementi adatti a cui dipende l'apprendimento personalizzato.
- Passare alla pagina del sito CustomLearningAdmin. aspx per caricare la Web part amministratore per inizializzare la configurazione del contenuto personalizzato.

> [!NOTE]
> Se si sta cercando un modo semplice e veloce per configurare l'apprendimento personalizzato, vedere [provision Custom Learning](installsitepackage.md).

## <a name="prerequisites"></a>Prerequisiti
Per garantire la corretta configurazione manuale della web part di apprendimento personalizzato, è necessario che vengano soddisfatti i prerequisiti seguenti. 

- È necessario configurare e configurare il catalogo app a livello di tenant. Per ulteriori informazioni, vedere [configurare il tenant di Office 365](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/set-up-your-developer-tenant#create-app-catalog-site) e seguire la sezione creare il sito di catalogo app. 
- Se è già stato effettuato il provisioning del catalogo delle app a livello di tenant, è necessario accedere a un account che disponga dei diritti di caricamento di un pacchetto per completare il processo di installazione. Si tratta in genere di un account con il ruolo di amministratore di SharePoint. 
- Se un account con quel ruolo non funziona, passare all'interfaccia di amministrazione di SharePoint e individuare gli amministratori della raccolta siti per la raccolta siti Catalogo app e accedere come uno degli amministratori della raccolta siti oppure aggiungere l'account amministratore di SharePoint. che non sono riusciti agli amministratori della raccolta siti. 
- Sarà inoltre necessario l'accesso a un account che sia un amministratore tenant di SharePoint.

## <a name="step-1---get-the-web-part-package-and-setup-script-from-github"></a>Passaggio 1-ottenere il pacchetto Web part e lo script di installazione da GitHub
Come parte del processo di installazione, è necessario il pacchetto Web part di apprendimento personalizzato e lo script di installazione di PowerShell.

- Andare al [repository di apprendimento GitHub personalizzato](https://github.com/pnp/custom-learning-office-365).
- Fare clic su **download** per salvare il pacchetto della web part e lo script su un'unità locale. Si utilizzerà lo script e il pacchetto Web part nei passaggi successivi di questo processo.

## <a name="step-2---upload-the-web-part-to-the-tenant-app-catalog"></a>Passaggio 2: caricare la Web part nel catalogo app tenant
Per configurare l'apprendimento personalizzato per Office 365, caricare il file customlearning. sppkg nel catalogo app a livello di tenant e distribuirlo. Per informazioni dettagliate su come aggiungere un'app al catalogo app, vedere [utilizzare il catalogo app per rendere disponibili le app aziendali personalizzate per l'ambiente di SharePoint Online](https://docs.microsoft.com/en-us/sharepoint/use-app-catalog) .

## <a name="step-3---provisionidentify-a-modern-communication-site"></a>Passaggio 3-proVisioning/identificare un sito di comunicazione moderno
Identificare un sito di comunicazione di SharePoint esistente o provisionare uno nuovo nel tenant di SharePoint Online. Per ulteriori informazioni su come eseguire il provisioning di un sito di comunicazione, vedere [creare un sito di comunicazione in SharePoint Online](https://support.office.com/en-us/article/create-a-communication-site-in-sharepoint-online-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb) e seguire la procedura per creare un sito di comunicazione.

## <a name="step-4---set-permissions-for-the-site"></a>Passaggio 4: impostare le autorizzazioni per il sito
Verificare che siano impostate le autorizzazioni seguenti per il sito:
- **Amministratore della raccolta siti o parte del gruppo proprietari** -autorizzazioni necessarie per inizializzare l'elemento dell'elenco di CustomConfig che configura l'apprendimento personalizzato per il primo utilizzo. 
- **Gruppo membri** -permissons necessario per amministraRe l'apprendimento personalizzato, incluso l'occultamento e la visualizzazione di contenuto e l'amministrazione di elenchi di riproduzione personalizzati
- **Gruppo visitatori** -autorizzazioni necessarie per visualizzare il contenuto del sito. 

## <a name="step-5--execute-powershell-configuration-script"></a>Passaggio 5-esecuzione dello script di configurazione di PowerShell
È incluso uno `CustomLearningConfiguration.ps1` script di PowerShell che sarà necessario eseguire per creare tre [Proprietà tenant](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/tenant-properties) utilizzate dalla soluzione. Lo script consente inoltre di creare due pagine dell'applicazione di una [singola parte](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/web-parts/single-part-app-pages) nella raccolta pagine del sito per ospitare l'amministratore e le web part dell'utente in una posizione nota.

### <a name="disabling-telemetry-collection"></a>Disabilitazione della raccolta di telemetria
Parte di questa soluzione include la verifica della telemetria di anonimi opt-in, che per impostazione predefinita è impostata su attivato. Se si sta eseguendo un'installazione manuale e si desidera disattivare la verifica della telemetria, modificare lo `CustomlearningConfiguration.ps1` script per impostare la variabile $optInTelemetry su $false.

Se non si esegue un'installazione manuale e si desidera disattivare la verifica della telemetria, è stato incluso `TelemetryOptOut.ps1` uno script separato che, quando l'esecuzione disattiverà la traccia di telemetria.

## <a name="step-6---initialize-web-part-custom-configuration"></a>Passaggio 6-inizializzare la configurazione personalizzata della web part
Dopo che lo script di PowerShell è stato eseguito correttamente `<YOUR-SITE-COLLECTION-URL>/SitePages/CustomLearningAdmin.aspx`, accedere a. Questo consente di inizializzare l'elemento di elenco **CustomConfig** che configura l'apprendimento personalizzato per il primo utilizzo.

La configurazione è ora completata. Per ulteriori informazioni su come personalizzare il sito di apprendimento personalizzato e la Web part per l'ambiente in uso, vedere [Customize the Training Experience](custom_overview.md).

### <a name="next-steps"></a>Operazioni successive
- [Personalizzare](custom_overview.md) l'esperienza di formazione per l'organizzazione.

