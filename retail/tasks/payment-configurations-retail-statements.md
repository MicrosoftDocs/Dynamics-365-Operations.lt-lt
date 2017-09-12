--- 
title: " Mažmeninės prekybos išrašų mokėjimo konfigūracijos"
description: "Ši procedūra nurodo mažmeninės prekybos parduotuvės mokėjimo metodų konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami mažmeninės prekybos išrašai."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6305eecebdd53f85167a0a60e11f1989f9f073c8
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="1b1eb-103"> Mažmeninės prekybos išrašų mokėjimo konfigūracijos</span><span class="sxs-lookup"><span data-stu-id="1b1eb-103">Payment configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1b1eb-104">Ši procedūra nurodo mažmeninės prekybos parduotuvės mokėjimo metodų konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami mažmeninės prekybos išrašai.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="1b1eb-105">Šiame įraše naudojama demonstracinė įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="1b1eb-106">Eikite į Mažmeninė prekyba ir prekyba > Kanalai > Mažmeninės prekybos parduotuvės > Visos mažmeninės prekybos parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="1b1eb-107">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1b1eb-108">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1b1eb-109">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="1b1eb-110">Spustelėkite Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-110">Click Payment methods.</span></span>
6. <span data-ttu-id="1b1eb-111">Išplėskite arba sutraukite sekciją Registravimas.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="1b1eb-112">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-112">Click Edit.</span></span>
    * <span data-ttu-id="1b1eb-113">Pasirinkite, ar naudojant šį mokėjimo būdą gautos sumos turi būti registruojamos į DK sąskaitą, ar į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="1b1eb-114">Pasirinkite sąskaitą, į kurią bus registruojamos sumos, gautos naudojant šį mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="1b1eb-115">Pasirinkite, į kurią sąskaitą registruoti galimus skirtumus tarp bendros gautos operacijos sumos ir šio mokėjimo būdo apskaičiuotos sumos.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="1b1eb-116">Šiame lauke galite įvesti sumą, norėdami valdyti, kada skirtumo sumą reikia registruoti kitoje skirtumo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="1b1eb-117">Šią parinktį galite naudoti, norėdami sekti didelius skirtumus.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="1b1eb-118">Pasirinkite, į kurią sąskaitą registruoti galimus skirtumus tarp bendros gautos operacijos sumos ir apskaičiuotos sumos, kai viršijama lauke „Didžiausia galima skirtumo suma“ reikšmė.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="1b1eb-119">Pasirinkite „Taip“, jei inkasavimo sumas norite registruoti atskiroje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-119">Select "Yes" to post bank drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="1b1eb-120">Šiame lauke galite pasirinkti, ar inkasavimo sumos turi būti registruojamos į DK sąskaitą, ar į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="1b1eb-121">Pasirinkite, į kurią sąskaitą norite registruoti inkasavimo sumas.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="1b1eb-122">Pasirinkite banko operacijos tipą, kuris bus naudojamas inkasavimo sumas registruojant į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="1b1eb-123">Pasirinkite „Taip“, jei pinigų įnešimo į įmonės kasą sumas norite registruoti atskiroje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-123">Select "Yes" to post safe drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="1b1eb-124">Pasirinkite, ar pinigų įnešimo į įmonės kasą sumos turi būti registruojamos į DK sąskaitą, ar į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="1b1eb-125">Pasirinkite, į kurią sąskaitą registruoti įnešimo į įmonės kasą sumas.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="1b1eb-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1b1eb-126">Click Save.</span></span>


