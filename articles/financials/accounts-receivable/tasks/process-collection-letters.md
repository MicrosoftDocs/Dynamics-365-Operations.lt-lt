--- 
title: "Apdoroti priminimo laiškus"
description: "Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti priminimo laiškus."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.translationtype: HT
ms.sourcegitcommit: 18eaadf417ce6d0aacf0b13b3e4f857e06031e66
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.contentlocale: lt-lt
ms.lasthandoff: 01/22/2019

---
# <a name="process-collection-letters"></a><span data-ttu-id="b792b-103">Apdoroti priminimo laiškus</span><span class="sxs-lookup"><span data-stu-id="b792b-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b792b-104">Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti priminimo laiškus.</span><span class="sxs-lookup"><span data-stu-id="b792b-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="b792b-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="b792b-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="b792b-106">Registravimo šablone nustatykite priminimo laiškų seką.</span><span class="sxs-lookup"><span data-stu-id="b792b-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="b792b-107">Pasirinkite **Kreditas ir mokėjimų priežiūra > Sąranka > Klientų registravimo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="b792b-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="b792b-108">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="b792b-108">Click **Edit**.</span></span>
3. <span data-ttu-id="b792b-109">Išplečiamajame sąraše pasirinkite priminimo laiškų seką.</span><span class="sxs-lookup"><span data-stu-id="b792b-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="b792b-110">Jei nenorite generuoti operacijų priminimo laiškų naudodami šį registravimo šabloną, palikite lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="b792b-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="b792b-111">Išplėskite lentelių apribojimų skirtuką, kad pakeistumėte būdą, kuriuo apdorojami priminimo laiškai.</span><span class="sxs-lookup"><span data-stu-id="b792b-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="b792b-112">Jei šio lauko reikšmė nustatyta kaip **Taip**, bus kuriami šio registravimo šablono priminimo laiškai.</span><span class="sxs-lookup"><span data-stu-id="b792b-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="b792b-113">Kurti priminimo laiškus</span><span class="sxs-lookup"><span data-stu-id="b792b-113">Create collection letters</span></span>
1. <span data-ttu-id="b792b-114">Pasirinkite **Kreditas ir mokėjimų priežiūra > Priminimo laiškas > Kurti priminimo laiškus**.</span><span class="sxs-lookup"><span data-stu-id="b792b-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="b792b-115">Pasirinkite operacijų, kurių laiškus rinksite, tipus.</span><span class="sxs-lookup"><span data-stu-id="b792b-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="b792b-116">Skaičiuojant bus įtrauktos visos atidarytos šių tipų operacijos.</span><span class="sxs-lookup"><span data-stu-id="b792b-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="b792b-117">Lauke **Priminimo laiškas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b792b-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="b792b-118">Įveskite priminimo laiško datą.</span><span class="sxs-lookup"><span data-stu-id="b792b-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="b792b-119">Pasirinkite registravimo šabloną, jei **Naudoti registravimo šabloną iš** pakeitėte į **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="b792b-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="b792b-120">Yra dvi registravimo profilio parinktys:</span><span class="sxs-lookup"><span data-stu-id="b792b-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="b792b-121">**Sąskaita** – naudokite registravimo šabloną, priskirtą kliento sąskaitai, kiekvienai delspinigių pažymai.</span><span class="sxs-lookup"><span data-stu-id="b792b-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="b792b-122">**Pasirinkti** – naudokite registravimo šabloną, kurį pasirenkate lauke **Registravimo šablonas**.</span><span class="sxs-lookup"><span data-stu-id="b792b-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="b792b-123">Išplėskite dalį **Įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="b792b-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="b792b-124">Spustelėkite **Filtras**.</span><span class="sxs-lookup"><span data-stu-id="b792b-124">Click **Filter**.</span></span>
7. <span data-ttu-id="b792b-125">Lauke **Kriterijai** įveskite Kliento ID.</span><span class="sxs-lookup"><span data-stu-id="b792b-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="b792b-126">Pvz., įveskite „US-001‟.</span><span class="sxs-lookup"><span data-stu-id="b792b-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="b792b-127">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b792b-127">Click **OK**.</span></span>
9. <span data-ttu-id="b792b-128">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b792b-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="b792b-129">Priminimo laiškų spausdinimas</span><span class="sxs-lookup"><span data-stu-id="b792b-129">Print collection letters</span></span>
1. <span data-ttu-id="b792b-130">Pasirinkite **Kreditas ir mokėjimų priežiūra > Priminimo laiškas > Peržiūrėti ir apdoroti priminimo laiškus**.</span><span class="sxs-lookup"><span data-stu-id="b792b-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="b792b-131">Lauke **Būsena** pasirinkite **Sukurta**.</span><span class="sxs-lookup"><span data-stu-id="b792b-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="b792b-132">Lauke **Išspausdinta** pasirinkite **Neišspausdinta**.</span><span class="sxs-lookup"><span data-stu-id="b792b-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="b792b-133">Spustelėkite **Spausdinti**.</span><span class="sxs-lookup"><span data-stu-id="b792b-133">Click **Print**.</span></span>
5. <span data-ttu-id="b792b-134">Spustelėkite **Priminimo laiško pastaba**.</span><span class="sxs-lookup"><span data-stu-id="b792b-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="b792b-135">Išplėskite dalį **Įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="b792b-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="b792b-136">Įveskite registravimų galutinę datą.</span><span class="sxs-lookup"><span data-stu-id="b792b-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="b792b-137">Spustelėkite **Gerai**, jei norite spausdinti priminimo laišką.</span><span class="sxs-lookup"><span data-stu-id="b792b-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="b792b-138">Priminimo laiško registravimas.</span><span class="sxs-lookup"><span data-stu-id="b792b-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="b792b-139">Spustelėkite **Registruoti.**</span><span class="sxs-lookup"><span data-stu-id="b792b-139">Click **Post**.</span></span>
   2. <span data-ttu-id="b792b-140">Įveskite priminimo laiško registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="b792b-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="b792b-141">Išplėskite dalį **Įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="b792b-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="b792b-142">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b792b-142">Click **OK**.</span></span>
   5. <span data-ttu-id="b792b-143">Lauke **Būsena** pasirinkite **Užregistruota**.</span><span class="sxs-lookup"><span data-stu-id="b792b-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="b792b-144">Lauke **Išspausdinta** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b792b-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="b792b-145">Valdykite priminimo laiškus kliento lygiu</span><span class="sxs-lookup"><span data-stu-id="b792b-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="b792b-146">Taip pat galite nustatyti priminimo laiškus kliento lygiu, kad būtų sekamas kiekvienos operacijos priminimo laiško kodas, tačiau priminimo laiško apdorojimas bus grindžiamas vieno priminimo laiško lygiu, kuris saugomas klientui.</span><span class="sxs-lookup"><span data-stu-id="b792b-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="b792b-147">Viename priminimo laiške bus visos pradelstos kliento operacijos.</span><span class="sxs-lookup"><span data-stu-id="b792b-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="b792b-148">Nors atidėjimo dienos dabar sekamos kliento lygiu, kitas priminimo laiškas nebus išsiųstas, kol nepraeis kito sekoje esančio priminimo laiško atidėjimo dienų skaičius net jei po paskutinio išsiųsto priminimo laiško operacijos taps pradelstos.</span><span class="sxs-lookup"><span data-stu-id="b792b-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="b792b-149">Ši parinktis sumažina priminimo laiškų, kuriuos siųsite vienam klientui, skaičių.</span><span class="sxs-lookup"><span data-stu-id="b792b-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="b792b-150">Nustatykite klientą, kad galėtumėte valdyti priminimo laiškus kliento lygiu</span><span class="sxs-lookup"><span data-stu-id="b792b-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="b792b-151">Pasirinkite **Kreditas ir mokėjimų priežiūra > Sąranka > Gautinų sumų parametrai** ir spustelėkite skirtuką **Mokėjimų priežiūra**.</span><span class="sxs-lookup"><span data-stu-id="b792b-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="b792b-152">Pakeiskite parametro **Priminimo laiško kūrimas** vertę į **Klientas**.</span><span class="sxs-lookup"><span data-stu-id="b792b-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="b792b-153">Pasirinkite **Kreditas ir mokėjimų priežiūra > Priminimo laiškas > Peržiūrėti ir apdoroti priminimo laiškus**.</span><span class="sxs-lookup"><span data-stu-id="b792b-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="b792b-154">Klientui bus sugeneruotas tik vienas priminimo laiškas su visomis pradelstomis operacijomis.</span><span class="sxs-lookup"><span data-stu-id="b792b-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="b792b-155">Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą</span><span class="sxs-lookup"><span data-stu-id="b792b-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="b792b-156">Jei į operacijas įtraukiami mokėjimai ir kredito pažymos, kurios bus įtrauktos į priminimo laiškus, gali būti mokėjimų arba kredito pažymų, kurios suaktyvins priminimo laišką.</span><span class="sxs-lookup"><span data-stu-id="b792b-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="b792b-157">Galite kontroliuoti, kaip mokėjimai ir kredito pažymos valdo priminimo laiško kodą, keisdami parametro **Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą** vertę.</span><span class="sxs-lookup"><span data-stu-id="b792b-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="b792b-158">Norėdami nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b792b-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="b792b-159">Pasirinkite **Kreditas ir mokėjimų priežiūra > Sąranka > Gautinų sumų parametrai** ir spustelėkite skirtuką **Mokėjimų priežiūra**.</span><span class="sxs-lookup"><span data-stu-id="b792b-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="b792b-160">Pakeiskite parametro **Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą** vertę į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b792b-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>

