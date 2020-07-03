---
author: pkrebs
ms.author: pkrebs
title: Opzioni di installazione per percorsi di apprendimento multilingue
ms.date: 07/6/2020
description: Opzioni di installazione per percorsi di apprendimento multilingue
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: e9e2c74f366dedf8e0010a01797aedb3c3316fa4
ms.sourcegitcommit: 1f080ed4cf3687f922907304db3fd7a06aa9d501
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/02/2020
ms.locfileid: "45031692"
---
# <a name="setup-options-for-multilingual-learning-pathways"></a>Opzioni di installazione per percorsi di apprendimento multilingue
Con il rilascio di funzionalità multilingue per i siti di comunicazione di SharePoint Online, i percorsi di apprendimento offrono ora il supporto per più lingue. Il modo in cui si configurano i percorsi di apprendimento per il supporto multilingue dipenderà dalle esigenze dell'organizzazione. Per facilitare la scelta del percorso migliore per l'organizzazione, sono stati descritti i possibili scenari.

## <a name="new-install-scenarios"></a>Nuovi scenari di installazione
Di seguito vengono illustrati gli scenari per l'installazione di una nuova istanza della soluzione per i percorsi di apprendimento utilizzando il servizio di provisioning di SharePoint, ora disponibile nell'elenco di ricerca di SharePoint.

### <a name="scenario-1-we-have-not-installed-learning-pathways-and-need-learning-pathways-multilingual-support"></a>Scenario 1: non sono stati installati percorsi di apprendimento e è necessario un supporto multilingue per i percorsi di apprendimento 
Se non sono stati installati percorsi di apprendimento e sono necessari più lingue, è possibile utilizzare il servizio di provisioning di SharePoint per creare un nuovo sito di percorsi di apprendimento in nove lingue. L'inglese sarà la lingua predefinita e non può essere modificata. 
- Per eseguire il provisioning di una nuova soluzione di percorsi di apprendimento con l'inglese come lingua predefinita per il sito, vedere [provisioning a New Learning pathways Solution](custom_provision_ml.md).

### <a name="scenario-2-we-installed-learning-pathways-but-arent-currently-using-it-andor-havent-made-any-customization-to-the-site-or-playlists"></a>Scenario 2: i percorsi di apprendimento sono stati installati ma non sono attualmente in uso e/o non sono state apportate personalizzazioni al sito o alle playlist 
Se sono stati installati percorsi di apprendimento ma non sono stati utilizzati attivamente o se non sono state apportate personalizzazioni al sito o alle playlist, è possibile utilizzare il servizio di provisioning di SharePoint per creare un nuovo sito in nove lingue. L'inglese sarà la lingua predefinita e non può essere modificata. 
- Per eseguire il provisioning di una nuova soluzione di percorsi di apprendimento con l'inglese come lingua predefinita per il sito, vedere [provisioning a New Learning pathways Solution](custom_provision_ml.md).

### <a name="scenario-3-we-have-not-installed-learning-pathways-and-dont-need-multilingual-support"></a>Scenario 3: non sono stati installati percorsi di apprendimento e non è necessario un supporto multilingue 
Se non sono stati precedentemente installati percorsi di apprendimento e non è necessario il supporto multilingue, è possibile eseguire il provisioning dei percorsi di apprendimento dal servizio di provisioning di SharePoint. L'inglese sarà la lingua predefinita. Dopo l'installazione, sarà necessario disattivare il supporto multilingue. 
- Per eseguire il provisioning di una nuova soluzione di percorsi di apprendimento senza supporto multilingue, vedere [provisioning an New Learning pathways Solution](custom_provision_ml.md).

## <a name="update-learning-pathways-with-web-part-upload-scenarios"></a>Aggiornare i percorsi di apprendimento con gli scenari di caricamento delle web part
Di seguito vengono illustrati gli scenari per l'aggiornamento di un'istanza esistente della soluzione di percorsi di apprendimento alla versione multilingue di 4,0. In questo scenario, è possibile caricare la Web part percorsi di apprendimento nel catalogo app di SharePoint.

### <a name="scenario-1-we-need-to-upgrade-an-existing-version-of-learning-pathways-but-do-not-need-multilingual-support"></a>Scenario 1: è necessario aggiornare una versione esistente dei percorsi di apprendimento ma non è necessario il supporto multilingue
È possibile eseguire l'aggiornamento a percorsi di apprendimento versione 4,0 senza supporto multilingue. Con l'aggiornamento, è possibile ottenere un paio di nuove funzionalità che possono essere utili per l'utente, tra cui un selettore di immagini per la scelta dell'immagine per un elenco di riproduzione personalizzato e una sottocategoria personalizzata. 

- Per aggiornare un sito di percorsi di apprendimento esistente senza supporto multilingue, vedere [Update Learning pathways for Multilingual Support](custom_update_ml.md). Il processo di aggiornamento per nessun supporto multilingue è lo stesso del supporto multilingue, ma con meno passaggi. 

### <a name="scenario-2-we-need-to-upgrade-to-multilingual-support-and-the-default-language-of-the-site-collection-is-our-default-language"></a>Scenario 2: è necessario eseguire l'aggiornamento al supporto multilingue e la lingua predefinita della raccolta siti è la lingua predefinita
Percorsi di apprendimento la versione 4. O sosterrà la caratteristica pagine multilingue nella raccolta siti. Oltre al supporto multilingue, è possibile ottenere un paio di aggiornamenti che possono essere utili per la scelta dell'immagine di un selettore di immagini per scegliere l'immagine di una playlist personalizzata e l'aggiunta di un'interfaccia utente per la modifica dell'immagine predefinita in una sottocategoria personalizzata. 
- Per aggiornare i percorsi di apprendimento esistenti supporto multilingue del sito, vedere [Update Learning pathways for Multilingual Support](custom_update_ml.md). 

## <a name="update-learning-pathways-for-multilingual-support-with-manual-install"></a>Aggiornare i percorsi di apprendimento per il supporto multilingue con installazione manuale 
Di seguito vengono illustrati gli scenari per l'aggiornamento di un'istanza esistente della soluzione di percorsi di apprendimento alla versione multilingue versione 4,0, installando manualmente la Web part percorsi di apprendimento. 

### <a name="scenario-1-we-need-multilingual-support-and-the-default-language-of-the-site-collection-is-not-our-default-language--no-custom-content"></a>Scenario 1: è necessario il supporto multilingue e la lingua predefinita della raccolta siti non è la lingua predefinita – nessun contenuto personalizzato 
Percorsi di apprendimento la versione 4,0 sosterrà questo scenario. Tuttavia, in questo scenario si presuppone che non vi siano contenuti o elenchi di riproduzione personalizzati nel sito esistente. Per questo scenario, è possibile creare un nuovo sito di comunicazione di SharePoint Online con la lingua predefinita, caricare la Web part e quindi configurare manualmente i percorsi di apprendimento con uno script di PowerShell. 
- Per aggiornare i percorsi di apprendimento per il supporto multilingue con la lingua predefinita, vedere **Manual Install of Learning pathways for Multilingual Support**.

### <a name="scenario-2-we-need-multilingual-support-and-the-default-language-of-the-site-collection-is-not-our-default-language--plus-we-have-custom-content"></a>Scenario 2: è necessario un supporto multilingue e la lingua predefinita della raccolta siti non è la lingua predefinita, oltre al contenuto personalizzato 
Per questo scenario, è possibile creare un nuovo sito di comunicazione di SharePoint Online con la lingua predefinita, caricare la Web part e quindi configurare manualmente i percorsi di apprendimento con uno script di PowerShell. Dopo aver ristabilito il sito dei percorsi di apprendimento seguendo la procedura descritta in alto, è necessario spostare i contenuti dell'elenco di **CustomPlaylists** e dell'elenco di **CustomAssets** . È anche possibile, facoltativamente, spostare le pagine personalizzate effettive che compongono le risorse personalizzate se sono presenti nel sito percorsi di apprendimento esistente e l'intenzione è di eliminarla. L'attività può essere difficile perché per tutti gli elementi nell'elenco **CustomPlaylists** , l'ID della voce di elenco nell'elenco **CustomAssets** è sepolto nel campo JSONData di ogni voce di elenco di playlist. Pertanto, semplicemente spostando il contenuto dell'elenco **CustomPlaylists** da un sito all'altro non sarà sufficiente. Inoltre, l'elenco **CustomAssets** contiene l'URL assoluto della pagina del cespite personalizzato nel campo JSONData della voce di elenco. Se le risorse non vengono spostate e il sito non viene rinominato (cambiando così l'URL assoluto della pagina del cespite), **CustomAssets** può rimanere. Tuttavia, sarà necessario correggere manualmente le voci. Data la complessità di questo tipo di migrazione, è consigliabile prendere in considerazione l'arruolamento di uno dei nostri partner di percorsi di apprendimento per facilitare la transizione.
- Per aggiornare i percorsi di apprendimento per il supporto multilingue con la lingua predefinita, vedere **Manual Install of Learning pathways for Multilingual Support**.

