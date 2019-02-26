---
author: karuanag
ms.author: karuanag
title: Personalizzare e condividere playlist
ms.date: 02/10/2019
description: Creare playlist personalizzate dal contenuto esistente o dalle nuove pagine di SharePoint
ms.openlocfilehash: d330b6e401c9020eb68877bc8a132350811a2f31
ms.sourcegitcommit: e10085e60ca3f38029fde229fb093e6bc4a34203
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/25/2019
ms.locfileid: "29989727"
---
# <a name="customize-and-share-playlists"></a>Personalizzare e condividere playlist

## <a name="create-a-playlist"></a>Creare una playlist

Una playlist è una Compliation di "asset". "Asset" è una pagina di SharePoint o un elemento esistente di Microsoft Training Content. Quando si crea una playlist, si selezionano risorse che vanno insieme per creare un percorso di apprendimento per l'utente.  

Il vantaggio dell'aggiunta di pagine di SharePoint è che è possibile creare pagine di SharePoint con video o video di YouTube ospitati nell'organizzazione. È inoltre possibile creare pagine con moduli o altri contenuti di Office 365.  

#### <a name="step-1-create-a-sharepoint-page-for-your-playlist"></a>Passaggio 1: creare una pagina di SharePoint per la playlist
In questo esempio viene creata prima una pagina di SharePoint da aggiungere alla playlist. Verrà creata una pagina con una Web part video di YouTube e una Web part di testo.  Queste istruzioni presuppongono che si utilizzi il servizio SharePoint Online. 

#### <a name="create-a-new-page"></a>Creare una nuova pagina
1.  Selezionare il menu impostazioni > contenuto del sito > pagine del sito > nuova pagina del sito di >.
2.  Nell'area titolo, digitare use the teams Command Box.
3.  Selezionare la sezione Aggiungi una nuova e quindi selezionare due colonne.

![Aggiunta di due colonne](media/clo365addtwocolumn.png)

4.  Nella casella a sinistra, selezionare Aggiungi una nuova Web part, quindi fare clic su incorpora. 
5.  In un Web browser, passare a questo URL https://youtu.be/wYrRCRphrp0 e ottenere il codice di incorporamento per il video. 
6.  Nella web part di SharePoint, selezionare Aggiungi codice embed e incollarlo nella casella incorpora. 
7.  Nella casella a destra, selezionare Aggiungi una nuova Web part, quindi selezionare testo. 
8.  In un Web browser, passare a questo URL: https://support.office.com/en-us/article/13c4e429-7324-4886-b377-5dbed539193b e copiare la prova! Istruzioni dalla pagina e incollarle nella web part testo. La pagina dovrebbe essere simile alla seguente. 

![Pagina incorporamento](media/clo365teamscommandbox.png)

9.  Fare clic su **pubblica**e quindi copiare l'URL della pagina e incollarlo nel blocco note

#### <a name="step-2-create-the-playlist"></a>Passaggio 2: creare la playlist

1. Passare alla pagina di **amministrazione dell'apprendimento personalizzata** nell'esperienza del sito. ![custom_admin. png](media/custom_admin.png)
1. Verificare che la **categoria** sia selezionata 
1. Fare clic sulla categoria in cui si desidera visualizzare la nuova playlist
1. Accanto al nome della categoria, fare clic sul segno più ![custom_addplay. png](media/custom_addplay.png)

1. Inserire i valori come illustrato nell'esempio riportato di seguito e selezionare **Crea**. ![custom_details. png](media/custom_details.png)
- **Titolo** -nome visualizzato della playlist
- **Descrizione** -informazioni su ciò che verrà imparato
- **Categoria** -preselezionata in base alla selezione iniziale
- **Sottocategoria** -preselezionata in base alla selezione iniziale
- **Tecnologia** : selezionare applicabile
- **Level** -Beginner, Intermidate o Advanced
- Gruppo di **destinatari** : consente di assegnare il contenuto in base a un elenco predefinito di ruoli forniti da Microsoft.

6. Fare clic su **Salva dettaglio**

> [!TIP]
> È possibile personalizzare l'immagine dell'icona per la playlist.  Fare clic sull'icona dell'immagine e inserire un URL di un'immagine caricata in precedenza.  Verificare che l'immagine si trovi all'interno della raccolta siti di apprendimento personalizzato o in un'altra posizione in cui tutti gli utenti avranno accesso al file.  
![custom_image. png](media/custom_image.png)

#### <a name="step-3-add-assets-to-the-playlist"></a>Passaggio 3: aggiungere risorse alla playlist
In questo passaggio, si aggiungono le risorse esistenti da Microsoft e la pagina di SharePoint creata per la playlist. 

1. Dopo aver salvato i dettagli per la playlist, è possibile utilizzare la ricerca per le risorse esistenti.
1. **Immettere un termine di ricerca** per visualizzare un elenco di risorse predefinite che sono disponibili da altre playlist. **Fare clic sul nome** di una risorsa per includerla nella nuova playlist. ![custom_slist. png](media/custom_slist.png)

È inoltre possibile aggiungere la pagina di SharePoint creata in precedenza o crearne una da zero nell'esperienza.

1. Fare clic sull'opzione **nuova risorsa** nella finestra di dialogo risorse playlist.
1. Assegnare un **titolo**alla propria risorsa. Una volta immesso, vengono visualizzate ![le opzioni aggiuntive custom_newpage. png](media/custom_newpage.png)
1. È ora possibile creare una nuova pagina di asset in SharePoint Online o immettere l'URL di una pagina esistente per aggiungerla alla playlist personalizzata. 
1. I campi **categoria**, sottocategoria e **tecnologia** verranno prepopolati in base alle selezioni precedenti per la playlist. ****
1. Effettuare le selezioni appropriate per il livello e il gruppo di destinatari per questo singolo cespite.  
1. Fare clic su **Salva risorsa** per aggiungerla all'elenco di riproduzione personalizzato
1. Ripetere questi passaggi, cercando o aggiungendo singole pagine, finché la playlist non è stata completata. 
1. Fare clic su **Chiudi playlist** per salvare

L'elenco di riproduzione con questo contenuto sarà ora disponibile ovunque sia stato installato/incorporato il WebPart di apprendimento personalizzato. 

> [!NOTE]
> Se si commette un errore dopo aver chiuso la playlist, è possibile eliminarla dalla categoria facendo clic sulla X accanto al nome della playlist.  

#### <a name="things-to-think-about"></a>Aspetti da considerare

Gli elenchi di riproduzione personalizzati possono essere utilizzati per assistere gli utenti finali in una vasta gamma di attività.  Si dispone di un modulo di richiesta di tempo di disattivazione?  Un modulo per richiedere apparecchiature hardware?  Tutte le risorse formative esistenti possono essere programmate nell'esperienza.  

## <a name="share-playlists"></a>Condivisione di playlist

1. Passare a una playlist all'interno di WebPart o di un'esperienza del sito
1. Nell'angolo in alto a sinistra vengono visualizzate tre icone
1. Fare clic sull'icona che rappresenta un collegamento
1. Copiare l'URL nella playlist

![Share. png](media/share.png) questo URL può ora essere inserito nella struttura di spostamento del sito o utilizzato in altre comunicazioni per portare i dipendenti direttamente a quella playlist. 

### <a name="next-steps---drive-adoptiondriveadoptionmd"></a>Passaggi successivi: [adozione dell'unità](driveadoption.md)
