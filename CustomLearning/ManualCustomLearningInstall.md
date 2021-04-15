---
author: pkrebs
ms.author: pkrebs
title: Percorsi di apprendimento per l'installazione manuale
ms.date: 02/18/2019
manager: bpardi
description: Percorsi di apprendimento per l'installazione manuale
audience: itpro
ms.service: o365-administration
ms.topic: article
ms.openlocfilehash: 212ee8a1517cf79538d4a2d076f60f9382eeaf74
ms.sourcegitcommit: 96ad347dc08694ce2af5a5d42bf1f753d1c30a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "51749314"
---
# <a name="manually-installing-and-configuring-custom-learning-for-office-365"></a>Installazione e configurazione manuale di Apprendimento personalizzato per Office 365

La web part Microsoft Custom Learning viene compilata utilizzando [SharePoint Framework](/sharepoint/dev/spfx/sharepoint-framework-overview) versione 1.7.1.

Per installare e configurare manualmente la web part e la raccolta siti, è necessario completare i passaggi seguenti:

1. Verificare di aver soddisfatto tutti i prerequisiti.
1. Installare il file customlearning.sppkg nel Catalogo app tenant di Office 365.
1. Effettuare il provisioning/identificare un sito di comunicazione moderno che agirà come sito principale di Apprendimento personalizzato per Office 365.
1. Eseguire uno script di PowerShell che configurerà il tenant con gli elementi appropriati da cui dipende Apprendimento personalizzato.
1. Passare alla pagina del sito CustomLearningAdmin.aspx per caricare la web part di amministrazione per inizializzare la configurazione del contenuto personalizzata.

## <a name="prerequisites"></a>Prerequisiti

È necessario aver configurato e configurato il Catalogo app a livello di tenant. Vedere [Configurare il tenant di Office 365](/sharepoint/dev/spfx/set-up-your-developer-tenant#create-app-catalog-site) e seguire la sezione Creare il sito catalogo app. Se il provisioning del Catalogo app a livello di tenant è già stato eseguito, sarà necessario accedere a un account che dispone dei diritti per caricare un pacchetto per completare il processo di installazione. In genere questo account ha il ruolo di amministratore di SharePoint. Se un account con tale ruolo non funziona, passare all'interfaccia di amministrazione di SharePoint e individuare Gli amministratori raccolta siti per la raccolta siti del catalogo app e accedere come uno degli amministratori della raccolta siti oppure aggiungere l'account amministratore di SharePoint che non è riuscito ad amministratori della raccolta siti. Sarà inoltre necessario accedere a un account che sia un amministratore tenant di SharePoint.

## <a name="upload-the-web-part-to-the-tenant-app-catalog"></a>Caricare la web part nel Catalogo app tenant

Per configurare l'apprendimento personalizzato per Office 365, caricare il file customlearning.sppkg nel Catalogo app a livello di tenant e distribuirlo. Per istruzioni dettagliate su come aggiungere un'app al catalogo app, vedere Use [the App Catalog to make custom business apps available for your SharePoint Online](/sharepoint/use-app-catalog) environment.

## <a name="provisionidentify-modern-communication-site"></a>Provisioning/identificazione del sito di comunicazione moderna

Identificare un sito di comunicazione di SharePoint esistente o eseguirne il provisioning nel tenant di SharePoint Online. Per ulteriori informazioni su come eseguire il provisioning di un sito di comunicazione, vedere [Create a communication site in SharePoint Online](https://support.office.com/article/create-a-communication-site-in-sharepoint-online-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb) e seguire la procedura per creare un sito di comunicazione.

## <a name="set-permissions-for-the-site"></a>Impostare le autorizzazioni per il sito

È consigliabile aggiungere tutti gli utenti che dovrebbero essere in grado di visualizzare il contenuto al gruppo Visitatori e tutti coloro che dovrebbero essere in grado di amministrare playlist personalizzate al gruppo Membri. Per configurare il sito per l'apprendimento personalizzato la prima volta che l'utente deve essere un amministratore della raccolta siti o parte del gruppo Proprietari.

Aggiungere apprendimento personalizzato per Office 365 App alla raccolta siti.

## <a name="execute-powershell-configuration-script"></a>Eseguire lo script di configurazione di PowerShell

È incluso uno script di PowerShell che sarà necessario eseguire per creare tre proprietà `CustomLearningConfiguration.ps1` [tenant](/sharepoint/dev/spfx/tenant-properties) utilizzate dalla soluzione. Inoltre, lo script crea due pagine dell'app a [parte singola](/sharepoint/dev/spfx/web-parts/single-part-app-pages) nella raccolta pagine del sito per ospitare le web part amministratore e utente in un percorso noto.

### <a name="disabling-telemetry-collection"></a>Disabilitazione della raccolta di telemetria

Parte di questa soluzione include il consenso esplicito per il rilevamento della telemetria anonimizzato, che per impostazione predefinita è impostato su on. Se si esegue un'installazione manuale e si desidera disattivare il rilevamento della telemetria, modificare lo script per impostare la variabile $optInTelemetry su `CustomlearningConfiguration.ps1` $false.

Se non si esegue un'installazione manuale e si desidera disattivare il rilevamento della telemetria, è stato incluso uno script separato che, quando eseguito, `TelemetryOptOut.ps1` disabiliterà il rilevamento della telemetria.

## <a name="initialize-web-part-custom-configuration"></a>Inizializzare la configurazione personalizzata della web part

Dopo aver eseguito correttamente lo script di PowerShell, passare a `<YOUR-SITE-COLLECTION-URL>/SitePages/CustomLearningAdmin.aspx` . In questo modo viene inizializzata la voce di elenco CustomConfig che configura l'apprendimento personalizzato per il primo utilizzo.

La configurazione è ora completa ed è possibile procedere con l'uso di Apprendimento personalizzato per Office 365. Per ulteriori informazioni, vedere la documentazione dell'utente.
