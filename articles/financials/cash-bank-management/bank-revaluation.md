---
title: Banko užsienio valiutos kurso pasikeitimas
description: Šioje temoje pateikta banko užsienio valiutos kurso pasikeitimo proceso apžvalga. Temoje pateikiama informacija apie sąranką, proceso vykdymą, proceso apskaičiavimą ir kurso keitimo operacijų atšaukimą.
author: mikefalkner
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankCurrencyRevalHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: 10
ms.openlocfilehash: 353153a3a5cbcb27749f21582fcf83ac4f3a8f36
ms.sourcegitcommit: 56ec43e459ba93f495bc76fed23d6737218ef37e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/17/2019
ms.locfileid: "1591765"
---
# <a name="bank-foreign-currency-revaluation"></a><span data-ttu-id="18762-104">Banko užsienio valiutos kurso pasikeitimas</span><span class="sxs-lookup"><span data-stu-id="18762-104">Bank foreign currency revaluation</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="18762-105">Šioje temoje pateikta banko užsienio valiutos kurso pasikeitimo proceso apžvalga.</span><span class="sxs-lookup"><span data-stu-id="18762-105">This topic provides an overview of the process of bank foreign currency revaluation.</span></span> <span data-ttu-id="18762-106">Temoje aiškinama, kaip nustatyti ir vykdyti procesą, bei pateikiama informacija apie proceso apskaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="18762-106">It explains how to set up and run the process, and provides information about the calculation for the process.</span></span> <span data-ttu-id="18762-107">Temoje taip pat aiškinama, kaip atšaukti kurso keitimo operacijas, jei to prireiktų.</span><span class="sxs-lookup"><span data-stu-id="18762-107">It also explains how to reverse revaluation transactions, if reversal is required.</span></span>

<span data-ttu-id="18762-108">Laikotarpio pabaigoje tvarkant apskaitos konvencijas būtina banko sąskaitų balansus užsienio valiuta perkainoti naudojant skirtingus valiutų kursų tipus (dabartinis, retrospektyvinis, vidurkio ir t. t.).</span><span class="sxs-lookup"><span data-stu-id="18762-108">As part of a period end, accounting conventions require that bank account balances in foreign currencies be revalued by using different exchange rate types (current, historical, average, and so on).</span></span> <span data-ttu-id="18762-109">Banko užsienio valiutos kurso pasikeitimo funkciją galima naudoti norint perkainoti vieną ar kelias banko sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="18762-109">The bank foreign currency revaluation feature can be used to revalue one or more bank accounts.</span></span> <span data-ttu-id="18762-110">Be to, ši funkcija taip pat yra visuotinė.</span><span class="sxs-lookup"><span data-stu-id="18762-110">The feature is also a global feature.</span></span> <span data-ttu-id="18762-111">Tai reiškia, kad lankydamiesi viename puslapyje gali perkainoti visų juridinių subjektų, prie kurių turite prieigą, bankus.</span><span class="sxs-lookup"><span data-stu-id="18762-111">Therefore, from a single page, you can revalue banks across all the legal entities that you have access to.</span></span>

> [!NOTE]
> <span data-ttu-id="18762-112">Kai paleidžiate kurso keitimo procesą, kiekvienos banko sąskaitos, registruotos užsienio valiuta, balansas bus perkainotas.</span><span class="sxs-lookup"><span data-stu-id="18762-112">When you run the revaluation process, the balance in each bank account that is posted in a foreign currency will be revalued.</span></span> <span data-ttu-id="18762-113">Perkainojimo metu sukurtas negauto pelno arba nuostolio operacijas sugeneruoja sistema.</span><span class="sxs-lookup"><span data-stu-id="18762-113">The unrealized gain or loss transactions that are created during the revaluation process are system-generated.</span></span> <span data-ttu-id="18762-114">Bus sukurtos dvi operacijos: viena, skirta apskaitos valiutai, o kita – ataskaitų valiutai, jei naudojama ataskaitų valiuta.</span><span class="sxs-lookup"><span data-stu-id="18762-114">Two transactions might be created, one for the accounting currency and one for the reporting currency, if a reporting currency is relevant.</span></span> <span data-ttu-id="18762-115">Kiekvienas apskaitos įrašas bus užregistruotas negauto pelno arba patirto nuostolio sąskaitose ir pagrindinėje sąskaitoje, kurie atliekamas perkainojimas.</span><span class="sxs-lookup"><span data-stu-id="18762-115">Each accounting entry will be posted to the unrealized gain or loss and the main account that is being revalued.</span></span>

## <a name="prepare-to-run-foreign-currency-revaluation"></a><span data-ttu-id="18762-116">Pasiruošimas paleisti užsienio valiutos kurso pasikeitimą</span><span class="sxs-lookup"><span data-stu-id="18762-116">Prepare to run foreign currency revaluation</span></span>

<span data-ttu-id="18762-117">Prieš vykdant perkainojimo procesą reikalinga tolesnė sąranka.</span><span class="sxs-lookup"><span data-stu-id="18762-117">Before you run the revaluation process, the following setup is required.</span></span>

- <span data-ttu-id="18762-118">Puslapyje **Didžioji knyga** nurodykite valiutos kurso tipą.</span><span class="sxs-lookup"><span data-stu-id="18762-118">On the **Ledger** page, specify the exchange rate type.</span></span> <span data-ttu-id="18762-119">Jei valiutos kurso tipas pagrindinėje sąskaitoje nenurodytas, šis valiutos kurso tipas bus naudojamas atliekant užsienio valiutos kurso keitimą.</span><span class="sxs-lookup"><span data-stu-id="18762-119">If an exchange rate type isn't defined on the main account, this exchange rate type is used during foreign currency revaluation.</span></span>
- <span data-ttu-id="18762-120">Puslapyje **Didžioji knyga** nurodykite valiutos kurso pasikeitimo gauto pelno, patirtų nuostolių, negauto pelno ir nepatirtų nuostolių sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="18762-120">On the **Ledger** page, specify the realized gain, realized loss, unrealized gain, and unrealized loss accounts for currency revaluation.</span></span> <span data-ttu-id="18762-121">Gauto pelno ir patirto nuostolio sąskaitos naudojamos sudengiant gautinų sumų ir mokėtinų sumų operacijas.</span><span class="sxs-lookup"><span data-stu-id="18762-121">Realized gain and realized loss accounts are used when Accounts receivable and Accounts payable transactions are settled.</span></span> <span data-ttu-id="18762-122">Negauto pelno ir nepatirto nuostolio sąskaitos naudojamos norint atlikti atvirų operacijų ir pagrindinių DK sąskaitų perkainojimą.</span><span class="sxs-lookup"><span data-stu-id="18762-122">Unrealized gain and unrealized loss accounts are used to revalue open transactions and general ledger main accounts.</span></span>
- <span data-ttu-id="18762-123">Puslapyje **Valiutos kurso pasikeitimo sąskaitos** kiekvienai valiutai ir įmonei parinkite skirtingą valiutos kurso pasikeitimo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="18762-123">On the **Currency revaluation accounts** page, select different currency revaluation accounts for each currency and company.</span></span> <span data-ttu-id="18762-124">Nenurodžius jokios sąskaitos naudojamos sąskaitos iš puslapio **Didžioji knyga**.</span><span class="sxs-lookup"><span data-stu-id="18762-124">If no accounts are defined, the accounts from the **Ledger** page are used.</span></span>

## <a name="enable-foreign-currency-revaluation"></a><span data-ttu-id="18762-125">Užsienio valiutos kurso pasikeitimo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="18762-125">Enable foreign currency revaluation</span></span>

<span data-ttu-id="18762-126">Užsienio valiutos kurso pasikeitimo funkciją turite įjungti prieš vykdydami užsienio valiutos kurso pasikeitimus.</span><span class="sxs-lookup"><span data-stu-id="18762-126">You must turn on the bank foreign currency revaluation feature before you can process foreign currency revaluations.</span></span>

1. <span data-ttu-id="18762-127">Eikite į **Grynųjų pinigų ir banko valdymas \> Sąranka \> Grynųjų pinigų ir banko valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="18762-127">Go to **Cash and bank management \> Setup \> Cash and bank management parameters**.</span></span>
2. <span data-ttu-id="18762-128">Skirtuke **Bendra**, pateiktame srityje **Užsienio valiutos kurso pasikeitimas**, parinktį **Įgalinti banko perkainojimą** nustatykite į **Taip** ir įjunkite šią funkciją dabartiniam juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="18762-128">On the **General** tab, under **Foreign currency revaluation**, set the **Enable bank revaluation** option to **Yes** to turn on the feature for the current legal entity.</span></span> 
3. <span data-ttu-id="18762-129">Skirtuke **Numeracijos** įtraukite užsienio valiutos kurso pasikeitimo numeraciją.</span><span class="sxs-lookup"><span data-stu-id="18762-129">On the **Number sequences** tab, add a number sequence for foreign currency revaluation.</span></span>
4. <span data-ttu-id="18762-130">Norėdami, kad skiltis **Užsienio valiutos kurso pasikeitimas** būtų rodoma vietos puslapio srityje **Periodinės užduotys**, atnaujinkite naršyklę.</span><span class="sxs-lookup"><span data-stu-id="18762-130">Refresh the browser to see **Foreign currency revaluation** in the **Periodic tasks** section of the area page.</span></span>

<span data-ttu-id="18762-131">Šią funkciją turite įjungti kiekvienam juridiniam subjektui, kuriame bus naudojama užsienio valiutos kurso pasikeitimo funkcija.</span><span class="sxs-lookup"><span data-stu-id="18762-131">You must turn on the feature for every legal entity that will use foreign currency revaluation.</span></span> <span data-ttu-id="18762-132">Jei jums priskirtas sistemos administratoriaus arba funkcijų valdytojo vaidmuo, galite praleisti šį veiksmą, įgalindami funkciją **Įgalinti pakartotinį banko įvertinimą be parametro** darbo srityje **Funckijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="18762-132">If you are assigned to the System Administrator role or Feature Manager role, you can eliminate this step by enabling the feature named **Enable bank revaluation without a parameter** in the **Feature management** workspace.</span></span>

> [!NOTE]
> <span data-ttu-id="18762-133">Jei jūsų juridiname subjekte naudojamas Rusijos, Lenkijos arba Vengrijos šalies / regiono kodas, banko užsienio valiutos kurso pasikeitimo procedūrą jau galite atlikti.</span><span class="sxs-lookup"><span data-stu-id="18762-133">If your legal entity uses a Russian, Polish, or Hungarian country/region code, you can already do bank foreign currency revaluation.</span></span> <span data-ttu-id="18762-134">Užsienio valiutos kurso pasikeitimo funkcijos, kuri naudojama kitose šalyse arba regionuose, naudoti negalėsite.</span><span class="sxs-lookup"><span data-stu-id="18762-134">You won't be able to use the foreign currency revaluation that is used by other countries or regions.</span></span>

## <a name="process-foreign-currency-revaluation"></a><span data-ttu-id="18762-135">Užsienio valiutos kurso pasikeitimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="18762-135">Process foreign currency revaluation</span></span>

<span data-ttu-id="18762-136">Baigę sąranką ir norėdami perkainoti visų juridinių subjektų vienos ar kelių banko sąskaitų balansus, pasinaudokite puslapiu **Užsienio valiutos kurso pasikeitimas**, pateiktu srityje Grynųjų pinigų ir banko paslaugų valdymas.</span><span class="sxs-lookup"><span data-stu-id="18762-136">After the setup is completed, use the **Foreign currency revaluation** page in Cash and bank management to revalue the balances of one or more bank accounts across all legal entities.</span></span> <span data-ttu-id="18762-137">Galite paleisti procesą realiuoju laiku arba suplanuoti, kad jis būtų paleistas naudojant paketą.</span><span class="sxs-lookup"><span data-stu-id="18762-137">You can run the process in real time, or you can schedule it to run by using a batch.</span></span>

<span data-ttu-id="18762-138">Puslapyje **Užsienio valiutos kurso pasikeitimas** pateikiama kiekvieno perkainojimo proceso retrospektyva.</span><span class="sxs-lookup"><span data-stu-id="18762-138">The **Foreign currency revaluation** page shows the history of each revaluation process.</span></span> <span data-ttu-id="18762-139">Jame nurodoma, kada procesas buvo vykdytas bei kokie kriterijai nurodyti, ir pateikiamas saitas į kvitą, sukurtą perkainojimo procesui.</span><span class="sxs-lookup"><span data-stu-id="18762-139">It shows when the process was run and what criteria were defined, and provides a link to the voucher that was created for the revaluation.</span></span> <span data-ttu-id="18762-140">Puslapyje taip pat nurodoma, ar ankstesnis perkainojimas buvo atšauktas.</span><span class="sxs-lookup"><span data-stu-id="18762-140">It also shows whether a previous revaluation was reversed.</span></span> <span data-ttu-id="18762-141">Norėdami vykdyti perkainojimo procesą, pasirinkite parinktį **Užsienio valiutos kurso pasikeitimas**, pateiktą veiksmų srityje, ir atidarykite dialogo langą **Bankas – užsienio valiutos kurso pasikeitimas**.</span><span class="sxs-lookup"><span data-stu-id="18762-141">To run the revaluation process, select **Foreign currency revaluation** on the Action Pane to open the **Bank - foreign currency revaluation** dialog box.</span></span>

<span data-ttu-id="18762-142">Lauke **Perkainojimo data** nurodoma galutinė užsienio valiutos balanso, kuris bus perkainotas, apskaičiavimo data.</span><span class="sxs-lookup"><span data-stu-id="18762-142">The **Revaluation date** field defines the cutoff date for calculating the foreign currency balance that will be revalued.</span></span> <span data-ttu-id="18762-143">Perkainojama visa banko operacijų, įvykdytų iki šios datos, suma.</span><span class="sxs-lookup"><span data-stu-id="18762-143">The sum of all bank transactions that occurred up through this date is revalued.</span></span>

<span data-ttu-id="18762-144">Lauke **Valiutos kurso data** nurodoma valiutos kurso, kuris bus naudojamas valiutos balansams perkainoti, data.</span><span class="sxs-lookup"><span data-stu-id="18762-144">The **Exchange rate date** field defines the date of the exchange rate that will be used to revalue the currency balances.</span></span> <span data-ttu-id="18762-145">Pavyzdžiui, galite perkainoti sausio 31 d. balansus, tačiau taikyti vasario 1 d. nurodytą valiutos kursą.</span><span class="sxs-lookup"><span data-stu-id="18762-145">For example, you can revalue the balances as of January 31 but use the exchange rate that is defined for February 1.</span></span>

<span data-ttu-id="18762-146">Perkainojimo procesą galima taikyti vienam arba daugiau juridinių subjektų.</span><span class="sxs-lookup"><span data-stu-id="18762-146">The revaluation process can be run for one or more legal entities.</span></span> <span data-ttu-id="18762-147">Peržiūroje rodomi tik tie juridiniai subjektai, prie kurių turite prieigą.</span><span class="sxs-lookup"><span data-stu-id="18762-147">The lookup shows only the legal entities that you have access to.</span></span> <span data-ttu-id="18762-148">Pasirinkite juridinius subjektus, kuriems norite parinkti užsienio valiutos kurso pasikeitimo procesui tinkamas banko sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="18762-148">Select the legal entities for which you want to select the bank accounts that are eligible for foreign currency revaluation.</span></span> <span data-ttu-id="18762-149">Visos šių juridinių subjektų banko sąskaitos bus rodomos tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="18762-149">All the bank accounts for those legal entities will be shown in the grid.</span></span>

<span data-ttu-id="18762-150">Jei perkainojimo rezultatus norite peržiūrėti prieš juos registruodami, parinktį **Peržiūrėti prieš registruojant** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="18762-150">Set the **Preview before posting** option to **Yes** if you want to review the results of the revaluation before you post it.</span></span> <span data-ttu-id="18762-151">Užsienio valiutos kurso pasikeitimo procedūrai būdinga peržiūra, kurią galima registruoti.</span><span class="sxs-lookup"><span data-stu-id="18762-151">The foreign currency revaluation has a preview that can be posted.</span></span> <span data-ttu-id="18762-152">Dar kartą vykdyti perkainojimo proceso nereikia.</span><span class="sxs-lookup"><span data-stu-id="18762-152">You don't have to run the revaluation process again.</span></span> <span data-ttu-id="18762-153">Peržiūros lange pateiktus rezultatus galite eksportuoti į „Microsoft Excel“ ir tokiu būdu kaupti sumų skaičiavimo retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="18762-153">You can export the results in the preview to Microsoft Excel to keep a history of how the amounts were calculated.</span></span> <span data-ttu-id="18762-154">Jei norite peržiūrėti perkainojimo rezultatus, naudoti paketinio vykdymo negalėsite.</span><span class="sxs-lookup"><span data-stu-id="18762-154">You can't use batch processing if you want to preview the results of the revaluation.</span></span>

<span data-ttu-id="18762-155">Pasirinkite **Gerai** ir vykdykite užsienio valiutos kurso pasikeitimą.</span><span class="sxs-lookup"><span data-stu-id="18762-155">Select **OK** to process the foreign currency revaluation.</span></span> <span data-ttu-id="18762-156">Bus sukurtas įrašas, kad galėtumėte sekti kiekvieno vykdymo retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="18762-156">A record is created to track the history of each run.</span></span> <span data-ttu-id="18762-157">Sukuriamas atskiras kiekvieno juridinio subjekto ir registravimo sluoksnio įrašas.</span><span class="sxs-lookup"><span data-stu-id="18762-157">A separate record is created for each legal entity and posting layer.</span></span>

## <a name="calculate-unrealized-gainloss"></a><span data-ttu-id="18762-158">Negauto pelno / nuostolio skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="18762-158">Calculate unrealized gain/loss</span></span>

<span data-ttu-id="18762-159">Srityje Grynųjų pinigų ir banko valdymas bazome valiuta laikoma banko valiuta, todėl ji nėra perkainojama.</span><span class="sxs-lookup"><span data-stu-id="18762-159">In Cash and bank management, the bank currency is considered to be the base currency and it is not revalued.</span></span> <span data-ttu-id="18762-160">Banko sąskaitos balansas apskaitos valiutos srityje perkainojamas naudojant valiutos kursus tarp banko valiutos ir apskaitos valiutos lauke **Valiutos kurso data**.</span><span class="sxs-lookup"><span data-stu-id="18762-160">The balance of the bank account in the accounting currency is revalued using the exchange rates between the bank currency and the accounting currency on the **Exchange rate date**.</span></span> <span data-ttu-id="18762-161">Banko sąskaitos balansas ataskaitų valiutos srityje taip pat perkainojamas naudojant valiutos kursus tarp banko valiutos ir ataskaitų valiutos lauke **Valiutos kurso data**.</span><span class="sxs-lookup"><span data-stu-id="18762-161">The balance of the bank account in the reporting currency is also revalued using the exchange rates between the bank currency and the reporting currency on the **Exchange rate date**.</span></span>

<span data-ttu-id="18762-162">Skirtumui tarp banko sąskaitos balanso ir naujo balanso, apskaičiuoto apskaitos valiuta, apskaičiuoti sukuriama operacija.</span><span class="sxs-lookup"><span data-stu-id="18762-162">A transaction is created for the difference between the balance of the bank account and the new balance that is calculated for the accounting currency.</span></span> <span data-ttu-id="18762-163">Skirtumui tarp banko sąskaitos balanso ir naujo balanso, apskaičiuoto ataskaitų valiuta, apskaičiuoti sukuriama dar viena operacija.</span><span class="sxs-lookup"><span data-stu-id="18762-163">Another transaction is created for the difference between the balance of the bank account and the new balance that is calculated for the reporting currency.</span></span> <span data-ttu-id="18762-164">Šių operacijų įrašai pažymimi kaip suderinti.</span><span class="sxs-lookup"><span data-stu-id="18762-164">The entries for these transactions are marked as reconciled.</span></span> 

<span data-ttu-id="18762-165">Jei banko valiuta atitinka apskaitos valiutą, apskaitos valiutos įrašas nesukuriamas.</span><span class="sxs-lookup"><span data-stu-id="18762-165">No entry is made for the accounting currency if the bank currency matches the accounting currency.</span></span> <span data-ttu-id="18762-166">Jei banko valiuta atitinka ataskaitų valiutą, ataskaitų valiutos įrašas taip pat nesukuriamas.</span><span class="sxs-lookup"><span data-stu-id="18762-166">Likewise, no entry is made for the reporting currency if the bank currency matches the reporting currency.</span></span>

<span data-ttu-id="18762-167">Be to, užsienio valiutos kurso pasikeitimo operacija išskaidoma po dimensijas, sutinkamas atliekant banko operacijas.</span><span class="sxs-lookup"><span data-stu-id="18762-167">The foreign currency revaluation transaction is also split across the dimensions that are found on the bank transactions.</span></span> <span data-ttu-id="18762-168">Išskaidymas pagrįstas kiekvienos dimensijos balansu.</span><span class="sxs-lookup"><span data-stu-id="18762-168">The split is based on the balance for each dimension.</span></span> <span data-ttu-id="18762-169">Pvz., bendras banko balansas yra 10 000, tačiau 001 verslo struktūros vieneto balansas yra 4 000, o 002 verslo struktūros vieneto balansas – 6 000.</span><span class="sxs-lookup"><span data-stu-id="18762-169">For example, the total bank balance is 10,000, but the balance for business unit 001 is 4,000, whereas the balance for business unit 002 is 6,000.</span></span> <span data-ttu-id="18762-170">Šiuo atveju 40 procentų perkainojimo sumos registruojama 001 verslo struktūros vieneto perkainojimo sąskaitoje, o 60 procentų – 002 verslo struktūros vieneto perkainojimo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="18762-170">In this case, 40 percent of the revaluation amount is posted to the revaluation account that has business unit 001, and 60 percent is posted to the revaluation account that has business unit 002.</span></span> <span data-ttu-id="18762-171">Jei sąskaitos struktūroje verslo struktūros vienetas neįtrauktas, visa suma registruojama perkainojimo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="18762-171">If the account structure doesn't include a business unit, the full amount is posted to the revaluation account.</span></span>

## <a name="reverse-foreign-currency-revaluation"></a><span data-ttu-id="18762-172">Atšaukti užsienio valiutos kurso pasikeitimą</span><span class="sxs-lookup"><span data-stu-id="18762-172">Reverse foreign currency revaluation</span></span>

<span data-ttu-id="18762-173">Jei perkainojimo operaciją reikia atšaukti, pasirinkite puslapio **Užsienio valiutos kurso pasikeitimas** veiksmų srityje pateiktą mygtuką **Atšaukti operaciją**.</span><span class="sxs-lookup"><span data-stu-id="18762-173">If you must reverse the revaluation transaction, select **Reverse transaction** on the Action Pane of the **Foreign currency revaluation** page.</span></span> <span data-ttu-id="18762-174">Sukuriamas naujas užsienio valiutos kurso pasikeitimo retrospektyvos įrašas, skirtas audito retrospektyvai tvarkyti ir naudojamas norint sekti, kada perkainojimas buvo vykdytas arba atšauktas.</span><span class="sxs-lookup"><span data-stu-id="18762-174">A new foreign currency revaluation historical record is created to maintain the historical audit trail of when the revaluation occurred or was reversed.</span></span>

<span data-ttu-id="18762-175">Norėdami atšaukti kelis perkainojimus, pirmiausia turite atšaukti naujausią perkainojimą.</span><span class="sxs-lookup"><span data-stu-id="18762-175">To reverse several revaluations, you must reverse the most current revaluation first.</span></span> <span data-ttu-id="18762-176">Tada datų tvarka toliau atšaukite senesnius perkainojimus.</span><span class="sxs-lookup"><span data-stu-id="18762-176">Then continue to reverse older revaluations in date order.</span></span> <span data-ttu-id="18762-177">Tai atlikę galite vykdyti naujus perkainojimus, susijusius su laikotarpiais, kada atliktus perkainojimus atšaukėte.</span><span class="sxs-lookup"><span data-stu-id="18762-177">You can then process new revaluations for the periods that you reversed.</span></span>