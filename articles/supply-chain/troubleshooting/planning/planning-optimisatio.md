---
title: Suplanuotas pirkimo užsakymas sukuriamas, kai pirkimas yra per neigiamas dienas
description: Jei padengimo kodas yra min. / maks., „Planning Optimization“ sukuria suplanuotą pirkimo užsakymą, kai pirkimas yra per neigiamas dienas.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026751"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="a32d0-103">Suplanuotas pirkimo užsakymas sukuriamas, kai pirkimas yra per neigiamas dienas</span><span class="sxs-lookup"><span data-stu-id="a32d0-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="a32d0-104">KB numeris: 4614298</span><span class="sxs-lookup"><span data-stu-id="a32d0-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="a32d0-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="a32d0-105">Symptoms</span></span>

<span data-ttu-id="a32d0-106">Jei padengimo kodas yra *Min./maks.*, „Planning Optimization“ sukuria suplanuotą pirkimo užsakymą, kai pirkimas yra per neigiamas dienas.</span><span class="sxs-lookup"><span data-stu-id="a32d0-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="a32d0-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="a32d0-107">Resolution</span></span>

<span data-ttu-id="a32d0-108">„Planning Optimization“ nepalaiko neigiamų dienų.</span><span class="sxs-lookup"><span data-stu-id="a32d0-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="a32d0-109">Tačiau, jis visada užtikrina, kad gamybos laiko, susijusios su dabartine data, suplanuoti užsakymai nebus planuojami.</span><span class="sxs-lookup"><span data-stu-id="a32d0-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="a32d0-110">Pavyzdžiui, pirkimo vykdymo laikas yra 10 dienų, o pirkimo užsakymas turėtų gauti aštuonias dienas nuo šiandien.</span><span class="sxs-lookup"><span data-stu-id="a32d0-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="a32d0-111">Šiuo atveju pirkimo užsakymas bus naudojamas kaip tiekimas pagal poreikį, kuris yra penkios dienos nuo šiandienos.</span><span class="sxs-lookup"><span data-stu-id="a32d0-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="a32d0-112">Dėl to rekomenduojame koreguoti gamybos laiką, kad jis apimtų visus (arba beveik visus) jūsų scenarijus.</span><span class="sxs-lookup"><span data-stu-id="a32d0-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
