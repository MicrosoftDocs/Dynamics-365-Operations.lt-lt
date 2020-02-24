---
title: Įtraukti parankinių piktogramą
description: Šioje temoje paaiškinama, kaip į savo svetainę įtraukti parankinių piktogramą.
author: bicyclingfool
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 287663817232e7ce86e8fdb1fb5c2fcfeed33d20
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001547"
---
# <a name="add-a-favicon"></a><span data-ttu-id="d8e49-103">Įtraukti parankinių piktogramą</span><span class="sxs-lookup"><span data-stu-id="d8e49-103">Add a favicon</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d8e49-104">Šioje temoje paaiškinama, kaip į savo svetainę įtraukti parankinių piktogramą.</span><span class="sxs-lookup"><span data-stu-id="d8e49-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="d8e49-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="d8e49-105">Overview</span></span>

<span data-ttu-id="d8e49-106">Parankinių piktogrma yra mažas grafikos failas, rodomas žiniatinklio naršyklės skirtuke, adresų juostoje, naršymo retrospektyvoje, žymelėse, parankiniuose ir kitose vietose.</span><span class="sxs-lookup"><span data-stu-id="d8e49-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="d8e49-107">Rekomenduojame parankinių piktogramą įtraukti į savo svetainę, nes ji vaizduoja ir sustiprina jūsų prekės ženklą bei jūsų svetainę padeda atskirti nuo kitų svetainių, kuriose lankosi jūsų klientai.</span><span class="sxs-lookup"><span data-stu-id="d8e49-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="d8e49-108">Nors į svetainę galima įtraukti kelias įvairių dydžių ir failų tipų parankinių piktogramas, šioje temoje parodyta, kaip įtraukti vieną parankinių piktogramą.</span><span class="sxs-lookup"><span data-stu-id="d8e49-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="d8e49-109">Tačiau tas pats procesas ir vieta naudojami norint įtraukti daugiau parankinių piktogramų.</span><span class="sxs-lookup"><span data-stu-id="d8e49-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="d8e49-110">Parankinių piktogramos nusiuntimas į svetainės turto rinkinį</span><span class="sxs-lookup"><span data-stu-id="d8e49-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="d8e49-111">Norėdami parankinių piktogramą nusiųsti į savo svetainės turto rinkinį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d8e49-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="d8e49-112">Nueikite į **Turtas \> Nusiųsti \> Nusiųsti turtą**.</span><span class="sxs-lookup"><span data-stu-id="d8e49-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="d8e49-113">Suraskite ir pasirinkite parankinių piktogramą vietinėje failų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="d8e49-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="d8e49-114">Įveskite pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d8e49-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="d8e49-115">Dešinėje esančioje ypatybių srityje nukopijuokite viešąjį parankinių piktogramos URL.</span><span class="sxs-lookup"><span data-stu-id="d8e49-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="d8e49-116">Jei nepasirenkate parinkties **Nusiųstą turtą publikuoti**, turite grįžti į puslapį **Turtas** ir parankinių piktogramą patys publikuoti vėliau.</span><span class="sxs-lookup"><span data-stu-id="d8e49-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="d8e49-117">Parankinių piktogramos HTML kūrimas</span><span class="sxs-lookup"><span data-stu-id="d8e49-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="d8e49-118">Norėdami sukurti parankinių piktogramos HTML, naudokite tolesnį HTML fragmentą.</span><span class="sxs-lookup"><span data-stu-id="d8e49-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="d8e49-119">Atribute **href** **"Public\_URL\_for\_your\_favicon"** („viešasis parankinių piktogramos URL“) pakeiskite anksčiau nukopijuotu viešuoju URL.</span><span class="sxs-lookup"><span data-stu-id="d8e49-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="d8e49-120">Parankinių piktogramos HTML įtraukimas į puslapių elementą \<head\></span><span class="sxs-lookup"><span data-stu-id="d8e49-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="d8e49-121">Norėdami į savo svetainę įtraukti parankinių piktogramą, naudokite tą pačią procedūrą, kurią naudojant į jūsų svetainės puslapių elementą **\<head\>** įtraukiamas bet kokio tipo HTML ar scenarijus.</span><span class="sxs-lookup"><span data-stu-id="d8e49-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8e49-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d8e49-122">Additional resources</span></span>

[<span data-ttu-id="d8e49-123">Įtraukti logotipą</span><span class="sxs-lookup"><span data-stu-id="d8e49-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="d8e49-124">Pasirinkti svetainės temą</span><span class="sxs-lookup"><span data-stu-id="d8e49-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="d8e49-125">Darbas su CSS perrašymo failais</span><span class="sxs-lookup"><span data-stu-id="d8e49-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="d8e49-126">Įtraukti pasveikinimo pranešimą</span><span class="sxs-lookup"><span data-stu-id="d8e49-126">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="d8e49-127">Įtraukti informaciją apie autorių teises</span><span class="sxs-lookup"><span data-stu-id="d8e49-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="d8e49-128">Kalbų įtraukimas į savo svetainę</span><span class="sxs-lookup"><span data-stu-id="d8e49-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="d8e49-129">Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija</span><span class="sxs-lookup"><span data-stu-id="d8e49-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

