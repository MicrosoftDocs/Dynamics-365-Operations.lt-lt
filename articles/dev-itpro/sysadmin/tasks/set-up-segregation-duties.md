--- 
title: "Nustatyti pareigų atskyrimą"
description: "Galite nustatyti taisykles, kad atskirtumėte užduotis, kurias turi atlikti skirtingi vartotojai."
author: maertenm
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 754f28cd2831d8a9a57c408518d240de460b732b
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="818ed-103">Nustatyti pareigų atskyrimą</span><span class="sxs-lookup"><span data-stu-id="818ed-103">Set up segregation of duties</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="818ed-104">Galite nustatyti taisykles, kad atskirtumėte užduotis, kurias turi atlikti skirtingi vartotojai.</span><span class="sxs-lookup"><span data-stu-id="818ed-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="818ed-105">Ši koncepcija vadinama pareigų atskyrimu.</span><span class="sxs-lookup"><span data-stu-id="818ed-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="818ed-106">Pavyzdžiui, galbūt nenorite, kad tas pats asmuo patvirtintų prekių gavimą ir apdorotų mokėjimą tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="818ed-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="818ed-107">Pareigų atskyrimas padeda sumažinti apgaulės riziką ir nustatyti klaidas arba pažeidimus.</span><span class="sxs-lookup"><span data-stu-id="818ed-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="818ed-108">Taip pat galite naudoti pareigų atskyrimą norėdami taikyti vidinės kontrolės strategijas.</span><span class="sxs-lookup"><span data-stu-id="818ed-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="818ed-109">Norėdami sukurti taisyklę, atlikite tolesnę procedūrą.</span><span class="sxs-lookup"><span data-stu-id="818ed-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="818ed-110">Turite būti sistemos administratorius, kad galėtumėte atlikti procedūrą.</span><span class="sxs-lookup"><span data-stu-id="818ed-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="818ed-111">Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DAT.</span><span class="sxs-lookup"><span data-stu-id="818ed-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="818ed-112">Eikite į Sistemos administravimas > Sauga > Pareigų atskyrimas > Pareigų atskyrimo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="818ed-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="818ed-113">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="818ed-113">Click New.</span></span>
3. <span data-ttu-id="818ed-114">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="818ed-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="818ed-115">Įveskite taisyklės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="818ed-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="818ed-116">Lauke Pirmoji pareiga spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="818ed-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="818ed-117">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="818ed-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="818ed-118">Pasirinkite pirmą taisyklės kontroliuojamą pareigą.</span><span class="sxs-lookup"><span data-stu-id="818ed-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="818ed-119">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="818ed-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="818ed-120">Lauke Antroji pareiga spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="818ed-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="818ed-121">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="818ed-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="818ed-122">Pasirinkite antrą taisyklės kontroliuojamą pareigą.</span><span class="sxs-lookup"><span data-stu-id="818ed-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="818ed-123">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="818ed-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="818ed-124">Lauke Svarba pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="818ed-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="818ed-125">Pasirinkite rizikos, patiriamos, kai tas pats vartotojas arba vaidmuo atlieka abi pareigas, svarbą.</span><span class="sxs-lookup"><span data-stu-id="818ed-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="818ed-126">Lauke Saugos rizika įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="818ed-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="818ed-127">Įveskite saugos rizikos aprašą.</span><span class="sxs-lookup"><span data-stu-id="818ed-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="818ed-128">Lauke Saugos sumažinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="818ed-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="818ed-129">Įveskite veiksmų, kuriuos atliekate siekdami sumažinti saugos riziką, aprašą.</span><span class="sxs-lookup"><span data-stu-id="818ed-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="818ed-130">Pavyzdžiui, riziką galite sumažinti atlikdami išsamesnes proceso apžvalgas, kas mėnesį atlikdami vadybinę peržiūrą arba dalindamiesi ištekliais su kitais padaliniais.</span><span class="sxs-lookup"><span data-stu-id="818ed-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="818ed-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="818ed-131">Click Save.</span></span>


