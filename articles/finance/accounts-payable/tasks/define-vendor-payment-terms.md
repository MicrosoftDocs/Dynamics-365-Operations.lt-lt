---
title: Tiekėjo mokėjimo sąlygų apibrėžimas
description: Šioje temoje aiškinama kaip nustatyti tiekėjo SF mokėjimo sąlygas.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b69b505996b5536088578885c11a7e8c27f4975
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971858"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="62380-103">Tiekėjo mokėjimo sąlygų apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="62380-103">Define vendor payment terms</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="62380-104">Šioje temoje aiškinama kaip nustatyti tiekėjo SF mokėjimo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="62380-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="62380-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="62380-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="62380-106">Pasirinkite **Naršymo sritis > Moduliai > Mokėtinos sumos > Mokėjimo konfigūracija > Mokėjimo sąlygos**.</span><span class="sxs-lookup"><span data-stu-id="62380-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="62380-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="62380-107">Select **New**.</span></span> <span data-ttu-id="62380-108">Mokėjimo sąlygų puslapis naudojamas apibrėžti, kaip bus skaičiuojamas terminas.</span><span class="sxs-lookup"><span data-stu-id="62380-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="62380-109">Ji nenaudojamas apibrėžti, kaip bus skaičiuojama mokėjimo nuolaidos data.</span><span class="sxs-lookup"><span data-stu-id="62380-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="62380-110">Lauke **Mokėjimo sąlygos** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="62380-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="62380-111">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="62380-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="62380-112">Lauke **Dienos** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="62380-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="62380-113">Čia įvestas skaičius bus pridedamas prie termino arba prie laikotarpio, nurodyto srityje Mokėjimo būdas.</span><span class="sxs-lookup"><span data-stu-id="62380-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="62380-114">Pvz., pasirinkus **Grynoji**, skaičius bus pridėtas prie termino.</span><span class="sxs-lookup"><span data-stu-id="62380-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="62380-115">Jei pasirinksite **Dabartinis mėnesis**, skaičius bus pridedamas prie dabartinio mėnesio paskutinės dienos, kad būtų apskaičiuota termino pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="62380-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="62380-116">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="62380-116">Select **Save**.</span></span>
7. <span data-ttu-id="62380-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="62380-117">Close the page.</span></span>
8. <span data-ttu-id="62380-118">Pasirinkit **Mokėtinos sumos > Mokėjimo konfigūracija > Mokėjimo nuolaida**.</span><span class="sxs-lookup"><span data-stu-id="62380-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="62380-119">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="62380-119">Select **New**.</span></span>
10. <span data-ttu-id="62380-120">Lauke **Mokėjimo nuolaida** įveskite ID.</span><span class="sxs-lookup"><span data-stu-id="62380-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="62380-121">Lauke **Aprašymas įveskite** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="62380-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="62380-122">Jei tiekėjas siūlo pakopinę nuolaidą, baigus galioti dabartinei nuolaidai, pasirinkite kitą mokėjimo nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="62380-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="62380-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="62380-123">Close the page.</span></span>
14. <span data-ttu-id="62380-124">Lauke **Dienos** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="62380-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="62380-125">Kiekis, įvestas lauke **Dienos**, pagal tai, kokia parinktis buvo pasirinkta lauke **Grynoji/dabartinė**, bus naudojamas skaičiuoti mokėjimo nuolaidos datai.</span><span class="sxs-lookup"><span data-stu-id="62380-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="62380-126">Jei buvo pasirinkta **Grynoji**, norint nustatyti mokėjimo nuolaidos datą, kiekis bus pridėtas prie SF datos.</span><span class="sxs-lookup"><span data-stu-id="62380-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="62380-127">Jei buvo pasirinktas **Dabartinis mėnesis**, norint nustatyti mokėjimo nuolaidos datą, kiekis bus pridėtas prie dabartinio mėnesio pabaigos.</span><span class="sxs-lookup"><span data-stu-id="62380-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="62380-128">Lauke **Nuolaida** įveskite mokėjimo nuolaidos procentą.</span><span class="sxs-lookup"><span data-stu-id="62380-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="62380-129">Įveskite pagrindinę sąskaitą, į kurią bus registruojamos kliento SF taikoma mokėjimo nuolaida, tada įveskite pagrindinę sąskaitą, į kurią bus registruojamos tiekėjo SF taikoma mokėjimo nuolaida.</span><span class="sxs-lookup"><span data-stu-id="62380-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="62380-130">Jei **Taikyti nuolaidą korespondentinėms sąskaitoms** nustatyta kaip **Naudoti pagrindinę sąskaitą, skirtą tiekėjo nuolaidoms**, bus naudojama pagrindinė sąskaita.</span><span class="sxs-lookup"><span data-stu-id="62380-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="62380-131">Jei parinktis nustatyta į **Sąskaitos faktūros eilutėse esančios sąskaitos**, mokėjimo nuolaida bus registruojama turto / išlaidų sąskaitose, esančiose SF eilutėse.</span><span class="sxs-lookup"><span data-stu-id="62380-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="62380-132">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="62380-132">Select **Save**.</span></span>

