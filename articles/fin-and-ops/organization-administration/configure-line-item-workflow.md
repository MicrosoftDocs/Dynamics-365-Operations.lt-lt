---
title: "Eilutės elemento darbo eigos konfigūravimas"
description: "Šioje temoje paaiškinta, kaip konfigūruoti eilutės elemento darbo eigos elementą."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 658829ccb79d0b2b4f627a45647ba6076e4384b0
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="configure-a-line-item-workflow"></a><span data-ttu-id="ef18e-103">Eilutės elemento darbo eigos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ef18e-103">Configure a line-item workflow</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ef18e-104">Šioje temoje paaiškinta, kaip konfigūruoti eilutės elemento darbo eigos elementą.</span><span class="sxs-lookup"><span data-stu-id="ef18e-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="ef18e-105">Norėdami darbo eigos rengyklėje konfigūruoti eilutės elemento darbo eigą, dešiniuoju pelės mygtuku spustelėkite elementą ir tada spustelėkite **Ypatybės**, kad atidarytumėte puslapį **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="ef18e-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="ef18e-106">Tada naudokite šias procedūras norėdami konfigūruoti eilutės elemento darbo eigos elementą.</span><span class="sxs-lookup"><span data-stu-id="ef18e-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="ef18e-107">Eilutės elemento darbo eigos elemento pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ef18e-107">Name the line-item workflow element</span></span>
<span data-ttu-id="ef18e-108">Norėdami įvesti eilutės elemento darbo eigos elemento pavadinimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ef18e-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1.  <span data-ttu-id="ef18e-109">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ef18e-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="ef18e-110">Lauke **Pavadinimas** įveskite unikalų eilutės elemento darbo eigos elemento pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ef18e-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="ef18e-111">Nurodykite, ar tą pačią darbo eigą reikia naudoti visiems elementams apdoroti</span><span class="sxs-lookup"><span data-stu-id="ef18e-111">Specify whether the same workflow is used to process all line items</span></span>
<span data-ttu-id="ef18e-112">Atlikite šiuos veiksmus, norėdami nurodyti, ar tą pačią darbo eigą reikia naudoti visiems dokumento elementams apdoroti.</span><span class="sxs-lookup"><span data-stu-id="ef18e-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1.  <span data-ttu-id="ef18e-113">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ef18e-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="ef18e-114">Jei tą pačią darbo eigą reikia naudoti visiems dokumento elementams apdoroti, spustelėkite **Iškviesti vieną visų eilutės elementų darbo eigą**.</span><span class="sxs-lookup"><span data-stu-id="ef18e-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="ef18e-115">Tada pasirinkite darbo eigą, kurią naudojant bus apdorojami eilutės elementai.</span><span class="sxs-lookup"><span data-stu-id="ef18e-115">Then select the workflow to use to process the line items.</span></span>
3.  <span data-ttu-id="ef18e-116">Jei konkrečią darbo eigą reikia naudoti norint apdoroti elementus, kurie atitinka konkretaus rinkinio sąlygas, spustelėkite **Iškviesti atskirą kiekvienam eilutės elementui darbo eigą**.</span><span class="sxs-lookup"><span data-stu-id="ef18e-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="ef18e-117">Tada, norėdami nurodyti sąlygų rinkinį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ef18e-117">Then follow these steps to define the set of conditions:</span></span>
    1.  <span data-ttu-id="ef18e-118">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="ef18e-118">Click **Add**.</span></span>
    2.  <span data-ttu-id="ef18e-119">Lentelėje pasirinkite sąlygą.</span><span class="sxs-lookup"><span data-stu-id="ef18e-119">Select the condition in the table.</span></span>
    3.  <span data-ttu-id="ef18e-120">Skirtuke **Sąlygos pavadinimas** įveskite nustatomo sąlygų rinkinio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ef18e-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4.  <span data-ttu-id="ef18e-121">Norėdami įvesti sąlygą, spustelėkite **Įtraukti sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="ef18e-121">Click **Add condition** to enter a condition.</span></span>
    5.  <span data-ttu-id="ef18e-122">Įveskite visas reikalingas papildomas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="ef18e-122">Enter any additional conditions that are required.</span></span>
    6.  <span data-ttu-id="ef18e-123">Norėdami patikrinti, ar įvestas sąlygų rinkinys yra sukonfigūruotas teisingai, spustelėkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="ef18e-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="ef18e-124">Puslapio **Tikrinti darbo eigos sąlygą** srityje **Tikrinti sąlygą** pasirinkite įrašą, o tada spustelėkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="ef18e-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="ef18e-125">Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="ef18e-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="ef18e-126">Spustelėkite **Gerai** arba **Atšaukti**, kad grįžtumėte į puslapį **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="ef18e-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="ef18e-127">Skirtuke **Darbo eiga** pasirinkite darbo eigą, kurią naudojant bus apdorojami eilutės elementai, atitinkantys jūsų nurodytą sąlygų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="ef18e-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>





