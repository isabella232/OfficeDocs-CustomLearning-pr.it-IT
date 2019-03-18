---
author: pkrebs
ms.author: pkrebs
title: Risoluzione dei problemi di apprendimento personalizzato
ms.date: 02/10/2019
description: Informazioni su come risolvere i problemi di apprendimento personalizzato
ms.openlocfilehash: 7cbd049d4794d14f9e8cc26fd0db5f444812d688
ms.sourcegitcommit: 64721b7763d988d3b669eeab26fdb8b677ddc486
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/17/2019
ms.locfileid: "30658215"
---
# <a name="troubleshoot-custom-learning"></a>Risoluzione dei problemi di apprendimento personalizzato

Di seguito vengono forniti suggerimenti per la risoluzione dei problemi che possono verificarsi con l'apprendimento personalizzato per Office 365 o per il servizio di provisioning di SharePoint Online.

## <a name="how-to-know-if-you-have-tenant-admin-permissions"></a>Informazioni su come sapere se si dispone delle autorizzazioni di amministratore tenant

Accedere al servizio di provisioning di SharePoint Online e il provisioning di apprendimento personalizzato richiede autorizzazioni di amministratore tenant. Se si verificano problemi di accesso con il servizio di provisioning di SharePoint Online, assicurarsi di aver assegnato il ruolo di amministratore globale. La soluzione di apprendimento personalizzata richiede autorizzazioni di amministratore tenant, altrimenti noto come ruolo di amministratore globale di Office 365. Ecco come determinare se è stato assegnato il ruolo di amministratore globale.

1.  Accedere a Office.com.
2.  Fare clic su **amministratore**
3.  In **utenti**selezionare **utenti attivi**
4.  Cerca il tuo nome
5.  Fare clic sul proprio nome nei risultati della ricerca. L'amministratore globale dovrebbe essere visualizzato per il ruolo.

![CG-globaladminrole. png](media/cg-globaladminrole.png)

### <a name="if-you-dont-have-the-global-administrator-role"></a>Se non si ha il ruolo di amministratore globale
- Trovare un amministratore globale nell'organizzazione e fare in modo che l'utente esegua l'accesso al servizio o che disponga di un ruolo di amministratore globale.

## <a name="tenant-app-catalog-troubleshooting"></a>Risoluzione dei problemi relativi ai cataloghi delle app tenant
Per l'apprendimento personalizzato è necessario eseguire il provisioning di un catalogo app nel tenant di destinazione. La creazione di un catalogo app richiede autorizzazioni di amministratore globale. Di seguito vengono illustrati i passaggi per la risoluzione dei problemi comuni del catalogo delle app:

### <a name="how-to-know-if-you-have-a-tenant-app-catalog"></a>Informazioni su come sapere se si dispone di un catalogo app tenant 
Per iniziare, verificare di disporre delle autorizzazioni di amministratore globale. Vedere i passaggi per le autorizzazioni di amministratore tenant precedenti.

1. da Office 365, fare clic su **amministratore**, fare clic su espandi freccia >, fare clic su **mostra tutti i** > **centri** > di amministrazione di**SharePoint**.
2. Fare clic su**** > **Catalogo app**di **amministrazione di SharePoint Center** > classico.
3. In **app**, dovrebbe essere visualizzato un riquadro inTitolato **Distribuisci app per SharePoint**. Se viene visualizzato il riquadro, si dispone di un catalogo app tenant. Vedere la sezione **How to sure your are a site colllection...** . Se il riquadro non è visibile, sarà necessario creare un catalogo app tenant per il tenant. Vedere la sezione **come creare un catalogo app tenant di** seguito.

### <a name="how-to-ensure-you-are-a-site-collection-owner-on-the-tenant-app-catalog"></a>Come assicurarsi di essere proprietari di una raccolta siti nel catalogo app tenant 
Per eseguire il provisioning dell'apprendimento personalizzato per Office 365, è necessario essere proprietari di una raccolta siti nel catalogo app tenant. Ecco come determin se sei un proprietario.

1. da Office 365, fare clic su **amministratore**, fare clic su espandi freccia >, fare clic su **mostra tutti i** > **centri** > di amministrazione di**SharePoint**.
2. Fare clic su interfaccia di **amministrazione di SharePoint classica**, quindi selezionare il **Catalogo app**.
3. Selezionare **owner**e quindi assicurarsi di essere proprietari della raccolta siti. Dovrebbe avere un aspetto simile al seguente.
 
![CG-sitecollectionowner. png](media/cg-sitecollectionowner.png)

### <a name="how-to-create-a-tenant-app-catalog-if-one-doesnt-exists"></a>Come creare un catalogo app tenant se non esiste 
1. Accedere a Office 365 con l'account di amministratore di SharePoint Online.
2. Fare clic su **Amministratore**.
3. In interfaccia di **Amministrazione**, fare clic su **SharePoint**. 
4. Fare clic su**Catalogo app** **Apps** > .
5. Fare clic su **Crea un nuovo sito Catalogo app**e quindi fare clic su **OK**. 
6.  Immettere le informazioni per il catalogo app. Potrebbe essere necessario includere più di un amministratore. Di seguito viene illustrato un esempio.  

![CG-appcatalogfinish. png](media/cg-appcatalogfinish.png)

7.  Questo è tutto. Sei finito. Tuttavia, prima di passare al provisioning di apprendimento personalizzato, è necessario attendere almeno 30 minuti per assicurarsi che la creazione del catalogo app sia stata completata. 

> [!IMPORTANT]
> Attendere almeno 30 minuti dopo la creazione del catalogo app tenant prima del provisioning dell'apprendimento personalizzato. Questo garantisce che il processo di provisioning del catalogo app sia completo all'interno di SharePoint. 