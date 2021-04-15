---
title: Įtraukti pasveikinimo pranešimą
description: Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ svetainę įtraukti pasisveikinimo pranešimą.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797388"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="558e0-103">Įtraukti pasveikinimo pranešimą</span><span class="sxs-lookup"><span data-stu-id="558e0-103">Add a welcome message</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="558e0-104">Šioje temoje aprašoma, kaip į savo „Microsoft Dynamics 365 Commerce“ svetainę įtraukti pasisveikinimo pranešimą.</span><span class="sxs-lookup"><span data-stu-id="558e0-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

<span data-ttu-id="558e0-105">Pasisveikinimo pranešimas jūsų el. prekybos svetainėje gali lankytojus informuoti apie vykstančius išpardavimus, svetainės naujienas ar esamas sezonines kolekcijas.</span><span class="sxs-lookup"><span data-stu-id="558e0-105">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="558e0-106">Pasisveikinimo pranešimas nustatomas naudojant įspėjimo modulį.</span><span class="sxs-lookup"><span data-stu-id="558e0-106">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="558e0-107">Įspėjimo modulį reikia įtraukti į antraštės fragmento vietą **Klaidų / informaciniai pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="558e0-107">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="558e0-108">Naudodami įspėjimo modulį galite nurodyti rodomą tekstą, teksto spalvą ir lygiuotę.</span><span class="sxs-lookup"><span data-stu-id="558e0-108">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="558e0-109">Jį naudodami taip pat galite nurodyti, ar svetainės lankytojai pranešimą gali atmesti.</span><span class="sxs-lookup"><span data-stu-id="558e0-109">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="558e0-110">Kai pasisveikinimo pranešimas įtraukiamas į bendrai naudojamą antraštės fragmentą, jis bus rodomas kiekviename puslapyje, kuriame naudojamas šablonas ir bendrai naudojamas antraštės fragmentas.</span><span class="sxs-lookup"><span data-stu-id="558e0-110">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="558e0-111">Norėdami į savo svetainę įtraukti pasisveikinimo pranešimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="558e0-111">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="558e0-112">Eikite į savo svetainę „Commerce“ svetainių daryklėje.</span><span class="sxs-lookup"><span data-stu-id="558e0-112">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="558e0-113">Pasirinkite **Fragmentai**.</span><span class="sxs-lookup"><span data-stu-id="558e0-113">Select **Fragments**.</span></span>
1. <span data-ttu-id="558e0-114">Pasirinkite antraštės fragmentą, į kurį norite įtraukti pranešimą.</span><span class="sxs-lookup"><span data-stu-id="558e0-114">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="558e0-115">Struktūros medyje išplėskite **Klaidų / informaciniai pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="558e0-115">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="558e0-116">Pasirinkite įspėjimo modulį ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="558e0-116">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="558e0-117">Jei įspėjimo modulio dar nėra, pirmiausia pasirinkite prie elemento **Klaidų / informaciniai pranešimai** esantį daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="558e0-117">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="558e0-118">Dešinėje esančios ypatybių srities skirtuke **Duomenys** pasirinkite **Įtraukti duomenų šaltinį** ir **Turinys**.</span><span class="sxs-lookup"><span data-stu-id="558e0-118">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="558e0-119">Lauke **Įvesties tekstas** įveskite pasisveikinimo pranešimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="558e0-119">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="558e0-120">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte antraštės fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="558e0-120">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="558e0-121">Pasisveikinimo pranešimas dabar bus rodomas kiekvieno svetainės puslapio, kuriame naudojamas pasirinktas antraštės fragmentas, viršuje.</span><span class="sxs-lookup"><span data-stu-id="558e0-121">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="558e0-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="558e0-122">Additional resources</span></span>

[<span data-ttu-id="558e0-123">Įtraukti logotipą</span><span class="sxs-lookup"><span data-stu-id="558e0-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="558e0-124">Pasirinkti svetainės temą</span><span class="sxs-lookup"><span data-stu-id="558e0-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="558e0-125">Darbas su CSS perrašymo failais</span><span class="sxs-lookup"><span data-stu-id="558e0-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="558e0-126">Įtraukti parankinių piktogramą</span><span class="sxs-lookup"><span data-stu-id="558e0-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="558e0-127">Įtraukti informaciją apie autorių teises</span><span class="sxs-lookup"><span data-stu-id="558e0-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="558e0-128">Kalbų įtraukimas į savo svetainę</span><span class="sxs-lookup"><span data-stu-id="558e0-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="558e0-129">Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija</span><span class="sxs-lookup"><span data-stu-id="558e0-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
