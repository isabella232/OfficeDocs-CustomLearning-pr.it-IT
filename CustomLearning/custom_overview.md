---
author: pkrebs
ms.author: pkrebs
title: Panoramica
ms.date: 02/18/2019
description: Panoramica dell'apprendimento personalizzato per Office 365 per gli amministratori
ms.openlocfilehash: 98187038b66252523c74d88dd9bfd0f217591bc5
ms.sourcegitcommit: e10085e60ca3f38029fde229fb093e6bc4a34203
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/25/2019
ms.locfileid: "30087535"
---
# <a name="customize-the-learning-experience"></a><span data-ttu-id="9cd45-103">Personalizzare l'esperienza di apprendimento</span><span class="sxs-lookup"><span data-stu-id="9cd45-103">Customize the Learning Experience</span></span>

<span data-ttu-id="9cd45-p101">Introduzione all'apprendimento personalizzato per Office 365, una nuova soluzione di Microsoft progettata per velocizzare l'utilizzo e l'adozione di Office 365 all'interno di un'organizzazione. Con l'apprendimento personalizzato, è possibile:</span><span class="sxs-lookup"><span data-stu-id="9cd45-p101">Introducing Custom Learning for Office 365, a new solution from Microsoft designed to speed the usage and adoption of Office 365 within an organization. With Custom Learning, you can:</span></span>
- <span data-ttu-id="9cd45-106">Adattare il contenuto di apprendimento e adozione di Office 365 per l'ambiente in uso</span><span class="sxs-lookup"><span data-stu-id="9cd45-106">Tailor Office 365 learning and adoption content for your environment</span></span> 
- <span data-ttu-id="9cd45-107">Nascondere o visualizzare il contenuto in modo che rifletta i servizi o le funzionalità supportate nell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="9cd45-107">Hide or show content to reflect the services or features supported in your organization</span></span> 
- <span data-ttu-id="9cd45-108">Mantenere aggiornati i contenuti e gli utenti con un feed aggiornato dei contenuti di apprendimento di Microsoft</span><span class="sxs-lookup"><span data-stu-id="9cd45-108">Keep your content and users current with an up-to-date feed of learning content from Microsoft</span></span> 
- <span data-ttu-id="9cd45-109">Creare playlist e categorie personalizzate in base alle esigenze dell'utente</span><span class="sxs-lookup"><span data-stu-id="9cd45-109">Build custom playlists and categories crafted specifically for your user's needs</span></span>

![CG-Introducing. png](media/cg-introducing.png)

## <a name="how-does-custom-learning-work"></a><span data-ttu-id="9cd45-111">Come funziona l'apprendimento personalizzato?</span><span class="sxs-lookup"><span data-stu-id="9cd45-111">How does Custom Learning work?</span></span>

<span data-ttu-id="9cd45-112">L'apprendimento personalizzato per Office 365 (apprendimento personalizzato per brevità) è costituito da tre parti:</span><span class="sxs-lookup"><span data-stu-id="9cd45-112">Custom Learning for Office 365 (Custom Learning for short) consists of three parts:</span></span> 
1. <span data-ttu-id="9cd45-113">feed live del contenuto di un catalogo Microsoft online</span><span class="sxs-lookup"><span data-stu-id="9cd45-113">a live feed of content from a Microsoft online catalog</span></span>
2. <span data-ttu-id="9cd45-114">un sito di comunicazione di SharePoint</span><span class="sxs-lookup"><span data-stu-id="9cd45-114">a SharePoint communication site</span></span>
3. <span data-ttu-id="9cd45-115">una Web part di SharePoint</span><span class="sxs-lookup"><span data-stu-id="9cd45-115">a SharePoint web part</span></span> 

![CG-howitworks. png](media/cg-howitworks.png)

## <a name="requirements-and-permissions"></a><span data-ttu-id="9cd45-117">Requisiti e autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="9cd45-117">Requirements and Permissions</span></span>

<span data-ttu-id="9cd45-p102">Prima di iniziare a usare questa guida, assicurarsi che l'apprendimento personalizzato sia stato configurato dall'amministratore del tenant di SharePoint. Se non si è certi che sia stata configurata, rivolgersi all'amministratore tenant di SharePoint per verificare che l'apprendimento personalizzato sia stato installato. Assicurarsi inoltre di ottenere l'URL del sito di SharePoint di apprendimento personalizzato. Se l'amministratore tenant e l'apprendimento personalizzato non sono stati installati, vedere la Guida all'installazione di apprendimento personalizzato per Office 365.</span><span class="sxs-lookup"><span data-stu-id="9cd45-p102">Before getting started with this guide, ensure that Custom Learning has been set up by your  SharePoint tenant administrator. If you’re not sure if it's been set up, contact your SharePoint tenant administrator to verify that Custom Learning has been installed. Also be sure to get the URL of the Custom Learning SharePoint site. If you are the Tenant Administrator and Custom Learning has not been installed, see the Custom Learning for Office 365 Installation Guide.</span></span> 

### <a name="permissions-to-install-custom-learning"></a><span data-ttu-id="9cd45-122">Autorizzazioni per l'installazione di apprendimento personalizzato</span><span class="sxs-lookup"><span data-stu-id="9cd45-122">Permissions to install Custom Learning</span></span>

- <span data-ttu-id="9cd45-123">Amministratore globale di Office 365</span><span class="sxs-lookup"><span data-stu-id="9cd45-123">Office 365 Global Administrator</span></span>
- <span data-ttu-id="9cd45-124">Amministratore di SharePoint</span><span class="sxs-lookup"><span data-stu-id="9cd45-124">SharePoint Administrator</span></span>

### <a name="permissions-to-use-custom-learning-administration-features"></a><span data-ttu-id="9cd45-125">Autorizzazioni per l'utilizzo delle funzionalità di amministrazione dell'apprendimento personalizzate</span><span class="sxs-lookup"><span data-stu-id="9cd45-125">Permissions to use Custom Learning Administration features</span></span>

- <span data-ttu-id="9cd45-126">Autorizzazioni di Office 365 SharePoint Administrator/Owner del sito di SharePoint</span><span class="sxs-lookup"><span data-stu-id="9cd45-126">Office 365 SharePoint Administrator/SharePoint Site Owner Permissions</span></span>
- <span data-ttu-id="9cd45-127">Autorizzazioni dell'amministratore di raccolta siti di SharePoint/proprietario del sito di SharePoint</span><span class="sxs-lookup"><span data-stu-id="9cd45-127">SharePoint Site Collection Administrator/SharePoint Site Owner Permissions</span></span>

### <a name="permissions-to-use-the-custom-learning-site-as-a-user"></a><span data-ttu-id="9cd45-128">Autorizzazioni per l'utilizzo del sito di apprendimento personalizzato come utente</span><span class="sxs-lookup"><span data-stu-id="9cd45-128">Permissions to use the Custom Learning site as a user</span></span>

- <span data-ttu-id="9cd45-129">Autorizzazioni utente di Office 365/autorizzazioni per i visitatori del sito di SharePoint o versioni successive</span><span class="sxs-lookup"><span data-stu-id="9cd45-129">Office 365 user permissions/SharePoint Site Visitor Permissions or higher</span></span>


