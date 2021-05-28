---
title: Negalima išrašyti sf su klientu susieti pardavimo užsakymui
description: Kai įgalinsite pasirinktį Registruoti SF automatiškai, nebegalėsite išrašyti pradinio pardavimo užsakymo ir pradinio tiesioginio pristatymo pirkimo užsakymo SF.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026741"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="9c3c1-103">Negalima išrašyti sf su klientu susieti pardavimo užsakymui</span><span class="sxs-lookup"><span data-stu-id="9c3c1-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="9c3c1-104">KB numeris: 4611793</span><span class="sxs-lookup"><span data-stu-id="9c3c1-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="9c3c1-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="9c3c1-105">Symptoms</span></span>

<span data-ttu-id="9c3c1-106">Nebegalėsite išrašyti originalaus pardavimo užsakymo ir originalaus tiesioginio pristatymo įsigijimo užsakymo po jo įjungimo **Publikuoti sąskaitą automatiškai** parinktį **Tarpinės įmonės** puslapyje tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="9c3c1-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="9c3c1-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="9c3c1-107">Resolution</span></span>

<span data-ttu-id="9c3c1-108">Vidinės įmonės ir tiesioginio pristatymo užsakymo SF sinchronizavimo elgseną kontroliuoja ir juos verčia parametrai, aprašyti parametruose, kuriuos reikia nurodyti [vidinės įmonės užsakymui registruoti](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span><span class="sxs-lookup"><span data-stu-id="9c3c1-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="9c3c1-109">Nustatę šiuos parametrus, pirmiausia turite išrašyti vidinės įmonės pardavimo užsakymo SF.</span><span class="sxs-lookup"><span data-stu-id="9c3c1-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="9c3c1-110">Tada sinchronizuojami pradiniai pardavimo ir pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="9c3c1-110">The original sales orders and purchase orders will then be synchronized.</span></span>
