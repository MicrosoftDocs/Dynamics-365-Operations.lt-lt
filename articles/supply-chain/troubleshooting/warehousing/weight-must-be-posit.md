---
title: Svoris turi būti teigiamas
description: Svoris turi būti teigiamas
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924308"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="c02e8-103">Svoris turi būti teigiamas</span><span class="sxs-lookup"><span data-stu-id="c02e8-103">Weight must be positive</span></span>

<span data-ttu-id="c02e8-104">Klaidos kodas: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="c02e8-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="c02e8-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="c02e8-105">Symptoms</span></span>

<span data-ttu-id="c02e8-106">Sistema rodo tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="c02e8-106">The system shows the following error message:</span></span>

> <span data-ttu-id="c02e8-107">Svoris turi būti teigiamas.</span><span class="sxs-lookup"><span data-stu-id="c02e8-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="c02e8-108">Priežastis</span><span class="sxs-lookup"><span data-stu-id="c02e8-108">Cause</span></span>

<span data-ttu-id="c02e8-109">Lauke **Bruto** svoris nustatytas *0* (nulis) arba neigiama vertė.</span><span class="sxs-lookup"><span data-stu-id="c02e8-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="c02e8-110">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="c02e8-110">Resolution</span></span>

<span data-ttu-id="c02e8-111">Norėdami nustatyti svorį, atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="c02e8-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="c02e8-112">Lauke **Bruto** svoris nustatykite vertę.</span><span class="sxs-lookup"><span data-stu-id="c02e8-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="c02e8-113">Tada pasirinkite vienetą iš išplečiamojo sąrašo.</span><span class="sxs-lookup"><span data-stu-id="c02e8-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="c02e8-114">Pasirinkite **Gauti sistemos svorį, kad būtų skaičiuojama** bruto **svorio** vertė.</span><span class="sxs-lookup"><span data-stu-id="c02e8-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
