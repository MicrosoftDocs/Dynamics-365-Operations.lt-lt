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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 85530cf644c7b7ffe922a6fb3288f4e05c5df91c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685618"
---
# <a name="dual-write-overview"></a><span data-ttu-id="4500c-104">Dvigubo rašymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="4500c-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="4500c-105">Kas yra dvigubas rašymas?</span><span class="sxs-lookup"><span data-stu-id="4500c-105">What is dual-write?</span></span>

<span data-ttu-id="4500c-106">Dvigubas rašymas yra parengta naudoti infrastruktūra, kuri beveik realiuoju laiku teikia sąveiką tarp klientų įtraukimo programų ir „Finance and Operations” programų.</span><span class="sxs-lookup"><span data-stu-id="4500c-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="4500c-107">Kai duomenys apie klientus, produktus, žmones ir operacijas siunčiami už programos ribų, visiems organizacijos padaliniams suteikiami įgaliojimai.</span><span class="sxs-lookup"><span data-stu-id="4500c-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="4500c-108">Dvigubu rašymu pateikiama glaudžiai susieta, dvikryptė integracija tarp „Finance and Operations” programų ir „Dataverse”.</span><span class="sxs-lookup"><span data-stu-id="4500c-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="4500c-109">Bet kokie duomenų keitimai, vykdomi „Finance and Operations” programose, taip pat įrašomi į „Dataverse”, o bet kokie „Dataverse” duomenų keitimai yra įrašomi  „Finance and Operations” programose.</span><span class="sxs-lookup"><span data-stu-id="4500c-109">Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="4500c-110">Šis automatizuotas duomenų srautas suteikia integruotą vartotojo patirtį susietose programose.</span><span class="sxs-lookup"><span data-stu-id="4500c-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Duomenų ryšys tarp programų](media/dual-write-overview.jpg)

<span data-ttu-id="4500c-112">Dvigubo rašymo aspektai yra du – *infrastruktūros* aspektas ir *programos* aspektas.</span><span class="sxs-lookup"><span data-stu-id="4500c-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="4500c-113">Infrastruktūra</span><span class="sxs-lookup"><span data-stu-id="4500c-113">Infrastructure</span></span>

<span data-ttu-id="4500c-114">Dvigubo rašymo infrastruktūra yra išplėstinė ir patikima, joje yra šios pagrindinės funkcijos:</span><span class="sxs-lookup"><span data-stu-id="4500c-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="4500c-115">Sinchroninis ir dvikryptis duomenų srautas tarp programų</span><span class="sxs-lookup"><span data-stu-id="4500c-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="4500c-116">Sinchronizavimas, kartu su atkūrimo, pristabdymo ir papildymo režimais, siekiant palaikyti sistemą internetiniu ir autonominiu / asinchroniniu režimais.</span><span class="sxs-lookup"><span data-stu-id="4500c-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="4500c-117">Galimybė sinchronizuoti pradinius duomenis tarp programų</span><span class="sxs-lookup"><span data-stu-id="4500c-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="4500c-118">Jungtinis veiklos rodinys ir duomenų administratorių klaidų žurnalas</span><span class="sxs-lookup"><span data-stu-id="4500c-118">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="4500c-119">Galimybė konfigūruoti pasirinktinius įspėjimus ir ribines vertes bei prenumeruoti pranešimus</span><span class="sxs-lookup"><span data-stu-id="4500c-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="4500c-120">Intuityviosios vartotojo sąsajos (UI) filtravimas ir transformacijos</span><span class="sxs-lookup"><span data-stu-id="4500c-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="4500c-121">Galimybė nustatyti ir peržiūrėti objekto priklausomybes ir ryšius</span><span class="sxs-lookup"><span data-stu-id="4500c-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="4500c-122">Ir standartinių, ir tinkintų lentelių bei žemėlapių išplėtimas</span><span class="sxs-lookup"><span data-stu-id="4500c-122">Extensibility for both standard and custom tables and maps</span></span>
+ <span data-ttu-id="4500c-123">Patikimas programos vykdymo ciklo valdymas</span><span class="sxs-lookup"><span data-stu-id="4500c-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="4500c-124">Naujo kliento iš anksto parengtos sąrankos funkcijos</span><span class="sxs-lookup"><span data-stu-id="4500c-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="4500c-125">Programos</span><span class="sxs-lookup"><span data-stu-id="4500c-125">Application</span></span>

<span data-ttu-id="4500c-126">Dvigubu rašymu sukuriamas susiejimas tarp sąvokų, esančių „Finance and Operations” programose, ir sąvokų, esančių klientų įtraukimo programose.</span><span class="sxs-lookup"><span data-stu-id="4500c-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="4500c-127">Ši integracija palaiko šiuos scenarijus:</span><span class="sxs-lookup"><span data-stu-id="4500c-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="4500c-128">Bendrieji integruoto kliento duomenys</span><span class="sxs-lookup"><span data-stu-id="4500c-128">Integrated customer master</span></span>
+ <span data-ttu-id="4500c-129">Prieiga prie kliento lojalumo kortelių ir atlygio taškų</span><span class="sxs-lookup"><span data-stu-id="4500c-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="4500c-130">Bendrojo produkto bendrosios funkcijos</span><span class="sxs-lookup"><span data-stu-id="4500c-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="4500c-131">Supratimas apie organizacijos hierarchiją</span><span class="sxs-lookup"><span data-stu-id="4500c-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="4500c-132">Bendrieji integruoto tiekėjo duomenys</span><span class="sxs-lookup"><span data-stu-id="4500c-132">Integrated vendor master</span></span>
+ <span data-ttu-id="4500c-133">Prieiga prie finansinių ir mokesčių nuorodos duomenų</span><span class="sxs-lookup"><span data-stu-id="4500c-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="4500c-134">Kainos pagal poreikį mechanizmo funkcijos</span><span class="sxs-lookup"><span data-stu-id="4500c-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="4500c-135">Integruotos potencialių klientų ir grynųjų pinigų funkcijos</span><span class="sxs-lookup"><span data-stu-id="4500c-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="4500c-136">Galimybė aptarnauti vidaus turtą ir klientų turtą per techninės pagalbos darbo vietoje agentus</span><span class="sxs-lookup"><span data-stu-id="4500c-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="4500c-137">Integruotos įsigijimo ir apmokėjimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="4500c-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="4500c-138">Kliento duomenų ir dokumentų integruotos veiklos ir pastabos</span><span class="sxs-lookup"><span data-stu-id="4500c-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="4500c-139">Galimybė ieškoti turimų atsargų pasiekiamumą ir išsamią informaciją</span><span class="sxs-lookup"><span data-stu-id="4500c-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="4500c-140">Projekto ir grynųjų pinigų funkcijos</span><span class="sxs-lookup"><span data-stu-id="4500c-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="4500c-141">Galimybė tvarkyti kelis adresus ir vaidmenis naudojant šalies sąvoką</span><span class="sxs-lookup"><span data-stu-id="4500c-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="4500c-142">Vartotojams skirtas vieno šaltinio valdymas</span><span class="sxs-lookup"><span data-stu-id="4500c-142">Single source management for users</span></span>
+ <span data-ttu-id="4500c-143">Integruoti mažmeninės prekybos ir rinkodaros kanalai</span><span class="sxs-lookup"><span data-stu-id="4500c-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="4500c-144">Akcijų ir nuolaidų matomumas</span><span class="sxs-lookup"><span data-stu-id="4500c-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="4500c-145">Užklausų dėl aptarnavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="4500c-145">Request-for-service functions</span></span>
+ <span data-ttu-id="4500c-146">Racionalizuotos aptarnavimo operacijos</span><span class="sxs-lookup"><span data-stu-id="4500c-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="4500c-147">Pagrindinės priežastys naudoti dvigubą rašymą</span><span class="sxs-lookup"><span data-stu-id="4500c-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="4500c-148">Dvigubu rašymu pateikiama duomenų integracija „Microsoft Dynamics 365” programose.</span><span class="sxs-lookup"><span data-stu-id="4500c-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="4500c-149">Ši patikima sistema susieja aplinkas ir įgalina skirtingas verslo programas dirbti kartu.</span><span class="sxs-lookup"><span data-stu-id="4500c-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="4500c-150">Čia pateikiamos pagrindinės priežastys, kodėl reikia naudoti dvigubą rašymą:</span><span class="sxs-lookup"><span data-stu-id="4500c-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="4500c-151">Dvigubas rašymas suteikia glaudžiai susietą, beveik realiuoju laiku ir dvikryptę integraciją tarp „Finance and Operations” programų ir „Dynamics 365” modeliu pagrįstų programų.</span><span class="sxs-lookup"><span data-stu-id="4500c-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="4500c-152">Su šiuo integravimu „Microsoft Dynamics 365“ tampa ypač daugialype visiems jūsų verslo sprendimams.</span><span class="sxs-lookup"><span data-stu-id="4500c-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="4500c-153">Klientai, kurie naudoja „Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”, bet kurie naudoja ne „Microsoft” sprendimus kliento ryšių valdymui (CRM), ilgainiui renkasi dažniau „Dynamics 365” dėl jame palaikomo dvigubo rašymo.</span><span class="sxs-lookup"><span data-stu-id="4500c-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="4500c-154">Duomenys iš klientų, produktų, operacijų, projektų ir internetu sąveikaujančių įrenginių („IoT”) automatiškai siunčiami į „Dataverse” naudojant dvigubą rašymą.</span><span class="sxs-lookup"><span data-stu-id="4500c-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Dataverse through dual-write.</span></span> <span data-ttu-id="4500c-155">Šis ryšys yra naudingas verslo įmonėms, kurios domisi „Power Platform” plėtiniais.</span><span class="sxs-lookup"><span data-stu-id="4500c-155">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="4500c-156">Dvigubo rašymo infrastruktūra atitinka kodo nereikalavimo / automatizuoto kodavimo principą.</span><span class="sxs-lookup"><span data-stu-id="4500c-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="4500c-157">Reikia minimalių inžinerinių pastangų, kad būtų galima išplėsti standartinius tarpusavy susietų lentelių žemėlapius ir į juos įterpti pasirinktinius žemėlapius.</span><span class="sxs-lookup"><span data-stu-id="4500c-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="4500c-158">Dvigubas rašymas palaiko ir internetinį režimą, ir autonominį režimą.</span><span class="sxs-lookup"><span data-stu-id="4500c-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="4500c-159">„Microsoft” yra vienintelė įmonė, teikianti palaikymą internetiam ir autonominiam režimams.</span><span class="sxs-lookup"><span data-stu-id="4500c-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="4500c-160">Kuo dvigubas rašymas naudingas klientų įtraukimo programų kūrėjams ir architektams?</span><span class="sxs-lookup"><span data-stu-id="4500c-160">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="4500c-161">Dvigubas rašymas automatizuoja duomenų srautą tarp „Finance and Operations” programų ir klientų įtraukimo programų.</span><span class="sxs-lookup"><span data-stu-id="4500c-161">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="4500c-162">Dvigubas rašymas susideda iš dviejų „AppSource” sprendimų, įdiegtų „Dataverse”.</span><span class="sxs-lookup"><span data-stu-id="4500c-162">Dual-write consists of two AppSource solutions that are installed on Dataverse.</span></span> <span data-ttu-id="4500c-163">Sprendimai išplečia „Dataverse” objektų schemą, priedus ir darbo eigas, kad jie galėtų pritaikyti mastelį prie ERP dydžio.</span><span class="sxs-lookup"><span data-stu-id="4500c-163">The solutions expand the entity schema, plugins, and workflows on Dataverse so that they can scale to ERP size.</span></span> <span data-ttu-id="4500c-164">Kad diegimas būtų sėkmingas, klientų įtraukimo programų kūrėjai ir architektai turi suprasti šiuos keitimus ir bendradarbiauti su kolegomis „Finance and Operations” programose.</span><span class="sxs-lookup"><span data-stu-id="4500c-164">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="4500c-165">Norint sukurti atitikimą su „Finance and Operations” programomis, dvigubas rašymas įvykdo keletą esminių pakeitimų „Dataverse” schemoje.</span><span class="sxs-lookup"><span data-stu-id="4500c-165">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Dataverse schema.</span></span> <span data-ttu-id="4500c-166">Jei suprantate planą, galite išvengti kai kurių kūrimo ir tobulinimo perdarymo veiksmų ateityje.</span><span class="sxs-lookup"><span data-stu-id="4500c-166">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="4500c-167">Įdiegus dvigubo rašymo „AppSource” paketą, „Dataverse” bus naujų sąvokų, tokių kaip įmonė ir šalis.</span><span class="sxs-lookup"><span data-stu-id="4500c-167">When the dual-write AppSource package is installed, Dataverse will have new concepts such as company and party.</span></span> <span data-ttu-id="4500c-168">Šios sąvokos padeda programoms, sukurtoms remiantis „Dataverse”, įskaitant „Dynamics 365 Sales”, „Dynamics 365 Marketing”, „Dynamics 365 Customer Service” ir „Dynamics 365 Field Service”, sklandžiai sąveikauti su „Finance and Operations” programomis.</span><span class="sxs-lookup"><span data-stu-id="4500c-168">These concepts help applications built on Dataverse, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="4500c-169">Veiklos ir pastabos yra suvienodintos ir išplėstos, kad būtų palaikomi ir C1 (sistemos vartotojai), ir C2 (sistemos klientai).</span><span class="sxs-lookup"><span data-stu-id="4500c-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="4500c-170">Norėdami neprarasti duomenų atliekant valiutos perdavimą tarp „Finance and Operations” programų ir „Dataverse”, padidinkite klientų įtraukimo programų valiutos duomenų tipo skaitmenų po kablelio skaičių.</span><span class="sxs-lookup"><span data-stu-id="4500c-170">To prevent data loss during currency transmission between Finance and Operations apps and the Dataverse, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="4500c-171">Funkcija automatiškai paverčia esamas eilutes nauja išplėstine būsena metaduomenų sluoksnyje.</span><span class="sxs-lookup"><span data-stu-id="4500c-171">The feature autotranslates existing rows to the new extended state at the metadata layer.</span></span> <span data-ttu-id="4500c-172">Šio proceso metu valiutos vertė yra paverčiama dešimtainiais duomenimis, o ne pinigų duomenimis, ir valiutos vertė palaiko 10 skaitmenų po kablelio.</span><span class="sxs-lookup"><span data-stu-id="4500c-172">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="4500c-173">Ši funkcija pasirenkama, todėl organizacijoms, kurioms nereikia daugiau nei 4 skaitmenų po kablelio tikslumo, nereikia naudoti funkcijos.</span><span class="sxs-lookup"><span data-stu-id="4500c-173">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="4500c-174">Daugiau informacijos žr. [Dvigubo rašymo valiutos duomenų tipo perkėlimas](currrency-decimal-places.md).</span><span class="sxs-lookup"><span data-stu-id="4500c-174">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="4500c-175">[Datos galiojimas](../../dev-tools/date-effectivity.md) bus įtrauktas į „Dataverse”.</span><span class="sxs-lookup"><span data-stu-id="4500c-175">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Dataverse.</span></span> <span data-ttu-id="4500c-176">Jame bus palaikomi ankstesni, dabartiniai ir būsimi duomenys tame pačiame objekte.</span><span class="sxs-lookup"><span data-stu-id="4500c-176">It will support past, present, and future data on the same entity.</span></span>

+ <span data-ttu-id="4500c-177">Produkto [vienetų konvertavimai](../../../../supply-chain/pim/tasks/manage-unit-measure.md) palaikomi produktuose, pasiūlymuose, užsakymuose ir SF.</span><span class="sxs-lookup"><span data-stu-id="4500c-177">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="4500c-178">Daugiau informacijos apie būsimus keitimus žr. [Kas nauja ar pasikeitė dvigubo rašymo integravime](whats-new-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="4500c-178">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>

