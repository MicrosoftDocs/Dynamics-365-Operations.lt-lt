---
title: DK sudengimai
description: Šioje temoje paaiškinama, kaip, naudojantis DK sudengimų puslapiu, sudengti DK operacijas ir atšaukti sudengimus.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 7704c38f878784647b44e81922b7679c0fedfbb2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248884"
---
# <a name="ledger-settlements"></a><span data-ttu-id="894eb-103">DK sudengimai</span><span class="sxs-lookup"><span data-stu-id="894eb-103">Ledger settlements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="894eb-104">DK sudengimai leidžia suderinti DK debeto ir kredito operacijas ir pažymėti jas kaip sudengtas.</span><span class="sxs-lookup"><span data-stu-id="894eb-104">Ledger settlements let you match debit and credit transactions in the general ledger, and mark them as settled.</span></span> <span data-ttu-id="894eb-105">Tokiu būdu galite būti tikri, kad susijusios operacijos panaikintos.</span><span class="sxs-lookup"><span data-stu-id="894eb-105">In this way, you can make sure that related transactions have been cleared.</span></span> <span data-ttu-id="894eb-106">Atšaukti sudengimus galite ir tada, kai jie atlikti per klaidą.</span><span class="sxs-lookup"><span data-stu-id="894eb-106">You can also reverse settlements if they were made by mistake.</span></span>

## <a name="enable-advanced-ledger-settlements"></a><span data-ttu-id="894eb-107">Išplėstinių didžiosios knygos sudengimų įgalinimas</span><span class="sxs-lookup"><span data-stu-id="894eb-107">Enable advanced ledger settlements</span></span>

<span data-ttu-id="894eb-108">Išplėstinių DK sudengimų puslapyje siūloma papildomų operacijų filtravimo ir pasirinkimo galimybių.</span><span class="sxs-lookup"><span data-stu-id="894eb-108">The advanced ledger settlements page provides additional capabilities for filtering and selecting transactions.</span></span> <span data-ttu-id="894eb-109">Norėdami įgalinti išplėstinių DK sudengimų puslapį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="894eb-109">To enable advanced ledger settlements page, follow these steps.</span></span>

1. <span data-ttu-id="894eb-110">Paspauskite **Didžioji knyga** \> **DK nustatymas** \> **DK parametrai**.</span><span class="sxs-lookup"><span data-stu-id="894eb-110">Select **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span> 
2. <span data-ttu-id="894eb-111">Skirtuke **DK sudengimai** nustatę funkcijos **Išplėstinis DK sudengimas** parinktį **Taip** įjunkite išplėstinio DK sudengimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="894eb-111">On the **Ledger settlements** tab, set the **Advanced ledger settlement** option to **Yes** to turn on the advanced ledger settlement functionality.</span></span> <span data-ttu-id="894eb-112">Dalyje **Periodinės užduotys** pasirinkus **DK sudengimai** bus naudojamas išplėstiniams sudengimams skirtas puslapis **DK sudengimai**.</span><span class="sxs-lookup"><span data-stu-id="894eb-112">The advanced **Ledger settlements** page will be used when you select **Ledger settlements** in the **Periodic tasks**.</span></span> 
3. <span data-ttu-id="894eb-113">Turite įvesti kiekvieno sąskaitų plano DK sudengimams naudojamų sąskaitų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="894eb-113">You must enter the list of accounts to use for ledger settlements for each chart of accounts.</span></span> <span data-ttu-id="894eb-114">Šis sąrašas naudojamas puslapyje **DK sudengimai** rodomam operacijų sąrašui filtruoti.</span><span class="sxs-lookup"><span data-stu-id="894eb-114">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span> <span data-ttu-id="894eb-115">Sąraše **Sąskaitų planas** pasirinkite sąskaitų planą, paskui, paspaudę **Nauja**, į sąrašą įtraukite naujų sąskaitų.</span><span class="sxs-lookup"><span data-stu-id="894eb-115">In the **Chart of accounts** list, select a chart of accounts, and then select **New** to add new accounts to the list.</span></span>

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a><span data-ttu-id="894eb-116">Operacijų sudengimas naudojantis išplėstinių DK sudengimų puslapiu</span><span class="sxs-lookup"><span data-stu-id="894eb-116">Settle transactions by using the advanced ledger settlements page</span></span>

<span data-ttu-id="894eb-117">Norėdami sudengti DK operacijas, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="894eb-117">To settle ledger transactions, follow these steps.</span></span>

1. <span data-ttu-id="894eb-118">Paspauskite **Didžioji knyga** \> **Periodinės užduotys** \> **DK sudengimai**.</span><span class="sxs-lookup"><span data-stu-id="894eb-118">Select **General ledger** \> **Periodic tasks** \> **Ledger settlements**.</span></span>
2. <span data-ttu-id="894eb-119">Nustatyti puslapio viršuje esančius filtrus:</span><span class="sxs-lookup"><span data-stu-id="894eb-119">Set the filters at the top of the page:</span></span>

    - <span data-ttu-id="894eb-120">Pasirinkite datos intervalą arba pasirinkite **Datos intervalo kodas**, kad datos intervalas būtų užpildomas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="894eb-120">Select a date range, or select **Date interval code** to automatically fill in the date range.</span></span>
    - <span data-ttu-id="894eb-121">Pakeiskite registravimo sluoksnį, pagal tai, ko jums reikia.</span><span class="sxs-lookup"><span data-stu-id="894eb-121">Change the posting layer as you require.</span></span>
    - <span data-ttu-id="894eb-122">Norėdami, kad DK sąskaita ir dimensijos būtų rodomos atskirai, pasirinkite finansinių dimensijų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="894eb-122">To show the ledger account and dimensions separately, select a financial dimension set.</span></span>

3. <span data-ttu-id="894eb-123">Pasirinkite **Rodyti operacijas**, kad būtų rodomos visos jūsų nustatytus filtrus atitinkančios operacijos ir nustatant ankstesniame skyriuje pateiktą sąskaitų plano sąrašą nurodytų sąskaitų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="894eb-123">Select **Display transactions** to show all the transactions that match the filters that you set and the list of accounts that you specified when you set up the chart of accounts list in the previous section.</span></span> <span data-ttu-id="894eb-124">Pakeitus bet kurį filtrą arba dimensijų rinkinius, būtina dar kartą pasirinkti **Rodyti operacijas**.</span><span class="sxs-lookup"><span data-stu-id="894eb-124">If you change any of the filters or the dimension sets, you must select **Display transactions** again.</span></span>
4. <span data-ttu-id="894eb-125">Pasirinkite vieną ar kelias eilutes, kurias ketinate sudengti.</span><span class="sxs-lookup"><span data-stu-id="894eb-125">Select one or more lines that you're considering for settlement.</span></span> <span data-ttu-id="894eb-126">Puslapio viršuje esančio lauko **Pasirinkta suma** vertė didėja arba mažėja, priklausomai nuo bendros jūsų pasirinktų eilučių sumos.</span><span class="sxs-lookup"><span data-stu-id="894eb-126">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
5. <span data-ttu-id="894eb-127">Pasirinkę operacijas, paspauskite **Žymėti pasirinktas**.</span><span class="sxs-lookup"><span data-stu-id="894eb-127">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="894eb-128">Kiekvienos pasirinktos operacijos stulpelyje **Pažymėta** rodoma žymės varnelė.</span><span class="sxs-lookup"><span data-stu-id="894eb-128">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="894eb-129">Be to, virš tinklelio esančio lauko **Pažymėta suma** vertė didėja arba mažėja, priklausomai nuo bendros jūsų pžymėtų eilučių sumos.</span><span class="sxs-lookup"><span data-stu-id="894eb-129">Additionally, the value of the **Marked amount** field above the grid increases or decreases by the total amount on the lines that you marked.</span></span>
6. <span data-ttu-id="894eb-130">Kai **Pažymėta suma** vertė yra **0** (nulis), pasirinkite **Sudengti pažymėtas operacijas**.</span><span class="sxs-lookup"><span data-stu-id="894eb-130">When the **Marked amount** value is **0** (zero), select **Settle marked transactions**.</span></span> <span data-ttu-id="894eb-131">Pažymėtų operacijų būsena atnaujinama į **Sudengta**.</span><span class="sxs-lookup"><span data-stu-id="894eb-131">The status of the marked transactions is updated to **Settled**.</span></span>

## <a name="make-transactions-easier-to-find"></a><span data-ttu-id="894eb-132">Lengvesnė operacijų paieška</span><span class="sxs-lookup"><span data-stu-id="894eb-132">Make transactions easier to find</span></span>

<span data-ttu-id="894eb-133">Puslapyje **DK sudengimai** pateikiama galimybių, kuriomis naudojantis paprasčiau pastebėti operacijas, kurias reikia sudengti.</span><span class="sxs-lookup"><span data-stu-id="894eb-133">The **Ledger settlements** page includes capabilities that make it easier to see the transactions that you need for settlement.</span></span>

- <span data-ttu-id="894eb-134">Naudojantis mygtuku **Panaikinti žymėjimus** išvalomi visų pažymėtų eilučių laukai **Pažymėta**.</span><span class="sxs-lookup"><span data-stu-id="894eb-134">The **Unmark selected** button clears the **Marked** field for all lines that are selected.</span></span>
- <span data-ttu-id="894eb-135">Naudodamiesi filtru **Pažymėta** galite filtruoti operacijas, pagal tai, ar jų laukas **Pažymėta** pažymėtas, ar ne.</span><span class="sxs-lookup"><span data-stu-id="894eb-135">The **Marked** filter lets you filter transactions based on whether the **Marked** field for them is selected or cleared.</span></span>
- <span data-ttu-id="894eb-136">Naudodamiesi filtru **Būsena** galite filtruoti operacijas, pagal tai, ar jų būsena **Sudengta**, ar **Nesudengta**.</span><span class="sxs-lookup"><span data-stu-id="894eb-136">The **Status** filter lets you filter transactions based on whether their status is **Settled** or **Not settled**.</span></span>
- <span data-ttu-id="894eb-137">Naudodamiesi mygtuku **Rūšiuoti pagal absoliučią sumą** galite rūšiuoti sumas pagal absoliučią vertę, kad galėtumėte sugrupuoti tos pačios sumos debetus ir kreditus.</span><span class="sxs-lookup"><span data-stu-id="894eb-137">The **Sort by absolute amount** button lets you sort the amounts by absolute value, so that you can group together debits and credits that have the same amount.</span></span>

## <a name="reverse-a-settlement"></a><span data-ttu-id="894eb-138">Sudengimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="894eb-138">Reverse a settlement</span></span>

<span data-ttu-id="894eb-139">Galite atšaukti per klaida atliktą sudengimą.</span><span class="sxs-lookup"><span data-stu-id="894eb-139">You can reverse a settlement that was made by mistake.</span></span>

1. <span data-ttu-id="894eb-140">Atlikite nuo 1 iki 3 skyriaus „Operacijų sudengimas naudojantis išplėstinių DK sudengimų puslapiu“ veiksmus, kad būtų rodomos ieškomos operacijos.</span><span class="sxs-lookup"><span data-stu-id="894eb-140">Follow steps 1 through 3 in the "Settle transactions by using advanced ledger settlements page" section to show the transactions that you're looking for.</span></span>
2. <span data-ttu-id="894eb-141">Filtre **Būsena** pasirinkite **Sudengta**.</span><span class="sxs-lookup"><span data-stu-id="894eb-141">In the **Status** filter, select **Settled**.</span></span>
3. <span data-ttu-id="894eb-142">Pasirinkite vieną ar kelias eilutes, kurias ketinate atkurti.</span><span class="sxs-lookup"><span data-stu-id="894eb-142">Select one or more lines that you're considering for reversal.</span></span> <span data-ttu-id="894eb-143">Puslapio viršuje esančio lauko **Pasirinkta suma** vertė didėja arba mažėja, priklausomai nuo bendros jūsų pasirinktų eilučių sumos.</span><span class="sxs-lookup"><span data-stu-id="894eb-143">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
4. <span data-ttu-id="894eb-144">Pasirinkę operacijas, paspauskite **Žymėti pasirinktas**.</span><span class="sxs-lookup"><span data-stu-id="894eb-144">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="894eb-145">Kiekvienos pasirinktos operacijos stulpelyje **Pažymėta** rodoma žymės varnelė.</span><span class="sxs-lookup"><span data-stu-id="894eb-145">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="894eb-146">Be to, puslapio viršuje esančio lauko **Pažymėta suma** vertė didėja arba mažėja, priklausomai nuo bendros jūsų pažymėtų eilučių sumos.</span><span class="sxs-lookup"><span data-stu-id="894eb-146">Additionally, the value of the **Marked amount** field at the top of the page increases or decreases by the total amount on the lines that you marked.</span></span>
5. <span data-ttu-id="894eb-147">Kai **Pažymėta suma** vertė yra **0** (nulis), pasirinkite **Atšaukti pažymėtas operacijas**.</span><span class="sxs-lookup"><span data-stu-id="894eb-147">When the **Marked amount** value is **0** (zero), select **Reverse marked transactions**.</span></span> <span data-ttu-id="894eb-148">Pažymėtų operacijų būsena atnaujinama į **Nesudengta**.</span><span class="sxs-lookup"><span data-stu-id="894eb-148">The status of the marked transactions is updated to **Not settled**.</span></span>

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a><span data-ttu-id="894eb-149">Į operacijų sąrašą įtrauktų sąskaitų sąrašo atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="894eb-149">Update the list of accounts that are included in the list of transactions</span></span>

<span data-ttu-id="894eb-150">Paspauskite **DK sudengimo sąskaitos**, kad būtų atidarytas dialogo langas, kuriame galėsite redaguoti į operacijų sąrašą įtrauktas sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="894eb-150">Select **Ledger settlement accounts** to open a dialog box where you can edit the accounts that are included in the list of transactions.</span></span> <span data-ttu-id="894eb-151">Norėdami į sąrašą įtraukti naujų sąskaitų, paspauskite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="894eb-151">Select **New** to add new accounts to the list.</span></span> <span data-ttu-id="894eb-152">Šis sąrašas naudojamas puslapyje **DK sudengimai** rodomam operacijų sąrašui filtruoti.</span><span class="sxs-lookup"><span data-stu-id="894eb-152">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]