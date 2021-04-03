---
title: Kanalo grąžinimo politikos kūrimas ir atnaujinimas
description: Šioje temoje pateikiama informacija apie tai, kaip sukonfigūruoti kanalo grąžinimo politiką.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 03e46a7f8d110bd9ef3b353b150116bbf8a70ad5
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478121"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="eebf6-103">Kanalo prekių ir pinigų grąžinimų strategijos kūrimas ir naujinimas</span><span class="sxs-lookup"><span data-stu-id="eebf6-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eebf6-104">Kanalo grąžinimo politika, esanti „Dynamics 365 Commerce“, suteikia galimybę mažmenininkams nustatyti vykdymo principus, pagal kuriuos gali būti leidžiama priimti grąžinimus elektroninio kasos aparato (EKA) įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="eebf6-104">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="eebf6-105">Šioje temoje aprašomi kanalo grąžinimo politikos sukonfigūravimo veiksmai.</span><span class="sxs-lookup"><span data-stu-id="eebf6-105">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="eebf6-106">Politikos taikymo sritis šiuo metu apsiriboja mokėjimo būdų, kurias galima leisti kanalui, nustatymu.</span><span class="sxs-lookup"><span data-stu-id="eebf6-106">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="eebf6-107">„Leidžiamų“ mokėjimo būdų sąrašas yra pagrįstas mokėjimo būdais, naudojamais įsigyjant prekes.</span><span class="sxs-lookup"><span data-stu-id="eebf6-107">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="eebf6-108">Pavyzdys:</span><span class="sxs-lookup"><span data-stu-id="eebf6-108">For example:</span></span>

- <span data-ttu-id="eebf6-109">Jei už prekes buvo sumokėta naudojant dovanų kortelę, parduotuvės politika yra grąžinti pinigus į naują dovanų kortelę arba išrašyti sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="eebf6-109">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="eebf6-110">Jei už prekes buvo sumokėta grynaisiais pinigais, galima grąžinti grynuosius pinigus, grąžinti pinigus į dovanų kortelę arba į kliento sąskaitą, bet ne į kredito kortelę.</span><span class="sxs-lookup"><span data-stu-id="eebf6-110">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="eebf6-111">Grąžinimo politikos įgalinimas</span><span class="sxs-lookup"><span data-stu-id="eebf6-111">Enable return policy</span></span>

<span data-ttu-id="eebf6-112">Norėdami įjungti kanalo grąžinimo politikos funkciją, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="eebf6-112">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="eebf6-113">Eikite į darbo sritį **Funkcijų valdymas**, esančią „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="eebf6-113">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="eebf6-114">Funkcijų pavadinimų sąraše ieškokite **Įgalinti kanalų grąžinimo politiką**.</span><span class="sxs-lookup"><span data-stu-id="eebf6-114">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="eebf6-115">Pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="eebf6-115">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="eebf6-116">Grąžinimo politikos sukonfigūravimas</span><span class="sxs-lookup"><span data-stu-id="eebf6-116">Configure return policy</span></span>

<span data-ttu-id="eebf6-117">Norėdami sukonfigūruoti mažmeninės parduotuvės ar internetinės mažmeninės prekybos parduotuvės kanalo grąžinimo politiką, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="eebf6-117">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="eebf6-118">Eikite į **„Retail and Commerce“** \> **Kanalo sąranka** \> **Grąžinimai** \> **Kanalo grąžinimo politika**.</span><span class="sxs-lookup"><span data-stu-id="eebf6-118">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="eebf6-119">Norėdami sukurti naują grąžinimo politikos šabloną, pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="eebf6-119">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="eebf6-120">Norėdami naudoti esamą šabloną, pasirinkite šabloną kairiojoje srityje.</span><span class="sxs-lookup"><span data-stu-id="eebf6-120">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="eebf6-121">Jei norite kurti naujus šablonus, pridėkite pavadinimą ir aprašą, kurie padės nustatyti politiką, kai ji taikoma kanalui.</span><span class="sxs-lookup"><span data-stu-id="eebf6-121">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="eebf6-122">![Pridėti naują grąžinimo politiką](media/Return-policy-page1.png "Pridėti naują grąžinimo politiką")</span><span class="sxs-lookup"><span data-stu-id="eebf6-122">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="eebf6-123">Skyriuje **„Leistini grąžinimo įmokos būdai“** apibrėžkite **Leistini** grąžinimo įmokų mokėjimo priemones, būdingas kiekvienam mokėjimo būdui.</span><span class="sxs-lookup"><span data-stu-id="eebf6-123">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="eebf6-124">![Pridėti mokėjimo būdą](media/Return-policy-page2.PNG "Leidžiamų mokėjimo būdų nustatymas kiekvienam mokėjimo tipui")</span><span class="sxs-lookup"><span data-stu-id="eebf6-124">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="eebf6-125">Mokėjimo būdai sukuriami iš organizacijai nustatytų mokėjimo būdų.</span><span class="sxs-lookup"><span data-stu-id="eebf6-125">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="eebf6-126">Pridėję leistiną grąžinimo mokėjimo būdo tipą kiekvienam nurodytam mokėjimo būdui, užtikrinsite, kad bus galima grąžinti leidžiamu grąžinimo būdu.</span><span class="sxs-lookup"><span data-stu-id="eebf6-126">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="eebf6-127">Susiekite grąžinimo politikos šabloną su parduotuvėmis, kuriose jis bus naudojamas.</span><span class="sxs-lookup"><span data-stu-id="eebf6-127">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="eebf6-128">Skirtuke **Mažmeninės prekybos kanalai** pasirinkite **Pridėti** ir susiekite galimus kanalus.</span><span class="sxs-lookup"><span data-stu-id="eebf6-128">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="eebf6-129">Dialogo lange **Pasirinkti organizacijos mazgus** pasirinkite parduotuves, regionus ir organizacijas, su kuriomis turėtų būti susietas šablonas.</span><span class="sxs-lookup"><span data-stu-id="eebf6-129">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="eebf6-130">Su kiekviena parduotuve galima susieti tik vieną grąžinimo politikos šabloną.</span><span class="sxs-lookup"><span data-stu-id="eebf6-130">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="eebf6-131">Pasirinkite parduotuves, regionus ar organizacijas naudodami rodyklių mygtukus.</span><span class="sxs-lookup"><span data-stu-id="eebf6-131">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="eebf6-132">Politikos įsigaliojimo data bus ta diena, kai politika bus taikoma kanalams ir bus vykdomos kanalo užduotys.</span><span class="sxs-lookup"><span data-stu-id="eebf6-132">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="eebf6-133">![Pasirinkti organizacijos mazgų dialogo langą](media/Return-policy-page3.PNG "Pasirinkti organizacijos mazgų dialogo langą")</span><span class="sxs-lookup"><span data-stu-id="eebf6-133">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="eebf6-134">Puslapyje **Pasiskirstymo grafikas** paleiskite **1070** užduotį, kad kanalo grąžinimo politika būtų prieinama EKA.</span><span class="sxs-lookup"><span data-stu-id="eebf6-134">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="eebf6-135">Peržiūrėkite kanalo grąžinimo politiką, esančią EKA</span><span class="sxs-lookup"><span data-stu-id="eebf6-135">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="eebf6-136">Jei norite pamatyti leistinus grąžinimo mokėjimo būdus, esančius EKA, atlikite veiksmus, pateiktus bet kuriame iš toliau nurodytų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="eebf6-136">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="eebf6-137">Prisijunkite prie EKA kaip kasininkas ar vadovas.</span><span class="sxs-lookup"><span data-stu-id="eebf6-137">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="eebf6-138">Skyriuje **Pamaina ir stalčius** pasirinkite **Rodyti žurnalą**.</span><span class="sxs-lookup"><span data-stu-id="eebf6-138">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="eebf6-139">Pasirinkite operaciją, kuri yra grąžinimo dalis.</span><span class="sxs-lookup"><span data-stu-id="eebf6-139">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="eebf6-140">Pasirinkite prekes, kurias norite grąžinti, ir pasirinkite mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="eebf6-140">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="eebf6-141">Jei pasirinktas mokėjimo būdas yra leidžiamų grąžinti būdų tipų sąraše, kasininkas gali atlikti grąžinimą.</span><span class="sxs-lookup"><span data-stu-id="eebf6-141">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="eebf6-142">Jei pasirinktas mokėjimo būdas neleidžiamas, rodomas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="eebf6-142">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="eebf6-143">Pasirinkite **Atlikti mokėjimą**, kad būtų parodytas visų leidžiamų grąžinimo būdų tipų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="eebf6-143">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="eebf6-144">Arba</span><span class="sxs-lookup"><span data-stu-id="eebf6-144">-or-</span></span>

1. <span data-ttu-id="eebf6-145">Prisijunkite prie EKA kaip kasininkas ar vadovas.</span><span class="sxs-lookup"><span data-stu-id="eebf6-145">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="eebf6-146">Pasirinkite **Grąžinimas** ir įveskite kvito ID, nuskaitydami brūkšninį kodą arba įvesdami jį rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="eebf6-146">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="eebf6-147">Pasirinkite operaciją, kuri yra grąžinimo dalis.</span><span class="sxs-lookup"><span data-stu-id="eebf6-147">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="eebf6-148">Pasirinkite prekes, kurias norite grąžinti, ir pasirinkite mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="eebf6-148">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="eebf6-149">Jei pasirinktas mokėjimo būdas yra leidžiamų grąžinti būdų tipų sąraše, kasininkas gali atlikti grąžinimą.</span><span class="sxs-lookup"><span data-stu-id="eebf6-149">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="eebf6-150">Jei pasirinktas mokėjimo būdas neleidžiamas, rodomas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="eebf6-150">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="eebf6-151">Pasirinkite **Atlikti mokėjimą**, kad būtų parodytas visų leidžiamų grąžinimo būdų tipų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="eebf6-151">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="eebf6-152">![Grąžinti negalima](media/Return-policy-page6.png "Blogas grąžinimo tipas")</span><span class="sxs-lookup"><span data-stu-id="eebf6-152">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="eebf6-153">![Mokėjimo būdų sąrašas](media/Return-policy-page5.PNG "Galimi grąžinimo tipai")</span><span class="sxs-lookup"><span data-stu-id="eebf6-153">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
