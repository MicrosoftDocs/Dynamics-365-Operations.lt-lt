---
title: Nustatyti pareigų atskyrimą
description: Galite nustatyti taisykles, kad atskirtumėte užduotis, kurias turi atlikti skirtingi vartotojai.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47747cba7f83d0b43a284750cff232824e00053a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982411"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="4a379-103">Nustatyti pareigų atskyrimą</span><span class="sxs-lookup"><span data-stu-id="4a379-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a379-104">Galite nustatyti taisykles, kad atskirtumėte užduotis, kurias turi atlikti skirtingi vartotojai.</span><span class="sxs-lookup"><span data-stu-id="4a379-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="4a379-105">Ši koncepcija vadinama pareigų atskyrimu.</span><span class="sxs-lookup"><span data-stu-id="4a379-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="4a379-106">Pavyzdžiui, galbūt nenorite, kad tas pats asmuo patvirtintų prekių gavimą ir apdorotų mokėjimą tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="4a379-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="4a379-107">Pareigų atskyrimas padeda sumažinti apgaulės riziką ir nustatyti klaidas arba pažeidimus.</span><span class="sxs-lookup"><span data-stu-id="4a379-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="4a379-108">Taip pat galite naudoti pareigų atskyrimą norėdami taikyti vidinės kontrolės strategijas.</span><span class="sxs-lookup"><span data-stu-id="4a379-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="4a379-109">Norėdami sukurti taisyklę, atlikite tolesnę procedūrą.</span><span class="sxs-lookup"><span data-stu-id="4a379-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="4a379-110">Turite būti sistemos administratorius, kad galėtumėte atlikti procedūrą.</span><span class="sxs-lookup"><span data-stu-id="4a379-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="4a379-111">Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DAT.</span><span class="sxs-lookup"><span data-stu-id="4a379-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="4a379-112">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Pareigų atskyrimas > Pareigų atskyrimo taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="4a379-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="4a379-113">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="4a379-113">Click **New**.</span></span>
3. <span data-ttu-id="4a379-114">Lauke **Pavadinimas** įveskite taisyklės reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4a379-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="4a379-115">Lauke **Pirmoji pareiga** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="4a379-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4a379-116">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="4a379-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="4a379-117">Pasirinkite pirmą taisyklės kontroliuojamą pareigą.</span><span class="sxs-lookup"><span data-stu-id="4a379-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="4a379-118">Lauke **Antroji pareiga** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="4a379-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="4a379-119">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="4a379-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="4a379-120">Pasirinkite antrą taisyklės kontroliuojamą pareigą.</span><span class="sxs-lookup"><span data-stu-id="4a379-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="4a379-121">Lauke **Svarba** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="4a379-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="4a379-122">Pasirinkite rizikos, patiriamos, kai tas pats vartotojas arba vaidmuo atlieka abi pareigas, svarbą.</span><span class="sxs-lookup"><span data-stu-id="4a379-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="4a379-123">Lauke **Saugos rizika** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4a379-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="4a379-124">Įveskite saugos rizikos aprašą.</span><span class="sxs-lookup"><span data-stu-id="4a379-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="4a379-125">Lauke **Saugos sumažinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4a379-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="4a379-126">Įveskite veiksmų, kuriuos atliekate siekdami sumažinti saugos riziką, aprašą.</span><span class="sxs-lookup"><span data-stu-id="4a379-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="4a379-127">Pavyzdžiui, riziką galite sumažinti atlikdami išsamesnes proceso apžvalgas, kas mėnesį atlikdami vadybinę peržiūrą arba dalindamiesi ištekliais su kitais padaliniais.</span><span class="sxs-lookup"><span data-stu-id="4a379-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="4a379-128">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4a379-128">Click **Save**.</span></span>

