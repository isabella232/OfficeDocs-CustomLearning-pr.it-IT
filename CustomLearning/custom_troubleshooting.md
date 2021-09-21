---
author: pkrebs
ms.author: pkrebs
title: Risolvere i problemi dei percorsi di apprendimento di Microsoft 365
ms.date: 02/10/2019
description: Informazioni su come risolvere i Microsoft 365 di apprendimento
ms.service: sharepoint-online
manager: bpardi
ms.topic: article
ms.openlocfilehash: 2afaaf8291f284b641172e816c4a3946fa8145e8
ms.sourcegitcommit: 6005c2551bdea334767e6a056fdcb79533f2c858
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/21/2021
ms.locfileid: "59461145"
---
# <a name="troubleshoot-microsoft-365-learning-pathways"></a>Risolvere i Microsoft 365 percorsi di apprendimento

Ecco i suggerimenti per la risoluzione dei problemi che possono verificarsi Microsoft 365 percorsi di apprendimento o SharePoint Online Provisioning Service.

## <a name="how-to-know-if-you-have-tenant-admin-permissions"></a>Come sapere se si dispone delle autorizzazioni di amministratore tenant

Accedere al servizio di provisioning SharePoint Online e provisioning Learning richiede autorizzazioni di amministratore tenant. Se si verificano problemi di accesso con il servizio di provisioning SharePoint Online, assicurarsi di avere assegnato il ruolo amministratore globale. La soluzione Learning personalizzata richiede autorizzazioni di amministratore tenant, altrimenti noto come Office 365 amministratore globale. Ecco come determinare se è stato assegnato il ruolo amministratore globale.

1.  Accedi a Office.com.
2.  Fare clic **su Amministratore**
3.  In **Utenti** selezionare **Utenti attivi**
4.  Cercare il proprio nome
5.  Fare clic sul proprio nome nei risultati della ricerca. Dovrebbe essere visualizzato Amministratore globale per il proprio ruolo.

![Amministratore globale per il ruolo](media/cg-globaladminrole.png)

### <a name="if-you-dont-have-the-global-administrator-role"></a>Se non si dispone del ruolo amministratore globale
- Trovare un amministratore globale nell'organizzazione e fare in modo che la persona a cui accede il servizio o che gli assegni il ruolo di amministratore globale.

## <a name="tenant-app-catalog-troubleshooting"></a>Risoluzione dei problemi del Catalogo app tenant
Il Learning richiede il provisioning di un Catalogo app nel tenant di destinazione. La creazione di un catalogo app richiede autorizzazioni di amministratore globale. Ecco i passaggi per la risoluzione dei problemi comuni del Catalogo app:

### <a name="how-to-know-if-you-have-a-tenant-app-catalog"></a>Come sapere se si dispone di un catalogo app tenant 
Per iniziare, assicurarsi di disporre delle autorizzazioni di amministratore globale. Vedi i passaggi per le autorizzazioni di amministratore tenant sopra riportate.

1. Da Office 365, fare clic **su Amministratore,** fare clic sulla freccia di espansione >, fare clic su **Mostra** tutte le SharePoint  >    >  .
2. Fare **clic su Catalogo app SharePoint Centro**  >  **amministrazione**  >  **classico**.
3. In **App** dovrebbe essere visualizzato un riquadro inTitolato **Distribuisci app per SharePoint.** Se viene visualizzato il riquadro, si dispone di un Catalogo app tenant. Vedi la sezione Come garantire che i tuoi siti siano una **colllezione del sito...** di seguito. Se non vedi il riquadro, dovrai creare un catalogo app tenant per il tenant. Vedi la **sezione Come creare un Catalogo app tenant di** seguito.

### <a name="how-to-ensure-you-are-a-site-collection-owner-on-the-tenant-app-catalog"></a>Come assicurarsi di essere proprietari di una raccolta siti nel Catalogo app tenant 
Per eseguire Microsoft 365 percorsi di apprendimento, è necessario essere proprietari di una raccolta siti nel Catalogo app tenant. Ecco come determinare se sei un proprietario.

1. Da Office 365, fare clic **su Amministratore,** fare clic sulla freccia di espansione >, fare clic su **Mostra** tutte le SharePoint  >    >  .
2. Fai **clic su SharePoint Center classico** e quindi seleziona il catalogo **app.**
3. Selezionare **Proprietario** e quindi assicurarsi di essere un proprietario della raccolta siti. Dovrebbe essere simile al seguente.
 
![Proprietario della raccolta siti](media/cg-sitecollectionowner.png)

### <a name="how-to-create-a-tenant-app-catalog-if-one-doesnt-exists"></a>Come creare un Catalogo app tenant se non ne esiste uno 
1. Accedi a Office 365 con il tuo account SharePoint amministratore di SharePoint Online.
2. Fare clic su **Amministratore**.
3. In **Interfaccia di amministrazione** fare clic su **SharePoint**. 
4. Fare **clic su** Catalogo app app  >  **app**.
5. Fare **clic su Crea un nuovo sito catalogo app** e quindi su **OK.** 
6.  Immetti le informazioni per il Catalogo app. È possibile includere più di un amministratore. Di seguito viene illustrato un esempio.  

![Completare l'immissione delle informazioni per il catalogo app](media/cg-appcatalogfinish.png)

7.  Questo è tutto. Hai finito. Ma prima di passare al provisioning Learning, è necessario attendere almeno 30 minuti per assicurarsi che la creazione del Catalogo app sia stata completata. 

> [!IMPORTANT]
> Attendere almeno 30 minuti dopo aver creato il Catalogo app tenant prima di eseguire il provisioning di Learning. In questo modo si garantisce che il processo di provisioning del Catalogo app sia completo entro SharePoint. 