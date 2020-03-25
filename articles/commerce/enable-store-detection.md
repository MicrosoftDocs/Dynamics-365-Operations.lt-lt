---
title: Įgalinti parduotuvės nustatymą pagal vietą
description: Šioje temoje aprašoma, kaip įjungti parduotuvės nustatymą pagal vietą jūsų „Dynamics 365 Commerce“ svetainei.
author: brianshook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 66ffe56f9d969c9d62ed4ff49f0848fab7e58a56
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096874"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="abe01-103">Įgalinti parduotuvės nustatymą pagal vietą</span><span class="sxs-lookup"><span data-stu-id="abe01-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="abe01-104">Šioje temoje aprašoma, kaip įjungti parduotuvės nustatymą pagal vietą jūsų „Dynamics 365 Commerce“ svetainei.</span><span class="sxs-lookup"><span data-stu-id="abe01-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="abe01-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="abe01-105">Overview</span></span>

<span data-ttu-id="abe01-106">„Commerce“ parduotuvės nustatymu pagal vietą galite suteikti klientams atitinkamą svetainės turinį pagal jų vietą.</span><span class="sxs-lookup"><span data-stu-id="abe01-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="abe01-107">Įjungus parduotuvės nustatymą pagal vietą, „Commerce“ generavimo paslauga naudoja šalies / regiono informaciją iš kliento žiniatinklio naršyklės IP adreso ir nukreipia klientą į geriausią galimą geografinę svetainės konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="abe01-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="abe01-108">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="abe01-108">Privacy notice</span></span>

<span data-ttu-id="abe01-109">Jei įjungiate parduotuvės nustatymo pagal vietą funkciją, kliento naršyklės informacija siunčiama „Microsoft“ vietos paslaugai.</span><span class="sxs-lookup"><span data-stu-id="abe01-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="abe01-110">Tada ši informacija naudojama kliento turiniui, kuris yra aktualus jo arba jos vietai, teikti.</span><span class="sxs-lookup"><span data-stu-id="abe01-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="abe01-111">Ir informacijai, siunčiamai iš kliento naršyklės, ir informacijai pagal vietą, kuri grįžta klientui, taikoma privatumo ir slapukų atitikites strategija.</span><span class="sxs-lookup"><span data-stu-id="abe01-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="abe01-112">Parduotuvės nustatymo pagal vietą įjungimas</span><span class="sxs-lookup"><span data-stu-id="abe01-112">Turn on location-based store detection</span></span>

<span data-ttu-id="abe01-113">Norėdami įjungti parduotuvės nustatymą pagal vietą programoje „Commerce“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="abe01-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="abe01-114">Kūrimo įrankyje eikite į savo svetainę.</span><span class="sxs-lookup"><span data-stu-id="abe01-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="abe01-115">Kairėje naršymo srityje pasirinkite **Svetainės valdymas**.</span><span class="sxs-lookup"><span data-stu-id="abe01-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="abe01-116">Pasirinkite **Svetainės parametrai**.</span><span class="sxs-lookup"><span data-stu-id="abe01-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="abe01-117">Nustatykite parinktį **Įjungti parduotuvės nustatymą pagal vietą** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="abe01-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="abe01-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="abe01-118">Additional resources</span></span>

[<span data-ttu-id="abe01-119">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="abe01-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="abe01-120">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="abe01-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="abe01-121">Interneto parduotuvės kanalo integravimas</span><span class="sxs-lookup"><span data-stu-id="abe01-121">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="abe01-122">El. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="abe01-122">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="abe01-123">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="abe01-123">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="abe01-124">„Robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="abe01-124">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="abe01-125">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="abe01-125">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="abe01-126">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="abe01-126">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="abe01-127">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="abe01-127">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="abe01-128">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="abe01-128">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="abe01-129">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="abe01-129">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
