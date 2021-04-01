---
title: Turto nuomos sutartys
description: Šioje temoje aprašomos sutartys išnuomotam turtui.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7072c34ccbffc6bf135f55fd594cac4d9ea5a463
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237521"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="675f3-103">Turto nuomos sutartys</span><span class="sxs-lookup"><span data-stu-id="675f3-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="675f3-104">Šioje temoje aprašomos sutartys išnuomotam turtui.</span><span class="sxs-lookup"><span data-stu-id="675f3-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="675f3-105">Lizingo sutartys yra naudojamas nustatyti nuomos knygos pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="675f3-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="675f3-106">Jei lizingo sutartis yra nustatyta į **Jokia**, pradžios data yra tokia pati kaip nuomos pradžios data (tai reiškia, kad vertė yra **Nuomos pradžios datos** laukelio).</span><span class="sxs-lookup"><span data-stu-id="675f3-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="675f3-107">Jei lizingo sutartis yra nustatyta į **Viso mėnesio**, pradžios data yra pirmoji mėnesio data, į kurį patenka nuomos pradžios data.</span><span class="sxs-lookup"><span data-stu-id="675f3-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="675f3-108">Pradžios datos nustato įsipareigojimų amortizavimo laikotarpio pradžios datą ir turto nuvertėjimo grafikus.</span><span class="sxs-lookup"><span data-stu-id="675f3-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="675f3-109">Interesų išlaidos ir nuvertėjimo kaštai yra publikuojami atitinkamų grafikų laikotarpio pabaigos duomenimis.</span><span class="sxs-lookup"><span data-stu-id="675f3-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="675f3-110">Pradinis pripažinimas ir koregavimo žurnalo įrašas yra publikuojami pradžios dieną.</span><span class="sxs-lookup"><span data-stu-id="675f3-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="675f3-111">Lizingo sutarčių funkcija turi būti įjungta per Funkcijų valdymą.</span><span class="sxs-lookup"><span data-stu-id="675f3-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="675f3-112">Darbo srityje **Funkcijų valdymas** raskite ir pasirinkite funkciją pavadinimu **Lizingo sutartis turto nuomai** ir tada rinkitės **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="675f3-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="675f3-113">Lizingo sutartys yra priskiriamos lizingo turto knygos nustatymui.</span><span class="sxs-lookup"><span data-stu-id="675f3-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="675f3-114">Norėdami peržiūrėti ir priskirti lizingo sutartį, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="675f3-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="675f3-115">Eikite į **Turto nuoma \> Sąranka \> Nuomos knygos**.</span><span class="sxs-lookup"><span data-stu-id="675f3-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="675f3-116">Laukelyje **Lizingo sutartis** rinkitės vieną tolesnių verčių.</span><span class="sxs-lookup"><span data-stu-id="675f3-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="675f3-117">Nuomos konvencija</span><span class="sxs-lookup"><span data-stu-id="675f3-117">Leasing convention</span></span> | <span data-ttu-id="675f3-118">aprašymas</span><span class="sxs-lookup"><span data-stu-id="675f3-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="675f3-119">None</span><span class="sxs-lookup"><span data-stu-id="675f3-119">None</span></span>               | <span data-ttu-id="675f3-120">Įsipareigojimų amortizavimo ir turto nuvertėjimo grafikai prasideda nuomos pradžios dieną, nes pradžios data atitinka nuomos pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="675f3-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="675f3-121">Pabaigos data yra vienu mėnesiu vėliau.</span><span class="sxs-lookup"><span data-stu-id="675f3-121">The end date is one month later.</span></span> <span data-ttu-id="675f3-122">Ši lizingo sutarti neužtikrina, kad interesas bus publikuotas paskutinę kiekvieno mėnesio dieną.</span><span class="sxs-lookup"><span data-stu-id="675f3-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="675f3-123">Visas mėnuo</span><span class="sxs-lookup"><span data-stu-id="675f3-123">Full month</span></span>         | <span data-ttu-id="675f3-124">Nuomai, kurios pradžios data yra bet kada šį mėnesį, įsipareigojimų amortizavimas ir turto nuvertėjimo grafikai pradeda skaičiuoti išlaidas pirmą to mėnesio dieną.</span><span class="sxs-lookup"><span data-stu-id="675f3-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="675f3-125">Ši lizingo sutarti užtikrina, kad interesas būtų apskaičiuotas paskutinę kiekvieno mėnesio dieną už visą mėnesį.</span><span class="sxs-lookup"><span data-stu-id="675f3-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="675f3-126">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="675f3-126">Select **Save**.</span></span>

<span data-ttu-id="675f3-127">Sukūrus nuomą, kiekvienos knygos pradžios diena yra automatiškai įvedama pagal pradžios dieną, kuri įvedama už nuomą ir nuomos sutartį nurodytą knygoje.</span><span class="sxs-lookup"><span data-stu-id="675f3-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]