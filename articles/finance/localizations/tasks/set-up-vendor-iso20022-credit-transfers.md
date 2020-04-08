---
title: Nustatyti ISO20022 kredito pervedimų tiekėjus ir tiekėjų banko sąskaitas
description: Ši procedūra padeda nustatyti tiekėjo ir konkretaus tiekėjo banko sąskaitos informaciją, reikalingą generuojant ISO20022 kredito pervedimo ar bet kurio kito tiekėjo mokėjimo failą.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4809a352f87cc3d88429461a06dfe36189ed5f31
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138974"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="2e065-103">Nustatyti ISO20022 kredito pervedimų tiekėjus ir tiekėjų banko sąskaitas</span><span class="sxs-lookup"><span data-stu-id="2e065-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2e065-104">Ši procedūra padeda nustatyti tiekėjo ir konkretaus tiekėjo banko sąskaitos informaciją, reikalingą generuojant ISO20022 kredito pervedimo ar bet kurio kito tiekėjo mokėjimo failą.</span><span class="sxs-lookup"><span data-stu-id="2e065-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="2e065-105">Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DEMF.</span><span class="sxs-lookup"><span data-stu-id="2e065-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="2e065-106">Tai yra ketvirtoji iš penkių procedūrų, kuriose aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="2e065-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="2e065-107">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="2e065-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="2e065-108">Nustatyti banko informaciją</span><span class="sxs-lookup"><span data-stu-id="2e065-108">Set up bank details</span></span>
1. <span data-ttu-id="2e065-109">Pasirinkite Mokėtinos sumos > Tiekėjai > Visi tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="2e065-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="2e065-110">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="2e065-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2e065-111">Pvz., filtruokite lauką Tiekėjo sąskaita naudodami reikšmę „DE-001“.</span><span class="sxs-lookup"><span data-stu-id="2e065-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="2e065-112">Spustelėkite DE-001, kad atidarytumėte tiekėjo informaciją.</span><span class="sxs-lookup"><span data-stu-id="2e065-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="2e065-113">Veiksmų srityje spustelėkite Tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="2e065-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="2e065-114">Spustelėkite Banko sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="2e065-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="2e065-115">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="2e065-115">Click Edit.</span></span>
    * <span data-ttu-id="2e065-116">Jei banko sąskaitos nėra, turite sukurti naują.</span><span class="sxs-lookup"><span data-stu-id="2e065-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="2e065-117">Lauke SWIFT kodas surinkite „COBADEFFXXX‟.</span><span class="sxs-lookup"><span data-stu-id="2e065-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="2e065-118">Lauke IBAN surinkite „DE36200400000628808808‟.</span><span class="sxs-lookup"><span data-stu-id="2e065-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="2e065-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2e065-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="2e065-120">Tiekėjo mokėjimo būdo nustatymas</span><span class="sxs-lookup"><span data-stu-id="2e065-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="2e065-121">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="2e065-121">Click Edit.</span></span>
2. <span data-ttu-id="2e065-122">Išplėskite arba sutraukite skyrių „Mokėjimas“.</span><span class="sxs-lookup"><span data-stu-id="2e065-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="2e065-123">Lauke Mokėjimo būdas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2e065-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2e065-124">Sąraše spustelėkite saitą eilutėje SEPA CT.</span><span class="sxs-lookup"><span data-stu-id="2e065-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="2e065-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2e065-125">Click Save.</span></span>

