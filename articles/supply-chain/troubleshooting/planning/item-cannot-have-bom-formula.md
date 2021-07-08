---
title: Prekė negali turėti KS arba formulės
description: Kai bandote patvirtinti užsakymą, prekės patikrinimo metu gaunate klaidos pranešimą. Jame teigiama, kad prekė negali turėti komplektavimo specifikacijos (KS) ar formulės.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294137"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="7fc34-104">Prekė negali turėti KS arba formulės</span><span class="sxs-lookup"><span data-stu-id="7fc34-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="7fc34-105">Klaidos kodas: PRO2614</span><span class="sxs-lookup"><span data-stu-id="7fc34-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="7fc34-106">Požymiai</span><span class="sxs-lookup"><span data-stu-id="7fc34-106">Symptoms</span></span>

<span data-ttu-id="7fc34-107">Kai bandote patvirtinti užsakymą, prekės patikrinimo metu gaunate tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="7fc34-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="7fc34-108">Prekė negali turėti KS arba formulės</span><span class="sxs-lookup"><span data-stu-id="7fc34-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="7fc34-109">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="7fc34-109">Resolution</span></span>

<span data-ttu-id="7fc34-110">Prekės, kurios turi komplektavimo specifikaciją (KS) arba formulę, privalo būti *Planavimo prekės*, *KS* arba *formulės* tipo.</span><span class="sxs-lookup"><span data-stu-id="7fc34-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="7fc34-111">Norėdami pakeisti prekės tipą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7fc34-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="7fc34-112">Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="7fc34-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="7fc34-113">Atidarykite atitinkamą produktą.</span><span class="sxs-lookup"><span data-stu-id="7fc34-113">Open the relevant product.</span></span>
1. <span data-ttu-id="7fc34-114">„FastTab“ **Inžinierius** nustatykite lauką **Produkto tipas** į *Planavimo prekė*, *KS* arba *formulė*.</span><span class="sxs-lookup"><span data-stu-id="7fc34-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>
