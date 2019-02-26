---
author: karuanag
ms.author: karuanag
title: Installazione della soluzione di apprendimento personalizzata WebPart
ms.date: 02/10/2019
description: Istruzioni di installazione per la soluzione di apprendimento personalizzata WebPart
ms.openlocfilehash: 53229e5b1b8175b06d888091963d1a9f2f0bd361
ms.sourcegitcommit: e10085e60ca3f38029fde229fb093e6bc4a34203
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/25/2019
ms.locfileid: "29989687"
---
# <a name="installing-the-custom-learning-solution-webpart"></a><span data-ttu-id="ec86b-103">Installazione della soluzione di apprendimento personalizzata WebPart</span><span class="sxs-lookup"><span data-stu-id="ec86b-103">Installing the Custom Learning Solution Webpart</span></span>

## <a name="prerequisites-for-a-tenant-wide-installation"></a><span data-ttu-id="ec86b-104">Prerequisiti per un'installazione a livello di tenant</span><span class="sxs-lookup"><span data-stu-id="ec86b-104">Prerequisites for a tenant-wide installation</span></span>

- <span data-ttu-id="ec86b-p101">Per installare il WebPart di apprendimento personalizzato per l'intero tenant, sarà necessario disporre delle autorizzazioni amministrative di Office 365.  Se non si dispone di queste autorizzazioni, è possibile collaborare con l'amministratore di Office 365 o installare WebPart per una singola raccolta siti.</span><span class="sxs-lookup"><span data-stu-id="ec86b-p101">To install the Custom Learning webpart for your entire tenant you will need to have Office 365 Administrative permissions.  If you do not have these permissions you can either work with your Office 365 Administrator or install the webpart for an individual site collection.</span></span>
- <span data-ttu-id="ec86b-107">L'utente o l'amministratore di Office 365 deve disporre di un programma di installazione e configurazione di un [Catalogo](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/set-up-your-developer-tenant) app a livello di tenant o di una [raccolta siti](https://docs.microsoft.com/en-us/sharepoint/dev/general-development/site-collection-app-catalog)per la ricezione del controllo WebPart.</span><span class="sxs-lookup"><span data-stu-id="ec86b-107">You or your Office 365 Administrator must have setup and configured a tenant-wide [App Catalog](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/set-up-your-developer-tenant) or a [Site Collection App Catalog](https://docs.microsoft.com/en-us/sharepoint/dev/general-development/site-collection-app-catalog)to receive the webpart.]</span></span>
- <span data-ttu-id="ec86b-p102">Il supporto di SharePoint Online è solo. La Web part non è supportata per l'installazione in qualsiasi versione di SharePoint in locale.</span><span class="sxs-lookup"><span data-stu-id="ec86b-p102">We support SharePoint Online only. The web part is not support for installation on any version of SharePoint on premises.</span></span>

## <a name="add-the-custom-learning-webpart-to-your-tenant"></a><span data-ttu-id="ec86b-110">Aggiungere il WebPart di apprendimento personalizzato al tenant</span><span class="sxs-lookup"><span data-stu-id="ec86b-110">Add the Custom Learning webpart to your tenant</span></span> 

1. <span data-ttu-id="ec86b-p103">Scaricare il WebPart di apprendimento personalizzato e salvarlo nell'unità locale.  Questo file è denominato "MS-Custom-Learning. sppkg".  Non modificare il nome o il suffisso del file.</span><span class="sxs-lookup"><span data-stu-id="ec86b-p103">Download the Custom Learning webpart and save it to your local drive.  This file is named "ms-custom-learning.sppkg".  Do not change the name or suffix of the file.</span></span> 
2. <span data-ttu-id="ec86b-114">Accedere al [portale di amministrazione di Office 365](https://admin.microsoft.com/AdminPortal/Home#/homepage) per il tenant</span><span class="sxs-lookup"><span data-stu-id="ec86b-114">Navigate to the [Office 365 Admin portal](https://admin.microsoft.com/AdminPortal/Home#/homepage) for your tenant</span></span>
3. <span data-ttu-id="ec86b-p104">Dal riquadro di spostamento sinistro selezionare interfaccia di amministrazione di SharePoint. Verrà aperto in una nuova scheda., nell'interfaccia di amministrazione di SharePoint selezionare app, Catalogo app, app per SharePoint</span><span class="sxs-lookup"><span data-stu-id="ec86b-p104">From the left navigation select Admin Centers, SharePoint. This will open in a new tab. , In the SharePoint Admin Center select Apps, App Catalog, Apps for SharePoint</span></span> 
4. <span data-ttu-id="ec86b-117">Selezionare carica il WebPart e scegliere il file "MS-Custom-Learning. sppkg" Scaricato</span><span class="sxs-lookup"><span data-stu-id="ec86b-117">Select upload the webpart and choose the "ms-custom-learning.sppkg" file you downloaded</span></span>
5. <span data-ttu-id="ec86b-118">Per questa installazione a livello di tenant, selezionare la casella accanto a "rendere disponibile la soluzione a tutti gli alloggi nell'organizzazione".</span><span class="sxs-lookup"><span data-stu-id="ec86b-118">For this tenant-wide installation check the box next to "Make this solution available to all sits in the organization."</span></span>  
 
> [!NOTE]
> <span data-ttu-id="ec86b-p105">Dopo aver installato il controllo WebPart, sarà possibile trovarlo nella raccolta WebPart in SharePoint Online.  **Nella raccolta il controllo WebPart è denominato "Microsoft Learning"**</span><span class="sxs-lookup"><span data-stu-id="ec86b-p105">Once the webpart is installed you will find it in your webpart gallery in SharePoint Online.  **In the gallery the webpart is named "Microsoft Learning"**</span></span>

![Distribuire la soluzione](media/trustapp_sm.png)


## <a name="add-the-microsoft-learning-webpart-to-a-sharepoint-online-page"></a><span data-ttu-id="ec86b-122">Aggiungere la Microsoft Learning WebPart a una pagina di SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="ec86b-122">Add the Microsoft Learning webpart to a SharePoint Online Page</span></span>

<span data-ttu-id="ec86b-p106">Dopo aver installato l'apprendimento personalizzato nel tenant, è possibile aggiungere la Web part a una pagina di SharePoint. Quando si esegue Office 365 e la formazione di Windows 10 è disponibile per il sito.</span><span class="sxs-lookup"><span data-stu-id="ec86b-p106">After Custom Learning is installed in your tenant you can add the Web part to a SharePoint page. When you do Office 365 and Windows 10 training is available to your site.</span></span>

1. <span data-ttu-id="ec86b-125">Aggiungere il controllo WebPart di apprendimento personalizzato in un layout di colonna a larghezza intera:</span><span class="sxs-lookup"><span data-stu-id="ec86b-125">Add the Custom Learning webpart in a full width column layout:</span></span>

![Layout di pagina di SharePoint](media/clo365fullcolumnwidth.png)

2. <span data-ttu-id="ec86b-p107">Nella pagina di SharePoint, selezionare Aggiungi sezione e quindi colonna larghezza intera.  Verrà visualizzato il seguente messaggio di richiesta:</span><span class="sxs-lookup"><span data-stu-id="ec86b-p107">In the SharePoint page, select Add section and then select full width column.  You'll see the following prompt:</span></span>

![AddWebpart](media/clo365addfullwidthwebpart.png)

3. <span data-ttu-id="ec86b-p108">Selezionare Microsoft Learning.  È ora necessario vedere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="ec86b-p108">Select Microsoft Learning.  You should now see the following:</span></span> 

![WebPart di apprendimento personalizzato](media/clo365addwebpart.png)

 <span data-ttu-id="ec86b-133">È ora possibile fare clic sui riquadri per esplorare il contenuto predefinito incluso nella soluzione.</span><span class="sxs-lookup"><span data-stu-id="ec86b-133">You can now click on the tiles to explore the default content included in the solution.</span></span>  

### <a name="next-steps"></a><span data-ttu-id="ec86b-134">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="ec86b-134">Next Steps</span></span>
- <span data-ttu-id="ec86b-135">Esaminare il [contenuto predefinito](webpartcontent.md) incluso in WebPart.</span><span class="sxs-lookup"><span data-stu-id="ec86b-135">Explore the [default content](webpartcontent.md) included in the webpart.</span></span>
- <span data-ttu-id="ec86b-136">[Personalizzare](customization.md) l'esperienza di formazione per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="ec86b-136">[Customize](customization.md) the training experience for your organization.</span></span>
- <span data-ttu-id="ec86b-137">[Guidare l'adozione](driveadoption.md) della soluzione di formazione.</span><span class="sxs-lookup"><span data-stu-id="ec86b-137">[Drive adoption](driveadoption.md) of your training solution.</span></span>

