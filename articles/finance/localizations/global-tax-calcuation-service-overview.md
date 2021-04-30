---
title: Mokesčių skaičiavimas (peržiūros versija)
description: Šioje temoje paaiškinama bendroji Mokesčių skaičiavimo galimybės apimtis ir funkcijos.
author: wangchen
ms.date: 04/12/2021
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
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892354"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="11503-103">Mokesčių skaičiavimas (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="11503-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="11503-104">Mokesčių skaičiavimas yra hiper išplečiama kelių nuomotojų paslauga, įgalinanti „Global Tax Engine“ automatizuoti ir supaprastinti mokesčių nustatymo ir skaičiavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="11503-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="11503-105">Visiškai konfigūruotinas mokesčių modulis.</span><span class="sxs-lookup"><span data-stu-id="11503-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="11503-106">Elementai, kuriuos galima konfigūruoti, apima (bet tuo neapsiribojama) apmokestinamą duomenų modelį, mokesčio kodą, mokesčių taikomumo matricą ir mokesčių skaičiavimo formulę.</span><span class="sxs-lookup"><span data-stu-id="11503-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="11503-107">Mokesčių sistema veikia pagrindinių paslaugų „Microsoft Azure“ platformoje ir siūlo modernias technologiją bei proporcingai keičiamumą.</span><span class="sxs-lookup"><span data-stu-id="11503-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="11503-108">Mokesčių skaičiavimas integruojamas su „Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="11503-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="11503-109">Galiausiai ji taip pat bus „Dynamics 365 Project Operations“ integruota į, ir kitas pirmosios šalies ir trečiosios šalies „Dynamics 365 Commerce“ programas.</span><span class="sxs-lookup"><span data-stu-id="11503-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="11503-110">Mokesčių skaičiavimas yra mikrotarnyba pagrįstas mokesčių variklis, siūlantis eksponentinį išplečiamumą.</span><span class="sxs-lookup"><span data-stu-id="11503-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="11503-111">Galite atlikti šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="11503-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="11503-112">Konfigūruokite Mokesčių skaičiavimą per „Regulatory Configuration Service“ (RCS).</span><span class="sxs-lookup"><span data-stu-id="11503-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="11503-113">RCS yra patobulinta elektroninių ataskaitų (ER) dizaino įrankio versija, galima naudoti kaip atskirą paslaugą.</span><span class="sxs-lookup"><span data-stu-id="11503-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="11503-114">Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatyti mokesčių kodai ir tarifai.</span><span class="sxs-lookup"><span data-stu-id="11503-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="11503-115">Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatytas registracijos numeris.</span><span class="sxs-lookup"><span data-stu-id="11503-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="11503-116">Konfigūruokite mokesčių skaičiavimo konstruktorių, kad būtų galima apibrėžti formules ir sąlygas.</span><span class="sxs-lookup"><span data-stu-id="11503-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="11503-117">Juridiniuose subjektuose bendrai naudoti mokesčių nustatymo ir skaičiavimo sprendimą.</span><span class="sxs-lookup"><span data-stu-id="11503-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="11503-118">Norėdami naudoti mokesčių skaičiavimo tarnybą, įdiekite mokesčių skaičiavimo tarnybos priedą iš ciklo tarnybų „Microsoft Dynamics Lifecycle Services“ (LCS) projekto.</span><span class="sxs-lookup"><span data-stu-id="11503-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="11503-119">Tada užbaikite RCS nustatymą ir įjunkite mokesčių skaičiavimo paslaugą „Finance and Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="11503-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="11503-120">Daugiau informacijos žr. [Darbo su mokesčių paslaugų pradžia](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="11503-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="11503-121">Prieinamumas</span><span class="sxs-lookup"><span data-stu-id="11503-121">Availability</span></span>

<span data-ttu-id="11503-122">Mokesčių skaičiavimas galimas tik smėlio dėžės aplinkose ir tik pasirinktiems klientams, naudojant viešosios peržiūros versijos programą.</span><span class="sxs-lookup"><span data-stu-id="11503-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="11503-123">Galiausiai ji bus bendrai pasiekiama visiems klientams ir gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="11503-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="11503-124">Atsiras vis naujos funkcijas, tad nepamirškite dažnai peržvelgti naujausią dokumentaciją, kad sužinotumėte apie palaikomų funkcijų padengimą ir aprėptį.</span><span class="sxs-lookup"><span data-stu-id="11503-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="11503-125">Mokesčių skaičiavimas yra įdiegtas toliau nurodytose „Azure" geografinėse srityse.</span><span class="sxs-lookup"><span data-stu-id="11503-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="11503-126">Ji taip pat bus įdiegta į daugiau „Azure" geografinių diagramų, atsižvelgiant į kliento poreikius:</span><span class="sxs-lookup"><span data-stu-id="11503-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="11503-127">Jungtinės Valstijos</span><span class="sxs-lookup"><span data-stu-id="11503-127">United States</span></span>
- <span data-ttu-id="11503-128">Europa</span><span class="sxs-lookup"><span data-stu-id="11503-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="11503-129">Mokesčių skaičiavimas nepalaiko „Dynamics 365" vietinių diegimų.</span><span class="sxs-lookup"><span data-stu-id="11503-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="11503-130">Tai nepalaiko ir ankstesnių versijų, pvz., „Dynamics AX 2012".</span><span class="sxs-lookup"><span data-stu-id="11503-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="11503-131">Svarbiausi funkcijų aspektai</span><span class="sxs-lookup"><span data-stu-id="11503-131">Feature highlights</span></span>

- <span data-ttu-id="11503-132">Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatyti mokesčių kodai ir tarifai.</span><span class="sxs-lookup"><span data-stu-id="11503-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="11503-133">Kelių mokesčių registracijos numerių palaikymas</span><span class="sxs-lookup"><span data-stu-id="11503-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="11503-134">Perkėlimo užsakymo palaikymas nustatant mokesčius ir skaičiuojant</span><span class="sxs-lookup"><span data-stu-id="11503-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="11503-135">Perkėlimo užsakymo palaikymas nustatant kelių mokesčių registracijos numerius</span><span class="sxs-lookup"><span data-stu-id="11503-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="11503-136">Palaikomos operacijos</span><span class="sxs-lookup"><span data-stu-id="11503-136">Supported transactions</span></span>

<span data-ttu-id="11503-137">Mokesčių skaičiavimą gali įgalinti juridinis subjektas ir operacija.</span><span class="sxs-lookup"><span data-stu-id="11503-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="11503-138">Palaikomos toliau nurodytos operacijos:</span><span class="sxs-lookup"><span data-stu-id="11503-138">The following transactions are supported:</span></span>

- <span data-ttu-id="11503-139">Pardavimo procesas</span><span class="sxs-lookup"><span data-stu-id="11503-139">Sales process</span></span>

    - <span data-ttu-id="11503-140">Pardavimo pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="11503-140">Sales quotation</span></span>
    - <span data-ttu-id="11503-141">Pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="11503-141">Sales order</span></span>
    - <span data-ttu-id="11503-142">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="11503-142">Confirmation</span></span>
    - <span data-ttu-id="11503-143">Išrinkimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="11503-143">Picking list</span></span>
    - <span data-ttu-id="11503-144">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="11503-144">Packing slip</span></span>
    - <span data-ttu-id="11503-145">Pardavimo sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="11503-145">Sales invoice</span></span>
    - <span data-ttu-id="11503-146">Kredito sąskaita</span><span class="sxs-lookup"><span data-stu-id="11503-146">Credit note</span></span>
    - <span data-ttu-id="11503-147">Grąžinimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="11503-147">Return order</span></span>
    - <span data-ttu-id="11503-148">Antraštės įvairūs keitimai</span><span class="sxs-lookup"><span data-stu-id="11503-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="11503-149">Įvairių išlaidų eilutė</span><span class="sxs-lookup"><span data-stu-id="11503-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="11503-150">Pirkimo procesas</span><span class="sxs-lookup"><span data-stu-id="11503-150">Purchase process</span></span>

    - <span data-ttu-id="11503-151">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="11503-151">Purchase order</span></span>
    - <span data-ttu-id="11503-152">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="11503-152">Confirmation</span></span>
    - <span data-ttu-id="11503-153">Gavimų sąrašas</span><span class="sxs-lookup"><span data-stu-id="11503-153">Receipts list</span></span>
    - <span data-ttu-id="11503-154">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="11503-154">Product receipt</span></span>
    - <span data-ttu-id="11503-155">Pirkimo SF</span><span class="sxs-lookup"><span data-stu-id="11503-155">Purchase invoice</span></span>
    - <span data-ttu-id="11503-156">Antraštės įvairūs keitimai</span><span class="sxs-lookup"><span data-stu-id="11503-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="11503-157">Įvairių išlaidų eilutė</span><span class="sxs-lookup"><span data-stu-id="11503-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="11503-158">Kredito sąskaita</span><span class="sxs-lookup"><span data-stu-id="11503-158">Credit note</span></span>
    - <span data-ttu-id="11503-159">Grąžinimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="11503-159">Return order</span></span>
    - <span data-ttu-id="11503-160">Pirkimo paraiška</span><span class="sxs-lookup"><span data-stu-id="11503-160">Purchase requisition</span></span>
    - <span data-ttu-id="11503-161">Papildomos pirkimo paraiškos eilutės išlaidos</span><span class="sxs-lookup"><span data-stu-id="11503-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="11503-162">Pasiūlymo patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="11503-162">Request for quotation</span></span>
    - <span data-ttu-id="11503-163">Pasiūlymo patvirtinimo antraštės papildomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="11503-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="11503-164">Pasiūlymo patvirtinimo eilutės papildomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="11503-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="11503-165">Atsargų procesas</span><span class="sxs-lookup"><span data-stu-id="11503-165">Inventory process</span></span>

    - <span data-ttu-id="11503-166">Perlaidos užsakymas - siuntimas</span><span class="sxs-lookup"><span data-stu-id="11503-166">Transfer order – ship</span></span>
    - <span data-ttu-id="11503-167">Perlaidos užsakymas - gavimas</span><span class="sxs-lookup"><span data-stu-id="11503-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="11503-168">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="11503-168">Related resources</span></span>

[<span data-ttu-id="11503-169">Darbo su mokesčių paslaugomi pradžia</span><span class="sxs-lookup"><span data-stu-id="11503-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="11503-170">Kelių PVM registracijų numeris</span><span class="sxs-lookup"><span data-stu-id="11503-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="11503-171">Mokesčių priemonės perkėlimo užsakymo palaikymas</span><span class="sxs-lookup"><span data-stu-id="11503-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="11503-172">Kaip sukurti plėtinį mokesčių tarnybose</span><span class="sxs-lookup"><span data-stu-id="11503-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)