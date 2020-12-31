---
title: Nustatyti pareigų atskyrimą
description: Galite nustatyti taisykles, kad atskirtumėte užduotis, kurias turi atlikti skirtingi vartotojai.
author: peakerbl
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57c7c436c91ab11404cac3ea056b028023a0617a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688178"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="fe4dc-103">Nustatyti pareigų atskyrimą</span><span class="sxs-lookup"><span data-stu-id="fe4dc-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe4dc-104">Galite nustatyti taisykles, kad atskirtumėte užduotis, kurias turi atlikti skirtingi vartotojai.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="fe4dc-105">Ši koncepcija vadinama pareigų atskyrimu.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="fe4dc-106">Pavyzdžiui, galbūt nenorite, kad tas pats asmuo patvirtintų prekių gavimą ir apdorotų mokėjimą tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="fe4dc-107">Pareigų atskyrimas padeda sumažinti apgaulės riziką ir nustatyti klaidas arba pažeidimus.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="fe4dc-108">Taip pat galite naudoti pareigų atskyrimą norėdami taikyti vidinės kontrolės strategijas.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="fe4dc-109">Norėdami sukurti taisyklę, atlikite tolesnę procedūrą.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="fe4dc-110">Turite būti sistemos administratorius, kad galėtumėte atlikti procedūrą.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="fe4dc-111">Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DAT.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="fe4dc-112">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Pareigų atskyrimas > Pareigų atskyrimo taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="fe4dc-113">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-113">Click **New**.</span></span>
3. <span data-ttu-id="fe4dc-114">Lauke **Pavadinimas** įveskite taisyklės reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="fe4dc-115">Lauke **Pirmoji pareiga** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="fe4dc-116">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="fe4dc-117">Pasirinkite pirmą taisyklės kontroliuojamą pareigą.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="fe4dc-118">Lauke **Antroji pareiga** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="fe4dc-119">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="fe4dc-120">Pasirinkite antrą taisyklės kontroliuojamą pareigą.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="fe4dc-121">Lauke **Svarba** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="fe4dc-122">Pasirinkite rizikos, patiriamos, kai tas pats vartotojas arba vaidmuo atlieka abi pareigas, svarbą.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="fe4dc-123">Lauke **Saugos rizika** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="fe4dc-124">Įveskite saugos rizikos aprašą.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="fe4dc-125">Lauke **Saugos sumažinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="fe4dc-126">Įveskite veiksmų, kuriuos atliekate siekdami sumažinti saugos riziką, aprašą.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="fe4dc-127">Pavyzdžiui, riziką galite sumažinti atlikdami išsamesnes proceso apžvalgas, kas mėnesį atlikdami vadybinę peržiūrą arba dalindamiesi ištekliais su kitais padaliniais.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="fe4dc-128">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-128">Click **Save**.</span></span>

