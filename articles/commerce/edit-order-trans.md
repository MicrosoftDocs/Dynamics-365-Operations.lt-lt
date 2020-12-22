---
title: Internetinio užsakymo ir asinchroninio kliento užsakymo operacijų redagavimas ir tikrinimas
description: Šioje temoje aprašoma, kaip redaguoti ir tikrinti internetinio užsakymo ir asinchroninio kliento užsakymo operacijas „Microsoft Dynamics 365 Commerce“.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9f2db25c8897662baa177752d0c5fc4ac6178a4
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/04/2020
ms.locfileid: "4459595"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="e78f7-103">Internetinio užsakymo ir asinchroninio kliento užsakymo operacijų redagavimas ir tikrinimas</span><span class="sxs-lookup"><span data-stu-id="e78f7-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e78f7-104">Šioje temoje aprašoma, kaip redaguoti ir tikrinti internetinio užsakymo ir asinchroninio kliento užsakymo operacijas „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="e78f7-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e78f7-105">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="e78f7-105">Overview</span></span>

<span data-ttu-id="e78f7-106">„Commerce“ 10.0.5 ir 10.0.6 versijos skiriasi tuo, kad į pastarąją buvo įtrauktas atsiskaitymo grynaisiais operacijų (pvz., pardavimo ir grąžinimo) ir grynųjų pinigų valdymo operacijų (pvz., srauto įrašo ir mokėjimo priemonės šalinimo) redagavimo palaikymas.</span><span class="sxs-lookup"><span data-stu-id="e78f7-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="e78f7-107">„Commerce“ 10.0.7 versijoje įtrauktas internetinio užsakymo operacijų ir asinchroninio kliento užsakymo operacijų redagavimo palaikymas.</span><span class="sxs-lookup"><span data-stu-id="e78f7-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="e78f7-108">Užsakymo operacijų redagavimas ir tikrinimas</span><span class="sxs-lookup"><span data-stu-id="e78f7-108">Edit and audit order transactions</span></span>

<span data-ttu-id="e78f7-109">Norėdami redaguoti ir tikrinti užsakymo operacijas „Commerce“ būstinėje, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e78f7-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e78f7-110">Įdiekite [„Microsoft Dynamics Office Add-in“](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span><span class="sxs-lookup"><span data-stu-id="e78f7-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="e78f7-111">Puslapio **Mažmeninės prekybos parametrai** skirtuko **Kliento užsakymai** „FastTab“ **Užsakymas** nurodykite sulaikymo kodą, skirtą **Užsakymo sinchronizavimo klaidų sulaikymo kodas**.</span><span class="sxs-lookup"><span data-stu-id="e78f7-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="e78f7-112">Atidarykite darbo sritį **Parduotuvės finansai**.</span><span class="sxs-lookup"><span data-stu-id="e78f7-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="e78f7-113">Plytelėmis **Internetinio užsakymo sinchronizavimo klaidos** ir **Kliento užsakymo sinchronizavimo klaidos** pateikiamas iš anksto filtruotas mažmeninės prekybos operacijos puslapio rodinys.</span><span class="sxs-lookup"><span data-stu-id="e78f7-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="e78f7-114">Kiekvienoje rodomi operacijų įrašai, kurių atitinkamo užsakymo tipo sinchronizavimas nepavyko.</span><span class="sxs-lookup"><span data-stu-id="e78f7-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="e78f7-115">Atidarykite puslapį **Internetinio užsakymo sinchronizavimo klaidos** arba puslapį **Kliento užsakymo sinchronizavimo klaidos**.</span><span class="sxs-lookup"><span data-stu-id="e78f7-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="e78f7-116">Pasirinkite įrašą, kad peržiūrėtumėte išsamią sinchronizavimo klaidos informaciją.</span><span class="sxs-lookup"><span data-stu-id="e78f7-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="e78f7-117">„FastTab“ **Sinchronizavimo būsena** pateikiama ši išsami klaidos informacija:</span><span class="sxs-lookup"><span data-stu-id="e78f7-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="e78f7-118">Laukiama užsakymo būsena</span><span class="sxs-lookup"><span data-stu-id="e78f7-118">Pending order status</span></span>
    - <span data-ttu-id="e78f7-119">Išsami užsakymo klaidos informacija</span><span class="sxs-lookup"><span data-stu-id="e78f7-119">Order error details</span></span>
    - <span data-ttu-id="e78f7-120">Pakeitimo data ir laikas</span><span class="sxs-lookup"><span data-stu-id="e78f7-120">Modified date and time</span></span>
    - <span data-ttu-id="e78f7-121">Mėginimų skaičius</span><span class="sxs-lookup"><span data-stu-id="e78f7-121">Retry count</span></span>

1. <span data-ttu-id="e78f7-122">Jei išsamia klaidos informacija nurodoma, kad įrašą reikia ištaisyti, pasirinkite **„Office“ papildinys** ir pasirinkite **Redaguoti pasirinktą operaciją**.</span><span class="sxs-lookup"><span data-stu-id="e78f7-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="e78f7-123">Atidaromas „Excel“ failas, kuriame rodoma išsami pasirinktos operacijos informacija.</span><span class="sxs-lookup"><span data-stu-id="e78f7-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="e78f7-124">Jei redaguojama operacija yra internetinio užsakymo operacija, „Excel“ faile yra šie darbalapiai:</span><span class="sxs-lookup"><span data-stu-id="e78f7-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="e78f7-125">**Operacija** – šiame darbalapyje pateikiama išsami antraštės informacija apie operaciją.</span><span class="sxs-lookup"><span data-stu-id="e78f7-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="e78f7-126">**Pardavimo operacija** – šiame darbalapyje pateikiama išsami eilutės informacija apie operaciją.</span><span class="sxs-lookup"><span data-stu-id="e78f7-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="e78f7-127">**Mokėjimo operacijos** – šiame darbalapyje pateikiama išsami informacija apie operacijos mokėjimo eilutes.</span><span class="sxs-lookup"><span data-stu-id="e78f7-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="e78f7-128">**Nuolaidų operacijos** – šiame darbalapyje pateikiama su nuolaidomis susijusi informacija apie operaciją.</span><span class="sxs-lookup"><span data-stu-id="e78f7-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="e78f7-129">**Mokesčių operacijos** – šiame darbalapyje pateikiama su mokesčiais susijusi informacija apie operaciją.</span><span class="sxs-lookup"><span data-stu-id="e78f7-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="e78f7-130">**Išlaidų operacijos** – šiame darbalapyje pateikiami su išlaidomis susiję duomenys apie operaciją.</span><span class="sxs-lookup"><span data-stu-id="e78f7-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="e78f7-131">Jei redaguojama operacija yra asinchroninio kliento užsakymo operacija, „Excel“ faile yra šie darbalapiai:</span><span class="sxs-lookup"><span data-stu-id="e78f7-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="e78f7-132">**Eilutės** – šiame darbalapyje pateikiama išsami antraštės ir eilutės informacija apie operaciją.</span><span class="sxs-lookup"><span data-stu-id="e78f7-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="e78f7-133">**Mokėjimai** – šiame darbalapyje pateikiama išsami informacija apie operacijos mokėjimo eilutes.</span><span class="sxs-lookup"><span data-stu-id="e78f7-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="e78f7-134">**Nuolaidos** – šiame darbalapyje pateikiama su nuolaidomis susijusi informacija apie operaciją.</span><span class="sxs-lookup"><span data-stu-id="e78f7-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="e78f7-135">**Mokesčiai** – šiame darbalapyje pateikiama su mokesčiais susijusi informacija apie operaciją.</span><span class="sxs-lookup"><span data-stu-id="e78f7-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="e78f7-136">**Išlaidos** – šiame darbalapyje pateikiami su išlaidomis susiję duomenys apie operaciją.</span><span class="sxs-lookup"><span data-stu-id="e78f7-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="e78f7-137">„Excel“ faile lauke **Laukiama užsakymo būsena** įveskite **Redaguojama** ir tada publikuokite keitimą.</span><span class="sxs-lookup"><span data-stu-id="e78f7-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="e78f7-138">Tokiu būdu per apdorojimą užduotis **Sinchronizuoti užsakymą**, vykdoma paketiniu režimu, nepraleis šio įrašo.</span><span class="sxs-lookup"><span data-stu-id="e78f7-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="e78f7-139">„Excel” faile modifikuokite atitinkamus laukus ir tada įkelkite duomenis atgal į „Commerce“ būstinę naudodami „Dynamics Excel“ papildinio publikavimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="e78f7-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="e78f7-140">Publikavus duomenis, pakeitimai bus rodomi sistemoje.</span><span class="sxs-lookup"><span data-stu-id="e78f7-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="e78f7-141">Publikuojant, vartotojo atlikti keitimai netikrinami.</span><span class="sxs-lookup"><span data-stu-id="e78f7-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="e78f7-142">Visą keitimų įrašų seką galima peržiūrėti pasirinkus **Peržiūrėti įrašo sekimą** antraštėje **Mažmeninės prekybos operacijos** (antraštės lygmens keitimai) ir atitinkamame skyriuje bei operacijų puslapio įraše.</span><span class="sxs-lookup"><span data-stu-id="e78f7-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="e78f7-143">Pavyzdžiui, visi su pardavimo eilutėmis susiję pakeitimai bus rodomi puslapyje **Pardavimo operacijos**, o visi su mokėjimais susiję pakeitimai – puslapyje **Mokėjimo operacijos**.</span><span class="sxs-lookup"><span data-stu-id="e78f7-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="e78f7-144">Pakeitimams palaikoma toliau pateikiama išsami audito informacija:</span><span class="sxs-lookup"><span data-stu-id="e78f7-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="e78f7-145">Pakeitimo data ir laikas</span><span class="sxs-lookup"><span data-stu-id="e78f7-145">Modified date and time</span></span>
    - <span data-ttu-id="e78f7-146">Laukas</span><span class="sxs-lookup"><span data-stu-id="e78f7-146">Field</span></span>
    - <span data-ttu-id="e78f7-147">Sena vertė</span><span class="sxs-lookup"><span data-stu-id="e78f7-147">Old value</span></span>
    - <span data-ttu-id="e78f7-148">Nauja vertė</span><span class="sxs-lookup"><span data-stu-id="e78f7-148">New value</span></span>
    - <span data-ttu-id="e78f7-149">Modifikavo</span><span class="sxs-lookup"><span data-stu-id="e78f7-149">Modified by</span></span>

1. <span data-ttu-id="e78f7-150">Atlikę ir publikavę keitimus, pasirinkite **Sinchronizuoti užsakymą**, kad būtų nedelsiant pradėtas sinchronizavimo procesas.</span><span class="sxs-lookup"><span data-stu-id="e78f7-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="e78f7-151">Taip pat galite palaukti, kol paketiniu režimu vykdant sinchronizavimo procesą bus apdorota operacija.</span><span class="sxs-lookup"><span data-stu-id="e78f7-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="e78f7-152">Pagal numatytuosius parametrus, sėkmingai sinchronizavus užsakymus, jie yra perkeliami į sulaikymo būseną, atsižvelgiant į sulaikymo kodą, apibrėžtą „Commerce“ parametruose.</span><span class="sxs-lookup"><span data-stu-id="e78f7-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="e78f7-153">Užsakymų sulaikymas turi būti pašalintas, kad užsakymus būtų galima toliau apdoroti norint juos įvykdyti arba atlikti kitas operacijas.</span><span class="sxs-lookup"><span data-stu-id="e78f7-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e78f7-154">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e78f7-154">Additional resources</span></span>

[<span data-ttu-id="e78f7-155">Atsiskaitymo grynaisiais ir grynųjų pinigų valdymo operacijų redagavimas ir tikrinimas</span><span class="sxs-lookup"><span data-stu-id="e78f7-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="e78f7-156">Mažmeninės prekybos operacijų finansinių dimensijų redagavimas</span><span class="sxs-lookup"><span data-stu-id="e78f7-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="e78f7-157">„Excel“ darbaknygės kūrimas norint redaguoti mažmeninės prekybos operacijas</span><span class="sxs-lookup"><span data-stu-id="e78f7-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="e78f7-158">Laukų įtraukimas į „Excel“ darbaknygę norint redaguoti mažmeninės prekybos operacijas</span><span class="sxs-lookup"><span data-stu-id="e78f7-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
