---
title: Darbininkams paskolintų prekių valdymas
description: Panaudos objektai yra įrašai, kurie vadovams padeda sekti fizines prekes, kurias įmonė skolina savo darbuotojams.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: d34551e4a3cc08ce3fe47e8f8fd2c3cc68c0daf7
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130138"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="590c6-103">Darbininkams paskolintų prekių valdymas</span><span class="sxs-lookup"><span data-stu-id="590c6-103">Manage items that are lent to workers</span></span>

<span data-ttu-id="590c6-104">Panaudos objektai yra įrašai, kurie vadovams padeda sekti fizines prekes, kurias įmonė skolina savo darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="590c6-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="590c6-105">Toliau pateiktuose punktuose nurodomi elementų, kuriuos įmonė gali paskolinti darbuotojams, pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="590c6-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="590c6-106">Mobilieji telefonai;</span><span class="sxs-lookup"><span data-stu-id="590c6-106">Mobile telephones</span></span>
-   <span data-ttu-id="590c6-107">Automobiliai;</span><span class="sxs-lookup"><span data-stu-id="590c6-107">Automobiles</span></span>
-   <span data-ttu-id="590c6-108">Kompiuterinė įranga.</span><span class="sxs-lookup"><span data-stu-id="590c6-108">Computer equipment</span></span>

<span data-ttu-id="590c6-109">Kiekviena fizinė prekė turi turėti atitinkamą panaudos objektą.</span><span class="sxs-lookup"><span data-stu-id="590c6-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="590c6-110">Kiekviename panaudos objekto įraše turi būti aprašyta, kas skolinama, kas atsakingas už panaudą ir galimas dienų, kada objektas paskolintas darbuotojui, skaičius.</span><span class="sxs-lookup"><span data-stu-id="590c6-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="590c6-111">Vienu kartu galite sukurti keletą tokių objektų kaip raktai, įėjimo kortelės ar uniformos panaudos objektų.</span><span class="sxs-lookup"><span data-stu-id="590c6-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="590c6-112">Skolindami objektą, įveskite skolinimo datą ir planuojamą grąžinimo datą.</span><span class="sxs-lookup"><span data-stu-id="590c6-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="590c6-113">Kai objektas grąžinamas, įveskite faktinę grąžinimo datą.</span><span class="sxs-lookup"><span data-stu-id="590c6-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="590c6-114">Darbuotojai peržiūrėti objektų, kurie jiems buvo paskolinti, įrašus gali naudodami darbo sritį Darbuotojų savitarna.</span><span class="sxs-lookup"><span data-stu-id="590c6-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="590c6-115">Jei darbuotojai gavo papildomų faktinių objektų, jie taip pat gali redaguoti esamus įrašus arba įvesti naujų panaudos objektų.</span><span class="sxs-lookup"><span data-stu-id="590c6-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="590c6-116">Galima nustatyti darbo eigą, kad, naudojant patvirtinimo procesą, pakeitimus būtų galima nukreipti į naujus arba esamus panaudos objektus.</span><span class="sxs-lookup"><span data-stu-id="590c6-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="590c6-117">Vadovai gali peržiūrėti savo tiesioginių ataskaitų panaudos objektus.</span><span class="sxs-lookup"><span data-stu-id="590c6-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="590c6-118">Jiems taip pat gali būti suteikta teisė darbuotojų vardu pridėti naujų panaudos objektų.</span><span class="sxs-lookup"><span data-stu-id="590c6-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="590c6-119"> Pamestų arba negrąžintų panaudos objektų sąskaita</span><span class="sxs-lookup"><span data-stu-id="590c6-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="590c6-120">Jei objektas sugadinamas arba negrąžinamas, įveskite fiktyvų grąžinimo įrašą.</span><span class="sxs-lookup"><span data-stu-id="590c6-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="590c6-121">Tada panaikinkite objektą arba saugokite peržiūroje ir pakeiskite aprašymą, kad matytumėte, jog objekto nėra.</span><span class="sxs-lookup"><span data-stu-id="590c6-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="590c6-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="590c6-122">Additional resources</span></span>
--------

[<span data-ttu-id="590c6-123">Personalas</span><span class="sxs-lookup"><span data-stu-id="590c6-123">Human resources</span></span>](index.md)



