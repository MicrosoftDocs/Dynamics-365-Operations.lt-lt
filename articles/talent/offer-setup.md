---
title: Pasiūlymų valdymo nustatymas
description: Šioje temoje aprašoma, kaip nustatyti „Talent“ pasiūlymus.
author: andreabichsel
manager: AnnBe
ms.date: 02/04/2019
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
ms.openlocfilehash: 7fa0e5d30c06db16e105631e492af022acfcfd66
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/19/2019
ms.locfileid: "857874"
---
# <a name="set-up-offer-management"></a><span data-ttu-id="1a40a-103">Pasiūlymų valdymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="1a40a-103">Set up offer management</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="1a40a-104">Kai kandidatas perkeliamas į „Dynamics 365 for Talent: Attract“ pasiūlymo etapą, reikia užtikrinti, kad bus galima greitai kurti kandidatui skirtus pasiūlymus, juos atitinkamai patvirtinti ir išsiųsti kandidatui.</span><span class="sxs-lookup"><span data-stu-id="1a40a-104">When a candidate is moved to the offer stage in Dynamics 365 for Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="1a40a-105">Kadangi dauguma pasiūlymų standartiniai, juos galima sukurti naudojant pakartotinai naudotinus šablonus.</span><span class="sxs-lookup"><span data-stu-id="1a40a-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="1a40a-106">Naudojantis „Attract“ visi pasiūlymai įtraukiami į pasiūlymų paketą, kuris yra vieno ar kelių pasiūlymo dokumentų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="1a40a-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="1a40a-107">Šioje temoje pateikiamas visų veiksmų, kuriuos turėtų atlikti „Attract“ administratorius, norėdamas kaip „Attract“ pasiūlymo valdymo galimybės dalį nustatyti kitus pasiūlymo paketo šablonus, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="1a40a-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="1a40a-108">Vartotojai, kuriems priskirti ne administratoriaus vaidmenys, šiomis galimybėmis naudotis negalės.</span><span class="sxs-lookup"><span data-stu-id="1a40a-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="1a40a-109">Pasiūlymo valdymo galimybės pateikiamos kaip išsamios įdarbinimo informacijos priedo dalis.</span><span class="sxs-lookup"><span data-stu-id="1a40a-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="1a40a-110">Pasiūlymo duomenys</span><span class="sxs-lookup"><span data-stu-id="1a40a-110">Offer data</span></span> 

<span data-ttu-id="1a40a-111">Pasiūlymo duomenys yra mažiausias pasiūlymo paketo šablono vienetas.</span><span class="sxs-lookup"><span data-stu-id="1a40a-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="1a40a-112">Įprastą pasiūlymą sudaro standartinis tekstas ir reikšmių rinkinys.</span><span class="sxs-lookup"><span data-stu-id="1a40a-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="1a40a-113">Reikšmių rinkiniai yra vienintelės tarp pasiūlymų galinčios pasikeisti dalys.</span><span class="sxs-lookup"><span data-stu-id="1a40a-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="1a40a-114">Kuriant pasiūlymą svarbiausias aspektas, į kurį atsižvelgia pasiūlymo kūrėjas, yra pasiūlymo paketo šablone esančių pasiūlymo duomenų vietos rezervavimo ženklų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="1a40a-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="1a40a-115">Norėdami nustatyti pasiūlymo duomenis, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1a40a-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="1a40a-116">Eikite į **Pasiūlymo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="1a40a-117">Išplėskite kairiosios naršymo srities skyrių **Biblioteka**, paskui eikite į **Pasiūlymo duomenys**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="1a40a-118">Puslapyje **Pasiūlymo duomenys** yra skyrius **Kandidato informacija** ir **Informacija apie darbą**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="1a40a-119">„Attract“ siūloma keletas parengtų naudoti pasiūlymo duomenų vietos rezervavimo ženklų.</span><span class="sxs-lookup"><span data-stu-id="1a40a-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    
    > <span data-ttu-id="1a40a-120">Puslapyje yra skyrių, skirtų grupuoti skirtingus pasiūlymų duomenų vietos rezervavimo ženklus į logines grupes.</span><span class="sxs-lookup"><span data-stu-id="1a40a-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="1a40a-121">Šie skyriai gali padėti tvarkyti pasiūlymo duomenis ir įvesti duomenis kuriant pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>

1.  <span data-ttu-id="1a40a-122">Norėdami sukurti naują pasiūlymo duomenų skyrių, spustelėkite **Įtraukti skyrių** ir įveskite unikalų skyriaus pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-122">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="1a40a-123">Norėdami pasiūlymo duomenų vietos rezervavimo ženklus įtraukti į bet kurį skyrių, spustelėkite **Įtraukti pasiūlymo duomenis** ir įveskite unikalų vietos rezervavimo ženklo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-123">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="1a40a-124">Norėdami redaguoti bet kurio skyriaus pavadinimą, laikykite žymiklį virš skyriaus pavadinimo ir atnaujinkite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-124">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="1a40a-125">Norėdami redaguoti bet kurio esamo pasiūlymo duomenų vietos rezervavimo ženklo pavadinimą, pirmiausia įsitikinkite, kad vietos rezervavimo ženklas nėra jokio šablono dalis.</span><span class="sxs-lookup"><span data-stu-id="1a40a-125">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="1a40a-126">Paskui, laikydami žymiklį virš pasiūlymo duomenų vietos rezervavimo ženklo pavadinimo, atnaujinkite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-126">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="1a40a-127">Norėdami panaikinti esamą pasiūlymo duomenų vietos rezervavimo ženklą, pirmiausia įsitikinkite, kad vietos rezervavimo ženklas nėra jokio kito šablono dalis.</span><span class="sxs-lookup"><span data-stu-id="1a40a-127">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="1a40a-128">Paskui laikykite žymiklį virš vietos rezervavimo ženklo ir, pasirodžius šiukšliadėžės piktogramai, spustelėkite ją ir panaikinkite pasiūlymo duomenų vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-128">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="1a40a-129">Šalia kiekvieno pasiūlymo duomenų esantis skaičius nurodo, keliems šablonams priskiriamas pasiūlymo duomenų vietos rezervavimo ženklas.</span><span class="sxs-lookup"><span data-stu-id="1a40a-129">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="1a40a-130">Norėdami panaikinti bet kurį skyrių, laikykite žymiklį virš pavadinimo.</span><span class="sxs-lookup"><span data-stu-id="1a40a-130">To delete any section, hover over the name.</span></span> <span data-ttu-id="1a40a-131">Jei nė vienas skyriaus pasiūlymo duomenų vietos rezervavimo ženklų nerodomas jokiame šablone, spustelėję šiukšliadėžės piktogramą galite jį panaikinti.</span><span class="sxs-lookup"><span data-stu-id="1a40a-131">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="1a40a-132">Panaikinus skyrių taip pat panaikinami visi to skyriaus pasiūlymo duomenų vietos rezervavimo ženklai.</span><span class="sxs-lookup"><span data-stu-id="1a40a-132">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="1a40a-133">Nustatę pasiūlymo duomenų vietos rezervavimo ženklus, galite juos naudoti bet kuriame dokumento šablone.</span><span class="sxs-lookup"><span data-stu-id="1a40a-133">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="1a40a-134">Pasiūlymo duomenų vietos rezervavimo ženklai gali būti naudojami ne tik konkrečiame šablone -- tą patį rinkinį galima naudoti visuose šablonuose.</span><span class="sxs-lookup"><span data-stu-id="1a40a-134">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="1a40a-135">Pasiūlymo duomenų taisyklės</span><span class="sxs-lookup"><span data-stu-id="1a40a-135">Offer data rules</span></span>

<span data-ttu-id="1a40a-136">Daugumoje organizacijų nustatytos pasiūlymų kūrimo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="1a40a-136">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="1a40a-137">Pavyzdžiui, organizacija gali reikalauti, kad maksimalaus metinio konkrečios vietos atlyginimo pasiūlymo ir paaukštinimo lygio derinys patektų į tam tikrą intervalą, arba kad samdant naują darbuotoją būtų galimos tik kelios konkrečios pasiūlymo lygio vertės.</span><span class="sxs-lookup"><span data-stu-id="1a40a-137">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="1a40a-138">„Attract“ šiuo metu palaiko visas tokias duomenų taisykles (naudojant CSV failą).</span><span class="sxs-lookup"><span data-stu-id="1a40a-138">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="1a40a-139">Norėdami parengti duomenų taisyklių CSV failą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1a40a-139">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="1a40a-140">Nustatykite taisyklių rinkinio pasiūlymo duomenų vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-140">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="1a40a-141">Pavyzdžiui, **Metinis atlyginimas**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-141">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="1a40a-142">Nurodykite priklausomąsias pasiūlymo duomenų vietos rezervavimo ženklo vertes.</span><span class="sxs-lookup"><span data-stu-id="1a40a-142">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="1a40a-143">Pavyzdžiui, **Darbo vieta** ir **Lygis**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-143">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="1a40a-144">1 ir 2 stulpelyje nurodykite **Darbo vieta** ir **Lygis**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-144">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="1a40a-145">Norint įkelti intervalo vertę, 3 ir 4 stulpeliai turi būti **Metinis atlyginimas**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-145">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="1a40a-146">Norint įkelti konkrečią reikšmę, o ne intervalą, 3 stulpelis turi būti **Metinis atlyginimas**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-146">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="1a40a-147">Automatiškai užpildykite „Microsoft Excel“ failą pagal reikiamus vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="1a40a-147">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="1a40a-148">Patikrinkite, ar kiekvienoje eilutėje pateikiama unikali visų susumuotų verčių kombinacija.</span><span class="sxs-lookup"><span data-stu-id="1a40a-148">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="1a40a-149">Failą išsaugokite CSV formatu.</span><span class="sxs-lookup"><span data-stu-id="1a40a-149">Save the file as a CSV format.</span></span>

<span data-ttu-id="1a40a-150">Norėdami įkelti pasiūlymo duomenų taisyklių failą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1a40a-150">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="1a40a-151">Eikite į **Pasiūlymo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-151">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="1a40a-152">Išplėskite kairiosios naršymo srities skyrių **Biblioteka**, paskui eikite į **Pasiūlymo duomenų taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-152">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="1a40a-153">Spustelėjus **Naujas duomenų rinkinys** rodomas dialogo langas **Įkelti**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-153">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="1a40a-154">Nurodykite unikalų taisyklių rinkinio pavadinimą, paskui įkelkite išsaugotą CSV failą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-154">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="1a40a-155">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-155">Click **Add**.</span></span>
    <span data-ttu-id="1a40a-156">Taisyklių rinkinys bus vykdomas fone ir jums bus pranešta (programoje ir elektroniniu paštu), kai veiksmas bus baigtas.</span><span class="sxs-lookup"><span data-stu-id="1a40a-156">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="1a40a-157">Jums bus pranešta, jei vykdant įkėlimą kiltų klaidų.</span><span class="sxs-lookup"><span data-stu-id="1a40a-157">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="1a40a-158">Tada galite atsisiųsti klaidų žurnalą, pataisyti failą ir įkelti jį dar kartą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-158">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="1a40a-159">Norėdami atsisiųsti taisyklių rinkinį ir atnaujinti reikšmių rinkinį (**…**), naudokitės elipsės mygtuko parinktimi.</span><span class="sxs-lookup"><span data-stu-id="1a40a-159">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="1a40a-160">Atlikę atnaujinimą failą galite įkelti dar kartą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-160">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="1a40a-161">Galite panaikinti esamą taisyklių rinkinio įkėlimą (jei apibrėžiamas vietos rezervavimo ženklas nenaudojamas kitame dokumento šablone).</span><span class="sxs-lookup"><span data-stu-id="1a40a-161">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="1a40a-162">Kiekvienas vietos rezervavimo ženklas gali turėti tik vieną unikalų stulpelių rinkinį, nuo kurio jis priklauso.</span><span class="sxs-lookup"><span data-stu-id="1a40a-162">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="1a40a-163">Pavyzdžiui, jei **Metinis atlyginimas** priklauso nuo verčių **Darbo vieta** ir **Lygis**, negalite įkelti kito taisyklių rinkinio, kuriame **Metinis atlyginimas** priklauso nuo kito stulpelių rinkinio.</span><span class="sxs-lookup"><span data-stu-id="1a40a-163">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="1a40a-164">Pasiūlymo duomenų taisyklių rinkinių pavyzdžius galite atsisiųsti iš puslapio **Pasiūlymo duomenų taisyklės** skirtuko **Pavyzdžiai**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-164">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="1a40a-165">Kai pasiūlymo kūrėjas perrašo pasiūlymo duomenų taisyklėse rekomenduojamas vertes, pasiūlymas pažymimas kaip nestandartinis, o pasiūlymo patvortinimo darbo eiga privaloma.</span><span class="sxs-lookup"><span data-stu-id="1a40a-165">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="1a40a-166">Dokumento šablonai</span><span class="sxs-lookup"><span data-stu-id="1a40a-166">Document templates</span></span>

<span data-ttu-id="1a40a-167">Pasiūlymo dokumento šablonas gali būti pagalba administratoriams kuriant pasiūlymo laiškus.</span><span class="sxs-lookup"><span data-stu-id="1a40a-167">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="1a40a-168">Pasiūlymo dokumento šablonas yra į pasiūlymą ketinamas įtraukti tekstas, taip pat nurodyti pasiūlymo duomenų vietos rezervavimo ženklai.</span><span class="sxs-lookup"><span data-stu-id="1a40a-168">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="1a40a-169">Norėdami sukurti pasiūlymo dokumento šabloną, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1a40a-169">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="1a40a-170">Eikite į **Pasiūlymo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-170">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="1a40a-171">Išplėskite kairiosios naršymo srities skyrių **Biblioteka** ir eikite į **Šablonai**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-171">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="1a40a-172">Puslapyje **Šablonai** rodomas jau apibrėžtų dokumentų šablonų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="1a40a-172">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="1a40a-173">Norėdami sukurti naują dokumento šabloną, spustelėkite **Naujas šablonas**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-173">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="1a40a-174">Įveskite unikalų šablono pavadinimą ir spustelėkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-174">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="1a40a-175">Naudodamiesi raiškiojo teksto rengykle galite įterpti arba redaguoti pasiūlymo dokumento turinį.</span><span class="sxs-lookup"><span data-stu-id="1a40a-175">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="1a40a-176">Naudodamiesi tekstų rengyklės viršuje pateikiamomis parinktimis, galite įterpti lentelių, vaizdų ir hipersaitų.</span><span class="sxs-lookup"><span data-stu-id="1a40a-176">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="1a40a-177">Norėdami į pasiūlymo šablono dokumentą įtraukti pasiūlymo duomenų vietos rezervavimo ženklų, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1a40a-177">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="1a40a-178">Nuvilkite nuo dešiniosios srities.</span><span class="sxs-lookup"><span data-stu-id="1a40a-178">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="1a40a-179">Saitažodžiu susiekite pasiūlymo duomenų vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-179">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="1a40a-180">Įveskite **\#**, o paskui pradėkite rašyti pasiūlymo duomenų vietos rezervavimo ženklo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-180">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="1a40a-181">Išplečiamajame sąraše bus rodomos parinktys.</span><span class="sxs-lookup"><span data-stu-id="1a40a-181">Options will appear in the drop-down list.</span></span> <span data-ttu-id="1a40a-182">Spustelėję arba paspaudę **Enter** įveskite pasiūlymo duomenų vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-182">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="1a40a-183">Norėdami susieti vietos rezervavimo ženklą su pasiūlymo dokumento šablonu, nenurodant jo vertės kandidatui, laikykite žymiklį virš pasiūlymo duomenų vietos rezervavimo ženklo ir spustelėkite piktogramą **Prisegti**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-183">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="1a40a-184">Tokiu būdu vietos rezervavimo ženklas bus pastumtas į pasiūlymo dokumento šablono skyrių **Prisegti pasiūlymo duomenys**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-184">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="1a40a-185">Norėdami atsegti, atlikite tuos pačius veiksmus, bet pasiūlymo duomenų vietos rezervavimo ženklų sąraše spustelėkite **Atsegti**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-185">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="1a40a-186">Norėdami peržiūrėti aktyvių pasiūlymo duomenų vietos rezervavimo ženklų sąrašą, įjunkite dešiniosios srities skirtuką **Aktyvūs**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-186">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="1a40a-187">Įterpę vietos rezervavimo ženklą, kuriam taikomas pasiūlymo duomenų taisyklių rinkinys, galite matyti to pasiūlymo vietos rezervavimo ženklo priklausomybę nuo kitų verčių.</span><span class="sxs-lookup"><span data-stu-id="1a40a-187">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="1a40a-188">Arba galite **Importuoti** turinį iš jūsų vietinio įrenginio .docx failo ir atlikti reikiamus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="1a40a-188">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="1a40a-189">Tokiu būdu jums nereikės įvesti viso turinio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="1a40a-189">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="1a40a-190">Norėdami peržiūrėti pasiūlymo dokumentą, naudokitės puslapio viršuje esančia parinktimi **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-190">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="1a40a-191">Norėdami kontroliuoti, ar pasiūlymo kūrėjas gali redaguoti pasiūlymo dokumento turinį, naudokitės puslapio viršuje esančia parinktimi **Valdyti teisę**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-191">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="1a40a-192">Jei norite, kad pasiūlymo kūrėjas galėtų tik įterpti vietos rezervavimo ženklo vertes, bet negalėtų redaguoti teksto, nustatykite teisės vertę **Ne**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-192">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="1a40a-193">Spustelėkite **Įrašyti** ir išsaugokite savo eigą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-193">Click **Save** to save your progress.</span></span> <span data-ttu-id="1a40a-194">Šablonas bus išsaugotas juodraščio būsenos.</span><span class="sxs-lookup"><span data-stu-id="1a40a-194">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="1a40a-195">Norėdami baigti ir pažymėti dokumentą pagal tai, koks jis buvo paskelbtas, spustelėkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-195">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="1a40a-196">Galite matyti, kurie dokumento šablonai šiuo metu aktyvūs (juodraščio režimu), taip pat yra archyvuojami ir nebus naudojami naudojantis dokumentų šablonų bibliotekos nukreipimo patirtimi.</span><span class="sxs-lookup"><span data-stu-id="1a40a-196">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="1a40a-197">Galite panaikinti bet kurį pasiūlymo dokumento šabloną, kuris nėra esamo pasiūlymo paketo šablono dalis.</span><span class="sxs-lookup"><span data-stu-id="1a40a-197">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="1a40a-198">Pasiūlymo paketo šablonai</span><span class="sxs-lookup"><span data-stu-id="1a40a-198">Offer package templates</span></span>

<span data-ttu-id="1a40a-199">Pasiūlymų paketai yra pasiūlymo artefaktai, kurie bendrinami su kandidatu ir yra sudaryti iš vieno ar kelių pasiūlymo dokumento šablonų.</span><span class="sxs-lookup"><span data-stu-id="1a40a-199">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="1a40a-200">Norėdami sukurti pasiūlymo paketą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1a40a-200">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="1a40a-201">Eikite į **Pasiūlymo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-201">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="1a40a-202">Kairiojoje naršymo srityje eikite į **Pakuotės**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-202">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="1a40a-203">Rodomas aktyvių paketo šablonų, kuriais gali naudotis pasiūlymo kūrėjai, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="1a40a-203">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="1a40a-204">Norėdami sukurti naują pasiūlymo paketą, spustelėkite **Naujas paketas**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-204">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="1a40a-205">Įveskite unikalų pavadinimą ir spustelėkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-205">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="1a40a-206">Spustelėkite **Įtraukti šabloną**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-206">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="1a40a-207">Galite pasirinkti sukurti naują šabloną arba pasirinkti iš esamų.</span><span class="sxs-lookup"><span data-stu-id="1a40a-207">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="1a40a-208">Pasirinkę įtraukti esamą šabloną turite įsitikinti, kad pasiūlymo dokumento šablonas įrašytas, baigtas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="1a40a-208">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="1a40a-209">Galite pasirinkti tiek dokumentų šablonųų, kiek norite.</span><span class="sxs-lookup"><span data-stu-id="1a40a-209">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="1a40a-210">Spustelėkite **Atlikta** ir grįžkite į **Paketų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-210">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="1a40a-211">Galite sukonfigūruoti dokumentų seką, taip pat pažymėti, ar kuriant pasiūlymą reikalingas konkretaus pasiūlymo dokumentas.</span><span class="sxs-lookup"><span data-stu-id="1a40a-211">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="1a40a-212">Pasiūlymo kūrėjas turi galimybę panaikinti dokumentus, pažymėtus **Nebūtina**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-212">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="1a40a-213">Norėdami įrašyti pasiūlymo paketo šabloną, kad juo galėtų naudotis visi pasiūlymo kūrėjai, spustelėkite **Įrašyti ir paskelbti**.</span><span class="sxs-lookup"><span data-stu-id="1a40a-213">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="1a40a-214">Norėdami peržiūrėti pasiūlymo paketo šablonų juodraščius, eikite į skirtuką **Juodraščiai**. Atlikus pasiūlymo paketo šablono pakeitimą, būtina jį įrašyti ir paskelbti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="1a40a-214">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="1a40a-215">Pasiūlymo proceso konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1a40a-215">Configure an offer process</span></span>

<span data-ttu-id="1a40a-216">Yra keletas pasiūlymo kūrimo proceso dalių, kurias gali konfigūruoti „Attract“ administratorius.</span><span class="sxs-lookup"><span data-stu-id="1a40a-216">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="1a40a-217">**Pasiūlymų patvirtinimai** – pasirinkite, ar, prieš siunčiant pasiūlymą kandidatui, būtina jį patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="1a40a-217">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="1a40a-218">Jei esate administratorius, taip pat galite nuspręsti, ar visi pasiūlymų patvirtinimai vyks eilės tvarka, ar lygiagrečia patvirtinimo darbo eiga.</span><span class="sxs-lookup"><span data-stu-id="1a40a-218">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="1a40a-219">Taip pat gali nurodyti, ar pasiūlymų tvirtintojams būtina tvirtinant pasiūlymą pateikti ir komentarą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-219">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="1a40a-220">Visų nestandartinių pasiūlymų atveju patvirtinimai būtini.</span><span class="sxs-lookup"><span data-stu-id="1a40a-220">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="1a40a-221">**Kandidato pasiūlymo patirtis** – jei esate administratorius, galite pasirinkti nustatyti, ar visi pasiūlymai turės galiojimo datą, ir, jei taip, koks bus numatytasis galiojimo datos poslinkis.</span><span class="sxs-lookup"><span data-stu-id="1a40a-221">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="1a40a-222">Taip pat galite sukonfigūruoti ar kandidatai gali atmesti pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="1a40a-222">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="1a40a-223">**Elektroniniai parašai** – jūs, administratorius, taip pat galite pasirinkti metodą, kurį kandidatai gali naudoti pasirašydami pasiūlymus.</span><span class="sxs-lookup"><span data-stu-id="1a40a-223">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="1a40a-224">„Adobe Sign“ – visi pasiūlymų paketai bus siunčiami ir pasirašomi naudojant „Adobe Sign“.</span><span class="sxs-lookup"><span data-stu-id="1a40a-224">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="1a40a-225">Kiekvienas pasiūlymo kūrėjas, publikuojantis pasiūlymą, turi būti prijungęs savo „Adobe Sign“ paskyrą prie „Attract“.</span><span class="sxs-lookup"><span data-stu-id="1a40a-225">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="1a40a-226">Norėdami informacijos apie „Adobe Sign“ licencijas ir nemokamą bandomąją versiją, naudokite šį [saitą](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span><span class="sxs-lookup"><span data-stu-id="1a40a-226">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="1a40a-227">„DocuSign“ – visi pasiūlymų paketai bus siunčiami ir pasirašomi naudojant „DocuSign“.</span><span class="sxs-lookup"><span data-stu-id="1a40a-227">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="1a40a-228">Kiekvienas pasiūlymo kūrėjas, publikuojantis pasiūlymą, turi būti prijungęs savo „DocuSign“ paskyrą prie „Attract“.</span><span class="sxs-lookup"><span data-stu-id="1a40a-228">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="1a40a-229">„ESign“ – tai numatytoji parengta naudoti parinktis, kai vartotojas gali pasirašyti pasiūlymą įvesdamas savo vardą ir inicialus.</span><span class="sxs-lookup"><span data-stu-id="1a40a-229">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="1a40a-230">Norėdami daugiau sužinoti apie pasiūlymo kūrimo procesą, žr. [Pasiūlymų kūrimas, tvirtinimas ir pasirašymas](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="1a40a-230">To learn more about the offer creation process, see [Creating, approving, and signing offers](./creating-offers.md).</span></span>
