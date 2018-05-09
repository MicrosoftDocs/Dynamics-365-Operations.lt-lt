--- 
title: "Tiekėjo mokėjimų kūrimas ir eksportavimas naudojant ISO20022 mokėjimo formatą"
description: "Šioje procedūroje parodoma, kaip kurti mokėjimo eilutes tiekėjo mokėjimų žurnale ir generuoti tiekėjo mokėjimo failą naudojant ISO2022 kredito pervedimo pavyzdį."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 906f9611370e19ad4f063d15608d3564c5292c96
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="c09a4-103">Tiekėjo mokėjimų kūrimas ir eksportavimas naudojant ISO20022 mokėjimo formatą</span><span class="sxs-lookup"><span data-stu-id="c09a4-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c09a4-104">Šioje procedūroje parodoma, kaip kurti mokėjimo eilutes tiekėjo mokėjimų žurnale ir generuoti tiekėjo mokėjimo failą naudojant ISO2022 kredito pervedimo pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="c09a4-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="c09a4-105">Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DEMF.</span><span class="sxs-lookup"><span data-stu-id="c09a4-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="c09a4-106">Tai yra penktoji iš penkių procedūrų, kuriose aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="c09a4-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="c09a4-107">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="c09a4-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="c09a4-108">Kurti mokėjimo eilutes</span><span class="sxs-lookup"><span data-stu-id="c09a4-108">Create payment lines</span></span>
1. <span data-ttu-id="c09a4-109">Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas.</span><span class="sxs-lookup"><span data-stu-id="c09a4-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="c09a4-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c09a4-110">Click New.</span></span>
3. <span data-ttu-id="c09a4-111">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c09a4-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c09a4-112">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c09a4-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="c09a4-113">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="c09a4-113">Click Lines.</span></span>
6. <span data-ttu-id="c09a4-114">Spustelėkite Mokėjimo pasiūlymas.</span><span class="sxs-lookup"><span data-stu-id="c09a4-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="c09a4-115">Spustelėkite Kurti mokėjimo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="c09a4-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="c09a4-116">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="c09a4-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="c09a4-117">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="c09a4-117">Click Filter.</span></span>
10. <span data-ttu-id="c09a4-118">Sąraše pasirinkite lentelės Tiekėjai eilutę ir lauką Tiekėjo kodas.</span><span class="sxs-lookup"><span data-stu-id="c09a4-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="c09a4-119">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c09a4-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="c09a4-120">Galite taikyti bet kokį kriterijų, norėdami pasirinkti, kurias tiekėjo operacijas apmokėti, šiame pavyzdyje kaip tiekėjo kodą naudokite DE-001.</span><span class="sxs-lookup"><span data-stu-id="c09a4-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="c09a4-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c09a4-121">Click OK.</span></span>
13. <span data-ttu-id="c09a4-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c09a4-122">Click OK.</span></span>
14. <span data-ttu-id="c09a4-123">Spustelėkite Kurti mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="c09a4-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="c09a4-124">ISO20022 mokėjimo failo generavimas</span><span class="sxs-lookup"><span data-stu-id="c09a4-124">Generate an ISO20022 payment file</span></span>


