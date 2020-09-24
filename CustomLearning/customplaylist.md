---
author: karuanag
ms.author: karuanag
title: Personalizzare e condividere playlist
ms.date: 02/10/2019
description: Creare playlist personalizzate dal contenuto esistente o dalle nuove pagine di SharePoint
ms.service: sharepoint online
ms.openlocfilehash: 6258668b417ba496c7ac75e36ce2bc1f1dae27a5
ms.sourcegitcommit: ee4aebf60893887ae95a1294a9ad8975539ea762
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/23/2020
ms.locfileid: "48233808"
---
# <a name="customize-and-share-playlists"></a><span data-ttu-id="26fe9-103">Personalizzare e condividere playlist</span><span class="sxs-lookup"><span data-stu-id="26fe9-103">Customize and Share Playlists</span></span>

## <a name="create-a-playlist"></a><span data-ttu-id="26fe9-104">Creare una playlist</span><span class="sxs-lookup"><span data-stu-id="26fe9-104">Create a Playlist</span></span>

<span data-ttu-id="26fe9-105">Una playlist è una Compliation di "asset".</span><span class="sxs-lookup"><span data-stu-id="26fe9-105">A playlist is a compliation of "assets".</span></span> <span data-ttu-id="26fe9-106">"Asset" è una pagina di SharePoint o un elemento esistente di Microsoft Training Content.</span><span class="sxs-lookup"><span data-stu-id="26fe9-106">An "asset" is a SharePoint page or existing item of Microsoft training content.</span></span> <span data-ttu-id="26fe9-107">Quando si crea una playlist, si selezionano risorse che vanno insieme per creare un percorso di apprendimento per l'utente.</span><span class="sxs-lookup"><span data-stu-id="26fe9-107">When you create a playlist you select assets that go together to create a learning path for your user.</span></span>  

<span data-ttu-id="26fe9-108">Il vantaggio dell'aggiunta di pagine di SharePoint è che è possibile creare pagine di SharePoint con video o video di YouTube ospitati nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="26fe9-108">The benefit of adding SharePoint pages is that you can create SharePoint pages with a YouTube videos or videos hosted in your organization.</span></span> <span data-ttu-id="26fe9-109">È inoltre possibile creare pagine con moduli o altri contenuti di Office 365.</span><span class="sxs-lookup"><span data-stu-id="26fe9-109">You can also create pages with Forms or other Office 365 content.</span></span>  

#### <a name="step-1-create-a-sharepoint-page-for-your-playlist"></a><span data-ttu-id="26fe9-110">Passaggio 1: creare una pagina di SharePoint per la playlist</span><span class="sxs-lookup"><span data-stu-id="26fe9-110">Step 1: Create a SharePoint page for your playlist</span></span>
<span data-ttu-id="26fe9-111">In questo esempio viene creata prima una pagina di SharePoint da aggiungere alla playlist.</span><span class="sxs-lookup"><span data-stu-id="26fe9-111">In this example, we’ll first create a SharePoint page to add to the playlist.</span></span> <span data-ttu-id="26fe9-112">Verrà creata una pagina con una Web part video di YouTube e una Web part di testo.</span><span class="sxs-lookup"><span data-stu-id="26fe9-112">We’ll create a page with a YouTube video web part and Text web part.</span></span>  <span data-ttu-id="26fe9-113">Queste istruzioni presuppongono che si utilizzi il servizio SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="26fe9-113">These instructions assume you are using the SharePoint Online service.</span></span> 

#### <a name="create-a-new-page"></a><span data-ttu-id="26fe9-114">Creare una nuova pagina</span><span class="sxs-lookup"><span data-stu-id="26fe9-114">Create a new page</span></span>
1.  <span data-ttu-id="26fe9-115">Selezionare il menu impostazioni > contenuto del sito > pagine del sito > nuova pagina del sito >.</span><span class="sxs-lookup"><span data-stu-id="26fe9-115">Select the Settings menu > Site Contents > Site Pages > New > Site Page.</span></span>
2.  <span data-ttu-id="26fe9-116">Nell'area titolo, digitare use the teams Command Box.</span><span class="sxs-lookup"><span data-stu-id="26fe9-116">In the title area, type Use the Teams command box</span></span>
3.  <span data-ttu-id="26fe9-117">Selezionare la sezione Aggiungi una nuova e quindi selezionare due colonne.</span><span class="sxs-lookup"><span data-stu-id="26fe9-117">Select the Add a new section, and then select Two Columns.</span></span>

![Aggiunta di due colonne](media/clo365addtwocolumn.png)

4.  <span data-ttu-id="26fe9-119">Nella casella a sinistra, selezionare Aggiungi una nuova Web part, quindi fare clic su incorpora.</span><span class="sxs-lookup"><span data-stu-id="26fe9-119">In the left-hand box, select Add a new web part, and then select Embed.</span></span> 
5.  <span data-ttu-id="26fe9-120">In un Web browser, passare a questo URL https://youtu.be/wYrRCRphrp0 e ottenere il codice di incorporamento per il video.</span><span class="sxs-lookup"><span data-stu-id="26fe9-120">In a Web browser, go to this URL https://youtu.be/wYrRCRphrp0 and get the embed code for the video.</span></span> 
6.  <span data-ttu-id="26fe9-121">Nella web part di SharePoint, selezionare Aggiungi codice embed e incollarlo nella casella incorpora.</span><span class="sxs-lookup"><span data-stu-id="26fe9-121">In the SharePoint Web part, select Add Embed code and then paste it into the Embed box.</span></span> 
7.  <span data-ttu-id="26fe9-122">Nella casella a destra, selezionare Aggiungi una nuova Web part, quindi selezionare testo.</span><span class="sxs-lookup"><span data-stu-id="26fe9-122">In the right-hand box, select Add a new web part, and then select Text.</span></span> 
8.  <span data-ttu-id="26fe9-123">In un Web browser, passare a questo URL: https://support.office.com/article/13c4e429-7324-4886-b377-5dbed539193b e copiare la prova!</span><span class="sxs-lookup"><span data-stu-id="26fe9-123">In a Web browser, go to this URL: https://support.office.com/article/13c4e429-7324-4886-b377-5dbed539193b and copy the Try it!</span></span> <span data-ttu-id="26fe9-124">Istruzioni dalla pagina e incollarle nella web part testo.</span><span class="sxs-lookup"><span data-stu-id="26fe9-124">Instructions from the page and paste them into the Text Web part.</span></span> <span data-ttu-id="26fe9-125">La pagina dovrebbe essere simile alla seguente.</span><span class="sxs-lookup"><span data-stu-id="26fe9-125">Your page should look like the following.</span></span> 

![Pagina incorporamento](media/clo365teamscommandbox.png)

9.  <span data-ttu-id="26fe9-127">Fare clic su **pubblica**e quindi copiare l'URL della pagina e incollarlo nel blocco note</span><span class="sxs-lookup"><span data-stu-id="26fe9-127">Click **Publish**, and then copy the URL of the page and paste it in Notepad</span></span>

#### <a name="step-2-create-the-playlist"></a><span data-ttu-id="26fe9-128">Passaggio 2: creare la playlist</span><span class="sxs-lookup"><span data-stu-id="26fe9-128">Step 2: Create the Playlist</span></span>

1. <span data-ttu-id="26fe9-129">Passare alla pagina di **amministrazione dell'apprendimento personalizzata** nell'esperienza del sito.</span><span class="sxs-lookup"><span data-stu-id="26fe9-129">Navigate to the **Custom Learning Administration** page in your site experience.</span></span>
<span data-ttu-id="26fe9-130">![custom_admin.png](media/custom_admin.png)</span><span class="sxs-lookup"><span data-stu-id="26fe9-130">![custom_admin.png](media/custom_admin.png)</span></span>
1. <span data-ttu-id="26fe9-131">Verificare che la **categoria** sia selezionata</span><span class="sxs-lookup"><span data-stu-id="26fe9-131">Make sure **Category** is selected</span></span> 
1. <span data-ttu-id="26fe9-132">Fare clic sulla categoria in cui si desidera visualizzare la nuova playlist</span><span class="sxs-lookup"><span data-stu-id="26fe9-132">Click on the category where you'd like your new playlist to appear</span></span>
1. <span data-ttu-id="26fe9-133">Accanto al nome della categoria, fare clic sul segno più ![custom_addplay.png](media/custom_addplay.png)</span><span class="sxs-lookup"><span data-stu-id="26fe9-133">Next to the category name, click on the plus symbol ![custom_addplay.png](media/custom_addplay.png)</span></span>

1. <span data-ttu-id="26fe9-134">Inserire i valori come illustrato nell'esempio riportato di seguito e selezionare **Crea**.</span><span class="sxs-lookup"><span data-stu-id="26fe9-134">Fill in the values as shown in the example below and select **Create**.</span></span> 
<span data-ttu-id="26fe9-135">![custom_details.png](media/custom_details.png)</span><span class="sxs-lookup"><span data-stu-id="26fe9-135">![custom_details.png](media/custom_details.png)</span></span>
- <span data-ttu-id="26fe9-136">**Titolo** -nome visualizzato della playlist</span><span class="sxs-lookup"><span data-stu-id="26fe9-136">**Title** - Display name of the playlist</span></span>
- <span data-ttu-id="26fe9-137">**Descrizione** -informazioni su ciò che verrà imparato</span><span class="sxs-lookup"><span data-stu-id="26fe9-137">**Description** - Information about what will be learned</span></span>
- <span data-ttu-id="26fe9-138">**Categoria** -preselezionata in base alla selezione iniziale</span><span class="sxs-lookup"><span data-stu-id="26fe9-138">**Category** - Preselected based on your initial selection</span></span>
- <span data-ttu-id="26fe9-139">**Sottocategoria** -preselezionata in base alla selezione iniziale</span><span class="sxs-lookup"><span data-stu-id="26fe9-139">**Sub Category** - Preselected based on your intial selection</span></span>
- <span data-ttu-id="26fe9-140">**Tecnologia** : selezionare applicabile</span><span class="sxs-lookup"><span data-stu-id="26fe9-140">**Technology** - Select as applicable</span></span>
- <span data-ttu-id="26fe9-141">**Level** -Beginner, Intermidate o Advanced</span><span class="sxs-lookup"><span data-stu-id="26fe9-141">**Level** - Beginner, Intermidate or Advanced</span></span>
- <span data-ttu-id="26fe9-142">Gruppo di **destinatari** : consente di assegnare il contenuto in base a un elenco predefinito di ruoli forniti da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="26fe9-142">**Audience** - This allows you to target content based on a pre-defined list of roles provided by Microsoft.</span></span>

6. <span data-ttu-id="26fe9-143">Fare clic su **Salva dettaglio**</span><span class="sxs-lookup"><span data-stu-id="26fe9-143">Click **Save Detail**</span></span>

> [!TIP]
> <span data-ttu-id="26fe9-144">È possibile personalizzare l'immagine dell'icona per la playlist.</span><span class="sxs-lookup"><span data-stu-id="26fe9-144">You can customize the icon image for your playlist.</span></span>  <span data-ttu-id="26fe9-145">Fare clic sull'icona dell'immagine e inserire un URL di un'immagine caricata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="26fe9-145">Click the image icon and insert an URL of a previously uploaded image.</span></span>  <span data-ttu-id="26fe9-146">Verificare che l'immagine si trovi all'interno della raccolta siti di apprendimento personalizzato o in un'altra posizione in cui tutti gli utenti avranno accesso al file.</span><span class="sxs-lookup"><span data-stu-id="26fe9-146">Make sure the image is located within the Custom Learning site collection or in another location that all users will have access to the file.</span></span>  
<span data-ttu-id="26fe9-147">![custom_image.png](media/custom_image.png)</span><span class="sxs-lookup"><span data-stu-id="26fe9-147">![custom_image.png](media/custom_image.png)</span></span>

#### <a name="step-3-add-assets-to-the-playlist"></a><span data-ttu-id="26fe9-148">Passaggio 3: aggiungere risorse alla playlist</span><span class="sxs-lookup"><span data-stu-id="26fe9-148">Step 3: Add assets to the playlist</span></span>
<span data-ttu-id="26fe9-149">In questo passaggio, si aggiungono le risorse esistenti da Microsoft e la pagina di SharePoint creata per la playlist.</span><span class="sxs-lookup"><span data-stu-id="26fe9-149">In this step, you’ll add existing assets from Microsoft and the SharePoint page you created to the playlist.</span></span> 

1. <span data-ttu-id="26fe9-150">Dopo aver salvato i dettagli per la playlist, è possibile utilizzare la ricerca per le risorse esistenti.</span><span class="sxs-lookup"><span data-stu-id="26fe9-150">Once you have saved the details for your Playlist you can use the Search for Existing Assets.</span></span>
1. <span data-ttu-id="26fe9-151">**Immettere un termine di ricerca** per visualizzare un elenco di risorse predefinite che sono disponibili da altre playlist.</span><span class="sxs-lookup"><span data-stu-id="26fe9-151">**Enter in any search term** to see a list of predefined assets that are available from other playlists.</span></span> <span data-ttu-id="26fe9-152">**Fare clic sul nome** di una risorsa per includerla nella nuova playlist.</span><span class="sxs-lookup"><span data-stu-id="26fe9-152">**Click on the name** of an asset to include it in your new playlist.</span></span>
<span data-ttu-id="26fe9-153">![custom_slist.png](media/custom_slist.png)</span><span class="sxs-lookup"><span data-stu-id="26fe9-153">![custom_slist.png](media/custom_slist.png)</span></span>

<span data-ttu-id="26fe9-154">È inoltre possibile aggiungere la pagina di SharePoint creata in precedenza o crearne una da zero nell'esperienza.</span><span class="sxs-lookup"><span data-stu-id="26fe9-154">You can also add the SharePoint page you created earlier or create one from scratch in the experience.</span></span>

1. <span data-ttu-id="26fe9-155">Fare clic sull'opzione **nuova risorsa** nella finestra di dialogo risorse playlist.</span><span class="sxs-lookup"><span data-stu-id="26fe9-155">Click on the **New Asset** option in the Playlist Assets dialog</span></span>
1. <span data-ttu-id="26fe9-156">Assegnare un **titolo**alla propria risorsa.</span><span class="sxs-lookup"><span data-stu-id="26fe9-156">Give your asset a **Title**.</span></span> <span data-ttu-id="26fe9-157">Una volta immessa, vengono visualizzate altre opzioni ![custom_newpage.png](media/custom_newpage.png)</span><span class="sxs-lookup"><span data-stu-id="26fe9-157">Once entered, additional options will display ![custom_newpage.png](media/custom_newpage.png)</span></span>
1. <span data-ttu-id="26fe9-158">È ora possibile creare una nuova pagina di asset in SharePoint Online o immettere l'URL di una pagina esistente per aggiungerla alla playlist personalizzata.</span><span class="sxs-lookup"><span data-stu-id="26fe9-158">You can now create a new asset page in SharePoint Online or enter in the URL of an existing page to add it to your custom playlist.</span></span> 
1. <span data-ttu-id="26fe9-159">I campi **categoria**, **sottocategoria** e **tecnologia** verranno prepopolati in base alle selezioni precedenti per la playlist.</span><span class="sxs-lookup"><span data-stu-id="26fe9-159">**Category**, **Sub Category** and **Technology** fields will be pre-populated based on your previous selections for this playlist.</span></span>
1. <span data-ttu-id="26fe9-160">Effettuare le selezioni appropriate per il livello e il gruppo di destinatari per questo singolo cespite.</span><span class="sxs-lookup"><span data-stu-id="26fe9-160">Make the appropriate selections for Level and Audience for this individual asset.</span></span>  
1. <span data-ttu-id="26fe9-161">Fare clic su **Salva risorsa** per aggiungerla all'elenco di riproduzione personalizzato</span><span class="sxs-lookup"><span data-stu-id="26fe9-161">Click **Save Asset** to add it to the custom playlist</span></span>
1. <span data-ttu-id="26fe9-162">Ripetere questi passaggi, cercando o aggiungendo singole pagine, finché la playlist non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="26fe9-162">Repeat these steps, either searching or adding individual pages, until your playlist is complete.</span></span> 
1. <span data-ttu-id="26fe9-163">Fare clic su **Chiudi playlist** per salvare</span><span class="sxs-lookup"><span data-stu-id="26fe9-163">Click **Close Playlist** to save</span></span>

<span data-ttu-id="26fe9-164">L'elenco di riproduzione con questo contenuto sarà ora disponibile ovunque sia stato installato/incorporato il WebPart di apprendimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="26fe9-164">Your playlist with this content will now be available anywhere you have installed / embedded the Custom Learning webpart.</span></span> 

> [!NOTE]
> <span data-ttu-id="26fe9-165">Se si commette un errore dopo aver chiuso la playlist, è possibile eliminarla dalla categoria facendo clic sulla X accanto al nome della playlist.</span><span class="sxs-lookup"><span data-stu-id="26fe9-165">If you make a mistake once you have closed the playlist, you can delete it from the category by clicking the X next to the playlist name.</span></span>  

#### <a name="things-to-think-about"></a><span data-ttu-id="26fe9-166">Aspetti da considerare</span><span class="sxs-lookup"><span data-stu-id="26fe9-166">Things to Think About</span></span>

<span data-ttu-id="26fe9-167">Gli elenchi di riproduzione personalizzati possono essere utilizzati per assistere gli utenti finali in una vasta gamma di attività.</span><span class="sxs-lookup"><span data-stu-id="26fe9-167">Custom playlists can be used to assist your end users in a variety of tasks.</span></span>  <span data-ttu-id="26fe9-168">Si dispone di un modulo di richiesta di tempo di disattivazione?</span><span class="sxs-lookup"><span data-stu-id="26fe9-168">Do you have a time off request form?</span></span>  <span data-ttu-id="26fe9-169">Un modulo per richiedere apparecchiature hardware?</span><span class="sxs-lookup"><span data-stu-id="26fe9-169">A form to request hardware equipment?</span></span>  <span data-ttu-id="26fe9-170">Tutte le risorse formative esistenti possono essere programmate nell'esperienza.</span><span class="sxs-lookup"><span data-stu-id="26fe9-170">Any existing training assets can be programmed into the experience.</span></span>  

## <a name="share-playlists"></a><span data-ttu-id="26fe9-171">Condivisione di playlist</span><span class="sxs-lookup"><span data-stu-id="26fe9-171">Share Playlists</span></span>

1. <span data-ttu-id="26fe9-172">Passare a una playlist all'interno di WebPart o di un'esperienza del sito</span><span class="sxs-lookup"><span data-stu-id="26fe9-172">Navigate to any playlist within the webpart or site experience</span></span>
1. <span data-ttu-id="26fe9-173">Nell'angolo in alto a sinistra vengono visualizzate tre icone</span><span class="sxs-lookup"><span data-stu-id="26fe9-173">In the upper left hand corner you will see three icons</span></span>
1. <span data-ttu-id="26fe9-174">Fare clic sull'icona che rappresenta un collegamento</span><span class="sxs-lookup"><span data-stu-id="26fe9-174">Click on the icon representing a link</span></span>
1. <span data-ttu-id="26fe9-175">Copiare l'URL nella playlist</span><span class="sxs-lookup"><span data-stu-id="26fe9-175">Copy the URL to the playlist</span></span>

<span data-ttu-id="26fe9-176">![share.png](media/share.png) questo URL ora può essere inserito nella struttura di spostamento del sito o utilizzato in altre comunicazioni per portare i dipendenti direttamente a quella playlist.</span><span class="sxs-lookup"><span data-stu-id="26fe9-176">![share.png](media/share.png) This URL can now be inserted in your site navigation or utilized in other communications to take your employees directly to that playlist.</span></span> 

### <a name="next-steps---drive-adoption"></a><span data-ttu-id="26fe9-177">Passaggi successivi: [adozione dell'unità](driveadoption.md)</span><span class="sxs-lookup"><span data-stu-id="26fe9-177">Next Steps - [Drive Adoption](driveadoption.md)</span></span>
