---
title: Gabenimo valdymo įvairūs mokesčiai
description: Šioje temoje paaiškinama, kaip gabenimo sukurti mokesčiai turi būti susieti su mokesčių kodu.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cb503072fb76e04aa01ff2d231c756eeb244c65a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004707"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="6c150-103">Gabenimo valdymo įvairūs mokesčiai</span><span class="sxs-lookup"><span data-stu-id="6c150-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c150-104">Taip kaip ir su visais įvairiais mokesčiais, gabenimo sukurti mokesčiai turi būti susieti su mokesčių kodu.</span><span class="sxs-lookup"><span data-stu-id="6c150-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="6c150-105">Kitu atveju, jie bus įtraukti atgal į užsakymą kaip įvairūs mokesčiai.</span><span class="sxs-lookup"><span data-stu-id="6c150-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="6c150-106">Taigi **Mokesčių kodas** nustato, kaip mokestis yra apskaičiuojamas pagal užsakymą ir užsakymo eilutę, į kurią jis įtrauktas.</span><span class="sxs-lookup"><span data-stu-id="6c150-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="6c150-107">Eikite į **Gabenimo valdymas > Nustatymai > Reitingavimas > Įvairūs mokesčiai** tam, kad nustatytumėte kvalifikavimo kriterijus, nustatančius, kada konkretus **Mokesčių kodas** yra taikomas mokesčiui.</span><span class="sxs-lookup"><span data-stu-id="6c150-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="6c150-108">Turėtumėte turėti mažiausiai vieną nustatymą kiekvienam svarbiam **Nuskaičiavimo modulio** nustatymui (*Klientas* ir *Tiekėjas*), kai **Įvairūs nuskaičiavimai tipai** yra nustatyti į *Jokių*.</span><span class="sxs-lookup"><span data-stu-id="6c150-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="6c150-109">Jei jo nėra, įvairūs mokesčiai *nebus* įtraukti į užsakymą.</span><span class="sxs-lookup"><span data-stu-id="6c150-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>
