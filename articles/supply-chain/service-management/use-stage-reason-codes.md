---
title: Etapo priežasties kodų naudojimas
description: Naudokite priežasties kodą, kad nurodytumėte, kodėl teikiamų paslaugų sutartis (SLA) buvo atšaukta arba kodėl viršijamas paslaugų užsakymo laiko limitas, nurodytas SLA.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 307e6b3e67de702135662e047aef00fd181d4749
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824251"
---
# <a name="use-stage-reason-codes"></a><span data-ttu-id="1646b-103">Etapo priežasties kodų naudojimas</span><span class="sxs-lookup"><span data-stu-id="1646b-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1646b-104">Naudokite priežasties kodą, kad nurodytumėte, kodėl teikiamų paslaugų sutartis (SLA) buvo atšaukta arba kodėl viršijamas paslaugų užsakymo laiko limitas, nurodytas SLA.</span><span class="sxs-lookup"><span data-stu-id="1646b-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="1646b-105">Jūs taip pat galite nurodyti, kad priežasties kodas yra reikalingas atšaukus SLA arba viršijus laiko limitą, nurodytą paslaugų užsakymo SLA.</span><span class="sxs-lookup"><span data-stu-id="1646b-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="1646b-106">Jei nurodėte, kad priežasties kodas yra reikalingas, reikia įvesti priežasties kodą toliau nurodytais atvejais.</span><span class="sxs-lookup"><span data-stu-id="1646b-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="1646b-107">Kai paslaugų užsakymas yra perkeliamas į etapą, kuriame paslaugų trukmės įrašymas yra stabdomas pagal SLA.</span><span class="sxs-lookup"><span data-stu-id="1646b-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="1646b-108">Kai aptarnavimo užsakymas yra baigtas.</span><span class="sxs-lookup"><span data-stu-id="1646b-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="1646b-109">Kai laiko įrašymas yra sustabdomas rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="1646b-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="1646b-110">Nustatyti priežasčių kodus</span><span class="sxs-lookup"><span data-stu-id="1646b-110">Set up reason codes</span></span>

1.  <span data-ttu-id="1646b-111">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo užsakymai** \> **Etapo priežasties kodai**.</span><span class="sxs-lookup"><span data-stu-id="1646b-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="1646b-112">Formoje **Etapo priežasties kodai** spustelėkite **Naujas**, kad sukurtumėte naują priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="1646b-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="1646b-113">Lauke **Etapo priežasties kodai** įveskite unikalųjį etapo priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="1646b-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="1646b-114">Lauke **Aprašas** įveskite etapo priežasties kodo aprašą.</span><span class="sxs-lookup"><span data-stu-id="1646b-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="1646b-115">Uždarę formą įrašysite savo pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="1646b-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="1646b-116">Priežasties kodų reikalavimas, kai atšaukiama aptarnavimo lygio sutartis</span><span class="sxs-lookup"><span data-stu-id="1646b-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="1646b-117">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1646b-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="1646b-118">Formoje **Aptarnavimo valdymo parametrai** spustelėkite nuorodą **Bendra**, tada pasirinkite žymės langelį **Atšaukimo priežasties kodas**.</span><span class="sxs-lookup"><span data-stu-id="1646b-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="1646b-119">Reikalavimas nurodyti priežasties kodus, kai viršijamas paslaugų užsakymo laiko limitas, nustatytas teikiamų paslaugų sutartyje</span><span class="sxs-lookup"><span data-stu-id="1646b-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="1646b-120">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1646b-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="1646b-121">Formoje **Aptarnavimo valdymo parametrai** spustelėkite nuorodą **Bendra**, tada pasirinkite žymės langelį **Laiko viršijimo priežasties kodas**.</span><span class="sxs-lookup"><span data-stu-id="1646b-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="1646b-122">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="1646b-122">See also</span></span>

[<span data-ttu-id="1646b-123">Aptarnavimo užsakymo laiko įrašymo pradžia ir sustabdymas</span><span class="sxs-lookup"><span data-stu-id="1646b-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]