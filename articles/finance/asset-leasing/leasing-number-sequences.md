---
title: Numeracijų priskyrimas
description: Šioje temoje paaiškinama, kaip kurti nuomos ID numeracijas. Joje taip pat paaiškina, kaip kurti unikalius ID, naudojamus indekso perkainojimo procese.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0b5d622df1e5dcdf7f1322328bce7e185f8edb8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819823"
---
# <a name="assign-number-sequences"></a><span data-ttu-id="5f246-104">Numeracijų priskyrimas</span><span class="sxs-lookup"><span data-stu-id="5f246-104">Assign number sequences</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="5f246-105">Šioje temoje paaiškinama, kaip kurti nuomos ID numeracijas.</span><span class="sxs-lookup"><span data-stu-id="5f246-105">This topic explains how to create number sequences for lease IDs.</span></span> <span data-ttu-id="5f246-106">Joje taip pat paaiškina, kaip kurti unikalius ID, naudojamus indekso perkainojimo procese.</span><span class="sxs-lookup"><span data-stu-id="5f246-106">It also explains how to create unique IDs that are used in the index revaluation process.</span></span>

1. <span data-ttu-id="5f246-107">Eikite į **Turto nuoma \> Sąranka \> Turto nuomos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5f246-107">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="5f246-108">Pasirinkite šoninį skirtuką **Numeracijos**.</span><span class="sxs-lookup"><span data-stu-id="5f246-108">Select the **Number sequences** side tab.</span></span>
3. <span data-ttu-id="5f246-109">Šoniniame skirtuke pasirinkite **Numeracijos**.</span><span class="sxs-lookup"><span data-stu-id="5f246-109">Select **Number sequences** in the side bar.</span></span>
4. <span data-ttu-id="5f246-110">Pasirinkite nuorodos **Nuomos ID** numeraciją.</span><span class="sxs-lookup"><span data-stu-id="5f246-110">Select the number sequence for the **Lease ID** reference.</span></span> <span data-ttu-id="5f246-111">Ši numeracija bus naudojama kiekvienos nuomos unikaliam identifikatoriui generuoti.</span><span class="sxs-lookup"><span data-stu-id="5f246-111">This number sequence will be used to generate the unique identifier for each lease.</span></span>
5. <span data-ttu-id="5f246-112">Pasirinkite nuorodos **Proceso ID** numeraciją.</span><span class="sxs-lookup"><span data-stu-id="5f246-112">Select the number sequence for the **Process ID** reference.</span></span> <span data-ttu-id="5f246-113">Ši numeracija bus naudojama kiekvieno indekso perkainojimo proceso unikaliam identifikatoriui generuoti.</span><span class="sxs-lookup"><span data-stu-id="5f246-113">This number sequence will be used to generate the unique identifier for each index revaluation process.</span></span>
6. <span data-ttu-id="5f246-114">Rinkitės skaičių seką **Pasiūlymo pabaigos ID** nuorodai.</span><span class="sxs-lookup"><span data-stu-id="5f246-114">Select the number sequence for the **Termination Proposal ID** reference.</span></span> <span data-ttu-id="5f246-115">Ši skaičių seka bus naudojama siekiant sukurti unikalų identifikatorių kiekvienam pabaigos pasiūlymui.</span><span class="sxs-lookup"><span data-stu-id="5f246-115">This number sequence will be used to generate the unique identifier for each termination proposal.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]