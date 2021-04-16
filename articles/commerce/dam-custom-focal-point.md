---
title: Tinkinti centrinius vaizdo taškus
description: Šioje temoje aprašoma, kaip tinkinti centrinius vaizdo taškus „Microsoft Dynamics 365 Commerce“ svetainės generatoriuje.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 962caff0e8e41487231c6075fa7b2df2a59dca48
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799306"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="0bf9e-103">Vaizdų centro tinkinimas</span><span class="sxs-lookup"><span data-stu-id="0bf9e-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0bf9e-104">Šioje temoje aprašoma, kaip tinkinti centrinius vaizdo taškus „Microsoft Dynamics 365 Commerce“ svetainės generatoriuje.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="0bf9e-105">Kai vaizdas įkeliamas į „Commerce“ svetainės generatoriaus medijos biblioteką, sistema bando nustatyti vaizdo centrinę vietą.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-105">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="0bf9e-106">Pavyzdžiui, jei paveikslėlyje yra žmogus, sistema nustatys asmens veido centrinį tašką pagal numatytuosius nustatymus.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-106">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="0bf9e-107">Daugeliu atvejų automatiškai nustatomas centrinis taškas gerai tinka visoms peržiūros sritims, tačiau kartais galite norėti pakoreguoti centrinį tašką, kad būtų užtikrinta, jog konkreti vaizdo dalis visada bus matoma.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-107">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="0bf9e-108">Pasirinktinio centrinio vaizdo taško nustatymas</span><span class="sxs-lookup"><span data-stu-id="0bf9e-108">Define a custom focal point for an image</span></span>

<span data-ttu-id="0bf9e-109">Norėdami nustatyti pasirinktą centrinį vaizdo tašką, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-109">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="0bf9e-110">Kairiojoje „Commerce“ svetainės generatoriaus naršymo srityje pasirinkite **Medijos biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-110">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="0bf9e-111">Pagrindiniame lange pasirinkite vaizdą, kurį norite modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-111">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="0bf9e-112">Komandų juostoje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-112">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="0bf9e-113">Pasirinkite vaizdą, kad atsidarytų **Redaguoti režimą** langas.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-113">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="0bf9e-114">Po pasirinktimi **Redaguoti režimą** pasirinkite **Pakeisti centrinį tašką**.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-114">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="0bf9e-115">Virš vaizdo atsiras žiedinis centrinio taško valdiklis.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-115">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="0bf9e-116">Pažymėkite centrinio taško valdiklį, kad galėtumėte jį perkelti į norimą centrinį tašką.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-116">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="0bf9e-117">Kai baigsite, komandų juostoje pasirinkite **Įrašyti** ir pasirinkite **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-117">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0bf9e-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0bf9e-118">Additional resources</span></span>

[<span data-ttu-id="0bf9e-119">Skaitmeninio turto valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="0bf9e-119">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="0bf9e-120">Vaizdų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="0bf9e-120">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="0bf9e-121">Vaizdo įrašų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="0bf9e-121">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="0bf9e-122">Įkelti failus</span><span class="sxs-lookup"><span data-stu-id="0bf9e-122">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="0bf9e-123">Vaizdų apkarpymas</span><span class="sxs-lookup"><span data-stu-id="0bf9e-123">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="0bf9e-124">Naujinti ir aptarnauti statinius failus</span><span class="sxs-lookup"><span data-stu-id="0bf9e-124">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
