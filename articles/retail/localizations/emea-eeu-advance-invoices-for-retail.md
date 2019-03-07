---
title: Išankstinės „Retail“ SF (Rytų Europa)
description: Šioje temoje paaiškinama, kaip nustatyti išankstinius Rytų Europos „Retail“ pranešimus.
author: epopov
manager: annbe
ms.date: 10/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: ba2cfb176242e2e611375c9943a9e4da2b2bb02a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "371180"
---
# <a name="advance-invoices-for-retail-for-eastern-europe"></a><span data-ttu-id="83e41-103">Išankstinės „Retail“ SF (Rytų Europa)</span><span class="sxs-lookup"><span data-stu-id="83e41-103">Advance invoices for Retail for Eastern Europe</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="83e41-104">Šioje temoje pateikta informacija taikoma atliekant lokalizavimą Rytų Europoje ir yra susijusi su mažmeninės prekybos verslu.</span><span class="sxs-lookup"><span data-stu-id="83e41-104">The information in this topic applies to the Eastern European localization and is specific to the retail industry.</span></span>

<span data-ttu-id="83e41-105">Jei Lenkijoje, Vengrijoje ir Čekijos Respublikoje išankstinis apmokėjimas iš kliento gaunamas naudojantis elektroniniu kasos aparatu (EKA), išankstinį apmokėjimą būtina užregistruoti mokesčių tikslais ir būtina sukurti ir atsispausdinti išankstinės SF dokumentą, kuriame nurodyta išankstinio apmokėjimo suma.</span><span class="sxs-lookup"><span data-stu-id="83e41-105">For Poland, Hungary, and Czech Republic, when a prepayment is received from a customer via Point of Sale (POS), the prepayment must be registered for tax purposes, and it's required to generate and print an advance invoice document that includes the prepayment amount.</span></span> <span data-ttu-id="83e41-106">Be to, Lenkijoje atliekamos išankstinės SF operacijos turi būti registruojamos didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="83e41-106">Additionally, for Poland, advance invoice transactions must be posted in the general ledger.</span></span>

<span data-ttu-id="83e41-107">Galiausiai užregistravus pardavimo užsakymo SF, galutiniame dokumente turi būti išankstinė SF ir turi būti nurodyti visi išankstiniai mokėjimai.</span><span class="sxs-lookup"><span data-stu-id="83e41-107">When the invoice for the sales order is finally posted, the final document should include the advance invoice, and any prepayments should be indicated.</span></span>

<span data-ttu-id="83e41-108">Jei pardavimo užsakymus kuriate iš dalies Gautinos sumos, pasinaudodami dalyje [Išankstinės SF, skirtos Rytų Europai](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/emea-advance-invoice) nurodyta procedūra, turite būtinai patys sukurti išankstines SF.</span><span class="sxs-lookup"><span data-stu-id="83e41-108">If you generate sales orders from Accounts receivable, you must manually generate advance invoices by using the procedure in [Advance invoices for Eastern Europe](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/emea-advance-invoice).</span></span> <span data-ttu-id="83e41-109">Pardavimo užsakymus kuriant naudojantis EKA, išankstines SF sukuria ir užregistruoja sistema.</span><span class="sxs-lookup"><span data-stu-id="83e41-109">If you generate sales orders via POS, the system generates and posts the advance invoices for you.</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="83e41-110">Palaikomi scenarijai</span><span class="sxs-lookup"><span data-stu-id="83e41-110">Supported scenarios</span></span>

<span data-ttu-id="83e41-111">Palaikomi toliau nurodyti scenarijai:</span><span class="sxs-lookup"><span data-stu-id="83e41-111">The following scenarios are supported:</span></span>

- <span data-ttu-id="83e41-112">Sukurkite ir užregistruokite išankstinę SF.</span><span class="sxs-lookup"><span data-stu-id="83e41-112">Create and post an advance invoice.</span></span>
- <span data-ttu-id="83e41-113">Pakeiskite depozito sumą.</span><span class="sxs-lookup"><span data-stu-id="83e41-113">Modify a deposit amount.</span></span> <span data-ttu-id="83e41-114">Jei klientas nusprendžia padidinti depozito sumą, išrašoma papildoma išankstinė SF.</span><span class="sxs-lookup"><span data-stu-id="83e41-114">If a customer decides to increase the amount of a deposit, an additional advance invoice is issued.</span></span> <span data-ttu-id="83e41-115">Atliekant bet kokius kitus depozito sumos pakeitimus (pavyzdžiui, jei redaguojamas kliento užsakymas) sukuriama pirmiau sukurtos išankstinės SF kredito pažyma, taip pat sukuriama nauja išankstinė SF, kuri užregistruojama nurodžius pataisytą sumą.</span><span class="sxs-lookup"><span data-stu-id="83e41-115">For all other changes to the deposit amount (for example, if a customer order is edited), a credit note is created for the advance invoice that was previously generated, and a new advance invoice is generated and posted for the corrected amount.</span></span>
- <span data-ttu-id="83e41-116">Atšaukite pardavimo užsakymą, kuriame yra susietų išankstinių SF.</span><span class="sxs-lookup"><span data-stu-id="83e41-116">Cancel a sales order that has linked advance invoices.</span></span> <span data-ttu-id="83e41-117">Šiuo atveju sukuriama išankstinės SF kredito pažyma.</span><span class="sxs-lookup"><span data-stu-id="83e41-117">In this case, a credit note is created for the advance invoice.</span></span>
- <span data-ttu-id="83e41-118">Užregistruokite pardavimo užsakymo SF, kurioje yra susietų išankstinių SF.</span><span class="sxs-lookup"><span data-stu-id="83e41-118">Post a sales order invoice that has linked advance invoices.</span></span> <span data-ttu-id="83e41-119">Atšaukiama su pardavimo užsakymu susieta išankstinė SF, kurioje nurodyta pardavimo SF suma.</span><span class="sxs-lookup"><span data-stu-id="83e41-119">The advance invoice that is linked to a sales order is reversed for the amount of the sales invoice.</span></span> <span data-ttu-id="83e41-120">Sudengiamos išankstinės SF operacijos su išankstinės SF atšaukimo operacijomis.</span><span class="sxs-lookup"><span data-stu-id="83e41-120">The advance invoice transactions are settled with advance invoice reversal transactions.</span></span>

## <a name="set-up-advance-invoices"></a><span data-ttu-id="83e41-121">Išankstinių SF nustatymas</span><span class="sxs-lookup"><span data-stu-id="83e41-121">Set up advance invoices</span></span>

### <a name="turn-on-the-functionality-for-creating-advance-invoices"></a><span data-ttu-id="83e41-122">Funkcijos, kuria naudojantis galima kurti išankstines SF, įjungimas</span><span class="sxs-lookup"><span data-stu-id="83e41-122">Turn on the functionality for creating advance invoices</span></span>

1. <span data-ttu-id="83e41-123">Eikite į **Mažmeninė prekyba \> Būstinės sąranka \> Parametrai \> Mažmeninės prekybos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="83e41-123">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span>
2. <span data-ttu-id="83e41-124">„FastTab“ skirtuko **Užsakymas** skirtuke **Kliento užsakymai** nustatykite veiksmo **Sukurti depozito išankstinę SF** parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="83e41-124">On the **Customer orders** tab, on the **Order** FastTab, set the **Create advance invoice for deposit** option to **Yes**.</span></span>

### <a name="define-the-parameters-for-posting-advance-invoices"></a><span data-ttu-id="83e41-125">Išankstinių SF registravimo parametrų nurodymas</span><span class="sxs-lookup"><span data-stu-id="83e41-125">Define the parameters for posting advance invoices</span></span>

1. <span data-ttu-id="83e41-126">Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="83e41-126">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="83e41-127">„FastTab“ skirtuko **Išankstinė SF** skirtuke **Naujiniai** nustatykite laukus **Registravimo šablonas**, **PVM grupė** ir **Prekės PVM grupė**.</span><span class="sxs-lookup"><span data-stu-id="83e41-127">On the **Updates** tab, on the **Advance invoice** FastTab, set the **Posting profile**, **Sales tax group**, and **Item sales tax group** fields.</span></span> <span data-ttu-id="83e41-128">Jei šie laukai nustatyti teisingai, išankstinė SF užregistruojama.</span><span class="sxs-lookup"><span data-stu-id="83e41-128">If these fields are set correctly, the advance invoice will be posted.</span></span> <span data-ttu-id="83e41-129">Jei šie laukai nenustatyti, išankstinės SF neregistruojamos.</span><span class="sxs-lookup"><span data-stu-id="83e41-129">If these fields aren't set, advance invoices won't be posted.</span></span>

### <a name="turn-off-posting-of-the-sales-tax-on-prepayment-journal-voucher"></a><span data-ttu-id="83e41-130">PVM registravimo išankstinio mokėjimo žurnalo kvite išjungimas</span><span class="sxs-lookup"><span data-stu-id="83e41-130">Turn off posting of the Sales tax on prepayment journal voucher</span></span>

<span data-ttu-id="83e41-131">Įjungus išankstinės SF registravimą PVM išankstinio mokėjimo žurnalo kvite registruoti negalima.</span><span class="sxs-lookup"><span data-stu-id="83e41-131">The Sales tax on prepayment journal voucher must not be posted if advance invoice posting is turned on.</span></span> <span data-ttu-id="83e41-132">Norėdami patikrinti, ar laikomasi šio reikalavimo, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="83e41-132">To verify that this requirement is met, follow these steps.</span></span>

1. <span data-ttu-id="83e41-133">Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="83e41-133">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="83e41-134">„FastTab“ skirtuko **Mokėjimas** skirtuke **DK ir PVM** patikrinkite, ar toliau nurodyti laukai yra tušti arba ar nustatyta jų parinktis **Ne**:</span><span class="sxs-lookup"><span data-stu-id="83e41-134">On the **Ledger and sales tax** tab, on the **Payment** FastTab, make sure that the following fields are blank or set to **No**:</span></span>

    - <span data-ttu-id="83e41-135">Išankstinio mokėjimo žurnalo kvite nurodytas PVM</span><span class="sxs-lookup"><span data-stu-id="83e41-135">Sales tax on prepayment journal voucher</span></span>
    - <span data-ttu-id="83e41-136">Registravimo šablonas su išankstinio mokėjimo žurnalo kvitu</span><span class="sxs-lookup"><span data-stu-id="83e41-136">Posting profile with prepayment journal voucher</span></span>
    - <span data-ttu-id="83e41-137">Išankstinio mokėjimo mokesčių grupė</span><span class="sxs-lookup"><span data-stu-id="83e41-137">Tax group for prepayment</span></span>
    - <span data-ttu-id="83e41-138">Prekės PVM grupė</span><span class="sxs-lookup"><span data-stu-id="83e41-138">Item Sales tax group</span></span>

## <a name="print-advance-invoices"></a><span data-ttu-id="83e41-139">Išankstinių SF spausdinimas</span><span class="sxs-lookup"><span data-stu-id="83e41-139">Print advance invoices</span></span>

<span data-ttu-id="83e41-140">Išankstines SF iš EKA alite spausdinti naudodamiesi „Microsoft Windows“ spausdintuvu, kuris susietas su aparatūros stotimi.</span><span class="sxs-lookup"><span data-stu-id="83e41-140">You can print advance invoices from POS on a Microsoft Windows printer that is connected to the hardware station.</span></span> <span data-ttu-id="83e41-141">Išankstinės SF iš EKA galima spausdinti dviem būdais:</span><span class="sxs-lookup"><span data-stu-id="83e41-141">There are two options for printing an advance invoice from POS:</span></span>

- <span data-ttu-id="83e41-142">**Spausdinkite išankstinę SF pasibaigus EKA operacijai.**</span><span class="sxs-lookup"><span data-stu-id="83e41-142">**Print an advance invoice after a transaction is concluded in POS.**</span></span> <span data-ttu-id="83e41-143">Jei sukurta išankstinė SF ir teisingai nustatytas „Windows“ spausdintuvas, šis veiksmas atliekamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="83e41-143">This option occurs automatically if an advance invoice was generated and a Windows printer was correctly set up.</span></span> <span data-ttu-id="83e41-144">Tokiu atveju spausdinama tik paskutinė su kliento užsakymu susieta išankstinė SF.</span><span class="sxs-lookup"><span data-stu-id="83e41-144">In this case, only the last advance invoice that is linked to the customer order is printed.</span></span>
- <span data-ttu-id="83e41-145">**Iš naujo spausdinkite iš operacijų žurnalo gautą išankstinę SF.**</span><span class="sxs-lookup"><span data-stu-id="83e41-145">**Reprint an advance invoice from the transaction journal.**</span></span> <span data-ttu-id="83e41-146">Paspaudę **Rodyti žurnalą** atidarykite operacijų žurnalą, suraskite kliento užsakymą ir paspauskite **Spausdinti išankstinę SF**.</span><span class="sxs-lookup"><span data-stu-id="83e41-146">Select **Show journal** to open the transactions journal, find the customer order, and then select **Print Advance invoice**.</span></span> <span data-ttu-id="83e41-147">Tokiu atveju spausdinamos visos su kliento užsakymu susietos išankstinės SF.</span><span class="sxs-lookup"><span data-stu-id="83e41-147">In this case, all advance invoices that are linked to the customer order are printed.</span></span>

### <a name="set-up-a-windows-printer"></a><span data-ttu-id="83e41-148">„Windows“ spausdintuvo nustatymas</span><span class="sxs-lookup"><span data-stu-id="83e41-148">Set up a Windows printer</span></span>

<span data-ttu-id="83e41-149">Atlikite šiuos veiksmus, kad dokumentus būtų galima spausdinti iš EKA naudojant su aparatūros storimi sujungtą „Windows“ spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="83e41-149">Follow these steps to enable documents to be printed from POS on a Windows printer that is connected to the hardware station.</span></span>

1. <span data-ttu-id="83e41-150">Eikite į **Mažmeninė prekyba \> Kanalų sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**.</span><span class="sxs-lookup"><span data-stu-id="83e41-150">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**.</span></span>
2. <span data-ttu-id="83e41-151">Pasirinkite aparatūros šabloną, susietą su parduotuve, kurioje naudojamas spausdintuvas.</span><span class="sxs-lookup"><span data-stu-id="83e41-151">Select a hardware profile that is related to the store where the printer is used.</span></span>
3. <span data-ttu-id="83e41-152">Atnaujinkite skyriaus **Spausdintuvas** arba **2 spausdintuvas** parametrus:</span><span class="sxs-lookup"><span data-stu-id="83e41-152">In either the **Printer** section or the **Printer 2** section, update the settings:</span></span>

    - <span data-ttu-id="83e41-153">Lauke **Spausdintuvas** pasirinkite **„Windows“ tvarkyklė**.</span><span class="sxs-lookup"><span data-stu-id="83e41-153">In the **Printer** field, select **Windows driver**.</span></span>
    - <span data-ttu-id="83e41-154">Lauke **Įrenginio pavadinimas** įveskite spausdintuvo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="83e41-154">In the **Device name** field, enter the name of the printer.</span></span>

4. <span data-ttu-id="83e41-155">Eikite į **Mažmeninė prekyba \> Mažmeninės prekybos IT \> Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="83e41-155">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="83e41-156">Pasirinkite užduotį **1090**, paskui paspauskite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="83e41-156">Select job **1090**, and then select **Run now**.</span></span>
