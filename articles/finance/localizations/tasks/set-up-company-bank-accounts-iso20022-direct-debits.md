---
title: Nustatyti ISO20022 tiesioginio debeto įmonės banko sąskaitas
description: Ši užduotis apžvelgia, kaip nustatyti konkrečios įmonės banko sąskaitos informaciją, kurios reikia norint generuoti kliento mokėjimo failus.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 652d8aa8f78d9a12ee390d23904f2c94d9bcf684
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445914"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="fcbec-103">Nustatyti ISO20022 tiesioginio debeto įmonės banko sąskaitas</span><span class="sxs-lookup"><span data-stu-id="fcbec-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fcbec-104">Ši užduotis apžvelgia, kaip nustatyti konkrečios įmonės banko sąskaitos informaciją, kurios reikia norint generuoti kliento mokėjimo failus.</span><span class="sxs-lookup"><span data-stu-id="fcbec-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="fcbec-105">Šioje procedūroje kaip pavyzdys naudojamas ISO 20022 tiesioginio debeto formatas.</span><span class="sxs-lookup"><span data-stu-id="fcbec-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="fcbec-106">Naudojant kitus formatus gali reikėti papildomos sąrankos informacijos, pvz., įmonės ID arba rūšiavimo kodo.</span><span class="sxs-lookup"><span data-stu-id="fcbec-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="fcbec-107">Ši užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF.</span><span class="sxs-lookup"><span data-stu-id="fcbec-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="fcbec-108">Tai yra antroji iš penkių procedūrų, kuriose apibūdinamas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="fcbec-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="fcbec-109">Nustatyti IBAN ir SWIFT kodus</span><span class="sxs-lookup"><span data-stu-id="fcbec-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="fcbec-110">Eikite į Grynųjų pinigų ir banko valdymas > Banko sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="fcbec-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="fcbec-111">Naudokite spartųjį filtrą, kad filtruotumėte lauką Banko sąskaita reikšme „DEMF OPER‟.</span><span class="sxs-lookup"><span data-stu-id="fcbec-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="fcbec-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="fcbec-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fcbec-113">Pavyzdžiui: spustelėkite DEMF OPER, kad atidarytumėte banko kodo informaciją.</span><span class="sxs-lookup"><span data-stu-id="fcbec-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="fcbec-114">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="fcbec-114">Click Edit.</span></span>
5. <span data-ttu-id="fcbec-115">Išplėskite arba sutraukite dalį Papildoma identifikacija.</span><span class="sxs-lookup"><span data-stu-id="fcbec-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="fcbec-116">Lauke IBAN surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fcbec-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="fcbec-117">Pavyzdžiui, įveskite DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="fcbec-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="fcbec-118">Lauke SWIFT kodas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fcbec-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="fcbec-119">Pavyzdžiui, įveskite DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="fcbec-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="fcbec-120">Atkreipkite dėmesį, kad SWIFT / BIC nereikalingas naudojant daugelį mokėjimo formatų, tačiau vis tiek rekomenduojama užregistruoti banko kodo SWIFT / BIC.</span><span class="sxs-lookup"><span data-stu-id="fcbec-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="fcbec-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="fcbec-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="fcbec-122">Nustatyti juridinio subjekto banko sąskaitą</span><span class="sxs-lookup"><span data-stu-id="fcbec-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="fcbec-123">Pasirinkite Organizacijos administravimas > Organizacijos > Juridiniai subjektai.</span><span class="sxs-lookup"><span data-stu-id="fcbec-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="fcbec-124">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="fcbec-124">Click Edit.</span></span>
3. <span data-ttu-id="fcbec-125">Išplėskite arba sutraukite dalį Banko sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="fcbec-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="fcbec-126">Lauke Banko sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="fcbec-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="fcbec-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="fcbec-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fcbec-128">Pavyzdžiui: pasirinkite DEMF OPER banko kodą.</span><span class="sxs-lookup"><span data-stu-id="fcbec-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="fcbec-129">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="fcbec-129">Click Save.</span></span>

