---
title: Registruoti tiekėjo vėlesnį čekį
description: Naudodami žurnalo kvitą galite registruoti išsamią vėlesnio čekio informaciją prieš išduodami čekį tiekėjui.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 63a822350ce2bd4d673d7f9841822c84fb883601
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144192"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="d2391-103">Registruoti tiekėjo vėlesnį čekį</span><span class="sxs-lookup"><span data-stu-id="d2391-103">Register and post a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2391-104">Naudodami žurnalo kvitą galite registruoti išsamią vėlesnio čekio informaciją prieš išduodami čekį tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="d2391-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="d2391-105">Taip pat galite užregistruoti vėlesnį čekį ir sugeneruoti finansines operacijas.</span><span class="sxs-lookup"><span data-stu-id="d2391-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="d2391-106">Atlikite tolesnę užduotį prieš užregistruodami ir pateikdami vėlesnį tiekėjo čekį:</span><span class="sxs-lookup"><span data-stu-id="d2391-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="d2391-107">Nustatykite vėlesnius čekius grynųjų pinigų ir banko valdymo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="d2391-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="d2391-108">Šio užduočių vadovo vaidmuo yra Iždininkas.</span><span class="sxs-lookup"><span data-stu-id="d2391-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="d2391-109">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="d2391-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="d2391-110">Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas</span><span class="sxs-lookup"><span data-stu-id="d2391-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="d2391-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d2391-111">Click New.</span></span>
3. <span data-ttu-id="d2391-112">Lauke Pavadinimas įveskite „VendPay“.</span><span class="sxs-lookup"><span data-stu-id="d2391-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="d2391-113">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="d2391-113">Click Lines.</span></span>
5. <span data-ttu-id="d2391-114">Lauke Sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d2391-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="d2391-115">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d2391-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="d2391-116">Lauke Debetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d2391-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="d2391-117">Lauke Mokėjimo būdas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="d2391-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d2391-118">Vėlesnio čekio mokėjimo būdo pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="d2391-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="d2391-119">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="d2391-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="d2391-120">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="d2391-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="d2391-121">Spustelėkite skirtuką Vėlesni čekiai.</span><span class="sxs-lookup"><span data-stu-id="d2391-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="d2391-122">Lauke Čekio numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d2391-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="d2391-123">Įveskite arba modifikuokite vėlesnio čekio numerį.</span><span class="sxs-lookup"><span data-stu-id="d2391-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="d2391-124">Lauke Išduodančio banko pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d2391-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="d2391-125">įveskite išduodančio banko informaciją.</span><span class="sxs-lookup"><span data-stu-id="d2391-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="d2391-126">Spustelėkite skirtuką Sąrašas.</span><span class="sxs-lookup"><span data-stu-id="d2391-126">Click the List tab.</span></span>
15. <span data-ttu-id="d2391-127">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="d2391-127">Click Post.</span></span>
16. <span data-ttu-id="d2391-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d2391-128">Close the page.</span></span>
17. <span data-ttu-id="d2391-129">Spustelėkite skirtuką Vėlesni čekiai.</span><span class="sxs-lookup"><span data-stu-id="d2391-129">Click the Postdated checks tab.</span></span>

