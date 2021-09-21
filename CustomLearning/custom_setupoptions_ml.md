---
author: pkrebs
ms.author: pkrebs
title: Opzioni di installazione per percorsi di apprendimento multilingue
ms.date: 07/6/2020
description: Opzioni di installazione per percorsi di apprendimento multilingue
ROBOTS: NOINDEX, NOFOLLOW
ms.service: sharepoint-online
manager: bpardi
ms.topic: article
audience: admin
ms.openlocfilehash: b4f5b569e7c8395deaea8c436577fb630bce0668
ms.sourcegitcommit: 6005c2551bdea334767e6a056fdcb79533f2c858
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/21/2021
ms.locfileid: "59461165"
---
# <a name="setup-options-for-pathways-for-multilingual-learning"></a>Opzioni di installazione per percorsi di apprendimento multilingue
Con il rilascio di funzionalità multilingue per SharePoint siti di comunicazione online, i percorsi di apprendimento ora offrono supporto per più lingue. È possibile configurare percorsi di apprendimento in diversi modi per soddisfare le esigenze dell'organizzazione. Per aiutarti a decidere il percorso migliore per la tua organizzazione, abbiamo delineato le opzioni di installazione. 

## <a name="new-install-scenarios"></a>Nuovi scenari di installazione
I "nuovi scenari di installazione" illustrano le opzioni per l'installazione di una nuova istanza dei percorsi di apprendimento tramite il servizio di provisioning di SharePoint, ora disponibile dal manuale SharePoint look book.

### <a name="scenario-1-we-have-not-installed-learning-pathways-and-need-learning-pathways-multilingual-support"></a>Scenario 1: non sono stati installati percorsi di apprendimento e sono necessari percorsi di apprendimento per il supporto multilingue 
Se non sono stati installati percorsi di apprendimento e sono necessarie più lingue, è possibile utilizzare il servizio di provisioning di SharePoint per installare una nuova soluzione di percorsi di apprendimento con supporto per nove lingue. L'inglese sarà la lingua predefinita e non può essere modificato. 
- Per effettuare il provisioning di una nuova soluzione di percorsi di apprendimento con l'inglese come lingua predefinita per il sito, vedere Provisioning di una nuova soluzione [di percorsi di apprendimento.](custom_provision_ml.md)

### <a name="scenario-2-we-installed-learning-pathways-but-arent-currently-using-it-andor-havent-made-any-customization-to-the-site-or-playlists"></a>Scenario 2: sono stati installati percorsi di apprendimento ma non sono attualmente in uso e/o non è stata apportata alcuna personalizzazione al sito o alle playlist 
Se sono stati installati percorsi di apprendimento ma non vengono utilizzati attivamente o non sono state apportate personalizzazioni al sito o alle playlist, è possibile utilizzare il servizio di provisioning di SharePoint per installare una nuova soluzione con supporto per nove lingue. L'inglese sarà la lingua predefinita e non può essere modificato. 
- Per effettuare il provisioning di una nuova soluzione di percorsi di apprendimento con l'inglese come lingua predefinita per il sito, vedere Provisioning di una nuova soluzione [di percorsi di apprendimento.](custom_provision_ml.md)

### <a name="scenario-3-we-havent-installed-learning-pathways-and-dont-need-multilingual-support"></a>Scenario 3: non sono stati installati percorsi di apprendimento e non è necessario supporto multilingue 
Se non sono stati installati percorsi di apprendimento e non è necessario il supporto multilingue, è possibile installarlo dal SharePoint provisioning. L'inglese sarà la lingua predefinita. Dopo l'installazione, è necessario disattivare il supporto multilingue. 
- Per effettuare il provisioning di una nuova soluzione di percorsi di apprendimento senza supporto multilingue, vedere [Provisioning di una nuova soluzione di percorsi di apprendimento.](custom_provision_ml.md)

## <a name="update-learning-pathways-with-a-web-part-upload-scenarios"></a>Aggiornare gli scenari dei percorsi di apprendimento (con caricamento di web part)
Se è installata una versione esistente dei percorsi di apprendimento, è possibile caricare la web part percorsi di apprendimento nel Catalogo app di SharePoint per abilitare il supporto multilingue. 

### <a name="scenario-1-we-need-to-upgrade-an-existing-version-of-learning-pathways-but-dont-need-multilingual-support"></a>Scenario 1: è necessario aggiornare una versione esistente dei percorsi di apprendimento, ma non è necessario il supporto multilingue
È possibile aggiornare i percorsi di apprendimento versione 4.0 senza supporto multilingue. Con l'aggiornamento, ottieni un paio di nuove funzionalità, tra cui un selettore di immagine per playlist e sottocategorie personalizzate. 

- Per aggiornare una soluzione esistente di percorsi di apprendimento senza supporto multilingue, vedere Aggiornare i percorsi [di apprendimento per il supporto multilingue.](custom_update_ml.md) Il processo di aggiornamento per nessun supporto multilingue è lo stesso del supporto multilingue, ma con meno passaggi. 

### <a name="scenario-2-we-need-to-upgrade-to-multilingual-support-and-the-default-language-of-the-site-collection-is-our-default-language"></a>Scenario 2: è necessario eseguire l'aggiornamento al supporto multilingue e la lingua predefinita della raccolta siti è la lingua predefinita
Learning percorsi versione 4.O supporteranno le pagine multilingue nella raccolta siti. Oltre al supporto multilingue, ottieni un paio di nuove funzionalità, tra cui un selettore di immagine per playlist e sottocategorie personalizzate. 
- Per aggiornare un supporto multilingue per i percorsi di apprendimento esistenti, vedere Aggiornare i percorsi [di apprendimento per il supporto multilingue.](custom_update_ml.md) 

## <a name="update-learning-pathways-for-multilingual-support-with-manual-install"></a>Aggiornare i percorsi di apprendimento per il supporto multilingue con l'installazione manuale 
Di seguito vengono descritti gli scenari per l'aggiornamento di un'istanza esistente della soluzione dei percorsi di apprendimento alla versione multilingue versione 4.0 installando manualmente la web part percorsi di apprendimento. 

### <a name="scenario-1-we-need-multilingual-support-and-the-default-language-of-the-site-collection-is-not-our-default-language--no-custom-content"></a>Scenario 1: è necessario il supporto multilingue e la lingua predefinita della raccolta siti non è la lingua predefinita, ma nessun contenuto personalizzato 
Learning percorsi di distribuzione versione 4.0 supporteranno questo scenario. Tuttavia, questo scenario presuppone che tu non abbia contenuti o playlist personalizzati nel sito esistente. Per questo scenario, è possibile creare un nuovo sito di comunicazione di SharePoint Online con la lingua predefinita, caricare la web part e quindi configurare manualmente i percorsi di apprendimento con uno script di PowerShell. 
- Per configurare percorsi di apprendimento per il supporto multilingue con la lingua predefinita, vedere [Manual Install of Learning Pathways for multilingual support](custom_manualsetup_ml.md).

### <a name="scenario-2-we-need-multilingual-support-and-the-default-language-of-the-site-collection-is-not-our-default-language--plus-we-have-custom-content"></a>Scenario 2: è necessario il supporto multilingue e la lingua predefinita della raccolta siti non è la lingua predefinita, oltre a disporre di contenuto personalizzato 
Per questo scenario, è possibile creare un nuovo sito di comunicazione di SharePoint Online con la lingua predefinita, caricare la web part e quindi configurare manualmente i percorsi di apprendimento con uno script di PowerShell. 

Dopo aver ristabilito il sito dei percorsi di apprendimento seguendo i passaggi precedenti, dovrai spostare il contenuto dell'elenco **CustomPlaylists** e **dell'elenco CustomAssets.** Facoltativamente, puoi anche spostare le pagine personalizzate effettive che costituiscono gli asset personalizzati se si trova nel sito dei percorsi di apprendimento esistenti e l'intento è eliminarlo. L'attività può essere difficile perché per tutti gli elementi nell'elenco **CustomPlaylists,** l'ID della voce di elenco **nell'elenco CustomAssets** viene nascosto nel campo JSONData di ogni elemento dell'elenco di playlist. Pertanto, non sarà sufficiente spostare semplicemente il contenuto dell'elenco **CustomPlaylists** da un sito all'altro. Inoltre, **l'elenco CustomAssets** contiene l'URL assoluto della pagina dell'asset personalizzato nel campo JSONData dell'elemento di elenco. Se le risorse non vengono spostate e il sito non viene rinominato (modificando così l'URL assoluto nella pagina dell'asset), **CustomAssets** può rimanere. Sarà tuttavia necessario correggere manualmente le voci. Data la complessità di questo tipo di migrazione, ti consigliamo di prendere in considerazione l'integrazione di uno dei nostri partner dei percorsi di apprendimento per aiutarti a eseguire questa transizione.
- Per configurare percorsi di apprendimento per il supporto multilingue con la lingua predefinita, vedere [Manual Install of Learning Pathways for multilingual support](custom_manualsetup_ml.md).

