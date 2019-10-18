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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179141"
---
# <a name="create-a-new-benefit"></a><span data-ttu-id="ce2db-103">Kurti naują išmoką</span><span class="sxs-lookup"><span data-stu-id="ce2db-103">Create a new benefit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce2db-104">Ši užduotis parodys, kaip kurti išmokų elementus, kurie bus naudojami kuriant naują išmoką.</span><span class="sxs-lookup"><span data-stu-id="ce2db-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="ce2db-105">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="ce2db-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="ce2db-106">Ši užduotis yra skirta kompensacijų ir išmokų vadovui.</span><span class="sxs-lookup"><span data-stu-id="ce2db-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="ce2db-107">Kurti išmokų elementus</span><span class="sxs-lookup"><span data-stu-id="ce2db-107">Create benefit elements</span></span>
1. <span data-ttu-id="ce2db-108">Eikite į Žmogiškieji ištekliai > Išmokos > Nustatymas > Išmokų elementai.</span><span class="sxs-lookup"><span data-stu-id="ce2db-108">Go to Human resources > Benefits > Setup > Benefit elements.</span></span>
2. <span data-ttu-id="ce2db-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ce2db-109">Click New.</span></span>
3. <span data-ttu-id="ce2db-110">Lauke Tipas įveskite kuriamo išmokų tipo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ce2db-110">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="ce2db-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ce2db-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ce2db-112">Lauke Registravimas tuo pačiu metu pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="ce2db-112">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="ce2db-113">Norėdami apriboti darbuotojų galimybę registruotis keliems medicinos planams, pasirinkite Viena vieno tipo registracija.</span><span class="sxs-lookup"><span data-stu-id="ce2db-113">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="ce2db-114">Lauke Algalapių kategorija pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="ce2db-114">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="ce2db-115">Spustelėkite skirtuką Planai.</span><span class="sxs-lookup"><span data-stu-id="ce2db-115">Click the Plans tab.</span></span>
8. <span data-ttu-id="ce2db-116">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ce2db-116">Click New.</span></span>
9. <span data-ttu-id="ce2db-117">Lauke Planas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ce2db-117">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="ce2db-118">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ce2db-118">In the Description field, type a value.</span></span>
11. <span data-ttu-id="ce2db-119">Lauke Tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ce2db-119">In the Type field, enter or select a value.</span></span>
12. <span data-ttu-id="ce2db-120">Lauke Poveikis algalapiui pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="ce2db-120">In the Payroll impact field, select an option.</span></span>
13. <span data-ttu-id="ce2db-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ce2db-121">Click Save.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="ce2db-122">Išmokos kūrimas</span><span class="sxs-lookup"><span data-stu-id="ce2db-122">Create a benefit</span></span>
1. <span data-ttu-id="ce2db-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ce2db-123">Close the page.</span></span>
2. <span data-ttu-id="ce2db-124">Pasirinkite Personalas > Išmokos > Išmokos.</span><span class="sxs-lookup"><span data-stu-id="ce2db-124">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="ce2db-125">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ce2db-125">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="ce2db-126">Lauke Planas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="ce2db-126">In the Plan field, enter or select a value.</span></span>
5. <span data-ttu-id="ce2db-127">Lauke Parinktis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ce2db-127">In the Option field, enter or select a value.</span></span>
6. <span data-ttu-id="ce2db-128">Lauke Įsigalioja įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="ce2db-128">In the Effective field, enter a date and time.</span></span>
7. <span data-ttu-id="ce2db-129">Spustelėkite Kurti išmoką.</span><span class="sxs-lookup"><span data-stu-id="ce2db-129">Click Create benefit.</span></span>

