---
title: Įtraukti pasveikinimo pranešimą
description: Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ svetainę įtraukti pasisveikinimo pranešimą.
author: psimolin
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d2a125b4e71016ad620f128af2e3c9f29aa04f4c
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269619"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="37a82-103">Įtraukti pasveikinimo pranešimą</span><span class="sxs-lookup"><span data-stu-id="37a82-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="37a82-104">Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ svetainę įtraukti pasisveikinimo pranešimą.</span><span class="sxs-lookup"><span data-stu-id="37a82-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="37a82-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="37a82-105">Overview</span></span>

<span data-ttu-id="37a82-106">Pasisveikinimo pranešimas jūsų el. prekybos svetainėje gali lankytojus informuoti apie vykstančius išpardavimus, svetainės naujienas ar esamas sezonines kolekcijas.</span><span class="sxs-lookup"><span data-stu-id="37a82-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="37a82-107">Pasisveikinimo pranešimas nustatomas naudojant įspėjimo modulį.</span><span class="sxs-lookup"><span data-stu-id="37a82-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="37a82-108">Įspėjimo modulį reikia įtraukti į antraštės fragmento vietą **Klaidų / informaciniai pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="37a82-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="37a82-109">Naudodami įspėjimo modulį galite nurodyti rodomą tekstą, teksto spalvą ir lygiuotę.</span><span class="sxs-lookup"><span data-stu-id="37a82-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="37a82-110">Jį naudodami taip pat galite nurodyti, ar svetainės lankytojai pranešimą gali atmesti.</span><span class="sxs-lookup"><span data-stu-id="37a82-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="37a82-111">Kai pasisveikinimo pranešimas įtraukiamas į bendrai naudojamą antraštės fragmentą, jis bus rodomas kiekviename puslapyje, kuriame naudojamas šablonas ir bendrai naudojamas antraštės fragmentas.</span><span class="sxs-lookup"><span data-stu-id="37a82-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="37a82-112">Norėdami į savo svetainę įtraukti pasisveikinimo pranešimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="37a82-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="37a82-113">Eikite į savo svetainę „Commerce“ svetainių daryklėje.</span><span class="sxs-lookup"><span data-stu-id="37a82-113">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="37a82-114">Pasirinkite **Fragmentai**.</span><span class="sxs-lookup"><span data-stu-id="37a82-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="37a82-115">Pasirinkite antraštės fragmentą, į kurį norite įtraukti pranešimą.</span><span class="sxs-lookup"><span data-stu-id="37a82-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="37a82-116">Struktūros medyje išplėskite **Klaidų / informaciniai pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="37a82-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="37a82-117">Pasirinkite įspėjimo modulį ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="37a82-117">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="37a82-118">Jei įspėjimo modulio dar nėra, pirmiausia pasirinkite prie elemento **Klaidų / informaciniai pranešimai** esantį daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="37a82-118">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="37a82-119">Dešinėje esančios ypatybių srities skirtuke **Duomenys** pasirinkite **Įtraukti duomenų šaltinį** ir **Turinys**.</span><span class="sxs-lookup"><span data-stu-id="37a82-119">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="37a82-120">Lauke **Įvesties tekstas** įveskite pasisveikinimo pranešimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="37a82-120">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="37a82-121">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte antraštės fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="37a82-121">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="37a82-122">Pasisveikinimo pranešimas dabar bus rodomas kiekvieno svetainės puslapio, kuriame naudojamas pasirinktas antraštės fragmentas, viršuje.</span><span class="sxs-lookup"><span data-stu-id="37a82-122">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37a82-123">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="37a82-123">Additional resources</span></span>

[<span data-ttu-id="37a82-124">Įtraukti logotipą</span><span class="sxs-lookup"><span data-stu-id="37a82-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="37a82-125">Pasirinkti svetainės temą</span><span class="sxs-lookup"><span data-stu-id="37a82-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="37a82-126">Darbas su CSS perrašymo failais</span><span class="sxs-lookup"><span data-stu-id="37a82-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="37a82-127">Įtraukti parankinių piktogramą</span><span class="sxs-lookup"><span data-stu-id="37a82-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="37a82-128">Įtraukti informaciją apie autorių teises</span><span class="sxs-lookup"><span data-stu-id="37a82-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="37a82-129">Kalbų įtraukimas į savo svetainę</span><span class="sxs-lookup"><span data-stu-id="37a82-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="37a82-130">Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija</span><span class="sxs-lookup"><span data-stu-id="37a82-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

