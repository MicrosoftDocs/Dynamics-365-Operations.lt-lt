---
title: Užduoties įrašų saugos diagnostika
description: Šioje temoje pateikiama informacija apie tai, kaip analizuoti ir valdyti saugos teisių reikalavimus, paremtus užduoties įrašu.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 88eb90b35f1a9754cc4daa01d8f40cdf712db4f8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679795"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="00966-103">Užduoties įrašų saugos diagnostika</span><span class="sxs-lookup"><span data-stu-id="00966-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="00966-104">Prieš pradedant</span><span class="sxs-lookup"><span data-stu-id="00966-104">Before you begin</span></span>

<span data-ttu-id="00966-105">Šioje temoje pateikiama informacija apie tai, kaip analizuoti ir valdyti saugos teisių reikalavimus, paremtus užduoties įrašu.</span><span class="sxs-lookup"><span data-stu-id="00966-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="00966-106">Prieš atlikdami šioje temoje aprašytus veiksmus, turite turėti verslo proceso, kurį norite analizuoti, užduoties įrašą.</span><span class="sxs-lookup"><span data-stu-id="00966-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="00966-107">Norėdami įrašyti verslo procesą, žr. [Užduočių įrašymo priemonės ištekliai](../../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="00966-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="00966-108">Užduoties įrašo saugos valdymas</span><span class="sxs-lookup"><span data-stu-id="00966-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="00966-109">Eikite į **Sistemos administravimas** > **Sauga** > **Užduoties įrašo saugos diagnostika**.</span><span class="sxs-lookup"><span data-stu-id="00966-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="00966-110">Atidarykite užduoties įrašą iš jo buvimo vietos.</span><span class="sxs-lookup"><span data-stu-id="00966-110">Open the task recording from its location.</span></span> <span data-ttu-id="00966-111">Pasirinkite **Atidaryti iš šio kompiuterio** arba **Atidaryti iš „Lifecycle Services”** ir pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="00966-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="00966-112">Atsidarys puslapis **Saugos meniu elementų informacija**, kuriame pateikiami procesui būtini saugos objektai.</span><span class="sxs-lookup"><span data-stu-id="00966-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="00966-113">Meniu elementai **Veiksmas** ir **Išvestis** nėra įtraukti į sąrašą.</span><span class="sxs-lookup"><span data-stu-id="00966-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="00966-114">Lauke **Vartotojo ID** pasirinkite vartotoją.</span><span class="sxs-lookup"><span data-stu-id="00966-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="00966-115">Jei vartotojas neturi kai kurių meniu elementų teisių, laukas **Trūkstamos teisės** bus atnaujintas į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="00966-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![Saugos meniu elementų informacijos puslapis](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="00966-117">Pasirinkite **Įtraukti nuorodą**, kad peržiūrėtumėte saugos objektų sąrašą, įskaitant vaidmenis, pareigas ir teises, pagal kurias suteikiama trūkstama teisė.</span><span class="sxs-lookup"><span data-stu-id="00966-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="00966-118">Pasirinkite saugos objektą sąraše.</span><span class="sxs-lookup"><span data-stu-id="00966-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="00966-119">Jei pasirinkta **Vaidmuo**, pasirinkite **Įtraukti vaidmenį vartotojui**.</span><span class="sxs-lookup"><span data-stu-id="00966-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="00966-120">Atsidarys puslapis **Priskirti vartotojus vaidmenims**.</span><span class="sxs-lookup"><span data-stu-id="00966-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="00966-121">Norėdami gauti daugiau informacijos, žr. puslapį [Vartotojų priskyrimas saugos vaidmenims](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="00966-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="00966-122">Jei pasirinkta **Pareiga**, pasirinkite **Įtraukti pareigą vaidmeniui**, tada pasirinkite vaidmenis, į kuriuos turi būti įtraukta pareiga, tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="00966-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="00966-123">Jei pasirinkta **Teisė**, pasirinkite **Įtraukti teisę pareigoms**, tada pasirinkite vaidmenis, į kuriuos turi būti įtraukta pareiga, tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="00966-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>
