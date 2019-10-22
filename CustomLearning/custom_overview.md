---
author: pkrebs
ms.author: pkrebs
title: Panoramica
ms.date: 02/18/2019
description: Panoramica dei percorsi di apprendimento di Microsoft 365
ms.openlocfilehash: 74fac090177ad8009155e21a977b05ee2b742b3b
ms.sourcegitcommit: f5a7079d56598c14aef2f4b886c025a59ba89276
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "34247851"
---
# <a name="customize-the-learning-experience"></a><span data-ttu-id="e327f-103">Personalizzare l'esperienza di apprendimento</span><span class="sxs-lookup"><span data-stu-id="e327f-103">Customize the learning experience</span></span>

<span data-ttu-id="e327f-104">Introduzione a Microsoft 365 Learning pathways, una nuova soluzione di Microsoft progettata per velocizzare l'utilizzo e l'adozione di Office 365 all'interno di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="e327f-104">Introducing Microsoft 365 learning pathways, a new solution from Microsoft designed to speed the usage and adoption of Office 365 within an organization.</span></span> <span data-ttu-id="e327f-105">Con Learning pathwyas, è possibile:</span><span class="sxs-lookup"><span data-stu-id="e327f-105">With learning pathwyas, you can:</span></span>
- <span data-ttu-id="e327f-106">Adattare il contenuto Microsoft 365 Learning and adoption for your environment</span><span class="sxs-lookup"><span data-stu-id="e327f-106">Tailor Microsoft 365 learning and adoption content for your environment</span></span> 
- <span data-ttu-id="e327f-107">Nascondere o visualizzare il contenuto in modo che rifletta i servizi o le funzionalità supportate nell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="e327f-107">Hide or show content to reflect the services or features supported in your organization</span></span> 
- <span data-ttu-id="e327f-108">Mantenere aggiornati i contenuti e gli utenti con un feed aggiornato dei contenuti di apprendimento di Microsoft</span><span class="sxs-lookup"><span data-stu-id="e327f-108">Keep your content and users current with an up-to-date feed of learning content from Microsoft</span></span> 
- <span data-ttu-id="e327f-109">Creare playlist e categorie personalizzate in base alle esigenze dell'utente</span><span class="sxs-lookup"><span data-stu-id="e327f-109">Build custom playlists and categories crafted specifically for your user's needs</span></span>

![CG-Introducing. png](media/cg-introducing.png)

## <a name="how-does-learning-pathways-work"></a><span data-ttu-id="e327f-111">Come funziona il percorso di apprendimento?</span><span class="sxs-lookup"><span data-stu-id="e327f-111">How does learning pathways work?</span></span>

<span data-ttu-id="e327f-112">i percorsi di apprendimento per Office 365 (percorsi di apprendimento in breve) sono costituiti da tre parti:</span><span class="sxs-lookup"><span data-stu-id="e327f-112">learning pathways for Office 365 (learning pathways for short) consists of three parts:</span></span> 
1. <span data-ttu-id="e327f-113">feed live del contenuto di un catalogo Microsoft online</span><span class="sxs-lookup"><span data-stu-id="e327f-113">a live feed of content from a Microsoft online catalog</span></span>
2. <span data-ttu-id="e327f-114">un sito di comunicazione di SharePoint</span><span class="sxs-lookup"><span data-stu-id="e327f-114">a SharePoint communication site</span></span>
3. <span data-ttu-id="e327f-115">una Web part di SharePoint</span><span class="sxs-lookup"><span data-stu-id="e327f-115">a SharePoint web part</span></span> 

![CG-howitworks. png](media/cg-howitworks.png)

## <a name="requirements-and-permissions"></a><span data-ttu-id="e327f-117">Requisiti e autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="e327f-117">Requirements and Permissions</span></span>

<span data-ttu-id="e327f-118">Prima di iniziare a usare questa guida, assicurarsi che i percorsi di apprendimento siano stati configurati dall'amministratore del tenant di SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e327f-118">Before getting started with this guide, ensure that learning pathways has been set up by your SharePoint Tenant Administrator.</span></span> <span data-ttu-id="e327f-119">Se non si è certi che sia stato configurato, rivolgersi all'amministratore tenant di SharePoint per verificare che i percorsi di apprendimento siano stati sottoposti a provisioning.</span><span class="sxs-lookup"><span data-stu-id="e327f-119">If you’re not sure if it's been set up, contact your SharePoint tenant administrator to verify that learning pathways has been provisioned.</span></span> <span data-ttu-id="e327f-120">Assicurarsi inoltre di ottenere l'URL del sito di SharePoint percorsi di apprendimento.</span><span class="sxs-lookup"><span data-stu-id="e327f-120">Also be sure to get the URL of the learning pathways SharePoint site.</span></span> <span data-ttu-id="e327f-121">Se si è l'amministratore tenant e non è stato effettuato il provisioning dei percorsi di apprendimento, vedere [provision Learning pathways](custom_provision.md).</span><span class="sxs-lookup"><span data-stu-id="e327f-121">If you are the Tenant Administrator and learning pathways has not been provisioned, see [Provision learning pathways](custom_provision.md).</span></span> 

### <a name="permissions-to-provision-learning-pathways"></a><span data-ttu-id="e327f-122">Autorizzazioni per il provisioning di percorsi di apprendimento</span><span class="sxs-lookup"><span data-stu-id="e327f-122">Permissions to provision learning pathways</span></span>

- <span data-ttu-id="e327f-123">Amministratore tenant, noto anche come amministratore globale di Office 365</span><span class="sxs-lookup"><span data-stu-id="e327f-123">Tenant Administrator, also known as Office 365 Global Administrator</span></span>
- <span data-ttu-id="e327f-124">Amministratore di raccolta siti di SharePoint con autorizzazioni proprietario nel sito</span><span class="sxs-lookup"><span data-stu-id="e327f-124">SharePoint Site Collection Administrator with Owner permissions on the site</span></span>

### <a name="permissions-to-use-learning-pathways-administration-features"></a><span data-ttu-id="e327f-125">Autorizzazioni per l'utilizzo delle caratteristiche di amministrazione di percorsi di apprendimento</span><span class="sxs-lookup"><span data-stu-id="e327f-125">Permissions to use learning pathways Administration features</span></span>

- <span data-ttu-id="e327f-126">Amministratori delle raccolte siti</span><span class="sxs-lookup"><span data-stu-id="e327f-126">Site Collection Administrator</span></span>
- <span data-ttu-id="e327f-127">Autorizzazioni proprietario o membro di SharePoint</span><span class="sxs-lookup"><span data-stu-id="e327f-127">SharePoint Owner or Member permissions</span></span>

### <a name="permissions-to-use-the-learning-pathways-site-as-a-user"></a><span data-ttu-id="e327f-128">Autorizzazioni per l'utilizzo del sito percorsi di apprendimento come utente</span><span class="sxs-lookup"><span data-stu-id="e327f-128">Permissions to use the learning pathways site as a user</span></span>

- <span data-ttu-id="e327f-129">Autorizzazioni utente di Office 365/autorizzazioni per i visitatori del sito di SharePoint o versioni successive</span><span class="sxs-lookup"><span data-stu-id="e327f-129">Office 365 user permissions/SharePoint Site Visitor permissions or higher</span></span>

## <a name="get-started-with-customization"></a><span data-ttu-id="e327f-130">Introduzione alla personalizzazione</span><span class="sxs-lookup"><span data-stu-id="e327f-130">Get started with customization</span></span>
<span data-ttu-id="e327f-131">Dopo aver ottenuto le autorizzazioni necessarie per personalizzare il sito e la Web part, è ora di iniziare a utilizzare il processo di personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="e327f-131">Once you've ensured you have the necessary permissions to customize the site and web part, it's time to get started with the customization process.</span></span> 

- <span data-ttu-id="e327f-132">Per iniziare, vedere [andare al sito percorsi di apprendimento](custom_goto.md).</span><span class="sxs-lookup"><span data-stu-id="e327f-132">To get started, see [Go to the learning pathways site](custom_goto.md).</span></span>