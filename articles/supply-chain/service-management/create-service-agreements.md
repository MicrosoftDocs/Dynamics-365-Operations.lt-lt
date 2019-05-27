---
title: Aptarnavimo sutarčių kūrimas
description: Šioje temoje paaiškinta, kaip kurti aptarnavimo sutartis naudojant aptarnavimo valdymo ir projektų valdymo bei apskaitos modulių funkcijas.
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
ms.openlocfilehash: a094ce9f0d9323b089055e74d41cf1f45323a7d4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554557"
---
# <a name="create-service-agreements"></a><span data-ttu-id="b0f8f-103">Aptarnavimo sutarčių kūrimas</span><span class="sxs-lookup"><span data-stu-id="b0f8f-103">Create service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0f8f-104">Šioje temoje paaiškinta, kaip kurti aptarnavimo sutartis naudojant aptarnavimo valdymo ir projektų valdymo bei apskaitos modulių funkcijas.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="b0f8f-105">Aptarnavimo sutarties kūrimas tarnybos valdymo portale</span><span class="sxs-lookup"><span data-stu-id="b0f8f-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="b0f8f-106">Pereikite į **Aptarnavimo valdymą**.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="b0f8f-107">Norėdami sukurti naują aptarnavimo sutarties eilutę puslapio antraštėje, spustelėkite **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="b0f8f-108">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-108">Click **New**.</span></span> <span data-ttu-id="b0f8f-109">Lauke **Projekto ID** įveskite aprašą, pasirinkite nuorodą į projektą ir užpildykite likusius laukus ir aptarnavimo sutarties eilutes.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="b0f8f-110">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-110">Click **Save**.</span></span>
4. <span data-ttu-id="b0f8f-111">Skirtuke **Ryšiai** pasirinkite **Aptarnavimo objektai** arba **Aptarnavimo užduotys**, kad galėtumėte sukurti aptarnavimo sutarties aptarnavimo objektų arba aptarnavimo užduočių ryšius.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="b0f8f-112">Aptarnavimo objektai ir užduotys, kuriems sukūrėte ryšius, gali būti įtraukti į aptarnavimo sutarties eilutes.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="b0f8f-113">Apatinėje puslapio pusėje sukurkite aptarnavimo sutarties eilutes nukopijuodami eilutes iš aptarnavimo šablono, kitos aptarnavimo sutarties arba rankiniu būdu sukurdami aptarnavimo sutarties eilutes.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="b0f8f-114">Jei eilutes į aptarnavimo sutartį nukopijuojate iš kitos aptarnavimo sutarties, galite nurodyti, ar norite kopijuoti ir aptarnavimo objekto ir aptarnavimo užduoties ryšius.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="b0f8f-115">Jei nukopijuojate šiuos ryšius, jie įtraukiami į visus esamus aptarnavimo sutarties ryšius.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="b0f8f-116">Jei aptarnavimo sutarties eilutes nukopijuojate iš aptarnavimo šablono, aptarnavimo objekto ir aptarnavimo užduoties ryšiai automatiškai nukopijuojami į naujas aptarnavimo sutarties eilutes kaip aptarnavimo objekto ryšiai ir aptarnavimo užduoties ryšiai.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="b0f8f-117">Aptarnavimo sutarties eilučių kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="b0f8f-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="b0f8f-118">Puslapyje **Aptarnavimo sutartys** pridėkite aptarnavimo sutarties eilutę eilučių tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="b0f8f-119">Įveskite atitinkamą aptarnavimo sutarties eilutės informaciją.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="b0f8f-120">Norėdami įrašyti eilutę, paspauskite **CTRL+S**, tada uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="b0f8f-121">Aptarnavimo sutarties sukūrimas iš Projektas</span><span class="sxs-lookup"><span data-stu-id="b0f8f-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="b0f8f-122">Spustelėkite **Projektų valdymas ir apskaita**.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="b0f8f-123">Spustelėkite **Visi projektai**.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-123">Click **All projects**.</span></span>
3. <span data-ttu-id="b0f8f-124">Pasirinkite projektą iš sąrašo.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-124">Select the project from the list.</span></span>
4. <span data-ttu-id="b0f8f-125">**Veiksmų srityje** spustelėkite **Valdyti**.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="b0f8f-126">Veiksmų grupėje **Naujas** spustelėkite **Aptarnavimas** ir pasirinkite **Aptarnavimo sutartis**.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="b0f8f-127">Atlikite skyriuje **Aptarnavimo sutarties kūrimas** nurodytus veiksmus kaip jau minėta šioje temoje, kad būtų įvesta projekto nuoroda.</span><span class="sxs-lookup"><span data-stu-id="b0f8f-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="b0f8f-128">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="b0f8f-128">Related topics</span></span>

[<span data-ttu-id="b0f8f-129">Aptarnavimo sutartys</span><span class="sxs-lookup"><span data-stu-id="b0f8f-129">Service agreements</span></span>](service-agreements.md)


