---
title: Laiko ir buvimo darbe registracija
description: "Laiko registravimo darbuotojai gali įvesti skirtingų tipų laiko registracijas, pavyzdžiui, atėjimo į darbą, išėjimo iš darbo, netiesioginių veiklų registravimo ir neatvykimo registravimo. Šiame straipsnyje aprašomos registracijos, jų skaičiavimas, tvirtinimas ir darbo eigos naudojimas norint į tabelių tvirtinimo procesą įtraukti struktūrą ir automatinį tvirtinimą."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, JmgCalcApprovePickDialog, JmgGroupApprove, JmgGroupCalc, JmgGroupSigningTable, JmgRegistration, JmgTimeCalcParmeters, WorkflowTableListPageRnr
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53351
ms.assetid: 885b0cdf-53d7-4cb4-92fe-da1b9e32b39f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 83603b1f8d20c18b7f10cd7224d491b558ee1b8b
ms.contentlocale: lt-lt
ms.lasthandoff: 06/29/2017


---

# <a name="time-and-attendance-registration"></a><span data-ttu-id="e100d-104">Laiko ir buvimo darbe registracija</span><span class="sxs-lookup"><span data-stu-id="e100d-104">Time and attendance registration</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e100d-105">Laiko registravimo darbuotojai gali įvesti skirtingų tipų laiko registracijas, pavyzdžiui, atėjimo į darbą, išėjimo iš darbo, netiesioginių veiklų registravimo ir neatvykimo registravimo.</span><span class="sxs-lookup"><span data-stu-id="e100d-105">Time registration workers can enter different types of time registrations, for example, clock in, clock out, register indirect activities, and absence registration.</span></span> <span data-ttu-id="e100d-106">Šiame straipsnyje aprašomos registracijos, jų skaičiavimas, tvirtinimas ir darbo eigos naudojimas norint į tabelių tvirtinimo procesą įtraukti struktūrą ir automatinį tvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="e100d-106">This article describes registrations, their calculation, approval, and the use of workflow to add structure and automated approval to the process of approving timesheets.</span></span> 

<a name="registrations"></a><span data-ttu-id="e100d-107">Registracijos</span><span class="sxs-lookup"><span data-stu-id="e100d-107">Registrations</span></span>
-------------

<span data-ttu-id="e100d-108">Įmonių, kurios naudoja laiko ir buvimo darbe registracijas, darbuotojai turi registruoti darbe praleidžiamą laiką ir lankomumą.</span><span class="sxs-lookup"><span data-stu-id="e100d-108">In companies that use Time and attendance, workers must register the time that they spend at work, as well as their attendance.</span></span> <span data-ttu-id="e100d-109">Kai kurių įmonių darbuotojams registruotis gali reikėti tik atėjus į darbą ir išeinant iš jo.</span><span class="sxs-lookup"><span data-stu-id="e100d-109">Some companies may only require workers to register clocking-in and clocking-out times.</span></span> <span data-ttu-id="e100d-110">Kitose įmonėse darbuotojai taip pat gali turėti registruoti faktinių veiklų, kurias jie atlieka, laiko sąnaudas ir pertraukas.</span><span class="sxs-lookup"><span data-stu-id="e100d-110">In other companies, workers may also be required to register time consumption on the actual activities they perform as well as the breaks they take.</span></span> <span data-ttu-id="e100d-111">Numatyti laiko ir lankomumo vartotojai nurodyti toliau.</span><span class="sxs-lookup"><span data-stu-id="e100d-111">The intended users of Time and attendance are:</span></span>
-   <span data-ttu-id="e100d-112">Darbuotojai, kurie turi registruoti laiką ir lankomumą reguliariais intervalais, pavyzdžiui, kasdien, kas savaitę arba kas dvi savaites.</span><span class="sxs-lookup"><span data-stu-id="e100d-112">Workers, who are required to register time and attendance at regular intervals, for example daily, weekly or bi-weekly.</span></span>
-   <span data-ttu-id="e100d-113">Prižiūrėtojai, vadovai ir darbo užmokestį skaičiuojantys buhalteriai, kurie skaičiuoja, tvirtina ir perkelia darbuotojo registracijas toliau apdoroti.</span><span class="sxs-lookup"><span data-stu-id="e100d-113">Supervisors, managers, and payroll officers who calculate, approve, and transfer worker registrations for further processing.</span></span>

| <span data-ttu-id="e100d-114">**Pastaba**</span><span class="sxs-lookup"><span data-stu-id="e100d-114">**Note**</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e100d-115">Jei vykdote laiko ir lankomumo registracijas vykdydami gamybą, visos projektų, projekto veiklų, netiesioginių veiklų, neatvykimo kodų ir viršvalandžių bei nukrypimo laiko registracijos bus įrašytos ir naudojamos atlyginimams abiejuose moduliuose apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="e100d-115">If you run Time and attendance together with Manufacturing execution, all registrations on projects, project activities, indirect activities, absence codes, and overtime and flex time will be recorded and are used to calculate payroll in both modules.</span></span> |

## <a name="time-registrations-workers"></a><span data-ttu-id="e100d-116"> Laiko registracijų darbuotojai</span><span class="sxs-lookup"><span data-stu-id="e100d-116">Time registrations workers</span></span>
<span data-ttu-id="e100d-117">Norėdami registruoti laiką ir neatvykimą, darbuotojus reikia nustatyti kaip laiko registracijos darbuotojus įmonėje, kurioje jie dirba.</span><span class="sxs-lookup"><span data-stu-id="e100d-117">To be able to register time and absence, workers must be set up as time registration workers in the company they are employed in.</span></span>

<span data-ttu-id="e100d-118">Atlikus sąranką darbuotojai gali įvesti skirtingų tipų registracijas.</span><span class="sxs-lookup"><span data-stu-id="e100d-118">After setup, the workers can enter different types of registrations.</span></span>

-   <span data-ttu-id="e100d-119">Atėjimo į darbą ir išėjimo iš darbo registracijos, kai atvykstama arba išvykstama iš darbo.</span><span class="sxs-lookup"><span data-stu-id="e100d-119">Clocking in- and out when arriving or leaving work.</span></span>
-   <span data-ttu-id="e100d-120">Laiko ir prekių suvartojimas gamybos užduotyse.</span><span class="sxs-lookup"><span data-stu-id="e100d-120">Time and item consumption on production jobs.</span></span>
-   <span data-ttu-id="e100d-121">Laikas, kurį sunaudoja cecho mašina, jei ji nurodyta kaip išteklius.</span><span class="sxs-lookup"><span data-stu-id="e100d-121">Time used on a machine on the shop floor, if the machine has been defined as a resource.</span></span>

| <span data-ttu-id="e100d-122">**Pastaba**</span><span class="sxs-lookup"><span data-stu-id="e100d-122">**Note**</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e100d-123">Darbuotojui gali būti automatiškai priskiriamos laiko registracijos, atliktos naudojant konkrečią cecho mašiną, jei darbuotojas nusprendžia dirbti kaip mašinos asistentas, kai jis pradeda gamybos užduotį.</span><span class="sxs-lookup"><span data-stu-id="e100d-123">A worker can be automatically assigned the time registrations that are made on a particular machine on the shop floor, if the worker chooses to work as an assistant to the machine when he or she starts the production job.</span></span> |

-   <span data-ttu-id="e100d-124">Projektų ir projektų veiklų laiko registracijos.</span><span class="sxs-lookup"><span data-stu-id="e100d-124">Time registrations on projects and project activities.</span></span>
-   <span data-ttu-id="e100d-125">Projekto mokesčių bei prekių suvartojimo registravimas naudojant atitinkamus projekto mokesčių žurnalus ir projekto prekių žurnalus.</span><span class="sxs-lookup"><span data-stu-id="e100d-125">Registering project fees and item consumption via the respective project fee journals and project item journals.</span></span>
-   <span data-ttu-id="e100d-126">Suplanuotas neatvykimas.</span><span class="sxs-lookup"><span data-stu-id="e100d-126">Planned absence.</span></span>
-   <span data-ttu-id="e100d-127">Neatvykimas, kai vėluojama atvykti į darbą arba iš darbo išeinama anksčiau nei planuota.</span><span class="sxs-lookup"><span data-stu-id="e100d-127">Absence when arriving late to work or leaving earlier than planned.</span></span>
-   <span data-ttu-id="e100d-128">Darbo pertraukos, užregistruotos neautomatiniu būdu arba sistemos automatiškai apskaičiuotos.</span><span class="sxs-lookup"><span data-stu-id="e100d-128">Work breaks, either manually registered or automatically calculated by the system.</span></span>
-   <span data-ttu-id="e100d-129">Netiesioginės veiklos, t. y. negamybinės veiklos, kurias darbuotojas gali vykdyti darbo dienos metu.</span><span class="sxs-lookup"><span data-stu-id="e100d-129">Indirect activities, which are non-productive activities a worker might engage in during a workday.</span></span> <span data-ttu-id="e100d-130">Šių veiklų pavyzdžiai apima susitikimus arba savo darbo srities valymą.</span><span class="sxs-lookup"><span data-stu-id="e100d-130">Examples of these activities include meetings or cleaning their workspace.</span></span>
-   <span data-ttu-id="e100d-131">Viršvalandžiai, kurie gali būti registruojami kaip viršvalandžiai, nukrypimo laikas arba viršvalandžiai.</span><span class="sxs-lookup"><span data-stu-id="e100d-131">Overtime, which can be registered either as extra hours, flextime, or overtime.</span></span>

## <a name="adding-clockout-registrations"></a><span data-ttu-id="e100d-132">Išėjimo iš darbo registracijos įtraukimas</span><span class="sxs-lookup"><span data-stu-id="e100d-132">Adding clockout registrations</span></span>
<span data-ttu-id="e100d-133">Jei darbo dienos pabaigoje darbuotojas pamiršta užregistruoti išėjimą iš darbo, trūkstamą registraciją galima įtraukti paleidžiant paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="e100d-133">If a worker forgets to clock-out at the end of their workday, the missing registration can be added by running a batch job.</span></span> <span data-ttu-id="e100d-134">Sistema palygins atėjimo į darbą ir išėjimo iš darbo laikus pagal susietą darbuotojo šabloną ir automatiškai įterps trūkstamą išėjimo iš darbo registraciją, kad ji atitiktų šablono pabaigos laiką.</span><span class="sxs-lookup"><span data-stu-id="e100d-134">The system will compare the clock-in time and the clock-out time according to the associated profile of the worker, and automatically insert the missing clock-out registration to match the profile’s end time.</span></span> <span data-ttu-id="e100d-135">Atėjimo į darbą ir išėjimo iš darbo registracijos yra labai svarbios toliau skaičiuojant ir tvirtinant laiko registracijas prieš juos perkeliant į algalapį.</span><span class="sxs-lookup"><span data-stu-id="e100d-135">Both the clock-in and clock-out registrations are vital for the subsequent calculation and approval of time registrations before they can be transferred to payroll.</span></span>

## <a name="calculating-registrations"></a><span data-ttu-id="e100d-136">Registracijų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="e100d-136">Calculating registrations</span></span>
<span data-ttu-id="e100d-137">Kai registracijos darbuotojui priskiriama skaičiavimo grupė, kuri paprastai yra susijusi su konkrečia komanda, pamaina arba darbo grupe.</span><span class="sxs-lookup"><span data-stu-id="e100d-137">When a registration worker is assigned a calculation group that typically relates to a specific team, shift, or work group.</span></span> <span data-ttu-id="e100d-138">Komandos vadovas arba prižiūrėtojas paprastai patikrina darbuotojų registracijas ir todėl jis yra atsakingas už kasdienį atitinkamų skaičiavimo grupių skaičiavimo vykdymą.</span><span class="sxs-lookup"><span data-stu-id="e100d-138">The team manager or supervisor typically validates the registrations made by the workers, and is therefore also the responsible person to run the calculation for the respective calculation groups on a daily basis.</span></span> <span data-ttu-id="e100d-139">Skaičiavimo proceso metu komandos vadovas arba prižiūrėtojas gali atlikti toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e100d-139">As part of the calculation process the team manager or supervisor is able to:</span></span>
-   <span data-ttu-id="e100d-140">Taisyti klaidingas registracijas.</span><span class="sxs-lookup"><span data-stu-id="e100d-140">Correct erroneous registrations.</span></span> <span data-ttu-id="e100d-141">Pvz., keisti gamybos užduočių perjungimo kodus ir koreguoti grįžtamąjį ryšį.</span><span class="sxs-lookup"><span data-stu-id="e100d-141">For example, change switch codes and adjust feedback on production jobs.</span></span>
-   <span data-ttu-id="e100d-142">Įtraukti trūkstamas registracijas.</span><span class="sxs-lookup"><span data-stu-id="e100d-142">Add missing registrations.</span></span> <span data-ttu-id="e100d-143">Pvz., kurti išėjimo iš darbo registracijas ir kurti neatvykimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="e100d-143">For example, create clock-out registrations and create absence transactions.</span></span>
-   <span data-ttu-id="e100d-144">Naikinti neteisingas registracijas.</span><span class="sxs-lookup"><span data-stu-id="e100d-144">Delete incorrect registrations.</span></span>

<span data-ttu-id="e100d-145">Kadangi užregistruotas laikas turi atitikti darbuotojo laiko profilį prieš skaičiuojant registracijas, galite perrašyti bet kurio darbuotojo, turinčio savo standartinio darbo laiko profilio išimčių, darbo laiko profilį.</span><span class="sxs-lookup"><span data-stu-id="e100d-145">Because the registered time must match the worker’s time profile prior to calculating the registrations, you must override the work time profile for any worker who has an exception to his standard work time profile.</span></span> <span data-ttu-id="e100d-146">Jei darbuotojo profilis yra dieninė pamaina, o darbuotojas sutiko dirbti naktinėje pamainoje neapmokant už viršvalandžius, komandos vadovas arba prižiūrėtojas turi perrašyti numatytąjį darbuotojo profilį, kad darbo laiką apskaičiuotų naudodamas standartinį nakties tarifą, o ne viršvalandžių tarifą.</span><span class="sxs-lookup"><span data-stu-id="e100d-146">In the case, where the worker profile is day shift, and the worker has agreed to work a night shift with no overtime pay, the team manager or supervisor must override the default worker profile in order to calculate the working time at the standard night rate and not as overtime.</span></span> <span data-ttu-id="e100d-147">Skaičiavimas taip pat rodys klaidą, jei trūksta neatvykimo registracijos.</span><span class="sxs-lookup"><span data-stu-id="e100d-147">The calculation will also display an error if an absence registration is missing.</span></span> <span data-ttu-id="e100d-148">Ji turi būti įtraukta, kad būtų užbaigtas skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="e100d-148">It must be added before the calculation can be completed.</span></span>

## <a name="approving-registrations"></a><span data-ttu-id="e100d-149">Registracijų tvirtinimas</span><span class="sxs-lookup"><span data-stu-id="e100d-149">Approving registrations</span></span>
<span data-ttu-id="e100d-150">Kaip laiko registracijos darbuotojui priskiriate skaičiavimo grupę, taip turite priskirti ir patvirtinimo grupę.</span><span class="sxs-lookup"><span data-stu-id="e100d-150">Just as you assign a calculation group to a time registration worker, you must assign an approval group as well.</span></span> <span data-ttu-id="e100d-151">Paprastai grupė bus būdinga konkrečiai komandai, pamainai arba darbo grupei.</span><span class="sxs-lookup"><span data-stu-id="e100d-151">Typically the group will be specific to a team, shift, or work group.</span></span> <span data-ttu-id="e100d-152">Turite patvirtinti laiko registracijas, kurios buvo apskaičiuotos teisingai (tai reiškia, kad skaičiavimas turi būti atliktas be klaidų), kad mokėjimo elementus būtų galima generuoti ir vėliau perkelti į algalapio sistemą.</span><span class="sxs-lookup"><span data-stu-id="e100d-152">You must approve the time registrations that were calculated correctly – this means doing a calculation without errors – before pay items can be generated that afterward can be transferred to a payroll system.</span></span> <span data-ttu-id="e100d-153">Algalapio administratorius paprastai tvirtins registracijas, o prieš patvirtindamas jis gali atlikti toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e100d-153">The payroll administrator will typically do the approval of registrations, and prior to the approval he is able to:</span></span>
-   <span data-ttu-id="e100d-154">Perrašyti atskirų darbuotojų mokėjimo sutartis.</span><span class="sxs-lookup"><span data-stu-id="e100d-154">Override pay agreements for individual workers.</span></span>
-   <span data-ttu-id="e100d-155">Įtraukti neautomatiškai nustatomas premijas.</span><span class="sxs-lookup"><span data-stu-id="e100d-155">Add manual premiums.</span></span>
-   <span data-ttu-id="e100d-156">Įvesti papildomą informaciją apie neatvykimo registracijas.</span><span class="sxs-lookup"><span data-stu-id="e100d-156">Enter additional information about absence registrations.</span></span>

| <span data-ttu-id="e100d-157">**Pastaba**</span><span class="sxs-lookup"><span data-stu-id="e100d-157">**Note**</span></span>                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e100d-158">Jei tam tikriems darbuotojams buvo skaičiuojami viršvalandžiai, viršvalandžiai gali būti paskirstyti specialiems darbams dienos metu.</span><span class="sxs-lookup"><span data-stu-id="e100d-158">If overtime has been calculated for specific workers, the overtime can be allocated to specific jobs during the day.</span></span> <span data-ttu-id="e100d-159">Tai tinka, jei darbo išlaidos skaičiuojamos pagal darbuotojo mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="e100d-159">This is relevant if job cost is calculated based on worker pay.</span></span> |

## <a name="approving-registrations-using-workflow"></a><span data-ttu-id="e100d-160"> Registracijų tvirtinimas naudojant darbo eigą</span><span class="sxs-lookup"><span data-stu-id="e100d-160">Approving registrations using workflow</span></span>
<span data-ttu-id="e100d-161">Galite nustatyti darbo eigos tvirtinimo procesą, kurio metu automatiškai patvirtinamos registracijos, atitinkančios darbo eigos taisykles, paliekant tik nuokrypius, kurie turi būti tvarkomi neautomatiškai.</span><span class="sxs-lookup"><span data-stu-id="e100d-161">You can set up a workflow approval process that automatically approves registrations which comply with workflow rules, leaving only deviations to be handled manually.</span></span> <span data-ttu-id="e100d-162">Jei darbo eigos tvirtinimo funkcija yra suaktyvinta, komandos vadovas arba prižiūrėtojas pateikia apskaičiuotas registracijas patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="e100d-162">If workflow approval is activated, the team manager or supervisor submits the calculated registrations for approval.</span></span> <span data-ttu-id="e100d-163">Darbo eigos procesas sukurs atitinkamus patvirtinimus bei užduotis ir tada juos priskirs tinkamiems vartotojams bei vaidmenims, kaip nurodyta darbo eigoje.</span><span class="sxs-lookup"><span data-stu-id="e100d-163">The workflow process will generate the appropriate approvals and tasks, and then assign them to the right users and roles as identified in the workflow.</span></span> <span data-ttu-id="e100d-164">Galima naudoti du laiko ir lankomumo darbo eigos patvirtinimus.</span><span class="sxs-lookup"><span data-stu-id="e100d-164">There are two workflow approvals for time and attendance.</span></span>

| <span data-ttu-id="e100d-165">Darbo eiga</span><span class="sxs-lookup"><span data-stu-id="e100d-165">Workflow</span></span>                                  | <span data-ttu-id="e100d-166">Paskirtis</span><span class="sxs-lookup"><span data-stu-id="e100d-166">Purpose</span></span>                                                                                                   | <span data-ttu-id="e100d-167">Registracijos tipas</span><span class="sxs-lookup"><span data-stu-id="e100d-167">Registration type</span></span>                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e100d-168">Bendras laiko ir buvimo darbe dienų skaičius</span><span class="sxs-lookup"><span data-stu-id="e100d-168">Time and attendance days total</span></span>            | <span data-ttu-id="e100d-169">Darbo eiga tikrina registracijas pagal, pvz., numatomą dienos darbo valandų skaičių.</span><span class="sxs-lookup"><span data-stu-id="e100d-169">The workflow validates registrations against, for example, the expected number of work hours for the day.</span></span> |                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e100d-170">Laiko ir buvimo darbe žurnalo registracija.</span><span class="sxs-lookup"><span data-stu-id="e100d-170">Time and attendance journal registration.</span></span> | <span data-ttu-id="e100d-171">Darbo eiga tikrina kiekvieno registracijos tipo registracijos datą.</span><span class="sxs-lookup"><span data-stu-id="e100d-171">The workflow validates each registration type for the date of the registration.</span></span>                           | <span data-ttu-id="e100d-172">Laikas ir buvimas darbe • Atėjimas į darbą • Išėjimas iš darbo • Neatvykimas • Pertrauka • Perjungimo kodas • Projektas • Projekto veikla • Netiesioginės veiklos gamybos užduotys • Eilė prieš • Sąranka • Procesas • Persidengimas • Transportas • Eilė po • Pradėti asistuoti • Sustabdyti asistavimą</span><span class="sxs-lookup"><span data-stu-id="e100d-172">Time and attendance • Clock-in • Clock-out • Absence • Break • Switch code • Project • Project activity • Indirect activity Production jobs • Queue before • Setup • Process • Overlap • Transport • Queue after • Start assistance • Stop assistance</span></span> |

 

## <a name="transferring-approved-registrations"></a><span data-ttu-id="e100d-173">Patvirtintų registracijų perkėlimas</span><span class="sxs-lookup"><span data-stu-id="e100d-173">Transferring approved registrations</span></span>
<span data-ttu-id="e100d-174">Patvirtinus registracijas jas galima perkelti į periodinę atlyginimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="e100d-174">After approval of the registrations you can transfer them to a periodic payroll job.</span></span> <span data-ttu-id="e100d-175">Perkeltos registracijos užregistruojamos į veiklą arba užduotį, su kuria jos yra susijusios, pvz., į gamybos užsakymą arba projektą.</span><span class="sxs-lookup"><span data-stu-id="e100d-175">A transferred registration is posted to an activity or job that it relates to, for example, a production order or a project.</span></span> <span data-ttu-id="e100d-176">Algalapio operacijos kiekvienam darbuotojui generuojamos pagal registracijas.</span><span class="sxs-lookup"><span data-stu-id="e100d-176">Payroll transactions are generated for each worker based on the registrations.</span></span>  

## <a name="reversing-transferred-registrations"></a><span data-ttu-id="e100d-177">Perkeltų registracijų atšaukimas</span><span class="sxs-lookup"><span data-stu-id="e100d-177">Reversing transferred registrations</span></span>
<span data-ttu-id="e100d-178">Operacijų atšaukimo užduotį galima vykdyti (pakartoti), kol neįvykdytas periodinio atlyginimo mokėjimo pervedimas.</span><span class="sxs-lookup"><span data-stu-id="e100d-178">The task of reversing transactions – rolling them back – can be done until the time when the payroll period’s pay transfer is run.</span></span> <span data-ttu-id="e100d-179">Tai reiškia, algalapio duomenys buvo perkelti į išorinį failą.</span><span class="sxs-lookup"><span data-stu-id="e100d-179">This means that payroll data has been transferred to an external file.</span></span> <span data-ttu-id="e100d-180">Kai atšaukiama, visos registracijos panaikinamos, o registruotos gamybos užsakymų arba projektų operacijos yra korespondentinės neutralios.</span><span class="sxs-lookup"><span data-stu-id="e100d-180">When reversed, all registrations are withdrawn, and any transactions posted on production orders or projects are offset and neutralized.</span></span>

| <span data-ttu-id="e100d-181">**Pastaba**</span><span class="sxs-lookup"><span data-stu-id="e100d-181">**Note**</span></span>                                                 |
|----------------------------------------------------------|
| <span data-ttu-id="e100d-182">Išorinį failą galima importuoti į algalapio sistemą.</span><span class="sxs-lookup"><span data-stu-id="e100d-182">The external file can be imported into a payroll system.</span></span> |

## <a name="registrations-in-electronic-timecards"></a><span data-ttu-id="e100d-183">Registracijos elektroninėse laiko kortelėse</span><span class="sxs-lookup"><span data-stu-id="e100d-183">Registrations in electronic timecards</span></span>
<span data-ttu-id="e100d-184">Darbuotojams, kurių atliekamų užduočių greitas grįžtamasis ryšys nėra būtinas (pvz., gamybos užduočių), bet kurie vykdo projekto veiklas, gali būti naudinga naudoti elektroninę laiko kortelę.</span><span class="sxs-lookup"><span data-stu-id="e100d-184">Workers with job tasks that do not require immediate feedback, as is the case with production jobs, but who work on project activities, can benefit from using the electronic timecard.</span></span> <span data-ttu-id="e100d-185">Elektroninės laiko kortelių suteikia galimybę lanksčiau įvesti registracijas bet kuriuo metu ir atsižvelgiant į jūsų verslo grafiką – kasdien, kas savaitę arba kai darbuotojas yra vėl darbe po to, kai buvo neatvykęs.</span><span class="sxs-lookup"><span data-stu-id="e100d-185">Electronic timecards offer the flexibility to enter registrations any time and in the best way for your business schedule – daily, weekly, or when a worker is in the office again after being away.</span></span> <span data-ttu-id="e100d-186">Norėdami naudoti elektronines laiko korteles arba šiuos darbuotojus, darbuotojo informacijoje turite nurodyti Naudoti laiko kortelę.</span><span class="sxs-lookup"><span data-stu-id="e100d-186">To use electronic timecards or these workers, you must specify, Use timecard, in the worker details.</span></span> <span data-ttu-id="e100d-187">Naudodamas elektronines laiko korteles darbuotojas gali registruoti toliau nurodytus elementus.</span><span class="sxs-lookup"><span data-stu-id="e100d-187">Electronic timecards enable the worker to register:</span></span>

-   <span data-ttu-id="e100d-188">Data</span><span class="sxs-lookup"><span data-stu-id="e100d-188">Date</span></span>
-   <span data-ttu-id="e100d-189">Registracijos tipas</span><span class="sxs-lookup"><span data-stu-id="e100d-189">Registration type</span></span>
-   <span data-ttu-id="e100d-190">Užduoties nuoroda, pvz., projektas, netiesioginė veikla arba gamybos užsakymas</span><span class="sxs-lookup"><span data-stu-id="e100d-190">Job reference, such as project, indirect activity, or production order</span></span>
-   <span data-ttu-id="e100d-191">Užduoties identifikavimas</span><span class="sxs-lookup"><span data-stu-id="e100d-191">Job identification</span></span>
-   <span data-ttu-id="e100d-192">Laiko suvartojimas</span><span class="sxs-lookup"><span data-stu-id="e100d-192">Time consumption</span></span>
-   <span data-ttu-id="e100d-193">Projekto mokesčiai</span><span class="sxs-lookup"><span data-stu-id="e100d-193">Project fees</span></span>
-   <span data-ttu-id="e100d-194">Projekto prekės</span><span class="sxs-lookup"><span data-stu-id="e100d-194">Project items</span></span>




