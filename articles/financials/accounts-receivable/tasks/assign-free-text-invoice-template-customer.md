--- 
title: "Priskirti klientui laisvos formos SF šabloną"
description: "Ši užduotis parodo, kaip klientui priskirti laisvos formos SF šabloną."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3bcb59c6edd04877dc2a052002be513205ae840a
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="9ee17-103">Priskirti klientui laisvos formos SF šabloną</span><span class="sxs-lookup"><span data-stu-id="9ee17-103">Assign a free text invoice template to a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ee17-104">Ši užduotis parodo, kaip klientui priskirti laisvos formos SF šabloną.</span><span class="sxs-lookup"><span data-stu-id="9ee17-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="9ee17-105">Ši užduotis naudoja USMF demonstracinę įmonę ir yra skirta naudotojui, kuris yra atsakingas už A/R SF valdymą ir apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="9ee17-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="9ee17-106">Pasirinkite Gautinos sumos > Klientai > Visi klientai.</span><span class="sxs-lookup"><span data-stu-id="9ee17-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="9ee17-107">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9ee17-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9ee17-108">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="9ee17-108">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="9ee17-109">Spustelėkite Pasikartojančios SF.</span><span class="sxs-lookup"><span data-stu-id="9ee17-109">Click Recurring invoices.</span></span>
    * <span data-ttu-id="9ee17-110">Naudokite šį puslapį, kad laisvos formos SF šablonus priskirtumėte klientams ir nurodytumėte, kaip dažnai SF bus siunčiamos klientui.</span><span class="sxs-lookup"><span data-stu-id="9ee17-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="9ee17-111">Spustelėkite Naujas, kad klientui priskirtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="9ee17-111">Click New to assign a new template to the customer.</span></span>
6. <span data-ttu-id="9ee17-112">Pasirinkite laisvos formos SF šabloną, kurį norite priskirti klientui.</span><span class="sxs-lookup"><span data-stu-id="9ee17-112">Select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="9ee17-113">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9ee17-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="9ee17-114">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="9ee17-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9ee17-115">Įveskite pirmosios SF sugeneravimo datą.</span><span class="sxs-lookup"><span data-stu-id="9ee17-115">Enter the date when the first invoice will be generated.</span></span>
    * <span data-ttu-id="9ee17-116">Įveskite pasikartojančią pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="9ee17-116">Enter a recurring end date.</span></span>  
    * <span data-ttu-id="9ee17-117">Pasirinkite vieną iš šių parinkčių: Nėra pabaigos datos – SF bus generuojamos neribotą laiką, kol šablonas bus pašalintas iš kliento sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="9ee17-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>  <span data-ttu-id="9ee17-118">Atsiskaitymo pabaigos data – pasirinkite šią parinktį ir įveskite paskutinę galimą SF generavimo datą.</span><span class="sxs-lookup"><span data-stu-id="9ee17-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
    * <span data-ttu-id="9ee17-119">Maksimali kaupiamoji suma, po kurios SF nebebus generuojamos.</span><span class="sxs-lookup"><span data-stu-id="9ee17-119">Maximum cumulative amount after which invoice generation will stop.</span></span>  
    * <span data-ttu-id="9ee17-120">Įveskite maksimalią kaupiamąją sumą, kurią galima pasiekti naudojant pasirinktą šabloną.</span><span class="sxs-lookup"><span data-stu-id="9ee17-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="9ee17-121">Pvz., jei įvesite 1 000,00 ir generuosite mėnesines 100,00 SF, SF nebebus generuojamos sugeneravus dešimtąją SF.</span><span class="sxs-lookup"><span data-stu-id="9ee17-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
    * <span data-ttu-id="9ee17-122">Generuokite pasikartojančias SF naudodami numatytąsias reikšmes iš laisvos formos SF šablono arba kliento sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="9ee17-122">Generate recurring invoices by using the default values from either free text invoice template or the customer account.</span></span>  
    * <span data-ttu-id="9ee17-123">Pasirinkite laisvos formos SF šabloną arba kliento sąskaitą, pagal kurią bus nustatomos kalbos, registravimo šablono, PVM grupės, prekės PVM grupės, sąrašo kodo, pristatymo šalies / regiono, valiutos, mokėjimo sąlygų, mokėjimo būdo, mokėjimo specifikacijos, mokėjimo grafiko, mokėjimo nuolaidos, finansinių dimensijų ir žiro mokėjimo dokumento numatytosios vertės, kai kuriamos SF.</span><span class="sxs-lookup"><span data-stu-id="9ee17-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
10. <span data-ttu-id="9ee17-124">Pasirinkite kartojimo modelį.</span><span class="sxs-lookup"><span data-stu-id="9ee17-124">Select the recurrence pattern.</span></span>
    * <span data-ttu-id="9ee17-125">Kasdien – pasirinkite šią parinktį ir lauke Per įveskite dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="9ee17-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="9ee17-126">Pavyzdžiui, jei įvesite 15, šio kliento SF bus generuojama kas 15 dienų.</span><span class="sxs-lookup"><span data-stu-id="9ee17-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>  <span data-ttu-id="9ee17-127">Kas savaitę – pasirinkite šią parinktį ir lauke Per įveskite savaičių skaičių.</span><span class="sxs-lookup"><span data-stu-id="9ee17-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="9ee17-128">Pavyzdžiui, jei įvesite 2, šio kliento SF bus generuojama kas dvi savaites.</span><span class="sxs-lookup"><span data-stu-id="9ee17-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>  <span data-ttu-id="9ee17-129">Kas mėnesį – pasirinkite šią parinktį ir lauke Per įveskite mėnesių skaičių.</span><span class="sxs-lookup"><span data-stu-id="9ee17-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="9ee17-130">Pavyzdžiui, jei įvesite 6, šio kliento SF bus generuojama kas šešis mėnesius.</span><span class="sxs-lookup"><span data-stu-id="9ee17-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>  <span data-ttu-id="9ee17-131">Kas metus – pasirinkite šią parinktį ir lauke Per įveskite metų skaičių.</span><span class="sxs-lookup"><span data-stu-id="9ee17-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="9ee17-132">Pavyzdžiui, jei įvesite 2, šio kliento SF bus generuojama kas dvejus metus.</span><span class="sxs-lookup"><span data-stu-id="9ee17-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
11. <span data-ttu-id="9ee17-133">Lauke Per įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9ee17-133">In the Per field, enter a number.</span></span>


