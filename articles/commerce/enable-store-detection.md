---
title: Įgalinti parduotuvės nustatymą pagal vietą
description: Šioje temoje aprašoma, kaip įjungti parduotuvės nustatymą pagal vietą jūsų „Dynamics 365 Commerce“ svetainei.
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: a542d6987280451910b4ff3bcfb3a109a0e028c6
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697617"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="9daf5-103">Įgalinti parduotuvės nustatymą pagal vietą</span><span class="sxs-lookup"><span data-stu-id="9daf5-103">Enable location-based store detection</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9daf5-104">Šioje temoje aprašoma, kaip įjungti parduotuvės nustatymą pagal vietą jūsų „Dynamics 365 Commerce“ svetainei.</span><span class="sxs-lookup"><span data-stu-id="9daf5-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="9daf5-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="9daf5-105">Overview</span></span>

<span data-ttu-id="9daf5-106">„Commerce“ parduotuvės nustatymu pagal vietą galite suteikti klientams atitinkamą svetainės turinį pagal jų vietą.</span><span class="sxs-lookup"><span data-stu-id="9daf5-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="9daf5-107">Įjungus parduotuvės nustatymą pagal vietą, „Commerce“ generavimo paslauga naudoja šalies / regiono informaciją iš kliento žiniatinklio naršyklės IP adreso ir nukreipia klientą į geriausią galimą geografinę svetainės konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9daf5-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="9daf5-108">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="9daf5-108">Privacy notice</span></span>

<span data-ttu-id="9daf5-109">Jei įjungiate parduotuvės nustatymo pagal vietą funkciją, kliento naršyklės informacija siunčiama „Microsoft“ vietos paslaugai.</span><span class="sxs-lookup"><span data-stu-id="9daf5-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="9daf5-110">Tada ši informacija naudojama kliento turiniui, kuris yra aktualus jo arba jos vietai, teikti.</span><span class="sxs-lookup"><span data-stu-id="9daf5-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="9daf5-111">Ir informacijai, siunčiamai iš kliento naršyklės, ir informacijai pagal vietą, kuri grįžta klientui, taikoma privatumo ir slapukų atitikites strategija.</span><span class="sxs-lookup"><span data-stu-id="9daf5-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="9daf5-112">Parduotuvės nustatymo pagal vietą įjungimas</span><span class="sxs-lookup"><span data-stu-id="9daf5-112">Turn on location-based store detection</span></span>

<span data-ttu-id="9daf5-113">Norėdami įjungti parduotuvės nustatymą pagal vietą programoje „Commerce“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9daf5-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="9daf5-114">Kūrimo įrankyje eikite į savo svetainę.</span><span class="sxs-lookup"><span data-stu-id="9daf5-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="9daf5-115">Kairėje naršymo srityje pasirinkite **Svetainės valdymas**.</span><span class="sxs-lookup"><span data-stu-id="9daf5-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="9daf5-116">Pasirinkite **Svetainės parametrai**.</span><span class="sxs-lookup"><span data-stu-id="9daf5-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="9daf5-117">Nustatykite parinktį **Įjungti parduotuvės nustatymą pagal vietą** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="9daf5-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9daf5-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9daf5-118">Additional resources</span></span>

[<span data-ttu-id="9daf5-119">Interneto parduotuvės peržiūra</span><span class="sxs-lookup"><span data-stu-id="9daf5-119">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="9daf5-120">E. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="9daf5-120">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="9daf5-121">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="9daf5-121">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="9daf5-122">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="9daf5-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="9daf5-123">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9daf5-123">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="9daf5-124">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="9daf5-124">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="9daf5-125">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="9daf5-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
