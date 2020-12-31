---
title: Įrašyti tiekėjo SF į SF žurnalą
description: Šis užduočių vadovas parodys, kaip įrašyti tiekėjo SF, kurios nėra susietos su pirkimo užsakymais.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9f2cbe0c9d1609aa3713776f81bafa396fff301
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645286"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="85b8a-103">Įrašyti tiekėjo SF į SF žurnalą</span><span class="sxs-lookup"><span data-stu-id="85b8a-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85b8a-104">Šis užduočių vadovas parodys, kaip įrašyti tiekėjo SF, kurios nėra susietos su pirkimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="85b8a-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="85b8a-105">Šio tipo SF pavyzdžiai yra tiekimo ar paslaugų išlaidos.</span><span class="sxs-lookup"><span data-stu-id="85b8a-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="85b8a-106">Šiame įraše naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="85b8a-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="85b8a-107">Eikite į **Naršymo sritis > Moduliai > Mokėtinos sumos > Darbo sritys > Tiekėjo SF įrašas**.</span><span class="sxs-lookup"><span data-stu-id="85b8a-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="85b8a-108">**Veiksmų srityje** spustelėkite **Naujas SF žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="85b8a-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="85b8a-109">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="85b8a-109">Click **New**.</span></span>
4. <span data-ttu-id="85b8a-110">Lauke **Pavadinimas** įveskite žurnalo pavadinimą arba spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="85b8a-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="85b8a-111">Lauke **Aprašymas įveskite** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85b8a-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="85b8a-112">**Veiksmų srityje** spustelėkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="85b8a-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="85b8a-113">Lauke **Data** įveskite registravimo datą, kuri atnaujins DK.</span><span class="sxs-lookup"><span data-stu-id="85b8a-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="85b8a-114">Lauke **Sąskaita** turi būti nurodyta **Tiekėjo sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="85b8a-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="85b8a-115">Lauke **Sąskaita faktūra** įveskite SF numerį.</span><span class="sxs-lookup"><span data-stu-id="85b8a-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="85b8a-116">Lauke **Aprašymas įveskite** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85b8a-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="85b8a-117">Lauke **Kreditas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="85b8a-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="85b8a-118">Lauke **Korespondentinė sąskaita** įveskite sąskaitos numerį arba spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą</span><span class="sxs-lookup"><span data-stu-id="85b8a-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="85b8a-119">Pagal numatytąsias nuostatas bus naudojama tokia pati **PVM grupė**, kaip ir tiekėjo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="85b8a-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="85b8a-120">Pagal numatytąsias nuostatas bus naudojama tokia pati **Prekės PVM grupė**, kaip ir pagrindinėje sąskaitoje, nurodytoje lauke **Korespondentinė sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="85b8a-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="85b8a-121">**Terminas** bus apskaičiuotas remiantis mokėjimo sąlygomis.</span><span class="sxs-lookup"><span data-stu-id="85b8a-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="85b8a-122">Pagal numatytąsias nuostatas bus naudojama tokia pati **Mokėjimo nuolaida** kaip ir tiekėjo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="85b8a-122">The **Cash discount** will default from the Vendor account.</span></span>
12. <span data-ttu-id="85b8a-123">Jei įjungėte tiekėjo SF žurnalo darbo eigą, spustelėkite **Darbo eiga > Pateikti**.</span><span class="sxs-lookup"><span data-stu-id="85b8a-123">If you have enabled Vendor invoice journal workflow, click **Workflow > Submit**.</span></span>
    * <span data-ttu-id="85b8a-124">Patvirtinus jūsų pateikimą, data bus pakeista į pirmą artimiausio atviro laikotarpio dieną, jei operacijos registravimo data patenka į sulaikytą arba uždarytą DK registravimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="85b8a-124">When your submission is approved, the date will be advanced to the first day of the next open period, if the transaction posting date falls within a period that is On hold or Closed for ledger posting.</span></span>
12. <span data-ttu-id="85b8a-125">Spustelėkite **Registruoti.**</span><span class="sxs-lookup"><span data-stu-id="85b8a-125">Click **Post**.</span></span>
13. <span data-ttu-id="85b8a-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="85b8a-126">Close the page.</span></span>

