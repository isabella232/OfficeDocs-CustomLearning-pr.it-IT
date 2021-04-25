---
author: pkrebs
ms.author: pkrebs
title: Aggiornare i percorsi di apprendimento per il supporto multilingue
ms.date: 05/20/2019
description: Aggiornare i percorsi di apprendimento per il supporto multilingue
ROBOTS: NOINDEX, NOFOLLOW
ms.service: sharepoint-online
manager: bpardi
ms.topic: article
audience: admin
ms.openlocfilehash: 9344cd91e5b6718b1eb0e73e25fdc8311afed793
ms.sourcegitcommit: 97e175e5ff5b6a9e0274d5ec9b39fdf7e18eb387
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/25/2021
ms.locfileid: "52000242"
---
# <a name="update-learning-pathways-for-multilingual-support"></a>Aggiornare i percorsi di apprendimento per il supporto multilingue
Se si dispone di un sito percorsi di apprendimento esistente, è possibile aggiornarlo per il supporto multilingue. Per aggiornare i percorsi di apprendimento alla versione multilingue 4.0, caricare il pacchetto della web part, customlearning.sppkg, nel Catalogo app tenant di SharePoint. Quando aggiorni i percorsi di apprendimento:  

- Tutte le playlist e gli asset personalizzati creati in precedenza vengono mantenuti
- Vengono mantenute le impostazioni per nascondere o visualizzare il contenuto
- Il modello di SharePoint percorsi di apprendimento rimane invariato
- Le pagine del sito dei percorsi di apprendimento non vengono tradotte. Questa operazione deve essere eseguita manualmente

## <a name="read-the-learning-pathways-multilingual-overview"></a>Leggere la panoramica multilingue dei percorsi di apprendimento
Per informazioni sul funzionamento del supporto multilingue per i percorsi di apprendimento, leggere [panoramica multilingue](custom_overview_ml.md)percorsi di apprendimento . 

## <a name="prerequisites-to-update"></a>Prerequisiti per l'aggiornamento
Prima di aggiornare i percorsi di apprendimento, è necessario che siano soddisfatti i prerequisiti seguenti:
- La persona che aggiorna i percorsi di apprendimento deve essere un proprietario della raccolta siti del Catalogo app tenant. Se la persona che provisioning percorsi di apprendimento non è un proprietario della raccolta siti del Catalogo app, [completare queste istruzioni](addappadmin.md) e continuare. 

## <a name="set-language-settings"></a>Impostare le impostazioni della lingua 
Prima di aggiornare i percorsi di apprendimento, imposta le impostazioni della lingua del sito. Per abilitare il supporto multilingue per il sito dei percorsi di apprendimento, è possibile impostare l'opzione Abilita la traduzione di pagine e **notizie in** più lingue su **Attivato** e quindi aggiungere le lingue che si desidera supportare per il sito.
1.  Nel sito Percorsi di apprendimento seleziona **Impostazioni** in alto a destra e quindi seleziona **Informazioni sito.**
2.  Nella parte inferiore del riquadro informazioni sito selezionare **Visualizza tutte le impostazioni del sito.**
3.  In **Amministrazione sito** selezionare Impostazioni **lingua.**
4.  In **Abilita la traduzione di pagine e notizie in più lingue** imposta l'interruttore attiva/disattiva. 
- Per un sito multiliguale, scorrere l'interruttore su **Attivato** e quindi passare alla sezione Aggiungi lingue. 
- Per un sito solo in inglese, fai scorrere l'interruttore su **Disattivato.**

### <a name="add-languages"></a>Aggiungere le lingue
I percorsi di apprendimento supportano nove lingue, è consigliabile aggiungere solo le lingue necessarie. Negli esempi utilizzati in questa documentazione verrà aggiunto l'italiano. 
- In **Aggiungere o rimuovere lingue del sito** iniziare a digitare un nome di lingua in **Selezionare** o digitare una lingua oppure scegliere una lingua nell'elenco a discesa. È possibile ripetere questo passaggio per aggiungere più lingue. È possibile aggiungere o rimuovere lingue dal sito in qualsiasi momento tornando a questa pagina.
 
### <a name="assign-translators"></a>Assegnare traduttori
Quando si definiscono le impostazioni della lingua per i percorsi di apprendimento, è possibile assegnare traduttori. I traduttori devono avere un profilo di lingua esterna configurato. Per ulteriori informazioni sui profili delle lingue straniere, vedere [Create multilingual communication sites, pages, and news](https://support.office.com/article/2bb7d610-5453-41c6-a0e8-6f40b3ed750c).  
- Per una lingua supportata, fare clic **su Seleziona o digita un traduttore** e quindi selezionare un traduttore. 

## <a name="update-the-learning-pathways-web-part-package"></a>Aggiornare il pacchetto web part percorsi di apprendimento
In questo passaggio la web part percorsi di apprendimento 4.0 viene caricata nel Catalogo app di SharePoint e quindi si passa alla pagina Di amministrazione dei percorsi di apprendimento per avviare il processo di aggiornamento.

### <a name="upload-the-web-part-package"></a>Caricare il pacchetto web part
1.  Vai all'archivio di apprendimento personalizzato [GitHub,](https://github.com/pnp/custom-learning-office-365/tree/master/webpart)seleziona **customlearning.sppkg** e quindi scaricalo in un'unità locale nel PC. 
2.  Se non è ancora stato eseguito l'accesso, accedere al tenant con un account di amministratore tenant o amministratore della raccolta siti. 
3.  Fare **clic su Admin** Show  >  **All**  >  **SharePoint** More  >  **Features**. 
4.  In **App** fare clic su **Apri.** 
5.  Fare **clic su Catalogo app**  >  **Distribuisci app per SharePoint.** 
6.  Fare **clic su Carica** Scegli  >  **file**. 
7.  Selezionare il file **customlearning.sppkg** scaricato, fare clic su **OK**  >  **Distribuisci.** 

### <a name="complete-the-update"></a>Completare l'aggiornamento
1.  Nel sito Percorsi di apprendimento seleziona **Amministrazione percorsi di apprendimento** dal menu **Home.** 
2.  Verrà visualizzato un prompt che richiede se si desidera eseguire l'aggiornamento. 
![custom_update_adminprompt_ml.png](media/custom_update_adminprompt_ml.png)
3.  Fare clic su **Avvia**. 
4. Al termine dell'aggiornamento, fare clic su **Chiudi**. 

### <a name="next-steps"></a>Operazioni successive
- Esplorare il [contenuto predefinito](custom_exploresite.md) fornito nel sito e nella web part.
- Per ulteriori informazioni sulla traduzione delle pagine del sito, vedere [Translate site pages](custom_translate_page_ml.md). 

