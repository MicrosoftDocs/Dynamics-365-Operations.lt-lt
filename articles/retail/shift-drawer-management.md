---
title: "Pamainos ir kasos stalčių valdymas"
description: "Šiame straipsnyje paaiškinta, kaip nustatyti ir naudoti dviejų tipų mažmeninės prekybos elektroninio kasos aparato (EKA) pamainas – bendrai naudojamą ir atskirą. Bendrai naudojimas pamainas keliose vietose gali naudoti keli vartotojai, o atskiras pamainas vienu metu gali naudoti tik vienas darbuotojas."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 72f73404f99330c3ff8b23dabed78477a0cd30cd
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="shift-and-cash-drawer-management"></a><span data-ttu-id="2e675-104">Pamainos ir kasos stalčių valdymas</span><span class="sxs-lookup"><span data-stu-id="2e675-104">Shift and cash drawer management</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="2e675-105">Šiame straipsnyje paaiškinta, kaip nustatyti ir naudoti dviejų tipų mažmeninės prekybos elektroninio kasos aparato (EKA) pamainas – bendrai naudojamą ir atskirą.</span><span class="sxs-lookup"><span data-stu-id="2e675-105">This article explains how to set up and use the two types of retail point of sale (POS) shifts -  shared and stand-alone.</span></span> <span data-ttu-id="2e675-106">Bendrai naudojimas pamainas keliose vietose gali naudoti keli vartotojai, o atskiras pamainas vienu metu gali naudoti tik vienas darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="2e675-106">Shared shifts can be used by multiple users in multiple places, whereas stand-alone shifts can be used by only one worker at a time.</span></span>

<span data-ttu-id="2e675-107">Galimi du mažmeninės prekybos elektroninio kasos aparato (EKA) pamainų tipai: atskira ir bendrai naudojama.</span><span class="sxs-lookup"><span data-stu-id="2e675-107">There are two types of retail point of sale (POS) shifts: stand-alone and shared.</span></span> <span data-ttu-id="2e675-108">Atskiras pamainas vienu metu gali naudoti tik vienas darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="2e675-108">Stand-alone shifts can be used by only one worker at a time.</span></span> <span data-ttu-id="2e675-109">Bendrai naudojimas pamainas gali naudoti keli vartotojai keliose vietose.</span><span class="sxs-lookup"><span data-stu-id="2e675-109">Shared shifts can be used by multiple users in multiple places.</span></span> <span data-ttu-id="2e675-110">Todėl parduotuvėje galima veiksmingai sukurti keliems vartotojams skirtą vieną pamainą.</span><span class="sxs-lookup"><span data-stu-id="2e675-110">Therefore, they effectively create a single shift for multiple workers in a store.</span></span>

## <a name="standalone-shifts"></a><span data-ttu-id="2e675-111">Atskiros pamainos</span><span class="sxs-lookup"><span data-stu-id="2e675-111">Standalone shifts</span></span>
<span data-ttu-id="2e675-112">Atskiros pamainos naudojamos tradiciniu, pastoviu POS scenarijumi, kada kiekvieno EKA registro grynieji pinigai yra suderinamos atskirai.</span><span class="sxs-lookup"><span data-stu-id="2e675-112">Stand-alone shifts are used in a traditional, fixed POS scenario, where cash is reconciled independently for each POS register.</span></span> <span data-ttu-id="2e675-113">Pvz., parduotuvės aplinkoje paprastai yra keli fiksuoti EKA registrai, o kasininkas priskirtas kiekvienam registrui.</span><span class="sxs-lookup"><span data-stu-id="2e675-113">For example, in a grocery store setting, there are typically several fixed POS registers, and a cashier is assigned to each register.</span></span> <span data-ttu-id="2e675-114">Šiuo atveju kiekvienas registras greičiausiai naudoja atskirą pamainą, o kasininkas yra atsakingas už to registro kasos stalčiaus skyrelį arba fizinės formos grynuosius pinigus.</span><span class="sxs-lookup"><span data-stu-id="2e675-114">In this case, each register likely uses a stand-alone shift, and the cashier is responsible for the till or physical cash at that register.</span></span> <span data-ttu-id="2e675-115">Atskira pamaina apima visą veiklą tame registre per kasininko darbo pamainą.</span><span class="sxs-lookup"><span data-stu-id="2e675-115">A stand-alone shift encompasses all the activity on that register during the cashier’s work shift.</span></span> <span data-ttu-id="2e675-116">Veiklos gali apimti į kasos stalčiaus skyrelį padėtos sumos atidarymą, visas grynųjų pinigų išėmimo ir įdėjimo operacijas, pvz., inkasavimus ir srauto įrašą, ir mokėjimo priemonių deklaravimą pamainai pasibaigus.</span><span class="sxs-lookup"><span data-stu-id="2e675-116">Activities can include the opening amount that is deposited in the till, all removal and addition of cash through operations such as bank drops and float entry, and the tender declaration at the end of the shift.</span></span>

### <a name="set-up-a-stand-alone-shift"></a><span data-ttu-id="2e675-117">Atskiros pamainos nustatymas</span><span class="sxs-lookup"><span data-stu-id="2e675-117">Set up a stand-alone shift</span></span>

<span data-ttu-id="2e675-118">Atskira pamaina priskiriama kasos stalčiaus lygyje.</span><span class="sxs-lookup"><span data-stu-id="2e675-118">A stand-alone shift is designated at the cash drawer level.</span></span> <span data-ttu-id="2e675-119">Šioje procedūroje paaiškinama, kaip nustatyt atskirą pamainą EKA registre.</span><span class="sxs-lookup"><span data-stu-id="2e675-119">This procedure explains how to set up a stand-alone shift on a POS register.</span></span>

1.  <span data-ttu-id="2e675-120">Spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **EKA profiliai** &gt; **Aparatūros profiliai**.</span><span class="sxs-lookup"><span data-stu-id="2e675-120">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>
2.  <span data-ttu-id="2e675-121">Pasirinkite naudotiną atskirtos pamainos aparatūros šabloną.</span><span class="sxs-lookup"><span data-stu-id="2e675-121">Select the hardware profile to use for the stand-alone shift.</span></span>
3.  <span data-ttu-id="2e675-122">„FastTab“ **Stalčius** patikrinkite, ar parinktis **Bendrai naudojamos pamainos stalčius** yra nustatyta į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="2e675-122">On the **Drawer** FastTab, confirm that the **Shared shift drawer** option is set to **No**.</span></span>
4.  <span data-ttu-id="2e675-123">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2e675-123">Click **Save**.</span></span>
5.  <span data-ttu-id="2e675-124">Spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **Registrai**.</span><span class="sxs-lookup"><span data-stu-id="2e675-124">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span>
6.  <span data-ttu-id="2e675-125">Pasirinkite registrą, kuriam reikalinga atskira pamaina, ir tada spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="2e675-125">Select the register that requires a stand-alone shift, and then click **Edit**.</span></span>
7.  <span data-ttu-id="2e675-126">Lauke **Aparatūros šablonas** pasirinkite aparatūros šabloną, kurį pasirinkote atlikdami 2 veiksmą.</span><span class="sxs-lookup"><span data-stu-id="2e675-126">In the **Hardware profile** field, select the hardware profile that you selected in step 2.</span></span>
8.  <span data-ttu-id="2e675-127">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2e675-127">Click **Save**.</span></span>
9.  <span data-ttu-id="2e675-128">Spustelėkite **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="2e675-128">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
10. <span data-ttu-id="2e675-129">Pasirinkite **1090** pasiskirstymo grafiką, o tada spustelėkite **Vykdyti dabar**, kad sinchronizuotumėte EKA keitimus.</span><span class="sxs-lookup"><span data-stu-id="2e675-129">Select the **1090** distribution schedule, and then click **Run now** to synchronize changes to the POS.</span></span>

### <a name="use-a-stand-alone-shift"></a><span data-ttu-id="2e675-130">Atskiros pamainos naudojimas</span><span class="sxs-lookup"><span data-stu-id="2e675-130">Use a stand-alone shift</span></span>

1.  <span data-ttu-id="2e675-131">Prisijunkite prie EKA.</span><span class="sxs-lookup"><span data-stu-id="2e675-131">Sign in to the POS.</span></span>
2.  <span data-ttu-id="2e675-132">Jei neatidaryta jokia pamaina, pasirinkite **Atidaryti naują pamainą**.</span><span class="sxs-lookup"><span data-stu-id="2e675-132">If no shift is open, select **Open a new shift**.</span></span>
3.  <span data-ttu-id="2e675-133">Pasirinkite operaciją **Deklaruoti pradinę sumą** ir nurodykite grynųjų pinigų sumą, kuri bus įtraukta į kasos stalčiaus skyrelį darbo dienos pradžioje.</span><span class="sxs-lookup"><span data-stu-id="2e675-133">Go to the **Declare start amount** operation, and specify the amount of cash that is being added to the till to start the work day.</span></span>
4.  <span data-ttu-id="2e675-134">Atlikite keletą operacijų.</span><span class="sxs-lookup"><span data-stu-id="2e675-134">Perform some transactions.</span></span>
5.  <span data-ttu-id="2e675-135">Pasibaigus dienai pasirinkite **Deklaruoti mokėjimo priemonę**, kad deklaruotumėte kasos stalčiuje likusią grynųjų pinigų sumą.</span><span class="sxs-lookup"><span data-stu-id="2e675-135">At the end of the day, select **Declare tender** to declare the amount of cash that remains in the cash drawer.</span></span>
6.  <span data-ttu-id="2e675-136">Įveskite grynųjų pinigų sumą, o tada spustelėkite **Įrašyti**, kad įrašytumėte mokėjimo priemonės deklaravimą.</span><span class="sxs-lookup"><span data-stu-id="2e675-136">Enter the amount of cash, and then click **Save** to save the tender declaration.</span></span>
7.  <span data-ttu-id="2e675-137">Pasirinkite **Uždaryti pamainą**, kad uždarytumėte pamainą.</span><span class="sxs-lookup"><span data-stu-id="2e675-137">Select **Close shift** to close the shift.</span></span>

<span data-ttu-id="2e675-138">**Pastaba.** Pamainos metu galima atlikti kitas operacijas, priklausomai nuo vykdomų verslo procesų.</span><span class="sxs-lookup"><span data-stu-id="2e675-138">**Note:** Other operations are available during the shift, depending on the business processes that are in place.</span></span> <span data-ttu-id="2e675-139">Galima atlikti operacijas **Pinigų įnešimas į kasą**, **Inkasavimas** ir **Mokėjimo priemonės šalinimas**, norint dienos metu arba prieš uždarant pamainą iš kasos stalčiaus skyrelio išimti pinigus.</span><span class="sxs-lookup"><span data-stu-id="2e675-139">The **Safe drop**, **Bank drop**, and **Tender removal** operations can be used to remove money from the till during the day or before the shift is closed.</span></span> <span data-ttu-id="2e675-140">Jei kasos stalčiaus skyrelyje yra per mažai pinigų, galima naudoti operaciją **Srauto įrašas**, norint į kasos stalčiaus skyrelį įdėti grynųjų pinigų.</span><span class="sxs-lookup"><span data-stu-id="2e675-140">If a till runs low on cash, the **Float entry** operation can be used to add cash to the till.</span></span>

## <a name="shared-shifts"></a><span data-ttu-id="2e675-141">Bendrai naudojamos pamainos</span><span class="sxs-lookup"><span data-stu-id="2e675-141">Shared shifts</span></span>
<span data-ttu-id="2e675-142">Bendrai naudojama pamaina naudojama tada, kai visą darbo dieną keli kasininkai bendrai naudoja kasos stalčių arba kasos stalčių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="2e675-142">A shared shift is used in an environment where multiple cashiers share a cash drawer or a set of cash drawers throughout the work day.</span></span> <span data-ttu-id="2e675-143">Paprastai bendrai naudojama pamaina yra naudojama mobiliojoje EKA aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="2e675-143">Typically, a shared shift is used in mobile POS environments.</span></span> <span data-ttu-id="2e675-144">Mobiliojoje aplinkoje nė vienas kasininkas nėra priskirtas arba atsakingas už vieną kasos stalčių.</span><span class="sxs-lookup"><span data-stu-id="2e675-144">In a mobile environment, each cashier isn’t assigned to and responsible for a single cash drawer.</span></span> <span data-ttu-id="2e675-145">Visi kasininkai turi turėti galimybę užregistruoti pardavimą ir įdėti pinigų į artimiausią kasos aparatą.</span><span class="sxs-lookup"><span data-stu-id="2e675-145">Instead, all cashiers must be able to tender a sale and add cash to whatever cash drawer is closest to them.</span></span> <span data-ttu-id="2e675-146">Tokiu atveju kasos stalčiai, kuriuos kasininkai bendrai naudoja, įtraukiami į bendrai naudojamą pamainą.</span><span class="sxs-lookup"><span data-stu-id="2e675-146">In this scenario, the cash drawers that are shared among cashiers are included in a shared shift.</span></span> <span data-ttu-id="2e675-147">Visi bendrai naudojamos pamainos kasos stalčiai įtraukiami į vieną pamainą, kad būtų galima vykdyti su grynųjų pinigų valdymu susijusias tos pamainos veiklas.</span><span class="sxs-lookup"><span data-stu-id="2e675-147">All the cash drawers in a shared shift are included in the same shift for the purpose of activities that are related to cash management for that shift.</span></span> <span data-ttu-id="2e675-148">Todėl pradinė pamainos suma turėtų apimti visuose į bendrai naudojamą pamainą įtrauktuose kasos stalčiuose esančią grynųjų pinigų sumą.</span><span class="sxs-lookup"><span data-stu-id="2e675-148">Therefore, the starting amount for the shift should include the sum of all cash in all the cash drawers that are included in the shared shift.</span></span> <span data-ttu-id="2e675-149">Taip pat mokėjimo priemonės deklaravimas bus visuose į bendrai naudojamą pamainą įtrauktuose kasos stalčiuose esanti grynųjų pinigų suma.</span><span class="sxs-lookup"><span data-stu-id="2e675-149">Likewise, the tender declaration will be the sum of all the cash in all the cash drawers that are included in the shared shift.</span></span> <span data-ttu-id="2e675-150">**Pastaba:** kiekvienoje parduotuvėje vienu metu galima atidaryti tik vieną bendrai naudojamą pamainą.</span><span class="sxs-lookup"><span data-stu-id="2e675-150">**Note:** Only one shared shift can be open at a time in each store.</span></span> <span data-ttu-id="2e675-151">Toje pačioje parduotuvėje galima naudoti bendrai naudojamas pamainas ir atskiras pamainas.</span><span class="sxs-lookup"><span data-stu-id="2e675-151">Shared shifts and stand-alone shifts can be used in the same store.</span></span>

### <a name="set-up-a-shared-shift"></a><span data-ttu-id="2e675-152">Bendrai naudojamos pamainos nustatymas</span><span class="sxs-lookup"><span data-stu-id="2e675-152">Set up a shared shift</span></span>

1.  <span data-ttu-id="2e675-153">Spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **EKA profiliai** &gt; **Aparatūros profiliai**.</span><span class="sxs-lookup"><span data-stu-id="2e675-153">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>
2.  <span data-ttu-id="2e675-154">Pasirinkite naudotiną bendrai naudojamos pamainos aparatūros šabloną.</span><span class="sxs-lookup"><span data-stu-id="2e675-154">Select the hardware profile to use for the shared shift.</span></span>
3.  <span data-ttu-id="2e675-155">„FastTab“ **Stalčius** parinktį **Bendrai naudojamos pamainos stalčius** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="2e675-155">On the **Drawer** FastTab, set the **Shared shift drawer** option to **Yes**.</span></span>
4.  <span data-ttu-id="2e675-156">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2e675-156">Click **Save**.</span></span>
5.  <span data-ttu-id="2e675-157">Spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **Registrai**.</span><span class="sxs-lookup"><span data-stu-id="2e675-157">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span>
6.  <span data-ttu-id="2e675-158">Pasirinkite registrą, kuriam reikalinga bendrai naudojama pamaina, ir tada spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="2e675-158">Select the register that requires a shared shift, and then click **Edit**.</span></span>
7.  <span data-ttu-id="2e675-159">Lauke **Aparatūros šablonas** pasirinkite aparatūros šabloną, kurį pasirinkote atlikdami 2 veiksmą.</span><span class="sxs-lookup"><span data-stu-id="2e675-159">In the **Hardware profile** field, select the hardware profile that you selected in step 2.</span></span>
8.  <span data-ttu-id="2e675-160">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2e675-160">Click **Save**.</span></span>
9.  <span data-ttu-id="2e675-161">Spustelėkite **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="2e675-161">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
10. <span data-ttu-id="2e675-162">Pasirinkite **1090** pasiskirstymo grafiką, o tada spustelėkite **Vykdyti dabar**, kad sinchronizuotumėte EKA keitimus.</span><span class="sxs-lookup"><span data-stu-id="2e675-162">Select the **1090** distribution schedule, and then click **Run now** to synchronize changes to the POS.</span></span>

### <a name="use-a-shared-shift"></a><span data-ttu-id="2e675-163">Bendrai naudojamos pamainos naudojimas</span><span class="sxs-lookup"><span data-stu-id="2e675-163">Use a shared shift</span></span>

1.  <span data-ttu-id="2e675-164">Prisijunkite prie EKA.</span><span class="sxs-lookup"><span data-stu-id="2e675-164">Sign in to the POS.</span></span>
2.  <span data-ttu-id="2e675-165">Jei dar EKA dar neprijungtas prie aparatūros stoties, pasirinkite **Su stalčiumi nesusijusi operacija**, o tada pasirinkite operaciją **Pasirinkti aparatūros stotį**, kad suaktyvintumėte bendrai naudojamos pamainos aparatūros stotį.</span><span class="sxs-lookup"><span data-stu-id="2e675-165">If the POS isn’t yet connected to a hardware station, select **Non-drawer operation**, and then select the **Select hardware station** operation to make a hardware station active for the shared shift.</span></span> <span data-ttu-id="2e675-166">Šį veiksmą reikia atlikti tik pirmą kartą registrą įtraukiant į bendrai naudojamos pamainos aplinką.</span><span class="sxs-lookup"><span data-stu-id="2e675-166">This step is required only the first time that a register is added to a shared shift environment.</span></span>
3.  <span data-ttu-id="2e675-167">Atsijunkite nuo EKA ir vėl prisijunkite.</span><span class="sxs-lookup"><span data-stu-id="2e675-167">Sign out of the POS, and then sign back in.</span></span>
4.  <span data-ttu-id="2e675-168">Pasirinkite **Kurti naują pamainą**.</span><span class="sxs-lookup"><span data-stu-id="2e675-168">Select **Create a new shift**.</span></span>
5.  <span data-ttu-id="2e675-169">Pasirinkite **Deklaruoti pradinę sumą**.</span><span class="sxs-lookup"><span data-stu-id="2e675-169">Select **Declare start amount**.</span></span>
6.  <span data-ttu-id="2e675-170">Įveskite visų parduotuvės kasos stalčių, įtrauktų į bendrai naudojamą pamainą, pradinę sumą, o tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2e675-170">Enter the starting amount of all the cash drawers in the store that are part of the shared shift, and then click **Save**.</span></span>
    -   <span data-ttu-id="2e675-171">Norėdami pradinės sumos dalį įtraukti į kiekvieną paskesnį kasos stalčių, naudokite operaciją **Pasirinkti aparatūros stotį**, kad suaktyvintumėte aparatūros stotį.</span><span class="sxs-lookup"><span data-stu-id="2e675-171">To add part of the starting amount to each subsequent cash drawer, use the **Select hardware station** operation to make the hardware station active.</span></span>
    -   <span data-ttu-id="2e675-172">Norėdami į konkretų kasos stalčių įtraukti kasos stalčiaus skyrelį, naudokite operaciją **Atidaryti stalčių**.</span><span class="sxs-lookup"><span data-stu-id="2e675-172">To add a till to a specific cash drawer, use the **Open drawer** operation.</span></span>
    -   <span data-ttu-id="2e675-173">Tęskite, kol visose bendrai naudojamos pamainos kasos stalčiuose bus reikiama pradinės sumos dalis.</span><span class="sxs-lookup"><span data-stu-id="2e675-173">Continue until all cash drawers in the shared shift have their part of the starting amount.</span></span>

7.  <span data-ttu-id="2e675-174">Pasibaigus dienai atidarykite kiekvieną kasos stalčių ir išimkite grynuosius pinigus.</span><span class="sxs-lookup"><span data-stu-id="2e675-174">At the end of the day, open each cash drawer, and remove the cash.</span></span>
8.  <span data-ttu-id="2e675-175">Išėmę grynuosius pinigus iš paskutinio kasos stalčiaus, suskaičiuokite visų kasos stalčių grynuosius pinigus.</span><span class="sxs-lookup"><span data-stu-id="2e675-175">After you’ve removed the cash from the last cash drawer, count all the cash from all the cash drawers.</span></span>
9.  <span data-ttu-id="2e675-176">Naudokite operaciją **Deklaruoti mokėjimo priemonę**, kad deklaruotumėte bendrą grynųjų pinigų sumą visuose bendrai naudojamos pamainos kasos stalčiuose.</span><span class="sxs-lookup"><span data-stu-id="2e675-176">Use the **Declare tender** operation to declare the total amount of cash from all the cash drawers that are included in the shared shift.</span></span>
10. <span data-ttu-id="2e675-177">Naudokite operaciją **Uždaryti pamainą**, kad uždarytumėte bendrai naudojamą pamainą.</span><span class="sxs-lookup"><span data-stu-id="2e675-177">Use the **Close shift** operation to close the shared shift.</span></span>




