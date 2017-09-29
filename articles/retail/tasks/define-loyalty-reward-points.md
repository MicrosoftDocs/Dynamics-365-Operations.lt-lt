--- 
title: " Atlygio už lojalumą taškų nustatymas"
description: "Ši procedūra padeda nustatyti atlygio už lojalumą taškus."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 05237a0ba3aa785432c8b1fc36284a47f9aabd4a
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="21815-103"> Atlygio už lojalumą taškų nustatymas</span><span class="sxs-lookup"><span data-stu-id="21815-103">Define loyalty reward points</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="21815-104">Ši procedūra padeda nustatyti atlygio už lojalumą taškus.</span><span class="sxs-lookup"><span data-stu-id="21815-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="21815-105">Atlygio taškus turite nustatyti prieš nustatydami lojalumo programą.</span><span class="sxs-lookup"><span data-stu-id="21815-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="21815-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="21815-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="21815-107">Pasirinkite Mažmeninė prekyba ir prekyba > Klientai > Lojalumas > Atlygio už lojalumą taškai.</span><span class="sxs-lookup"><span data-stu-id="21815-107">Go to Retail and commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="21815-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="21815-108">Click New.</span></span>
3. <span data-ttu-id="21815-109">Lauke Atlygio taško ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="21815-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="21815-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="21815-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="21815-111">Lauke Atlygio taško tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="21815-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="21815-112">Pasirinkite Kiekis, jei norite atlygio taškus apvalinti iki artimiausio sveikojo skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="21815-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="21815-113">Pasirinkite Suma, jei norite atlygio taškus apvalinti pagal valiutos apvalinimo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="21815-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="21815-114">Jei pasirinksite Kiekis, praleiskite kitą šios procedūros veiksmą.</span><span class="sxs-lookup"><span data-stu-id="21815-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="21815-115">Lauke Valiuta surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="21815-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="21815-116">Visi išduoti tipo Suma atlygio taškai bus pateikiami pasirinkta valiuta.</span><span class="sxs-lookup"><span data-stu-id="21815-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="21815-117">Tipo Kiekis atlygio taškams šis laukas nėra taikomas, praleiskite šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="21815-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="21815-118">Pažymėkite arba atžymėkite žymės langelį Galima išnaudoti.</span><span class="sxs-lookup"><span data-stu-id="21815-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="21815-119">Lauke išnaudojimo tvarka įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="21815-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="21815-120">Panaudojimo tvarka yra naudojama, kai galima naudoti du ar daugiau naudojamų atlygio taškų norint mokėti už produktus.</span><span class="sxs-lookup"><span data-stu-id="21815-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="21815-121">Jei dviejų atlygio taškų panaudojimo tvarka yra ta pati, tada bus naudojamas tas, kurio taškų skaičių reikia sumažinti.</span><span class="sxs-lookup"><span data-stu-id="21815-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="21815-122">Lauke Galiojimo pabaigos laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="21815-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="21815-123">Atlygio taškų galiojimas baigsis po nurodyto dienų, mėnesių ar metų nuo taškų išdavimo skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="21815-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="21815-124">Reikšmė „0“ nurodo, kad atlygio taškai niekada nesibaigs.</span><span class="sxs-lookup"><span data-stu-id="21815-124">A value of ‘0’ means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="21815-125">Lauke Galiojimo pabaigos laiko vienetas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="21815-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="21815-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="21815-126">Click Save.</span></span>

