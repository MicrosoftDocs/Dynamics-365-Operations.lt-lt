---
title: Lygiagrečių darbo eigos veiklų konfigūravimas
description: Norėdami konfigūruoti lygiagrečią veiklą, darbo eigos rengyklėje atlikite toliau nurodytas procedūras.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dfbe78f31082ad0b1272f02e3ae9d7adbd993b1
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797731"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="fdd69-103">Lygiagrečių darbo eigos veiklų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="fdd69-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdd69-104">Norėdami konfigūruoti lygiagrečią veiklą, darbo eigos rengyklėje atlikite toliau nurodytas procedūras.</span><span class="sxs-lookup"><span data-stu-id="fdd69-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="fdd69-105">Lygiagrečią veiklą sudaro vienu metu veikiančios darbo eigos šakos.</span><span class="sxs-lookup"><span data-stu-id="fdd69-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="fdd69-106">Lygiagrečios veiklos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="fdd69-106">Name a parallel activity</span></span>

<span data-ttu-id="fdd69-107">Norėdami įvesti lygiagrečios veiklos pavadinimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fdd69-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="fdd69-108">Dešiniuoju pelės mygtuku spustelėkite lygiagrečią veiklą, o tada spustelėkite **Ypatybės**, kad atidarytumėte formą **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="fdd69-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="fdd69-109">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="fdd69-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="fdd69-110">Lauke **Pavadinimas** įveskite unikalų lygiagrečios veiklos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="fdd69-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="fdd69-111">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="fdd69-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="fdd69-112">Lygiagrečios veiklos šakų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="fdd69-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="fdd69-113">Atlikite šiuos veiksmus, norėdami įtraukti ir konfigūruoti šios lygiagrečios veiklos šakas.</span><span class="sxs-lookup"><span data-stu-id="fdd69-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="fdd69-114">Dukart spustelėkite lygiagrečią veiklą, kad būtų rodomos lygiagrečios veiklos šakos.</span><span class="sxs-lookup"><span data-stu-id="fdd69-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="fdd69-115">Norėdami įtraukti šaką, nuvilkite elementą **Šaka** iš srities **Darbo eigos elementai** į įterpimo vietą drobėje.</span><span class="sxs-lookup"><span data-stu-id="fdd69-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="fdd69-116">Toliau pateiktame paveikslėlyje parodyta įterpimo vieta.</span><span class="sxs-lookup"><span data-stu-id="fdd69-116">The following figure shows an insertion point.</span></span>

    ![Įterpimo vieta](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="fdd69-118">Šakų tvarka nėra svarbi, nes visos lygiagrečios veiklos šakos vykdomos tuo pačiu metu.</span><span class="sxs-lookup"><span data-stu-id="fdd69-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="fdd69-119">Norėdami sukonfigūruoti kiekvieną šaką, žr. puslapį [Lygiagrečių šakų konfigūravimas darbo eigoje](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="fdd69-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>
