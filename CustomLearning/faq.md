---
author: karuanag
ms.author: karuanag
title: Domande frequenti per i percorsi di apprendimento di Microsoft 365
ms.date: 02/10/2019
description: Informazioni sulle domande più frequenti per i percorsi di apprendimento di Microsoft 365
ms.openlocfilehash: 5b90971ef6e411b4bd8d0cece2d8211f6fd5db23
ms.sourcegitcommit: 86cfa176d50b324c964b1a8609270cc73a2468b3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/17/2019
ms.locfileid: "40068817"
---
# <a name="frequently-asked-questions"></a>Domande frequenti

### <a name="i-recently-saw-a-blog-post-that-custom-learning-for-office-365-is-being-renamed-to-microsoft-365-learning-pathways-are-there-other-changes-being-added-to-the-solution-as-part-of-the-renaming-effort-should-i-update-the-solution-in-my-organization"></a>Recentemente ho visto un post di Blog in cui l'apprendimento personalizzato per Office 365 viene rinominato nei percorsi di apprendimento di Microsoft 365. Sono state aggiunte altre modifiche alla soluzione come parte dello sforzo di ridenominazione? È necessario aggiornare la soluzione nell'organizzazione?

Microsoft 365 Learning pathways release è uno sforzo di rebranding dedicato alla modifica del nome della soluzione da allineare con Microsoft 365 branding. Se si dispone di un'istruzione personalizzata per Office 365 attualmente in esecuzione correttamente nell'organizzazione, non è necessario aggiornare la soluzione in questo momento.  

### <a name="what-are-the-requirements-for-installing-microsoft-365-learning-pathways-into-my-tenant-environment"></a>Quali sono i requisiti per l'installazione di percorsi di apprendimento di Microsoft 365 nell'ambiente tenant?

- SharePoint Online e i siti di comunicazione sono abilitati.
- L'individuo che dovrà eseguire il provisioning di CLO365 deve essere l'amministratore tenant del tenant di destinazione per l'installazione.
- Il tenant ' App Catalog ' deve essere disponibile all'interno dell'opzione ' Apps ' dell'interfaccia di amministrazione di SharePoint.
- Se viene creato un nuovo catalogo app, è necessario un tempo di attesa di 30 minuti o più per il provisioning completo del catalogo app. Se si tenta di eseguire il provisioning dei percorsi di apprendimento di Microsoft 365 direttamente dopo la creazione del catalogo app tenant, verrà generato un errore di predisposizione della soluzione di percorsi di apprendimento. 
- L'individuo che dovrà eseguire il provisioning di CLO365 deve essere un amministratore della raccolta siti del catalogo app nel tenant di destinazione per l'installazione.

### <a name="why-is-microsoft-asking-for-tenant-permissions-when-installing-microsoft-365-learning-pathways"></a>Perché Microsoft richiede autorizzazioni tenant quando si installano i percorsi di apprendimento di Microsoft 365 

- Il servizio di provisioning di SharePoint Online utilizza le autorizzazioni per eseguire il provisioning del sito di SharePoint per i percorsi di apprendimento, creare le pagine del sito e installare l'applicazione Microsoft 365 Learning pathways all'interno del tenant. Questo è l'unico motivo per il quale noi chiediamo le autorizzazioni. Senza le autorizzazioni richieste, il servizio di provisioning di SharePoint non è in grado di eseguire i comandi che installano automaticamente il modello di sito e la Web part di apprendimento. 

### <a name="what-are-the-implications-of-microsoft-365-learning-pathways-being-in-a-beta-preview"></a>Quali sono le implicazioni dei percorsi di apprendimento di Microsoft 365 che si trovano in un'anteprima beta? 

Microsoft 365 Learning pathways è attualmente in anteprima beta. Tenere presente quanto segue durante la valutazione, la pianificazione e l'implementazione dei percorsi di apprendimento di Microsoft 365:

- Come per qualsiasi soluzione beta, il team di gestione del servizio si riserva il diritto di apportare modifiche al servizio e ai relativi componenti. Poiché si stanno risolvendo attivamente i problemi relativi a bug e UX, è probabile che sia necessario aggiornare il controllo WebPart.
- Per aggiornare la Web part è necessario scaricarla dal repository GitHub e caricarla nel catalogo app tenant. Vedere la sezione "Updating the Solution" del file [Readme](https://github.com/pnp/custom-learning-office-365/blob/master/README.md) di Microsoft 365 Learning pathways. 

### <a name="what-languages-is-microsoft-365-learning-pathways-available-in"></a>In quali lingue sono disponibili i percorsi di apprendimento di Microsoft 365?

Microsoft 365 Learning pathways è attualmente disponibile solo in inglese. Il provisioning finale automatico è compatibile solo con i tenant inglesi. Si prevede di implementare il supporto multilingue per queste nove lingue nel primo trimestre di 2020. 

- Cinese (semplificato) 
- Olandese (Paesi Bassi) 
- Francese  
- Tedesco 
- Italiano (Italia) 
- Giapponese (Giappone)  
- Portoghese (Brasile) 
- Russo (Russo)  
- Spagnolo 

### <a name="how-long-will-it-take-to-install-the-site-in-our-tenant-environment"></a>Quanto tempo richiederà l'installazione del sito nell'ambiente tenant?

In base al testing dell'installazione, dovrebbe essere necessario meno di 15 minuti. Questo non include il tempo necessario per personalizzare il sito in base alle proprie esigenze.

### <a name="is-microsoft-365-learning-pathways-an-open-source-solution-and-what-are-the-implications"></a>Microsoft 365 Learning pathways è una soluzione open source e quali sono le implicazioni?

Microsoft 365 Learning pathways è una soluzione open source software (OSS) e, come tale, trasporta una serie di vantaggi e considerazioni in tedesco per OSS:

#### <a name="benefits"></a>Benefit 
- **Microsoft 365 Learning pathways è una soluzione gratuita:** I clienti possono installare la soluzione nel tenant, personalizzarla e renderla disponibile per gli utenti finali
- **OSS consente lo sviluppo e la collaborazione rapidi:**  Tutte le soluzioni open source sono disponibili per una vasta community di collaboratori.  Microsoft si impegna a questo metodo di guida dell'innovazione.  Per garantire la realizzazione di un'esperienza che avvantaggia il più ampio gruppo di clienti, il team di gestione dei servizi di base si riserva il diritto di stabilire quali contributi vengono uniti nella build ufficiale.  
- **OSS consente la collaborazione con i partner:** Microsoft sta lavorando con diversi partner di apprendimento per supportare i propri sforzi per future estensioni e contributi a Microsoft 365 Learning pathways. Verranno fornite ulteriori informazioni man mano che questi piani vengono definiti. 
    
#### <a name="implications"></a>Implicazioni
- **OSS non è un prodotto disponibile commercialmente:** I prodotti commerciali includono l'aggiornamento e l'applicazione di patch e sono inclusi nei contratti di supporto basati sulla tariffa. Anche se Microsoft offre attualmente la documentazione, l'aggiornamento e l'applicazione di patch per i percorsi di apprendimento di Microsoft 365, si basa sul nostro impegno a migliorare questo scenario aziendale specifico. I nostri piani devono continuare a investire nei percorsi di apprendimento, ma i clienti devono essere consapevoli del fatto che il team di gestione dei servizi può modificare le strategie in futuro. Tutte le future modifiche apportate ai percorsi di apprendimento di Microsoft 365 verranno comunicate in anticipo. 
- **Come OSS, microsoft 365 Learning pathways è supportato tramite un elenco di problemi online su GitHub**: i percorsi di apprendimento di Microsoft 365 non sono coperti da alcun contratto di supporto tecnico Microsoft esistente. I problemi inviati vengono valutati da Microsoft 365 Learning pathways Service owners e dalla community. I livelli del servizio di risoluzione dei problemi non sono allo stesso livello del contratto di supporto tecnico Microsoft pagato.  

### <a name="can-we-make-the-microsoft-365-learning-pathways-a-subsite-of-our-primary-sharepoint-site-collection"></a>È possibile creare percorsi di apprendimento di Microsoft 365 come siti secondari della raccolta siti di SharePoint principale?

No. Il sito si basa su un modello di sito di comunicazione, che deve essere sempre costituito da una raccolta siti radice.

> [!NOTE]
> È importante prendere in considerazione le autorizzazioni necessarie per accedere al sito da parte degli utenti finali. La maggior parte delle organizzazioni ha definito i gruppi di sicurezza o di utenti. È necessario aggiungere i gruppi di sicurezza adeguati al nuovo portale di training dopo essere pronti a avviarlo nella community dei dipendenti.

### <a name="i-need-to-reinstall-the-site-what-should-i-do"></a>È necessario reinstallare il sito. Cosa dovrei fare?

Seguire le istruzioni per l'installazione pubblicate [qui](custom_provision.md).

> [!NOTE]
> Se la telemetria è stata disattivata nell'installazione precedente e si desidera continuare con la telemetria disattivata, sarà necessario seguire le istruzioni per disabilitare la telemetria.

### <a name="we-made-updates-to-our-implementation-of-microsoft-365-learning-pathways-will-we-lose-these-updates-made-to-site-template-playlists-if-we-reinstall-the-site"></a>Sono stati apportati aggiornamenti alla nostra implementazione dei percorsi di apprendimento di Microsoft 365. Se si reinstalla il sito, verranno persi questi aggiornamenti (creati per il modello di sito, le playlist)?

Le personalizzazioni di singole pagine e playlist personalizzate andranno perse se si reinstalla il sito tramite l'installazione corrente.  