---
title: "„Retail“ smulkių išlaidų valdymas (Rytų Europa)"
description: "Šioje temoje aprašoma, kaip nustatyti ir naudoti „Retail“ grynųjų pinigų valdymo funkcijas Rytų Europoje."
author: epopov
manager: annbe
ms.date: 10/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 01239f0eff3e59f62188fca64f99e93be843d2e2
ms.openlocfilehash: c198cedba9268229dc1057711d9f16ca33acebac
ms.contentlocale: lt-lt
ms.lasthandoff: 10/24/2018

---

# <a name="petty-cash-management-for-retail-for-eastern-europe"></a><span data-ttu-id="b538b-103">„Retail“ smulkių išlaidų valdymas (Rytų Europa)</span><span class="sxs-lookup"><span data-stu-id="b538b-103">Petty cash management for Retail for Eastern Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b538b-104">Šiame straipsnyje pateikiama informacijos apie Rytų Europos „Retail“ verslo lokalizavimą.</span><span class="sxs-lookup"><span data-stu-id="b538b-104">This article contains information about Eastern European localization specific for the Retail industry.</span></span> 

<span data-ttu-id="b538b-105">Pagal Rytų Europos apskaitos reikalavimus, galite nustatyti grynųjų pinigų sąskaitų operacijas ir automatizuoti gavimų, grynųjų pinigų dokumentų ir grynųjų pinigų ataskaitų procesus.</span><span class="sxs-lookup"><span data-stu-id="b538b-105">In accordance with the Eastern Europe accounting requirements, you can set up operations for cash accounts to automate the processes for receipts, cash documents and cash reports.</span></span> <span data-ttu-id="b538b-106">Daugiau informacijos ieškokite [(EEUR) Nustatyti grynųjų pinigų valdymo parametrus](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).</span><span class="sxs-lookup"><span data-stu-id="b538b-106">For more information, go to [(EEUR) Set up parameters for cash management](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).</span></span> 

<span data-ttu-id="b538b-107">Mažmenininkai gali priimti įvairių tipų mokėjimą mainais už produktus ir paslaugas, kurias jie parduoda.</span><span class="sxs-lookup"><span data-stu-id="b538b-107">Retailers can accept various types of payment in exchange for the products and services that they sell.</span></span> <span data-ttu-id="b538b-108">Nors dažniausia mokėjimo forma yra grynieji pinigai, mažmenininkai taip pat gali priimti mokėjimą čekiais, kortelėmis ar kvitais.</span><span class="sxs-lookup"><span data-stu-id="b538b-108">Although cash is the most common form of payment, retailers can also receive payment in the form of checks, cards, or vouchers.</span></span> <span data-ttu-id="b538b-109">„Retail“ elektroniniame kasos aparate (EKA) grynieji pinigai, kredito kortelių kvitai ir kiti mokėjimai apdorojami naudojant kasos aparatą.</span><span class="sxs-lookup"><span data-stu-id="b538b-109">In Retail point of sale (POS), cash, credit card receipts, and other payments are processed through a cash office.</span></span>

<span data-ttu-id="b538b-110">Naudodami „Retail“ grynųjų pinigų valdymą galite atlikti toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b538b-110">You can do the following by using Cash management in Retail:</span></span>

- <span data-ttu-id="b538b-111">Sukurti pasirinkto mokėjimo būdo grynųjų pinigų sąskaitą kiekvienai mažmeninės prekybos parduotuvei.</span><span class="sxs-lookup"><span data-stu-id="b538b-111">Create a cash account for the selected payment method for each retail store.</span></span>
- <span data-ttu-id="b538b-112">Naudoti grynųjų pinigų žurnalus grynųjų pinigų operacijoms ir klientų mokėjimams, gautiems mažmeninės prekybos EKA, registruoti.</span><span class="sxs-lookup"><span data-stu-id="b538b-112">Use cash journals to post cash transactions and customer payments that are received at a retail POS.</span></span>
- <span data-ttu-id="b538b-113">Sujungti išrašo eilutės operacijas registruojant mažmeninės prekybos išrašą.</span><span class="sxs-lookup"><span data-stu-id="b538b-113">Aggregate transactions in a statement line when you post a retail statement.</span></span> <span data-ttu-id="b538b-114">Galite sujungti pinigų įnešimą į kasą, inkasavimą, kvitų operacijas, mokėjimo priemonės išėmimo operacijas, pinigų srauto įrašo operacijas, pajamų operacijas, išlaidų operacijas, klientų mokėjimus, pardavimo operacijas ir grąžinimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="b538b-114">You can aggregate safe drops, bank drops, voucher transactions, remove tender transactions, float entry transactions, income transactions, expense transactions, customer payments, sales transactions, and return transactions.</span></span>

<span data-ttu-id="b538b-115">Visos „Retail“ EKA vykstančios operacijos užregistruojamos naudojant didžiosios knygos žurnalą.</span><span class="sxs-lookup"><span data-stu-id="b538b-115">All transactions that take place in Retail POS are posted using a ledger journal.</span></span> <span data-ttu-id="b538b-116">Norėdami kurti ir registruoti išrašus, galite naudoti grynųjų pinigų mokėjimo žurnalus, klientų mokėjimo žurnalus ir pagrindinius žurnalus.</span><span class="sxs-lookup"><span data-stu-id="b538b-116">You can use cash payment journals, customer payment journals, and general journals to create and post the statements.</span></span> <span data-ttu-id="b538b-117">Norėdami gauti daugiau informacijos, eikite į [Mažmeninės prekybos parduotuvės išrašų kūrimas, skaičiavimas ir registravimas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).</span><span class="sxs-lookup"><span data-stu-id="b538b-117">For more information, go to [Create, calculate, and post statements for a retail store](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).</span></span>

<span data-ttu-id="b538b-118">Veiksmų srities puslapyje **Užregistruoti išrašai** galite atlikti toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b538b-118">On the **Posted statements** page, on the Action Pane, you can do the following:</span></span>
  - <span data-ttu-id="b538b-119">Eikite į **Užklausos > Mokėjimų grynaisiais pinigais žurnalas** ir prisijunkite prie su išrašu susietų mokėjimų grynaisiais pinigais žurnalų.</span><span class="sxs-lookup"><span data-stu-id="b538b-119">Go to **Inquiries > Cash payment journal** to access the cash payment journals that are related to the statement.</span></span>
  - <span data-ttu-id="b538b-120">Eikite į **Užklausos > Pagrindinis žurnalas** ir prisijunkite prie su išrašu susijusių didžiosios knygos žurnalų (išskyrus klientų mokėjimų ir mokėjimų grynaisiais pinigais).</span><span class="sxs-lookup"><span data-stu-id="b538b-120">Go to **Inquiries > General journal** to access the ledger journals that are related to the statement, other than customer payments and cash payments.</span></span>

## <a name="set-up-for-cash-management-for-retail-pos"></a><span data-ttu-id="b538b-121">„Retail POS“ grynųjų pinigų valdymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="b538b-121">Set up for cash management for Retail POS</span></span>

<span data-ttu-id="b538b-122">Prieš naudodami grynųjų pinigų valdymą mažmeninėje prekyboje, privalote baigti tolesnę nustatymo procedūrą:</span><span class="sxs-lookup"><span data-stu-id="b538b-122">You must complete the following setup procedure before you use cash management in Retail:</span></span>
- <span data-ttu-id="b538b-123">Puslapyje **Mokėjimo būdai** nustatyti kiekvienam mokėjimo tipui skirtą mokėjimo būdą, su kuriuo sutinka pardavėjas.</span><span class="sxs-lookup"><span data-stu-id="b538b-123">Set up a payment method for each payment type that the retailer accepts on the **Payment methods** page.</span></span> <span data-ttu-id="b538b-124">Galite naudoti skirtingus „Retail POS“ registravimo operacijų mokėjimo būdus.</span><span class="sxs-lookup"><span data-stu-id="b538b-124">You can use different payment methods for posting transactions in Retail POS.</span></span> <span data-ttu-id="b538b-125">Daugiau informacijos apie „Retail“ mokėjimo būdus ieškokite [Mokėjimo būdai](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/payment-methods).</span><span class="sxs-lookup"><span data-stu-id="b538b-125">For more information about payment methods in Retail, see [Payment methods](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/payment-methods).</span></span>

- <span data-ttu-id="b538b-126">Nustatyti grynųjų pinigų operacijų mažmeninės prekybos parametrus.</span><span class="sxs-lookup"><span data-stu-id="b538b-126">Set up retail parameters for cash operations.</span></span>

- <span data-ttu-id="b538b-127">Nustatyti mokėjimų grynaisiais pinigais mažmeninės prekybos parduotuvėje mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="b538b-127">Set up a payment method for cash payments in a retail store.</span></span>

### <a name="set-up-retail-parameters-for-cash-operations"></a><span data-ttu-id="b538b-128">Grynųjų pinigų operacijų mažmeninės prekybos parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="b538b-128">Set up retail parameters for cash operations</span></span>

<span data-ttu-id="b538b-129">Galite nustatyti parametrus, kad galėtumėte kurti ir registruoti mažmeninės prekybos grynųjų pinigų operacijas.</span><span class="sxs-lookup"><span data-stu-id="b538b-129">You can set up parameters to create and post cash transactions in Retail.</span></span> <span data-ttu-id="b538b-130">Pardavimo ir mokėjimo operacijoms registruoti „Retail POS“ galite naudoti mokėjimų grynaisiais pinigais žurnalus, kliento mokėjimų žurnalus arba bendruosius žurnalus.</span><span class="sxs-lookup"><span data-stu-id="b538b-130">You can use cash payment journals, customer payment journals, or general journals to post sales transactions and payment transactions in the Retail POS.</span></span> <span data-ttu-id="b538b-131">Registruodami išrašą galite sujungti operacijas, kurių ypatybės tokios pačios.</span><span class="sxs-lookup"><span data-stu-id="b538b-131">You can aggregate transactions that have the same properties when you post a statement.</span></span> 

1. <span data-ttu-id="b538b-132">Eikite į **Mažmeninė prekyba > Būstinės sąranka > Parametrai > Mažmeninės prekybos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b538b-132">Go to **Retail > Headquarters setup > Parameters > Retail parameters**.</span></span> <span data-ttu-id="b538b-133">Kairiojoje srityje spustelėkite **Registravimas**</span><span class="sxs-lookup"><span data-stu-id="b538b-133">In the left pane, click **Posting**</span></span>

2. <span data-ttu-id="b538b-134">„FastTab“ skirtuko **Telkimas** srityje **Registravimas** nustatykite **Mokėjimo priemonės šalinimas / pinigų srautas** parinktį **Taip**, jei norite sujungti mokėjimo priemonės išėmimo operacijas arba pinigų srauto įrašo operacijas, susietas su išrašo eilute, kai registruojate išrašą.</span><span class="sxs-lookup"><span data-stu-id="b538b-134">In the **Posting** area, on the **Aggregation** FastTab, set **Tender remove/float** to **Yes** to aggregate the remove tender transactions or float entry transactions that are associated with a statement line when you post the statement.</span></span> <span data-ttu-id="b538b-135">Mokėjimo priemonės šalinimo operacija sukuriama, kai išimate grynuosius pinigus iš EKA kasos stalčiaus.</span><span class="sxs-lookup"><span data-stu-id="b538b-135">A remove tender transaction is created when you withdraw cash from the POS cash drawer.</span></span> <span data-ttu-id="b538b-136">Pinigų srauto įrašo operacija sukuriama, kai įdedate grynuosius pinigus į EKA kasos stalčių.</span><span class="sxs-lookup"><span data-stu-id="b538b-136">A float entry transaction is created when you deposit cash in the POS cash drawer.</span></span>

3. <span data-ttu-id="b538b-137">Kai registruojate išrašą, suaktyvinkite toliau nurodytus atskirus parametrus, jei norite sujungti operacijas, kurios susietos su išrašo eilute.</span><span class="sxs-lookup"><span data-stu-id="b538b-137">Activate the individual parameters listed below to aggregate the transactions that are associated with a statement line when you post the statement:</span></span>
   - <span data-ttu-id="b538b-138">**Inkasavimas** – sujunkite banko operacijas.</span><span class="sxs-lookup"><span data-stu-id="b538b-138">**Bank drop** – Aggregate bank transactions.</span></span>
   - <span data-ttu-id="b538b-139">**Pinigų įnešimas į kasą** – sujunkite kasos operacijas.</span><span class="sxs-lookup"><span data-stu-id="b538b-139">**Safe drop** – Aggregate safe transactions.</span></span>
   - <span data-ttu-id="b538b-140">**Pajamų / išlaidų operacijos** – sujunkite pajamų arba išladų operacijas.</span><span class="sxs-lookup"><span data-stu-id="b538b-140">**Income/Expense transactions** – Aggregate income transactions or expense transactions.</span></span>
   - <span data-ttu-id="b538b-141">**Kvito operacijos** – sujunkite kvito operacijas.</span><span class="sxs-lookup"><span data-stu-id="b538b-141">**Voucher transactions** – Aggregate voucher transactions.</span></span>
   - <span data-ttu-id="b538b-142">**Kliento mokėjimai** – sujunkite kliento mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="b538b-142">**Customer payments** – Aggregate customer payments.</span></span>
   - <span data-ttu-id="b538b-143">**Pardavimas ir grąžinimai** – sujunkite pardavimo ir grąžinimų operacijas.</span><span class="sxs-lookup"><span data-stu-id="b538b-143">**Sales and returns** – Aggregate sales and returns transactions.</span></span>

4. <span data-ttu-id="b538b-144">„FastTab“ skirtuke **Mokėjimai** pasirinkite numatytąjį žurnalo pavadinimą. Galimos šios pasirinktys:</span><span class="sxs-lookup"><span data-stu-id="b538b-144">On the **Payments** FastTab, select a default journal name for the following options:</span></span>
     - <span data-ttu-id="b538b-145">**Kliento mokėjimų žurnalas** – šis žurnalas naudojamas kliento mokėjimams registruoti.</span><span class="sxs-lookup"><span data-stu-id="b538b-145">**Customer payment journal** – This journal is used to post customer payments.</span></span>
     - <span data-ttu-id="b538b-146">**Mokėjimų grynaisiais pinigais žurnalas** – šis žurnalas naudojamas mokėjimams grynaisiais pinigais registruoti.</span><span class="sxs-lookup"><span data-stu-id="b538b-146">**Cash payment journal** – This journal is used to post cash payments.</span></span>
     - <span data-ttu-id="b538b-147">**Pagrindinis žurnalas** – šis žurnalas naudojamas norint registruoti kitas operacijas (ne mokėjimų grynaisiais pinigais ir ne kliento mokėjimų operacijas).</span><span class="sxs-lookup"><span data-stu-id="b538b-147">**General journal** – This journal is used to post transactions other than cash payments and customer payments.</span></span>

### <a name="set-up-a-payment-method-for-cash-payments-in-a-retail-store"></a><span data-ttu-id="b538b-148">Mokėjimų grynaisiais pinigais mažmeninės prekybos parduotuvėje mokėjimo būdo nustatymas</span><span class="sxs-lookup"><span data-stu-id="b538b-148">Set up a payment method for cash payments in a retail store</span></span>

<span data-ttu-id="b538b-149">Naudokite šią procedūrą norėdami nustatyti mokėjimų grynaisiais pinigais mažmeninės prekybos parduotuvėje mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="b538b-149">Use the following procedure to set up a payment method for cash payments in a retail store.</span></span>

1. <span data-ttu-id="b538b-150">Eikite į **Mažmeninė prekyba > Kanalai > Mažmeninės prekybos parduotuvės > Visos mažmeninės prekybos parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="b538b-150">Go to **Retail > Channels > Retail stores > All retail stores**.</span></span>

2. <span data-ttu-id="b538b-151">Sąrašo puslapyje **Visos mažmeninės prekybos parduotuvės** pasirinkite parduotuvę, kuriai norite nustatyti mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="b538b-151">On the **All retail stores** list page, select the store to set up a payment method for.</span></span>

3. <span data-ttu-id="b538b-152">Veiksmų srityje, skirtuke **Nustatymas**, grupėje **Nustatymas** spustelėkite **Mokėjimo būdai**.</span><span class="sxs-lookup"><span data-stu-id="b538b-152">On the Action Pane, on the **Set up** tab, in the **Set up** group, click **Payment methods**.</span></span>

4. <span data-ttu-id="b538b-153">Puslapyje **Mokėjimo būdas** sukurkite arba pasirinkite mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="b538b-153">On the **Payment method** page, create or select a payment method.</span></span> 

5. <span data-ttu-id="b538b-154">„FastTab“ skirtuke **Registravimas**, lauko grupėje **Sąskaita**, lauke **Sąskaitos tipas** pasirinkite **Grynųjų pinigų sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="b538b-154">On the **Posting** FastTab, in the **Account** field group, in the **Account type** field, select **Cash account**.</span></span>

   > [!NOTE]
    > <span data-ttu-id="b538b-155">Parinktis **Grynųjų pinigų sąskaita** lauke **Sąskaitos tipas** galima tik lauke **Funkcija** pasirinkus **Įprasta** arba **Mokėjimo priemonės šalinimas / pinigų srautas**.</span><span class="sxs-lookup"><span data-stu-id="b538b-155">You can select **Cash account** in the **Account type** field only if you select **Normal** or **Tender remove/float** in the **Function** field.</span></span>

6. <span data-ttu-id="b538b-156">Lauke **Sąskaitos numeris** pasirinkite mokėjimo būdo grynųjų pinigų sąskaitos numerį.</span><span class="sxs-lookup"><span data-stu-id="b538b-156">In the **Account number** field, select a cash account number for the payment method.</span></span>

7. <span data-ttu-id="b538b-157">Laukų grupės **Mokėjimo priemonės šalinimas / pinigų srautas** lauke **Korespondentinė sąskaita** pasirinkite korespondentinę sąskaitą, kurioje bus registruojamos mokėjimo būdo mokėjimo priemonės šalinimo arba pinigų srauto įrašo operacijos.</span><span class="sxs-lookup"><span data-stu-id="b538b-157">In the **Tender remove/float** field group, in the **Offset account** field, select the offset account to post remove tender or float entry transactions for the payment method.</span></span>

> [!NOTE]
> <span data-ttu-id="b538b-158">Parduotuvėje būtina nustatyti ir mokėjimo grynaisiais pinigais priemonės, ir mokėjimo priemonės šalinimo arba pinigų srauto įrašo mokėjimo būdo korespondentines sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="b538b-158">You must set up offset accounts for both the cash tender payment method and the remove tender or float entry payment method for a store.</span></span> <span data-ttu-id="b538b-159">Tokiu būdu sukuriami subalansuoti mokėjimo priemonės šalinimo arba pinigų srauto operacijų DK įrašai.</span><span class="sxs-lookup"><span data-stu-id="b538b-159">This creates balanced general ledger entries for remove tender or float entry transactions.</span></span>

