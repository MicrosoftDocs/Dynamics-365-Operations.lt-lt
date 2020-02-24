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
ms.openlocfilehash: 4db774783dba4b1cea9552da3cff29a9528bd496
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002179"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="1ff4c-103">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1ff4c-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1ff4c-104">Šioje temoje paaiškinama, kaip sukonfigūruoti „Microsoft Dynamics 365“ el. prekybos svetainės domeno pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="1ff4c-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="1ff4c-105">Domenų įtraukimas inicijuojant el. prekybą</span><span class="sxs-lookup"><span data-stu-id="1ff4c-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="1ff4c-106">Norėdami domenus susieti su savo el. prekybos aplinka, inicijuokite el. prekybą, kaip aprašyta temoje [Naujos el. prekybos svetainės diegimas](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="1ff4c-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="1ff4c-107">Inicijavimo metu jūsų paprašoma pateikti informaciją, kuri bus naudojama konfigūruojant jūsų el. prekybos aplinką.</span><span class="sxs-lookup"><span data-stu-id="1ff4c-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="1ff4c-108">Lauke **Palaikomi pagrindinių kompiuterių vardai** įtraukite visus domenus, kuriuos planuojate naudoti su šia aplinka.</span><span class="sxs-lookup"><span data-stu-id="1ff4c-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="1ff4c-109">Domenus reikia atskirti kabliataškiu.</span><span class="sxs-lookup"><span data-stu-id="1ff4c-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="1ff4c-110">Taip domenai sukonfigūruojami visuose būtinuose el. prekybos komponentuose ir yra paruošti naudoti, kai perjungiate srautą iš savo turinio pristatymo tinklo (CDN) arba žiniatinklio serverio ir nukreipiate į el. prekybos sąsajos serverius.</span><span class="sxs-lookup"><span data-stu-id="1ff4c-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="1ff4c-111">Domenų įtraukimas inicijavus el. prekybą</span><span class="sxs-lookup"><span data-stu-id="1ff4c-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="1ff4c-112">Norėdami naujus domenus su savo el. prekybos aplinka susieti inicijavę el. prekybą, turite pateikti aptarnavimo užklausą.</span><span class="sxs-lookup"><span data-stu-id="1ff4c-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ff4c-113">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1ff4c-113">Additional resources</span></span>

[<span data-ttu-id="1ff4c-114">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="1ff4c-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="1ff4c-115">E. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="1ff4c-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="1ff4c-116">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="1ff4c-116">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="1ff4c-117">„Robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="1ff4c-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="1ff4c-118">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="1ff4c-118">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="1ff4c-119">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="1ff4c-119">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="1ff4c-120">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="1ff4c-120">Enable location-based store detection</span></span>](enable-store-detection.md)
