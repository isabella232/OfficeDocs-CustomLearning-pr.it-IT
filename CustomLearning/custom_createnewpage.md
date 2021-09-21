---
author: pkrebs
ms.author: pkrebs
title: Creare SharePoint per le playlist
ms.date: 02/10/2019
description: Creare SharePoint per le playlist
ms.service: sharepoint-online
manager: bpardi
ms.topic: article
ms.openlocfilehash: e29fca92fd4102f89f08a90a8a1be11776f35995
ms.sourcegitcommit: 6005c2551bdea334767e6a056fdcb79533f2c858
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/21/2021
ms.locfileid: "59461125"
---
# <a name="create-sharepoint-pages-for-custom-playlists"></a>Creare SharePoint pagine per playlist personalizzate

Una delle caratteristiche uniche dei percorsi di apprendimento è la possibilità di creare playlist assemblate da risorse di Microsoft e da SharePoint risorse create dall'utente. In questo esempio creeremo una pagina SharePoint prima di creare una playlist. La possibilità di creare playlist da SharePoint pagine offre un'ampia gamma di opportunità per creare pagine utilizzando le web part disponibili da Microsoft o dall'organizzazione. Ad esempio, una playlist può includere una pagina SharePoint con video incorporati da YouTube o un modulo creato da Office 365 Forms o un report Power BI incorporato. In questo esempio verrà illustrato come creare una pagina con la web part Incorpora e la web part Testo.  

## <a name="create-a-sharepoint-page-for-a-custom-playlist"></a>Creare una SharePoint per una playlist personalizzata

1. Fare clic **SharePoint'icona Ingranaggio** e quindi fare clic **su Aggiungi pagina.**
2. Fai **clic su Aggiungi una nuova sezione (+)** sul lato sinistro della pagina e quindi fai clic su Due **colonne** per il layout della sezione.
3. Nella colonna sinistra fare clic su + e quindi **sulla** web part Incorpora. 
4. Nella colonna destra fare clic su +, quindi **fare** clic sulla web part Testo. La pagina dovrebbe essere simile alla seguente.

![creazione di una pagina di SharePoint](media/cg-pagenewstart.png)

### <a name="add-a-video-and-text-from-youtube"></a>Aggiungere un video e un testo da YouTube

1. Nel browser passare a YouTube. Per questo esempio, cercare "What is Office 365– Microsoft's best productivity apps".
2. Fai clic sul video per riprodurlo, quindi sospendelo, quindi fai clic con il pulsante destro del mouse su di esso. 
3. Fare **clic su Copia codice** di incorporamento e quindi tornare alla SharePoint pagina. 
4. Fai **clic su Aggiungi** codice di incorporamento nella web part Incorpora e quindi aggiungi il codice dal video di YouTube. 
5. Torna alla pagina di YouTube e copia il testo **Descrizione** per il video. 
6. Torna alla pagina SharePoint, seleziona **la** web part Testo, quindi copia il testo dal video di YouTube.
7. Selezionare **l'icona Modifica web part** nell'area Titolo della pagina SharePoint e quindi assegnare alla pagina il nome "Introduzione playlist personalizzata". 
8. Per **Layout** selezionare **Normale,** quindi chiudere **il riquadro proprietà Area** titolo. La pagina dovrebbe essere simile alla seguente. 

![Completare la pagina](media/cg-pagenewfinish.png)

### <a name="publish-the-page"></a>Pubblicare la pagina

- Selezionare il **pulsante** Pubblica. Ora sei pronto per aggiungere questa pagina SharePoint alla playlist personalizzata. 