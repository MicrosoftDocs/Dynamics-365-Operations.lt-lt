---
title: Kurti naują išmoką
description: Ši užduotis parodys, kaip kurti išmokų elementus, kurie bus naudojami kuriant naują išmoką.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a74900f288fb5ce145f89e0ccad509deaac505cb
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/19/2019
ms.locfileid: "856283"
---
# <a name="create-a-new-benefit"></a><span data-ttu-id="c23da-103">Kurti naują išmoką</span><span class="sxs-lookup"><span data-stu-id="c23da-103">Create a new benefit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c23da-104">Ši užduotis parodys, kaip kurti išmokų elementus, kurie bus naudojami kuriant naują išmoką.</span><span class="sxs-lookup"><span data-stu-id="c23da-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="c23da-105">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="c23da-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="c23da-106">Ši užduotis yra skirta kompensacijų ir išmokų vadovui.</span><span class="sxs-lookup"><span data-stu-id="c23da-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="c23da-107">Kurti išmokų elementus</span><span class="sxs-lookup"><span data-stu-id="c23da-107">Create benefit elements</span></span>
1. <span data-ttu-id="c23da-108">Eikite į Žmogiškieji ištekliai > Išmokos > Nustatymas > Išmokų elementai.</span><span class="sxs-lookup"><span data-stu-id="c23da-108">Go to Human resources > Benefits > Setup > Benefit elements.</span></span>
2. <span data-ttu-id="c23da-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c23da-109">Click New.</span></span>
3. <span data-ttu-id="c23da-110">Lauke Tipas įveskite kuriamo išmokų tipo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c23da-110">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="c23da-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c23da-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c23da-112">Lauke Registravimas tuo pačiu metu pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c23da-112">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="c23da-113">Norėdami apriboti darbuotojų galimybę registruotis keliems medicinos planams, pasirinkite Viena vieno tipo registracija.</span><span class="sxs-lookup"><span data-stu-id="c23da-113">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="c23da-114">Lauke Algalapių kategorija pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c23da-114">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="c23da-115">Spustelėkite skirtuką Planai.</span><span class="sxs-lookup"><span data-stu-id="c23da-115">Click the Plans tab.</span></span>
8. <span data-ttu-id="c23da-116">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c23da-116">Click New.</span></span>
9. <span data-ttu-id="c23da-117">Lauke Planas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c23da-117">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="c23da-118">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c23da-118">In the Description field, type a value.</span></span>
11. <span data-ttu-id="c23da-119">Lauke Tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c23da-119">In the Type field, enter or select a value.</span></span>
12. <span data-ttu-id="c23da-120">Lauke Poveikis algalapiui pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c23da-120">In the Payroll impact field, select an option.</span></span>
13. <span data-ttu-id="c23da-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c23da-121">Click Save.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="c23da-122">Išmokos kūrimas</span><span class="sxs-lookup"><span data-stu-id="c23da-122">Create a benefit</span></span>
1. <span data-ttu-id="c23da-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c23da-123">Close the page.</span></span>
2. <span data-ttu-id="c23da-124">Pasirinkite Personalas > Išmokos > Išmokos.</span><span class="sxs-lookup"><span data-stu-id="c23da-124">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="c23da-125">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c23da-125">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="c23da-126">Lauke Planas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="c23da-126">In the Plan field, enter or select a value.</span></span>
5. <span data-ttu-id="c23da-127">Lauke Parinktis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c23da-127">In the Option field, enter or select a value.</span></span>
6. <span data-ttu-id="c23da-128">Lauke Įsigalioja įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="c23da-128">In the Effective field, enter a date and time.</span></span>
7. <span data-ttu-id="c23da-129">Spustelėkite Kurti išmoką.</span><span class="sxs-lookup"><span data-stu-id="c23da-129">Click Create benefit.</span></span>

