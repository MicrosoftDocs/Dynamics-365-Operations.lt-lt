---
title: Vėlesnių čekių nustatymas
description: Šioje temoje paaiškinama, kaip nurodyti, ar registruoti vėlesnių čekių žurnalo įrašus ir kuriuos registravimo žurnalus naudoti su tarpuskaitos įrašais bei tiekėjo mokėjimais.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d4afd74f9a0f9018629fa92ab6595bfa94f973
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026210"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="4d7f1-103">Vėlesnių čekių nustatymas</span><span class="sxs-lookup"><span data-stu-id="4d7f1-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d7f1-104">Šioje temoje paaiškinama, kaip nurodyti, ar registruoti vėlesnių čekių žurnalo įrašus ir kuriuos registravimo žurnalus naudoti su tarpuskaitos įrašais bei tiekėjo mokėjimais.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="4d7f1-105">Taip pat galite nurodyti išrašytų čekių, gautų čekių ir išskaitomo mokesčio tarpuskaitos sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="4d7f1-106">Vėlesni čekiai, išrašomi norint atlikti ir gauti mokėjimus ateityje.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="4d7f1-107">Galite nurodyti, ar čekis turi būti rodomas apskaitos knygose prieš mokėjimo termino datą.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="4d7f1-108">Šios procedūros vaidmuo yra Iždininkas.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="4d7f1-109">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="4d7f1-110">Vėlesnių čekių nustatymas</span><span class="sxs-lookup"><span data-stu-id="4d7f1-110">Set up postdated checks</span></span>
1. <span data-ttu-id="4d7f1-111">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="4d7f1-112">Spustelėkite skirtuką Vėlesni čekiai.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="4d7f1-113">Pažymėkite arba išvalykite žymės langelį Įjungti vėlesnius čekius.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="4d7f1-114">Pažymėkite arba išvalykite žymės langelį Registruoti vėlesnių čekių žurnalo įrašus.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="4d7f1-115">Lauke Išrašytų čekių atsiskaitymo sąskaita nurodykite norimas vertes.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="4d7f1-116">Lauke Gautų čekių atsiskaitymo sąskaita nurodykite norimas vertes.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="4d7f1-117">Lauke Atsiskaitymo įrašų bendrasis žurnalas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="4d7f1-118">Lauke Perkelti vėlesnius čekius į šio tiekėjo mokėjimų žurnalą įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="4d7f1-119">Lauke Išskaitomo mokesčio atsiskaitymo sąskaita nurodykite norimas vertes.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="4d7f1-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-120">Click Save.</span></span>
11. <span data-ttu-id="4d7f1-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-121">Close the page.</span></span>
12. <span data-ttu-id="4d7f1-122">Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="4d7f1-123">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-123">Click New.</span></span>
14. <span data-ttu-id="4d7f1-124">Lauke Mokėjimo būdas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="4d7f1-125">Pažymėkite parinktį Vėlesnių čekių atsiskaitymo registravimas, jei norite nurodyti, kad čekio suma užregistruota atsiskaitymo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="4d7f1-126">Lauke Kliento sąskaita pasirinkite „Bankas‟.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="4d7f1-127">Mokėjimo metodo korespondentinė sąskaita bus bankas.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="4d7f1-128">Lauke Mokėjimo sąskaita nurodykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="4d7f1-129">Pasirinkite banko sąskaitą, naudojamą atskaityti SF sumai.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="4d7f1-130">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-130">Click Save.</span></span>
19. <span data-ttu-id="4d7f1-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-131">Close the page.</span></span>
> [!NOTE]
> <span data-ttu-id="4d7f1-132">Norėdami banko sąskaitoje užregistruoti naują čekią, kai seanso data vėlesnė arba lygi mokėjimo termino datai, turite įgalinti mokėjimo žurnalo registravimo su vėlesnėmis čekiais į banko **sąskaitą priemonės mokėjimo termino datos tikrinimą**.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-132">To be able to post a postdated check to a bank account when the session date is greater than or equal to the maturity date, you must enable the feature **Maturity date validation of posting payment journal with postdated checks to bank account**.</span></span> <span data-ttu-id="4d7f1-133">Ši funkcija leidžia registruoti tiekėjų arba klientų mokėjimų žurnalus su vėlesnėis čekiais, kai seanso data yra vėlesnė negu mokėjimo termino data arba tokia pat.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-133">This feature allows you to post payment journals for vendors or customers with postdated checks, when the session date is greater than or equal to the maturity date.</span></span>
> 
> <span data-ttu-id="4d7f1-134">Nustatydami **mokėjimo būdą** (**Mokėtinos sumos > Mokėjimo nustatymas > Mokėjimo būdai**), tarpinės **sąskaitos užpildyti** nereikia.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-134">When setting the **Method of payment** (**Accounts payable > Payment setup > Methods of payment**), do not fill in **Bridging account**.</span></span> <span data-ttu-id="4d7f1-135">Šiuo atveju, korespondentinė sąskaita užpildoma banko sąskaita, kuri nustatoma **mokėjimo metode**.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-135">In this case, the offset account is filled in with the bank account, which is set up in the **Method of payment**.</span></span>
>  
> <span data-ttu-id="4d7f1-136">Kai priemonė įgalinta, o seanso data yra mažesnė nei mokėjimo termino data, registruojant mokėjimų žurnalą rodomas šis klaidos pranešimas: "Mokėjimo termino data turi būti mažesnė už seanso datą arba tokia pat, jei korespondentinės sąskaitos tipas yra Bankas".</span><span class="sxs-lookup"><span data-stu-id="4d7f1-136">When the feature is enabled and the session date is less than the maturity date, the following error message is displayed when posting a payment journal, "Maturity date must be less or equal to the session date if offset account type is Bank".</span></span> <span data-ttu-id="4d7f1-137">Jei priemonė neįgalinta, galite užregistruoti mokėjimo žurnalą su postduotu čekiu, kai seanso data yra mažesnė nei mokėjimo termino data.</span><span class="sxs-lookup"><span data-stu-id="4d7f1-137">If the feature is not enabled, you can post a payment journal with a postdated check when the session date is less than the maturity date.</span></span>    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
