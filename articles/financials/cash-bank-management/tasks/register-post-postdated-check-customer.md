---
title: Registruoti kliento vėlesnį čekį
description: Galite užregistruoti išsamią vėlesnio čekio informaciją, gautą iš kliento.
author: kweekley
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 131e4f364c62d03b95fb4b77f472828b9483d5e1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "347381"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="caef3-103">Registruoti kliento vėlesnį čekį</span><span class="sxs-lookup"><span data-stu-id="caef3-103">Register and post a postdated check for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="caef3-104">Galite užregistruoti išsamią vėlesnio čekio informaciją, gautą iš kliento.</span><span class="sxs-lookup"><span data-stu-id="caef3-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="caef3-105">Taip pat galite užregistruoti vėlesnį čekį ir sugeneruoti finansines operacijas.</span><span class="sxs-lookup"><span data-stu-id="caef3-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="caef3-106">Prieš registruodami iš kliento gautą vėlesnį čekį, gautas iš kliento, atlikite šias užduotis:  • Nustatykite vėlesnį čekį puslapyje Grynųjų pinigų ir banko valdymas • Nustatykite vėlesnių čekių apmokėjimo būdą  Šios procedūros vaidmuo yra Iždininkas.</span><span class="sxs-lookup"><span data-stu-id="caef3-106">Complete the following tasks before you register and post a postdated check received from a customer:   • Set up postdated check in the Cash and bank management page • Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="caef3-107">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="caef3-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="caef3-108">Pasirinkite Gautinos sumos > Mokėjimai > Mokėjimų žurnalas.</span><span class="sxs-lookup"><span data-stu-id="caef3-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="caef3-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="caef3-109">Click New.</span></span>
3. <span data-ttu-id="caef3-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="caef3-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="caef3-111">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="caef3-111">Click Lines.</span></span>
5. <span data-ttu-id="caef3-112">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="caef3-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="caef3-113">Lauke Sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="caef3-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="caef3-114">Lauke Kreditas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="caef3-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="caef3-115">Įveskite vėlesniame čekyje nurodytą sumą.</span><span class="sxs-lookup"><span data-stu-id="caef3-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="caef3-116">Spustelėkite skirtuką Mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="caef3-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="caef3-117">Lauke Mokėjimo būdas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="caef3-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="caef3-118">Vėlesnio čekio mokėjimo būdo pasirinkimas.</span><span class="sxs-lookup"><span data-stu-id="caef3-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="caef3-119">Spustelėkite skirtuką Vėlesni čekiai.</span><span class="sxs-lookup"><span data-stu-id="caef3-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="caef3-120">Lauke Mokėjimo termino data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="caef3-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="caef3-121">Įveskite vėlesnio čekio apmokėjimo termino datą.</span><span class="sxs-lookup"><span data-stu-id="caef3-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="caef3-122">Lauke Išduodančio banko filialas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="caef3-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="caef3-123">Įveskite vėlesnio čekio banko informaciją.</span><span class="sxs-lookup"><span data-stu-id="caef3-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="caef3-124">Čekio numerio lauke įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="caef3-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="caef3-125">Lauke Išduodančio banko pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="caef3-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="caef3-126">Įveskite vėlesnio čekio banko informaciją.</span><span class="sxs-lookup"><span data-stu-id="caef3-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="caef3-127">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="caef3-127">Click Post.</span></span>
16. <span data-ttu-id="caef3-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="caef3-128">Close the page.</span></span>

