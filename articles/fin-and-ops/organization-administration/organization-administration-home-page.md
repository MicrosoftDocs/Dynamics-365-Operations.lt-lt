---
title: Organizacijos administravimo pagrindinis puslapis
description: "Šioje temoje nurodyti ištekliai, kurie padės organizacijoje naudoti „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“."
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f1cff2388b02ff6dfd52a39b7f3ea90f10807096
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="organization-administration-home-page"></a><span data-ttu-id="cbac9-103">Organizacijos administravimo pagrindinis puslapis</span><span class="sxs-lookup"><span data-stu-id="cbac9-103">Organization administration home page</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cbac9-104">Šioje temoje nurodytas turinys, patyrusiems vartotojams ir administratoriams padėsiantis konfigūruoti „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“.</span><span class="sxs-lookup"><span data-stu-id="cbac9-104">This topic points to content that will help power users and administrators configure Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="cbac9-105">Šis turinys jiems padės sistemą sukonfigūruoti taip, kad ji jūsų organizacijoje ir įmonėje veiktų sklandžiai bei efektyviai.</span><span class="sxs-lookup"><span data-stu-id="cbac9-105">This content will help them configure the system to work smoothly and effectively for your organization and business.</span></span>

<span data-ttu-id="cbac9-106">Didelė čia pateikto turinio dalis taikoma modulio **Organizacijos administravimas** funkcijoms.</span><span class="sxs-lookup"><span data-stu-id="cbac9-106">Much of the content listed here applies to features in the **Organizational administration** module.</span></span> <span data-ttu-id="cbac9-107">Tačiau yra keletas užduočių, pavyzdžiui, įrašo šablono kūrimo ir naudojimo, kurias galima atlikti bet kokiame modulyje, kad organizacija galėtų veikti efektyviau.</span><span class="sxs-lookup"><span data-stu-id="cbac9-107">However, there are a couple of tasks, such as creating and using a record template, that can be performed in any module to help your organization run more efficiently.</span></span> 

<a name="number-sequences"></a><span data-ttu-id="cbac9-108">Numeravimai</span><span class="sxs-lookup"><span data-stu-id="cbac9-108">Number sequences</span></span>
----------------
<span data-ttu-id="cbac9-109">Numeracija naudojama bendrųjų duomenų įrašų ir operacijų įrašų, kuriems reikia identifikatorių, nuskaitomiems unikaliems identifikatoriams sugeneruoti.</span><span class="sxs-lookup"><span data-stu-id="cbac9-109">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="cbac9-110">Pagrindinių duomenų įrašas arba operacijų įrašas, kuriam reikia identifikatoriaus, vadinamas *nuoroda*.</span><span class="sxs-lookup"><span data-stu-id="cbac9-110">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span> <span data-ttu-id="cbac9-111">Kad galėtumėte kurti naujus įrašus kaip nuorodas, turite nustatyti numeraciją ir susieti ją su nuoroda.</span><span class="sxs-lookup"><span data-stu-id="cbac9-111">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span>

-   [<span data-ttu-id="cbac9-112">Numeracijos apžvalga</span><span class="sxs-lookup"><span data-stu-id="cbac9-112">Number sequence overview</span></span>](number-sequence-overview.md)
-   <span data-ttu-id="cbac9-113">[Nustatyti numeracijas naudojant vedlį](tasks/set-up-number-sequences-wizard.md) (Užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="cbac9-113">[Set up number sequences by using a wizard](tasks/set-up-number-sequences-wizard.md) (Task guide)</span></span>
-   <span data-ttu-id="cbac9-114">[Atskirų numeracijų nustatymas](tasks/set-up-number-sequences-individual-basis.md) (Užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="cbac9-114">[Set up number sequences on an individual basis](tasks/set-up-number-sequences-individual-basis.md) (Task guide)</span></span>

## <a name="organizations"></a><span data-ttu-id="cbac9-115">Organizacijos</span><span class="sxs-lookup"><span data-stu-id="cbac9-115">Organizations</span></span>
<span data-ttu-id="cbac9-116">Organizacija yra grupė žmonių, kurie dirba kartu vykdydami verslo procesą arba siekdami tikslo.</span><span class="sxs-lookup"><span data-stu-id="cbac9-116">An organization is a group of people who are working together to carry out a business process or achieve a goal.</span></span> <span data-ttu-id="cbac9-117">Organizacijos hierarchijos nurodo ryšius tarp organizacijų, kurios sudaro jūsų verslą.</span><span class="sxs-lookup"><span data-stu-id="cbac9-117">Organizational hierarchies represent the relationships between the organizations that make up your business.</span></span>

<span data-ttu-id="cbac9-118">Prieš sprendime „Finance and Operations“ nustatydami organizacijas ir hierarchijas, būtinai suplanuokite, kaip bus modeliuojamas jūsų verslas.</span><span class="sxs-lookup"><span data-stu-id="cbac9-118">Before you set up organizations and organization hierarchies in Finance and Operations, make sure that you plan how your business will be modeled.</span></span> <span data-ttu-id="cbac9-119">Organizacijos modelis turi didelės įtakos „Finance and Operations“ diegimui ir verslo procesams.</span><span class="sxs-lookup"><span data-stu-id="cbac9-119">The organization model has a significant effect on the implementation of Finance and Operations and on business processes.</span></span>

-   [<span data-ttu-id="cbac9-120">Organizacijos ir organizacijų hierarchijos</span><span class="sxs-lookup"><span data-stu-id="cbac9-120">Organizations and organizational hierarchies</span></span>](organizations-organizational-hierarchies.md)
-   [<span data-ttu-id="cbac9-121">Organizacijos hierarchijos planavimas</span><span class="sxs-lookup"><span data-stu-id="cbac9-121">Plan your organizational hierarchy</span></span>](plan-organizational-hierarchy.md)
-   <span data-ttu-id="cbac9-122">[Organizacijos hierarchijos kūrimas](tasks/create-organization-hierarchy.md) (Užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="cbac9-122">[Create an organization hierarchy](tasks/create-organization-hierarchy.md) (Task guide)</span></span>
-   <span data-ttu-id="cbac9-123">[Juridinio subjekto kūrimas](tasks/create-legal-entity.md) (Užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="cbac9-123">[Create a legal entity](tasks/create-legal-entity.md) (Task guide)</span></span>
-   <span data-ttu-id="cbac9-124">[Valdymo vieneto kūrimas](tasks/create-operating-unit.md) (Užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="cbac9-124">[Create an operating unit](tasks/create-operating-unit.md) (Task guide)</span></span>

## <a name="address-books"></a><span data-ttu-id="cbac9-125">Adresų knygelės</span><span class="sxs-lookup"><span data-stu-id="cbac9-125">Address books</span></span>
<span data-ttu-id="cbac9-126">Visuotinė adresų knygelė yra centralizuota saugykla, kurioje turi būti saugomi visų vidinių ir išorinių asmenų bei organizacijų, su kuriais įmonė bendrauja, bendrieji duomenys.</span><span class="sxs-lookup"><span data-stu-id="cbac9-126">The global address book is a centralized repository for master data that must be stored for all internal and external persons and organizations that the company interacts with.</span></span> <span data-ttu-id="cbac9-127">Duomenys, susieti su šalies įrašais, apima šalies pavadinimą, adresą ir kontaktinę informaciją.</span><span class="sxs-lookup"><span data-stu-id="cbac9-127">The data that is associated with party records includes the party's name, address, and contact information.</span></span> 

<span data-ttu-id="cbac9-128">Sukūrę visuotinę adresų knygelę, pagal poreikį galite kurti papildomų adresų knygelių, pvz., atskirą adresų knygelę kiekvienai jūsų organizacijos įmonei ar kiekvienai verslo šakai.</span><span class="sxs-lookup"><span data-stu-id="cbac9-128">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> 

-   [<span data-ttu-id="cbac9-129">Visuotinė adresų knygelė</span><span class="sxs-lookup"><span data-stu-id="cbac9-129">Global address book</span></span>](overview-global-address-book.md)
-   [<span data-ttu-id="cbac9-130">Planavimas, kaip konfigūruoti visuotinę adresų knygelę ir papildomas adresų knygeles</span><span class="sxs-lookup"><span data-stu-id="cbac9-130">Plan how to configure the global address book and additional address books</span></span>](plan-configuration-global-address-book-additional-address-books.md)
- [<span data-ttu-id="cbac9-131">Visuotinės adresų knygelės konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cbac9-131">Configure the global address book</span></span>](tasks/configure-global-address-book.md)
-   [<span data-ttu-id="cbac9-132">DUK apie adresų knygeles</span><span class="sxs-lookup"><span data-stu-id="cbac9-132">Address books FAQ</span></span>](qa-address-books.md)


## <a name="workflow"></a><span data-ttu-id="cbac9-133">Darbo eiga</span><span class="sxs-lookup"><span data-stu-id="cbac9-133">Workflow</span></span>
<span data-ttu-id="cbac9-134">Darbo eiga yra su „Finance and Operations“ įdiegta sistema, kurią naudodami galite kurti atskiras darbo eigas ar verslo procesus.</span><span class="sxs-lookup"><span data-stu-id="cbac9-134">Workflow is a system that is installed with Finance and Operations that you can use to create individual workflows, or business processes.</span></span> <span data-ttu-id="cbac9-135">Kurdami darbo eigą nurodote, kaip dokumentas juda sistemoje, parodydami, kas turi įvykdyti užduotį, priimti sprendimą ar patvirtinti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="cbac9-135">When you create a workflow, you specify how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> 

-   [<span data-ttu-id="cbac9-136">Darbo eigos apžvalga</span><span class="sxs-lookup"><span data-stu-id="cbac9-136">Workflow overview</span></span>](overview-workflow-system.md)
-   [<span data-ttu-id="cbac9-137">Darbo eigos elementai</span><span class="sxs-lookup"><span data-stu-id="cbac9-137">Workflow elements</span></span>](workflow-elements.md)
-   [<span data-ttu-id="cbac9-138">Darbo eigos veiksmai</span><span class="sxs-lookup"><span data-stu-id="cbac9-138">Workflow actions</span></span>](workflow-actions.md)
-   [<span data-ttu-id="cbac9-139">Darbo eigos kūrimas</span><span class="sxs-lookup"><span data-stu-id="cbac9-139">Create a workflow</span></span>](create-workflow.md)

## <a name="electronic-signatures"></a><span data-ttu-id="cbac9-140">Elektroniniai parašai</span><span class="sxs-lookup"><span data-stu-id="cbac9-140">Electronic signatures</span></span>
<span data-ttu-id="cbac9-141">Elektroninis parašas patvirtina asmens, kuris ketina pradėti ar patvirtinti skaičiavimo procesą, tapatybę.</span><span class="sxs-lookup"><span data-stu-id="cbac9-141">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="cbac9-142">Kai kuriose pramonės šakose elektroninis parašas turi tokią pat teisinę galią kaip parašas ranka.</span><span class="sxs-lookup"><span data-stu-id="cbac9-142">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> <span data-ttu-id="cbac9-143">Elektroniniai parašai yra reglamentus atitinkantis reikalavimas kai kurioms reguliuojamoms pramonės šakoms, pvz., vaistų, maisto ir gėrimų, aviacijos ir gynybos.</span><span class="sxs-lookup"><span data-stu-id="cbac9-143">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span>

<span data-ttu-id="cbac9-144">Programoje „Finance and Operations“ galite naudoti elektroninius parašus svarbiems verslo procesams.</span><span class="sxs-lookup"><span data-stu-id="cbac9-144">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="cbac9-145">Kai kuriuose procesuose yra įdiegtos elektroninio parašo galimybės.</span><span class="sxs-lookup"><span data-stu-id="cbac9-145">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="cbac9-146">Taip pat galite sukurti pasirinktinius parašo reikalavimus bet kuriai duomenų bazės lentelei ir laukui.</span><span class="sxs-lookup"><span data-stu-id="cbac9-146">You can also create custom signature requirements for any database table and field.</span></span>

-   [<span data-ttu-id="cbac9-147">Elektroninio parašo apžvalga</span><span class="sxs-lookup"><span data-stu-id="cbac9-147">Electronic signature overview</span></span>](electronic-signature-overview.md)
-   <span data-ttu-id="cbac9-148">[Elektroninių parašų nustatymas](tasks/set-up-electronic-signatures.md) (Užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="cbac9-148">[Set up electronic signatures](tasks/set-up-electronic-signatures.md) (Task guide)</span></span>

## <a name="case-management"></a><span data-ttu-id="cbac9-149">Atvejų valdymas</span><span class="sxs-lookup"><span data-stu-id="cbac9-149">Case management</span></span>
<span data-ttu-id="cbac9-150">Planuojant, sekant ir analizuojant atvejus galima sukurti efektyvius sprendimus, skirtus panašioms problemoms spręsti.</span><span class="sxs-lookup"><span data-stu-id="cbac9-150">By planning, tracking, and analyzing cases, you can develop efficient resolutions that can be used for similar issues.</span></span> <span data-ttu-id="cbac9-151">Pavyzdžiui, kai klientų aptarnavimo atstovai arba personalo srities darbuotojai kuria atvejus, informacijos, padėsiančios efektyviau dirbti su atveju ar jį spręsti, jie gali rasti informaciniuose straipsniuose.</span><span class="sxs-lookup"><span data-stu-id="cbac9-151">For example, when customer service representatives or Human Resources generalists create cases, they can find information in knowledge articles to help them work with or resolve a case more efficiently.</span></span> 

-   [<span data-ttu-id="cbac9-152">Atvejų valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="cbac9-152">Case management overview</span></span>](cases.md)
-   [<span data-ttu-id="cbac9-153">Atvejų saugos, procesų ir kategorijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cbac9-153">Configure case security, processes, and categories</span></span>](plan-case-management.md)

## <a name="record-templates"></a><span data-ttu-id="cbac9-154">Įrašų šablonai</span><span class="sxs-lookup"><span data-stu-id="cbac9-154">Record templates</span></span>
<span data-ttu-id="cbac9-155">Įrašų šablonai gali padėti greičiau kurti įrašus.</span><span class="sxs-lookup"><span data-stu-id="cbac9-155">Record templates can help you to create records more quickly.</span></span> <span data-ttu-id="cbac9-156">Galite sukurti įrašo šabloną, kad dėl kiekvieno naujo įrašo nereikėtų tiesiogiai įvedinėti dažnai naudojamų laukų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="cbac9-156">You can create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> 

-   [<span data-ttu-id="cbac9-157">Įrašų šablonai</span><span class="sxs-lookup"><span data-stu-id="cbac9-157">Record templates</span></span>](record-templates.md)
- <span data-ttu-id="cbac9-158">[Įrašo šablono sukūrimas, kad būtų paprasčiau įvesti duomenis](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="cbac9-158">[Create a record template to facilitate data entry](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Task guide)</span></span>
- <span data-ttu-id="cbac9-159">[Naujo įrašo kūrimas naudojant įrašo šabloną](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="cbac9-159">[Use a record template to create a new record](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Task guide)</span></span>

## <a name="general-organization-administration"></a><span data-ttu-id="cbac9-160">Bendrasis organizacijos administravimas</span><span class="sxs-lookup"><span data-stu-id="cbac9-160">General organization administration</span></span>
-   <span data-ttu-id="cbac9-161">[Keisti reklaminę juostą arba logotipą](../get-started/tasks/change-banner-or-logo.md) (Užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="cbac9-161">[Change the banner or logo](../get-started/tasks/change-banner-or-logo.md) (Task guide)</span></span>
- [<span data-ttu-id="cbac9-162">Dokumentų valdymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cbac9-162">Configure document management</span></span>](configure-document-management.md)
- [<span data-ttu-id="cbac9-163">El. pašto konfigūravimas ir siuntimas</span><span class="sxs-lookup"><span data-stu-id="cbac9-163">Configure and send email</span></span>](configure-email.md)
-   [<span data-ttu-id="cbac9-164">Datos / laiko duomenys ir laiko juostos</span><span class="sxs-lookup"><span data-stu-id="cbac9-164">Date/time data and time zones</span></span>](date-time-zones.md)








