---
title: „Talent“ išplėtimas su „Power Apps“ ir „Power Automate“
description: Šiame straipsnyje aprašomi keli „Microsoft Dynamics 365 Human Resources“ išplėtimo scenarijų pavyzdžiai, kuriuose naudojami „Microsoft Power Apps“ ir „Microsoft Power Automate“.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: Dynamics 365 Human Resources;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8d4185b958ed35e9d2bc764db8ea77b3a2f53c37
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029870"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="0f639-103">Išplėtimas su „Power Apps“ ir „Power Automate“</span><span class="sxs-lookup"><span data-stu-id="0f639-103">Extend with Power Apps and Power Automate</span></span>

<span data-ttu-id="0f639-104">Šiame straipsnyje aprašomi keli „Microsoft Dynamics 365 Human Resources“ išplėtimo scenarijų pavyzdžiai, kuriuose naudojami „Microsoft Power Apps“ ir „Microsoft Power Automate“.</span><span class="sxs-lookup"><span data-stu-id="0f639-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="0f639-105">Su kiekvienu pavyzdžiu susietą sprendimų paketą galite importuoti į savo „Power Apps“ aplinką.</span><span class="sxs-lookup"><span data-stu-id="0f639-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="0f639-106">Paskui šiais paketais galite naudotis kaip nurodymais arba kaip atskaitos taškais jūsų organizacijai taikomiems scenarijams įgyvendinti.</span><span class="sxs-lookup"><span data-stu-id="0f639-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f639-107">Norėdami šioje temoje aprašytus šablonus ir programas naudoti tokius, kokie jie yra, būtinai patikrinkite juos, kad įsitikintumėte, jog jie apima visus jūsų diegimui būdingus scenarijus.</span><span class="sxs-lookup"><span data-stu-id="0f639-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0f639-108">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="0f639-108">Prerequisites</span></span>

- <span data-ttu-id="0f639-109">Norėdami importuoti paketus, vartotojai privalo turėti teisę **Aplinkos kūrėjas**.</span><span class="sxs-lookup"><span data-stu-id="0f639-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="0f639-110">Norėdami eksportuoti arba importuoti programas, vartotojai privalo turėti „Power Apps“ 2 plano licenciją arba bandomąją „Power Apps“ 2 plano licenciją.</span><span class="sxs-lookup"><span data-stu-id="0f639-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-office-365-power-automate"></a><span data-ttu-id="0f639-111">Integravimas su „Office 365“, „Power Automate“</span><span class="sxs-lookup"><span data-stu-id="0f639-111">Integration with Office 365, Power Automate</span></span>

<span data-ttu-id="0f639-112">Naudojantis programa **Integravimas su „Office 365“**, iš „Microsoft Office 365“ galima gauti prisijungusių vartotojų komandos informaciją.</span><span class="sxs-lookup"><span data-stu-id="0f639-112">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="0f639-113">Nurodomi „Human Resources“ darbuotojai, kurių darbuotojų identifikacijos tipai bus gaunami.</span><span class="sxs-lookup"><span data-stu-id="0f639-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="0f639-114">Vadybininkai gali patikrinti darbuotojų ID tipų galiojimo pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="0f639-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="0f639-115">Jie taip pat gali nusiųsti priminimą el. paštu, jei darbuotojo ID tipo galiojimas greitai pasibaigs.</span><span class="sxs-lookup"><span data-stu-id="0f639-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="0f639-116">„Power Automate“ integruojama su „Power Apps“, kad būtų galima išsiųsti šį priminimą.</span><span class="sxs-lookup"><span data-stu-id="0f639-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="0f639-117">Nusiuntus priminimą, patvirtinimas bus atsiųstas atgal į „Power Apps“ iš „Power Automate“.</span><span class="sxs-lookup"><span data-stu-id="0f639-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="0f639-118">Identifikavimo tipai yra vairuotojo pažymėjimas, pasas ir kitos priimtinos tapatybės nustatymo formos.</span><span class="sxs-lookup"><span data-stu-id="0f639-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="0f639-119">Galite naudoti šią programą ir kituose scenarijuose.</span><span class="sxs-lookup"><span data-stu-id="0f639-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="0f639-120">Pavyzdžiui, galite ją naudoti, kad būtų rodoma komandos atostogų informaciją, kalendoriaus įvykiai ir visi konkrečios komandos įvykiai.</span><span class="sxs-lookup"><span data-stu-id="0f639-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="0f639-121">Norėdami atsisiųsti **integravimo su „Office 365“ programą „Power Automate“**, „Microsoft“ atsisiuntimo centre eikite į skyrių [Integravimas su „Office 365“](https://go.microsoft.com/fwlink/?linkid=2081787).</span><span class="sxs-lookup"><span data-stu-id="0f639-121">To download the **Integration with Office 365, Power Automate** app, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="0f639-122">„Power Automate – SQL prisijungimas ir vykdymas“</span><span class="sxs-lookup"><span data-stu-id="0f639-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="0f639-123">**Power Automate – SQL prisijungimas ir vykdymas** šablonas prisijungia prie „Microsoft SQL Server“ ir leidžia vykdyti SQL užklausas.</span><span class="sxs-lookup"><span data-stu-id="0f639-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="0f639-124">Nors šis šablonas skaito ir atnaujina SQL lenteles, taip pat galite jį naudoti kituose scenarijuose.</span><span class="sxs-lookup"><span data-stu-id="0f639-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="0f639-125">Pavyzdžiui, jį galima naudoti „Common Data Service“ išdėstymo lentelėje norint įvesti duomenis iš SQL serverio ir periodiškai sinchronizuojant išdėstymo lentelę naudojantis papildančiuoju skirstymu iš SQL serverio.</span><span class="sxs-lookup"><span data-stu-id="0f639-125">For example, you can use it to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="0f639-126">Išplėstinė užklausa yra integruota su srautu, kad būtų įjungtas duomenų perkėlimas ir papildantysis skirstymas.</span><span class="sxs-lookup"><span data-stu-id="0f639-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="0f639-127">Norėdami atsisiųsti **Power Automate – SQL prisijungimas ir vykdymas** šabloną, „Microsoft“ atsisiuntimų centre eikite į [Power Automate – SQL prisijungimas ir vykdymas](https://go.microsoft.com/fwlink/?linkid=2081789).</span><span class="sxs-lookup"><span data-stu-id="0f639-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f639-128">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0f639-128">Additional resources</span></span>

[<span data-ttu-id="0f639-129">„Microsoft Power Platform“</span><span class="sxs-lookup"><span data-stu-id="0f639-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="0f639-130">Programos perkėlimas įvairiems nuomotojams ir į įvairias aplinkas</span><span class="sxs-lookup"><span data-stu-id="0f639-130">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)