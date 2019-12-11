---
title: Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus
description: Šioje temoje paaiškinama, kaip sutikti naudoti įvertinimus ir apžvalgas savo „Microsoft Dynamics 365 Commerce“ svetainėje.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697985"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="9c4aa-103">Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus</span><span class="sxs-lookup"><span data-stu-id="9c4aa-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9c4aa-104">Šioje temoje paaiškinama, kaip sutikti naudoti įvertinimus ir apžvalgas savo „Microsoft Dynamics 365 Commerce“ svetainėje.</span><span class="sxs-lookup"><span data-stu-id="9c4aa-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="9c4aa-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="9c4aa-105">Overview</span></span>

<span data-ttu-id="9c4aa-106">Įvertinimų ir apžvalgų sprendimas – tai daugiakanalis sprendimas, pasiekiamas „Dynamics 365 Commerce“ naudojant „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="9c4aa-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9c4aa-107">LCS yra administravimo portalas, kurį prekybininkai naudoja valdyti savo aplinką nuo jos parengimo iki jos ekspoatacijos nutraukimo.</span><span class="sxs-lookup"><span data-stu-id="9c4aa-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="9c4aa-108">Jei norite naudoti įvertinimų ir apžvalgų sprendimą savo „Commerce“ svetainėje, pirmiausia turite sutikti.</span><span class="sxs-lookup"><span data-stu-id="9c4aa-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="9c4aa-109">Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus</span><span class="sxs-lookup"><span data-stu-id="9c4aa-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="9c4aa-110">Norėdami sutikti naudoti įvertinimus ir apžvalgas savo svetainėje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9c4aa-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="9c4aa-111">Vykdykite veiksmus, nurodytus temoje [Naujos el. prekybos svetainės diegimas](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="9c4aa-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="9c4aa-112">Kol jūs vis dar esate LCS portale, eikite į **„Retail“ diegimo sąranka \> Kiti parametrai**.</span><span class="sxs-lookup"><span data-stu-id="9c4aa-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="9c4aa-113">Parinktį **Įjungti įvertinimų ir apžvalgų paslaugą** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="9c4aa-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="9c4aa-114">Lauke **AAD saugos grupė, skirta įvertinimų ir apžvalgų moderatoriui (saugos grupės objekto ID)**, įveskite „Microsoft Azure Active Directory“ („Azure AD“) saugos grupės, apimančios įvertinimų ir atsiliepimų moderatorių vaidmenį, ID.</span><span class="sxs-lookup"><span data-stu-id="9c4aa-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="9c4aa-116">Baikite el. prekybos inicijavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="9c4aa-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c4aa-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9c4aa-117">Additional resources</span></span>

[<span data-ttu-id="9c4aa-118">Įvertinimų ir atsiliepimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="9c4aa-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="9c4aa-119">Įvertinimų ir atsiliepimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="9c4aa-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="9c4aa-120">Įvertinimų ir atsiliepimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9c4aa-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="9c4aa-121">Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Retail“</span><span class="sxs-lookup"><span data-stu-id="9c4aa-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
