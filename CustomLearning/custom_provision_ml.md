---
author: pkrebs
ms.author: pkrebs
title: Provisioning di una nuova soluzione di percorsi di apprendimento multilingue
ms.date: 02/10/2019
description: Eseguire il provisioning del sito Microsoft 365 Learning pathways tramite il servizio di provisioning di SharePoint
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 380063b92713bf571438a0e2be21f0638dde0cfb
ms.sourcegitcommit: 1f080ed4cf3687f922907304db3fd7a06aa9d501
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/02/2020
ms.locfileid: "45031712"
---
# <a name="provision-a-new-learning-pathways-multilingual-solution"></a>Provisioning di una nuova soluzione di percorsi di apprendimento multilingue
Le organizzazioni che non dispongono di percorsi di apprendimento già sottoposto a provisioning nel tenant possono aggiungere alla propria tenant la soluzione per i percorsi di apprendimento multilingue. Con questa opzione, il modello di percorsi di apprendimento di SharePoint viene convertito in nove lingue e può essere utilizzato con una modifica minima. 

> [!IMPORTANT]
> Se è già stato effettuato il provisioning dei percorsi di apprendimento nel tenant, è consigliabile seguire il [percorso di aggiornamento](custom_update_ml.md) per i percorsi di apprendimento. Se si installano percorsi di apprendimento su un'istanza esistente del tenant, le eventuali modifiche apportate al modello di sito percorsi di apprendimento o alle playlist potrebbero andare perse.

## <a name="prerequisites-for-multilingual-support"></a>Prerequisiti per il supporto multilingue
 
Per configurare correttamente i percorsi di apprendimento di Microsoft 365 con il servizio di provisioning, la persona che effettua il provisioning deve soddisfare i requisiti seguenti: 
 
- I percorsi di apprendimento per il provisioning delle persone devono essere un amministratore tenant del tenant in cui verrà eseguito il provisioning dei percorsi di apprendimento.  
- Un catalogo app tenant deve essere disponibile all'interno dell'opzione Apps dell'interfaccia di amministrazione di SharePoint. Se nell'organizzazione non è presente un catalogo delle app di SharePoint tenant, fare riferimento alla [documentazione di SharePoint Online](https://docs.microsoft.com/sharepoint/use-app-catalog) per crearne uno. Prima di eseguire il provisioning dei percorsi di apprendimento, è necessario attendere almeno due ore dopo aver creato il catalogo app.  
- I percorsi di apprendimento per il provisioning delle persone devono essere proprietari di una raccolta siti del catalogo app tenant. Se il provisioning dei percorsi di apprendimento della persona non è un proprietario della raccolta siti del catalogo app, [completare queste istruzioni](addappadmin.md) e continuare. 

## <a name="ensure-the-tenant-admin-account-doesnt-have-a-language-selected"></a>Assicurarsi che l'account amministratore tenant non disponga di una lingua selezionata
Prima di eseguire il provisioning dei percorsi di apprendimento, assicurarsi che l'account di amministratore per il tenant non disponga di una lingua selezionata. Ecco come verificare se l'account amministratore non dispone di una lingua selezionata. 
1.  Con il profilo di amministratore del server perimetrale, passare a office.com.
2.  Immettere le credenziali utente (se necessario).
3.  In Microsoft 365, fare clic su **tutte le app** > approfondire. 
4.  Fare clic su **me**  >  **Update profile**.
5.  Scorrere verso il basso la pagina e fare clic su **come è possibile modificare le impostazioni internazionali e della lingua**.
6.  Fare clic **qui**e quindi fare clic sui puntini di ellisse **.**
7.  In **My Display languages**, non è necessario visualizzare le **lingue selezionate**. Se è selezionata una lingua, deselezionarla.

### <a name="to-provision-learning-pathways"></a>Per eseguire il provisioning di percorsi di apprendimento

1. Passare alla [pagina Microsoft 365 Learning pathways Solution](https://provisioning.sharepointpnp.com/details/3df8bd55-b872-4c9d-88e3-6b2f05344239).
2. Fare clic su **Aggiungi al tenant**. Se non è stato eseguito l'accesso al tenant, il servizio di provisioning richiederà le credenziali di amministratore tenant. 
3. Nella finestra di dialogo autorizzazioni richieste selezionare **consenso per conto dell'organizzazione** e quindi selezionare **accetta**.

Il servizio di provisioning richiede queste autorizzazioni per creare il catalogo app tenant, installare l'applicazione nel catalogo app tenant e provisionare il modello di sito. Non è previsto alcun impatto generale sul tenant. Queste autorizzazioni vengono utilizzate in modo esplicito per l'installazione della soluzione. È necessario accettare queste autorizzazioni per continuare con l'installazione.

4. Completare i campi nella pagina informazioni di provisioning in base alle proprie esigenze per l'installazione. Immettere almeno l'indirizzo di posta elettronica in cui si desidera ottenere le notifiche relative al processo di provisioning e l'URL di destinazione per il sito di cui eseguire il provisioning.  
> [!NOTE]
> Rendere l'URL di destinazione per il sito una cosa semplice per i dipendenti, ad esempio "/sites/MyTraining" o "/teams/LearnMicrosoft365".

![inst_options.png](media/inst_options.png)

6. Fare clic su **provisioning** quando si è pronti per installare percorsi di apprendimento nell'ambiente tenant.  Il processo di provisioning può richiedere fino a 15 minuti. L'utente riceverà una notifica tramite posta elettronica quando il sito sarà pronto. 

> [!IMPORTANT]
> L'amministratore tenant che accantona il sito percorsi di apprendimento deve passare al sito e quindi aprire **CustomLearningAdmin. aspx** per inizializzare le proprietà di amministratore di percorsi di apprendimento. A questo punto, l'amministratore del tenant deve anche assegnare i proprietari al sito. 

## <a name="validate-provisioning-success-and-initialize-the-customconfig-list"></a>Convalidare il provisioning di esito positivo e inizializzare l'elenco CustomConfig

Al termine del provisioning, l'amministratore del tenant che ha eseguito il provisioning del sito riceve un messaggio di posta elettronica dal servizio di provisioning PnP. Il messaggio di posta elettronica contiene un collegamento al sito. A questo punto, l'amministratore del tenant deve passare al sito utilizzando il collegamento fornito nel messaggio di posta elettronica e configurare il sito per il primo utilizzo:

- Passare a `<YOUR-SITE-COLLECTION-URL>sites/<YOUR-SITE-NAME>/SitePages/CustomLearningAdmin.aspx`. L'apertura di **CustomLearningAdmin. aspx** consente di inizializzare l'elemento di elenco **CustomConfig** che consente di configurare i percorsi di apprendimento per il primo utilizzo. Dovrebbe essere visualizzata una pagina simile alla seguente:

![cg-adminapppage.png](media/cg-adminapppage.png)

## <a name="add-owners-to-site"></a>Aggiungere proprietari al sito
Come amministratore del tenant, è improbabile che tu sia la persona che Personalizza il sito, quindi dovrai assegnare alcuni proprietari al sito. I proprietari dispongono di privilegi amministrativi per il sito in modo che possano modificare le pagine del sito e rimarcare il sito. Sono inoltre in grado di nascondere e visualizzare contenuto e creare playlist e sottocategorie personalizzate.  

1. Scegliere **autorizzazioni sito**dal menu **Impostazioni** di SharePoint.
2. Fare clic su **Impostazioni avanzate di autorizzazione**.
3. Fare clic su **Microsoft 365 Learning pathways owners**.
4. Fare clic su **nuovo**  >  **Aggiungi utenti a questo gruppo**e quindi aggiungere le persone che si desidera siano proprietari. 
5. Aggiungere un collegamento per [esplorare il sito](custom_exploresite.md) nel messaggio di condivisione e quindi fare clic su **Condividi**.

## <a name="add-translators-to-the-site"></a>Aggiungere i traduttori al sito
I traduttori richiedono autorizzazioni per i membri o superiori nel sito. 

## <a name="choose-options-for-using-multiple-languages-on-the-site"></a>Scegliere le opzioni per l'utilizzo di più lingue nel sito
Il servizio di provisioning di SharePoint crea il sito percorsi di apprendimento in nove lingue. Vengono applicati i seguenti suggerimenti:
- Disattivare le lingue che non si desidera supportare
- Se non si supporta un sito in più lingue, disattivare la funzionalità multilingue. 

### <a name="remove-languages-you-dont-want-to-support"></a>Rimuovere le lingue che non si desidera supportare
Per le organizzazioni che scelgono di supportare una sola lingua, oltre alla lingua inglese predefinita, è consigliabile rimuovere le lingue che non sono supportate. 
1. Dal sito percorsi di apprendimento selezionare **Impostazioni** dall'alto a destra della pagina e quindi selezionare **informazioni sito**.
2. Nella parte inferiore del riquadro delle informazioni del sito selezionare **Visualizza tutte le impostazioni del sito**.
3. In **Amministrazione sito**selezionare **Impostazioni lingua**.
4. In **attiva pagine e notizie da tradurre in più lingue**, scorrere l'interruttore **su**attivato. Dovrebbe essere attiva per impostazione predefinita.
5. In Aggiungi o Rimuovi lingue sito fare clic su **Rimuovi** per rimuovere le lingue che non sono necessarie per il sito. Di seguito è riportato un esempio della pagina Impostazioni lingua per mostrare l'italiano supportato per il sito, oltre alla lingua inglese predefinita.

![custom_update_ml_langsettings.png](media/custom_update_ml_langsettings.png)

> [!NOTE]
> Quando si rimuovono le lingue, non è possibile rimuovere la lingua inglese predefinita. 

### <a name="assign-translators"></a>Assegnare i traduttori
Se si intende tradurre le pagine, facoltativamente assegnare uno o più traduttori per ogni lingua (eccetto la lingua predefinita del sito). 
- Nella colonna **Translator** , iniziare a digitare il nome di una persona che si desidera essere un traduttore, quindi selezionare il nome nell'elenco. 

> [!NOTE]
> Tutti gli utenti di Active Directory dell'organizzazione possono essere assegnati come traduttori. Alle persone assegnate come traduttori non verranno automaticamente concesse le autorizzazioni appropriate. Quando un utente che non dispone di autorizzazioni di modifica per un sito tenta di accedere al sito, verrà indirizzato a una pagina Web in cui è possibile richiedere l'accesso.

## <a name="turn-off-multilingual-support"></a>Disattiva supporto multilingue
Se non si desidera un sito multilingue, ad esempio si desidera un sito solo in lingua inglese, è consigliabile disattivare la funzionalità multilingue. 
- In **attiva pagine e notizie da tradurre**, selezionare **disattivata**. 

### <a name="add-languages"></a>Aggiungere le lingue
I percorsi di apprendimento supportano 9 lingue, ma è consigliabile aggiungere solo le lingue necessarie per il supporto per il sito percorsi di apprendimento. È possibile aggiungere lingue in qualsiasi momento. 
- In **Aggiungi o Rimuovi lingue sito**, iniziare a digitare un nome di lingua in **Seleziona o digitare una**lingua oppure scegliere una lingua dall'elenco a discesa. È possibile ripetere questo passaggio per aggiungere più lingue. È possibile aggiungere o rimuovere le lingue dal sito in qualsiasi momento tornando alla pagina.



