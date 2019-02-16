---
author: pkrebs
ms.author: pkrebs
title: Panoramica
ms.date: 02/15/2019
description: Panoramica dell'apprendimento personalizzato per Office 365 per gli amministratori
ms.openlocfilehash: c4b9679ae5a7158306bfd53e345f8e892ab206bc
ms.sourcegitcommit: afb5502604d271f49f6d1133db9dfc499f710eec
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/15/2019
ms.locfileid: "30064986"
---
# <a name="overview-of-custom-learning"></a><span data-ttu-id="80082-103">Panoramica sull'apprendimento personalizzato</span><span class="sxs-lookup"><span data-stu-id="80082-103">Overview of Custom Learning</span></span>
<span data-ttu-id="80082-p101">Introduzione all'apprendimento personalizzato per Office 365, una nuova soluzione di Microsoft progettata per velocizzare l'utilizzo e l'adozione di Office 365 all'interno di un'organizzazione. Con l'apprendimento personalizzato, è possibile:</span><span class="sxs-lookup"><span data-stu-id="80082-p101">Introducing Custom Learning for Office 365, a new solution from Microsoft designed to speed the usage and adoption of Office 365 within an organization. With Custom Learning, you can:</span></span>

- <span data-ttu-id="80082-p102">Personalizzare l'apprendimento personalizzato per Office 365 nell'ambiente in uso. Modificare le pagine del sito con il marchio e il logo, gli eventi di formazione e le informazioni di supporto. Nascondere e visualizzare il contenuto per servizi o funzionalità non supportati nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="80082-p102">Tailor Custom Learning for Office 365 to your environment. Modify site pages with your brand and logo, training events, and support info. Hide and show content for services or features that are not supported in your organization.</span></span> 
- <span data-ttu-id="80082-109">Consenti a Microsoft di mantenere aggiornati i contenuti e gli utenti – l'apprendimento personalizzato fornisce un feed dinamico di contenuti di apprendimento che Microsoft mantiene aggiornati.</span><span class="sxs-lookup"><span data-stu-id="80082-109">Let Microsoft keep your content and users up-to-date – Custom Learning provides a dynamic feed of learning content that Microsoft keeps up-to-date.</span></span> 
- <span data-ttu-id="80082-110">Categorie di compilazione e playlist personalizzate che riflettono i criteri, le procedure e la cultura dell'organizzazione, consentendo agli utenti di creare competenze con contenuti didattici appositamente progettati per le proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="80082-110">Build categories and custom playlists reflecting your organization’s policies, procedures, and culture, enabling users to build skills with learning content crafted specifically to their needs.</span></span>

![cg_introducing. png](media/cg_introducing.png)

## <a name="how-does-custom-learning-word"></a><span data-ttu-id="80082-112">Come funziona l'apprendimento personalizzato?</span><span class="sxs-lookup"><span data-stu-id="80082-112">How does Custom Learning word?</span></span>
<span data-ttu-id="80082-113">L'apprendimento personalizzato per Office 365 (apprendimento personalizzato per brevità) è costituito da tre parti:</span><span class="sxs-lookup"><span data-stu-id="80082-113">Custom Learning for Office 365 (Custom Learning for short) consists of three parts:</span></span> 
- <span data-ttu-id="80082-114">un sito di comunicazione di SharePoint</span><span class="sxs-lookup"><span data-stu-id="80082-114">a SharePoint communication site</span></span>
- <span data-ttu-id="80082-115">una Web part di SharePoint</span><span class="sxs-lookup"><span data-stu-id="80082-115">a SharePoint web part</span></span>
- <span data-ttu-id="80082-116">feed live del contenuto di un catalogo Microsoft online</span><span class="sxs-lookup"><span data-stu-id="80082-116">a live feed of content from a Microsoft online catalog</span></span>

![cg_howitworks. png](media/cg_howitworks.png)

## <a name="requirements-and-permissions"></a><span data-ttu-id="80082-118">Requisiti e autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="80082-118">Requirements and Permissions</span></span>
<span data-ttu-id="80082-p103">L'apprendimento personalizzato per Office 365 deve essere installato dall'amministratore tenant dell'organizzazione, ovvero da un utente che dispone dell'autorizzazione di amministratore tenant. Prima di iniziare a usare queste procedure di personalizzazione descritte in questa guida, assicurarsi che l'apprendimento personalizzato sia stato configurato da un amministratore tenant di SharePoint. Se non si è certi, contattare l'amministratore tenant di SharePoint per verificare che l'apprendimento personalizzato sia stato installato. Assicurarsi inoltre di ottenere l'URL del sito di SharePoint di apprendimento personalizzato. Se l'amministratore tenant e l'apprendimento personalizzato non sono stati installati, vedere la Guida all'installazione di apprendimento personalizzato per Office 365.</span><span class="sxs-lookup"><span data-stu-id="80082-p103">Custom Learning for Office 365 must be installed by your organization’s tenant administrator - someone who has Tenant Administrator permission. Before getting started with this customization procedures covered in this guide, ensure that Custom Learning has been set up by a SharePoint tenant administrator. If you’re not sure, contact your SharePoint tenant administrator to verify that Custom Learning has been installed. Also be sure to get the URL of the Custom Learning SharePoint site. If you are the Tenant Administrator and Custom Learning has not been installed, see the Custom Learning for Office 365 Installation Guide.</span></span> 

### <a name="permissions-required-for-custom-learning"></a><span data-ttu-id="80082-124">Autorizzazioni necessarie per l'apprendimento personalizzato</span><span class="sxs-lookup"><span data-stu-id="80082-124">Permissions required for Custom Learning</span></span> 
<span data-ttu-id="80082-125">Di seguito vengono riPartite le autorizzazioni necessarie per l'installazione, la personalizzazione e l'utilizzo dell'apprendimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="80082-125">Here’s a breakdown of the permissions required for installing, customizing, and using Custom Learning.</span></span> 

<span data-ttu-id="80082-126">**Autorizzazioni per l'installazione di apprendimento personalizzato**</span><span class="sxs-lookup"><span data-stu-id="80082-126">**Permissions to install Custom Learning**</span></span>
- <span data-ttu-id="80082-127">Amministratore globale di Office 365</span><span class="sxs-lookup"><span data-stu-id="80082-127">Office 365 Global Administrator</span></span>
- <span data-ttu-id="80082-128">Amministratore di SharePoint</span><span class="sxs-lookup"><span data-stu-id="80082-128">SharePoint Administrator</span></span>

<span data-ttu-id="80082-129">**Autorizzazioni per l'utilizzo delle funzionalità di amministrazione dell'apprendimento personalizzate**</span><span class="sxs-lookup"><span data-stu-id="80082-129">**Permissions to use Custom Learning Administration features**</span></span>
- <span data-ttu-id="80082-130">Autorizzazioni di Office 365 SharePoint Administrator/Owner del sito di SharePoint</span><span class="sxs-lookup"><span data-stu-id="80082-130">Office 365 SharePoint Administrator/SharePoint Site Owner Permissions</span></span>
- <span data-ttu-id="80082-131">Autorizzazioni dell'amministratore di raccolta siti di SharePoint/proprietario del sito di SharePoint</span><span class="sxs-lookup"><span data-stu-id="80082-131">SharePoint Site Collection Administrator/SharePoint Site Owner Permissions</span></span>

<span data-ttu-id="80082-132">**Per utilizzare il sito di apprendimento personalizzato come utente**</span><span class="sxs-lookup"><span data-stu-id="80082-132">**To use the Custom Learning site as a user**</span></span>
- <span data-ttu-id="80082-133">Autorizzazioni utente di Office 365/autorizzazioni per i visitatori del sito di SharePoint o versioni successive</span><span class="sxs-lookup"><span data-stu-id="80082-133">Office 365 user permissions/SharePoint Site Visitor Permissions or higher</span></span>
- <span data-ttu-id="80082-134">Se non si è certi che siano state concesse le autorizzazioni necessarie, contattare l'amministratore del tenant di SharePoint.</span><span class="sxs-lookup"><span data-stu-id="80082-134">If you’re not sure if you’ve been granted the necessary permissions, contact your SharePoint Tenant Administrator.</span></span>

### <a name="next-steps"></a><span data-ttu-id="80082-135">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="80082-135">Next Steps</span></span>

- [<span data-ttu-id="80082-136">Personalizzare e condividere playlist</span><span class="sxs-lookup"><span data-stu-id="80082-136">Customize and Share Playlists</span></span>](customplaylist.md)
- [<span data-ttu-id="80082-137">Adozione di unità</span><span class="sxs-lookup"><span data-stu-id="80082-137">Drive Adoption</span></span>](driveadoption.md) 