---
author: karuanag
ms.author: karuanag
manager: alexb
title: Personalizzare e condividere playlist
ms.date: 02/10/2019
description: Creare playlist personalizzate da contenuto esistente o da nuove pagine di SharePoint
ms.service: sharepoint-online
audience: itpro
ms.topic: article
ms.openlocfilehash: 31a0e5524181d26f4d62ae7206636c9e553b6f8f
ms.sourcegitcommit: 97e175e5ff5b6a9e0274d5ec9b39fdf7e18eb387
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/25/2021
ms.locfileid: "52000212"
---
# <a name="customize-and-share-playlists"></a><span data-ttu-id="5dadd-103">Personalizzare e condividere playlist</span><span class="sxs-lookup"><span data-stu-id="5dadd-103">Customize and share playlists</span></span>

## <a name="create-a-playlist"></a><span data-ttu-id="5dadd-104">Creare una playlist</span><span class="sxs-lookup"><span data-stu-id="5dadd-104">Create a Playlist</span></span>

<span data-ttu-id="5dadd-105">Una playlist è una compilazione di "asset".</span><span class="sxs-lookup"><span data-stu-id="5dadd-105">A playlist is a compliation of "assets".</span></span> <span data-ttu-id="5dadd-106">Un "asset" è una pagina di SharePoint o un elemento esistente del contenuto di formazione Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5dadd-106">An "asset" is a SharePoint page or existing item of Microsoft training content.</span></span> <span data-ttu-id="5dadd-107">Quando crei una playlist, seleziona gli asset che vanno insieme per creare un percorso di apprendimento per l'utente.</span><span class="sxs-lookup"><span data-stu-id="5dadd-107">When you create a playlist you select assets that go together to create a learning path for your user.</span></span>  

<span data-ttu-id="5dadd-108">Il vantaggio dell'aggiunta di pagine di SharePoint è che è possibile creare pagine di SharePoint con video di YouTube o video ospitati nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5dadd-108">The benefit of adding SharePoint pages is that you can create SharePoint pages with a YouTube videos or videos hosted in your organization.</span></span> <span data-ttu-id="5dadd-109">È inoltre possibile creare pagine con moduli o altro contenuto di Office 365.</span><span class="sxs-lookup"><span data-stu-id="5dadd-109">You can also create pages with Forms or other Office 365 content.</span></span>  

#### <a name="step-1-create-a-sharepoint-page-for-your-playlist"></a><span data-ttu-id="5dadd-110">Passaggio 1: Creare una pagina di SharePoint per la playlist</span><span class="sxs-lookup"><span data-stu-id="5dadd-110">Step 1: Create a SharePoint page for your playlist</span></span>
<span data-ttu-id="5dadd-111">In questo esempio verrà innanzitutto creata una pagina di SharePoint da aggiungere alla playlist.</span><span class="sxs-lookup"><span data-stu-id="5dadd-111">In this example, we’ll first create a SharePoint page to add to the playlist.</span></span> <span data-ttu-id="5dadd-112">Verrà creata una pagina con una web part video di YouTube e una web part Testo.</span><span class="sxs-lookup"><span data-stu-id="5dadd-112">We’ll create a page with a YouTube video web part and Text web part.</span></span>  <span data-ttu-id="5dadd-113">Queste istruzioni presuppongono che si utilizzi il servizio SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="5dadd-113">These instructions assume you are using the SharePoint Online service.</span></span> 

#### <a name="create-a-new-page"></a><span data-ttu-id="5dadd-114">Creare una nuova pagina</span><span class="sxs-lookup"><span data-stu-id="5dadd-114">Create a new page</span></span>
1.  <span data-ttu-id="5dadd-115">Selezionare il menu Impostazioni > contenuto del sito > pagine del sito > Nuova > Pagina sito.</span><span class="sxs-lookup"><span data-stu-id="5dadd-115">Select the Settings menu > Site Contents > Site Pages > New > Site Page.</span></span>
2.  <span data-ttu-id="5dadd-116">Nell'area del titolo digitare Use the Teams command box</span><span class="sxs-lookup"><span data-stu-id="5dadd-116">In the title area, type Use the Teams command box</span></span>
3.  <span data-ttu-id="5dadd-117">Selezionare la sezione Aggiungi nuovo e quindi selezionare Due colonne.</span><span class="sxs-lookup"><span data-stu-id="5dadd-117">Select the Add a new section, and then select Two Columns.</span></span>

![aggiunta di due colonne](media/clo365addtwocolumn.png)

4.  <span data-ttu-id="5dadd-119">Nella casella a sinistra selezionare Aggiungi una nuova web part e quindi incorporare.</span><span class="sxs-lookup"><span data-stu-id="5dadd-119">In the left-hand box, select Add a new web part, and then select Embed.</span></span> 
5.  <span data-ttu-id="5dadd-120">In un Web browser passare a questo URL https://youtu.be/wYrRCRphrp0 e ottenere il codice di incorporamento per il video.</span><span class="sxs-lookup"><span data-stu-id="5dadd-120">In a Web browser, go to this URL https://youtu.be/wYrRCRphrp0 and get the embed code for the video.</span></span> 
6.  <span data-ttu-id="5dadd-121">Nella web part Di SharePoint selezionare Aggiungi codice di incorporamento e quindi incollarlo nella casella Incorpora.</span><span class="sxs-lookup"><span data-stu-id="5dadd-121">In the SharePoint Web part, select Add Embed code and then paste it into the Embed box.</span></span> 
7.  <span data-ttu-id="5dadd-122">Nella casella a destra selezionare Aggiungi una nuova web part e quindi testo.</span><span class="sxs-lookup"><span data-stu-id="5dadd-122">In the right-hand box, select Add a new web part, and then select Text.</span></span> 
8.  <span data-ttu-id="5dadd-123">In un Web browser passare all'URL seguente: https://support.office.com/article/13c4e429-7324-4886-b377-5dbed539193b e copiare l'opzione Prova.</span><span class="sxs-lookup"><span data-stu-id="5dadd-123">In a Web browser, go to this URL: https://support.office.com/article/13c4e429-7324-4886-b377-5dbed539193b and copy the Try it!</span></span> <span data-ttu-id="5dadd-124">Istruzioni della pagina e incollarle nella web part Testo.</span><span class="sxs-lookup"><span data-stu-id="5dadd-124">Instructions from the page and paste them into the Text Web part.</span></span> <span data-ttu-id="5dadd-125">La pagina dovrebbe essere simile alla seguente.</span><span class="sxs-lookup"><span data-stu-id="5dadd-125">Your page should look like the following.</span></span> 
<span data-ttu-id="5dadd-126">![Pagina Incorpora](media/clo365teamscommandbox.png)</span><span class="sxs-lookup"><span data-stu-id="5dadd-126">![Embed page](media/clo365teamscommandbox.png)</span></span>
9.  <span data-ttu-id="5dadd-127">Fare **clic su** Pubblica e quindi copiare l'URL della pagina e incollarlo nel Blocco note</span><span class="sxs-lookup"><span data-stu-id="5dadd-127">Click **Publish**, and then copy the URL of the page and paste it in Notepad</span></span>

#### <a name="step-2-create-the-playlist"></a><span data-ttu-id="5dadd-128">Passaggio 2: Creare la playlist</span><span class="sxs-lookup"><span data-stu-id="5dadd-128">Step 2: Create the Playlist</span></span>

1. <span data-ttu-id="5dadd-129">Passare alla **pagina Amministrazione apprendimento personalizzata** nell'esperienza del sito.</span><span class="sxs-lookup"><span data-stu-id="5dadd-129">Navigate to the **Custom Learning Administration** page in your site experience.</span></span>
<span data-ttu-id="5dadd-130">![Schermata in cui selezionare Amministrazione apprendimento personalizzata.](media/custom_admin.png)</span><span class="sxs-lookup"><span data-stu-id="5dadd-130">![Screen where you select Custom Learning Administration.](media/custom_admin.png)</span></span>
1. <span data-ttu-id="5dadd-131">Verificare che **l'opzione Categoria** sia selezionata</span><span class="sxs-lookup"><span data-stu-id="5dadd-131">Make sure **Category** is selected</span></span> 
1. <span data-ttu-id="5dadd-132">Fai clic sulla categoria in cui vuoi che venga visualizzata la nuova playlist</span><span class="sxs-lookup"><span data-stu-id="5dadd-132">Click on the category where you'd like your new playlist to appear</span></span>
1. <span data-ttu-id="5dadd-133">Accanto al nome della categoria, fai clic sul simbolo più ![ Finestra con l'opzione Categoria e il segno più evidenziato.](media/custom_addplay.png)</span><span class="sxs-lookup"><span data-stu-id="5dadd-133">Next to the category name, click on the plus symbol ![Window with the Category option and the Plus sign highlighted.](media/custom_addplay.png)</span></span>

1. <span data-ttu-id="5dadd-134">Inserire i valori come illustrato nell'esempio seguente e selezionare **Crea**.</span><span class="sxs-lookup"><span data-stu-id="5dadd-134">Fill in the values as shown in the example below and select **Create**.</span></span> 
<span data-ttu-id="5dadd-135">![Pagina in cui immettere i dettagli della playlist.](media/custom_details.png)</span><span class="sxs-lookup"><span data-stu-id="5dadd-135">![Page where you enter playlist details.](media/custom_details.png)</span></span>
- <span data-ttu-id="5dadd-136">**Title** - Nome visualizzato della playlist</span><span class="sxs-lookup"><span data-stu-id="5dadd-136">**Title** - Display name of the playlist</span></span>
- <span data-ttu-id="5dadd-137">**Descrizione** - Informazioni su ciò che verrà appreso</span><span class="sxs-lookup"><span data-stu-id="5dadd-137">**Description** - Information about what will be learned</span></span>
- <span data-ttu-id="5dadd-138">**Categoria** : preselezionata in base alla selezione iniziale</span><span class="sxs-lookup"><span data-stu-id="5dadd-138">**Category** - Preselected based on your initial selection</span></span>
- <span data-ttu-id="5dadd-139">**Sottocategozia** - Preselezionata in base alla selezione inziale</span><span class="sxs-lookup"><span data-stu-id="5dadd-139">**Sub Category** - Preselected based on your intial selection</span></span>
- <span data-ttu-id="5dadd-140">**Tecnologia** - Seleziona come applicabile</span><span class="sxs-lookup"><span data-stu-id="5dadd-140">**Technology** - Select as applicable</span></span>
- <span data-ttu-id="5dadd-141">**Livello** - Principiante, Intermidate o Avanzato</span><span class="sxs-lookup"><span data-stu-id="5dadd-141">**Level** - Beginner, Intermidate or Advanced</span></span>
- <span data-ttu-id="5dadd-142">**Gruppo** di destinatari: in questo modo è possibile scegliere come destinazione il contenuto in base a un elenco predefinito di ruoli forniti da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5dadd-142">**Audience** - This allows you to target content based on a pre-defined list of roles provided by Microsoft.</span></span>

6. <span data-ttu-id="5dadd-143">Fare clic **su Salva dettagli**</span><span class="sxs-lookup"><span data-stu-id="5dadd-143">Click **Save Detail**</span></span>

> [!TIP]
> <span data-ttu-id="5dadd-144">Puoi personalizzare l'immagine dell'icona per la playlist.</span><span class="sxs-lookup"><span data-stu-id="5dadd-144">You can customize the icon image for your playlist.</span></span>  <span data-ttu-id="5dadd-145">Fai clic sull'icona dell'immagine e inserisci un URL di un'immagine caricata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="5dadd-145">Click the image icon and insert an URL of a previously uploaded image.</span></span>  <span data-ttu-id="5dadd-146">Verificare che l'immagine si trovi all'interno della raccolta siti di apprendimento personalizzato o in un'altra posizione in cui tutti gli utenti avranno accesso al file.</span><span class="sxs-lookup"><span data-stu-id="5dadd-146">Make sure the image is located within the Custom Learning site collection or in another location that all users will have access to the file.</span></span>  
<span data-ttu-id="5dadd-147">![Scegliere una finestra immagine.](media/custom_image.png)</span><span class="sxs-lookup"><span data-stu-id="5dadd-147">![Choose an image window.](media/custom_image.png)</span></span>

#### <a name="step-3-add-assets-to-the-playlist"></a><span data-ttu-id="5dadd-148">Passaggio 3: Aggiungere asset alla playlist</span><span class="sxs-lookup"><span data-stu-id="5dadd-148">Step 3: Add assets to the playlist</span></span>
<span data-ttu-id="5dadd-149">In questo passaggio verranno aggiunti asset esistenti da Microsoft e dalla pagina di SharePoint creata alla playlist.</span><span class="sxs-lookup"><span data-stu-id="5dadd-149">In this step, you’ll add existing assets from Microsoft and the SharePoint page you created to the playlist.</span></span> 

1. <span data-ttu-id="5dadd-150">Dopo aver salvato i dettagli per la playlist, puoi usare la ricerca di asset esistenti.</span><span class="sxs-lookup"><span data-stu-id="5dadd-150">Once you have saved the details for your Playlist you can use the Search for Existing Assets.</span></span>
1. <span data-ttu-id="5dadd-151">**Immettere un termine di ricerca** per visualizzare un elenco di risorse predefinite disponibili in altre playlist.</span><span class="sxs-lookup"><span data-stu-id="5dadd-151">**Enter in any search term** to see a list of predefined assets that are available from other playlists.</span></span> <span data-ttu-id="5dadd-152">**Fai clic sul nome** di una risorsa per includerla nella nuova playlist.</span><span class="sxs-lookup"><span data-stu-id="5dadd-152">**Click on the name** of an asset to include it in your new playlist.</span></span><br/>
<span data-ttu-id="5dadd-153">![Pagina Risorse playlist](media/custom_slist.png)</span><span class="sxs-lookup"><span data-stu-id="5dadd-153">![Playlist assets page](media/custom_slist.png)</span></span>

<span data-ttu-id="5dadd-154">È inoltre possibile aggiungere la pagina di SharePoint creata in precedenza o crearne una da zero nell'esperienza.</span><span class="sxs-lookup"><span data-stu-id="5dadd-154">You can also add the SharePoint page you created earlier or create one from scratch in the experience.</span></span>

1. <span data-ttu-id="5dadd-155">Fai clic **sull'opzione Nuovo asset** nella finestra di dialogo Asset playlist.</span><span class="sxs-lookup"><span data-stu-id="5dadd-155">Click on the **New Asset** option in the Playlist Assets dialog.</span></span>
1. <span data-ttu-id="5dadd-156">Assegnare un titolo **all'asset.**</span><span class="sxs-lookup"><span data-stu-id="5dadd-156">Give your asset a **Title**.</span></span> <span data-ttu-id="5dadd-157">Dopo l'immissione, verranno visualizzate altre opzioni.</span><span class="sxs-lookup"><span data-stu-id="5dadd-157">Once entered, additional options will display.</span></span>
<span data-ttu-id="5dadd-158">![Modulo in cui immettere il titolo e ulteriori dettagli.](media/custom_newpage.png)</span><span class="sxs-lookup"><span data-stu-id="5dadd-158">![Form where you enter your title and additional details.](media/custom_newpage.png)</span></span>
1. <span data-ttu-id="5dadd-159">È ora possibile creare una nuova pagina di asset in SharePoint Online o immettere l'URL di una pagina esistente per aggiungerla alla playlist personalizzata.</span><span class="sxs-lookup"><span data-stu-id="5dadd-159">You can now create a new asset page in SharePoint Online or enter in the URL of an existing page to add it to your custom playlist.</span></span> 
1. <span data-ttu-id="5dadd-160">**I** campi **Categoria, Categoria** secondaria **e** Tecnologia verranno pre-popolati in base alle selezioni precedenti per questa playlist.</span><span class="sxs-lookup"><span data-stu-id="5dadd-160">**Category**, **Sub Category** and **Technology** fields will be pre-populated based on your previous selections for this playlist.</span></span>
1. <span data-ttu-id="5dadd-161">Effettuare le selezioni appropriate per Livello e Gruppo di destinatari per questa singola risorsa.</span><span class="sxs-lookup"><span data-stu-id="5dadd-161">Make the appropriate selections for Level and Audience for this individual asset.</span></span>  
1. <span data-ttu-id="5dadd-162">Fai **clic su Salva** risorsa per aggiungerlo alla playlist personalizzata</span><span class="sxs-lookup"><span data-stu-id="5dadd-162">Click **Save Asset** to add it to the custom playlist</span></span>
1. <span data-ttu-id="5dadd-163">Ripeti questi passaggi, cercando o aggiungendo singole pagine, fino al completamento della playlist.</span><span class="sxs-lookup"><span data-stu-id="5dadd-163">Repeat these steps, either searching or adding individual pages, until your playlist is complete.</span></span> 
1. <span data-ttu-id="5dadd-164">Fare **clic su Chiudi playlist** per salvare</span><span class="sxs-lookup"><span data-stu-id="5dadd-164">Click **Close Playlist** to save</span></span>

<span data-ttu-id="5dadd-165">La playlist con questo contenuto sarà ora disponibile ovunque sia stata installata/incorporata la web part Apprendimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="5dadd-165">Your playlist with this content will now be available anywhere you have installed / embedded the Custom Learning webpart.</span></span> 

> [!NOTE]
> <span data-ttu-id="5dadd-166">Se commette un errore dopo aver chiuso la playlist, puoi eliminarla dalla categoria facendo clic sulla X accanto al nome della playlist.</span><span class="sxs-lookup"><span data-stu-id="5dadd-166">If you make a mistake once you have closed the playlist, you can delete it from the category by clicking the X next to the playlist name.</span></span>  

#### <a name="things-to-think-about"></a><span data-ttu-id="5dadd-167">Aspetti da riflettere</span><span class="sxs-lookup"><span data-stu-id="5dadd-167">Things to Think About</span></span>

<span data-ttu-id="5dadd-168">Le playlist personalizzate possono essere usate per assistere gli utenti finali in un'ampia gamma di attività.</span><span class="sxs-lookup"><span data-stu-id="5dadd-168">Custom playlists can be used to assist your end users in a variety of tasks.</span></span>  <span data-ttu-id="5dadd-169">Hai un modulo di richiesta di tempo libero?</span><span class="sxs-lookup"><span data-stu-id="5dadd-169">Do you have a time off request form?</span></span>  <span data-ttu-id="5dadd-170">Un modulo per richiedere attrezzature hardware?</span><span class="sxs-lookup"><span data-stu-id="5dadd-170">A form to request hardware equipment?</span></span>  <span data-ttu-id="5dadd-171">Tutte le risorse di formazione esistenti possono essere programmate nell'esperienza.</span><span class="sxs-lookup"><span data-stu-id="5dadd-171">Any existing training assets can be programmed into the experience.</span></span>  

## <a name="share-playlists"></a><span data-ttu-id="5dadd-172">Condividere playlist</span><span class="sxs-lookup"><span data-stu-id="5dadd-172">Share Playlists</span></span>

1. <span data-ttu-id="5dadd-173">Passare a qualsiasi playlist all'interno della web part o dell'esperienza del sito</span><span class="sxs-lookup"><span data-stu-id="5dadd-173">Navigate to any playlist within the webpart or site experience</span></span>
1. <span data-ttu-id="5dadd-174">Nell'angolo in alto a sinistra verranno visualizzate tre icone</span><span class="sxs-lookup"><span data-stu-id="5dadd-174">In the upper left hand corner you will see three icons</span></span>
1. <span data-ttu-id="5dadd-175">Fare clic sull'icona che rappresenta un collegamento</span><span class="sxs-lookup"><span data-stu-id="5dadd-175">Click on the icon representing a link</span></span>
1. <span data-ttu-id="5dadd-176">Copia l'URL nella schermata della playlist ![ in cui fai clic su Copia accanto all'URL.](media/share.png)</span><span class="sxs-lookup"><span data-stu-id="5dadd-176">Copy the URL to the playlist ![Screen where you click Copy next to the URL.](media/share.png)</span></span>
<span data-ttu-id="5dadd-177">Questo URL può ora essere inserito nella struttura di spostamento del sito o utilizzato in altre comunicazioni per portare i dipendenti direttamente a tale playlist.</span><span class="sxs-lookup"><span data-stu-id="5dadd-177">This URL can now be inserted in your site navigation or utilized in other communications to take your employees directly to that playlist.</span></span> 

### <a name="next-steps---drive-adoption"></a><span data-ttu-id="5dadd-178">Passaggi successivi - [Guidare l'adozione](driveadoption.md)</span><span class="sxs-lookup"><span data-stu-id="5dadd-178">Next Steps - [Drive Adoption](driveadoption.md)</span></span>
