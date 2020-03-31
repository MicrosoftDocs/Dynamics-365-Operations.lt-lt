---
title: Įspėjimų dėl apgaulės nustatymas skambučių centre ir jų naudojimas
description: Šioje temoje paaiškinama, kaip nustatyti taisykles, kad klientų aptarnavimo atstovai užsakymų apdorojimo metu būtų įspėjami apie galimai apgaulingą informaciją. Galite apibrėžti konkrečius kodus, kuriuos naudojant galima automatiškai arba rankiniu būdu sulaikyti įtartinus užsakymus.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 38649e40021d1caaf70f217b3ebae0d488806180
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057214"
---
# <a name="set-up-and-work-with-call-center-fraud-alerts"></a><span data-ttu-id="b8c23-104">Įspėjimų dėl apgaulės nustatymas skambučių centre ir jų naudojimas</span><span class="sxs-lookup"><span data-stu-id="b8c23-104">Set up and work with call center fraud alerts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b8c23-105">Šioje temoje paaiškinama, kaip nustatyti kriterijus ir taisykles, leidžiančias sulaikyti galimai apgaulingus pardavimo užsakymus ir juos peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="b8c23-105">This topic explains how to set up criteria and rules to put potentially fraudulent sales orders on hold for further review.</span></span> <span data-ttu-id="b8c23-106">Apgaulės patikros funkcija naudojama siekiant nustatyti pardavimo užsakymo informacijos pagrįstumą.</span><span class="sxs-lookup"><span data-stu-id="b8c23-106">The fraud check feature is used to determine the validity of the information in a sales order.</span></span> <span data-ttu-id="b8c23-107">Jei remiantis organizacijos nustatytais apgaulės kriterijais ir taisyklėmis, pardavimo užsakyme esanti informacija pradeda kelti abejonių, užsakymas gali būti sulaikytas siekiant jį atidžiau peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="b8c23-107">If the information in the sales order appears to be questionable, based on an organization's fraud criteria and rules, the order can be put on hold for further review.</span></span> <span data-ttu-id="b8c23-108">Tokiu atveju užsakymo negalima išleisti į sandėlį toliau apdoroti, kol nebus atšauktas sulaikymas.</span><span class="sxs-lookup"><span data-stu-id="b8c23-108">In this case, the order can't be released to the warehouse for further processing until the hold has been cleared.</span></span>

> [!NOTE]
> <span data-ttu-id="b8c23-109">Šią funkciją galima naudoti tik apdorojant pardavimo užsakymus, gautus per „Commerce“ skambučių centro kanalą.</span><span class="sxs-lookup"><span data-stu-id="b8c23-109">This feature can be used only with sales order processing for the Commerce call center channel.</span></span>

## <a name="turning-on-the-fraud-check-feature"></a><span data-ttu-id="b8c23-110">Apgaulės patikros funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="b8c23-110">Turning on the fraud check feature</span></span>

<span data-ttu-id="b8c23-111">Norėdami naudoti apgaulės patikros funkciją, nustatykite kanalo parinktį **Įgalinti užsakymo baigimą** kaip **Taip**, kai skambučių centro kanalas yra [apibrėžtas](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-order-processing-options).</span><span class="sxs-lookup"><span data-stu-id="b8c23-111">To use the fraud check feature, you must set the **Enable order completion** option on the channel to **Yes** when the call center channel is [defined](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-order-processing-options).</span></span> <span data-ttu-id="b8c23-112">Įjungus užsakymo baigimo funkciją, skambučių centro vartotojai kiekvieno sukurto pardavimo užsakymo puslapyje turi pasirinkti **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-112">When order completion is turned on, call center users must select **Complete** on the sales order page for all sales orders that are created.</span></span> <span data-ttu-id="b8c23-113">Pasirinkus baigimo veiksmą atidaromas puslapis **Pardavimo užsakymo suvestinė**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-113">The Complete action causes the **Sales order summary** page to open.</span></span> <span data-ttu-id="b8c23-114">Kai vartotojai įveda reikiamus mokėjimo duomenis puslapyje **Pardavimo užsakymo suvestinė**, reikia pasirinkti **Pateikti**, kad užsakymas būtų baigtas.</span><span class="sxs-lookup"><span data-stu-id="b8c23-114">After users enter the required payment data on the **Sales order summary** page, they select **Submit** to finalize the order.</span></span> <span data-ttu-id="b8c23-115">Pateikus užsakymą, suaktyvinama apgaulės patikros funkcija ir automatiškai patikrinamos bet kokios sistemoje esančios aktyvios taisyklės.</span><span class="sxs-lookup"><span data-stu-id="b8c23-115">When the order is submitted, the fraud check feature is triggered, and any rules that are active in the system are automatically validated.</span></span>

<span data-ttu-id="b8c23-116">Skambučių centro vartotojai taip pat gali rankiniu būdu sulaikyti pardavimo užsakymus ir patikrinti juos dėl galimos apgaulės prieš pasirinkdami **Pateikti**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-116">Call center users can also manually put sales orders on hold for fraud review before they select **Submit**.</span></span> <span data-ttu-id="b8c23-117">Norėdami rankiniu būdu sulaikyti pardavimo užsakymą, puslapyje **Pardavimo užsakymo suvestinė** pasirinkite **Sulaikyti** \> **Sulaikymas dėl apgaulės rankiniu būdu**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-117">To manually put a sales order on hold, on the **Sales order summary** page, select **Hold** \> **Manual fraud hold**.</span></span> <span data-ttu-id="b8c23-118">Tada būsite paraginti įvesti komentarą, nurodantį užsakymo sulaikymo priežastį.</span><span class="sxs-lookup"><span data-stu-id="b8c23-118">You're then prompted to enter a comment to explain your reason for putting the order on hold.</span></span> <span data-ttu-id="b8c23-119">Šis komentaras bus rodomas [užsakymų sulaikymo](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) darbo srityje, kad sulaikytus užsakymus peržiūrinčiam vartotojui būtų paprasčiau nuspręsti, ar užsakymo sulaikymą reikia atšaukti.</span><span class="sxs-lookup"><span data-stu-id="b8c23-119">This comment will appear in the [order holds](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) workbench to provide context to the user who reviews orders that are on hold to determine whether the order should be released.</span></span>

<span data-ttu-id="b8c23-120">Sukonfigūravus kanale parinktį **Įgalinti užsakymo baigimą**, skambučių centro parametrų dalyje taip pat reikia sukonfigūruoti apgaulės patikros funkciją.</span><span class="sxs-lookup"><span data-stu-id="b8c23-120">In addition to configuring the **Enable order completion** option on the channel, you must configure the fraud check feature in the Call center parameters.</span></span> <span data-ttu-id="b8c23-121">Eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalo nustatymas** \> **Skambučių centro sąranka** \> **Skambučių centro parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-121">Go to **Retail and Commerce** \> **Channel setup** \> **Call center setup** \> **Call center parameters**.</span></span> <span data-ttu-id="b8c23-122">Puslapio **Skambučių centro parametrai** skirtuke **Sulaikymai** nustatykite parinkties **Apgaulės patikra** parametrą **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-122">On the **Call center parameters** page, on the **Holds** tab, set the **Fraud check** option to **Yes**.</span></span>

<span data-ttu-id="b8c23-123">Skirtuke **Sulaikymai** taip pat reikia apibrėžti [sulaikymo kodus](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds), kurie taikomi rankiniu būdu ar automatiškai sulaikytam užsakymui, kurį reikia peržiūrėti dėl galimos apgaulės.</span><span class="sxs-lookup"><span data-stu-id="b8c23-123">On the **Holds** tab, you should also define the [hold codes](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) that will be applied to an order that is either manually or automatically put on hold for fraud review.</span></span> <span data-ttu-id="b8c23-124">Nustatykite sulaikymo kodus laukuose **Sulaikymo dėl apgaulės rankiniu būdu kodas** ir **Sulaikymo dėl apgaulės kodas**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-124">Set the hold codes in the **Manual fraud hold code** and **Fraud hold code** fields.</span></span> <span data-ttu-id="b8c23-125">Galite sukurti du unikalius sulaikymo kodus, kad sulaikymo darbo srityje dirbantys vartotojai galėtų lengvai filtruoti ir atskirti automatinius sulaikymus ir rankiniu būdu atliktus sulaikymus.</span><span class="sxs-lookup"><span data-stu-id="b8c23-125">You might find it helpful to create two unique hold codes, so that users who work in the holds workbench can easily filter and distinguish automatic holds from manual holds.</span></span>

<span data-ttu-id="b8c23-126">Kad apgaulės patikros funkcija veiktų efektyviai, taip pat reikia nustatyti lauką **Minimalus rezultatas**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-126">For the fraud check feature to work effectively, you must also set the **Minimum score** field.</span></span> <span data-ttu-id="b8c23-127">Kiekvienas sistemoje nustatytas apgaulės kriterijus ir taisyklė turi priskirtą rezultato vertę.</span><span class="sxs-lookup"><span data-stu-id="b8c23-127">Every fraud criterion and rule that is defined in the system has a score.</span></span> <span data-ttu-id="b8c23-128">Kai pardavimo užsakymas tikrinamas dėl apgaulės, radus vieną arba kelis atitinkančius kriterijus, rezultatai sudedami ir gaunamas bendras užsakymo apgaulės rezultatas.</span><span class="sxs-lookup"><span data-stu-id="b8c23-128">When a sales order is checked for fraud matches, if one or more matches are found, the scores are added together to give the order a total fraud score.</span></span> <span data-ttu-id="b8c23-129">Jei bendras užsakymo apgaulės rezultatas viršija lauke **Minimalus rezultatas** nurodytą vertę, užsakymas automatiškai sulaikomas.</span><span class="sxs-lookup"><span data-stu-id="b8c23-129">If the total fraud score for an order exceeds the value of the **Minimum score** field, the order is automatically put on hold.</span></span> <span data-ttu-id="b8c23-130">Pasirinktinai naudodami kitus su rezultatu susijusius skirtuko **Sulaikymai** laukus, galite apibrėžti el. pašto rezultatą, telefono rezultatą, pašto indekso rezultatą ir išplėsto pašto indekso rezultatą.</span><span class="sxs-lookup"><span data-stu-id="b8c23-130">You can optionally use the other score-related fields on the **Holds** tab to define the email score, phone score, ZIP/postal code score, and extended ZIP/postal code score.</span></span> <span data-ttu-id="b8c23-131">Jei nenurodysite jokių statinių apgaulės duomenų kriterijų, kai juos apibrėžiate puslapyje **Statiniai apgaulės duomenys**, rezultatų verčių, sistema juos vertins naudodama numatytąsias rezultatų vertes, kurias nurodėte puslapio **Skambučių centro parametrai** skirtuke **Sulaikymai**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-131">If you don't specify a score for any of these static fraud criteria when you define them on the **Static fraud data** page, the system will score them by using the default scores that you specify on the **Holds** tab of the **Call center parameters** page.</span></span>

<span data-ttu-id="b8c23-132">Galiausiai naudodami lauką **Apgaulės komentaro tipas** nurodykite dokumento tipą, kurį reikia naudoti, kai vartotojai įveda komentarus, kai rankiniu būdu dėl galimos apgaulės sulaiko užsakymą, kurį reikia peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="b8c23-132">Finally, use the **Fraud comment type** field to specify the document type that should be used when users enter comments when they manually put an order on hold for fraud review.</span></span> <span data-ttu-id="b8c23-133">Dažniausiai nustatomas šio lauko parametras yra **Pastaba**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-133">Most often, this field is set to **Note**.</span></span>

## <a name="defining-fraud-criteria-and-rules"></a><span data-ttu-id="b8c23-134">Apgaulės kriterijų ir taisyklių apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="b8c23-134">Defining fraud criteria and rules</span></span>

<span data-ttu-id="b8c23-135">Sistema naudoja dviejų tipų apgaulės kriterijus, pagal kuriuos nustatoma, ar užsakymą reikia sulaikyti dėl galimos apgaulės ir peržiūrėti:</span><span class="sxs-lookup"><span data-stu-id="b8c23-135">The system references two types of fraud criteria to determine whether an order should be put on hold for fraud review:</span></span>

- <span data-ttu-id="b8c23-136">**Statiniai apgaulės duomenys** naudoja konkrečią vertę, pvz., telefono numerį, kuris buvo įtrauktas į užblokuotų numerių sąrašą, ar el. pašto adresą, kuris yra pažymėtas, nes buvo anksčiau naudotas atliekant apgaulingas operacijas.</span><span class="sxs-lookup"><span data-stu-id="b8c23-136">**Static fraud data** uses a specific value, such as a phone number that has been put on a list of blocked numbers or an email address that has been flagged because it's known to have been used for previous fraudulent transactions.</span></span> <span data-ttu-id="b8c23-137">Norėdami nustatyti statinius apgaulės duomenis, eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalo nustatymas** \> **Skambučių centro sąranka** \> **Apgaulė** \> **Statiniai apgaulės duomenys**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-137">To set up static fraud data, go to **Retail and Commerce** \> **Channel setup** \> **Call center setup** \> **Fraud** \> **Static fraud data**.</span></span> <span data-ttu-id="b8c23-138">Puslapyje **Statiniai apgaulės duomenys** galite įtraukti apgaulės kriterijus rankiniu būdu ar importuodami duomenis.</span><span class="sxs-lookup"><span data-stu-id="b8c23-138">On the **Static fraud data** page, you can add fraud criteria manually or through data import.</span></span> <span data-ttu-id="b8c23-139">Prie apgaulingos informacijos pridedamos rezultatų vertės.</span><span class="sxs-lookup"><span data-stu-id="b8c23-139">Scores are attached to the fraudulent information.</span></span> <span data-ttu-id="b8c23-140">Jei įjungta apgaulės patikros funkcija, kiekvienas įvestas pardavimo užsakymas bus lyginamas su statiniais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="b8c23-140">If the fraud check feature is turned on, every sales order that is entered is compared to the static data.</span></span> <span data-ttu-id="b8c23-141">Jei duomenys randami kliento sąskaitų siuntimo adrese arba pristatymo adrese, susietame su užsakymo antrašte, arba jei duomenys randami pristatymo adresuose, susietuose su bet kuria to pardavimo užsakymo eilute, visų unikalių atitikmenų rezultatų vertės sudedamos ir bendras rezultatas palyginamas su lauke **Minimalus rezultatas** nurodyta verte, siekiant nustatyti, ar užsakymą reikia sulaikyti.</span><span class="sxs-lookup"><span data-stu-id="b8c23-141">If the data is found in either the customer's billing address or the delivery address that is linked to the order header, or if the data is found in the delivery addresses that are linked to any of the lines on that sales order, the scores of all unique matches are added together and compared to the **Minimum score** value to determine whether the order should be put on hold.</span></span>

- <span data-ttu-id="b8c23-142">**Apgaulės taisykles** sudaro vartotojo apibrėžti kintamieji ir apibrėžtos tų kintamųjų sąlygos.</span><span class="sxs-lookup"><span data-stu-id="b8c23-142">**Fraud rules** consist of user-defined variables and the conditions that are defined for those variables.</span></span> <span data-ttu-id="b8c23-143">Norėdami kurti taisykles, eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalo nustatymas** \> **Skambučių centro sąranka** \> **Apgaulė** \> **Taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-143">To create rules, go to **Retail and Commerce** \> **Channel setup** \> **Call center setup** \> **Fraud** \> **Rules**.</span></span> <span data-ttu-id="b8c23-144">Naudodama apgaulės taisykles įmonė gali sukonfigūruoti sudėtingesnį taisyklių rinkinį, kuriame naudojami sakiniai **IR** arba **ARBA**, kad būtų galima įvertinti keletą sąlygų.</span><span class="sxs-lookup"><span data-stu-id="b8c23-144">Fraud rules let a company configure a more complex rule set that can include **AND** or **OR** statements to evaluate multiple conditions.</span></span> <span data-ttu-id="b8c23-145">Pavyzdžiui, vartotojas nori sulaikyti ir peržiūrėti dėl galimos apgaulės visus klientų, kurie priklauso konkrečiai klientų grupei ir kurie užsisakė konkretų produktą, užsakymus.</span><span class="sxs-lookup"><span data-stu-id="b8c23-145">For example, a user wants all orders for customers who belong to a specific customer group and who ordered a specific product to be put on hold for fraud review.</span></span> <span data-ttu-id="b8c23-146">Tokiu atveju sąlygos, taikomos tikrinant klientą ir produktus, apibrėžiamos puslapyje **Taisyklės** ir naudojama sąlyga IR.</span><span class="sxs-lookup"><span data-stu-id="b8c23-146">In this case, conditions to validate the customer and products are defined on the **Rules** page, and an AND condition is used.</span></span> <span data-ttu-id="b8c23-147">Užsakymas sulaikomas tik tada, jei tenkinamos abi sąlygos ir jei bendras užsakymo apgaulės rezultatas, sudarytas iš šiai taisyklei priskirtos rezultato vertės ir kitų taisyklių, kurias atitinka užsakymas, rezultatų verčių, viršija vertę **Minimalus rezultatas**, kuri apibrėžta puslapyje **Skambučių centro parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-147">An order is then put on hold only if both conditions are true, and if the score value that is assigned to this rule, plus the score value of any other rules that the order matches, causes the order's total fraud score to exceed the **Minimum score** value that is defined on the **Call center parameters** page.</span></span>

> [!NOTE]
> <span data-ttu-id="b8c23-148">Kelių taisyklių arba pernelyg sudėtingų taisyklių naudojimas paveiks sistemos našumą, pateikiant pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="b8c23-148">Multiple rules or overly complex rules will affect system performance when sales orders are submitted.</span></span> <span data-ttu-id="b8c23-149">Apgaulės patikros funkcija nėra optimizuota apdoroti didelį statinių apgaulės duomenų kiekį ir daug aktyvių taisyklių.</span><span class="sxs-lookup"><span data-stu-id="b8c23-149">The fraud check feature hasn't been optimized to handle a large volume of static fraud data entries and many active rules.</span></span> <span data-ttu-id="b8c23-150">Atminkite, kad kiekviena taisyklė įvertinama tada, kai skambučių centro vartotojas įvesdamas pardavimo užsakymą pasirenka **Pateikti**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-150">Remember that every rule is evaluated when call center users select **Submit** during sales order entry.</span></span> <span data-ttu-id="b8c23-151">Taisyklės vertinamos pagal pardavimo užsakymo antraštę ir visas užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="b8c23-151">The rules are evaluated against the sales order header and all order lines.</span></span> <span data-ttu-id="b8c23-152">Kuo daugiau taisyklių taikote ir kuo sudėtingesni taisyklių sakiniai, tuo ilgiau truks apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="b8c23-152">The more rules there are and the more complex the rule statements are, the more time will be required for processing.</span></span> <span data-ttu-id="b8c23-153">Jei užsakyme yra daug eilučių elementų, daug aktyvių taisyklių ir statinių duomenų įvesčių, šis automatinis procesas, kurio metu peržiūrimi ir patikrinami visi duomenys bei apskaičiuojamas apgaulės rezultatas, gali stipriai paveikti našumą.</span><span class="sxs-lookup"><span data-stu-id="b8c23-153">If there are many line items on an order, and many active rules and static data entries, the automatic process of reviewing and validating all the data and calculating a fraud score can have a severe impact on performance.</span></span> <span data-ttu-id="b8c23-154">Organizacijos, naudojančios šią funkciją, prieš keisdamos taisykles ar statinių apgaulės duomenų kriterijus gamybos aplinkoje, turi visada patikrinti ir patvirtinti, kad užsakymo pateikimo apdorojimo laikas yra priimtinas.</span><span class="sxs-lookup"><span data-stu-id="b8c23-154">Organizations that use this feature should always test and confirm that the processing time for order submission is acceptable before they apply any changes to rules or static fraud criteria to the production environment.</span></span>

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a><span data-ttu-id="b8c23-155">Užsakymų, kurie yra sulaikyti ir kuriuos reikia peržiūrėti dėl apgaulės, identifikavimas</span><span class="sxs-lookup"><span data-stu-id="b8c23-155">Identifying orders that are on hold for fraud review</span></span>

<span data-ttu-id="b8c23-156">Kai skambučių centro vartotojai pateikia pardavimo užsakymą, jei užsakymas atitinka apgaulės kriterijus arba taisykles ir jei bendras rezultatas viršiją minimalų rezultatą, vartotojai gauna įspėjimo pranešimą, informuojantį, kad užsakymas yra sulaikytas.</span><span class="sxs-lookup"><span data-stu-id="b8c23-156">When call center users submit a sales order, if the order matches the fraud criteria or rules, and if the score exceeds the minimum, the users receive a warning message that states that the order has been put on hold.</span></span> <span data-ttu-id="b8c23-157">Vartotojai gali uždaryti šį pranešimą, nes jis pateikiamas tik informaciniais tikslais.</span><span class="sxs-lookup"><span data-stu-id="b8c23-157">Users can close this message, because it's for informational purposes only.</span></span> <span data-ttu-id="b8c23-158">Vartotojai gali pasirinktinai apie tai informuoti klientą.</span><span class="sxs-lookup"><span data-stu-id="b8c23-158">Users can optionally communicate this information to the customer.</span></span> <span data-ttu-id="b8c23-159">Įmonė turėtų nustatyti protokolą, kuriuo tokioje situacijoje turėtų vadovautis vartotojai.</span><span class="sxs-lookup"><span data-stu-id="b8c23-159">The business should determine the protocol that users follow in this situation.</span></span>

<span data-ttu-id="b8c23-160">Užsakymas įrašomas, bet jis pažymimas žyme **Neapdoroti**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-160">The order is saved, but the **Do not process** flag is set on it.</span></span> <span data-ttu-id="b8c23-161">Ši žymė padeda užtikrinti, kad užsakymas nebūtų išleistas į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="b8c23-161">This flag helps guarantee that the order can't be released to the warehouse.</span></span> <span data-ttu-id="b8c23-162">Vartotojai bet kada gali peržiūrėti bet kurio pardavimo užsakymo žymės **Neapdoroti** nustatymą puslapyje **Išsami būsena**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-162">At any time, users can view the setting of the **Do not process** flag for any sales order on the **Detailed status** page.</span></span> <span data-ttu-id="b8c23-163">Šį puslapį galima atidaryti puslapiuose **Visi pardavimo užsakymai** ir **Klientų aptarnavimas**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-163">This page can be opened from the **All sales order** and **Customer service** pages.</span></span> <span data-ttu-id="b8c23-164">Sistema taip pat pakeičia užsakymo lauko **Išsami būsena** parametrą į **Sulaikymas dėl apgaulės**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-164">The system also updates the value of the **Detailed status** field for the order to **Fraud hold**.</span></span>

<span data-ttu-id="b8c23-165">Norėdami peržiūrėti ir tvarkyti užsakymus, kurie sulaikyti ir kuriuos reikia peržiūrėti dėl apgaulės, eikite į **Mažmeninė prekyba ir prekyba** \> **Klientai** \> **Užsakymo sulaikymas**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-165">To view and manage the orders that are on hold for fraud review, go to **Retail and Commerce** \> **Customers** \> **Order holds**.</span></span> <span data-ttu-id="b8c23-166">Puslapyje **Užsakymo sulaikymas** esančiame sąraše pasirinkite įrašą ir spustelėkite **Užsakymo sulaikymas**, kad pamatytumėte išsamesnį rodinį, kuriame pateikiama informacija apie sulaikymo priežastį.</span><span class="sxs-lookup"><span data-stu-id="b8c23-166">On the **Order holds** page, select an entry in the list, and then click **Order hold** to see a more detailed view that includes information about the reason for the hold.</span></span> <span data-ttu-id="b8c23-167">„FastTab“ **Apgaulės informacija** galite peržiūrėti sistemoje nustatytus apgaulės kriterijus, pagal kuriuos rasta atitikmenų užsakyme, ir pritaikytas rezultatų vertes.</span><span class="sxs-lookup"><span data-stu-id="b8c23-167">On the **Fraud details** FastTab, you can view the systematic fraud criteria that were found to be a match for the order and the scores that were applied.</span></span> <span data-ttu-id="b8c23-168">Jei užsakymas buvo sulaikytas rankiniu būdu, galite peržiūrėti užsakymą sulaikiusio vartotojo įvestus komentarus „FastTab“ **Pastabos** skyriuje **Apgaulės pastabos**.</span><span class="sxs-lookup"><span data-stu-id="b8c23-168">If the order was put on manual hold, you can review any comments that were entered by the user who put the order on hold by looking at the **Fraud notes** section on the **Notes** FastTab.</span></span>

<span data-ttu-id="b8c23-169">Daugiau informacijos apie tai, kaip dirbti su sulaikytais užsakymais, žr. [Užsakymo sulaikymas](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds).</span><span class="sxs-lookup"><span data-stu-id="b8c23-169">For more information about how to work with hold orders, see [Order holds](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds).</span></span>