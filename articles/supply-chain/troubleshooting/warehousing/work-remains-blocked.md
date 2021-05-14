---
title: Darbo lieka užblokuotas
description: Darbo lieka užblokuotas
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924135"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="ce5d1-103">Darbo lieka užblokuotas</span><span class="sxs-lookup"><span data-stu-id="ce5d1-103">Work remains blocked</span></span>

<span data-ttu-id="ce5d1-104">Klaidos kodas: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="ce5d1-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="ce5d1-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="ce5d1-105">Symptoms</span></span>

<span data-ttu-id="ce5d1-106">Sistema rodo tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="ce5d1-106">The system shows the following error message:</span></span>

> <span data-ttu-id="ce5d1-107">Darbas %1 lieka užblokuotas, nes susijusios bangos %2 būsena yra %3.</span><span class="sxs-lookup"><span data-stu-id="ce5d1-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="ce5d1-108">Priežastis</span><span class="sxs-lookup"><span data-stu-id="ce5d1-108">Cause</span></span>

<span data-ttu-id="ce5d1-109">Darbas šiuo metu apdorojamas bangoje ir jo negalima atblokuoti, kaip nurodyta vienoje iš šių sąlygų:</span><span class="sxs-lookup"><span data-stu-id="ce5d1-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="ce5d1-110">Blokavimo priežasčių skirtuke vienos ar daugiau eilučių darbo blokavimo priežasties laukas **nustatytas** į **Apdorojama** *bangą*.</span><span class="sxs-lookup"><span data-stu-id="ce5d1-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="ce5d1-111">Jums pasirinkus **Bangą** grupėje **Susijusi informacija** skirtuke **susijusi informacija** veiksmų juostoje, **Bangos būsenos** laukelis nustatytas *Apdorojimas*.</span><span class="sxs-lookup"><span data-stu-id="ce5d1-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="ce5d1-112">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="ce5d1-112">Resolution</span></span>

<span data-ttu-id="ce5d1-113">Veiksmų srities skirtuko **Susijusi informacija** grupėje **Susijusi informacija** pasirinkite **Banga**.</span><span class="sxs-lookup"><span data-stu-id="ce5d1-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="ce5d1-114">Tada, **bangos** puslapyje veiksmų juostoje **Bangos** skirtuke, **Bangos** grupėje rinkitės **Išvalyti bangos duomenis**.</span><span class="sxs-lookup"><span data-stu-id="ce5d1-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="ce5d1-115">Apėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="ce5d1-115">Workaround</span></span>

<span data-ttu-id="ce5d1-116">Jei ankstesni veiksmai neištaisė problemos, galite atšaukti darbą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce5d1-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="ce5d1-117">Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="ce5d1-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="ce5d1-118">Laukelyje **Darbo ID** nurodykite darbo ID, kurį norite atšaukti ir tai, kad dabar **Darbo būsenos** vertė *Atidaryta*, *Vykdoma*, *Atšaukta*, *Kombinuota* ar *Uždaryta*.</span><span class="sxs-lookup"><span data-stu-id="ce5d1-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="ce5d1-119">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ce5d1-119">Select **OK**.</span></span>
1. <span data-ttu-id="ce5d1-120">Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.</span><span class="sxs-lookup"><span data-stu-id="ce5d1-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="ce5d1-121">Dėl platesnės informacijos, žr. [Darbo sandėlyje atšaukimas dėl išimčių tvarkymo](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="ce5d1-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
