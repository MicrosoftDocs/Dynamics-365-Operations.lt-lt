---
title: Pasirinktas formulės numeris nėra patvirtintas paketiniam užsakymui
description: Kai bandote patvirtinti suplanuotą užsakymą, gaunate klaidos pranešimą, kuriame teigiama, kad pasirinktas formulės numeris nėra patvirtintas paketiniam užsakymui.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294133"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="14cbe-103">Pasirinktas formulės numeris nėra patvirtintas paketiniam užsakymui</span><span class="sxs-lookup"><span data-stu-id="14cbe-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="14cbe-104">Klaidos kodas: PRO2614</span><span class="sxs-lookup"><span data-stu-id="14cbe-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="14cbe-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="14cbe-105">Symptoms</span></span>

<span data-ttu-id="14cbe-106">Kai bandote patvirtinti suplanuotą užsakymą, gaunate tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="14cbe-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="14cbe-107">Pasirinktas formulės numeris nėra patvirtintas naudoti paketiniam užsakymui.</span><span class="sxs-lookup"><span data-stu-id="14cbe-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="14cbe-108">Priežastis</span><span class="sxs-lookup"><span data-stu-id="14cbe-108">Cause</span></span>

<span data-ttu-id="14cbe-109">Sistema patikrina patvirtinimo operaciją, kad įsitikintų, jog aktyviai prekei galima patvirtinta formulė.</span><span class="sxs-lookup"><span data-stu-id="14cbe-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="14cbe-110">Tikriausiai turite patvirtinti formulę.</span><span class="sxs-lookup"><span data-stu-id="14cbe-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="14cbe-111">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="14cbe-111">Resolution</span></span>

<span data-ttu-id="14cbe-112">Norėdami patvirtinti formulę, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="14cbe-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="14cbe-113">Eikite į **Produkto informacijos valdymas \> Komplektavimo specifikacijos ir formulės \> Formulės**.</span><span class="sxs-lookup"><span data-stu-id="14cbe-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="14cbe-114">Pasirinkite reikalingą formulę.</span><span class="sxs-lookup"><span data-stu-id="14cbe-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="14cbe-115">Veiksmų srities skirtuke **Formulė**, grupėje **Prižiūrėti** pasirinkite **Patvirtinti formulę**.</span><span class="sxs-lookup"><span data-stu-id="14cbe-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="14cbe-116">Dialogo lange **Patvirtinti KS arba formulę** pasirinkite tai, ką reikia patvirtinti ir **GERAI**.</span><span class="sxs-lookup"><span data-stu-id="14cbe-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>
