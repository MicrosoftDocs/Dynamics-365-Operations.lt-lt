---
title: Aptarnavimo užduočių ryšių kūrimas
description: Aptarnavimo užduotis galima susieti su aptarnavimo sutartimis arba aptarnavimo užsakymais, siekiant aprašyti aptarnavimo užduotį, kurią reikia atlikti pagal sutartį arba užsakymą.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2aa0e5200ff2a6822e631c72124335e2dc556c14
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552120"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="86831-103">Aptarnavimo užduočių ryšių kūrimas</span><span class="sxs-lookup"><span data-stu-id="86831-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86831-104">Aptarnavimo užduotis galima susieti su aptarnavimo sutartimis arba aptarnavimo užsakymais, siekiant aprašyti aptarnavimo užduotį, kurią reikia atlikti pagal sutartį arba užsakymą.</span><span class="sxs-lookup"><span data-stu-id="86831-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="86831-105">Šią informaciją matys aptarnavimo technikai ir klientai.</span><span class="sxs-lookup"><span data-stu-id="86831-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="86831-106">Ryšio su aptarnavimo sutartimi kūrimas</span><span class="sxs-lookup"><span data-stu-id="86831-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="86831-107">Spustelėkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="86831-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="86831-108">Pasirinkite esamą aptarnavimo sutartį arba sukurkite naują.</span><span class="sxs-lookup"><span data-stu-id="86831-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="86831-109">Veiksmų srityje spustelėkite mygtuką **Aptarnavimo užduotys**.</span><span class="sxs-lookup"><span data-stu-id="86831-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="86831-110">Formoje **Aptarnavimo užduotys** paspaudę CTRL+N sukursite naują eilutę, tada iš sąrašo **Aptarnavimo užduotis** pasirinkite aptarnavimo užduotį ir prie aptarnavimo sutarties pridėkite aptarnavimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="86831-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="86831-111">Skirtuke **Aprašas** esančiuose laisvos formos teksto laukuose įveskite bet kurių vidinių ir išorinių pastabų aprašus.</span><span class="sxs-lookup"><span data-stu-id="86831-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="86831-112">Norėdami įrašyti įrašą, uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="86831-112">Close the form to save the record.</span></span>

<span data-ttu-id="86831-113">Šią procedūrą kartokite, kol sukursite visus reikalingus aptarnavimo sutarties užduočių ryšius.</span><span class="sxs-lookup"><span data-stu-id="86831-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="86831-114">Tada šias aptarnavimo užduotis galėsite nurodyti bet kuriose pridėtose sutarties eilutėse.</span><span class="sxs-lookup"><span data-stu-id="86831-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="86831-115">Aptarnavimo užduočių ryšys, sukurtas aptarnavimo užduotyje, prieinamas iš visų aptarnavimo užsakymų, pridėtų prie aptarnavimo sutarties.</span><span class="sxs-lookup"><span data-stu-id="86831-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="86831-116">Ryšio su aptarnavimo užsakymu kūrimas</span><span class="sxs-lookup"><span data-stu-id="86831-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="86831-117">Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="86831-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="86831-118">Pasirinkite esamą aptarnavimo užsakymą arba sukurkite naują.</span><span class="sxs-lookup"><span data-stu-id="86831-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="86831-119">Veiksmų srityje spustelėkite mygtuką **Aptarnavimo užduotys**.</span><span class="sxs-lookup"><span data-stu-id="86831-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="86831-120">Formoje **Aptarnavimo užduotys** paspaudę CTRL+N sukursite naują eilutę, tada iš sąrašo **Aptarnavimo užduotis** pasirinkite aptarnavimo užduotį ir prie aptarnavimo užsakymo pridėkite aptarnavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="86831-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="86831-121">Skirtuke **Aprašas** esančiuose laisvos formos teksto laukuose įveskite bet kurių vidinių ir išorinių pastabų aprašus.</span><span class="sxs-lookup"><span data-stu-id="86831-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="86831-122">Norėdami įrašyti įrašą, uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="86831-122">Close the form to save the record.</span></span>

<span data-ttu-id="86831-123">Šią procedūrą kartokite, kol sukursite visus reikalingus aptarnavimo sutarties užsakymo ryšius.</span><span class="sxs-lookup"><span data-stu-id="86831-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="86831-124">Tada, kurdami aptarnavimo užsakymo eilutes, galėsite pasirinkti aptarnavimo užduotis, kurioms sukūrėte ryšį.</span><span class="sxs-lookup"><span data-stu-id="86831-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="86831-125">Aptarnavimo užsakyme sukurti aptarnavimo užduočių ryšiai prieinami konkrečiame aptarnavimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="86831-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="86831-126">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="86831-126">See also</span></span>

[<span data-ttu-id="86831-127">Aptarnavimo užduotys</span><span class="sxs-lookup"><span data-stu-id="86831-127">Service tasks</span></span>](service-tasks.md)


  


