---
author: pkrebs
ms.author: pkrebs
title: Modelli di integrazione dei partner
ms.date: 3/9/2019
description: Modelli di integrazione dei partner
ms.service: sharepoint online
ms.openlocfilehash: 91980782f64d101d3128daff81ed4e2b6205faa8
ms.sourcegitcommit: ee4aebf60893887ae95a1294a9ad8975539ea762
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/23/2020
ms.locfileid: "48234138"
---
# <a name="partner-integration-models"></a>Modelli di integrazione dei partner
Anche se non è possibile completare il contenuto dei percorsi di apprendimento di Microsoft 365 direttamente "out of the box" dal servizio di provisioning di SharePoint Online, esistono diversi modelli di integrazione che i partner possono sfruttare per creare offerte di servizi di aggiunta di valore allineate. I modelli di integrazione dei partner di cui sopra sono presentati in ordine di complessità ascendente e livelli di investimento. Di conseguenza, la nostra guida è quella di sviluppare le proprie competenze e perfezionarsi a livelli più avanzati basati sui modelli aziendali.

![cg-part-intmodel.png](media/cg-part-intmodel.png) 

## <a name="how-should-i-get-started"></a>Come iniziare? 
Per iniziare, Ecco alcune procedure consigliate da seguire.     

### <a name="1-begin-with-building-expertise-as-an-enabler"></a>1. iniziare con la creazione di competenze come Enabler. 
È possibile aiutare una percentuale della propria base di clienti, abilitando il portale di formazione dei percorsi di apprendimento e eseguendo la curation del contenuto Microsoft mirata. Per istruzioni su come eseguire il provisioning dei percorsi di apprendimento, vedere https://docs.microsoft.com/office365/customlearning/custom_provision .  

### <a name="2-then-extend-your-services-as-an-integrator"></a>2. quindi estendere i servizi come integratore
Eseguire un ripristino dell'automazione nell'analisi degli investimenti, a seconda della quantità di contenuto e/o delle esigenze di integrazione dei servizi. Ad esempio, potrebbe non essere opportuno prendere in considerazione i costi di sviluppo e operativi rispetto alle linee guida per l'integrazione del contenuto, se è possibile creare rapidamente manualmente una playlist personalizzata mirata che punta al contenuto da pagare o che fa riferimento ai servizi.

### <a name="3-when-the-return-on-investment-makes-sense--consider-redistribution"></a>3. quando il ritorno sull'investimento ha senso – prendere in considerazione la ridistribuzione 
Quando il ritorno sull'investimento ha senso – prendere in considerazione la ridistribuzione (o collaborare con i partner dei percorsi di apprendimento correlati) per creare soluzioni ricreate. Questi sono basati sui modelli di SharePoint e sul Framework di esercitazione che forniscono soluzioni per estrarre siti personalizzati e quindi distribuirli in ambienti dei clienti 

## <a name="partner-provided-content-integration-guidelines"></a>Linee guida per l'integrazione del contenuto fornite dai partner
Il contenuto per i percorsi di apprendimento di Microsoft 365 è guidato da un insieme di file JSON che fungono da manifesti del contenuto per il pacchetto di apprendimento. Sono disponibili tre file: metadata.jsattivato, playlists.jse assets.js. Questi file devono essere strutturati in modo che corrispondano ai modelli che la Web part riconosce e quindi ospitati da una rete di distribuzione del contenuto (CDN) per consentire alla web part di caricarli. Microsoft fornirà i modelli di avvio di questi file per iniziare.  

**Dichiarazione di non responsabilità:** la struttura dei file JSON è soggetta a modifiche in base al lavoro della soluzione imminente. Microsoft 365 Learning pathways partner Early Adopter Program (EAP) sarà informato di eventuali modifiche imminenti di questo tipo. Insieme a tutti i clienti con una guida alla compatibilità e/o alla transizione. 

### <a name="download-the-microsoft-365-learning-pathways-solution"></a>Scaricare la soluzione Microsoft 365 Learning pathways
È possibile scaricare la soluzione Microsoft 365 Learning pathways, insieme ai file JSON, dall'archivio GitHub: https://github.com/pnp/custom-learning-office-365 . Si noti che in questo momento, Microsoft non sta prendendo GitHub pull request sulla soluzione. Tuttavia, è possibile utilizzare i file GitHub come punto di partenza per la creazione di un pacchetto di contenuto personalizzato. 

### <a name="metadatajson-structure"></a>Metadata.jssulla struttura
Questo file può essere pensato come il cervello dei menu e della struttura. Contiene tutta la struttura di spostamento e gli elenchi di raccolta per i dati negli altri due file. 


|              Nome        |                     Descrizione                                                               | 
|:-----------------------------|-------------------------------------------------------------------------------------------|
|**Tecnologie**              |Il contenuto è contrassegnato e può essere nascosto in base alla tecnologia assegnata.                 |  
|&nbsp;&nbsp;ID                |GUID che rappresenta la tecnologia                                                           |  
|&nbsp;&nbsp;Nome              |Nome visualizzato della tecnologia                                                             |
|&nbsp;&nbsp;*Subjects []*     |Una matrice di soggetti che sono un sottoinsieme della tecnologia                                   | 
|&nbsp;&nbsp;&nbsp;&nbsp;ID    |GUID che rappresenta l'oggetto                                                              |
|&nbsp;&nbsp;&nbsp;&nbsp;Nome  |Nome visualizzato dell'oggetto                                                                |
|**Categories []**             |Le categorie informano la struttura di spostamento del controllo WebPart. Ogni categoria rappresenta un livello principale della struttura di spostamento                                                                                                                 |
|&nbsp;&nbsp;ID                |GUID che rappresenta la categoria/sottocategoria                                                 |
|&nbsp;&nbsp;Nome              |Nome visualizzato per la categoria/sottocategoria                                                  |
|&nbsp;&nbsp;Immagine             |URL dell'immagine da visualizzare nell'UX (rispetto alla base della rete CDN)            |
|&nbsp;&nbsp;TechnologyId      |Il GUID della tecnologia a cui è associato questo contenuto (facoltativo – stringa vuota)            |
|&nbsp;&nbsp;SubjectId         |Il GUID dell'oggetto a cui si riferisce questo contenuto (facoltativo – stringa vuota)               |
|&nbsp;&nbsp;Fonte            |La matrice di origine, non utilizzata in modo specifico in UX diversi dai dati personalizzati aggiunti dall'utente, è contrassegnata come "tenant" e l'area di amministrazione UX non consente la modifica di qualsiasi elemento non contrassegnato come "tenant".                           |
|&nbsp;&nbsp;*Sottocategorie []*|Le sottocategorie sono fondamentalmente il livello di NAV dal livello 2 verso il basso. La struttura è identica a quella di una categoria appena nidificata.          |
|**Gruppi di destinatari []**             |Quando gli elenchi di riproduzione associati a una categoria/sottocategoria sono diversi gruppi di destinatari contrassegnati, sarà disponibile un selettore per visualizzare i gruppi di destinatari disponibili. |         
|&nbsp;&nbsp;ID                |GUID del gruppo di destinatari                                                                       |  
|&nbsp;&nbsp;Nome              |Nome visualizzato del gruppo di destinatari                                                               |       
|**Origini []**               |La matrice di stringhe che contrassegnano il contenuto con l'origine, non utilizzata in modo specifico in UX diversi dai dati personalizzati aggiunti dall'utente, è contrassegnata come "tenant" e l'area di amministrazione di UX non consente la modifica di qualsiasi elemento non contrassegnato come "tenant".                                                   |  
|**Levels []**               |Quando gli elenchi di riproduzione associati a una categoria/sottocategoria sono contrassegnati da vari livelli, un selettore sarà disponibile per visualizzare i livelli disponibili.             |  
|&nbsp;&nbsp;ID                |GUID del livello                                                                          |  
|&nbsp;&nbsp;Nome              |Nome visualizzato del livello                                                                  | 
|**StatusTag [ ]**           |Tag di stato è quello di identificare il contenuto con vari status che verranno esposti in UX. Alcuni di questi flag verranno visualizzati per il consumer e alcuni solo per l'amministratore.                                                   |  
|&nbsp;&nbsp;ID                |GUID del StatugTag                                                                      |  
|&nbsp;&nbsp;Nome              |Nome visualizzato dell'StatusTag                                                              | 
|**Telemetria []**            |                                                                                           |  
|&nbsp;&nbsp;AppInsightsKey    |GUID della chiave dell'app Insights configurata per monitorare il caricamento della web part Visualizzatore. La verifica può essere disattivata da un amministratore per l'intero tenant, ma le informazioni inviate sono utente di anonimi con l'ID del tenant. Per ulteriori informazioni, vedere questa sezione. https://github.com/pnp/custom-learning-office-365#disabling-telemetry-collection               |  
|**Versione**                   |Le informazioni sulla versione vengono utilizzate dalla soluzione per indicare agli amministratori che il controllo WebPart è stato aggiornato e consentono anche a WebPart di aggiornare il contenuto personalizzato all'ultima versione del manifesto se sono state apportate modifiche significative.         | 
|&nbsp;&nbsp;Manifesto          |La versione del manifesto                                               |
|&nbsp;&nbsp;ManifestMinWebPart|La versione minima del controllo WebPart che utilizza la versione del manifesto             |
|&nbsp;&nbsp;CurrentWebPart    |URL dell'immagine da visualizzare nell'UX (rispetto alla base della rete CDN)            |
|&nbsp;&nbsp;Repourl           |URL dell'archivio in cui sono riportate le istruzioni della web part di aggiornamento.                    |
|**Pacchetti di contenuto**             |In questo momento i pacchetti di contenuto per CDN aggiuntivi non sono supportati. I pacchetti di contenuto consentono a Microsoft di suggerire altre soluzioni Microsoft create che possono essere provisionate tramite il servizio di provisioning che sfruttano M365LP per distribuire contenuti e sono di per sé reti CDN personalizzati.       | 
|&nbsp;&nbsp;ID                |GUID del pacchetto di contenuto/CDN                                                              |
|&nbsp;&nbsp;Nome              |Nome visualizzato della rete CDN                                                                   |
|&nbsp;&nbsp;Descrizione       |Descrizione da visualizzare nell'interfaccia utente per l'aggiunta di un pacchetto di contenuto                               |
|&nbsp;&nbsp;Immagine             |Immagine da visualizzare nell'interfaccia utente per l'aggiunta di un pacchetto di contenuto                                     |
|&nbsp;&nbsp;ProvisionURL      |L'URL del pacchetto del servizio di provisioning per creare la raccolta siti del pacchetto di contenuto  |
|&nbsp;&nbsp;CDNbase           |L'URL di base dei manifesti per il pacchetto di contenuto                                       |
|AssetOrigins                  |Una matrice di origine URL utilizzata nel assets.jssu file descritto in un secondo momento. Se l'URL di origine lo supporta, verrà inviato un messaggio di posta elettronica a help_getClientHeight. Una risposta nella proprietà Data di: "help_getClientHeight = {Height of content}" (ad esempio "help_getClientHeight = 5769") consentirà di ridimensionare l'iFrame all'altezza appropriata del contenuto incorniciato.         |

### <a name="playlistsjson-structure"></a>Playlists.jssulla struttura
playlists.json – il manifesto delle playlist è una matrice di oggetti che descrivono i metadati relativi a una playlist e le risorse incluse nell'elenco di riproduzione.

|              Nome        |                     Descrizione                                                               | 
|:-----------------------------|-------------------------------------------------------------------------------------------|
|Id                            |GUID che rappresenta la playlist                                                             |  
|Titolo                         |Nome visualizzato della playlist                                                               |
|Immagine                         |URL relativo (dalla rete CDN) a un'immagine per visualizzare la playlist                              |                      
|LevelId                       |Livello associato                                                                           |
|AudienceId                   |Gruppo di destinatari associato                                                                        |
|TechnologyId                 |Tecnologia associata                                                                      |
|SubjectId                    |Nome visualizzato per la categoria/sottocategoria                                                  |
|Origine                        |La matrice di origine, non utilizzata in modo specifico in UX diversi dai dati personalizzati aggiunti dall'utente, è contrassegnata come "tenant" e l'area di amministrazione UX non consente la modifica di qualsiasi elemento non contrassegnato come "tenant".                                              |
|CatId                         |ID categoria o sottocategoria che rappresenta il contenitore in cui deve essere visualizzata la playlist. Attualmente il manifesto non supporta la selezione di una categoria o di una sottocategoria come contenitore se dispone anche di sottocategorie figlio.        |
|Descrizione                   |Descrizione mostrata per ogni playlist nell'UX                                           |
|StatusTagId                   |Tag di stato associato                                                                      |
|StatusNote                    |Note sul contenuto visualizzato agli amministratori                                            |
|*Assets []*                        |Una matrice di GUID per le risorse che fanno parte di questa playlist, in ordine di visualizzazione.        |         

### <a name="assetjson-structure"></a>Asset.jssulla struttura
playlists.json – il manifesto delle playlist è una matrice di oggetti che descrivono i metadati relativi a una playlist e le risorse incluse nell'elenco di riproduzione.

|              Nome        |                     Descrizione                                                               | 
|:-----------------------------|-------------------------------------------------------------------------------------------|
|Id                            |GUID che rappresenta la playlist                                                             |  
|Titolo                         |Nome visualizzato della playlist                                                               |
|Descrizione                   |---                                                                                           |                      
|URL                           |L'URL di origine del cespite da applicare all'iFrame                                  |
|TechnologyId                  |Tecnologia associata                                                                      |
|SubjectId                     |Oggetto associato                                                                         |
|Origine                        |Nome visualizzato per la categoria/sottocategoria                                                  |
|StatusTagId                   |Tag di stato associato                                                                      |
|StatusNote                    |Note sul contenuto visualizzato agli amministratori.                                           |

### <a name="caching"></a>Memorizzazione nella cache
La versione corrente della web part visualizzatore utilizza una versione memorizzata nella cache dei file manifesto per 24 ore. Dopo 24 ore, il primo utente che ha colpito il controllo WebPart prende la hit delle prestazioni per aggiornare la cache scaricando i manifesti dalla rete CDN di origine e unire tali informazioni con le tecnologie e le playlist nascoste, nonché l'Unione nelle sottocategorie, nelle playlist e nelle risorse personalizzate. In alternativa, la Web part admin Scarica sempre il contenuto dai manifesti e li unisce e aggiorna la cache.  Pertanto, in altre parole, l'amministratore può forzare l'aggiornamento della cache in qualsiasi momento caricando la Web part amministratore, ovvero accedendo alla pagina di amministrazione.

## <a name="content-pack-guidelines"></a>Linee guida per il pacchetto di contenuto
La funzionalità del pacchetto di contenuto Sblocca gli scenari seguenti:
- La possibilità per i partner di ridistribuire il contenuto di apprendimento personalizzato aggiunto a valore personalizzato su misura per l'ambiente dei clienti
- La possibilità per le organizzazioni con un team di formazione forte e supporto IT di creare contenuto di apprendimento personalizzato diretto ai propri sistemi interni e governance
- La possibilità per Microsoft di fornire ulteriori percorsi di apprendimento in futuro che i clienti possano scegliere

Questo set di documentazione corrente è destinato intenzionalmente ai partner a causa della complessità della caratteristica. Il team del servizio lavora attivamente per migliorare il supporto e l'abilitazione dello scenario #2, in futuro. 

### <a name="how-content-packs-work"></a>Funzionamento del pacchetto di contenuto
Microsoft utilizza le pagine GitHub come origine della rete di distribuzione dei contenuti (CDN) per i file e le immagini manifesti. Nella root del repository GitHub è presente una cartella Docs che include sottocartelle per ogni versione dei file manifesto. All'interno di ogni cartella sono presenti tre file manifesto, oltre a una cartella immagini per archiviare tutte le immagini categoria, sottocategoria e playlist. 

È importante mantenere la stessa struttura di controllo delle versioni che Microsoft deve scegliere per estendere la soluzione di percorsi di apprendimento con il proprio pacchetto di contenuto. L'endpoint della rete CDN non deve includere la cartella della versione, poiché la versione del manifesto supportata dalla web part viene aggiunta al forno e viene automaticamente accodata all'URL della CDN. Ovviamente, è possibile creare nuove istanze dei file manifesto ogni volta che viene revisionato.

![cg-part-json-folder.png](media/cg-part-json-folder.png) 

Per ulteriori informazioni sull'utilizzo di pagine GitHub come origine della rete CDN, vedere la documentazione della guida seguente: [https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages](https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages) .

La soluzione Microsoft rende accessibili al pubblico le informazioni relative alle risorse, in quanto non vi è alcuna sicurezza per gli utenti che hanno accesso a questi file. Noi crediamo che ci dovrebbe essere un livello di contenuto gratuito per un consumatore, che ha detto che se si ha la necessità di pagare il muro per alcuni o tutti i contenuti, sarà necessario implementarlo in modo diverso all'interno delle limitazioni tecniche della soluzione e l'utilizzo di GitHub Pages non è assolutamente un requisito. Qualsiasi provider della rete CDN che si desidera utilizzare va bene se si mantiene la struttura di numerazione delle versioni descritta. Come indicato in precedenza, la versione della struttura del manifesto supportata dalla web part viene aggiunta al forno nel codice e viene automaticamente accodata all'URL della rete CDN. 

### <a name="content-pack-integration-guidance"></a>Guida all'integrazione del pacchetto di contenuto 
Le web part di amministratore e Visualizzatore sono state estese per consentire al consumer di configurare altri endpoint della rete CDN nel tenant, che consentirà quindi alla web part Visualizzatore di selezionare la CDN che dovrebbe utilizzare come origine dei dati visualizzati. 

Inquadratura dei tasti da tenere presente per questa caratteristica: 
- Questo è il principale applicabile per gli scenari di ridistribuzione dei partner – dove la configurazione manuale della playlist è troppo ingombrante 
- I pacchetti di contenuto personalizzati sono una funzionalità avanzata e devono essere utilizzati solo dai partner che dispongono di contenuti Web che gestiscono l'esperienza. Le origini di contenuto non attendibili possono introdurre contenuto non sicuro nel sito. È consigliabile aggiungere solo le origini attendibili.

> **Importante** Prima di aggiungere un pacchetto di contenuto personalizzato, è necessario eseguire il provisioning di Microsoft 365 Learning pathways 3,0 o versione successiva. Per informataion sul provisioning dei percorsi di apprendimento di Microsoft 365, vedere [provision microsoft 365 Learning pathways](https://docs.microsoft.com/office365/customlearning/custom_provision).

### <a name="content-whitelisting"></a>Whitelist del contenuto
Come partner è vostra responsabilità assistere i consumatori nel garantire che il contenuto sia in whitelist nel proprio ambiente. Si consiglia di creare uno scenario di testing nel proprio ambiente per convalidare che il contenuto può essere iFrame ' d in una pagina di SharePoint all'interno del proprio firewall. Seguire le istruzioni [create SharePoint pages for Custom playlists](https://docs.microsoft.com/office365/customlearning/custom_createnewpage) per confermare che questo è il caso.

### <a name="add-a-content-pack-to-learning-pathways"></a>Aggiungere un pacchetto di contenuto ai percorsi di apprendimento
Dopo aver creato la modifica JSON e aver definito la rete CDN, è possibile aggiungere il contatto Pack ai percorsi di apprendimento. 

1. Nella **Home** page del sito percorsi di apprendimento scegliere **Home** e quindi fare clic su **Learning pathways Administration**. 
2. Dalla pagina **Amministrazione** , fare clic su **... Aggiungere il pacchetto di contenuto** nell'angolo in alto a destra della pagina.
3. Fare clic su pacchetto di contenuto personalizzato e quindi immettere un nome per il pacchetto di contenuto e quindi specificare la rete CDN in cui si trovano i file JSON.

![cg-part-addconpack.png](media/cg-part-addconpack.png)

4. Fare clic su **Salva**. Il contenuto del pacchetto di contenuto personalizzato dovrebbe ora essere visualizzato nella pagina di amministrazione. Ecco un esempio. 

![cg-part-addconpackex.png](media/cg-part-addconpackex.png)

### <a name="filter-to-the-content-pack-in-the-web-part"></a>Filtro per il pacchetto di contenuto nella web part
Con i percorsi di apprendimento, è possibile aggiungere la Web part percorsi di apprendimento a una pagina, filtrare la Web part in modo che punti all'origine del pacchetto di contenuto personalizzato e quindi filtrare la Web part per la categoria, la sottocategoria, la playlist e la risorsa desiderata. 

1. Dal sito percorsi di apprendimento fare clic su **nuovo**e quindi su **pagina**.
2. Fare clic su **vuoto**e quindi su **Crea pagina**.
3. Assegnare un nome alla pagina. 
4. Fare clic su **+ Aggiungi una nuova sezione** sul lato sinistro della pagina.
5. Fare clic **+** nella parte superiore centrale della nuova sezione e quindi aggiungere la Web part **Microsoft 365 Learning pathways** .
6. Fare clic sulla Web part e quindi fare clic sull'icona **modifica** .
7. Nella casella **selezionare l'origine di apprendimento** selezionare il pacchetto di contenuto personalizzato e quindi filtrare la Web part in base al contenuto desiderato. Di seguito viene fornito un esempio di filtraggio della web part per una playlist da un pacchetto di contenuto personalizzato.

![cg-part-conpackfilter.png](media/cg-part-conpackfilter.png)  




