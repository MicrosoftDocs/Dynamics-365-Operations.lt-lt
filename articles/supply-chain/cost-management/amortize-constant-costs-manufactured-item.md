---
title: Amortizuoti pastovias išlaidas pagamintai prekei
description: Gamintojo prekės pastovios išlaidos rodo operacijos nustatymo laikus ir komponentus, turinčius pastovų kiekį arba pastovią nurašymų sumą.
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 7ccd5ce3e2ed58db8f13eebbcfa6fe5fb544d6c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564229"
---
# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="848f8-103">Amortizuoti pastovias išlaidas pagamintai prekei</span><span class="sxs-lookup"><span data-stu-id="848f8-103">Amortize constant costs for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="848f8-104">Gamintojo prekės pastovios išlaidos rodo operacijos nustatymo laikus ir komponentus, turinčius pastovų kiekį arba pastovią nurašymų sumą.</span><span class="sxs-lookup"><span data-stu-id="848f8-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="848f8-105">Įkainojimo partijos dydžio sąvoka naudojama amortizuoti šias pastovias išlaidas pagamintos prekės apskaičiuotose išlaidose.</span><span class="sxs-lookup"><span data-stu-id="848f8-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="848f8-106">Ši sąvoka turi keletą sinonimų, vienas iš kurių – apskaitos partijos dydis.</span><span class="sxs-lookup"><span data-stu-id="848f8-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="848f8-107">Amortizuojamų pastovių išlaidų sąvoka taip pat turi keletą sinonimų, vienas iš kurių – proporcinės pastovios išlaidos.</span><span class="sxs-lookup"><span data-stu-id="848f8-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>

<span data-ttu-id="848f8-108">Pagamintos prekės įkainojimo partijos dydžio kiekis naudojamas komplektavimo specifikacijai (KS) skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="848f8-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="848f8-109">Kiekis priklauso nuo KS skaičiavimo inicijavimo ir atlikimo, kaip pateikta toliau:</span><span class="sxs-lookup"><span data-stu-id="848f8-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>

-   <span data-ttu-id="848f8-110">Prekės KS skaičiavimo numatytasis skaičiavimo kiekis – prekės standartinis atsargų užsakymo kiekis veikia kaip įkainojimo partijos dydis, tačiau numatytoji reikšmė gali būti didesnis kiekis, kad atspindėtų prekės užsakymo sudėtinį kiekį.</span><span class="sxs-lookup"><span data-stu-id="848f8-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="848f8-111">Prekės standartinis užsakymo kiekis ir sudėtinis kiekis gali būti nustatomi savo numatytuose užsakymo parametruose arba nuo teritorijos priklausomuose užsakymo parametruose.</span><span class="sxs-lookup"><span data-stu-id="848f8-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="848f8-112">Nurodytas skaičiavimo kiekis skaičiuojant prekės KS  – nurodytas skaičiavimo kiekis yra prekės įkainojimo partijos dydis.</span><span class="sxs-lookup"><span data-stu-id="848f8-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="848f8-113">Skaičiavimo kiekis iš pradžių naudoja prekės standartinio užsakymo kiekį, tačiau numatytoji reikšmė gali būti panaikinama rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="848f8-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="848f8-114">Nurodytas skaičiavimo kiekis rodo nurodytos prekės ir pagamintų komponentų, turinčių gamybos KS eilutės tipą, įkainojimo partijos dydį.</span><span class="sxs-lookup"><span data-stu-id="848f8-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="848f8-115">Tai svarbu, nes laikoma, kad komponentas bus pagamintas tiksliu kiekiu.</span><span class="sxs-lookup"><span data-stu-id="848f8-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="848f8-116">Kitų pagamintų komponentų, turinčių prekės KS eilutės tipą, įkainojimo partijos dydis parodys jų standartinį užsakymo kiekį.</span><span class="sxs-lookup"><span data-stu-id="848f8-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="848f8-117">Nurodytas gamybos pagal užsakymą skaičiavimo kiekis skaičiuojant prekės KS − nurodytas skaičiavimo kiekis yra prekės ir jos pagamintų komponentų įkainojimo partijos dydis, kai KS skaičiavimai naudoja gamybos pagal užsakymą išskleidimo režimą.</span><span class="sxs-lookup"><span data-stu-id="848f8-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="848f8-118">Laikoma, kad pagaminti komponentai bus gaminami tiksliu kiekiu, kaip ir pagamintas komponentas, turintis gamybos KS eilutės tipą.</span><span class="sxs-lookup"><span data-stu-id="848f8-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="848f8-119">Nustatytas skaičiavimo kiekis skaičiuojant būdingą užsakymui KS − būdingo užsakymui KS skaičiavimas gali būti atliekamas pardavimo užsakymo, pardavimo pasiūlymo arba aptarnavimo užsakymo eilutės elementui.</span><span class="sxs-lookup"><span data-stu-id="848f8-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="848f8-120">Nurodytas skaičiavimo kiekis naudoja pradinio eilutės elemento kiekį, tačiau numatytojo kiekio galima nepaisyti.</span><span class="sxs-lookup"><span data-stu-id="848f8-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="848f8-121">Galite pasirinkti, ar būdingas užsakymui KS skaičiavimas naudos gamybos pagal užsakymą, ar daugialygmenį išskleidimo režimą.</span><span class="sxs-lookup"><span data-stu-id="848f8-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="848f8-122">Pagamintos prekės amortizuotų pastovių išlaidų apskaičiuota suma laikoma išlaidomis.</span><span class="sxs-lookup"><span data-stu-id="848f8-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>





