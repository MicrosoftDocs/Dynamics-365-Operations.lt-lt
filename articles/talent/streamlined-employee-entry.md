---
title: Supaprastintas darbuotojo įrašo sukūrimas ir naršymas
description: Buvo patobulintas darbuotojų duomenų įvedimas „Dynamics 365 Talent”, kad visiems buvusiems, aktyviems ar būsimiems darbuotojams būtų užtikrintas kuo greitesnis įvedimas. Supaprastintas/konsoliduotas naršymo modelis buvo atnaujintas, siekiant greitai rasti susijusią informaciją ir peržiūrėti bei atlikti būtinus naujinimus.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: 40bbb8429355fa18fe12c7cf56f8d58f19766cad
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009427"
---
# <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="e03d9-104">Supaprastintas darbuotojo įrašo sukūrimas ir naršymas</span><span class="sxs-lookup"><span data-stu-id="e03d9-104">Streamlined employee entry and navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e03d9-105">„Dynamics 365 Talent” leidžia efektyviai įvesti darbuotojų ir įdarbinimo duomenis.</span><span class="sxs-lookup"><span data-stu-id="e03d9-105">Dynamics 365 Talent allows efficient entry of employee and employment data.</span></span> <span data-ttu-id="e03d9-106">Galite greitai atnaujinti buvusių, aktyvių ir būsimų darbuotojų bei rangovų darbo retrospektyvos informaciją.</span><span class="sxs-lookup"><span data-stu-id="e03d9-106">You can quickly update work history information for past, active, and future employees and contractors.</span></span>

<span data-ttu-id="e03d9-107">Taip pat galite įgalinti supaprastintą naršymo patirtį, kad greitai rastumėte susijusią informaciją ir įvykdytumėte reikiamus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="e03d9-107">You can also enable a simplified navigation experience to quickly find related information and make any necessary changes.</span></span> <span data-ttu-id="e03d9-108">Ši funkcija dabar yra smėlio dėžės aplinkose.</span><span class="sxs-lookup"><span data-stu-id="e03d9-108">This functionality is now available in sandbox environments.</span></span> <span data-ttu-id="e03d9-109">Norėdami įjungti šią funkciją, pereikite prie **Sistemos administravimas > Saitai > Sąranka > Sistemos parametrai > Peržiūros funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="e03d9-109">To turn this feature on, navigate to **System administration > Links > Setup > System parameters > Preview features**.</span></span> <span data-ttu-id="e03d9-110">Pasirinkite **Patobulintoji darbuotojo forma ir naršymas**.</span><span class="sxs-lookup"><span data-stu-id="e03d9-110">Select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="e03d9-111">Tai įgalins šiuos pakeitimus visiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="e03d9-111">This will enable these changes for all users.</span></span> <span data-ttu-id="e03d9-112">Šią parinktį galite bet kuriuo metu išjungti.</span><span class="sxs-lookup"><span data-stu-id="e03d9-112">You can turn this option off at any time.</span></span>

## <a name="view-options"></a><span data-ttu-id="e03d9-113">Rodyti parinktis</span><span class="sxs-lookup"><span data-stu-id="e03d9-113">View options</span></span>

<span data-ttu-id="e03d9-114">Norėdami pasirinkti bet kokį darbuotojų ir rangovų derinį iš vieno sąrašo, galite naudoti **Peržiūrėti parinktis** darbininko formoje.</span><span class="sxs-lookup"><span data-stu-id="e03d9-114">You can use **View options** on the worker form to select any combination of employees and contractors from a single list.</span></span> <span data-ttu-id="e03d9-115">Šios parinktys leidžia peržiūrėti juridinių subjektų arba juridinio subjekto, prie kurio šiuo metu esate prisijungę, darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="e03d9-115">These options allow you to view workers across legal entities or for the legal entity you're currently signed into.</span></span> <span data-ttu-id="e03d9-116">Taip pat galite peržiūrėti aktyvius, laukiančius ir atleistus darbininkus ir apriboti rezultatus pagal darbininko tipą (darbuotojas ar rangovas).</span><span class="sxs-lookup"><span data-stu-id="e03d9-116">You can also view active, pending, and exited workers, and you can restrict results based on the type of worker (employee or contractor).</span></span> <span data-ttu-id="e03d9-117">Jei įgalinote išplėstinę saugą, matysite tik tuos juridinių subjektų darbuotojus ir rangovus, prie kurių turite priėjimą.</span><span class="sxs-lookup"><span data-stu-id="e03d9-117">If advanced security is enabled, you will only see those employees and contractors in the legal entities you have access to.</span></span>

<span data-ttu-id="e03d9-118">Stulpeliai sąrašo rodinyje keičiasi pagal jūsų pasirinkimus.</span><span class="sxs-lookup"><span data-stu-id="e03d9-118">Columns in the list view change based on your selections.</span></span> <span data-ttu-id="e03d9-119">Pavyzdžiui, kai peržiūrite atleistus darbuotojus, atleidimo data ir priežasties kodai rodomi kaip papildomi stulpeliai sąraše.</span><span class="sxs-lookup"><span data-stu-id="e03d9-119">For example, when viewing exited employees, the termination date and reason codes display as additional columns in the list.</span></span> 

<span data-ttu-id="e03d9-120">[![Rodyti parinktis](./media/Worker-view-option.png)](./media/worker-view-option.png)</span><span class="sxs-lookup"><span data-stu-id="e03d9-120">[![View options](./media/Worker-view-option.png)](./media/worker-view-option.png)</span></span>

## <a name="navigation-and-banner"></a><span data-ttu-id="e03d9-121">Naršymas ir reklaminė juosta</span><span class="sxs-lookup"><span data-stu-id="e03d9-121">Navigation and banner</span></span>

<span data-ttu-id="e03d9-122">Reklaminėje juostoje rodoma pagrindinė kiekvieno darbuotojo informacija.</span><span class="sxs-lookup"><span data-stu-id="e03d9-122">A banner displays key information for each worker.</span></span> <span data-ttu-id="e03d9-123">Aktyvių darbuotojų reklaminėje juostoje rodomi toliau nurodyti laukai.</span><span class="sxs-lookup"><span data-stu-id="e03d9-123">The banner for active workers displays the following fields:</span></span>

- <span data-ttu-id="e03d9-124">**Pareigos**</span><span class="sxs-lookup"><span data-stu-id="e03d9-124">**Title**</span></span>
- <span data-ttu-id="e03d9-125">**Skyrius**</span><span class="sxs-lookup"><span data-stu-id="e03d9-125">**Department**</span></span>
- <span data-ttu-id="e03d9-126">**Pareigų tipas**</span><span class="sxs-lookup"><span data-stu-id="e03d9-126">**Position type**</span></span>
- <span data-ttu-id="e03d9-127">**Darbininko tipas**</span><span class="sxs-lookup"><span data-stu-id="e03d9-127">**Worker type**</span></span>
- <span data-ttu-id="e03d9-128">**Vadovas**</span><span class="sxs-lookup"><span data-stu-id="e03d9-128">**Manager**</span></span>
- <span data-ttu-id="e03d9-129">**Juridinis subjektas**</span><span class="sxs-lookup"><span data-stu-id="e03d9-129">**Legal entity**</span></span>

<span data-ttu-id="e03d9-130">Atleistų darbuotojų reklaminėje juostoje rodomi toliau nurodyti laukai.</span><span class="sxs-lookup"><span data-stu-id="e03d9-130">The banner for exited workers displays the following fields:</span></span>

- <span data-ttu-id="e03d9-131">**Atleidimo data**</span><span class="sxs-lookup"><span data-stu-id="e03d9-131">**Exited date**</span></span>
- <span data-ttu-id="e03d9-132">**Priežastis**</span><span class="sxs-lookup"><span data-stu-id="e03d9-132">**Reason**</span></span>

<span data-ttu-id="e03d9-133">Laukiančių darbuotojų reklaminėje juostoje rodomi toliau nurodyti laukai.</span><span class="sxs-lookup"><span data-stu-id="e03d9-133">The banner for pending employees displays the following fields:</span></span>

- <span data-ttu-id="e03d9-134">**Pareigos**</span><span class="sxs-lookup"><span data-stu-id="e03d9-134">**Title**</span></span>
- <span data-ttu-id="e03d9-135">**Skyrius**</span><span class="sxs-lookup"><span data-stu-id="e03d9-135">**Department**</span></span>
- <span data-ttu-id="e03d9-136">**Pareigų tipas**</span><span class="sxs-lookup"><span data-stu-id="e03d9-136">**Position type**</span></span>
- <span data-ttu-id="e03d9-137">**Vadovas**</span><span class="sxs-lookup"><span data-stu-id="e03d9-137">**Manager**</span></span>
- <span data-ttu-id="e03d9-138">**Pradžios data**</span><span class="sxs-lookup"><span data-stu-id="e03d9-138">**Starting date**</span></span>
- <span data-ttu-id="e03d9-139">**Juridinis subjektas**</span><span class="sxs-lookup"><span data-stu-id="e03d9-139">**Legal entity**</span></span>

<span data-ttu-id="e03d9-140">Darbininko puslapio veiksmų sritis buvo perorganizuota, kad apimtų mažiau parinkčių.</span><span class="sxs-lookup"><span data-stu-id="e03d9-140">The action pane of the worker page has been re-organized to include fewer options.</span></span> <span data-ttu-id="e03d9-141">Informacija dabar yra suskirstyta į toliau nurodytas kategorijas.</span><span class="sxs-lookup"><span data-stu-id="e03d9-141">Information is now organized in the following categories:</span></span> 

- <span data-ttu-id="e03d9-142">Darbas</span><span class="sxs-lookup"><span data-stu-id="e03d9-142">Work</span></span>
- <span data-ttu-id="e03d9-143">Asmuo</span><span class="sxs-lookup"><span data-stu-id="e03d9-143">Person</span></span>
- <span data-ttu-id="e03d9-144">Išeiti</span><span class="sxs-lookup"><span data-stu-id="e03d9-144">Leave</span></span>
- <span data-ttu-id="e03d9-145">Kompensacija</span><span class="sxs-lookup"><span data-stu-id="e03d9-145">Compensation</span></span>
- <span data-ttu-id="e03d9-146">Išmokos</span><span class="sxs-lookup"><span data-stu-id="e03d9-146">Benefits</span></span>
- <span data-ttu-id="e03d9-147">Atitiktis</span><span class="sxs-lookup"><span data-stu-id="e03d9-147">Compliance</span></span>

<span data-ttu-id="e03d9-148">Be to, naujame pagrindinio darbuotojo puslapio skirtuke **Saitai** vartotojams suteikiama centrinė vieta, kur jie gali pasiekti visą su darbuotoju susijusią informaciją.</span><span class="sxs-lookup"><span data-stu-id="e03d9-148">In addtion, a new **Links** tab on the main worker page gives users a central location to access all related information for a worker.</span></span>

<span data-ttu-id="e03d9-149">Dėl šių pakeitimų informacija gali būti rodoma kitoje vietoje nei esate įpratę.</span><span class="sxs-lookup"><span data-stu-id="e03d9-149">Due to these changes, information may appear in a different location than you're used to.</span></span> <span data-ttu-id="e03d9-150">Pavyzdžiui, algalapių informacija, kuri anksčiau buvo rodoma darbuotojo formoje, dabar rodoma veiksmų srities dalyje **Kompensacija > Algalapis**, o skirtuke **Asmeninė informacija** dabar yra mygtukas **Daugiau informacijos**, skirtas laukams, kurie nėra dažnai pasiekiami, paslėpti.</span><span class="sxs-lookup"><span data-stu-id="e03d9-150">For example, payroll information that previously displayed on the worker form now appears in the action pane under **Compensation > Payroll**, and the **Personal information** tab now has a **More information** button to hide fields that aren't accessed often.</span></span>

<span data-ttu-id="e03d9-151">[![Reklaminė juosta](./media/Banner.png)](./media/Banner.png)</span><span class="sxs-lookup"><span data-stu-id="e03d9-151">[![Banner](./media/Banner.png)](./media/Banner.png)</span></span>

## <a name="work-history"></a><span data-ttu-id="e03d9-152">Darbo istorija</span><span class="sxs-lookup"><span data-stu-id="e03d9-152">Work history</span></span>

<span data-ttu-id="e03d9-153">Skirtuke **Darbo retrospektyva** rodoma visų juridinių subjektų darbo retrospektyva ir ją gali pasiekti atleisti, aktyvūs ir laukiantys darbuotojai bei rangovai.</span><span class="sxs-lookup"><span data-stu-id="e03d9-153">The **Work history** tab shows work history accross all legal entities and is available for exited, active, and pending employees and contractors.</span></span> <span data-ttu-id="e03d9-154">Dabar galite peržiūrėti visą juridinių subjektų, prie kurių turite prieigą, darbo retrospektyvą vienu metu.</span><span class="sxs-lookup"><span data-stu-id="e03d9-154">You can now view all work history at once for the legal entities you have access to.</span></span> <span data-ttu-id="e03d9-155">Be to, galite redaguoti kiekvieno darbo retrospektyvos įrašo informaciją nekeisdami duomenų konteksto.</span><span class="sxs-lookup"><span data-stu-id="e03d9-155">In addition, you can edit information for each of the work history entries without changing the data context.</span></span> <span data-ttu-id="e03d9-156">Visą informaciją galite atnaujinti tiesiogiai puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e03d9-156">You can update all information directly on the page.</span></span> 

<span data-ttu-id="e03d9-157">[![Darbo istorija](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span><span class="sxs-lookup"><span data-stu-id="e03d9-157">[![Work history](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span></span>

## <a name="position-history"></a><span data-ttu-id="e03d9-158">Pareigų retrospektyva</span><span class="sxs-lookup"><span data-stu-id="e03d9-158">Position history</span></span>

<span data-ttu-id="e03d9-159">Pagrindiniame darbininko puslapyje esančiame skirtuke **Pareigos** pateikiamas visų organizacijoje einamų pareigų, įskaitant buvusius, esančius ir būsimus priskyrimus, rodinys.</span><span class="sxs-lookup"><span data-stu-id="e03d9-159">The **Positions** tab on the main worker page provides a full view of all positions held within the organization, including past, present, and any future assignments.</span></span> <span data-ttu-id="e03d9-160">Taip pat galite eiti tiesiai į darbininko pareigų retrospektyvą veiksmų srityje.</span><span class="sxs-lookup"><span data-stu-id="e03d9-160">You can still navigate directly to the worker's position history in the action pane as well.</span></span>

<span data-ttu-id="e03d9-161">[![Pareigybės](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span><span class="sxs-lookup"><span data-stu-id="e03d9-161">[![Positions](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span></span>

