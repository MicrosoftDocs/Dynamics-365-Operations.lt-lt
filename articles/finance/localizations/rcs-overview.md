---
title: Regulatory Configuration Service
description: Šioje temoje pateikiama „Regulatory Configuration Service” (RCS) galimybių apžvalga ir paaiškinama, kaip pasiekti paslaugą.
author: JaneA07
ms.date: 06/04/2021
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
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216567"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="5428d-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="5428d-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5428d-104">„Regulatory Configuration Service” (RCS) yra atskira dizaino ir ciklo valdymo paslauga, skirta „jokio kodo”/„mažai kodų” globalizavimo funkcijai.</span><span class="sxs-lookup"><span data-stu-id="5428d-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="5428d-105">RCS leidžia globalizavimo suinteresuotosioms šalims be programų kūrėjų dalyvavimo išplėsti ir tinkinti mokesčių, elektroninių SF išrašymo, teisės aktų nustatytų ataskaitų, bankininkystės ir verslo dokumentų pagrindines globalizavimo sritis.</span><span class="sxs-lookup"><span data-stu-id="5428d-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="5428d-106">Dėl šio „jokio kodo”/„mažai kodų” globalizavimo požiūrio, globalizavimas yra paprastesnis, greitesnis ir ekonomiškesnis kūrimui ir išplėtimui.</span><span class="sxs-lookup"><span data-stu-id="5428d-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="5428d-107">„RCS” suteikia šias galimybes:</span><span class="sxs-lookup"><span data-stu-id="5428d-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="5428d-108">Visų Elektroninių ataskaitų (ER) suteikiamų funkcijų palaikymą.</span><span class="sxs-lookup"><span data-stu-id="5428d-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="5428d-109">Būtinuosius naujų globalizavimo mikropaslaugų konfigūravimo komponentus.</span><span class="sxs-lookup"><span data-stu-id="5428d-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="5428d-110">Elektroninių sąskaitų faktūrų išrašymo palaikymą.</span><span class="sxs-lookup"><span data-stu-id="5428d-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="5428d-111">Daugiau informacijos rasite [Elektroninių sąskaitų faktūrų išrašymas](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="5428d-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="5428d-112">Mokesčių skaičiavimo palaikymą.</span><span class="sxs-lookup"><span data-stu-id="5428d-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="5428d-113">Daugiau informacijos rasite [Mokesčių paslauga](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="5428d-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="5428d-114">Naujų globalizavimo funkcijų, kurios supaprastina kelių komponentų funkcijų ciklo valdymą ir suteikia daugiau galimybių konfigūruoti veiksmus ir nustatyti funkcijų parametrus palaikymą.</span><span class="sxs-lookup"><span data-stu-id="5428d-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="5428d-115">Daugiau informacijos rasite [„Regulatory Configuration Service” – supaprastintas globalizavimo funkcijų valdymas, skirtas globalizavimo paslaugoms](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="5428d-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="5428d-116">Pasirinktinių konfigūracijų centralizuoto skelbimo, saugojimo ir bendrinimo bendrojoje saugykloje, kurie supaprastina konfigūracijų valdymą nenaudojant „Microsoft Dynamics Lifecycle Services” (LCS), palaikymą.</span><span class="sxs-lookup"><span data-stu-id="5428d-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="5428d-117">RCS prieiga</span><span class="sxs-lookup"><span data-stu-id="5428d-117">Access RCS</span></span>

<span data-ttu-id="5428d-118">Galite užsiregistruoti arba prisijungti prie RCS iš [„Regulatory Configuration Service” puslapio](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="5428d-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![RCS registravimasis/prisijungimas](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="5428d-120">Puslapyje **„Regulatory Configuration Service”** peržiūrėkite ir priimkite papildomas paslaugos naudojimo sąlygas ir pasirinkite vieną iš šių mygtukų:</span><span class="sxs-lookup"><span data-stu-id="5428d-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="5428d-121">**Registruotis**, jei pirmą kartą naudojatės paslauga ir naudojate darbo el. pašto adresą, kad savo organizacijai parengtumėte paslaugų aplinką</span><span class="sxs-lookup"><span data-stu-id="5428d-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="5428d-122">**Prisijungti**, jeigu anksčiau buvote prisiregistravę prie paslaugos ir norite pasiekti savo organizacijos aplinką</span><span class="sxs-lookup"><span data-stu-id="5428d-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="5428d-123">Regioninis prieinamumas</span><span class="sxs-lookup"><span data-stu-id="5428d-123">Regional availability</span></span>

<span data-ttu-id="5428d-124">RCS yra bendrai prieinamas šiuose regionuose:</span><span class="sxs-lookup"><span data-stu-id="5428d-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="5428d-125">Jungtinės Valstijos</span><span class="sxs-lookup"><span data-stu-id="5428d-125">United States</span></span>
- <span data-ttu-id="5428d-126">Indija</span><span class="sxs-lookup"><span data-stu-id="5428d-126">India</span></span>
- <span data-ttu-id="5428d-127">Prancūzija</span><span class="sxs-lookup"><span data-stu-id="5428d-127">France</span></span>
- <span data-ttu-id="5428d-128">Europa</span><span class="sxs-lookup"><span data-stu-id="5428d-128">Europe</span></span>

<span data-ttu-id="5428d-129">Pilną regionų sąrašą rasite [„Dynamics 365” ir „Power Platform”: Pasiekiamumas, duomenų vieta, kalba ir lokalizavimas](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="5428d-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="rcs-default-company"></a><span data-ttu-id="5428d-130">RCS numatytoji įmonė</span><span class="sxs-lookup"><span data-stu-id="5428d-130">RCS default company</span></span>

<span data-ttu-id="5428d-131">Kūrimo laiko funkcija, naudojama RCS, bendrai naudojama visoms įmonėms.</span><span class="sxs-lookup"><span data-stu-id="5428d-131">Design time functionality that is used in RCS is shared across all companies.</span></span> <span data-ttu-id="5428d-132">Nėra įmonei specialių funkcijų.</span><span class="sxs-lookup"><span data-stu-id="5428d-132">There is no company-specific functionality.</span></span> <span data-ttu-id="5428d-133">Todėl rekomenduojame naudoti vieną įmonę, **DAT**, su savo RCS aplinka.</span><span class="sxs-lookup"><span data-stu-id="5428d-133">Therefore, we recommend that you use one company, **DAT**, with your RCS environment.</span></span>

<span data-ttu-id="5428d-134">Tačiau kai kuriuose scenarijuose galite norėti, kad ER formatai būtų naudojami parametrai, susiję su konkrečiu juridiniu subjektu.</span><span class="sxs-lookup"><span data-stu-id="5428d-134">However, in some scenarios, you might want to make ER formats use parameters that are related to a specific legal entity.</span></span> <span data-ttu-id="5428d-135">Tik šiuose scenarijuose turėtumėte naudoti numatytąjį įmonės perjungimo priemonę.</span><span class="sxs-lookup"><span data-stu-id="5428d-135">In these scenarios only, you should use the default company switcher.</span></span> <span data-ttu-id="5428d-136">Dėl pavyzdžio, žr. [ER formato konfigūravimas, kurį atlikus naudojami juridiniam subjektui nurodyti parametrai](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="5428d-136">For an example, see [Configure ER format to use parameters that are specified per legal entity](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="5428d-137">Susijusi RCS dokumentacija</span><span class="sxs-lookup"><span data-stu-id="5428d-137">Related RCS documentation</span></span>

<span data-ttu-id="5428d-138">Daugiau informacijos apie susijusius komponentus rasite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="5428d-138">For more information about related components, see the following topics:</span></span>

- <span data-ttu-id="5428d-139">**Rcs:**</span><span class="sxs-lookup"><span data-stu-id="5428d-139">**RCS:**</span></span>

    - [<span data-ttu-id="5428d-140">Kurkite ER konfigūracijas RCS ir įkelkite jas į bendrąją saugyklą</span><span class="sxs-lookup"><span data-stu-id="5428d-140">Create ER configurations in RCS and upload them to the Global repository</span></span>](rcs-global-repo-upload.md)

- <span data-ttu-id="5428d-141">**Bendroji saugykla:**</span><span class="sxs-lookup"><span data-stu-id="5428d-141">**Global repository:**</span></span>

    - [<span data-ttu-id="5428d-142">ER konfigūracijos kūrimas ir įkėlimas į Bendrąją saugyklą</span><span class="sxs-lookup"><span data-stu-id="5428d-142">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="5428d-143">Konfigūracijos bendrinimas Bendrojoje saugykloje</span><span class="sxs-lookup"><span data-stu-id="5428d-143">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="5428d-144">Išplėstinis filtravimas Bendrojoje saugykloje</span><span class="sxs-lookup"><span data-stu-id="5428d-144">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="5428d-145">ER konfigūracijų atsisiuntimas iš Bendrosios saugyklos</span><span class="sxs-lookup"><span data-stu-id="5428d-145">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="5428d-146">Konfigūracijų nutraukimas Bendrojoje saugykloje</span><span class="sxs-lookup"><span data-stu-id="5428d-146">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)
    - [<span data-ttu-id="5428d-147">„Regulatory Configuration Service“ (RCS) – „Lifecycle Services“ (LCS) saugykla nebegalioja</span><span class="sxs-lookup"><span data-stu-id="5428d-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>](rcs-lcs-repo-dep-faq.md)

- <span data-ttu-id="5428d-148">**Globalizavimo funkcija**</span><span class="sxs-lookup"><span data-stu-id="5428d-148">**Globalization feature:**</span></span>

    - [<span data-ttu-id="5428d-149">„Regulatory Configuration Service“ (RCS) – Globalizavimo funkcija</span><span class="sxs-lookup"><span data-stu-id="5428d-149">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a><span data-ttu-id="5428d-150">RCS trikčių šalinimo prisijungimas</span><span class="sxs-lookup"><span data-stu-id="5428d-150">Troubleshooting RCS sign-up</span></span>

<span data-ttu-id="5428d-151">Kai prisiregistruojate prie RCS aptarnavimo puslapyje, galite susidurti su problema, kuri susijusi „Azure Active Directory“ („Azure AD“).</span><span class="sxs-lookup"><span data-stu-id="5428d-151">When you sign up for RCS from the service page, you might encounter an issue that is related to Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="5428d-152">Klaidos pranešimas, kurį gaunate, nurodo, kad RCS registracija šiuo metu išjungta ir turi būti įjungta prieš užbaigiant registracijos procesą.</span><span class="sxs-lookup"><span data-stu-id="5428d-152">The error message that you receive indicates that sign-up for RCS is currently turned off and must be turned on before you can complete the sign-up process.</span></span>

![RCS registracijos klaidos pranešimas](media/01_RCSSignUpError.jpg)

<span data-ttu-id="5428d-154">Problema kyla dėl to, kad jūs blokuojate ad hoc abonementų pasirašymą ir ypatybė turi būti įgalinta `AllowAdHocSubscriptions` jūsų nuomininke.</span><span class="sxs-lookup"><span data-stu-id="5428d-154">The issue occurs because you're blocked from signing up for ad-hoc subscriptions, and the `AllowAdHocSubscriptions` property must be enabled in your tenant.</span></span> 

- <span data-ttu-id="5428d-155">Jei jūsų IT padalinys valdo jūsų organizacijos „Azure" nuomininkus, susisiekite su tuo padaliniu ir praneškite apie išdavimą.</span><span class="sxs-lookup"><span data-stu-id="5428d-155">If your IT department manages your organization's Azure tenants, contact that department to report the issue.</span></span>
- <span data-ttu-id="5428d-156">Jei esate atsakingas už „Azure" nuomininkų valdymą, galite išspręsti problemas, atlikite nurodytus veiksmus, nurodytus [Kas yra savitarnos „Azure Active Directory“ registracija](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span><span class="sxs-lookup"><span data-stu-id="5428d-156">If you're responsible for managing your Azure tenants, you can fix the issues by following the steps in [What is self-service sign-up for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span></span>
