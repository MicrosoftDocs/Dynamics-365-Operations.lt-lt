---
title: Vėlesnių čekių nustatymas
description: Šioje temoje paaiškinama, kaip nurodyti, ar registruoti vėlesnių čekių žurnalo įrašus ir kuriuos registravimo žurnalus naudoti su tarpuskaitos įrašais bei tiekėjo mokėjimais.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b677056f11a8733bf90f18110b8ee47f6447503b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976296"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="c62d2-103">Vėlesnių čekių nustatymas</span><span class="sxs-lookup"><span data-stu-id="c62d2-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c62d2-104">Šioje temoje paaiškinama, kaip nurodyti, ar registruoti vėlesnių čekių žurnalo įrašus ir kuriuos registravimo žurnalus naudoti su tarpuskaitos įrašais bei tiekėjo mokėjimais.</span><span class="sxs-lookup"><span data-stu-id="c62d2-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="c62d2-105">Taip pat galite nurodyti išrašytų čekių, gautų čekių ir išskaitomo mokesčio tarpuskaitos sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="c62d2-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="c62d2-106">Vėlesni čekiai, išrašomi norint atlikti ir gauti mokėjimus ateityje.</span><span class="sxs-lookup"><span data-stu-id="c62d2-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="c62d2-107">Galite nurodyti, ar čekis turi būti rodomas apskaitos knygose prieš mokėjimo termino datą.</span><span class="sxs-lookup"><span data-stu-id="c62d2-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="c62d2-108">Šios procedūros vaidmuo yra Iždininkas.</span><span class="sxs-lookup"><span data-stu-id="c62d2-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="c62d2-109">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="c62d2-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="c62d2-110">Vėlesnių čekių nustatymas</span><span class="sxs-lookup"><span data-stu-id="c62d2-110">Set up postdated checks</span></span>
1. <span data-ttu-id="c62d2-111">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="c62d2-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="c62d2-112">Spustelėkite skirtuką Vėlesni čekiai.</span><span class="sxs-lookup"><span data-stu-id="c62d2-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="c62d2-113">Pažymėkite arba išvalykite žymės langelį Įjungti vėlesnius čekius.</span><span class="sxs-lookup"><span data-stu-id="c62d2-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="c62d2-114">Pažymėkite arba išvalykite žymės langelį Registruoti vėlesnių čekių žurnalo įrašus.</span><span class="sxs-lookup"><span data-stu-id="c62d2-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="c62d2-115">Lauke Išrašytų čekių atsiskaitymo sąskaita nurodykite norimas vertes.</span><span class="sxs-lookup"><span data-stu-id="c62d2-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="c62d2-116">Lauke Gautų čekių atsiskaitymo sąskaita nurodykite norimas vertes.</span><span class="sxs-lookup"><span data-stu-id="c62d2-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="c62d2-117">Lauke Atsiskaitymo įrašų bendrasis žurnalas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="c62d2-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="c62d2-118">Lauke Perkelti vėlesnius čekius į šio tiekėjo mokėjimų žurnalą įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="c62d2-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="c62d2-119">Lauke Išskaitomo mokesčio atsiskaitymo sąskaita nurodykite norimas vertes.</span><span class="sxs-lookup"><span data-stu-id="c62d2-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="c62d2-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c62d2-120">Click Save.</span></span>
11. <span data-ttu-id="c62d2-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c62d2-121">Close the page.</span></span>
12. <span data-ttu-id="c62d2-122">Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="c62d2-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="c62d2-123">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c62d2-123">Click New.</span></span>
14. <span data-ttu-id="c62d2-124">Lauke Mokėjimo būdas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c62d2-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="c62d2-125">Pažymėkite parinktį Vėlesnių čekių atsiskaitymo registravimas, jei norite nurodyti, kad čekio suma užregistruota atsiskaitymo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="c62d2-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="c62d2-126">Lauke Kliento sąskaita pasirinkite „Bankas‟.</span><span class="sxs-lookup"><span data-stu-id="c62d2-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="c62d2-127">Mokėjimo metodo korespondentinė sąskaita bus bankas.</span><span class="sxs-lookup"><span data-stu-id="c62d2-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="c62d2-128">Lauke Mokėjimo sąskaita nurodykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="c62d2-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="c62d2-129">Pasirinkite banko sąskaitą, naudojamą atskaityti SF sumai.</span><span class="sxs-lookup"><span data-stu-id="c62d2-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="c62d2-130">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c62d2-130">Click Save.</span></span>
19. <span data-ttu-id="c62d2-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c62d2-131">Close the page.</span></span>

