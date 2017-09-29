---
title: "Lygiagrečios darbo eigos veiklos konfigūravimas"
description: "Norėdami konfigūruoti lygiagrečią veiklą, darbo eigos rengyklėje atlikite toliau nurodytas procedūras."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 5473327c0665c9183746eb8125c7a368fbedc21e
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="configure-a-parallel-activity-in-a-workflow"></a><span data-ttu-id="d800f-103">Lygiagrečios darbo eigos veiklos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="d800f-103">Configure a parallel activity in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d800f-104">Norėdami konfigūruoti lygiagrečią veiklą, darbo eigos rengyklėje atlikite toliau nurodytas procedūras.</span><span class="sxs-lookup"><span data-stu-id="d800f-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="d800f-105">Lygiagrečią veiklą sudaro vienu metu veikiančios darbo eigos šakos.</span><span class="sxs-lookup"><span data-stu-id="d800f-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="d800f-106">Lygiagrečios veiklos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="d800f-106">Name a parallel activity</span></span>
<span data-ttu-id="d800f-107">Norėdami įvesti lygiagrečios veiklos pavadinimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d800f-107">Follow these steps to enter a name for a parallel activity.</span></span>
1.  <span data-ttu-id="d800f-108">Dešiniuoju pelės mygtuku spustelėkite lygiagrečią veiklą, o tada spustelėkite **Ypatybės**, kad atidarytumėte formą **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="d800f-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2.  <span data-ttu-id="d800f-109">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="d800f-109">In the left pane, click **Basic Settings**.</span></span>
3.  <span data-ttu-id="d800f-110">Lauke **Pavadinimas** įveskite unikalų lygiagrečios veiklos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="d800f-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4.  <span data-ttu-id="d800f-111">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="d800f-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="d800f-112">Lygiagrečios veiklos šakų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="d800f-112">Configure the branches of a parallel activity</span></span>
<span data-ttu-id="d800f-113">Atlikite šiuos veiksmus, norėdami įtraukti ir konfigūruoti šios lygiagrečios veiklos šakas.</span><span class="sxs-lookup"><span data-stu-id="d800f-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>
1.  <span data-ttu-id="d800f-114">Dukart spustelėkite lygiagrečią veiklą, kad būtų rodomos lygiagrečios veiklos šakos.</span><span class="sxs-lookup"><span data-stu-id="d800f-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2.  <span data-ttu-id="d800f-115">Norėdami įtraukti šaką, nuvilkite elementą **Šaka** iš srities **Darbo eigos elementai** į įterpimo vietą drobėje.</span><span class="sxs-lookup"><span data-stu-id="d800f-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="d800f-116">Toliau pateiktame paveikslėlyje parodyta įterpimo vieta.![Įterpimo vieta](./media/workflow_insertionpoint.gif)</span><span class="sxs-lookup"><span data-stu-id="d800f-116">The following figure shows an insertion point.![Insertion point](./media/workflow_insertionpoint.gif)</span></span>
    | <span data-ttu-id="d800f-117">**Pastaba.**</span><span class="sxs-lookup"><span data-stu-id="d800f-117">**Note**</span></span>                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d800f-118">Šakų tvarka nėra svarbi, nes visos lygiagrečios veiklos šakos vykdomos tuo pačiu metu.</span><span class="sxs-lookup"><span data-stu-id="d800f-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span> |

3.  <span data-ttu-id="d800f-119">Norėdami konfigūruoti kiekvieną šaką, žr. puslapį [Lygiagrečios šakos konfigūravimas](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="d800f-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>






