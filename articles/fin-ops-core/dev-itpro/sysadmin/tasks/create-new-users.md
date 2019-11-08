---
title: Naujų vartotojų kūrimas
description: Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
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
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570526"
---
# <a name="create-new-users"></a><span data-ttu-id="800bd-103">Naujų vartotojų kūrimas</span><span class="sxs-lookup"><span data-stu-id="800bd-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="800bd-104">Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.</span><span class="sxs-lookup"><span data-stu-id="800bd-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="800bd-105">Susiekite vartotoją su licencija (tik naujų licencijų tipais)</span><span class="sxs-lookup"><span data-stu-id="800bd-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="800bd-106">Klientams, kurių licencija yra viena iš naujų licencijų tipų, įtrauktų 2019 m. spalio mėn., vartotojai turi būti susieti su licencija.</span><span class="sxs-lookup"><span data-stu-id="800bd-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="800bd-107">Vartotojai, kurie susieti su licencija, automatiškai pridedami kaip sistemos vartotojai, kurie neturi vaidmenų pirmą kartą prisiregistravus.</span><span class="sxs-lookup"><span data-stu-id="800bd-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="800bd-108">Vartotojai, kurie nesusieti su licencija, gauna įspėjamąjį pranešimą.</span><span class="sxs-lookup"><span data-stu-id="800bd-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="800bd-109">Sistemos administratoriai gali [priskirti licencijas vartotojams](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) [„Microsoft 365” administravimo centre](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="800bd-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="800bd-110">Naujo vartotojo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="800bd-110">Add a new user</span></span>
1. <span data-ttu-id="800bd-111">Eikite į **Sistemos administravimas \> Vartotojai \> Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="800bd-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="800bd-112">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="800bd-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="800bd-113">Lauke **Vartotojo ID** įveskite vartotojo unikalųjį identifikatorių (ID).</span><span class="sxs-lookup"><span data-stu-id="800bd-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="800bd-114">Reikės vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="800bd-114">A user ID is required.</span></span>  
4. <span data-ttu-id="800bd-115">Lauke **Vartotojo vardas** įveskite vartotojo vardą.</span><span class="sxs-lookup"><span data-stu-id="800bd-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="800bd-116">Lauke **Domenas** įveskite vartotojo domeną.</span><span class="sxs-lookup"><span data-stu-id="800bd-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="800bd-117">Lauke **Pseudonimas** įveskite vartotojo pseudonimą.</span><span class="sxs-lookup"><span data-stu-id="800bd-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="800bd-118">Lauke **Įmonė** pasirinkite norimą įmonę.</span><span class="sxs-lookup"><span data-stu-id="800bd-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="800bd-119">„FastTab” konteineryje **Vartotojo vaidmenys** pasirinkite **Priskirti vaidmenis**, kad [priskirtumėte vartotojams saugos vaidmenis](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="800bd-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="800bd-120">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="800bd-120">Select **OK**.</span></span>
10. <span data-ttu-id="800bd-121">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="800bd-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="800bd-122">Importuoti vartotojus</span><span class="sxs-lookup"><span data-stu-id="800bd-122">Import users</span></span>
1. <span data-ttu-id="800bd-123">Veiksmų srityje pasirinkite **Importuoti vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="800bd-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="800bd-124">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="800bd-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="800bd-125">Pasirinkite **Importuoti vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="800bd-125">Select **Import users**.</span></span>
4. <span data-ttu-id="800bd-126">Pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="800bd-126">Select **Close**.</span></span>

