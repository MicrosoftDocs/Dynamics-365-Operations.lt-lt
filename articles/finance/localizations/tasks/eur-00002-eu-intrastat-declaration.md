---
title: EUR-00002 ES Intrastat deklaracijos generavimas
description: Šia procedūra rodomi veiksmai, kuriuos reikia atlikti norint elektroniniu failo formatu eksportuoti Intrastat deklaraciją ir „Excel‟ formatu peržiūrėti deklaracijos duomenis.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2aba5caaaf0fbee511e1a293b09fa8301bb6831
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145269"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a><span data-ttu-id="edc2a-103">EUR-00002 ES Intrastat deklaracijos generavimas</span><span class="sxs-lookup"><span data-stu-id="edc2a-103">EUR-00002 Generate an EU Intrastat declaration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="edc2a-104">Šia procedūra rodomi veiksmai, kuriuos reikia atlikti norint elektroniniu failo formatu eksportuoti Intrastat deklaraciją ir „Excel‟ formatu peržiūrėti deklaracijos duomenis.</span><span class="sxs-lookup"><span data-stu-id="edc2a-104">This procedure walks you through the steps required to export the Intrastat declaration in the electronic file format and preview the declaration data in an Excel format.</span></span> 

<span data-ttu-id="edc2a-105">Kol operacijų neperkelsite į Intrastat, tol negalėsite atlikti šios procedūros.</span><span class="sxs-lookup"><span data-stu-id="edc2a-105">Before you can complete this procedure, you must transfer transactions to the Intrastat.</span></span> 

<span data-ttu-id="edc2a-106">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonės DEMF.</span><span class="sxs-lookup"><span data-stu-id="edc2a-106">This procedure was created using the demo data company DEMF.</span></span>


## <a name="import-configurations-with-settings"></a><span data-ttu-id="edc2a-107">Konfigūracijų su parametrais importavimas</span><span class="sxs-lookup"><span data-stu-id="edc2a-107">Import configurations with settings</span></span>
1. <span data-ttu-id="edc2a-108">Pasirinkite Darbo sritys > Elektroninės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="edc2a-108">Go to Workspaces > Electronic reporting</span></span>
2. <span data-ttu-id="edc2a-109">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="edc2a-109">Click Set active.</span></span>
3. <span data-ttu-id="edc2a-110">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="edc2a-110">Click Repositories.</span></span>
4. <span data-ttu-id="edc2a-111">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="edc2a-111">Click Open.</span></span>
5. <span data-ttu-id="edc2a-112">Atidarykite stulpelio filtrą Konfigūracijos pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="edc2a-112">Open Configuration name column filter.</span></span>
6. <span data-ttu-id="edc2a-113">Lauke Konfigūracijos pavadinimas pritaikykite filtrą, naudodami reikšmę „Intrastat (DE)‟ ir filtro operatorių „prasideda‟.</span><span class="sxs-lookup"><span data-stu-id="edc2a-113">Apply a filter on the "Configuration name" field, with a value of "Intrastat (DE)", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="edc2a-114">Turėtumėte pasirinkti tinkamą jūsų juridinio subjekto šalies konfigūracijos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="edc2a-114">You should select the configuration name applicable for the country of your legal entity.</span></span> <span data-ttu-id="edc2a-115">Šioje procedūroje kaip pavyzdys naudojamas Vokietijos juridinis subjektas (DEMF), todėl reikėtų pasirinkti „Intrastat (DE)".</span><span class="sxs-lookup"><span data-stu-id="edc2a-115">This procedure uses the German legal entity (DEMF) as an example, therefore "Intrastat (DE)" should be chosen.</span></span>  
    * <span data-ttu-id="edc2a-116">Spustelėkite Importuoti, tada spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="edc2a-116">Click Import and then click Yes.</span></span>  
7. <span data-ttu-id="edc2a-117">Atidarykite stulpelio filtrą Konfigūracijos pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="edc2a-117">Open Configuration name column filter.</span></span>
8. <span data-ttu-id="edc2a-118">Lauke Konfigūracijos pavadinimas pritaikykite filtrą, naudodami reikšmę „Intrastat ataskaita‟ ir filtro operatorių „prasideda‟.</span><span class="sxs-lookup"><span data-stu-id="edc2a-118">Apply a filter on the "Configuration name" field, with a value of "intrastat report", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="edc2a-119">Spustelėkite Importuoti, tada spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="edc2a-119">Click Import and then click Yes.</span></span>  

## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="edc2a-120">Užsienio prekybos parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="edc2a-120">Set up Foreign trade parameters</span></span>
1. <span data-ttu-id="edc2a-121">Pasirinkite Mokesčiai > Nustatymai > Užsienio prekyba > Užsienio prekybos parametrai.</span><span class="sxs-lookup"><span data-stu-id="edc2a-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
2. <span data-ttu-id="edc2a-122">Išplėskite skyrių Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="edc2a-122">Expand the Electronic reporting section.</span></span>
3. <span data-ttu-id="edc2a-123">Lauke Failo formato susiejimas įveskite arba pasirinkite reikšmę Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="edc2a-123">In the File format mapping field, enter or select a value Intrastat (DE)</span></span>
4. <span data-ttu-id="edc2a-124">Lauke Ataskaitos formato susiejimas įveskite arba pasirinkite reikšmę Intrastat ataskaita.</span><span class="sxs-lookup"><span data-stu-id="edc2a-124">In the Report format mapping field, enter or select a value Intrastat report</span></span>
5. <span data-ttu-id="edc2a-125">Išplėskite skyrių Apvalinimo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="edc2a-125">Expand the Rounding rules section.</span></span>
    * <span data-ttu-id="edc2a-126">Turėtumėte nustatyti Intrastat ataskaitų apvalinimo taisykles, taikomas jūsų šalyje / regione.</span><span class="sxs-lookup"><span data-stu-id="edc2a-126">You should set up rounding rules that are applicable in your country/region for Intrastat reporting.</span></span>  
6. <span data-ttu-id="edc2a-127">Lauke Apvalinimo taisyklė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="edc2a-127">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="edc2a-128">Įveskite apvalinimo tikslumą, pavyzdžiui, įveskite „0,01‟.</span><span class="sxs-lookup"><span data-stu-id="edc2a-128">Enter rounding precision, for example, enter '0.01'.</span></span>  
7. <span data-ttu-id="edc2a-129">Lauke Sumos skaitmenų po kablelio skaičius įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="edc2a-129">In the Number of decimals for amount field, enter a number.</span></span>
    * <span data-ttu-id="edc2a-130">Pvz., įveskite „2‟.</span><span class="sxs-lookup"><span data-stu-id="edc2a-130">For example, enter '2'.</span></span>  
8. <span data-ttu-id="edc2a-131">Lauke Apvalinimas žemiau 1 kg pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="edc2a-131">In the Rounding below 1 kg field, select an option.</span></span>
    * <span data-ttu-id="edc2a-132">Pavyzdžiui, pasirinkite Apvalinimas iki 1 kg.</span><span class="sxs-lookup"><span data-stu-id="edc2a-132">For example, select 'Rounding up to 1 kg'.</span></span>  
9. <span data-ttu-id="edc2a-133">Lauke Apvalinimo taisyklė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="edc2a-133">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="edc2a-134">Pavyzdžiui, įveskite „1‟, kad svorį apvalintumėte iki sveikojo skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="edc2a-134">For example, enter '1' for rounding weight to the integer.</span></span>  
10. <span data-ttu-id="edc2a-135">Išplėskite dalį Mažiausia riba.</span><span class="sxs-lookup"><span data-stu-id="edc2a-135">Expand the Minimum limit section.</span></span>
11. <span data-ttu-id="edc2a-136">Lauke Svoris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="edc2a-136">In the Weight field, enter a number.</span></span>
    * <span data-ttu-id="edc2a-137">Pavyzdžiui, kaip mažiausią svorį įveskite „10‟.</span><span class="sxs-lookup"><span data-stu-id="edc2a-137">For example, enter '10' as the minimum weight.</span></span>  
12. <span data-ttu-id="edc2a-138">Lauke Suma įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="edc2a-138">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="edc2a-139">Pavyzdžiui, kaip mažiausią sumą įveskite „200‟.</span><span class="sxs-lookup"><span data-stu-id="edc2a-139">For example, enter '200' as the minimum amount.</span></span>  
13. <span data-ttu-id="edc2a-140">Lauke Prekė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="edc2a-140">In the Commodity field, enter or select a value.</span></span>

## <a name="set-up-compression-of-intrastat"></a><span data-ttu-id="edc2a-141">Intrastat glaudinimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="edc2a-141">Set up Compression of Intrastat</span></span>
1. <span data-ttu-id="edc2a-142">Pasirinkite Mokesčiai > Nustatymas > Užsienio prekyba > Intrastat glaudinimas.</span><span class="sxs-lookup"><span data-stu-id="edc2a-142">Go to Tax > Setup > Foreign trade > Compression of Intrastat.</span></span>
2. <span data-ttu-id="edc2a-143">Spustelėkite Šalinti.</span><span class="sxs-lookup"><span data-stu-id="edc2a-143">Click Remove.</span></span>
3. <span data-ttu-id="edc2a-144">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="edc2a-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="edc2a-145">Pavyzdžiui, dalyje Yra pasirinkite Prekė.</span><span class="sxs-lookup"><span data-stu-id="edc2a-145">For example, select Commodity in the Available section.</span></span>  
4. <span data-ttu-id="edc2a-146">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="edc2a-146">Click Add.</span></span>

## <a name="generate-intrastat-declaration"></a><span data-ttu-id="edc2a-147">Intrastat deklaracijos generavimas</span><span class="sxs-lookup"><span data-stu-id="edc2a-147">Generate Intrastat declaration</span></span>
1. <span data-ttu-id="edc2a-148">Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat</span><span class="sxs-lookup"><span data-stu-id="edc2a-148">Go to Tax > Declarations > Foreign trade > Intrastat</span></span>
2. <span data-ttu-id="edc2a-149">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="edc2a-149">Click Validate.</span></span>
    * <span data-ttu-id="edc2a-150">Tikrinama pagal puslapio Užsienio prekybos parametrai lauką Tikrinti nustatymus.</span><span class="sxs-lookup"><span data-stu-id="edc2a-150">The validation is done according to the Check setup field on the Foreign trade parameters page.</span></span>  
3. <span data-ttu-id="edc2a-151">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="edc2a-151">Click OK.</span></span>
4. <span data-ttu-id="edc2a-152">Spustelėkite Naujinti.</span><span class="sxs-lookup"><span data-stu-id="edc2a-152">Click Update.</span></span>
5. <span data-ttu-id="edc2a-153">Spustelėkite Mažiausia riba.</span><span class="sxs-lookup"><span data-stu-id="edc2a-153">Click Minimum limit.</span></span>
6. <span data-ttu-id="edc2a-154">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="edc2a-154">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="edc2a-155">Pvz., įveskite 2015 m. sausio 1 d.</span><span class="sxs-lookup"><span data-stu-id="edc2a-155">For example, enter January 1, 2015.</span></span>  
7. <span data-ttu-id="edc2a-156">Lauke Glaudinti pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="edc2a-156">Select Yes in the Compress field.</span></span>
8. <span data-ttu-id="edc2a-157">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="edc2a-157">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="edc2a-158">Pvz., įveskite 2015 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="edc2a-158">For example, enter January 31, 2015.</span></span>  
9. <span data-ttu-id="edc2a-159">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="edc2a-159">Click OK.</span></span>
10. <span data-ttu-id="edc2a-160">Spustelėkite Naujinti.</span><span class="sxs-lookup"><span data-stu-id="edc2a-160">Click Update.</span></span>
11. <span data-ttu-id="edc2a-161">Spustelėkite Glaudinti.</span><span class="sxs-lookup"><span data-stu-id="edc2a-161">Click Compress.</span></span>
    * <span data-ttu-id="edc2a-162">Šis glaudinimas vyksta atsižvelgiant į tai, kaip nustatėte Intrastat glaudinimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="edc2a-162">This compression happens according to how you set the Compression of intrastate settings.</span></span>  
12. <span data-ttu-id="edc2a-163">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="edc2a-163">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="edc2a-164">Pvz., įveskite 2015 m. sausio 1 d.</span><span class="sxs-lookup"><span data-stu-id="edc2a-164">For example, enter January 1, 2015.</span></span>  
13. <span data-ttu-id="edc2a-165">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="edc2a-165">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="edc2a-166">Pvz., įveskite 2015 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="edc2a-166">For example, enter 31st January 2015.</span></span>  
14. <span data-ttu-id="edc2a-167">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="edc2a-167">Click OK.</span></span>
15. <span data-ttu-id="edc2a-168">Spustelėkite Naujinti.</span><span class="sxs-lookup"><span data-stu-id="edc2a-168">Click Update.</span></span>
16. <span data-ttu-id="edc2a-169">Spustelėkite Regeneruoti eilės numerius.</span><span class="sxs-lookup"><span data-stu-id="edc2a-169">Click Regenerate sequence numbers.</span></span>
17. <span data-ttu-id="edc2a-170">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="edc2a-170">Click OK.</span></span>
18. <span data-ttu-id="edc2a-171">Spustelėkite Išvestis.</span><span class="sxs-lookup"><span data-stu-id="edc2a-171">Click Output.</span></span>
19. <span data-ttu-id="edc2a-172">Spustelėkite Ataskaita.</span><span class="sxs-lookup"><span data-stu-id="edc2a-172">Click Report.</span></span>
20. <span data-ttu-id="edc2a-173">Lauke Pradžios data įveskite pirmąją ataskaitinio laikotarpio datą.</span><span class="sxs-lookup"><span data-stu-id="edc2a-173">In the From date field, enter the first date of the reporting period.</span></span>
    * <span data-ttu-id="edc2a-174">Pavyzdžiui, nustatykite datą 2015 m. sausio 1 d.</span><span class="sxs-lookup"><span data-stu-id="edc2a-174">For example, set the date to January 1, 2015.</span></span>  
21. <span data-ttu-id="edc2a-175">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="edc2a-175">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="edc2a-176">Pvz., įveskite 2015 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="edc2a-176">For example, enter January 31, 2015.</span></span>  
22. <span data-ttu-id="edc2a-177">Lauke Generuoti failą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="edc2a-177">Select Yes in the Generate file field.</span></span>
23. <span data-ttu-id="edc2a-178">Lauke „Failo pavadinimas“ suveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="edc2a-178">In the File name field, type a value.</span></span>
24. <span data-ttu-id="edc2a-179">Lauke Generuoti ataskaitą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="edc2a-179">Select Yes in the Generate report field.</span></span>
25. <span data-ttu-id="edc2a-180">Lauke Ataskaitos failo pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="edc2a-180">In the Report file name field, type a value.</span></span>
26. <span data-ttu-id="edc2a-181">Lauke Kryptis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="edc2a-181">In the Direction field, select an option.</span></span>
    * <span data-ttu-id="edc2a-182">Pavyzdžiui, pasirinkite Išsiuntimai.</span><span class="sxs-lookup"><span data-stu-id="edc2a-182">For example, select 'Dispatches'.</span></span>  
27. <span data-ttu-id="edc2a-183">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="edc2a-183">Click OK.</span></span>

