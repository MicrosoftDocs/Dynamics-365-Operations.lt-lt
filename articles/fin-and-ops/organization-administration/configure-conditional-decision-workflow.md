---
title: Sąlyginių darbo eigos sprendimų konfigūravimas
description: Naudokite šią procedūrą, norėdami konfigūruoti sąlyginio sprendimo ypatybes.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a01290b3e2810aa1762f2230e8d01d219d6b10bf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "328199"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a><span data-ttu-id="6c05c-103">Sąlyginių darbo eigos sprendimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="6c05c-103">Configure conditional decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c05c-104">Naudokite šią procedūrą, norėdami konfigūruoti sąlyginio sprendimo ypatybes.</span><span class="sxs-lookup"><span data-stu-id="6c05c-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="6c05c-105">Sąlyginis sprendimas – tai taškas, kuriame darbo eiga padalijama į dvi šakas.</span><span class="sxs-lookup"><span data-stu-id="6c05c-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="6c05c-106">Norėdami darbo eigos rengyklėje konfigūruoti sąlyginį sprendimą, dešiniuoju pelės mygtuku spustelėkite sąlyginį sprendimą ir tada spustelėkite **Ypatybės**, kad atidarytumėte formą **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="6c05c-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="6c05c-107">Sprendimo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="6c05c-107">Name a decision</span></span>

<span data-ttu-id="6c05c-108">Norėdami įvesti sąlyginio sprendimo pavadinimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6c05c-108">Follow these steps to enter a name for a conditional decision.</span></span>

1. <span data-ttu-id="6c05c-109">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6c05c-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="6c05c-110">Lauke **Pavadinimas** įveskite unikalų sąlyginio sprendimo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="6c05c-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="6c05c-111"> Sąlygų nustatymas</span><span class="sxs-lookup"><span data-stu-id="6c05c-111">Set conditions</span></span>

<span data-ttu-id="6c05c-112">Patikrinusi pateiktą dokumentą sistema nustato, kurią šaką naudoti, ir nustato, ar ji atitinka konkrečias sąlygas.</span><span class="sxs-lookup"><span data-stu-id="6c05c-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>

1. <span data-ttu-id="6c05c-113">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6c05c-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="6c05c-114">Spustelėkite **Įtraukti sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="6c05c-114">Click **Add condition**.</span></span>
3. <span data-ttu-id="6c05c-115">Įveskite sąlygą</span><span class="sxs-lookup"><span data-stu-id="6c05c-115">Enter a condition.</span></span>
4. <span data-ttu-id="6c05c-116">Įveskite papildomas sąlygas, jei jos reikalingos.</span><span class="sxs-lookup"><span data-stu-id="6c05c-116">Enter additional conditions, if they are required.</span></span>
5. <span data-ttu-id="6c05c-117">Norėdami patikrinti, kad sąlygos, kurias įvedėte yra sukonfigūruotos teisingai, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6c05c-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="6c05c-118">Spustelėkite **Tikrinti**, norėdami atidaryti formą **Tikrinti darbo eigos sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="6c05c-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="6c05c-119">Formos srityje **Tikrinti sąlygą** pasirinkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="6c05c-119">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="6c05c-120">Spustelėkite **Išbandyti**.</span><span class="sxs-lookup"><span data-stu-id="6c05c-120">Click **Test**.</span></span> <span data-ttu-id="6c05c-121">Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="6c05c-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="6c05c-122">Spustelėkite **Gerai** arba **Atšaukti**, norėdami vėl atidaryti formą **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="6c05c-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>
