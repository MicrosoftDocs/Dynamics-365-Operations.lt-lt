---
title: Dvigubo rašymo apžvalga
description: Šioje temoje pateikiama dvigubo rašymo apžvalga. Dvigubas rašymas yra infrastruktūra, kuri beveik realiuoju laiku teikia sąveiką tarp „Microsoft Dynamics 365” modeliu pagrįstų programų ir „Finance and Operations” programų.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 12c6a39700a260c138fab67ed370f94b3aa04213
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/20/2020
ms.locfileid: "3075995"
---
# <a name="dual-write-overview"></a><span data-ttu-id="f25ac-104">Dvigubo rašymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="f25ac-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a><span data-ttu-id="f25ac-105">Kas yra dvigubas rašymas?</span><span class="sxs-lookup"><span data-stu-id="f25ac-105">What is dual-write?</span></span>

<span data-ttu-id="f25ac-106">Dvigubas rašymas yra parengta naudoti infrastruktūra, kuri beveik realiuoju laiku teikia sąveiką tarp „Microsoft Dynamics 365” esančių modeliu pagrįstų programų ir „Finance and Operations” programų.</span><span class="sxs-lookup"><span data-stu-id="f25ac-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="f25ac-107">Kai duomenys apie klientus, produktus, žmones ir operacijas siunčiami už programos ribų, visiems organizacijos padaliniams suteikiami įgaliojimai.</span><span class="sxs-lookup"><span data-stu-id="f25ac-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="f25ac-108">Dvigubu rašymu pateikiama glaudžiai susieta, dvikryptė integracija tarp „Finance and Operations” programų ir „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="f25ac-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="f25ac-109">Bet kokie duomenų keitimai, vykdomi „Finance and Operations” programose, taip pat įrašomi į „Common Data Service”, o bet kokie „Common Data Service” duomenų keitimai yra įrašomi  „Finance and Operations” programose.</span><span class="sxs-lookup"><span data-stu-id="f25ac-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="f25ac-110">Šis automatizuotas duomenų srautas suteikia integruotą vartotojo patirtį susietose programose.</span><span class="sxs-lookup"><span data-stu-id="f25ac-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Duomenų ryšys tarp programų](media/dual-write-overview.jpg)

<span data-ttu-id="f25ac-112">Dvigubo rašymo aspektai yra du – *infrastruktūros* aspektas ir *programos* aspektas.</span><span class="sxs-lookup"><span data-stu-id="f25ac-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="f25ac-113">Infrastruktūra</span><span class="sxs-lookup"><span data-stu-id="f25ac-113">Infrastructure</span></span>

<span data-ttu-id="f25ac-114">Dvigubo rašymo infrastruktūra yra išplėstinė ir patikima, joje yra šios pagrindinės funkcijos:</span><span class="sxs-lookup"><span data-stu-id="f25ac-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="f25ac-115">Sinchroninis ir dvikryptis duomenų srautas tarp programų</span><span class="sxs-lookup"><span data-stu-id="f25ac-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="f25ac-116">Sinchronizavimas, kartu su atkūrimo, pristabdymo ir papildymo režimais, siekiant palaikyti sistemą internetiniu ir autonominiu / asinchroniniu režimais.</span><span class="sxs-lookup"><span data-stu-id="f25ac-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="f25ac-117">Galimybė sinchronizuoti pradinius duomenis tarp programų</span><span class="sxs-lookup"><span data-stu-id="f25ac-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="f25ac-118">Konsoliduotas veiklos rodinys ir duomenų administratorių klaidų žurnalas</span><span class="sxs-lookup"><span data-stu-id="f25ac-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="f25ac-119">Galimybė konfigūruoti pasirinktinius įspėjimus ir ribines vertes bei prenumeruoti pranešimus</span><span class="sxs-lookup"><span data-stu-id="f25ac-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="f25ac-120">Intuityviosios vartotojo sąsajos (UI) filtravimas ir transformacijos</span><span class="sxs-lookup"><span data-stu-id="f25ac-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="f25ac-121">Galimybė nustatyti ir peržiūrėti objekto priklausomybes ir ryšius</span><span class="sxs-lookup"><span data-stu-id="f25ac-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="f25ac-122">Ir standartinių, ir tinkintų objektų bei žemėlapių išplėtimas</span><span class="sxs-lookup"><span data-stu-id="f25ac-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="f25ac-123">Patikimas programos vykdymo ciklo valdymas</span><span class="sxs-lookup"><span data-stu-id="f25ac-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="f25ac-124">Naujo kliento iš anksto parengtos sąrankos funkcijos</span><span class="sxs-lookup"><span data-stu-id="f25ac-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="f25ac-125">Programos</span><span class="sxs-lookup"><span data-stu-id="f25ac-125">Application</span></span>

<span data-ttu-id="f25ac-126">Dvigubu rašymu sukuriamas susiejimas tarp sąvokų, esančių „Finance and Operations” programose, ir sąvokų, esančių „Dynamics 365” modeliu pagrįstų programų.</span><span class="sxs-lookup"><span data-stu-id="f25ac-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="f25ac-127">Ši integracija palaiko šiuos scenarijus:</span><span class="sxs-lookup"><span data-stu-id="f25ac-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="f25ac-128">Bendrieji integruoto kliento duomenys</span><span class="sxs-lookup"><span data-stu-id="f25ac-128">Integrated customer master</span></span>
+ <span data-ttu-id="f25ac-129">Prieiga prie kliento lojalumo kortelių ir atlygio taškų</span><span class="sxs-lookup"><span data-stu-id="f25ac-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="f25ac-130">Bendrojo produkto bendrosios funkcijos</span><span class="sxs-lookup"><span data-stu-id="f25ac-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="f25ac-131">Supratimas apie organizacijos hierarchiją</span><span class="sxs-lookup"><span data-stu-id="f25ac-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="f25ac-132">Bendrieji integruoto tiekėjo duomenys</span><span class="sxs-lookup"><span data-stu-id="f25ac-132">Integrated vendor master</span></span>
+ <span data-ttu-id="f25ac-133">Prieiga prie finansinių ir mokesčių nuorodos duomenų</span><span class="sxs-lookup"><span data-stu-id="f25ac-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="f25ac-134">Kainos pagal poreikį mechanizmo funkcijos</span><span class="sxs-lookup"><span data-stu-id="f25ac-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="f25ac-135">Integruotos potencialių klientų ir grynųjų pinigų funkcijos</span><span class="sxs-lookup"><span data-stu-id="f25ac-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="f25ac-136">Galimybė aptarnauti vidaus turtą ir klientų turtą per techninės pagalbos darbo vietoje agentus</span><span class="sxs-lookup"><span data-stu-id="f25ac-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="f25ac-137">Integruotos įsigijimo ir apmokėjimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="f25ac-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="f25ac-138">Kliento duomenų ir dokumentų integruotos veiklos ir pastabos</span><span class="sxs-lookup"><span data-stu-id="f25ac-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="f25ac-139">Galimybė ieškoti turimų atsargų pasiekiamumą ir išsamią informaciją</span><span class="sxs-lookup"><span data-stu-id="f25ac-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="f25ac-140">Projekto ir grynųjų pinigų funkcijos</span><span class="sxs-lookup"><span data-stu-id="f25ac-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="f25ac-141">Galimybė tvarkyti kelis adresus ir vaidmenis naudojant šalies sąvoką</span><span class="sxs-lookup"><span data-stu-id="f25ac-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="f25ac-142">Vartotojams skirtas vieno šaltinio valdymas</span><span class="sxs-lookup"><span data-stu-id="f25ac-142">Single source management for users</span></span>
+ <span data-ttu-id="f25ac-143">Integruoti mažmeninės prekybos ir rinkodaros kanalai</span><span class="sxs-lookup"><span data-stu-id="f25ac-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="f25ac-144">Akcijų ir nuolaidų matomumas</span><span class="sxs-lookup"><span data-stu-id="f25ac-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="f25ac-145">Užklausų dėl aptarnavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="f25ac-145">Request-for-service functions</span></span>
+ <span data-ttu-id="f25ac-146">Racionalizuotos aptarnavimo operacijos</span><span class="sxs-lookup"><span data-stu-id="f25ac-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="f25ac-147">Pagrindinės priežastys naudoti dvigubą rašymą</span><span class="sxs-lookup"><span data-stu-id="f25ac-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="f25ac-148">Dvigubu rašymu pateikiama duomenų integracija „Microsoft Dynamics 365” programose.</span><span class="sxs-lookup"><span data-stu-id="f25ac-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="f25ac-149">Ši patikima sistema susieja aplinkas ir įgalina skirtingas verslo programas dirbti kartu.</span><span class="sxs-lookup"><span data-stu-id="f25ac-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="f25ac-150">Čia pateikiamos pagrindinės priežastys, kodėl reikia naudoti dvigubą rašymą:</span><span class="sxs-lookup"><span data-stu-id="f25ac-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="f25ac-151">Dvigubas rašymas suteikia glaudžiai susietą, beveik realiuoju laiku ir dvikryptę integraciją tarp „Finance and Operations” programų ir „Dynamics 365” modeliu pagrįstų programų.</span><span class="sxs-lookup"><span data-stu-id="f25ac-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="f25ac-152">Su šiuo integravimu „Microsoft Dynamics 365“ tampa ypač daugialype visiems jūsų verslo sprendimams.</span><span class="sxs-lookup"><span data-stu-id="f25ac-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="f25ac-153">Klientai, kurie naudoja „Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”, bet kurie naudoja ne „Microsoft” sprendimus kliento ryšių valdymui (CRM), ilgainiui renkasi dažniau „Dynamics 365” dėl jame palaikomo dvigubo rašymo.</span><span class="sxs-lookup"><span data-stu-id="f25ac-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="f25ac-154">Duomenys iš klientų, produktų, operacijų, projektų ir internetu sąveikaujančių įrenginių („IoT”) automatiškai siunčiami į „Common Data Service” naudojant dvigubą rašymą.</span><span class="sxs-lookup"><span data-stu-id="f25ac-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="f25ac-155">Šis ryšys yra labai naudingas verslo įmonėms, kurios domisi „Microsoft Power Platform” plėtiniais.</span><span class="sxs-lookup"><span data-stu-id="f25ac-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="f25ac-156">Dvigubo rašymo infrastruktūra atitinka kodo nereikalavimo / automatizuoto kodavimo principą.</span><span class="sxs-lookup"><span data-stu-id="f25ac-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="f25ac-157">Reikia minimalių inžinerinių pastangų, kad būtų galima išplėsti standartinius tarpusavy susietų lentelių žemėlapius ir į juos įterpti pasirinktinius žemėlapius.</span><span class="sxs-lookup"><span data-stu-id="f25ac-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="f25ac-158">Dvigubas rašymas palaiko ir internetinį režimą, ir autonominį režimą.</span><span class="sxs-lookup"><span data-stu-id="f25ac-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="f25ac-159">„Microsoft” yra vienintelė įmonė, teikianti palaikymą internetiam ir autonominiam režimams.</span><span class="sxs-lookup"><span data-stu-id="f25ac-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="f25ac-160">Kuo vartotojui ir CRM produktų architektams naudingas dvigubas rašymas?</span><span class="sxs-lookup"><span data-stu-id="f25ac-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="f25ac-161">Dvigubas rašymas automatizuoja duomenų srautą tarp „Finance and Operations” programų ir „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="f25ac-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="f25ac-162">Būsimuose leidimuose sąvokos, esančios „Dynamics 365” modeliu pagrįstose programose, (pvz., klientas, kontaktas, pasiūlymas ir užsakymas) bus pritaikytos vidutinių įmonių ir didesnių nei vidutinės įmonių klientams.</span><span class="sxs-lookup"><span data-stu-id="f25ac-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="f25ac-163">Pirmuoju leidimu didžioji dalis automatizavimo valdoma dvigubo rašymo sprendimų.</span><span class="sxs-lookup"><span data-stu-id="f25ac-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="f25ac-164">Būsimuose leidimuose šie sprendimai taps „Common Data Service“ dalimi.</span><span class="sxs-lookup"><span data-stu-id="f25ac-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="f25ac-165">Suprasdami būsimų keitimų, kurie bus vykdomi „Common Data Service”, naudą ilgainiui galėsite sutaupyti pastangų.</span><span class="sxs-lookup"><span data-stu-id="f25ac-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="f25ac-166">Štai keletas esminių keitimų:</span><span class="sxs-lookup"><span data-stu-id="f25ac-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="f25ac-167">„Common Data Service” bus naujų sąvokų, tokių kaip įmonė ir šalis.</span><span class="sxs-lookup"><span data-stu-id="f25ac-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="f25ac-168">Šios sąvokos paveiks visas programas, kurios yra sukurtos platformoje „Common Data Service”, pvz., „Dynamics 365 Sales”, „Dynamics 365 Marketing”, „Dynamics 365 Customer Service” ir „Dynamics 365 Field Service”.</span><span class="sxs-lookup"><span data-stu-id="f25ac-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="f25ac-169">Veiklos ir pastabos yra suvienodintos ir išplėstos, kad būtų palaikomi ir C1 (sistemos vartotojai), ir C2 (sistemos klientai).</span><span class="sxs-lookup"><span data-stu-id="f25ac-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="f25ac-170">Štai keletas būsimų „Common Data Service” keitimų:</span><span class="sxs-lookup"><span data-stu-id="f25ac-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="f25ac-171">Dešimtainių duomenų tipas pakeis pinigų duomenų tipą.</span><span class="sxs-lookup"><span data-stu-id="f25ac-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="f25ac-172">Datos galiojime bus palaikomi ankstesni, dabartiniai ir būsimi duomenys toje pačioje vietoje.</span><span class="sxs-lookup"><span data-stu-id="f25ac-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="f25ac-173">Bus išplėstas valiutos ir valiutos kursų palaikymas, o programos programavimo sąsaja (API) **Valiutos kursas** bus peržiūrėta.</span><span class="sxs-lookup"><span data-stu-id="f25ac-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="f25ac-174">Bus palaikomi vienetų konvertavimai.</span><span class="sxs-lookup"><span data-stu-id="f25ac-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="f25ac-175">Norėdami gauti daugiau informacijos apie būsimus keitimus, žr. [Duomenys platformoje „Common Data Service” – 1 ir 2 etapai](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).</span><span class="sxs-lookup"><span data-stu-id="f25ac-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).</span></span>
