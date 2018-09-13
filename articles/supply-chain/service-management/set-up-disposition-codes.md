---
title: Nustatyti perdavimo kodus
description: "Galite nustatyti perdavimo kodus ir nurodyti, kaip apdoroti kliento grąžintą prekę."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnDispositionCode
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 96fb8bd2ce7fed6962563773ad63a7a48943e1ca
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---


# <a name="set-up-disposition-codes"></a><span data-ttu-id="dfbab-103">Nustatyti perdavimo kodus</span><span class="sxs-lookup"><span data-stu-id="dfbab-103">Set up disposition codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="dfbab-104">Galite nustatyti perdavimo kodus ir nurodyti, kaip apdoroti kliento grąžintą prekę.</span><span class="sxs-lookup"><span data-stu-id="dfbab-104">You can set up disposition codes to specify how to process an item that is returned by a customer.</span></span> <span data-ttu-id="dfbab-105">Pvz., sukurkite perdavimo kodą pavadinimu **Sutaisyti ir grąžinti**, kad nurodytumėte, jog grąžinta prekė bus sutaisyta ir tada grąžinta klientui.</span><span class="sxs-lookup"><span data-stu-id="dfbab-105">For example, create a disposition code named **Repair and return** to indicate that the returned item will be repaired and then returned to the customer.</span></span> <span data-ttu-id="dfbab-106">Daugiau perdavimo kodų, paprastai naudojamų apdorojant klientų grąžintas prekes, pavyzdžių rasite faile [Nustatymas, kaip išmesti grąžintas prekes](specify-how-to-dispose-of-returned-items.md).</span><span class="sxs-lookup"><span data-stu-id="dfbab-106">For more examples of disposition codes that are typically used for items that are returned by customers, see [Specify how to dispose of returned items](specify-how-to-dispose-of-returned-items.md).</span></span>

<span data-ttu-id="dfbab-107">Taip pat galite nustatyti priežasties kodą, kuris padės paaiškinti, kodėl prekė buvo grąžinta.</span><span class="sxs-lookup"><span data-stu-id="dfbab-107">You can also set up a reason code to help explain why an item was returned.</span></span> <span data-ttu-id="dfbab-108">Daugiau informacijos apie priežasties kodus ieškokite faile [Grąžinimo priežasties kodo nustatymas](set-up-return-reason-code.md).</span><span class="sxs-lookup"><span data-stu-id="dfbab-108">For more information about reason codes, see [Set up return reason code](set-up-return-reason-code.md).</span></span>

1.  <span data-ttu-id="dfbab-109">Spustelėkite **Pardavimas ir rinkodara** \> **Sąranka** \> **Pardavimo užsakymai** \> **Grąžinimai** \> **Perdavimo kodai**.</span><span class="sxs-lookup"><span data-stu-id="dfbab-109">Click **Sales and marketing** \> **Setup** \> **Sales orders** \> **Returns** \> **Disposition codes**.</span></span>

2.  <span data-ttu-id="dfbab-110">Spustelėkite **Naujas** arba paspauskite CTRL + N, kad sukurtumėte naują perdavimo kodą.</span><span class="sxs-lookup"><span data-stu-id="dfbab-110">Click **New** or press CTRL+N to create a new disposition code.</span></span>

3.  <span data-ttu-id="dfbab-111">Įveskite unikalų aprašomąjį pavadinimą, pasirinkite veiksmą ir įveskite perdavimo kodo aprašą.</span><span class="sxs-lookup"><span data-stu-id="dfbab-111">Enter a unique, descriptive name, select an action, and enter a description for the disposition code.</span></span>

4.  <span data-ttu-id="dfbab-112">Jei norite susieti kokias nors kliento išlaidas su šiuo perdavimo kodu, spustelėję mygtuką **Išlaidos** atidarykite formą **Nustatyti išlaidas**.</span><span class="sxs-lookup"><span data-stu-id="dfbab-112">If you want to associate any customer charges with this disposition code, click the **Charges** button to open the **Set up charges** form.</span></span>

5.  <span data-ttu-id="dfbab-113">Jei norite nurodyti kokius nors išorinius kodus, kurie atitiktų įmonės perdavimo kodus, spustelėję mygtuką **Išoriniai kodai** atidarykite formą **Išoriniai kodai**.</span><span class="sxs-lookup"><span data-stu-id="dfbab-113">If you want to define any external codes to match with the company's own disposition codes, click the **External codes** button to open the **External codes** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="dfbab-114">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="dfbab-114">See also</span></span>

[<span data-ttu-id="dfbab-115">Perdavimo kodai ir grąžinimo priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="dfbab-115">Disposition codes and return reason codes</span></span>](disposition-and-return-reason-codes.md)

<span data-ttu-id="dfbab-116">[Perdavimo kodai (forma)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="dfbab-116">[Disposition codes (form)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span></span>

<span data-ttu-id="dfbab-117">[Automatinės išlaidos (forma)](https://technet.microsoft.com/en-us/library/aa582856\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="dfbab-117">[Auto charges (form)](https://technet.microsoft.com/en-us/library/aa582856\(v=ax.60\))</span></span>

<span data-ttu-id="dfbab-118">[Išoriniai kodai (forma)](https://technet.microsoft.com/en-us/library/aa583814\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="dfbab-118">[External codes (form)](https://technet.microsoft.com/en-us/library/aa583814\(v=ax.60\))</span></span>

  


