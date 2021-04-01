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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ffd482facc629e65a79f328cb237fd72f6f6b5c5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225326"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="9fc86-103">Registruoti tiekėjo vėlesnį čekį</span><span class="sxs-lookup"><span data-stu-id="9fc86-103">Register and post a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9fc86-104">Naudodami žurnalo kvitą galite registruoti išsamią vėlesnio čekio informaciją prieš išduodami čekį tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="9fc86-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="9fc86-105">Taip pat galite užregistruoti vėlesnį čekį ir sugeneruoti finansines operacijas.</span><span class="sxs-lookup"><span data-stu-id="9fc86-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="9fc86-106">Atlikite tolesnę užduotį prieš užregistruodami ir pateikdami vėlesnį tiekėjo čekį:</span><span class="sxs-lookup"><span data-stu-id="9fc86-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="9fc86-107">Nustatykite vėlesnius čekius grynųjų pinigų ir banko valdymo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9fc86-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="9fc86-108">Šio užduočių vadovo vaidmuo yra Iždininkas.</span><span class="sxs-lookup"><span data-stu-id="9fc86-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="9fc86-109">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="9fc86-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="9fc86-110">Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas</span><span class="sxs-lookup"><span data-stu-id="9fc86-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="9fc86-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="9fc86-111">Click New.</span></span>
3. <span data-ttu-id="9fc86-112">Lauke Pavadinimas įveskite „VendPay“.</span><span class="sxs-lookup"><span data-stu-id="9fc86-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="9fc86-113">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="9fc86-113">Click Lines.</span></span>
5. <span data-ttu-id="9fc86-114">Lauke Sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="9fc86-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="9fc86-115">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="9fc86-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="9fc86-116">Lauke Debetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9fc86-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="9fc86-117">Lauke Mokėjimo būdas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="9fc86-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9fc86-118">Vėlesnio čekio mokėjimo būdo pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="9fc86-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="9fc86-119">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9fc86-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9fc86-120">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="9fc86-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="9fc86-121">Spustelėkite skirtuką Vėlesni čekiai.</span><span class="sxs-lookup"><span data-stu-id="9fc86-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="9fc86-122">Lauke Čekio numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9fc86-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="9fc86-123">Įveskite arba modifikuokite vėlesnio čekio numerį.</span><span class="sxs-lookup"><span data-stu-id="9fc86-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="9fc86-124">Lauke Išduodančio banko pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9fc86-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="9fc86-125">įveskite išduodančio banko informaciją.</span><span class="sxs-lookup"><span data-stu-id="9fc86-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="9fc86-126">Spustelėkite skirtuką Sąrašas.</span><span class="sxs-lookup"><span data-stu-id="9fc86-126">Click the List tab.</span></span>
15. <span data-ttu-id="9fc86-127">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="9fc86-127">Click Post.</span></span>
16. <span data-ttu-id="9fc86-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9fc86-128">Close the page.</span></span>
17. <span data-ttu-id="9fc86-129">Spustelėkite skirtuką Vėlesni čekiai.</span><span class="sxs-lookup"><span data-stu-id="9fc86-129">Click the Postdated checks tab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]