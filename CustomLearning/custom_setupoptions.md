---
author: pkrebs
ms.author: pkrebs
title: Opzioni di installazione di Microsoft 365 Learning pathways
ms.date: 02/11/2019
description: Opzione di installazione per l'installazione di apprendimento personalizzato
ms.openlocfilehash: 6906b5e70b186c106b3a9969b5bce1cbe87d7021
ms.sourcegitcommit: f4c2b6ef531d2d820c3d97871e187d0a2220d8f4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2019
ms.locfileid: "37956653"
---
# <a name="learning-pathways-setup-options"></a>Opzioni di installazione percorsi di apprendimento
I percorsi di apprendimento offrono la flessibilità necessaria per configurare la soluzione in un paio di modi diversi. Nelle sezioni seguenti vengono illustrate le opzioni disponibili.

> [!IMPORTANT]
> Se è già stato effettuato il provisioning di apprendimento personalizzato per Office 365 nell'organizzazione e si desidera aggiornare la soluzione, seguire le istruzioni "Updating the Solution" nel [file Leggimi di Microsoft 365 Learning pathways](https://github.com/pnp/custom-learning-office-365). Se si desidera eseguire il provisioning dei percorsi di apprendimento di Microsoft 365 per la prima volta, vedere [provision microsoft 365 Learning pathways instructions]( https://docs.microsoft.com/en-us/office365/customlearning/custom_provision) nella documentazione relativa ai percorsi di apprendimento di Microsoft 365.  


## <a name="recommended---sharepoint-online-provisioning-service-setup"></a>Procedura consigliata: installazione del servizio di provisioning di SharePoint Online 
Il servizio di provisioning di SharePoint Online offre il metodo più rapido, semplice e consigliato per la configurazione dell'apprendimento personalizzato. Con il servizio di provisioning di SharePoint Online, un amministratore di Office 365 tenant accede al servizio, effettua alcune scelte e fa clic su **Aggiungi al tenant** per eseguire il provisioning del sito di apprendimento personalizzato e della web part di apprendimento personalizzata. Quando si esegue il provisioning, l'amministratore del tenant riceve un messaggio di posta elettronica che il sito è pronto per l'esecuzione. 

- Per iniziare a utilizzare il servizio di provisioning di SharePoint, andare a provisioning [con il servizio di provisioning PNP](custom_provision.md) .   

## <a name="stand-alone-learning-pathways-web-part-setup"></a>Configurazione della web part percorsi di apprendimento stand alone
Per le organizzazioni che già dispongono di un portale di formazione per la comunicazione moderna di SharePoint Online, i percorsi di apprendimento offrono la possibilità di installare manualmente la Web part Microsoft 365 Learning pathways in un sito di SharePoint Online esistente. Si noti che il sito deve essere un sito di SharePoint Online moderno. Questo metodo richiede autorizzazioni di amministratore tenant e esperienza con Windows PowerShell o SharePoint Online Management Shell. Si noti che questo metodo richiede un'esperienza più tecnica e quindi la configurazione del servizio di provisioning di SharePoint Online.

- Per istruzioni sull'installazione di Web part manuali, vedere Manual [Install the Web part](custom_manualsetup.md). 

## <a name="update-learning-pathways"></a>Aggiornare i percorsi di apprendimento
Le organizzazioni che hanno utilizzato il servizio di provisioning di SharePoint Online per installare le versioni precedenti dei percorsi di apprendimento di Microsoft 365 possono aggiornare la soluzione alla versione più recente. Per istruzioni su come verificare la versione distribuita rispetto alla versione più recente della soluzione, insieme alle istruzioni su come aggiornare la soluzione, vedere la sezione "Updating the Solution" del [file Readme](https://github.com/pnp/custom-learning-office-365/blob/master/README.md).

### <a name="next-steps---provision-microsoft-365-learning-pathwayscustom_provisionmd"></a>Passaggi successivi- [provisioning di Microsoft 365 Learning pathways](custom_provision.md)
