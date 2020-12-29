---
title: KS versijos nustatymas
description: Jei nustatytas numatytasis prekės užsakymo tipas Gamyba, poreikio išskleidimo metu planavimo variklis pagal teritoriją suranda tinkamą KS versiją.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 766c857cca603f84bb7fcef2c7eea3bc76620c19
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433832"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="65e9a-103">KS versijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="65e9a-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65e9a-104">Jei nustatytas numatytasis prekės užsakymo tipas Gamyba, poreikio išskleidimo metu planavimo variklis pagal teritoriją suranda tinkamą KS versiją.</span><span class="sxs-lookup"><span data-stu-id="65e9a-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="65e9a-105">Teritorijos dimensija visada žinoma ir yra nurodyta poreikio operacijoje.</span><span class="sxs-lookup"><span data-stu-id="65e9a-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="65e9a-106">Tolesnis procesas naudojamas nustatyti, kokią KS versiją naudoti.</span><span class="sxs-lookup"><span data-stu-id="65e9a-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="65e9a-107">Jei poreikio teritorijoje yra nurodyta prekės KS versija, naudojama konkrečios teritorijos KS.</span><span class="sxs-lookup"><span data-stu-id="65e9a-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="65e9a-108">Jei poreikio teritorijoje konkrečios teritorijos KS versija nenustatyta, naudojama bendroji KS.</span><span class="sxs-lookup"><span data-stu-id="65e9a-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="65e9a-109">Bendrajame KS teritorija nenurodoma, tad jis tinka kelioms teritorijoms.</span><span class="sxs-lookup"><span data-stu-id="65e9a-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="65e9a-110">Jei yra bendroji KS, naudojama ji.</span><span class="sxs-lookup"><span data-stu-id="65e9a-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="65e9a-111">Jei nėra galimos naudoti bendrojo KS versijos, poreikio išskleidimas sustoja.</span><span class="sxs-lookup"><span data-stu-id="65e9a-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="65e9a-112">Tinkama KS versija, konkrečios teritorijos ar bendroji, turi atitikti nurodytus datos ir kiekio kriterijus.</span><span class="sxs-lookup"><span data-stu-id="65e9a-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>





