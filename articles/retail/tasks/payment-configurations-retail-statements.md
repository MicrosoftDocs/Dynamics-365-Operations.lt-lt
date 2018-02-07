--- 
title: " Mažmeninės prekybos išrašų mokėjimo konfigūracijos"
description: "Ši procedūra nurodo mažmeninės prekybos parduotuvės mokėjimo metodų konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami mažmeninės prekybos išrašai."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 0ffd6dc5fff6d27ec3cfdcd68c53b2299c4100b9
ms.contentlocale: lt-lt
ms.lasthandoff: 02/07/2018

---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="f29b7-103"> Mažmeninės prekybos išrašų mokėjimo konfigūracijos</span><span class="sxs-lookup"><span data-stu-id="f29b7-103">Payment configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f29b7-104">Ši procedūra nurodo mažmeninės prekybos parduotuvės mokėjimo metodų konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami mažmeninės prekybos išrašai.</span><span class="sxs-lookup"><span data-stu-id="f29b7-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="f29b7-105">Šiame įraše naudojama demonstracinė įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="f29b7-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="f29b7-106">Eikite į Mažmeninė prekyba ir prekyba > Kanalai > Mažmeninės prekybos parduotuvės > Visos mažmeninės prekybos parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="f29b7-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="f29b7-107">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f29b7-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f29b7-108">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f29b7-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f29b7-109">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="f29b7-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="f29b7-110">Spustelėkite Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="f29b7-110">Click Payment methods.</span></span>
6. <span data-ttu-id="f29b7-111">Išplėskite arba sutraukite sekciją Registravimas.</span><span class="sxs-lookup"><span data-stu-id="f29b7-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="f29b7-112">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="f29b7-112">Click Edit.</span></span>
    * <span data-ttu-id="f29b7-113">Pasirinkite, ar naudojant šį mokėjimo būdą gautos sumos turi būti registruojamos į DK sąskaitą, ar į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="f29b7-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="f29b7-114">Pasirinkite sąskaitą, į kurią bus registruojamos sumos, gautos naudojant šį mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="f29b7-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="f29b7-115">Pasirinkite, į kurią sąskaitą registruoti galimus skirtumus tarp bendros gautos operacijos sumos ir šio mokėjimo būdo apskaičiuotos sumos.</span><span class="sxs-lookup"><span data-stu-id="f29b7-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="f29b7-116">Šiame lauke galite įvesti sumą, norėdami valdyti, kada skirtumo sumą reikia registruoti kitoje skirtumo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="f29b7-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="f29b7-117">Šią parinktį galite naudoti, norėdami sekti didelius skirtumus.</span><span class="sxs-lookup"><span data-stu-id="f29b7-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="f29b7-118">Pasirinkite, į kurią sąskaitą registruoti galimus skirtumus tarp bendros gautos operacijos sumos ir apskaičiuotos sumos, kai viršijama lauke „Didžiausia galima skirtumo suma“ reikšmė.</span><span class="sxs-lookup"><span data-stu-id="f29b7-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="f29b7-119">Pasirinkite „Taip“, jei inkasavimo sumas norite registruoti atskiroje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="f29b7-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="f29b7-120">Šiame lauke galite pasirinkti, ar inkasavimo sumos turi būti registruojamos į DK sąskaitą, ar į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="f29b7-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="f29b7-121">Pasirinkite, į kurią sąskaitą norite registruoti inkasavimo sumas.</span><span class="sxs-lookup"><span data-stu-id="f29b7-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="f29b7-122">Pasirinkite banko operacijos tipą, kuris bus naudojamas inkasavimo sumas registruojant į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="f29b7-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="f29b7-123">Pasirinkite „Taip“, jei pinigų įnešimo į įmonės kasą sumas norite registruoti atskiroje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="f29b7-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="f29b7-124">Pasirinkite, ar pinigų įnešimo į įmonės kasą sumos turi būti registruojamos į DK sąskaitą, ar į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="f29b7-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="f29b7-125">Pasirinkite, į kurią sąskaitą registruoti įnešimo į įmonės kasą sumas.</span><span class="sxs-lookup"><span data-stu-id="f29b7-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="f29b7-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f29b7-126">Click Save.</span></span>


