---
title: Užsienio valiutos kurso pasikeitimas banko sąskaitoms
description: Šioje temoje pateikiama informacija apie užsienio valiutos kurso pasikeitimą banko sąskaitoms.
author: panolte
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 11464
ms.search.region: Czech Republic, Estonia, Latvia, Lithuania, Poland
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db8dab0aef0349632d19ad407336a18641c358d1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002976"
---
# <a name="foreign-currency-revaluation-for-bank-accounts"></a><span data-ttu-id="fdc5f-103">Užsienio valiutos kurso pasikeitimas banko sąskaitoms</span><span class="sxs-lookup"><span data-stu-id="fdc5f-103">Foreign currency revaluation for bank accounts</span></span>

[!include [banner](../includes/banner.md)]

## <a name="revalue-foreign-currency-amounts-for-bank-account-transactions"></a><span data-ttu-id="fdc5f-104">Su banko sąskaita susijusių operacijų užsienio valiutos sumų perkainojimas</span><span class="sxs-lookup"><span data-stu-id="fdc5f-104">Revalue foreign currency amounts for bank account transactions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fdc5f-105">Šis skyrius taikomas tik juridiniams subjektams, kurių pagrindinis adresas yra Lenkijoje.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-105">This section applies only to legal entities that have a primary address in Poland.</span></span>

<span data-ttu-id="fdc5f-106">Galite perkainoti su banko sąskaita susijusių operacijų užsienio valiutos sumas.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-106">You can revalue foreign currency amounts for bank transactions.</span></span> <span data-ttu-id="fdc5f-107">Tada galite sukurti ataskaitą, kad peržiūrėtumėte banko operacijas, kuriose atlikta užsienio valiutos pasikeitimų koregavimų.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-107">You can then create a report to view the bank transactions that have adjustments for foreign currency revaluations.</span></span>

1. <span data-ttu-id="fdc5f-108">Pasirinkite **Grynųjų pinigų ir banko valdymas** &gt; **Periodinės užduotys** &gt; **Bankas – valiutos kurso koregavimas (FIFO/LIFO)**.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-108">Select **Cash and bank management** &gt; **Periodic tasks** &gt; **Bank - Exchange adjustment (FIFO/LIFO)**.</span></span>
2. <span data-ttu-id="fdc5f-109">Lauke **Nustatytai datai** įveskite pasikeitimo pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-109">In the **On date** field, enter an end date for the revaluation.</span></span> <span data-ttu-id="fdc5f-110">Į skaičiavimą įtraukiamos tik tos operacijos, kurių data yra ankstesnė už nurodytą.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-110">The calculation includes only transactions that have a date that is before the specified date.</span></span>
3. <span data-ttu-id="fdc5f-111">Pasirinkite **Įtrauktini įrašai** &gt; **Filtras** &gt; **Įtraukti** ir įtraukite banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-111">Select **Records to include** &gt; **Filter** &gt; **Add** to add a bank account.</span></span> <span data-ttu-id="fdc5f-112">Jei nenurodote banko sąskaitos, sumos perkainojamos visose banko sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-112">If you don't specify a bank account, amounts are revalued for all bank accounts.</span></span>
4. <span data-ttu-id="fdc5f-113">Pasirinkite **Gerai** ir uždarykite užklausos puslapį.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-113">Select **OK** to close the query page.</span></span>
5. <span data-ttu-id="fdc5f-114">Puslapyje **Užsienio valiutos kurso pasikeitimas** pasirinkite žymės langelį **Perskaičiavimas** ir perkainokite visų atvirų laikotarpių užsienio valiutos sumas.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-114">On the **Foreign currency revaluation** page, select the **Recalculation** check box to revalue foreign currency amounts for all open periods.</span></span>

## <a name="create-a-report-to-view-bank-transactions-that-have-adjustments-for-foreign-currency-revaluations"></a><span data-ttu-id="fdc5f-115">Sukurkite ataskaitą, kad peržiūrėtumėte banko operacijas, kuriose atlikta užsienio valiutos pasikeitimų koregavimų.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-115">Create a report to view bank transactions that have adjustments for foreign currency revaluations</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fdc5f-116">Šis skyrius taikomas tik juridiniams subjektams, kurių pagrindinis adresas yra Lenkijoje.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-116">This section applies only to legal entities that have a primary address in Poland.</span></span>

1. <span data-ttu-id="fdc5f-117">Pasirinkite **Grynųjų pinigų ir banko valdymas** &gt; **Užklausos ir ataskaitos** &gt; **Bankas – kurso koregavimo ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-117">Select **Cash and bank management** &gt; **Inquiries and reports** &gt; **Bank - Exchange adjustment report**.</span></span>
2. <span data-ttu-id="fdc5f-118">Pasirinkite **Įtrauktini įrašai** &gt; **Filtras** ir raskite vieną ar daugiau banko sąskaitų, kurių informaciją norite peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-118">Select **Records to include** &gt; **Filter** to find one or more bank accounts to view information for.</span></span>
3. <span data-ttu-id="fdc5f-119">Pasirinktinai: lauke **Banko sąskaita** pasirinkite banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-119">Optional: In the **Bank account** field, select a bank account.</span></span> <span data-ttu-id="fdc5f-120">Jei šį lauką paliksite tuščią, ataskaitoje bus nurodyta visų banko sąskaitų banko operacijos informacija.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-120">If you leave this field blank, the report includes bank transaction details for all bank accounts.</span></span>
4. <span data-ttu-id="fdc5f-121">Pasirinkite **Gerai**, kad sugeneruotumėte šią ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-121">Select **OK** to generate the report.</span></span> 

## <a name="calculate-exchange-rate-adjustments-for-bank-account-transactions"></a><span data-ttu-id="fdc5f-122">Banko sąskaitos operacijų valiutos kurso koregavimo skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="fdc5f-122">Calculate exchange rate adjustments for bank account transactions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fdc5f-123">Šis skyrius taikomas tik juridiniams subjektams, kurių pagrindinis adresas yra Čekijos Respublikoje, Estijoje, Lietuvoje ar Latvijoje.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-123">This section applies only to legal entities that have a primary address in the Czech Republic, Estonia, Lithuania, or Latvia.</span></span>

<span data-ttu-id="fdc5f-124">Jus turi iš naujo įvertinti ir koreguoti banko sąskaitas, jei yra valiutos kurso skirtumas tarp apskaitos valiutos ir ataskaitų valiutos.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-124">You must revalue and adjust bank accounts if there is a difference in the exchange rate between the accounting currency and the reporting currency.</span></span> <span data-ttu-id="fdc5f-125">Ši užduotis padeda apskaičiuoti tinkamą banko sąskaitų balansą tiek apskaitos, tiek ir finansinės atskaitomybės valiuta.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-125">This task helps you calculate the correct balance in both the accounting currency and the reporting currency for the bank accounts.</span></span>

1. <span data-ttu-id="fdc5f-126">Pasirinkite **Grynųjų pinigų ir banko valdymas** &gt; **Sąranka** &gt; **Grynųjų pinigų ir banko valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-126">Select **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span>
2. <span data-ttu-id="fdc5f-127">Skirtuko **Numeracijos** lauke **Nuoroda** pasirinkite nuorodos **Bankas – derinimas dėl valiutos kurso** numeraciją.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-127">On the **Number sequences** tab, in the **Reference** field, select a number sequence for the **Bank - Exchange adjustment** reference.</span></span>
3. <span data-ttu-id="fdc5f-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-128">Close the page.</span></span>
4. <span data-ttu-id="fdc5f-129">Pasirinkite **DK** &gt; **Sąranka** &gt; **Valiuta** &gt; **Valiutų kursai**.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-129">Select **General ledger** &gt; **Setup** &gt; **Currency** &gt; **Currency exchange rates**.</span></span> <span data-ttu-id="fdc5f-130">Puslapyje **Valiutų kursai** galite nurodyti valiutos kursą tarp dviejų valiutų ar valiutų porą.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-130">On the **Currency exchange rates** page, you can define the exchange rate between two currencies or a currency pair.</span></span>
5. <span data-ttu-id="fdc5f-131">Baigę uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-131">When you've finished, close the page.</span></span>
6. <span data-ttu-id="fdc5f-132">Pasirinkite **DK** &gt; **Sąranka** &gt; **DK**.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-132">Select **General ledger** &gt; **Setup** &gt; **Ledger**.</span></span> <span data-ttu-id="fdc5f-133">Laukuose **Negautas pelnas** ir **Nepatirtas nuostolis** pasirinkite pagrindinę sąskaitą, kuriai valiutų keitimo kursai yra registruojami.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-133">In the **Unrealized gain** and **Unrealized loss** fields, select the main account that the exchange rates are posted for.</span></span>
7. <span data-ttu-id="fdc5f-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-134">Close the page.</span></span>
8. <span data-ttu-id="fdc5f-135">Pasirinkite **Grynųjų pinigų ir banko valdymas** &gt; **Periodinės užduotys** &gt; **Užsienio valiutos kurso pasikeitimas**.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-135">Select **Cash and bank management** &gt; **Periodic tasks** &gt; **Foreign currency revaluation**.</span></span>
9. <span data-ttu-id="fdc5f-136">Lauke **Nustatytai datai** pasirinkite pasikeitimo datą arba koregavimo datą.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-136">In the **On date** field, select the revaluation date or adjustment date.</span></span>
10. <span data-ttu-id="fdc5f-137">Lauke **Iš valiutos** pasirinkite dabartinės valiutos kodą.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-137">In the **From currency** field, select the current currency code.</span></span> <span data-ttu-id="fdc5f-138">Lauke **Į valiutą** pasirinkite valiutą, kurią reikia pakoreguoti.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-138">In the **To currency** field, select the currency that the adjustment should be made to.</span></span>
11. <span data-ttu-id="fdc5f-139">Pasirinkite **Įtrauktini įrašai** &gt; **Filtras** ir raskite banko sąskaitą, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-139">Select **Records to include** &gt; **Filter** to find the bank account, and then select **OK**.</span></span>
12. <span data-ttu-id="fdc5f-140">Puslapyje **Užsienio valiutos kurso pasikeitimas** pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-140">On the **Foreign currency revaluation** page, select **OK**.</span></span> <span data-ttu-id="fdc5f-141">Banko sąskaitos operacijų koregavimas apskaičiuojamas pasirinktai dienai.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-141">The adjustment for the bank account transactions on the selected date is calculated.</span></span>

> [!NOTE]
> <span data-ttu-id="fdc5f-142">Didžiojoje knygoje galite peržiūrėti dvi atskiras operacijas: apskaitos valiuta ir ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="fdc5f-142">In the general ledger, you can view two separate transactions: one for the accounting currency and one for the reporting currency.</span></span>
