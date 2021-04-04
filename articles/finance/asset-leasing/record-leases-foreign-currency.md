---
title: Nuomų įrašymas užsienio valiutomis
description: Šioje temoje paaiškinama, kaip įrašyti nuomą kitomis valiutomis nei apskaitos ar ataskaitų valiuta.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fd4d04ae7e89b8ce41ed745c643b8e736484789d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241495"
---
# <a name="record-leases-in-foreign-currencies"></a><span data-ttu-id="bd909-103">Nuomų įrašymas užsienio valiutomis</span><span class="sxs-lookup"><span data-stu-id="bd909-103">Record leases in foreign currencies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd909-104">Puslapyje **DK sąranka** yra nustatytos nuomos, kuri yra kita nei apskaitos valiuta arba ataskaitų valiuta, turto nuomos sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="bd909-104">Asset leasing accounts for leases that are in currencies other than the accounting currency or the reporting currency are established on the **Ledger setup** page.</span></span> <span data-ttu-id="bd909-105">Visas nuomos sutartis turi būti įvesta į savo operacijų valiutą.</span><span class="sxs-lookup"><span data-stu-id="bd909-105">All leases should be entered in their transaction currency.</span></span> <span data-ttu-id="bd909-106">Kitaip tariant, jie turėtų būti įvedami į nuomos sutartyje nurodytą valiutą.</span><span class="sxs-lookup"><span data-stu-id="bd909-106">In other words, they should be entered in the currency that is specified in the lease contract.</span></span> <span data-ttu-id="bd909-107">Šioje temoje paaiškinama, kaip įrašyti nuomą kitomis valiutomis nei apskaitos ar ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="bd909-107">This topic explains how to record leases in currencies other than the accounting or reporting currency.</span></span>

<span data-ttu-id="bd909-108">Jei įvesite nuomos užsienio valiuta, naudojimo teise valdomas turtas yra nuvertėja ir apskaitos valiuta, ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="bd909-108">If you enter a lease in a foreign currency, the right-of-use (ROU) asset is depreciated in both the accounting currency and the reporting currency.</span></span> <span data-ttu-id="bd909-109">Šios valiutos sukonfigūruotos puslapyje **DK sąranka**.</span><span class="sxs-lookup"><span data-stu-id="bd909-109">These currencies are configured on the **Ledger setup** page.</span></span> <span data-ttu-id="bd909-110">Taip pat naudojama ilgalaikiam turtui.</span><span class="sxs-lookup"><span data-stu-id="bd909-110">This behavior is also used in Fixed assets.</span></span> <span data-ttu-id="bd909-111">Kai kuriate nuomą užsienio valiuta, lauke **valiuta** pasirinkite operacijos valiutą.</span><span class="sxs-lookup"><span data-stu-id="bd909-111">When you create a lease in a foreign currency, select the transaction currency in the **Currency** field.</span></span>

<span data-ttu-id="bd909-112">Apskaitos valiutos kursas yra numatytoji vertė lauke **Apskaitos valiutos keitimo kursas**.</span><span class="sxs-lookup"><span data-stu-id="bd909-112">The exchange rate of the accounting currency is the default value in **Accounting currency exchange rate** field.</span></span> <span data-ttu-id="bd909-113">Ataskaitų valiutos kursas yra numatytoji vertė lauke **Ataskaitų valiutos keitimo kursas**.</span><span class="sxs-lookup"><span data-stu-id="bd909-113">The exchange rate of the reporting currency is the default value in the **Reporting currency exchange rate** field.</span></span> <span data-ttu-id="bd909-114">Šie valiutos kursai buvo veiksmingi nuomos pradžios dieną.</span><span class="sxs-lookup"><span data-stu-id="bd909-114">These exchange rates were effective on the commencement date of the lease.</span></span> <span data-ttu-id="bd909-115">Laukai **Apskaitos valiutos kursas** ir **Ataskaitų valiutos kursas** yra puslapio **Nuomos informacija** „FastTab“ **Finansinių ir ataskaitų valiutos keitimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="bd909-115">The **Accounting currency exchange rate** and **Reporting currency exchange rate** fields, are in the **Financial and reporting exchange information** FastTab, on the **Lease details** page.</span></span>

1. <span data-ttu-id="bd909-116">Pasirinkite žymės langelį **Fiksuotą tarifas**, kad būtų nepaisoma automatiškai įvesto valiutos kurso, o tada įveskite naują tarifą.</span><span class="sxs-lookup"><span data-stu-id="bd909-116">Select the **Fixed rate** check box to override the exchange rate that was automatically entered, and then enter the new rate.</span></span>
2. <span data-ttu-id="bd909-117">Kituose laukuose įveskite reikiamą nuomos informaciją ir pasirinkite **Kurti grafikus**.</span><span class="sxs-lookup"><span data-stu-id="bd909-117">In the other fields, enter the information that is required for the lease, and then select **Create schedules**.</span></span>
3. <span data-ttu-id="bd909-118">Puslapyje **Nuomos informacija** pasirinkite **Knygos**.</span><span class="sxs-lookup"><span data-stu-id="bd909-118">On the new **Lease details** page, select **Books**.</span></span>
4. <span data-ttu-id="bd909-119">Puslapio **Nuomos knyga** skirtuke **Finansinės ir ataskaitų valiutos keitimo informacija** patikrinkite laukų **Apskaitos valiutos pradinis naudojimo teise valdomas turtas** ir **Ataskaitų valiutos pradinis naudojimo teise valdomas turtas** vertes.</span><span class="sxs-lookup"><span data-stu-id="bd909-119">On the **Lease book** page, on the **Financial and reporting exchange information** tab, verify the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span> <span data-ttu-id="bd909-120">Kiekvienas iš šių laukų nurodo, kaip išverstas ROU turto balansas atitinkama valiuta.</span><span class="sxs-lookup"><span data-stu-id="bd909-120">Each of these fields shows the translated ROU asset balance in the corresponding currency.</span></span> <span data-ttu-id="bd909-121">Šie laukai atnaujinami kaskart, kai pakeičiate finansinę informaciją.</span><span class="sxs-lookup"><span data-stu-id="bd909-121">These fields are updated whenever you change any financial information.</span></span> <span data-ttu-id="bd909-122">Prieš patvirtindami apmokėjimo grafiką pasirinkite **Kurti grafikus**.</span><span class="sxs-lookup"><span data-stu-id="bd909-122">Select **Create schedules** before you confirm the payment schedule.</span></span>

    <span data-ttu-id="bd909-123">Pradinis pripažinimo žurnalo įrašas įrašo naudojimo teise valdomą turtą, kuris naudoja valiutų kursus, kurie išvardyti nuomos sutartyje.</span><span class="sxs-lookup"><span data-stu-id="bd909-123">The initial recognition journal entry records the ROU asset that uses the currency exchange rates that are listed on the lease.</span></span> <span data-ttu-id="bd909-124">Be to, į žurnalo įrašą įtraukiamos laukų **Apskaitos valiutos pradinis naudojimo teise valdomas turtas** ir **Ataskaitų valiutos pradinis naudojimo teise valdomas turtas** vertės.</span><span class="sxs-lookup"><span data-stu-id="bd909-124">The journal entry also includes the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

## <a name="subsequent-measurement-for-foreign-currency-leases"></a><span data-ttu-id="bd909-125">Vėlesnis užsienio valiutos nuomos matavimas</span><span class="sxs-lookup"><span data-stu-id="bd909-125">Subsequent measurement for foreign currency leases</span></span>

<span data-ttu-id="bd909-126">Nusidėvėjimo grafikas parodo numatomas nusidėvėjimo išlaidų sumas ataskaitų valiuta, apskaitos valiuta ir operacijos valiuta.</span><span class="sxs-lookup"><span data-stu-id="bd909-126">The depreciation schedule shows the expected depreciation expense amounts in the reporting currency, the accounting currency, and the transaction currency.</span></span>

<span data-ttu-id="bd909-127">Norėdami peržiūrėti naudojimo teise valdomo turto balansus ir nusidėvėjimo sumas ataskaitų valiuta arba apskaitos valiuta, atsidarykite puslapį **Turto nusidėvėjimo grafikas** ir pasirinkite žymės langelį **Rodyti apskaitos valiutos sumas** arba **Rodyti ataskaitų valiutos sumas**.</span><span class="sxs-lookup"><span data-stu-id="bd909-127">To view the ROU asset balances and depreciation amounts in either the reporting currency or the accounting currency, open the **Asset depreciation schedule** page, and select the **Show accounting currency amounts** or **Show reporting currency amounts** check box.</span></span>

<span data-ttu-id="bd909-128">Kai sukuriate nusidėvėjimo išlaidų žurnalo įrašus su nuoma, išreikšta užsienio valiuta, įrašas naudoja valiutos kursus, kurie išvardyti nuomos sutartyje.</span><span class="sxs-lookup"><span data-stu-id="bd909-128">When you create the depreciation expense journal entries against a lease that is denominated in a foreign currency, the entry uses the exchange rates that are listed on the lease.</span></span> <span data-ttu-id="bd909-129">Be to, jis naudoja laukų **Apskaitos valiutos pradinis naudojimo teise valdomas turtas** ir **Ataskaitų valiutos pradinis naudojimo teise valdomas turtas** vertes.</span><span class="sxs-lookup"><span data-stu-id="bd909-129">It also uses the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

<span data-ttu-id="bd909-130">Galutinę nusidėvėjimo išlaidų sumą galima apskaičiuoti naudojant šiek tiek kitokį valiutos kursą, kad naudojimo teise valdomas turtas būtų visiškai nusidėvėjęs tiek apskaitos valiuta, tiek ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="bd909-130">The final depreciation expense amount can be calculated by using a slightly different exchange rate, so that the ROU asset is fully depreciated in both the accounting currency and the reporting currency.</span></span>

<span data-ttu-id="bd909-131">Jei nuoma buvo perklasifikuota kaip **Atidėtasis nuomos mokėjimas**, sistema automatiškai panaikina apskaitos ir ataskaitų valiutų kursus, jei jie jau nustatyti.</span><span class="sxs-lookup"><span data-stu-id="bd909-131">If the lease has been reclassified as **Deferred rent**, the system automatically clears the exchange rates of the accounting and reporting currencies, if they have already been defined.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]