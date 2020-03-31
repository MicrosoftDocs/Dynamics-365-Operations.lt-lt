---
title: Mažmeninės prekybos pardavimo kuponų nustatymas
description: Šioje temoje apžvelgiami kuponai ir paaiškinama, kaip juos nustatyti.
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4c580e40ae1f0398ab9f8437d42ddcb2979558c3
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057376"
---
# <a name="set-up-coupons-for-retail-sales"></a><span data-ttu-id="ee54f-103">Mažmeninės prekybos pardavimo kuponų nustatymas</span><span class="sxs-lookup"><span data-stu-id="ee54f-103">Set up coupons for retail sales</span></span>

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a><span data-ttu-id="ee54f-104">Kuponų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ee54f-104">Overview of coupons</span></span>

<span data-ttu-id="ee54f-105">Kuponai yra kodai ir brūkšniniai kodai, naudojami suteikti nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="ee54f-105">Coupons are codes and bar codes that are used to add discounts to transactions.</span></span> <span data-ttu-id="ee54f-106">Kiekviename kupone gali būti keli kodai ir kiekvienas kodas gali turėti savo galiojimo datą.</span><span class="sxs-lookup"><span data-stu-id="ee54f-106">Each coupon can have multiple codes, and each code can have its own effective dates.</span></span>

<span data-ttu-id="ee54f-107">Kiekviename kupone yra viena nuolaida.</span><span class="sxs-lookup"><span data-stu-id="ee54f-107">Each coupon is related to one discount.</span></span> <span data-ttu-id="ee54f-108">Su nuolaida susietos kainų grupės apibrėžia klientus, galinčius naudoti kuponą, arba kanalus, kuriuose kuponas galioja.</span><span class="sxs-lookup"><span data-stu-id="ee54f-108">The price groups that are associated with the discount define the customers that can use a coupon or the channels where a coupon is valid.</span></span>

<span data-ttu-id="ee54f-109">Iš esmės kuponai suteikia papildomą nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="ee54f-109">Essentially, coupons are additional validation on top of discounts.</span></span> <span data-ttu-id="ee54f-110">Kupone pateikiami reikiami įprasti ir brūkšniniai kodai bei jų datų intervalai.</span><span class="sxs-lookup"><span data-stu-id="ee54f-110">The coupon provides the coupon codes and bar codes that are required, together with date ranges for those codes.</span></span> <span data-ttu-id="ee54f-111">Kupone taip pat pateikiamos pasirenkamos naudojimo ribos ir klientų reikalaujamos ypatybės.</span><span class="sxs-lookup"><span data-stu-id="ee54f-111">The coupon also provides optional usage limits and customer required properties.</span></span> <span data-ttu-id="ee54f-112">Nuolaida nurodo produktus, kuriems galioja kuponas.</span><span class="sxs-lookup"><span data-stu-id="ee54f-112">The discount provides the set of products that the coupon is valid for.</span></span> <span data-ttu-id="ee54f-113">Nuolaidos kainų grupės nurodo klientus, kanalus ar katalogus, kuriems galioja kuponas.</span><span class="sxs-lookup"><span data-stu-id="ee54f-113">The price groups for the discount provide the set of customers, channels, or catalogs that the coupon is valid for.</span></span>

<span data-ttu-id="ee54f-114">Norint sukurti kuponą, atskirai sukuriami nuolaida ir kuponas.</span><span class="sxs-lookup"><span data-stu-id="ee54f-114">To create a coupon, you create the discount and the coupon separately.</span></span> <span data-ttu-id="ee54f-115">Tada jie susiejami pasirinkus nuolaidą kupono puslapyje „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="ee54f-115">You then link them by selecting the discount on the coupon page in Commerce.</span></span>

> [!NOTE]
> <span data-ttu-id="ee54f-116">Susiejus kuponą su nuolaida, keli nuolaidos puslapyje „Commerce“ esantys laukai tampa tik skaitomais, nes jie priklauso nuo kupono nustatymų.</span><span class="sxs-lookup"><span data-stu-id="ee54f-116">After a coupon is linked to a discount, several fields on the discount page in Commerce become read-only, because they are managed by the coupon's settings.</span></span> <span data-ttu-id="ee54f-117">Šie laukai apima būsenos ir standartinių datų intervalų laukus.</span><span class="sxs-lookup"><span data-stu-id="ee54f-117">These fields include the fields for the status and standard date ranges.</span></span>

### <a name="limited-use-coupons"></a><span data-ttu-id="ee54f-118">Riboto naudojimo kuponai</span><span class="sxs-lookup"><span data-stu-id="ee54f-118">Limited-use coupons</span></span>

<span data-ttu-id="ee54f-119">Kuponus galima sukonfigūruoti kaip riboto naudojimo.</span><span class="sxs-lookup"><span data-stu-id="ee54f-119">Coupons can be configured as limited-use coupons.</span></span> <span data-ttu-id="ee54f-120">Naudojimo limitą galima apibrėžti vienam klientui ar kanalui arba kaip visuotinį limitą.</span><span class="sxs-lookup"><span data-stu-id="ee54f-120">The usage limit can be defined per customer or channel, or as a global limit.</span></span> <span data-ttu-id="ee54f-121">Šis limitas taikomas įprastą ar brūkšninį kodą įvedant ar nuskaitant elektroniniame kasos aparate arba įvedant pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ee54f-121">This limit is enforced when the code or bar code is entered or scanned in POS or during sales order entry.</span></span>

<span data-ttu-id="ee54f-122">Limitas taikomas vienam kupono kodui.</span><span class="sxs-lookup"><span data-stu-id="ee54f-122">The limit is enforced per coupon code on a coupon.</span></span> <span data-ttu-id="ee54f-123">Pavyzdžiui, vienkartinį kuponą su dviem kodais galima naudoti du kartus: kiekvieną kupono kodą po kartą.</span><span class="sxs-lookup"><span data-stu-id="ee54f-123">For example, a single-use coupon that has two coupon codes can be used two times: one time for each coupon code.</span></span> <span data-ttu-id="ee54f-124">Kiekvieną kupono kodą galima nepriklausomai nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="ee54f-124">Each code on a coupon can be independently set to active.</span></span>

> [!NOTE]
> <span data-ttu-id="ee54f-125">Kupono kodui pasiekus savo naudojimo limitą sistema automatiškai *nepakeičia* kupono kodo būsenos į „Panaudotas“.</span><span class="sxs-lookup"><span data-stu-id="ee54f-125">Once a coupon code has reached its usage limit, the system does *not* automatically change the status of the coupon code to "Used".</span></span> <span data-ttu-id="ee54f-126">Tačiau sistema neleidžia toliau naudotis kuponu jam pasiekus naudojimo limitą.</span><span class="sxs-lookup"><span data-stu-id="ee54f-126">The system however, does not allow further usage of a coupon code which has reached its usage limit.</span></span> <span data-ttu-id="ee54f-127">Jei neautomatiškai nustatoma kita kupono kodo būsena išskyrus „Aktyvus“, šio kupono kodo negalima naudoti jokiame kanale.</span><span class="sxs-lookup"><span data-stu-id="ee54f-127">If the status of a coupon code is manually set to anything apart from "Active" then this coupon code cannot be used in any channel.</span></span>

## <a name="managing-coupons"></a><span data-ttu-id="ee54f-128">Kuponų valdymas</span><span class="sxs-lookup"><span data-stu-id="ee54f-128">Managing coupons</span></span>

<span data-ttu-id="ee54f-129">Nuolaidą ir kuponą turite sukurti atskirai.</span><span class="sxs-lookup"><span data-stu-id="ee54f-129">You must create the discount and the coupon separately.</span></span> <span data-ttu-id="ee54f-130">Tada jie susiejami kuponų puslapyje pasirenkant nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="ee54f-130">You then link them by selecting the discount on the coupon page.</span></span> <span data-ttu-id="ee54f-131">Kuponą susiejus su nuolaida, keli nuolaidos laukai tampa galimi tik skaityti, nes juos valdo kupono parametrai.</span><span class="sxs-lookup"><span data-stu-id="ee54f-131">After you link a coupon to a discount, several fields for the discount become read-only, because they are managed by the coupon's settings.</span></span> <span data-ttu-id="ee54f-132">Šie laukai apima būsenos ir standartinių datų intervalų laukus.</span><span class="sxs-lookup"><span data-stu-id="ee54f-132">These fields include the fields for the status and standard date ranges.</span></span>

<span data-ttu-id="ee54f-133">Iš esmės kuponai dabar suteikia papildomą nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="ee54f-133">Essentially, coupons are now additional validation on top of discounts.</span></span> <span data-ttu-id="ee54f-134">Kupone pateikiami įprasti ir brūkšniniai kodai bei jų datų intervalai, naudojimo limitai ir kliento reikalaujama ypatybė.</span><span class="sxs-lookup"><span data-stu-id="ee54f-134">The coupon provides the coupon codes and bar codes, together with date ranges, the usage limits, and the customer required property.</span></span> <span data-ttu-id="ee54f-135">Nuolaida nurodo produktus, kuriems galioja kuponas.</span><span class="sxs-lookup"><span data-stu-id="ee54f-135">The discount provides the set of products that the coupon is valid for.</span></span> <span data-ttu-id="ee54f-136">Nuolaidos kainų grupės nurodo klientus, kanalus ar katalogus, kuriems galioja kuponas.</span><span class="sxs-lookup"><span data-stu-id="ee54f-136">The discount's price groups provide the set of customers, channels, or catalogs that the coupon is valid for.</span></span>

## <a name="system-setup-for-coupons"></a><span data-ttu-id="ee54f-137">Kuponų sistemos sąranka</span><span class="sxs-lookup"><span data-stu-id="ee54f-137">System setup for coupons</span></span>

<span data-ttu-id="ee54f-138">Nustatyti kuponą galite tik nustatę kupono brūkšninį kodą ir dvi kupono numeracijas.</span><span class="sxs-lookup"><span data-stu-id="ee54f-138">Before you can set up a coupon, you must set up the coupon bar code and two coupon number sequences.</span></span>

1. <span data-ttu-id="ee54f-139">Puslapyje **Skaičių sekos simboliai** sukurkite naują kupono kodo skaičių sekos simbolį.</span><span class="sxs-lookup"><span data-stu-id="ee54f-139">On the **Mask characters** page, create a new mask character for the coupon code.</span></span> <span data-ttu-id="ee54f-140">Galite pasirinkti bet kokį nepanaudotą simbolį.</span><span class="sxs-lookup"><span data-stu-id="ee54f-140">You can select any unused character.</span></span>
2. <span data-ttu-id="ee54f-141">Puslapyje **Brūkšninių kodų skaičių sekų sąranka** sukurkite naują brūkšninio kodo skaičių seką.</span><span class="sxs-lookup"><span data-stu-id="ee54f-141">On the **Bar code mask setup** page, create a new bar code mask.</span></span> <span data-ttu-id="ee54f-142">Lauką **Tipas** nustatykite kaip **Kuponas**.</span><span class="sxs-lookup"><span data-stu-id="ee54f-142">Set the **Type** field to **Coupon**.</span></span>
3. <span data-ttu-id="ee54f-143">Puslapyje **Brūkšninių kodų sąranka** sukurkite naują brūkšninį kodą, kuris naudoja jūsų ką tik sukurtą brūkšninio kodo skaičių seką.</span><span class="sxs-lookup"><span data-stu-id="ee54f-143">On the **Bar code setup** page, create a new bar code that uses the bar code mask that you just created.</span></span>
4. <span data-ttu-id="ee54f-144">Puslapyje **Numeracijos** sukurkite dvi naujas numeracijas.</span><span class="sxs-lookup"><span data-stu-id="ee54f-144">On the **Number sequences** page, create two new number sequences.</span></span> <span data-ttu-id="ee54f-145">Viena numeracija skirta kupono kodo ID, o kita – kupono numeriui.</span><span class="sxs-lookup"><span data-stu-id="ee54f-145">One sequence is for the coupon code ID, and the other sequence is for the coupon number.</span></span> <span data-ttu-id="ee54f-146">Kupono kodo ID yra unikalusis kiekvieno kupono kodo identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="ee54f-146">The coupon code ID is the unique identifier for each coupon code for a coupon.</span></span> <span data-ttu-id="ee54f-147">Kupono numeris yra unikalusis kupono identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="ee54f-147">The coupon number is the unique identifier for a coupon.</span></span> <span data-ttu-id="ee54f-148">Kiekviename kupone gali būti keli įprasti ir brūkšniniai kodai, suaktyvinantys kuponą.</span><span class="sxs-lookup"><span data-stu-id="ee54f-148">Each coupon can have multiple codes and bar codes that trigger the coupon.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ee54f-149">Abiejų numeracijų lauką **Aprėptis** turite nustatyti kaip **Įmonė**.</span><span class="sxs-lookup"><span data-stu-id="ee54f-149">For both number sequences, you must set the **Scope** field to **Company**.</span></span> <span data-ttu-id="ee54f-150">Daugeliu atvejų abi numeracijas turėtumėte generuoti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="ee54f-150">In most cases, you should automatically generate both sequence numbers.</span></span>

5. <span data-ttu-id="ee54f-151">Puslapio **„Commerce“ parametrai** skirtuke **Brūkšniniai kodai** pasirinkite brūkšninį kodą, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="ee54f-151">On the **Commerce parameters** page, on the **Bar codes** tab, select the bar code that you created earlier.</span></span>
6. <span data-ttu-id="ee54f-152">Puslapio **Bendri „Commerce“ parametrai** skirtuke **Skaičių sekos** pasirinkite skaičių sekas, kurias sukūrėte kupono numeriui ir kupono kodo ID.</span><span class="sxs-lookup"><span data-stu-id="ee54f-152">On the **Commerce shared parameters** page, on the **Number sequences** tab, select the number sequences that you created for the coupon number and coupon code ID.</span></span>
7. <span data-ttu-id="ee54f-153">Dabar galite atidaryti puslapį **Kuponai** ir kurti naujus kuponus.</span><span class="sxs-lookup"><span data-stu-id="ee54f-153">You can now open the **Coupons** page and create new coupons.</span></span>

## <a name="the-effect-of-partial-updates-on-coupons"></a><span data-ttu-id="ee54f-154">Kas nutinka kuponus atnaujinus iš dalies</span><span class="sxs-lookup"><span data-stu-id="ee54f-154">The effect of partial updates on coupons</span></span>

<span data-ttu-id="ee54f-155">Kuponų funkcijos apima kelias atskiras funkcijas.</span><span class="sxs-lookup"><span data-stu-id="ee54f-155">Coupon functionality comprises multiple distinct features.</span></span> <span data-ttu-id="ee54f-156">„Commerce“ būstinė (angl. HQ) ir kanalas gali būti iš dalies atnaujinami pagal komponentus.</span><span class="sxs-lookup"><span data-stu-id="ee54f-156">Commerce Headquarters (HQ) and the channel can be partially updated across components.</span></span> <span data-ttu-id="ee54f-157">Todėl svarbu suprasti, kas nutinka iš dalies atnaujinus visas kuponų funkcijas.</span><span class="sxs-lookup"><span data-stu-id="ee54f-157">Therefore, it's important that you understand how partial updates affect coupon functionality as a whole.</span></span>

- <span data-ttu-id="ee54f-158">**Būstinė yra iš dalies atnaujinama, tačiau „Commerce Scale Unit“ ir EKA nėra atnaujinami.**</span><span class="sxs-lookup"><span data-stu-id="ee54f-158">**HQ is partially updated, but Commerce Scale Unit and POS aren't updated.**</span></span> <span data-ttu-id="ee54f-159">Atnaujinant būstinę, atnaujinami kuponų ir nuolaidų puslapiai, taip pat atnaujinamas „Commerce“ kainų mechanizmas.</span><span class="sxs-lookup"><span data-stu-id="ee54f-159">In an HQ update, the coupon and discount pages are updated, and the commerce price engine is also updated.</span></span> <span data-ttu-id="ee54f-160">Jei atnaujinamas tik vienas iš šių dviejų komponentų, kai kurie „Commerce“ puslapiai neatitiks kainos apskaičiavimo duomenų.</span><span class="sxs-lookup"><span data-stu-id="ee54f-160">If only one of those two components is updated, some pages in Commerce won't match the price calculation data.</span></span> <span data-ttu-id="ee54f-161">Todėl skaičiuojant nuolaidas galima gauti netikėtų rezultatų arba gali įvykti klaidų.</span><span class="sxs-lookup"><span data-stu-id="ee54f-161">Therefore, unexpected discount calculations or errors might occur during discount calculations.</span></span>
- <span data-ttu-id="ee54f-162">**Būstinė yra iš dalies atnaujinama, tačiau „Commerce Scale Unit“ ir EKA nėra atnaujinami (N-1).**</span><span class="sxs-lookup"><span data-stu-id="ee54f-162">**HQ is updated, but Commerce Scale Unit and POS aren't updated (N-1).**</span></span> <span data-ttu-id="ee54f-163">Kadangi ne visas parduotuves galima atnaujinti tuo pačiu metu, prieš atnaujindami parduotuves rekomenduojame atnaujinti būstinę.</span><span class="sxs-lookup"><span data-stu-id="ee54f-163">Because not all stores can be updated at the same time, we recommend that you update HQ before you update stores.</span></span> <span data-ttu-id="ee54f-164">Scenarijuje N-1 naujų su kuponais susijusių funkcijų nebus galima naudoti dar neatnaujintose parduotuvėse.</span><span class="sxs-lookup"><span data-stu-id="ee54f-164">In the N-1 scenario, new functionality that is related to coupons won't be available in stores that haven't been updated yet.</span></span> <span data-ttu-id="ee54f-165">Pavyzdžiui, kuponų funkcijos pradeda naudoti „neįtraukimo“ eilutes.</span><span class="sxs-lookup"><span data-stu-id="ee54f-165">For example, the coupon functionality introduces "exclude" lines.</span></span> <span data-ttu-id="ee54f-166">Jei naudodami nuolaidą pašalinsite eilutes, jos nebus pritaikytos parduotuvėje, kurioje veikia senesnė versija.</span><span class="sxs-lookup"><span data-stu-id="ee54f-166">If you use exclude lines on a discount, they won't be applied in a store that is running an earlier version.</span></span>
- <span data-ttu-id="ee54f-167">**Būstinė nėra atnaujinama, tačiau „Commerce Scale Unit“ ir EKA yra atnaujinami (N+1).**</span><span class="sxs-lookup"><span data-stu-id="ee54f-167">**HQ isn't updated, but Commerce Scale Unit and POS are updated (N+1).**</span></span> <span data-ttu-id="ee54f-168">Kadangi atnaujintas „Commerce Scale Unit“ kainų mechanizmas gali apskaičiuoti kainą seniems nuolaidų kodams, atnaujinimas tam neturėtų daryti jokios įtakos.</span><span class="sxs-lookup"><span data-stu-id="ee54f-168">Because the updated price engine in Commerce Scale Unit can handle legacy discount codes during price calculations, the update should have no functional impact in this scenario.</span></span>