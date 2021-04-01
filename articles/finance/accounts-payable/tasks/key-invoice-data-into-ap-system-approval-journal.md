---
title: Pagrindiniai SF duomenys mokėtinose sumose naudojant patvirtinimo žurnalą
description: Šioje temoje paaiškinama, kaip naudoti sąskaitų faktūrų registrą kuriant sąskaitas faktūras ir kaip paskui naudoti patvirtinimo žurnalą išlaidų sąskaitoms atnaujinti.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0fee32d9fd1ab89b1a8cedb2e1965674586d4e7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227189"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="8316c-103">Pagrindiniai SF duomenys mokėtinose sumose naudojant patvirtinimo žurnalą</span><span class="sxs-lookup"><span data-stu-id="8316c-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8316c-104">Šioje temoje paaiškinama, kaip naudoti sąskaitų faktūrų registrą kuriant sąskaitas faktūras ir kaip paskui naudoti patvirtinimo žurnalą išlaidų sąskaitoms atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="8316c-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="8316c-105">Kurti ir registruoti SF</span><span class="sxs-lookup"><span data-stu-id="8316c-105">Create and post and invoice</span></span>
1. <span data-ttu-id="8316c-106">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Sąskaitos faktūros > Sąskaitų faktūrų registras**.</span><span class="sxs-lookup"><span data-stu-id="8316c-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="8316c-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="8316c-107">Select **New**.</span></span>
3. <span data-ttu-id="8316c-108">Pasirinkite norimo naudoti SF registro pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="8316c-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="8316c-109">Pasirinkę **Eilutės**, atidarykite registrą ir įveskite išlaidų eilutes.</span><span class="sxs-lookup"><span data-stu-id="8316c-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="8316c-110">Pasirinkite tiekėją.</span><span class="sxs-lookup"><span data-stu-id="8316c-110">Select a vendor.</span></span> <span data-ttu-id="8316c-111">Pavyzdžiui, įveskite arba pasirinkite `US-104`.</span><span class="sxs-lookup"><span data-stu-id="8316c-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="8316c-112">Lauke **Sąskaita faktūra** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8316c-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="8316c-113">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8316c-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="8316c-114">Lauke **Kreditas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8316c-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="8316c-115">Lauke **Patvirtino** išplečiamajame meniu pasirinkite tvirtintoją.</span><span class="sxs-lookup"><span data-stu-id="8316c-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="8316c-116">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="8316c-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="8316c-117">Tvirtinti SF</span><span class="sxs-lookup"><span data-stu-id="8316c-117">Approve an invoice</span></span>
1. <span data-ttu-id="8316c-118">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Sąskaitos faktūros > Sąskaitų faktūrų patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="8316c-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="8316c-119">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="8316c-119">Select **New**.</span></span>
3. <span data-ttu-id="8316c-120">Pasirinkite norimo naudoti SF tvirtinimo žurnalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="8316c-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="8316c-121">Pasirinkite **Eilutės**, kad butų parodytas puslapis, kuriame galėsite pasirinkti norimas patvirtinti sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="8316c-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="8316c-122">Pasirinkite **Rasti kvitus**, kad būtų parodytos visos sąskaitos faktūros, kurias galima tvirtinti.</span><span class="sxs-lookup"><span data-stu-id="8316c-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="8316c-123">Pažymėkite sukurtą sąskaitą faktūrą, tada spustelėkite **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="8316c-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="8316c-124">Jums pasirinkus pirmiau pateiktus kvitus, jie perkeliami į šį sąrašą.</span><span class="sxs-lookup"><span data-stu-id="8316c-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="8316c-125">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8316c-125">Select **OK**.</span></span>
8. <span data-ttu-id="8316c-126">Pasirinkę lauką **kliento numeris**, į sąskaitą faktūrą įtraukite išlaidų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="8316c-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="8316c-127">Įveskite sąskaitos numerį ir pereikite iš lauko.</span><span class="sxs-lookup"><span data-stu-id="8316c-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="8316c-128">Pavyzdžiui, įveskite `600120`.</span><span class="sxs-lookup"><span data-stu-id="8316c-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="8316c-129">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="8316c-129">Select **Post**.</span></span>
11. <span data-ttu-id="8316c-130">Pasirinkę **Kvitas**, pamatysite užregistruotus įrašus.</span><span class="sxs-lookup"><span data-stu-id="8316c-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="8316c-131">Patvirtinimo laukiančių SF sąskaita atšaukiama ir pakeičiama faktine išlaidų sąskaita.</span><span class="sxs-lookup"><span data-stu-id="8316c-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]