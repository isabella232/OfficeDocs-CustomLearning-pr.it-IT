---
author: pkrebs
ms.author: pkrebs
title: Configurazione della web part autonoma
ms.date: 02/10/2019
description: Installazione di Web part manuale per l'apprendimento personalizzato per Office 365
ms.openlocfilehash: 650e6c12ebe8ca7fedc6edc107b5822c48ead99a
ms.sourcegitcommit: b6617bbbaee0784d6216e96052c2469f97cf51e9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2019
ms.locfileid: "30411876"
---
# <a name="stand-alone-web-part-setup"></a><span data-ttu-id="3ccb3-103">Configurazione della web part autonoma</span><span class="sxs-lookup"><span data-stu-id="3ccb3-103">Stand alone web part setup</span></span>

<span data-ttu-id="3ccb3-104">L'apprendimento personalizzato offre una configurazione di Web part autonoma e manuale per le organizzazioni che dispongono già di un sito di comunicazione moderno di SharePoint Online definito dedicato all'allenamento o che desiderano solo configurare la Web part di apprendimento personalizzata in modo autonomo. sito di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-104">Custom Learning offers a manual, stand alone web part setup for those organizations that already have an established SharePoint Online modern communication site dedicated to training, or that just want to set up the Custom Learning web part in their own communication site.</span></span> <span data-ttu-id="3ccb3-105">Si noti che la configurazione manuale richiede un'esperienza di utilizzo di Windows PowerShell e di SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-105">Note that the manual setup requires experience working with Windows PowerShell and the SharePoint Online Management Shell.</span></span> <span data-ttu-id="3ccb3-106">I passaggi per una configurazione manuale della web part di apprendimento personalizzata come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="3ccb3-106">The steps for a manual set up of the Custom Learning Web part as as follows:</span></span>

- <span data-ttu-id="3ccb3-107">Verificare che siano stati soddisfatti tutti i prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-107">Validate that you have met all the prerequisites.</span></span>
- <span data-ttu-id="3ccb3-108">Installare il file customlearning. sppkg nel catalogo delle app tenant di Office 365.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-108">Install the customlearning.sppkg file in your Office 365 Tenant App Catalog.</span></span>
- <span data-ttu-id="3ccb3-109">ProVisioning/identificare un sito di comunicazione moderno che funga da apprendimento personalizzato per il sito Home di Office 365.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-109">Provision/Identify a modern communication site to act as your Custom Learning for Office 365 home site.</span></span>
- <span data-ttu-id="3ccb3-110">Eseguire uno script di PowerShell che configurerà il tenant con gli elementi adatti a cui dipende l'apprendimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-110">Execute a PowerShell script that will configure your tenant with the appropriate artifacts that Custom Learning depends on.</span></span>
- <span data-ttu-id="3ccb3-111">Passare alla pagina del sito CustomLearningAdmin. aspx per caricare la Web part amministratore per inizializzare la configurazione del contenuto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-111">Navigate to the CustomLearningAdmin.aspx site page to load the admin web part to initialize the custom content configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="3ccb3-112">Se si sta cercando un modo semplice e veloce per configurare l'apprendimento personalizzato, vedere [provision Custom Learning](installsitepackage.md).</span><span class="sxs-lookup"><span data-stu-id="3ccb3-112">If you are looking for a fast, easy way to set up Custom Learning, see [Provision Custom Learning](installsitepackage.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3ccb3-113">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="3ccb3-113">Prerequisites</span></span>
<span data-ttu-id="3ccb3-114">Per garantire la corretta configurazione manuale della web part di apprendimento personalizzato, è necessario che vengano soddisfatti i prerequisiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-114">To ensure a successful manual setup of the Custom Learning web part, the follow prerequisites must be met.</span></span> 

- <span data-ttu-id="3ccb3-115">È necessario configurare e configurare il catalogo app a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-115">You must have set up and configured the tenant-wide App Catalog.</span></span> <span data-ttu-id="3ccb3-116">Per ulteriori informazioni, vedere [configurare il tenant di Office 365](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/set-up-your-developer-tenant#create-app-catalog-site) e seguire la sezione creare il sito di catalogo app.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-116">Please see [Set up your Office 365 tenant](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/set-up-your-developer-tenant#create-app-catalog-site) and follow the Create app catalog site section.</span></span> 
- <span data-ttu-id="3ccb3-117">Se è già stato effettuato il provisioning del catalogo delle app a livello di tenant, è necessario accedere a un account che disponga dei diritti di caricamento di un pacchetto per completare il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-117">If your tenant-wide App Catalog has already been provisioned you will need access to an account that has rights to upload a package to it to complete this setup process.</span></span> <span data-ttu-id="3ccb3-118">Si tratta in genere di un account con il ruolo di amministratore di SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-118">Generally this is an account with the SharePoint administrator role.</span></span> 
- <span data-ttu-id="3ccb3-119">Se un account con quel ruolo non funziona, passare all'interfaccia di amministrazione di SharePoint e individuare gli amministratori della raccolta siti per la raccolta siti Catalogo app e accedere come uno degli amministratori della raccolta siti oppure aggiungere l'account amministratore di SharePoint. che non sono riusciti agli amministratori della raccolta siti.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-119">If an account with that role does not work, go to the SharePoint admin center and find the Site Collection Administrators for the app catalog site collection and either log in as one of the Site Collection Administrators, or add the SharePoint administrator account that failed to the Site Collection Administrators.</span></span> 
- <span data-ttu-id="3ccb3-120">Sarà inoltre necessario l'accesso a un account che sia un amministratore tenant di SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-120">You will also need access to an account that is a SharePoint Tenant Admin.</span></span>

## <a name="step-1---get-the-web-part-package-and-setup-script-from-github"></a><span data-ttu-id="3ccb3-121">Passaggio 1-ottenere il pacchetto Web part e lo script di installazione da GitHub</span><span class="sxs-lookup"><span data-stu-id="3ccb3-121">Step 1 - Get the web part package and setup script from GitHub</span></span>
<span data-ttu-id="3ccb3-122">Come parte del processo di installazione, è necessario il pacchetto Web part di apprendimento personalizzato e lo script di installazione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-122">As part of the setup process, you'll need the Custom Learning Web part package and the PowerShell Setup Script.</span></span>

- <span data-ttu-id="3ccb3-123">Andare al [repository di apprendimento GitHub personalizzato](https://github.com/pnp/custom-learning-office-365).</span><span class="sxs-lookup"><span data-stu-id="3ccb3-123">Go the the [Custom Learning GitHub Repository](https://github.com/pnp/custom-learning-office-365).</span></span>
- <span data-ttu-id="3ccb3-124">Fare clic su **download** per salvare il pacchetto della web part e lo script su un'unità locale.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-124">Click **Download** to save the web part package and script to a local drive.</span></span> <span data-ttu-id="3ccb3-125">Si utilizzerà lo script e il pacchetto Web part nei passaggi successivi di questo processo.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-125">You'll be using the script and the web part package in later steps of this process.</span></span>

## <a name="step-2---upload-the-web-part-to-the-tenant-app-catalog"></a><span data-ttu-id="3ccb3-126">Passaggio 2: caricare la Web part nel catalogo app tenant</span><span class="sxs-lookup"><span data-stu-id="3ccb3-126">Step 2 - Upload the web part to the Tenant App Catalog</span></span>
<span data-ttu-id="3ccb3-127">Per configurare l'apprendimento personalizzato per Office 365, caricare il file customlearning. sppkg nel catalogo app a livello di tenant e distribuirlo.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-127">To set up Custom Learning for Office 365, you upload the customlearning.sppkg file to the tenant-wide App Catalog and deploy it.</span></span> <span data-ttu-id="3ccb3-128">Per informazioni dettagliate su come aggiungere un'app al catalogo app, vedere [utilizzare il catalogo app per rendere disponibili le app aziendali personalizzate per l'ambiente di SharePoint Online](https://docs.microsoft.com/en-us/sharepoint/use-app-catalog) .</span><span class="sxs-lookup"><span data-stu-id="3ccb3-128">Please see [Use the App Catalog to make custom business apps available for your SharePoint Online environment](https://docs.microsoft.com/en-us/sharepoint/use-app-catalog) for detailed instructions on how to add an app to the app catalog.</span></span>

## <a name="step-3---provisionidentify-a-modern-communication-site"></a><span data-ttu-id="3ccb3-129">Passaggio 3-proVisioning/identificare un sito di comunicazione moderno</span><span class="sxs-lookup"><span data-stu-id="3ccb3-129">Step 3 - Provision/identify a modern communication site</span></span>
<span data-ttu-id="3ccb3-130">Identificare un sito di comunicazione di SharePoint esistente o provisionare uno nuovo nel tenant di SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-130">Either identify an existing SharePoint communication site or provision a new one in your SharePoint Online tenant.</span></span> <span data-ttu-id="3ccb3-131">Per ulteriori informazioni su come eseguire il provisioning di un sito di comunicazione, vedere [creare un sito di comunicazione in SharePoint Online](https://support.office.com/en-us/article/create-a-communication-site-in-sharepoint-online-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb) e seguire la procedura per creare un sito di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-131">For more information about how to provision a communication site see [Create a communication site in SharePoint Online](https://support.office.com/en-us/article/create-a-communication-site-in-sharepoint-online-7fb44b20-a72f-4d2c-9173-fc8f59ba50eb) and follow the steps to create a communication site.</span></span>

## <a name="step-4---set-permissions-for-the-site"></a><span data-ttu-id="3ccb3-132">Passaggio 4: impostare le autorizzazioni per il sito</span><span class="sxs-lookup"><span data-stu-id="3ccb3-132">Step 4 - Set permissions for the site</span></span>
<span data-ttu-id="3ccb3-133">Verificare che siano impostate le autorizzazioni seguenti per il sito:</span><span class="sxs-lookup"><span data-stu-id="3ccb3-133">Ensure the following permissions are set for the site:</span></span>
- <span data-ttu-id="3ccb3-134">**Amministratore della raccolta siti o parte del gruppo proprietari** -autorizzazioni necessarie per inizializzare l'elemento dell'elenco di CustomConfig che configura l'apprendimento personalizzato per il primo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-134">**Site Collection Administrator or part of the Owners group** - Permissions required to  initialize the CustomConfig list item that sets up custom learning for its first use.</span></span> 
- <span data-ttu-id="3ccb3-135">**Gruppo membri** -permissons necessario per amministraRe l'apprendimento personalizzato, incluso l'occultamento e la visualizzazione di contenuto e l'amministrazione di elenchi di riproduzione personalizzati</span><span class="sxs-lookup"><span data-stu-id="3ccb3-135">**Members group** - permissons required to Administer Custom Learning, including hiding and showing content and administering custom playlists</span></span>
- <span data-ttu-id="3ccb3-136">**Gruppo visitatori** -autorizzazioni necessarie per visualizzare il contenuto del sito.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-136">**Visitors group** - permissions required to view site content.</span></span> 

## <a name="step-5--execute-powershell-configuration-script"></a><span data-ttu-id="3ccb3-137">Passaggio 5-esecuzione dello script di configurazione di PowerShell</span><span class="sxs-lookup"><span data-stu-id="3ccb3-137">Step 5- Execute PowerShell Configuration Script</span></span>
<span data-ttu-id="3ccb3-138">È incluso uno `CustomLearningConfiguration.ps1` script di PowerShell che sarà necessario eseguire per creare tre [Proprietà tenant](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/tenant-properties) utilizzate dalla soluzione.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-138">A PowerShell script `CustomLearningConfiguration.ps1` is included that you will need to execute to create three [tenant properties](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/tenant-properties) that the solution uses.</span></span> <span data-ttu-id="3ccb3-139">Lo script consente inoltre di creare due pagine dell'applicazione di una [singola parte](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/web-parts/single-part-app-pages) nella raccolta pagine del sito per ospitare l'amministratore e le web part dell'utente in una posizione nota.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-139">In addition the script creates two [single part app pages](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/web-parts/single-part-app-pages) in the site pages library to host the admin and user web parts at a known location.</span></span>

### <a name="disabling-telemetry-collection"></a><span data-ttu-id="3ccb3-140">Disabilitazione della raccolta di telemetria</span><span class="sxs-lookup"><span data-stu-id="3ccb3-140">Disabling Telemetry Collection</span></span>
<span data-ttu-id="3ccb3-141">Parte di questa soluzione include la verifica della telemetria di anonimi opt-in, che per impostazione predefinita è impostata su attivato.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-141">Part of this solution includes anonymized telemetry tracking opt in, which by default is set to on.</span></span> <span data-ttu-id="3ccb3-142">Se si sta eseguendo un'installazione manuale e si desidera disattivare la verifica della telemetria, modificare lo `CustomlearningConfiguration.ps1` script per impostare la variabile $optInTelemetry su $false.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-142">If you are performing a manual install and you would like to turn telemetry tracking off, please change the `CustomlearningConfiguration.ps1` script to set the $optInTelemetry variable to $false.</span></span>

<span data-ttu-id="3ccb3-143">Se non si esegue un'installazione manuale e si desidera disattivare la verifica della telemetria, è stato incluso `TelemetryOptOut.ps1` uno script separato che, quando l'esecuzione disattiverà la traccia di telemetria.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-143">If you are not performing a manual install and would like to turn telemetry tracking off, a seperate script `TelemetryOptOut.ps1` has been included that when run will disable telemetry tracking.</span></span>

## <a name="step-6---initialize-web-part-custom-configuration"></a><span data-ttu-id="3ccb3-144">Passaggio 6-inizializzare la configurazione personalizzata della web part</span><span class="sxs-lookup"><span data-stu-id="3ccb3-144">Step 6 - Initialize web part custom configuration</span></span>
<span data-ttu-id="3ccb3-145">Dopo che lo script di PowerShell è stato eseguito correttamente `<YOUR-SITE-COLLECTION-URL>/SitePages/CustomLearningAdmin.aspx`, accedere a.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-145">After the PowerShell script is successfully run, navigate to `<YOUR-SITE-COLLECTION-URL>/SitePages/CustomLearningAdmin.aspx`.</span></span> <span data-ttu-id="3ccb3-146">Questo consente di inizializzare l'elemento di elenco **CustomConfig** che configura l'apprendimento personalizzato per il primo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-146">This initializes the **CustomConfig** list item that sets up Custom Learning for its first use.</span></span>

<span data-ttu-id="3ccb3-147">La configurazione è ora completata.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-147">The configuration is now complete.</span></span> <span data-ttu-id="3ccb3-148">Per ulteriori informazioni su come personalizzare il sito di apprendimento personalizzato e la Web part per l'ambiente in uso, vedere [Customize the Training Experience](custom_overview.md).</span><span class="sxs-lookup"><span data-stu-id="3ccb3-148">To learn more about how to tailor the Custom Learning site and web part for your environment, see [Customize the training experience](custom_overview.md).</span></span>

### <a name="next-steps"></a><span data-ttu-id="3ccb3-149">Operazioni successive</span><span class="sxs-lookup"><span data-stu-id="3ccb3-149">Next Steps</span></span>
- <span data-ttu-id="3ccb3-150">[Personalizzare](custom_overview.md) l'esperienza di formazione per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ccb3-150">[Customize](custom_overview.md) the training experience for your organization.</span></span>
