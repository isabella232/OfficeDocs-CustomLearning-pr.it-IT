---
author: pkrebs
ms.author: pkrebs
title: Effettuare il provisioning del sito Learning personalizzato
ms.date: 02/10/2019
description: Eseguire il provisioning del Learning personalizzato Office 365 sito tramite il motore di provisioning SharePoint
ms.service: sharepoint-online
manager: bpardi
ms.topic: article
audience: admin
ms.openlocfilehash: d8fa6d3c3dbcbcf6c82659e28526bd026c5594e0
ms.sourcegitcommit: a93cae8ea6e3c1141d7266d04131b69f2c2498cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/23/2021
ms.locfileid: "59485224"
---
# <a name="provision-custom-learning"></a>Effettuare il provisioning di Learning

Con il SharePoint di provisioning online, un Office 365 tenant può avviare il processo di provisioning con pochi semplici clic. Il servizio di provisioning è il modo consigliato per eseguire il provisioning di Learning. L'avvio del processo è rapido, semplice e richiede solo pochi minuti. Prima di iniziare a usare il servizio di provisioning, tuttavia, assicurati di aver soddisfatto i prerequisiti per il provisioning.

## <a name="prerequisites"></a>Prerequisiti
 
Per configurare correttamente il Learning personalizzato con il servizio di provisioning [SharePoint Online Provisioning Service,](https://provisioning.sharepointpnp.com)l'utente che effettua il provisioning deve soddisfare i prerequisiti seguenti: 
 
- La persona che effettua il provisioning Learning deve essere un amministratore tenant del tenant in cui verrà eseguito il provisioning Learning personalizzato.  
- Un Catalogo app tenant deve essere disponibile all'interno dell'opzione App dell'SharePoint admin center. Se l'organizzazione non dispone di un SharePoint app tenant, fare riferimento alla documentazione [SharePoint Online](/sharepoint/use-app-catalog) per crearne uno.  
- L'utente che Learning deve essere un proprietario della raccolta siti del Catalogo app tenant. Se l'utente che provisioning Learning non è un proprietario della raccolta siti del Catalogo [app, completare queste istruzioni](addappadmin.md) e continuare. 

### <a name="to-provision-custom-learning"></a>Per eseguire il provisioning di Learning

1. Vai a http://provisioning.sharepointpnp.com e **accedi dall'angolo** in alto a destra della home page.  Accedere con le credenziali per il tenant di destinazione in cui si prevede di installare il modello di sito.
![Pagina principale del servizio di provisioning.](media/inst_signin.png)

2. Deselezionare **Consenso per conto dell'organizzazione e** selezionare **Accetta**.

   ![autorizzazioni di installazione](media/inst_perms.png)

3. Selezionare **Personalizzato Learning per Office 365** dalla raccolta soluzioni.
![Schermata in cui selezionare Personalizzato Learning per Office 365.](media/inst_select.png)

   ![selezione dell'opzione di installazione](media/inst_select.png)

4. Nella home page della soluzione seleziona **Aggiungi al tenant**

      ![inst_select.png](media/inst_add.png)

5. Completare i campi nella pagina delle informazioni sul provisioning, come opportuno per l'installazione. Immettere almeno l'indirizzo di posta elettronica in cui si desidera ricevere notifiche sul processo di provisioning e sull'URL di destinazione per il provisioning del sito.  
   > [!NOTE]
   > Rendere l'URL di destinazione del sito più semplice per i dipendenti, ad esempio "/sites/MyTraining" o "/teams/LearnOffice365".

   ![opzioni di installazione](media/inst_options.png)

6. Selezionare **Esegui il** provisioning quando si è pronti per installare Learning personalizzata nell'ambiente tenant.  Il processo di provisioning richiederà fino a 15 minuti. Quando il sito è pronto per l'accesso, si riceverà una notifica tramite posta elettronica (all'indirizzo di posta elettronica immesso nella pagina del provisioning).

> [!IMPORTANT]
> L'amministratore tenant che esegue il provisioning del sito Learning personalizzato deve accedere al sito e quindi aprire CustomLearningAdmin.aspx per inizializzare le proprietà di Learning personalizzate. In questo momento, l'amministratore tenant deve anche assegnare proprietari al sito. 

## <a name="validate-provisioning-success"></a>Convalida del provisioning completata

Al termine del provisioning, l'amministratore tenant riceve un messaggio di posta elettronica dal servizio di provisioning PnP. L'amministratore può copiare il collegamento al sito fornito nel messaggio di posta elettronica e quindi seguire le istruzioni per accedere al sito. In alternativa, l'amministratore tenant può passare a YOUR-SITE-COLLECTION-URL/SitePages/CustomLearningAdmin.aspx. In questo modo viene inizializzata la voce di elenco CustomConfig che configura i Learning personalizzati per il primo utilizzo. La persona che apre per la prima volta questa pagina deve essere un amministratore tenant, un amministratore della raccolta siti o un proprietario del sito. Dovrebbe essere visualizzata una pagina simile alla seguente: 

## <a name="add-owners-to-site"></a>Aggiungere proprietari al sito
In quanto amministratore tenant, è improbabile che tu sia la persona che personalizza il sito, quindi dovrai assegnare proprietari al sito. I proprietari dispongono di privilegi amministrativi per il sito in modo che possano modificare le pagine del sito e rebrand il sito. Possono inoltre nascondere e visualizzare il contenuto recapitato tramite la web part Learning personalizzata. Inoltre, possono creare playlist personalizzate e assegnarle a sottocategorie personalizzate.  

1. Scegliere Autorizzazioni sito **dal** menu SharePoint Impostazioni **sito.**
2. Fare **clic su Autorizzazioni avanzate Impostazioni**.
3. Fare **clic Formazione personalizzata per Office 365 proprietari**.
4. Fare **clic** su Nuovo Aggiungi utenti a questo gruppo, aggiungere le persone che si desidera siano proprietari  >  e quindi fare clic su **Condividi.**

8. Fare clic **sull'opzione** Seguente nell'angolo in alto a destra della pagina per seguire il sito.  
