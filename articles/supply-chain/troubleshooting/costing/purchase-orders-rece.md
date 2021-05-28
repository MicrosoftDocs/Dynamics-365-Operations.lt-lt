---
title: Faktiškai gauti pirkimo užsakymai atsargų uždarymo ataskaitoje nerodomi
description: Faktiškai gauti pirkimo užsakymai atvirų kiekių tikrinimo atsargų uždarymo ataskaitoje nerodomi.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026745"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a><span data-ttu-id="ca67a-103">Faktiškai gauti pirkimo užsakymai atsargų uždarymo ataskaitoje nerodomi</span><span class="sxs-lookup"><span data-stu-id="ca67a-103">Physically received purchase orders don't appear on the inventory closing report</span></span>

<span data-ttu-id="ca67a-104">KB numeris: 4612595</span><span class="sxs-lookup"><span data-stu-id="ca67a-104">KB number: 4612595</span></span>

## <a name="symptoms"></a><span data-ttu-id="ca67a-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="ca67a-105">Symptoms</span></span>

<span data-ttu-id="ca67a-106">Faktiškai gauti pirkimo užsakymai atvirų kiekių tikrinimo **atsargų uždarymo ataskaitoje** nerodomi.</span><span class="sxs-lookup"><span data-stu-id="ca67a-106">Physically received purchase orders don't appear on the **Check open quantities** inventory closing report.</span></span>

## <a name="resolution"></a><span data-ttu-id="ca67a-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="ca67a-107">Resolution</span></span>

<span data-ttu-id="ca67a-108">Atvirų **kiekių tikrinimo ataskaitoje** rodomos išdavimo operacijos, kurių negalima sudengti su finansiškai atnaujintu atsargų gavimu pasirinktą uždarymo datą.</span><span class="sxs-lookup"><span data-stu-id="ca67a-108">The **Check open quantities** report shows issue transactions that can't be settled against financially updated inventory receipts as of the selected closing date.</span></span> <span data-ttu-id="ca67a-109">Galite pasirinkti į ataskaitą įtraukti faktinius gavimus.</span><span class="sxs-lookup"><span data-stu-id="ca67a-109">You can choose to include physical receipts on the report.</span></span> <span data-ttu-id="ca67a-110">Tokiu atveju faktiniai gavime bus rodomi, jei jie gali padengti išdavimo operacijas, kurių negalima sudengti.</span><span class="sxs-lookup"><span data-stu-id="ca67a-110">In that case, physical receipts will be shown if they can cover the issue transactions that can't be settled.</span></span> <span data-ttu-id="ca67a-111">Dėl daugiau informacijos, žr. [Parengimas vykdyti atsargų uždarymą](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span><span class="sxs-lookup"><span data-stu-id="ca67a-111">For more information, see [Preparing to run inventory close](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span></span>
