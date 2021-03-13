---
title: Mišrios realybės vadovų pateikimas į gamybą įtrauktiems darbuotojams
description: Šioje temoje paaiškinta, kaip susieti „Microsoft Dynamics 365 Supply Chain Management“ gamybos valdymo modulį su „Dynamics 365 Guides“.
author: cabeln
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 3e69f9007b6605a07c6bec189b596d36a26f6222
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007220"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="d862c-103">Mišrios realybės vadovų pateikimas į gamybą įtrauktiems darbuotojams</span><span class="sxs-lookup"><span data-stu-id="d862c-103">Provide mixed-reality Guides for workers in production</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d862c-104">Į gamybos procesus įtrauktiems darbuotojams bus pateikiami atitinkamos instrukcijos, kurios bus rodomos tinkamu laiku, atsižvelgiant į atliekamą darbą.</span><span class="sxs-lookup"><span data-stu-id="d862c-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="d862c-105">*Instrukcijos* taikomos kelioms darbo sritims, įskaitant surinkimą, aptarnavimą, operacijas, sertifikavimą ir saugą.</span><span class="sxs-lookup"><span data-stu-id="d862c-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="d862c-106">Kalbant apie visas šios pagrindines verslo veiklas, pateikiamos mokymo instrukcijos gali padėti darbuotojams daugiau pasiekti ir geriau dirbti.</span><span class="sxs-lookup"><span data-stu-id="d862c-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="d862c-107">Įžanga</span><span class="sxs-lookup"><span data-stu-id="d862c-107">Introduction</span></span>

<span data-ttu-id="d862c-108">Instrukcijas galite pateikti skirtingais būdais.</span><span class="sxs-lookup"><span data-stu-id="d862c-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="d862c-109">Viena efektyvi sistema, kurią galima naudoti iš karto, naudoja [„Dynamics 365 Guides“](https://dynamics.microsoft.com/mixed-reality/guides/).</span><span class="sxs-lookup"><span data-stu-id="d862c-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="d862c-110">„Dynamics 365 Guides“ gali padėti darbuotojams suteikdama galimybę mokytis.</span><span class="sxs-lookup"><span data-stu-id="d862c-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="d862c-111">Galite apibrėžti standartinius procesus su nuosekliomis instrukcijomis, kurios padės jūsų darbuotojams naudoti reikalingus įrankius ir dalis bei suteiks informacijos darbuotojams, kaip naudoti šiuos įrankius realiose darbo situacijose.</span><span class="sxs-lookup"><span data-stu-id="d862c-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="d862c-112">Vadovus galite susieti su įvairiomis gamybos kontrolės sritimis, įskaitant toliau nurodytas:</span><span class="sxs-lookup"><span data-stu-id="d862c-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="d862c-113">Ištekliai</span><span class="sxs-lookup"><span data-stu-id="d862c-113">Resources</span></span>](#resources)
- [<span data-ttu-id="d862c-114">Išteklių grupės</span><span class="sxs-lookup"><span data-stu-id="d862c-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="d862c-115">Patvirtinti produktai</span><span class="sxs-lookup"><span data-stu-id="d862c-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="d862c-116">Formulės</span><span class="sxs-lookup"><span data-stu-id="d862c-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="d862c-117">Formulės versijos</span><span class="sxs-lookup"><span data-stu-id="d862c-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="d862c-118">Komplektavimo specifikacijos (KS)</span><span class="sxs-lookup"><span data-stu-id="d862c-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="d862c-119">KS versijos</span><span class="sxs-lookup"><span data-stu-id="d862c-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="d862c-120">Maršrutai</span><span class="sxs-lookup"><span data-stu-id="d862c-120">Routes</span></span>](#routes)
- [<span data-ttu-id="d862c-121">Maršruto versijos</span><span class="sxs-lookup"><span data-stu-id="d862c-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="d862c-122">Įprastų operacijų ryšiai</span><span class="sxs-lookup"><span data-stu-id="d862c-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="d862c-123">Taip pat vadovus galite susieti su turto valdymu.</span><span class="sxs-lookup"><span data-stu-id="d862c-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="d862c-124">Išsamesnės informacijos apie šią parinktį žr. [„Dynamics 365 Supply Chain Management“ (turto valdymo) integravimas su „Dynamics 365 Guides“](../asset-management/asset-management-guides-integration.md).</span><span class="sxs-lookup"><span data-stu-id="d862c-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="d862c-125">Kai darbą atliekantis darbuotojas ceche pasirenka užduotį naudodamas „Supply Chain Management“, užduoties kortelėje darbuotojas gali matyti [susijusias instrukcijas](#logic).</span><span class="sxs-lookup"><span data-stu-id="d862c-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="d862c-126">Darbuotojui pasirinkus konkrečią instrukciją, ekrane rodomas instrukcijos QR kodas.</span><span class="sxs-lookup"><span data-stu-id="d862c-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="d862c-127">Tada darbuotojas naudodamas „HoloLens“ nuskaito QR kodą, kuris paleidžia „Guides“ ir rodo reikiamas instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="d862c-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="d862c-128">Toliau esančiuose poskyriuose aprašyti keli pasirinkti scenarijai, kai pramonės įmonės, naudodamos „Guides“ gamybos instrukcijoms rodyti, gali siekti didžiausios vertės.</span><span class="sxs-lookup"><span data-stu-id="d862c-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="d862c-129">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d862c-129">Assembly</span></span>

<span data-ttu-id="d862c-130">![„Guides“ naudojimas surinkimo užduotims](media/instruction-guides-hero-assembly.png "„Guides“ naudojimas aptarnavimo užduotims")</span><span class="sxs-lookup"><span data-stu-id="d862c-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="d862c-131">Surinkimo operacijų instrukcijose darbuotojams nurodomi reikalingi įrankiai ir dalys bei kaip juos naudoti realiose darbo situacijose.</span><span class="sxs-lookup"><span data-stu-id="d862c-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="d862c-132">Gamybos vadovai gali kurti ir priskirti vadovus, pavyzdžiui, [gamybos maršrutams](routes-operations.md), [operacijų ryšiams](routes-operations.md#operation-relations) arba [komplektavimo specifikacijoms](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="d862c-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="d862c-133">Darbuotojai matys reikiamas instrukcijas, susijusias su atitinkama darbo patirtimi ceche.</span><span class="sxs-lookup"><span data-stu-id="d862c-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="d862c-134">Aptarnavimas</span><span class="sxs-lookup"><span data-stu-id="d862c-134">Service</span></span>

<span data-ttu-id="d862c-135">![„Guides“ naudojimas aptarnavimo užduotims](media/instruction-guides-hero-service.png "„Guides“ naudojimas aptarnavimo užduotims")</span><span class="sxs-lookup"><span data-stu-id="d862c-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="d862c-136">Teikite technikams instrukcijas darbo vietoje, kad nebereikėtų planuoti papildomų apsilankymų.</span><span class="sxs-lookup"><span data-stu-id="d862c-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="d862c-137">Aptarnavimo vadovai, pavyzdžiui, gali priskirti vadovus, padedančius atlikti kokybės vertinimo procedūras, konkretiems [produktams](../../commerce/product.md).</span><span class="sxs-lookup"><span data-stu-id="d862c-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="d862c-138">Kokybė</span><span class="sxs-lookup"><span data-stu-id="d862c-138">Quality</span></span>

<span data-ttu-id="d862c-139">![„Guides“ naudojimas kokybės užtikrinimo užduotims](media/instruction-guides-hero-quality.png "„Guides“ naudojimas kokybės užtikrinimo užduotims")</span><span class="sxs-lookup"><span data-stu-id="d862c-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="d862c-140">Diekite naujus procesus ir užtikrinkite didesnį nuoseklumą paversdami darbuotojo žinias į pakartotinai pritaikomą įrankį.</span><span class="sxs-lookup"><span data-stu-id="d862c-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="d862c-141">Kokybės užtikrinimo vadovai, pavyzdžiui, gali priskirti vadovus, padedančius atlikti kokybės vertinimo procedūras, [produktams](../../commerce/product.md).</span><span class="sxs-lookup"><span data-stu-id="d862c-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="d862c-142">Sertifikatai</span><span class="sxs-lookup"><span data-stu-id="d862c-142">Certifications</span></span>

<span data-ttu-id="d862c-143">![„Guides“ naudojimas su sertifikavimu susijusioms užduotims](media/instruction-guides-hero-certification.png "„Guides“ naudojimas su sertifikavimu susijusioms užduotims")</span><span class="sxs-lookup"><span data-stu-id="d862c-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="d862c-144">Užtikrinkite, kad kiekvienas darbuotojas atitiktų aukštus standartus, greitai identifikuodami darbuotojus ir vietas, kuriems reikia pagalbos.</span><span class="sxs-lookup"><span data-stu-id="d862c-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="d862c-145">Sauga</span><span class="sxs-lookup"><span data-stu-id="d862c-145">Safety</span></span>

<span data-ttu-id="d862c-146">![„Guides“ naudojimas darbo saugos instrukcijose](media/instruction-guides-hero-safety.png "„Guides“ naudojimas darbo saugos instrukcijose")</span><span class="sxs-lookup"><span data-stu-id="d862c-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="d862c-147">Pateikite instrukcijas, kaip vykdyti pavojingas procedūras, virtualiai prieš jas atliekant fizinėje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="d862c-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="d862c-148">Taikant mišrios tikrovės koncepciją, darbuotojai gali susipažinti su pavojingomis procedūromis virtualiai.</span><span class="sxs-lookup"><span data-stu-id="d862c-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="d862c-149">Gamybos vadovai gali pateikti specialias pavojingų medžiagų tvarkymo arba atidaus tvarkymo procedūrų instrukcijas, priskirdami instrukcijas [produktams](../../commerce/product.md), [maršrutams](routes-operations.md) ir [operacijoms](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="d862c-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="d862c-150">Darbo su instrukcijomis ir „Guides“ pradžia</span><span class="sxs-lookup"><span data-stu-id="d862c-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="d862c-151">Tam, kad būtų galima gauti instrukcijas vykdant gamybos procesą, „Supply Chain Management“ yra iš karto integruotas su „Dynamics 365 Guides“.</span><span class="sxs-lookup"><span data-stu-id="d862c-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="d862c-152">Norint kurti, tvarkyti ir priskirti mišrios realybės instrukcijas gamybos ištekliams ir darbui, reikalingas licencijuotas ir įdiegtas „Guides“ programos egzempliorius.</span><span class="sxs-lookup"><span data-stu-id="d862c-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="d862c-153">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="d862c-153">Prerequisites</span></span>

<span data-ttu-id="d862c-154">Tam, kad galėtumėte naudoti šią funkciją, jūsų sistemą turi sudaryti toliau nurodytos dalys.</span><span class="sxs-lookup"><span data-stu-id="d862c-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="d862c-155">„Dynamics 365 Supply Chain Management“ 10.0.15 arba naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="d862c-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="d862c-156">[Dvigubas rašymas](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) „Supply Chain Management“ programoms.</span><span class="sxs-lookup"><span data-stu-id="d862c-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="d862c-157">[„Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution)“ 400.0.1.48 arba naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="d862c-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="d862c-158">Funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="d862c-158">Turn on the feature</span></span>

<span data-ttu-id="d862c-159">Tam, kad funkcija būtų prieinama jūsų sistemoje, turite aktyvinti jos konfigūracijos raktus.</span><span class="sxs-lookup"><span data-stu-id="d862c-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="d862c-160">Tai atlikti reikia tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="d862c-160">You only need to do this once.</span></span> <span data-ttu-id="d862c-161">Norinti tai padaryti, administratorius turi atlikti šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="d862c-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="d862c-162">Perjunkite savo sistemą į priežiūros režimą, kaip aprašyta [Priežiūros režimas](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="d862c-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="d862c-163">Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="d862c-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="d862c-164">Išplėskite sritį **Mišrioji realybė** ir pasirinkite žymės langelį **Mišriosios realybės vadovas**.</span><span class="sxs-lookup"><span data-stu-id="d862c-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="d862c-165">Išplėskite sritį **Gamybos valdymas** ir pasirinkite žymės langelį **Gamybos instrukcijos**.</span><span class="sxs-lookup"><span data-stu-id="d862c-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="d862c-166">Išjunkite priežiūros režimą, kaip aprašyta [Priežiūros režimas](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="d862c-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="d862c-167">Konfigūravimas, kaip vadovai bus rodomi ceche</span><span class="sxs-lookup"><span data-stu-id="d862c-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="d862c-168">Norėdami sukonfigūruoti, kaip vadovai bus rodomi ceche, eikite į **Mišrioji realybė \>Dynamics 365 Guides\>Konfigūruoti „Guides“ integravimą**.</span><span class="sxs-lookup"><span data-stu-id="d862c-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="d862c-169">![Vadovo integravimo gamybai konfigūravimas](media/instruction-guides-configure-integration.png "Vadovo integravimo gamybai konfigūravimas")</span><span class="sxs-lookup"><span data-stu-id="d862c-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="d862c-170">Užpildykite toliau nurodytus laukus:</span><span class="sxs-lookup"><span data-stu-id="d862c-170">Set the following fields:</span></span>

- <span data-ttu-id="d862c-171">**„Microsoft Dataverse“ URL** - Nurodykite URL „Microsoft Dataverse“ aplinkai, kurioje kuriate savo „Guides“.</span><span class="sxs-lookup"><span data-stu-id="d862c-171">**Microsoft Dataverse URL** - Specify the URL for the Microsoft Dataverse environment where you create your Guides.</span></span> <span data-ttu-id="d862c-172">Formatas yra „contoso.crm4.dynamics.com", kuriame pirmoji dalis URL dažniausiai pavadinta organizacijos vardu (tokiu kaip „contoso."), antroji dalis yra duomenų regiono jūsų aplinka (tokia kaip „crm4."), o paskutinė dalis - domenas (toks kaip „dynamics.com").</span><span class="sxs-lookup"><span data-stu-id="d862c-172">The format is "contoso.crm4.dynamics.com", where the first part of the URL is typically named after your organization (such as "contoso."), the second part is specific to the data region of your environment (such as "crm4."), and the last part is the domain (such as "dynamics.com").</span></span> <span data-ttu-id="d862c-173">Vienas būdas surasti reikiamą URL yra eiti į [home.dynamics.com](https://home.dynamics.com/) ir tada atverti savo „Guides“ programą.</span><span class="sxs-lookup"><span data-stu-id="d862c-173">One way to find the right URL is to go to [home.dynamics.com](https://home.dynamics.com/) and then open your Guides app.</span></span> <span data-ttu-id="d862c-174">Atvėrus „Guides“ programą, matysite URL adreso juostoje savo naršyklėje (imkite tik pagrindinį URL, kuris parodytas ankstesniame pavyzdyje).</span><span class="sxs-lookup"><span data-stu-id="d862c-174">When Guides opens, you will see the URL in the address bar of your browser (only take the base URL, which should resemble the previous example).</span></span> <span data-ttu-id="d862c-175">Ši vertė naudojama sudaryti adresus jūsų gairėse ir bus koduojama į QR kodus."</span><span class="sxs-lookup"><span data-stu-id="d862c-175">This value is used to compose addresses for your guides and will be encoded into the QR codes."</span></span>
- <span data-ttu-id="d862c-176">**QR kodo dydis** – nurodykite sugeneruoto QR kodo dydį.</span><span class="sxs-lookup"><span data-stu-id="d862c-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="d862c-177">Rekomenduojame pasirinkti dydį, kuris didžiąją ekrano dalį, bet ne didesnį.</span><span class="sxs-lookup"><span data-stu-id="d862c-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="d862c-178">Įprastai tinkama reikšmė yra *15*.</span><span class="sxs-lookup"><span data-stu-id="d862c-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="d862c-179">**QR kodo klaidų taisymo lygis** – nurodykite QR kodo detalumo lygį.</span><span class="sxs-lookup"><span data-stu-id="d862c-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="d862c-180">Didesnis detalumas gali padėti užtikrinti didesnį kodo patikimumą, bet **QR kodo dydis** turi būti pakankamai didelis, kad būtų užtikrintas detalumo lygis, kurio reikia pasirinktam koregavimo lygiui.</span><span class="sxs-lookup"><span data-stu-id="d862c-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>

> [!TIP]
> - <span data-ttu-id="d862c-181">QR kodai, kurie yra per dideli jūsų monitoriui, gali būti generuojami šiek tiek ilgiau, o po to jie bus sumažinami, kad atitiktų ekraną.</span><span class="sxs-lookup"><span data-stu-id="d862c-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="d862c-182">Tai nesuteikia kokių nors pranašumų.</span><span class="sxs-lookup"><span data-stu-id="d862c-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="d862c-183">Esant per mažiems QR kodams, tam tikrose aplinkose „HoloLens“ gali nepavykti tinkamai nuskaityti kodo.</span><span class="sxs-lookup"><span data-stu-id="d862c-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="d862c-184">Rekomenduojame išbandyti kiekvieno įrenginio, kuris rodytis QR kodus „HoloLens“ vartotojams, parametrus.</span><span class="sxs-lookup"><span data-stu-id="d862c-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="d862c-185">Pasirinkite parametrus, kurie užtikrintų pakankamą patikimumą cecho aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="d862c-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="d862c-186">Peržiūrėkite visų vadovo priskyrimų apžvalgą</span><span class="sxs-lookup"><span data-stu-id="d862c-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="d862c-187">Norėdami peržiūrėti visų jūsų organizacijoje prieinamų vadovų sąrašą bei visų gamybos procesų ir išteklių priskyrimų sąrašą, naudokite puslapį **Visi vadovai“**.</span><span class="sxs-lookup"><span data-stu-id="d862c-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="d862c-188">Norėdami atidaryti, eikite į **Mišrioji realybė \> Vadovai \> Visi vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="d862c-189">Viršuje esančiame sąraše rodomi visi prienami vadovai, be to, norėdami filtruoti sąrašą, galite naudoti čia esantį lauką.</span><span class="sxs-lookup"><span data-stu-id="d862c-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="d862c-190">Apačioje esančiame sąraše rodomi visi vadovo priskyrimai ir yra valdymui skirta įrankių juosta.</span><span class="sxs-lookup"><span data-stu-id="d862c-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="d862c-191">![Vadovų valdymas](media/instruction-guides-allguides.png "Vadovų valdymas")</span><span class="sxs-lookup"><span data-stu-id="d862c-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="d862c-192">Toliau esančiuose skyriuose aprašyti objektų tipai, kuriems galite priskirti vadovus.</span><span class="sxs-lookup"><span data-stu-id="d862c-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="d862c-193">Kiekviename priskirtame vadove pateikiamos instrukcijos, kurios automatiškai pridedamos prie atitinkamų gamybos užduočių ir kurios bus pateikiamos ceche.</span><span class="sxs-lookup"><span data-stu-id="d862c-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="d862c-194">Vadovo susiejimas su ištekliu</span><span class="sxs-lookup"><span data-stu-id="d862c-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="d862c-195">Pridėkite vadovą prie [ištekliaus](operations-resources.md), kuris pateiks vadovą, atitinkamų gamybos užduočių kontekste.</span><span class="sxs-lookup"><span data-stu-id="d862c-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="d862c-196">Tipinis scenarijus naudojant išteklius</span><span class="sxs-lookup"><span data-stu-id="d862c-196">Typical scenario using resources</span></span>

<span data-ttu-id="d862c-197">Pavyzdžiui, vadovą su bendrosiomis mašinų saugos arba darbo instrukcijomis galite pridėti prie mašinos tipo ištekliaus.</span><span class="sxs-lookup"><span data-stu-id="d862c-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="d862c-198">Tada vadovas bus pasiekiamas kiekvienai mašina atliekamai užduočiai.</span><span class="sxs-lookup"><span data-stu-id="d862c-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="d862c-199">Vadovo pridėjimas prie ištekliaus</span><span class="sxs-lookup"><span data-stu-id="d862c-199">Add a Guide to a resource</span></span>

<span data-ttu-id="d862c-200">Norėdami pridėti vadovą prie ištekliaus:</span><span class="sxs-lookup"><span data-stu-id="d862c-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="d862c-201">Eikite į **Gamybos kontrolė \> Sąranka \> Ištekliai \> Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="d862c-202">Sąrašo srityje pasirinkite išteklių, kuriam norite priskirti vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="d862c-203">Išplėskite „FastTab“ **Susiję vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="d862c-204">Įrankių juostoje **Susiję vadovai** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d862c-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="d862c-205">Nauja eilutė pridedama prie tinklelio.</span><span class="sxs-lookup"><span data-stu-id="d862c-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="d862c-206">Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.</span><span class="sxs-lookup"><span data-stu-id="d862c-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="d862c-207">Jei yra daug vadovų, galite filtruoti sąrašą, kad surastumėte tą, kurio ieškote.</span><span class="sxs-lookup"><span data-stu-id="d862c-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="d862c-208">![Vadovų valdymas](media/instruction-guides-allguides.png "Vadovų valdymas")</span><span class="sxs-lookup"><span data-stu-id="d862c-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="d862c-209">Vadovo susiejimas su išteklių grupe</span><span class="sxs-lookup"><span data-stu-id="d862c-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="d862c-210">Jei vadovą naudojate mašinų grupių, gamybos linijų arba darbo elementų valdymui, jį galite įtraukti į [išteklių grupes](tasks/define-discrete-manufacturing-resource-group.md).</span><span class="sxs-lookup"><span data-stu-id="d862c-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="d862c-211">Tipiniai scenarijai naudojant išteklių grupes</span><span class="sxs-lookup"><span data-stu-id="d862c-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="d862c-212">**1 pavyzdys.** Sukonfigūravote išteklių grupę kelioms to paties modelio mašinoms.</span><span class="sxs-lookup"><span data-stu-id="d862c-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="d862c-213">Užuot priskyrę atitinkamą darbo su mašinos modeliu instrukciją kiekvienam atitinkamam ištekliui, vadovą galite priskirti išteklių grupei, kuri atitinka mašinos modelį.</span><span class="sxs-lookup"><span data-stu-id="d862c-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="d862c-214">**2 pavyzdys.** Sukonfigūravote darbo elementų, kuriuose yra įvairių mašinų, išteklių grupę ir turite vadovą, kuris pateikia bendrąsias instrukcijas, kaip tvarkyti darbo elementą.</span><span class="sxs-lookup"><span data-stu-id="d862c-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="d862c-215">Vadovas taikomas bet kokiai darbo elemento gamybos veiklai.</span><span class="sxs-lookup"><span data-stu-id="d862c-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="d862c-216">Vadovo įtraukimas į išteklių grupę</span><span class="sxs-lookup"><span data-stu-id="d862c-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="d862c-217">Norėdami įtraukti vadovą į išteklių grupę:</span><span class="sxs-lookup"><span data-stu-id="d862c-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="d862c-218">Eikite į **Gamybos kontrolė \> Sąranka \> Ištekliai \> Išteklių grupės**.</span><span class="sxs-lookup"><span data-stu-id="d862c-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="d862c-219">Sąrašo srityje pasirinkite išteklių grupę, kuriai norite priskirti vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="d862c-220">Išplėskite „FastTab“ **Susiję vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="d862c-221">Įrankių juostoje **Susiję vadovai** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d862c-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="d862c-222">Nauja eilutė pridedama prie tinklelio.</span><span class="sxs-lookup"><span data-stu-id="d862c-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="d862c-223">Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.</span><span class="sxs-lookup"><span data-stu-id="d862c-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="d862c-224">Jei yra daug vadovų, galite filtruoti sąrašą, kad surastumėte tą, kurio ieškote.</span><span class="sxs-lookup"><span data-stu-id="d862c-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="d862c-225">![Vadovo įtraukimas į išteklių grupę](media/instruction-guides-resourcegroup.png "Vadovo įtraukimas į išteklių grupę")</span><span class="sxs-lookup"><span data-stu-id="d862c-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="d862c-226">Vadovo susiejimas su išleistu produktu</span><span class="sxs-lookup"><span data-stu-id="d862c-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="d862c-227">Vadovą galite pridėti prie bet kurio [išleisto produkto](../pim/tasks/create-released-product-single-company.md).</span><span class="sxs-lookup"><span data-stu-id="d862c-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="d862c-228">Įprastinis scenarijus naudojant išleistus produktus</span><span class="sxs-lookup"><span data-stu-id="d862c-228">Typical scenario using released products</span></span>

<span data-ttu-id="d862c-229">Produktų lygio vadovai pateikia cecho darbuotojams darbo su konkrečiu išleistu produktu ar preke arba eksploatavimo instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="d862c-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="d862c-230">Vadovo pridėjimas prie išleisto produkto</span><span class="sxs-lookup"><span data-stu-id="d862c-230">Add a Guide to a released product</span></span>

<span data-ttu-id="d862c-231">Norėdami pridėti vadovą prie išleisto produkto:</span><span class="sxs-lookup"><span data-stu-id="d862c-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="d862c-232">Eikite į **Gamybos informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="d862c-233">Atidarykite produktą, kuriam norite priskirti vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="d862c-234">Veiksmų srityje atidarykite skirtuką **Inžinierius** ir grupėje **Peržiūra** pasirinkite **Susiję vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="d862c-235">Atidaromas pasirinkto produkto puslapis **Susiję vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="d862c-236">Veiksmų srityje pasirinkite **Įtraukti** ir pridėkite naują eilutę prie tinklelio.</span><span class="sxs-lookup"><span data-stu-id="d862c-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="d862c-237">Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.</span><span class="sxs-lookup"><span data-stu-id="d862c-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="d862c-238">![Vadovo pridėjimas prie išleisto produkto](media/instruction-guides-ReleasedProduct-AddGuides.png "Vadovo pridėjimas prie išleisto produkto")</span><span class="sxs-lookup"><span data-stu-id="d862c-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="d862c-239">Vadovo susiejimas su formule</span><span class="sxs-lookup"><span data-stu-id="d862c-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="d862c-240">Vadovą galite pridėti prie bet kurios [formulės](bill-of-material-bom.md#formulas-co-products-and-by-products).</span><span class="sxs-lookup"><span data-stu-id="d862c-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="d862c-241">Tipinis scenarijus naudojant formules</span><span class="sxs-lookup"><span data-stu-id="d862c-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="d862c-242">Formulės lygio vadovai teikia cecho darbuotojams darbo instrukcijas formulės arba recepto kontekste.</span><span class="sxs-lookup"><span data-stu-id="d862c-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="d862c-243">Vadovus taip pat galima priskirti formulės versijoms.</span><span class="sxs-lookup"><span data-stu-id="d862c-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="d862c-244">Vadovus, susijusius su gamybos procesais, pagal formulę galite priskirti maršrutui, maršruto versijai ar maršruto operacijų ryšiams.</span><span class="sxs-lookup"><span data-stu-id="d862c-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="d862c-245">Šiuo metu vadovų negalima pridėti prie atskirų formulės eilučių.</span><span class="sxs-lookup"><span data-stu-id="d862c-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="d862c-246">Vadovo pridėjimas prie fromulės</span><span class="sxs-lookup"><span data-stu-id="d862c-246">Add a Guide to a formula</span></span>

<span data-ttu-id="d862c-247">Norėdami pridėti vadovą prie formulės:</span><span class="sxs-lookup"><span data-stu-id="d862c-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="d862c-248">Eikite į **Gamybos informacijos valdymas \> KS ir formulės \> Formulės**.</span><span class="sxs-lookup"><span data-stu-id="d862c-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="d862c-249">Atidarykite formulę, kuriai norite priskirti vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="d862c-250">Atidarykite skirtuką **Antraštė**, esantį virš viršutinio „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="d862c-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="d862c-251">Išplėskite „FastTab“ **Susiję vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="d862c-252">Įrankių juostoje **Susiję vadovai** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d862c-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="d862c-253">Nauja eilutė pridedama prie tinklelio.</span><span class="sxs-lookup"><span data-stu-id="d862c-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="d862c-254">Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.</span><span class="sxs-lookup"><span data-stu-id="d862c-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="d862c-255">![Vadovo pridėjimas prie formulės](media/instruction-guides-Formula.png "Vadovo pridėjimas prie formulės")</span><span class="sxs-lookup"><span data-stu-id="d862c-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="d862c-256">Vadovo susiejimas su formulės versija</span><span class="sxs-lookup"><span data-stu-id="d862c-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="d862c-257">Vadovą galite pridėti prie bet kurios [formulės versijos](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="d862c-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="d862c-258">Tipinis scenarijus naudojant formulės versijas</span><span class="sxs-lookup"><span data-stu-id="d862c-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="d862c-259">Prie atskirų formulės versijų pridėti vadovai teikia cecho darbuotojams instrukcijas, kurios yra susijusios su gamyba taikant atitinkamą formulės recepto versiją.</span><span class="sxs-lookup"><span data-stu-id="d862c-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="d862c-260">Vadovus, susijusius su gamybos procesais, pagal formulės versiją galite priskirti maršrutui, maršruto versijai ar maršruto operacijų ryšiams.</span><span class="sxs-lookup"><span data-stu-id="d862c-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="d862c-261">Šiuo metu vadovų negalima pridėti prie atskirų formulės eilučių.</span><span class="sxs-lookup"><span data-stu-id="d862c-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="d862c-262">Vadovo pridėjimas prie formulės versijos</span><span class="sxs-lookup"><span data-stu-id="d862c-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="d862c-263">Norėdami pridėti vadovą prie formulės versijos:</span><span class="sxs-lookup"><span data-stu-id="d862c-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="d862c-264">Eikite į **Gamybos informacijos valdymas \> KS ir formulės \> Formulės**.</span><span class="sxs-lookup"><span data-stu-id="d862c-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="d862c-265">Atidarykite formulę, prie kurios versijos norite priskirti vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="d862c-266">Atidarykite skirtuką **Antraštė**, esantį virš viršutinio „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="d862c-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="d862c-267">„FastTab“ **Formulės versijos** pasirinkite versiją, kuriai norite priskirti vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="d862c-268">Įrankių juostoje **Formulės versijos** pasirinkite **Susiję vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="d862c-269">![Su pasirinkta formulės versija susijusių vadovų atidarymas](media/instruction-guides-FormulaVersion.png "Su pasirinkta formulės versija susijusių vadovų atidarymas")</span><span class="sxs-lookup"><span data-stu-id="d862c-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="d862c-270">Atidaromas formulės versijos puslapis **Susiję vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="d862c-271">Veiksmų srityje pasirinkite **Įtraukti** ir pridėkite naują eilutę prie tinklelio.</span><span class="sxs-lookup"><span data-stu-id="d862c-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="d862c-272">Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.</span><span class="sxs-lookup"><span data-stu-id="d862c-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="d862c-273">![Vadovo pridėjimas prie formulės versijos](media/instruction-guides-FormulaVersionAddGuide.png "Vadovo pridėjimas prie formulės versijos")</span><span class="sxs-lookup"><span data-stu-id="d862c-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="d862c-274">Vadovo susiejimas su KS</span><span class="sxs-lookup"><span data-stu-id="d862c-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="d862c-275">Vadovą galite įtraukti į bet kurią [komplektavimo specifikaciją](bill-of-material-bom.md) (KS).</span><span class="sxs-lookup"><span data-stu-id="d862c-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="d862c-276">Įprastinis scenarijus naudojant komplektavimo specifikacijas</span><span class="sxs-lookup"><span data-stu-id="d862c-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="d862c-277">Prie KS pridėti vadovai teikia cecho darbuotojams instrukcijas, paaiškinančias, kaip ruošti ir dirbti su medžiaga iš KS.</span><span class="sxs-lookup"><span data-stu-id="d862c-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="d862c-278">Vadovus taip pat galima priskirti KS versijoms.</span><span class="sxs-lookup"><span data-stu-id="d862c-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="d862c-279">Šiuo metu vadovų negalima pridėti prie atskirų KS eilučių.</span><span class="sxs-lookup"><span data-stu-id="d862c-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="d862c-280">Vadovo pridėjimas prie KS</span><span class="sxs-lookup"><span data-stu-id="d862c-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="d862c-281">Norėdami pridėti vadovą prie KS:</span><span class="sxs-lookup"><span data-stu-id="d862c-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="d862c-282">Eikite į **Gamybos informacijos valdymas \> KS ir formulės \> Komplektavimo specifikacijos**.</span><span class="sxs-lookup"><span data-stu-id="d862c-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="d862c-283">Atidarykite KS, kuriai norite priskirti vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="d862c-284">Atidarykite skirtuką **Antraštė**, esantį virš viršutinio „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="d862c-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="d862c-285">Išplėskite „FastTab“ **Susiję vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="d862c-286">Įrankių juostoje **Susiję vadovai** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d862c-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="d862c-287">Nauja eilutė pridedama prie tinklelio.</span><span class="sxs-lookup"><span data-stu-id="d862c-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="d862c-288">Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.</span><span class="sxs-lookup"><span data-stu-id="d862c-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="d862c-289">![Vadovo pridėjimas prie KS](media/instruction-guides-BOM.png "Vadovo pridėjimas prie KS")</span><span class="sxs-lookup"><span data-stu-id="d862c-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="d862c-290">Vadovo susiejimas su KS versija</span><span class="sxs-lookup"><span data-stu-id="d862c-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="d862c-291">Vadovą galite įtraukti į bet kurią [komplektavimo specifikacijos versiją](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="d862c-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="d862c-292">Įprastinis scenarijus naudojant komplektavimo specifikacijos versijas</span><span class="sxs-lookup"><span data-stu-id="d862c-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="d862c-293">Prie atskiros KS versijos pridėti vadovai teikia cecho darbuotojams instrukcijas, kurios paaiškina, kaip paruošti ir dirbti su KS medžiagos versija, kuri skiriasi nuo bendrosios KS ar kitų versijų.</span><span class="sxs-lookup"><span data-stu-id="d862c-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="d862c-294">Šiuo metu vadovų negalima pridėti prie atskirų KS eilučių.</span><span class="sxs-lookup"><span data-stu-id="d862c-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="d862c-295">Vadovo pridėjimas prie KS versijos</span><span class="sxs-lookup"><span data-stu-id="d862c-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="d862c-296">Norėdami pridėti vadovą prie KS versijos:</span><span class="sxs-lookup"><span data-stu-id="d862c-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="d862c-297">Eikite į **Gamybos informacijos valdymas \> KS ir formulės \> Komplektavimo specifikacijos**.</span><span class="sxs-lookup"><span data-stu-id="d862c-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="d862c-298">Atidarykite KS, prie kurios versijos norite priskirti vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="d862c-299">Atidarykite skirtuką **Antraštė**, esantį virš viršutinio „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="d862c-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="d862c-300">„FastTab“ **KS versijos** pasirinkite versiją, kuriai norite priskirti vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="d862c-301">Įrankių juostoje **KS versijos** pasirinkite **Susiję vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="d862c-302">![Su pasirinkta KS versija susijusių vadovų atidarymas](media/instruction-guides-BOMVersion.png "Su pasirinkta KS versija susijusių vadovų atidarymas")</span><span class="sxs-lookup"><span data-stu-id="d862c-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="d862c-303">Atidaromas KS versijos puslapis **Susiję vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="d862c-304">Veiksmų srityje pasirinkite **Įtraukti** ir pridėkite naują eilutę prie tinklelio.</span><span class="sxs-lookup"><span data-stu-id="d862c-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="d862c-305">Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.</span><span class="sxs-lookup"><span data-stu-id="d862c-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="d862c-306">![Vadovo pridėjimas prie KS versijos](media/instruction-guides-BOMVersionAddGuide.png "Vadovo pridėjimas prie KS versijos")</span><span class="sxs-lookup"><span data-stu-id="d862c-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="d862c-307">Vadovo susiejimas su maršrutu</span><span class="sxs-lookup"><span data-stu-id="d862c-307">Associate a Guide to a route</span></span>

<span data-ttu-id="d862c-308">Vadovą galite pridėti prie bet kurio [maršruto](routes-operations.md).</span><span class="sxs-lookup"><span data-stu-id="d862c-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="d862c-309">Tipinis scenarijus naudojant maršrutus</span><span class="sxs-lookup"><span data-stu-id="d862c-309">Typical scenario using routes</span></span>

<span data-ttu-id="d862c-310">Maršrutai paprastai naudojami nurodyti, kaip tam tikras išleistas produktas turi būti gaminamas pagal KS arba KS versiją ir esant tam tikriems ištekliams arba išteklių grupėms.</span><span class="sxs-lookup"><span data-stu-id="d862c-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="d862c-311">Priskirkite vadovą maršrutui, kad pateiktumėte nuoseklias atitinkamo gamybos proceso instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="d862c-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="d862c-312">Vadovo pridėjimas prie maršruto</span><span class="sxs-lookup"><span data-stu-id="d862c-312">Add a Guide to a route</span></span>

<span data-ttu-id="d862c-313">Norėdami pridėti vadovą prie maršruto:</span><span class="sxs-lookup"><span data-stu-id="d862c-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="d862c-314">Eikite į **Gamybos kontrolė \> Visi maršrutai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="d862c-315">Atidarykite maršrutą, kuriam norite priskirti vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="d862c-316">Išplėskite „FastTab“ **Susiję vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="d862c-317">Įrankių juostoje **Susiję vadovai** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d862c-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="d862c-318">Nauja eilutė pridedama prie tinklelio.</span><span class="sxs-lookup"><span data-stu-id="d862c-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="d862c-319">Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.</span><span class="sxs-lookup"><span data-stu-id="d862c-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="d862c-320">![Vadovo pridėjimas prie maršruto](media/instruction-guides-Route.png "Vadovo pridėjimas prie maršruto")</span><span class="sxs-lookup"><span data-stu-id="d862c-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="d862c-321">Vadovo susiejimas su maršruto versija</span><span class="sxs-lookup"><span data-stu-id="d862c-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="d862c-322">Vadovą galite pridėti prie bet kurios [maršruto versijos](routes-operations.md#route-versions).</span><span class="sxs-lookup"><span data-stu-id="d862c-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="d862c-323">Tipinis scenarijus naudojant maršruto versijas</span><span class="sxs-lookup"><span data-stu-id="d862c-323">Typical scenario using route versions</span></span>

<span data-ttu-id="d862c-324">Maršrutų versijos paprastai naudojamos norint nurodyti gamybos procesų variantus pagal esamą maršrutą.</span><span class="sxs-lookup"><span data-stu-id="d862c-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="d862c-325">Kiekvienai maršruto versijai galite priskirti skirtingus vadovus.</span><span class="sxs-lookup"><span data-stu-id="d862c-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="d862c-326">Vadovo pridėjimas prie maršruto versijos</span><span class="sxs-lookup"><span data-stu-id="d862c-326">Add a Guide to a route version</span></span>

<span data-ttu-id="d862c-327">Norėdami pridėti vadovą prie maršruto versijos:</span><span class="sxs-lookup"><span data-stu-id="d862c-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="d862c-328">Eikite į **Gamybos kontrolė \> Visi maršrutai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="d862c-329">Atidarykite maršrutą, kuriam norite priskirti vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="d862c-330">„FastTab“ **Versijos** pasirinkite versiją, kuriai norite priskirti vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="d862c-331">Įrankių juostoje **Versijos** pasirinkite **Susiję vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="d862c-332">![Su pasirinkta maršruto versija susijusių vadovų atidarymas](media/instruction-guides-RouteVersion.png "Su pasirinkta maršruto versija susijusių vadovų atidarymas")</span><span class="sxs-lookup"><span data-stu-id="d862c-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="d862c-333">Atidaromas KS versijos puslapis **Susiję vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="d862c-334">Veiksmų srityje pasirinkite **Įtraukti** ir pridėkite naują eilutę prie tinklelio.</span><span class="sxs-lookup"><span data-stu-id="d862c-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="d862c-335">Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.</span><span class="sxs-lookup"><span data-stu-id="d862c-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="d862c-336">![Vadovo pridėjimas prie maršruto versijos](media/instruction-guides-RouteVersionAddGuide.png "Vadovo pridėjimas prie maršruto versijos")</span><span class="sxs-lookup"><span data-stu-id="d862c-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="d862c-337">Vadovo susiejimas su maršruto operacijų ryšiu</span><span class="sxs-lookup"><span data-stu-id="d862c-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="d862c-338">Vadovą galite pridėti prie bet kurio [maršruto operacijų ryšio](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="d862c-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="d862c-339">Tipinis scenarijus naudojant maršruto operacijų ryšius</span><span class="sxs-lookup"><span data-stu-id="d862c-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="d862c-340">Operacijų ryšiai yra konkretus būdas, leidžiantis įtraukti rekomendacijas į produkto procesą ir susijusias operacijas.</span><span class="sxs-lookup"><span data-stu-id="d862c-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="d862c-341">Galite nurodyti kiekvienos maršruto operacijos rekomendacijas bei nurodyti skirtingas rekomendacijas bet kuriam sukonfigūruotam maršruto ryšio kontekstui, pvz., konkrečioms prekėms, konfigūracijoms ir pan.</span><span class="sxs-lookup"><span data-stu-id="d862c-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="d862c-342">Taip pat galite nurodyti, kuriems operacijos etapams taikomos rekomendacijos (pvz., nustatymas, eilių sudarymas, apdorojimas arba gabenimas).</span><span class="sxs-lookup"><span data-stu-id="d862c-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="d862c-343">Jei vadovus nurodysite keliams maršruto operacijų ryšiams, iš šių vadovų ceche sugeneruotai užduočiai bus rodomas tik vienas tiksliausio ryšio vadovas.</span><span class="sxs-lookup"><span data-stu-id="d862c-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="d862c-344">Vadovo pridėjimas prie maršruto operacijų ryšio</span><span class="sxs-lookup"><span data-stu-id="d862c-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="d862c-345">Norėdami pridėti vadovą prie maršruto operacijų ryšio:</span><span class="sxs-lookup"><span data-stu-id="d862c-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="d862c-346">Eikite į **Gamybos kontrolė \> Visi maršrutai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="d862c-347">Atidarykite maršrutą, kuriam norite priskirti vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="d862c-348">Veiksmų srityje atidarykite skirtuką **Maršrutas** ir grupėje **Tvarkyti** pasirinkite **Maršruto informacija**.</span><span class="sxs-lookup"><span data-stu-id="d862c-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="d862c-349">Atidaromas pasirinkto maršruto puslapis **Maršruto informacija**.</span><span class="sxs-lookup"><span data-stu-id="d862c-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="d862c-350">Viršutiniame tinklelyje pasirinkite operaciją, su kuria susijusias rekomendacijas norite teikti.</span><span class="sxs-lookup"><span data-stu-id="d862c-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="d862c-351">Apatiniame tinklelyje pasirinkite konkretų ryšį (arba bendrąjį ryšį **Visi**).</span><span class="sxs-lookup"><span data-stu-id="d862c-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="d862c-352">![Pasirinkite operaciją, o tada ryšį](media/instruction-guides-RouteOperationRelation.png "Pasirinkite operaciją, o tada ryšį")</span><span class="sxs-lookup"><span data-stu-id="d862c-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="d862c-353">Virš apatinio tinklelio atsidarykite skirtuką **Susiję vadovai**.  ![Skirtukas Susiję vadovai](media/instruction-guides-RouteOperationRelation-AddGuide.png "Skirtukas Susiję vadovai")</span><span class="sxs-lookup"><span data-stu-id="d862c-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="d862c-354">Apatinio tinklelio viršuje pasirinkite **Įtraukti**, kad į tinklelį įtrauktumėte naują liniją.</span><span class="sxs-lookup"><span data-stu-id="d862c-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="d862c-355">Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.</span><span class="sxs-lookup"><span data-stu-id="d862c-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="d862c-356">Likusioje eilutės dalyje pažymėkite kiekvieno konteksto, kuriame turi būti prieinamas pasirinktas vadovas, žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="d862c-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="d862c-357">Kiekvienam operacijos etapui galite pridėti vieną ar daugiau vadovų.</span><span class="sxs-lookup"><span data-stu-id="d862c-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="d862c-358">Vadovų pasirinkimas iš cecho vykdymo sąsajos</span><span class="sxs-lookup"><span data-stu-id="d862c-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="d862c-359">Kai darbuotojas atidaro užduočių sąrašą cecho vykdymo sąsajoje, „Supply Chain Management“ randa atitinkamus vadovus rodomoms užduotims.</span><span class="sxs-lookup"><span data-stu-id="d862c-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="d862c-360">Norėdami peržiūrėti atitinkamus vadovus, naudokite mygtuką **Vadovai**.</span><span class="sxs-lookup"><span data-stu-id="d862c-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="d862c-361">![Vadovų mygtukas cecho vykdymo sąsajoje](media/instruction-guides-Shopfloor1.png "Vadovų mygtukas cecho vykdymo sąsajoje")</span><span class="sxs-lookup"><span data-stu-id="d862c-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="d862c-362">Tada pasiruoškite „HoloLens“ ir pasiekite atitinkamą vadovą nukreipdami į QR kodą ir suaktyvindami atitinkamą vadovą.</span><span class="sxs-lookup"><span data-stu-id="d862c-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="d862c-363">![QR kodas, skirtas prieigai prie vadovų naudojant „HoloLens“](media/instruction-guides-Shopfloor2.png "QR kodas, skirtas prieigai prie vadovų naudojant „HoloLens“")</span><span class="sxs-lookup"><span data-stu-id="d862c-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="d862c-364">Vadovų pasirinkimo logikos sprendimas</span><span class="sxs-lookup"><span data-stu-id="d862c-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="d862c-365">Vadovus galite pridėti vadovus prie šių gamybos duomenų:</span><span class="sxs-lookup"><span data-stu-id="d862c-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="d862c-366">Ištekliai</span><span class="sxs-lookup"><span data-stu-id="d862c-366">Resources</span></span>](#resources)
- [<span data-ttu-id="d862c-367">Išteklių grupės</span><span class="sxs-lookup"><span data-stu-id="d862c-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="d862c-368">Patvirtinti produktai</span><span class="sxs-lookup"><span data-stu-id="d862c-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="d862c-369">Formulės</span><span class="sxs-lookup"><span data-stu-id="d862c-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="d862c-370">Formulės versijos</span><span class="sxs-lookup"><span data-stu-id="d862c-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="d862c-371">Komplektavimo specifikacijos (KS)</span><span class="sxs-lookup"><span data-stu-id="d862c-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="d862c-372">KS versijos</span><span class="sxs-lookup"><span data-stu-id="d862c-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="d862c-373">Maršrutai</span><span class="sxs-lookup"><span data-stu-id="d862c-373">Routes</span></span>](#routes)
- [<span data-ttu-id="d862c-374">Maršruto versijos</span><span class="sxs-lookup"><span data-stu-id="d862c-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="d862c-375">Įprastų operacijų ryšiai</span><span class="sxs-lookup"><span data-stu-id="d862c-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="d862c-376">Kai „Supply Chain Management“ generuoja gamybos cecho užduotis, iš šių šaltinių surenkami atitinkami vadovai.</span><span class="sxs-lookup"><span data-stu-id="d862c-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="d862c-377">Atkreipkite dėmesį į toliau pateiktas svarbias taisykles.</span><span class="sxs-lookup"><span data-stu-id="d862c-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="d862c-378">Jei prie maršruto ar gamybos užsakymo pridedate KS versiją arba formulės versiją, tada užduotyje bus rodomi visi vadovai, pridėti prie šios versijos, ir vadovai, pridėti prie pirminės KS arba versijos formulės.</span><span class="sxs-lookup"><span data-stu-id="d862c-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="d862c-379">Jei prie gamybos užsakymo pridedate maršruto versiją, tada užduotyje bus rodomi visi vadovai, pridėti prie šios versijos, ir vadovai, pridėti prie pirminio versijos maršruto.</span><span class="sxs-lookup"><span data-stu-id="d862c-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="d862c-380">Jei nurodysite kelis maršruto operacijų ryšius, apimančius ryšį *Visi*, ir jiems priskirsite vadovus, užduotyje bus rodomi tik labiausiai specifinio ryšio vadovai.</span><span class="sxs-lookup"><span data-stu-id="d862c-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="d862c-381">![Atitinkamų vadovų sprendimo diagrama](media/instruction-guides-Resolve.png "Atitinkamų vadovų sprendimo diagrama")</span><span class="sxs-lookup"><span data-stu-id="d862c-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>
