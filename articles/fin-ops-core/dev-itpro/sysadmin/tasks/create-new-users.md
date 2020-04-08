---
title: Naujų vartotojų kūrimas
description: Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.
author: maertenm
manager: AnnBe
ms.date: 02/06/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9db4b6d355d6499bce6c550b2fbe76b82cf69fd4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143586"
---
# <a name="create-new-users"></a><span data-ttu-id="5de3e-103">Naujų vartotojų kūrimas</span><span class="sxs-lookup"><span data-stu-id="5de3e-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5de3e-104">Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.</span><span class="sxs-lookup"><span data-stu-id="5de3e-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="5de3e-105">Susiekite vartotoją su licencija (tik naujų licencijų tipais)</span><span class="sxs-lookup"><span data-stu-id="5de3e-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="5de3e-106">Klientams, kurių licencija yra viena iš naujų licencijų tipų, įtrauktų 2019 m. spalio mėn., vartotojai turi būti susieti su licencija.</span><span class="sxs-lookup"><span data-stu-id="5de3e-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="5de3e-107">Vartotojai, kurie susieti su licencija, automatiškai pridedami kaip sistemos vartotojai, kurie neturi vaidmenų pirmą kartą prisiregistravus.</span><span class="sxs-lookup"><span data-stu-id="5de3e-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="5de3e-108">Sistemos administratoriai gali [priskirti licencijas vartotojams](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [„Microsoft 365” administravimo centre](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="5de3e-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="5de3e-109">Išorinio vartotojo susiejimas su licencija (tik su naujais licencijų tipais)</span><span class="sxs-lookup"><span data-stu-id="5de3e-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="5de3e-110">Vartotojai, nepriklausantys nuomotojui, kuriame buvo įdiegta aplinka, turi būti pateikiami pagrindinio nuomotojo kataloge („Azure Active Directory“ („Azure AD“)), kad jiems būtų galima priskirti licencijas.</span><span class="sxs-lookup"><span data-stu-id="5de3e-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="5de3e-111">Minėtus išorinius vartotojus reikia įtraukti į „Azure AD“ esantį nuomotoją kaip vartotojus svečius ir priskirti jiems atitinkamas licencijas.</span><span class="sxs-lookup"><span data-stu-id="5de3e-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="5de3e-112">Norėdami gauti daugiau informacijos, žr. [„Azure Active Directory“ B2B bendradarbiavimo vartotojų įtraukimas „Azure“ portale](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="5de3e-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="5de3e-113">Naujo vartotojo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="5de3e-113">Add a new user</span></span>
1. <span data-ttu-id="5de3e-114">Eikite į **Sistemos administravimas \> Vartotojai \> Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="5de3e-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="5de3e-115">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="5de3e-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="5de3e-116">Lauke **Vartotojo ID** įveskite vartotojo unikalųjį identifikatorių (ID).</span><span class="sxs-lookup"><span data-stu-id="5de3e-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="5de3e-117">Reikės vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="5de3e-117">A user ID is required.</span></span>  
4. <span data-ttu-id="5de3e-118">Lauke **Vartotojo vardas** įveskite vartotojo vardą.</span><span class="sxs-lookup"><span data-stu-id="5de3e-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="5de3e-119">Lauke **Domenas** įveskite vartotojo domeną.</span><span class="sxs-lookup"><span data-stu-id="5de3e-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="5de3e-120">Lauke **Pseudonimas** įveskite vartotojo pseudonimą.</span><span class="sxs-lookup"><span data-stu-id="5de3e-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="5de3e-121">Lauke **Įmonė** pasirinkite norimą įmonę.</span><span class="sxs-lookup"><span data-stu-id="5de3e-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="5de3e-122">„FastTab” **Vartotojo vaidmenys** pasirinkite **Priskirti vaidmenis**, kad priskirtumėte vartotojams saugos vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="5de3e-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="5de3e-123">Norėdami gauti daugiau informacijos, žr. [Vartotojų priskyrimas saugos vaidmenims](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="5de3e-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="5de3e-124">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5de3e-124">Select **OK**.</span></span>
10. <span data-ttu-id="5de3e-125">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5de3e-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="5de3e-126">Importuoti vartotojus</span><span class="sxs-lookup"><span data-stu-id="5de3e-126">Import users</span></span>
1. <span data-ttu-id="5de3e-127">Veiksmų srityje pasirinkite **Importuoti vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="5de3e-127">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="5de3e-128">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="5de3e-128">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="5de3e-129">Pasirinkite **Importuoti vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="5de3e-129">Select **Import users**.</span></span>
4. <span data-ttu-id="5de3e-130">Pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="5de3e-130">Select **Close**.</span></span>

