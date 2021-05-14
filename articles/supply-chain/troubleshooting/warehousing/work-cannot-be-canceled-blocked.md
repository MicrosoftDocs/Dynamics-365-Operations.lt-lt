---
title: Darbo atšaukti negalima dėl to, kad jis užblokuotas
description: Darbo atšaukti negalima dėl to, kad jis užblokuotas
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924284"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="f582d-103">Darbo atšaukti negalima dėl to, kad jis užblokuotas</span><span class="sxs-lookup"><span data-stu-id="f582d-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="f582d-104">Klaidos kodas: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="f582d-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="f582d-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="f582d-105">Symptoms</span></span>

<span data-ttu-id="f582d-106">Sistema rodo tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="f582d-106">The system shows the following error message:</span></span>

> <span data-ttu-id="f582d-107">Darbo %1atšaukti negalima, nes jį užblokavo priežasties %2 tipas.</span><span class="sxs-lookup"><span data-stu-id="f582d-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="f582d-108">Darbas turi būti atblokuotas prieš jo atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="f582d-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="f582d-109">Priežastis</span><span class="sxs-lookup"><span data-stu-id="f582d-109">Cause</span></span>

<span data-ttu-id="f582d-110">Darbą užblokuoja vartotojas ir jo atšaukti negalima.</span><span class="sxs-lookup"><span data-stu-id="f582d-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="f582d-111">Skirtuko **Bendra** puslapyje Darbas **nustatyta** **parinktis** Užblokuota kaip *Taip*.</span><span class="sxs-lookup"><span data-stu-id="f582d-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="f582d-112">Šis parametras nurodo, kad darbas užblokuotas.</span><span class="sxs-lookup"><span data-stu-id="f582d-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="f582d-113">Blokavimo **priežasčių** skirtukas rodo, kodėl darbas buvo užblokuotas.</span><span class="sxs-lookup"><span data-stu-id="f582d-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="f582d-114">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="f582d-114">Resolution</span></span>

<span data-ttu-id="f582d-115">Norėdami atblokuoti darbą, pasirinkite **blokavimo priežasčių** skirtuką ir atlikite vieną iš šių veiksmų:</span><span class="sxs-lookup"><span data-stu-id="f582d-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="f582d-116">Jei **darbo blokavimo priežasties** laukelis yra nustatytas į *Neapibrėžta priežastis*: Veiksmų srities skirtuko **Darbas** skirtuke, **Darbas** grupėje rinkitės **Atblokuoti darbą**.</span><span class="sxs-lookup"><span data-stu-id="f582d-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="f582d-117">Jei **Darbo blokavimo priežasties** laukelis yra nustatytas į *Apdorojimo banga*: Veiksmų juostoje **Susijusi informacija** skirtuke **Susijusi informacija** grupėje rinkitės **Banga**.</span><span class="sxs-lookup"><span data-stu-id="f582d-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="f582d-118">Tada, **bangos** puslapyje veiksmų juostoje **Bangos** skirtuke, **Bangos** grupėje rinkitės **Išvalyti bangos duomenis**.</span><span class="sxs-lookup"><span data-stu-id="f582d-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="f582d-119">Apėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="f582d-119">Workaround</span></span>

<span data-ttu-id="f582d-120">Jei ankstesni veiksmai neištaisė problemos, galite atšaukti darbą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f582d-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="f582d-121">Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="f582d-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="f582d-122">Laukelyje **Darbo ID** nurodykite darbo ID, kurį norite atšaukti ir tai, kad dabar **Darbo būsenos** vertė *Atidaryta*, *Vykdoma*, *Atšaukta*, *Kombinuota* ar *Uždaryta*.</span><span class="sxs-lookup"><span data-stu-id="f582d-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="f582d-123">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f582d-123">Select **OK**.</span></span>
1. <span data-ttu-id="f582d-124">Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.</span><span class="sxs-lookup"><span data-stu-id="f582d-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="f582d-125">Dėl platesnės informacijos, žr. [Darbo sandėlyje atšaukimas dėl išimčių tvarkymo](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="f582d-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
