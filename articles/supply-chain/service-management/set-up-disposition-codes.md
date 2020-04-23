---
title: Nustatyti perdavimo kodus
description: Galite nustatyti perdavimo kodus ir nurodyti, kaip apdoroti kliento grąžintą prekę.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnDispositionCode
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56f04c80652278aa24425dc3898063d5178e419e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205833"
---
# <a name="set-up-disposition-codes"></a><span data-ttu-id="375f9-103">Nustatyti perdavimo kodus</span><span class="sxs-lookup"><span data-stu-id="375f9-103">Set up disposition codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="375f9-104">Galite nustatyti perdavimo kodus ir nurodyti, kaip apdoroti kliento grąžintą prekę.</span><span class="sxs-lookup"><span data-stu-id="375f9-104">You can set up disposition codes to specify how to process an item that is returned by a customer.</span></span> <span data-ttu-id="375f9-105">Pvz., sukurkite perdavimo kodą pavadinimu **Sutaisyti ir grąžinti**, kad nurodytumėte, jog grąžinta prekė bus sutaisyta ir tada grąžinta klientui.</span><span class="sxs-lookup"><span data-stu-id="375f9-105">For example, create a disposition code named **Repair and return** to indicate that the returned item will be repaired and then returned to the customer.</span></span> <span data-ttu-id="375f9-106">Daugiau perdavimo kodų, paprastai naudojamų apdorojant klientų grąžintas prekes, pavyzdžių rasite faile [Nustatymas, kaip išmesti grąžintas prekes](specify-how-to-dispose-of-returned-items.md).</span><span class="sxs-lookup"><span data-stu-id="375f9-106">For more examples of disposition codes that are typically used for items that are returned by customers, see [Specify how to dispose of returned items](specify-how-to-dispose-of-returned-items.md).</span></span>

<span data-ttu-id="375f9-107">Taip pat galite nustatyti priežasties kodą, kuris padės paaiškinti, kodėl prekė buvo grąžinta.</span><span class="sxs-lookup"><span data-stu-id="375f9-107">You can also set up a reason code to help explain why an item was returned.</span></span> <span data-ttu-id="375f9-108">Daugiau informacijos apie priežasties kodus žr. [Grąžinimo priežasties kodų nustatymas](set-up-return-reason-code.md).</span><span class="sxs-lookup"><span data-stu-id="375f9-108">For more information about reason codes, see [Set up return reason codes](set-up-return-reason-code.md).</span></span>

1.  <span data-ttu-id="375f9-109">Spustelėkite **Pardavimas ir rinkodara** \> **Sąranka** \> **Pardavimo užsakymai** \> **Grąžinimai** \> **Perdavimo kodai**.</span><span class="sxs-lookup"><span data-stu-id="375f9-109">Click **Sales and marketing** \> **Setup** \> **Sales orders** \> **Returns** \> **Disposition codes**.</span></span>

2.  <span data-ttu-id="375f9-110">Spustelėkite **Naujas** arba paspauskite CTRL + N, kad sukurtumėte naują perdavimo kodą.</span><span class="sxs-lookup"><span data-stu-id="375f9-110">Click **New** or press CTRL+N to create a new disposition code.</span></span>

3.  <span data-ttu-id="375f9-111">Įveskite unikalų aprašomąjį pavadinimą, pasirinkite veiksmą ir įveskite perdavimo kodo aprašą.</span><span class="sxs-lookup"><span data-stu-id="375f9-111">Enter a unique, descriptive name, select an action, and enter a description for the disposition code.</span></span>

4.  <span data-ttu-id="375f9-112">Jei norite susieti kokias nors kliento išlaidas su šiuo perdavimo kodu, spustelėję mygtuką **Išlaidos** atidarykite formą **Nustatyti išlaidas**.</span><span class="sxs-lookup"><span data-stu-id="375f9-112">If you want to associate any customer charges with this disposition code, click the **Charges** button to open the **Set up charges** form.</span></span>

5.  <span data-ttu-id="375f9-113">Jei norite nurodyti kokius nors išorinius kodus, kurie atitiktų įmonės perdavimo kodus, spustelėję mygtuką **Išoriniai kodai** atidarykite formą **Išoriniai kodai**.</span><span class="sxs-lookup"><span data-stu-id="375f9-113">If you want to define any external codes to match with the company's own disposition codes, click the **External codes** button to open the **External codes** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="375f9-114">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="375f9-114">See also</span></span>

[<span data-ttu-id="375f9-115">Kliento grąžinimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="375f9-115">Customer returns overview</span></span>](disposition-and-return-reason-codes.md)

<span data-ttu-id="375f9-116">[Perdavimo kodai (forma)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="375f9-116">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

<span data-ttu-id="375f9-117">[Automatinės išlaidos (forma)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="375f9-117">[Auto charges (form)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))</span></span>

<span data-ttu-id="375f9-118">[Išoriniai kodai (forma)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="375f9-118">[External codes (form)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))</span></span>

  


