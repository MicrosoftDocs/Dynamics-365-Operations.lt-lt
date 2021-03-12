---
title: Jūsų domeno vardo konfigūravimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti „Microsoft Dynamics 365“ el. prekybos svetainės domeno pavadinimą.
author: psimolin
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d3df563b62b40970509340802a09bb36dda14777
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001005"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="be59e-103">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="be59e-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="be59e-104">Šioje temoje paaiškinama, kaip sukonfigūruoti „Microsoft Dynamics 365“ el. prekybos svetainės domeno pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="be59e-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="be59e-105">Įtraukite domenus e-komercijos pradžiai</span><span class="sxs-lookup"><span data-stu-id="be59e-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="be59e-106">Norėdami susieti domenus su savo „Dynamics 365 Commerce“ e-komercijos aplinka, pradėkite e-komerciją kaip aprašyta [Talpinti naują e-komercijos nuomotoją](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="be59e-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="be59e-107">Pradžios metu jūsų bus prašoma pateikti informaciją, kuri bus naudojama siekiant suteikti e-komercijos aplinką.</span><span class="sxs-lookup"><span data-stu-id="be59e-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="be59e-108">Lauke **Palaikomi pagrindinių kompiuterių vardai** įtraukite visus domenus, kuriuos planuojate naudoti su šia aplinka.</span><span class="sxs-lookup"><span data-stu-id="be59e-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="be59e-109">Domenus reikia atskirti kabliataškiu.</span><span class="sxs-lookup"><span data-stu-id="be59e-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="be59e-110">Tokiu būdu, domenai yra konfigūruojami visuose būtinuose komercijos komponentuose ir jie yra pasirengę būti naudojami jums perjungiant eismą iš jūsų turinio pristatymo tinklo (CDN) ar žiniatinklio serverio ir nukreipti jį į e-komercijos priekines linijas.</span><span class="sxs-lookup"><span data-stu-id="be59e-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="be59e-111">Įtraukite domenus po e-komercijos pradžios</span><span class="sxs-lookup"><span data-stu-id="be59e-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="be59e-112">Norėdami susieti naujus domenus su savo e-komercijos aplinka po to, kai e-komercija pradėta, privalote pateikti paslaugų prašymą.</span><span class="sxs-lookup"><span data-stu-id="be59e-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be59e-113">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="be59e-113">Additional resources</span></span>

[<span data-ttu-id="be59e-114">Talpinkite naują e-komercijos nuomotoją</span><span class="sxs-lookup"><span data-stu-id="be59e-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="be59e-115">Sukurkite e-komercijos saitą</span><span class="sxs-lookup"><span data-stu-id="be59e-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="be59e-116">Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu</span><span class="sxs-lookup"><span data-stu-id="be59e-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="be59e-117">robots.txt failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="be59e-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="be59e-118">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="be59e-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="be59e-119">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="be59e-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="be59e-120">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="be59e-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="be59e-121">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="be59e-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="be59e-122">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="be59e-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="be59e-123">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="be59e-123">Enable location-based store detection</span></span>](enable-store-detection.md)
