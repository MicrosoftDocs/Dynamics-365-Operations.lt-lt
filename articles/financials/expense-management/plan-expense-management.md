---
title: Konfigūruoti išlaidų valdymą
description: Šiame straipsnyje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš konfigūruodami Išlaidų valdymą programoje „Microsoft Dynamics 365 for Finance and Operations“.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf0725a368969e8a2f85f38371d9f18f308246a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840918"
---
# <a name="configure-expense-management"></a><span data-ttu-id="65631-103">Konfigūruoti išlaidų valdymą</span><span class="sxs-lookup"><span data-stu-id="65631-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65631-104">Šioje temoje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš konfigūruodami Išlaidų valdymą programoje „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="65631-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="65631-105">Modulyje Išlaidų valdymas galite saugoti informaciją apie mokėjimo būdus, kelionių paraiškas, išlaidų ataskaitas, strategijas ir t. t.</span><span class="sxs-lookup"><span data-stu-id="65631-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="65631-106">Kadangi daugelis sprendimų, kuriuos priimate planuodami savo Išlaidų valdymo konfigūraciją, paremti jūsų organizacijos hierarchija ir finansine struktūra, turite žr. tų sričių planavimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="65631-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="65631-107">Vidinės įmonės išlaidos</span><span class="sxs-lookup"><span data-stu-id="65631-107">Intercompany expenses</span></span>

<span data-ttu-id="65631-108">Kai įgalinate vidinės įmonės išlaidas, juridiniams subjektams ir darbuotojams leidžiate numatyti išlaidas kito juridinio subjekto vardu ir rinkti mokėjimus iš įdarbinusio juridinio subjekto, priklausančio jūsų organizacijai.</span><span class="sxs-lookup"><span data-stu-id="65631-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="65631-109">Pavyzdžiui, juridinio subjekto A darbuotojas įvykdo projektą juridiniam subjektui B ir projekto metu patiriama su keliavimu susijusių išlaidų.</span><span class="sxs-lookup"><span data-stu-id="65631-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="65631-110">Jei įgalintos vidinės įmonės išlaidos, darbuotojas gali pateikti išlaidų ataskaitą, kurioje išlaidos bus užregistruotos juridiniam subjektui B, o jas padengti turės juridinis subjektas A. Jei jūsų organizacijoje nėra kelių juridinių subjektų, įgalinti vidinės įmonės išlaidų nereikia.</span><span class="sxs-lookup"><span data-stu-id="65631-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="65631-111">**Sprendimas:** ar norite įgalinti vidinės įmonės išlaidas?</span><span class="sxs-lookup"><span data-stu-id="65631-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="65631-112">Finansų valdymas</span><span class="sxs-lookup"><span data-stu-id="65631-112">Financial management</span></span>

<span data-ttu-id="65631-113">Išlaidų valdymas yra glaudžiai integruotas su jūsų organizacijos finansų valdymu.</span><span class="sxs-lookup"><span data-stu-id="65631-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="65631-114">Didelė modulio Išlaidų valdymas konfigūracijos dalis bus paremta sprendimais, kuriuos priėmėte dėl savo organizacijos finansų.</span><span class="sxs-lookup"><span data-stu-id="65631-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="65631-115">Toliau pateikiamuose skyriuose aprašomos įvairios sritys, kurioms reikia planavimo ir sprendimų, paremtų jūsų organizacijos finansiniais sprendimais ir vadovavimo komandos patarimais.</span><span class="sxs-lookup"><span data-stu-id="65631-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="65631-116">Dienpinigiai</span><span class="sxs-lookup"><span data-stu-id="65631-116">Per diems</span></span>

<span data-ttu-id="65631-117">Turite apibrėžti darbuotojų dienpinigius, kuriuos suteikia jūsų organizacija.</span><span class="sxs-lookup"><span data-stu-id="65631-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="65631-118">Kadangi dienpinigiai paprastai naudojami padengti tokioms išlaidoms kaip maistas, apgyvendinimas ir kitos papildomos išlaidos, galite kurti dienpinigių, kuriuos suteikia jūsų organizacija, taisykles.</span><span class="sxs-lookup"><span data-stu-id="65631-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="65631-119">dienpinigių tarifus galima nustatyti pagal metų laiką, kelionės vietą, arba abu.</span><span class="sxs-lookup"><span data-stu-id="65631-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="65631-120">Apibrėždami dienpinigių taisyklę, galite nurodyti, kad, jeigu darbuotojas nemokamai gauna maitinimą ar paslaugas, iš dienpinigių bus išskaitytas tam tikras procentas.</span><span class="sxs-lookup"><span data-stu-id="65631-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="65631-121">Taip pat galite apibrėžti dienpinigių tarifų pakopas, taip nustatant mažiausią ir didžiausią valandų skaičių, kada dienpinigių tarifas gali būti taikomas darbuotojo kelionei.</span><span class="sxs-lookup"><span data-stu-id="65631-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="65631-122">**Sprendimai:**</span><span class="sxs-lookup"><span data-stu-id="65631-122">**Decisions:**</span></span>

- <span data-ttu-id="65631-123">Toliau pateiktos numatytosios pirmosios ir paskutiniosios dienų dienpinigių taisykles.</span><span class="sxs-lookup"><span data-stu-id="65631-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="65631-124">Koks yra minimalus valandų skaičius, kurio darbuotojas gali reikalauti ir vis tiek gauti dienpinigius?</span><span class="sxs-lookup"><span data-stu-id="65631-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="65631-125">Ar pirmąją dieną ir paskutiniąją dieną maistui siūloma mažesnė suma?</span><span class="sxs-lookup"><span data-stu-id="65631-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="65631-126">Jei suma sumažėjo, koks yra sumažėjimo procentas?</span><span class="sxs-lookup"><span data-stu-id="65631-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="65631-127">Ar pirmąją dieną ir paskutiniąją dieną viešbučiui siūloma mažesnė suma?</span><span class="sxs-lookup"><span data-stu-id="65631-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="65631-128">Jei suma sumažėjo, koks yra sumažėjimo procentas?</span><span class="sxs-lookup"><span data-stu-id="65631-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="65631-129">Ar pirmąją dieną ir paskutiniąją dieną patirtoms kitoms išlaidoms siūloma mažesnė suma?</span><span class="sxs-lookup"><span data-stu-id="65631-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="65631-130">Jei suma sumažėjo, koks yra sumažėjimo procentas?</span><span class="sxs-lookup"><span data-stu-id="65631-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="65631-131">Toliau pateiktos numatytosios dienpinigių taisyklės.</span><span class="sxs-lookup"><span data-stu-id="65631-131">Default per diem rules:</span></span>

    - <span data-ttu-id="65631-132">Ar kiekvienam valgiui dienpinigių skiriama tam tikru procentu mažiau, jei, pavyzdžiui, maistas yra nemokamas?</span><span class="sxs-lookup"><span data-stu-id="65631-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="65631-133">Jei suma sumažėjo, koks yra kiekvieno valgio sumos sumažėjimo procentas?</span><span class="sxs-lookup"><span data-stu-id="65631-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="65631-134">Ar maisto dienpinigių sumažinimas skaičiuojamas dienai, kelionei, ar pagal valgių per dieną skaičių?</span><span class="sxs-lookup"><span data-stu-id="65631-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="65631-135">Ar dienpinigių sumas reikia apvalinti įprastai, ar iki didesnio skaičiaus?</span><span class="sxs-lookup"><span data-stu-id="65631-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="65631-136">Ar dienpinigiai skaičiuojami 24 valandų laikotarpiui, ar kalendorinei dienai?</span><span class="sxs-lookup"><span data-stu-id="65631-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="65631-137">Toliau nurodytos dienpinigių taisyklės pagal vietą.</span><span class="sxs-lookup"><span data-stu-id="65631-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="65631-138">Ar dienpinigių tarifai skiriasi atsižvelgiant į vietą?</span><span class="sxs-lookup"><span data-stu-id="65631-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="65631-139">Kokios vietos yra įtrauktos?</span><span class="sxs-lookup"><span data-stu-id="65631-139">What locations are included?</span></span>
    - <span data-ttu-id="65631-140">Jei dienpinigių tarifai skiriasi atsižvelgiant į vietą, kokia procentinė suma yra numatyta tolesnių tipų išlaidoms kiekvienoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="65631-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="65631-141">Maitinimo išlaidos</span><span class="sxs-lookup"><span data-stu-id="65631-141">Meals</span></span>
        - <span data-ttu-id="65631-142">Viešbutis</span><span class="sxs-lookup"><span data-stu-id="65631-142">Hotel</span></span>
        - <span data-ttu-id="65631-143">Kitos išlaidos</span><span class="sxs-lookup"><span data-stu-id="65631-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="65631-144">Išlaidų valdymo žurnalai ir sąskaitos</span><span class="sxs-lookup"><span data-stu-id="65631-144">Expense management journals and accounts</span></span>

<span data-ttu-id="65631-145">Valdant išlaidas reikia naudoti kelis žurnalus ir sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="65631-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="65631-146">Turite nuspręsti, pvz., ar tą pačią sąskaitą naudoti avansams grynaisiais pinigais ir kredito kortelės konfliktams.</span><span class="sxs-lookup"><span data-stu-id="65631-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="65631-147">**Sprendimai:**</span><span class="sxs-lookup"><span data-stu-id="65631-147">**Decisions:**</span></span>

- <span data-ttu-id="65631-148">Kuriame DK žurnale registruojamos patvirtintos išlaidų ataskaitos?</span><span class="sxs-lookup"><span data-stu-id="65631-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="65631-149">Kuri sąskaita naudojama avansams grynaisiais pinigais?</span><span class="sxs-lookup"><span data-stu-id="65631-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="65631-150">Ar avansai grynaisiais pinigais turėtų būti registruojami nedelsiant?</span><span class="sxs-lookup"><span data-stu-id="65631-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="65631-151">Mokėjimo būdai</span><span class="sxs-lookup"><span data-stu-id="65631-151">Payment methods</span></span>

<span data-ttu-id="65631-152">Kai darbuotojams leidžiate jūsų įmonės vardu numatyti išlaidas, turite apibrėžti mokėjimo metodus, kuriuos darbuotojams leidžiama naudoti.</span><span class="sxs-lookup"><span data-stu-id="65631-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="65631-153">Pavyzdžiui, galite darbuotojams leisti naudoti grynųjų pinigų ar įmonės kredito kortelę.</span><span class="sxs-lookup"><span data-stu-id="65631-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="65631-154">Taip pat darbuotojams galite leisti naudoti asmenines kredito korteles, ir tada jiems sumokėti kompensacijas.</span><span class="sxs-lookup"><span data-stu-id="65631-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="65631-155">Dėl kiekvieno leidžiamo mokėjimo būdo turite atlikti toliau nurodytus sprendimus.</span><span class="sxs-lookup"><span data-stu-id="65631-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="65631-156">**Sprendimai:**</span><span class="sxs-lookup"><span data-stu-id="65631-156">**Decisions:**</span></span>

- <span data-ttu-id="65631-157">Kokie mokėjimo būdai leidžiami?</span><span class="sxs-lookup"><span data-stu-id="65631-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="65631-158">Kam priklauso mokėjimo būdo išlaidos?</span><span class="sxs-lookup"><span data-stu-id="65631-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="65631-159">Ar yra koks korespondentinės sąskaitos tipas?</span><span class="sxs-lookup"><span data-stu-id="65631-159">Is there an offset account type?</span></span> <span data-ttu-id="65631-160">Jei yra korespondentinės sąskaitos tipas, koks jis?</span><span class="sxs-lookup"><span data-stu-id="65631-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="65631-161">Jei korespondentinė sąskaita yra, kuri ji?</span><span class="sxs-lookup"><span data-stu-id="65631-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="65631-162">Jei mokėjimo būdas yra kredito kortelė, ar mokėjimo būdas turėtų būti naudojamas tik su importuotomis operacijomis?</span><span class="sxs-lookup"><span data-stu-id="65631-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="65631-163">Išlaidų kategorijos ir bendro naudojimo kategorijos</span><span class="sxs-lookup"><span data-stu-id="65631-163">Expense categories and shared categories</span></span>

<span data-ttu-id="65631-164">Darbuotojams kuriant išlaidų ataskaitą, visos jų įrašomos išlaidos turi būti susietos su išlaidų kategorija.</span><span class="sxs-lookup"><span data-stu-id="65631-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="65631-165">Išlaidų kategorijos išvedamos iš bendro naudojimo kategorijų, kurios gali būti bendrai naudojamos visuose jūsų organizacijos juridiniuose subjektuose.</span><span class="sxs-lookup"><span data-stu-id="65631-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="65631-166">Šios kategorijos taip pat gali būti bendrai naudojamos modulyje Projektų valdymas ir apskaita – tai priklauso nuo to, kaip apibrėžta jūsų organizacija.</span><span class="sxs-lookup"><span data-stu-id="65631-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="65631-167">Pagal savo organizacijos apibrėžtį ir diegimo komandos patarimus nustatykite, ar modulyje Išlaidų valdymas naudojamos kategorijos bus naudojamos tik modulyje Išlaidų valdymas, ar jas reikia bendrai naudoti moduliuose Projektų valdymas ir apskaita bei Išlaidų valdymas.</span><span class="sxs-lookup"><span data-stu-id="65631-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="65631-168">Atkreipkite dėmesį, kad šios kategorijos gali būti bendrai naudojamos Projektui ir Išlaidoms arba Projektui ir Gamybai, bet ne Išlaidoms ir Gamybai.</span><span class="sxs-lookup"><span data-stu-id="65631-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="65631-169">Dėl kiekvienos išlaidų kategorijos turite priimti toliau nurodytus sprendimus.</span><span class="sxs-lookup"><span data-stu-id="65631-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="65631-170">**Sprendimai:**</span><span class="sxs-lookup"><span data-stu-id="65631-170">**Decisions:**</span></span>

- <span data-ttu-id="65631-171">Kas yra išlaidų kategorija?</span><span class="sxs-lookup"><span data-stu-id="65631-171">What is the expense category?</span></span> <span data-ttu-id="65631-172">Pavyzdžiui, skrydžių, viešbučio ar kilometražo kategorijos.</span><span class="sxs-lookup"><span data-stu-id="65631-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="65631-173">Ar išlaidų kategoriją taip pat galima naudoti modulyje Projektų valdymas ir apskaita?</span><span class="sxs-lookup"><span data-stu-id="65631-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="65631-174">Kas yra išlaidų tipas?</span><span class="sxs-lookup"><span data-stu-id="65631-174">What is the expense type?</span></span>
- <span data-ttu-id="65631-175">Koks yra numatytasis išlaidų kategorijos mokėjimo būdas?</span><span class="sxs-lookup"><span data-stu-id="65631-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="65631-176">Ar išlaidų kategorijos išlaidas reikia detaliai išvardyti?</span><span class="sxs-lookup"><span data-stu-id="65631-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="65631-177">Kuri yra pagrindinė numatytoji išlaidų kategorijos sąskaita?</span><span class="sxs-lookup"><span data-stu-id="65631-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="65631-178">Kokia yra numatytoji išlaidų kategorijos prekių PVM grupė?</span><span class="sxs-lookup"><span data-stu-id="65631-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="65631-179">Ar leidžiami papildomi išlaidų kategorijos mokėjimo būdai?</span><span class="sxs-lookup"><span data-stu-id="65631-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="65631-180">Jei leidžiami papildomi mokėjimo būdai, kokie jie?</span><span class="sxs-lookup"><span data-stu-id="65631-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="65631-181">Ar šioje išlaidų kategorijoje yra subkategorijų?</span><span class="sxs-lookup"><span data-stu-id="65631-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="65631-182">Jei subkategorijų yra, taip pat turite priimti tolesnius sprendimus.</span><span class="sxs-lookup"><span data-stu-id="65631-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="65631-183">ar kuri nors subkategorija neįtraukta į mokesčių susigrąžinimo procesą?</span><span class="sxs-lookup"><span data-stu-id="65631-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="65631-184">Kokia yra subkategorijų prekių PVM grupė?</span><span class="sxs-lookup"><span data-stu-id="65631-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="65631-185">Jei išlaidų kategorija taip pat naudojama modulyje Projektų valdymas ir apskaita, atsakykite į likusius klausimus.</span><span class="sxs-lookup"><span data-stu-id="65631-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="65631-186">Kitu atveju pereikite prie kito skyriaus.</span><span class="sxs-lookup"><span data-stu-id="65631-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="65631-187">Kokios išlaidų sąskaitos bus naudojamos toliau nurodytoms išlaidoms?</span><span class="sxs-lookup"><span data-stu-id="65631-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="65631-188">Savikaina</span><span class="sxs-lookup"><span data-stu-id="65631-188">Cost</span></span>
    - <span data-ttu-id="65631-189">Atlyginimo paskirstymas</span><span class="sxs-lookup"><span data-stu-id="65631-189">Payroll allocation</span></span>
    - <span data-ttu-id="65631-190">NG - Savikaina</span><span class="sxs-lookup"><span data-stu-id="65631-190">WIP-cost value</span></span>
    - <span data-ttu-id="65631-191">Išlaidos – prekė</span><span class="sxs-lookup"><span data-stu-id="65631-191">Cost-item</span></span>
    - <span data-ttu-id="65631-192">Vykdomas projektas – Išlaidų vertė – Prekė</span><span class="sxs-lookup"><span data-stu-id="65631-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="65631-193">Sukauptas nuostolis</span><span class="sxs-lookup"><span data-stu-id="65631-193">Accrued loss</span></span>
    - <span data-ttu-id="65631-194">NG – sukauptas nuostolis</span><span class="sxs-lookup"><span data-stu-id="65631-194">WIP-accrued loss</span></span>

- <span data-ttu-id="65631-195">Kokios pajamų sąskaitos bus naudojamos toliau nurodytiems dalykams?</span><span class="sxs-lookup"><span data-stu-id="65631-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="65631-196">Įplaukos, kurioms išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="65631-196">Invoiced revenue</span></span>
    - <span data-ttu-id="65631-197">Sukauptos įplaukos – pardavimo vertė</span><span class="sxs-lookup"><span data-stu-id="65631-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="65631-198">NG – Pardavimo vertė</span><span class="sxs-lookup"><span data-stu-id="65631-198">WIP-sales value</span></span>
    - <span data-ttu-id="65631-199">Sukauptos įplaukos – gamyba</span><span class="sxs-lookup"><span data-stu-id="65631-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="65631-200">NG – gamyba</span><span class="sxs-lookup"><span data-stu-id="65631-200">WIP-production</span></span>
    - <span data-ttu-id="65631-201">Sukauptos įplaukos – pelnas</span><span class="sxs-lookup"><span data-stu-id="65631-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="65631-202">NG – pelnas</span><span class="sxs-lookup"><span data-stu-id="65631-202">WIP-profit</span></span>
    - <span data-ttu-id="65631-203">Sukauptos įplaukos – abonementas</span><span class="sxs-lookup"><span data-stu-id="65631-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="65631-204">NG – abonementas</span><span class="sxs-lookup"><span data-stu-id="65631-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="65631-205">Mokesčiai</span><span class="sxs-lookup"><span data-stu-id="65631-205">Taxes</span></span>

<span data-ttu-id="65631-206">Turite nustatyti, kurie su išlaidomis susiję mokesčiai įtraukti ar įgalinti išlaidų ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="65631-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="65631-207">**Sprendimai:**</span><span class="sxs-lookup"><span data-stu-id="65631-207">**Decisions:**</span></span>

- <span data-ttu-id="65631-208">Ar į išlaidų sumas įtrauktas PVM?</span><span class="sxs-lookup"><span data-stu-id="65631-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="65631-209">Ar turėtų būti įgalintas išlaidų mokesčių susigrąžinimas?</span><span class="sxs-lookup"><span data-stu-id="65631-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="65631-210">Jei, planuodami didžiąją knygą, nusprendėte taikyti JAV PVM ir naudojimo mokesčio taisykles, išlaidoms mokesčių susigrąžinimo funkcijos įjungti negalite.</span><span class="sxs-lookup"><span data-stu-id="65631-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="65631-211">(Norėdami taikyti JAV PVM ir naudojimo mokesčio taisykles, parinktį **Taikyti PVM apmokestinimo taisykles** nustatykite kaip **Taip**.)</span><span class="sxs-lookup"><span data-stu-id="65631-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="65631-212">Strategijos</span><span class="sxs-lookup"><span data-stu-id="65631-212">Policies</span></span>

<span data-ttu-id="65631-213">Sukūrę išlaidų ataskaitų strategijų, savo organizacijai galite padėti sutaupyti laiko ir pinigų, kai darbuotojai jos vardu numato išlaidas.</span><span class="sxs-lookup"><span data-stu-id="65631-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="65631-214">Strategijos padeda užtikrinti, kad darbuotojai neviršytų biudžeto, pateiktų visą reikiamą informaciją ir pinigus leistų, tik kai reikia.</span><span class="sxs-lookup"><span data-stu-id="65631-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="65631-215">Dėl kiekvienos išlaidų ataskaitų strategijos ir kiekvienos išlaidų ataskaitų patvirtinimo strategijos, kurią sukuriate, turite priimti toliau nurodytus sprendimus.</span><span class="sxs-lookup"><span data-stu-id="65631-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="65631-216">**Sprendimai:**</span><span class="sxs-lookup"><span data-stu-id="65631-216">**Decisions:**</span></span>

- <span data-ttu-id="65631-217">Koks yra strategijos pavadinimas?</span><span class="sxs-lookup"><span data-stu-id="65631-217">What is the name of the policy?</span></span>
- <span data-ttu-id="65631-218">Kam išlaidų strategija skirta?</span><span class="sxs-lookup"><span data-stu-id="65631-218">What is the expense policy for?</span></span>
- <span data-ttu-id="65631-219">Jei anksčiau nusprendėte įgalinti vidinės įmonės išlaidas, kurioms jūsų organizacijos įmonėms ši strategija bus taikoma?</span><span class="sxs-lookup"><span data-stu-id="65631-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="65631-220">Kada strategija įsigalioja?</span><span class="sxs-lookup"><span data-stu-id="65631-220">When does the policy become effective?</span></span>
- <span data-ttu-id="65631-221">Kai strategija baigia galioti?</span><span class="sxs-lookup"><span data-stu-id="65631-221">When does the policy expire?</span></span>
- <span data-ttu-id="65631-222">Kas yra strategijos taisyklė?</span><span class="sxs-lookup"><span data-stu-id="65631-222">What is the policy rule?</span></span>
- <span data-ttu-id="65631-223">Koks yra strategijos taisyklės rezultatas?</span><span class="sxs-lookup"><span data-stu-id="65631-223">What is the outcome of the policy rule?</span></span>
