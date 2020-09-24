---
author: pkrebs
ms.author: pkrebs
title: Personalizzare i percorsi di apprendimento
ms.date: 02/18/2019
description: Personalizzare i percorsi di apprendimento
ms.service: sharepoint online
ms.openlocfilehash: 56027e48917cbdeeb2187f87497f3281fff3c23a
ms.sourcegitcommit: ee4aebf60893887ae95a1294a9ad8975539ea762
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/23/2020
ms.locfileid: "48234228"
---
# <a name="customize-learning-pathways"></a><span data-ttu-id="8b7a8-103">Personalizzare i percorsi di apprendimento</span><span class="sxs-lookup"><span data-stu-id="8b7a8-103">Customize learning pathways</span></span>

<span data-ttu-id="8b7a8-104">I percorsi di apprendimento Microsoft 365 offrono vari modi per personalizzare i contenuti dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="8b7a8-104">Microsoft 365 learning pathways provides a variety of ways that you can customize content for your organization.</span></span> <span data-ttu-id="8b7a8-105">Ad esempio, è possibile:</span><span class="sxs-lookup"><span data-stu-id="8b7a8-105">For example, you can:</span></span>  
- <span data-ttu-id="8b7a8-106">Modificare i percorsi di apprendimento sito di SharePoint-modificare il nome del sito, il logo e gli stessi.</span><span class="sxs-lookup"><span data-stu-id="8b7a8-106">Modify the learning pathways SharePoint site - Change the site name, logo, and them.</span></span> <span data-ttu-id="8b7a8-107">Modificare la pagina Chiedi informazioni e ottenere assistenza per creare un centro assistenza personalizzato.</span><span class="sxs-lookup"><span data-stu-id="8b7a8-107">Modify the Ask Questions and Get Help page to create your own Help Center.</span></span> 
- <span data-ttu-id="8b7a8-108">Nascondere o visualizzare il contenuto in modo che rifletta i servizi o le funzionalità supportate nell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="8b7a8-108">Hide or show content to reflect the services or features supported in your organization</span></span> 
- <span data-ttu-id="8b7a8-109">Creare playlist e sottocategorie personalizzate in base alle esigenze dell'utente</span><span class="sxs-lookup"><span data-stu-id="8b7a8-109">Build custom playlists and subcategories crafted specifically for your user's needs</span></span>
- <span data-ttu-id="8b7a8-110">Creare pagine di destinazione con contenuto filtrato per supportare i risultati aziendali, ad esempio la guida dell'adozione di Microsoft teams, Outlook Mobile o la collaborazione con Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8b7a8-110">Build landing pages with content filtered to support business outcomes, such as driving the adoption of Microsoft Teams, Outlook mobile, or working more collaboratively with Microsoft 365.</span></span>

![cg-introducing.png](media/cg-introducing.png)

## <a name="requirements-and-permissions"></a><span data-ttu-id="8b7a8-112">Requisiti e autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="8b7a8-112">Requirements and Permissions</span></span>

<span data-ttu-id="8b7a8-113">Prima di iniziare a usare le istruzioni per la personalizzazione dei percorsi di apprendimento, assicurarsi che i percorsi di apprendimento siano stati configurati dall'amministratore tenant di SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8b7a8-113">Before getting started with the Customize learning pathways guidance, ensure that learning pathways has been set up by your SharePoint Tenant Administrator.</span></span> <span data-ttu-id="8b7a8-114">Se non si è certi che sia stato configurato, rivolgersi all'amministratore tenant di SharePoint per verificare che i percorsi di apprendimento siano stati sottoposti a provisioning.</span><span class="sxs-lookup"><span data-stu-id="8b7a8-114">If you’re not sure if it's been set up, contact your SharePoint tenant administrator to verify that learning pathways has been provisioned.</span></span> <span data-ttu-id="8b7a8-115">Assicurarsi inoltre di ottenere l'URL del sito di SharePoint percorsi di apprendimento.</span><span class="sxs-lookup"><span data-stu-id="8b7a8-115">Also be sure to get the URL of the learning pathways SharePoint site.</span></span> <span data-ttu-id="8b7a8-116">Se si è l'amministratore tenant e non è stato effettuato il provisioning dei percorsi di apprendimento, vedere [provision Learning pathways](custom_provision.md).</span><span class="sxs-lookup"><span data-stu-id="8b7a8-116">If you are the Tenant Administrator and learning pathways has not been provisioned, see [Provision learning pathways](custom_provision.md).</span></span> 

### <a name="permissions-to-provision-learning-pathways"></a><span data-ttu-id="8b7a8-117">Autorizzazioni per il provisioning di percorsi di apprendimento</span><span class="sxs-lookup"><span data-stu-id="8b7a8-117">Permissions to provision learning pathways</span></span>

- <span data-ttu-id="8b7a8-118">Amministratore tenant, noto anche come amministratore globale di Office 365</span><span class="sxs-lookup"><span data-stu-id="8b7a8-118">Tenant Administrator, also known as Office 365 Global Administrator</span></span>
- <span data-ttu-id="8b7a8-119">L’amministratore della raccolta siti di SharePoint con autorizzazioni di proprietario nel sito</span><span class="sxs-lookup"><span data-stu-id="8b7a8-119">SharePoint Site Collection Administrator with Owner permissions on the site</span></span>

### <a name="permissions-to-use-learning-pathways-administration-features"></a><span data-ttu-id="8b7a8-120">Autorizzazioni per l'utilizzo delle caratteristiche di amministrazione di percorsi di apprendimento</span><span class="sxs-lookup"><span data-stu-id="8b7a8-120">Permissions to use learning pathways Administration features</span></span>

- <span data-ttu-id="8b7a8-121">Amministratori delle raccolte siti</span><span class="sxs-lookup"><span data-stu-id="8b7a8-121">Site Collection Administrator</span></span>
- <span data-ttu-id="8b7a8-122">Autorizzazioni proprietario o membro di SharePoint</span><span class="sxs-lookup"><span data-stu-id="8b7a8-122">SharePoint Owner or Member permissions</span></span>

### <a name="permissions-to-use-the-learning-pathways-site-as-a-user"></a><span data-ttu-id="8b7a8-123">Autorizzazioni per l'utilizzo del sito percorsi di apprendimento come utente</span><span class="sxs-lookup"><span data-stu-id="8b7a8-123">Permissions to use the learning pathways site as a user</span></span>

- <span data-ttu-id="8b7a8-124">Autorizzazioni utente di Office 365/autorizzazioni di visitatore del sito di SharePoint o superiore</span><span class="sxs-lookup"><span data-stu-id="8b7a8-124">Office 365 user permissions/SharePoint Site Visitor permissions or higher</span></span>

## <a name="get-started-with-customization"></a><span data-ttu-id="8b7a8-125">Introduzione alla personalizzazione</span><span class="sxs-lookup"><span data-stu-id="8b7a8-125">Get started with customization</span></span>
<span data-ttu-id="8b7a8-126">Dopo aver ottenuto le autorizzazioni necessarie per personalizzare il sito e la Web part, è ora di iniziare a utilizzare il processo di personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="8b7a8-126">Once you've ensured you have the necessary permissions to customize the site and web part, it's time to get started with the customization process.</span></span> 

- <span data-ttu-id="8b7a8-127">Per iniziare, vedere [andare al sito percorsi di apprendimento](custom_goto.md).</span><span class="sxs-lookup"><span data-stu-id="8b7a8-127">To get started, see [Go to the learning pathways site](custom_goto.md).</span></span>