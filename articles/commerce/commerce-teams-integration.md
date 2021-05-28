---
title: „Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c22af9bf76818dd682b4147c3677cd1715e4cbf8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021994"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="fc2de-103">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="fc2de-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fc2de-104">Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga.</span><span class="sxs-lookup"><span data-stu-id="fc2de-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="fc2de-105">„Dynamics 365 Commerce” yra integruojama su „Teams” tam, kad padėtų klientams ir jų darbuotojams padidinti produktyvumą sinchronizuojant užduočių valdymą tarp dviejų programų.</span><span class="sxs-lookup"><span data-stu-id="fc2de-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="fc2de-106">Vientisas užduočių valdymas, kurį suteikia „Commerce” ir „Teams” integravimas, leidžia parduotuvių vadovams ir darbuotojams kurti užduočių sąrašus, priskirti užduotis kelioms parduotuvėms ir sekti parduotuvių užduočių būseną iš bet kurios šių programų.</span><span class="sxs-lookup"><span data-stu-id="fc2de-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="fc2de-107">„Commerce” ir „Teams” integravimas prieinamas „Commerce” 10.0.18 versijos leidime.</span><span class="sxs-lookup"><span data-stu-id="fc2de-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="fc2de-108">Pagrindinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="fc2de-108">Key features</span></span>

<span data-ttu-id="fc2de-109">Štai keletas pagrindinių funkcijų, kurias suteikia „Commerce” ir „Microsoft Teams” integravimas:</span><span class="sxs-lookup"><span data-stu-id="fc2de-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="fc2de-110">„Teams” konfigūravimas naudojantis gerai apibrėžta informacija iš „Commerce”, pavyzdžiui, organizacinė struktūra ir informacija apie parduotuves, darbuotojus, teises bei veiklos kontekstą.</span><span class="sxs-lookup"><span data-stu-id="fc2de-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="fc2de-111">Lengvas vykstančių pakeitimų sinchronizavimas (pavyzdžiui, naujų parduotuvių pridėjimas arba naujų darbuotojų samdymas) tarp „Commerce” ir „Teams”, tačiau „Commerce” turi išlikti pagrindinis organizacinės struktūros duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="fc2de-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="fc2de-112">Užduočių valdymo integravimas tarp „Commerce” ir „Teams” siekiant padėti parduotuvių darbuotojams, vadovams, regioninėms vadovams ir komunikacijos vadovams tvarkytis su užduočių valdymu iš bet kurios šių programų.</span><span class="sxs-lookup"><span data-stu-id="fc2de-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="fc2de-113">Būtinosios integravimo funkcijų naudojimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="fc2de-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="fc2de-114">Prieš pradėdami naudoti „Microsoft Teams” integravimo funkcijas, užtikrinkite šias būtinąsias sąlygas:</span><span class="sxs-lookup"><span data-stu-id="fc2de-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="fc2de-115">„Microsoft 365 Business Standard” licenciją (Ši licencija apima „Teams”.)</span><span class="sxs-lookup"><span data-stu-id="fc2de-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="fc2de-116">„Azure Active Directory” ( „Azure AD”) paskyras visiems parduotuvių vadovams ir darbuotojams</span><span class="sxs-lookup"><span data-stu-id="fc2de-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="fc2de-117">Elektroninio kasos aparato (EKA) sistemas, sukonfigūruotas naudojant „Azure AD” autentifikavimą</span><span class="sxs-lookup"><span data-stu-id="fc2de-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="fc2de-118">Koncepcinė architektūra</span><span class="sxs-lookup"><span data-stu-id="fc2de-118">Conceptual architecture</span></span>

<span data-ttu-id="fc2de-119">Šioje iliustracijoje pateikta koncepcinė „Dynamics 365 Commerce” ir „Microsoft Teams” integravimo architektūra, naudojanti San Fransisko parduotuvę kaip pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="fc2de-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="fc2de-120">Tiek „Teams”, tiek „Commerce” EKA programa naudoja „Microsoft Planner” kaip saugyklą, kad publikuotos užduotys iš „Teams” atsirastų EKA programoje, o specialiosios užduotys, sukurtos parduotuvių vadovų EKA programoje, atsirastų „Teams”, taip sukuriama vientisa užduočių valdymo patirtis tarp programų.</span><span class="sxs-lookup"><span data-stu-id="fc2de-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![„Commerce” ir „Teams” integravimo architektūra](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="fc2de-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="fc2de-122">Additional resources</span></span>

[<span data-ttu-id="fc2de-123">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="fc2de-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="fc2de-124">„Microsoft Teams” parengimas iš „Dynamics 365 Commerce”</span><span class="sxs-lookup"><span data-stu-id="fc2de-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="fc2de-125">Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA</span><span class="sxs-lookup"><span data-stu-id="fc2de-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="fc2de-126">Vartotojų vaidmenų tvarkymas Microsoft Teams” platformoje</span><span class="sxs-lookup"><span data-stu-id="fc2de-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="fc2de-127">Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje</span><span class="sxs-lookup"><span data-stu-id="fc2de-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="fc2de-128">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo DUK</span><span class="sxs-lookup"><span data-stu-id="fc2de-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
