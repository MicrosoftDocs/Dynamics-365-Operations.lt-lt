---
title: "Kas nauja ar pasikeitė 7.0.1 programos „Dynamics AX“ versijoje (2016 m. gegužės mėn.)"
description: "Šiame straipsnyje aprašomos naujos ir pakeistos 7.0.1 programos „Microsoft Dynamics AX“ versijoje veikiančios funkcijos. Ši versija buvo išleista 2016 m. gegužės mėn. ir jos versijos numeris yra 7.0.1265.23014."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: f3853169b7452e307a36579facea0cf0ab83ca47
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="7eabd-104">Kas nauja ar pasikeitė 7.0.1 programos „Dynamics AX“ versijoje (2016 m. gegužės mėn.)</span><span class="sxs-lookup"><span data-stu-id="7eabd-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7eabd-105">Šiame straipsnyje aprašomos naujos ir pakeistos 7.0.1 programos „Microsoft Dynamics AX“ versijoje veikiančios funkcijos.</span><span class="sxs-lookup"><span data-stu-id="7eabd-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="7eabd-106">Ši versija buvo išleista 2016 m. gegužės mėn. ir jos versijos numeris yra 7.0.1265.23014.</span><span class="sxs-lookup"><span data-stu-id="7eabd-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

<a name="electronic-reporting-er"></a><span data-ttu-id="7eabd-107">Elektroninė ataskaita (ER)</span><span class="sxs-lookup"><span data-stu-id="7eabd-107">Electronic reporting (ER)</span></span>
-------------------------

|                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eabd-108">**Ką galite daryti?**</span><span class="sxs-lookup"><span data-stu-id="7eabd-108">**What can you do?**</span></span>                                                                                                                                                                   | <span data-ttu-id="7eabd-109">**Kodėl tai svarbu?**</span><span class="sxs-lookup"><span data-stu-id="7eabd-109">**Why is this important?**</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="7eabd-110">Sukonfigūruokite elektroninė perdavimo ataskaitų (ER) kūrimo apdorojimo laiko dialogo langą, kad vartotojai galėtų pasirinkti norimas finansines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="7eabd-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span>                                     | <span data-ttu-id="7eabd-111">Apdorojimo metu ER ataskaitos apdorojimo dialogo lange vartotojai gali pasirinkti kelias finansines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="7eabd-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="7eabd-112">Pasirinktų finansinių dimensijų išsami informacija bus rodoma sugeneruotame elektroniniame dokumente.</span><span class="sxs-lookup"><span data-stu-id="7eabd-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span>                                                                                                                              |
| <span data-ttu-id="7eabd-113">Kai kuriate ER ataskaitą, sukonfigūruokite prieigą prie kelių finansinių dimensijų, nustatydami vieną susiejimą su norimo duomenų šaltiniu.</span><span class="sxs-lookup"><span data-stu-id="7eabd-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span>                                                  | <span data-ttu-id="7eabd-114">Tą pačią ER ataskaitos konfigūraciją galima naudoti generuojant elektroninius dokumentus, kuriuose pateikiami operaciniai duomenys ir išsami informacija apie finansines dimensijas, nepriklausomai nuo vartotojo pasirinktų arba dabartiniam juridiniam subjektui ar egzemplioriui sukonfigūruotų finansinių dimensijų skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="7eabd-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span>                                             |
| <span data-ttu-id="7eabd-115">Konfigūruokite ER ataskaitą, kad jį duomenis įvestų į OPENXML darbalapio formatu sukurto elektroninio dokumento dinamiškai sugeneruotus stulpelius.</span><span class="sxs-lookup"><span data-stu-id="7eabd-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span>                                           | <span data-ttu-id="7eabd-116">ER ataskaita gali įvesti duomenis į sugeneruotą OPENXML darbalapį horizontaliai pakeisdama stulpelius.</span><span class="sxs-lookup"><span data-stu-id="7eabd-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="7eabd-117">Todėl pakartotinai naudojant tą pačią ER ataskaitos konfigūraciją galima generuoti elektroninius dokumentus, kurie turi skirtingą dinamiškai sugeneruotų stulpelių skaičių.</span><span class="sxs-lookup"><span data-stu-id="7eabd-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span>                                                                                 |
| <span data-ttu-id="7eabd-118">Konfigūruokite ER paskirties vietas, kad formato išeigos rezultatas būtų nukreiptas į konkrečią paskirties vietą: failą, el. pašto adresą arba archyvą („Microsoft SharePoint“ aplanką arba „Microsoft Azure“ saugyklą).</span><span class="sxs-lookup"><span data-stu-id="7eabd-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="7eabd-119">Anksčiau paleidžiant ER konfigūraciją pasirodydavo pranešimo langas, nurodantis vartotojui failą įrašyti arba atidaryti.</span><span class="sxs-lookup"><span data-stu-id="7eabd-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="7eabd-120">Dabar kiekvienos formato konfigūracijos ir kiekvienos komponento paskirties vietą (aplanką arba failą) galite iš anksto sukonfigūruoti atskirai.</span><span class="sxs-lookup"><span data-stu-id="7eabd-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="7eabd-121">Vartotojai, turintys reikiamas teises, paskirties vietos parametrus gali taip pat keisti apdorojimo metu.</span><span class="sxs-lookup"><span data-stu-id="7eabd-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="7eabd-122">EKA – „Microsoft Dynamics AX Retail“</span><span class="sxs-lookup"><span data-stu-id="7eabd-122">POS – Microsoft Dynamics AX Retail</span></span>
|                                |                                                                                                                                                                                         |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eabd-123">**Ką galite daryti?**</span><span class="sxs-lookup"><span data-stu-id="7eabd-123">**What can you do?**</span></span>           | <span data-ttu-id="7eabd-124">**Kodėl tai svarbu?**</span><span class="sxs-lookup"><span data-stu-id="7eabd-124">**Why is this important?**</span></span>                                                                                                                                                              |
| <span data-ttu-id="7eabd-125">Naudokite naršyklę „Google Chrome“.</span><span class="sxs-lookup"><span data-stu-id="7eabd-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="7eabd-126">Dabar mažmenininkai debesies EKA gali paleisti naršyklėje „Chrome“ ir naudoti visas funkcijas, kurios yra debesies EKA „Microsoft Edge“ ir „Internet Explorer“ versijose.</span><span class="sxs-lookup"><span data-stu-id="7eabd-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="7eabd-127">Finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="7eabd-127">Financial reporting</span></span>
|                                                                     |                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eabd-128">**Ką galite daryti?**</span><span class="sxs-lookup"><span data-stu-id="7eabd-128">**What can you do?**</span></span>                                                | <span data-ttu-id="7eabd-129">**Kodėl tai svarbu?**</span><span class="sxs-lookup"><span data-stu-id="7eabd-129">**Why is this important?**</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="7eabd-130">Atstatykite finansinių ataskaitų duomenų sritį.</span><span class="sxs-lookup"><span data-stu-id="7eabd-130">Rebuild the Financial reporting data mart.</span></span>                          | <span data-ttu-id="7eabd-131">Kai „Dynamics AX“ duomenų bazes perkeliate iš vienos aplinkos į kitą arba atliekate kitus esminius aplinkos pakeitimus, finansinių ataskaitų duomenų bazę gali tekti kurti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="7eabd-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="7eabd-132">Nuo šiol „Windows PowerShell“ scenarijus teikiamas duomenų bazei kurti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="7eabd-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span>                                                                |
| <span data-ttu-id="7eabd-133">Daugiau nebegalite pasirinkti ataskaitų dizaino įrankio parinkčių, kurios negalioja.</span><span class="sxs-lookup"><span data-stu-id="7eabd-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="7eabd-134">Kelios ataskaitų kūrimo parinktys, kurios buvo naudojamos rinkoje esančiose „Management reporter“ versijose, šioje „Dynamics AX“ versijoje netaikomos.</span><span class="sxs-lookup"><span data-stu-id="7eabd-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="7eabd-135">Šios parinktys buvo susijusios su finansinių ataskaitų kūrimu, išvedamais duomenimis ir susiejimu.</span><span class="sxs-lookup"><span data-stu-id="7eabd-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="7eabd-136">Šios parinktys buvo pašalintos iš finansinių ataskaitų dizaino įrankio, kad vartotojai nedarytų klaidų.</span><span class="sxs-lookup"><span data-stu-id="7eabd-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="7eabd-137">Finansų valdymas</span><span class="sxs-lookup"><span data-stu-id="7eabd-137">Financial management</span></span>
|                                                            |                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="7eabd-138">**Ką galite daryti?**</span><span class="sxs-lookup"><span data-stu-id="7eabd-138">**What can you do?**</span></span>                                       | <span data-ttu-id="7eabd-139">**Kodėl tai svarbu?**</span><span class="sxs-lookup"><span data-stu-id="7eabd-139">**Why is this important?**</span></span>                                       |
| <span data-ttu-id="7eabd-140">Generuokite mokėtinų sumų mokėjimų teigiamo mokėjimo failus.</span><span class="sxs-lookup"><span data-stu-id="7eabd-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="7eabd-141">Galima generuoti teigiamo mokėjimo failus, kad bankai galėtų lengviau išvengti su čekiais susijusio sukčiavimo.</span><span class="sxs-lookup"><span data-stu-id="7eabd-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="7eabd-142">Sandėlis ir gamyba</span><span class="sxs-lookup"><span data-stu-id="7eabd-142">Warehouse and production</span></span>
|                                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eabd-143">**Ką galite daryti?**</span><span class="sxs-lookup"><span data-stu-id="7eabd-143">**What can you do?**</span></span>                                                                                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="7eabd-144">**Kodėl tai svarbu?**</span><span class="sxs-lookup"><span data-stu-id="7eabd-144">**Why is this important?**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="7eabd-145">Nustatykite sandėlio darbo strategiją, kuri kontroliuoja produktų rinkinio darbo kūrimą konkrečiose vietose.</span><span class="sxs-lookup"><span data-stu-id="7eabd-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="7eabd-146">Sandėlio procesai ne visada apima darbą.</span><span class="sxs-lookup"><span data-stu-id="7eabd-146">Warehouse processes don’t always include work.</span></span> <span data-ttu-id="7eabd-147">Naudodami naująją sandėlio darbo strategiją, galite neleisti konkrečiose vietose kurti tam tikro produktų rinkinio žaliavų paėmimo ir pagamintų prekių padėjimo darbo.</span><span class="sxs-lookup"><span data-stu-id="7eabd-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="7eabd-148">Nurodykite, kad gamybos išeigos vieta nėra kontroliuojama pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="7eabd-148">Specify that a production output location isn't license plate–controlled.</span></span>                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="7eabd-149">Dabar galite nurodyti, kad produktų išeigos vieta nėra kontroliuojama pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="7eabd-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="7eabd-150">Pavyzdžiui, ši funkcija yra naudinga, kai pirminės gamybos užsakymas ataskaitą apie baigtas prekes pateikia tiesiai toje vietoje, kuri naudojama kaip tolesnio gamybos užsakymo gamybos išeigos vieta.</span><span class="sxs-lookup"><span data-stu-id="7eabd-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span>                                                                                                                                                     |
| <span data-ttu-id="7eabd-151">Teikite pagalbą KS, kuriose yra prekių, turinčių skirtingas tos pačios prekės produktų dimensijas.</span><span class="sxs-lookup"><span data-stu-id="7eabd-151">Support BOMs that include items with different product dimensions of the same item.</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="7eabd-152">Gamyboje naudodami vieną ar kelias produkto dimensijas, gali būti atvejų, kai jūs norėsite prekę gaminti pagal kitą tos pačios prekės variantą.</span><span class="sxs-lookup"><span data-stu-id="7eabd-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="7eabd-153">Daugiau informacijos žr. [šiame tinklaraštyje](https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/).</span><span class="sxs-lookup"><span data-stu-id="7eabd-153">For more information, see [this blog](https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/).</span></span>                                                                  |
| <span data-ttu-id="7eabd-154">Gamybos užsakymai, kurių cikliškumo struktūros yra pirmame KS lygyje, nėra įtraukiamos į materialiųjų išteklių planavimo KS lygio skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="7eabd-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="7eabd-155">Produkto variantams priskirti teisingų KS lygių neįmanoma, jei pasirinkti gamybos užsakymai yra KS hierarchijos cikliškumo priežastis.</span><span class="sxs-lookup"><span data-stu-id="7eabd-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7eabd-156">Apskaičiuokite atskirus materialiųjų išteklių planavimo ir išlaidų apskaičiavimo KS lygius. • Materialiųjų išteklių planavimo KS lygiai yra apskaičiuojami naujoje lentelėje **ReqItemLevel**.</span><span class="sxs-lookup"><span data-stu-id="7eabd-156">Calculate separate BOM levels for material resource planning and cost calculation: • For material resource planning, BOM levels are calculated in the new **ReqItemLevel** table.</span></span> <span data-ttu-id="7eabd-157">Baigti gamybos užsakymai į skaičiavimą neįtraukiami.</span><span class="sxs-lookup"><span data-stu-id="7eabd-157">Ended production orders are ignored in the calculation.</span></span> <span data-ttu-id="7eabd-158">• Gamybos išlaidų skaičiavimo KS lygiai yra apskaičiuojami lentelėje **InventTable**.</span><span class="sxs-lookup"><span data-stu-id="7eabd-158">• For production cost calculation, BOM levels are calculated in the **InventTable**.</span></span> <span data-ttu-id="7eabd-159">Baigti gamybos užsakymai įtraukiami į skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="7eabd-159">Ended production orders are included in the calculation.</span></span> | <span data-ttu-id="7eabd-160">• Vykdant materialiųjų išteklių planavimą, pvz., bendrojo planavimo plano planavimą ir išskleidimą, reikia perskaičiuoti tik materialiųjų išteklių planavime naudojamus KS lygius.</span><span class="sxs-lookup"><span data-stu-id="7eabd-160">• When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="7eabd-161">Kitaip tariant, gamybos išlaidų skaičiavime naudojamų KS lygių skaičiuoti nereikia.</span><span class="sxs-lookup"><span data-stu-id="7eabd-161">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span> <span data-ttu-id="7eabd-162">• Vykdant išlaidų operacijas, pvz., atsargų uždarymą, reikia perskaičiuoti tik gamybos išlaidų skaičiavime naudojamus KS lygius.</span><span class="sxs-lookup"><span data-stu-id="7eabd-162">• When running  costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to recalculated.</span></span> |

 

<a name="see-also"></a><span data-ttu-id="7eabd-163">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="7eabd-163">See also</span></span>
--------

[<span data-ttu-id="7eabd-164">Kas nauja ar pasikeitė</span><span class="sxs-lookup"><span data-stu-id="7eabd-164">What's new or changed</span></span>](whats-new-changed.md)

[<span data-ttu-id="7eabd-165">Nauji ar atnaujinti užduočių vedliai (2016 m. gegužės mėn.)</span><span class="sxs-lookup"><span data-stu-id="7eabd-165">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)



