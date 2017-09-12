--- 
title: "Nustatyti ISO20022 kredito pervedimų įmonės banko sąskaitas"
description: "Šioje procedūroje parodoma, kaip nustatyti konkrečios įmonės banko kodo informaciją, kurios reikia norint generuoti mokėjimo failą."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1d0eabdfdeb5ed7d0bdb6df87ebdfa0d41e87492
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="1d4f2-103">Nustatyti ISO20022 kredito pervedimų įmonės banko sąskaitas</span><span class="sxs-lookup"><span data-stu-id="1d4f2-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d4f2-104">Šioje procedūroje parodoma, kaip nustatyti konkrečios įmonės banko kodo informaciją, kurios reikia norint generuoti mokėjimo failą.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="1d4f2-105">Galite nustatyti informaciją, kurios reikia norint generuoti ISO 20022 kredito pervedimo formatą, tačiau, atsižvelgiant į formatą, gali būti reikalinga kita informacija, pvz., įmonės ID arba rūšiavimo kodas.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="1d4f2-106">Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DEMF.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="1d4f2-107">Tai yra antroji iš penkių procedūrų, kuriose aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="1d4f2-108">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="1d4f2-109">IBAN ir SWIFT kodo nustatymas</span><span class="sxs-lookup"><span data-stu-id="1d4f2-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="1d4f2-110">Eikite į Grynųjų pinigų ir banko valdymas > Banko sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="1d4f2-111">Naudokite spartųjį filtrą, kad filtruotumėte lauką Banko sąskaita reikšme „DEMF OPER‟.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="1d4f2-112">Spustelėkite DEMF OPER, kad atidarytumėte banko kodo informaciją.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="1d4f2-113">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-113">Click Edit.</span></span>
5. <span data-ttu-id="1d4f2-114">Išplėskite skyrių Papildoma identifikacija.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="1d4f2-115">Lauke IBAN surinkite „DE89370400440532013000‟.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="1d4f2-116">Lauke SWIFT kodas surinkite „DEUTDEFF‟.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="1d4f2-117">Atkreipkite dėmesį, kad SWIFT / BIC nereikalingas naudojant daugelį mokėjimo formatų, tačiau vis tiek rekomenduojama užregistruoti banko kodo SWIFT / BIC.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="1d4f2-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="1d4f2-119">Juridinio subjekto banko kodo nustatymas</span><span class="sxs-lookup"><span data-stu-id="1d4f2-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="1d4f2-120">Pasirinkite Organizacijos administravimas > Organizacijos > Juridiniai subjektai.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="1d4f2-121">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-121">Click Edit.</span></span>
3. <span data-ttu-id="1d4f2-122">Išplėskite skyrių Banko sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="1d4f2-123">Lauke Banko sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="1d4f2-124">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1d4f2-124">Click Save.</span></span>


