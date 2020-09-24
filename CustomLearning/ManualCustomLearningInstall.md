---
author: pkrebs
ms.author: pkrebs
title: Percorsi di apprendimento per l'installazione manuale
ms.date: 02/18/2019
description: Percorsi di apprendimento per l'installazione manuale
ms.service: sharepoint online
ms.openlocfilehash: a9ae97bbafcc82c54251cae9a0ad658b7a0c16f4
ms.sourcegitcommit: ee4aebf60893887ae95a1294a9ad8975539ea762
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/23/2020
ms.locfileid: "48234668"
---
# <a name="manually-installing-and-configuring-custom-learning-for-office-365"></a>Installare e configurare manualmente l'apprendimento personalizzato per Office 365

La Web part Microsoft Learning personalizzata viene creata utilizzando la versione di [SharePoint Framework](https://docs.microsoft.com/sharepoint/dev/spfx/sharepoint-framework-overview) 1.7.1.

Per installare e configurare manualmente la Web part e la raccolta siti, è necessario eseguire i passaggi seguenti:

1. Verificare che siano stati soddisfatti tutti i prerequisiti.
1. Installare il file customlearning. sppkg nel catalogo delle app tenant di Office 365.
1. Provisioning/identificare un sito di comunicazione moderno che funga da apprendimento personalizzato per il sito Home di Office 365.
1. Eseguire uno script di PowerShell che configurerà il tenant con gli elementi adatti a cui dipende l'apprendimento personalizzato.
1. Passare alla pagina del sito CustomLearningAdmin. aspx per caricare la Web part amministratore per inizializzare la configurazione del contenuto personalizzato.

## <a name="prerequisites"></a>Prerequisiti

È necessario configurare e configurare il catalogo app a livello di tenant. Per ulteriori informazioni, vedere [configurare il tenant di Office 365](https://docs.microsoft.com/sharepoint/dev/spfx/set-up-your-developer-tenant#create-app-catalog-site) e seguire la sezione creare il sito di catalogo app. Se è già stato effettuato il provisioning del catalogo delle app a livello di tenant, è necessario accedere a un account che disponga dei diritti di caricamento di un pacchetto per completare il processo di installazione. Si tratta in genere di un account con il ruolo di amministratore di SharePoint. Se un account con quel ruolo non funziona, passare all'interfaccia di amministrazione di SharePoint e individuare gli amministratori della raccolta siti per la raccolta siti del catalogo app e accedere come amministratori della raccolta siti oppure aggiungere l'account di amministratore di SharePoint che non è riuscito agli amministratori della raccolta siti. Sarà inoltre necessario l'accesso a un account che sia un amministratore tenant di SharePoint.

## <a name="upload-the-web-part-to-the-tenant-app-catalog"></a>Caricare la Web part nel catalogo app tenant

Per configurare l'apprendimento personalizzato per Office 365, caricare il file customlearning. sppkg nel catalogo app a livello di tenant e distribuirlo. Per informazioni dettagliate su come aggiungere un'app al catalogo app, vedere [utilizzare il catalogo app per rendere disponibili le app aziendali personalizzate per l'ambiente di SharePoint Online](https://docs.microsoft.com/sharepoint/use-app-catalog) .

## <a name="provisionidentify-modern-communication-site"></a>Provisioning/identificare il sito di comunicazione moderno

Identificare un sito di comunicazione di SharePoint esistente o provisionare uno nuovo nel tenant di SharePoint Online. Per ulteriori informazioni su come eseguire il provisioning di un sito di comunicazione, vedere [creare un sito di comunicazione in SharePoint Online](https://support.office.com/article/create-a-communication-site-in-sharepoint-online-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb) e seguire la procedura per creare un sito di comunicazione.

## <a name="set-permissions-for-the-site"></a>Impostare le autorizzazioni per il sito

Si desidera aggiungere tutti gli utenti che devono essere in grado di visualizzare il contenuto nel gruppo visitatori e tutti gli utenti che devono essere in grado di amministrare playlist personalizzate al gruppo membri. Per configurare il sito per l'apprendimento personalizzato, la prima volta che l'utente deve essere un amministratore della raccolta siti o una parte del gruppo proprietari.

Aggiungere l'app di apprendimento personalizzato per Office 365 alla raccolta siti.

## <a name="execute-powershell-configuration-script"></a>Eseguire lo script di configurazione di PowerShell

È incluso uno script di PowerShell `CustomLearningConfiguration.ps1` che sarà necessario eseguire per creare tre [Proprietà tenant](https://docs.microsoft.com/sharepoint/dev/spfx/tenant-properties) utilizzate dalla soluzione. Lo script consente inoltre di creare due pagine dell'applicazione di una [singola parte](https://docs.microsoft.com/sharepoint/dev/spfx/web-parts/single-part-app-pages) nella raccolta pagine del sito per ospitare l'amministratore e le web part dell'utente in una posizione nota.

### <a name="disabling-telemetry-collection"></a>Disabilitazione della raccolta di telemetria

Parte di questa soluzione include la verifica della telemetria di anonimi opt-in, che per impostazione predefinita è impostata su attivato. Se si sta eseguendo un'installazione manuale e si desidera disattivare la verifica della telemetria, modificare lo `CustomlearningConfiguration.ps1` script per impostare la variabile $optInTelemetry su $false.

Se non si esegue un'installazione manuale e si desidera disattivare la verifica della telemetria, `TelemetryOptOut.ps1` è stato incluso uno script separato che, quando l'esecuzione disattiverà la traccia di telemetria.

## <a name="initialize-web-part-custom-configuration"></a>Inizializzare la configurazione personalizzata della web part

Dopo che lo script di PowerShell è stato eseguito correttamente, accedere a `<YOUR-SITE-COLLECTION-URL>/SitePages/CustomLearningAdmin.aspx` . Questo consente di inizializzare l'elemento di elenco CustomConfig che configura l'apprendimento personalizzato per il primo utilizzo.

La configurazione è ora completata ed è possibile procedere con l'utilizzo di apprendimento personalizzato per Office 365. Per ulteriori informazioni, vedere la documentazione relativa all'utente.