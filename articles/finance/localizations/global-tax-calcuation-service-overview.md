---
title: Mokesčių skaičiavimas (peržiūros versija)
description: Šioje temoje paaiškinama bendroji Mokesčių skaičiavimo galimybės apimtis ir funkcijos.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184106"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="6cdcd-103">Mokesčių skaičiavimas (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="6cdcd-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="6cdcd-104">Mokesčių skaičiavimas yra hiper išplečiama kelių nuomotojų paslauga, įgalinanti „Global Tax Engine“ automatizuoti ir supaprastinti mokesčių nustatymo ir skaičiavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="6cdcd-105">Visiškai konfigūruotinas mokesčių modulis.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="6cdcd-106">Elementai, kuriuos galima konfigūruoti, apima (bet tuo neapsiribojama) apmokestinamą duomenų modelį, mokesčio kodą, mokesčių taikomumo matricą ir mokesčių skaičiavimo formulę.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="6cdcd-107">Mokesčių sistema veikia pagrindinių paslaugų „Microsoft Azure“ platformoje ir siūlo modernias technologiją bei proporcingai keičiamumą.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="6cdcd-108">Mokesčių skaičiavimas integruojamas su „Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6cdcd-109">Galiausiai ji taip pat bus „Dynamics 365 Project Operations“ integruota į, ir kitas pirmosios šalies ir trečiosios šalies „Dynamics 365 Commerce“ programas.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6cdcd-110">Kai įgalinate mokesčių skaičiavimo tarnybą, kai kurios su susijusiais duomenimis susijusios operacijos gali būti atliekamos ne duomenų centre, kuris prižiūri jūsų aptarnavimo duomenis.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="6cdcd-111">Prieš [įgalindami mokesčių](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) skaičiavimo tarnybą, peržiūrėkite sąlygas.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="6cdcd-112">Mes rūpinamės jūsų privatumu.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-112">Your privacy is important to us.</span></span> <span data-ttu-id="6cdcd-113">Norėdami sužinoti daugiau, perskaitykite mūsų [Pareiškimą dėl privatumo](https://go.microsoft.com/fwlink/?LinkId=521839).</span><span class="sxs-lookup"><span data-stu-id="6cdcd-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="6cdcd-114">Mokesčių skaičiavimas yra mikrotarnyba pagrįstas mokesčių variklis, siūlantis eksponentinį išplečiamumą.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="6cdcd-115">Galite atlikti šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="6cdcd-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="6cdcd-116">Konfigūruokite Mokesčių skaičiavimą per „Regulatory Configuration Service“ (RCS).</span><span class="sxs-lookup"><span data-stu-id="6cdcd-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="6cdcd-117">RCS yra patobulinta elektroninių ataskaitų (ER) dizaino įrankio versija, galima naudoti kaip atskirą paslaugą.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="6cdcd-118">Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatyti mokesčių kodai ir tarifai.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="6cdcd-119">Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatytas registracijos numeris.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="6cdcd-120">Konfigūruokite mokesčių skaičiavimo konstruktorių, kad būtų galima apibrėžti formules ir sąlygas.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="6cdcd-121">Juridiniuose subjektuose bendrai naudoti mokesčių nustatymo ir skaičiavimo sprendimą.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="6cdcd-122">Norėdami naudoti mokesčių skaičiavimo tarnybą, įdiekite mokesčių skaičiavimo tarnybos priedą iš ciklo tarnybų „Microsoft Dynamics Lifecycle Services“ (LCS) projekto.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="6cdcd-123">Tada užbaikite RCS nustatymą ir įjunkite mokesčių skaičiavimo paslaugą „Finance and Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="6cdcd-124">Daugiau informacijos žr. [Darbo su mokesčių paslaugų pradžia](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="6cdcd-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="6cdcd-125">Prieinamumas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-125">Availability</span></span>

<span data-ttu-id="6cdcd-126">Mokesčių skaičiavimas galimas tik smėlio dėžės aplinkose ir tik pasirinktiems klientams, naudojant viešosios peržiūros versijos programą.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="6cdcd-127">Galiausiai ji bus bendrai pasiekiama visiems klientams ir gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="6cdcd-128">Atsiras vis naujos funkcijas, tad nepamirškite dažnai peržvelgti naujausią dokumentaciją, kad sužinotumėte apie palaikomų funkcijų padengimą ir aprėptį.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="6cdcd-129">Mokesčių skaičiavimas yra įdiegtas toliau nurodytose „Azure" geografinėse srityse.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="6cdcd-130">Ji taip pat bus įdiegta į daugiau „Azure" geografinių diagramų, atsižvelgiant į kliento poreikius:</span><span class="sxs-lookup"><span data-stu-id="6cdcd-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="6cdcd-131">Jungtinės Valstijos</span><span class="sxs-lookup"><span data-stu-id="6cdcd-131">United States</span></span>
- <span data-ttu-id="6cdcd-132">Europa</span><span class="sxs-lookup"><span data-stu-id="6cdcd-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="6cdcd-133">Mokesčių skaičiavimas nepalaiko „Dynamics 365" vietinių diegimų.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="6cdcd-134">Tai nepalaiko ir ankstesnių versijų, pvz., „Dynamics AX 2012".</span><span class="sxs-lookup"><span data-stu-id="6cdcd-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="6cdcd-135">Svarbiausi funkcijų aspektai</span><span class="sxs-lookup"><span data-stu-id="6cdcd-135">Feature highlights</span></span>

- <span data-ttu-id="6cdcd-136">Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatyti mokesčių kodai ir tarifai.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="6cdcd-137">Kelių mokesčių registracijos numerių palaikymas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="6cdcd-138">Perkėlimo užsakymo palaikymas nustatant mokesčius ir skaičiuojant</span><span class="sxs-lookup"><span data-stu-id="6cdcd-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="6cdcd-139">Perkėlimo užsakymo palaikymas nustatant kelių mokesčių registracijos numerius</span><span class="sxs-lookup"><span data-stu-id="6cdcd-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="6cdcd-140">Palaikomos operacijos</span><span class="sxs-lookup"><span data-stu-id="6cdcd-140">Supported transactions</span></span>

<span data-ttu-id="6cdcd-141">Mokesčių skaičiavimą gali įgalinti juridinis subjektas ir operacija.</span><span class="sxs-lookup"><span data-stu-id="6cdcd-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="6cdcd-142">Palaikomos toliau nurodytos operacijos:</span><span class="sxs-lookup"><span data-stu-id="6cdcd-142">The following transactions are supported:</span></span>

- <span data-ttu-id="6cdcd-143">Pardavimo procesas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-143">Sales process</span></span>

    - <span data-ttu-id="6cdcd-144">Pardavimo pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-144">Sales quotation</span></span>
    - <span data-ttu-id="6cdcd-145">Pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-145">Sales order</span></span>
    - <span data-ttu-id="6cdcd-146">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-146">Confirmation</span></span>
    - <span data-ttu-id="6cdcd-147">Išrinkimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-147">Picking list</span></span>
    - <span data-ttu-id="6cdcd-148">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="6cdcd-148">Packing slip</span></span>
    - <span data-ttu-id="6cdcd-149">Pardavimo sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="6cdcd-149">Sales invoice</span></span>
    - <span data-ttu-id="6cdcd-150">Kredito sąskaita</span><span class="sxs-lookup"><span data-stu-id="6cdcd-150">Credit note</span></span>
    - <span data-ttu-id="6cdcd-151">Grąžinimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-151">Return order</span></span>
    - <span data-ttu-id="6cdcd-152">Antraštės įvairūs keitimai</span><span class="sxs-lookup"><span data-stu-id="6cdcd-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="6cdcd-153">Įvairių išlaidų eilutė</span><span class="sxs-lookup"><span data-stu-id="6cdcd-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="6cdcd-154">Pirkimo procesas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-154">Purchase process</span></span>

    - <span data-ttu-id="6cdcd-155">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-155">Purchase order</span></span>
    - <span data-ttu-id="6cdcd-156">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-156">Confirmation</span></span>
    - <span data-ttu-id="6cdcd-157">Gavimų sąrašas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-157">Receipts list</span></span>
    - <span data-ttu-id="6cdcd-158">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-158">Product receipt</span></span>
    - <span data-ttu-id="6cdcd-159">Pirkimo SF</span><span class="sxs-lookup"><span data-stu-id="6cdcd-159">Purchase invoice</span></span>
    - <span data-ttu-id="6cdcd-160">Antraštės įvairūs keitimai</span><span class="sxs-lookup"><span data-stu-id="6cdcd-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="6cdcd-161">Įvairių išlaidų eilutė</span><span class="sxs-lookup"><span data-stu-id="6cdcd-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="6cdcd-162">Kredito sąskaita</span><span class="sxs-lookup"><span data-stu-id="6cdcd-162">Credit note</span></span>
    - <span data-ttu-id="6cdcd-163">Grąžinimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-163">Return order</span></span>
    - <span data-ttu-id="6cdcd-164">Pirkimo paraiška</span><span class="sxs-lookup"><span data-stu-id="6cdcd-164">Purchase requisition</span></span>
    - <span data-ttu-id="6cdcd-165">Papildomos pirkimo paraiškos eilutės išlaidos</span><span class="sxs-lookup"><span data-stu-id="6cdcd-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="6cdcd-166">Pasiūlymo patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-166">Request for quotation</span></span>
    - <span data-ttu-id="6cdcd-167">Pasiūlymo patvirtinimo antraštės papildomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="6cdcd-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="6cdcd-168">Pasiūlymo patvirtinimo eilutės papildomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="6cdcd-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="6cdcd-169">Atsargų procesas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-169">Inventory process</span></span>

    - <span data-ttu-id="6cdcd-170">Perlaidos užsakymas - siuntimas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-170">Transfer order – ship</span></span>
    - <span data-ttu-id="6cdcd-171">Perlaidos užsakymas - gavimas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="6cdcd-172">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="6cdcd-172">Related resources</span></span>

[<span data-ttu-id="6cdcd-173">Darbo su mokesčių paslaugomi pradžia</span><span class="sxs-lookup"><span data-stu-id="6cdcd-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="6cdcd-174">Kelių PVM registracijų numeris</span><span class="sxs-lookup"><span data-stu-id="6cdcd-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="6cdcd-175">Mokesčių priemonės perkėlimo užsakymo palaikymas</span><span class="sxs-lookup"><span data-stu-id="6cdcd-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="6cdcd-176">Kaip sukurti plėtinį mokesčių tarnybose</span><span class="sxs-lookup"><span data-stu-id="6cdcd-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
