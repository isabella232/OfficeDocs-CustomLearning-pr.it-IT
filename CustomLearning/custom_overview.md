---
author: pkrebs
ms.author: pkrebs
title: Panoramica
ms.date: 02/18/2019
description: Panoramica dell'apprendimento personalizzato per Office 365 per gli amministratori
ms.openlocfilehash: 6aee3a93a5109b37e43a7118bd98ca31e8b9ac1f
ms.sourcegitcommit: 775d6807291ab263eea5ec649d9aaf1933fb41ca
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "32055638"
---
# <a name="customize-the-learning-experience"></a><span data-ttu-id="520d9-103">Personalizzare l'esperienza di apprendimento</span><span class="sxs-lookup"><span data-stu-id="520d9-103">Customize the Learning Experience</span></span>

<span data-ttu-id="520d9-104">Introduzione all'apprendimento personalizzato per Office 365, una nuova soluzione di Microsoft progettata per velocizzare l'utilizzo e l'adozione di Office 365 all'interno di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="520d9-104">Introducing Custom Learning for Office 365, a new solution from Microsoft designed to speed the usage and adoption of Office 365 within an organization.</span></span> <span data-ttu-id="520d9-105">Con l'apprendimento personalizzato, è possibile:</span><span class="sxs-lookup"><span data-stu-id="520d9-105">With Custom Learning, you can:</span></span>
- <span data-ttu-id="520d9-106">Adattare il contenuto di apprendimento e adozione di Office 365 per l'ambiente in uso</span><span class="sxs-lookup"><span data-stu-id="520d9-106">Tailor Office 365 learning and adoption content for your environment</span></span> 
- <span data-ttu-id="520d9-107">Nascondere o visualizzare il contenuto in modo che rifletta i servizi o le funzionalità supportate nell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="520d9-107">Hide or show content to reflect the services or features supported in your organization</span></span> 
- <span data-ttu-id="520d9-108">Mantenere aggiornati i contenuti e gli utenti con un feed aggiornato dei contenuti di apprendimento di Microsoft</span><span class="sxs-lookup"><span data-stu-id="520d9-108">Keep your content and users current with an up-to-date feed of learning content from Microsoft</span></span> 
- <span data-ttu-id="520d9-109">Creare playlist e categorie personalizzate in base alle esigenze dell'utente</span><span class="sxs-lookup"><span data-stu-id="520d9-109">Build custom playlists and categories crafted specifically for your user's needs</span></span>

![CG-Introducing. png](media/cg-introducing.png)

## <a name="how-does-custom-learning-work"></a><span data-ttu-id="520d9-111">Come funziona l'apprendimento personalizzato?</span><span class="sxs-lookup"><span data-stu-id="520d9-111">How does Custom Learning work?</span></span>

<span data-ttu-id="520d9-112">L'apprendimento personalizzato per Office 365 (apprendimento personalizzato per brevità) è costituito da tre parti:</span><span class="sxs-lookup"><span data-stu-id="520d9-112">Custom Learning for Office 365 (Custom Learning for short) consists of three parts:</span></span> 
1. <span data-ttu-id="520d9-113">feed live del contenuto di un catalogo Microsoft online</span><span class="sxs-lookup"><span data-stu-id="520d9-113">a live feed of content from a Microsoft online catalog</span></span>
2. <span data-ttu-id="520d9-114">un sito di comunicazione di SharePoint</span><span class="sxs-lookup"><span data-stu-id="520d9-114">a SharePoint communication site</span></span>
3. <span data-ttu-id="520d9-115">una Web part di SharePoint</span><span class="sxs-lookup"><span data-stu-id="520d9-115">a SharePoint web part</span></span> 

![CG-howitworks. png](media/cg-howitworks.png)

## <a name="requirements-and-permissions"></a><span data-ttu-id="520d9-117">Requisiti e autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="520d9-117">Requirements and Permissions</span></span>

<span data-ttu-id="520d9-118">Prima di iniziare a usare questa guida, assicurarsi che l'apprendimento personalizzato sia stato configurato dall'amministratore del tenant di SharePoint.</span><span class="sxs-lookup"><span data-stu-id="520d9-118">Before getting started with this guide, ensure that Custom Learning has been set up by your SharePoint Tenant Administrator.</span></span> <span data-ttu-id="520d9-119">Se non si è certi che sia stata configurata, contattare l'amministratore tenant di SharePoint per verificare che sia stato effettuato il provisioning dell'apprendimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="520d9-119">If you’re not sure if it's been set up, contact your SharePoint tenant administrator to verify that Custom Learning has been provisioned.</span></span> <span data-ttu-id="520d9-120">Assicurarsi inoltre di ottenere l'URL del sito di SharePoint di apprendimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="520d9-120">Also be sure to get the URL of the Custom Learning SharePoint site.</span></span> <span data-ttu-id="520d9-121">Se si è l'amministratore tenant e non è stato effettuato il provisioning dell'apprendimento personalizzato, vedere [provision Custom Learning](custom_provision.md).</span><span class="sxs-lookup"><span data-stu-id="520d9-121">If you are the Tenant Administrator and Custom Learning has not been provisioned, see [Provision Custom Learning](custom_provision.md).</span></span> 

### <a name="permissions-to-provision-custom-learning"></a><span data-ttu-id="520d9-122">Autorizzazioni per il provisioning dell'apprendimento personalizzato</span><span class="sxs-lookup"><span data-stu-id="520d9-122">Permissions to provision Custom Learning</span></span>

- <span data-ttu-id="520d9-123">Amministratore tenant, noto anche come amministratore globale di Office 365</span><span class="sxs-lookup"><span data-stu-id="520d9-123">Tenant Administrator, also known as Office 365 Global Administrator</span></span>
- <span data-ttu-id="520d9-124">Amministratore di raccolta siti di SharePoint con autorizzazioni proprietario nel sito</span><span class="sxs-lookup"><span data-stu-id="520d9-124">SharePoint Site Collection Administrator with Owner permissions on the site</span></span>

### <a name="permissions-to-use-custom-learning-administration-features"></a><span data-ttu-id="520d9-125">Autorizzazioni per l'utilizzo delle funzionalità di amministrazione dell'apprendimento personalizzate</span><span class="sxs-lookup"><span data-stu-id="520d9-125">Permissions to use Custom Learning Administration features</span></span>

- <span data-ttu-id="520d9-126">Amministratori delle raccolte siti</span><span class="sxs-lookup"><span data-stu-id="520d9-126">Site Collection Administrator</span></span>
- <span data-ttu-id="520d9-127">Autorizzazioni proprietario o membro di SharePoint</span><span class="sxs-lookup"><span data-stu-id="520d9-127">SharePoint Owner or Member permissions</span></span>

### <a name="permissions-to-use-the-custom-learning-site-as-a-user"></a><span data-ttu-id="520d9-128">Autorizzazioni per l'utilizzo del sito di apprendimento personalizzato come utente</span><span class="sxs-lookup"><span data-stu-id="520d9-128">Permissions to use the Custom Learning site as a user</span></span>

- <span data-ttu-id="520d9-129">Autorizzazioni utente di Office 365/autorizzazioni per i visitatori del sito di SharePoint o versioni successive</span><span class="sxs-lookup"><span data-stu-id="520d9-129">Office 365 user permissions/SharePoint Site Visitor permissions or higher</span></span>

## <a name="get-started-with-customization"></a><span data-ttu-id="520d9-130">Introduzione alla personalizzazione</span><span class="sxs-lookup"><span data-stu-id="520d9-130">Get started with customization</span></span>
<span data-ttu-id="520d9-131">Dopo aver ottenuto le autorizzazioni necessarie per personalizzare il sito e la Web part, è ora di iniziare a utilizzare il processo di personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="520d9-131">Once you've ensured you have the necessary permissions to customize the site and web part, it's time to get started with the customization process.</span></span> 

- <span data-ttu-id="520d9-132">Per iniziare, vedere [andare al sito di apprendimento personalizzato](custom_goto.md).</span><span class="sxs-lookup"><span data-stu-id="520d9-132">To get started, see [Go to the Custom Learning Site](custom_goto.md).</span></span>