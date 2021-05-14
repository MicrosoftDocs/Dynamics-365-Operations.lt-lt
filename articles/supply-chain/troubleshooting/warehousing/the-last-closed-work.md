---
title: Paskutinė uždaryto darbo eilutė turi būti padėta
description: Paskutinė uždaryto darbo eilutė turi būti padėta
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924380"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="03d42-103">Paskutinė uždaryto darbo eilutė turi būti padėta</span><span class="sxs-lookup"><span data-stu-id="03d42-103">The last closed work line must be a put</span></span>

<span data-ttu-id="03d42-104">Klaidos kodas: WAX1285</span><span class="sxs-lookup"><span data-stu-id="03d42-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="03d42-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="03d42-105">Symptoms</span></span>

<span data-ttu-id="03d42-106">Sistema rodo tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="03d42-106">The system shows the following error message:</span></span>

> <span data-ttu-id="03d42-107">Paskutinė uždaryto darbo eilutė turi būti padėta.</span><span class="sxs-lookup"><span data-stu-id="03d42-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="03d42-108">Priežastis</span><span class="sxs-lookup"><span data-stu-id="03d42-108">Cause</span></span>

<span data-ttu-id="03d42-109">Dabartinės darbo būsenos atšaukti negalima.</span><span class="sxs-lookup"><span data-stu-id="03d42-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="03d42-110">Paskutinėje darbo eilutėje laukas Darbo būsena nustatytas kaip Uždaryta, **bet laukas** Darbo *tipas* nėra **nustatytas** kaip *Padėti*.</span><span class="sxs-lookup"><span data-stu-id="03d42-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="03d42-111">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="03d42-111">Resolution</span></span>

<span data-ttu-id="03d42-112">Norėdami atšaukti darbą atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="03d42-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="03d42-113">Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="03d42-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="03d42-114">Lauke **Darbo ID** nurodykite darbo, kurį norite atšaukti, ID.</span><span class="sxs-lookup"><span data-stu-id="03d42-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="03d42-115">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="03d42-115">Select **OK**.</span></span>
1. <span data-ttu-id="03d42-116">Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.</span><span class="sxs-lookup"><span data-stu-id="03d42-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="03d42-117">Dėl platesnės informacijos, žr. [Darbo sandėlyje atšaukimas dėl išimčių tvarkymo](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="03d42-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
