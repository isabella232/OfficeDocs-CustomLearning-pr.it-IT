---
author: pkrebs
ms.author: pkrebs
title: Eseguire il provisioning del sito Microsoft 365 Learning pathways
ms.date: 02/10/2019
description: Eseguire il provisioning del sito Microsoft 365 Learning pathways tramite il servizio di provisioning di SharePoint
ms.openlocfilehash: e48052a395a8669ef684110a1c93409f5859a1d2
ms.sourcegitcommit: 0077704d7edcc26eda76900115716fc5b7b1c518
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2019
ms.locfileid: "34334745"
---
# <a name="provision-microsoft-365-learning-pathways"></a>Provisioning di percorsi di apprendimento Microsoft 365

Con il servizio di provisioning di SharePoint Online, un amministratore del tenant di Office 365 può avviare il processo di provisioning con alcuni semplici clic. Il servizio di provisioning è il modo consigliato per eseguire il provisioning dei percorsi di apprendimento. È veloce, semplice e richiede solo alcuni minuti per iniziare il processo. Prima di iniziare a usare il servizio di provisioning, accertarsi di aver soddisfatto i prerequisiti per il provisioning.

> [!IMPORTANT]
> A 5/21/2019, Microsoft 365 Learning pathways è il nuovo nome della soluzione precedentemente noto come Custom learning per Office 365. Se è già stato effettuato il provisioning di apprendimento personalizzato per Office 365 nell'organizzazione e si desidera aggiornare la soluzione, seguire le istruzioni "Updating the Solution" nel [file Leggimi di Microsoft 365 Learning pathways](https://github.com/pnp/custom-learning-office-365). Se si desidera eseguire il provisioning dei percorsi di apprendimento di Microsoft 365 per la prima volta, vedere [provision microsoft 365 Learning pathways]( https://docs.microsoft.com/en-us/office365/customlearning/custom_provision) instructions nella documentazione relativa ai percorsi di apprendimento di Microsoft 365.  

## <a name="prerequisites"></a>Prerequisiti
 
Per configurare correttamente i percorsi di apprendimento di Microsoft 365 con il servizio di provisioning, la persona che effettua il provisioning deve soddisfare i requisiti seguenti: 
 
- I percorsi di apprendimento per il provisioning delle persone devono essere un amministratore tenant del tenant in cui verrà eseguito il provisioning dei percorsi di apprendimento.  
- Un catalogo app tenant deve essere disponibile all'interno dell'opzione Apps dell'interfaccia di amministrazione di SharePoint. Se nell'organizzazione non è presente un catalogo delle app di SharePoint tenant, fare riferimento alla [documentazione di SharePoint Online](https://docs.microsoft.com/en-us/sharepoint/use-app-catalog) per crearne uno.  
- I percorsi di apprendimento per il provisioning delle persone devono essere proprietari di una raccolta siti del catalogo app tenant. Se il provisioning dei percorsi di apprendimento della persona non è un proprietario della raccolta siti del catalogo app, [completare queste istruzioni](addappadmin.md) e continuare. 

### <a name="to-provision-learning-pathways"></a>Per eseguire il provisioning di percorsi di apprendimento

1. Passare a http://provisioning.sharepointpnp.com e **accedere** dall'angolo in alto a destra della Home page.  Accedere con le credenziali del tenant di destinazione in cui si intende installare il modello di sito.

![pnphome. png](media/inst_signin.png)

2. Cancellare il **consenso per conto dell'organizzazione** e selezionare **accetta**.

![in](media/inst_perms.png)

Il servizio di provisioning richiede queste autorizzazioni per creare il catalogo app tenant, installare l'applicazione nel catalogo app tenant e provisionare il modello di sito. Non vi è alcun impatto generale sul tenant e queste autorizzazioni vengono utilizzate in modo esplicito per l'installazione della soluzione. È necessario accettare queste autorizzazioni per procedere con l'installazione.

3. Scorrere verso il basso la pagina, selezionare la scheda **soluzioni** e quindi fare clic **su percorsi di apprendimento per Office 365**. 

![in](media/inst_select.png)

4. Selezionare **Aggiungi al tenant**

![inst_select. png](media/inst_add.png)

5. Completare i campi nella pagina informazioni di provisioning in base alle proprie esigenze per l'installazione. Immettere almeno l'indirizzo di posta elettronica in cui si desidera ottenere le notifiche relative al processo di provisioning e all'URL di destinazione del sito di cui eseguire il provisioning.  
> [!NOTE]
> Rendere l'URL di destinazione per il sito una cosa semplice per i dipendenti, ad esempio "/sites/MyTraining" o "/teams/LearnMicrosoft365".

![inst_options. png](media/inst_options.png)

6. Selezionare **** provisioning quando si è pronti per installare percorsi di apprendimento nell'ambiente tenant.  Il processo di provisioning richiederà fino a 15 minuti. L'utente riceverà una notifica tramite posta elettronica (all'indirizzo di posta elettronica di notifica immesso nella pagina di provisioning) quando il sito è pronto per l'accesso. 

> [!IMPORTANT]
> L'amministratore tenant che accantona il sito percorsi di apprendimento deve passare al sito e quindi aprire **CustomLearningAdmin. aspx** per inizializzare le proprietà di amministratore di percorsi di apprendimento. A questo punto, l'amministratore del tenant deve anche assegnare i proprietari al sito. 

## <a name="validate-provisioning-success-and-initialize-the-customconfig-list"></a>Convalidare il provisioning di esito positivo e inizializzare l'elenco CustomConfig

Al termine del provisioning, l'amministratore del tenant che ha eseguito il provisioning del sito riceve un messaggio di posta elettronica dal servizio di provisioning PnP. Il messaggio di posta elettronica contiene un collegamento al sito. A questo punto, l'amministratore del tenant deve passare al sito utilizzando il collegamento fornito nel messaggio di posta elettronica e configurare il sito per il primo utilizzo:

- Passare a `<YOUR-SITE-COLLECTION-URL>sites/<YOUR-SITE-NAME>/SitePages/CustomLearningAdmin.aspx`. L'apertura di **CustomLearningAdmin. aspx** consente di inizializzare l'elemento di elenco **CustomConfig** che consente di configurare i percorsi di apprendimento per il primo utilizzo. Dovrebbe essere visualizzata una pagina simile alla seguente:

![CG-adminapppage. png](media/cg-adminapppage.png)

## <a name="add-owners-to-site"></a>Aggiungere proprietari al sito
Come amministratore del tenant, è improbabile che tu sia la persona che Personalizza il sito, quindi dovrai assegnare alcuni proprietari al sito. I proprietari dispongono di privilegi amministrativi per il sito in modo che possano modificare le pagine del sito e rimarcare il sito. Sono inoltre in grado di nascondere e visualizzare i contenuti forniti tramite la Web part percorsi di apprendimento. Inoltre, avranno la possibilità di creare playlist personalizzate e assegnarle a sottocategorie personalizzate.  

1. Scegliere **autorizzazioni sito**dal menu **Impostazioni** di SharePoint.
2. Fare clic su **Impostazioni avanzate di autorizzazione**.
3. Fare clic su **Microsoft 365 Learning pathways owners**.
4. Fare clic su **nuovo** > **Aggiungi utenti a questo gruppo**e quindi aggiungere le persone che si desidera siano proprietari. 
5. Aggiungere un collegamento per [esplorare il sito](custom_exploresite.md) nel messaggio di condivisione e quindi fare clic su **Condividi**.

### <a name="next-steps"></a>Operazioni successive
- Esaminare il [contenuto predefinito](custom_exploresite.md) fornito nel sito e nella web part.
