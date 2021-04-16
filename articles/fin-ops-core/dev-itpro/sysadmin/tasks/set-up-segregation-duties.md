---
title: Nustatyti pareigų atskyrimą
description: Galite nustatyti taisykles, kad atskirtumėte užduotis, kurias turi atlikti skirtingi vartotojai.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e25fee324ce95cd04b86ee0e4e6a56cfacb61a53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745746"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="ee185-103">Nustatyti pareigų atskyrimą</span><span class="sxs-lookup"><span data-stu-id="ee185-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee185-104">Galite nustatyti taisykles, kad atskirtumėte užduotis, kurias turi atlikti skirtingi vartotojai.</span><span class="sxs-lookup"><span data-stu-id="ee185-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="ee185-105">Ši koncepcija vadinama pareigų atskyrimu.</span><span class="sxs-lookup"><span data-stu-id="ee185-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="ee185-106">Pavyzdžiui, galbūt nenorite, kad tas pats asmuo patvirtintų prekių gavimą ir apmokėtų tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="ee185-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="ee185-107">Pareigų atskyrimas padeda sumažinti apgaulės riziką ir nustatyti klaidas arba pažeidimus.</span><span class="sxs-lookup"><span data-stu-id="ee185-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="ee185-108">Taip pat galite naudoti pareigų atskyrimą norėdami taikyti vidinės kontrolės strategijas.</span><span class="sxs-lookup"><span data-stu-id="ee185-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="ee185-109">Norėdami sukurti taisyklę, atlikite tolesnę procedūrą.</span><span class="sxs-lookup"><span data-stu-id="ee185-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="ee185-110">Turite būti sistemos administratorius, kad galėtumėte atlikti procedūrą.</span><span class="sxs-lookup"><span data-stu-id="ee185-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="ee185-111">Eikite į **Sistemos administravimas** > **Sauga** > **Pareigų atskyrimas** > **Pareigų atskyrimo taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="ee185-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="ee185-112">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ee185-112">Click **New**.</span></span>
3. <span data-ttu-id="ee185-113">Lauke **Pavadinimas** įveskite taisyklės reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee185-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="ee185-114">Lauke **Pirmoji pareiga** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ee185-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ee185-115">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ee185-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="ee185-116">Pasirinkite pirmą taisyklės kontroliuojamą pareigą.</span><span class="sxs-lookup"><span data-stu-id="ee185-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="ee185-117">Lauke **Antroji pareiga** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ee185-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="ee185-118">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ee185-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="ee185-119">Pasirinkite antrą taisyklės kontroliuojamą pareigą.</span><span class="sxs-lookup"><span data-stu-id="ee185-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="ee185-120">Lauke **Svarba** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="ee185-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="ee185-121">Pasirinkite rizikos, patiriamos, kai tas pats vartotojas arba vaidmuo atlieka abi pareigas, svarbą.</span><span class="sxs-lookup"><span data-stu-id="ee185-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="ee185-122">Lauke **Saugos rizika** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee185-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="ee185-123">Įveskite saugos rizikos aprašą.</span><span class="sxs-lookup"><span data-stu-id="ee185-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="ee185-124">Lauke **Saugos sumažinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee185-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="ee185-125">Įveskite veiksmų, kuriuos atliekate siekdami sumažinti saugos riziką, aprašą.</span><span class="sxs-lookup"><span data-stu-id="ee185-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="ee185-126">Pavyzdžiui, riziką galite sumažinti atlikdami išsamesnes proceso apžvalgas, kas mėnesį atlikdami vadybinę peržiūrą arba dalindamiesi ištekliais su kitais padaliniais.</span><span class="sxs-lookup"><span data-stu-id="ee185-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="ee185-127">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ee185-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="ee185-128">Sukuriant taisyklę, pareigų atskyrimo taisyklių laikymasis nėra patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="ee185-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="ee185-129">Galite sukurti taisyklę, kuri sukurs esamų vaidmenų nesuderinamumą.</span><span class="sxs-lookup"><span data-stu-id="ee185-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="ee185-130">Esami vartotojo vaidmens priskyrimai gali būti nesuderinami su nauja taisykle.</span><span class="sxs-lookup"><span data-stu-id="ee185-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="ee185-131">Sukūrę arba modifikuodami taisyklę, turite patikrinti atitikimą.</span><span class="sxs-lookup"><span data-stu-id="ee185-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="ee185-132">Daugiau informacijos žr. [Pareigų atskyrimo konfliktų nustatymas ir sprendimas](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="ee185-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]