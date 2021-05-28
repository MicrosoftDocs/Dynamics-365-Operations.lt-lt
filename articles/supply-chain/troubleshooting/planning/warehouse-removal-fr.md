---
title: Negalima pašalinti sandėlio poreikio prognozės dimensijos iš prognozės eilučių
description: Negalima pašalinti sandėlio poreikio prognozės dimensijos iš prognozės eilučių.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026748"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="b3091-103">Negalima pašalinti sandėlio poreikio prognozės dimensijos iš prognozės eilučių</span><span class="sxs-lookup"><span data-stu-id="b3091-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="b3091-104">KB numeris: 4614408</span><span class="sxs-lookup"><span data-stu-id="b3091-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="b3091-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="b3091-105">Symptoms</span></span>

<span data-ttu-id="b3091-106">Ši problema kyla, kai **sandėlio** dimensija nėra priskirta **poreikio prognozės** parametrų puslapio skirtuke **Prognozės dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="b3091-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="b3091-107">Nepaisant to, **Sandėlio** stulpelis yra rodomas **Poreikio prognozės** puslapyje (**Bendrojo planavimo \> prognozės \> Rankinio prognozės objekto \> Poreikio prognozės eilutėse**).</span><span class="sxs-lookup"><span data-stu-id="b3091-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="b3091-108">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="b3091-108">Resolution</span></span>

<span data-ttu-id="b3091-109">Nustatymai **Poreikio prognozės** skirtuke **Prognozės dimensijos parametrai** puslapyje neveikia **Poreikio prognozės** puslapio.</span><span class="sxs-lookup"><span data-stu-id="b3091-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="b3091-110">Jie kontroliuoja bazinę prognozę, kuri yra generuojama ir rodoma pakoreguotoje poreikio prognozėje.</span><span class="sxs-lookup"><span data-stu-id="b3091-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="b3091-111">Tačiau jie nekontroliuoja dimensijų, kurių reikia „tikrai" poreikio prognozei.</span><span class="sxs-lookup"><span data-stu-id="b3091-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="b3091-112">Autorizdami įrašus, kurie rodomi puslapyje **Pakoreguota poreikio prognozė** galite juos konvertuoti į realius prognozės įrašus prognozės modeliui.</span><span class="sxs-lookup"><span data-stu-id="b3091-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="b3091-113">Tada tą modelį galima naudoti bendrojo planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="b3091-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="b3091-114">Poreikio prognozės puslapyje, **poreikio prognozės** dimensijos, rodomos poreikio prognozės eilutėse, yra atsargų dimensijų dalis.</span><span class="sxs-lookup"><span data-stu-id="b3091-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="b3091-115">(Taip panaši į pardavimo užsakymo eilučių elgseną.) Jei jūsų sistema nėra nustatyta naudoti sandėlio kaip privalomos atsargų dimensijos, galite pritaikyti puslapį, kad **paslėptumėte** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="b3091-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
