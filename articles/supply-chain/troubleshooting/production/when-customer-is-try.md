---
title: Pasirinkus naują partijos ID paketo numeris išvalomas
description: Peržiūrint išrinkimo dokumento žurnalo eilutę, lauke Paketo numeris vertė išvaloma, jei lauke Partijos numeris pasirenkate naują vertę.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026730"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a><span data-ttu-id="e1469-103">Pasirinkus naują partijos ID paketo numeris išvalomas</span><span class="sxs-lookup"><span data-stu-id="e1469-103">Batch number is cleared when a new lot ID is selected</span></span>

<span data-ttu-id="e1469-104">KB numeris: 4613107</span><span class="sxs-lookup"><span data-stu-id="e1469-104">KB number: 4613107</span></span>

## <a name="symptoms"></a><span data-ttu-id="e1469-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="e1469-105">Symptoms</span></span>

<span data-ttu-id="e1469-106">Peržiūrint išrinkimo dokumento žurnalo eilutę, lauke **Paketo numeris** vertė išvaloma, jei lauke **Partijos ID** pasirenkate naują vertę.</span><span class="sxs-lookup"><span data-stu-id="e1469-106">When you're reviewing a picking list journal line, the value in the **Batch number** field is cleared if you select a new value in the **Lot ID** field.</span></span>

## <a name="resolution"></a><span data-ttu-id="e1469-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="e1469-107">Resolution</span></span>

<span data-ttu-id="e1469-108">Sistema veikia kaip sukurta.</span><span class="sxs-lookup"><span data-stu-id="e1469-108">The system is behaving as designed.</span></span> <span data-ttu-id="e1469-109">Jei pakeisite partijos ID, pakeisite prekės kontekstą.</span><span class="sxs-lookup"><span data-stu-id="e1469-109">If you change the lot ID, you change the item context.</span></span> <span data-ttu-id="e1469-110">Todėl paketo numeris yra atkurtas.</span><span class="sxs-lookup"><span data-stu-id="e1469-110">Therefore, the batch number is reset.</span></span>

<span data-ttu-id="e1469-111">Norėdami susieti paketo numerį su partijos ID, pirmiausia turite nustatyti partijos ID.</span><span class="sxs-lookup"><span data-stu-id="e1469-111">To associate the batch number with a lot ID, you must set the lot ID first.</span></span>
