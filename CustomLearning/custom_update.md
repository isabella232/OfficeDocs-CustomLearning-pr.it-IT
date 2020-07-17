---
author: pkrebs
ms.author: pkrebs
title: Aggiornare i percorsi di apprendimento di Microsoft 365
ms.date: 07/06/2020
description: Aggiornare i percorsi di apprendimento di Microsoft 365
ms.openlocfilehash: 5fe9dc64916eb75d309c44188cd2f72fa88ba9e4
ms.sourcegitcommit: ba0cddd12dd8687ec4b97c26174fdda09de83b05
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/06/2020
ms.locfileid: "45043248"
---
# <a name="update-learning-pathways"></a>Aggiornare i percorsi di apprendimento
Se si dispone di un sito di percorsi di apprendimento esistente, è possibile aggiornarlo per il supporto multilingue. Per aggiornare i percorsi di apprendimento alla versione multilingue di 4,0, caricare il pacchetto della web part, customlearning. sppkg, nel catalogo app tenant di SharePoint. Quando si aggiornano i percorsi di apprendimento:  

- Tutte le playlist e le risorse personalizzate create in precedenza vengono mantenute
- Le impostazioni per nascondere o visualizzare il contenuto vengono mantenute
- Il modello di percorsi di apprendimento di SharePoint è rimasto invariato
- Le pagine del sito percorsi di apprendimento non vengono convertite. Questo lavoro deve essere svolto manualmente

## <a name="read-the-learning-pathways-multilingual-overview"></a>Leggere la panoramica dei percorsi di apprendimento multilingue
Per ulteriori informazioni sul funzionamento del supporto multilingue per i percorsi di apprendimento, leggere la [Panoramica dei percorsi di apprendimento multilingue](custom_overview.md). 

## <a name="prerequisites-to-update"></a>Prerequisiti per l'aggiornamento
Prima di aggiornare i percorsi di apprendimento, è necessario soddisfare i prerequisiti seguenti:
- La persona che aggiorna i percorsi di apprendimento deve essere il proprietario di una raccolta siti del catalogo app tenant. Se la persona che esegue il provisioning dei percorsi di apprendimento non è un proprietario della raccolta siti del catalogo app, [completare queste istruzioni](addappadmin.md) e continuare. 

## <a name="set-language-settings"></a>Impostare le impostazioni della lingua 
Prima di aggiornare i percorsi di apprendimento, impostare le impostazioni della lingua del sito. Per abilitare il supporto multilingue per il sito percorsi di apprendimento, è possibile impostare le **pagine e le notizie da tradurre in più lingue** **su**attivato e quindi aggiungere le lingue che si desidera supportare per il sito.
1.  Dal sito percorsi di apprendimento selezionare **Impostazioni** dall'alto a destra e quindi fare clic su **informazioni sito**.
2.  Nella parte inferiore del riquadro delle informazioni del sito selezionare **Visualizza tutte le impostazioni del sito**.
3.  In **Amministrazione sito**selezionare **Impostazioni lingua**.
4.  In **Enable Pages and News to be translated in multiple languages**, impostare l'interruttore toggle. 
- Per un sito di multiligual, scorrere l'interruttore **su**attivato e quindi passare alla sezione add languages. 
- Per un sito solo in lingua inglese, fare scorrere l'interruttore su **disattivata**.

### <a name="add-languages"></a>Aggiungere le lingue
I percorsi di apprendimento supportano nove lingue, è consigliabile aggiungere solo le lingue necessarie. Negli esempi utilizzati in questa documentazione verrà aggiunto italiano. 
- In **Aggiungi o Rimuovi lingue sito**, iniziare a digitare un nome di lingua in **Seleziona o digitare una**lingua oppure scegliere una lingua dall'elenco a discesa. È possibile ripetere questo passaggio per aggiungere più lingue. È possibile aggiungere o rimuovere le lingue dal sito in qualsiasi momento tornando alla pagina.
 
### <a name="assign-translators"></a>Assegnare i traduttori
Quando si definiscono le impostazioni della lingua per i percorsi di apprendimento, è possibile assegnare i traduttori. I traduttori devono disporre di un profilo di lingua straniera configurato. Per ulteriori informazioni sui profili di lingua straniera, vedere [creare siti di comunicazione multilingue, pagine e notizie](https://support.office.com/article/2bb7d610-5453-41c6-a0e8-6f40b3ed750c).  
- Per una lingua supportata, fare clic su **Seleziona o digitare un traduttore** e quindi selezionare un traduttore. 

## <a name="update-the-learning-pathways-web-part-package"></a>Aggiornare il pacchetto Web part percorsi di apprendimento
In questo passaggio viene caricata la Web part percorsi di apprendimento 4,0 nel catalogo app di SharePoint e quindi si passa alla pagina Amministrazione percorsi di apprendimento per avviare il processo di aggiornamento.

### <a name="upload-the-web-part-package"></a>Caricare il pacchetto della web part
1.  Passare al percorso di condivisione multilingue in teams e scaricare **customlearning. sppkg** in un'unità locale del PC. 
2.  Se non è già stato eseguito l'accesso, accedere al tenant con un account amministratore tenant o una raccolta siti. 
3.  Fare clic su **amministratore**per  >  **visualizzare tutte le**  >  **SharePoint**  >  **funzionalità**di SharePoint. 
4.  In **app**fare clic su **Apri**. 
5.  Fare clic su **App Catalog**  >  **distribuire le app per SharePoint**. 
6.  Fare clic su **carica**  >  **scegliere file**. 
7.  Selezionare il file **customlearning. sppkg** scaricato, fare clic su **OK**  >  **deploy**. 

### <a name="complete-the-update"></a>Completare l'aggiornamento
1.  Dal sito percorsi di apprendimento selezionare **Amministrazione percorsi di apprendimento** dal menu **Home** . 
2.  Verrà visualizzato un messaggio che richiede se si desidera eseguire l'aggiornamento. 
![custom_update_adminprompt_ml.png](media/custom_update_adminprompt_ml.png)
3.  Fare clic su **Avvia**. 
4. Al termine dell'aggiornamento, fare clic su **Chiudi**. 

### <a name="next-steps"></a>Operazioni successive
- Esaminare il [contenuto predefinito](custom_exploresite.md) fornito nel sito e nella web part.
- Per ulteriori informazioni sulla traduzione delle pagine del sito, vedere [translate site pages](custom_translate_page_ml.md). 

