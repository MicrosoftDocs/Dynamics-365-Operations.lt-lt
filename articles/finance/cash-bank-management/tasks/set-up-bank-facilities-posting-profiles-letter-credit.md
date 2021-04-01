---
title: Nustatyti akredityvo banko priemones ir registravimo šablonus
description: Ši procedūra padeda sukurti banko priemonę ir užregistruoti šabloną, reikalingą norint apdoroti akredityvus.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc94100461bc82e9e7cd243f198711ab61a79b0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225278"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="a4eff-103">Nustatyti akredityvo banko priemones ir registravimo šablonus</span><span class="sxs-lookup"><span data-stu-id="a4eff-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4eff-104">Ši procedūra padeda sukurti banko priemonę ir užregistruoti šabloną, reikalingą norint apdoroti akredityvus.</span><span class="sxs-lookup"><span data-stu-id="a4eff-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="a4eff-105">Šioje užduotyje naudojama demonstracinė įmonė „USMF‟.</span><span class="sxs-lookup"><span data-stu-id="a4eff-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="a4eff-106">Didžiosios knygos parametras</span><span class="sxs-lookup"><span data-stu-id="a4eff-106">General ledger parameter</span></span>
1. <span data-ttu-id="a4eff-107">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="a4eff-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="a4eff-108">Išplėskite skyrių Banko dokumentas.</span><span class="sxs-lookup"><span data-stu-id="a4eff-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="a4eff-109">Pasirinkite parinktį Įjungti importo akredityvą.</span><span class="sxs-lookup"><span data-stu-id="a4eff-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="a4eff-110">Pasirinkite parinktį Įjungti eksporto akredityvą.</span><span class="sxs-lookup"><span data-stu-id="a4eff-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="a4eff-111">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a4eff-111">Click Save.</span></span>
6. <span data-ttu-id="a4eff-112">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a4eff-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="a4eff-113">Banko priemonės kūrimas</span><span class="sxs-lookup"><span data-stu-id="a4eff-113">Create Bank facility</span></span>
1. <span data-ttu-id="a4eff-114">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymai > Banko priemonės.</span><span class="sxs-lookup"><span data-stu-id="a4eff-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="a4eff-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a4eff-115">Click New.</span></span>
3. <span data-ttu-id="a4eff-116">Lauke Priemonių grupė įveskite banko priemonių grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="a4eff-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="a4eff-117">Lauke Aprašas įveskite banko priemonių grupės aprašymą.</span><span class="sxs-lookup"><span data-stu-id="a4eff-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="a4eff-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a4eff-118">Click Save.</span></span>
6. <span data-ttu-id="a4eff-119">Spustelėkite skirtuką Paslaugų tipai.</span><span class="sxs-lookup"><span data-stu-id="a4eff-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="a4eff-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a4eff-120">Click New.</span></span>
8. <span data-ttu-id="a4eff-121">Lauke Paslaugų tipai įveskite unikalų kodą.</span><span class="sxs-lookup"><span data-stu-id="a4eff-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="a4eff-122">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a4eff-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="a4eff-123">Lauke Priemonių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a4eff-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="a4eff-124">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a4eff-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="a4eff-125">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a4eff-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="a4eff-126">Lauke Priemonės pobūdis pasirinkite banko priemonės pobūdį.</span><span class="sxs-lookup"><span data-stu-id="a4eff-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="a4eff-127">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a4eff-127">Click Save.</span></span>
15. <span data-ttu-id="a4eff-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a4eff-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="a4eff-129">Banko registravimo šablonas</span><span class="sxs-lookup"><span data-stu-id="a4eff-129">Bank posting profile</span></span>
1. <span data-ttu-id="a4eff-130">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymai > Banko dokumentų registravimo šablonas.</span><span class="sxs-lookup"><span data-stu-id="a4eff-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="a4eff-131">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a4eff-131">Click New.</span></span>
3. <span data-ttu-id="a4eff-132">Lauke Sąskaitos / grupės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a4eff-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a4eff-133">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a4eff-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a4eff-134">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a4eff-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a4eff-135">Pasirinkite pagrindinę atsiskaitymo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="a4eff-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="a4eff-136">Ši sąskaita naudojama skaičiuojant grynųjų pinigų srautų prognozę.</span><span class="sxs-lookup"><span data-stu-id="a4eff-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="a4eff-137">Lauke Išlaidų sąskaita pasirinkite išlaidų operacijų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="a4eff-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="a4eff-138">Lauke Maržos sąskaita pasirinkite maržos operacijų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="a4eff-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="a4eff-139">Ši sąskaita debetuojama registruojant atidarymo maržą ir kredituojama registruojant mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="a4eff-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="a4eff-140">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a4eff-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]