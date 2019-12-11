---
title: Jūsų domeno vardo konfigūravimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti „Microsoft Dynamics 365“ el. prekybos svetainės domeno pavadinimą.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
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
ms.openlocfilehash: 7a988f533757cc3f8555fcf4fb724a22a5b014f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770463"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="cf225-103">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cf225-103">Configure your domain name</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="cf225-104">Šioje temoje paaiškinama, kaip sukonfigūruoti „Microsoft Dynamics 365“ el. prekybos svetainės domeno pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="cf225-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="cf225-105">Domenų įtraukimas inicijuojant el. prekybą</span><span class="sxs-lookup"><span data-stu-id="cf225-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="cf225-106">Norėdami domenus susieti su savo el. prekybos aplinka, inicijuokite el. prekybą, kaip aprašyta temoje [Naujos el. prekybos svetainės diegimas](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="cf225-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="cf225-107">Inicijavimo metu jūsų paprašoma pateikti informaciją, kuri bus naudojama konfigūruojant jūsų el. prekybos aplinką.</span><span class="sxs-lookup"><span data-stu-id="cf225-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="cf225-108">Lauke **Palaikomi pagrindinių kompiuterių vardai** įtraukite visus domenus, kuriuos planuojate naudoti su šia aplinka.</span><span class="sxs-lookup"><span data-stu-id="cf225-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="cf225-109">Domenus reikia atskirti kabliataškiu.</span><span class="sxs-lookup"><span data-stu-id="cf225-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="cf225-110">Taip domenai sukonfigūruojami visuose būtinuose el. prekybos komponentuose ir yra paruošti naudoti, kai perjungiate srautą iš savo turinio pristatymo tinklo (CDN) arba žiniatinklio serverio ir nukreipiate į el. prekybos sąsajos serverius.</span><span class="sxs-lookup"><span data-stu-id="cf225-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="cf225-111">Domenų įtraukimas inicijavus el. prekybą</span><span class="sxs-lookup"><span data-stu-id="cf225-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="cf225-112">Norėdami naujus domenus su savo el. prekybos aplinka susieti inicijavę el. prekybą, turite pateikti aptarnavimo užklausą.</span><span class="sxs-lookup"><span data-stu-id="cf225-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf225-113">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="cf225-113">Additional resources</span></span>

[<span data-ttu-id="cf225-114">Interneto parduotuvės peržiūra</span><span class="sxs-lookup"><span data-stu-id="cf225-114">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="cf225-115">E. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="cf225-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="cf225-116">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="cf225-116">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="cf225-117">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="cf225-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="cf225-118">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="cf225-118">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="cf225-119">Įgalinti parduotuvės nustatymą pagal vietą</span><span class="sxs-lookup"><span data-stu-id="cf225-119">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="cf225-120">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="cf225-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
