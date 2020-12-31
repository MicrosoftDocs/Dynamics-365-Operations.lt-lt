---
title: Kompensacija klientams
description: Šiame straipsnyje paaiškinta, kaip kurti klientų grupės kompensavimo operacijas. Jei klientas turi kredito balansą, galite kompensuoti klientui balanso sumą.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65ee884fb22c1a38e2d3022085fed7e3e6077d1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644542"
---
# <a name="reimburse-customers"></a><span data-ttu-id="f2e72-104">Kompensacija klientams</span><span class="sxs-lookup"><span data-stu-id="f2e72-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2e72-105">Šiame straipsnyje paaiškinta, kaip kurti klientų grupės kompensavimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="f2e72-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="f2e72-106">Jei klientas turi kredito balansą, galite kompensuoti klientui balanso sumą.</span><span class="sxs-lookup"><span data-stu-id="f2e72-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="f2e72-107">Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="f2e72-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="f2e72-108">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="f2e72-108">Prerequisite</span></span>                                                            | <span data-ttu-id="f2e72-109">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f2e72-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="f2e72-110">Nurodykite mažiausią kompensacijos sumą juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="f2e72-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="f2e72-111">Puslapyje **Gautinų sumų parametrai**, srityje **Bendra**, lauke **Mažiausia kompensacija** įveskite mažiausią sumą, kurią galima kompensuoti dėl klientų permokėjimo.</span><span class="sxs-lookup"><span data-stu-id="f2e72-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="f2e72-112">Pasirinktinai: įtraukite tiekėjo sąskaitą kiekvienam klientui, kuriam galima kompensuoti.</span><span class="sxs-lookup"><span data-stu-id="f2e72-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="f2e72-113">Puslapyje **Klientai**, „FastTab“ skirtuke **Įvairi informacija**, lauke **Tiekėjo sąskaita** pasirinkite kliento tiekėjo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="f2e72-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="f2e72-114">Kuriant kompensavimo operacijas, kredito balanso sumai sukuriama tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="f2e72-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="f2e72-115">Kompensacijos procesas pašalina kliento sąskaitos kredito balansą ir sukuria mokėtiną balanso sumą tiekėjo sąskaitai, kuri atitinka klientą.</span><span class="sxs-lookup"><span data-stu-id="f2e72-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="f2e72-116">Gautinose sumose vykdykite procesą **Kompensavimas** (**Gautinos sumos \> Periodinės užduotys \> Kompensavimas**).</span><span class="sxs-lookup"><span data-stu-id="f2e72-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="f2e72-117">Norėdami sugrupuoti visas operacijas, nepriklausomai nuo DK dimensijų, nustatykite parinktį **Klientų sumavimas** į parametrą **Taip**.</span><span class="sxs-lookup"><span data-stu-id="f2e72-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="f2e72-118">Norėdami grupuoti tik tas operacijas, kurių DK dimensijos yra panašios, nustatykite pasirinktį **Ne**.</span><span class="sxs-lookup"><span data-stu-id="f2e72-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="f2e72-119">Pasirinkite **Įtraukti klientus su neapmokėtomis debeto operacijomis** ir pasirinkite klientus, kurie turi nesudengtų debeto sumų.</span><span class="sxs-lookup"><span data-stu-id="f2e72-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="f2e72-120">Norėdami kompensuoti tam tikras klientų sąskaitas, „FastTab“ **Įtrauktini įrašai** pasirinkite **Filtruoti** ir nurodykite klientų sąskaitas užklausoje.</span><span class="sxs-lookup"><span data-stu-id="f2e72-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="f2e72-121">Kredito sumos perkeliamos į klientų tiekėjų sąskaitas ir apdorojamos kaip įprasti mokėjimai.</span><span class="sxs-lookup"><span data-stu-id="f2e72-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="f2e72-122">Jei klientas neturi tiekėjo sąskaitos, klientui automatiškai sukuriama vienkartinė tiekėjo sąskaita.</span><span class="sxs-lookup"><span data-stu-id="f2e72-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="f2e72-123">Norėdami peržiūrėti sukurtas kompensavimo operacijas, naudokite ataskaitą **Kompensavimas** (**Gautinos sumos \> Užklausos ir ataskaitos \> Kompensavimo ataskaita**).</span><span class="sxs-lookup"><span data-stu-id="f2e72-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="f2e72-124">Mokėtinų sumų srityje sukurkite mokėjimą tiekėjo SF, kurias sukūrė kompensacijos procesas.</span><span class="sxs-lookup"><span data-stu-id="f2e72-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="f2e72-125">Norėdami gauti daugiau informacijos apie tai, kaip mokėti tiekėjams, žr. [Tiekėjų mokėjimo apžvalga](../accounts-payable/Vendor-payments-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="f2e72-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>
