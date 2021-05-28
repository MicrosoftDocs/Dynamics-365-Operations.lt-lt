---
title: Regulatory Configuration Service
description: Šioje temoje pateikiama „Regulatory Configuration Service” (RCS) galimybių apžvalga ir paaiškinama, kaip pasiekti paslaugą.
author: JaneA07
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1eeac7217290e0583fcecdf5b4b5b9153d266240
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019399"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="2e523-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="2e523-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e523-104">„Regulatory Configuration Service” (RCS) yra atskira dizaino ir ciklo valdymo paslauga, skirta „jokio kodo”/„mažai kodų” globalizavimo funkcijai.</span><span class="sxs-lookup"><span data-stu-id="2e523-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="2e523-105">RCS leidžia globalizavimo suinteresuotosioms šalims be programų kūrėjų dalyvavimo išplėsti ir tinkinti mokesčių, elektroninių SF išrašymo, teisės aktų nustatytų ataskaitų, bankininkystės ir verslo dokumentų pagrindines globalizavimo sritis.</span><span class="sxs-lookup"><span data-stu-id="2e523-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="2e523-106">Dėl šio „jokio kodo”/„mažai kodų” globalizavimo požiūrio, globalizavimas yra paprastesnis, greitesnis ir ekonomiškesnis kūrimui ir išplėtimui.</span><span class="sxs-lookup"><span data-stu-id="2e523-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="2e523-107">„RCS” suteikia šias galimybes:</span><span class="sxs-lookup"><span data-stu-id="2e523-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="2e523-108">Visų Elektroninių ataskaitų (ER) suteikiamų funkcijų palaikymą.</span><span class="sxs-lookup"><span data-stu-id="2e523-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="2e523-109">Būtinuosius naujų globalizavimo mikropaslaugų konfigūravimo komponentus.</span><span class="sxs-lookup"><span data-stu-id="2e523-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="2e523-110">Elektroninių sąskaitų faktūrų išrašymo palaikymą.</span><span class="sxs-lookup"><span data-stu-id="2e523-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="2e523-111">Daugiau informacijos rasite [Elektroninių sąskaitų faktūrų išrašymas](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="2e523-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="2e523-112">Mokesčių skaičiavimo palaikymą.</span><span class="sxs-lookup"><span data-stu-id="2e523-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="2e523-113">Daugiau informacijos rasite [Mokesčių paslauga](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="2e523-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="2e523-114">Naujų globalizavimo funkcijų, kurios supaprastina kelių komponentų funkcijų ciklo valdymą ir suteikia daugiau galimybių konfigūruoti veiksmus ir nustatyti funkcijų parametrus palaikymą.</span><span class="sxs-lookup"><span data-stu-id="2e523-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="2e523-115">Daugiau informacijos rasite [„Regulatory Configuration Service” – supaprastintas globalizavimo funkcijų valdymas, skirtas globalizavimo paslaugoms](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="2e523-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="2e523-116">Pasirinktinių konfigūracijų centralizuoto skelbimo, saugojimo ir bendrinimo bendrojoje saugykloje, kurie supaprastina konfigūracijų valdymą nenaudojant „Microsoft Dynamics Lifecycle Services” (LCS), palaikymą.</span><span class="sxs-lookup"><span data-stu-id="2e523-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="2e523-117">RCS prieiga</span><span class="sxs-lookup"><span data-stu-id="2e523-117">Access RCS</span></span>

<span data-ttu-id="2e523-118">Galite užsiregistruoti arba prisijungti prie RCS iš [„Regulatory Configuration Service” puslapio](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="2e523-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![RCS registravimasis/prisijungimas](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="2e523-120">Puslapyje **„Regulatory Configuration Service”** peržiūrėkite ir priimkite papildomas paslaugos naudojimo sąlygas ir pasirinkite vieną iš šių mygtukų:</span><span class="sxs-lookup"><span data-stu-id="2e523-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="2e523-121">**Registruotis**, jei pirmą kartą naudojatės paslauga ir naudojate darbo el. pašto adresą, kad savo organizacijai parengtumėte paslaugų aplinką</span><span class="sxs-lookup"><span data-stu-id="2e523-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="2e523-122">**Prisijungti**, jeigu anksčiau buvote prisiregistravę prie paslaugos ir norite pasiekti savo organizacijos aplinką</span><span class="sxs-lookup"><span data-stu-id="2e523-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="2e523-123">Regioninis prieinamumas</span><span class="sxs-lookup"><span data-stu-id="2e523-123">Regional availability</span></span>

<span data-ttu-id="2e523-124">RCS yra bendrai prieinamas šiuose regionuose:</span><span class="sxs-lookup"><span data-stu-id="2e523-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="2e523-125">Jungtinės Valstijos</span><span class="sxs-lookup"><span data-stu-id="2e523-125">United States</span></span>
- <span data-ttu-id="2e523-126">Indija</span><span class="sxs-lookup"><span data-stu-id="2e523-126">India</span></span>
- <span data-ttu-id="2e523-127">Prancūzija</span><span class="sxs-lookup"><span data-stu-id="2e523-127">France</span></span>
- <span data-ttu-id="2e523-128">Europa</span><span class="sxs-lookup"><span data-stu-id="2e523-128">Europe</span></span>

<span data-ttu-id="2e523-129">Pilną regionų sąrašą rasite [„Dynamics 365” ir „Power Platform”: Pasiekiamumas, duomenų vieta, kalba ir lokalizavimas](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="2e523-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="2e523-130">Susijusi RCS dokumentacija</span><span class="sxs-lookup"><span data-stu-id="2e523-130">Related RCS documentation</span></span>

<span data-ttu-id="2e523-131">Daugiau informacijos apie susijusius komponentus rasite šioje dokumentacijoje:</span><span class="sxs-lookup"><span data-stu-id="2e523-131">For more information about related components, see the following documentation:</span></span>

- <span data-ttu-id="2e523-132">**Bendroji saugykla:**</span><span class="sxs-lookup"><span data-stu-id="2e523-132">**Global repository:**</span></span>

    - [<span data-ttu-id="2e523-133">ER konfigūracijos kūrimas ir įkėlimas į Bendrąją saugyklą</span><span class="sxs-lookup"><span data-stu-id="2e523-133">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="2e523-134">Konfigūracijos bendrinimas Bendrojoje saugykloje</span><span class="sxs-lookup"><span data-stu-id="2e523-134">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="2e523-135">Išplėstinis filtravimas Bendrojoje saugykloje</span><span class="sxs-lookup"><span data-stu-id="2e523-135">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="2e523-136">ER konfigūracijų atsisiuntimas iš Bendrosios saugyklos</span><span class="sxs-lookup"><span data-stu-id="2e523-136">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="2e523-137">Konfigūracijų nutraukimas Bendrojoje saugykloje</span><span class="sxs-lookup"><span data-stu-id="2e523-137">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)

- <span data-ttu-id="2e523-138">**Globalizavimo funkcija**</span><span class="sxs-lookup"><span data-stu-id="2e523-138">**Globalization feature:**</span></span>

    - [<span data-ttu-id="2e523-139">„Regulatory Configuration Service“ (RCS) – Globalizavimo funkcija</span><span class="sxs-lookup"><span data-stu-id="2e523-139">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)