---
title: Pasiūlymų valdymo nustatymas „Attract“
description: Šioje temoje aprašoma, kaip nustatyti „Microsoft Dynamics 365 Talent“ pasiūlymus.
author: andreabichsel
manager: AnnBe
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc91a83afd5ce1627376685bcf612d6998ddbc02
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461985"
---
# <a name="set-up-offer-management-in-attract"></a><span data-ttu-id="f4cd9-103">Pasiūlymų valdymo nustatymas „Attract“</span><span class="sxs-lookup"><span data-stu-id="f4cd9-103">Set up offer management in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f4cd9-104">Kai kandidatas perkeliamas į „Dynamics 365 Talent: Attract“ pasiūlymo etapą, reikia užtikrinti, kad bus galima greitai kurti kandidatui skirtus pasiūlymus, juos atitinkamai patvirtinti ir išsiųsti kandidatui.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-104">When a candidate is moved to the offer stage in Dynamics 365 Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="f4cd9-105">Kadangi dauguma pasiūlymų standartiniai, juos galima sukurti naudojant pakartotinai naudotinus šablonus.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="f4cd9-106">Naudojantis „Attract“ visi pasiūlymai įtraukiami į pasiūlymų paketą, kuris yra vieno ar kelių pasiūlymo dokumentų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="f4cd9-107">Šioje temoje pateikiamas visų veiksmų, kuriuos turėtų atlikti „Attract“ administratorius, norėdamas kaip „Attract“ pasiūlymo valdymo galimybės dalį nustatyti kitus pasiūlymo paketo šablonus, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="f4cd9-108">Vartotojai, kuriems priskirti ne administratoriaus vaidmenys, šiomis galimybėmis naudotis negalės.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="f4cd9-109">Pasiūlymo valdymo galimybės pateikiamos kaip išsamios įdarbinimo informacijos priedo dalis.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="f4cd9-110">Pasiūlymo duomenys</span><span class="sxs-lookup"><span data-stu-id="f4cd9-110">Offer data</span></span> 

<span data-ttu-id="f4cd9-111">Pasiūlymo duomenys yra mažiausias pasiūlymo paketo šablono vienetas.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="f4cd9-112">Įprastą pasiūlymą sudaro standartinis tekstas ir reikšmių rinkinys.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="f4cd9-113">Reikšmių rinkiniai yra vienintelės tarp pasiūlymų galinčios pasikeisti dalys.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="f4cd9-114">Kuriant pasiūlymą svarbiausias aspektas, į kurį atsižvelgia pasiūlymo kūrėjas, yra pasiūlymo paketo šablone esančių pasiūlymo duomenų vietos rezervavimo ženklų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="f4cd9-115">Norėdami nustatyti pasiūlymo duomenis, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="f4cd9-116">Eikite į **Pasiūlymo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="f4cd9-117">Išplėskite kairiosios naršymo srities skyrių **Biblioteka**, paskui eikite į **Pasiūlymo duomenys**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="f4cd9-118">Puslapyje **Pasiūlymo duomenys** yra skyrius **Kandidato informacija** ir **Informacija apie darbą**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="f4cd9-119">„Attract“ siūloma keletas parengtų naudoti pasiūlymo duomenų vietos rezervavimo ženklų.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    > 
    > <span data-ttu-id="f4cd9-120">Puslapyje yra skyrių, skirtų grupuoti skirtingus pasiūlymų duomenų vietos rezervavimo ženklus į logines grupes.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="f4cd9-121">Šie skyriai gali padėti tvarkyti pasiūlymo duomenis ir įvesti duomenis kuriant pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>
    > 
    > <span data-ttu-id="f4cd9-122">Norėdami sukurti vietos rezervavimo ženklo reikšmių sąrašą, įkelkite „Excel“ skaičiuoklę, kurioje yra vienas stulpelis su vietos rezervavimo ženklu kaip stulpelio pavadinimas ir eilučių, esančių apačioje, pasirinkimų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-122">To create a list of values for a placeholder, upload an Excel spreadsheet that has one column with the placeholder as the column title and the list of choices in the rows underneath.</span></span> <span data-ttu-id="f4cd9-123">Jei tas pats vietos rezervavimo ženklas nurodomas kitame duomenų taisyklių rinkinyje, įsitikinkite, kad jie turi bendrą reikšmių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-123">If the same placeholder is referenced in another data rule set, ensure they have a common set of values.</span></span>
    
1.  <span data-ttu-id="f4cd9-124">Norėdami sukurti naują pasiūlymo duomenų skyrių, spustelėkite **Įtraukti skyrių** ir įveskite unikalų skyriaus pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-124">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="f4cd9-125">Norėdami pasiūlymo duomenų vietos rezervavimo ženklus įtraukti į bet kurį skyrių, spustelėkite **Įtraukti pasiūlymo duomenis** ir įveskite unikalų vietos rezervavimo ženklo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-125">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="f4cd9-126">Norėdami redaguoti bet kurio skyriaus pavadinimą, laikykite žymiklį virš skyriaus pavadinimo ir atnaujinkite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-126">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="f4cd9-127">Norėdami redaguoti bet kurio esamo pasiūlymo duomenų vietos rezervavimo ženklo pavadinimą, pirmiausia įsitikinkite, kad vietos rezervavimo ženklas nėra jokio šablono dalis.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-127">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="f4cd9-128">Paskui, laikydami žymiklį virš pasiūlymo duomenų vietos rezervavimo ženklo pavadinimo, atnaujinkite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-128">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="f4cd9-129">Norėdami panaikinti esamą pasiūlymo duomenų vietos rezervavimo ženklą, pirmiausia įsitikinkite, kad vietos rezervavimo ženklas nėra jokio kito šablono dalis.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-129">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="f4cd9-130">Paskui laikykite žymiklį virš vietos rezervavimo ženklo ir, pasirodžius šiukšliadėžės piktogramai, spustelėkite ją ir panaikinkite pasiūlymo duomenų vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-130">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="f4cd9-131">Šalia kiekvieno pasiūlymo duomenų esantis skaičius nurodo, keliems šablonams priskiriamas pasiūlymo duomenų vietos rezervavimo ženklas.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-131">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="f4cd9-132">Norėdami panaikinti bet kurį skyrių, laikykite žymiklį virš pavadinimo.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-132">To delete any section, hover over the name.</span></span> <span data-ttu-id="f4cd9-133">Jei nė vienas skyriaus pasiūlymo duomenų vietos rezervavimo ženklų nerodomas jokiame šablone, spustelėję šiukšliadėžės piktogramą galite jį panaikinti.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-133">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="f4cd9-134">Panaikinus skyrių taip pat panaikinami visi to skyriaus pasiūlymo duomenų vietos rezervavimo ženklai.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-134">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="f4cd9-135">Nustatę pasiūlymo duomenų vietos rezervavimo ženklus, galite juos naudoti bet kuriame dokumento šablone.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-135">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="f4cd9-136">Pasiūlymo duomenų vietos rezervavimo ženklai gali būti naudojami ne tik konkrečiame šablone -- tą patį rinkinį galima naudoti visuose šablonuose.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-136">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="f4cd9-137">Pasiūlymo duomenų taisyklės</span><span class="sxs-lookup"><span data-stu-id="f4cd9-137">Offer data rules</span></span>

<span data-ttu-id="f4cd9-138">Daugumoje organizacijų nustatytos pasiūlymų kūrimo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-138">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="f4cd9-139">Pavyzdžiui, organizacija gali reikalauti, kad maksimalaus metinio konkrečios vietos atlyginimo pasiūlymo ir paaukštinimo lygio derinys patektų į tam tikrą intervalą, arba kad samdant naują darbuotoją būtų galimos tik kelios konkrečios pasiūlymo lygio vertės.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-139">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="f4cd9-140">„Attract“ šiuo metu palaiko visas tokias duomenų taisykles (naudojant CSV failą).</span><span class="sxs-lookup"><span data-stu-id="f4cd9-140">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="f4cd9-141">Norėdami parengti duomenų taisyklių CSV failą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-141">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="f4cd9-142">Nustatykite taisyklių rinkinio pasiūlymo duomenų vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-142">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="f4cd9-143">Pavyzdžiui, **Metinis atlyginimas**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-143">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="f4cd9-144">Nurodykite priklausomąsias pasiūlymo duomenų vietos rezervavimo ženklo vertes.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-144">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="f4cd9-145">Pavyzdžiui, **Darbo vieta** ir **Lygis**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-145">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="f4cd9-146">1 ir 2 stulpelyje nurodykite **Darbo vieta** ir **Lygis**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-146">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="f4cd9-147">Norint įkelti intervalo vertę, 3 ir 4 stulpeliai turi būti **Metinis atlyginimas**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-147">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="f4cd9-148">Norint įkelti konkrečią reikšmę, o ne intervalą, 3 stulpelis turi būti **Metinis atlyginimas**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-148">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="f4cd9-149">Automatiškai užpildykite „Microsoft Excel“ failą pagal reikiamus vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-149">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="f4cd9-150">Patikrinkite, ar kiekvienoje eilutėje pateikiama unikali visų susumuotų verčių kombinacija.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-150">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="f4cd9-151">Failą išsaugokite CSV formatu.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-151">Save the file as a CSV format.</span></span>

<span data-ttu-id="f4cd9-152">Norėdami įkelti pasiūlymo duomenų taisyklių failą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-152">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="f4cd9-153">Eikite į **Pasiūlymo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-153">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="f4cd9-154">Išplėskite kairiosios naršymo srities skyrių **Biblioteka**, paskui eikite į **Pasiūlymo duomenų taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-154">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="f4cd9-155">Spustelėjus **Naujas duomenų rinkinys** rodomas dialogo langas **Įkelti**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-155">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="f4cd9-156">Nurodykite unikalų taisyklių rinkinio pavadinimą, paskui įkelkite išsaugotą CSV failą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-156">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="f4cd9-157">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-157">Click **Add**.</span></span>
    <span data-ttu-id="f4cd9-158">Taisyklių rinkinys bus vykdomas fone ir jums bus pranešta (programoje ir elektroniniu paštu), kai veiksmas bus baigtas.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-158">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="f4cd9-159">Jums bus pranešta, jei vykdant įkėlimą kiltų klaidų.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-159">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="f4cd9-160">Tada galite atsisiųsti klaidų žurnalą, pataisyti failą ir įkelti jį dar kartą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-160">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="f4cd9-161">Norėdami atsisiųsti taisyklių rinkinį ir atnaujinti reikšmių rinkinį (**…**), naudokitės elipsės mygtuko parinktimi.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-161">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="f4cd9-162">Atlikę atnaujinimą failą galite įkelti dar kartą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-162">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="f4cd9-163">Galite panaikinti esamą taisyklių rinkinio įkėlimą (jei apibrėžiamas vietos rezervavimo ženklas nenaudojamas kitame dokumento šablone).</span><span class="sxs-lookup"><span data-stu-id="f4cd9-163">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="f4cd9-164">Kiekvienas vietos rezervavimo ženklas gali turėti tik vieną unikalų stulpelių rinkinį, nuo kurio jis priklauso.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-164">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="f4cd9-165">Pavyzdžiui, jei **Metinis atlyginimas** priklauso nuo verčių **Darbo vieta** ir **Lygis**, negalite įkelti kito taisyklių rinkinio, kuriame **Metinis atlyginimas** priklauso nuo kito stulpelių rinkinio.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-165">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="f4cd9-166">Pasiūlymo duomenų taisyklių rinkinių pavyzdžius galite atsisiųsti iš puslapio **Pasiūlymo duomenų taisyklės** skirtuko **Pavyzdžiai**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-166">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="f4cd9-167">Kai pasiūlymo kūrėjas perrašo pasiūlymo duomenų taisyklėse rekomenduojamas vertes, pasiūlymas pažymimas kaip nestandartinis, o pasiūlymo patvortinimo darbo eiga privaloma.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-167">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="f4cd9-168">Dokumento šablonai</span><span class="sxs-lookup"><span data-stu-id="f4cd9-168">Document templates</span></span>

<span data-ttu-id="f4cd9-169">Pasiūlymo dokumento šablonas gali būti pagalba administratoriams kuriant pasiūlymo laiškus.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-169">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="f4cd9-170">Pasiūlymo dokumento šablonas yra į pasiūlymą ketinamas įtraukti tekstas, taip pat nurodyti pasiūlymo duomenų vietos rezervavimo ženklai.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-170">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="f4cd9-171">Norėdami sukurti pasiūlymo dokumento šabloną, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-171">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="f4cd9-172">Eikite į **Pasiūlymo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-172">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="f4cd9-173">Išplėskite kairiosios naršymo srities skyrių **Biblioteka** ir eikite į **Šablonai**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-173">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="f4cd9-174">Puslapyje **Šablonai** rodomas jau apibrėžtų dokumentų šablonų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-174">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="f4cd9-175">Norėdami sukurti naują dokumento šabloną, spustelėkite **Naujas šablonas**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-175">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="f4cd9-176">Įveskite unikalų šablono pavadinimą ir spustelėkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-176">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="f4cd9-177">Naudodamiesi raiškiojo teksto rengykle galite įterpti arba redaguoti pasiūlymo dokumento turinį.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-177">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="f4cd9-178">Naudodamiesi tekstų rengyklės viršuje pateikiamomis parinktimis, galite įterpti lentelių, vaizdų ir hipersaitų.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-178">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="f4cd9-179">Norėdami į pasiūlymo šablono dokumentą įtraukti pasiūlymo duomenų vietos rezervavimo ženklų, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-179">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="f4cd9-180">Nuvilkite nuo dešiniosios srities.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-180">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="f4cd9-181">Saitažodžiu susiekite pasiūlymo duomenų vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-181">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="f4cd9-182">Įveskite **\#**, o paskui pradėkite rašyti pasiūlymo duomenų vietos rezervavimo ženklo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-182">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="f4cd9-183">Išplečiamajame sąraše bus rodomos parinktys.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-183">Options will appear in the drop-down list.</span></span> <span data-ttu-id="f4cd9-184">Spustelėję arba paspaudę **Enter** įveskite pasiūlymo duomenų vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-184">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="f4cd9-185">Norėdami susieti vietos rezervavimo ženklą su pasiūlymo dokumento šablonu, nenurodant jo vertės kandidatui, laikykite žymiklį virš pasiūlymo duomenų vietos rezervavimo ženklo ir spustelėkite piktogramą **Prisegti**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="f4cd9-186">Tokiu būdu vietos rezervavimo ženklas bus pastumtas į pasiūlymo dokumento šablono skyrių **Prisegti pasiūlymo duomenys**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="f4cd9-187">Norėdami atsegti, atlikite tuos pačius veiksmus, bet pasiūlymo duomenų vietos rezervavimo ženklų sąraše spustelėkite **Atsegti**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="f4cd9-188">Norėdami peržiūrėti aktyvių pasiūlymo duomenų vietos rezervavimo ženklų sąrašą, įjunkite dešiniosios srities skirtuką **Aktyvūs**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="f4cd9-189">Įterpę vietos rezervavimo ženklą, kuriam taikomas pasiūlymo duomenų taisyklių rinkinys, galite matyti to pasiūlymo vietos rezervavimo ženklo priklausomybę nuo kitų verčių.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="f4cd9-190">Arba galite **Importuoti** turinį iš jūsų vietinio įrenginio .docx failo ir atlikti reikiamus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="f4cd9-191">Tokiu būdu jums nereikės įvesti viso turinio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="f4cd9-192">Norėdami peržiūrėti pasiūlymo dokumentą, naudokitės puslapio viršuje esančia parinktimi **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="f4cd9-193">Norėdami kontroliuoti, ar pasiūlymo kūrėjas gali redaguoti pasiūlymo dokumento turinį, naudokitės puslapio viršuje esančia parinktimi **Valdyti teisę**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="f4cd9-194">Jei norite, kad pasiūlymo kūrėjas galėtų tik įterpti vietos rezervavimo ženklo vertes, bet negalėtų redaguoti teksto, nustatykite teisės vertę **Ne**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="f4cd9-195">Spustelėkite **Įrašyti** ir išsaugokite savo eigą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="f4cd9-196">Šablonas bus išsaugotas juodraščio būsenos.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="f4cd9-197">Norėdami baigti ir pažymėti dokumentą pagal tai, koks jis buvo paskelbtas, spustelėkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="f4cd9-198">Galite matyti, kurie dokumento šablonai šiuo metu aktyvūs (juodraščio režimu), taip pat yra archyvuojami ir nebus naudojami naudojantis dokumentų šablonų bibliotekos nukreipimo patirtimi.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="f4cd9-199">Galite panaikinti bet kurį pasiūlymo dokumento šabloną, kuris nėra esamo pasiūlymo paketo šablono dalis.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="f4cd9-200">Pasiūlymo paketo šablonai</span><span class="sxs-lookup"><span data-stu-id="f4cd9-200">Offer package templates</span></span>

<span data-ttu-id="f4cd9-201">Pasiūlymų paketai yra pasiūlymo artefaktai, kurie bendrinami su kandidatu ir yra sudaryti iš vieno ar kelių pasiūlymo dokumento šablonų.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="f4cd9-202">Norėdami sukurti pasiūlymo paketą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="f4cd9-203">Eikite į **Pasiūlymo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="f4cd9-204">Kairiojoje naršymo srityje eikite į **Pakuotės**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="f4cd9-205">Rodomas aktyvių paketo šablonų, kuriais gali naudotis pasiūlymo kūrėjai, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="f4cd9-206">Norėdami sukurti naują pasiūlymo paketą, spustelėkite **Naujas paketas**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="f4cd9-207">Įveskite unikalų pavadinimą ir spustelėkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="f4cd9-208">Spustelėkite **Įtraukti šabloną**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-208">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="f4cd9-209">Galite pasirinkti sukurti naują šabloną arba pasirinkti iš esamų.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-209">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="f4cd9-210">Pasirinkę įtraukti esamą šabloną turite įsitikinti, kad pasiūlymo dokumento šablonas įrašytas, baigtas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-210">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="f4cd9-211">Galite pasirinkti tiek dokumentų šablonųų, kiek norite.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-211">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="f4cd9-212">Spustelėkite **Atlikta** ir grįžkite į **Paketų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-212">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="f4cd9-213">Galite sukonfigūruoti dokumentų seką, taip pat pažymėti, ar kuriant pasiūlymą reikalingas konkretaus pasiūlymo dokumentas.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-213">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="f4cd9-214">Pasiūlymo kūrėjas turi galimybę panaikinti dokumentus, pažymėtus **Nebūtina**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-214">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="f4cd9-215">Norėdami įrašyti pasiūlymo paketo šabloną, kad juo galėtų naudotis visi pasiūlymo kūrėjai, spustelėkite **Įrašyti ir paskelbti**.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-215">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="f4cd9-216">Norėdami peržiūrėti pasiūlymo paketo šablonų juodraščius, eikite į skirtuką **Juodraščiai**. Atlikus pasiūlymo paketo šablono pakeitimą, būtina jį įrašyti ir paskelbti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-216">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="f4cd9-217">Pasiūlymo proceso konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f4cd9-217">Configure an offer process</span></span>

<span data-ttu-id="f4cd9-218">Yra keletas pasiūlymo kūrimo proceso dalių, kurias gali konfigūruoti „Attract“ administratorius.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-218">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="f4cd9-219">**Pasiūlymų patvirtinimai** – pasirinkite, ar, prieš siunčiant pasiūlymą kandidatui, būtina jį patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-219">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="f4cd9-220">Jei esate administratorius, taip pat galite nuspręsti, ar visi pasiūlymų patvirtinimai vyks eilės tvarka, ar lygiagrečia patvirtinimo darbo eiga.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-220">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="f4cd9-221">Taip pat gali nurodyti, ar pasiūlymų tvirtintojams būtina tvirtinant pasiūlymą pateikti ir komentarą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-221">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="f4cd9-222">Visų nestandartinių pasiūlymų atveju patvirtinimai būtini.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-222">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="f4cd9-223">**Kandidato pasiūlymo patirtis** – jei esate administratorius, galite pasirinkti nustatyti, ar visi pasiūlymai turės galiojimo datą, ir, jei taip, koks bus numatytasis galiojimo datos poslinkis.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-223">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="f4cd9-224">Taip pat galite sukonfigūruoti ar kandidatai gali atmesti pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-224">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="f4cd9-225">**Elektroniniai parašai** – jūs, administratorius, taip pat galite pasirinkti metodą, kurį kandidatai gali naudoti pasirašydami pasiūlymus.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-225">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="f4cd9-226">„Adobe Sign“ – visi pasiūlymų paketai bus siunčiami ir pasirašomi naudojant „Adobe Sign“.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-226">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="f4cd9-227">Kiekvienas pasiūlymo kūrėjas, publikuojantis pasiūlymą, turi būti prijungęs savo „Adobe Sign“ paskyrą prie „Attract“.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-227">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="f4cd9-228">Norėdami informacijos apie „Adobe Sign“ licencijas ir nemokamą bandomąją versiją, naudokite šį [saitą](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span><span class="sxs-lookup"><span data-stu-id="f4cd9-228">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="f4cd9-229">„DocuSign“ – visi pasiūlymų paketai bus siunčiami ir pasirašomi naudojant „DocuSign“.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-229">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="f4cd9-230">Kiekvienas pasiūlymo kūrėjas, publikuojantis pasiūlymą, turi būti prijungęs savo „DocuSign“ paskyrą prie „Attract“.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-230">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="f4cd9-231">„ESign“ – tai numatytoji parengta naudoti parinktis, kai vartotojas gali pasirašyti pasiūlymą įvesdamas savo vardą ir inicialus.</span><span class="sxs-lookup"><span data-stu-id="f4cd9-231">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="f4cd9-232">Norėdami daugiau sužinoti apie pasiūlymo kūrimo procesą, žr. [Pasiūlymų kūrimas, tvirtinimas ir pasirašymas](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="f4cd9-232">To learn more about the offer creation process, see [Create, approve, and sign offers](./creating-offers.md).</span></span>
