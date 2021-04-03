---
title: Darbo laiko kalendoriaus kūrimas
description: Darbo laiko kalendoriaus, šventinių dienų ir ne darbo laiko nustatymas programoje „Dynamics 365 Human Resources“.
author: andreabichsel
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ecabac54134629074ac01944963a037c2cdc63c9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467174"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="90ace-103">Darbo laiko kalendoriaus kūrimas</span><span class="sxs-lookup"><span data-stu-id="90ace-103">Create a working time calendar</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="90ace-104">Darbo laiko kalendoriuje programoje „Dynamics 365 Human Resources“ rodomos dienos ir valandos, kurias darbuotojai dirba jūsų organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="90ace-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="90ace-105">Pateikdamas atostogų užklausą, darbuotojas neturi nerimauti dėl švenčių ir nedarbo dienų.</span><span class="sxs-lookup"><span data-stu-id="90ace-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="90ace-106">Norėdami racionalizuoti atostogų užklausas, konfigūruokite šiuos elementus savo organizacijoje:</span><span class="sxs-lookup"><span data-stu-id="90ace-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="90ace-107">Darbo laiko kalendorius</span><span class="sxs-lookup"><span data-stu-id="90ace-107">Working time calendar</span></span>
- <span data-ttu-id="90ace-108">Šventės ir nedarbo dienos</span><span class="sxs-lookup"><span data-stu-id="90ace-108">Holidays and closures</span></span>
- <span data-ttu-id="90ace-109">Ne darbo laikas</span><span class="sxs-lookup"><span data-stu-id="90ace-109">Non-work time</span></span>

<span data-ttu-id="90ace-110">Nustatydami darbo laiko kalendorių, galite pridėti paskutinius du elementus.</span><span class="sxs-lookup"><span data-stu-id="90ace-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="90ace-111">Taip pat galite juos konfigūruoti arba atnaujinti atskirai.</span><span class="sxs-lookup"><span data-stu-id="90ace-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="90ace-112">Darbo laiko kalendoriaus nustatymas</span><span class="sxs-lookup"><span data-stu-id="90ace-112">Set up a working time calendar</span></span>

<span data-ttu-id="90ace-113">Nustatykite bent vieną darbo kalendorių, kuriame parodytos darbo dienos ir valandos.</span><span class="sxs-lookup"><span data-stu-id="90ace-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="90ace-114">Jeigu jūsų darbo vietos yra keliose šalyse ir regionuose, galite nustatyti kiekvienos vietos darbo laiko kalendorių.</span><span class="sxs-lookup"><span data-stu-id="90ace-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="90ace-115">Puslapyje **Organizacijos administravimas** pasirinkite **Kalendorius**.</span><span class="sxs-lookup"><span data-stu-id="90ace-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="90ace-116">Pasirinkite **Naujas** ir įveskite kalendoriaus pavadinimą bei aprašą.</span><span class="sxs-lookup"><span data-stu-id="90ace-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="90ace-117">Dalyje **Generavimo pasirinktys** pasirinkite savo organizacijos darbo dienas ir įveskite darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="90ace-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="90ace-118">Norėdami pridėti švenčių ar nedarbo dienų, pasirinkite šalia dalies **Šventės ir darbo dienos** esantį mygtuką **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="90ace-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="90ace-119">Norėdami pridėti ne darbo laiką, pvz., pietus arba pertraukas, pasirinkite **Pridėti** dalyje **NE DARBO LAIKAS** ir įveskite pavadinimą ir laiko intervalą.</span><span class="sxs-lookup"><span data-stu-id="90ace-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="90ace-120">Dalyje **Dienos** pasirinkite **Generuoti**, kad sugeneruotumėte dienų kalendorių.</span><span class="sxs-lookup"><span data-stu-id="90ace-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="90ace-121">Įveskite kalendoriaus datų intervalą, tada pasirinkite **Generuoti dienas**.</span><span class="sxs-lookup"><span data-stu-id="90ace-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="90ace-122">Norėdami pridėti darbo grafikus, dalyje **Darbo grafikas** pasirinkite **Pridėti** ir įveskite kiekvieno darbo grafiko laiką.</span><span class="sxs-lookup"><span data-stu-id="90ace-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="90ace-123">Švenčių ir nedarbo dienų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="90ace-123">Configure holidays and closures</span></span>

<span data-ttu-id="90ace-124">Galite pridėti arba keisti šventes ir nedarbo dienas atskirai nuo darbo laiko kalendoriaus.</span><span class="sxs-lookup"><span data-stu-id="90ace-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="90ace-125">Puslapyje **Organizacijos administravimas** pasirinkite **Šventės ir nedarbo dienos**.</span><span class="sxs-lookup"><span data-stu-id="90ace-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="90ace-126">Pasirinkite **Nauja** ir įveskite šventės ar nedarbo dienos pavadinimą bei datą.</span><span class="sxs-lookup"><span data-stu-id="90ace-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="90ace-127">Ne darbo laiko konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="90ace-127">Configure non-work time</span></span>

<span data-ttu-id="90ace-128">Galite pridėti arba keisti ne darbo laiką atskirai nuo darbo laiko kalendoriaus.</span><span class="sxs-lookup"><span data-stu-id="90ace-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="90ace-129">Puslapyje **Organizacijos administravimas** pasirinkite **Ne darbo laikas**.</span><span class="sxs-lookup"><span data-stu-id="90ace-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="90ace-130">Pasirinkite **Naujas** ir įveskite ne darbo laiko pavadinimą bei laiko intervalą.</span><span class="sxs-lookup"><span data-stu-id="90ace-130">Select **New** and enter a name and time range for the non-work time.</span></span>

<span data-ttu-id="90ace-131">Jeigu įgalinote atostogų ir neatvykimų koregavimų peržiūros funkciją, „Human Resources“ naudoja atostogų ir nedarbo dienų datas, kad nustatytų dienų, kurias reikia koreguoti kalendoriuje užregistruotiems darbuotojams, skaičių.</span><span class="sxs-lookup"><span data-stu-id="90ace-131">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="90ace-132">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="90ace-132">See also</span></span>

- [<span data-ttu-id="90ace-133">Atostogų ir neatvykimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="90ace-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="90ace-134">Atostogų ir neatvykimų tipai konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="90ace-134">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]