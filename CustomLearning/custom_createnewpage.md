---
author: pkrebs
ms.author: pkrebs
title: Creare pagine di SharePoint per le playlist
ms.date: 02/10/2019
description: Creare pagine di SharePoint per le playlist
ms.service: sharepoint-online
ms.openlocfilehash: 40c249fbd5b0fdaefd555f23bf20ac23240ea954
ms.sourcegitcommit: 97e175e5ff5b6a9e0274d5ec9b39fdf7e18eb387
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/25/2021
ms.locfileid: "51999092"
---
# <a name="create-sharepoint-pages-for-custom-playlists"></a>Creare pagine di SharePoint per playlist personalizzate

Una delle caratteristiche uniche dei percorsi di apprendimento è la possibilità di creare playlist assemblate da risorse di Microsoft e da risorse di SharePoint create dall'utente. In questo esempio verrà creata una pagina di SharePoint prima di creare una playlist. La possibilità di creare playlist da pagine di SharePoint offre un'ampia gamma di opportunità per creare pagine utilizzando le web part disponibili da Microsoft o dall'organizzazione. Ad esempio, una playlist può includere una pagina di SharePoint con video incorporati da YouTube o un modulo creato da Moduli di Office 365 o un report Power BI incorporato. In questo esempio verrà illustrato come creare una pagina con la web part Incorpora e la web part Testo.  

## <a name="create-a-sharepoint-page-for-a-custom-playlist"></a>Creare una pagina di SharePoint per una playlist personalizzata

1. Fare clic sull'icona **a forma di** ingranaggio di SharePoint e quindi su Aggiungi **pagina.**
2. Fai **clic su Aggiungi una nuova sezione (+)** sul lato sinistro della pagina e quindi fai clic su Due **colonne** per il layout della sezione.
3. Nella colonna sinistra fare clic su + e quindi **sulla** web part Incorpora. 
4. Nella colonna destra fare clic su +, quindi **fare** clic sulla web part Testo. La pagina dovrebbe essere simile alla seguente.

![cg-pagenewstart.png](media/cg-pagenewstart.png)

### <a name="add-a-video-and-text-from-youtube"></a>Aggiungere un video e un testo da YouTube

1. Nel browser passare a YouTube. Per questo esempio, cercare "What is Office 365 – Microsoft's best productivity apps".
2. Fai clic sul video per riprodurlo, quindi sospendelo, quindi fai clic con il pulsante destro del mouse su di esso. 
3. Fare **clic su Copia codice** di incorporamento e quindi tornare alla pagina di SharePoint. 
4. Fai **clic su Aggiungi** codice di incorporamento nella web part Incorpora e quindi aggiungi il codice dal video di YouTube. 
5. Torna alla pagina di YouTube e copia il testo **Descrizione** per il video. 
6. Tornare alla pagina di SharePoint, selezionare **la** web part Testo, quindi copiare il testo dal video di YouTube.
7. Selezionare **l'icona Modifica web part** nell'area Titolo della pagina di SharePoint e quindi assegnare alla pagina il nome "Introduzione playlist personalizzata". 
8. Per **Layout** selezionare **Normale** e quindi chiudere il riquadro **proprietà Area** titolo. La pagina dovrebbe essere simile alla seguente. 

![cg-pagenewfinish.png](media/cg-pagenewfinish.png)

### <a name="publish-the-page"></a>Pubblicare la pagina

- Selezionare il **pulsante** Pubblica. A questo punto è possibile aggiungere questa pagina di SharePoint alla playlist personalizzata. 