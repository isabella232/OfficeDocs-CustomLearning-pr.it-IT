# <a name="installing-the-custom-learning-solution-webpart"></a><span data-ttu-id="34551-101">L'installazione personalizzata soluzione Web part di apprendimento</span><span class="sxs-lookup"><span data-stu-id="34551-101">Installing the Custom Learning Solution Webpart</span></span>

## <a name="prerequisites-for-a-tenant-wide-installation"></a><span data-ttu-id="34551-102">Prerequisiti per un'installazione a livello di tenant</span><span class="sxs-lookup"><span data-stu-id="34551-102">Prerequisites for a tenant-wide installation</span></span>

- <span data-ttu-id="34551-p101">Per installare la Web part apprendimento personalizzato per il tenant intero è necessario disporre delle autorizzazioni di amministrazione di Office 365.  Se non si dispone di queste autorizzazioni, è possibile contattare l'amministratore di Office 365 oppure installare la Web part per una singola raccolta di siti.</span><span class="sxs-lookup"><span data-stu-id="34551-p101">To install the Custom Learning webpart for your entire tenant you will need to have Office 365 Administrative permissions.  If you do not have these permissions you can either work with your Office 365 Administrator or install the webpart for an individual site collection.</span></span>
- <span data-ttu-id="34551-105">Utente o dall'amministratore di Office 365 deve già stato installato e configurato un livello di tenant [Catalogo applicazioni](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/set-up-your-developer-tenant) o un [Catalogo App raccolta siti](https://docs.microsoft.com/en-us/sharepoint/dev/general-development/site-collection-app-catalog)per la ricezione della Web part.]</span><span class="sxs-lookup"><span data-stu-id="34551-105">You or your Office 365 Administrator must have setup and configured a tenant-wide [App Catalog](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/set-up-your-developer-tenant) or a [Site Collection App Catalog](https://docs.microsoft.com/en-us/sharepoint/dev/general-development/site-collection-app-catalog)to receive the webpart.]</span></span>
- <span data-ttu-id="34551-p102">È solo supportano SharePoint Online. La web part non è supportato per l'installazione su qualsiasi versione di SharePoint in locale.</span><span class="sxs-lookup"><span data-stu-id="34551-p102">We support SharePoint Online only. The web part is not support for installation on any version of SharePoint on premises.</span></span>

## <a name="add-the-custom-learning-webpart-to-your-tenant"></a><span data-ttu-id="34551-108">Aggiungere la Web part apprendimento personalizzato per il tenant</span><span class="sxs-lookup"><span data-stu-id="34551-108">Add the Custom Learning webpart to your tenant</span></span> 

1. <span data-ttu-id="34551-p103">Scaricare la Web part personalizzata apprendimento e salvarlo nell'unità disco locale.  In questo file è denominato "ms-personalizzato-learning.sppkg".  Non modificare il nome o il suffisso del file.</span><span class="sxs-lookup"><span data-stu-id="34551-p103">Download the Custom Learning webpart and save it to your local drive.  This file is named "ms-custom-learning.sppkg".  Do not change the name or suffix of the file.</span></span> 
2. <span data-ttu-id="34551-112">Passare al [portale di amministrazione di Office 365](https://admin.microsoft.com/AdminPortal/Home#/homepage) per il tenant</span><span class="sxs-lookup"><span data-stu-id="34551-112">Navigate to the [Office 365 Admin portal](https://admin.microsoft.com/AdminPortal/Home#/homepage) for your tenant</span></span>
3. <span data-ttu-id="34551-p104">Riquadro di spostamento sinistro selezionare interfacce di amministrazione, di SharePoint. Verrà aperta in una nuova scheda, nell'interfaccia di amministrazione SharePoint Apps select, catalogo App, App per SharePoint</span><span class="sxs-lookup"><span data-stu-id="34551-p104">From the left navigation select Admin Centers, SharePoint. This will open in a new tab. , In the SharePoint Admin Center select Apps, App Catalog, Apps for SharePoint</span></span> 
4. <span data-ttu-id="34551-115">Selezionare caricare la Web part e selezionare il file "ms-personalizzato-learning.sppkg" è stato scaricato</span><span class="sxs-lookup"><span data-stu-id="34551-115">Select upload the webpart and choose the "ms-custom-learning.sppkg" file you downloaded</span></span>
5. <span data-ttu-id="34551-116">Per l'installazione a livello di tenant selezionare la casella accanto a "Creazione della soluzione disponibile per tutti i risiede all'interno dell'organizzazione".</span><span class="sxs-lookup"><span data-stu-id="34551-116">For this tenant-wide installation check the box next to "Make this solution available to all sits in the organization."</span></span>  

![Distribuire la soluzione](media/trustapp_sm.png)


## <a name="add-the-customer-learning-webpart-to-a-sharepoint-online-page"></a><span data-ttu-id="34551-118">Aggiungere la Web part formazione dei clienti per una pagina di SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="34551-118">Add the Customer Learning webpart to a SharePoint Online Page</span></span>

<span data-ttu-id="34551-p105">Dopo l'installazione di apprendimento personalizzato nel tenant è possibile aggiungere la Web part a una pagina di SharePoint. In questo caso, improvvisamente formazione di Office 365 è disponibile.</span><span class="sxs-lookup"><span data-stu-id="34551-p105">After Custom Learning is installed in your tenant you can add the Web part to a SharePoint page. When you do, suddenly Office 365 training is available to you.</span></span> 

1. <span data-ttu-id="34551-121">Aggiungere la Web part apprendimento personalizzato in un layout di colonna larghezza intera:</span><span class="sxs-lookup"><span data-stu-id="34551-121">Add the Custom Learning webpart in a full width column layout:</span></span>

![Layout di pagina di SharePoint](media/clo365fullcolumnwidth.png)

2. <span data-ttu-id="34551-p106">Nella pagina di SharePoint, selezionare Aggiungi sezione e quindi selezionare larghezza intera colonna.  Verrà visualizzato il prompt dei comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="34551-p106">In the SharePoint page, select Add section and then select full width column.  You'll see the following prompt:</span></span>

![AddWebpart](media/clo365addfullwidthwebpart.png)

3. <span data-ttu-id="34551-p107">Selezionare Microsoft Learning.  Viene visualizzato il seguente:</span><span class="sxs-lookup"><span data-stu-id="34551-p107">Select Microsoft Learning.  You should now see the following:</span></span> 

![Apprendimento di Web part personalizzate](media/clo365addwebpart.png)

 <span data-ttu-id="34551-129">È possibile ora fare clic su sezioni per esplorare il contenuto predefinito incluso nella soluzione.</span><span class="sxs-lookup"><span data-stu-id="34551-129">You can now click on the tiles to explore the default content included in the solution.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="34551-130">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="34551-130">Next Steps</span></span>
- <span data-ttu-id="34551-131">Esplorare il [contenuto predefinito](webpartcontent.md) incluso nella Web part.</span><span class="sxs-lookup"><span data-stu-id="34551-131">Explore the [default content](webpartcontent.md) included in the webpart.</span></span>
- <span data-ttu-id="34551-132">[Personalizzare](customization.md) l'esperienza di formazione per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="34551-132">[Customize](customization.md) the training experience for your organization.</span></span>
- <span data-ttu-id="34551-133">[Unità adozione](driveadoption.md) della soluzione di formazione.</span><span class="sxs-lookup"><span data-stu-id="34551-133">[Drive adoption](driveadoption.md) of your training solution.</span></span>

