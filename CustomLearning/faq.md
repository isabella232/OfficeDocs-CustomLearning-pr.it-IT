---
title: Microsoft 365 domande frequenti sui percorsi di apprendimento
author: karuanag
ms.author: karuanag
manager: alexb
ms.date: 02/10/2019
description: Informazioni sulle domande frequenti per i Microsoft 365 di apprendimento
ms.service: sharepoint-online
ms.topic: article
ms.openlocfilehash: f24f16455ba41724d300d038a01dc04c2170dc4a
ms.sourcegitcommit: 33acfc2149de89e8375b064b2223cae505d2a102
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2021
ms.locfileid: "52575921"
---
# <a name="frequently-asked-questions"></a>Domande frequenti

### <a name="i-recently-saw-a-blog-post-that-custom-learning-for-office-365-is-being-renamed-to-microsoft-365-learning-pathways-are-there-other-changes-being-added-to-the-solution-as-part-of-the-renaming-effort-should-i-update-the-solution-in-my-organization"></a>Di recente ho visto un post di blog che l'apprendimento personalizzato per Office 365 viene rinominato Microsoft 365 percorsi di apprendimento. Sono state aggiunte altre modifiche alla soluzione nell'ambito dell'operazione di ridenominazione? È consigliabile aggiornare la soluzione nell'organizzazione?

Il Microsoft 365 dei percorsi di apprendimento è uno sforzo di rebranding dedicato alla modifica del nome della soluzione per allinearsi con Microsoft 365 personalizzazione. Se l'apprendimento personalizzato per Office 365 è attualmente in esecuzione correttamente nell'organizzazione, non è necessario aggiornare la soluzione in questo momento.  

### <a name="what-are-the-requirements-for-installing-microsoft-365-learning-pathways-into-my-tenant-environment"></a>Quali sono i requisiti per l'installazione Microsoft 365 percorsi di apprendimento nell'ambiente tenant?

- SharePoint Online e i siti di comunicazione sono abilitati.
- L'utente che dovrà eseguire il provisioning di CLO365 deve essere l'amministratore tenant del tenant di destinazione per l'installazione.
- Un tenant 'Catalogo app' deve essere disponibile nell'opzione "App" dell'interfaccia SharePoint admin center.
- Se viene creato un nuovo Catalogo app, è necessario un tempo di attesa di 30 minuti o più per il provisioning completo del Catalogo app. Se si tenta di effettuare Microsoft 365 percorsi di apprendimento direttamente dopo aver creato il Catalogo app tenant, si verifica un errore di provisioning della soluzione dei percorsi di apprendimento. 
- La persona che dovrà eseguire il provisioning di CLO365 deve essere un amministratore della raccolta siti del catalogo app nel tenant di destinazione per l'installazione.

### <a name="why-is-microsoft-asking-for-tenant-permissions-when-installing-microsoft-365-learning-pathways"></a>Perché Microsoft richiede autorizzazioni tenant durante l'installazione Microsoft 365 percorsi di apprendimento 

- Il servizio SharePoint Online Provisioning usa le autorizzazioni per eseguire il provisioning del sito di SharePoint Percorsi di apprendimento, creare le pagine del sito e installare l'applicazione dei percorsi di apprendimento Microsoft 365 all'interno del tenant. Questo è l'unico motivo per cui richiediamo le autorizzazioni. Senza le autorizzazioni richieste, SharePoint servizio di provisioning non può eseguire i comandi che installano automaticamente il modello di sito e la web part percorsi di apprendimento. 

### <a name="what-are-the-implications-of-microsoft-365-learning-pathways-being-in-a-beta-preview"></a>Quali sono le implicazioni di Microsoft 365 percorsi di apprendimento in un'anteprima beta? 

Microsoft 365 percorsi di apprendimento è attualmente in Anteprima beta. Durante la valutazione, la pianificazione e l'implementazione dei percorsi di apprendimento Microsoft 365 seguenti:

- Come per qualsiasi soluzione Beta, il team di gestione dei servizi si riserva il diritto di apportare modifiche al servizio e ai relativi componenti. Poiché si stanno risolvendo attivamente bug e problemi relativi all'esperienza utente, è probabile che sia necessario aggiornare WebPart.
- Per aggiornare la web part, è necessario scaricarla dal repository GitHub e caricarla nel catalogo app tenant. Vedere la sezione "Aggiornamento della soluzione" del [file](https://github.com/pnp/custom-learning-office-365/blob/master/README.md) Readme Microsoft 365 percorsi di apprendimento. 

### <a name="what-languages-is-microsoft-365-learning-pathways-available-in"></a>In quali lingue Microsoft 365 percorsi di apprendimento disponibili?

Microsoft 365 percorsi di apprendimento sono attualmente disponibili solo in inglese. Il provisioning end-to-end automatico funziona solo con i tenant inglesi. Nel secondo trimestre del 2020 è in programma l'implementazione del supporto multilingue per le lingue seguenti. 

- Cinese (semplificato) 
- Francese  
- Tedesco 
- Italiano (Italia) 
- Giapponese (Giappone)  
- Portoghese (Brasile) 
- Russo (russo)  
- Spagnolo 

> Il supporto per la lingua olandese non sarà incluso nella prossima versione del supporto multilingue per i percorsi di apprendimento. Continueremo a valutare le nuove opzioni linguistiche in futuro.

### <a name="how-long-will-it-take-to-install-the-site-in-our-tenant-environment"></a>Quanto tempo è necessario per installare il sito nell'ambiente tenant?

In base ai test dell'installazione, l'installazione dovrebbe richiedere meno di 15 minuti. Questa operazione non include il tempo necessario per personalizzare il sito in base alle proprie esigenze.

### <a name="is-microsoft-365-learning-pathways-an-open-source-solution-and-what-are-the-implications"></a>I Microsoft 365 di apprendimento sono una soluzione open source e quali sono le implicazioni?

Microsoft 365 percorsi di apprendimento è una soluzione di software open source (OSS) e di conseguenza comporta una serie di vantaggi e considerazioni all'OSS:

#### <a name="benefits"></a>Vantaggi 
- **Microsoft 365 percorsi di apprendimento è una soluzione gratuita:** I clienti possono installare la soluzione nel tenant, personalizzarla e renderla disponibile per gli utenti finali
- **OSS consente uno sviluppo e una collaborazione rapidi:**  Tutte le soluzioni open source sono disponibili per un'ampia community di collaboratori.  Microsoft si impegna a utilizzare questo metodo per guidare l'innovazione.  Per garantire che stiamo offrendo un'esperienza a vantaggio del più ampio set di clienti, il nostro team di gestione dei servizi di base si riserva il diritto di determinare quali contributi vengono uniti nella build ufficiale.  
- **OSS consente la collaborazione con i partner:** Microsoft sta collaborando con diversi partner di apprendimento per supportare i propri sforzi per le estensioni future e i contributi per Microsoft 365 percorsi di apprendimento. Verranno fornite ulteriori informazioni man appena questi piani verranno finalizzati. 
    
#### <a name="implications"></a>Implicazioni
- **OSS non è un prodotto disponibile in commercio:** I prodotti commerciali includono l'aggiornamento e l'applicazione di patch e sono inclusi nei contratti di supporto a pagamento. Mentre Microsoft attualmente offre documentazione, aggiornamento e applicazione di patch per Microsoft 365 percorsi di apprendimento, si basa sul nostro impegno a migliorare questo specifico scenario aziendale. I nostri piani sono di continuare a investire nei percorsi di apprendimento, tenere presente che il team di gestione dei servizi potrebbe cambiare le strategie in futuro. Eventuali modifiche future ai Microsoft 365 di apprendimento verranno comunicate prima di essere applicate. 
- **Come OSS, i Microsoft 365** di apprendimento sono supportati tramite un elenco di problemi online in GitHub : i percorsi di apprendimento di Microsoft 365 non sono coperti da alcun contratto di supporto Microsoft esistente. I problemi inviati vengono valutati dai Microsoft 365 dei percorsi di apprendimento e dalla community. I livelli di servizio per la risoluzione dei problemi NON sono allo stesso livello di un contratto di supporto Microsoft a pagamento.  

### <a name="can-we-make-the-microsoft-365-learning-pathways-a-subsite-of-our-primary-sharepoint-site-collection"></a>È possibile impostare i Microsoft 365 di apprendimento come sito secondario della raccolta siti SharePoint principale?

No. Il sito si basa su un modello di sito di comunicazione, che deve sempre essere una raccolta siti radice.

> [!NOTE]
> È importante considerare le autorizzazioni necessarie agli utenti finali per accedere al sito. La maggior parte delle organizzazioni dispone di gruppi di utenti o di sicurezza definiti. È necessario aggiungere i gruppi di sicurezza appropriati al nuovo portale di formazione quando si è pronti per avviarlo nella community dei dipendenti.

### <a name="i-need-to-reinstall-the-site-what-should-i-do"></a>È necessario reinstallare il sito. Cosa dovrei fare?

Seguire le istruzioni di installazione pubblicate [qui.](custom_provision.md)

> [!NOTE]
> Se la telemetria è stata disabilitata nell'installazione precedente e si desidera continuare con la telemetria disabilitata, è necessario seguire le istruzioni per disabilitare la telemetria qui.

### <a name="we-made-updates-to-our-implementation-of-microsoft-365-learning-pathways-will-we-lose-these-updates-made-to-site-template-playlists-if-we-reinstall-the-site"></a>Sono stati apportati aggiornamenti all'implementazione Microsoft 365 percorsi di apprendimento. Questi aggiornamenti (apportati a modelli di sito, playlist) andranno persi se si reinstalla il sito?

Le personalizzazioni per singole pagine e playlist personalizzate andranno perse se si reinstalla il sito nell'installazione corrente.  
