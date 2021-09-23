---
author: pkrebs
ms.author: pkrebs
title: Learning dei percorsi manuali per ml
ms.date: 02/10/2019
description: Learning percorsi manuali
ROBOTS: NOINDEX, NOFOLLOW
ms.service: sharepoint-online
manager: bpardi
ms.topic: article
ms.openlocfilehash: 89693e3020baa46f86b51b97c54240f12fec2d3a
ms.sourcegitcommit: a93cae8ea6e3c1141d7266d04131b69f2c2498cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/23/2021
ms.locfileid: "59485167"
---
# <a name="learning-pathways-manual-setup-for-multilingual"></a>Learning percorsi manuali per multilingue

Microsoft 365 percorsi di apprendimento offre una configurazione manuale per le organizzazioni che necessitano del supporto per uno degli scenari seguenti:

- L'organizzazione dispone di un SharePoint di comunicazione moderna online dedicato alla formazione e si desidera aggiungere percorsi di apprendimento a tale sito. In questo scenario, la web part percorsi di apprendimento non è stata impostata nel sito.

- Si desidera installare percorsi di apprendimento per il supporto multilingue in uno dei siti di comunicazione SharePoint dell'organizzazione. Il sito ha o avrà una lingua predefinita diversa dall'inglese ed è una delle lingue supportate dai percorsi di apprendimento. Ecco le lingue supportate dai percorsi di apprendimento:

- Inglese
- Cinese (semplificato)
- Francese
- Tedesco
- Italiano (Italia)
- Giapponese (Giappone)
- Portoghese (Brasile)
- Russo (russo)
- Spanish

La configurazione manuale dei percorsi di apprendimento richiede esperienza di Windows PowerShell e SharePoint Online Management Shell. Ecco una panoramica dei passaggi per la configurazione manuale dei percorsi di apprendimento: 

- Verificare di aver soddisfatto tutti i prerequisiti.
- Controllare le impostazioni di lingua predefinite per il sito. Se OK, continuare con l'installazione manuale. Se è necessaria un'impostazione di lingua predefinita diversa, è necessario creare un nuovo sito. 
- Installare il file customlearning.sppkg nel Catalogo app tenant SharePoint tenant.
- Effettuare il provisioning/identificare un sito di comunicazione moderno che agirà Microsoft 365 sito principale dei percorsi di apprendimento.
- Eseguire uno script di PowerShell che configurerà il tenant con gli artefatti da cui dipendono i percorsi di apprendimento.
- Passare alla pagina del sito CustomLearningAdmin.aspx per caricare la web part di amministrazione per inizializzare la configurazione del contenuto personalizzato.

## <a name="prerequisites"></a>Prerequisiti
Per garantire una corretta configurazione manuale della web part percorsi di apprendimento, è necessario che siano soddisfatti i prerequisiti seguenti. 

- È necessario aver configurato e configurato il Catalogo app a livello di tenant. Vedere [Configurare il tenant Office 365 e](/sharepoint/dev/spfx/set-up-your-developer-tenant#create-app-catalog-site) seguire la sezione "Creare il catalogo app". 
- Se il provisioning del Catalogo app a livello di tenant è già stato eseguito, è necessario accedere a un account che dispone dei diritti per caricare un pacchetto. In genere questo account ha un SharePoint amministratore. 
- Se un account con tale ruolo non funziona, passare all'interfaccia di amministrazione di SharePoint e individuare gli amministratori della raccolta siti del Catalogo app e accedere come uno degli amministratori della raccolta siti oppure aggiungere l'account di amministratore di SharePoint che non è riuscito ad Amministratori raccolta siti. 
- Sarà inoltre necessario accedere a un account che sia un SharePoint Tenant Admin.

## <a name="step-1---check-your-language-settings"></a>Passaggio 1 - Controllare le impostazioni della lingua
Come primo passaggio del processo di installazione manuale, controllare le impostazioni della lingua del sito. Ecco le opzioni possibili:

### <a name="option-1---you-dont-want-multilingual-support"></a>Opzione 1 - Non si desidera il supporto multilingue
Se non si desidera il supporto multilingue per il sito, verificare che sia disattivato.
1.  Nel sito SharePoint comunicazioni selezionare **Impostazioni** Informazioni sito  >    >  **Visualizza tutte le impostazioni del sito** Impostazioni  >  **lingua.** 
2.  Impostare **l'opzione Abilita la traduzione di pagine** e notizie in più lingue su **Disattivato.**
3.  Fare clic su **Salva**. 
4.  Continuare con il passaggio 2.

## <a name="option-2---you-want-multilingual-support-and-youre-ok-with-the-default-language"></a>Opzione 2 - Si desidera il supporto multilingue e si sta bene con la lingua predefinita
Un SharePoint di comunicazione ha una lingua predefinita. La lingua predefinita determina la lingua in cui si visualizzano i percorsi di apprendimento, inclusa la pagina Di amministrazione dei percorsi di apprendimento. L'impostazione predefinita della lingua viene impostata quando il sito viene creato per la prima volta e non può essere modificato in seguito. Prima di continuare con la configurazione manuale, assicurati di avere la lingua predefinita del sito di destinazione.

1.  Nel sito SharePoint comunicazioni selezionare **Impostazioni** Informazioni sito  >    >  **Visualizza tutte le impostazioni del sito** Impostazioni  >  **lingua.** 
2.  Impostare **l'opzione Abilita la traduzione** di pagine e notizie in più lingue su **Attivato.**
    - Se si sta bene con la lingua visualizzata all'inizio dell'elenco in **Lingua**, è possibile aggiungere altre lingue e quindi fare clic su **Salva**. Continuare con il passaggio 2.
    - Se si desidera una lingua predefinita diversa da quella selezionata per il sito, sarà necessario creare un nuovo sito di SharePoint Communication con la lingua desiderata. Passare all'opzione 3. 

## <a name="option-3---you-want-multilingual-support-but-want-a-different-default-language-for-the-site"></a>Opzione #3 - Si desidera il supporto multilingue ma si desidera una lingua predefinita diversa per il sito
Con questa opzione, si crea un nuovo SharePoint di comunicazione online con la lingua predefinita desiderata e quindi si impostano le impostazioni della lingua per il sito. 
1.  Per creare un nuovo sito SharePoint comunicazione, vedere [Create a communication site in SharePoint Online](https://support.microsoft.com/office/create-a-communication-site-in-sharepoint-online-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb). Quando crei il sito, assicurati di impostare la lingua predefinita per i percorsi di apprendimento. 
2. Dal sito creato, selezionare Impostazioni Informazioni sito Visualizza tutte le impostazioni  >    >  **del sito**  >  **Impostazioni lingua.** 
2.  Impostare **l'opzione Abilita la traduzione** di pagine e notizie in più lingue su **Attivato.**
3. Aggiungere altre lingue, se necessario, e quindi fare clic su **Salva.** 
4. Continuare con il passaggio 2. 

>! [Nota] Se è necessario eseguire la migrazione di contenuto personalizzato da un sito a un sito appena creato, vedere la sezione "Eseguire la migrazione del contenuto personalizzato" più avanti in questo documento. 

## <a name="step-2---get-the-web-part-package-and-setup-script-from-github"></a>Passaggio 2: ottenere il pacchetto web part e lo script di installazione da GitHub
Come parte del processo di installazione, è necessario il pacchetto web part Microsoft 365 percorsi di apprendimento e lo script di installazione di PowerShell.

- Passare ai [percorsi di apprendimento GitHub Repository](https://github.com/pnp/custom-learning-office-365).
- Fare **clic su** Download per salvare il pacchetto web part e lo script in un'unità locale. Nei passaggi successivi di questo processo verrà utilizzato lo script e il pacchetto della web part.

## <a name="step-2---upload-the-web-part-to-the-tenant-app-catalog"></a>Passaggio 2 : Upload la web part nel Catalogo app tenant
Per configurare Microsoft 365 percorsi di apprendimento, devi caricare il file customlearning.sppkg nel Catalogo app a livello di tenant e distribuirlo. Vedi [Usare il Catalogo app](/sharepoint/use-app-catalog) per rendere disponibili app aziendali personalizzate per l'ambiente SharePoint Online per istruzioni dettagliate su come aggiungere un'app al Catalogo app.

## <a name="step-3---provisionidentify-a-modern-communication-site"></a>Passaggio 3 - Provisioning/identificazione di un sito di comunicazione moderno
Identificare un sito di SharePoint esistente o eseguirne il provisioning nel tenant di SharePoint Online. Per ulteriori informazioni su come eseguire il provisioning di un sito di comunicazione, vedere [Create a communication site in SharePoint Online](https://support.office.com/article/create-a-communication-site-in-sharepoint-online-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb) e seguire la procedura per creare un sito di comunicazione.

## <a name="step-4---add-the-microsoft-365-learning-pathways-app-to-the-site"></a>Passaggio 4 - Aggiungere l'app Microsoft 365 percorsi di apprendimento al sito

1. Nel sito SharePoint, fai clic sul menu Sistema, quindi fai clic **su Aggiungi un'app.** 
2. In **App fare** clic su **Dall'organizzazione** e quindi su Percorsi di apprendimento **per Office 365**. 

## <a name="step-5---set-permissions-for-the-site"></a>Passaggio 5 - Impostare le autorizzazioni per il sito
Verificare che per il sito siano impostate le autorizzazioni seguenti:
- **Amministratore raccolta siti o parte del** gruppo Proprietari - Autorizzazioni necessarie per inizializzare la voce di elenco CustomConfig che configura i percorsi di apprendimento per il primo utilizzo. 
- **Gruppo Membri** - Autorizzazioni necessarie per amministrare i percorsi di apprendimento, tra cui nascondere e visualizzare il contenuto e amministrare playlist personalizzate
- **Gruppo Visitatori** - Autorizzazioni necessarie per visualizzare il contenuto del sito. 

## <a name="step-6--execute-powershell-configuration-script"></a>Passaggio 6- Eseguire lo script di configurazione di PowerShell
È incluso uno script di PowerShell che sarà necessario eseguire per creare tre proprietà `CustomLearningConfiguration.ps1` [tenant](/sharepoint/dev/spfx/tenant-properties) utilizzate dalla soluzione. Inoltre, lo script crea due pagine dell'app a [parte singola](/sharepoint/dev/spfx/web-parts/single-part-app-pages) nella raccolta pagine del sito per ospitare le web part amministratore e utente in un percorso noto.

1. Se non hai già scaricato la SharePoint Online Management Shell, scaricala ora. Vedere [SharePoint Online Management Shell Download](https://go.microsoft.com/fwlink/p/?LinkId=255251).
2. Potrebbe essere necessario impostare un criterio di esecuzione di PowerShell per eseguire lo script. Per ulteriori informazioni, vedere [About Execution Policies.](/powershell/module/microsoft.powershell.core/about/about_execution_policies)
3. Eseguire lo `CustomLearningConfiguration.ps1` script. Oltre alle credenziali di amministratore tenant, lo script richiederà il nome del tenant e il nome del sito. Considerando l'esempio seguente per l'URL del sito, `https://contoso.sharepoint.com/sites/O365CL` , è il nome del tenant e il nome del `contoso` `O365CL` sito. 

### <a name="disabling-telemetry-collection"></a>Disabilitazione della raccolta di telemetria
Parte di questa soluzione include il consenso esplicito per il rilevamento della telemetria anonimizzato, che per impostazione predefinita è impostato su on. Se si esegue un'installazione manuale e si desidera disattivare il rilevamento della telemetria, modificare lo script per impostare la variabile $optInTelemetry su $false ed `CustomlearningConfiguration.ps1` eseguire lo script.

## <a name="validate-provisioning-success-and-initialize-the-customconfig-list"></a>Convalidare il provisioning con esito positivo e inizializzare l'elenco CustomConfig

Dopo la corretta esecuzione dello script di PowerShell, passare al sito, inizializzare la voce di elenco **CustomConfig** che configura i percorsi di apprendimento per il primo utilizzo e verificare che il sito funzioni.

- Vai a `<YOUR-SITE-COLLECTION-URL>/SitePages/CustomLearningAdmin.aspx`. Aprendo **CustomLearningAdmin.aspx** inizializza la voce di elenco **CustomConfig** che configura i percorsi di apprendimento per il primo utilizzo. Dovrebbe essere visualizzata una pagina simile alla seguente:

![Impostazioni dell'app page.png](media/cg-adminapppage.png)

## <a name="add-owners-to-site"></a>Aggiungere proprietari al sito
In quanto amministratore tenant, è improbabile che tu sia la persona che personalizza il sito, quindi dovrai assegnare alcuni proprietari al sito. I proprietari dispongono di privilegi amministrativi per il sito in modo che possano modificare le pagine del sito e rebrand il sito. Hanno anche la possibilità di nascondere e mostrare il contenuto fornito tramite la web part percorsi di apprendimento. Inoltre, hanno la possibilità di creare playlist personalizzate e assegnarle a sottocategorie personalizzate.  

1. Scegliere Autorizzazioni sito **dal** menu SharePoint Impostazioni **sito.**
2. Fare **clic su Autorizzazioni avanzate Impostazioni**.
3. Fare **clic su Percorsi di apprendimento per Office 365 proprietari**.
4. Fare **clic** su Nuovo Aggiungi utenti a questo gruppo e quindi aggiungere le  >  persone che si desidera siano proprietari. 
5. Aggiungere un collegamento a [Esplora sito](custom_exploresite.md) nel messaggio Condividi e quindi fare clic su **Condividi.**

## <a name="migrate-custom-content"></a>Eseguire la migrazione del contenuto personalizzato
Dopo aver ristabilito il sito dei percorsi di apprendimento seguendo i passaggi precedenti, dovrai spostare il contenuto dell'elenco **CustomPlaylists** e **dell'elenco CustomAssets.** Facoltativamente, puoi anche spostare le pagine personalizzate effettive che costituiscono gli asset personalizzati se si trova nel sito dei percorsi di apprendimento esistenti e l'intento è eliminarlo. L'attività può essere difficile perché per tutti gli elementi nell'elenco **CustomPlaylists,** l'ID della voce di elenco **nell'elenco CustomAssets** viene nascosto nel campo JSONData di ogni elemento dell'elenco di playlist. Pertanto, non sarà sufficiente spostare semplicemente il contenuto dell'elenco **CustomPlaylists** da un sito all'altro. Inoltre, **l'elenco CustomAssets** contiene l'URL assoluto della pagina dell'asset personalizzato nel campo JSONData dell'elemento di elenco. Se le risorse non vengono spostate e il sito non viene rinominato (modificando così l'URL assoluto nella pagina dell'asset), **CustomAssets** può rimanere. Sarà tuttavia necessario correggere manualmente le voci. Data la complessità di questo tipo di migrazione, ti consigliamo di prendere in considerazione l'integrazione di uno dei nostri partner dei percorsi di apprendimento per aiutarti a eseguire questa transizione. 

### <a name="next-steps"></a>Operazioni successive
- Vedi [Personalizzare i percorsi di apprendimento.](custom_overview.md) 
- Vedere [Tradurre le pagine del sito.](custom_translate_page_ml.md)