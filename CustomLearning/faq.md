---
author: karuanag
ms.author: karuanag
title: Domande frequenti per l'apprendimento personalizzato per le soluzioni di Office 365
ms.date: 02/10/2019
description: Informazioni sulle domande più frequenti per l'apprendimento personalizzato per Office 365
ms.openlocfilehash: 7da1f3da197fc298c83eac89e3455312cba7a851
ms.sourcegitcommit: 775d6807291ab263eea5ec649d9aaf1933fb41ca
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "32056009"
---
# <a name="frequently-asked-questions"></a>Domande frequenti

### <a name="1-what-are-the-requirements-for-installing-custom-learning-for-office-365-into-my-tenant-environment"></a>1. quali sono i requisiti per l'installazione dell'apprendimento personalizzato per Office 365 nell'ambiente tenant?

- SharePoint Online e i siti di comunicazione sono abilitati.
- L'individuo che dovrà eseguire il provisioning di CLO365 deve essere l'amministratore tenant del tenant di destinazione per l'installazione.
- Il tenant ' App Catalog ' deve essere disponibile all'interno dell'opzione ' Apps ' dell'interfaccia di amministrazione di SharePoint.
- L'individuo che dovrà eseguire il provisioning di CLO365 deve essere un amministratore della raccolta siti del catalogo app nel tenant di destinazione per l'installazione.

### <a name="2-what-languages-is-custom-learning-for-office-365-available-in"></a>2. in quale lingua è disponibile l'apprendimento personalizzato per Office 365?

L'apprendimento personalizzato per Office 365 è attualmente disponibile solo in inglese. Il provisioning finale automatico è compatibile solo con i tenant inglesi. È possibile aggiungere altre lingue nelle versioni future.

### <a name="3-how-long-will-it-take-to-install-the-site-in-our-tenant-environment"></a>3. quanto tempo è necessario per installare il sito nell'ambiente tenant?

In base al testing dell'installazione, dovrebbe essere necessario meno di 15 minuti. Questo non include il tempo necessario per personalizzare il sito in base alle proprie esigenze.

### <a name="4-can-we-make-the-custom-learning-for-office-365-a-subsite-of-our-primary-sharepoint-site-collection"></a>4. è possibile rendere l'apprendimento personalizzato per Office 365 un sito secondario della raccolta siti di SharePoint principale?

No. Il sito si basa su un modello di sito di comunicazione, che deve essere sempre costituito da una raccolta siti radice.

> [!NOTE]
> È importante prendere in considerazione le autorizzazioni necessarie per accedere al sito da parte degli utenti finali. La maggior parte delle organizzazioni ha definito i gruppi di sicurezza o di utenti. È necessario aggiungere i gruppi di sicurezza adeguati al nuovo portale di training dopo essere pronti a avviarlo nella community dei dipendenti.

### <a name="5-i-need-to-reinstall-the-site-what-should-i-do"></a>5. è necessario reinstallare il sito. Cosa dovrei fare?

Seguire le istruzioni per l'installazione pubblicate [qui](custom_provision.md).

> [!NOTE]
> Se la telemetria è stata disattivata nell'installazione precedente e si desidera continuare con la telemetria disattivata, sarà necessario seguire le istruzioni per disabilitare la telemetria.

### <a name="6-we-made-updates-to-our-implementation-of-custom-learning-for-office-365-will-we-lose-these-updates-made-to-site-template-playlists-if-we-reinstall-the-site"></a>6. sono stati apportati aggiornamenti alla nostra implementazione di apprendimento personalizzato per Office 365. Se si reinstalla il sito, verranno persi questi aggiornamenti (creati per il modello di sito, le playlist)?

Le personalizzazioni di singole pagine e playlist personalizzate andranno perse se si reinstalla il sito tramite l'installazione corrente.  