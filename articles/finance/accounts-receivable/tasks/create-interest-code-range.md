---
title: Kurti palūkanų kodą su intervalu
description: Palūkanų kodus galima nustatyti apskaičiuoti kitas palūkanų sumas pagal verčių diapazoną.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44b98436d6e0c40f0458dc4744b8b1d96baa8b54
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216574"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="6cfd0-103">Kurti palūkanų kodą su intervalu</span><span class="sxs-lookup"><span data-stu-id="6cfd0-103">Create an interest code with a range</span></span>

[!include [banner](../../includes/banner.md)]
<span data-ttu-id="6cfd0-104">Palūkanų kodus galima nustatyti apskaičiuoti kitas palūkanų sumas pagal verčių diapazoną.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="6cfd0-105">Šios procedūros metu pamatysite, kaip įtraukti palūkanų kodą ir į jį įtraukti diapazoną.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="6cfd0-106">Pasirinkite Kreditas ir mokėjimai > Palūkanos > Nustatyti palūkanų kodus.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="6cfd0-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-107">Click New.</span></span>
3. <span data-ttu-id="6cfd0-108">Lauke Palūkanų kodas įveskite palūkanų kodo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="6cfd0-109">Lauke Aprašas įveskite palūkanų kodo aprašą.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="6cfd0-110">Pasirinkite Mėnuo.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-110">Select Month.</span></span>
6. <span data-ttu-id="6cfd0-111">Išplėskite skyrių Pajamos.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="6cfd0-112">Išplėskite skyrių Pajamos pagal valiutą.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="6cfd0-113">Lauke Didžiosios knygos registravimo sąskaita nurodykite norimas vertes.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="6cfd0-114">Lauke Palūkanos pagal diapazoną pasirinkite 'Mėnesiai'.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="6cfd0-115">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-115">Click Add.</span></span>
11. <span data-ttu-id="6cfd0-116">Lauke Aprašas įveskite šios valiutos ir diapazono aprašymą.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="6cfd0-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-117">Click Save.</span></span>
13. <span data-ttu-id="6cfd0-118">Spustelėkite Diapazonai.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-118">Click Ranges.</span></span>
14. <span data-ttu-id="6cfd0-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-119">Click New.</span></span>
15. <span data-ttu-id="6cfd0-120">Vertę Nuo įveskite kaip 0, tada įveskite palūkanų procentą per mėnesį, kuris bus naudojamas skaičiuojant palūkanas.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="6cfd0-121">Mūsų pavyzdyje tai yra 1,5.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="6cfd0-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-122">Click New.</span></span>
17. <span data-ttu-id="6cfd0-123">Įveskite kitą vertę Nuo kaip 4, tai yra pirmas mėnuo, kada apskaičiuosite naują palūkanų sumą.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="6cfd0-124">Įveskite palūkanų procentą per mėnesį, kuris bus naudojamas skaičiuojant palūkanas nuo 4 mėnesio.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="6cfd0-125">Šiame pavyzdyje tai yra 2,0.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="6cfd0-126">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-126">Click New.</span></span>
20. <span data-ttu-id="6cfd0-127">Įveskite kitą vertę Nuo kaip 7, tai yra kitas mėnuo, kada apskaičiuosite naują palūkanų sumą.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="6cfd0-128">Įveskite palūkanų procentą per mėnesį, kuris bus naudojamas skaičiuojant palūkanas nuo 7 mėnesio.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="6cfd0-129">Šiame pavyzdyje tai yra 2,5.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="6cfd0-130">Spustelėję Uždaryti užbaigsite nustatymą.</span><span class="sxs-lookup"><span data-stu-id="6cfd0-130">Click Close to complete the setup.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]