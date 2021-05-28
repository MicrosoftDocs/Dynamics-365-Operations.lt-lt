---
title: Viename kvite spausdinama tik viena kelių darbo antraščių žymė
description: Viename kvite spausdinama tik viena kelių darbo antraščių žymė.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026744"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="a11a2-103">Viename kvite spausdinama tik viena kelių darbo antraščių žymė</span><span class="sxs-lookup"><span data-stu-id="a11a2-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="a11a2-104">KB numeris: 4614667</span><span class="sxs-lookup"><span data-stu-id="a11a2-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="a11a2-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="a11a2-105">Symptoms</span></span>

<span data-ttu-id="a11a2-106">Tai pačiai paskirties numerio daliai, kaip vienos sandėlio programos gavimo įvykio dalis, sukuriamos kelios darbo antraštės.</span><span class="sxs-lookup"><span data-stu-id="a11a2-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="a11a2-107">Tačiau, gautame produkte spausdinama tik viena numerio lentelės žymė.</span><span class="sxs-lookup"><span data-stu-id="a11a2-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="a11a2-108">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="a11a2-108">Resolution</span></span>

<span data-ttu-id="a11a2-109">Sistema veikia kaip sukurta.</span><span class="sxs-lookup"><span data-stu-id="a11a2-109">The system is behaving as designed.</span></span>

<span data-ttu-id="a11a2-110">Dabartiniame dizaine visada generuojama viena numerio lentelės žymė, neatsižvelgiant į esamą darbo antraštės skaičių ir darbo eilučių derinius.</span><span class="sxs-lookup"><span data-stu-id="a11a2-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="a11a2-111">Sugeneruotoje etiketėje yra informacija tik vienam deriniui.</span><span class="sxs-lookup"><span data-stu-id="a11a2-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="a11a2-112">Norėdami išspręsti šią problemą, įsitikinkite, kad darbo antraštės kūrimas visada susietas su viena paskirties numerio lentelėmis.</span><span class="sxs-lookup"><span data-stu-id="a11a2-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
