---
author: pkrebs
ms.author: pkrebs
title: Eseguire il provisioning del sito di apprendimento personalizzato
ms.date: 02/10/2019
description: Eseguire il provisioning del sito di apprendimento personalizzato per Office 365 tramite il motore di provisioning di SharePoint
ms.service: sharepoint online
ms.openlocfilehash: be45ade7588f08801062710d310ca967ddd23926
ms.sourcegitcommit: 907c657e7cc5a4a44d2b9f38cc35fea9ac5c5943
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2021
ms.locfileid: "51162923"
---
# <a name="provision-custom-learning"></a>Eseguire il provisioning dell'apprendimento personalizzato

Con il servizio di provisioning di SharePoint Online, un amministratore tenant di Office 365 può avviare il processo di provisioning con pochi semplici clic. Il servizio di provisioning è il modo consigliato per eseguire il provisioning dell'apprendimento personalizzato. L'avvio del processo è rapido, semplice e richiede solo pochi minuti. Prima di iniziare a usare il servizio di provisioning, tuttavia, assicurati di aver soddisfatto i prerequisiti per il provisioning.

## <a name="prerequisites"></a>Prerequisiti
 
Per configurare correttamente l'apprendimento personalizzato con il servizio di provisioning del servizio di provisioning [di SharePoint Online,](https://provisioning.sharepointpnp.com)l'utente che effettua il provisioning deve soddisfare i prerequisiti seguenti: 
 
- La persona che effettua il provisioning di Apprendimento personalizzato deve essere un amministratore tenant del tenant in cui verrà eseguito il provisioning dell'apprendimento personalizzato.  
- Un Catalogo app tenant deve essere disponibile nell'opzione App dell'interfaccia di amministrazione di SharePoint. Se l'organizzazione non dispone di un catalogo app tenant di SharePoint, fare riferimento alla documentazione [di SharePoint Online](/sharepoint/use-app-catalog) per crearne uno.  
- L'utente che provisioning apprendimento personalizzato deve essere un proprietario della raccolta siti del Catalogo app tenant. Se l'utente che provisioning apprendimento personalizzato non è un proprietario della raccolta siti del Catalogo [app, completare queste istruzioni](addappadmin.md) e continuare. 

### <a name="to-provision-custom-learning"></a>Per eseguire il provisioning dell'apprendimento personalizzato

1. Vai a http://provisioning.sharepointpnp.com e **accedi dall'angolo** in alto a destra della home page.  Accedere con le credenziali per il tenant di destinazione in cui si prevede di installare il modello di sito.

![pnphome.png](media/inst_signin.png)

2. Deselezionare **Consenso per conto dell'organizzazione e** selezionare **Accetta**.

![in](media/inst_perms.png)

3. Selezionare **Apprendimento personalizzato per Office 365** dalla raccolta soluzioni.

![in](media/inst_select.png)

4. Nella home page della soluzione seleziona **Aggiungi al tenant**

![inst_select.png](media/inst_add.png)

5. Completare i campi nella pagina delle informazioni sul provisioning, come opportuno per l'installazione. Immettere almeno l'indirizzo di posta elettronica in cui si desidera ricevere notifiche sul processo di provisioning e sull'URL di destinazione per il provisioning del sito.  
> [!NOTE]
> Rendere l'URL di destinazione del sito più semplice per i dipendenti, ad esempio "/sites/MyTraining" o "/teams/LearnOffice365".

![inst_options.png](media/inst_options.png)

6. Selezionare **Esegui il** provisioning quando si è pronti per installare Apprendimento personalizzato nell'ambiente tenant.  Il processo di provisioning richiederà fino a 15 minuti. Quando il sito è pronto per l'accesso, si riceverà una notifica tramite posta elettronica (all'indirizzo di posta elettronica immesso nella pagina del provisioning).

> [!IMPORTANT]
> L'amministratore tenant che esegue il provisioning del sito di apprendimento personalizzato deve accedere al sito e quindi aprire CustomLearningAdmin.aspx per inizializzare le proprietà di Amministratore apprendimento personalizzato. In questo momento, l'amministratore tenant deve anche assegnare proprietari al sito. 

## <a name="validate-provisioning-success"></a>Convalida del provisioning completata

Al termine del provisioning, l'amministratore tenant riceve un messaggio di posta elettronica dal servizio di provisioning PnP. L'amministratore può copiare il collegamento al sito fornito nel messaggio di posta elettronica e quindi seguire le istruzioni per accedere al sito. In alternativa, l'amministratore tenant può passare <YOUR-SITE-COLLECTION-URL>/SitePages/CustomLearningAdmin.aspx. In questo modo viene inizializzata la voce di elenco CustomConfig che configura l'apprendimento personalizzato per il primo utilizzo. La persona che apre per la prima volta questa pagina deve essere un amministratore tenant, un amministratore della raccolta siti o un proprietario del sito. Dovrebbe essere visualizzata una pagina simile alla seguente: 

## <a name="add-owners-to-site"></a>Aggiungere proprietari al sito
In quanto amministratore tenant, è improbabile che tu sia la persona che personalizza il sito, quindi dovrai assegnare proprietari al sito. I proprietari dispongono di privilegi amministrativi per il sito in modo che possano modificare le pagine del sito e rebrand il sito. Hanno anche la possibilità di nascondere e mostrare il contenuto recapitato tramite la web part Apprendimento personalizzato. Inoltre, possono creare playlist personalizzate e assegnarle a sottocategorie personalizzate.  

1. Scegliere Autorizzazioni sito **dal** menu Impostazioni di SharePoint. 
2. Fare clic **su Impostazioni di autorizzazione avanzate**.
3. Fare **clic su Apprendimento personalizzato per i proprietari di Office 365**.
4. Fare **clic** su Nuovo Aggiungi utenti a questo gruppo, aggiungere le persone che si desidera siano proprietari  >  e quindi fare clic su **Condividi.**

8. Fare clic **sull'opzione** Seguente nell'angolo in alto a destra della pagina per seguire il sito.  

### <a name="next-steps"></a>Operazioni successive
- Esplorare il [contenuto predefinito](sitecontent.md) incluso nella web part.