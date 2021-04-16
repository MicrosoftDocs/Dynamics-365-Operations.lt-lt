---
title: Mokesčių skaičiavimo paslauga (peržiūros versija)
description: Šioje temoje paaiškinama bendroji mokesčių skaičiavimo tarnybos apimtis ir funkcijos.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818229"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="5d7f6-103">Mokesčių skaičiavimo paslauga (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="5d7f6-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="5d7f6-104">Mokesčių skaičiavimo tarnyba yra hyper-scalable multitenant paslauga, kuri leidžia „Global Tax Engine“ automatizuoti ir supaprastinti mokesčių nustatymo ir skaičiavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="5d7f6-105">Visiškai konfigūruotinas mokesčių modulis.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="5d7f6-106">Elementai, kuriuos galima konfigūruoti, apima (bet tuo neapsiribojama) apmokestinamą duomenų modelį, mokesčio kodą, mokesčių taikomumo matricą ir mokesčių skaičiavimo formulę.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="5d7f6-107">Mokesčių sistema veikia pagrindinių paslaugų „Microsoft Azure“ platformoje ir siūlo modernias technologiją bei proporcingai keičiamumą.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="5d7f6-108">Mokesčių skaičiavimo tarnyba integruojama su „Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5d7f6-109">Galiausiai ji taip pat bus „Dynamics 365 Project Operations“ integruota į, ir kitas pirmosios šalies ir trečiosios šalies „Dynamics 365 Commerce“ programas.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="5d7f6-110">Mokesčių skaičiavimo tarnyba yra „Microsoft" mokesčių sistema, kuri siūlo proporcingai keičiamumą.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="5d7f6-111">Galite atlikti šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="5d7f6-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="5d7f6-112">Konfigūruokite mokesčių skaičiavimo tarnybą per „Regulatory Configuration Service“ (RCS).</span><span class="sxs-lookup"><span data-stu-id="5d7f6-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="5d7f6-113">RCS yra patobulinta elektroninių ataskaitų (ER) dizaino įrankio versija, galima naudoti kaip atskirą paslaugą.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="5d7f6-114">Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatyti mokesčių kodai ir tarifai.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="5d7f6-115">Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatytas registracijos numeris.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="5d7f6-116">Konfigūruokite mokesčių skaičiavimo konstruktorių, kad būtų galima apibrėžti formules ir sąlygas.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="5d7f6-117">Juridiniuose subjektuose bendrai naudoti mokesčių nustatymo ir skaičiavimo sprendimą.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="5d7f6-118">Norėdami naudoti mokesčių skaičiavimo tarnybą, įdiekite mokesčių skaičiavimo tarnybos priedą iš ciklo tarnybų „Microsoft Dynamics Lifecycle Services“ (LCS) projekto.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5d7f6-119">Tada užbaikite RCS nustatymą ir įjunkite mokesčių skaičiavimo paslaugą „Finance and Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="5d7f6-120">Daugiau informacijos žr. [Darbo su mokesčių paslaugų pradžia](https://go.microsoft.com/fwlink/?linkid=2138482).</span><span class="sxs-lookup"><span data-stu-id="5d7f6-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="5d7f6-121">Prieinamumas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-121">Availability</span></span>

<span data-ttu-id="5d7f6-122">Mokesčių skaičiavimo paslauga galima tik sandų saugyklos aplinkose ir pasirinktiems klientams, naudojant viešąją peržiūros programą.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="5d7f6-123">Galiausiai ji bus bendrai pasiekiama visiems klientams ir gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="5d7f6-124">Naujos priemonės ir toliau bus pristatytos mokesčių skaičiavimo paslaugoje.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="5d7f6-125">Todėl nepamirškite dažnai patikrinti naujausiais dokumentais, kad sužinotumėte apie palaikomų funkcijų padengimą ir aprėptį.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="5d7f6-126">Mokesčių skaičiavimo paslauga įdiegiama toliau nurodytose „Azure" geografinėse diagramose.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="5d7f6-127">Ji taip pat bus įdiegta į daugiau „Azure" geografinių diagramų, atsižvelgiant į kliento poreikius:</span><span class="sxs-lookup"><span data-stu-id="5d7f6-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="5d7f6-128">Jungtinės Valstijos</span><span class="sxs-lookup"><span data-stu-id="5d7f6-128">United States</span></span>
- <span data-ttu-id="5d7f6-129">Europa</span><span class="sxs-lookup"><span data-stu-id="5d7f6-129">Europe</span></span>
- <span data-ttu-id="5d7f6-130">Prancūzija</span><span class="sxs-lookup"><span data-stu-id="5d7f6-130">France</span></span>
- <span data-ttu-id="5d7f6-131">Jungtinė Karalystė</span><span class="sxs-lookup"><span data-stu-id="5d7f6-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="5d7f6-132">Mokesčių skaičiavimo tarnyba nepalaiko „Dynamics 365" vietinio diegimo.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="5d7f6-133">Tai nepalaiko ir ankstesnių versijų, pvz., „Dynamics AX 2012".</span><span class="sxs-lookup"><span data-stu-id="5d7f6-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="5d7f6-134">Svarbiausi funkcijų aspektai</span><span class="sxs-lookup"><span data-stu-id="5d7f6-134">Feature highlights</span></span>

- <span data-ttu-id="5d7f6-135">Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatyti mokesčių kodai ir tarifai.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="5d7f6-136">Kelių pridėtinės vertės mokesčio (PVM) registracijos numerių palaikymas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="5d7f6-137">Perkėlimo užsakymo palaikymas nustatant mokesčius ir skaičiuojant</span><span class="sxs-lookup"><span data-stu-id="5d7f6-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="5d7f6-138">Perkėlimo užsakymo palaikymas nustatant keletą PVM registracijos numerių</span><span class="sxs-lookup"><span data-stu-id="5d7f6-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="5d7f6-139">Palaikomos operacijos</span><span class="sxs-lookup"><span data-stu-id="5d7f6-139">Supported transactions</span></span>

<span data-ttu-id="5d7f6-140">Mokesčių skaičiavimo paslauga gali būti įgalinta juridinio subjekto ir operacijos.</span><span class="sxs-lookup"><span data-stu-id="5d7f6-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="5d7f6-141">Palaikomos toliau nurodytos operacijos:</span><span class="sxs-lookup"><span data-stu-id="5d7f6-141">The following transactions are supported:</span></span>

- <span data-ttu-id="5d7f6-142">Pardavimo procesas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-142">Sales process</span></span>

    - <span data-ttu-id="5d7f6-143">Pardavimo pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-143">Sales quotation</span></span>
    - <span data-ttu-id="5d7f6-144">Pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-144">Sales order</span></span>
    - <span data-ttu-id="5d7f6-145">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-145">Confirmation</span></span>
    - <span data-ttu-id="5d7f6-146">Išrinkimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-146">Picking list</span></span>
    - <span data-ttu-id="5d7f6-147">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="5d7f6-147">Packing slip</span></span>
    - <span data-ttu-id="5d7f6-148">Pardavimo sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="5d7f6-148">Sales invoice</span></span>
    - <span data-ttu-id="5d7f6-149">Kredito sąskaita</span><span class="sxs-lookup"><span data-stu-id="5d7f6-149">Credit note</span></span>
    - <span data-ttu-id="5d7f6-150">Grąžinimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-150">Return order</span></span>
    - <span data-ttu-id="5d7f6-151">Antraštės įvairūs keitimai</span><span class="sxs-lookup"><span data-stu-id="5d7f6-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="5d7f6-152">Įvairių išlaidų eilutė</span><span class="sxs-lookup"><span data-stu-id="5d7f6-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="5d7f6-153">Pirkimo procesas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-153">Purchase process</span></span>

    - <span data-ttu-id="5d7f6-154">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-154">Purchase order</span></span>
    - <span data-ttu-id="5d7f6-155">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-155">Confirmation</span></span>
    - <span data-ttu-id="5d7f6-156">Gavimų sąrašas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-156">Receipts list</span></span>
    - <span data-ttu-id="5d7f6-157">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-157">Product receipt</span></span>
    - <span data-ttu-id="5d7f6-158">Pirkimo SF</span><span class="sxs-lookup"><span data-stu-id="5d7f6-158">Purchase invoice</span></span>
    - <span data-ttu-id="5d7f6-159">Antraštės įvairūs keitimai</span><span class="sxs-lookup"><span data-stu-id="5d7f6-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="5d7f6-160">Įvairių išlaidų eilutė</span><span class="sxs-lookup"><span data-stu-id="5d7f6-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="5d7f6-161">Kredito sąskaita</span><span class="sxs-lookup"><span data-stu-id="5d7f6-161">Credit note</span></span>
    - <span data-ttu-id="5d7f6-162">Grąžinimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-162">Return order</span></span>
    - <span data-ttu-id="5d7f6-163">Pirkimo paraiška</span><span class="sxs-lookup"><span data-stu-id="5d7f6-163">Purchase requisition</span></span>
    - <span data-ttu-id="5d7f6-164">Papildomos pirkimo paraiškos eilutės išlaidos</span><span class="sxs-lookup"><span data-stu-id="5d7f6-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="5d7f6-165">Pasiūlymo patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-165">Request for quotation</span></span>
    - <span data-ttu-id="5d7f6-166">Pasiūlymo patvirtinimo antraštės papildomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="5d7f6-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="5d7f6-167">Pasiūlymo patvirtinimo eilutės papildomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="5d7f6-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="5d7f6-168">Atsargų procesas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-168">Inventory process</span></span>

    - <span data-ttu-id="5d7f6-169">Perlaidos užsakymas - siuntimas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-169">Transfer order – ship</span></span>
    - <span data-ttu-id="5d7f6-170">Perlaidos užsakymas - gavimas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="5d7f6-171">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="5d7f6-171">Related resources</span></span>

[<span data-ttu-id="5d7f6-172">Darbo su mokesčių paslaugomi pradžia</span><span class="sxs-lookup"><span data-stu-id="5d7f6-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="5d7f6-173">Kelių PVM registracijų numeris</span><span class="sxs-lookup"><span data-stu-id="5d7f6-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="5d7f6-174">Mokesčių priemonės perkėlimo užsakymo palaikymas</span><span class="sxs-lookup"><span data-stu-id="5d7f6-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="5d7f6-175">Kaip sukurti plėtinį mokesčių tarnybose</span><span class="sxs-lookup"><span data-stu-id="5d7f6-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
