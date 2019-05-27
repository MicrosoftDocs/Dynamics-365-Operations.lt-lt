---
title: Aptarnavimo sutartys
description: Aptarnavimo sutartys leidžia nustatyti išteklius, kurie bus naudojami įprasto aptarnavimo vizito metu, ir kaip už šiuos išteklius bus išrašoma sąskaita klientui.
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6425dcf1c89f625d997be0dd4a52aaecb6e6d65
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568286"
---
# <a name="service-agreements"></a><span data-ttu-id="b9b13-103">Aptarnavimo sutartys</span><span class="sxs-lookup"><span data-stu-id="b9b13-103">Service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9b13-104">Aptarnavimo sutartys leidžia nustatyti išteklius, kurie bus naudojami įprasto aptarnavimo vizito metu, ir kaip už šiuos išteklius bus išrašoma sąskaita klientui.</span><span class="sxs-lookup"><span data-stu-id="b9b13-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="b9b13-105">Kiekviena aptarnavimo sutartis yra pridėta prie projekto, kurio operacijos registruojamos ir už jas išrašomos sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="b9b13-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="b9b13-106">Tačiau sąskaitas už aptarnavimo užsakymo operacijas galima išrašyti ir tiesiogiai per projektą – ir tam nereikės iš pradžių prijungti aptarnavimo užsakymo prie aptarnavimo sutarties.</span><span class="sxs-lookup"><span data-stu-id="b9b13-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="b9b13-107">Galite nuspręsti taip daryti, jei aptarnavimo užsakymas yra sukurtas tik vienkartiniam aptarnavimo vizitui, o poreikis greitai apdoroti aptarnavimo operacijas yra svarbesnis už poreikį prižiūrėti, kad aptarnavimo sutarties informacija apie klientą per tam tikrą laikotarpį būtų išsami.</span><span class="sxs-lookup"><span data-stu-id="b9b13-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="b9b13-108">Aptarnavimo sutartis</span><span class="sxs-lookup"><span data-stu-id="b9b13-108">Service agreement</span></span>

<span data-ttu-id="b9b13-109">Kiekvienoje aptarnavimo sutartyje reikia nustatyti projektą, aptarnavimo sutarties ID ir aptarnavimo sutarčių grupę.</span><span class="sxs-lookup"><span data-stu-id="b9b13-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="b9b13-110">Aptarnavimo sutarčių grupė gali būti naudojama aptarnavimo sutartims rūšiuoti ir organizuoti.</span><span class="sxs-lookup"><span data-stu-id="b9b13-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="b9b13-111">Aptarnavimo sutarties antraštėje yra parametrai, taikomi visoms pridėtoms sutarties eilutėms:</span><span class="sxs-lookup"><span data-stu-id="b9b13-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="b9b13-112">Ar aptarnavimo sutartis yra sustabdyta.</span><span class="sxs-lookup"><span data-stu-id="b9b13-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="b9b13-113">Jei aptarnavimo sutartis yra sustabdyta, iš jos negalima generuoti aptarnavimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="b9b13-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="b9b13-114">Aptarnavimo sutarties trukmė.</span><span class="sxs-lookup"><span data-stu-id="b9b13-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="b9b13-115">Kaip aptarnavimo užsakymo eilutės jungiamos į aptarnavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="b9b13-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="b9b13-116">Ar aptarnavimo sutartis yra šablonas.</span><span class="sxs-lookup"><span data-stu-id="b9b13-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="b9b13-117">Aptarnavimo sutarties antraštėje taip pat galite nustatyti visus aptarnavimo objektus ir aptarnavimo užduotis, kuriuos bus galima naudoti su aptarnavimo sutartimi, įvedę konkrečias aptarnavimo užduotis ar aptarnavimo objektus, kurie turi būti pridėti prie įvairių sutarties eilučių.</span><span class="sxs-lookup"><span data-stu-id="b9b13-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="b9b13-118">Iš aptarnavimo sutarties antraštės taip pat galima nukopijuoti aptarnavimo sutarties eilutes arba aptarnavimo šablono eilutes į dabartinę aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="b9b13-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="b9b13-119">Galima laikinai sustabdyti aptarnavimo sutartis ir sustabdyti atskiras aptarnavimo sutarties eilutes.</span><span class="sxs-lookup"><span data-stu-id="b9b13-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="b9b13-120">Aptarnavimo sutartyje pažymėję žymės langelį **Laikinai sustabdyta**, negalėsite:</span><span class="sxs-lookup"><span data-stu-id="b9b13-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="b9b13-121">Iš aptarnavimo sutarties automatiškai arba rankiniu būdu sukurti aptarnavimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="b9b13-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="b9b13-122">Aptarnavimo sutarties eilutėje pažymėję žymės langelį **Sustabdyta**, negalėsite:</span><span class="sxs-lookup"><span data-stu-id="b9b13-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="b9b13-123">Iš aptarnavimo sutarties eilutės automatiškai arba rankiniu būdu sukurti aptarnavimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="b9b13-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="b9b13-124">Nukopijuoti aptarnavimo sutarties eilutę į kitą aptarnavimo sutartį arba aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b9b13-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="b9b13-125">Jei aptarnavimo sutartis laikinai sustabdoma, visos pridėtos eilutės sustabdomos, neatsižvelgiant į jų būseną.</span><span class="sxs-lookup"><span data-stu-id="b9b13-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="b9b13-126">Aptarnavimo sutarties eilutės</span><span class="sxs-lookup"><span data-stu-id="b9b13-126">Service-agreement lines</span></span>

<span data-ttu-id="b9b13-127">Kiekviena aptarnavimo sutarties eilutė išsamiai aprašo siūlomo aptarnavimo darbo turinį.</span><span class="sxs-lookup"><span data-stu-id="b9b13-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="b9b13-128">Eilutėse yra tokie parametrai:</span><span class="sxs-lookup"><span data-stu-id="b9b13-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="b9b13-129">Operacijos tipas ir operacijos tipo aprašymas.</span><span class="sxs-lookup"><span data-stu-id="b9b13-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="b9b13-130">Aptarnavimo darbą atliekantis darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="b9b13-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="b9b13-131">Objektai, kuriems turi būti atliekamas aptarnavimas pagal aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="b9b13-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="b9b13-132">Užregistruojamas dažnumas, kuriuo atliekamas darbas, ir užregistruojamos susijusios prekės, išlaidų ir mokesčių operacijos.</span><span class="sxs-lookup"><span data-stu-id="b9b13-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="b9b13-133">Laiko langas, per kurį aptarnavimo užsakymo eilutės gali būti sugrupuotos į aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b9b13-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="b9b13-134">Aptarnavimo užduotys, naudojamos sutarties eilučių rinkiniams į darbo užduotis grupuoti ir pateikti aptarnavimo technikams bei klientams apibendrintą informaciją, kokia aptarnavimo užduotis turi būti atlikta.</span><span class="sxs-lookup"><span data-stu-id="b9b13-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="b9b13-135">Ar eilutė sustabdyta.</span><span class="sxs-lookup"><span data-stu-id="b9b13-135">Whether a line is stopped.</span></span> <span data-ttu-id="b9b13-136">Jei eilutė sustabdyta, negalima sukurti aptarnavimo užsakymų tai atskirai eilutei.</span><span class="sxs-lookup"><span data-stu-id="b9b13-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="b9b13-137">Projekto parametrai, pvz., kategorija ir eilutės ypatybė.</span><span class="sxs-lookup"><span data-stu-id="b9b13-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9b13-138">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="b9b13-138">Related topics</span></span>

[<span data-ttu-id="b9b13-139">Aptarnavimo sutarčių kūrimas</span><span class="sxs-lookup"><span data-stu-id="b9b13-139">Create service agreements</span></span>](create-service-agreements.md)
