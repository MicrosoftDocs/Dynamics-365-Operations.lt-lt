---
title: Kaupimo schemų kūrimas
description: Šioje temoje aiškinama, kaip kurti kaupimo schemą.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457be741dfd3b44cb963db37857d6a7bceecc14e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994670"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="c5bf9-103">Kaupimo schemų kūrimas</span><span class="sxs-lookup"><span data-stu-id="c5bf9-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5bf9-104">Šioje temoje aiškinama, kaip kurti kaupimo schemą.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="c5bf9-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c5bf9-106">Eikite į **Naršymo sritis > Moduliai > Bendroji didžioji knyga > Žurnalo sąranka > Kaupimo schemos**.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="c5bf9-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-107">Select **New**.</span></span>
3. <span data-ttu-id="c5bf9-108">Lauke **Kaupimo identifikavimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="c5bf9-109">Lauke **Kaupimo schemos aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="c5bf9-110">Lauke **Debetas”** nurodykite pageidaujamas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="c5bf9-111">Nurodyta pagrindinė sąskaita žurnalo kvito eilutėje pakeis debeto pagrindinę sąskaitą, be to ji bus naudojama atšaukiant atidėjimą pagal DK kaupimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="c5bf9-112">Lauke **Kreditas”** nurodykite pageidaujamas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="c5bf9-113">Nurodyta pagrindinė sąskaita žurnalo kvito eilutėje pakeis kredito pagrindinę sąskaitą, be to ji bus naudojama atšaukiant atidėjimą pagal DK kaupimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="c5bf9-114">Lauke **Kvitas** pasirinkite, kaip norite apibrėžti kvitą, kaip užregistruojamos operacijos.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="c5bf9-115">Lauke **Aprašas** įveskite reikšmę, aprašančią sandorius, kurie bus registruojami.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="c5bf9-116">Lauke **Laikotarpio dažnumas** pasirinkite, kaip dažnai operacijos turi vykti.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="c5bf9-117">Lauke **Įvykių skaičius pagal laikotarpį** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="c5bf9-118">Lauke **Registruoti sandorius** pasirinkite, kada operacijos turi būti registruojamos, pavyzdžiui, **Kas mėnesį**.</span><span class="sxs-lookup"><span data-stu-id="c5bf9-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>

