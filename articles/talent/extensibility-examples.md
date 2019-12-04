---
title: „Talent“ išplėtimas su „Power Apps“ ir „Power Automate“
description: Šiame skyriuje aprašomi keli „Microsoft Dynamics 365 Talent“ išplėtimo scenarijų pavyzdžiai, kuriuose naudojami „Microsoft Power Apps“ ir „Microsoft Power Automate“.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 3bb61297e294aa3f2d06f542bebe29d7afae9c3b
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832843"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="f921e-103">„Talent“ išplėtimas su „Power Apps“ ir „Power Automate“</span><span class="sxs-lookup"><span data-stu-id="f921e-103">Extend Talent with Power Apps and Power Automate</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f921e-104">Šiame skyriuje aprašomi keli „Microsoft Dynamics 365 Talent“ išplėtimo scenarijų pavyzdžiai, kuriuose naudojami „Microsoft Power Apps“ ir „Microsoft Power Automate“.</span><span class="sxs-lookup"><span data-stu-id="f921e-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="f921e-105">Su kiekvienu pavyzdžiu susietą sprendimų paketą galite importuoti į savo „Power Apps“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="f921e-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="f921e-106">Paskui šiais paketais galite naudotis kaip nurodymais arba kaip atskaitos taškais jūsų organizacijai taikomiems scenarijams įgyvendinti.</span><span class="sxs-lookup"><span data-stu-id="f921e-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f921e-107">Norėdami šioje temoje aprašytus šablonus ir programą naudoti tokius, kokie jie yra, būtinai patikrinkite juos, kad įsitikintumėte, jog jie apima visus jūsų diegimui būdingus scenarijus.</span><span class="sxs-lookup"><span data-stu-id="f921e-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="f921e-108">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="f921e-108">Prerequisites</span></span>

- <span data-ttu-id="f921e-109">Norėdami importuoti paketus, vartotojai privalo turėti teisę **Aplinkos kūrėjas**.</span><span class="sxs-lookup"><span data-stu-id="f921e-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="f921e-110">Norėdami eksportuoti arba importuoti programas, vartotojai privalo turėti „Power Apps“ 2 plano licenciją arba bandomąją „Power Apps“ 2 plano licenciją.</span><span class="sxs-lookup"><span data-stu-id="f921e-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="f921e-111">„Power Automate – Form Connect“</span><span class="sxs-lookup"><span data-stu-id="f921e-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="f921e-112">**Power Automate – Form Connect** šabloną galima naudoti norint nuskaityti duomenis iš „Microsoft Forms“ ir saugoti juos „Common Data Service“ objekte.</span><span class="sxs-lookup"><span data-stu-id="f921e-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="f921e-113">Šį šabloną galima išplėsti, kad jį būtų galima naudoti kitiems scenarijams.</span><span class="sxs-lookup"><span data-stu-id="f921e-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="f921e-114">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="f921e-114">Here are some examples:</span></span>

- <span data-ttu-id="f921e-115">Kandidatų vertinimų fiksavimas.</span><span class="sxs-lookup"><span data-stu-id="f921e-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="f921e-116">Kurso klausimynų rezultatų fiksavimas.</span><span class="sxs-lookup"><span data-stu-id="f921e-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="f921e-117">Iš pokalbiuose su personalo išteklių administratoriais pateiktų klausimų sudarytos bibliotekos kompiliavimas.</span><span class="sxs-lookup"><span data-stu-id="f921e-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="f921e-118">Kandidato pateikto pokalbio proceso vertinimo fiksavimas</span><span class="sxs-lookup"><span data-stu-id="f921e-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="f921e-119">Naudojantis „Microsoft Dynamics 365: Attract“, formos gali būti rodomos kandidatų portale ir kandidatai gali įvesti duomenis.</span><span class="sxs-lookup"><span data-stu-id="f921e-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="f921e-120">Užduoties šablone formas galima įdėti ir kaip veiklas.</span><span class="sxs-lookup"><span data-stu-id="f921e-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="f921e-121">Kai kandidatas pateikia formą, „Microsoft Power Automate“ užfiksuoja formos pateikimą, nuskaito duomenis ir saugo juos „Common Data Service“ objekte.</span><span class="sxs-lookup"><span data-stu-id="f921e-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="f921e-122">Norėdami atsisiųsti **Power Automate – Form Connect** šabloną ir pasirinktinio objekto struktūrą, „Microsoft“ atsisiuntimų centre eikite į [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988).</span><span class="sxs-lookup"><span data-stu-id="f921e-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a><span data-ttu-id="f921e-123">Parametrų, perduotų „ Power Apps“, inicijavimas ir ištraukimas</span><span class="sxs-lookup"><span data-stu-id="f921e-123">Initiate and Extract Parameters Passed to Power Apps</span></span>

<span data-ttu-id="f921e-124">Šabloną **Parametrų, perduotų „Power Apps**“, inicijavimas ir ištraukimas“ galima naudoti kaip kiekvieno „Power Apps“ scenarijaus, kuris yra būdingas „Attract“, pradžios tašką.</span><span class="sxs-lookup"><span data-stu-id="f921e-124">The **Initiate and Extract Parameters Passed to Power Apps** template can be used as a starting point for any Power Apps scenario that is specific to Attract.</span></span> <span data-ttu-id="f921e-125">Jis apima visus numatytuosius „Attract“ perduodamus parametrus, pavyzdžiui, **Prašymas įdarbinti**, **Kandidato ID** ir **JobID**.</span><span class="sxs-lookup"><span data-stu-id="f921e-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="f921e-126">Naudojantis šiuo šablonu galima gauti kandidato vertinimo formą, kad samdos vadovas galėtų peržiūrėti kandidato užpildytą vertinimo formą.</span><span class="sxs-lookup"><span data-stu-id="f921e-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="f921e-127">Naudojant „Power Apps“ sukurtas programas galima įdėti į „Attract“ užduoties šabloną.</span><span class="sxs-lookup"><span data-stu-id="f921e-127">Apps that are created by using Power Apps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="f921e-128">Norėdami atsisiųsti **Parametrų, perduotų „Power Apps“, inicijavimas ir ištraukimas** šabloną ir pasirinktinio objekto struktūrą, eikite į [Parametrų, perduotų „Power Apps“, inicijavimas ir ištraukimas](https://go.microsoft.com/fwlink/?linkid=2081991) „Microsoft“ atsisiuntimų centre.</span><span class="sxs-lookup"><span data-stu-id="f921e-128">To download the **Initiate and Extract Parameters Passed to Power Apps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="f921e-129">Integravimas su „Office 365“</span><span class="sxs-lookup"><span data-stu-id="f921e-129">Integration with Office 365</span></span>

<span data-ttu-id="f921e-130">Naudojantis programa **Integravimas su „Office 365“**, iš „Microsoft Office 365“ galima gauti prisijungusių vartotojų komandos informaciją.</span><span class="sxs-lookup"><span data-stu-id="f921e-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="f921e-131">Nurodomi „Talent“ darbuotojai, kurių atėjimo į darbą ir išėjimo iš darbo duomenys bei išimčių įrašai gaunami.</span><span class="sxs-lookup"><span data-stu-id="f921e-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="f921e-132">Atėjimo į darbą ir išėjimo iš darbo duomenys saugomi pasirinktiniame „Common Data Service“ objekte.</span><span class="sxs-lookup"><span data-stu-id="f921e-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="f921e-133">Daroma prielaida, kad šiuos duomenis įveda trečiųjų šalių sistemos naudodamosi integravimu.</span><span class="sxs-lookup"><span data-stu-id="f921e-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="f921e-134">Šią programą galima išplėsti, kad ją būtų galima naudoti kitiems scenarijams.</span><span class="sxs-lookup"><span data-stu-id="f921e-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="f921e-135">Pavyzdžiui, naudojantis ja gali būti rodoma komandos atostogų informaciją, kalendoriaus įvykiai ir visi konkrečios komandos įvykiai.</span><span class="sxs-lookup"><span data-stu-id="f921e-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="f921e-136">Norėdami atsisiųsti programą **Integravimas su „Office 365“** ir pasirinktinę objekto struktūrą, „Microsoft“ atsisiuntimo centre eikite į [Integravimas su „Office 365“](https://go.microsoft.com/fwlink/?linkid=2081787).</span><span class="sxs-lookup"><span data-stu-id="f921e-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--email-notification"></a><span data-ttu-id="f921e-137">„Power Automate – el. laiško pranešimas“</span><span class="sxs-lookup"><span data-stu-id="f921e-137">Power Automate – Email Notification</span></span>

<span data-ttu-id="f921e-138">**Power Automate – el. laiško pranešimas** šabloną galima naudoti el. laiškų pranešimų scenarijams.</span><span class="sxs-lookup"><span data-stu-id="f921e-138">The **Power Automate – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="f921e-139">Juo naudojantis galima suaktyvinti el. paštu kandidatams siunčiamus pranešimus, kai samdos komanda bet kuriame įdarbinimo proceso etape juos atmeta.</span><span class="sxs-lookup"><span data-stu-id="f921e-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="f921e-140">Šį šabloną galima išplėsti, kad būtų galima sekti kandidato įdarbinimo proceso etapo pokyčius ir siųsti pranešimus samdos komandai ir kandidatui.</span><span class="sxs-lookup"><span data-stu-id="f921e-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="f921e-141">Apskritai, jei objektai saugomi „Common Data Service“, galima nustatyti, kad srautai siųstų pranešimus apie „Core HR“, „Attract“ arba „Onboard“ įvykius.</span><span class="sxs-lookup"><span data-stu-id="f921e-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Onboard.</span></span>

<span data-ttu-id="f921e-142">Norėdami atsisiųsti **Power Automate – el. laiško pranešimas** šabloną, „Microsoft“ atsisiuntimų centre eikite į [Power Automate – el. laiško pranešimas](https://go.microsoft.com/fwlink/?linkid=2082103).</span><span class="sxs-lookup"><span data-stu-id="f921e-142">To download the **Power Automate – Email Notification** template, go to [Power Automate – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="f921e-143">„Power Automate – SQL prisijungimas ir vykdymas“</span><span class="sxs-lookup"><span data-stu-id="f921e-143">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="f921e-144">**Power Automate – SQL prisijungimas ir vykdymas** šablonas prisijungia prie „Microsoft SQL Server“ ir leidžia vykdyti SQL užklausas.</span><span class="sxs-lookup"><span data-stu-id="f921e-144">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="f921e-145">Nors šis šablonas skirtas SQL lentelėms skaityti ir naujinti, jį galima išplėsti, kad jį galima būtų naudoti kitiems scenarijams.</span><span class="sxs-lookup"><span data-stu-id="f921e-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="f921e-146">Pavyzdžiui, jį galima naudoti „Common Data Service“ išdėstymo lentelėje norint įvesti duomenis iš SQL serverio ir periodiškai sinchronizuojant išdėstymo lentelę naudojantis papildančiuoju skirstymu iš SQL serverio.</span><span class="sxs-lookup"><span data-stu-id="f921e-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="f921e-147">Norėdami atsisiųsti **Power Automate – SQL prisijungimas ir vykdymas** šabloną, „Microsoft“ atsisiuntimų centre eikite į [Power Automate – SQL prisijungimas ir vykdymas](https://go.microsoft.com/fwlink/?linkid=2081789).</span><span class="sxs-lookup"><span data-stu-id="f921e-147">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="f921e-148">„Power Automate – SharePoint integravimas“</span><span class="sxs-lookup"><span data-stu-id="f921e-148">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="f921e-149">**Power Automate – SharePoint integravimas** šabloną galima naudoti norint nuskaityti duomenis iš „Microsoft SharePoint“ sąrašo, palyginti sąrašą su bet kurio „Common Data Service“ objekto lauko reikšmėmis ir siųsti palyginimo rezultatus kaip pranešimo el. laišką.</span><span class="sxs-lookup"><span data-stu-id="f921e-149">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="f921e-150">Organizacija gali turėti tam tikrų skubiai reikiamų įgūdžių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f921e-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="f921e-151">Šie įgūdžiai gali būti saugomi „SharePoint“ kaip „SharePoint“ sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f921e-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="f921e-152">Kai kandidatas kreipiasi dėl darbo ir norėdamas įsidarbinti turi turėti reikiamų įgūdžių rinkinyje išvardytų įgūdžių, aptikus didelį kandidato įgūdžių sutapimą su „SharePoint“ saugomais įgūdžiais, el. paštu išsiunčiamas pranešimas.</span><span class="sxs-lookup"><span data-stu-id="f921e-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="f921e-153">Tokiu būdu pareigoms, kurioms darbuotojų reikia skubiai, jų surandama greičiau, nes naudojantis pranešimais darbdaviams lengviau ieškoti kandidatų visoje organizacijoje ir atlikti kryžminį įdarbinimą.</span><span class="sxs-lookup"><span data-stu-id="f921e-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="f921e-154">Šį šabloną galima išplėsti, kad jį būtų galima naudoti bet kuriam „SharePoint“ integraciją apimančiam scenarijui.</span><span class="sxs-lookup"><span data-stu-id="f921e-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="f921e-155">Norėdami atsisiųsti **Power Automate – SharePoint integravimas** šabloną, eikite į [Power Automate – SharePoint integravimas](https://go.microsoft.com/fwlink/?linkid=2082109) „Microsoft“ atsisiuntimų centre.</span><span class="sxs-lookup"><span data-stu-id="f921e-155">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="f921e-156">Programėlė „Referral”</span><span class="sxs-lookup"><span data-stu-id="f921e-156">Referral App</span></span>
<span data-ttu-id="f921e-157">Programėlę „Referral” galite naudoti kandidatams įtraukti į bendrinamą talento telkinį.</span><span class="sxs-lookup"><span data-stu-id="f921e-157">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="f921e-158">Pateikdamas kandidatą, jį rekomendavęs asmuo gali įvesti jo **vardą**, **pavardę**, **el. pašto adresą** ir **„LinkedIn“ URL**.</span><span class="sxs-lookup"><span data-stu-id="f921e-158">The referrer can enter **Firstname**, **Lastname**, **Email**, and **Linkedln URL** when submitting a candidate.</span></span> <span data-ttu-id="f921e-159">Kandidato šaltinio metaduomenys yra įvedami kartu su jį rekomendavusio asmens informacija.</span><span class="sxs-lookup"><span data-stu-id="f921e-159">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="f921e-160">Galite įterpti šią programėlę į darbuotojų savitarną (ESS) teikti rekomendacijoms arba galite naudoti ją kaip hipersaitą įmonės portale ir vykdyti kaip atskirą programėlę.</span><span class="sxs-lookup"><span data-stu-id="f921e-160">You can embed this app in Employee self-service (ESS) for submitting referrals, or you can be use it as a hyperlink in the Corporate Portal and run as a stand-alone app.</span></span>

<span data-ttu-id="f921e-161">Norėdami atsisiųsti **programėlę „Referral”**, eikite į [Dynamics 365 Talent išplečiamumo sprendimas: programėlė „Referral”](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) „Microsoft” atsisiuntimo centre.</span><span class="sxs-lookup"><span data-stu-id="f921e-161">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) on the Microsoft Download Center.</span></span> <span data-ttu-id="f921e-162">Galite importuoti šią programėlę ir pritaikyti papildomų funkcijų įtraukimui.</span><span class="sxs-lookup"><span data-stu-id="f921e-162">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f921e-163">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f921e-163">Additional resources</span></span>

[<span data-ttu-id="f921e-164">„Microsoft Power Platform“</span><span class="sxs-lookup"><span data-stu-id="f921e-164">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="f921e-165">Programos perkėlimas įvairiems nuomotojams ir į įvairias aplinkas</span><span class="sxs-lookup"><span data-stu-id="f921e-165">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
