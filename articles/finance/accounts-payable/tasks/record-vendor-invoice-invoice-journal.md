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
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140380"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="f4d40-103">Įrašyti tiekėjo SF į SF žurnalą</span><span class="sxs-lookup"><span data-stu-id="f4d40-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4d40-104">Šis užduočių vadovas parodys, kaip įrašyti tiekėjo SF, kurios nėra susietos su pirkimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="f4d40-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="f4d40-105">Šio tipo SF pavyzdžiai yra tiekimo ar paslaugų išlaidos.</span><span class="sxs-lookup"><span data-stu-id="f4d40-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="f4d40-106">Šiame įraše naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="f4d40-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="f4d40-107">Eikite į **Naršymo sritis > Moduliai > Mokėtinos sumos > Darbo sritys > Tiekėjo SF įrašas**.</span><span class="sxs-lookup"><span data-stu-id="f4d40-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="f4d40-108">**Veiksmų srityje** spustelėkite **Naujas SF žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="f4d40-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="f4d40-109">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f4d40-109">Click **New**.</span></span>
4. <span data-ttu-id="f4d40-110">Lauke **Pavadinimas** įveskite žurnalo pavadinimą arba spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f4d40-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="f4d40-111">Lauke **Aprašymas įveskite**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f4d40-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="f4d40-112">**Veiksmų srityje** spustelėkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="f4d40-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="f4d40-113">Lauke **Data**įveskite registravimo datą, kuri atnaujins DK.</span><span class="sxs-lookup"><span data-stu-id="f4d40-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="f4d40-114">Lauke **Sąskaita** turi būti nurodyta **Tiekėjo sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="f4d40-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="f4d40-115">Lauke **Sąskaita faktūra** įveskite SF numerį.</span><span class="sxs-lookup"><span data-stu-id="f4d40-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="f4d40-116">Lauke **Aprašymas įveskite**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f4d40-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="f4d40-117">Lauke **Kreditas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="f4d40-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="f4d40-118">Lauke **Korespondentinė sąskaita** įveskite sąskaitos numerį arba spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą</span><span class="sxs-lookup"><span data-stu-id="f4d40-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="f4d40-119">Pagal numatytąsias nuostatas bus naudojama tokia pati **PVM grupė**, kaip ir tiekėjo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="f4d40-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="f4d40-120">Pagal numatytąsias nuostatas bus naudojama tokia pati **Prekės PVM grupė**, kaip ir pagrindinėje sąskaitoje, nurodytoje lauke **Korespondentinė sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="f4d40-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="f4d40-121">**Terminas** bus apskaičiuotas remiantis mokėjimo sąlygomis.</span><span class="sxs-lookup"><span data-stu-id="f4d40-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="f4d40-122">Pagal numatytąsias nuostatas bus naudojama tokia pati **Mokėjimo nuolaida** kaip ir tiekėjo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="f4d40-122">The **Cash discount** will default from the Vendor account.</span></span>  
12. <span data-ttu-id="f4d40-123">Spustelėkite **Registruoti.**</span><span class="sxs-lookup"><span data-stu-id="f4d40-123">Click **Post**.</span></span>
13. <span data-ttu-id="f4d40-124">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f4d40-124">Close the page.</span></span>

