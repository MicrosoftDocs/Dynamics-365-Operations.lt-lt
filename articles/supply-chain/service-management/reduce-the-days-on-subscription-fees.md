---
title: "Abonementinio mokesčio dienų sumažinimas"
description: "Norėdami sumažinti esamo abonementinio mokesčio dienų skaičių, galite sukurti naują operaciją, į kurią perkelsite laikotarpį, kuris turi nebebūti abonementinio mokesčio intervalo dalimi."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c70e393c125eecef85e8711d1635250f5ff408d9
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---


# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="5a124-103">Abonementinio mokesčio dienų sumažinimas</span><span class="sxs-lookup"><span data-stu-id="5a124-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5a124-104">Norėdami sumažinti esamo abonementinio mokesčio dienų skaičių, galite sukurti naują operaciją, į kurią perkelsite laikotarpį, kuris turi nebebūti abonementinio mokesčio intervalo dalimi.</span><span class="sxs-lookup"><span data-stu-id="5a124-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="5a124-105">Abonementinio mokesčio dienų sumažinimas</span><span class="sxs-lookup"><span data-stu-id="5a124-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="5a124-106">Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo abonementai** \> **Visi aptarnavimo abonementai**.</span><span class="sxs-lookup"><span data-stu-id="5a124-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="5a124-107">Pasirinkite aptarnavimo abonementas ir veiksmų srityje spustelėkite **Abonementiniai mokesčiai**</span><span class="sxs-lookup"><span data-stu-id="5a124-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="5a124-108">Lauke **Abonemento tipas** pasirinkite **Mažinimo dienos**.</span><span class="sxs-lookup"><span data-stu-id="5a124-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="5a124-109">Laukuose **Pradžios data** ir **Pabaigos data** nustatykite abonementinio mokesčio dienų intervalą, kurį norite pašalinti iš abonementinio mokesčio laikotarpio, ir spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5a124-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="5a124-110">Norėdami peržiūrėti sukurtą operaciją, formoje **Abonementas** spustelėkite **Mokesčių operacijos**.</span><span class="sxs-lookup"><span data-stu-id="5a124-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="5a124-111">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="5a124-111">Example</span></span>

<span data-ttu-id="5a124-112">Jei abonementinės operacijos laikotarpis trunka nuo sausio 1 d iki sausio 31 d., o jūs norite sumažinti šį laikotarpį 10 dienų, sukurkite naują operaciją, kurioje sumažinimo laikotarpis bus nuo sausio 1 d. iki sausio 10 d.</span><span class="sxs-lookup"><span data-stu-id="5a124-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="5a124-113">(Sumažinimo laikotarpis taip pat gali būti nuo sausio 5 d. iki sausio 15 d. arba bet kuris kitas dešimties dienų laikotarpis).</span><span class="sxs-lookup"><span data-stu-id="5a124-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="5a124-114">Be to, jei **Pradžios data** sumažinimo laikotarpyje yra sausio 21 d. (31 minus 10), kaip **Pabaigos datą** galite nustatyti bet kurią datą po sausio 31 d. ir vis tiek iš mokesčio operacijos laikotarpio bus pašalintos 10 dienų.</span><span class="sxs-lookup"><span data-stu-id="5a124-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a124-115">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="5a124-115">See also</span></span>

[<span data-ttu-id="5a124-116">Mažinimo dienų pavyzdys</span><span class="sxs-lookup"><span data-stu-id="5a124-116">Reduction days example</span></span>](reduction-days-example.md)

  



