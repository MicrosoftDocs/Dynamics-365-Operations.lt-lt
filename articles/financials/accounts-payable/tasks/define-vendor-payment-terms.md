--- 
title: "Nustatyti tiekėjo mokėjimo sąlygas"
description: "Nustatykite tiekėjų SF mokėjimo sąlygas."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 28de122f8742e16731387a63beb12ae774d4d9c1
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="996fc-103">Nustatyti tiekėjo mokėjimo sąlygas</span><span class="sxs-lookup"><span data-stu-id="996fc-103">Define vendor payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="996fc-104">Nustatykite tiekėjų SF mokėjimo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="996fc-104">Set up payment terms for vendor invoices.</span></span> <span data-ttu-id="996fc-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="996fc-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="996fc-106">Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo sąlygos.</span><span class="sxs-lookup"><span data-stu-id="996fc-106">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="996fc-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="996fc-107">Click New.</span></span>
    * <span data-ttu-id="996fc-108">Mokėjimo sąlygų puslapis naudojamas apibrėžti, kaip bus skaičiuojamas terminas.</span><span class="sxs-lookup"><span data-stu-id="996fc-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="996fc-109">Ji nenaudojamas apibrėžti, kaip bus skaičiuojama mokėjimo nuolaidos data.</span><span class="sxs-lookup"><span data-stu-id="996fc-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="996fc-110">Lauke Mokėjimo sąlygos surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="996fc-110">In the Terms of payment field, type a value.</span></span>
4. <span data-ttu-id="996fc-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="996fc-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="996fc-112">Lauke Dienos įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="996fc-112">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="996fc-113">Čia įvestas skaičius bus pridedamas prie termino arba prie laikotarpio, nurodyto srityje Mokėjimo būdas.</span><span class="sxs-lookup"><span data-stu-id="996fc-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="996fc-114">Pvz., pasirinkus Grynasis, skaičius bus pridėtas prie termino.</span><span class="sxs-lookup"><span data-stu-id="996fc-114">For example, if you select Net, the number will be added to the due date.</span></span> <span data-ttu-id="996fc-115">Jei pasirinksite Dabartinis mėnuo, skaičius bus pridedamas prie dabartinio mėnesio paskutinės dienos, kad būtų apskaičiuota termino pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="996fc-115">If you select Current month, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="996fc-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="996fc-116">Click Save.</span></span>
7. <span data-ttu-id="996fc-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="996fc-117">Close the page.</span></span>
8. <span data-ttu-id="996fc-118">Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo nuolaidos.</span><span class="sxs-lookup"><span data-stu-id="996fc-118">Go to Accounts payable > Payment setup > Cash discounts.</span></span>
9. <span data-ttu-id="996fc-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="996fc-119">Click New.</span></span>
10. <span data-ttu-id="996fc-120">Lauke Mokėjimo nuolaida įveskite ID.</span><span class="sxs-lookup"><span data-stu-id="996fc-120">In the Cash discount field, enter an ID.</span></span>
11. <span data-ttu-id="996fc-121">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="996fc-121">In the Description field, type a value.</span></span>
12. <span data-ttu-id="996fc-122">Jei tiekėjas siūlo pakopinę nuolaidą, baigus galioti dabartinei nuolaidai, pasirinkite kitą mokėjimo nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="996fc-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="996fc-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="996fc-123">Close the page.</span></span>
14. <span data-ttu-id="996fc-124">Lauke Dienos įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="996fc-124">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="996fc-125">Kiekis, įvestas lauke Dienos, pagal tai, kokia parinktis buvo pasirinkta lauke Grynasis / dabartinis, bus naudojamas skaičiuoti mokėjimo nuolaidos datai.</span><span class="sxs-lookup"><span data-stu-id="996fc-125">The quantity entered in the Days field will be used to calculate the Cash discount date, based on what option was selected in the Net/Current field.</span></span> <span data-ttu-id="996fc-126">Jei buvo pasirinktas Grynasis, norint nustatyti mokėjimo nuolaidos datą, kiekis bus pridėtas prie SF datos.</span><span class="sxs-lookup"><span data-stu-id="996fc-126">If Net was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="996fc-127">Jei buvo pasirinktas Dabartinis mėnuo, norint nustatyti mokėjimo nuolaidos datą, kiekis bus pridėtas prie dabartinio mėnesio pabaigos.</span><span class="sxs-lookup"><span data-stu-id="996fc-127">If Current month was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="996fc-128">Lauke Nuolaida įveskite mokėjimo nuolaidos procentą.</span><span class="sxs-lookup"><span data-stu-id="996fc-128">Enter the percentage of the cash discount in the Discount field.</span></span> 
16. <span data-ttu-id="996fc-129">Įveskite pagrindinę sąskaitą, kurioje bus registruojama klientų SF mokėjimo nuolaida.</span><span class="sxs-lookup"><span data-stu-id="996fc-129">Enter the main account to which the cash discount will be posted for customer invoices.</span></span>
17. <span data-ttu-id="996fc-130">Įveskite pagrindinę sąskaitą, kurioje bus registruojama tiekėjų SF mokėjimo nuolaida.</span><span class="sxs-lookup"><span data-stu-id="996fc-130">Enter the main account to which the cash discount will be posted for vendor invoices.</span></span>
    * <span data-ttu-id="996fc-131">Jei srityje Taikyti nuolaidą korespondentinėms sąskaitoms nustatyta Tiekėjo SF naudoti pagrindinę sąskaitą, bus naudojama pagrindinė sąskaita.</span><span class="sxs-lookup"><span data-stu-id="996fc-131">If 'Discount offset accounts' is set to Use main account for vendor discount, then the Main account will be used.</span></span>  <span data-ttu-id="996fc-132">Jei parinktis nustatyta į Sąskaitos SF eilutėse, mokėjimo nuolaida bus registruojama turto / išlaidų sąskaitose, esančiose SF eilutėse.</span><span class="sxs-lookup"><span data-stu-id="996fc-132">If the option is set to Accounts on the invoice lines, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
18. <span data-ttu-id="996fc-133">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="996fc-133">Click Save.</span></span>


