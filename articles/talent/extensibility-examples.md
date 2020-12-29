---
title: „Talent“ išplėtimas su „Power Apps“ ir „Power Automate“
description: Šiame straipsnyje aprašomi keli „Microsoft Dynamics 365 Talent - Attract“ išplėtimo scenarijų pavyzdžiai, kuriuose naudojami „Microsoft Power Apps“ ir „Microsoft Power Automate“.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529639"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="3e54d-103">„Talent“ išplėtimas su „Power Apps“ ir „Power Automate“</span><span class="sxs-lookup"><span data-stu-id="3e54d-103">Extend Talent with Power Apps and Power Automate</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3e54d-104">Šiame straipsnyje aprašomi keli „Microsoft Dynamics 365 Talent: Attract“ išplėtimo scenarijų pavyzdžiai, kuriuose naudojami „Microsoft Power Apps“ ir „Microsoft Power Automate“.</span><span class="sxs-lookup"><span data-stu-id="3e54d-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="3e54d-105">Su kiekvienu pavyzdžiu susietą sprendimų paketą galite importuoti į savo „Power Apps“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="3e54d-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="3e54d-106">Paskui šiais paketais galite naudotis kaip nurodymais arba kaip atskaitos taškais jūsų organizacijai taikomiems scenarijams įgyvendinti.</span><span class="sxs-lookup"><span data-stu-id="3e54d-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e54d-107">Norėdami šiame straipsnyje aprašytus šablonus ir programą naudoti tokius, kokie jie yra, būtinai patikrinkite juos, kad įsitikintumėte, jog jie apima visus jūsų diegimui būdingus scenarijus.</span><span class="sxs-lookup"><span data-stu-id="3e54d-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="3e54d-108">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="3e54d-108">Prerequisites</span></span>

- <span data-ttu-id="3e54d-109">Norėdami importuoti paketus, vartotojai privalo turėti teisę **Aplinkos kūrėjas**.</span><span class="sxs-lookup"><span data-stu-id="3e54d-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="3e54d-110">Norėdami eksportuoti arba importuoti programas, vartotojai privalo turėti „Power Apps“ 2 plano licenciją arba bandomąją „Power Apps“ 2 plano licenciją.</span><span class="sxs-lookup"><span data-stu-id="3e54d-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="3e54d-111">„Power Automate – Form Connect“</span><span class="sxs-lookup"><span data-stu-id="3e54d-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="3e54d-112">**Power Automate – Form Connect** šabloną galima naudoti norint nuskaityti duomenis iš „Microsoft Forms“ ir saugoti juos „Common Data Service“ objekte.</span><span class="sxs-lookup"><span data-stu-id="3e54d-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="3e54d-113">Šį šabloną galima išplėsti, kad jį būtų galima naudoti kitiems scenarijams.</span><span class="sxs-lookup"><span data-stu-id="3e54d-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="3e54d-114">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="3e54d-114">Here are some examples:</span></span>

- <span data-ttu-id="3e54d-115">Kandidatų vertinimų fiksavimas.</span><span class="sxs-lookup"><span data-stu-id="3e54d-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="3e54d-116">Kurso klausimynų rezultatų fiksavimas.</span><span class="sxs-lookup"><span data-stu-id="3e54d-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="3e54d-117">Iš pokalbiuose su personalo išteklių administratoriais pateiktų klausimų sudarytos bibliotekos kompiliavimas.</span><span class="sxs-lookup"><span data-stu-id="3e54d-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="3e54d-118">Kandidato pateikto pokalbio proceso vertinimo fiksavimas</span><span class="sxs-lookup"><span data-stu-id="3e54d-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="3e54d-119">Naudodamiesi „Microsoft Dynamics 365: Attract“, galite naudoti formas kandidatų portale, kuriame kandidatai įveda duomenis.</span><span class="sxs-lookup"><span data-stu-id="3e54d-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="3e54d-120">Užduoties šablone formas galite įdėti ir kaip veiklas.</span><span class="sxs-lookup"><span data-stu-id="3e54d-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="3e54d-121">Kai kandidatas pateikia formą, „Microsoft Power Automate“ užfiksuoja formos pateikimą, nuskaito duomenis ir saugo juos „Common Data Service“ objekte.</span><span class="sxs-lookup"><span data-stu-id="3e54d-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="3e54d-122">Norėdami atsisiųsti **Power Automate – Form Connect** šabloną ir pasirinktinio objekto struktūrą, „Microsoft“ atsisiuntimų centre eikite į [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988).</span><span class="sxs-lookup"><span data-stu-id="3e54d-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="3e54d-123">„Power Automate – SharePoint integravimas“</span><span class="sxs-lookup"><span data-stu-id="3e54d-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="3e54d-124">**Power Automate – SharePoint integravimas** šabloną galima naudoti norint nuskaityti duomenis iš „Microsoft SharePoint“ sąrašo, palyginti sąrašą su bet kurio „Common Data Service“ objekto lauko reikšmėmis ir siųsti palyginimo rezultatus kaip pranešimo el. laišką.</span><span class="sxs-lookup"><span data-stu-id="3e54d-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="3e54d-125">Organizacija gali turėti tam tikrų skubiai reikiamų įgūdžių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="3e54d-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="3e54d-126">Šie įgūdžiai gali būti saugomi „SharePoint“ kaip „SharePoint“ sąrašas.</span><span class="sxs-lookup"><span data-stu-id="3e54d-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="3e54d-127">Kai kandidatas kreipiasi dėl darbo ir norėdamas įsidarbinti turi turėti reikiamų įgūdžių rinkinyje išvardytų įgūdžių, aptikus didelį kandidato įgūdžių sutapimą su „SharePoint“ saugomais įgūdžiais, el. paštu išsiunčiamas pranešimas.</span><span class="sxs-lookup"><span data-stu-id="3e54d-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="3e54d-128">Tokiu būdu pareigoms, kurioms darbuotojų reikia skubiai, jų surandama greičiau, nes naudojantis pranešimais darbdaviams lengviau atlikti kryžminį kandidatų įdarbinimą visoje organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="3e54d-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="3e54d-129">Šį šabloną galima išplėsti, kad jį būtų galima naudoti bet kuriam „SharePoint“ integraciją apimančiam scenarijui.</span><span class="sxs-lookup"><span data-stu-id="3e54d-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="3e54d-130">Norėdami atsisiųsti **Power Automate – SharePoint integravimas** šabloną, eikite į [Power Automate – SharePoint integravimas](https://go.microsoft.com/fwlink/?linkid=2082109) „Microsoft“ atsisiuntimų centre.</span><span class="sxs-lookup"><span data-stu-id="3e54d-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="3e54d-131">Programėlė „Referral”</span><span class="sxs-lookup"><span data-stu-id="3e54d-131">Referral App</span></span>

<span data-ttu-id="3e54d-132">Programėlę „Referral” galite naudoti kandidatams įtraukti į bendrinamą talento telkinį.</span><span class="sxs-lookup"><span data-stu-id="3e54d-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="3e54d-133">Pateikdamas kandidatą, jį rekomendavęs asmuo gali įvesti jo duomenis: **Vardas**, **Pavardė**, **El. pašto adresas** ir **„LinkedIn“ URL**.</span><span class="sxs-lookup"><span data-stu-id="3e54d-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="3e54d-134">Kandidato šaltinio metaduomenys yra įvedami kartu su jį rekomendavusio asmens informacija.</span><span class="sxs-lookup"><span data-stu-id="3e54d-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="3e54d-135">Galite įterpti šią programą į darbuotojų savitarną teikti rekomendacijoms arba galite naudoti ją kaip hipersaitą įmonės portale ir vykdyti kaip atskirą programą.</span><span class="sxs-lookup"><span data-stu-id="3e54d-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="3e54d-136">Norėdami atsisiųsti **programėlę „Referral”**, eikite į [Dynamics 365 Talent išplečiamumo sprendimas: programėlė „Referral”](https://www.microsoft.com/download/details.aspx?id=58497) „Microsoft” atsisiuntimo centre.</span><span class="sxs-lookup"><span data-stu-id="3e54d-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="3e54d-137">Galite importuoti šią programėlę ir pritaikyti papildomų funkcijų įtraukimui.</span><span class="sxs-lookup"><span data-stu-id="3e54d-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e54d-138">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3e54d-138">Additional resources</span></span>

[<span data-ttu-id="3e54d-139">„Microsoft Power Platform“</span><span class="sxs-lookup"><span data-stu-id="3e54d-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="3e54d-140">Programos perkėlimas įvairiems nuomotojams ir į įvairias aplinkas</span><span class="sxs-lookup"><span data-stu-id="3e54d-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
