---
title: Nustatyti ISO20022 tiesioginio debeto klientus ir klientų banko sąskaitas
description: Ši užduotis apžvelgia, kaip nustatyti kliento banko sąskaitą ir kliento tiesioginio debeto įgaliojimą, kurių reikia norint generuoti kliento mokėjimo failą, pvz., ISO20022 tiesioginio debeto mokėjimo failą.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b09d7d203f1bb58fad26a109962005affa6d307
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445916"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="3b65c-103">Nustatyti ISO20022 tiesioginio debeto klientus ir klientų banko sąskaitas</span><span class="sxs-lookup"><span data-stu-id="3b65c-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3b65c-104">Ši užduotis apžvelgia, kaip nustatyti kliento banko sąskaitą ir kliento tiesioginio debeto įgaliojimą, kurių reikia norint generuoti kliento mokėjimo failą, pvz., ISO20022 tiesioginio debeto mokėjimo failą.</span><span class="sxs-lookup"><span data-stu-id="3b65c-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="3b65c-105">Atsižvelgiant į nustatytus kliento mokėjimo formatus, gali būti reikalinga papildoma kliento arba kliento banko kodo informacija, kuri nėra aprašyta šioje procedūroje.</span><span class="sxs-lookup"><span data-stu-id="3b65c-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="3b65c-106">Ši užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kai juridinio subjekto pirminis adresas yra Vokietijoje.</span><span class="sxs-lookup"><span data-stu-id="3b65c-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="3b65c-107">Tai yra ketvirtoji iš penkių procedūrų, kuriose apibūdinamas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="3b65c-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="3b65c-108">Nustatyti kliento banko sąskaitą</span><span class="sxs-lookup"><span data-stu-id="3b65c-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="3b65c-109">Pasirinkite Gautinos sumos > Klientai > Visi klientai.</span><span class="sxs-lookup"><span data-stu-id="3b65c-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="3b65c-110">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="3b65c-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3b65c-111">Pvz., filtruokite lauką Sąskaita naudodami reikšmę „DE-010 “.</span><span class="sxs-lookup"><span data-stu-id="3b65c-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="3b65c-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3b65c-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3b65c-113">Veiksmų srityje spustelėkite Klientas.</span><span class="sxs-lookup"><span data-stu-id="3b65c-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="3b65c-114">Spustelėkite Banko sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="3b65c-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="3b65c-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3b65c-115">Click New.</span></span>
7. <span data-ttu-id="3b65c-116">Lauke Banko sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3b65c-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="3b65c-117">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3b65c-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="3b65c-118">Pavyzdžiui, įveskite EUR bankas.</span><span class="sxs-lookup"><span data-stu-id="3b65c-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="3b65c-119">Lauke Bankų grupės įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3b65c-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="3b65c-120">Lauke IBAN surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3b65c-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="3b65c-121">Pavyzdžiui, įveskite DE36200400000628808808.</span><span class="sxs-lookup"><span data-stu-id="3b65c-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="3b65c-122">Lauke SWIFT kodas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3b65c-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="3b65c-123">Pavyzdžiui: įveskite „COBADEFFXXX‟.</span><span class="sxs-lookup"><span data-stu-id="3b65c-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="3b65c-124">Atkreipkite dėmesį, kad SWIFT / BIC nereikalingas naudojant daugelį mokėjimo formatų, tačiau vis tiek rekomenduojama užregistruoti banko kodo SWIFT / BIC.</span><span class="sxs-lookup"><span data-stu-id="3b65c-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="3b65c-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3b65c-125">Click Save.</span></span>
13. <span data-ttu-id="3b65c-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3b65c-126">Close the page.</span></span>
14. <span data-ttu-id="3b65c-127">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="3b65c-127">Click Edit.</span></span>
15. <span data-ttu-id="3b65c-128">Išplėskite dalį Numatytosios mokėjimo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="3b65c-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="3b65c-129">Lauke Banko sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3b65c-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="3b65c-130">Pridėti tiesioginio debeto įgaliojimą</span><span class="sxs-lookup"><span data-stu-id="3b65c-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="3b65c-131">Išplėskite dalį Tiesioginio debeto įgaliojimai.</span><span class="sxs-lookup"><span data-stu-id="3b65c-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="3b65c-132">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3b65c-132">Click Add.</span></span>
3. <span data-ttu-id="3b65c-133">Lauke Kreditoriaus banko sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3b65c-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="3b65c-134">Pavyzdžiui, pasirinkite DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="3b65c-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="3b65c-135">Lauke Pasirašymo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="3b65c-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="3b65c-136">Spustelėkite Taip, kad patvirtintumėte datos atnaujinimą.</span><span class="sxs-lookup"><span data-stu-id="3b65c-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="3b65c-137">Lauke Pasirašymo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3b65c-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="3b65c-138">Lauke Numatomas mokėjimų skaičius įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="3b65c-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="3b65c-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3b65c-139">Click OK.</span></span>
9. <span data-ttu-id="3b65c-140">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3b65c-140">Click Save.</span></span>

