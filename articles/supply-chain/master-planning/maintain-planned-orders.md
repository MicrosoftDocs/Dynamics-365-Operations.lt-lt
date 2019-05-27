---
title: Suplanuotų užsakymų tvarkymas
description: Šioje temoje pateikiama informacija apie tai, kaip valdyti suplanuotus užsakymus. Jame aprašoma, kaip galite atnaujinti suplanuotų užsakymų būseną, juos patvirtinti ir filtruoti suplanuotus užsakymus, kurių būsena tokia pati, kaip pasirinkto suplanuoto užsakymo.
author: roxanadiaconu
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf578d98abc4825c5607ec031da6ab6737c3183a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560377"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="22359-104">Suplanuotų užsakymų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="22359-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22359-105">Šioje temoje pateikiama informacija apie tai, kaip valdyti suplanuotus užsakymus.</span><span class="sxs-lookup"><span data-stu-id="22359-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="22359-106">Jame aprašoma, kaip galite atnaujinti suplanuotų užsakymų būseną, juos patvirtinti ir filtruoti suplanuotus užsakymus, kurių būsena tokia pati, kaip pasirinkto suplanuoto užsakymo.</span><span class="sxs-lookup"><span data-stu-id="22359-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="22359-107">Suplanuotus užsakymus galite valdyti naudodami darbo sritį **Bendrasis planavimas**, sąrašą **Suplanuoti užsakymai** arba sąrašus **Suplanuoti gamybos užsakymai**, **Suplanuoti pirkimo užsakymai** ir **Suplanuotas perkėlimas**.</span><span class="sxs-lookup"><span data-stu-id="22359-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="22359-108">Galite naudoti lauką **Būsena** progresui sekti.</span><span class="sxs-lookup"><span data-stu-id="22359-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="22359-109">Naudojamos toliau nurodytos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="22359-109">The following values are used:</span></span>

-   <span data-ttu-id="22359-110">Kai bendrasis planavimas sugeneruoja suplanuotus užsakymus, suplanuotų užsakymų būsena yra **Neapdorota**.</span><span class="sxs-lookup"><span data-stu-id="22359-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="22359-111">Jei nenorite patvirtinti suplanuoto užsakymo, galite jam nustatyti būseną **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="22359-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="22359-112">Jei norite patvirtinti suplanuotą užsakymą, galite jam nustatyti būseną **Patvirtinta**.</span><span class="sxs-lookup"><span data-stu-id="22359-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="22359-113">Būsena nurodo, kad pritariate suplanuoto užsakymo patvirtinimui, bet jis dar nėra patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="22359-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="22359-114">**Pastaba:** esamos būsenos patvirtintas suplanuotas užsakymas perkeliamas į kitą pagrindinio planavimo skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="22359-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="22359-115">Galite tvirtinti suplanuotus užsakymus spustelėdami **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="22359-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="22359-116">Galite tvirtinti šiuos suplanuotus užsakymus:</span><span class="sxs-lookup"><span data-stu-id="22359-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="22359-117">Pasirinktas suplanuotas užsakymas.</span><span class="sxs-lookup"><span data-stu-id="22359-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="22359-118">Keli suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="22359-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="22359-119">Suplanuoti užsakymai, sugeneruoti išskleidžiant juos puslapyje **Išskleidimas**.</span><span class="sxs-lookup"><span data-stu-id="22359-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="22359-120">Spustelėkite **Suplanuoti užsakymai**, pasirinkite suplanuotą užsakymą ir spustelėkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="22359-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="22359-121">Kai suplanuotas užsakymas patvirtinamas, jis perkeliamas į atitinkamo modulio užsakymų dalį.</span><span class="sxs-lookup"><span data-stu-id="22359-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> 

<a name="additional-resources"></a><span data-ttu-id="22359-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="22359-122">Additional resources</span></span>
--------

[<span data-ttu-id="22359-123">Bendrieji planai</span><span class="sxs-lookup"><span data-stu-id="22359-123">Master plans</span></span>](master-plans.md)



