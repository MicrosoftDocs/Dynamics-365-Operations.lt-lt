---
title: Prekių kainų puslapio skirtuke Aktyvios kainos nėra vertės Nuo datos
description: Prekių kainų puslapio skirtuke Aktyvios kainos nėra vertės Nuo datos.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026760"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="47435-103">Prekių kainų puslapio skirtuke Aktyvios kainos nėra vertės Nuo datos</span><span class="sxs-lookup"><span data-stu-id="47435-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="47435-104">KB numeris: 4613548</span><span class="sxs-lookup"><span data-stu-id="47435-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="47435-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="47435-105">Symptoms</span></span>

<span data-ttu-id="47435-106">Nėra jokios **Nuo datos** vertės **Aktyvios kainos** skirtuke **Prekių kaina** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="47435-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="47435-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="47435-107">Resolution</span></span>

<span data-ttu-id="47435-108">Datos **Nuo vertės** (galiojimo data), kuri nustatyta laukiančią kainą, nepervesta į aktyvią kainą.</span><span class="sxs-lookup"><span data-stu-id="47435-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="47435-109">Kai pirmą kartą įvedamas prekės išlaidų įrašas, jo būsena yra *Laukiantis* ir jis turi numatomą įsigaliojimo datą.</span><span class="sxs-lookup"><span data-stu-id="47435-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="47435-110">Kai prekės išlaidų įrašą suaktyvinate, būsena atnaujinama į *Aktyvus*, o įsigaliojimo data atnaujinama į aktyvavimo datą.</span><span class="sxs-lookup"><span data-stu-id="47435-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="47435-111">Todėl aktyvios kainos aktyvinimo data visada yra faktinė aktyvinimo data.</span><span class="sxs-lookup"><span data-stu-id="47435-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="47435-112">Daugiau informacijos rasite [Kaštų versijos apžvalga](../../cost-management/costing-versions.md).</span><span class="sxs-lookup"><span data-stu-id="47435-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
