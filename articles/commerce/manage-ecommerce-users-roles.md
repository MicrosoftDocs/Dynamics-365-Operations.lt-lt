---
title: Tvarkyti el. prekybos vartotojus ir vaidmenis
description: Šioje temoje paaiškinama, kaip suteikti vartotojams prieigą prie „Microsoft Dynamics 365 Commerce“ svetainės kūrimo aplinkos.
author: bicyclingfool
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
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a1f9abae20d0f2e71790a3b27337338dc042b52
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414235"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="68154-103">Tvarkyti el. prekybos vartotojus ir vaidmenis</span><span class="sxs-lookup"><span data-stu-id="68154-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="68154-104">Šioje temoje paaiškinama, kaip suteikti vartotojams prieigą prie „Microsoft Dynamics 365 Commerce“ svetainės kūrimo aplinkos.</span><span class="sxs-lookup"><span data-stu-id="68154-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="68154-105">Siekiant padėti valdyti vartotojo prieigą ir suteikti vartotojams teisę atlikti konkrečias užduotis, svetainės kūrimo aplinkoje naudojamos saugos grupės, sukurtos tarnyboje „Microsoft Azure Active Directory“ („Azure AD“).</span><span class="sxs-lookup"><span data-stu-id="68154-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="68154-106">Pirmiausia kūrimo aplinkoje kiekvienam vaidmeniui priskiriate naują arba esamą saugos grupę iš „Azure AD“.</span><span class="sxs-lookup"><span data-stu-id="68154-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="68154-107">Tada suteikiate arba panaikinate teises atskiriems vartotojams įtraukdami šiuos vartotojus į reikiamą saugos grupę arba pašalindami juos iš saugos grupės.</span><span class="sxs-lookup"><span data-stu-id="68154-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="68154-108">Kūrimo aplinkos vaidmenų apžvalga</span><span class="sxs-lookup"><span data-stu-id="68154-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="68154-109">„Dynamics 365 for Commerce“ kūrimo aplinkoje palaikomi šie vaidmenys.</span><span class="sxs-lookup"><span data-stu-id="68154-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="68154-110">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="68154-110">Role</span></span>                 | <span data-ttu-id="68154-111">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="68154-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="68154-112">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="68154-112">System Administrator</span></span> | <span data-ttu-id="68154-113">Vartotojai, turintys šį vaidmenį, turi visas teises visiems įrankiams bei visiems įvertinimams ir apžvalgoms.</span><span class="sxs-lookup"><span data-stu-id="68154-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="68154-114">Jie taip pat gali kurti svetaines.</span><span class="sxs-lookup"><span data-stu-id="68154-114">They can also create sites.</span></span> |
| <span data-ttu-id="68154-115">Administratorius</span><span class="sxs-lookup"><span data-stu-id="68154-115">Administrator</span></span>   | <span data-ttu-id="68154-116">Vartotojai, turintys šį vaidmenį, turi visas teises visiems įrankiams ir registravimo ir sprendimo paslaugai konkrečioje svetainės struktūroje.</span><span class="sxs-lookup"><span data-stu-id="68154-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="68154-117">Žiniatinklio svetainių kūrėjas</span><span class="sxs-lookup"><span data-stu-id="68154-117">Web Producer</span></span>         | <span data-ttu-id="68154-118">Šiuos vaidmenis turintys vartotojai gali kurti puslapius, fragmentus ir šablonus, įkelti ir tvarkyti išteklius bei papildyti produktus ir kategorijas.</span><span class="sxs-lookup"><span data-stu-id="68154-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="68154-119">Skaitytojas</span><span class="sxs-lookup"><span data-stu-id="68154-119">Reader</span></span>               | <span data-ttu-id="68154-120">Vartotojai, turintys šį vaidmenį, gali peržiūrėti puslapius, šablonus, išteklius, fragmentus, struktūras ir parametrus, bet negali nieko keisti.</span><span class="sxs-lookup"><span data-stu-id="68154-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="68154-121">Registravimo ir sprendimo moderatorius</span><span class="sxs-lookup"><span data-stu-id="68154-121">RnR Moderator</span></span>        | <span data-ttu-id="68154-122">Vartotojai, turintys šį vaidmenį, gali moderuoti produktų apžvalgas.</span><span class="sxs-lookup"><span data-stu-id="68154-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="68154-123">Sistemos administratoriaus vaidmuo</span><span class="sxs-lookup"><span data-stu-id="68154-123">System Administrator role</span></span>

<span data-ttu-id="68154-124">Kai sukonfigūruojate „Dynamics 365 Commerce“, esančią „Microsoft Dynamics“ „Lifecycle Services“ (LCS) aplinkoje, būsite paprašyti pateikti saugos grupę vaidmeniui **Sistemos administratorius**.</span><span class="sxs-lookup"><span data-stu-id="68154-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="68154-125">Šis vaidmuo automatiškai taikomas visoms svetainėms, kurias kuriate konfigūruodami aplinką.</span><span class="sxs-lookup"><span data-stu-id="68154-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="68154-126">Šio vaidmens saugos grupę galima atnaujinti tik LCS portale.</span><span class="sxs-lookup"><span data-stu-id="68154-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="68154-127">Visų svetainių puslapyje **Svetainės administravimas** jis yra tik skaitomas ir skirtas tik informaciniams tikslams.</span><span class="sxs-lookup"><span data-stu-id="68154-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="68154-128">Administratoriaus vaidmuo</span><span class="sxs-lookup"><span data-stu-id="68154-128">Administrator role</span></span>

<span data-ttu-id="68154-129">Kai sukuriate naują svetainę „Commerce“ programoje, būsite paprašyti pateikti saugos grupę vaidmeniui **Administratorius**.</span><span class="sxs-lookup"><span data-stu-id="68154-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="68154-130">Žiūrėkite anksčiau šioje temoje pateiktą lentelę, kad peržiūrėtumėte teises, kurias teikia šis vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="68154-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="68154-131">Saugos grupių įtraukimas arba naujinimas</span><span class="sxs-lookup"><span data-stu-id="68154-131">Add or update security groups</span></span>

<span data-ttu-id="68154-132">Sukūrus svetainę, tik tie vartotojai, kurie yra saugos grupėse, susietose su vaidmenimis **Sistemos administratorius** ir **Administratorius**, gali turėti prieigą prie tos svetainės kūrimo aplinkos.</span><span class="sxs-lookup"><span data-stu-id="68154-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="68154-133">Norėdami priskirti vartotojus vaidmenims **Žiniatinklio svetainės kūrėjas**, **Registravimo ir sprendimo moderatorius** ir **Skaitytojas**, turite priskirti saugos grupes šiems vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="68154-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="68154-134">Norėdami vaidmeniui pridėti saugos grupę arba atnaujinti saugos grupę, kuri šiuo metu priskirta vaidmeniui, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="68154-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="68154-135">Eikite į svetainę, kurią norite atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="68154-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="68154-136">Dalyje **Svetainės valdymas** atidarykite puslapį **Sauga**.</span><span class="sxs-lookup"><span data-stu-id="68154-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="68154-137">Pasirinkite vaidmenį, kurį norite modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="68154-137">Select the role to modify.</span></span>
1. <span data-ttu-id="68154-138">Įtraukite saugos grupes į vaidmenis arba pašalinkite saugos grupes iš vaidmenų.</span><span class="sxs-lookup"><span data-stu-id="68154-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68154-139">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="68154-139">Additional resources</span></span>

[<span data-ttu-id="68154-140">Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija</span><span class="sxs-lookup"><span data-stu-id="68154-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="68154-141">Ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei</span><span class="sxs-lookup"><span data-stu-id="68154-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="68154-142">Tvarkyti turinio saugos strategiją (CSP)</span><span class="sxs-lookup"><span data-stu-id="68154-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
