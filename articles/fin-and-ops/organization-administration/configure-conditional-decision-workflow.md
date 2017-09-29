---
title: "Sąlyginio darbo eigos sprendimo konfigūravimas"
description: "Naudokite šią procedūrą, norėdami konfigūruoti sąlyginio sprendimo ypatybes."
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
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: e9d5c8add546cad0446e863f64cac8f9cb603cbb
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a><span data-ttu-id="dd6a1-103">Sąlyginio darbo eigos sprendimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="dd6a1-103">Configure a conditional decision in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="dd6a1-104">Naudokite šią procedūrą, norėdami konfigūruoti sąlyginio sprendimo ypatybes.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="dd6a1-105">Sąlyginis sprendimas – tai taškas, kuriame darbo eiga padalijama į dvi šakas.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="dd6a1-106">Norėdami darbo eigos rengyklėje konfigūruoti sąlyginį sprendimą, dešiniuoju pelės mygtuku spustelėkite sąlyginį sprendimą ir tada spustelėkite **Ypatybės**, kad atidarytumėte formą **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="dd6a1-107">Sprendimo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="dd6a1-107">Name a decision</span></span>
<span data-ttu-id="dd6a1-108">Norėdami įvesti sąlyginio sprendimo pavadinimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-108">Follow these steps to enter a name for a conditional decision.</span></span>
1.  <span data-ttu-id="dd6a1-109">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="dd6a1-110">Lauke **Pavadinimas** įveskite unikalų sąlyginio sprendimo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="dd6a1-111"> Sąlygų nustatymas</span><span class="sxs-lookup"><span data-stu-id="dd6a1-111">Set conditions</span></span>
<span data-ttu-id="dd6a1-112">Patikrinusi pateiktą dokumentą sistema nustato, kurią šaką naudoti, ir nustato, ar ji atitinka konkrečias sąlygas.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>
1.  <span data-ttu-id="dd6a1-113">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="dd6a1-114">Spustelėkite **Įtraukti sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-114">Click **Add condition**.</span></span>
3.  <span data-ttu-id="dd6a1-115">Įveskite sąlygą</span><span class="sxs-lookup"><span data-stu-id="dd6a1-115">Enter a condition.</span></span>
4.  <span data-ttu-id="dd6a1-116">Įveskite papildomas sąlygas, jei jos reikalingos.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-116">Enter additional conditions, if they are required.</span></span>
5.  <span data-ttu-id="dd6a1-117">Norėdami patikrinti, kad sąlygos, kurias įvedėte yra sukonfigūruotos teisingai, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="dd6a1-118">Spustelėkite **Tikrinti**, norėdami atidaryti formą **Tikrinti darbo eigos sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="dd6a1-119">Formos srityje **Tikrinti sąlygą** pasirinkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-119">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="dd6a1-120">Spustelėkite **Išbandyti**.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-120">Click **Test**.</span></span> <span data-ttu-id="dd6a1-121">Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="dd6a1-122">Spustelėkite **Gerai** arba **Atšaukti**, norėdami vėl atidaryti formą **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="dd6a1-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>






