---
title: Ataskaitų pagal įstatymą dėl prieinamos sveikatos priežiūros (ACA) generavimas
description: Prieinamos sveikatos priežiūros ataskaitos sukuria formas 1095-B ir 1095-C palaikančias **Darbdavio mandato** dalį prieinamos sveikatos priežiūros akto.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1091460ee1996b944b760f3771007bd2a26666a9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053206"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="49ffa-103">ACA ataskaitų generavimas</span><span class="sxs-lookup"><span data-stu-id="49ffa-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="49ffa-104">Prieinamos sveikatos priežiūros ataskaitos sukuria formas 1095-B ir 1095-C palaikančias **Darbdavio mandato** dalį prieinamos sveikatos priežiūros akto.</span><span class="sxs-lookup"><span data-stu-id="49ffa-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="49ffa-105">ACA ataskaitos yra įjungtos tik juridiniams asmenims JAV.</span><span class="sxs-lookup"><span data-stu-id="49ffa-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="49ffa-106">Darbo pradžia</span><span class="sxs-lookup"><span data-stu-id="49ffa-106">Getting started</span></span>

<span data-ttu-id="49ffa-107">Norėdami sekti informaciją 1095-B ir 1095-C formoms, pirmiausia sukurkite vieną ir daugiau prieinamos sveikatos priežiūros aprėpties grupių.</span><span class="sxs-lookup"><span data-stu-id="49ffa-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="49ffa-108">Prieinamos sveikatos priežiūros grupės rodo:</span><span class="sxs-lookup"><span data-stu-id="49ffa-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="49ffa-109">Aprėpties pasiūlymas pateiktas darbuotojui</span><span class="sxs-lookup"><span data-stu-id="49ffa-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="49ffa-110">Darbuotojo dalis mažiausių kaštų mėnesio premijos, jei kaštai viršija federalinį skurdo lygį</span><span class="sxs-lookup"><span data-stu-id="49ffa-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="49ffa-111">Saugų uostą naudojamą darbuotojo, jei taikomas</span><span class="sxs-lookup"><span data-stu-id="49ffa-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="49ffa-112">Prieinamos sveikatos priežiūros aprėpties grupė jums leidžia valdyti informaciją šiems laukeliams nekeičiant kiekvieno darbuotojo įrašo, kai sąlygos nekinta.</span><span class="sxs-lookup"><span data-stu-id="49ffa-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="49ffa-113">Galtie nesunkiai iš naujo paskirti prieinamos sveikatos priežiūros aprėpties grupes vienam ar keliems darbuotojams su **Masinio paskyrimo** parinktimi puslapyje.</span><span class="sxs-lookup"><span data-stu-id="49ffa-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="49ffa-114">Kelių draudimo grupės versijų išlaikymas</span><span class="sxs-lookup"><span data-stu-id="49ffa-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="49ffa-115">Galite išlaikyti kelias bet kurios aprėpties grupės versijas.</span><span class="sxs-lookup"><span data-stu-id="49ffa-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="49ffa-116">Ši funkcija jums leidžia atlikti keitimus be poreikio kurti naują grupę ir paskirti jai darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="49ffa-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="49ffa-117">Jums kuriant ACA aprėpties grupes, galite kurti masių priskyrimą grupėms ir darbuotojams su **masių priskyrimo** parinktimi.</span><span class="sxs-lookup"><span data-stu-id="49ffa-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="49ffa-118">Galite ir atskirai priskirti darbuotojus grupėms siekiant sekti ir pranešti ACA informaciją bei paskirti darbuotoją prienamų sveikatos priežiūros paslaugų aprėpties grupei.</span><span class="sxs-lookup"><span data-stu-id="49ffa-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="49ffa-119">Jums nereikia sekti kai kurios ACA aprėpties informacijos, tokios kaip ne pilno etato darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="49ffa-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="49ffa-120">Tokiu atveju, nustatykite **Pranešti aprėptį** laukelį į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="49ffa-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="49ffa-121">Nepaisant to, kad turite priskirti kiekvieną darbuotoją sekamai ACA informacijai į prieinamų sveikatos priežiūros paslaugų aprėpties grupę, vis dar galite keisti tolesnes parinktis bet kuriems mėnesiams, kuriems reikia kitų verčių:</span><span class="sxs-lookup"><span data-stu-id="49ffa-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="49ffa-122">**Draudimo pasiūlymas**</span><span class="sxs-lookup"><span data-stu-id="49ffa-122">**Offer of coverage**</span></span>
- <span data-ttu-id="49ffa-123">**Darbuotojui tenkanti išlaidų dalis**</span><span class="sxs-lookup"><span data-stu-id="49ffa-123">**Employee share of cost**</span></span>
- <span data-ttu-id="49ffa-124">**Saugus prieglobstis**</span><span class="sxs-lookup"><span data-stu-id="49ffa-124">**Safe Harbor**</span></span>

<span data-ttu-id="49ffa-125">Norėdami įvesti išlygas prieinamoms sveikatos priežiūros paslaugų grupems vertėms, rinkitės **Prieinamos sveikatos priežiūros paslaugos** nuorodą **Darbuotojo išsami informacija** puslapyje skyriuje **Papildoma informacija** esančiame **Darbuotojo skirtukas**.</span><span class="sxs-lookup"><span data-stu-id="49ffa-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="49ffa-126">Sveikatos priežiūros draudimo ataskaitos</span><span class="sxs-lookup"><span data-stu-id="49ffa-126">Reporting health care coverage</span></span>

<span data-ttu-id="49ffa-127">Kartu su sveikatos draudimo aprėpties sekimu siūlomu pilno etato darbuotojams, jei darbdavys siūlo darbuotojo remiamaą draduimą sveikatos paslaugoms, už kurį darbuotojas yra įtrauktas (nepriklausomai nuo jo darbo pilnu ar ne pilnu etatu), papipldoma informacija turi būti pranešta 1095-C formoje.</span><span class="sxs-lookup"><span data-stu-id="49ffa-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="49ffa-128">Kiekvienas darbuotojas (įskaitant priklausomuosius), kuriems taikomi darbdavio remiami išmokų planai, turi būti įtrauktas į tų mėnesių, kuriais planai buvo taikomi, ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="49ffa-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="49ffa-129">Galite nurodyti, ar norite, kad kiekvienas išmokų planas būtų praneštas pasirenkant **ACA ataskaitas** žymimame laukelyje.</span><span class="sxs-lookup"><span data-stu-id="49ffa-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="49ffa-130">Taip pat, jei darbuotojas pasirinko turėti išlaikytinių šiame išmokų plane, galite nurodyti išlaikytinių datas kiekvienam darbuotojui **Išlaikyti išmokas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="49ffa-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="49ffa-131">Norėdami nurodyti, kad išlaikytinis yra apdraustas išmoka, rinkitės **Redaguoti** mygtuką veiksmų juostoje **Išlaikytiniai** greitame skirtuke.</span><span class="sxs-lookup"><span data-stu-id="49ffa-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="49ffa-132">Puslapyje **Priklausomųjų draudimo datų tvarkytuvas** galite nurodyti datas, kada priklausomajam buvo taikoma išmoka.</span><span class="sxs-lookup"><span data-stu-id="49ffa-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="49ffa-133">Šiame puslapyje įvedus datas, puslapyje **Prižiūrėti išmokas** bus automatiškai pasirinktas žymės langelis **Apdraustas**.</span><span class="sxs-lookup"><span data-stu-id="49ffa-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="49ffa-134">Kurti 1095-B ir 1095-C formas</span><span class="sxs-lookup"><span data-stu-id="49ffa-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="49ffa-135">Galite taip pat kurti 1095-B ir 1095-C formas produkte ir dalyti juos visiems savo darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="49ffa-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="49ffa-136">Sistema gali elektroniniu būdu kurti 1095-C formas ir 1094-C IRS perdavimo failus.</span><span class="sxs-lookup"><span data-stu-id="49ffa-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="49ffa-137">Kuriant 1095-C formą, įveskite atitinkamus mokesčių metus ir nurodykite socialinio draudimo numerius, kurie turi būti paslėpti.</span><span class="sxs-lookup"><span data-stu-id="49ffa-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="49ffa-138">Jei spausdinate 1095-C formas daugiau nei 500 darbuotojų, gausite daugiau nei vieną PDF failą.</span><span class="sxs-lookup"><span data-stu-id="49ffa-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="49ffa-139">Rekomenduojama padidinti į **maksimalų failo dydį** lange **Dokumentų valdymo parametrai** iki 150 MB.</span><span class="sxs-lookup"><span data-stu-id="49ffa-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="49ffa-140">Informacijos peržiūra</span><span class="sxs-lookup"><span data-stu-id="49ffa-140">Viewing information</span></span>

<span data-ttu-id="49ffa-141">Norėdami peržiūrėti, kurie darbuotojai buvo priskirti kiekvienai draudimo grupei, kurių darbuotojų nereikia įtraukti į ataskaitą ir kurie darbuotojai nepriskirti, galite naudoti puslapį **Darbininko prieinamos sveikatos priežiūros draudimas**.</span><span class="sxs-lookup"><span data-stu-id="49ffa-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="49ffa-142">Jei bet kurios iš numatytų verčių prieinamų sveikatos priežiūros paslaugų grupė buvo viršyta, žvaigždutė pasirodys šalia pakeistos vertės.</span><span class="sxs-lookup"><span data-stu-id="49ffa-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="49ffa-143">Jei visų 12 mėnesių reikšmės sutampa ir jų nebuvo nepaisoma, reikšmė bus išspausdinta stulpelyje **Visi 12 mėnesių**.</span><span class="sxs-lookup"><span data-stu-id="49ffa-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="49ffa-144">Galite taip pat prašyti lango suprasti, kurie darbuotojai buvo pažymėti kaip ACA neįtraukti.</span><span class="sxs-lookup"><span data-stu-id="49ffa-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="49ffa-145">Jums nereikia sekti, ar aprėptis buvo siūloma jiems ar jiems nereikia išduoti 1095-C metų gale.</span><span class="sxs-lookup"><span data-stu-id="49ffa-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="49ffa-146">Rinkitės **Ne ACA pranešami** laukelyje **Filtruoti pagal** siekiant sukurti darbuotojų sąrašą, kurie negaus 1095-C.</span><span class="sxs-lookup"><span data-stu-id="49ffa-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="49ffa-147">Taip pat, galite peržiūrėti visus darbuotjus, kurie nebuvo priskirti (**ACA ataskaitos aprėpties** laukelis tuščias) arba kurie nebuvo priskirti prieinamų sveikatos priežiūros paslaugų grupei, kuri nebegalioja pasirinktų **Metų** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="49ffa-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="49ffa-148">Galite eksportuoti darbuotojų sąrašus, kurie sugeneruoti naudojant filtravimo parinktis, į „Excel“.</span><span class="sxs-lookup"><span data-stu-id="49ffa-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="49ffa-149">Jums reikia pranešti apdraustus asmenis, nes suteikiate savarankišką draudimą, galite peržiūrėti visus išlaikytinius, kurie apdrausti išmokų planais ir pažymėti kaip **ACA pranešama**.</span><span class="sxs-lookup"><span data-stu-id="49ffa-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="49ffa-150">Rinkitės **Žiūrėti išlaikytinių draudimą** veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="49ffa-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="49ffa-151">Tik išmokų planai pažymėti kaip **ACA pranešami** rodomi užklausos lange.</span><span class="sxs-lookup"><span data-stu-id="49ffa-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]