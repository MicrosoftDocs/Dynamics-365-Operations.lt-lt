---
title: Nustatykite el. prekybos kūrimo aplinką, kad būtų galima derinti su „Tier 1 Retail Server“ virtualiąja mašina
description: Šioje temoje aiškinama, kaip nustatyti el. prekybos kūrimo aplinką, kad būtų galima derinti su „Tier 1 Retail Server“ virtualiąja mašina (VM).
author: Reza-Assadi
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
ms.openlocfilehash: 5ef286aa28ff459befb72b0178f308e5fb85ec44
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801488"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="e18bf-103">Nustatykite el. prekybos kūrimo aplinką, kad būtų galima derinti su „Tier 1 Retail Server“ virtualiąja mašina</span><span class="sxs-lookup"><span data-stu-id="e18bf-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e18bf-104">Šioje temoje aiškinama, kaip nustatyti el. prekybos kūrimo aplinką, kad būtų galima derinti su „Tier 1 Retail Server“ virtualiąja mašina (VM).</span><span class="sxs-lookup"><span data-stu-id="e18bf-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="e18bf-105">aprašymas</span><span class="sxs-lookup"><span data-stu-id="e18bf-105">Description</span></span>

<span data-ttu-id="e18bf-106">„Microsoft Dynamics 365 Commerce” 1 pakopos aplinkos paprastai diegiamos dėl „Commerce Runtime” (CRT) ir elektroninis kasos aparato (EKA) plėtinio kūrimo.</span><span class="sxs-lookup"><span data-stu-id="e18bf-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="e18bf-107">Jos yra atskiros aplinkos.</span><span class="sxs-lookup"><span data-stu-id="e18bf-107">They are standalone environments.</span></span> <span data-ttu-id="e18bf-108">Dėl architektūros programinės įrangos nuomos paslaugos (SaaS) jos neapima el. prekybos komponentų.</span><span class="sxs-lookup"><span data-stu-id="e18bf-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="e18bf-109">Kai kuriuose scenarijuose galite norėti patikrinti plėtinių iškvietimus 1 pakopos aplinkoje, kad būtų galima suderinti plėtinius iš el. prekybos komponentų.</span><span class="sxs-lookup"><span data-stu-id="e18bf-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="e18bf-110">Bendrųjų instrukcijų ieškokite [Derinimas pagal 1 pakopos „Commerce“ plėtros aplinką](../e-commerce-extensibility/debug-tier-1.md).</span><span class="sxs-lookup"><span data-stu-id="e18bf-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="e18bf-111">Derinant su 1 pakopos aplinka, kadangi svetainė iškviečia kitą „Retail Server“, kelių serverių skambučiai gali sukelti įvairių klaidų, susijusių su turinio saugos strategija.</span><span class="sxs-lookup"><span data-stu-id="e18bf-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="e18bf-112">Toliau pateiktoje iliustracijoje nurodomas klaidos, kuri gali įvykti produkto informacijos puslapyje pasirinkus variantą, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e18bf-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![Klaida, kai variantas pasirenkamas produkto informacijos puslapyje](media/unhandled-rejection-error.jpg)

<span data-ttu-id="e18bf-114">Šioje iliustracijoje pateikiamas panašios naršyklės derintuvės įrankių (F12 programavimo įrankių) klaidos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e18bf-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="e18bf-115">Klaidos pranešime minimi turinio saugos strategijos direktyvos pažeidimai.</span><span class="sxs-lookup"><span data-stu-id="e18bf-115">The error message mentions violation of the content security policy directive.</span></span>

![Derintuvės įrankių klaida](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="e18bf-117">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="e18bf-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="e18bf-118">Išjungti svetainės turinio saugos strategiją „Commerce“ svetainių daryklėje</span><span class="sxs-lookup"><span data-stu-id="e18bf-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="e18bf-119">Pasirinkite svetainę, su kuria dirbate.</span><span class="sxs-lookup"><span data-stu-id="e18bf-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="e18bf-120">Pasirinkite **Parametrai**, tada – **Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="e18bf-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="e18bf-121">Skirtuke **Turinio saugos strategija** pasirinkite **Išjungti turinio saugos strategiją**.</span><span class="sxs-lookup"><span data-stu-id="e18bf-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="e18bf-122">Pasirinkite **įrašyti ir publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="e18bf-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="e18bf-123">Verslo ir vartotojų (B2C) prisijungimas neveikia vietinėje programavimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="e18bf-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="e18bf-124">Tačiau, jei reikia imituoti vartotojo prisijungimą, galite naudoti svečio pirkimo užbaigimą ar kurti puslapių maketus.</span><span class="sxs-lookup"><span data-stu-id="e18bf-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e18bf-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e18bf-125">Additional resources</span></span>

[<span data-ttu-id="e18bf-126">Darbo su el. prekybos išplečiamumo internetu kūrimu pradžia</span><span class="sxs-lookup"><span data-stu-id="e18bf-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="e18bf-127">Turinio saugos strategijos (CSP) valdymas el. prekybos svetainėje</span><span class="sxs-lookup"><span data-stu-id="e18bf-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
