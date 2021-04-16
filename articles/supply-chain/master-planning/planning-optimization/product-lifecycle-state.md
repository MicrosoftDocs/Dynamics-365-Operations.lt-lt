---
title: Išmesti produktus, kurie turi konkrečias produkto gyvavimo ciklo būsenas
description: Šioje temoje paaiškinama, kaip išmesti produktus pagal jų gyvavimo ciklo būseną naudojant „Planning Optimization“ funkcijas.
author: ChristianRytt
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7028a509aa884589958542f7ec627d69dffcfcec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839252"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="9fff6-103">Išmesti produktus, kurie turi konkrečias produkto gyvavimo ciklo būsenas</span><span class="sxs-lookup"><span data-stu-id="9fff6-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9fff6-104">Išleisti produktai ir išleistų produktų versijos įskaitant **Produkto gyvavimo ciklo būsenos** laukelį.</span><span class="sxs-lookup"><span data-stu-id="9fff6-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="9fff6-105">Šis laukelis jums leidžia valdyti, tarp kitų dalykų, kurie produktai yra įskaityti pagrindinio planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="9fff6-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="9fff6-106">Galite įtraukti, pašalinti ir redaguoti gyvavimo ciklo būsenas kaip būtina patekę į **Produkto informacijos valdymas \> Nustatymai \> Produkto gyvavimo būsena**.</span><span class="sxs-lookup"><span data-stu-id="9fff6-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="9fff6-107">Kiekvienai produkto gyvavimo ciklo būsenai, nustatykite **Aktyvus planavimui** parinktį į *Taip* jei produktai, turintys šią būseną, turi būti įtraukti pagrindinio planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="9fff6-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="9fff6-108">Nustačius parinktį į *Ne*, susieti produktai ir variantai bus išmesti iš visų pagrindinių planavimų ir visų skaičiavimų medžiagų važtaraštyje (BOM) lygmeniu.</span><span class="sxs-lookup"><span data-stu-id="9fff6-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="9fff6-109">Išleisti produktai ir variantai, kai **Produkto gyvavimo ciklo būsenos** laukelis yra paliktas tuščias yra apdorojami taip tarsi produkto gyvavimo būsena, kai **Aktyvus planavimui** parinktis yra nustatyta į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="9fff6-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="9fff6-110">Kitaip tariant, jie bus įtraukti pagrindinio planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="9fff6-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="9fff6-111">Norėdami padėti išvengti nereikalingų tiekimo siūlymų, stipriai rekomenduojame jums susieti visus negaliojančius išleistus produktus ir variantus su produkto gyvavimo ciklo būsena, kai **Aktyvus planavimui** parinktis nustatyta į *Ne*.</span><span class="sxs-lookup"><span data-stu-id="9fff6-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="9fff6-112">Šis būdas yra ypač svarbus jums dirbant su produkto konfigūravimo variantais, kurie nėra panaudojami iš naujo, nes jis jums padės apsisaugoti nuo šiukšlių.</span><span class="sxs-lookup"><span data-stu-id="9fff6-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="9fff6-113">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="9fff6-113">Related resources</span></span>

<span data-ttu-id="9fff6-114">Daugiau informacijos apie produktų gyvavimo ciklo būsenas rasite [Produkto gyvavimo ciklo būsenų apžvalga](../../pim/product-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="9fff6-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="9fff6-115">Dėl išsamios informacijos apimančios žingsnius produkto gyvavimo ciklo būsenų naudojimui siekiant išmesti produktus ir pagrindinio planavimo ir BOM-level skaičiuokles, žr. [Sukurti produkto gyvavimo ciklo būseną siekiant išmesti produktus iš pagrindinio planavimo](../../pim/tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="9fff6-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]