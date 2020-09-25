---
title: Laiko rezervai
description: Šioje temoje aprašoma, kaip galima naudoti laiko rezervus su planavimo optimizavimo papildiniu, skirtu „Microsoft Dynamics 365 Supply Chain Management”.
author: ChristianRytt
manager: tfehr
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 05ac817081689f27cdf55cb86a3235d7707a737b
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803426"
---
# <a name="safety-margins"></a><span data-ttu-id="167b5-103">Laiko rezervai</span><span class="sxs-lookup"><span data-stu-id="167b5-103">Safety margins</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="167b5-104">Šioje temoje aprašoma, kaip galima naudoti laiko rezervus su planavimo optimizavimo papildiniu, skirtu „Microsoft Dynamics 365 Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="167b5-104">This topic describes how safety margins can be used with the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="safety-margins-overview"></a><span data-ttu-id="167b5-105">Laiko rezervų peržiūra</span><span class="sxs-lookup"><span data-stu-id="167b5-105">Safety margins overview</span></span>

<span data-ttu-id="167b5-106">Laiko rezervų paskirtis yra įgalinti sąranką, suteikiančią buferio laiko siekiant viršyti įprastą gamybos laiką.</span><span class="sxs-lookup"><span data-stu-id="167b5-106">The purpose of safety margins is to enable a setup that provides some buffer time beyond the normal lead time.</span></span> <span data-ttu-id="167b5-107">Pavyzdžiui, kai medžiaga turi būti išpakuota ar patikrinta po to, kai ji atvyksta iš tiekėjo, negalima tiesiog įtraukti papildomo laiko į pirkimo gamybos laiką, nes tokiu atveju papildomas buferio laikas bus priskirtas tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="167b5-107">For example, when material must be unpacked or inspected after it arrives from the vendor, you can't just add the extra time to the purchase lead time, because this approach will give the additional buffer time to the supplier.</span></span> <span data-ttu-id="167b5-108">Šiame pavyzdyje galima naudoti gavimo laiko rezervą siekiant užtikrinti, kad tiekėjas pristatytų anksčiau.</span><span class="sxs-lookup"><span data-stu-id="167b5-108">In this example, the receipt margin can be used to ensure that the supplier delivers earlier.</span></span> <span data-ttu-id="167b5-109">Šis metodas teikia buferio laiko, kad prekes būtų galima apdoroti viduje.</span><span class="sxs-lookup"><span data-stu-id="167b5-109">This approach provides buffer time so that the goods can be handled internally.</span></span>

<span data-ttu-id="167b5-110">Yra trys laiko rezervų tipai:</span><span class="sxs-lookup"><span data-stu-id="167b5-110">There are three types of safety margins:</span></span>

- <span data-ttu-id="167b5-111">**Užsakymo laiko rezervas** – tiekimo užsakymo pateikimo buferio laikas</span><span class="sxs-lookup"><span data-stu-id="167b5-111">**Reorder margin** – The buffer time for placing the supply order</span></span>
- <span data-ttu-id="167b5-112">**Gavimo laiko rezervas** – gaunamo tiekimo tvarkymo buferio laikas</span><span class="sxs-lookup"><span data-stu-id="167b5-112">**Receipt margin** – The buffer time for handling incoming supply</span></span>
- <span data-ttu-id="167b5-113">**Išdavimo laiko rezervas** – siuntų tvarkymo buferio laikas</span><span class="sxs-lookup"><span data-stu-id="167b5-113">**Issue margin** – The buffer time for handling shipments</span></span>

<span data-ttu-id="167b5-114">Toliau pateiktoje iliustracijoje parodyta, kaip šie laiko rezervai taikomi laikui bėgant.</span><span class="sxs-lookup"><span data-stu-id="167b5-114">The following illustration shows how these safety margins apply over time.</span></span>

![Laiko rezervai](media/safety-margins-1.png)

<span data-ttu-id="167b5-116">Visi laiko rezervai apibrėžiami dienomis.</span><span class="sxs-lookup"><span data-stu-id="167b5-116">All margins are defined in days.</span></span> <span data-ttu-id="167b5-117">Numatytoji vertė yra *0* (nulis), nurodanti, kad netaikomas laiko rezervas.</span><span class="sxs-lookup"><span data-stu-id="167b5-117">The default value, *0* (zero), indicates that no margin is applied.</span></span> <span data-ttu-id="167b5-118">Jei nustatote kelis laiko rezervus, jie visi įtraukiami į bendrą laiką nuo tiekimo *užsakymo datos* iki paklausos *poreikio datos*.</span><span class="sxs-lookup"><span data-stu-id="167b5-118">If you set up multiple margins, they all add to the total time from the supply *order date* to the demand *requirement date*.</span></span> <span data-ttu-id="167b5-119">Pavyzdžiui, sąrankoje nenustatytas gamybos laikas, o visi trys laiko rezervų tipai nustatyti į vieną dieną.</span><span class="sxs-lookup"><span data-stu-id="167b5-119">For example, a setup has no lead time, and all three margin types are set to one day.</span></span> <span data-ttu-id="167b5-120">Tokiu atveju nuo tiekimo užsakymo datos ir paklausos poreikio datos bus trys dienos, taigi, jei užsakymo data yra liepos 1 d., poreikio data būtų liepos 4 d.</span><span class="sxs-lookup"><span data-stu-id="167b5-120">In this case, there will be three days between the supply order date and the demand requirement date, so if the order date is July 1, the requirement date would be July 4.</span></span>

### <a name="receipt-margin"></a><span data-ttu-id="167b5-121">Gavimo laiko rezervas</span><span class="sxs-lookup"><span data-stu-id="167b5-121">Receipt margin</span></span>

<span data-ttu-id="167b5-122">Gavimo laiko rezervas yra turbūt labiausiai naudojamas iš trijų laiko rezervų.</span><span class="sxs-lookup"><span data-stu-id="167b5-122">The receipt margin is probably the most used of the three safety margins.</span></span> <span data-ttu-id="167b5-123">Jis taikomas *pristatymo datai* ir atgal nuo *poreikio datos*.</span><span class="sxs-lookup"><span data-stu-id="167b5-123">It's applied to the *delivery date* and backward from the *requirement date*.</span></span> <span data-ttu-id="167b5-124">Kitaip tariant, produktai turi būti gauti nurodytą gavimo laiko rezervo dienų skaičių iki poreikio datos.</span><span class="sxs-lookup"><span data-stu-id="167b5-124">In other words, the products should be received the specified number of receipt margin days before they are required.</span></span>

<span data-ttu-id="167b5-125">Toliau pateiktoje iliustracijoje pabrėžiamas gavimo laiko rezervas.</span><span class="sxs-lookup"><span data-stu-id="167b5-125">The following illustration highlights the receipt margin.</span></span>

![Gavimo laiko rezervas](media/safety-margins-2.png)

<span data-ttu-id="167b5-127">Gavimo laiko rezervas paprastai naudojamas kaip buferis, siekiant užtikrinti sandėlio registravimo laiką arba kitus daug laiko reikalaujančius procesus, kurie nėra fiksuojami kaip bendrojo gamybos laiko dalis sistemoje.</span><span class="sxs-lookup"><span data-stu-id="167b5-127">The receipt margin is typically used as a buffer to ensure time for warehouse registration or other time-consuming processes that aren't captured as part of the general lead time in the system.</span></span> <span data-ttu-id="167b5-128">Pirkimo atveju vienas privalumas yra tai, kad pirkimo užsakymo *pristatymo data* atitinkamai perkeliama į priekį.</span><span class="sxs-lookup"><span data-stu-id="167b5-128">For purchases, one benefit is that the *delivery date* of the purchase order is moved forward accordingly.</span></span> <span data-ttu-id="167b5-129">Jei pratęsite gamybos laiką, užuot naudoję laiko rezervą, tiekėjo vis tiek bus paprašyta pristatyti paskutinę minutę.</span><span class="sxs-lookup"><span data-stu-id="167b5-129">If you  increase the lead time instead of using a safety margin, the vendor will still be asked to deliver at the last minute.</span></span>

<span data-ttu-id="167b5-130">Atkreipkite dėmesį, kad gavimo laiko rezervas nekeičia tiekimo *poreikio datos*.</span><span class="sxs-lookup"><span data-stu-id="167b5-130">Notice that the receipt margin doesn't change the *requirement date* of the supply.</span></span> <span data-ttu-id="167b5-131">Todėl gavimo laiko rezervas nėra tiesiogiai matomas, kai lyginamos paklausos ir tiekimo poreikio datos (pvz., puslapyje **Grynieji poreikiai**).</span><span class="sxs-lookup"><span data-stu-id="167b5-131">Therefore, the receipt margin isn't directly visible when requirement dates for demand and supply are compared (for example, on the **Net requirements** page).</span></span> <span data-ttu-id="167b5-132">Pvz., jei nustatytas keturių dienų gavimo laiko rezervas, o pirkimo užsakymo eilutės gavimas penkioliktą 15 mėnesio dieną, bendrasis planavimas apskaičiuoja koreguotą gavimo datą, kuri yra devyniolikta mėnesio diena.</span><span class="sxs-lookup"><span data-stu-id="167b5-132">For example, if the receipt margin is set to four days, and a purchase order line is planned for receipt on the fifteenth of the month, master planning calculates the adjusted receipt date as the nineteenth of the month.</span></span>

<span data-ttu-id="167b5-133">Atkreipkite dėmesį, kad gavimo laiko rezervas nėra taikomas, kai tiekimui naudojamos turimos atsargos.</span><span class="sxs-lookup"><span data-stu-id="167b5-133">Note that a receipt margin isn't applied when on-hand inventory is used as the supply.</span></span> <span data-ttu-id="167b5-134">Visos turimos atsargos laikomos pasiekiamomis nedelsiant, neatsižvelgiant į tai, kada jos buvo gautos.</span><span class="sxs-lookup"><span data-stu-id="167b5-134">All on-hand inventory is assumed to be available immediately, regardless of when it was actually received.</span></span>

### <a name="reorder-margin"></a><span data-ttu-id="167b5-135">Užsakymo laiko rezervas</span><span class="sxs-lookup"><span data-stu-id="167b5-135">Reorder margin</span></span>

> [!NOTE]
> <span data-ttu-id="167b5-136">**Jau greitai:** šios funkcijos planavimo optimizavimas dar nepalaiko.</span><span class="sxs-lookup"><span data-stu-id="167b5-136">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="167b5-137">Kol ji nepalaikoma, visos reikšmės, įvestos **Užsakymo laiko rezervas, įtrauktas į prekės gamybos laiką**, nebus vertinamos kaip *0* (nulis).</span><span class="sxs-lookup"><span data-stu-id="167b5-137">Until it's supported, all values that are entered for **Reorder margin added to item lead time** will be treated as *0* (zero).</span></span>

<span data-ttu-id="167b5-138">Toliau pateiktoje iliustracijoje pabrėžiamas užsakymo laiko rezervas.</span><span class="sxs-lookup"><span data-stu-id="167b5-138">The following illustration highlights the reorder margin.</span></span>

![Užsakymo laiko rezervas](media/safety-margins-3.png)

<span data-ttu-id="167b5-140">Užsakymo laiko rezervas įtraukiamas prieš visų suplanuotų užsakymų prekių gamybos laiką bendrojo planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="167b5-140">The reorder margin is added before the item lead time for all planned orders during master planning.</span></span> <span data-ttu-id="167b5-141">Todėl tai užtikrina papildomą laiką, kurio reikia pateikti tiekimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="167b5-141">Therefore, it ensures additional time for a supply order to be placed.</span></span> <span data-ttu-id="167b5-142">Šis laiko rezervas paprastai naudojamas kaip buferis, siekiant užtikrinti patvirtinimo procesų ir kitų vidinių procesų, reikalingų kuriant tiekimo užsakymus, laiką.</span><span class="sxs-lookup"><span data-stu-id="167b5-142">This margin is typically used as a buffer to ensure time for approval processes or other internal processes that are required during the creation of supply orders.</span></span> <span data-ttu-id="167b5-143">Užsakymo laiko rezervas pateikiamas tarp tiekimo *užsakymo datos* ir *pradžios datos*.</span><span class="sxs-lookup"><span data-stu-id="167b5-143">The reorder margin is put between the supply *order date* and *start date*.</span></span>

### <a name="issue-margin"></a><span data-ttu-id="167b5-144">Išdavimo laiko rezervas</span><span class="sxs-lookup"><span data-stu-id="167b5-144">Issue margin</span></span>

> [!NOTE]
> <span data-ttu-id="167b5-145">**Jau greitai:** šios funkcijos planavimo optimizavimas dar nepalaiko.</span><span class="sxs-lookup"><span data-stu-id="167b5-145">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="167b5-146">Kol ji nepalaikoma, visos reikšmės, įvestos **Išdavimo laiko rezervas, atimtas iš poreikio datos**, nebus vertinamos kaip *0* (nulis).</span><span class="sxs-lookup"><span data-stu-id="167b5-146">Until it's supported, all values that are entered for **Issue margin deducted from requirement date** will be treated as *0* (zero).</span></span>

<span data-ttu-id="167b5-147">Toliau pateiktoje iliustracijoje pabrėžiamas išdavimo laiko rezervas.</span><span class="sxs-lookup"><span data-stu-id="167b5-147">The following illustration highlights the issue margin.</span></span>

![Išdavimo laiko rezervas](media/safety-margins-4.png)

<span data-ttu-id="167b5-149">Išdavimo laiko rezervas atimamas iš paklausos poreikio datos bendrojo planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="167b5-149">The issue margin is deducted from the demand requirement date during master planning.</span></span> <span data-ttu-id="167b5-150">Tai padeda užtikrinti, kad turėtumėte laiko reaguoti į gaunamus poreikio užsakymus ir juos išsiųsti.</span><span class="sxs-lookup"><span data-stu-id="167b5-150">It helps ensure that you have time to react to and ship incoming demand orders.</span></span> <span data-ttu-id="167b5-151">Šis laiko rezervas paprastai naudojamas kaip buferis, siekiant užtikrinti siuntimo ir susijusių siunčiamų sandėlio procesų laiką.</span><span class="sxs-lookup"><span data-stu-id="167b5-151">This margin is typically used as a buffer to ensure time for shipment and related outbound warehouse processes.</span></span>

<span data-ttu-id="167b5-152">Atkreipkite dėmesį, kad kai taikomas išdavimo laiko rezervas, nesutampa susijusios tiekimo ir paklausos poreikio datos.</span><span class="sxs-lookup"><span data-stu-id="167b5-152">Notice that when an issue margin is applied, related supply and demand requirement dates don't match.</span></span> <span data-ttu-id="167b5-153">Vietoj to jos skiriasi pagal išdavimo laiko rezervą, nes išdavimo laiko rezervas įtraukiamas tarp tiekimo *poreikio datos* ir paklausos *poreikio datos*.</span><span class="sxs-lookup"><span data-stu-id="167b5-153">Instead, they differ by the issue margin, because the issue margin is added between the supply *requirement date* and the demand *requirement date*.</span></span>

## <a name="set-up-safety-margins"></a><span data-ttu-id="167b5-154">Laiko rezervų nustatymas</span><span class="sxs-lookup"><span data-stu-id="167b5-154">Set up safety margins</span></span>

### <a name="turn-on-safety-margins-in-feature-management"></a><span data-ttu-id="167b5-155">Laiko rezervų įjungimas srityje Funkcijų valdymas</span><span class="sxs-lookup"><span data-stu-id="167b5-155">Turn on safety margins in Feature management</span></span>

<span data-ttu-id="167b5-156">Kad galėtumėte naudoti šią funkciją su planavimo optimizavimu, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="167b5-156">Before you can use this feature with Planning Optimization, it must be turned on in your system.</span></span> <span data-ttu-id="167b5-157">Administratoriai gali naudoti [Funkcijos valdymas](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="167b5-157">Admins can use the [Feature management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="167b5-158">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="167b5-158">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="167b5-159">**Modulis:** _Bendrasis planavimas_</span><span class="sxs-lookup"><span data-stu-id="167b5-159">**Module:** _Master planning_</span></span>
- <span data-ttu-id="167b5-160">**Funkcijos pavadinimas:** _Planavimo optimizavimo laiko rezervai_</span><span class="sxs-lookup"><span data-stu-id="167b5-160">**Feature name:** _Margins for Planning Optimization_</span></span>

### <a name="define-safety-margins"></a><span data-ttu-id="167b5-161">Laiko rezervų nustatymas</span><span class="sxs-lookup"><span data-stu-id="167b5-161">Define safety margins</span></span>

<span data-ttu-id="167b5-162">Laiko rezervų sąranka yra lanksti.</span><span class="sxs-lookup"><span data-stu-id="167b5-162">Safety margins have a flexible setup.</span></span> <span data-ttu-id="167b5-163">Juos galima nustatyti ir *padengimo grupėje*, ir *bendrajame plane*.</span><span class="sxs-lookup"><span data-stu-id="167b5-163">They can be set on both the *coverage group* and the *master plan*.</span></span> <span data-ttu-id="167b5-164">Svarbu, kad suprastumėte, jog laiko rezervai įtraukiami vienas ant kito.</span><span class="sxs-lookup"><span data-stu-id="167b5-164">It's important that you understand that the margins are added on top of each other.</span></span> <span data-ttu-id="167b5-165">Pavyzdžiui, dviejų dienų gavimo laiko rezervas padengimo grupėje ir trijų dienų bendrajame plane užtikrins penkias dienas galiojantį gavimo laiko rezervą.</span><span class="sxs-lookup"><span data-stu-id="167b5-165">For example, a receipt margin of two days on the coverage group and three days on the master plan will produce an effective receipt margin of five days.</span></span>

<span data-ttu-id="167b5-166">Galimybė nustatyti laiko rezervą bendrajame plane gali būti naudinga, kai norite imituoti ilgesnį gamybos laiką arba tam tikro plano neapibrėžtumą nekeisdami kasdienio planavimo.</span><span class="sxs-lookup"><span data-stu-id="167b5-166">The ability to set the margin on the master plan can be useful when you want to simulate longer lead times or uncertainty for a specific plan, but without affecting the daily planning.</span></span>

#### <a name="coverage-group-safety-margins"></a><span data-ttu-id="167b5-167">Padengimo grupių laiko rezervai</span><span class="sxs-lookup"><span data-stu-id="167b5-167">Coverage group safety margins</span></span>

<span data-ttu-id="167b5-168">Norėdami taikyti laiko rezervą padengimo grupei, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="167b5-168">To apply a safety margin to a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="167b5-169">Eikite į **Bendrasis planavimas \> Sąranka \> Padengimo grupės**.</span><span class="sxs-lookup"><span data-stu-id="167b5-169">Go to **Master planning \> Setup \> Coverage groups**.</span></span>
1. <span data-ttu-id="167b5-170">Sąrašo srityje pasirinkite norimą padengimo grupę.</span><span class="sxs-lookup"><span data-stu-id="167b5-170">In the list pane, select the desired coverage group.</span></span>
1. <span data-ttu-id="167b5-171">Skyriaus **Laiko rezervai dienomis** „FastTab” **Kita** naudokite toliau pateiktus laukus, kad nustatytumėte reikiamus laiko rezervus (dienomis).</span><span class="sxs-lookup"><span data-stu-id="167b5-171">On the **Other** FastTab, in the **Safety margins in days** section, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="167b5-172">Gavimo laiko rezervas, pridėtas prie pareikalavimo datos</span><span class="sxs-lookup"><span data-stu-id="167b5-172">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="167b5-173">Išdavimo laiko rezervas, atimtas iš pareikalavimo datos</span><span class="sxs-lookup"><span data-stu-id="167b5-173">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="167b5-174">Keisti maržos, įtrauktos į prekės gamybos laiką, tvarką</span><span class="sxs-lookup"><span data-stu-id="167b5-174">Reorder margin added to item lead time</span></span>

#### <a name="master-plan-safety-margins"></a><span data-ttu-id="167b5-175">Bendrųjų planų laiko rezervai</span><span class="sxs-lookup"><span data-stu-id="167b5-175">Master plan safety margins</span></span>

<span data-ttu-id="167b5-176">Norėdami taikyti laiko rezervą bendrajam planui, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="167b5-176">To apply a safety margin to a master plan, follow these steps.</span></span>

1. <span data-ttu-id="167b5-177">Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.</span><span class="sxs-lookup"><span data-stu-id="167b5-177">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="167b5-178">Sąrašo srityje pasirinkite norimą bendrąjį planą.</span><span class="sxs-lookup"><span data-stu-id="167b5-178">In the list pane, select the desired master plan.</span></span>
1. <span data-ttu-id="167b5-179">„FastTab” **Laiko rezervai dienomis** naudokite toliau pateiktus laukus, kad nustatytumėte reikiamus laiko rezervus (dienomis).</span><span class="sxs-lookup"><span data-stu-id="167b5-179">On the **Safety margins in days** FastTab, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="167b5-180">Gavimo laiko rezervas, pridėtas prie pareikalavimo datos</span><span class="sxs-lookup"><span data-stu-id="167b5-180">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="167b5-181">Išdavimo laiko rezervas, atimtas iš pareikalavimo datos</span><span class="sxs-lookup"><span data-stu-id="167b5-181">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="167b5-182">Keisti maržos, įtrauktos į prekės gamybos laiką, tvarką</span><span class="sxs-lookup"><span data-stu-id="167b5-182">Reorder margin added to item lead time</span></span>

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a><span data-ttu-id="167b5-183">Nurodykite, ar skaičiavimai pagrįsti kalendorinėmis dienomis, ar darbo dienomis</span><span class="sxs-lookup"><span data-stu-id="167b5-183">Define whether calculations are based on calendar days or work days</span></span>

<span data-ttu-id="167b5-184">Galite nustatyti visus laiko rezervus, kad jie būtų apskaičiuojami pagal kalendorines dienas arba darbo dienas.</span><span class="sxs-lookup"><span data-stu-id="167b5-184">You can set all safety margins so that they are calculated based on either calendar days or work days.</span></span>

1. <span data-ttu-id="167b5-185">Eikite į **Bendrasis planavimas \> Sąranka \> Bendrojo planavimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="167b5-185">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
1. <span data-ttu-id="167b5-186">Skyriaus **Laiko rezervai dienomis** skirtuke **Bendra** nustatykite parinktį **Darbo dienos** į *Taip*, kad laiko rezervai būtų apskaičiuoti pagal darbo dienas.</span><span class="sxs-lookup"><span data-stu-id="167b5-186">On the **General** tab, in the **Safety margins in days** section, set the **Working days** option to *Yes* to calculate margins based on working days.</span></span> <span data-ttu-id="167b5-187">Nustatykite parinktį į *Ne*, kad laiko rezervai būtų apskaičiuoti pagal kalendorines dienas.</span><span class="sxs-lookup"><span data-stu-id="167b5-187">Set the option to *No* to calculate margins based on calendar days.</span></span>

<span data-ttu-id="167b5-188">Pavyzdžiui, kalendorius yra atidarytas nuo pirmadienio iki penktadienio ir uždarytas nuo šeštadienio iki sekmadienio.</span><span class="sxs-lookup"><span data-stu-id="167b5-188">For example, a calendar is open from Monday through Friday and closed from Saturday through Sunday.</span></span> <span data-ttu-id="167b5-189">Jei yra vienos dienos laiko rezervas, pirmadienio poreikio data pateikia praėjusio penktadienio pristatymo datą, nes šeštadienis ir sekmadienis nėra darbo dienos.</span><span class="sxs-lookup"><span data-stu-id="167b5-189">If there is a receipt margin of one day, a requirement date on a Monday produces a delivery date on the previous Friday, because Saturday and Sunday aren't working days.</span></span>

<span data-ttu-id="167b5-190">Kalendorius, naudojamas darbo dienoms nustatyti, priklauso nuo sąrankos ir tiekimo tipo.</span><span class="sxs-lookup"><span data-stu-id="167b5-190">The calendar that is used to determine the working days depends on the setup and the supply type.</span></span> <span data-ttu-id="167b5-191">Jį gali valdyti padengimo grupės, sandėlio ir tiekėjo kalendoriai.</span><span class="sxs-lookup"><span data-stu-id="167b5-191">It can be controlled by the calendars of the coverage group, the warehouse, and the vendor.</span></span>

> [!NOTE]
> <span data-ttu-id="167b5-192">Jei *sandėlis* nėra padengimo dimensijos dalis (kitaip tariant, planavimas paremtas tik *svetaine*), sandėlio kalendorius nenaudojamas.</span><span class="sxs-lookup"><span data-stu-id="167b5-192">If *warehouse* isn't part of the coverage dimension (in other words, planning is based only on *site*), the warehouse calendar isn't used.</span></span>

<span data-ttu-id="167b5-193">Sistema gali tvarkyti sąranką, kurioje apibrėžti vienas arba daugiau kalendorių.</span><span class="sxs-lookup"><span data-stu-id="167b5-193">The system can handle a setup where one or more calendars are defined.</span></span> <span data-ttu-id="167b5-194">Toliau esančiuose poskirsniuose aprašomi galimi deriniai, kuriuos galima naudoti rezultatui valdyti.</span><span class="sxs-lookup"><span data-stu-id="167b5-194">The following subsections describe the possible combinations that can be used to control the result.</span></span>

#### <a name="calendar-that-is-used-for-the-duration"></a><span data-ttu-id="167b5-195">Kalendorius, naudojamas trukmei</span><span class="sxs-lookup"><span data-stu-id="167b5-195">Calendar that is used for the duration</span></span>

<span data-ttu-id="167b5-196">Nustatyti kalendoriai valdo faktinį bendrąjį gamybos laiką kalendorinėmis dienomis nuo tiekimo užsakymo datos iki paklausos poreikio datos.</span><span class="sxs-lookup"><span data-stu-id="167b5-196">The defined calendars control the actual total lead time in calendar days, from the supply order date to the demand requirement date.</span></span> <span data-ttu-id="167b5-197">Naudojami toliau pateikti kalendoriaus prioritetai.</span><span class="sxs-lookup"><span data-stu-id="167b5-197">The following calendar prioritization is used:</span></span>

- <span data-ttu-id="167b5-198">**Pirkimo gamybos laikas** – atsižvelgiama tik į padengimo grupės kalendorių.</span><span class="sxs-lookup"><span data-stu-id="167b5-198">**Purchase lead time** – Only the coverage group calendar is considered.</span></span>
- <span data-ttu-id="167b5-199">**Gavimo laiko rezervas** – naudojamas padengimo grupės kalendorius, jei jis nustatytas.</span><span class="sxs-lookup"><span data-stu-id="167b5-199">**Receipt margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="167b5-200">Kitu atveju bus naudojamas sandėlio kalendorius.</span><span class="sxs-lookup"><span data-stu-id="167b5-200">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="167b5-201">**Išdavimo laiko rezervas** – naudojamas padengimo grupės kalendorius, jei jis nustatytas.</span><span class="sxs-lookup"><span data-stu-id="167b5-201">**Issue margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="167b5-202">Kitu atveju bus naudojamas sandėlio kalendorius.</span><span class="sxs-lookup"><span data-stu-id="167b5-202">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="167b5-203">**Užsakymo laiko rezervas** – atsižvelgiama tik į padengimo grupės kalendorių.</span><span class="sxs-lookup"><span data-stu-id="167b5-203">**Order margin** – Only the coverage group calendar is considered.</span></span>

#### <a name="calendar-that-is-used-for-the-final-date"></a><span data-ttu-id="167b5-204">Kalendorius, naudojamas galutinei datai</span><span class="sxs-lookup"><span data-stu-id="167b5-204">Calendar that is used for the final date</span></span>

<span data-ttu-id="167b5-205">Toliau pateiktos taisyklės taikomos siekiant nustatyti, ar planavimo mechanizmas gali naudoti nurodytos datos tipo nurodytą datą.</span><span class="sxs-lookup"><span data-stu-id="167b5-205">The following rules are applied to determine whether the planning engine can use a given date for a given date type:</span></span>

- <span data-ttu-id="167b5-206">**Pirkimo gavimo data** – naudojamas tiekėjo kalendorius, jei jis nustatytas.</span><span class="sxs-lookup"><span data-stu-id="167b5-206">**Purchase receipt date** – The vendor calendar is used, if it's defined.</span></span> <span data-ttu-id="167b5-207">Kitu atveju naudojamas padengimo grupės kalendorius, jei jis nustatytas.</span><span class="sxs-lookup"><span data-stu-id="167b5-207">Otherwise, the coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="167b5-208">Jei nei vienas iš šių kalendorių nenustatytas, naudojamas sandėlio kalendorius.</span><span class="sxs-lookup"><span data-stu-id="167b5-208">If neither of those calendars is defined, the warehouse calendar is used.</span></span>
- <span data-ttu-id="167b5-209">**Perkėlimo gavimo data** – naudojamas padengimo grupės kalendorius, jei jis nustatytas.</span><span class="sxs-lookup"><span data-stu-id="167b5-209">**Transfer receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="167b5-210">Kitu atveju bus naudojamas sandėlio kalendorius.</span><span class="sxs-lookup"><span data-stu-id="167b5-210">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="167b5-211">**Gamybos gavimo data** – naudojamas padengimo grupės kalendorius, jei jis nustatytas.</span><span class="sxs-lookup"><span data-stu-id="167b5-211">**Production receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="167b5-212">Kitu atveju bus naudojamas sandėlio kalendorius.</span><span class="sxs-lookup"><span data-stu-id="167b5-212">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="167b5-213">**Poreikio išdavimo atvira data** – naudojamas sandėlio kalendorius, jei jis nustatytas.</span><span class="sxs-lookup"><span data-stu-id="167b5-213">**Demand issue open day** – The warehouse calendar is used, if it's defined.</span></span> <span data-ttu-id="167b5-214">Kitu atveju naudojamas padengimo grupės kalendorius.</span><span class="sxs-lookup"><span data-stu-id="167b5-214">Otherwise, the coverage group calendar is used.</span></span>
- <span data-ttu-id="167b5-215">**Užsakymo atvira data** – naudojamas padengimo grupės kalendoriaus ir tiekėjo kalendoriaus derinys (sankirta).</span><span class="sxs-lookup"><span data-stu-id="167b5-215">**Order open day** – A combination (intersection) of the coverage group calendar and the vendor calendar is used.</span></span> <span data-ttu-id="167b5-216">Abu kalendoriai turi būti atidaryti, kad būtų galima naudoti datą.</span><span class="sxs-lookup"><span data-stu-id="167b5-216">Both calendars must be open to use the date.</span></span> <span data-ttu-id="167b5-217">Jei tik vienas iš šių kalendorių nustatytas, naudojamas tik tas kalendorius.</span><span class="sxs-lookup"><span data-stu-id="167b5-217">If only one of the calendars is defined, that calendar is used alone.</span></span>

#### <a name="calendar-setup-overview-matrix"></a><span data-ttu-id="167b5-218">Kalendoriaus nustatymo peržiūros matrica</span><span class="sxs-lookup"><span data-stu-id="167b5-218">Calendar setup overview matrix</span></span>

<span data-ttu-id="167b5-219">Toliau pateikiamoje iliustracijoje vaizduojama matrica, kurioje apibendrinama, kurie kalendoriai taikomi, kai apskaičiuojami laiko rezervai..</span><span class="sxs-lookup"><span data-stu-id="167b5-219">The following illustration presents a matrix that summarizes which calendars apply when safety margins are calculated.</span></span> <span data-ttu-id="167b5-220">Toliau pateiktos santrumpos ir spalvos naudojamos nurodyti, kur nurodytas kiekvienas kalendoriaus tipas.</span><span class="sxs-lookup"><span data-stu-id="167b5-220">The following abbreviations and colors are used to indicate where each type of calendar is specified:</span></span>

- <span data-ttu-id="167b5-221">**Padengimo grupė (CG):** žalia</span><span class="sxs-lookup"><span data-stu-id="167b5-221">**Coverage group (CG):** Green</span></span>
- <span data-ttu-id="167b5-222">**Sandėlis (WH):** geltona</span><span class="sxs-lookup"><span data-stu-id="167b5-222">**Warehouse (WH):** Yellow</span></span>
- <span data-ttu-id="167b5-223">**Tiekėjas (V):** mėlyna</span><span class="sxs-lookup"><span data-stu-id="167b5-223">**Vendor (V):** Blue</span></span>

![Kalendoriaus nustatymo peržiūros matrica](media/safety-margins-calendar-matrix.png)

## <a name="calculating-delays"></a><span data-ttu-id="167b5-225">Atidėjimų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="167b5-225">Calculating delays</span></span>

<span data-ttu-id="167b5-226">Visi trys laiko rezervai įtraukiami, kai sistema nustato, ar užsakymas atidėtas.</span><span class="sxs-lookup"><span data-stu-id="167b5-226">All three types of safety margins are included when the system determines whether an order is delayed.</span></span>

<span data-ttu-id="167b5-227">Pavyzdžiui, prekės gamybos laikas yra viena diena , o gavimo laiko rezervas yra trys dienos.</span><span class="sxs-lookup"><span data-stu-id="167b5-227">For example, an item has lead time of one day and a receipt margin of three days.</span></span> <span data-ttu-id="167b5-228">Šios prekės pardavimo užsakymas nustatomas taip, kad jis reikalingas šiandien.</span><span class="sxs-lookup"><span data-stu-id="167b5-228">A sales order for this item is set as required today.</span></span> <span data-ttu-id="167b5-229">Šiuo atveju atidėjimas skaičiuojamas kaip *gamybos laikas* + *gavimo laiko rezervas* = keturios dienos.</span><span class="sxs-lookup"><span data-stu-id="167b5-229">In this case, the delay is calculated as *lead time* + *receipt margin* = four days.</span></span> <span data-ttu-id="167b5-230">Todėl, jei šiandien yra rugpjūčio 14 d., keturios atidėjimo dienos nustato pristatymą į rugpjūčio 18 d.</span><span class="sxs-lookup"><span data-stu-id="167b5-230">Therefore, if today is August 14, the four days of delay produces a delivery on August 18.</span></span> <span data-ttu-id="167b5-231">Toliau pateikiamoje iliustracijoje vaizduojamas šis pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="167b5-231">The following illustration shows this example.</span></span>

![Atidėjimo skaičiavimo pavyzdys](media/safety-margins-delays.png)

## <a name="additional-resources"></a><span data-ttu-id="167b5-233">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="167b5-233">Additional resources</span></span>

[<span data-ttu-id="167b5-234">Darbo su planavimo optimizavimu pradžia</span><span class="sxs-lookup"><span data-stu-id="167b5-234">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="167b5-235">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="167b5-235">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
