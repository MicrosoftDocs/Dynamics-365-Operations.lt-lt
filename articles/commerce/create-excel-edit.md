---
title: „Excel“ darbaknygės kūrimas norint redaguoti mažmeninės prekybos operacijas
description: Šioje temoje aprašoma, kaip sukurti „Excel“ darbaknygę, kad galėtumėte redaguoti mažmeninės prekybos operacijas „Microsoft Dynamics 365 Commerce“.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 73a3387d1e7251168002ff683b5b58e0c82a620c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965382"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="9b5dd-103">„Excel“ darbaknygės kūrimas norint redaguoti mažmeninės prekybos operacijas</span><span class="sxs-lookup"><span data-stu-id="9b5dd-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b5dd-104">Šioje temoje aprašoma, kaip sukurti „Excel“ darbaknygę, kad galėtumėte redaguoti mažmeninės prekybos operacijas „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9b5dd-105">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="9b5dd-105">Overview</span></span>

<span data-ttu-id="9b5dd-106">Yra iš anksto nustatytas „Excel“ šablonas, kurį klientai gali pasiekti iš skirtingų sistemos dalių ir naudoti mažmeninės prekybos operacijoms redaguoti ir tikrinti.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="9b5dd-107">Tačiau klientai taip pat gali sukurti pasirinktinę „Excel“ darbaknygę šiam tikslui.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="9b5dd-108">„Excel“ darbaknygės kūrimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9b5dd-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="9b5dd-109">Norėdami sukurti ir konfigūruoti „Excel“ darbaknygę, kad galėtumėte redaguoti mažmeninės prekybos operacijas, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="9b5dd-110">Atidarykite „Excel“ ir sukurkite tuščią darbaknygę.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="9b5dd-111">Skirtuke **Įterpti** pasirinkite **Mano papildiniai**.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="9b5dd-112">Dešiniojoje srityje pasirinkite saitą **Įtraukti serverio informaciją**.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="9b5dd-113">Įveskite serverio URL ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="9b5dd-114">Jei gaunate klaidos pranešimą „Nerasta jokių programėlės registracijų“, atlikite šiuos veiksmus, kad išspręstumėte problemą:</span><span class="sxs-lookup"><span data-stu-id="9b5dd-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="9b5dd-115">„Commerce“ eikite į **Sistemos administravimas \> Sąranka \> „Office“ programos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="9b5dd-116">„FastTab“ **Programos parametrai** pasirinkite **Inicijuoti programos parametrus**.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="9b5dd-117">Patvirtinimo pranešimo lauke pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="9b5dd-118">„FastTab“ **Užregistruotos programėlės** pasirinkite **Inicijuoti programėlės registraciją**.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="9b5dd-119">Kaip reikalaujama, pakartokite tris ankstesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="9b5dd-120">Pasirinkite **Dizainas** ir tada pasirinkite **Įtraukti lentelę**.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="9b5dd-121">Remdamiesi modifikuotinais duomenimis, pasirinkite objektus, kuriuos reikia įtraukti į „Excel“ darbaknygę ir redaguoti.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="9b5dd-122">Naudokite toliau pateikiamą lentelę kaip nuorodą.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="9b5dd-123">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="9b5dd-123">Transaction type</span></span> | <span data-ttu-id="9b5dd-124">Naudotini duomenų objektai</span><span class="sxs-lookup"><span data-stu-id="9b5dd-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="9b5dd-125">Atsiskaitymo grynaisiais operacijos, internetiniai užsakymai, asinchroniniai kliento užsakymai, asinchroniniai kliento pasiūlymai</span><span class="sxs-lookup"><span data-stu-id="9b5dd-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="9b5dd-126">Operacija (patikrinama), pardavimo operacija (patikrinama), mokėjimo operacijos (patikrinamos), mokesčių operacijos (patikrinamos), nuolaidų operacijos (patikrinamos), išlaidų operacijos (patikrinamos)</span><span class="sxs-lookup"><span data-stu-id="9b5dd-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="9b5dd-127">Inkasavimas</span><span class="sxs-lookup"><span data-stu-id="9b5dd-127">Bank drop</span></span> | <span data-ttu-id="9b5dd-128">Operacija (patikrinama), bankinio mokėjimo priemonių operacijos (patikrinamos)</span><span class="sxs-lookup"><span data-stu-id="9b5dd-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="9b5dd-129">Pinigų įnešimas į kasą</span><span class="sxs-lookup"><span data-stu-id="9b5dd-129">Safe drop</span></span> | <span data-ttu-id="9b5dd-130">Operacija (patikrinama), kasos mokėjimo priemonių operacijos (patikrinamos)</span><span class="sxs-lookup"><span data-stu-id="9b5dd-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="9b5dd-131">Mokėjimo priemonių deklaravimas</span><span class="sxs-lookup"><span data-stu-id="9b5dd-131">Tender declaration</span></span> | <span data-ttu-id="9b5dd-132">Operacija (patikrinama), mokėjimo priemonių deklaravimo operacijos (patikrinamos)</span><span class="sxs-lookup"><span data-stu-id="9b5dd-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="9b5dd-133">Pajamos, išlaidos</span><span class="sxs-lookup"><span data-stu-id="9b5dd-133">Income, Expense</span></span> | <span data-ttu-id="9b5dd-134">Operacija (patikrinama), pajamų / išlaidų operacijos (patikrinamos), mokėjimo operacijos (patikrinamos)</span><span class="sxs-lookup"><span data-stu-id="9b5dd-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="9b5dd-135">Deklaruoti pradžios sumą, mokėjimo priemonės šalinimas, srauto įrašas, mokėjimo priemonės grąža, sąskaitos faktūros apmokėjimas, kliento depozitas</span><span class="sxs-lookup"><span data-stu-id="9b5dd-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="9b5dd-136">Operacija (patikrinama), mokėjimo operacijos (patikrinamos)</span><span class="sxs-lookup"><span data-stu-id="9b5dd-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="9b5dd-137">Svarbu, kad į kiekvieną „Excel“ darbaknygę įtrauktumėte tik vieną duomenų objektą.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="9b5dd-138">Be to, visi laukai, pažymėti rakto simboliu, turi būti įtraukti į atitinkamą darbaknygę.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="9b5dd-139">Sukonfigūravę darbaknygę, pritaikykite reikalingus filtrus.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="9b5dd-140">Nepamirškite tų pačių filtrų pritaikyti visuose failo darbalapiuose.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="9b5dd-141">Į „Excel“ failą neįkelkite labai didelio duomenų kiekio.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="9b5dd-142">Kitu atveju tai gali turėti įtakos našumui ir „Excel“ bei jūsų sistema gali veikti lėčiau.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="9b5dd-143">Rekomenduojame visada naudoti filtrus „Įmonė“ ir „Išrašo numeris“ arba „Operacijos numeris“ kaip filtrus, skirtus jūsų failui.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="9b5dd-144">Sukonfigūravę filtrus, pasirinkite **Atnaujinti**, kad įkeltumėte duomenis.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="9b5dd-145">Redaguokite reikalingus duomenis ir tada publikuokite juos.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="9b5dd-146">Jei mygtukas **Publikuoti** neprieinamas, tikriausiai kai kurie pagrindiniai laukai nebuvo įtraukti į „Excel“ darbaknygę.</span><span class="sxs-lookup"><span data-stu-id="9b5dd-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b5dd-147">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9b5dd-147">Additional resources</span></span>

[<span data-ttu-id="9b5dd-148">Atsiskaitymo grynaisiais ir grynųjų pinigų valdymo operacijų redagavimas ir tikrinimas</span><span class="sxs-lookup"><span data-stu-id="9b5dd-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="9b5dd-149">Internetinio užsakymo ir asinchroninio kliento užsakymo operacijų redagavimas ir tikrinimas</span><span class="sxs-lookup"><span data-stu-id="9b5dd-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="9b5dd-150">Mažmeninės prekybos operacijų finansinių dimensijų redagavimas</span><span class="sxs-lookup"><span data-stu-id="9b5dd-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="9b5dd-151">Laukų įtraukimas į „Excel“ darbaknygę norint redaguoti mažmeninės prekybos operacijas</span><span class="sxs-lookup"><span data-stu-id="9b5dd-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
