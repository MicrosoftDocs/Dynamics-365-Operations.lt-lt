---
title: "Adreso įtraukimas į aptarnavimo užsakymą"
description: "Šioje temoje aprašoma, kaip įtraukti kliento adresą į aptarnavimo užsakymą."
author: YuyuScheller
manager: AnnBe
ms.date: 05/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
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
ms.openlocfilehash: e6dfa27b2101e84fbab678e781c26126cf1db898
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="19daa-103">Adreso įtraukimas į aptarnavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="19daa-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="19daa-104">Šioje temoje aprašoma, kaip įtraukti kliento adresą į aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="19daa-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="19daa-105">Kai kuriate aptarnavimo užsakymą, adreso informacija yra perkeliama iš projekto, prie kurio yra pridėtas aptarnavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="19daa-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="19daa-106">Tačiau klientams, tiekėjams, vietoms, sandėliams, aptarnavimo užsakymams ir projektams galite pasirinkti alternatyvią vietą iš adresų, kurie jau yra įtraukti į „Microsoft Dynamics AX“.</span><span class="sxs-lookup"><span data-stu-id="19daa-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="19daa-107">Taip pat galite kurti naują adresą.</span><span class="sxs-lookup"><span data-stu-id="19daa-107">You can also create a new address.</span></span> <span data-ttu-id="19daa-108">Pagal numatytuosius nustatymus naujas adresas yra perkeliamas į projektą.</span><span class="sxs-lookup"><span data-stu-id="19daa-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="19daa-109">Tačiau galite nurodyti, kad naujasis adresas būtų taikomas tik šiam aptarnavimo atvejui.</span><span class="sxs-lookup"><span data-stu-id="19daa-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="19daa-110">Jei tai padarysite, naujasis adresas nebus perkeliamas į projektą.</span><span class="sxs-lookup"><span data-stu-id="19daa-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="19daa-111">Kliento adreso kūrimas aptarnavimo užsakymui</span><span class="sxs-lookup"><span data-stu-id="19daa-111">Create a customer address for a service order</span></span>

<span data-ttu-id="19daa-112">Norėdami įtraukti adresą į aptarnavimo užsakymą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="19daa-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="19daa-113">Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="19daa-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="19daa-114">Atidarykite aptarnavimo užsakymą, kuriam norite sukurti adresą.</span><span class="sxs-lookup"><span data-stu-id="19daa-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="19daa-115">Dalyje **Veiksmų sritis**, spustelėkite **Redaguoti**, tada spustelėkite **Antraštės rodinys**.</span><span class="sxs-lookup"><span data-stu-id="19daa-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="19daa-116">Dalies **Adresas** „FastTab“ spustelėkite **Pridėti adresą**.</span><span class="sxs-lookup"><span data-stu-id="19daa-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="19daa-117">Formoje **Naujas adresas** įveskite unikalų adreso pavadinimą ir užpildykite likusius laukus.</span><span class="sxs-lookup"><span data-stu-id="19daa-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="19daa-118">Jei įvesite tą patį pavadinimą kaip esamo adreso, informacija, kurią įvedate likusiuose laukuose, perrašys esamo adreso informaciją.</span><span class="sxs-lookup"><span data-stu-id="19daa-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="19daa-119">Spustelėkite **Gerai**, kad nukopijuotumėte naują adresą į aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="19daa-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="19daa-120">Alternatyvaus adreso nurodymas aptarnavimo užsakyme</span><span class="sxs-lookup"><span data-stu-id="19daa-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="19daa-121">Norėdami įtraukti alternatyvų adresą į aptarnavimo užsakymą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="19daa-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="19daa-122">Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="19daa-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="19daa-123">Atidarykite aptarnavimo užsakymą, kuriame norite įvesti alternatyvų adresą.</span><span class="sxs-lookup"><span data-stu-id="19daa-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="19daa-124">Dalyje **Veiksmų sritis**, spustelėkite **Redaguoti**, tada spustelėkite **Antraštės rodinys**.</span><span class="sxs-lookup"><span data-stu-id="19daa-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="19daa-125">Dalies **Adresas** „FastTab“ spustelėkite **Kiti adresai**.</span><span class="sxs-lookup"><span data-stu-id="19daa-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="19daa-126">Formos **Adreso pasirinkimas** lauke **Įrašo tipas** pasirinkite **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="19daa-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="19daa-127">Pasirinkite adresą, tada spustelėkite **Gerai**, kad nukopijuotumėte jį į aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="19daa-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  



