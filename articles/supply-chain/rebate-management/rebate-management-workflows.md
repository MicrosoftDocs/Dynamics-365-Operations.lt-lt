---
title: Grąžinimų valdymo sandorio darbo eigos
description: Šioje temoje paaiškinama, kaip nustatyti grąžinimo valdymo sandorio darbo eigą, skirtą sandorių patvirtinimui ir aktyvavimui.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020392"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="a0ba6-103">Grąžinimų valdymo sandorio darbo eigos</span><span class="sxs-lookup"><span data-stu-id="a0ba6-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0ba6-104">Grąžinimo sandorių patvirtinimams grąžinimų valdymas naudoja tą pačią darbo eigos platformą kaip ir kitos „Finance and Operations” programos.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="a0ba6-105">Su kiekviena darbo eiga yra susieti du užduočių procesai:</span><span class="sxs-lookup"><span data-stu-id="a0ba6-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="a0ba6-106">Vienas darbo eigos elementas suaktyvina sandorį tam, kad vartotojas arba darbo eigos procesas galėtų patvirtinti operacijas.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="a0ba6-107">Kitas darbo eigos elementas patvirtina sandorį.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="a0ba6-108">Kad būtų galima naudoti grąžinimo sandorį, jis turi būti aktyvus **Grąžinimų valdymo** modulyje.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="a0ba6-109">Norėdami aktyvuoti sandorį, pirmiausia turite sukurti ir sukonfigūruoti *Grąžinimų valdymo sandorio darbo eigą*.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="a0ba6-110">Kai grąžinimų valdymui suaktyvinama darbo eiga, vartotojai negali rankiniu būdu patvirtinti sandorių.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="a0ba6-111">Visada turi būti naudojama darbo eiga.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="a0ba6-112">Grąžinimų valdymo sandorio darbo eigų kūrimas ir valdymas</span><span class="sxs-lookup"><span data-stu-id="a0ba6-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="a0ba6-113">Norėdami dirbti su savo grąžinimų valdymo sandorio darbo eigomis, eikite į **Grąžinimo valdymas \> Nustatymas \> Grąžinimų valdymo darbo eigos**.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="a0ba6-114">Ten galite peržiūrėti, kurti ir atnaujinti darbo eigas taip, kaip jums reikia.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="a0ba6-115">Tik viena šio tipo darbo eiga gali būti aktyvi tuo pačiu metu.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="a0ba6-116">Daugiau informacijos apie darbo eigas, kaip dirbti su **Grąžinimo darbo eigų** puslapių ir kaip kurti darbo eigas, rasite [Darbo eigos sistemos apžvalga](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) ir su ja susijusiose temose.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="a0ba6-117">Sandorio aktyvavimas naudojant darbo eigą</span><span class="sxs-lookup"><span data-stu-id="a0ba6-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="a0ba6-118">Norėdami aktyvuoti sandorį naudodami darbo eigą, atidarykite sandorį (pavyzdžiui, **Visų grąžinimų valdymo sandorių** puslapyje).</span><span class="sxs-lookup"><span data-stu-id="a0ba6-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="a0ba6-119">Tada veiksmų srityje pasirinkite **Darbo eiga \> Pateikti**.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="a0ba6-120">Kai naujas sandoris bus apdorotas ir patvirtintas per darbo eigą, jis bus aktyvus ir parengtas naudoti.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="a0ba6-121">Aktyvavę sandorį negalite pakeisti jo nustatymo.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="a0ba6-122">Jeigu reikia pakeisti aktyvų sandorį, padarykite jį neaktyvų ir tada sukurkite naują sandorį.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="a0ba6-123">Jei naujas sandoris bus panašus į senąjį, galite sukurti jį nukopijuodami seną sandorį.</span><span class="sxs-lookup"><span data-stu-id="a0ba6-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
