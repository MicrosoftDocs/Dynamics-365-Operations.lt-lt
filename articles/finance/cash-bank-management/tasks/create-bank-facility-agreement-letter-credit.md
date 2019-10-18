---
title: Kurti akredityvo banko priemonės sutartį
description: Ši užduotis apžvelgia, kaip sukurti banko priemonės sutartį, kad būtų galima apdoroti Akredityvą.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e63e0ffa4ddafd38595d7e9d84ffa2399a9f67b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188216"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="28e10-103">Kurti akredityvo banko priemonės sutartį</span><span class="sxs-lookup"><span data-stu-id="28e10-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="28e10-104">Ši užduotis apžvelgia, kaip sukurti banko priemonės sutartį, kad būtų galima apdoroti Akredityvą.</span><span class="sxs-lookup"><span data-stu-id="28e10-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="28e10-105">Prieš vykdant šią užduotį rekomenduojama nustatyti banko priemones ir registravimo šablonus.</span><span class="sxs-lookup"><span data-stu-id="28e10-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="28e10-106">Šioje užduotyje naudojama demonstracinė įmonė „USMF‟.</span><span class="sxs-lookup"><span data-stu-id="28e10-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="28e10-107">Kurti banko priemonių sutartį</span><span class="sxs-lookup"><span data-stu-id="28e10-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="28e10-108">Pasirinkite Grynųjų pinigų ir banko valdymas > Akredityvai > Banko paslaugų sutartys.</span><span class="sxs-lookup"><span data-stu-id="28e10-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="28e10-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="28e10-109">Click New.</span></span>
3. <span data-ttu-id="28e10-110">Lauke Sutarties numeris įveskite sutarties numerį pagal sutartį su banku.</span><span class="sxs-lookup"><span data-stu-id="28e10-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="28e10-111">Lauke Banko sąskaita įveskite sąskaitos ją išduodančiame banke numerį.</span><span class="sxs-lookup"><span data-stu-id="28e10-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="28e10-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="28e10-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="28e10-113">Lauke Pradžios data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="28e10-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="28e10-114">Lauke Pabaigos data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="28e10-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="28e10-115">Išplėskite arba sutraukite dalį Bendra.</span><span class="sxs-lookup"><span data-stu-id="28e10-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="28e10-116">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="28e10-116">Click Add line.</span></span>
10. <span data-ttu-id="28e10-117">Lauke Priemonės tipas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="28e10-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="28e10-118">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="28e10-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="28e10-119">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="28e10-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="28e10-120">Lauke Limitas įveskite su banku sutartą priemonės sumą.</span><span class="sxs-lookup"><span data-stu-id="28e10-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="28e10-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="28e10-121">Click Save.</span></span>
15. <span data-ttu-id="28e10-122">Spustelėdami Išplėsti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="28e10-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="28e10-123">Lauke Naujas sutarties numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="28e10-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="28e10-124">Lauke Pabaigos data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="28e10-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="28e10-125">Spustelėkite Pratęsti.</span><span class="sxs-lookup"><span data-stu-id="28e10-125">Click Extend.</span></span>
19. <span data-ttu-id="28e10-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="28e10-126">Close the page.</span></span>

