---
author: karuanag
ms.author: karuanag
title: Domande frequenti per apprendere come personalizzato soluzioni per Office 365
ms.date: 02/10/2019
description: Domande frequenti informazioni di domande per l'apprendimento personalizzato per Office 365
ms.openlocfilehash: d8b5104e8feeaa4e70296f61594233b27363481b
ms.sourcegitcommit: f93a6a691331515ba10f4d43b491928ec268f0ec
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2019
ms.locfileid: "29952625"
---
# <a name="frequently-asked-questions"></a>Domande frequenti

### <a name="1-what-are-the-requirements-for-installing-custom-learning-for-office-365-into-my-tenant-environment"></a>1. che cosa sono i requisiti per l'installazione di apprendimento personalizzato per Office 365 in ambiente tenant?

- SharePoint Online e abilitate nei siti di comunicazione.
- La persona che provisioning di CLO365 deve essere l'amministratore tenant del tenant di destinazione per l'installazione.
- Un tenant 'App Catalog' deve essere disponibile all'interno dell'opzione "Apps" dell'interfaccia di amministrazione di SharePoint.
- La persona che provisioning di CLO365 deve essere un amministratore della raccolta siti del catalogo app nel tenant di destinazione per l'installazione.

### <a name="2-what-languages-is-custom-learning-for-office-365-available-in"></a>2. quali lingue è disponibile in apprendimento personalizzato per Office 365?

Personalizzata di formazione per Office 365 è attualmente disponibile solo in inglese. Il provisioning automatico end-to-end funziona solo con tenant inglese. Lingue aggiuntive possono essere aggiunti nelle future versioni.

### <a name="3-how-long-will-it-take-to-install-the-site-in-our-tenant-environment"></a>3. per quanto tempo è necessario installare il sito nell'ambiente di tenant?

Test dell'installazione di base, richiede meno di 15 minuti. Non si include tempo necessario per personalizzare il sito in base ai requisiti.

### <a name="4-can-we-make-the-custom-learning-for-office-365-a-subsite-of-our-primary-sharepoint-site-collection"></a>4. possibile rendere personalizzato di formazione per Office 365 un sito secondario dei nostri principale raccolta siti di SharePoint?

No. Il sito è basato su un modello di sito di comunicazione, in genere sempre in una raccolta siti radice.

> [!NOTE]
> È importante prendere in considerazione le autorizzazioni che agli utenti finali sarà necessario per accedere al sito. La maggior parte delle organizzazioni sono definite gruppi di sicurezza o un utente. Quando si è pronti per l'avvio, alla Comunità dei dipendenti, è necessario aggiungere gruppi di protezione appropriati per il nuovo portale dedicato alla formazione.

### <a name="5-i-need-to-reinstall-the-site-what-should-i-do"></a>5. necessario reinstallare il sito. Cosa dovrei fare?

Eseguire l'installazione istruzioni pubblicato [di seguito](installsitepackage.md).

> [!NOTE]
> Se si era disattivato telemetria nell'installazione precedente e per continuare con telemetrico disabilitato, è necessario seguire le istruzioni per la disattivazione di telemetria di seguito.

### <a name="6-we-made-updates-to-our-implementation-of-custom-learning-for-office-365-will-we-lose-these-updates-made-to-site-template-playlists-if-we-reinstall-the-site"></a>6. apportate aggiornamenti per l'implementazione di apprendimento personalizzato per Office 365. Se si reinstalla il sito, è andranno persi questi aggiornamenti (apportati al modello di sito, gli elenchi di riproduzione)?

Le personalizzazioni di singole pagine e gli elenchi di riproduzione personalizzato andranno persi se si reinstalla il sito tramite l'installazione corrente.  