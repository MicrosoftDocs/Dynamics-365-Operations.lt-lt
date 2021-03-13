---
title: Dvigubo rašymo apžvalga
description: Šioje temoje pateikta dvigubo rašymo, kuris beveik realiuoju laiku teikia sąveiką tarp klientų įtraukimo programų ir „Finance and Operations” programų, apžvalga.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 3937850a9df716113591e49b25373beb48e3acdd
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130010"
---
# <a name="dual-write-overview"></a><span data-ttu-id="9294e-103">Dvigubo rašymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="9294e-103">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="9294e-104">Kas yra dvigubas rašymas?</span><span class="sxs-lookup"><span data-stu-id="9294e-104">What is dual-write?</span></span>

<span data-ttu-id="9294e-105">Dvigubas rašymas yra parengta naudoti infrastruktūra, kuri beveik realiuoju laiku teikia sąveiką tarp klientų įtraukimo programų ir „Finance and Operations” programų.</span><span class="sxs-lookup"><span data-stu-id="9294e-105">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="9294e-106">Kai duomenys apie klientus, produktus, žmones ir operacijas siunčiami už programos ribų, visiems organizacijos padaliniams suteikiami įgaliojimai.</span><span class="sxs-lookup"><span data-stu-id="9294e-106">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="9294e-107">Dvigubu rašymu pateikiama glaudžiai susieta, dvikryptė integracija tarp „Finance and Operations” programų ir „Dataverse”.</span><span class="sxs-lookup"><span data-stu-id="9294e-107">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="9294e-108">Bet kokie duomenų keitimai, vykdomi „Finance and Operations” programose, taip pat įrašomi į „Dataverse”, o bet kokie „Dataverse” duomenų keitimai yra įrašomi  „Finance and Operations” programose.</span><span class="sxs-lookup"><span data-stu-id="9294e-108">Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="9294e-109">Šis automatizuotas duomenų srautas suteikia integruotą vartotojo patirtį susietose programose.</span><span class="sxs-lookup"><span data-stu-id="9294e-109">This automated data flow provides an integrated user experience across the apps.</span></span>

![Duomenų ryšys tarp programų](media/dual-write-overview.jpg)

<span data-ttu-id="9294e-111">Dvigubo rašymo aspektai yra du – *infrastruktūros* aspektas ir *programos* aspektas.</span><span class="sxs-lookup"><span data-stu-id="9294e-111">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="9294e-112">Infrastruktūra</span><span class="sxs-lookup"><span data-stu-id="9294e-112">Infrastructure</span></span>

<span data-ttu-id="9294e-113">Dvigubo rašymo infrastruktūra yra išplėstinė ir patikima, joje yra šios pagrindinės funkcijos:</span><span class="sxs-lookup"><span data-stu-id="9294e-113">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="9294e-114">Sinchroninis ir dvikryptis duomenų srautas tarp programų</span><span class="sxs-lookup"><span data-stu-id="9294e-114">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="9294e-115">Sinchronizavimas, kartu su atkūrimo, pristabdymo ir papildymo režimais, siekiant palaikyti sistemą internetiniu ir autonominiu / asinchroniniu režimais.</span><span class="sxs-lookup"><span data-stu-id="9294e-115">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="9294e-116">Galimybė sinchronizuoti pradinius duomenis tarp programų</span><span class="sxs-lookup"><span data-stu-id="9294e-116">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="9294e-117">Jungtinis veiklos rodinys ir duomenų administratorių klaidų žurnalas</span><span class="sxs-lookup"><span data-stu-id="9294e-117">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="9294e-118">Galimybė konfigūruoti pasirinktinius įspėjimus ir ribines vertes bei prenumeruoti pranešimus</span><span class="sxs-lookup"><span data-stu-id="9294e-118">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="9294e-119">Intuityviosios vartotojo sąsajos (UI) filtravimas ir transformacijos</span><span class="sxs-lookup"><span data-stu-id="9294e-119">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="9294e-120">Galimybė nustatyti ir peržiūrėti lentelės priklausomybes ir ryšius</span><span class="sxs-lookup"><span data-stu-id="9294e-120">Ability to set and view table dependencies and relationships</span></span>
+ <span data-ttu-id="9294e-121">Ir standartinių, ir tinkintų lentelių bei žemėlapių išplėtimas</span><span class="sxs-lookup"><span data-stu-id="9294e-121">Extensibility for both standard and custom tables and maps</span></span>
+ <span data-ttu-id="9294e-122">Patikimas programos vykdymo ciklo valdymas</span><span class="sxs-lookup"><span data-stu-id="9294e-122">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="9294e-123">Naujo kliento iš anksto parengtos sąrankos funkcijos</span><span class="sxs-lookup"><span data-stu-id="9294e-123">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="9294e-124">Programos</span><span class="sxs-lookup"><span data-stu-id="9294e-124">Application</span></span>

<span data-ttu-id="9294e-125">Dvigubu rašymu sukuriamas susiejimas tarp sąvokų, esančių „Finance and Operations” programose, ir sąvokų, esančių klientų įtraukimo programose.</span><span class="sxs-lookup"><span data-stu-id="9294e-125">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="9294e-126">Ši integracija palaiko šiuos scenarijus:</span><span class="sxs-lookup"><span data-stu-id="9294e-126">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="9294e-127">Bendrieji integruoto kliento duomenys</span><span class="sxs-lookup"><span data-stu-id="9294e-127">Integrated customer master</span></span>
+ <span data-ttu-id="9294e-128">Prieiga prie kliento lojalumo kortelių ir atlygio taškų</span><span class="sxs-lookup"><span data-stu-id="9294e-128">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="9294e-129">Bendrojo produkto bendrosios funkcijos</span><span class="sxs-lookup"><span data-stu-id="9294e-129">Unified product mastering experience</span></span>
+ <span data-ttu-id="9294e-130">Supratimas apie organizacijos hierarchiją</span><span class="sxs-lookup"><span data-stu-id="9294e-130">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="9294e-131">Bendrieji integruoto tiekėjo duomenys</span><span class="sxs-lookup"><span data-stu-id="9294e-131">Integrated vendor master</span></span>
+ <span data-ttu-id="9294e-132">Prieiga prie finansinių ir mokesčių nuorodos duomenų</span><span class="sxs-lookup"><span data-stu-id="9294e-132">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="9294e-133">Kainos pagal poreikį mechanizmo funkcijos</span><span class="sxs-lookup"><span data-stu-id="9294e-133">On-demand price engine experience</span></span>
+ <span data-ttu-id="9294e-134">Integruotos potencialių klientų ir grynųjų pinigų funkcijos</span><span class="sxs-lookup"><span data-stu-id="9294e-134">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="9294e-135">Galimybė aptarnauti vidaus turtą ir klientų turtą per techninės pagalbos darbo vietoje agentus</span><span class="sxs-lookup"><span data-stu-id="9294e-135">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="9294e-136">Integruotos įsigijimo ir apmokėjimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="9294e-136">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="9294e-137">Kliento duomenų ir dokumentų integruotos veiklos ir pastabos</span><span class="sxs-lookup"><span data-stu-id="9294e-137">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="9294e-138">Galimybė ieškoti turimų atsargų pasiekiamumą ir išsamią informaciją</span><span class="sxs-lookup"><span data-stu-id="9294e-138">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="9294e-139">Projekto ir grynųjų pinigų funkcijos</span><span class="sxs-lookup"><span data-stu-id="9294e-139">Project-to-cash experience</span></span>
+ <span data-ttu-id="9294e-140">Galimybė tvarkyti kelis adresus ir vaidmenis naudojant šalies sąvoką</span><span class="sxs-lookup"><span data-stu-id="9294e-140">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="9294e-141">Vartotojams skirtas vieno šaltinio valdymas</span><span class="sxs-lookup"><span data-stu-id="9294e-141">Single source management for users</span></span>
+ <span data-ttu-id="9294e-142">Integruoti mažmeninės prekybos ir rinkodaros kanalai</span><span class="sxs-lookup"><span data-stu-id="9294e-142">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="9294e-143">Akcijų ir nuolaidų matomumas</span><span class="sxs-lookup"><span data-stu-id="9294e-143">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="9294e-144">Užklausų dėl aptarnavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="9294e-144">Request-for-service functions</span></span>
+ <span data-ttu-id="9294e-145">Racionalizuotos aptarnavimo operacijos</span><span class="sxs-lookup"><span data-stu-id="9294e-145">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="9294e-146">Pagrindinės priežastys naudoti dvigubą rašymą</span><span class="sxs-lookup"><span data-stu-id="9294e-146">Top reasons to use dual-write</span></span>

<span data-ttu-id="9294e-147">Dvigubu rašymu pateikiama duomenų integracija „Microsoft Dynamics 365” programose.</span><span class="sxs-lookup"><span data-stu-id="9294e-147">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="9294e-148">Ši patikima sistema susieja aplinkas ir įgalina skirtingas verslo programas dirbti kartu.</span><span class="sxs-lookup"><span data-stu-id="9294e-148">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="9294e-149">Čia pateikiamos pagrindinės priežastys, kodėl reikia naudoti dvigubą rašymą:</span><span class="sxs-lookup"><span data-stu-id="9294e-149">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="9294e-150">Dvigubas rašymas suteikia glaudžiai susietą, beveik realiuoju laiku ir dvikryptę integraciją tarp „Finance and Operations” programų ir „Dynamics 365” modeliu pagrįstų programų.</span><span class="sxs-lookup"><span data-stu-id="9294e-150">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="9294e-151">Su šiuo integravimu „Microsoft Dynamics 365“ tampa ypač daugialype visiems jūsų verslo sprendimams.</span><span class="sxs-lookup"><span data-stu-id="9294e-151">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="9294e-152">Klientai, kurie naudoja „Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”, bet kurie naudoja ne „Microsoft” sprendimus kliento ryšių valdymui (CRM), ilgainiui renkasi dažniau „Dynamics 365” dėl jame palaikomo dvigubo rašymo.</span><span class="sxs-lookup"><span data-stu-id="9294e-152">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="9294e-153">Duomenys iš klientų, produktų, operacijų, projektų ir internetu sąveikaujančių įrenginių („IoT”) automatiškai siunčiami į „Dataverse” naudojant dvigubą rašymą.</span><span class="sxs-lookup"><span data-stu-id="9294e-153">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Dataverse through dual-write.</span></span> <span data-ttu-id="9294e-154">Šis ryšys yra naudingas verslo įmonėms, kurios domisi „Power Platform” plėtiniais.</span><span class="sxs-lookup"><span data-stu-id="9294e-154">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="9294e-155">Dvigubo rašymo infrastruktūra atitinka kodo nereikalavimo / automatizuoto kodavimo principą.</span><span class="sxs-lookup"><span data-stu-id="9294e-155">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="9294e-156">Reikia minimalių inžinerinių pastangų, kad būtų galima išplėsti standartinius tarpusavy susietų lentelių žemėlapius ir į juos įterpti pasirinktinius žemėlapius.</span><span class="sxs-lookup"><span data-stu-id="9294e-156">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="9294e-157">Dvigubas rašymas palaiko ir internetinį režimą, ir autonominį režimą.</span><span class="sxs-lookup"><span data-stu-id="9294e-157">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="9294e-158">„Microsoft” yra vienintelė įmonė, teikianti palaikymą internetiam ir autonominiam režimams.</span><span class="sxs-lookup"><span data-stu-id="9294e-158">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="9294e-159">Kuo dvigubas rašymas naudingas klientų įtraukimo programų kūrėjams ir architektams?</span><span class="sxs-lookup"><span data-stu-id="9294e-159">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="9294e-160">Dvigubas rašymas automatizuoja duomenų srautą tarp „Finance and Operations” programų ir klientų įtraukimo programų.</span><span class="sxs-lookup"><span data-stu-id="9294e-160">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="9294e-161">Dvigubas rašymas susideda iš dviejų „AppSource” sprendimų, įdiegtų „Dataverse”.</span><span class="sxs-lookup"><span data-stu-id="9294e-161">Dual-write consists of two AppSource solutions that are installed on Dataverse.</span></span> <span data-ttu-id="9294e-162">Sprendimai išplečia „Dataverse” lentelių schemą, priedus ir darbo eigas, kad jie galėtų pritaikyti mastelį prie ERP dydžio.</span><span class="sxs-lookup"><span data-stu-id="9294e-162">The solutions expand the table schema, plugins, and workflows on Dataverse so that they can scale to ERP size.</span></span> <span data-ttu-id="9294e-163">Kad diegimas būtų sėkmingas, klientų įtraukimo programų kūrėjai ir architektai turi suprasti šiuos keitimus ir bendradarbiauti su kolegomis „Finance and Operations” programose.</span><span class="sxs-lookup"><span data-stu-id="9294e-163">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="9294e-164">Norint sukurti atitikimą su „Finance and Operations” programomis, dvigubas rašymas įvykdo keletą esminių pakeitimų „Dataverse” schemoje.</span><span class="sxs-lookup"><span data-stu-id="9294e-164">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Dataverse schema.</span></span> <span data-ttu-id="9294e-165">Jei suprantate planą, galite išvengti kai kurių kūrimo ir tobulinimo perdarymo veiksmų ateityje.</span><span class="sxs-lookup"><span data-stu-id="9294e-165">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="9294e-166">Įdiegus dvigubo rašymo „AppSource” paketą, „Dataverse” bus naujų sąvokų, tokių kaip įmonė ir šalis.</span><span class="sxs-lookup"><span data-stu-id="9294e-166">When the dual-write AppSource package is installed, Dataverse will have new concepts such as company and party.</span></span> <span data-ttu-id="9294e-167">Šios sąvokos padeda programoms, sukurtoms remiantis „Dataverse”, įskaitant „Dynamics 365 Sales”, „Dynamics 365 Marketing”, „Dynamics 365 Customer Service” ir „Dynamics 365 Field Service”, sklandžiai sąveikauti su „Finance and Operations” programomis.</span><span class="sxs-lookup"><span data-stu-id="9294e-167">These concepts help applications built on Dataverse, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="9294e-168">Veiklos ir pastabos yra suvienodintos ir išplėstos, kad būtų palaikomi ir C1 (sistemos vartotojai), ir C2 (sistemos klientai).</span><span class="sxs-lookup"><span data-stu-id="9294e-168">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="9294e-169">Norėdami neprarasti duomenų atliekant valiutos perdavimą tarp „Finance and Operations” programų ir „Dataverse”, padidinkite klientų įtraukimo programų valiutos duomenų tipo skaitmenų po kablelio skaičių.</span><span class="sxs-lookup"><span data-stu-id="9294e-169">To prevent data loss during currency transmission between Finance and Operations apps and the Dataverse, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="9294e-170">Funkcija automatiškai paverčia esamas eilutes nauja išplėstine būsena metaduomenų sluoksnyje.</span><span class="sxs-lookup"><span data-stu-id="9294e-170">The feature autotranslates existing rows to the new extended state at the metadata layer.</span></span> <span data-ttu-id="9294e-171">Šio proceso metu valiutos vertė yra paverčiama dešimtainiais duomenimis, o ne pinigų duomenimis, ir valiutos vertė palaiko 10 skaitmenų po kablelio.</span><span class="sxs-lookup"><span data-stu-id="9294e-171">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="9294e-172">Ši funkcija pasirenkama, todėl organizacijoms, kurioms nereikia daugiau nei 4 skaitmenų po kablelio tikslumo, nereikia naudoti funkcijos.</span><span class="sxs-lookup"><span data-stu-id="9294e-172">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="9294e-173">Daugiau informacijos žr. [Dvigubo rašymo valiutos duomenų tipo perkėlimas](currrency-decimal-places.md).</span><span class="sxs-lookup"><span data-stu-id="9294e-173">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="9294e-174">[Datos galiojimas](../../dev-tools/date-effectivity.md) bus įtrauktas į „Dataverse”.</span><span class="sxs-lookup"><span data-stu-id="9294e-174">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Dataverse.</span></span> <span data-ttu-id="9294e-175">Jame bus palaikomi ankstesni, dabartiniai ir būsimi duomenys toje pačioje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="9294e-175">It will support past, present, and future data on the same table.</span></span>

+ <span data-ttu-id="9294e-176">Produkto [vienetų konvertavimai](../../../../supply-chain/pim/tasks/manage-unit-measure.md) palaikomi produktuose, pasiūlymuose, užsakymuose ir SF.</span><span class="sxs-lookup"><span data-stu-id="9294e-176">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="9294e-177">Daugiau informacijos apie būsimus keitimus žr. [Kas nauja ar pasikeitė dvigubo rašymo integravime](whats-new-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="9294e-177">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>

