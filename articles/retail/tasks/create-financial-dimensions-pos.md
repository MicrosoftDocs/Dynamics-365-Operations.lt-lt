--- 
title: " Kurti EKA registrų finansines dimensijas ir konfigūruoti dimensijų reikšmes registruose"
description: "Ši procedūra padeda kurti elektroninio kasos aparato (EKA) registrų finansines dimensijas ir nurodo, kaip konfigūruoti registrų finansinių dimensijų reikšmes."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 74f9f16ab3dfc6e41a720d73cd62583aebbdd84e
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="8bbe4-103"> Kurti EKA registrų finansines dimensijas ir konfigūruoti dimensijų reikšmes registruose</span><span class="sxs-lookup"><span data-stu-id="8bbe4-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8bbe4-104">Ši procedūra padeda kurti elektroninio kasos aparato (EKA) registrų finansines dimensijas ir nurodo, kaip konfigūruoti registrų finansinių dimensijų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="8bbe4-105">Ši procedūra neapima kitų susijusių veiksmų, pavyzdžiui, dimensijų rinkinių ir sąskaitų struktūrų kūrimo.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="8bbe4-106">Šios užduotys aprašytos kitose temose.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="8bbe4-107">Šiame įraše naudojama demonstracinė įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="8bbe4-108">Eikite į Didžioji knyga > Sąskaitų planas > Dimensijos > Finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="8bbe4-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-109">Click New.</span></span>
3. <span data-ttu-id="8bbe4-110">Lauke Naudoti vertes iš pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="8bbe4-111">Lauke Dimensijos pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="8bbe4-112">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-112">Click Activate.</span></span>
6. <span data-ttu-id="8bbe4-113">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-113">Click Close.</span></span>
7. <span data-ttu-id="8bbe4-114">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-114">Click Activate.</span></span>
8. <span data-ttu-id="8bbe4-115">Spustelėkite Dimensijos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-115">Click Dimension values.</span></span>
9. <span data-ttu-id="8bbe4-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-116">Close the page.</span></span>
10. <span data-ttu-id="8bbe4-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-117">Click Save.</span></span>
11. <span data-ttu-id="8bbe4-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-118">Close the page.</span></span>
12. <span data-ttu-id="8bbe4-119">Pasirinkite Mažmeninė prekyba ir prekyba > Kanalo sąranka > EKA sąranka > Registrai.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-119">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="8bbe4-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="8bbe4-121">Perjunkite skyriaus „Finansinės dimensijos“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="8bbe4-122">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-122">Click Edit.</span></span>
16. <span data-ttu-id="8bbe4-123">Lauke Terminalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="8bbe4-124">Sąraše raskite ir pasirinkite naujinamo registro dimensijos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="8bbe4-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-125">Click Save.</span></span>


