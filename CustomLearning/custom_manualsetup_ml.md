---
author: pkrebs
ms.author: pkrebs
title: Percorsi di apprendimento installazione manuale per ml
ms.date: 02/10/2019
description: Percorsi di apprendimento installazione manuale
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 44bd47f0a49634a2f6ac6aca2d221fb8e6f15980
ms.sourcegitcommit: ba0cddd12dd8687ec4b97c26174fdda09de83b05
ms.translationtype: Auto
ms.contentlocale: it-IT
ms.lasthandoff: 07/06/2020
ms.locfileid: "45043278"
---
# <a name="learning-pathways-manual-setup-for-multilingual"></a>Percorsi di apprendimento configurazione manuale per la lingua multilingue

Microsoft 365 Learning pathways offre una configurazione manuale per le organizzazioni che necessitano del supporto per uno degli scenari seguenti:

- L'organizzazione dispone di un sito di comunicazione moderno di SharePoint Online definito dedicato all'allenamento e si desidera aggiungere percorsi di apprendimento a tale sito. In questo scenario, la Web part percorsi di apprendimento non è stata configurata nel sito.

- Si desidera installare percorsi di apprendimento per il supporto multilingue in uno dei siti di comunicazione di SharePoint dell'organizzazione. Il sito ha o avrà una lingua predefinita che non è l'inglese ed è una delle lingue supportate da percorsi di apprendimento. Di seguito sono ritratte le lingue supportate dai percorsi di apprendimento:

- English
- Cinese (semplificato)
- Francese
- Tedesco
- Italiano (Italia)
- Giapponese (Giappone)
- Portoghese (Brasile)
- Russo (Russo)
- Spanish

La configurazione manuale dei percorsi di apprendimento richiede un'esperienza di utilizzo di Windows PowerShell e di SharePoint Online Management Shell. Di seguito è riportata una panoramica dei passaggi per la configurazione manuale dei percorsi di apprendimento: 

- Verificare che siano stati soddisfatti tutti i prerequisiti.
- Controllare le impostazioni della lingua predefinite per il sito. Se si va bene, continuare con l'installazione manuale. Se è necessaria un'impostazione della lingua predefinita diversa, è necessario creare un nuovo sito. 
- Installare il file customlearning. sppkg nel catalogo delle app tenant di SharePoint.
- Provisioning/identificare un sito di comunicazione moderno che funga da Microsoft 365 Learning pathways Home site.
- Eseguire uno script di PowerShell che configurerà il tenant con gli elementi in base ai quali i percorsi di apprendimento dipendono.
- Passare alla pagina del sito CustomLearningAdmin. aspx per caricare la Web part amministratore per inizializzare la configurazione del contenuto personalizzato.

## <a name="prerequisites"></a>Prerequisiti
Per garantire una corretta configurazione manuale della web part percorsi di apprendimento, è necessario che vengano soddisfatti i prerequisiti seguenti. 

- È necessario configurare e configurare il catalogo app a livello di tenant. Per ulteriori informazioni, vedere [configurare il tenant di Office 365](https://docs.microsoft.com/sharepoint/dev/spfx/set-up-your-developer-tenant#create-app-catalog-site) e seguire la sezione "creare Catalogo app". 
- Se è già stato effettuato il provisioning del catalogo app a livello di tenant, è necessario accedere a un account che disponga dei diritti di caricamento di un pacchetto. In genere, questo account ha un ruolo di amministratore di SharePoint. 
- Se un account con quel ruolo non funziona, passare all'interfaccia di amministrazione di SharePoint e individuare gli amministratori della raccolta siti per la raccolta siti Catalogo app e accedere come uno degli amministratori della raccolta siti oppure aggiungere l'account di amministratore di SharePoint che non è riuscito agli amministratori della raccolta siti. 
- È inoltre necessario accedere a un account che sia un amministratore tenant di SharePoint.

## <a name="step-1---check-your-language-settings"></a>Passaggio 1-controllare le impostazioni della lingua
Come primo passaggio del processo di installazione manuale, controllare le impostazioni della lingua del sito. Di seguito sono elencate le opzioni possibili:

### <a name="option-1---you-dont-want-multilingual-support"></a>Opzione 1: non si desidera un supporto multilingue
Se non si desidera un supporto multilingue per il sito, assicurarsi che sia disattivata.
1.  Dal sito di comunicazione di SharePoint, selezionare **Impostazioni**  >  **sito informazioni**  >  **Visualizza tutte**le  >  **impostazioni della lingua**delle impostazioni del sito. 
2.  Impostare le **pagine e le notizie di abilitazione da tradurre in più lingue** passare a **disattivata**.
3.  Fare clic su **Salva**. 
4.  Continuare con il passaggio 2.

## <a name="option-2---you-want-multilingual-support-and-youre-ok-with-the-default-language"></a>Opzione 2: si desidera un supporto multilingue e si sta bene con la lingua predefinita
Un sito di comunicazione di SharePoint dispone di una lingua predefinita. La lingua predefinita determina la lingua in cui si visualizzano i percorsi di apprendimento, inclusa la pagina Amministrazione percorsi di apprendimento. L'impostazione della lingua predefinita è impostata quando il sito viene creato per la prima volta e non può essere modificato in seguito. Prima di continuare con la configurazione manuale, accertarsi di essere a posto con la lingua predefinita del sito di destinazione.

1.  Dal sito di comunicazione di SharePoint, selezionare **Impostazioni**  >  **sito informazioni**  >  **Visualizza tutte**le  >  **impostazioni della lingua**delle impostazioni del sito. 
2.  Impostare le **pagine e le notizie che verranno convertite in più lingue** passare **a attivato.**
    - Se si sta bene con la lingua visualizzata nella parte superiore dell'elenco in **lingua**, è possibile aggiungere altre lingue e quindi fare clic su **Salva**. Continuare con il passaggio 2.
    - Se si desidera una lingua predefinita diversa da quella selezionata per il sito, è necessario creare un nuovo sito di comunicazione di SharePoint con la lingua desiderata. Continuare con l'opzione 3. 

## <a name="option-3---you-want-multilingual-support-but-want-a-different-default-language-for-the-site"></a>Opzione #3-si desidera un supporto multilingue ma si desidera una lingua predefinita diversa per il sito
Con questa opzione, si crea un nuovo sito di comunicazione di SharePoint Online con la lingua predefinita desiderata e quindi si impostano le impostazioni della lingua per il sito. 
1.  Per creare un nuovo sito di comunicazione di SharePoint, vedere [creare un sito di comunicazione in SharePoint Online](https://support.microsoft.com/office/create-a-communication-site-in-sharepoint-online-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb). Quando si crea il sito, assicurarsi di impostare la lingua per la lingua predefinita desiderata per i percorsi di apprendimento. 
2. Dal sito creato, selezionare **Impostazioni**  >  **sito informazioni**  >  **Visualizza tutte**le  >  **impostazioni della lingua**delle impostazioni del sito. 
2.  Impostare le **pagine e le notizie che verranno convertite in più lingue** passare **a attivato.**
3. Aggiungere altre lingue, se necessario, e quindi fare clic su **Salva**. 
4. Continuare con il passaggio 2. 

>! Nota Se è necessario eseguire la migrazione di contenuto personalizzato da un sito a un sito appena creato, vedere la sezione "eseguire la migrazione di contenuto personalizzato" più avanti in questo documento. 

## <a name="step-2---get-the-web-part-package-and-setup-script-from-github"></a>Passaggio 2: ottenere il pacchetto Web part e lo script di installazione da GitHub
Come parte del processo di installazione, è necessario il pacchetto della web part di Microsoft 365 Learning pathways e lo script di installazione di PowerShell.

- Go the [Learning pathways GitHub repository](https://github.com/pnp/custom-learning-office-365).
- Fare clic su **download** per salvare il pacchetto della web part e lo script su un'unità locale. Si utilizzerà lo script e il pacchetto Web part nei passaggi successivi di questo processo.

## <a name="step-2---upload-the-web-part-to-the-tenant-app-catalog"></a>Passaggio 2: caricare la Web part nel catalogo app tenant
Per configurare i percorsi di apprendimento di Microsoft 365, caricare il file customlearning. sppkg nel catalogo app a livello di tenant e distribuirlo. Per informazioni dettagliate su come aggiungere un'app al catalogo app, vedere [utilizzare il catalogo app per rendere disponibili le app aziendali personalizzate per l'ambiente di SharePoint Online](https://docs.microsoft.com/sharepoint/use-app-catalog) .

## <a name="step-3---provisionidentify-a-modern-communication-site"></a>Passaggio 3-provisioning/identificare un sito di comunicazione moderno
Identificare un sito di comunicazione di SharePoint esistente o provisionare uno nuovo nel tenant di SharePoint Online. Per ulteriori informazioni su come eseguire il provisioning di un sito di comunicazione, vedere [creare un sito di comunicazione in SharePoint Online](https://support.office.com/en-us/article/create-a-communication-site-in-sharepoint-online-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb) e seguire la procedura per creare un sito di comunicazione.

## <a name="step-4---add-the-microsoft-365-learning-pathways-app-to-the-site"></a>Passaggio 4: aggiungere l'app percorsi di apprendimento di Microsoft 365 al sito

1. Dal sito di SharePoint, fare clic sul menu System, quindi fare clic su **Aggiungi un'app**. 
2. Nelle **app**fare clic **dall'organizzazione**e quindi fare clic su **percorsi di apprendimento per Office 365**. 

## <a name="step-5---set-permissions-for-the-site"></a>Passaggio 5: impostare le autorizzazioni per il sito
Verificare che siano impostate le autorizzazioni seguenti per il sito:
- **Amministratore della raccolta siti o parte del gruppo proprietari** -autorizzazioni necessarie per inizializzare l'elemento dell'elenco di CustomConfig che consente di configurare i percorsi di apprendimento per il primo utilizzo. 
- **Gruppo membri** -autorizzazioni necessarie per l'amministrazione di percorsi di apprendimento, tra cui il contenuto e la visualizzazione di contenuti e l'amministrazione di elenchi di riproduzione personalizzati
- **Gruppo visitatori** -autorizzazioni necessarie per visualizzare il contenuto del sito. 

## <a name="step-6--execute-powershell-configuration-script"></a>Passaggio 6-eseguire lo script di configurazione di PowerShell
È incluso uno script di PowerShell `CustomLearningConfiguration.ps1` che sarà necessario eseguire per creare tre [Proprietà tenant](https://docs.microsoft.com/sharepoint/dev/spfx/tenant-properties) utilizzate dalla soluzione. Lo script consente inoltre di creare due [pagine dell'applicazione di una singola parte](https://docs.microsoft.com/sharepoint/dev/spfx/web-parts/single-part-app-pages) nella raccolta pagine del sito per ospitare l'amministratore e le web part dell'utente in una posizione nota.

1. Se non è stato ancora scaricato SharePoint Online Management Shell, scaricarlo subito. Vedere [download di SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).
2. Potrebbe essere necessario impostare un criterio di esecuzione di PowerShell per eseguire lo script. Per ulteriori informazioni, vedere [informazioni sui criteri di esecuzione](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-6).
3. Eseguire lo `CustomLearningConfiguration.ps1` script. Oltre alle credenziali di amministratore tenant, lo script richiederà il nome del tenant e il nome del sito. Considerando l'esempio seguente relativo all'URL del sito `https://contoso.sharepoint.com/sites/O365CL` , `contoso` è il nome del tenant ed `O365CL` è il nome del sito. 

### <a name="disabling-telemetry-collection"></a>Disabilitazione della raccolta di telemetria
Parte di questa soluzione include la verifica della telemetria di anonimi opt-in, che per impostazione predefinita è impostata su attivato. Se si sta eseguendo un'installazione manuale e si desidera disattivare la verifica della telemetria, cambiare lo `CustomlearningConfiguration.ps1` script per impostare la variabile $optInTelemetry su $false ed eseguire lo script.

## <a name="validate-provisioning-success-and-initialize-the-customconfig-list"></a>Convalidare il provisioning di esito positivo e inizializzare l'elenco CustomConfig

Dopo che lo script di PowerShell è stato eseguito correttamente, passare al sito, inizializzare l'elemento dell'elenco **CustomConfig** che configura i percorsi di apprendimento per il primo utilizzo e convalidare il funzionamento del sito.

- Passare a `<YOUR-SITE-COLLECTION-URL>/SitePages/CustomLearningAdmin.aspx`. L'apertura di **CustomLearningAdmin. aspx** consente di inizializzare l'elemento di elenco **CustomConfig** che consente di configurare i percorsi di apprendimento per il primo utilizzo. Dovrebbe essere visualizzata una pagina simile alla seguente:

![cg-adminapppage.png](media/cg-adminapppage.png)

## <a name="add-owners-to-site"></a>Aggiungere proprietari al sito
Come amministratore del tenant, è improbabile che tu sia la persona che Personalizza il sito, quindi dovrai assegnare alcuni proprietari al sito. I proprietari dispongono di privilegi amministrativi per il sito in modo che possano modificare le pagine del sito e rimarcare il sito. Sono inoltre in grado di nascondere e visualizzare i contenuti forniti tramite la Web part percorsi di apprendimento. Inoltre, avranno la possibilità di creare playlist personalizzate e assegnarle a sottocategorie personalizzate.  

1. Scegliere **autorizzazioni sito**dal menu **Impostazioni** di SharePoint.
2. Fare clic su **Impostazioni avanzate di autorizzazione**.
3. Fare clic su **percorsi di apprendimento per i proprietari di Office 365**.
4. Fare clic su **nuovo**  >  **Aggiungi utenti a questo gruppo**e quindi aggiungere le persone che si desidera siano proprietari. 
5. Aggiungere un collegamento per [esplorare il sito](https://docs.microsoft.com/Office365/CustomLearning/custom_explore) nel messaggio di condivisione e quindi fare clic su **Condividi**.

## <a name="migrate-custom-content"></a>Eseguire la migrazione di contenuto personalizzato
Dopo aver ristabilito il sito dei percorsi di apprendimento seguendo la procedura descritta in alto, è necessario spostare i contenuti dell'elenco di **CustomPlaylists** e dell'elenco di **CustomAssets** . È anche possibile, facoltativamente, spostare le pagine personalizzate effettive che compongono le risorse personalizzate se sono presenti nel sito percorsi di apprendimento esistente e l'intenzione è di eliminarla. L'attività può essere difficile perché per tutti gli elementi nell'elenco **CustomPlaylists** , l'ID della voce di elenco nell'elenco **CustomAssets** è sepolto nel campo JSONData di ogni voce di elenco di playlist. Pertanto, semplicemente spostando il contenuto dell'elenco **CustomPlaylists** da un sito all'altro non sarà sufficiente. Inoltre, l'elenco **CustomAssets** contiene l'URL assoluto della pagina del cespite personalizzato nel campo JSONData della voce di elenco. Se le risorse non vengono spostate e il sito non viene rinominato (cambiando così l'URL assoluto della pagina del cespite), **CustomAssets** può rimanere. Tuttavia, sarà necessario correggere manualmente le voci. Data la complessità di questo tipo di migrazione, è consigliabile prendere in considerazione l'arruolamento di uno dei nostri partner di percorsi di apprendimento per facilitare la transizione. 

### <a name="next-steps"></a>Operazioni successive
- Per ulteriori informazioni, vedere [Customize Learning pathways](custom_overview.md). 
- Vedere [translate site pages](custom_translate_page_ml.md).

