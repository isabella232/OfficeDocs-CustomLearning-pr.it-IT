---
title: Microsoft 365 domande frequenti sui percorsi di apprendimento
author: karuanag
ms.author: karuanag
manager: alexb
ms.date: 02/10/2019
description: Informazioni sulle domande frequenti per i Microsoft 365 di apprendimento
ms.service: sharepoint-online
ms.topic: article
ms.openlocfilehash: 82a7e777490e13fde6fef5add40beee417050027
ms.sourcegitcommit: d05381fc4a58cf2949773d73877bacc5ef3a7ca6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/01/2021
ms.locfileid: "60048723"
---
# <a name="frequently-asked-questions"></a>Domande frequenti

## <a name="what-are-the-requirements-for-installing-microsoft-365-learning-pathways-into-my-tenant-environment"></a>Quali sono i requisiti per l'installazione Microsoft 365 percorsi di apprendimento nell'ambiente tenant?

- SharePoint Online e i siti di comunicazione sono abilitati.
- La persona che dovrà eseguire il provisioning Microsoft 365 percorsi di apprendimento deve essere l'amministratore tenant del tenant di destinazione per l'installazione.
- Un tenant 'Catalogo app' deve essere disponibile nell'opzione "App" dell'interfaccia SharePoint admin center.
- Se viene creato un nuovo Catalogo app, è necessario un tempo di attesa di 30 minuti o più per il provisioning completo del Catalogo app. Se si tenta di effettuare Microsoft 365 percorsi di apprendimento direttamente dopo aver creato il Catalogo app tenant, si verifica un errore di provisioning della soluzione dei percorsi di apprendimento.
- La persona che dovrà eseguire il provisioning Microsoft 365 percorsi di apprendimento deve essere un amministratore della raccolta siti del catalogo app nel tenant di destinazione per l'installazione.

## <a name="why-is-microsoft-asking-for-tenant-permissions-when-installing-microsoft-365-learning-pathways"></a>Perché Microsoft richiede autorizzazioni tenant durante l'installazione Microsoft 365 percorsi di apprendimento?

Il servizio di provisioning online di SharePoint usa le autorizzazioni per effettuare il provisioning del sito SharePoint dei percorsi di Learning, creare le pagine del sito e installare l'applicazione dei percorsi di apprendimento di Microsoft 365 all'interno del tenant. Questo è l'unico motivo per cui richiediamo le autorizzazioni. Senza le autorizzazioni richieste, SharePoint il servizio di provisioning non può eseguire i comandi che installano automaticamente il modello di sito e la web part percorsi di apprendimento.
![Screenshot della richiesta di autorizzazioni](media/faqs-permissions-request-screenshot.png "Richiesta di autorizzazioni") Se si hanno ancora dubbi su questo livello di accesso, è possibile concedere le autorizzazioni e distribuire i modelli di sito a cui si è interessati e quindi rimuovere immediatamente le autorizzazioni concesse per l'app nell'app store di [Azure.](https://myapps.microsoft.com)

## <a name="how-long-will-it-take-to-install-the-site-in-our-tenant-environment"></a>Quanto tempo è necessario per installare il sito nell'ambiente tenant?

L'applicazione richiede meno di 15 minuti. Questa operazione non include il tempo necessario per personalizzare il sito in base alle proprie esigenze.

## <a name="is-microsoft-365-learning-pathways-an-open-source-solution-and-what-are-the-implications"></a>I Microsoft 365 di apprendimento sono una soluzione open source e quali sono le implicazioni?

Microsoft 365 percorsi di apprendimento è una soluzione di software open source (OSS) e, di conseguenza, offre una serie di vantaggi e considerazioni all'OSS:

### <a name="benefits"></a>Vantaggi 

- **Microsoft 365 percorsi di apprendimento è una soluzione gratuita:** I clienti possono installare la soluzione nel tenant, personalizzarla e renderla disponibile per gli utenti finali.
- **OSS consente uno sviluppo e una collaborazione rapidi:** Tutte le soluzioni open source sono disponibili per un'ampia community di collaboratori. Microsoft si impegna a utilizzare questo metodo per guidare l'innovazione. Per garantire un'esperienza a vantaggio del più ampio set di clienti, il team di gestione dei servizi di base si riserva il diritto di determinare quali contributi vengono uniti nella build ufficiale.  
- **OSS consente la collaborazione con i partner:** Microsoft sta collaborando con diversi partner di apprendimento per supportare i propri sforzi per le estensioni future e i contributi Microsoft 365 percorsi di apprendimento. Verranno fornite ulteriori informazioni man appena questi piani verranno finalizzati.

### <a name="implications"></a>Implicazioni

- **OSS non è un prodotto disponibile in commercio:** I prodotti commerciali includono l'aggiornamento e l'applicazione di patch e sono inclusi nei contratti di supporto a pagamento. Mentre Microsoft attualmente offre documentazione, aggiornamento e applicazione di patch per Microsoft 365 percorsi di apprendimento, si basa sul nostro impegno a migliorare questo scenario aziendale specifico. Sebbene i nostri piani continuino a investire nei percorsi di apprendimento, tenere presente che il team di gestione dei servizi potrebbe cambiare le strategie in futuro. Eventuali modifiche future ai Microsoft 365 di apprendimento verranno comunicate prima di essere applicate.
- **Come OSS, i Microsoft 365** di apprendimento sono supportati tramite un elenco di problemi online in GitHub : i percorsi di apprendimento Microsoft 365 non sono coperti da alcun contratto di supporto Microsoft esistente. I problemi inviati vengono valutati dai proprietari dei Microsoft 365 di apprendimento e dalla community. I livelli di servizio per la risoluzione dei problemi NON sono allo stesso livello di un contratto di supporto Microsoft a pagamento.  

### <a name="can-we-make-the-microsoft-365-learning-pathways-a-sub-site-of-our-primary-sharepoint-site-collection"></a>È possibile rendere i percorsi Microsoft 365 di apprendimento secondario della raccolta siti SharePoint principale?

No. Il sito si basa su un modello di sito di comunicazione, che deve sempre essere una raccolta siti radice.

> [!NOTE]
> È importante considerare le autorizzazioni necessarie agli utenti finali per accedere al sito. La maggior parte delle organizzazioni dispone di gruppi di utenti o di sicurezza definiti. È necessario aggiungere i gruppi di sicurezza appropriati al nuovo portale di formazione quando si è pronti per avviarlo nella community dei dipendenti.

### <a name="i-need-to-reinstall-the-site-what-should-i-do"></a>È necessario reinstallare il sito. Cosa dovrei fare?

Seguire le istruzioni di installazione pubblicate [qui.](custom_provision.md)

> [!NOTE]
> Se la telemetria è stata disabilitata nell'installazione precedente e si desidera continuare con la telemetria disabilitata, è necessario seguire le istruzioni per disabilitare la [telemetria qui](https://github.com/pnp/custom-learning-office-365/blob/a7168c97a76e0b4122e3ddfc530f6a10c724c3e1/installation/README.md).

### <a name="we-made-updates-to-our-implementation-of-microsoft-365-learning-pathways-will-we-lose-these-updates-made-to-site-template-playlists-if-we-reinstall-the-site"></a>Abbiamo apportato aggiornamenti all'implementazione dei Microsoft 365 di apprendimento. Questi aggiornamenti (apportati a modelli di sito, playlist) andranno persi se si reinstalla il sito?

Le personalizzazioni per singole pagine e playlist personalizzate andranno perse se si reinstalla il sito nell'installazione corrente.  
