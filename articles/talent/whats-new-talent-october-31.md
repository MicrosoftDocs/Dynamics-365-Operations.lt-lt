---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. spalio 31 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent Core HR“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c5acd09e25ecd5fefa637342f83d0ee0f1891402
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "305486"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a><span data-ttu-id="c64ee-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. spalio 31 d.)</span><span class="sxs-lookup"><span data-stu-id="c64ee-103">What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c64ee-104">**8.1.2031 versija**</span><span class="sxs-lookup"><span data-stu-id="c64ee-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="c64ee-105">Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="c64ee-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance-and-operations"></a><span data-ttu-id="c64ee-106">Kurti duomenų saitus iš „Talent“ į „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="c64ee-106">Create links from Talent to Finance and Operations</span></span>
<span data-ttu-id="c64ee-107">Naudodamiesi šia nauja naršymo funkcija galite susieti „Talent“ su „Finance and Operations“ ir tiesiogiai pereiti į „Finance and Operations“ puslapius.</span><span class="sxs-lookup"><span data-stu-id="c64ee-107">This new navigation functionality allows you to link from Talent to Finance and Operations, giving you direct navigation into Finance and Operations pages.</span></span> <span data-ttu-id="c64ee-108">Konfigūruodami saitus galite nurodyti saito pavadinimą ir grupę, kur saitas bus rodomas „Talent“, bei paskirties puslapį, kuris bus atidaromas „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="c64ee-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance and Operations.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="c64ee-109">Jau greitai</span><span class="sxs-lookup"><span data-stu-id="c64ee-109">Coming soon</span></span>
<span data-ttu-id="c64ee-110">Ateityje bus įtrauktas laukų kontekstas, kad galėtumėte tiesiogiai pereiti į atitinkamus „Finance and Operations“ įrašus.</span><span class="sxs-lookup"><span data-stu-id="c64ee-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance and Operations.</span></span> <span data-ttu-id="c64ee-111">Pavyzdžiui, galite naudotiesi **lauko saitu** nurodyti kontekstą, leidžiantį tiesiogiai pereiti į konkretaus darbuotojo arba pareigų duomenis „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="c64ee-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance and Operations.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="c64ee-112">Konfigūruoti paskirties sistemas</span><span class="sxs-lookup"><span data-stu-id="c64ee-112">Configure target systems</span></span>

<span data-ttu-id="c64ee-113">Naudodamiesi „Talent“ sistemos administratoriai gali nustatyti saitus, kuriuos bus galima naudoti sistemos administravimo darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="c64ee-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="c64ee-114">Konfigūruodami turėsite nustatyti „Finance and Operations“ aplinkas, į kurias naudodamiesi saitu norite pereiti kaip į paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="c64ee-114">Part of the configuration is the Finance and Operations environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="c64ee-115">Tai padarysite suteikdami paskirties sistemai pavadinimą ir nurodydami „Finance and Operations“ aplinkos URL.</span><span class="sxs-lookup"><span data-stu-id="c64ee-115">You do this by giving the target system a name and providing the URL of the Finance and Operations environment.</span></span> <span data-ttu-id="c64ee-116">„Finance and Operations“ URL, kurį turėtumėte nurodyti, pavyzdys: https://devax00124aos.cloud.test.dynamics.com/.</span><span class="sxs-lookup"><span data-stu-id="c64ee-116">Here is an example of a Finance and Operations URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="c64ee-117">Sukonfigūravę paskirties sistemas galite nustatyti saitus.</span><span class="sxs-lookup"><span data-stu-id="c64ee-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="c64ee-118">Konfigūruoti saitus</span><span class="sxs-lookup"><span data-stu-id="c64ee-118">Configure links</span></span>

<span data-ttu-id="c64ee-119">Kiekviename kuriamame saite bus nurodyta tolesnė informacija.</span><span class="sxs-lookup"><span data-stu-id="c64ee-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="c64ee-120">Saitas – saito pavadinimas, naudojamas tik identifikavimui.</span><span class="sxs-lookup"><span data-stu-id="c64ee-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="c64ee-121">Įjungti šį saitą – nustatykite **Taip**, jei norite, kad saitą matytų „Talent“ vartotojai.</span><span class="sxs-lookup"><span data-stu-id="c64ee-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="c64ee-122">Rodomas pavadinimas – nurodykite pavadinimą, kuris bus rodomas kaip „Finance and Operations“ saitas.</span><span class="sxs-lookup"><span data-stu-id="c64ee-122">Display name - Define the name that will appear as a link to Finance and Operations.</span></span> <span data-ttu-id="c64ee-123">Šiuo metu šie duomenys nėra išversti.</span><span class="sxs-lookup"><span data-stu-id="c64ee-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="c64ee-124">Formoje pridėti saitą – pasirinkite, kurį puslapį norite rodyti naudodami saitą.</span><span class="sxs-lookup"><span data-stu-id="c64ee-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="c64ee-125">Grupė – grupės nėra būtinos, tačiau jei norite tvarkyti savo saitus naudodami grupes, pasirinkite esamą grupę arba sukurkite naują naudodamiesi lauku **Grupė**.</span><span class="sxs-lookup"><span data-stu-id="c64ee-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="c64ee-126">Paskiries sistema – pasirinkite paskirties sistemą, sukurtą naudojant parinktį **Konfigūruoti paskirties sistemą**.</span><span class="sxs-lookup"><span data-stu-id="c64ee-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="c64ee-127">Tai bus „Finance and Operations“ aplinka, į kurią bus pereinama naudojant saitą.</span><span class="sxs-lookup"><span data-stu-id="c64ee-127">This will be the Finance and Operations environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="c64ee-128">Naudoti dabartinę vartotojo įmonę – pasirinkite **Taip**, jei pereinant į „Finance and Operations“ norite naudoti dabartinės vartotojo įmonės kontekstą.</span><span class="sxs-lookup"><span data-stu-id="c64ee-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance and Operations.</span></span> <span data-ttu-id="c64ee-129">Jei pasirinksite **Ne**, galėsite pasirinkti įmonę, kuri bus naudojama.</span><span class="sxs-lookup"><span data-stu-id="c64ee-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="c64ee-130">Paskirties meniu elementas – įveskite meniu elementą iš „Finance and Operation“, į kurį bus pereinama pasirinkus saitą.</span><span class="sxs-lookup"><span data-stu-id="c64ee-130">Target menu item - Enter the menu item from Finance and Operation that the link should use when navigating.</span></span> <span data-ttu-id="c64ee-131">Yra meniu elementų, į kuriuos galite pereiti tiesiogiai.</span><span class="sxs-lookup"><span data-stu-id="c64ee-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="c64ee-132">Norėdami rasti reikiamą meniu elementą atidarykite „Finance and Operations“ ir naršymo paskirties puslapį.</span><span class="sxs-lookup"><span data-stu-id="c64ee-132">To find the menu item required, open Finance and Operations and open the page that is the target of the navigation.</span></span> <span data-ttu-id="c64ee-133">Nukopijuokite meniu elementą iš URL.</span><span class="sxs-lookup"><span data-stu-id="c64ee-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="c64ee-134">Pavyzdžiui, jei norite, kad saitas atidarytų darbuotojų sąrašą, esantį „Finance and Operations“, įveskite reikšmę, kuri URL bus po &mi.</span><span class="sxs-lookup"><span data-stu-id="c64ee-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="c64ee-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="c64ee-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="c64ee-136">Meniu elemento, perkeliančio į darbuotojų sąrašo puslapį, pavyzdys: HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="c64ee-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="c64ee-137">Susieti su duomenų šaltiniu – pasirinkite duomenų šaltinį, kurį nurodo saitas.</span><span class="sxs-lookup"><span data-stu-id="c64ee-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="c64ee-138">Galimi dažniausiai naudojami šaltiniai, pvz., **Darbininkas** ir **Pareigos**.</span><span class="sxs-lookup"><span data-stu-id="c64ee-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="c64ee-139">Lauko saitas – (jau greitai) pasirinkę šią lauko parinktį galėsite tiesiogiai pereiti iš vieno „Talent“ įrašo į vieną „Finance and Operations“ įrašą.</span><span class="sxs-lookup"><span data-stu-id="c64ee-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance and Operations.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="c64ee-140">Prieiga prie saitų</span><span class="sxs-lookup"><span data-stu-id="c64ee-140">Access to links</span></span>

<span data-ttu-id="c64ee-141">Sistemos administratoriai nustatytuose puslapiuose matys naujai sukurtus saitus, net jei pasirinkta parinkties **Įjungti šį saitą** reikšmė yra **Ne**.</span><span class="sxs-lookup"><span data-stu-id="c64ee-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="c64ee-142">Tai galima naudoti norint patikrinti saitus prieš pateikiant juos naudoti kitiems darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="c64ee-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="c64ee-143">Visi kiti vaidmenys matys tik sukonfigūruotus saitus, kai parinktis **Įjungti šį saitą** bus nustatyta kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="c64ee-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="c64ee-144">Saitus galės pasiekti darbuotojai, turintys prieigą prie puslapių, kuriuose šie saitai yra pridėti.</span><span class="sxs-lookup"><span data-stu-id="c64ee-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="c64ee-145">Vartotojai taip pat gali turėti saugos teisių „Finance and Operations “, nustatanių prieigą prie „Finance and Operations“ puslapių.</span><span class="sxs-lookup"><span data-stu-id="c64ee-145">Users can also have security rights within Finance and Operations defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="c64ee-146">Jei jie jų neturi, naudojant saitą bus rodomas saugos dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="c64ee-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="c64ee-147">Kiti pakeitimai / pataisos</span><span class="sxs-lookup"><span data-stu-id="c64ee-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="c64ee-148">Naujam darbuotojui negalima priskirti pareigų, kurių pradžios data yra ateityje.</span><span class="sxs-lookup"><span data-stu-id="c64ee-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="c64ee-149">Atlikti pakeitimai, leidžiantys darbuotojams priskirti būsimas pareigas.</span><span class="sxs-lookup"><span data-stu-id="c64ee-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="c64ee-150">Pareigas, kurių pradžios data yra ateityje, galima pasirinkti ir priskirti darbuotojui įrašius arba užbaigus darbo eigą (jei darbo eiga yra įjungta).</span><span class="sxs-lookup"><span data-stu-id="c64ee-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="c64ee-151">Naujam darbuotojui negalima priskirti esamų pareigų</span><span class="sxs-lookup"><span data-stu-id="c64ee-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="c64ee-152">Atlikti pakeitimai, todėl dabar naujam darbuotojui galima priskirti esamas pareigas.</span><span class="sxs-lookup"><span data-stu-id="c64ee-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="c64ee-153">Kai įdarbinimo pradžios data yra praeityje ir įrašas yra įrašytas, paaukštinimo data / biuro vieta neberodoma</span><span class="sxs-lookup"><span data-stu-id="c64ee-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="c64ee-154">Atlikti matomumo keitimai siekiant pakoreguoti **paaukštinimo datos** ir **biuro vietos** matomumą įrašant buvusių darbuotojų pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="c64ee-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="c64ee-155">Darbininko puslapyje negalima įvesti duomenų apie įdarbinimą, kurio pradžios data yra ateityje</span><span class="sxs-lookup"><span data-stu-id="c64ee-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="c64ee-156">Pagrindiniame darbininko puslapyje išjungti duomenys, susiję su įdarbinimais, kurių pradžios data yra ateityje.</span><span class="sxs-lookup"><span data-stu-id="c64ee-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="c64ee-157">Įdarbinimo duomenis galima įvesti **datų tvarkytuvo** puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="c64ee-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="c64ee-158">Būsimuose leidimuose bus atlikta daugiau pakeitimų siekiant sudaryti sąlygas įdarbinimo duomenis įvesti tiesiogiai darbo eigos procese.</span><span class="sxs-lookup"><span data-stu-id="c64ee-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="c64ee-159">Į HcmPersonalContactPersonEntity įtraukti ValidFrom ir ValidTo</span><span class="sxs-lookup"><span data-stu-id="c64ee-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="c64ee-160">Atnaujintas „Data Management Framework“ (DMF) objektas HcmPersonalContactPersonEntity įtraukiant datas Galioja nuo ir Galioja iki, kad būtų galima įjungti tam tikrus išmokų integravimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="c64ee-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="c64ee-161">Žinoma problema</span><span class="sxs-lookup"><span data-stu-id="c64ee-161">Known issue</span></span>
- <span data-ttu-id="c64ee-162">**Problema**: įtraukiant naują priedą į darbininko puslapį mygtukai **Naujas** ir **Redaguoti** yra papilkinti.</span><span class="sxs-lookup"><span data-stu-id="c64ee-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="c64ee-163">**Problemos sprendimas:** prieš atidarydami priedų puslapį įsitikinkite, kad „FactBoxes“ laukai puslapyje **Darbininkas** yra uždaryti.</span><span class="sxs-lookup"><span data-stu-id="c64ee-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="c64ee-164">Jei „FactBoxes“ laukai yra uždaryti, įkeliant puslapį **Darbininkas** priedų mygtukai bus įjungti.</span><span class="sxs-lookup"><span data-stu-id="c64ee-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="c64ee-165">(Ši problema bus pašalinta kitame platformos naujinime.)</span><span class="sxs-lookup"><span data-stu-id="c64ee-165">(This issue will be fixed in the next platform update.)</span></span>
