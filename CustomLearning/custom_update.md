---
author: pkrebs
ms.author: pkrebs
title: Aggiornare i percorsi di apprendimento di Microsoft 365
ms.date: 07/06/2020
description: Aggiornare i percorsi di apprendimento di Microsoft 365
ms.service: sharepoint-online
manager: bpardi
ms.topic: article
audience: admin
ms.openlocfilehash: daea2e2880c47a2ba5d961338e4f6d04c23b8e99
ms.sourcegitcommit: 152e8d7489c80beeb7d9ebfd04e6ef8ec7aed454
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/14/2021
ms.locfileid: "58350594"
---
# <a name="update-learning-pathways"></a>Aggiornare percorsi di apprendimento
Se si dispone di un sito Learning percorsi, è possibile aggiornarlo per il supporto multilingue. Per aggiornare i percorsi di apprendimento alla versione multilingue 4.0, caricare il pacchetto della web part, customlearning.sppkg, nel Catalogo app tenant di SharePoint. Quando aggiorni i percorsi di apprendimento:  

- Tutte le playlist e gli asset personalizzati creati in precedenza vengono mantenuti
- Impostazioni per nascondere o mostrare il contenuto vengono mantenuti
- I percorsi di apprendimento SharePoint modello rimangono invariati
- Le pagine del sito dei percorsi di apprendimento non vengono tradotte. Questa operazione deve essere eseguita manualmente

## <a name="read-the-learning-pathways-multilingual-overview"></a>Leggere la panoramica multilingue dei percorsi di apprendimento
Per informazioni sul funzionamento del supporto multilingue per i percorsi di apprendimento, leggere la Learning panoramica multilingue dei percorsi [multilingue.](custom_overview.md) 

## <a name="prerequisites-to-update"></a>Prerequisiti per l'aggiornamento
Prima di aggiornare i percorsi di apprendimento, è necessario che siano soddisfatti i prerequisiti seguenti:
- La persona che aggiorna i percorsi di apprendimento deve essere un proprietario della raccolta siti del Catalogo app tenant. Se la persona che provisioning percorsi di apprendimento non è un proprietario della raccolta siti del Catalogo app, [completare queste istruzioni](addappadmin.md) e continuare. 

## <a name="set-language-settings"></a>Impostare le impostazioni della lingua 
Prima di aggiornare i percorsi di apprendimento, imposta le impostazioni della lingua del sito. Per abilitare il supporto multilingue per il sito dei percorsi di apprendimento, è possibile impostare l'opzione Abilita la traduzione di pagine e **notizie in** più lingue su **Attivato** e quindi aggiungere le lingue che si desidera supportare per il sito.
1.  Nel sito Learning percorsi selezionare Impostazioni **dall'alto** a destra e quindi selezionare **Informazioni sito**.
2.  Nella parte inferiore del riquadro informazioni sito selezionare **Visualizza tutte le impostazioni del sito.**
3.  In **Amministrazione sito** selezionare Impostazioni **lingua.**
4.  In **Abilita la traduzione di pagine e notizie in più lingue** imposta l'interruttore attiva/disattiva. 
- Per un sito multiliguale, scorrere l'interruttore su **Attivato** e quindi passare alla sezione Aggiungi lingue. 
- Per un sito solo inglese, far scorrere l'interruttore su **Disattivato.**

### <a name="add-languages"></a>Aggiungere le lingue
Learning percorsi supporta nove lingue, è consigliabile aggiungere solo le lingue necessarie. Negli esempi utilizzati in questa documentazione verrà aggiunto l'italiano. 
- In **Aggiungere o rimuovere lingue del sito** iniziare a digitare un nome di lingua in Selezionare o **digitare** una lingua oppure scegliere una lingua nell'elenco a discesa. È possibile ripetere questo passaggio per aggiungere più lingue. È possibile aggiungere o rimuovere lingue dal sito in qualsiasi momento tornando a questa pagina.
 
### <a name="assign-translators"></a>Assegnare traduttori
Quando si definiscono le impostazioni della lingua per i percorsi di apprendimento, è possibile assegnare traduttori. I traduttori devono avere un profilo di lingua esterna configurato. Per ulteriori informazioni sui profili delle lingue straniere, vedere [Create multilingual communication sites, pages, and news](https://support.office.com/article/2bb7d610-5453-41c6-a0e8-6f40b3ed750c).  
- Per una lingua supportata, fare clic **su Seleziona o digita un traduttore** e quindi selezionare un traduttore. 

## <a name="update-the-learning-pathways-web-part-package"></a>Aggiornare il pacchetto web part percorsi di apprendimento
In questo passaggio, si carica la web part percorsi di apprendimento 4.0 nel Catalogo app di SharePoint e quindi si passa alla pagina Di amministrazione dei percorsi di apprendimento per avviare il processo di aggiornamento.

### <a name="upload-the-web-part-package"></a>Upload pacchetto web part
- Per le informazioni più aggiornate sull'aggiornamento della web part, vedere il file README Learning [pathways](https://github.com/pnp/custom-learning-office-365#updating-the-solution). 

### <a name="next-steps"></a>Operazioni successive
- Esplorare il [contenuto predefinito](custom_exploresite.md) fornito nel sito e nella web part.
- Per ulteriori informazioni sulla traduzione delle pagine del sito, vedere [Translate site pages](custom_translate_page_ml.md). 

