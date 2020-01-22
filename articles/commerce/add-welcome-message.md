---
title: Įtraukti pasveikinimo pranešimą
description: Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ svetainę įtraukti pasisveikinimo pranešimą.
author: psimolin
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4e9deeeaf491b77700ba0833e429f05d376a4392
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914521"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="c9a9a-103">Įtraukti pasveikinimo pranešimą</span><span class="sxs-lookup"><span data-stu-id="c9a9a-103">Add a welcome message</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c9a9a-104">Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ svetainę įtraukti pasisveikinimo pranešimą.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="c9a9a-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="c9a9a-105">Overview</span></span>

<span data-ttu-id="c9a9a-106">Pasisveikinimo pranešimas jūsų el. prekybos svetainėje gali lankytojus informuoti apie vykstančius išpardavimus, svetainės naujienas ar esamas sezonines kolekcijas.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="c9a9a-107">Pasisveikinimo pranešimas nustatomas naudojant įspėjimo modulį.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="c9a9a-108">Įspėjimo modulį reikia įtraukti į antraštės fragmento vietą **Klaidų / informaciniai pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="c9a9a-109">Naudodami įspėjimo modulį galite nurodyti rodomą tekstą, teksto spalvą ir lygiuotę.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="c9a9a-110">Jį naudodami taip pat galite nurodyti, ar svetainės lankytojai pranešimą gali atmesti.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="c9a9a-111">Kai pasisveikinimo pranešimas įtraukiamas į bendrai naudojamą antraštės fragmentą, jis bus rodomas kiekviename puslapyje, kuriame naudojamas šablonas ir bendrai naudojamas antraštės fragmentas.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="c9a9a-112">Norėdami į savo svetainę įtraukti pasisveikinimo pranešimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="c9a9a-113">Programoje „Dynamics 365 Commerce“ nueikite į savo svetainę.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="c9a9a-114">Pasirinkite **Fragmentai**.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="c9a9a-115">Pasirinkite antraštės fragmentą, į kurį norite įtraukti pranešimą.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="c9a9a-116">Struktūros medyje išplėskite **Klaidų / informaciniai pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="c9a9a-117">Pasirinkite įspėjimo modulį.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-117">Select the alert module.</span></span>

    <span data-ttu-id="c9a9a-118">Jei įspėjimo modulio dar nėra, pasirinkite prie elemento **Klaidų / informaciniai pranešimai** esantį daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="c9a9a-119">Pasirinkite įspėjimo modulį ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="c9a9a-120">Dešinėje esančios ypatybių srities skirtuke **Duomenys** pasirinkite **Įtraukti duomenų šaltinį** ir **Turinys**.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="c9a9a-121">Lauke **Įvesties tekstas** įveskite pasisveikinimo pranešimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="c9a9a-122">Antraštės fragmentą įrašykite, atrakinkite ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="c9a9a-123">Pasisveikinimo pranešimas dabar bus rodomas kiekvieno svetainės puslapio, kuriame naudojamas pasirinktas antraštės fragmentas, viršuje.</span><span class="sxs-lookup"><span data-stu-id="c9a9a-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9a9a-124">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c9a9a-124">Additional resources</span></span>

[<span data-ttu-id="c9a9a-125">Įtraukti logotipą</span><span class="sxs-lookup"><span data-stu-id="c9a9a-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="c9a9a-126">Pasirinkti svetainės temą</span><span class="sxs-lookup"><span data-stu-id="c9a9a-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="c9a9a-127">Darbas su CSS perrašymo failais</span><span class="sxs-lookup"><span data-stu-id="c9a9a-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="c9a9a-128">Įtraukti parankinių piktogramą</span><span class="sxs-lookup"><span data-stu-id="c9a9a-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="c9a9a-129">Įtraukti informaciją apie autorių teises</span><span class="sxs-lookup"><span data-stu-id="c9a9a-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="c9a9a-130">Kalbų įtraukimas į savo svetainę</span><span class="sxs-lookup"><span data-stu-id="c9a9a-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="c9a9a-131">Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija</span><span class="sxs-lookup"><span data-stu-id="c9a9a-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

