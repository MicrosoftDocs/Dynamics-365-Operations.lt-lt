---
title: Kaupimo abonementai
description: Naudodami aptarnavimo abonementus, rankiniu būdu sukaupiate įplaukas laikotarpiuose po datos, kai išrašėte SF apmokėjimo operacijai.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ebd65655db56ee1169f24dbc79fbfb5130f06a5
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978826"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="5ef3d-103">Kaupimo abonementai</span><span class="sxs-lookup"><span data-stu-id="5ef3d-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5ef3d-104">Naudodami aptarnavimo abonementus, rankiniu būdu sukaupiate įplaukas laikotarpiuose po datos, kai išrašėte SF apmokėjimo operacijai.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="5ef3d-105">Kaupimo laikotarpiai kuriami SF laikotarpiui, nurodytam abonemento apmokėjime ir kaupimo laikotarpiai yra paremti abonemento laikotarpio kodu.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="5ef3d-106">Galite kaupti ir grąžinti sukauptas įplaukas.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="5ef3d-107">Atšaukti kredito sumų kaupimus</span><span class="sxs-lookup"><span data-stu-id="5ef3d-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="5ef3d-108">Jei priskyrėte abonemento sumas, kurioms išrašytos SF, galite naudoti du metodus kaupimo sumoms atšaukti:</span><span class="sxs-lookup"><span data-stu-id="5ef3d-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="5ef3d-109">Galite atšaukti kiekvieną sukauptų įplaukų operaciją atskirai prieš sukurdami operacijos kredito pažymos pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="5ef3d-110">Tai rankinis metodas.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-110">This is the manual method.</span></span> <span data-ttu-id="5ef3d-111">(rankinis)</span><span class="sxs-lookup"><span data-stu-id="5ef3d-111">(manual)</span></span>

  - <span data-ttu-id="5ef3d-112">Galima nustatyti, kad sukauptos sumos būtų atšauktos tą dieną, kai užregistruojama kredito pažyma, arba tikrąją kaupimo registravimo dieną.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="5ef3d-113">Daugiau informacijos rasite [Abonemento parametrai (forma)](https://technet.microsoft.com/library/aa619615.aspx).</span><span class="sxs-lookup"><span data-stu-id="5ef3d-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="5ef3d-114">Nustatyti reikalavimus</span><span class="sxs-lookup"><span data-stu-id="5ef3d-114">Setup requirements</span></span>

<span data-ttu-id="5ef3d-115">Norėdami kaupti įplaukas, įsitikinkite, kad šie duomenų reikalavimai atitinka pateiktus:</span><span class="sxs-lookup"><span data-stu-id="5ef3d-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="5ef3d-116">Abonento nustatymas</span><span class="sxs-lookup"><span data-stu-id="5ef3d-116">Account setup</span></span>

<span data-ttu-id="5ef3d-117">**NG – abonementas** ir **Sukauptos įplaukos – abonementas** sumos turi būti nustatytos modulyje **Projektas**.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="5ef3d-118">Registruojant sukauptas įplaukas, nuo sąskaitos **NG – abonementas** nurašoma sukaupta suma ir į sąskaitą **Sukauptos įplaukos – abonementas** įrašoma sukaupta suma.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="5ef3d-119">Nustatyti sąskaitas sukauptoms abonementų įplaukoms</span><span class="sxs-lookup"><span data-stu-id="5ef3d-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="5ef3d-120">Spustelėkite **Projektų valdymas ir apskaita** \> **Nustatymas** \> **Registravimas** \> **Registravimo DK nustatymai**.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="5ef3d-121">Spustelėkite skirtuką **Įplaukų sąskaitos** ir pasirinkite **NG – abonementas** arba **Sukauptos įplaukos – abonementas** norėdami nustatyti sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="5ef3d-122">Abonementų grupės nustatymas</span><span class="sxs-lookup"><span data-stu-id="5ef3d-122">Subscription group setup</span></span>

<span data-ttu-id="5ef3d-123">Kad būtų galima kaupti įplaukas abonementams, turi būti pažymėtas žymės langelis **Kaupti įplaukas**.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="5ef3d-124">Tai rasite tos grupės, kuri susieta su abonementu, formoje **Abonementų grupės**.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="5ef3d-125">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo abonementai** \> **Abonementų grupės**.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="5ef3d-126">Įplaukų abonementų grupėje kaupimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="5ef3d-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="5ef3d-127">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo abonementai** \> **Abonementų grupės**.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="5ef3d-128">Laikotarpiai</span><span class="sxs-lookup"><span data-stu-id="5ef3d-128">Periods</span></span>

<span data-ttu-id="5ef3d-129">Turite nustatyti apskaitomo laikotarpio kodą.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="5ef3d-130">Išskyrus atvejį, kai norite kaupti įplaukas tuose pačiuose laiko intervaluose, kaip ir sąskaitų faktūrų išrašymo atveju, taip pat turite nustatyti kaupimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="5ef3d-131">Toliau pateiktoje lentelėje rasite sąrašą kaupimo laikotarpių, kuriuos galite nustatyti kiekvienam apskaitos laikotarpiui:</span><span class="sxs-lookup"><span data-stu-id="5ef3d-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ef3d-132">SF išrašymo laikotarpis</span><span class="sxs-lookup"><span data-stu-id="5ef3d-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="5ef3d-133">Kaupimo laikotarpis</span><span class="sxs-lookup"><span data-stu-id="5ef3d-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ef3d-134"><strong>Metai</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="5ef3d-135"><strong>Metai</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="5ef3d-136"><strong>Ketvirtis</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="5ef3d-137"><strong>Mėnuo</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="5ef3d-138"><strong>Diena</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ef3d-139"><strong>Ketvirtis</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="5ef3d-140"><strong>Ketvirtis</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="5ef3d-141"><strong>Mėnuo</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="5ef3d-142"><strong>Diena</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ef3d-143"><strong>Mėnuo</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="5ef3d-144"><strong>Mėnuo</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="5ef3d-145"><strong>Diena</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ef3d-146"><strong>Savaitė</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="5ef3d-147"><strong>Diena</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ef3d-148"><strong>Diena</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="5ef3d-149"><strong>Diena</strong></span><span class="sxs-lookup"><span data-stu-id="5ef3d-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef3d-150">SF išrašymo laikotarpio nustatymas yra privaloma visos abonementų grupės nustatymo dalis.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="5ef3d-151">Galite nuspręsti, ar nustatyti ir abonementų grupės kaupimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="5ef3d-152">Jei nustatysite abonementų grupės kaupimo laikotarpį, šis laikotarpis bus pasiūlytas lauke **Laikotarpio kodas**.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="5ef3d-153">Šį lauką rasite formoje **Kaupti abonemento įplaukas**, kai kaupiate abonemento įplaukas.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="5ef3d-154">Tačiau kaupimo laikotarpis yra pasirenkama informacija apie abonementų grupę.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5ef3d-155">Naudodami šį maršrutą atidarykite formą <STRONG>Kaupti abonemento įplaukas</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="5ef3d-156">Spustelėkite <STRONG>Aptarnavimo valdymas</STRONG> &gt; <STRONG>Periodinis</STRONG> &gt; <STRONG>Aptarnavimo abonementai</STRONG> &gt; <STRONG>Kaupti abonemento įplaukas</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="5ef3d-157">Operacijos</span><span class="sxs-lookup"><span data-stu-id="5ef3d-157">Transactions</span></span>

<span data-ttu-id="5ef3d-158">Galite valdyti DK operacijų, sukurtų registruojant sukauptas įplaukas, skaičių.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="5ef3d-159">Abonementuose nurodykite, ar DK operacijos turi būti sukurtos kaip suma, ar vienoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="5ef3d-160">Nurodykite rodomą sukauptų operacijų registravimo informacijos lygį</span><span class="sxs-lookup"><span data-stu-id="5ef3d-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="5ef3d-161">Spustelėkite **Projektų valdymas ir apskaita** \> **Sąranka** \> **Projektų valdymo ir apskaitos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="5ef3d-162">Skirtuke **Finansinis**, esančiame lauke **Sąskaita faktūra**, pasirinkite **Bendroji suma** arba **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="5ef3d-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="5ef3d-163">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="5ef3d-163">See also</span></span>

[<span data-ttu-id="5ef3d-164">Kaupti abonemento įplaukas</span><span class="sxs-lookup"><span data-stu-id="5ef3d-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  


