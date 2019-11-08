---
title: Analizės ataskaitų naudojimas „Microsoft Dynamics 365 Talent - Attract”
description: Šioje temoje aprašoma „Microsoft Dynamics 365 Talent - Attract” samdos procesų įžvalgų analizės ataskaitos.
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 5a4d160e8c90725d5ea129a76fd48da1c5af7900
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551523"
---
# <a name="use-analytic-reports-in-microsoft-dynamics-365-talent---attract"></a><span data-ttu-id="41d58-103">Analizės ataskaitų naudojimas „Microsoft Dynamics 365 Talent - Attract”</span><span class="sxs-lookup"><span data-stu-id="41d58-103">Use analytic reports in Microsoft Dynamics 365 Talent - Attract</span></span>

<span data-ttu-id="41d58-104">Analitinės ataskaitos programoje „Microsoft Dynamics 365 Talent: Attract“ suteikia nestandartinį (OOTB) sprendimą samdos proceso įžvalgoms.</span><span class="sxs-lookup"><span data-stu-id="41d58-104">Analytic reports in Microsoft Dynamics 365 Talent: Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="41d58-105">Galimos funkcijos:</span><span class="sxs-lookup"><span data-stu-id="41d58-105">Availabe features include:</span></span>

- <span data-ttu-id="41d58-106">**Užduoties analizė**: spustelėkite skirtuką **Analizė**, kad pamatytumėte darbo pretendento darbo metriką.</span><span class="sxs-lookup"><span data-stu-id="41d58-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="41d58-107">**Analizės telkinys:** spustelėkite **Analizė** kairiojoje naršymo srityje, kad būtų galima atlikti suvestines užduotis.</span><span class="sxs-lookup"><span data-stu-id="41d58-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="41d58-108">**Vartotojo lygio sauga**: prieigą prie ataskaitų valdo „Attract“ [vaidmuo](security-attract.md) ir užduoties dalyvio vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="41d58-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="41d58-109">**Kryžminis filtravimas:** spustelėkite vizualizavimą ataskaitoje, kad peržiūrėtumėte kitus rodiklius, atfiltruotus pagal pasirinktus duomenis.</span><span class="sxs-lookup"><span data-stu-id="41d58-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="41d58-110">Šiuo metu naudojama funkcijos [peržiūra](access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="41d58-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="41d58-111">Norėdami ją išbandyti, turite turėti [**Išsamios įdarbinimo informacijos priedą**](attract-comprehensive-hiring.md).</span><span class="sxs-lookup"><span data-stu-id="41d58-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="41d58-112">Visos viešosios peržiūros ataskaitos rodomos anglų kalba.</span><span class="sxs-lookup"><span data-stu-id="41d58-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="41d58-113">Ataskaitos atnaujinamos kas 3 val.</span><span class="sxs-lookup"><span data-stu-id="41d58-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="41d58-114">Paskutinis atnaujinimo laikas (vietinėje lauko juostoje) yra ataskaitos viršuje.</span><span class="sxs-lookup"><span data-stu-id="41d58-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="41d58-115">Atnaujinimo laikas yra apytikslis ir priklauso nuo jūsų regione esančio duomenų kiekio ir išteklių apkrovos.</span><span class="sxs-lookup"><span data-stu-id="41d58-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="41d58-116">Užduočių analizė</span><span class="sxs-lookup"><span data-stu-id="41d58-116">Job Analytics</span></span>

<span data-ttu-id="41d58-117">Užduoties analizės ataskaitos yra samdos konkrečiai samdos užduočiai momentinė kopija.</span><span class="sxs-lookup"><span data-stu-id="41d58-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="41d58-118">Pagrindinę metriką sudaro:</span><span class="sxs-lookup"><span data-stu-id="41d58-118">Key metrics include:</span></span>

- <span data-ttu-id="41d58-119">Aktyvūs pretendentai pagal etapą</span><span class="sxs-lookup"><span data-stu-id="41d58-119">Active applicants by stage</span></span>
- <span data-ttu-id="41d58-120">Pretendento šaltinis</span><span class="sxs-lookup"><span data-stu-id="41d58-120">Applicant source</span></span>
- <span data-ttu-id="41d58-121">Pretendento tipas (vidinis ar išorinis)</span><span class="sxs-lookup"><span data-stu-id="41d58-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="41d58-122">Analizės tranzito punktas</span><span class="sxs-lookup"><span data-stu-id="41d58-122">Analytics Hub</span></span>

<span data-ttu-id="41d58-123">Analizės tranzito punkto ataskaitose pateikiami suvestiniai darbų duomenys, siekiant išsiaiškinti samdos proceso tendencijas.</span><span class="sxs-lookup"><span data-stu-id="41d58-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="41d58-124">„Attract“ sudaro dvi OOTB ataskaitos: galimybių suvestinė ir kanalo analizė.</span><span class="sxs-lookup"><span data-stu-id="41d58-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="41d58-125">Pardavimo galimybių suvestinė</span><span class="sxs-lookup"><span data-stu-id="41d58-125">Pipeline Summary</span></span>

<span data-ttu-id="41d58-126">Pardavimo galimybių suvestinės ataskaita apibendrina siūlomų darbų duomenis.</span><span class="sxs-lookup"><span data-stu-id="41d58-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="41d58-127">Pagrindinę metriką sudaro:</span><span class="sxs-lookup"><span data-stu-id="41d58-127">Key metrics include:</span></span>

- <span data-ttu-id="41d58-128">Pretendentai visose užduotyse pagal etapą</span><span class="sxs-lookup"><span data-stu-id="41d58-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="41d58-129">Pretendento šaltinis</span><span class="sxs-lookup"><span data-stu-id="41d58-129">Applicant source</span></span>
- <span data-ttu-id="41d58-130">Laisvos užduotys pagal paaukštinimo lygį</span><span class="sxs-lookup"><span data-stu-id="41d58-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="41d58-131">Kanalo analizė</span><span class="sxs-lookup"><span data-stu-id="41d58-131">Funnel Analysis</span></span>

<span data-ttu-id="41d58-132">Kanalo analizės ataskaita apibendrina darbo vietų, kurios buvo uždarytos kaip užimtos, duomenis.</span><span class="sxs-lookup"><span data-stu-id="41d58-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="41d58-133">Pagrindinę metriką sudaro:</span><span class="sxs-lookup"><span data-stu-id="41d58-133">Key metrics include:</span></span>

- <span data-ttu-id="41d58-134">Įdarbinimo laiką</span><span class="sxs-lookup"><span data-stu-id="41d58-134">Time to hire</span></span>
- <span data-ttu-id="41d58-135">Konvertavimo metrika (užvedus žymiklį)</span><span class="sxs-lookup"><span data-stu-id="41d58-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="41d58-136">Pasiūlymo priėmimo koeficientas</span><span class="sxs-lookup"><span data-stu-id="41d58-136">Offer acceptance rate</span></span>

<span data-ttu-id="41d58-137">Pastaba: kad įdarbinimo laikp ataskaitos būtų kuo tikslesnės, rekomenduojama naudoti [pasiūlymo valdymą](offer-setup.md), funkciją, kuri yra išsamaus samdos priedo dalis.</span><span class="sxs-lookup"><span data-stu-id="41d58-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="41d58-138">Pabandykite užvesti žymiklį ant vaizdinių elementų, kad gautumėte papildomos informacijos.</span><span class="sxs-lookup"><span data-stu-id="41d58-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="41d58-139">Pavyzdžiui, užvedus žymiklį ant **Aktyvūs pretendentai** parodomas vidutinis etapo dienų skaičius.</span><span class="sxs-lookup"><span data-stu-id="41d58-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="41d58-140">Analizuojant šią informaciją galima gauti įžvalgų, padedančių sutrumpinti įdarbinimo laiką, ir padėti darbdaviams sutrumpinti kiekvieno etapo trukmę.</span><span class="sxs-lookup"><span data-stu-id="41d58-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="41d58-141">Vartotojo lygio sauga</span><span class="sxs-lookup"><span data-stu-id="41d58-141">User-specific security</span></span>

<span data-ttu-id="41d58-142">„Attract“ ataskaitas galima naudoti administratoriaus, skaityti visus, darbdavio ir samdos vadovo [vaidmenims.](security-attract.md)</span><span class="sxs-lookup"><span data-stu-id="41d58-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="41d58-143">Nepriskirtiems vartotojams prieiga prie analizės ataskaitos puslapių (Užduoties analizė arba Analizės tranzito punktas) nesuteikiama.</span><span class="sxs-lookup"><span data-stu-id="41d58-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="41d58-144">Ataskaitose Užduoties analizė pateikiami pasirinktos užduoties duomenys.</span><span class="sxs-lookup"><span data-stu-id="41d58-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="41d58-145">Analizės tranzito punkto ataskaitose apibendrinami visų užduočių duomenys, kuriuos gali peržiūrėti vartotojas.</span><span class="sxs-lookup"><span data-stu-id="41d58-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="41d58-146">Vartotojams, kurie gali peržiūrėti puslapį Mano užduotys ir Visos užduotys, pasiekiami tie patys rodiniai kaip Analizės tranzito punkte.</span><span class="sxs-lookup"><span data-stu-id="41d58-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="41d58-147">Kryžminis filtravimas</span><span class="sxs-lookup"><span data-stu-id="41d58-147">Cross-filter</span></span>

<span data-ttu-id="41d58-148">Vienas iš puikiausių „Power BI“ savybių yra tai visų vaizdinių ataskaitos puslapio elementų ryšys.</span><span class="sxs-lookup"><span data-stu-id="41d58-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="41d58-149">Jei viename iš vaizdinių elementų pasirenkate duomenų tašką, parodomi visi kiti puslapyje esantys vaizdiniai elementai, kuriuose yra duomenų pakeitimai, pagrįsti šiuo pasirinkimu.</span><span class="sxs-lookup"><span data-stu-id="41d58-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="41d58-150">Sužinokite daugiau ir peržiūrėkite pavyzdį, [Kaip atliekamas vaizdinių elementų kryžminis filtravimas „Power BI“ ataskaitoje](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span><span class="sxs-lookup"><span data-stu-id="41d58-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="41d58-151">Eksportuoti į Excel</span><span class="sxs-lookup"><span data-stu-id="41d58-151">Export to Excel</span></span>

<span data-ttu-id="41d58-152">Norėdami peržiūrėti ataskaitos duomenis programoje „Excel“, galite spustelėti parinkčių meniu (tris taškus) ir pasirinkti **Eksportuoti pagrindinius duomenis.**</span><span class="sxs-lookup"><span data-stu-id="41d58-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="41d58-153">Eksportuoti duomenys bus eksportuojami kaip filtruojami, atsižvelgiant į „Attract“ vartotojo teises.</span><span class="sxs-lookup"><span data-stu-id="41d58-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="41d58-154">Norėdami gauti daugiau informacijos, žr. [Duomenų eksportavimas iš vaizdinių elementų](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span><span class="sxs-lookup"><span data-stu-id="41d58-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
