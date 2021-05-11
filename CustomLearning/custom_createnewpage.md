---
author: pkrebs
ms.author: pkrebs
title: Creare SharePoint per le playlist
ms.date: 02/10/2019
description: Creare SharePoint per le playlist
ms.service: sharepoint-online
manager: bpardi
ms.topic: article
ms.openlocfilehash: ce4a204b3072469840b6f3fa8f93d9e78833b181
ms.sourcegitcommit: 956ab22dd8ce23ee1779f1a01d34b434243c3cb1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/11/2021
ms.locfileid: "52310660"
---
# <a name="create-sharepoint-pages-for-custom-playlists"></a><span data-ttu-id="bd150-103">Creare SharePoint per playlist personalizzate</span><span class="sxs-lookup"><span data-stu-id="bd150-103">Create SharePoint pages for Custom Playlists</span></span>

<span data-ttu-id="bd150-104">Una delle caratteristiche uniche dei percorsi di apprendimento è la possibilità di creare playlist assemblate da risorse di Microsoft e da SharePoint risorse create dall'utente.</span><span class="sxs-lookup"><span data-stu-id="bd150-104">One of the unique features of learning pathways is the ability to create playlists that are assembled from assets from Microsoft and from SharePoint assets that you create.</span></span> <span data-ttu-id="bd150-105">In questo esempio creeremo una pagina SharePoint prima di creare una playlist.</span><span class="sxs-lookup"><span data-stu-id="bd150-105">In this example, we’ll create a SharePoint page in advance of creating a playlist.</span></span> <span data-ttu-id="bd150-106">La possibilità di creare playlist da SharePoint pagine offre un'ampia gamma di opportunità per creare pagine utilizzando le web part disponibili da Microsoft o dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="bd150-106">The ability to build playlists from SharePoint pages offers a variety of opportunities to build pages using the Web parts available from Microsoft or your organization.</span></span> <span data-ttu-id="bd150-107">Ad esempio, una playlist può includere una pagina SharePoint con video incorporati da YouTube o un modulo creato da Office 365 Forms o un report Power BI incorporato.</span><span class="sxs-lookup"><span data-stu-id="bd150-107">For example, a playlist can include a SharePoint page with embedded videos from YouTube, or a form built from Office 365 Forms, or an embedded Power BI report.</span></span> <span data-ttu-id="bd150-108">In questo esempio verrà illustrato come creare una pagina con la web part Incorpora e la web part Testo.</span><span class="sxs-lookup"><span data-stu-id="bd150-108">In this example, we’ll show you how to build a page with the Embed web part and the Text web part.</span></span>  

## <a name="create-a-sharepoint-page-for-a-custom-playlist"></a><span data-ttu-id="bd150-109">Creare una SharePoint per una playlist personalizzata</span><span class="sxs-lookup"><span data-stu-id="bd150-109">Create a SharePoint page for a custom playlist</span></span>

1. <span data-ttu-id="bd150-110">Fare clic **SharePoint'icona a** forma di ingranaggio e quindi fare clic **su Aggiungi pagina.**</span><span class="sxs-lookup"><span data-stu-id="bd150-110">Click the SharePoint **Gear** icon, and then click **Add a page**.</span></span>
2. <span data-ttu-id="bd150-111">Fai **clic su Aggiungi una nuova sezione (+)** sul lato sinistro della pagina e quindi fai clic su Due **colonne** per il layout della sezione.</span><span class="sxs-lookup"><span data-stu-id="bd150-111">Click **Add a new section (+)** on the left-hand side of the page, and then click **Two Columns** for the section layout.</span></span>
3. <span data-ttu-id="bd150-112">Nella colonna sinistra fare clic su + e quindi **sulla** web part Incorpora.</span><span class="sxs-lookup"><span data-stu-id="bd150-112">In the left column, click + , and then click the **Embed** web part.</span></span> 
4. <span data-ttu-id="bd150-113">Nella colonna destra fare clic su +, quindi **fare** clic sulla web part Testo.</span><span class="sxs-lookup"><span data-stu-id="bd150-113">In the right column, click +, and then click the **Text** web part.</span></span> <span data-ttu-id="bd150-114">La pagina dovrebbe essere simile alla seguente.</span><span class="sxs-lookup"><span data-stu-id="bd150-114">Your page should look like this.</span></span>

![cg-pagenewstart.png](media/cg-pagenewstart.png)

### <a name="add-a-video-and-text-from-youtube"></a><span data-ttu-id="bd150-116">Aggiungere un video e un testo da YouTube</span><span class="sxs-lookup"><span data-stu-id="bd150-116">Add a video and text from YouTube</span></span>

1. <span data-ttu-id="bd150-117">Nel browser passare a YouTube.</span><span class="sxs-lookup"><span data-stu-id="bd150-117">In your browser, go to YouTube.</span></span> <span data-ttu-id="bd150-118">Per questo esempio, cercare "What is Office 365 – Microsoft's best productivity apps".</span><span class="sxs-lookup"><span data-stu-id="bd150-118">For this example, search for “What is Office 365 – Microsoft’s best productivity apps”.</span></span>
2. <span data-ttu-id="bd150-119">Fai clic sul video per riprodurlo, quindi sospendelo, quindi fai clic con il pulsante destro del mouse su di esso.</span><span class="sxs-lookup"><span data-stu-id="bd150-119">Click the video to play it, then pause it, then right-click on it.</span></span> 
3. <span data-ttu-id="bd150-120">Fare **clic su Copia** codice di incorporamento e quindi tornare alla SharePoint pagina.</span><span class="sxs-lookup"><span data-stu-id="bd150-120">Click **Copy embed code**, then return to the SharePoint page.</span></span> 
4. <span data-ttu-id="bd150-121">Fai **clic su Aggiungi** codice di incorporamento nella web part Incorpora e quindi aggiungi il codice dal video di YouTube. </span><span class="sxs-lookup"><span data-stu-id="bd150-121">Click **Add embed code** in the **Embed** web part, and then add the code from the YouTube video.</span></span>
5. <span data-ttu-id="bd150-122">Torna alla pagina di YouTube e copia il testo **Descrizione** per il video.</span><span class="sxs-lookup"><span data-stu-id="bd150-122">Return to the YouTube page and copy the **Description** text for the video.</span></span> 
6. <span data-ttu-id="bd150-123">Tornare alla pagina SharePoint, selezionare **la** web part Testo, quindi copiare il testo dal video di YouTube.</span><span class="sxs-lookup"><span data-stu-id="bd150-123">Return to the SharePoint page, select the **Text** web part, then copy the text from the YouTube video.</span></span>
7. <span data-ttu-id="bd150-124">Selezionare **l'icona Modifica web part** nell'area Titolo della pagina SharePoint e quindi assegnare alla pagina il nome "Introduzione playlist personalizzata".</span><span class="sxs-lookup"><span data-stu-id="bd150-124">Select the **Edit web part** icon  in the Title area of the SharePoint page, and then name the page “Custom Playlist Introduction”.</span></span> 
8. <span data-ttu-id="bd150-125">Per **Layout** selezionare **Normale** e quindi chiudere il riquadro **proprietà Area** titolo.</span><span class="sxs-lookup"><span data-stu-id="bd150-125">For **Layout**, select **Plain**, then close **Title Region** properties pane.</span></span> <span data-ttu-id="bd150-126">La pagina dovrebbe essere simile alla seguente.</span><span class="sxs-lookup"><span data-stu-id="bd150-126">The page should now look something like the following.</span></span> 

![cg-pagenewfinish.png](media/cg-pagenewfinish.png)

### <a name="publish-the-page"></a><span data-ttu-id="bd150-128">Pubblicare la pagina</span><span class="sxs-lookup"><span data-stu-id="bd150-128">Publish the page</span></span>

- <span data-ttu-id="bd150-129">Selezionare il **pulsante** Pubblica.</span><span class="sxs-lookup"><span data-stu-id="bd150-129">Select the **Publish** button.</span></span> <span data-ttu-id="bd150-130">Ora sei pronto per aggiungere questa pagina SharePoint alla playlist personalizzata.</span><span class="sxs-lookup"><span data-stu-id="bd150-130">Now you're ready to add this SharePoint page to your custom playlist.</span></span> 