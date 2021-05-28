---
title: Kai esamo svorio kiekis padalintas, mažiausias kiekis naudojamas vietoje nominalaus kiekio
description: Kai esamo svorio kiekis padalintas į paketus, lauke Paimtas kiekis naudojamas minimalus nustatytas prekės kiekis, o ne nominalusis kiekis.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026754"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="bf0f6-103">Kai esamo svorio kiekis padalintas, mažiausias kiekis naudojamas vietoje nominalaus kiekio</span><span class="sxs-lookup"><span data-stu-id="bf0f6-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="bf0f6-104">KB numeris: 4612073</span><span class="sxs-lookup"><span data-stu-id="bf0f6-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="bf0f6-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="bf0f6-105">Symptoms</span></span>

<span data-ttu-id="bf0f6-106">Kai esamo svorio kiekis padalintas į paketus, lauke **Paimtas kiekis** naudojamas minimalus nustatytas prekės kiekis, o ne nominalusis kiekis.</span><span class="sxs-lookup"><span data-stu-id="bf0f6-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="bf0f6-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="bf0f6-107">Resolution</span></span>

<span data-ttu-id="bf0f6-108">Sistema veikia kaip sukurta.</span><span class="sxs-lookup"><span data-stu-id="bf0f6-108">The system is behaving as designed.</span></span> <span data-ttu-id="bf0f6-109">Sistema paėmimui naudoja kiekvienos prekės minimalaus kiekio nustatymą.</span><span class="sxs-lookup"><span data-stu-id="bf0f6-109">The system uses each item's minimum quantity setup for picking.</span></span>
