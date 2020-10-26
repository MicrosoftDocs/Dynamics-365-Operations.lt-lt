---
title: Aptarnavimo lygio sutarčių apžvalga
description: Teikiamų paslaugų sutartyje klientas sutinka su minimaliu atsiliepimo laiku, kuris remiasi laiku, nuo to, kai aptarnavimo įmonė užregistruoja problemą, iki tol, kai problema išsprendžiama.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01cdfe519e55ca2a9aa17f4ac181ee675b2793cf
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982360"
---
# <a name="service-level-agreements-overview"></a><span data-ttu-id="410e9-103">Aptarnavimo lygio sutarčių apžvalga</span><span class="sxs-lookup"><span data-stu-id="410e9-103">Service level agreements overview</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="410e9-104">Aptarnavimo lygio sutartis (ALS) yra sutartis tarp aptarnavimo įmonės ir kliento.</span><span class="sxs-lookup"><span data-stu-id="410e9-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="410e9-105">ALS klientas sutinka su minimaliu atsiliepimo laiku, kuris remiasi laiku, nuo to, kai aptarnavimo įmonė užregistruoja problemą iki tol, kai problema išsprendžiama.</span><span class="sxs-lookup"><span data-stu-id="410e9-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="410e9-106">ALS suteikia standartinio lygio klientams siūlomą aptarnavimą, taip pat aiškiai nurodo aptarnavimo įmonei, kada turi būti baigta aptarnavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="410e9-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="410e9-107">Norint pasiūlyti klientams skirtingus aptarnavimo lygius, gali būti sukurtas bet koks ALS skaičius.</span><span class="sxs-lookup"><span data-stu-id="410e9-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="410e9-108">Kurti aptarnavimo sutartį</span><span class="sxs-lookup"><span data-stu-id="410e9-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="410e9-109">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo sutartys** \> **Aptarnavimo lygio sutartys**.</span><span class="sxs-lookup"><span data-stu-id="410e9-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="410e9-110">Lauke **Aptarnavimo lygio sutartis** įveskite aptarnavimo lygio sutarties pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="410e9-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="410e9-111">Įveskite laiką, per kurį norite, kad būtų atlikti prie aptarnavimo lygio sutarties pridėti aptarnavimo skambučiai.</span><span class="sxs-lookup"><span data-stu-id="410e9-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="410e9-112">Po to, jei norite, kad aptarnavimo lygio sutartis būtų grįsta tam tikru kalendoriumi, pasirinkite kalendorių.</span><span class="sxs-lookup"><span data-stu-id="410e9-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="410e9-113">Taikyti aptarnavimo lygio sutartį</span><span class="sxs-lookup"><span data-stu-id="410e9-113">Apply a service level agreement</span></span>

<span data-ttu-id="410e9-114">ALS taikoma tiesiogiai aptarnavimo sutarčiai.</span><span class="sxs-lookup"><span data-stu-id="410e9-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="410e9-115">Aptarnavimo užsakymai, kuriuos kuriate patys ir pridedate prie aptarnavimo sutarties ir kurie turi ALS, yra lyginami su šia ALS.</span><span class="sxs-lookup"><span data-stu-id="410e9-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="410e9-116">Aptarnavimo užsakymai, kuriuos jūs sukuriate automatiškai, prie ALS nepridedami.</span><span class="sxs-lookup"><span data-stu-id="410e9-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="410e9-117">Taikyti aptarnavimo lygio sutartį aptarnavimo sutarčiai</span><span class="sxs-lookup"><span data-stu-id="410e9-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="410e9-118">Spustelėkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="410e9-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="410e9-119">Pasirinkite aptarnavimo sutartį, kuriai norite taikyti ALS, po to srityje **Veiksmų sritis** spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="410e9-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="410e9-120">Lauke **Aptarnavimo lygio sutartis** pasirinkite norimą priskirti ASL.</span><span class="sxs-lookup"><span data-stu-id="410e9-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="410e9-121">Taikyti aptarnavimo lygio sutartį aptarnavimo sutarties grupei</span><span class="sxs-lookup"><span data-stu-id="410e9-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="410e9-122">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutarčių grupės**.</span><span class="sxs-lookup"><span data-stu-id="410e9-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="410e9-123">Lauke **Aptarnavimo lygio sutartis** pasirinkite norimą priskirti ASL.</span><span class="sxs-lookup"><span data-stu-id="410e9-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="410e9-124">Sekimo laikas aptarnavimo užsakyme nuo ALS</span><span class="sxs-lookup"><span data-stu-id="410e9-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="410e9-125">Sukūrus naują aptarnavimo sutarties, kuriai priskirta ALS, aptarnavimo užsakymą sukuriamas paslaugų suteikimo laiko intervalas ir sistema pradeda sekti paslaugų suteikimo laiką.</span><span class="sxs-lookup"><span data-stu-id="410e9-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="410e9-126">Be to, galite nustatyti toliau nurodytas pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="410e9-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="410e9-127">Jūs galite pradėti ir sustabdyti laiko įrašymą aptarnavimo užsakyme, norėdami registruoti laiko, praleisto aptarnavimo užsakymams, sumą.</span><span class="sxs-lookup"><span data-stu-id="410e9-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="410e9-128">Galite stebėti, ar yra laikomasi aptarnavimo lygio sutartyje nustatyto laiko intervalo.</span><span class="sxs-lookup"><span data-stu-id="410e9-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="410e9-129">Galite nurodyti priežasties kodus, kurie turi būti nustatyti, jei viršijamas aptarnavimo lygio sutarties laiko intervalas.</span><span class="sxs-lookup"><span data-stu-id="410e9-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="410e9-130">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="410e9-130">See also</span></span>

[<span data-ttu-id="410e9-131">Aptarnavimo lygio sutarčių atitikimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="410e9-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


