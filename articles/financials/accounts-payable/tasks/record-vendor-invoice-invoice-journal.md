--- 
title: "Įrašyti tiekėjo SF į SF žurnalą"
description: "Šis užduočių vadovas parodys, kaip įrašyti tiekėjo SF, kurios nėra susietos su pirkimo užsakymais."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 26515140b020d824f99441b9f1ee560a44e28f8f
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="c119c-103">Įrašyti tiekėjo SF į SF žurnalą</span><span class="sxs-lookup"><span data-stu-id="c119c-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c119c-104">Šis užduočių vadovas parodys, kaip įrašyti tiekėjo SF, kurios nėra susietos su pirkimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="c119c-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="c119c-105">Šio tipo SF pavyzdžiai yra tiekimo ar paslaugų išlaidos.</span><span class="sxs-lookup"><span data-stu-id="c119c-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="c119c-106">Šiame įraše naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="c119c-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="c119c-107">Pasirinkite Mokėtinos sumos > Darbo sritis > Tiekėjo SF įrašas.</span><span class="sxs-lookup"><span data-stu-id="c119c-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="c119c-108">Spustelėkite Naujas SF žurnalas.</span><span class="sxs-lookup"><span data-stu-id="c119c-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="c119c-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c119c-109">Click New.</span></span>
4. <span data-ttu-id="c119c-110">Lauke Pavadinimas įveskite žurnalo pavadinimą arba spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="c119c-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="c119c-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c119c-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="c119c-112">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="c119c-112">Click Lines.</span></span>
    * <span data-ttu-id="c119c-113">Lauke Data įveskite registravimo datą, kuri atnaujins DK.</span><span class="sxs-lookup"><span data-stu-id="c119c-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="c119c-114">Lauke Sąskaita nurodykite tiekėjo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="c119c-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="c119c-115">Lauke Sąskaita faktūra įveskite SF numerį.</span><span class="sxs-lookup"><span data-stu-id="c119c-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="c119c-116">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c119c-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="c119c-117">Lauke Kreditas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c119c-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="c119c-118">Lauke Korespondentinė sąskaita įveskite sąskaitos numerį arba spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą</span><span class="sxs-lookup"><span data-stu-id="c119c-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="c119c-119">Pagal numatytąsias nuostatas bus naudojama tokia pati PVM grupė, kaip ir tiekėjo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="c119c-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="c119c-120">Pagal numatytąsias nuostatas bus naudojama tokia pati grupė Prekių PVM, kaip ir pagrindinėje sąskaitoje, nurodytoje lauke Korespondentinė sąskaita.</span><span class="sxs-lookup"><span data-stu-id="c119c-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="c119c-121">Terminas bus apskaičiuotas remiantis mokėjimo sąlygomis.</span><span class="sxs-lookup"><span data-stu-id="c119c-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="c119c-122">Pagal numatytąsias nuostatas bus naudojama tokia pati mokėjimo nuolaida kaip ir tiekėjo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="c119c-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="c119c-123">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="c119c-123">Click Post.</span></span>
13. <span data-ttu-id="c119c-124">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c119c-124">Close the page.</span></span>


