---
title: Vartotojo vaidmenų nuomos priskyrimas
description: Šioje temoje aprašomi saugos vaidmenys, naudojami turto nuomoje. Jis taip pat paaiškina, kaip priskirti vartotojus šiems vaidmenims.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b31d0880d4f2cd2b8ad2dffcfe279421f935ed35
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446201"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="acfa5-104">Vartotojo vaidmenų nuomos priskyrimas</span><span class="sxs-lookup"><span data-stu-id="acfa5-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="acfa5-105">Šioje temoje aprašomi saugos vaidmenys, naudojami turto nuomoje.</span><span class="sxs-lookup"><span data-stu-id="acfa5-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="acfa5-106">Jis taip pat paaiškina, kaip priskirti vartotojus šiems vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="acfa5-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="acfa5-107">Trys vartotojo vaidmenys atskiria prieigą turto nuomoje.</span><span class="sxs-lookup"><span data-stu-id="acfa5-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="acfa5-108">Vienas vaidmuo yra tinkamas išnuomoti nuomos sutartis, jis tinkamas peržiūrėti nuomos sutartis, o vienas yra tinkamas nuomos sekretoriaus pareigoms atlikti.</span><span class="sxs-lookup"><span data-stu-id="acfa5-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="acfa5-109">Kiekvienas vaidmuo turi konkrečias visų nuomos puslapių teises ir leidžia vartotojams peržiūrėti, kurti, redaguoti arba naikinti nuomos sutartis pagal savo pareigas.</span><span class="sxs-lookup"><span data-stu-id="acfa5-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="acfa5-110">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="acfa5-110">Role</span></span>           | <span data-ttu-id="acfa5-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="acfa5-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="acfa5-112">Nuomos valdymas</span><span class="sxs-lookup"><span data-stu-id="acfa5-112">Maintain Lease</span></span> | <span data-ttu-id="acfa5-113">Šio vaidmens vartotojai gali pridėti, redaguoti, naikinti ir peržiūrėti nuomos sutartis.</span><span class="sxs-lookup"><span data-stu-id="acfa5-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="acfa5-114">Šis vaidmuo yra skirtas kasdieniam vartotojui, kurio užduotys apima mėnesio žurnalų įrašų kūrimą ir registravimą bei naujos nuomos įtraukimą.</span><span class="sxs-lookup"><span data-stu-id="acfa5-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="acfa5-115">Šis vaidmuo suteikia prieigą prie visų turto išperkamosios nuomos funkcinių galimybių.</span><span class="sxs-lookup"><span data-stu-id="acfa5-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="acfa5-116">Nuomos peržiūra</span><span class="sxs-lookup"><span data-stu-id="acfa5-116">View Lease</span></span>     | <span data-ttu-id="acfa5-117">Šio vaidmens vartotojai gali peržiūrėti tik nuomos įrašus, grafikus ir vykdyti ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="acfa5-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="acfa5-118">Jie negali sukurti naujos nuomos, redaguoti esamos nuomos arba kurti žurnalo įrašus pagal nuomos sutartis.</span><span class="sxs-lookup"><span data-stu-id="acfa5-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="acfa5-119">Šis vaidmuo yra skirtas vartotojams, kurie tereikia Peržiūrėti nuomos sutartis, nuomos grafikus ir operacijas, kurios vyksta prieš šias nuomos sutartis.</span><span class="sxs-lookup"><span data-stu-id="acfa5-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="acfa5-120">Nuomos klerkas</span><span class="sxs-lookup"><span data-stu-id="acfa5-120">Lease Clerk</span></span>    | <span data-ttu-id="acfa5-121">Šio vaidmens vartotojai gali kurti tik naujas nuomos sutartis.</span><span class="sxs-lookup"><span data-stu-id="acfa5-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="acfa5-122">Jie negali redaguoti arba naikinti esamos nuomos, peržiūrėti išperkamosios nuomos tvarkaraščius arba registruoti lizingo žurnalų įrašus.</span><span class="sxs-lookup"><span data-stu-id="acfa5-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="acfa5-123">Šis vaidmuo yra skirtas vartotojams, kurie dirba duomenų įvedimo pajėgumui.</span><span class="sxs-lookup"><span data-stu-id="acfa5-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="acfa5-124">Atlikite šiuos veiksmus, norėdami vartotojus priskirti vaidmenims, naudojamiems turto lizingui.</span><span class="sxs-lookup"><span data-stu-id="acfa5-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="acfa5-125">Eikite į **Sistemos administravimas \> Sauga \> Priskirti vartotojus vaidmenims**.</span><span class="sxs-lookup"><span data-stu-id="acfa5-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="acfa5-126">Pasirinkite vaidmenį **Nuomos valdymas**, **Nuomos klerkas** arba **Nuomos peržiūra** ir pasirinkite **Neautomatiškai priskirti / pašalinti vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="acfa5-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="acfa5-127">Pasirinkite vartotoją, kurį norite priskirti vaidmeniui, tada pasirinkite **Priskirti vaidmeniui**.</span><span class="sxs-lookup"><span data-stu-id="acfa5-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>
