---
title: "Kaupimų apžvalga"
description: "Šiame straipsnyje aprašyti kaupimai ir pateikta informacija apie tai, kaip juos nustatyti ir sukurti operacijas."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0b4d8e7eb268857ce753415a24e600b8006eb5e3
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="accruals-overview"></a><span data-ttu-id="75497-103">Kaupimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="75497-103">Accruals overview</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="75497-104">Šiame straipsnyje aprašyti kaupimai ir pateikta informacija apie tai, kaip juos nustatyti ir sukurti operacijas.</span><span class="sxs-lookup"><span data-stu-id="75497-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="75497-105">Kaupimai naudojami taikant kaupimo apskaitos principą, kuriuo sekamos įplaukos, priskiriamos tam pačiam laikotarpiui, kada jos uždirbtos, o ne kada gautas apmokėjimas, ir sekamos išlaidos (sąnaudos), priskiriamos tuomet, kai jos įvyksta, o ne kada atliekamas apmokėjimas.</span><span class="sxs-lookup"><span data-stu-id="75497-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="75497-106">Kaupimo schemos</span><span class="sxs-lookup"><span data-stu-id="75497-106">Accrual schemes</span></span>
<span data-ttu-id="75497-107">Kaupimo schemos naudojamos nustatant atidėtas įplaukas ir išlaidas – ta pati kaupimo schema gali būti naudojama ir įplaukoms, ir išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="75497-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="75497-108">DK kaupimai paskirsto žurnalo eilutės išlaidas ar įplaukas, kad išlaidos ir įplaukos būtų priskiriamos atitinkamuose laikotarpiuose.</span><span class="sxs-lookup"><span data-stu-id="75497-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="75497-109">Puslapyje **Kaupimo schema** galite nurodyti debeto ir kredito sąskaitas, kurios bus naudojamos pritaikius kaupimo schemą.</span><span class="sxs-lookup"><span data-stu-id="75497-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="75497-110">**Debetas** – jūsų nurodyta sąskaita pakeis debeto pagrindinę sąskaitą žurnalo kvito eilutėje.</span><span class="sxs-lookup"><span data-stu-id="75497-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="75497-111">Ši sąskaita bus taip pat naudojama atšaukiant atidėjimą pagal DK kaupimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="75497-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="75497-112">**Kreditas** – jūsų nurodyta pagrindinė sąskaita pakeis kredito pagrindinę sąskaitą žurnalo kvito eilutėje.</span><span class="sxs-lookup"><span data-stu-id="75497-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="75497-113">Ši sąskaita bus taip pat naudojama atšaukiant atidėjimą pagal DK kaupimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="75497-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="75497-114">Nusprendę, kurias sąskaitas naudoti, galite nurodyti, kaip kuriamas kvito numeris, kai kuriamos kaupimo operacijos.</span><span class="sxs-lookup"><span data-stu-id="75497-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="75497-115">Taip pat galite nurodyti, kaip dažnai vyksta operacijos, kiek kartų operacijos sukuriamos ir kada operacijos registurojamos.</span><span class="sxs-lookup"><span data-stu-id="75497-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="75497-116">Sukūrę kaupimo schemą, galite ją naudoti kai kuriuose žurnaluose, pasitelkdami DK kaupimų funkciją.</span><span class="sxs-lookup"><span data-stu-id="75497-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="75497-117">DK kaupimai</span><span class="sxs-lookup"><span data-stu-id="75497-117">Ledger accruals</span></span>
<span data-ttu-id="75497-118">Įvedę žurnalą, galite spustelėti **DK kaupimai** meniu **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="75497-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="75497-119">Tada, kai pasirenkate kaupimo schemą, matysite pagrindinę žurnalo sumą, kuri bus paskirstyta per laikotarpį pagal kaupimo schemą.</span><span class="sxs-lookup"><span data-stu-id="75497-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="75497-120">Pavyzdžiui, jei sausį mokate darbuotojo draudimą už visus metus, ir ši suma yra 12 000, šias išlaidas turite priskirti kiekvieną mėnesį.</span><span class="sxs-lookup"><span data-stu-id="75497-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="75497-121">Galite pasirinkti pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="75497-121">You can select the start date.</span></span> <span data-ttu-id="75497-122">Taip pat galite nurodyti, ar suma sukaupta pagal sąskaita arba korespondentinę sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="75497-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="75497-123">Atlikę savo pasirinkimus, spustelėkite **Operacijos**, kad peržiūrėtumėte visas operacijas, sukurtas pagal kaupimo schemą.</span><span class="sxs-lookup"><span data-stu-id="75497-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="75497-124">Pavyzdžiui, jei 12 000 draudimo išlaidų paskirstysite per metus, kiekvieną mėnesį matysite 1 000.</span><span class="sxs-lookup"><span data-stu-id="75497-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="75497-125">Užregistravę žurnalą, galite peržiūrėti operacijas naudodami užklausų puslapį **Kvito operacijos**.</span><span class="sxs-lookup"><span data-stu-id="75497-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="75497-126">Jei kaupimo schemos pritaikyti negalima (pvz., kai yra pardavimo užsakymo SF arba pirkimo užsakymo SF), galite kredituoti iš anksto sumokėtą sumą ir debetuoti išlaidų sumą.</span><span class="sxs-lookup"><span data-stu-id="75497-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="75497-127">Tada, taikydami kaupimo schemą, galite pasirinkti **Korespondentinė sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="75497-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="75497-128">Daugiau informacijos žr. [Kurti kaupimo schemas](tasks/create-accrual-schemes.md) ir [Kurti DK kaupimo operacijas](tasks/create-ledger-accrual-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="75497-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>

