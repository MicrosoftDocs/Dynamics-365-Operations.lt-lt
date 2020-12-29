---
title: Aptarnavimo užduočių ryšių kūrimas
description: Aptarnavimo užduotis galima susieti su aptarnavimo sutartimis arba aptarnavimo užsakymais, siekiant aprašyti aptarnavimo užduotį, kurią reikia atlikti pagal sutartį arba užsakymą.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e50b4322c65097ab4f8aba9c36e4d5e6cc4c01b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433716"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="a004d-103">Aptarnavimo užduočių ryšių kūrimas</span><span class="sxs-lookup"><span data-stu-id="a004d-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a004d-104">Aptarnavimo užduotis galima susieti su aptarnavimo sutartimis arba aptarnavimo užsakymais, siekiant aprašyti aptarnavimo užduotį, kurią reikia atlikti pagal sutartį arba užsakymą.</span><span class="sxs-lookup"><span data-stu-id="a004d-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="a004d-105">Šią informaciją matys aptarnavimo technikai ir klientai.</span><span class="sxs-lookup"><span data-stu-id="a004d-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="a004d-106">Ryšio su aptarnavimo sutartimi kūrimas</span><span class="sxs-lookup"><span data-stu-id="a004d-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="a004d-107">Spustelėkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="a004d-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="a004d-108">Pasirinkite esamą aptarnavimo sutartį arba sukurkite naują.</span><span class="sxs-lookup"><span data-stu-id="a004d-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="a004d-109">Veiksmų srityje spustelėkite mygtuką **Aptarnavimo užduotys**.</span><span class="sxs-lookup"><span data-stu-id="a004d-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="a004d-110">Formoje **Aptarnavimo užduotys** paspaudę CTRL+N sukursite naują eilutę, tada iš sąrašo **Aptarnavimo užduotis** pasirinkite aptarnavimo užduotį ir prie aptarnavimo sutarties pridėkite aptarnavimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="a004d-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="a004d-111">Skirtuke **Aprašas** esančiuose laisvos formos teksto laukuose įveskite bet kurių vidinių ir išorinių pastabų aprašus.</span><span class="sxs-lookup"><span data-stu-id="a004d-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="a004d-112">Norėdami įrašyti įrašą, uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="a004d-112">Close the form to save the record.</span></span>

<span data-ttu-id="a004d-113">Šią procedūrą kartokite, kol sukursite visus reikalingus aptarnavimo sutarties užduočių ryšius.</span><span class="sxs-lookup"><span data-stu-id="a004d-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="a004d-114">Tada šias aptarnavimo užduotis galėsite nurodyti bet kuriose pridėtose sutarties eilutėse.</span><span class="sxs-lookup"><span data-stu-id="a004d-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="a004d-115">Aptarnavimo užduočių ryšys, sukurtas aptarnavimo užduotyje, prieinamas iš visų aptarnavimo užsakymų, pridėtų prie aptarnavimo sutarties.</span><span class="sxs-lookup"><span data-stu-id="a004d-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="a004d-116">Ryšio su aptarnavimo užsakymu kūrimas</span><span class="sxs-lookup"><span data-stu-id="a004d-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="a004d-117">Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="a004d-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="a004d-118">Pasirinkite esamą aptarnavimo užsakymą arba sukurkite naują.</span><span class="sxs-lookup"><span data-stu-id="a004d-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="a004d-119">Veiksmų srityje spustelėkite mygtuką **Aptarnavimo užduotys**.</span><span class="sxs-lookup"><span data-stu-id="a004d-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="a004d-120">Formoje **Aptarnavimo užduotys** paspaudę CTRL+N sukursite naują eilutę, tada iš sąrašo **Aptarnavimo užduotis** pasirinkite aptarnavimo užduotį ir prie aptarnavimo užsakymo pridėkite aptarnavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="a004d-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="a004d-121">Skirtuke **Aprašas** esančiuose laisvos formos teksto laukuose įveskite bet kurių vidinių ir išorinių pastabų aprašus.</span><span class="sxs-lookup"><span data-stu-id="a004d-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="a004d-122">Norėdami įrašyti įrašą, uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="a004d-122">Close the form to save the record.</span></span>

<span data-ttu-id="a004d-123">Šią procedūrą kartokite, kol sukursite visus reikalingus aptarnavimo sutarties užsakymo ryšius.</span><span class="sxs-lookup"><span data-stu-id="a004d-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="a004d-124">Tada, kurdami aptarnavimo užsakymo eilutes, galėsite pasirinkti aptarnavimo užduotis, kurioms sukūrėte ryšį.</span><span class="sxs-lookup"><span data-stu-id="a004d-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="a004d-125">Aptarnavimo užsakyme sukurti aptarnavimo užduočių ryšiai prieinami konkrečiame aptarnavimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="a004d-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="a004d-126">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="a004d-126">See also</span></span>

[<span data-ttu-id="a004d-127">Aptarnavimo užduočių apžvalga</span><span class="sxs-lookup"><span data-stu-id="a004d-127">Service tasks overview</span></span>](service-tasks.md)


  


