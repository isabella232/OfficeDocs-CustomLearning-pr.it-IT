---
author: pkrebs
ms.author: pkrebs
title: Aggiungere risorse a una playlist
ms.date: 02/17/2019
description: Aggiungere nuove risorse esistenti a una scaletta di percorsi di apprendimento
ms.openlocfilehash: d1032139e2d753601cb269e487db343778938d64
ms.sourcegitcommit: f5a7079d56598c14aef2f4b886c025a59ba89276
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "34247641"
---
# <a name="add-assets-to-a-custom-playlist"></a>Aggiungere risorse a un elenco di riproduzione personalizzato

Con i percorsi di apprendimento, è possibile aggiungere le risorse seguenti a una playlist:

- **Asset dei percorsi di apprendimento microsoft 365 esistenti** -queste sono risorse che fanno parte del catalogo Microsoft online o delle risorse che l'organizzazione ha già aggiunto ai percorsi di apprendimento.
- **Nuove risorse** : sono risorse che vengono aggiunte ai percorsi di apprendimento creati dalle pagine di SharePoint create o da risorse di SharePoint già disponibili in un sito di SharePoint nell'organizzazione. 

> [!TIP]
> Se una risorsa Microsoft playlist non soddisfa le proprie esigenze, creare una nuova playlist e quindi aggiungere le risorse Microsoft e tutte le risorse appena create alla playlist per creare l'esperienza desiderata. Non è possibile modificare i percorsi di apprendimento delle playlist fornite da Microsoft, ma è possibile aggiungere risorse di apprendimento in una playlist personalizzata.   

## <a name="create-a-new-asset-for-a-playlist"></a>Creare una nuova risorsa per una playlist

Sono disponibili due opzioni per l'aggiunta di un nuovo asset a una playlist.

- **Pagina Crea risorsa** -con questa opzione, i percorsi di apprendimento generano una nuova pagina di SharePoint vuota per l'utente e la aggiungono alla playlist. È quindi possibile aggiungere contenuto alla pagina e salvarlo.  
- **Immettere l'URL** -con questa opzione, è possibile creare la pagina in anticipo oppure è già disponibile la pagina e si specifica l'URL per aggiungere la pagina alla playlist.

### <a name="create-asset-page"></a>Pagina Crea asset 
Con l'opzione **Crea pagina risorsa** , è possibile specificare un titolo per il bene, quindi fare clic su Crea pagina asset per creare e aprire una nuova pagina di SharePoint per la modifica. 

1.  Se la playlist non è ancora aperta per la modifica, dalla pagina **Custom Learning Administration** fare clic sulla playlist che si desidera modificare. 
2. Per aggiungere un nuovo cespite a una playlist, fare clic su **nuovo asset**. 
3. Immettere un titolo. In questo esempio viene immesso "Aggiungi risorse a una playlist" e quindi fare clic su **Crea asset page**.

![CG-addassetcreatenewpage. png](media/cg-addassetcreatenewpage.png)

4. Fare clic su **Apri pagina**.
5. Fare clic sull'icona **modifica** e quindi su **Modifica web part** nell'area titolo.
6. In **layout**fare clic su **normale**. 
7. Aggiungere una nuova sezione a una colonna e quindi aggiungere del testo di esempio alla pagina in modo che sia simile all'esempio seguente. 

![CG-addassetcreatenewpageedit. png](media/cg-addassetcreatenewpageedit.png)

7. Fare clic su **Pubblica**.
8. Tornare alla pagina **Custom Learning Administration** . 
9. Compilare la parte restante delle proprietà del cespite, quindi fare clic su **Salva risorsa.**

### <a name="enter-the-url"></a>Immettere l'URL
Con l'opzione **immettere l'URL** , è possibile specificare un titolo per il bene, quindi fare clic su **immettere l'URL** per indicare la pagina di SharePoint che si desidera aggiungere alla playlist. 

1.  Se la playlist non è aperta per la modifica, dalla pagina di **amministrazione dell'apprendimento personalizzato** fare clic sulla playlist che si desidera modificare. 
2. Per aggiungere un nuovo cespite a una playlist, fare clic su **nuovo asset**. 
3. Immettere un titolo. In questo esempio, immettere "Introduzione playlist personalizzata", quindi fare clic su **Immetti URL**. 

![CG-newplaylistasseturl. png](media/cg-newplaylistasseturl.png)

4. Immettere l'URL della pagina di SharePoint creata in una precedente sezione [creare pagine di SharePoint per playlist personalizzate](custom_createnewpage.md) e quindi compilare il resto dei campi, come illustrato nella figura seguente.

![CG-newplaylistassetdetails. png](media/cg-newplaylistassetdetails.png)

5. Fare clic su **Salva risorsa**. 

## <a name="add-an-existing-asset-to-a-playlist"></a>Aggiungere una risorsa esistente a una playlist

Le risorse esistenti sono costituite da percorsi di apprendimento forniti da Microsoft o da attività che sono già state aggiunte ai percorsi di apprendimento da parte dell'organizzazione. 

- Nella casella di **ricerca** immettere una frase di ricerca e quindi selezionare una risorsa dai risultati della ricerca. In questo esempio, immettere "che cos'è Excel?" per aggiungere un argomento introduttivo di Excel alla playlist.

![CG-existplaylistassetsearch. png](media/cg-existplaylistassetsearch.png)

## <a name="edit-move-and-delete-assets"></a>Modificare, spostare ed eliminare risorse
È possibile modificare le risorse personalizzate create, ma non le risorse di Microsoft. Tuttavia, è possibile rimuovere tutte le risorse da una playlist e cambiare le risorse degli ordini. 

![CG-playlistassetedit. png](media/cg-playlistassetedit.png)

### <a name="edit-an-asset"></a>Modificare una risorsa
- Fare clic sul pulsante modifica di un asset, modificare il cespite e quindi fare clic su Salva risorsa. 

### <a name="move-an-asset-in-a-playlist"></a>Spostare una risorsa in una playlist
- Fare clic sulla freccia verso l'alto o verso il basso a destra del cespite per spostare l'ordine dei cespiti nella playlist

### <a name="remove-an-asset-from-a-playlist"></a>Rimuovere una risorsa da una playlist
- Fare clic sull'icona Rimuovi da playlist X per il cespite. 

## <a name="view-the-playlist-in-action"></a>Visualizzazione dell'elenco di riproduzione in azione
Dopo aver aggiunto risorse a una playlist, chiudere la playlist e visualizzarla in azione. 

1. Fare clic su **Chiudi playlist**.
2. Fare clic sulla scheda con la pagina **training di Office 365** .
3. Aggiornare la pagina e quindi fare clic su **primi giorni** **in inizia**.
4. Fare clic su **Learning pathways Starter Kit** per visualizzare la prima playlist in azione. 

![CG-addassetcheckwork. png](media/cg-addassetcheckwork.png)