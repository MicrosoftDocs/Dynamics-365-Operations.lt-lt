---
title: Pagrindiniai SF duomenys AP sistemoje naudojant tvirtinimo žurnalą
description: Šis užduočių vadovas parodys, kaip naudojant SF registrą kurti SF ir tada, naudojant patvirtinimo žurnalą, atnaujinti išlaidų sąskaitas.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "363527"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a><span data-ttu-id="f4410-103">Pagrindiniai SF duomenys AP sistemoje naudojant tvirtinimo žurnalą</span><span class="sxs-lookup"><span data-stu-id="f4410-103">Key invoice data into AP system using approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4410-104">Šis užduočių vadovas parodys, kaip naudojant SF registrą kurti SF ir tada, naudojant patvirtinimo žurnalą, atnaujinti išlaidų sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="f4410-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="f4410-105">Kurti ir registruoti SF</span><span class="sxs-lookup"><span data-stu-id="f4410-105">Create and post and invoice</span></span>
1. <span data-ttu-id="f4410-106">Pasirinkite Mokėtinos sumos > Sąskaitos faktūros > SF registras.</span><span class="sxs-lookup"><span data-stu-id="f4410-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="f4410-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f4410-107">Click New.</span></span>
3. <span data-ttu-id="f4410-108">Pasirinkite norimo naudoti SF registro pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f4410-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="f4410-109">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f4410-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f4410-110">Spustelėdami Eilutės atidarykite registrą ir įveskite išlaidų eilutes.</span><span class="sxs-lookup"><span data-stu-id="f4410-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="f4410-111">Pasirinkite tiekėją.</span><span class="sxs-lookup"><span data-stu-id="f4410-111">Select a vendor.</span></span> <span data-ttu-id="f4410-112">Pavyzdžiui, įveskite arba pasirinkite US-104</span><span class="sxs-lookup"><span data-stu-id="f4410-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="f4410-113">Lauke Sąskaita faktūra surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f4410-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="f4410-114">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f4410-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="f4410-115">Lauke Kreditas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="f4410-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="f4410-116">Lauke Patvirtino spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f4410-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f4410-117">Pažymėkite tvirtintoją ir spustelėkite Pasirinkti, kad tą tvirtintoją pasirinktumėte.</span><span class="sxs-lookup"><span data-stu-id="f4410-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="f4410-118">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="f4410-118">Click Post.</span></span>
13. <span data-ttu-id="f4410-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f4410-119">Close the page.</span></span>
14. <span data-ttu-id="f4410-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f4410-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="f4410-121">Tvirtinti SF</span><span class="sxs-lookup"><span data-stu-id="f4410-121">Approve an invoice</span></span>
1. <span data-ttu-id="f4410-122">Pasirinkite Mokėtinos sumos > Sąskaitos faktūros > SF tvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="f4410-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="f4410-123">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f4410-123">Click New.</span></span>
3. <span data-ttu-id="f4410-124">Pasirinkite norimo naudoti SF tvirtinimo žurnalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f4410-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="f4410-125">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f4410-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f4410-126">Spustelėjus eilutes, bus rodomas puslapis, kuriame galėsite pasirinkti SF, kurias norite patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="f4410-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="f4410-127">Pasirinkus Rasti kvitus, bus rodomos visos SF, kurias galima tvirtinti.</span><span class="sxs-lookup"><span data-stu-id="f4410-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="f4410-128">Pažymėkite savo sukurtą sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="f4410-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="f4410-129">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="f4410-129">Click Select.</span></span>
    * <span data-ttu-id="f4410-130">Jums pasirinkus pirmiau pateiktus kvitus, jie perkeliami į šį sąrašą.</span><span class="sxs-lookup"><span data-stu-id="f4410-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="f4410-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f4410-131">Click OK.</span></span>
10. <span data-ttu-id="f4410-132">Spustelėkite ant sąskaitos numerio lauko, kad į SF įtrauktumėte išlaidų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="f4410-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="f4410-133">Įveskite sąskaitos numerį ir pereikite iš lauko.</span><span class="sxs-lookup"><span data-stu-id="f4410-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="f4410-134">Pavyzdžiui, įveskite 600120.</span><span class="sxs-lookup"><span data-stu-id="f4410-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="f4410-135">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="f4410-135">Click Post.</span></span>
13. <span data-ttu-id="f4410-136">Spustelėkite Kvitas, kad peržiūrėtumėte visus registruotus įrašus.</span><span class="sxs-lookup"><span data-stu-id="f4410-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="f4410-137">Patvirtinimo laukiančių SF sąskaita atšaukiama ir pakeičiama faktine išlaidų sąskaita.</span><span class="sxs-lookup"><span data-stu-id="f4410-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

