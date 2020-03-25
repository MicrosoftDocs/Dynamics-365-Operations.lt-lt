---
title: Jūsų domeno vardo konfigūravimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti „Microsoft Dynamics 365“ el. prekybos svetainės domeno pavadinimą.
author: psimolin
manager: AnnBe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2ad9ca3aee21301ef6d830d7b29982a45cd53f60
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096825"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="e866c-103">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e866c-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e866c-104">Šioje temoje paaiškinama, kaip sukonfigūruoti „Microsoft Dynamics 365“ el. prekybos svetainės domeno pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e866c-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="e866c-105">Domenų įtraukimas inicijuojant el. prekybą</span><span class="sxs-lookup"><span data-stu-id="e866c-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="e866c-106">Norėdami domenus susieti su savo el. prekybos aplinka, inicijuokite el. prekybą, kaip aprašyta temoje [Naujos el. prekybos svetainės diegimas](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="e866c-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="e866c-107">Inicijavimo metu jūsų paprašoma pateikti informaciją, kuri bus naudojama konfigūruojant jūsų el. prekybos aplinką.</span><span class="sxs-lookup"><span data-stu-id="e866c-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="e866c-108">Lauke **Palaikomi pagrindinių kompiuterių vardai** įtraukite visus domenus, kuriuos planuojate naudoti su šia aplinka.</span><span class="sxs-lookup"><span data-stu-id="e866c-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="e866c-109">Domenus reikia atskirti kabliataškiu.</span><span class="sxs-lookup"><span data-stu-id="e866c-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="e866c-110">Taip domenai sukonfigūruojami visuose būtinuose el. prekybos komponentuose ir yra paruošti naudoti, kai perjungiate srautą iš savo turinio pristatymo tinklo (CDN) arba žiniatinklio serverio ir nukreipiate į el. prekybos sąsajos serverius.</span><span class="sxs-lookup"><span data-stu-id="e866c-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="e866c-111">Domenų įtraukimas inicijavus el. prekybą</span><span class="sxs-lookup"><span data-stu-id="e866c-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="e866c-112">Norėdami naujus domenus su savo el. prekybos aplinka susieti inicijavę el. prekybą, turite pateikti aptarnavimo užklausą.</span><span class="sxs-lookup"><span data-stu-id="e866c-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e866c-113">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e866c-113">Additional resources</span></span>

[<span data-ttu-id="e866c-114">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="e866c-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e866c-115">Interneto parduotuvės kanalo integravimas</span><span class="sxs-lookup"><span data-stu-id="e866c-115">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="e866c-116">El. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="e866c-116">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e866c-117">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="e866c-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e866c-118">„Robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="e866c-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e866c-119">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="e866c-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="e866c-120">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="e866c-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="e866c-121">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="e866c-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="e866c-122">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e866c-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="e866c-123">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="e866c-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e866c-124">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="e866c-124">Enable location-based store detection</span></span>](enable-store-detection.md)
