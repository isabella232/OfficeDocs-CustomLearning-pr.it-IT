---
author: pkrebs
ms.author: pkrebs
title: Creare pagine di SharePoint per playlist
ms.date: 02/10/2019
description: Creare pagine di SharePoint per playlist
ms.openlocfilehash: c2de66a0746260e8f6539656ad70052b209c54ba
ms.sourcegitcommit: e10085e60ca3f38029fde229fb093e6bc4a34203
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2019
ms.locfileid: "30103691"
---
# <a name="create-sharepoint-pages-for-custom-playlists"></a><span data-ttu-id="c9e7a-103">Creare pagine di SharePoint per playlist personalizzate</span><span class="sxs-lookup"><span data-stu-id="c9e7a-103">Create SharePoint pages for Custom Playlists</span></span>

<span data-ttu-id="c9e7a-p101">Una delle caratteristiche esclusive dell'apprendimento personalizzato è la possibilità di creare playlist che vengono assemblate da risorse di Microsoft e da risorse di SharePoint create. In questo esempio viene creata una pagina di SharePoint prima della creazione di una playlist. La possibilità di creare playlist da pagine di SharePoint offre una vasta gamma di opportunità per creare pagine utilizzando le web part disponibili da Microsoft o dall'organizzazione. Ad esempio, una playlist può includere una pagina di SharePoint con video incorporati da YouTube o un modulo creato da moduli di Office 365 o un report incorporato di Power BI. In questo esempio viene illustrato come creare una pagina con la Web part embed e la Web part testo.</span><span class="sxs-lookup"><span data-stu-id="c9e7a-p101">One of the unique features of Custom Learning is the ability to create playlists that are assembled from assets from Microsoft and from SharePoint assets that you create. In this example, we’ll create a SharePoint page in advance of creating a playlist. The ability to build playlists from SharePoint pages offers a variety of opportunities to build pages using the Web parts available from Microsoft or your organization. For example, a playlist can include a SharePoint page with embedded videos from YouTube, or a form built from Office 365 Forms, or an embedded Power BI report. In this example, we’ll show you how to build a page with the Embed web part and the Text web part.</span></span>  

## <a name="create-a-sharepoint-page-for-a-custom-playlist"></a><span data-ttu-id="c9e7a-109">Creare una pagina di SharePoint per un elenco di riproduzione personalizzato</span><span class="sxs-lookup"><span data-stu-id="c9e7a-109">Create a SharePoint page for a custom playlist</span></span>

1. <span data-ttu-id="c9e7a-110">Fare clic sull' \*\*\*\* icona dell'ingranaGgio di SharePoint e quindi fare clic su **Aggiungi pagina**.</span><span class="sxs-lookup"><span data-stu-id="c9e7a-110">Click the SharePoint **Gear** icon, and then click **Add a page**.</span></span>
2. <span data-ttu-id="c9e7a-111">Fare clic su **Aggiungi una nuova sezione (+)** sul lato sinistro della pagina, quindi fare clic su **due colonne** per il layout della sezione.</span><span class="sxs-lookup"><span data-stu-id="c9e7a-111">Click **Add a new section (+)** on the left-hand side of the page, and then click **Two Columns** for the section layout.</span></span>
3. <span data-ttu-id="c9e7a-112">Nella colonna sinistra fare clic su + e quindi fare clic sulla Web part **Embed** .</span><span class="sxs-lookup"><span data-stu-id="c9e7a-112">In the left column, click + , and then click the **Embed** web part.</span></span> 
4. <span data-ttu-id="c9e7a-p102">Nella colonna a destra fare clic su +, quindi fare clic sulla Web part **testo** . La pagina dovrebbe essere simile alla seguente.</span><span class="sxs-lookup"><span data-stu-id="c9e7a-p102">In the right column, click +, and then click the **Text** web part. Your page should look like this.</span></span>

![CG-pagenewstart. png](media/cg-pagenewstart.png)

### <a name="add-a-video-and-text-from-youtube"></a><span data-ttu-id="c9e7a-116">Aggiungere un video e un testo da YouTube</span><span class="sxs-lookup"><span data-stu-id="c9e7a-116">Add a video and text from YouTube</span></span>

1. <span data-ttu-id="c9e7a-p103">Nel browser Vai su YouTube. Per questo esempio, cercare "che cos'è Office 365 – le migliori app per la produttività di Microsoft".</span><span class="sxs-lookup"><span data-stu-id="c9e7a-p103">In your browser, go to YouTube. For this example, search for “What is Office 365 – Microsoft’s best productivity apps”.</span></span>
2. <span data-ttu-id="c9e7a-119">Fare clic sul video per riprodurlo, quindi sospenderlo, quindi fare clic con il pulsante destro del mouse su di esso.</span><span class="sxs-lookup"><span data-stu-id="c9e7a-119">Click the video to play it, then pause it, then right-click on it.</span></span> 
3. <span data-ttu-id="c9e7a-120">Fare clic su **Copia codice embed**, quindi tornare alla pagina di SharePoint.</span><span class="sxs-lookup"><span data-stu-id="c9e7a-120">Click **Copy embed code**, then return to the SharePoint page.</span></span> 
4. <span data-ttu-id="c9e7a-121">Fare clic su **Aggiungi codice embed** nella web part **Embed** e quindi aggiungere il codice dal video di YouTube.</span><span class="sxs-lookup"><span data-stu-id="c9e7a-121">Click **Add embed code** in the **Embed** web part, and then add the code from the YouTube video.</span></span>
5. <span data-ttu-id="c9e7a-122">Tornare alla pagina di YouTube e copiare il testo della **Descrizione** del video.</span><span class="sxs-lookup"><span data-stu-id="c9e7a-122">Return to the YouTube page and copy the **Description** text for the video.</span></span> 
6. <span data-ttu-id="c9e7a-123">Tornare alla pagina di SharePoint, selezionare la Web part **testo** e quindi copiare il testo dal video di YouTube.</span><span class="sxs-lookup"><span data-stu-id="c9e7a-123">Return to the SharePoint page, select the **Text** web part, then copy the text from the YouTube video.</span></span>
7. <span data-ttu-id="c9e7a-124">Selezionare l'icona **Modifica web part** nell'area del titolo della pagina di SharePoint e quindi denominare la pagina "introduzione di playlist personalizzate".</span><span class="sxs-lookup"><span data-stu-id="c9e7a-124">Select the **Edit web part** icon  in the Title area of the SharePoint page, and then name the page “Custom Playlist Introduction”.</span></span> 
8. <span data-ttu-id="c9e7a-p104">Per **layout**, selezionare **pianura**, quindi riquadro delle proprietà dell' **area del titolo** . La pagina dovrebbe avere un aspetto analogo al seguente.</span><span class="sxs-lookup"><span data-stu-id="c9e7a-p104">For **Layout**, select **Plain**, then close **Title Region** properties pane. The page should now look something like the following.</span></span> 

![CG-pagenewfinish. png](media/cg-pagenewfinish.png)

### <a name="publish-the-page"></a><span data-ttu-id="c9e7a-128">Pubblicare la pagina</span><span class="sxs-lookup"><span data-stu-id="c9e7a-128">Publish the page</span></span>

- <span data-ttu-id="c9e7a-p105">Selezionare il pulsante **pubblica** . A questo punto si è pronti per aggiungere questa pagina di SharePoint alla playlist personalizzata.</span><span class="sxs-lookup"><span data-stu-id="c9e7a-p105">Select the **Publish** button. Now you're ready to add this SharePoint page to your custom playlist.</span></span> 