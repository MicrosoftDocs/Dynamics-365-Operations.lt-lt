---
title: Negalima atnaujinti prognozuojamų vieneto išlaidų importuojant poreikio prognozės įrašus
description: Kai duomenų objektus naudojate poreikio prognozės įrašams importuoti, esamų įrašų savikaina nėra atnaujinama taip, kad atitiktų importuotus duomenis.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026749"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="1a2e0-103">Negalima atnaujinti prognozuojamų vieneto išlaidų importuojant poreikio prognozės įrašus</span><span class="sxs-lookup"><span data-stu-id="1a2e0-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="1a2e0-104">KB numeris: 4614109</span><span class="sxs-lookup"><span data-stu-id="1a2e0-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="1a2e0-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="1a2e0-105">Symptoms</span></span>

<span data-ttu-id="1a2e0-106">Kai duomenų objektus naudojate poreikio prognozės įrašams importuoti, **Prognozuojamo vieneto kaštų** savikaina nėra atnaujinama taip, kad atitiktų importuotus duomenis.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="1a2e0-107">Priežastis</span><span class="sxs-lookup"><span data-stu-id="1a2e0-107">Cause</span></span>

<span data-ttu-id="1a2e0-108">**Prognozuojamos vieneto išlaidos** yra tik skaitomas laukas.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="1a2e0-109">Vertė priklauso nuo produkto vieneto savikainos ir jos negalima tiesiogiai nustatyti importuojant.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="1a2e0-110">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="1a2e0-110">Resolution</span></span>

<span data-ttu-id="1a2e0-111">Kadangi laukas yra tik skaitomas, jo verčių importuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="1a2e0-112">Vertė bus apskaičiuota pagal esamą verslo logiką.</span><span class="sxs-lookup"><span data-stu-id="1a2e0-112">The value will be calculated according to the existing business logic.</span></span>
