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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e5fd978c1e9db7e7ce3c06bbeb45b59854f1582
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974665"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="d745f-103">Aptarnavimo užduočių ryšių kūrimas</span><span class="sxs-lookup"><span data-stu-id="d745f-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d745f-104">Aptarnavimo užduotis galima susieti su aptarnavimo sutartimis arba aptarnavimo užsakymais, siekiant aprašyti aptarnavimo užduotį, kurią reikia atlikti pagal sutartį arba užsakymą.</span><span class="sxs-lookup"><span data-stu-id="d745f-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="d745f-105">Šią informaciją matys aptarnavimo technikai ir klientai.</span><span class="sxs-lookup"><span data-stu-id="d745f-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="d745f-106">Ryšio su aptarnavimo sutartimi kūrimas</span><span class="sxs-lookup"><span data-stu-id="d745f-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="d745f-107">Spustelėkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="d745f-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="d745f-108">Pasirinkite esamą aptarnavimo sutartį arba sukurkite naują.</span><span class="sxs-lookup"><span data-stu-id="d745f-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="d745f-109">Veiksmų srityje spustelėkite mygtuką **Aptarnavimo užduotys**.</span><span class="sxs-lookup"><span data-stu-id="d745f-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="d745f-110">Formoje **Aptarnavimo užduotys** paspaudę CTRL+N sukursite naują eilutę, tada iš sąrašo **Aptarnavimo užduotis** pasirinkite aptarnavimo užduotį ir prie aptarnavimo sutarties pridėkite aptarnavimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="d745f-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="d745f-111">Skirtuke **Aprašas** esančiuose laisvos formos teksto laukuose įveskite bet kurių vidinių ir išorinių pastabų aprašus.</span><span class="sxs-lookup"><span data-stu-id="d745f-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="d745f-112">Norėdami įrašyti įrašą, uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="d745f-112">Close the form to save the record.</span></span>

<span data-ttu-id="d745f-113">Šią procedūrą kartokite, kol sukursite visus reikalingus aptarnavimo sutarties užduočių ryšius.</span><span class="sxs-lookup"><span data-stu-id="d745f-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="d745f-114">Tada šias aptarnavimo užduotis galėsite nurodyti bet kuriose pridėtose sutarties eilutėse.</span><span class="sxs-lookup"><span data-stu-id="d745f-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="d745f-115">Aptarnavimo užduočių ryšys, sukurtas aptarnavimo užduotyje, prieinamas iš visų aptarnavimo užsakymų, pridėtų prie aptarnavimo sutarties.</span><span class="sxs-lookup"><span data-stu-id="d745f-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="d745f-116">Ryšio su aptarnavimo užsakymu kūrimas</span><span class="sxs-lookup"><span data-stu-id="d745f-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="d745f-117">Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="d745f-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="d745f-118">Pasirinkite esamą aptarnavimo užsakymą arba sukurkite naują.</span><span class="sxs-lookup"><span data-stu-id="d745f-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="d745f-119">Veiksmų srityje spustelėkite mygtuką **Aptarnavimo užduotys**.</span><span class="sxs-lookup"><span data-stu-id="d745f-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="d745f-120">Formoje **Aptarnavimo užduotys** paspaudę CTRL+N sukursite naują eilutę, tada iš sąrašo **Aptarnavimo užduotis** pasirinkite aptarnavimo užduotį ir prie aptarnavimo užsakymo pridėkite aptarnavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="d745f-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="d745f-121">Skirtuke **Aprašas** esančiuose laisvos formos teksto laukuose įveskite bet kurių vidinių ir išorinių pastabų aprašus.</span><span class="sxs-lookup"><span data-stu-id="d745f-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="d745f-122">Norėdami įrašyti įrašą, uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="d745f-122">Close the form to save the record.</span></span>

<span data-ttu-id="d745f-123">Šią procedūrą kartokite, kol sukursite visus reikalingus aptarnavimo sutarties užsakymo ryšius.</span><span class="sxs-lookup"><span data-stu-id="d745f-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="d745f-124">Tada, kurdami aptarnavimo užsakymo eilutes, galėsite pasirinkti aptarnavimo užduotis, kurioms sukūrėte ryšį.</span><span class="sxs-lookup"><span data-stu-id="d745f-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="d745f-125">Aptarnavimo užsakyme sukurti aptarnavimo užduočių ryšiai prieinami konkrečiame aptarnavimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="d745f-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="d745f-126">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="d745f-126">See also</span></span>

[<span data-ttu-id="d745f-127">Aptarnavimo užduočių apžvalga</span><span class="sxs-lookup"><span data-stu-id="d745f-127">Service tasks overview</span></span>](service-tasks.md)


  


