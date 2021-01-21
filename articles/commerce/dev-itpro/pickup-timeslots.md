---
title: Kurti ir naujinti laiko vietas kliento atsiėmimui
description: Šioje temoje aprašoma, kaip kurti, konfigūruoti ir naujinti kliento paėimimo laikų vietas „Commerce“ štabe.
author: anupamar-ms
manager: AnnBe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: f86eb47ec64dff230223ed0ecbe792373aca649f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681547"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a><span data-ttu-id="e6e19-103">Kurti ir naujinti laiko vietas kliento atsiėmimui</span><span class="sxs-lookup"><span data-stu-id="e6e19-103">Create and update time slots for customer pickup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6e19-104">Šioje temoje aprašoma, kaip kurti, konfigūruoti ir naujinti kliento paėimimo laikų vietas „Commerce“ štabe.</span><span class="sxs-lookup"><span data-stu-id="e6e19-104">This topic describes how to create, configure, and update customer pickup time slots in Commerce headquarters.</span></span>

<span data-ttu-id="e6e19-105">Laiko vietos funkcija suteikia mažmeniniams prekybininkams būdą nustatyti laiko vietas prekėms, kurios paėmimo pristatymo būdas yra įjungtas.</span><span class="sxs-lookup"><span data-stu-id="e6e19-105">The time slot feature gives retailers a way to define a time slot for items that the customer pickup delivery mode is turned on for.</span></span> <span data-ttu-id="e6e19-106">Laiko vietos leidžia mažmeniniams prekybininkams nustatyti dienas ir laikus, kai užsakymai gali būti paimami iš parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="e6e19-106">Time slots let retailers define the days and times when orders can be picked up from a store.</span></span> <span data-ttu-id="e6e19-107">Mažmeniniai prekeiviai taip pat gali nustatytoi užsakymų skaičius, kurie gali būti paimti per tam tikrą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="e6e19-107">Retailers can also define the number of orders that can be picked up during a given period.</span></span> <span data-ttu-id="e6e19-108">Tokiu būdu, mažmeniani prekeiviai gali apriboti užsakymų skaičių, kurį galima atsiimti per tam skirtą dieną ir tam skirtu laiku.</span><span class="sxs-lookup"><span data-stu-id="e6e19-108">In this way, retailers can limit the number of orders that can be picked up on a given day and at a given time.</span></span> <span data-ttu-id="e6e19-109">Rezultatai yra geros kokybės patirtis jų klientams.</span><span class="sxs-lookup"><span data-stu-id="e6e19-109">The result is a better-quality experience for their customers.</span></span>

> [!NOTE]
> <span data-ttu-id="e6e19-110">Laiko vietos funkcija yra prieinama „Microsoft Dynamics 365 Commerce“ versija 10.0.15 ir vėlesnė.</span><span class="sxs-lookup"><span data-stu-id="e6e19-110">The time slot feature is available in Microsoft Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="e6e19-111">Tolesnis paveikslėlis rodo laiko vietos pavyzdžio pasirinkimą e-komercijos išregistravimo metu.</span><span class="sxs-lookup"><span data-stu-id="e6e19-111">The following illustration shows an example of time slot selection during e-commerce checkout.</span></span>

![Laiko vietos pasirinkimo pavyzdys e-komercijos išsiregistravimo metu](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a><span data-ttu-id="e6e19-113">Laiko vietos ypatybės</span><span class="sxs-lookup"><span data-stu-id="e6e19-113">Time slot properties</span></span>

<span data-ttu-id="e6e19-114">Laiko vieta yra konkretus intervalas, kai klientas gali pasirinkti, ar atsiimti užsakymą iš konrkečios parduotuvės ar vietos.</span><span class="sxs-lookup"><span data-stu-id="e6e19-114">A time slot is a specific interval when a customer can choose to pick up an order from a specific store or location.</span></span> <span data-ttu-id="e6e19-115">Laiko vietos valdymo funkcija yra prieinama tik kai kliento atsiėmimo pristatymo būdas sukonfigūruotas „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="e6e19-115">The time slot management feature is available only when the customer pickup delivery mode is configured in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e6e19-116">Laiko vieta yra nustatyta naudojant tolesnes ypatybes:</span><span class="sxs-lookup"><span data-stu-id="e6e19-116">A time slot is defined by using the following properties:</span></span>

- <span data-ttu-id="e6e19-117">**Pristatymo būdas** – Nurodykite pristatymo atsiėmimo būdą, kai taikoma laiko vieta.</span><span class="sxs-lookup"><span data-stu-id="e6e19-117">**Mode of delivery** – Specify the pickup mode of delivery that the time slot applies to.</span></span>
- <span data-ttu-id="e6e19-118">**Mažiausia dienų** ir **Daugiausia dienų** – Nurodo anksčiausias ir vėliausias datas, kurias galima pasirinkti pasiėmimo metu pagal datą, kai užsakymas yra padarytas.</span><span class="sxs-lookup"><span data-stu-id="e6e19-118">**Minimum Days** and **Maximum Days** – Specify the earliest and latest dates that can be selected for pickup relative to the date when the order is placed.</span></span> 

    <span data-ttu-id="e6e19-119">**Mažiausia dienų** ypatybė užtikrina, kad yra pakankamai laiko mažmeniniam prekeiviui siekiant apdoroti užsakymą prieš tai, kai jis yra parengtas atsiėmimui.</span><span class="sxs-lookup"><span data-stu-id="e6e19-119">The **Minimum Days** property ensures that there is enough time for the retailer to process the order before it's ready for pickup.</span></span> <span data-ttu-id="e6e19-120">Ypatybė **Daugiausia dienų** užtikrina, kad vartotojas negalėtų pasirinkti datos, kuri yra toli ateityje.</span><span class="sxs-lookup"><span data-stu-id="e6e19-120">The **Maximum Days** property ensures that the user can't select a date that is too far in the future.</span></span> <span data-ttu-id="e6e19-121">Pavyzdžiui, jei minimali vertė yra nustatyta į **1**, o užsakymas yra padarytas rugsėjo 20 dieną, anksčiausią dieną, kai užsakymas bus prieinamas atsiėmimui kitą galiojančią dieną (rugsėjo 21 d.).</span><span class="sxs-lookup"><span data-stu-id="e6e19-121">For example, if the minimum value is set to **1**, and an order is placed on September 20, the earliest day that the order will be available for pickup is the next eligible day (September 21).</span></span> <span data-ttu-id="e6e19-122">Panašiu būdu, maksimalios vertės nustatymui, galite nustatyti maksimalų dienų skaičių, per kurį galima atsiimti užsakymą.</span><span class="sxs-lookup"><span data-stu-id="e6e19-122">In a similar way, by setting a maximum value, you can define the maximum number of days that an order can be picked up.</span></span> <span data-ttu-id="e6e19-123">Kai minimalios ir maksimalios vertės yra nustatytos, svetainės vartotojai gali matyti ar pasirinkti tik konkretų dienų rinkinį jų išsiregistravimo patirtyje.</span><span class="sxs-lookup"><span data-stu-id="e6e19-123">When minimum and maximum values are defined, site users can see and select only a specific set of days during their checkout experience.</span></span>

    <span data-ttu-id="e6e19-124">Galite nustatyti minimalią vertę iki dešimtainės, kuri yra mažesnė nei 1.</span><span class="sxs-lookup"><span data-stu-id="e6e19-124">You can set the minimum value to a decimal value that is less than 1.</span></span> <span data-ttu-id="e6e19-125">Pavyzdžiui, jei atsiėmimas yra prieinamas keturias valandas po to, kai užsakymas yra padarytas, nustatykite minimalią vertę į **0,17** (= 4 ÷ 24, suapvalinta iki dviejų dešimtainių vietų).</span><span class="sxs-lookup"><span data-stu-id="e6e19-125">For example, if pickup is available four hours after an order is placed, set the minimum value to **0.17** (= 4 ÷ 24, rounded up to two decimal places).</span></span> <span data-ttu-id="e6e19-126">Nepaisant to, jei nustatote minimalią vertę iki dešimtainės vertės, kuri yra daugiau nei 1, ji visuomet suapvalinta iki artimiausio sveiko skaičiaus (didesnio ar mažesnio).</span><span class="sxs-lookup"><span data-stu-id="e6e19-126">However, if you set the minimum value to a decimal value that is more than 1, it's always rounded to the nearest whole number (up or down).</span></span>

    <span data-ttu-id="e6e19-127">Jei nustatote maksimalią vertę iki dešimtainės vertės, ji visada apvalinama.</span><span class="sxs-lookup"><span data-stu-id="e6e19-127">If you set the maximum value to a decimal value, it's always rounded up.</span></span> <span data-ttu-id="e6e19-128">Pavyzdžiui, vertė **1,2** bus suapvalinta iki **2**.</span><span class="sxs-lookup"><span data-stu-id="e6e19-128">For example, a value of **1.2** will be rounded up to **2**.</span></span>

- <span data-ttu-id="e6e19-129">**Pradžios data** ir **Pabaigos data** – Nurodykite pradžios ir pabaigos datas laiko vietai.</span><span class="sxs-lookup"><span data-stu-id="e6e19-129">**Start Date** and **End Date** – Specify the start and end dates of the time slot.</span></span> <span data-ttu-id="e6e19-130">Kas kartą kai laiko vietos įrašas turi pradžios ir pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="e6e19-130">Each time slot entry has a start date and an end date.</span></span> <span data-ttu-id="e6e19-131">Dėl to, galite būti lankstūrs ir įtraukti kitą laiko vietą per metus (pavyzdžiui, paėmimui per atostogų valandas).</span><span class="sxs-lookup"><span data-stu-id="e6e19-131">Therefore, you have the flexibility to add different time slots throughout the year (for example, pickups during holiday hours).</span></span> <span data-ttu-id="e6e19-132">Jei laiko vietos pradžios ir datos yra keičiamos padarius užsakymą, pakeitimai nebus taikomi tam užsakymui.</span><span class="sxs-lookup"><span data-stu-id="e6e19-132">If a time slot's start and dates are changed after an order is placed, the changes won't apply to that order.</span></span> <span data-ttu-id="e6e19-133">Jums nustatčius pradžios ir pabaigos datas, turite apgalvoti parduotuvės užsidarymo datas (pavyzdžiui, Kalėdų dieną) ir įsitikinti, kad laiko vietos nėra nustatytos tomis dienomis.</span><span class="sxs-lookup"><span data-stu-id="e6e19-133">When you define start and end dates, you must consider store closure dates (for example, Christmas day) and ensure that time slots aren't defined for those days.</span></span>
- <span data-ttu-id="e6e19-134">**Veikiančios pristatymo valandos** – Nurodykite laikotarpį, kai leidžiamas paėmimas.</span><span class="sxs-lookup"><span data-stu-id="e6e19-134">**Active Hours of Delivery** – Specify the period when pickup is allowed.</span></span> <span data-ttu-id="e6e19-135">Pavyzdžiui, paėmimo laikai gali būti nuo 14:00 iki 17:00 kas dieną.</span><span class="sxs-lookup"><span data-stu-id="e6e19-135">For example, the pickup times might be between 2 PM and 5 PM every day.</span></span> <span data-ttu-id="e6e19-136">Ši ypatybė leidžia atsiėmimo laikus, kurie priklauso nuo parduotuvės valandų.</span><span class="sxs-lookup"><span data-stu-id="e6e19-136">This property enables the pickup times to be independent of store hours.</span></span> <span data-ttu-id="e6e19-137">Dėl to, pardavėjas gali konfigūruoti atsiėmimo laikus, kurie atitinka jo konkrečius įmonės reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="e6e19-137">Therefore, the retailer can configure pickup times that meet its specific business requirements.</span></span> <span data-ttu-id="e6e19-138">Jums nustačius veikiančias atsiėmimo valandas, privaltoe apgalvoti parduotuvės valandas ir užtikrinti, kad atsiėmimo laikai nėra nustatyti laiku, kai parduotuvė užverta.</span><span class="sxs-lookup"><span data-stu-id="e6e19-138">When you define the active hours of pickup, you must consider store hours and ensure that pickup times aren't defined for times when the store is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e6e19-139">Atsiėmimo parduotuvėje valandos turi būti nustatytos parduotuvę atitinkančioje laiko zonoje.</span><span class="sxs-lookup"><span data-stu-id="e6e19-139">The hours for store pickup must be defined in the time zone of the appropriate store.</span></span>

- <span data-ttu-id="e6e19-140">**Laiko vietos intervalas** – Nurodykite laiką, kuris gali būti priskirtas kiekvienai laiko vietai.</span><span class="sxs-lookup"><span data-stu-id="e6e19-140">**Time Slot Interval** – Specify the duration that can be allotted to each time slot.</span></span> <span data-ttu-id="e6e19-141">Pavyzdžiui, kiekvienos laiko vietos trukmė gali būti didėjanti 15, 30 minučių ar viena valanda.</span><span class="sxs-lookup"><span data-stu-id="e6e19-141">For example, the duration of each time slot might be in increments of 15 minutes, 30 minutes, or one hour.</span></span>
- <span data-ttu-id="e6e19-142">**Vietos vienam intervalui** – Nurodykite klientų ar užsakymų skaičių, kuris gali būti aptarnautas atsiėmimo metu per kiekvieną laiko intervalą.</span><span class="sxs-lookup"><span data-stu-id="e6e19-142">**Slots Per Interval** – Specify the number of customer or orders that can be served for pickup during each time slot interval.</span></span> <span data-ttu-id="e6e19-143">Pavyzdžiui, įveskite **1**, **2**, **3** ar bet kokį kitą sveiką skaičių.</span><span class="sxs-lookup"><span data-stu-id="e6e19-143">For example, enter **1**, **2**, **3**, or any other whole number.</span></span>
- <span data-ttu-id="e6e19-144">**Aktyvios dienos** – Nurodykite savaitės dienas, kai atsiėmimo laiko vieta yra veikianti.</span><span class="sxs-lookup"><span data-stu-id="e6e19-144">**Active Days** – Specify the days of the week when the pickup time slots are active.</span></span> <span data-ttu-id="e6e19-145">Ši ypatybė leidžia prekeiviui nustatyti dienas, kai jis nori palaikyti atsiėmimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="e6e19-145">This property lets the retailer define the days when it wants to support pickup orders.</span></span>
- <span data-ttu-id="e6e19-146">**Mažmeniniai kanalai** – Nurodyktie mažmeninius kanalus.</span><span class="sxs-lookup"><span data-stu-id="e6e19-146">**Retail Channels** – Specify the retail channels.</span></span> <span data-ttu-id="e6e19-147">Visos laiko vietos gali būti susietos su viena ar keliomis mažmenos parduotuvėmis.</span><span class="sxs-lookup"><span data-stu-id="e6e19-147">Each time slot can be associated with one or more retail stores.</span></span> <span data-ttu-id="e6e19-148">Priklausomai nuo kiekvienos parduotuvės darbo valandų, vienas ar daugiau laiko vietų gali būti sukurti ir susieti su kanalu.</span><span class="sxs-lookup"><span data-stu-id="e6e19-148">Depending on each store's hours of operation, one or more time slot entries can be created and associated with a channel.</span></span> 

<!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

<span data-ttu-id="e6e19-149">Tik vienas laiko vietos šablonas gali būti konfigūruojamas kanalui.</span><span class="sxs-lookup"><span data-stu-id="e6e19-149">Only one time slot template can be configured per channel.</span></span> <span data-ttu-id="e6e19-150">Šie kanalai apima fizines parduotuves, skambučių centrus, mobiliuosius įrenginius ir el. prekybos svetaines.</span><span class="sxs-lookup"><span data-stu-id="e6e19-150">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a><span data-ttu-id="e6e19-151">Konfigūruokite laiko vietos funkciją „Commerce“ štabe</span><span class="sxs-lookup"><span data-stu-id="e6e19-151">Configure the time slot feature in Commerce headquarters</span></span>

<span data-ttu-id="e6e19-152">Laiko vietos turi būti nustatytos kiekvienam atsiėmimo pristatymo būdui „Commerce“ štabe taip, kad pardavimo taškas ir e-komercijos kanalai į juos rodytų.</span><span class="sxs-lookup"><span data-stu-id="e6e19-152">Time slots must be defined for each pickup mode of delivery in Commerce headquarters, so that point of sale (POS) and e-commerce channels can reference them.</span></span>

- <span data-ttu-id="e6e19-153">Tik vienas laiko tarpo šablonas gali būti susietas su kiekviena parduotuve ar kanalu.</span><span class="sxs-lookup"><span data-stu-id="e6e19-153">Only one time slot template can be associated with each store or channel.</span></span>
- <span data-ttu-id="e6e19-154">Kiekviena laiko vieta, kuri yra sukurta, turi būti unikali kiekvienam pristatymo būdui kiekviename šablone.</span><span class="sxs-lookup"><span data-stu-id="e6e19-154">Each time slot that is created should be unique to each delivery mode in each template.</span></span>
- <span data-ttu-id="e6e19-155">Po to, kai laiko vietos funkcija sukonfigūruota, laiko vietos kalendorius bus prieinamas pasirinktoms parduotuvėms ar jų grupėms.</span><span class="sxs-lookup"><span data-stu-id="e6e19-155">After the time slot feature is configured, the time slot calendar will be available to the selected stores or store groups.</span></span> <span data-ttu-id="e6e19-156">Jis taip pat matomas POS nuorodai.</span><span class="sxs-lookup"><span data-stu-id="e6e19-156">It will also be visible at the POS, for reference.</span></span>

<span data-ttu-id="e6e19-157">Norėdami konfigūruoti laiko vietos funkciją „Commerce“ štabe, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="e6e19-157">To configure the time slot feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e6e19-158">Eikite į **„Commerce“** \> **Kanalo nustatymai** \> **Atsiėmimo parduotuvėje laiko vieta**.</span><span class="sxs-lookup"><span data-stu-id="e6e19-158">Go to **Commerce** \> **Channel setup** \> **Store pickup time slot**.</span></span>
1. <span data-ttu-id="e6e19-159">Rinkitės **Naujas** tam, kad sukurtumėte naują laiko vietos šabloną.</span><span class="sxs-lookup"><span data-stu-id="e6e19-159">Select **New** to create a new time slot template.</span></span> <span data-ttu-id="e6e19-160">Norėdami naudoti esamą šabloną, pasirinkite šabloną kairiojoje srityje.</span><span class="sxs-lookup"><span data-stu-id="e6e19-160">To use an existing template, select the template in the left pane.</span></span>
1. <span data-ttu-id="e6e19-161">Įverskite vertes  **Laiko vietos ID** ir **Aprašo** laukelius.</span><span class="sxs-lookup"><span data-stu-id="e6e19-161">Enter values in the **Time Slot ID** and **Description** fields.</span></span>
1. <span data-ttu-id="e6e19-162">„FastTab“**Užsakymo atsiėmimas - Laiko nustatymai** rinkitės **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="e6e19-162">On the **Order Pickup - Time Settings** FastTab, select **Add**.</span></span>
1. <span data-ttu-id="e6e19-163">Teksto laukelyje **Užsakymo atsiėmimas - Laiko nustatymai** nustatykite datos intervalą, pristatymo būdą, veikiančias pristatymo valandas, veikiančias dienas, laiko vietos intervalą, vietas vienam intervalui ir kitus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="e6e19-163">In the **Order Pickup - Time Settings** dialog box, define the date range, mode of delivery, active hours of delivery, active days, time slot interval, slots per interval, and other settings.</span></span>

    <span data-ttu-id="e6e19-164">Jei laiko vietos bus statinės numatytai ateičiai, palikite **Pabaigos data** laukelį tuščią.</span><span class="sxs-lookup"><span data-stu-id="e6e19-164">If time slots will be static for the foreseeable future, leave the **End Date** field blank.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e6e19-165">Galite sukurti keletą šablonų, tačiau tik vienas gali būti susietas su vienu kanalu ar parduotuve.</span><span class="sxs-lookup"><span data-stu-id="e6e19-165">You can create multiple templates, but only one template can be associated with a single channel or store.</span></span>

    ![Užsakymo atsiėmimas - Laiko nustatymų teksto laukelis](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. <span data-ttu-id="e6e19-167">Pabaigus, rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e6e19-167">When you've finished, select **OK**.</span></span>
1. <span data-ttu-id="e6e19-168">Jei laiko vietos per dieną gali skirtis, sukurkite papildomus įrašus **Užsakymo atsiėmimas - Laiko nustatymai** „FastTab“ tam, kad užtikrintumėte, jog datos ir laikai nepersidengtų.</span><span class="sxs-lookup"><span data-stu-id="e6e19-168">If the time slots in a day will vary, create additional entries on the **Order Pickup - Time Settings** FastTab to ensure that the dates and times don't overlap.</span></span>
1. <span data-ttu-id="e6e19-169">„FastTab“ **Prekybos kanalai** rinkitės **Įtraukti** tam, kad susietumėte laiko vietos šabloną su parduotuvėmis ar kanalais, kuriuose jie bus naudojami.</span><span class="sxs-lookup"><span data-stu-id="e6e19-169">On the **Retail Channels** FastTab, select **Add** to associate the time slot template with the stores or channels where it will be used.</span></span>
1. <span data-ttu-id="e6e19-170">Teksto laukelyje **Rinktis organizacijos mazgus** naudokite rodyklių mygtukus, kad pasirinktumėte (ar panaikintumėte pasirinktas) parduotuves, regionus ir organizacijas, su kuriomis šablonas bus susietas.</span><span class="sxs-lookup"><span data-stu-id="e6e19-170">In the **Choose organization nodes** dialog box, use the arrow buttons to select (or clear the selection of) the stores, regions, and organizations that the template should be associated with.</span></span>

    <!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. <span data-ttu-id="e6e19-171">Pabaigus, rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e6e19-171">When you've finished, select **OK**.</span></span>
1. <span data-ttu-id="e6e19-172">Puslapyje **Paskirstymo grafikas** vykdykite **1070** ir **1135** darbus taip, kad sinchronizuotumėte datą su kanalais.</span><span class="sxs-lookup"><span data-stu-id="e6e19-172">On the **Distribution schedule** page, run the **1070** and **1135** jobs to sync the data to the channels.</span></span>

## <a name="time-slot-selection-for-pos-orders"></a><span data-ttu-id="e6e19-173">Laiko vietos pasirinkimas POS užsakymams</span><span class="sxs-lookup"><span data-stu-id="e6e19-173">Time slot selection for POS orders</span></span>

<span data-ttu-id="e6e19-174">POS, užsakymą ar užsakymo eilutę nustačius atsiėmimui, kasininkas gali pasirinkti atsiėmimą parduotuvėje ar vietoje ir laiką bei laiko vietą.</span><span class="sxs-lookup"><span data-stu-id="e6e19-174">At the POS, when an order or order line is identified for pickup, the cashier can select the pickup store or location, and a date and time slot.</span></span> <span data-ttu-id="e6e19-175">Jei klientas turi kitos parduotuvės paėmimo užsakymą, kasininkas gali pasirinkti datas, kada toje parduotuvėje bus galima paimti prekes.</span><span class="sxs-lookup"><span data-stu-id="e6e19-175">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="e6e19-176">Parduotuvių peržvalgoje bus pateikta nuoroda į datas ir parduotuvių darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="e6e19-176">The store lookup will provide a reference to the dates and store times.</span></span>

<span data-ttu-id="e6e19-177">Tolesnis paveikslėlis rodo laiko vietos pavyzdžio pasirinkimą POS užsakymui.</span><span class="sxs-lookup"><span data-stu-id="e6e19-177">The following illustration shows an example of time slot selection for a POS order.</span></span>

![Laiko vietos pasirinkimo pavyzdys POS užsakymui](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a><span data-ttu-id="e6e19-179">Laiko vietos pasirinkimas e-komercijos užsakymams</span><span class="sxs-lookup"><span data-stu-id="e6e19-179">Time slot selection for e-commerce orders</span></span>

<span data-ttu-id="e6e19-180">Dėl informacijos, kaip padaryti laiko vietos pasirinkimą prieinamą e-komercijos užsakymams, žr. [Atsiėmimo informacijos modulis](../pickup-info-module.md).</span><span class="sxs-lookup"><span data-stu-id="e6e19-180">For information about how to make time slot selection available for e-commerce orders, see [Pickup information module](../pickup-info-module.md).</span></span>

> [!NOTE]
> <span data-ttu-id="e6e19-181">Vartotojai gali peržiūrėti ar redaguoti atsiėmimo laiko vietas „Commerce“ svetainės išsiregistravimo puslapyje tik, jei atsiėmimo informacijos modulis buvo įtrauktas į tą puslapį.</span><span class="sxs-lookup"><span data-stu-id="e6e19-181">Users can view or edit pickup time slots on a Commerce site's checkout page only if the pickup information module has been added to that page.</span></span> <span data-ttu-id="e6e19-182">Jei išsiregistravimo puslapis neapima atsiėmimo informacijso modulio, užsakymai bus padaromi neleidžiant vartotojams nurodyti ar peržiūrėti laiko vietos informacijos.</span><span class="sxs-lookup"><span data-stu-id="e6e19-182">If the checkout page doesn't include the pickup information module, orders will be placed without letting users specify or view time slot information.</span></span>

<span data-ttu-id="e6e19-183">Tolesnis paveikslėlis rodo laiko vietos pavyzdžio pasirinkimą e-komercijos užsakymui, kai atsiėmimo laiko vieta buvo pasirinkta.</span><span class="sxs-lookup"><span data-stu-id="e6e19-183">The following illustration shows an example of an e-commerce order where a pickup time slot has been selected.</span></span>

![E-komercijos užsakymo pavyzdys atsiėmimo laiko vietai buvo pasirinktas](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="e6e19-185">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e6e19-185">Additional resources</span></span>

[<span data-ttu-id="e6e19-186">Paėmimo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="e6e19-186">Pickup information module</span></span>](../pickup-info-module.md)