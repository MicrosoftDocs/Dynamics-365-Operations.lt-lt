---
title: „Human Resources“ parametrų konfigūravimas
description: Šioje temoje aiškinama, kaip nustatyti konkrečius įmonės parametrus programoje „Dynamics 365 Human Resources“.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cd66cb4f5ac02407250e15ae134b36f5ccd4d290
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889937"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="1bd1c-103">„Human Resources“ parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1bd1c-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1bd1c-104">Kai kurie žmogiškųjų išteklių parametrai naudojami keliose įmonėse, o kiti – konkrečioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="1bd1c-105">Šioje temoje aiškinama, kaip nustatyti konkrečius įmonės personalo parametrus.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="1bd1c-106">Personalo parametrams nustatyti naudojami du puslapiai.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="1bd1c-107">Jei parametrai yra bendrai naudojami keliose įmonėse, galite naudoti puslapį **Bendrai naudojami žmogiškųjų išteklių parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="1bd1c-108">Jei parametrai skirti konkrečiai įmonei (kitaip tariant, parametrai taikomi prie vienai įmonei), naudokite puslapį **Personalo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![Eikite į personalo parametrus](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="1bd1c-110">Puslapyje **Personalo parametrai** parametrai suskirstyti į šešis toliau pateiktus skirtukus.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="1bd1c-111">**Bendri**</span><span class="sxs-lookup"><span data-stu-id="1bd1c-111">**General**</span></span>
- <span data-ttu-id="1bd1c-112">**Įdarbinimas** (šio skirtuko „Dynamics 365 Human Resources“ nėra)</span><span class="sxs-lookup"><span data-stu-id="1bd1c-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="1bd1c-113">**Kompensacija**</span><span class="sxs-lookup"><span data-stu-id="1bd1c-113">**Compensation**</span></span>
- <span data-ttu-id="1bd1c-114">**Numeracija**</span><span class="sxs-lookup"><span data-stu-id="1bd1c-114">**Number sequences**</span></span>
- <span data-ttu-id="1bd1c-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="1bd1c-115">**FMLA**</span></span>
- <span data-ttu-id="1bd1c-116">**Darbuotojų savitarna**</span><span class="sxs-lookup"><span data-stu-id="1bd1c-116">**Employee self service**</span></span>
- <span data-ttu-id="1bd1c-117">**Vadovų savitarna**</span><span class="sxs-lookup"><span data-stu-id="1bd1c-117">**Manager self service**</span></span>
- <span data-ttu-id="1bd1c-118">**Išmokų valdymas**</span><span class="sxs-lookup"><span data-stu-id="1bd1c-118">**Benefits management**</span></span>
- <span data-ttu-id="1bd1c-119">**Atostogos ir neatvykimai**</span><span class="sxs-lookup"><span data-stu-id="1bd1c-119">**Leave and absence**</span></span>
- <span data-ttu-id="1bd1c-120">**Mokėjimo būdai**</span><span class="sxs-lookup"><span data-stu-id="1bd1c-120">**Payment methods**</span></span>

<span data-ttu-id="1bd1c-121">Kiekviename skirtuke yra informacijos, susijusios su viena įmone.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="1bd1c-122">Bendri</span><span class="sxs-lookup"><span data-stu-id="1bd1c-122">General</span></span>

<span data-ttu-id="1bd1c-123">Skirtuko **Bendra** parametrai apibrėžia informacijos apie neatvykimą, sužalojimus ir ligas bei naujus darbuotojus, rodymą.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="1bd1c-124">Šio skirtuko parametrai taip pat nustato kai kuriuos numatytuosius įrašus, rodomus, kai dirbate.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="1bd1c-125">Tiksliau šiame skirtuke galima:</span><span class="sxs-lookup"><span data-stu-id="1bd1c-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="1bd1c-126">pasirinkti spalvą, kurią taikysite atidarytoms neatvykimo operacijoms,</span><span class="sxs-lookup"><span data-stu-id="1bd1c-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="1bd1c-127">nurodyti ataskaitoms naudotiną stilių aprašą,</span><span class="sxs-lookup"><span data-stu-id="1bd1c-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="1bd1c-128">įgalinti integravimą tarp mokymo kursų ir neatvykimų registravimo,</span><span class="sxs-lookup"><span data-stu-id="1bd1c-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="1bd1c-129">pasirinkti neatvykimo kodą, naudojamą šiam integravimui valdyti,</span><span class="sxs-lookup"><span data-stu-id="1bd1c-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="1bd1c-130">nurodyti, ar ilgai laikyti sužalojimo ir ligos atvejų incidentus,</span><span class="sxs-lookup"><span data-stu-id="1bd1c-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="1bd1c-131">nurodyti numatytąjį identifikavimo numerį, rodomą pasamdžius naują darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-131">Specify the default identification number shown when a new worker is hired.</span></span>

![Skirtukas Bendra](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="1bd1c-133">Įdarbinimas</span><span class="sxs-lookup"><span data-stu-id="1bd1c-133">Recruitment</span></span>

<span data-ttu-id="1bd1c-134">Skirtuko **Įdarbinimas** parametrai apibrėžia dokumentų tipus, naudojamus pretendentams siunčiamai korespondencijai.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="1bd1c-135">Taip pat galima nurodyti įdarbinimo projektą, naudojamą neprašytoms paraiškoms.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="1bd1c-136">Nurodytas skirstymo pagal terminus laikotarpis nustato įdarbinimo projektus, įtrauktus į išklotinę **Suskirstyti pagal terminus projektai**, esančią darbo srityje **Įdarbinimo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="1bd1c-137">Nurodytas prašymo pateikimo termino įspėjimo laikotarpis yra naudojamas įdarbinimo projektams, kurių prašymo pateikimo terminas artėja, rodyti išklotinėje **Prašymo pateikimo terminas artėja**, esančioje darbo srityje **Įdarbinimas**.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="1bd1c-138">Daugiau informacijos apie įdarbinimą žr. skyriuje [Kandidatų į darbo vietas įdarbinimas](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="1bd1c-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="1bd1c-139">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="1bd1c-139">Compensation</span></span>

<span data-ttu-id="1bd1c-140">Programoje „Dynamics 365 Finance“ skirtuko **Kompensacija** nustatymai apibrėžia, ar naudotojai turi patvirtinti, kad nori išsaugoti informaciją fiksuotosios arba kintamosios atlyginimo dalies plane.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="1bd1c-141">Jei pasirinksite **Įgalinti tikrinimo įrašymą**, uždarydami su kompensacija susijusį puslapį vartotojai gaus pranešimą, kuriame klausiama, ar jie nori įrašyti įrašą.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="1bd1c-142">Kai kuriuose kompensacijos valdymo puslapiuose naudotojai informacijos naikinti negali.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="1bd1c-143">Reikalaudami, kad naudotojai patvirtintų, jog jie nori įrašyti informaciją, galėsite riboti informaciją, kuri įrašoma, bet kurios vėliau negalima panaikinti.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="1bd1c-144">Jei išdalysite žymės langelį **Aktyvinti įrašymo tvirtinimą**, įrašai išsaugomi iš karto, galimai anksčiau nei tai padaro naudotojas.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="1bd1c-145">Jei naudojate našumo valdymą, skirtuke **Kompensacija** taip pat galite pasirinkti vertinimo modelį, kuris bus naudojamas vietoje modelio, vertinant našumą priskirto kompensavimo planams.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="1bd1c-146">Personalo dalyje naudodami skirtuką **Kompensacija** galite pasirinkti apriboti prieigą prie kompensacijos planų ir nustatyti numatytąją valiutą.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="1bd1c-147">Daugiau informacijos apie kompensaciją žr. skyriuje [Kompensacijų planų apžvalga](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1bd1c-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Atlyginimo skirtukas](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="1bd1c-149">Numeracija</span><span class="sxs-lookup"><span data-stu-id="1bd1c-149">Number sequences</span></span>

<span data-ttu-id="1bd1c-150">Nustatymai skirtuke **Numerių seka** apibrėžia sekas, naudojama automatiniam ID priskyrimui personalo prekėms, pvz.:</span><span class="sxs-lookup"><span data-stu-id="1bd1c-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="1bd1c-151">Prašymai</span><span class="sxs-lookup"><span data-stu-id="1bd1c-151">Applications</span></span>
- <span data-ttu-id="1bd1c-152">Neatvykimo registracijos</span><span class="sxs-lookup"><span data-stu-id="1bd1c-152">Absence registrations</span></span>
- <span data-ttu-id="1bd1c-153">Kompensavimo proceso rezultatai</span><span class="sxs-lookup"><span data-stu-id="1bd1c-153">Compensation process results</span></span>
- <span data-ttu-id="1bd1c-154">Atvejų numeriai</span><span class="sxs-lookup"><span data-stu-id="1bd1c-154">Case numbers</span></span>
- <span data-ttu-id="1bd1c-155">Kursai</span><span class="sxs-lookup"><span data-stu-id="1bd1c-155">Courses</span></span>
- <span data-ttu-id="1bd1c-156">Kurso darbotvarkės</span><span class="sxs-lookup"><span data-stu-id="1bd1c-156">Course agendas</span></span>

<span data-ttu-id="1bd1c-157">Norėdami prižiūrėti numeracijų nuorodas ir kodus, naudokite **Numeracijos** sąrašo puslapį (pasirinkite **Organizacijos administravimas > Numeracijos > Numeracijos**).</span><span class="sxs-lookup"><span data-stu-id="1bd1c-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="1bd1c-158">Daugiau informacijos žr. skyriuje [Numeracijos apžvalga](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="1bd1c-158">For more information, see [Number sequences overview](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="1bd1c-159">Išdirbtų valandų skaičius negali viršyti 1 250, o įdarbinimo trukmė negali viršyti 12 mėnesių.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="1bd1c-160">Šios didžiausios galimos reikšmės atitinka Jungtinių Amerikos Valstijų federalinę teisę.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-160">These maximum values are in accordance with federal law in the United States.</span></span>

![Numeracijų skirtukas](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="1bd1c-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="1bd1c-162">FMLA</span></span>

<span data-ttu-id="1bd1c-163">Skirtuke FMLA nustatote FMLA tinkamumo reikalavimus ir FMLA atostogų valandas.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="1bd1c-164">Dėl daugiau informacijos, žr. [Konfigūruoti atostogų ir nebuvimo parametrus](hr-leave-and-absence-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1bd1c-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![FMLA skirtukas](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="1bd1c-166">Darbuotojų savitarna</span><span class="sxs-lookup"><span data-stu-id="1bd1c-166">Employee self service</span></span>

<span data-ttu-id="1bd1c-167">Skirtuko **Darbuotojo savitarna** nustatymai veikia tai, kaip darbuotojo savitarnos paslauga rodoma darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="1bd1c-168">Šiame skirtuke galima:</span><span class="sxs-lookup"><span data-stu-id="1bd1c-168">On this tab, you can:</span></span>

- <span data-ttu-id="1bd1c-169">keisti darbuotojo savitarnos darbo srities pavadinimą,</span><span class="sxs-lookup"><span data-stu-id="1bd1c-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="1bd1c-170">pasirinkti, kurią informaciją vadovas gali įvesti darbuotojams,</span><span class="sxs-lookup"><span data-stu-id="1bd1c-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="1bd1c-171">pridėti naudingų nuorodų darbuotojams,</span><span class="sxs-lookup"><span data-stu-id="1bd1c-171">Add useful links for employees</span></span>
- <span data-ttu-id="1bd1c-172">apriboti leidimus darbuotojams pridėti ar redaguoti įmonės kontaktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="1bd1c-173">Daugiau informacijos žr. skyriuje [Asmens informacijos redagavimo apribojimas](hr-employee-self-service-restrict-editing.md).</span><span class="sxs-lookup"><span data-stu-id="1bd1c-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="1bd1c-174">Daugiau informacijos apie tai, kaip nustatyti darbuotojo savitarną, žr. skyriuje [Darbuotojo ir vadovo savitarnos apžvalga](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1bd1c-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Darbuotojų savitarnos skirtukas](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="1bd1c-176">Vadovų savitarna</span><span class="sxs-lookup"><span data-stu-id="1bd1c-176">Manager self service</span></span>

<span data-ttu-id="1bd1c-177">Skirtuko **Vadovo savitarna** nustatymai daro įtaką tam, ką vadovai mato savo vadovo savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="1bd1c-178">Šiame skirtuke galima konfigūruoti šias parinktis:</span><span class="sxs-lookup"><span data-stu-id="1bd1c-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="1bd1c-179">Įrašų, kurių galiojimas baigiasi, diapazonas</span><span class="sxs-lookup"><span data-stu-id="1bd1c-179">The range for expiring records</span></span>
- <span data-ttu-id="1bd1c-180">Informaciją, kurią vadovai gali peržiūrėti įrašų su besibaigiančiu galiojimu srityje</span><span class="sxs-lookup"><span data-stu-id="1bd1c-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="1bd1c-181">Ar vadovai gali peržiūrėti atviras pareigas išplėstinėms ataskaitoms</span><span class="sxs-lookup"><span data-stu-id="1bd1c-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="1bd1c-182">Esamų darbuotojų rodiniai</span><span class="sxs-lookup"><span data-stu-id="1bd1c-182">Views of exiting workers</span></span>
- <span data-ttu-id="1bd1c-183">Naudingos nuorodos vadovams</span><span class="sxs-lookup"><span data-stu-id="1bd1c-183">Useful links for managers</span></span>

<span data-ttu-id="1bd1c-184">Daugiau informacijos apie tai, kaip nustatyti vadovo savitarną, žr. skyriuje [Darbuotojo ir vadovo savitarnos apžvalga](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1bd1c-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Vadovo savitarnos skirtukas](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="1bd1c-186">Išmokų valdymas</span><span class="sxs-lookup"><span data-stu-id="1bd1c-186">Benefits management</span></span>

<span data-ttu-id="1bd1c-187">Išmokų valdymo skirtuke galima konfigūruoti el. pašto parinktis išmokų valdymui.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="1bd1c-188">Informacijos apie tai, kaip nustatyti ir naudoti išmokų valdymą, žr. skyriuje [Išmokų valdymo apžvalga](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1bd1c-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![Išmokų valdymo skirtukas](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="1bd1c-190">Atostogos ir neatvykimai</span><span class="sxs-lookup"><span data-stu-id="1bd1c-190">Leave and absence</span></span>

<span data-ttu-id="1bd1c-191">Daugiau informacijos apie atostogų ir neatvykimo nustatymą ir naudojimą žr. skyriuje [Atostogų ir neatvykimo apžvalga](hr-leave-and-absence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1bd1c-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="1bd1c-192">Mokėjimo būdai</span><span class="sxs-lookup"><span data-stu-id="1bd1c-192">Payment methods</span></span>

<span data-ttu-id="1bd1c-193">Skirtuke **Mokėjimo būdai** galima pasirinkti jūsų įmonės palaikomus mokėjimo būdus.</span><span class="sxs-lookup"><span data-stu-id="1bd1c-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="1bd1c-194">Daugiau informacijos apie kompensacijos konfigūravimą žr. skyriuje [Kompensacijų planų apžvalga](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1bd1c-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Mokėjimo būdų skirtukas](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]