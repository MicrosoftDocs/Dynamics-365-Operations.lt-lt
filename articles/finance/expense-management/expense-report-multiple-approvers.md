---
title: Išlaidų ataskaitos ir keli tvirtintojai
description: Šioje temoje pateikiama informacijos apie išlaidų ataskaitas, kurias turi patvirtinti daugiau nei vienas asmuo.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d83a473e2e894856c12b36b4d005c6cb06b765a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179030"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="7261c-103">Išlaidų ataskaitos ir keli tvirtintojai</span><span class="sxs-lookup"><span data-stu-id="7261c-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7261c-104">Vartotojo pateiktą išlaidų ataskaitą gali reikėti patvirtini daugiau nei vienam asmeniui – tai priklauso nuo jūsų organizacijos išlaidų patvirtinimo strategijų.</span><span class="sxs-lookup"><span data-stu-id="7261c-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="7261c-105">Nustatydami išlaidų ataskaitų tvirtinimo darbo eigos procesą, galite įtraukti darbo eigos elementų, įskaitant užduotis ar veiksmus, skirtus vienam ar keliems išlaidų ataskaitų tvirtintojams.</span><span class="sxs-lookup"><span data-stu-id="7261c-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="7261c-106">Pavyzdžiui, galite reikalauti, kad visas išlaidų ataskaitas pirmiausia patvirtintų ataskaitą pateikusio darbuotojo vadovas, o tada – modulio Mokėtinos sumos koordinatorius.</span><span class="sxs-lookup"><span data-stu-id="7261c-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="7261c-107">Jei nusprendžiate reikalauti kelių išlaidų ataskaitų tvirtintojų, įtraukti darbo eigos elementų galite bet kuriuo iš tolesnių būdų.</span><span class="sxs-lookup"><span data-stu-id="7261c-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="7261c-108">Įtraukti vieną tvirtinimo elementą, kuris turi vieną veiksmą.</span><span class="sxs-lookup"><span data-stu-id="7261c-108">Add one approval element that has one step.</span></span> <span data-ttu-id="7261c-109">Pavyzdžiui, veiksmu galima reikalauti, kad išlaidų ataskaita būtų priskirta vartotojų grupei, ir kad ją patvirtintų 50 procentų vartotojų grupės narių.</span><span class="sxs-lookup"><span data-stu-id="7261c-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="7261c-110">Įtraukti vieną tvirtinimo elementą, kuris turi kelis veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7261c-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="7261c-111">Pavyzdžiui, tvirtinimo elementas gali turėti tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7261c-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="7261c-112">Išlaidų ataskaitą patvirtina ją pateikusio darbuotojo vadovas.</span><span class="sxs-lookup"><span data-stu-id="7261c-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="7261c-113">Modulio Mokėtinos sumos klerkas patikrina gavimus ir išlaidų ataskaitos elementus.</span><span class="sxs-lookup"><span data-stu-id="7261c-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="7261c-114">Išlaidų ataskaitą patvirtina biudžeto savininkas.</span><span class="sxs-lookup"><span data-stu-id="7261c-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="7261c-115">Įtraukti kelis tvirtinimo elementus, kurių kiekvienas turi vieną veiksmą.</span><span class="sxs-lookup"><span data-stu-id="7261c-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="7261c-116">Pavyzdžiui, atskirą tvirtinimo elementą galite įtraukti kiekvienam iš tolesnių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="7261c-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="7261c-117">Išlaidų ataskaitą patvirtina darbuotojo vadovas.</span><span class="sxs-lookup"><span data-stu-id="7261c-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="7261c-118">Išlaidų ataskaitą patvirtina biudžeto savininkas.</span><span class="sxs-lookup"><span data-stu-id="7261c-118">The budget owner approves the expense report.</span></span>
