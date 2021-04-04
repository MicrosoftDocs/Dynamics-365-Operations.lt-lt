---
title: Apriboti prieigą prie parduotuvės tikrinimo arba kūrimo metu
description: Šioje temoje paaiškinama, kaip riboti prieigą prie „Microsoft Dynamics 365 Commerce” parduotuvės, kol vyksta vidinis tikrinimas ar kūrimas.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2cdf131048e0fac940475322294ed99e76c0a53b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585451"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="c7991-103">Apriboti prieigą prie parduotuvės tikrinimo arba kūrimo metu</span><span class="sxs-lookup"><span data-stu-id="c7991-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7991-104">Šioje temoje paaiškinama, kaip riboti prieigą prie „Microsoft Dynamics 365 Commerce” parduotuvės, kol vyksta vidinis tikrinimas ar kūrimas.</span><span class="sxs-lookup"><span data-stu-id="c7991-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="c7991-105">aprašymas</span><span class="sxs-lookup"><span data-stu-id="c7991-105">Description</span></span>

<span data-ttu-id="c7991-106">Vidinio tikrinimo arba aktyvaus kūrimo metu galite norėti apriboti prieigą prie jūsų svetainės, kad išoriniai vartotojai negalėtų pasiekti publikuotų parduotuvės puslapių.</span><span class="sxs-lookup"><span data-stu-id="c7991-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="c7991-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="c7991-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="c7991-108">Nustatyti „Azure AD” B2C naudojant standartinius vartotojų srautus</span><span class="sxs-lookup"><span data-stu-id="c7991-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="c7991-109">Informacijos apie tai, kaip konfigūruoti jūsų el. prekybos svetainės „Azure Active Directory” B2C („Azure AD” B2C), ieškokite [„Commerce” B2C nuomotojo sąranka](../set-up-b2c-tenant.md).</span><span class="sxs-lookup"><span data-stu-id="c7991-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="c7991-110">Apriboti vartotojo prieigą prie parduotuvės puslapių ir blokuoti naujų vartotojų kūrimą</span><span class="sxs-lookup"><span data-stu-id="c7991-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="c7991-111">Norėdami apriboti vartotojo prieigą prie parduotuvės puslapių „Commerce” svetainių daryklėje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c7991-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c7991-112">Nueikite į savo svetainę.</span><span class="sxs-lookup"><span data-stu-id="c7991-112">Go to your site.</span></span>
1. <span data-ttu-id="c7991-113">Pasirinkite **Puslapiai**, tada pasirinkite puslapį, kurio vartotojų prieigą apribosite.</span><span class="sxs-lookup"><span data-stu-id="c7991-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="c7991-114">Pasirinkite modulio arba fragmento vietą, tada pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="c7991-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="c7991-115">Ypatybių srityje pasirinkite **Reikia prisijungti?**, tada pasirinkite **Baigti redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="c7991-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c7991-116">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="c7991-116">Select **Publish**.</span></span>

<span data-ttu-id="c7991-117">Norėdami blokuoti naujų vartotojų kūrimą „Azure AD”, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c7991-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="c7991-118">Eikite į [„Azure“ portalą](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="c7991-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="c7991-119">Pasirinkite „Azure AD” B2C programą, kurią sukūrėte jūsų svetainės prieigai.</span><span class="sxs-lookup"><span data-stu-id="c7991-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="c7991-120">Kairiojoje naršymo srityje pasirinkite **Vartotojų srautai**.</span><span class="sxs-lookup"><span data-stu-id="c7991-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="c7991-121">Puslapio **Vartotojo srautai** viršuje pasirinkite **Naujas vartotojo srautas**.</span><span class="sxs-lookup"><span data-stu-id="c7991-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="c7991-122">Puslapyje **Pasirinkti vartotojo srauto tipą** pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="c7991-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="c7991-123">Puslapio viduryje pasirinkite **Prisijungti prie v2**.</span><span class="sxs-lookup"><span data-stu-id="c7991-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="c7991-124">Tada atlikite veiksmus, pateiktus [„Commerce” B2C nuomotojo sąranka](../set-up-b2c-tenant.md), norėdami konfigūruoti srautą kaip jūsų svetainės standartinį „Azure AD” B2C vartotojų srautą tikrinimo ar kūrimo metu.</span><span class="sxs-lookup"><span data-stu-id="c7991-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7991-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c7991-125">Additional resources</span></span>

[<span data-ttu-id="c7991-126">„Commerce” B2C nuomotojo sąranka</span><span class="sxs-lookup"><span data-stu-id="c7991-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="c7991-127">Vartotojo registracijos pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="c7991-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
