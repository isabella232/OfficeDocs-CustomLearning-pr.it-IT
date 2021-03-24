---
author: pkrebs
ms.author: pkrebs
title: Effettuare il provisioning di una nuova soluzione di percorsi di apprendimento
ms.date: 02/10/2019
description: Effettuare il provisioning del sito dei percorsi di apprendimento di Microsoft 365 con il servizio look book di Microsoft 365
ms.service: sharepoint online
ms.openlocfilehash: fd50eed38ea6f2073eb61b4d21545a73bc918a49
ms.sourcegitcommit: 907c657e7cc5a4a44d2b9f38cc35fea9ac5c5943
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2021
ms.locfileid: "51162913"
---
# <a name="provision-a-new-learning-pathways-solution"></a>Effettuare il provisioning di una nuova soluzione di percorsi di apprendimento 
Le organizzazioni che non dispongono di percorsi di apprendimento di cui è stato eseguito il provisioning nel tenant possono utilizzare il servizio look book di SharePoint per aggiungere la soluzione di percorsi di apprendimento multilingue. Con questa opzione, il modello di SharePoint percorsi di apprendimento viene tradotto in nove lingue e può essere utilizzato con un minimo di modifica. 

> [!IMPORTANT]
> Se si dispone già di percorsi di apprendimento di cui è stato eseguito il provisioning nel tenant, è consigliabile [aggiornare i](custom_update.md) percorsi di apprendimento. Se si installa una nuova istanza dei percorsi di apprendimento, sarà necessario trasferire manualmente eventuali personalizzazioni dal sito esistente al nuovo sito. 

## <a name="prerequisites-for-multilingual-support"></a>Prerequisiti per il supporto multilingue
 
Per configurare correttamente i percorsi di apprendimento di Microsoft 365 con il servizio look book, la persona che effettua il provisioning deve soddisfare i prerequisiti seguenti:   
 
- La persona che effettua il provisioning dei percorsi di apprendimento deve essere un amministratore tenant del tenant in cui verrà eseguito il provisioning dei percorsi di apprendimento.  
- Un Catalogo app tenant deve essere disponibile nell'opzione App dell'interfaccia di amministrazione di SharePoint. Se l'organizzazione non dispone di un Catalogo app tenant di SharePoint, fare riferimento alla documentazione [di SharePoint Online](/sharepoint/use-app-catalog) per crearne uno. Devi attendere almeno due ore dopo aver creato il Catalogo app prima di eseguire il provisioning dei percorsi di apprendimento.  
- I percorsi di apprendimento di provisioning della persona devono essere proprietari della raccolta siti del Catalogo app tenant. Se la persona che provisioning percorsi di apprendimento non è un proprietario della raccolta siti del Catalogo app, [completare queste istruzioni](addappadmin.md) e continuare. 

## <a name="ensure-the-tenant-admin-account-doesnt-have-a-language-selected"></a>Verificare che l'account amministratore tenant non abbia una lingua selezionata
Prima di effettuare il provisioning dei percorsi di apprendimento, assicurati che l'account amministratore per il tenant non abbia una lingua selezionata. Ecco come verificare se l'account amministratore non ha una lingua selezionata. 
1.  Con il profilo di amministratore edge, passare a office.com.
2.  Immettere le credenziali utente (se necessario).
3.  In Microsoft 365, fare clic **su Tutte le app** > Delve. 
4.  Fare **clic su Aggiorna**  >  **profilo**.
5.  Scorrere la pagina verso il basso e fare **clic su Come modificare le impostazioni internazionali e della lingua.**
6.  Fare **clic qui** e quindi fare clic sui puntini di sospensione **...**.
7.  In **Lingue di visualizzazione** utente dovrebbe essere visualizzata **l'opzione Nessuna lingua selezionata.** Se è selezionata una lingua, deselezionarla.

### <a name="to-provision-learning-pathways"></a>Per effettuare il provisioning dei percorsi di apprendimento

1. Passare alla pagina della soluzione percorsi di apprendimento [di Microsoft 365](https://lookbook.microsoft.com/details/3df8bd55-b872-4c9d-88e3-6b2f05344239).
2. Fare **clic su Aggiungi al tenant.** Se non è stato eseguito l'accesso al tenant, il servizio di provisioning richiederà le credenziali di amministratore tenant. 
3. Nella finestra di dialogo Autorizzazioni richieste selezionare **Consenso per conto dell'organizzazione** e quindi selezionare **Accetta.**

Il servizio look book richiede queste autorizzazioni per creare il Catalogo app tenant, installare l'applicazione nel Catalogo app tenant ed eseguire il provisioning del modello di sito. Non c'è alcun impatto complessivo sul tenant. Queste autorizzazioni vengono utilizzate in modo esplicito ai fini dell'installazione della soluzione. Per continuare con l'installazione, è necessario accettare queste autorizzazioni.

4. Completare i campi nella pagina delle informazioni sul provisioning, come opportuno per l'installazione. Digitare almeno l'indirizzo e-mail in cui si vogliono ricevere le notifiche relative al processo di provisioning e l’URL di destinazione del sito in cui deve essere eseguito il provisioning.  
> [!NOTE]
> Impostare l’URL di destinazione in una maniera semplice per i tuoi dipendenti, come “/sites/MyTraining” o “/teams/LearnMicrosoft365”.

![inst_options.png](media/inst_options.png)

6. Fare **clic su Provisioning** quando si è pronti per installare i percorsi di apprendimento nell'ambiente tenant.  Il processo di provisioning può richiedere fino a 15 minuti. Quando il sito è pronto, si riceverà una notifica via e-mail. 

> [!IMPORTANT]
> L'amministratore tenant che esegue il provisioning del sito dei percorsi di apprendimento deve accedere al sito e quindi aprire **CustomLearningAdmin.aspx** per inizializzare i percorsi di apprendimento Proprietà dell'amministratore. In questo momento, l'amministratore tenant deve anche assegnare proprietari al sito. 

## <a name="validate-provisioning-success-and-initialize-the-customconfig-list"></a>Convalidare il provisioning con esito positivo e inizializzare l'elenco CustomConfig

Al termine del provisioning, l'amministratore tenant che ha effettuato il provisioning del sito riceve un messaggio di posta elettronica dal servizio look book. Il messaggio di posta elettronica contiene un collegamento al sito. A questo punto, l'amministratore tenant deve accedere al sito usando il collegamento fornito nel messaggio di posta elettronica e configurare il sito per il primo utilizzo:

- Passare a `<YOUR-SITE-COLLECTION-URL>sites/<YOUR-SITE-NAME>/SitePages/CustomLearningAdmin.aspx`. Aprendo **CustomLearningAdmin.aspx** inizializza la voce di elenco **CustomConfig** che configura i percorsi di apprendimento per il primo utilizzo. Dovrebbe essere visualizzata una pagina simile alla seguente:

![cg-adminapppage.png](media/cg-adminapppage.png)

## <a name="add-owners-to-site"></a>Aggiungere proprietari al sito
In quanto amministratore tenant, è improbabile che tu sia la persona che personalizza il sito, quindi dovrai assegnare alcuni proprietari al sito. I proprietari dispongono di privilegi amministrativi per il sito in modo che possano modificare le pagine del sito e rebrand il sito. Hanno anche la possibilità di nascondere e mostrare il contenuto e creare playlist e sottocategorie personalizzate.  

1. Scegliere Autorizzazioni sito **dal** menu Impostazioni di SharePoint. 
2. Fare clic **su Impostazioni di autorizzazione avanzate**.
3. Fare **clic su Microsoft 365 learning pathways Owners**.
4. Fare **clic** su Nuovo Aggiungi utenti a questo gruppo e quindi aggiungere le  >  persone che si desidera siano proprietari. 
5. Aggiungere un collegamento a [Esplora sito](custom_exploresite.md) nel messaggio Condividi e quindi fare clic su **Condividi.**

## <a name="add-translators-to-the-site"></a>Aggiungere traduttori al sito
Se si utilizzano traduttori per il sito, è possibile assegnare loro le autorizzazioni. I traduttori richiedono autorizzazioni membro o superiori. 

## <a name="choose-options-for-using-multiple-languages-on-the-site"></a>Scegliere le opzioni per l'utilizzo di più lingue nel sito
Il servizio look book di SharePoint crea il sito Percorsi di apprendimento in nove lingue. Si applicano le raccomandazioni seguenti:
- Disattivare le lingue che non si desidera supportare
- Se non si supporta un sito multilingue, disattivare la funzionalità multilingue. Vedere la sezione "Disattivare il supporto multilingue" più avanti in questo argomento.

### <a name="remove-languages-you-dont-want-to-support"></a>Rimuovere le lingue che non si desidera supportare
Per le organizzazioni che scelgono di supportare una sola lingua, oltre alla lingua inglese predefinita, è consigliabile rimuovere le lingue non supportate. 
1. Nel sito Percorsi di apprendimento selezionare **Impostazioni** nell'angolo in alto a destra della pagina e quindi selezionare **Informazioni sito.**
2. Nella parte inferiore del riquadro informazioni sito selezionare **Visualizza tutte le impostazioni del sito.**
3. In **Amministrazione sito** selezionare Impostazioni **lingua.**
4. In **Abilita la traduzione di pagine e notizie in più lingue,** fai scorrere l'interruttore su **Attivato.** Dovrebbe essere on per impostazione predefinita.
5. In Aggiungi o rimuovi lingue sito fare clic **su Rimuovi** per rimuovere le lingue non necessarie per il sito. Di seguito viene illustrato un esempio della pagina Impostazioni lingua per visualizzare l'italiano supportato per il sito, oltre alla lingua inglese predefinita.

![custom_update_ml_langsettings.png](media/custom_update_ml_langsettings.png)

> [!NOTE]
> Durante la rimozione delle lingue non è possibile rimuovere la lingua inglese predefinita. 

### <a name="assign-translators"></a>Assegnare traduttori
Se vuoi tradurre le pagine, assegna facoltativamente uno o più traduttori per ogni lingua (ad eccezione della lingua predefinita del sito). 
- Nella colonna **Translator** iniziare a digitare il nome di una persona che si desidera convertire e quindi selezionare il nome dall'elenco. 

> [!NOTE]
> Tutti gli utenti di Active Directory dell'organizzazione possono essere assegnati come traduttori. Le persone assegnate come traduttori non riceveranno automaticamente le autorizzazioni appropriate. Quando un utente senza autorizzazioni di modifica per un sito tenta di accedere al sito, verrà indirizzato a una pagina Web in cui può richiedere l'accesso.

## <a name="turn-off-multilingual-support"></a>Disattivare il supporto multilingue
Se ad esempio non si desidera un sito multilingue, è consigliabile disattivare la caratteristica multilingue. 

1. Nel sito Percorsi di apprendimento selezionare **Impostazioni** nell'angolo in alto a destra della pagina e quindi selezionare **Informazioni sito.**
2. Nella parte inferiore del riquadro informazioni sito selezionare **Visualizza tutte le impostazioni del sito.**
3. In **Amministrazione sito** selezionare Impostazioni **lingua.**
4. In **Abilita la traduzione di pagine e notizie in più lingue,** fai scorrere l'interruttore su **Attivato.** Dovrebbe essere on per impostazione predefinita.
- In **Abilita la traduzione di pagine e notizie** selezionare **Disattivato.** 

### <a name="add-languages"></a>Aggiungere le lingue
I percorsi di apprendimento supportano 9 lingue, ma è consigliabile aggiungere solo le lingue necessarie per il sito dei percorsi di apprendimento. Puoi aggiungere langauges in qualsiasi momento. 
- In **Aggiungere o rimuovere lingue del sito** iniziare a digitare un nome di lingua in **Selezionare** o digitare una lingua oppure scegliere una lingua nell'elenco a discesa. È possibile ripetere questo passaggio per aggiungere più lingue. È possibile aggiungere o rimuovere lingue dal sito in qualsiasi momento tornando a questa pagina.