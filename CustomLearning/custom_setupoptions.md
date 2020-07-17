---
author: pkrebs
ms.author: pkrebs
title: Opzione di installazione per i percorsi di apprendimento
ms.date: 07/16/2020
description: Opzione di installazione per i percorsi di apprendimento
ms.openlocfilehash: 1434a06fbe5f374de7b2f2e4fa471a8eda5ac871
ms.sourcegitcommit: ba0cddd12dd8687ec4b97c26174fdda09de83b05
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/06/2020
ms.locfileid: "45043218"
---
# <a name="setup-options-for-multilingual-learning-pathways"></a>Opzioni di installazione per percorsi di apprendimento multilingue
Con il rilascio di funzionalità multilingue per i siti di comunicazione di SharePoint Online, i percorsi di apprendimento offrono ora il supporto per più lingue. È possibile configurare percorsi di apprendimento in diversi modi per soddisfare le esigenze dell'organizzazione. Per facilitare la scelta del percorso migliore per l'organizzazione, sono state descritte le opzioni di installazione. 

## <a name="new-install-scenarios"></a>Nuovi scenari di installazione
Gli "scenari di installazione nuovi" spiegano le opzioni per l'installazione di una nuova istanza dei percorsi di apprendimento tramite il servizio Microsoft 365 look book. 

### <a name="scenario-1-we-have-not-installed-learning-pathways-and-need-learning-pathways-multilingual-support"></a>Scenario 1: non sono stati installati percorsi di apprendimento e è necessario un supporto multilingue per i percorsi di apprendimento 
Se non sono stati installati percorsi di apprendimento e sono necessari più lingue, è possibile utilizzare il servizio Microsoft 365 look book per installare una nuova soluzione di percorsi di apprendimento con supporto per nove lingue. L'inglese sarà la lingua predefinita e non può essere modificata. 
- Per eseguire il provisioning di una nuova soluzione di percorsi di apprendimento con l'inglese come lingua predefinita per il sito, vedere [provisioning a New Learning pathways Solution](custom_provision.md).

### <a name="scenario-2-we-installed-learning-pathways-but-arent-currently-using-it-andor-havent-made-any-customization-to-the-site-or-playlists"></a>Scenario 2: i percorsi di apprendimento sono stati installati ma non sono attualmente in uso e/o non sono state apportate personalizzazioni al sito o alle playlist 
Se i percorsi di apprendimento sono stati installati ma non sono stati utilizzati attivamente oppure non sono state apportate personalizzazioni al sito o alle playlist, è possibile utilizzare il servizio Microsoft 365 look book per installare una nuova soluzione con supporto per nove lingue. L'inglese sarà la lingua predefinita e non può essere modificata. 
- Per eseguire il provisioning di una nuova soluzione di percorsi di apprendimento con l'inglese come lingua predefinita per il sito, vedere [provisioning a New Learning pathways Solution](custom_provision.md).

### <a name="scenario-3-we-havent-installed-learning-pathways-and-dont-need-multilingual-support"></a>Scenario 3: non sono stati installati percorsi di apprendimento e non è necessario il supporto multilingue 
Se non sono stati installati percorsi di apprendimento e non è necessario un supporto multilingue, è possibile installarlo dal servizio Microsoft 365 look book. L'inglese sarà la lingua predefinita. Dopo l'installazione, è necessario disattivare il supporto multilingue. 
- Per eseguire il provisioning di una nuova soluzione di percorsi di apprendimento senza supporto multilingue, vedere [provisioning an New Learning pathways Solution](custom_provision.md).

## <a name="update-learning-pathways-with-a-web-part-upload-scenarios"></a>Aggiornare i percorsi di apprendimento (con caricamento di una Web part)
Se è installata una versione esistente dei percorsi di apprendimento, è possibile caricare la Web part percorsi di apprendimento nel catalogo app di SharePoint per abilitare il supporto multilingue. 

### <a name="scenario-1-we-need-to-upgrade-an-existing-version-of-learning-pathways-but-dont-need-multilingual-support"></a>Scenario 1: è necessario aggiornare una versione esistente dei percorsi di apprendimento ma non è necessario il supporto multilingue
È possibile aggiornare i percorsi di apprendimento versione 4,0 senza supporto multilingue. Con l'aggiornamento, è possibile ottenere un paio di nuove funzionalità, tra cui un selettore di immagini per playlist e sottocategorie personalizzate. 

- Per aggiornare una soluzione di percorsi di apprendimento esistente senza supporto multilingue, vedere [Update Learning pathways for Multilingual Support](custom_update.md). Il processo di aggiornamento per nessun supporto multilingue è lo stesso del supporto multilingue, ma con meno passaggi. 

### <a name="scenario-2-we-need-to-upgrade-to-multilingual-support-and-the-default-language-of-the-site-collection-is-our-default-language"></a>Scenario 2: è necessario eseguire l'aggiornamento al supporto multilingue e la lingua predefinita della raccolta siti è la lingua predefinita
Percorsi di apprendimento la versione 4. O supporterà pagine multilingue nella raccolta siti. Oltre al supporto multilingue, è possibile ottenere un paio di nuove funzionalità, tra cui un selettore di immagini per playlist e sottocategorie personalizzate. 
- Per aggiornare i percorsi di apprendimento esistenti supporto multilingue del sito, vedere [Update Learning pathways for Multilingual Support](custom_update.md). 

## <a name="update-learning-pathways-for-multilingual-support-with-manual-install"></a>Aggiornare i percorsi di apprendimento per il supporto multilingue con installazione manuale 
Di seguito vengono illustrati gli scenari per l'aggiornamento di un'istanza esistente della soluzione di percorsi di apprendimento alla versione multilingue versione 4,0, installando manualmente la Web part percorsi di apprendimento. 

### <a name="scenario-1-we-need-multilingual-support-and-the-default-language-of-the-site-collection-is-not-our-default-language--no-custom-content"></a>Scenario 1: è necessario il supporto multilingue e la lingua predefinita della raccolta siti non è la lingua predefinita – nessun contenuto personalizzato 
Percorsi di apprendimento la versione 4,0 sosterrà questo scenario. Tuttavia, in questo scenario si presuppone che non vi siano contenuti o elenchi di riproduzione personalizzati nel sito esistente. Per questo scenario, è possibile creare un nuovo sito di comunicazione di SharePoint Online con la lingua predefinita, caricare la Web part e quindi configurare manualmente i percorsi di apprendimento con uno script di PowerShell. 
- Per impostare percorsi di apprendimento per il supporto multilingue con la lingua predefinita, vedere [Manual Install of Learning pathways for Multilingual Support](custom_manualsetup.md).

### <a name="scenario-2-we-need-multilingual-support-and-the-default-language-of-the-site-collection-is-not-our-default-language--plus-we-have-custom-content"></a>Scenario 2: è necessario un supporto multilingue e la lingua predefinita della raccolta siti non è la lingua predefinita, oltre al contenuto personalizzato 
Per questo scenario, è possibile creare un nuovo sito di comunicazione di SharePoint Online con la lingua predefinita, caricare la Web part e quindi configurare manualmente i percorsi di apprendimento con uno script di PowerShell. 

Dopo aver ristabilito il sito dei percorsi di apprendimento seguendo la procedura descritta in alto, è necessario spostare i contenuti dell'elenco di **CustomPlaylists** e dell'elenco di **CustomAssets** . È anche possibile, facoltativamente, spostare le pagine personalizzate effettive che compongono le risorse personalizzate se sono presenti nel sito percorsi di apprendimento esistente e l'intenzione è di eliminarla. L'attività può essere difficile perché per tutti gli elementi nell'elenco **CustomPlaylists** , l'ID della voce di elenco nell'elenco **CustomAssets** è sepolto nel campo JSONData di ogni voce di elenco di playlist. Pertanto, semplicemente spostando il contenuto dell'elenco **CustomPlaylists** da un sito all'altro non sarà sufficiente. Inoltre, l'elenco **CustomAssets** contiene l'URL assoluto della pagina del cespite personalizzato nel campo JSONData della voce di elenco. Se le risorse non vengono spostate e il sito non viene rinominato (cambiando così l'URL assoluto della pagina del cespite), **CustomAssets** può rimanere. Tuttavia, sarà necessario correggere manualmente le voci. Data la complessità di questo tipo di migrazione, è consigliabile prendere in considerazione l'arruolamento di uno dei nostri partner di percorsi di apprendimento per facilitare la transizione.
- Per impostare percorsi di apprendimento per il supporto multilingue con la lingua predefinita, vedere [Manual Install of Learning pathways for Multilingual Support](custom_manualsetup.md).