---
title: Nustatyti ISO20022 kredito pervedimų įmonės banko sąskaitas
description: Šioje procedūroje parodoma, kaip nustatyti konkrečios įmonės banko kodo informaciją, kurios reikia norint generuoti mokėjimo failą.
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
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca0f0af3cccd4110c3da1703112a5b0f29bd64ad
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988175"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="23edf-103">Nustatyti ISO20022 kredito pervedimų įmonės banko sąskaitas</span><span class="sxs-lookup"><span data-stu-id="23edf-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23edf-104">Šioje procedūroje parodoma, kaip nustatyti konkrečios įmonės banko kodo informaciją, kurios reikia norint generuoti mokėjimo failą.</span><span class="sxs-lookup"><span data-stu-id="23edf-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="23edf-105">Galite nustatyti informaciją, kurios reikia norint generuoti ISO 20022 kredito pervedimo formatą, tačiau, atsižvelgiant į formatą, gali būti reikalinga kita informacija, pvz., įmonės ID arba rūšiavimo kodas.</span><span class="sxs-lookup"><span data-stu-id="23edf-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="23edf-106">Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DEMF.</span><span class="sxs-lookup"><span data-stu-id="23edf-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="23edf-107">Tai yra antroji iš penkių procedūrų, kuriose aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="23edf-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="23edf-108">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="23edf-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="23edf-109">IBAN ir SWIFT kodo nustatymas</span><span class="sxs-lookup"><span data-stu-id="23edf-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="23edf-110">Eikite į Grynųjų pinigų ir banko valdymas > Banko sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="23edf-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="23edf-111">Naudokite spartųjį filtrą, kad filtruotumėte lauką Banko sąskaita reikšme „DEMF OPER‟.</span><span class="sxs-lookup"><span data-stu-id="23edf-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="23edf-112">Spustelėkite DEMF OPER, kad atidarytumėte banko kodo informaciją.</span><span class="sxs-lookup"><span data-stu-id="23edf-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="23edf-113">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="23edf-113">Click Edit.</span></span>
5. <span data-ttu-id="23edf-114">Išplėskite skyrių Papildoma identifikacija.</span><span class="sxs-lookup"><span data-stu-id="23edf-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="23edf-115">Lauke IBAN surinkite „DE89370400440532013000‟.</span><span class="sxs-lookup"><span data-stu-id="23edf-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="23edf-116">Lauke SWIFT kodas surinkite „DEUTDEFF‟.</span><span class="sxs-lookup"><span data-stu-id="23edf-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="23edf-117">Atkreipkite dėmesį, kad SWIFT / BIC nereikalingas naudojant daugelį mokėjimo formatų, tačiau vis tiek rekomenduojama užregistruoti banko kodo SWIFT / BIC.</span><span class="sxs-lookup"><span data-stu-id="23edf-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="23edf-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="23edf-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="23edf-119">Juridinio subjekto banko kodo nustatymas</span><span class="sxs-lookup"><span data-stu-id="23edf-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="23edf-120">Pasirinkite Organizacijos administravimas > Organizacijos > Juridiniai subjektai.</span><span class="sxs-lookup"><span data-stu-id="23edf-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="23edf-121">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="23edf-121">Click Edit.</span></span>
3. <span data-ttu-id="23edf-122">Išplėskite skyrių Banko sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="23edf-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="23edf-123">Lauke Banko sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="23edf-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="23edf-124">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="23edf-124">Click Save.</span></span>

