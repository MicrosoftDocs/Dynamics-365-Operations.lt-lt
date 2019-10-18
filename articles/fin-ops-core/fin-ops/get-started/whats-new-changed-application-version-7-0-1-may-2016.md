---
title: Kas nauja ar pasikeitė „Dynamics AX“ 7.0.1 versijoje (2016 m. gegužės mėn.)
description: Šiame straipsnyje aprašomos naujos ir pakeistos 7.0.1 programos „Microsoft Dynamics AX“ versijoje veikiančios funkcijos. Ši versija buvo išleista 2016 m. gegužės mėn. ir jos versijos numeris yra 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 6bd40873d6890bc837188cba1aa1125d874f6bda
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179151"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="3ae83-104">Kas nauja ar pasikeitė „Dynamics AX“ 7.0.1 versijoje (2016 m. gegužės mėn.)</span><span class="sxs-lookup"><span data-stu-id="3ae83-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ae83-105">Šiame straipsnyje aprašomos naujos ir pakeistos 7.0.1 programos „Microsoft Dynamics AX“ versijoje veikiančios funkcijos.</span><span class="sxs-lookup"><span data-stu-id="3ae83-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="3ae83-106">Ši versija buvo išleista 2016 m. gegužės mėn. ir jos versijos numeris yra 7.0.1265.23014.</span><span class="sxs-lookup"><span data-stu-id="3ae83-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="3ae83-107">Elektroninė ataskaita (ER)</span><span class="sxs-lookup"><span data-stu-id="3ae83-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="3ae83-108">Ką galite daryti?</span><span class="sxs-lookup"><span data-stu-id="3ae83-108">What can you do?</span></span> | <span data-ttu-id="3ae83-109">Kodėl tai svarbu?</span><span class="sxs-lookup"><span data-stu-id="3ae83-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="3ae83-110">Sukonfigūruokite elektroninė perdavimo ataskaitų (ER) kūrimo apdorojimo laiko dialogo langą, kad vartotojai galėtų pasirinkti norimas finansines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="3ae83-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="3ae83-111">Apdorojimo metu ER ataskaitos apdorojimo dialogo lange vartotojai gali pasirinkti kelias finansines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="3ae83-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="3ae83-112">Pasirinktų finansinių dimensijų išsami informacija bus rodoma sugeneruotame elektroniniame dokumente.</span><span class="sxs-lookup"><span data-stu-id="3ae83-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="3ae83-113">Kai kuriate ER ataskaitą, sukonfigūruokite prieigą prie kelių finansinių dimensijų, nustatydami vieną susiejimą su norimo duomenų šaltiniu.</span><span class="sxs-lookup"><span data-stu-id="3ae83-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="3ae83-114">Tą pačią ER ataskaitos konfigūraciją galima naudoti generuojant elektroninius dokumentus, kuriuose pateikiami operaciniai duomenys ir išsami informacija apie finansines dimensijas, nepriklausomai nuo vartotojo pasirinktų arba dabartiniam juridiniam subjektui ar egzemplioriui sukonfigūruotų finansinių dimensijų skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="3ae83-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="3ae83-115">Konfigūruokite ER ataskaitą, kad jį duomenis įvestų į OPENXML darbalapio formatu sukurto elektroninio dokumento dinamiškai sugeneruotus stulpelius.</span><span class="sxs-lookup"><span data-stu-id="3ae83-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="3ae83-116">ER ataskaita gali įvesti duomenis į sugeneruotą OPENXML darbalapį horizontaliai pakeisdama stulpelius.</span><span class="sxs-lookup"><span data-stu-id="3ae83-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="3ae83-117">Todėl pakartotinai naudojant tą pačią ER ataskaitos konfigūraciją galima generuoti elektroninius dokumentus, kurie turi skirtingą dinamiškai sugeneruotų stulpelių skaičių.</span><span class="sxs-lookup"><span data-stu-id="3ae83-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="3ae83-118">Konfigūruokite ER paskirties vietas, kad formato išeigos rezultatas būtų nukreiptas į konkrečią paskirties vietą: failą, el. pašto adresą arba archyvą („Microsoft SharePoint“ aplanką arba „Microsoft Azure“ saugyklą).</span><span class="sxs-lookup"><span data-stu-id="3ae83-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="3ae83-119">Anksčiau paleidžiant ER konfigūraciją pasirodydavo pranešimo langas, nurodantis vartotojui failą įrašyti arba atidaryti.</span><span class="sxs-lookup"><span data-stu-id="3ae83-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="3ae83-120">Dabar kiekvienos formato konfigūracijos ir kiekvienos komponento paskirties vietą (aplanką arba failą) galite iš anksto sukonfigūruoti atskirai.</span><span class="sxs-lookup"><span data-stu-id="3ae83-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="3ae83-121">Vartotojai, turintys reikiamas teises, paskirties vietos parametrus gali taip pat keisti apdorojimo metu.</span><span class="sxs-lookup"><span data-stu-id="3ae83-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="3ae83-122">EKA – „Microsoft Dynamics AX Retail“</span><span class="sxs-lookup"><span data-stu-id="3ae83-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="3ae83-123">Ką galite daryti?</span><span class="sxs-lookup"><span data-stu-id="3ae83-123">What can you do?</span></span> | <span data-ttu-id="3ae83-124">Kodėl tai svarbu?</span><span class="sxs-lookup"><span data-stu-id="3ae83-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="3ae83-125">Naudokite naršyklę „Google Chrome“.</span><span class="sxs-lookup"><span data-stu-id="3ae83-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="3ae83-126">Dabar mažmenininkai debesies EKA gali paleisti naršyklėje „Chrome“ ir naudoti visas funkcijas, kurios yra debesies EKA „Microsoft Edge“ ir „Internet Explorer“ versijose.</span><span class="sxs-lookup"><span data-stu-id="3ae83-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="3ae83-127">Finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="3ae83-127">Financial reporting</span></span>

| <span data-ttu-id="3ae83-128">Ką galite daryti?</span><span class="sxs-lookup"><span data-stu-id="3ae83-128">What can you do?</span></span> | <span data-ttu-id="3ae83-129">Kodėl tai svarbu?</span><span class="sxs-lookup"><span data-stu-id="3ae83-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="3ae83-130">Atstatykite finansinių ataskaitų duomenų sritį.</span><span class="sxs-lookup"><span data-stu-id="3ae83-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="3ae83-131">Kai „Dynamics AX“ duomenų bazes perkeliate iš vienos aplinkos į kitą arba atliekate kitus esminius aplinkos pakeitimus, finansinių ataskaitų duomenų bazę gali tekti kurti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="3ae83-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="3ae83-132">Nuo šiol „Windows PowerShell“ scenarijus teikiamas duomenų bazei kurti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="3ae83-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="3ae83-133">Daugiau nebegalite pasirinkti ataskaitų dizaino įrankio parinkčių, kurios negalioja.</span><span class="sxs-lookup"><span data-stu-id="3ae83-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="3ae83-134">Kelios ataskaitų kūrimo parinktys, kurios buvo naudojamos rinkoje esančiose „Management reporter“ versijose, šioje „Dynamics AX“ versijoje netaikomos.</span><span class="sxs-lookup"><span data-stu-id="3ae83-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="3ae83-135">Šios parinktys buvo susijusios su finansinių ataskaitų kūrimu, išvedamais duomenimis ir susiejimu.</span><span class="sxs-lookup"><span data-stu-id="3ae83-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="3ae83-136">Šios parinktys buvo pašalintos iš finansinių ataskaitų dizaino įrankio, kad vartotojai nedarytų klaidų.</span><span class="sxs-lookup"><span data-stu-id="3ae83-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="3ae83-137">Finansų valdymas</span><span class="sxs-lookup"><span data-stu-id="3ae83-137">Financial management</span></span>

| <span data-ttu-id="3ae83-138">Ką galite daryti?</span><span class="sxs-lookup"><span data-stu-id="3ae83-138">What can you do?</span></span> | <span data-ttu-id="3ae83-139">Kodėl tai svarbu?</span><span class="sxs-lookup"><span data-stu-id="3ae83-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="3ae83-140">Generuokite mokėtinų sumų mokėjimų teigiamo mokėjimo failus.</span><span class="sxs-lookup"><span data-stu-id="3ae83-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="3ae83-141">Galima generuoti teigiamo mokėjimo failus, kad bankai galėtų lengviau išvengti su čekiais susijusio sukčiavimo.</span><span class="sxs-lookup"><span data-stu-id="3ae83-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="3ae83-142">Sandėlis ir gamyba</span><span class="sxs-lookup"><span data-stu-id="3ae83-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3ae83-143">Ką galite daryti?</span><span class="sxs-lookup"><span data-stu-id="3ae83-143">What can you do?</span></span></th>
<th><span data-ttu-id="3ae83-144">Kodėl tai svarbu?</span><span class="sxs-lookup"><span data-stu-id="3ae83-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3ae83-145">Nustatykite sandėlio darbo strategiją, kuri kontroliuoja produktų rinkinio darbo kūrimą konkrečiose vietose.</span><span class="sxs-lookup"><span data-stu-id="3ae83-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="3ae83-146">Sandėlio procesai ne visada apima darbą.</span><span class="sxs-lookup"><span data-stu-id="3ae83-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="3ae83-147">Naudodami naująją sandėlio darbo strategiją, galite neleisti konkrečiose vietose kurti tam tikro produktų rinkinio žaliavų paėmimo ir pagamintų prekių padėjimo darbo.</span><span class="sxs-lookup"><span data-stu-id="3ae83-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ae83-148">Nurodykite, kad gamybos išeigos vieta nėra kontroliuojama pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="3ae83-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="3ae83-149">Dabar galite nurodyti, kad produktų išeigos vieta nėra kontroliuojama pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="3ae83-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="3ae83-150">Pavyzdžiui, ši funkcija yra naudinga, kai pirminės gamybos užsakymas ataskaitą apie baigtas prekes pateikia tiesiai toje vietoje, kuri naudojama kaip tolesnio gamybos užsakymo gamybos išeigos vieta.</span><span class="sxs-lookup"><span data-stu-id="3ae83-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ae83-151">Teikite pagalbą KS, kuriose yra prekių, turinčių skirtingas tos pačios prekės produktų dimensijas.</span><span class="sxs-lookup"><span data-stu-id="3ae83-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="3ae83-152">Gamyboje naudodami vieną ar kelias produkto dimensijas, gali būti atvejų, kai jūs norėsite prekę gaminti pagal kitą tos pačios prekės variantą.</span><span class="sxs-lookup"><span data-stu-id="3ae83-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="3ae83-153">Daugiau informacijos žr. <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">šiame tinklaraštyje</a>.</span><span class="sxs-lookup"><span data-stu-id="3ae83-153">For more information, see <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ae83-154">Gamybos užsakymai, kurių cikliškumo struktūros yra pirmame KS lygyje, nėra įtraukiamos į materialiųjų išteklių planavimo KS lygio skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="3ae83-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="3ae83-155">Produkto variantams priskirti teisingų KS lygių neįmanoma, jei pasirinkti gamybos užsakymai yra KS hierarchijos cikliškumo priežastis.</span><span class="sxs-lookup"><span data-stu-id="3ae83-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ae83-156">Apskaičiuokite atskirus materialiųjų išteklių planavimo ir išlaidų apskaičiavimo KS lygius.</span><span class="sxs-lookup"><span data-stu-id="3ae83-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="3ae83-157">Materialinių išteklių planavimo KS lygiai yra apskaičiuojami naujoje lentelėje <strong>ReqItemLevel</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ae83-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="3ae83-158">Baigti gamybos užsakymai į skaičiavimą neįtraukiami.</span><span class="sxs-lookup"><span data-stu-id="3ae83-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="3ae83-159">Gamybos išlaidų skaičiavimo KS lygiai yra apskaičiuojami lentelėje <strong>InventTable</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ae83-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="3ae83-160">Baigti gamybos užsakymai įtraukiami į skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="3ae83-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="3ae83-161">Vykdant materialiųjų išteklių planavimą, pvz., bendrojo planavimo plano planavimą ir išskleidimą, reikia perskaičiuoti tik materialiųjų išteklių planavime naudojamus KS lygius.</span><span class="sxs-lookup"><span data-stu-id="3ae83-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="3ae83-162">Kitaip tariant, gamybos išlaidų skaičiavime naudojamų KS lygių skaičiuoti nereikia.</span><span class="sxs-lookup"><span data-stu-id="3ae83-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="3ae83-163">Vykdant išlaidų operacijas, pvz., atsargų uždarymą, reikia perskaičiuoti tik gamybos išlaidų skaičiavime naudojamus KS lygius.</span><span class="sxs-lookup"><span data-stu-id="3ae83-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="3ae83-164">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3ae83-164">Additional resources</span></span>

[<span data-ttu-id="3ae83-165">Kas nauja ar pasikeitė</span><span class="sxs-lookup"><span data-stu-id="3ae83-165">What's new or changed</span></span>](whats-new-changed.md)

[<span data-ttu-id="3ae83-166">Nauji ar atnaujinti užduočių vedliai (2016 m. gegužės mėn.)</span><span class="sxs-lookup"><span data-stu-id="3ae83-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)
