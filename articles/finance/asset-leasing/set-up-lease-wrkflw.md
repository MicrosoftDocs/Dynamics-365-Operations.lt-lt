---
title: Nuomos patvirtinimo darbo eigų nustatymas
description: Temoje paaiškinama, kaip nustatyti patvirtinimo darbo eigą, kuri bus vykdoma sukūrus naują nuomos sutartį.
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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1eaa2f5cc191ec93c30f4f10a662a87e501a341d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249586"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="dc808-103">Nuomos patvirtinimo darbo eigų nustatymas</span><span class="sxs-lookup"><span data-stu-id="dc808-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc808-104">Temoje paaiškinama, kaip nustatyti patvirtinimo darbo eigą, kuri bus vykdoma sukūrus naują nuomos sutartį.</span><span class="sxs-lookup"><span data-stu-id="dc808-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="dc808-105">Informacijos apie tai, kaip naudoti darbo eigą, ieškokite [Nuomos tvirtinimo darbo eigų naudojimas](use-create-lease-wrkflw.md).</span><span class="sxs-lookup"><span data-stu-id="dc808-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="dc808-106">Eikite į **Turto nuoma \> Sąranka \> Nuomos darbo eiga**.</span><span class="sxs-lookup"><span data-stu-id="dc808-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="dc808-107">Puslapyje **Nuomos darbo eiga** pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="dc808-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="dc808-108">Pasirodžiusiame dialogo lange, srityje **Darbo eigos tipas** pasirinkite saitą **Nuomos darbo eiga**.</span><span class="sxs-lookup"><span data-stu-id="dc808-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="dc808-109">Programa atidaroma.</span><span class="sxs-lookup"><span data-stu-id="dc808-109">The application is opened.</span></span> <span data-ttu-id="dc808-110">Ją paleidus, prisijunkite prie „Azure Active Directory“ („Azure AD“), kad nukreiptų į darbo eigos programą.</span><span class="sxs-lookup"><span data-stu-id="dc808-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="dc808-111">Nuvilkite elementą **Nuomos darbo eigos patvirtinimo** ant darbo eigos.</span><span class="sxs-lookup"><span data-stu-id="dc808-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="dc808-112">Sujungti vieną mazgą iš **Pradžia** į **Nuomos darbo eigos patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="dc808-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="dc808-113">Tada norėdami **baigti** prijunkite **nuomos darbo eigos patvirtinimą**.</span><span class="sxs-lookup"><span data-stu-id="dc808-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="dc808-114">Du kartus spustelėkite **Nuomos darbo eigos patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="dc808-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="dc808-115">Pasirinkite **Ypatybės**, tada dalyje **Pagrindiniai parametrai** įveskite darbo eigos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="dc808-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="dc808-116">Šiame puslapyje taip pat galite nustatyti daugiau darbo eigos parametrų.</span><span class="sxs-lookup"><span data-stu-id="dc808-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="dc808-117">Jei įjungėte **automatinius veiksmus**, sistema automatiškai imsis konkretaus veiksmo.</span><span class="sxs-lookup"><span data-stu-id="dc808-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="dc808-118">Pranešimus galima siųsti, jei jie nurodyti skirtuke **Pranešimai**. Skirtuke **Išplėstiniai parametrai** galite nurodyti galutinį tvirtintoją, nustatyti laiko limitą ir nurodyti konkrečius veiksmus, kuriuos reikia atlikti.</span><span class="sxs-lookup"><span data-stu-id="dc808-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="dc808-119">Kai baigsite nustatyti darbo eigos parametrus, pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="dc808-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="dc808-120">Pasirinkite **1 veiksmas**, tada – **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="dc808-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="dc808-121">Dalyje **Pagrindiniai parametrai** įveskite veiksmo pavadinimą, sukurkite patvirtinimo temos eilutę ir nurodykite patvirtinimo instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="dc808-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="dc808-122">Puslapyje **Priskyrimas** pasirinkite priskyrimo tipą.</span><span class="sxs-lookup"><span data-stu-id="dc808-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="dc808-123">Norėdami patvirtinti tam tikrus vartotojus, pasirinkite **Vartotojas**, pasirinkite vartotojus, kurie patvirtina nuomą, ir pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="dc808-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="dc808-124">Pasirinkite **Įrašyti ir uždaryti**, kad sukurtumėte darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="dc808-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="dc808-125">Tada, kai būsite raginami, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="dc808-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="dc808-126">Puslapyje **Darbo eigos kūrimas** pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="dc808-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="dc808-127">Pasirinkite naują darbo eigą ir pasirinkite **Versijos**.</span><span class="sxs-lookup"><span data-stu-id="dc808-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="dc808-128">Tada pasirinkite **Suaktyvinti**, kad įsitikintumėte, jog darbo eiga yra aktyvi.</span><span class="sxs-lookup"><span data-stu-id="dc808-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="dc808-129">Pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="dc808-129">Select **Close**.</span></span> <span data-ttu-id="dc808-130">Rodoma nauja aktyvi versija.</span><span class="sxs-lookup"><span data-stu-id="dc808-130">The new active version appears.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]