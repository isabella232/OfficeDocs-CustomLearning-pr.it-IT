---
author: pkrebs
ms.author: pkrebs
title: Personalizzare i percorsi di apprendimento
ms.date: 02/18/2019
manager: bpardi
audience: admin
ms.topic: article
description: Personalizzare i percorsi di apprendimento
ms.service: sharepoint-online
ms.openlocfilehash: a5087096ec3bd7c1194aab9dd089276fc196a736
ms.sourcegitcommit: 97e175e5ff5b6a9e0274d5ec9b39fdf7e18eb387
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/25/2021
ms.locfileid: "51999502"
---
# <a name="customize-learning-pathways"></a><span data-ttu-id="fc4f6-103">Personalizzare i percorsi di apprendimento</span><span class="sxs-lookup"><span data-stu-id="fc4f6-103">Customize learning pathways</span></span>

<span data-ttu-id="fc4f6-104">I percorsi di apprendimento di Microsoft 365 forniscono diversi modi per personalizzare il contenuto per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="fc4f6-104">Microsoft 365 learning pathways provides a variety of ways that you can customize content for your organization.</span></span> <span data-ttu-id="fc4f6-105">Ad esempio, è possibile:</span><span class="sxs-lookup"><span data-stu-id="fc4f6-105">For example, you can:</span></span>  
- <span data-ttu-id="fc4f6-106">Modificare i percorsi di apprendimento Sito di SharePoint- Modificare il nome del sito, il logo e i percorsi.</span><span class="sxs-lookup"><span data-stu-id="fc4f6-106">Modify the learning pathways SharePoint site - Change the site name, logo, and them.</span></span> <span data-ttu-id="fc4f6-107">Modificare la pagina Domande e assistenza per creare un Centro assistenza personalizzato.</span><span class="sxs-lookup"><span data-stu-id="fc4f6-107">Modify the Ask Questions and Get Help page to create your own Help Center.</span></span> 
- <span data-ttu-id="fc4f6-108">Nascondere o visualizzare il contenuto per riflettere i servizi o le funzionalità supportati nell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="fc4f6-108">Hide or show content to reflect the services or features supported in your organization</span></span> 
- <span data-ttu-id="fc4f6-109">Creare playlist e sottocategorie personalizzate appositamente per le esigenze dell'utente</span><span class="sxs-lookup"><span data-stu-id="fc4f6-109">Build custom playlists and subcategories crafted specifically for your user's needs</span></span>
- <span data-ttu-id="fc4f6-110">Creare pagine di destinazione con contenuto filtrato per supportare i risultati aziendali, ad esempio per guidare l'adozione di Microsoft Teams, Outlook mobile o lavorare in modo più collaborativo con Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="fc4f6-110">Build landing pages with content filtered to support business outcomes, such as driving the adoption of Microsoft Teams, Outlook mobile, or working more collaboratively with Microsoft 365.</span></span>

![Raccolta generale di foto per percorsi di apprendimento Microsoft.](media/cg-introducing.png)

## <a name="requirements-and-permissions"></a><span data-ttu-id="fc4f6-112">Requisiti e autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="fc4f6-112">Requirements and Permissions</span></span>

<span data-ttu-id="fc4f6-113">Prima di iniziare a usare le indicazioni per personalizzare i percorsi di apprendimento, verificare che i percorsi di apprendimento siano stati impostati dall'amministratore tenant di SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fc4f6-113">Before getting started with the Customize learning pathways guidance, ensure that learning pathways has been set up by your SharePoint Tenant Administrator.</span></span> <span data-ttu-id="fc4f6-114">Se non si è certi che sia stato configurato, contattare l'amministratore tenant di SharePoint per verificare che sia stato eseguito il provisioning dei percorsi di apprendimento.</span><span class="sxs-lookup"><span data-stu-id="fc4f6-114">If you’re not sure if it's been set up, contact your SharePoint tenant administrator to verify that learning pathways has been provisioned.</span></span> <span data-ttu-id="fc4f6-115">Assicurarsi inoltre di ottenere l'URL dei percorsi di apprendimento del sito di SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fc4f6-115">Also be sure to get the URL of the learning pathways SharePoint site.</span></span> <span data-ttu-id="fc4f6-116">Se si è l'amministratore tenant e non è stato eseguito il provisioning dei percorsi di apprendimento, vedere [Provisioning dei percorsi di apprendimento.](custom_provision.md)</span><span class="sxs-lookup"><span data-stu-id="fc4f6-116">If you are the Tenant Administrator and learning pathways has not been provisioned, see [Provision learning pathways](custom_provision.md).</span></span> 

### <a name="permissions-to-provision-learning-pathways"></a><span data-ttu-id="fc4f6-117">Autorizzazioni per il provisioning dei percorsi di apprendimento</span><span class="sxs-lookup"><span data-stu-id="fc4f6-117">Permissions to provision learning pathways</span></span>

- <span data-ttu-id="fc4f6-118">Amministratore tenant, noto anche come amministratore globale di Office 365</span><span class="sxs-lookup"><span data-stu-id="fc4f6-118">Tenant Administrator, also known as Office 365 Global Administrator</span></span>
- <span data-ttu-id="fc4f6-119">L’amministratore della raccolta siti di SharePoint con autorizzazioni di proprietario nel sito</span><span class="sxs-lookup"><span data-stu-id="fc4f6-119">SharePoint Site Collection Administrator with Owner permissions on the site</span></span>

### <a name="permissions-to-use-learning-pathways-administration-features"></a><span data-ttu-id="fc4f6-120">Autorizzazioni per l'utilizzo dei percorsi di apprendimento Funzionalità di amministrazione</span><span class="sxs-lookup"><span data-stu-id="fc4f6-120">Permissions to use learning pathways Administration features</span></span>

- <span data-ttu-id="fc4f6-121">Amministratori delle raccolte siti</span><span class="sxs-lookup"><span data-stu-id="fc4f6-121">Site Collection Administrator</span></span>
- <span data-ttu-id="fc4f6-122">Autorizzazioni proprietario o membro di SharePoint</span><span class="sxs-lookup"><span data-stu-id="fc4f6-122">SharePoint Owner or Member permissions</span></span>

### <a name="permissions-to-use-the-learning-pathways-site-as-a-user"></a><span data-ttu-id="fc4f6-123">Autorizzazioni per l'utilizzo del sito dei percorsi di apprendimento come utente</span><span class="sxs-lookup"><span data-stu-id="fc4f6-123">Permissions to use the learning pathways site as a user</span></span>

- <span data-ttu-id="fc4f6-124">Autorizzazioni utente di Office 365/autorizzazioni di visitatore del sito di SharePoint o superiore</span><span class="sxs-lookup"><span data-stu-id="fc4f6-124">Office 365 user permissions/SharePoint Site Visitor permissions or higher</span></span>

## <a name="get-started-with-customization"></a><span data-ttu-id="fc4f6-125">Introduzione alla personalizzazione</span><span class="sxs-lookup"><span data-stu-id="fc4f6-125">Get started with customization</span></span>
<span data-ttu-id="fc4f6-126">Dopo aver garantito di disporre delle autorizzazioni necessarie per personalizzare il sito e la web part, è il momento di iniziare il processo di personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="fc4f6-126">Once you've ensured you have the necessary permissions to customize the site and web part, it's time to get started with the customization process.</span></span> 

- <span data-ttu-id="fc4f6-127">Per iniziare, vedere [Go to the learning pathways site.](custom_goto.md)</span><span class="sxs-lookup"><span data-stu-id="fc4f6-127">To get started, see [Go to the learning pathways site](custom_goto.md).</span></span>