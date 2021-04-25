---
author: pkrebs
ms.author: pkrebs
title: Tradurre pagine del sito
ms.date: 07/06/2020
description: Tradurre pagine del sito
ms.service: sharepoint-online
manager: bpardi
ms.topic: article
audience: admin
ms.openlocfilehash: baa46deda7d7e10f3a7655fc6da076d37607e29f
ms.sourcegitcommit: 97e175e5ff5b6a9e0274d5ec9b39fdf7e18eb387
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/25/2021
ms.locfileid: "52000292"
---
# <a name="translate-site-pages"></a>Tradurre pagine del sito
Prima di iniziare a tradurre il sito dei percorsi di apprendimento, è importante comprendere alcuni concetti chiave del funzionamento della funzionalità multilingue con i percorsi di apprendimento. 
- Informazioni sul sito- Le traduzioni di spostamento, logo e nome del sito richiedono che il sito sia visualizzato e tradotto nel profilo della lingua dell'utente.  
- La web part Percorsi di apprendimento deve essere visualizzata con il profilo della lingua dell'utente perché venga visualizzata in una lingua diversa dall'inglese. La web part e il contenuto fornito da Microsoft sono già stati tradotti automaticamente. Per ulteriori informazioni sui profili delle lingue, vedere [Modificare la lingua personale e le impostazioni internazionali.](https://support.microsoft.com/office/change-your-personal-language-and-region-settings-caa1fccc-bcdb-42f3-9e5b-45957647ffd7)
- La modalità di configurazione dei percorsi di apprendimento determina se sono disponibili pagine tradotte. I nuovi siti di cui è stato eseguito il provisioning con il servizio look book di Microsoft 365 avranno pagine tradotte in nove lingue disponibili. I siti o i siti aggiornati creati richiederanno la traduzione manuale. Vedi [Opzioni di installazione per percorsi di apprendimento multilingue.](custom_setupoptions_ml.md)
- Il supporto multilingue per i percorsi di apprendimento è abilitato dalle funzionalità multilingue di SharePoint Online per i siti di comunicazione. Per informazioni sulle funzionalità multilingue di SharePoint Online, vedere [Create multilingual communication sites, pages, and news.](https://support.office.com/article/2bb7d610-5453-41c6-a0e8-6f40b3ed750c) 

## <a name="working-with-a-newly-provisioned-site"></a>Utilizzo di un nuovo sito di cui è stato eseguito il provisioning
Se è stato effettuato il provisioning di un nuovo sito di percorsi di apprendimento dal servizio look book di Microsoft 365, le pagine tradotte sono già disponibili. Per impostazione predefinita, il sito fornisce le pagine seguenti:

- Home.aspx
- Start-with-Six-Simple-Steps.aspx
- Introduzione a Microsoft-365.aspx
- Introduzione a Microsoft-Teams.aspx
- Introduzione a SharePoint.aspx
- Introduzione a OneDriive.aspx
- Domande e risposte
- Eventi di formazione calendar.aspx
- Become-a-Champion.aspx
- Recommended-Playlists.aspx
- Percorsi di apprendimento Admin Success Center

## <a name="view-translated-pages-from-the-newly-provisioned-site"></a>Visualizzare le pagine tradotte dal nuovo sito di cui è stato eseguito il provisioning
Per acquisire familiarità con il sito dei percorsi di apprendimento tradotti, diamo un'occhiata ad alcune pagine tradotte.

### <a name="view-the-translated-home-page"></a>Visualizzare la home page tradotta
Nella home page dei percorsi di apprendimento seleziona una lingua nell'elenco a discesa della lingua, come illustrato nell'esempio seguente. Nell'esempio viene visualizzato l'italiano selezionato nell'angolo superiore destro e tutti gli elementi della pagina vengono convertiti.

![Foto percorsi di apprendimento in uso](media/custom_ml_pages_home.png)

### <a name="view-the-translated-microsoft-365-training-page"></a>Visualizzare la pagina di formazione tradotta di Microsoft 365
Esamini ora la pagina di formazione di Microsoft 365. 

1. Nella home page del sito percorsi **di** apprendimento fare clic su Formazione su **Microsoft 365.**
2. Nell'angolo superiore destro della pagina selezionare una lingua. In questo esempio viene selezionato italiano.

![Pagina percorsi di apprendimento di esempio per l'italiano.](media/custom_ml_pages_training.png)

Quali traduzioni sono visibili quando si seleziona la lingua?
- La pagina di SharePoint viene tradotta come illustrato nell'immagine precedente. Si noti che il testo per il banner della pagina è ora in italiano.

Che cos'è che le traduzioni non sono visibili?
- Il nome del sito è in inglese
- La struttura di spostamento del sito è in inglese
- La web part percorsi di apprendimento è in inglese

## <a name="view-the-fully-translated-site"></a>Visualizzare il sito completamente tradotto 
Per visualizzare un sito completamente tradotto in una lingua specifica, incluse le pagine del sito, la struttura di spostamento e la web part, è necessario impostare la lingua personale e le impostazioni internazionali dell'utente per tale lingua. Per ulteriori informazioni sull'impostazione delle impostazioni internazionali e della lingua, vedere Modificare la lingua [personale e le impostazioni internazionali.](https://support.microsoft.com/office/change-your-personal-language-and-region-settings-caa1fccc-bcdb-42f3-9e5b-45957647ffd7) È consigliabile usare un account separato o fare in modo che un altro utente con le diverse impostazioni della lingua visualizza le pagine tradotte.  

## <a name="working-with-an-updated-or-manually-installed-learning-pathways-site"></a>Utilizzo di un sito di percorsi di apprendimento aggiornato o installato manualmente
Se è stato aggiornato un sito percorsi di apprendimento esistente o la web part è stata installata manualmente in un sito esistente, sarà necessario tradurre manualmente le pagine del sito. La web part percorsi di apprendimento e il contenuto sono già tradotti e verranno visualizzati nella lingua preferita dell'utente. Per tradurre le pagine, vedere le istruzioni seguenti "Creare pagine per le lingue desiderate". 

## <a name="create-pages-for-the-languages-you-want"></a>Creare pagine per le lingue desiderate
Dopo aver abilitato il sito per le caratteristiche multilingue e aver scelto le lingue che si desidera rendere disponibili, è possibile creare le pagine di traduzione desiderate. 

1. Passare alla pagina della lingua predefinita che si desidera rendere disponibile in un'altra lingua.
2. Sulla barra superiore selezionare **Traduzione.**
3. Selezionare **Crea** per le lingue desiderate.

> [!IMPORTANT]
> Dopo aver creato le pagine di traduzione, è necessario pubblicare (o ripubblicare) la pagina della lingua predefinita per assicurarsi che:
>- Le pagine di traduzione vengono visualizzate nel sito della lingua corrispondente.
>- Le pagine di traduzione vengono visualizzate correttamente nella web part Notizie e nelle web part Contenuto evidenziato.
>- L'elenco a discesa della lingua nella parte superiore del sito include tutte le lingue abilitate.
>- I traduttori vengono informati della richiesta di traduzione.

Dopo aver creato le pagine, lo stato della pagina (bozza salvata, pubblicata e così via) viene visualizzato nel riquadro di traduzione accanto a ogni lingua. Inoltre, i traduttori assegnati riceveranno una notifica tramite posta elettronica in cui viene richiesta una traduzione.

### <a name="view-the-fully-translated-site-in-a-specific-language"></a>Visualizzare il sito completamente tradotto in una lingua specifica
Per visualizzare un sito completamente tradotto in una lingua specifica, incluse le pagine del sito, la struttura di spostamento e la web part, è necessario impostare la lingua personale e le impostazioni internazionali dell'utente per tale lingua. Per ulteriori informazioni sull'impostazione delle impostazioni internazionali e della lingua, vedere Modificare la lingua [personale e le impostazioni internazionali.](https://support.microsoft.com/office/change-your-personal-language-and-region-settings-caa1fccc-bcdb-42f3-9e5b-45957647ffd7) Si noti che è meglio usare un account separato o fare in modo che un altro utente con le diverse impostazioni della lingua visualizza le pagine tradotte.

## <a name="what-does-a-translator-do"></a>Qual è il compito di un traduttore?
 Dopo aver configurato il sito in inglese, un utente con spagnolo come lingua personale preferita, ad esempio, modifica e converte manualmente il contenuto del titolo, dello spostamento e del piè di pagina in spagnolo. Gli utenti che hanno la lingua tedesca come preferenza personale procederanno similmente per il tedesco. Una volta tradotto il contenuto, verrà visualizzato per tutti gli utenti di quelle lingue preferite. La web part seleziona la lingua preferita dell'utente e mostra il contenuto tradotto in tale lingua. 

I traduttori traducono manualmente le copie della pagina della lingua predefinita nelle lingue specificate. Quando vengono create le copie delle pagine, i traduttori vengono informati tramite posta elettronica se è stato specificato un traduttore. Il messaggio di posta elettronica include un collegamento alla pagina della lingua predefinita e alla pagina di traduzione appena creata. Il traduttore:
1. Seleziona il **pulsante Avvia traduzione** nel messaggio di posta elettronica.
2. Seleziona **Modifica** in alto a destra della pagina e traduci il contenuto.
3. Al termine, selezionare Salva come bozza **(se** non si è pronti a renderla visibile ai lettori) o se la  pagina è pronta per essere visibile a tutti gli utenti che utilizzano tale lingua nel sito, selezionare Pubblica o **Pubblica notizie.**

Per ulteriori informazioni sul processo di traduzione, vedere [Create multilingual communication sites, pages, and news](https://support.office.com/article/2bb7d610-5453-41c6-a0e8-6f40b3ed750c). 

## <a name="updating-the-default-language-page"></a>Aggiornamento della pagina della lingua predefinita
Quando la pagina della lingua predefinita viene aggiornata, è necessario ripubblicare la pagina. Quindi, i traduttori per le pagine di traduzione vengono informati tramite posta elettronica che è stato effettuato un aggiornamento in modo che sia possibile aggiornere le singole pagine di traduzione.

## <a name="set-up-a-multilingual-site-name-navigation-and-footer"></a>Configurare un nome di sito multilingue, una struttura di spostamento e un piè di pagina
Per mostrare il nome del sito, lo spostamento e il piè di pagina nelle diverse lingue rese disponibili, ciascun elemento deve essere tradotto manualmente.

Ad esempio, si supponga di aver creato un sito di comunicazione con la lingua predefinita dell’inglese e di aver abilitato il sito per la lingua spagnola e quella tedesca. Quando si crea un sito, è possibile configurarne il nome e la descrizione nella lingua predefinita, in questo caso l’inglese. È anche possibile aggiornare il nome e la descrizione del sito dopo la creazione. Quindi, creare i nodi di spostamento e il contenuto del piè di pagina in inglese.

Dopo la configurazione del sito in inglese, un utente con lo spagnolo come lingua personale preferita eseguirà la modifica e la traduzione manuale del titolo, della descrizione, della struttura di spostamento e del contenuto del piè di pagina in spagnolo. Gli utenti che hanno la lingua tedesca come preferenza personale procederanno similmente per il tedesco. Una volta tradotto il contenuto, verrà visualizzato per tutti gli utenti di quelle lingue preferite. 

> [! NOTES]
>- Gli utenti che traducono il contenuto del sito per le lingue preferite devono essere membri del gruppo Proprietari del sito o disporre di autorizzazioni equivalenti per il sito.
>- Se viene apportata una modifica al nome del sito, alla struttura di spostamento o al piè di pagina nella lingua predefinita, l'elemento tradotto corrispondente in un'altra lingua non viene aggiornato automaticamente, a meno che non si sce se si sceglie di sovrascrivere le traduzioni del sito esistenti. In questo caso, l'elemento tradotto viene sostituito dall'aggiornamento nella lingua predefinita e deve essere tradotto di nuovo manualmente. Per sovrascrivere le traduzioni, passare alla pagina Lingue sito per la lingua predefinita e selezionare Mostra impostazioni avanzate. Quindi, fai scorrere l'interruttore per Sovrascrivi traduzioni su Attivato. Questa opzione non si applica al contenuto delle pagine o delle notizie.

### <a name="to-view-the-fully-translated-site-in-a-specific-language"></a>Per visualizzare il sito completamente tradotto in una lingua specifica
Per visualizzare un sito completamente tradotto in una lingua specifica, incluse le pagine del sito, la struttura di spostamento e la web part, è necessario impostare la lingua personale e le impostazioni internazionali dell'utente per tale lingua. Per ulteriori informazioni sull'impostazione delle impostazioni internazionali e della lingua, vedere Modificare la lingua [personale e le impostazioni internazionali.](https://support.microsoft.com/office/change-your-personal-language-and-region-settings-caa1fccc-bcdb-42f3-9e5b-45957647ffd7) È consigliabile usare un account separato o fare in modo che un altro utente con le diverse impostazioni della lingua visualizza le pagine tradotte.

## <a name="for-more-information"></a>Ulteriori informazioni
- Per ulteriori informazioni sulla traduzione delle pagine del sito di comunicazione di SharePoint, vedere [Create multilingual communication sites, pages, and news.](https://support.office.com/article/2bb7d610-5453-41c6-a0e8-6f40b3ed750c)
- Per ulteriori informazioni sulla personalizzazione dei percorsi di apprendimento, vedere [Customize Learning Pathways.](custom_overview.md)  
