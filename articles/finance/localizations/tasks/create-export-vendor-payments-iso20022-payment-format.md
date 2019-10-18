---
title: Tiekėjo mokėjimų kūrimas ir eksportavimas naudojant ISO20022 mokėjimo formatą
description: Šioje procedūroje parodoma, kaip kurti mokėjimo eilutes tiekėjo mokėjimų žurnale ir generuoti tiekėjo mokėjimo failą naudojant ISO2022 kredito pervedimo pavyzdį.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b70ad94014587ba8e55735192dbe0ab2e4adf4ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185824"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="fe666-103">Tiekėjų mokėjimų kūrimas ir eksportavimas naudojant ISO20022 mokėjimo formatą</span><span class="sxs-lookup"><span data-stu-id="fe666-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fe666-104">Šioje temoje paaiškinama, kaip kurti mokėjimo eilutes tiekėjo mokėjimų žurnale ir generuoti tiekėjo mokėjimo failą naudojant ISO2022 kredito pervedimo pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="fe666-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="fe666-105">Tai yra penktoji iš penkių procedūrų, kuriose aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="fe666-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="fe666-106">Šiame pavyzdyje naudokite demonstracinių duomenų įmonę DEMF.</span><span class="sxs-lookup"><span data-stu-id="fe666-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="fe666-107">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="fe666-107">Example</span></span>

1.  <span data-ttu-id="fe666-108">Pasirinkite **Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="fe666-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.  <span data-ttu-id="fe666-109">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="fe666-109">Click **New**.</span></span>
3.  <span data-ttu-id="fe666-110">Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe666-110">In the **Name** field, enter or select a value.</span></span>
4.  <span data-ttu-id="fe666-111">Spustelėkite **Eilutės > Mokėjimo pasiūlymas -> Kurti mokėjimo pasiūlymą**.</span><span class="sxs-lookup"><span data-stu-id="fe666-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.  <span data-ttu-id="fe666-112">Išplėskite dalį **Įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="fe666-112">Expand the **Records to include** section.</span></span>
6.  <span data-ttu-id="fe666-113">Spustelėkite **Filtras**.</span><span class="sxs-lookup"><span data-stu-id="fe666-113">Click **Filter**.</span></span>
7.  <span data-ttu-id="fe666-114">Sąraše pasirinkite lentelės **Tiekėjai** eilutę ir lauką **Tiekėjo kodas**.</span><span class="sxs-lookup"><span data-stu-id="fe666-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.  <span data-ttu-id="fe666-115">Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe666-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="fe666-116">Galite taikyti bet kokį kriterijų, norėdami pasirinkti, kurias tiekėjo operacijas apmokėti, šiame pavyzdyje kaip tiekėjo kodą naudokite DE-001.</span><span class="sxs-lookup"><span data-stu-id="fe666-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12. <span data-ttu-id="fe666-117">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fe666-117">Click **OK**.</span></span>
13. <span data-ttu-id="fe666-118">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fe666-118">Click **OK**.</span></span>
14. <span data-ttu-id="fe666-119">Spustelėkite **Kurti mokėjimus**.</span><span class="sxs-lookup"><span data-stu-id="fe666-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="fe666-120">Generuokite ISO20022 mokėjimo failą.</span><span class="sxs-lookup"><span data-stu-id="fe666-120">Generate an ISO20022 payment file.</span></span>
    1.  <span data-ttu-id="fe666-121">Spustelėkite **Generuoti mokėjimus**.</span><span class="sxs-lookup"><span data-stu-id="fe666-121">Click **Generate payments**.</span></span>
    2.  <span data-ttu-id="fe666-122">Lauke **Mokėjimo metodas** įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="fe666-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.  <span data-ttu-id="fe666-123">Lauke **Failo pavadinimas** suveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe666-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="fe666-124">Šiame pavyzdyje sugeneroro uostotas failas bus suderinamas su SEPA, nes mokėjimas – eurais.</span><span class="sxs-lookup"><span data-stu-id="fe666-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="fe666-125">ISO20022 kredito pavedimas ir kiti tiekėjo mokėjimo formatai taip pat gali būti naudojami generuojant mokėjimus kitomis valiutomis.</span><span class="sxs-lookup"><span data-stu-id="fe666-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.  <span data-ttu-id="fe666-126">Lauke **Banko sąskaita** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe666-126">In the **Bank account** field, enter or select a value.</span></span>

