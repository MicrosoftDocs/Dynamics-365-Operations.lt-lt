---
title: Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus
description: Šioje temoje paaiškinama, kaip sutikti naudoti įvertinimus ir apžvalgas savo „Microsoft Dynamics 365 Commerce“ svetainėje.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6c54a8fa01badb6a383c41dc979e71d82a25ef97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251240"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="537b7-103">Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite</span><span class="sxs-lookup"><span data-stu-id="537b7-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="537b7-104">Šioje temoje paaiškinama, kaip sutikti naudoti įvertinimus ir apžvalgas savo „Microsoft Dynamics 365 Commerce“ svetainėje.</span><span class="sxs-lookup"><span data-stu-id="537b7-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="537b7-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="537b7-105">Overview</span></span>

<span data-ttu-id="537b7-106">Įvertinimų ir apžvalgų sprendimas yra daugiakanalis sprendimas, kurį galite padaryti pasiekiamą „Dynamics 365 Commerce“, naudojant „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="537b7-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="537b7-107">LCS yra administravimo portalas, kurį prekybininkai naudoja valdyti savo aplinką nuo jos parengimo iki jos ekspoatacijos nutraukimo.</span><span class="sxs-lookup"><span data-stu-id="537b7-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="537b7-108">Jei norite naudoti įvertinimų ir apžvalgų sprendimą savo „Commerce“ svetainėje, turite pasirinkti įvertinimus ir apžvalgas diegiant savo „e-Commerce“ svetainę „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="537b7-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="537b7-109">Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite</span><span class="sxs-lookup"><span data-stu-id="537b7-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="537b7-110">Norėdami sutikti naudoti įvertinimus ir apžvalgas savo svetainėje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="537b7-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="537b7-111">Vykdykite veiksmus, nurodytus temoje [Naujos el. prekybos svetainės diegimas](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="537b7-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="537b7-112">Kol jūs vis dar esate LCS portale, eikite į **„Retail“ diegimo sąranka \> Kiti parametrai**.</span><span class="sxs-lookup"><span data-stu-id="537b7-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="537b7-113">Parinktį **Įjungti įvertinimų ir apžvalgų paslaugą** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="537b7-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="537b7-114">Lauke **AAD saugos grupė, skirta įvertinimų ir apžvalgų moderatoriui (saugos grupės objekto ID)**, įveskite „Microsoft Azure Active Directory“ („Azure AD“) saugos grupės, apimančios įvertinimų ir atsiliepimų moderatorių vaidmenį, ID.</span><span class="sxs-lookup"><span data-stu-id="537b7-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="537b7-116">Baikite el. prekybos inicijavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="537b7-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="537b7-117">Jei jau esate „Dynamics 365 Commerce“ klientas, įdiegėte „e-Commerce“ svetainę, bet nepasirinkote įvertinimų ir apžvalgų, o norite naudoti paketo „Dynamics 365 Commerce“ įvertinimus ir apžvalgas, pateikite aptarnavimo užklausą.</span><span class="sxs-lookup"><span data-stu-id="537b7-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="537b7-118">Norėdami gauti informacijos apie tai, kaip pateikti aptarnavimo užklausą, žr. [Pateikti aptarnavimo užklausų procesą](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="537b7-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="537b7-119">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="537b7-119">Additional resources</span></span>

[<span data-ttu-id="537b7-120">Įvertinimų ir atsiliepimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="537b7-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="537b7-121">Įvertinimų ir atsiliepimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="537b7-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="537b7-122">Įvertinimų ir atsiliepimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="537b7-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="537b7-123">Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Commerce“</span><span class="sxs-lookup"><span data-stu-id="537b7-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]