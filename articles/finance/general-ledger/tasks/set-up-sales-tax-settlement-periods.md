---
title: PVM sudengimo laikotarpių nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti PVM sudengimo laikotarpius sistemoje „Dynamics 365 Finance“.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd11068a31b5324d87416e7c00f75a59743f695a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813512"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="4308c-103">PVM sudengimo laikotarpių nustatymas</span><span class="sxs-lookup"><span data-stu-id="4308c-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4308c-104">Šioje temoje paaiškinta, kaip nustatyti PVM sudengimo laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="4308c-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="4308c-105">PVM sudengimo laikotarpiuose pateikiama informacija apie laikotarpių intervalus, už kuriuos reikia pranešti apie PVM ir jį sumokėti.</span><span class="sxs-lookup"><span data-stu-id="4308c-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="4308c-106">Galima vykdyti konkrečios datos intervalo sudengimo laikotarpio procesą.</span><span class="sxs-lookup"><span data-stu-id="4308c-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="4308c-107">Bus sudengti visi mokesčių kodai, susieti su sudengimo laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="4308c-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="4308c-108">Atsižvelgiant į susijusios PVM institucijos sąranką, mokestiniai įsipareigojimai registruojami arba tiekėjui, arba DK sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="4308c-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="4308c-109">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="4308c-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="4308c-110">Naršymo srityje eikite į **Moduliai > Mokestis > Netiesioginiai mokesčiai > PVM > PVM sudengimo laikotarpiai**.</span><span class="sxs-lookup"><span data-stu-id="4308c-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="4308c-111">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="4308c-111">Select **New**.</span></span>
3. <span data-ttu-id="4308c-112">Lauke **Sudengimo laikotarpis** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4308c-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="4308c-113">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4308c-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="4308c-114">Lauke **Institucija** pasirinkite PVM instituciją, kuri gauna už sudengimo laikotarpį sukurtas ataskaitas ir mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="4308c-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="4308c-115">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="4308c-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4308c-116">Lauke **Mokėjimo sąlygos** iš išplečiamojo meniu pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="4308c-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="4308c-117">Susijusią PVM instituciją galima nustatyti kaip tiekėją ir, sudengiant PVM, bus sukurta atidaryta tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="4308c-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="4308c-118">Mokėjimo sąlygos apibrėžia atidarytos tiekėjo SF terminą.</span><span class="sxs-lookup"><span data-stu-id="4308c-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="4308c-119">Pasirinkite sudengimo laikotarpių intervalų tipą.</span><span class="sxs-lookup"><span data-stu-id="4308c-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="4308c-120">Įveskite laikotarpio intervalo vienetų skaičių vienam laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="4308c-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="4308c-121">Pavyzdžiui, ketvirtį sudaro 3 mėnesiai.</span><span class="sxs-lookup"><span data-stu-id="4308c-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="4308c-122">Pažymėkite arba išvalykite žymės langelį **Sudengiant PVM naudoti paketinį apdorojimą**.</span><span class="sxs-lookup"><span data-stu-id="4308c-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="4308c-123">Sudengimo laikotarpio procesą galima apdoroti kaip paketinę užduotį fone.</span><span class="sxs-lookup"><span data-stu-id="4308c-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="4308c-124">Tai rekomenduojama atlikti su daug mokesčių operacijų, patenkančių į laikotarpio intervalą.</span><span class="sxs-lookup"><span data-stu-id="4308c-124">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="4308c-125">Šiuo metu ši funkcija nepalaikoma Ispanijoje, Japonijoje ir Nyderlanduose.</span><span class="sxs-lookup"><span data-stu-id="4308c-125">Currently this is not supported in Spain, Japan, and the Netherlands.</span></span>
11. <span data-ttu-id="4308c-126">Pažymėkite arba išvalykite žymės langelį **Neleisti generuoti korespondentinių mokesčių operacijų**.</span><span class="sxs-lookup"><span data-stu-id="4308c-126">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="4308c-127">Pagal numatytuosius parametrus sudengimo proceso metu sistema generuoja korespondentines mokesčių operacijas, galinčias sukelti našumo problemų, jei laikotarpio intervale yra daug mokesčių operacijų.</span><span class="sxs-lookup"><span data-stu-id="4308c-127">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="4308c-128">Norėdami neleisti generuoti korespondentinių mokesčių operacijų pažymėkite šį žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="4308c-128">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="4308c-129">Išplėskite skirtuką **Laikotarpio intervalai**.</span><span class="sxs-lookup"><span data-stu-id="4308c-129">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="4308c-130">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="4308c-130">Select **Add**.</span></span>
14. <span data-ttu-id="4308c-131">Lauke **Pradžios data** naujoje eilutėje įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="4308c-131">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="4308c-132">Lauke **Pabaigos data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="4308c-132">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="4308c-133">Pasirinkite **Naujo laikotarpio intervalas**.</span><span class="sxs-lookup"><span data-stu-id="4308c-133">Select **New period interval**.</span></span> <span data-ttu-id="4308c-134">Įvedus pirmąjį laikotarpio intervalą, galima automatiškai kurti naujus laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="4308c-134">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="4308c-135">Jei reikia, galite grįžti ir pridėti naujų laikotarpių intervalų.</span><span class="sxs-lookup"><span data-stu-id="4308c-135">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="4308c-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4308c-136">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]