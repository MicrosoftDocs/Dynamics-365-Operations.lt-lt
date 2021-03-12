---
title: Kliento mokėjimo būdo nustatymas
description: Šioje temoje aiškinama, kaip sukurti mokėjimo būdą kliento mokėjimams.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a948bf772e55f20c7010101fd11da83940a0b268
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990971"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="a79a5-103">Kliento mokėjimo būdo nustatymas</span><span class="sxs-lookup"><span data-stu-id="a79a5-103">Establish customer method of payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a79a5-104">Šioje temoje aiškinama, kaip sukurti mokėjimo būdą kliento mokėjimams.</span><span class="sxs-lookup"><span data-stu-id="a79a5-104">This topic explains how to create a method of payment for customer payments.</span></span> <span data-ttu-id="a79a5-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="a79a5-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a79a5-106">Naršymo srityje eikite į **Moduliai > Gautinos sumos > Mokėjimų sąranką > Mokėjimo būdai**.</span><span class="sxs-lookup"><span data-stu-id="a79a5-106">In the navigation pane, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="a79a5-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a79a5-107">Select **New**.</span></span>
3. <span data-ttu-id="a79a5-108">Lauke **Mokėjimo būdas** įveskite mokėjimo būdo ID.</span><span class="sxs-lookup"><span data-stu-id="a79a5-108">In the **Method of payment** field, enter an ID for the method of payment.</span></span> <span data-ttu-id="a79a5-109">Mokėjimo būdo ID rodomas SF ir mokėjimuose, todėl nurodykite jį pakankamai aprašomąjį, kad suprastumėte, kokio tipo mokėjimas registruojamas, ir kokios banko sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="a79a5-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="a79a5-110">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="a79a5-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="a79a5-111">Pasirinkite, kokios reikia mokėjimo būsenos, kad būtų galima registruoti mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="a79a5-111">Select what payment status is required in order for payments to be posted.</span></span> <span data-ttu-id="a79a5-112">Kuriant kliento mokėjimą, jį registruoti galima tik kai mokėjimo būsena atitinka čia jūsų apibrėžtą mokėjimo būseną.</span><span class="sxs-lookup"><span data-stu-id="a79a5-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="a79a5-113">Pasirinkite, kaip turėtų būti kuriami klientų mokėjimai už SF.</span><span class="sxs-lookup"><span data-stu-id="a79a5-113">Select how customers payments should be created for invoices.</span></span> <span data-ttu-id="a79a5-114">Ši parinktis naudojama tik vykdant mokėjimo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="a79a5-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="a79a5-115">Klientų mokėjimams mokėjimo pasiūlymas galėtų būti naudojamas atliekant tiesioginį debetą ir išimant lėšas iš klientų bankų sąskaitų.</span><span class="sxs-lookup"><span data-stu-id="a79a5-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="a79a5-116">Pasirinkite mokėjimo tipą.</span><span class="sxs-lookup"><span data-stu-id="a79a5-116">Select the type of payment.</span></span> <span data-ttu-id="a79a5-117">Mokėjimo tipas padės nustatyti, ar bus atliekamas koks nors mokėjimo tikrinimas, ar ne.</span><span class="sxs-lookup"><span data-stu-id="a79a5-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="a79a5-118">Pasirinkite, į kokio tipo sąskaitą bus registruojami mokėjimai.</span><span class="sxs-lookup"><span data-stu-id="a79a5-118">Select what account type payments will post to.</span></span> <span data-ttu-id="a79a5-119">Paprastai šiai parinkčiai būtų pasirinkta Bankas.</span><span class="sxs-lookup"><span data-stu-id="a79a5-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="a79a5-120">Pasirinkite banko sąskaitą, į kurią bus įrašytas šis mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="a79a5-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="a79a5-121">Įveskite banko operacijų tipą, kad identifikuotumėte jūsų banko naudojamą mokėjimo tipą.</span><span class="sxs-lookup"><span data-stu-id="a79a5-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span> <span data-ttu-id="a79a5-122">Bankų operacijos tipas naudojamas bankų derinimo proceso metu ir gali derinimą palengvinti.</span><span class="sxs-lookup"><span data-stu-id="a79a5-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="a79a5-123">Pasirinkite, ar šis mokėjimas bus laikinai registruojamas tarpinėje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="a79a5-123">Select whether this payment will temporarily post to a bridging account.</span></span> <span data-ttu-id="a79a5-124">Jei norite išbandyti mokėjimo srauto laiką, kad jį patvirtintų bankas, naudokite funkciją Tarpin.</span><span class="sxs-lookup"><span data-stu-id="a79a5-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="a79a5-125">Mokėjimas bus laikinai registruojamas DK sąskaitoje tol, kol jį patvirtins bankas, o tada mokėjimas bus perkeltas į banko sąskaitą, kurią apibrėžėte čia.</span><span class="sxs-lookup"><span data-stu-id="a79a5-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="a79a5-126">Įveskite pagrindinę sąskaitą, naudojamą registruoti tarpiškai.</span><span class="sxs-lookup"><span data-stu-id="a79a5-126">Enter the main account used for the bridging posting.</span></span> <span data-ttu-id="a79a5-127">Tai yra pagrindinė sąskaita, kurioje, jei naudojama tarpinė funkcija, bus laikinai registruojamas mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="a79a5-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="a79a5-128">Norėdami apibrėžti elektroninių mokėjimų parametrą, naudokite skirtuką **Failo formatas**.</span><span class="sxs-lookup"><span data-stu-id="a79a5-128">Use the **File format** tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="a79a5-129">Norėdami apibrėžti privalomus laukus, naudokite skirtuką **Mokėjimų kontrolė**.</span><span class="sxs-lookup"><span data-stu-id="a79a5-129">Use the **Payment control** tab to define fields that are mandatory.</span></span> <span data-ttu-id="a79a5-130">Pavyzdžiui, jei reikia pervesti visus šiuo būdu atliktus mokėjimus, tokią parinktį galite pasirinkti šiame skirtuke.</span><span class="sxs-lookup"><span data-stu-id="a79a5-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="a79a5-131">Naudokite skirtuką **Mokėjimo atributai**, kad apibrėžtumėte, kuriuos šio mokėjimo būdo atributus norite naudoti.</span><span class="sxs-lookup"><span data-stu-id="a79a5-131">Use the **Payment attributes** tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="a79a5-132">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a79a5-132">Select **Save**.</span></span>

