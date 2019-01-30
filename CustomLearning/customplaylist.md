# <a name="customize-the-services-and-playlists"></a><span data-ttu-id="eab96-101">Personalizzare i servizi e gli elenchi di riproduzione</span><span class="sxs-lookup"><span data-stu-id="eab96-101">Customize the Services and Playlists</span></span>

<span data-ttu-id="eab96-p101">Per impostazione predefinita l'esperienza del sito e della Web part includere contenuto per tutti i servizi di Office 365.  Se solo alcune o tutte le questi servizi sono disponibili all'interno della società è possibile modificare il contenuto è disponibile per gli utenti.  In questo articolo è verrà personalizzare il contenuto di Web part.</span><span class="sxs-lookup"><span data-stu-id="eab96-p101">By default both the site experience and the webpart include content for all Office 365 services.  If only all or some of these services are available in your company you can adjust what content is available to your users.  In this article we will customize the webpart content.</span></span>  

## <a name="customizing-the-webpart-content"></a><span data-ttu-id="eab96-105">La personalizzazione del contenuto Web part</span><span class="sxs-lookup"><span data-stu-id="eab96-105">Customizing the webpart content</span></span>

<span data-ttu-id="eab96-106">La Web part personalizzata Learning offre due funzionalità chiave:</span><span class="sxs-lookup"><span data-stu-id="eab96-106">The Custom Learning webpart provides two key features:</span></span>
- <span data-ttu-id="eab96-107">Mostra/Nascondi tecnologie</span><span class="sxs-lookup"><span data-stu-id="eab96-107">Hide/Show Technologies</span></span>
- <span data-ttu-id="eab96-108">Creare un elenco di riproduzione</span><span class="sxs-lookup"><span data-stu-id="eab96-108">Create a Playlist</span></span>

### <a name="hide-or-show-technology-categories"></a><span data-ttu-id="eab96-109">Categorie di tecnologia Mostra o Nascondi</span><span class="sxs-lookup"><span data-stu-id="eab96-109">Hide or Show Technology Categories</span></span>

<span data-ttu-id="eab96-110">Per nascondere e visualizzare contenuto nella Web part:</span><span class="sxs-lookup"><span data-stu-id="eab96-110">To hide and show content in the Web part:</span></span> 
1.  <span data-ttu-id="eab96-111">Fare clic sul menu a discesa della Web part e quindi fare clic su Mostra/Nascondi tecnologie</span><span class="sxs-lookup"><span data-stu-id="eab96-111">Click the dropdown menu on the webpart, then click Hide/Show Technologies</span></span>

![Opzione di menu](media/clohideshow.png)

2. <span data-ttu-id="eab96-113">Selezionare un checkox per nascondere o visualizzare una tecnologia e selezionare **Applica**.</span><span class="sxs-lookup"><span data-stu-id="eab96-113">Select a checkox to hide or show a technology and select **Apply**.</span></span>

![Opzioni di tecnologia](media/clohideshow1.png)

### <a name="create-a-playlist"></a><span data-ttu-id="eab96-115">Creare un elenco di riproduzione</span><span class="sxs-lookup"><span data-stu-id="eab96-115">Create a Playlist</span></span>

<span data-ttu-id="eab96-p102">Un elenco di riproduzione è compliation delle "risorse". Una risorsa"" è una pagina di SharePoint o un elemento esistente del contenuto per la formazione Microsoft. Quando si crea un elenco di riproduzione si selezionano risorse correlate per creare un percorso di apprendimento per l'utente.</span><span class="sxs-lookup"><span data-stu-id="eab96-p102">A playlist is a compliation of "assets". An "asset" is a SharePoint page or existing item of Microsoft training content. When you create a playlist you select assets that go together to create a learning path for your user.</span></span>  

<span data-ttu-id="eab96-p103">I vantaggi dell'aggiunta di pagine di SharePoint sono che è possibile creare pagine di SharePoint con un YouTube video o video ospitati all'interno dell'organizzazione. È inoltre possibile creare pagine con moduli o altro contenuto di Office 365.</span><span class="sxs-lookup"><span data-stu-id="eab96-p103">The benefit of adding SharePoint pages is that you can create SharePoint pages with a YouTube videos or videos hosted in your organization. You can also create pages with Forms or other Office 365 content.</span></span>  

#### <a name="step-1-create-a-sharepoint-page-for-your-playlist"></a><span data-ttu-id="eab96-121">Passaggio 1: Creare una pagina di SharePoint per l'elenco di riproduzione</span><span class="sxs-lookup"><span data-stu-id="eab96-121">Step 1: Create a SharePoint page for your playlist</span></span>
<span data-ttu-id="eab96-p104">In questo esempio, si creerà innanzitutto una pagina di SharePoint da aggiungere all'elenco di riproduzione. Verrà creata una pagina con una YouTube video web part e web part di testo.  Queste istruzioni si presuppone che si utilizza il servizio SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="eab96-p104">In this example, we’ll first create a SharePoint page to add to the playlist. We’ll create a page with a YouTube video web part and Text web part.  These instructions assume you are using the SharePoint Online service.</span></span> 

#### <a name="create-a-new-page"></a><span data-ttu-id="eab96-125">Creare una nuova pagina</span><span class="sxs-lookup"><span data-stu-id="eab96-125">Create a new page</span></span>
1.  <span data-ttu-id="eab96-126">Selezionare le impostazioni dal menu gt _ contenuto del sito gt _ pagine del sito gt _ nuovo gt _ Page del sito.</span><span class="sxs-lookup"><span data-stu-id="eab96-126">Select the Settings menu > Site Contents > Site Pages > New > Site Page.</span></span>
2.  <span data-ttu-id="eab96-127">Nell'area titolo digitare utilizzare la finestra di comando team</span><span class="sxs-lookup"><span data-stu-id="eab96-127">In the title area, type Use the Teams command box</span></span>
3.  <span data-ttu-id="eab96-128">Selezionare la sezione aggiungere una nuova e quindi selezionare due colonne.</span><span class="sxs-lookup"><span data-stu-id="eab96-128">Select the Add a new section, and then select Two Columns.</span></span>

![aggiungere due colonne](media/clo365addtwocolumn.png)

4.  <span data-ttu-id="eab96-130">Nel riquadro sinistro, selezionare Aggiungi nuova web part e quindi selezionare Embed.</span><span class="sxs-lookup"><span data-stu-id="eab96-130">In the left-hand box, select Add a new web part, and then select Embed.</span></span> 
5.  <span data-ttu-id="eab96-131">In un Web browser, accedere a questo URL https://youtu.be/wYrRCRphrp0 e ottenere il codice di incorporamento del video.</span><span class="sxs-lookup"><span data-stu-id="eab96-131">In a Web browser, go to this URL https://youtu.be/wYrRCRphrp0 and get the embed code for the video.</span></span> 
6.  <span data-ttu-id="eab96-132">Nella Web part di SharePoint, selezionare Aggiungi incorporare codice e incollarlo nella casella Embed.</span><span class="sxs-lookup"><span data-stu-id="eab96-132">In the SharePoint Web part, select Add Embed code and then paste it into the Embed box.</span></span> 
7.  <span data-ttu-id="eab96-133">Nella casella a destra, selezionare Aggiungi nuova web part e quindi selezionare il testo.</span><span class="sxs-lookup"><span data-stu-id="eab96-133">In the right-hand box, select Add a new web part, and then select Text.</span></span> 
8.  <span data-ttu-id="eab96-p105">In un Web browser, accedere a questo URL: https://support.office.com/en-us/article/13c4e429-7324-4886-b377-5dbed539193b e copiare il blocco Try viene! Le istruzioni nella pagina e incollarli in testo Web part. Nella pagina dovrebbe essere simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="eab96-p105">In a Web browser, go to this URL: https://support.office.com/en-us/article/13c4e429-7324-4886-b377-5dbed539193b and copy the Try it! Instructions from the page and paste them into the Text Web part. Your page should look like the following.</span></span> 

![Inserimento di una pagina](media/clo365teamscommandbox.png)

9.  <span data-ttu-id="eab96-138">Fare clic su pubblica, quindi copiare l'URL della pagina e incollarlo nel blocco note</span><span class="sxs-lookup"><span data-stu-id="eab96-138">Click Publish, and then copy the URL of the page and paste it in Notepad</span></span>

#### <a name="step-2-create-the-playlist"></a><span data-ttu-id="eab96-139">Passaggio 2: Creare l'elenco di riproduzione</span><span class="sxs-lookup"><span data-stu-id="eab96-139">Step 2: Create the Playlist</span></span>
1.  <span data-ttu-id="eab96-p106">Passare a in cui è installata la Web part apprendimento personalizzato. L'esperienza completa del sito si trova nella pagina formazione di Office 365.</span><span class="sxs-lookup"><span data-stu-id="eab96-p106">Navigate to where you have installed the Custom Learning webpart. In the full site experience it is hosted on the Office 365 training page.</span></span> 
2.  <span data-ttu-id="eab96-142">Nel menu a discesa selezionare Crea nuovo elenco di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="eab96-142">From the dropdown menu select Create New Playlist.</span></span> 

![creare l'elenco personalizzato di riproduzione](media/clo365createplaylist.png)

3.  <span data-ttu-id="eab96-144">Immettere i valori come illustrato nell'esempio riportato di seguito e selezionare **Crea**.</span><span class="sxs-lookup"><span data-stu-id="eab96-144">Fill in the values as shown in the example below and select **Create**.</span></span> 

#### <a name="step-3-add-assets-to-the-playlist"></a><span data-ttu-id="eab96-145">Passaggio 3: Aggiungere risorse all'elenco di riproduzione</span><span class="sxs-lookup"><span data-stu-id="eab96-145">Step 3: Add assets to the playlist</span></span>
<span data-ttu-id="eab96-146">In questo passaggio si aggiungeranno risorse esistenti da Microsoft e la pagina di SharePoint creata per l'elenco di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="eab96-146">In this step, you’ll add existing assets from Microsoft and the SharePoint page you created to the playlist.</span></span> 

1.  <span data-ttu-id="eab96-147">Fare clic sul pulsante menu, quindi fare clic su Aggiungi risorse esistenti.</span><span class="sxs-lookup"><span data-stu-id="eab96-147">Click the menu button, then click Add Existing Asset.</span></span>

![aggiungere risorse](media/clo365addasset.png)

2.  <span data-ttu-id="eab96-149">Filtrare formazione su Office 365 App gt _ team di Microsoft</span><span class="sxs-lookup"><span data-stu-id="eab96-149">Filter on Office 365 Apps > Microsoft Teams Training</span></span>
3.  <span data-ttu-id="eab96-150">Aggiungere iniziale a Microsoft Teams, diventare il team operativi e avviare le chat ed effettuare chiamate.</span><span class="sxs-lookup"><span data-stu-id="eab96-150">Add Welcome to Microsoft Teams, Get your team up and running, and Start chats and make calls.</span></span>
4.  <span data-ttu-id="eab96-151">Selezionare Crea risorse gt _ pulsante menu.</span><span class="sxs-lookup"><span data-stu-id="eab96-151">Select the menu button > Create Asset.</span></span>
5.  <span data-ttu-id="eab96-152">Tipo di utilizzare la casella di comando team nella casella titolo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="eab96-152">Type Use the Teams command box in the Asset title box.</span></span> 
6.  <span data-ttu-id="eab96-153">Incolla l'utilizzo di SharePoint Team comando casella URL della pagina sono stati copiati nel campo del contenuto delle risorse.</span><span class="sxs-lookup"><span data-stu-id="eab96-153">Paste the SharePoint Use the Teams command box page URL you copied in the Asset content field.</span></span> 
7.  <span data-ttu-id="eab96-p107">Passare nuovamente al gt _ personalizzato gli elenchi di riproduzione di gt _ Home Page del primo giorni con gt _ team utilizzando la finestra di comando team. Nella pagina dovrebbe essere simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="eab96-p107">Now navigate back to the Home Page > Custom Playlists > Your first days with Teams > Use the Teams command box. Your page should look like the following.</span></span> 

![pagina creata](media/clo365createplaylist2.png)

<span data-ttu-id="eab96-157">Elenco di riproduzione con tale contenuto ora sarà disponibile via Internet sono installati / incorporati della Web part apprendimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="eab96-157">Your playlist with this content will now be available anywhere you have installed / embedded the Custom Learning webpart.</span></span> 

#### <a name="things-to-think-about"></a><span data-ttu-id="eab96-158">Aspetti da considerare</span><span class="sxs-lookup"><span data-stu-id="eab96-158">Things to Think About</span></span>

<span data-ttu-id="eab96-p108">Consente di riproduzione personalizzati per aiutare gli utenti finali in un vareity delle attività.  Si dispone di un modulo di richiesta assente?  Un modulo per richiedere apparecchiature hardware?  È possibile programmare le risorse di formazione esistente nell'esperienza.</span><span class="sxs-lookup"><span data-stu-id="eab96-p108">Custom playlists can be used to assist your end users in a vareity of tasks.  Do you have a time off request form?  A form to request hardware equipment?  Any existing training assets can be programmed into the experience.</span></span>  
