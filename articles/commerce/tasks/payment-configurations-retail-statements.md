---
title: " Mažmeninės prekybos išrašų mokėjimo konfigūracijos"
description: Šioje procedūroje parodomos „Commerce“ parduotuvės mokėjimo metodų konfigūracijos, kurios turi įtakos ataskaitų kūrimui ir paskelbimui.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b1fc042bff4d801ae893b0370b67cd8e11ba95f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982320"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="e9db8-103"> Mažmeninės prekybos išrašų mokėjimo konfigūracijos</span><span class="sxs-lookup"><span data-stu-id="e9db8-103">Payment configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9db8-104">Šioje procedūroje parodomos „Commerce“ parduotuvės mokėjimo metodų konfigūracijos, kurios turi įtakos ataskaitų kūrimui ir paskelbimui.</span><span class="sxs-lookup"><span data-stu-id="e9db8-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="e9db8-105">Šiame įraše naudojama demonstracinė įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="e9db8-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="e9db8-106">Eikite į „Retail and Commerce“ > Kanalai > Parduotuvės > Visos parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="e9db8-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="e9db8-107">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="e9db8-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e9db8-108">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="e9db8-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e9db8-109">Veiksmų srityje spustelėkite Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="e9db8-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="e9db8-110">Spustelėkite Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="e9db8-110">Click Payment methods.</span></span>
6. <span data-ttu-id="e9db8-111">Išplėskite arba sutraukite sekciją Registravimas.</span><span class="sxs-lookup"><span data-stu-id="e9db8-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="e9db8-112">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="e9db8-112">Click Edit.</span></span>
    * <span data-ttu-id="e9db8-113">Pasirinkite, ar naudojant šį mokėjimo būdą gautos sumos turi būti registruojamos į DK sąskaitą, ar į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="e9db8-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="e9db8-114">Pasirinkite sąskaitą, į kurią bus registruojamos sumos, gautos naudojant šį mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="e9db8-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="e9db8-115">Pasirinkite, į kurią sąskaitą registruoti galimus skirtumus tarp bendros gautos operacijos sumos ir šio mokėjimo būdo apskaičiuotos sumos.</span><span class="sxs-lookup"><span data-stu-id="e9db8-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="e9db8-116">Šiame lauke galite įvesti sumą, norėdami valdyti, kada skirtumo sumą reikia registruoti kitoje skirtumo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="e9db8-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="e9db8-117">Šią parinktį galite naudoti, norėdami sekti didelius skirtumus.</span><span class="sxs-lookup"><span data-stu-id="e9db8-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="e9db8-118">Pasirinkite, į kurią sąskaitą registruoti galimus skirtumus tarp bendros gautos operacijos sumos ir apskaičiuotos sumos, kai viršijama lauke „Didžiausia galima skirtumo suma“ reikšmė.</span><span class="sxs-lookup"><span data-stu-id="e9db8-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="e9db8-119">Pasirinkite „Taip“, jei inkasavimo sumas norite registruoti atskiroje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="e9db8-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="e9db8-120">Šiame lauke galite pasirinkti, ar inkasavimo sumos turi būti registruojamos į DK sąskaitą, ar į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="e9db8-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="e9db8-121">Pasirinkite, į kurią sąskaitą norite registruoti inkasavimo sumas.</span><span class="sxs-lookup"><span data-stu-id="e9db8-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="e9db8-122">Pasirinkite banko operacijos tipą, kuris bus naudojamas inkasavimo sumas registruojant į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="e9db8-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="e9db8-123">Pasirinkite „Taip“, jei pinigų įnešimo į įmonės kasą sumas norite registruoti atskiroje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="e9db8-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="e9db8-124">Pasirinkite, ar pinigų įnešimo į įmonės kasą sumos turi būti registruojamos į DK sąskaitą, ar į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="e9db8-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="e9db8-125">Pasirinkite, į kurią sąskaitą registruoti įnešimo į įmonės kasą sumas.</span><span class="sxs-lookup"><span data-stu-id="e9db8-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="e9db8-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="e9db8-126">Click Save.</span></span>

