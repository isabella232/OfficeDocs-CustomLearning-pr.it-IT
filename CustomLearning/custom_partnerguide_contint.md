---
author: pkrebs
ms.author: pkrebs
title: Modelli di integrazione dei partner
ms.date: 3/9/2019
description: Modelli di integrazione dei partner
ms.service: sharepoint online
ms.openlocfilehash: f3b5c5ddc8de29d2805c86a24b1d9bef0c8cacfa
ms.sourcegitcommit: 907c657e7cc5a4a44d2b9f38cc35fea9ac5c5943
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/24/2021
ms.locfileid: "51162933"
---
# <a name="partner-integration-models"></a>Modelli di integrazione dei partner
Sebbene non sia possibile integrare il contenuto dei percorsi di apprendimento di Microsoft 365 direttamente "out of the box" dal servizio di provisioning di SharePoint Online, esistono diversi modelli di integrazione che i partner possono sfruttare per creare offerte di servizi a valore aggiunto allineate. I modelli di integrazione dei partner precedenti sono presentati in ordine di complessità crescente e livelli di investimento. Di conseguenza, la nostra guida è di sviluppare le tue competenze e i tuoi laureati a livelli più avanzati in base ai tuoi modelli di business.

![cg-part-intmodel.png](media/cg-part-intmodel.png) 

## <a name="how-should-i-get-started"></a>Come iniziare? 
Per iniziare, ecco alcune procedure consigliate da seguire.     

### <a name="1-begin-with-building-expertise-as-an-enabler"></a>1. Iniziare con la creazione di competenze come abilitazione. 
Puoi aiutare subito una percentuale della tua base di clienti abilitando il portale di formazione sui percorsi di apprendimento ed eseguendo una cura mirata dei contenuti Microsoft. Per istruzioni sul provisioning dei percorsi di apprendimento, vedere https://docs.microsoft.com/office365/customlearning/custom_provision .  

### <a name="2-then-extend-your-services-as-an-integrator"></a>2. Estendere quindi i servizi come integratore
Eseguire un'analisi del ritorno sull'investimento per l'automazione, a seconda della quantità di contenuti e/o esigenze di integrazione dei servizi. Ad esempio, potrebbe non avere senso prendere in conto i costi di sviluppo e operativi rispetto alle linee guida per l'integrazione dei contenuti se puoi creare rapidamente manualmente una playlist personalizzata mirata che punti al contenuto a pagamento o fare riferimento ai tuoi servizi.

### <a name="3-when-the-return-on-investment-makes-sense--consider-redistribution"></a>3. Quando il ritorno sull'investimento è sensato, prendere in considerazione la ridistribuzione 
Quando il ritorno sull'investimento ha senso, prendi in considerazione la ridistribuzione (o l'utilizzo di partner correlati ai percorsi di apprendimento) per creare soluzioni riconfezionate. Si basano sul framework di modelli e procedure di SharePoint che fornisce soluzioni per estrarre siti personalizzati e quindi distribuirlo negli ambienti dei clienti 

## <a name="partner-provided-content-integration-guidelines"></a>Linee guida per l'integrazione del contenuto fornite dai partner
Il contenuto per i percorsi di apprendimento di Microsoft 365 è guidato da un set di file JSON che agiscono come manifesti di contenuto per il pacchetto di apprendimento. Sono disponibili tre file: metadata.js, playlists.jse assets.jssu. Questi file devono essere strutturati in modo da corrispondere ai modelli che la web part riconosce e quindi ospitati da una rete per la distribuzione di contenuto (CDN) per consentire alla web part di caricarli. Microsoft fornirà modelli di avvio di questi file per iniziare.  

**Dichiarazione di non responsabilità:** la struttura del file JSON è soggetta a modifiche in base al lavoro della soluzione imminente. Il partner dei percorsi di apprendimento di Microsoft 365 Early Adopter Program (EAP) sarà informato di eventuali cambiamenti imminenti di questa natura. Insieme a qualsiasi guida alla compatibilità con le versioni precedenti e/o alla transizione dei clienti. 

### <a name="download-the-microsoft-365-learning-pathways-solution"></a>Scaricare la soluzione percorsi di apprendimento di Microsoft 365
È possibile scaricare la soluzione percorsi di apprendimento di Microsoft 365, insieme ai file JSON, dal repository GitHub: https://github.com/pnp/custom-learning-office-365 . Tieni presente che al momento Microsoft non sta prendendo la richiesta pull GitHub nella soluzione. Tuttavia, puoi usare i file GitHub come punto di partenza per creare un pacchetto di contenuto personalizzato. 

### <a name="metadatajson-structure"></a>Metadata.jssulla struttura
Puoi pensare a questo file come al cervello dei menu e della struttura. Contiene tutta la struttura di spostamento e gli elenchi di selezione per i dati negli altri due file. 


|              Nome        |                     Descrizione                                                               | 
|:-----------------------------|-------------------------------------------------------------------------------------------|
|**Tecnologie**              |Il contenuto è contrassegnato con tag e può essere nascosto in base alla tecnologia assegnata.                 |  
|&nbsp;&nbsp;ID                |GUID che rappresenta la tecnologia                                                           |  
|&nbsp;&nbsp;Nome              |Nome visualizzato della tecnologia                                                             |
|&nbsp;&nbsp;*Soggetti[ ]*     |Matrice di argomenti che sono un sottoinsieme della tecnologia                                   | 
|&nbsp;&nbsp;&nbsp;&nbsp;ID    |GUID che rappresenta l'oggetto                                                              |
|&nbsp;&nbsp;&nbsp;&nbsp;Nome  |Nome visualizzato dell'oggetto                                                                |
|**Categorie [ ]**             |Le categorie informano lo spostamento della web part. Ogni categoria rappresenta un livello superiore della struttura di spostamento                                                                                                                 |
|&nbsp;&nbsp;ID                |GUID che rappresenta la categoria/sottocategoria                                                 |
|&nbsp;&nbsp;Nome              |Nome visualizzato per la categoria/sottocategoria                                                  |
|&nbsp;&nbsp;Immagine             |URL dell'immagine che deve essere visualizzata nell'esperienza utente (rispetto alla base della rete CDN)            |
|&nbsp;&nbsp;TechnologyId      |GUID della tecnologia a cui è correlato questo contenuto (facoltativo - stringa vuota)            |
|&nbsp;&nbsp;SubjectId         |GUID dell'oggetto a cui è correlato il contenuto (facoltativo - stringa vuota)               |
|&nbsp;&nbsp;Source            |From Source array, not specifically used in UX other than custom data added by the user is marked as "Tenant" and the UX admin area does not allow editing of anything not marked "Tenant".                           |
|&nbsp;&nbsp;*Sottocategorie[ ]*|Sub-Categories sono fondamentalmente il livello di spostamento dal livello 2 verso il basso. La struttura è la stessa di un oggetto Category appena annidato.          |
|**Gruppi di destinatari [ ]**             |Quando alle playlist associate a una categoria/sottocategoria sono associati diversi gruppi di destinatari, sarà disponibile un selettore per visualizzare i gruppi di destinatari disponibili. |         
|&nbsp;&nbsp;ID                |GUID del gruppo di destinatari                                                                       |  
|&nbsp;&nbsp;Nome              |Nome visualizzato del gruppo di destinatari                                                               |       
|**Origini [ ]**               |Matrice di stringhe che contrassegna il contenuto con la relativa origine, non specificatamente utilizzata nell'esperienza utente oltre ai dati personalizzati aggiunti dall'utente è contrassegnata come "Tenant" e l'area di amministrazione dell'esperienza utente non consente la modifica di elementi non contrassegnati come "Tenant".                                                   |  
|**Livelli [ ]**               |Quando alle playlist associate a una categoria/sottocategoria sono associati diversi livelli, sarà disponibile un selettore per visualizzare i livelli disponibili.             |  
|&nbsp;&nbsp;ID                |GUID del livello                                                                          |  
|&nbsp;&nbsp;Nome              |Nome visualizzato del livello                                                                  | 
|**StatusTag [ ]**           |Il tag di stato consente di identificare il contenuto con vari stati che verranno esposti nell'esperienza utente. Alcuni di questi flag verranno visualizzati all'utente e altri solo all'amministratore.                                                   |  
|&nbsp;&nbsp;ID                |GUID di StatugTag                                                                      |  
|&nbsp;&nbsp;Nome              |Nome visualizzato dell'oggetto StatusTag                                                              | 
|**Telemetria [ ]**            |                                                                                           |  
|&nbsp;&nbsp;AppInsightsKey    |GUID della chiave di analisi delle app che hai configurato per tenere traccia del caricamento della web part visualizzatore. La verifica può essere disattivata da un amministratore per l'intero tenant, ma le informazioni inviate sono un utente anonimizzato con l'ID tenant. Per ulteriori informazioni, vedere questa sezione https://github.com/pnp/custom-learning-office-365#disabling-telemetry-collection               |  
|**Versione**                   |Le informazioni sulla versione vengono utilizzate dalla soluzione per indicare agli amministratori che la web part è stata aggiornata e consentono inoltre alla web part di aggiornare automaticamente il contenuto personalizzato alla versione più recente del manifesto se sono state apportate modifiche significative.         | 
|&nbsp;&nbsp;Manifesto          |Versione del manifesto                                               |
|&nbsp;&nbsp;ManifestMinWebPart|Versione minima della web part che funziona con la versione del manifesto             |
|&nbsp;&nbsp;CurrentWebPart    |URL dell'immagine che deve essere visualizzata nell'esperienza utente (rispetto alla base della rete CDN)            |
|&nbsp;&nbsp;RepoURL           |URL del repository in cui si trova la web part di aggiornamento.                    |
|**Pacchetti di contenuto**             |Al momento i pacchetti di contenuto per le reti CDN aggiuntive non sono supportati. I pacchetti di contenuto consentono a Microsoft di suggerire altre soluzioni create da Microsoft di cui è possibile eseguire il provisioning tramite il servizio di provisioning che sfruttano M365LP per distribuire contenuto e si trovano in reti CDN personalizzate.       | 
|&nbsp;&nbsp;ID                |GUID del pacchetto di contenuto/rete CDN                                                              |
|&nbsp;&nbsp;Nome              |Nome visualizzato della rete CDN                                                                   |
|&nbsp;&nbsp;Descrizione       |Descrizione da visualizzare nell'interfaccia utente per l'aggiunta di un pacchetto di contenuto                               |
|&nbsp;&nbsp;Immagine             |Immagine da visualizzare nell'interfaccia utente per l'aggiunta di un pacchetto di contenuto                                     |
|&nbsp;&nbsp;ProvisionURL      |URL del pacchetto del servizio di provisioning per creare la raccolta siti del pacchetto di contenuto  |
|&nbsp;&nbsp;CDNbase           |URL di base per i manifesti per il pacchetto di contenuto                                       |
|AssetOrigins                  |Matrice di origini URL utilizzata nel file assets.jsdescritto più avanti. Se l'URL di origine lo supporta, verrà inviato un messaggio post help_getClientHeight. Una risposta nella proprietà data di: "help_getClientHeight={height of content}" (ad esempio "help_getClientHeight=5769") consentirà all'iFrame di essere ridimensionato all'altezza appropriata del contenuto con frame.         |

### <a name="playlistsjson-structure"></a>Playlists.jssulla struttura
playlists.jsattivo: il manifesto delle playlist è una matrice di oggetti che descrivono i metadati relativi a una playlist e gli asset inclusi nella playlist.

|              Nome        |                     Descrizione                                                               | 
|:-----------------------------|-------------------------------------------------------------------------------------------|
|Id                            |GUID che rappresenta la playlist                                                             |  
|Titolo                         |Nome visualizzato della playlist                                                               |
|Immagine                         |URL relativo (dalla rete CDN) a un'immagine per visualizzare la playlist                              |                      
|LevelId                       |Livello associato                                                                           |
|AudienceId                   |Gruppo di destinatari associato                                                                        |
|TechnologyId                 |Tecnologia associata                                                                      |
|SubjectId                    |Nome visualizzato per la categoria/sottocategoria                                                  |
|Origine                        |Dalla matrice di origine, non specificatamente utilizzata nell'esperienza utente oltre ai dati personalizzati aggiunti dall'utente, viene contrassegnata come "Tenant" e l'area di amministrazione dell'esperienza utente non consente la modifica di elementi non contrassegnati come "Tenant".                                              |
|CatId                         |L'ID categoria o sottocategoria che rappresenta il contenitore in cui deve essere visualizzata la playlist. Attualmente il manifesto non supporta la selezione di una categoria o di una sottocategoria come contenitore se ha anche figli SubCategory.        |
|Descrizione                   |Una descrizione mostrata per ogni playlist nell'esperienza utente                                           |
|StatusTagId                   |Tag di stato associato                                                                      |
|StatusNote                    |Note sul contenuto visualizzato agli amministratori                                            |
|*Assets[]*                        |Matrice di GUID per gli asset che fanno parte di questa playlist, in ordine di visualizzazione.        |         

### <a name="assetjson-structure"></a>Asset.jssulla struttura
playlists.jsattivo: il manifesto delle playlist è una matrice di oggetti che descrivono i metadati relativi a una playlist e gli asset inclusi nella playlist.

|              Nome        |                     Descrizione                                                               | 
|:-----------------------------|-------------------------------------------------------------------------------------------|
|Id                            |GUID che rappresenta la playlist                                                             |  
|Titolo                         |Nome visualizzato della playlist                                                               |
|Descrizione                   |---                                                                                           |                      
|URL                           |URL di origine dell'asset da applicare all'iFrame                                  |
|TechnologyId                  |Tecnologia associata                                                                      |
|SubjectId                     |Oggetto associato                                                                         |
|Origine                        |Nome visualizzato per la categoria/sottocategoria                                                  |
|StatusTagId                   |Tag di stato associato                                                                      |
|StatusNote                    |Note sul contenuto visualizzato agli amministratori.                                           |

### <a name="caching"></a>Memorizzazione nella cache
La versione corrente della web part visualizzatore utilizza una versione memorizzata nella cache dei file manifesto per 24 ore. Dopo 24 ore, il primo utente che ha raggiunto la web part utilizza l'hit delle prestazioni per aggiornare la cache scaricando i manifesti dalla rete CDN di origine e unendo le informazioni con tecnologie e playlist nascoste, nonché unendo sottocategorie, playlist e asset personalizzati. In alternativa, la web part di amministrazione scarica sempre il contenuto dai manifesti e li unisce e aggiorna la cache.  Pertanto, in altre parole, l'amministratore può forzare un aggiornamento della cache in qualsiasi momento caricando la web part di amministrazione, aka andando alla pagina Amministrazione.

## <a name="content-pack-guidelines"></a>Linee guida per i pacchetto di contenuto
La funzionalità Pacchetto di contenuto consente di sbloccare gli scenari seguenti:
- Possibilità per i partner di ridistribuire contenuti di apprendimento personalizzati a valore aggiunto personalizzati personalizzati per l'ambiente dei clienti
- Possibilità per le organizzazioni con un team di formazione e supporto IT di creare contenuti di apprendimento personalizzati indirizzati ai propri sistemi interni e alla governance
- La possibilità per Microsoft di offrire ulteriori percorsi di apprendimento in futuro a cui i clienti possono acconsentire esplicitamente

Questo set di documentazione corrente è intenzionalmente destinato ai partner a causa della complessità della funzionalità. Il team del servizio sta lavorando attivamente per supportare e abilitare meglio gli scenari #2, in futuro. 

### <a name="how-content-packs-work"></a>Funzionamento dei pacchetti di contenuto
Microsoft utilizza le pagine GitHub come origine CDN (Content Delivery Network) per i file manifesto e le immagini. Nella radice del repository GitHub è disponibile una cartella documenti che include sottocartelle per ogni versione dei file manifesto. All'interno di ogni cartella sono presenti tre file manifesto, oltre a una cartella immagini per archiviare tutte le immagini di categoria, sottocategoria e playlist. 

È importante mantenere la stessa struttura di controllo delle versioni di Microsoft se si sceglie di estendere la soluzione dei percorsi di apprendimento con il proprio pacchetto di contenuto. L'endpoint della rete CDN non deve includere la cartella della versione, poiché la versione del manifesto supportata dalla web part viene aggiunta automaticamente all'URL della rete CDN. Ti daremo ovviamente il tempo di creare nuove istanze dei file manifesto ogni volta che li revisioniamo.

![cg-part-json-folder.png](media/cg-part-json-folder.png) 

Per ulteriori informazioni sull'utilizzo delle pagine GitHub come origine CDN, vedere la documentazione della Guida seguente: [https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages](https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages) .

La soluzione di Microsoft rende aperte al pubblico le informazioni sugli asset, in quanto non esiste alcuna sicurezza per chi ha accesso a questi file. Riteniamo che dovrebbe essere disponibile un livello gratuito di contenuto per un utente, che ha detto che se hai bisogno di una parete di pagamento per parte o tutto il contenuto dovrai implementare questo in modo diverso entro le limitazioni tecniche della soluzione e l'uso delle pagine GitHub non è affatto un requisito. Qualsiasi provider di rete CDN che si desidera utilizzare è valido se si mantiene la struttura di numerazione delle versioni delineata. Come indicato in precedenza, la versione della struttura del manifesto supportata dalla web part viene aggiunta automaticamente all'URL della rete CDN. 

### <a name="content-pack-integration-guidance"></a>Linee guida per l'integrazione dei pacchetto di contenuto 
Le web part di amministrazione e visualizzatore sono state estese per consentire all'utente di configurare endpoint CDN aggiuntivi nel tenant, in modo da consentire alla web part visualizzatore di selezionare quale rete CDN deve fornire i dati visualizzati. 

Inquadratura chiave da tenere presente per questa funzionalità: 
- Ciò è applicabile in modo primario per gli scenari di ridistribuzione dei partner, in cui la configurazione manuale delle playlist è troppo complicata 
- I pacchetti di contenuto personalizzati sono una funzionalità avanzata e devono essere utilizzati solo dai partner con esperienza di amministrazione del contenuto Web. Le origini di contenuto non attendibili possono introdurre contenuto non sicuro nel sito. È consigliabile aggiungere solo origini attendibili.

> **IMPORTANTE** Prima di aggiungere un pacchetto di contenuto personalizzato, è necessario aver effettuato il provisioning dei percorsi di apprendimento di Microsoft 365 3.0 o versioni successive. Per informazioni sul provisioning dei percorsi di apprendimento di Microsoft 365, vedere Provisioning dei percorsi di apprendimento di [Microsoft 365.](./custom_provision.md)

### <a name="content-whitelisting"></a>Whitelisting del contenuto
In quanto partner, è responsabilità dell'utente assistere gli utenti nell'assicurarsi che il contenuto sia nella whitelist nel proprio ambiente. Ti consigliamo di creare uno scenario di test nel loro ambiente per verificare che il contenuto possa essere iFrame in una pagina di SharePoint all'interno del firewall. Seguire le [istruzioni Create SharePoint pages for Custom Playlists](./custom_createnewpage.md) per verificare che questo sia il caso.

### <a name="add-a-content-pack-to-learning-pathways"></a>Aggiungere un pacchetto di contenuto ai percorsi di apprendimento
Dopo aver creato json modificato e definito la rete CDN, puoi aggiungere il Contact Pack ai percorsi di apprendimento. 

1. Nella home page del sito percorsi **di** apprendimento scegliere **Home** e quindi fare clic su Amministrazione percorsi **di apprendimento.** 
2. Nella pagina **Amministrazione** fare clic sul **pulsante ... Aggiungere il pacchetto di** contenuto nell'angolo superiore destro della pagina.
3. Fare clic su Pacchetto di contenuto personalizzato, quindi immettere un nome del pacchetto di contenuto e quindi specificare la rete CDN in cui si trovano i file JSON.

![cg-part-addconpack.png](media/cg-part-addconpack.png)

4. Fare clic su **Salva**. Il contenuto del pacchetto di contenuto personalizzato dovrebbe ora essere visualizzato nella pagina Amministrazione. Ecco un esempio. 

![cg-part-addconpackex.png](media/cg-part-addconpackex.png)

### <a name="filter-to-the-content-pack-in-the-web-part"></a>Filtrare in base al pacchetto di contenuto nella web part
Con i percorsi di apprendimento, è possibile aggiungere la web part percorsi di apprendimento a una pagina, filtrare la web part in modo che punti all'origine Pacchetto di contenuto personalizzato e quindi filtrare la web part in base alla categoria, alla sottocategoria, alla playlist e all'asset desiderati. 

1. Nel sito percorsi di apprendimento fare clic su **Nuovo** e quindi **su Pagina.**
2. Fare **clic su** Vuoto e quindi su Crea **pagina.**
3. Assegna un nome alla pagina. 
4. Fai clic su + **Aggiungi una nuova** sezione sul lato sinistro della pagina.
5. Fare clic nella parte superiore centrale della nuova sezione e quindi aggiungere la web part Percorsi di apprendimento di **+** **Microsoft 365.**
6. Fare clic sulla web part e quindi **sull'icona** Modifica.
7. Nella casella **Selezionare l'origine di** apprendimento selezionare il pacchetto di contenuto personalizzato e quindi filtrare la web part in base al contenuto desiderato. Di seguito viene fornito un esempio della web part filtrata in una playlist da un pacchetto di contenuto personalizzato.

![cg-part-conpackfilter.png](media/cg-part-conpackfilter.png)