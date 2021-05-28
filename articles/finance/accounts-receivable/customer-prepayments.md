---
title: Kliento išankstiniai mokėjimai
description: Šioje temoje paaiškinama, kaip nustatyti ir apdoroti kliento išankstinius apmokėjimus (dar vadinamus klientų depozitais).
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019425"
---
# <a name="customer-prepayments"></a><span data-ttu-id="b7181-103">Kliento išankstiniai mokėjimai</span><span class="sxs-lookup"><span data-stu-id="b7181-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7181-104">Kliento išankstiniai mokėjimai naudojami tada, kai gaunate mokėjimą iš kliento, bet nėra SF, pagal kurią būtų galima sudengti mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="b7181-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="b7181-105">Šie mokėjimų tipai dar vadinami klientų depozitais.</span><span class="sxs-lookup"><span data-stu-id="b7181-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="b7181-106">Išankstinių kliento mokėjimų nustatymo ir darbo su klientais procesą sudaro šie pagrindiniai veiksmai.</span><span class="sxs-lookup"><span data-stu-id="b7181-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="b7181-107">Sukurkite kliento registravimo profilį išankstiniams mokėjimams.</span><span class="sxs-lookup"><span data-stu-id="b7181-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="b7181-108">Nustatykite **Registravimo šablonas su išankstinio mokėjimo žurnalo kvitu** parametrą.</span><span class="sxs-lookup"><span data-stu-id="b7181-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="b7181-109">Sukurkite kliento mokėjimų žurnalą ir kiekvienoje eilutėje **pažymėkite žymės langelį Išankstinio mokėjimo** žurnalo kvitas.</span><span class="sxs-lookup"><span data-stu-id="b7181-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="b7181-110">Registruokite kliento mokėjimų žurnalą.</span><span class="sxs-lookup"><span data-stu-id="b7181-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="b7181-111">Sugener pasirinkę SF sudengkite išankstinį mokėjimą naudodami puslapį **Sudengti atviras operacijas**.</span><span class="sxs-lookup"><span data-stu-id="b7181-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="b7181-112">Sukurkite kliento registravimo profilį išankstiniams mokėjimams</span><span class="sxs-lookup"><span data-stu-id="b7181-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="b7181-113">Paprastai, kai priimate išankstinius apmokėjimus ar depozitus iš savo klientų prieš pritaikant prekes ar paslaugas, arba kol sistemoje yra SF, norėsite įrašyti grynuosius pinigus kaip įsipareigojimus, o ne kaip turtą savo sąskaitų lentelėje.</span><span class="sxs-lookup"><span data-stu-id="b7181-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="b7181-114">Tačiau šių sumų įrašymo į jūsų DK reikalavimai gali skirtis, atsižvelgiant į šalį arba regioną.</span><span class="sxs-lookup"><span data-stu-id="b7181-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="b7181-115">Todėl kreipkitės į savo apskait specialistus dėl bet kokių vietinių taisyklių, kurios yra taikomos.</span><span class="sxs-lookup"><span data-stu-id="b7181-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="b7181-116">Apskritai, registravimo šablono, kurį galima naudoti išankstiniams mokėjimams, sukūrimo procesas yra toks pat kaip ir kitų registravimo šablonų kūrimo procesas.</span><span class="sxs-lookup"><span data-stu-id="b7181-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="b7181-117">Pirminis skirtumas yra pagrindinė sąskaita, kurią pasirenkate lauke **Suminė sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="b7181-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="b7181-118">Daugiau informacijos žr. [Kliento publikavimo profiliai](customer-posting-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="b7181-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="b7181-119">Nustatyti kliento išankstinių mokėjimų parametrus</span><span class="sxs-lookup"><span data-stu-id="b7181-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="b7181-120">Yra du pagrindiniai gautinų sumų parametrai, kuriuos turite apsvarstyti konfigūruokite klientų išankstinių mokėjimų sistemą.</span><span class="sxs-lookup"><span data-stu-id="b7181-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="b7181-121">Atlikite šiuos veiksmus, norėdami sukonfigūruoti parametrus.</span><span class="sxs-lookup"><span data-stu-id="b7181-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="b7181-122">Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b7181-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="b7181-123">Pasirinktinas: Skirtuke **Didžioji knyga ir pardavimo mokesčiai** „FastTab“ **Mokėjimas** nustatykite **Išankstinio mokėjimo žurnalo kvito PVM** pasirinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b7181-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="b7181-124">Lauke **Registravimo šablonas su išankstinio mokėjimo** žurnalo kvitu pasirinkite kliento registravimo šabloną, kuris bus naudojamas registruojant kliento išankstinius apmokėjimus.</span><span class="sxs-lookup"><span data-stu-id="b7181-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="b7181-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b7181-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="b7181-126">Kurti kliento išankstinio apmokėjimo kvitus</span><span class="sxs-lookup"><span data-stu-id="b7181-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="b7181-127">Kai sukuriate kliento mokėjimų žurnalą, kiekvienam išankstiniam mokėjimui turite nustatyti **išankstinio mokėjimo žurnalo** pasirinktį į **Taip** puslapyje **Kliento mokėjimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="b7181-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="b7181-128">Atlikite šiuos veiksmus norėdami sukurti kliento išankstinį mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="b7181-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="b7181-129">Eikite į **Gautinos sumos \> Mokėjimai \> Klientų mokėjimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="b7181-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="b7181-130">Pasirinkite **Naujas** žurnalui sukurti.</span><span class="sxs-lookup"><span data-stu-id="b7181-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="b7181-131">Lauke **Pavadinimas** pasirinkite norimo naudoti žurnalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b7181-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b7181-132">Jei nustatėte **PVM išankstinio mokėjimo žurnalo kvite** parinktį į **Taip** anstesnėje procedūroje, turite pasirinkti žurnalo pvadinimą, kuriame **Suma apima PVM** pasirinktą paramtrą.</span><span class="sxs-lookup"><span data-stu-id="b7181-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="b7181-133">Pasirinktinai: Laukelyje **Aprašas** įveskite išsamų aprašą.</span><span class="sxs-lookup"><span data-stu-id="b7181-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="b7181-134">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="b7181-134">Select **Lines**.</span></span>
6. <span data-ttu-id="b7181-135">Jei nėra tuščios eilutės, pasirinkite **Nauja,** kad sukurtumėte eilutę.</span><span class="sxs-lookup"><span data-stu-id="b7181-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="b7181-136">Lauke **Data** įveskite datą, nuo kurios turi būti užregistruotas išankstinis mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="b7181-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="b7181-137">Lauke **Klientas** pasirinkite klientą išankstiniam mokėjimui.</span><span class="sxs-lookup"><span data-stu-id="b7181-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="b7181-138">Pasirinktinai: Laukelyje **Aprašas** įveskite išsamų transakcijos aprašą.</span><span class="sxs-lookup"><span data-stu-id="b7181-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="b7181-139">Lauke **Kreditas** įveskite išankstinio mokėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="b7181-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="b7181-140">Lauke **Korespondentinė sąskaita** pasirinkite sąskaitą norėdami kompensuoti mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="b7181-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="b7181-141">Pavyzdžiui, pasirinkite banką arba pagrindinę sąskaitą, į kurios norite registruoti mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="b7181-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="b7181-142">Lauke **Mokėjimo būdas** pasirinkite kliento mokėjimo metodą.</span><span class="sxs-lookup"><span data-stu-id="b7181-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="b7181-143">Skirtuke **Mokėjimas** nustatykite **išankstinio mokėjimo žurnalo** pasirinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b7181-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="b7181-144">Su kiekvienu papildomu išankstiniu apmokėjimu, kuris turi būti užregistruotas, pakartokite veiksmus nuo 7 iki 13.</span><span class="sxs-lookup"><span data-stu-id="b7181-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="b7181-145">Pasirinkę **Publikuoti** užbaigsite žurnalą.</span><span class="sxs-lookup"><span data-stu-id="b7181-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="b7181-146">Išankstinių mokėjimų sudengimas su SF</span><span class="sxs-lookup"><span data-stu-id="b7181-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="b7181-147">Kliento mokėjimų darbo sritį **galite naudoti** norėdami lengvai rasti ir sudengti mokėjimus, kurie nebuvo visiškai sudengti.</span><span class="sxs-lookup"><span data-stu-id="b7181-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="b7181-148">Namų **skelbimų** skelbimų srityje pasirinkite kliento **mokėjimų išklotąją** sritį.</span><span class="sxs-lookup"><span data-stu-id="b7181-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="b7181-149">Kliento operacijų **skyriaus skirtuke** Mokėjimai **nesudengti ieškoti ir** pasirinkti sudengti norimą mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="b7181-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="b7181-150">Pasirinkite **Nustatyti operacijas**</span><span class="sxs-lookup"><span data-stu-id="b7181-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="b7181-151">Pažymėkite **SF** ir mokėjimo, kuris bus sudengtas, žymės langelį Žymėti.</span><span class="sxs-lookup"><span data-stu-id="b7181-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="b7181-152">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="b7181-152">Select **Post**.</span></span>

<span data-ttu-id="b7181-153">Daugiau informacijos apie tai, kaip sudengti atviras operacijas, ieškokite [Sudengimo peržiūra](/cash-bank-management/settlement-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b7181-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
