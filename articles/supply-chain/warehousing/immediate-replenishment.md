---
title: Skubus papildymas
description: "Šioje temoje aprašoma, kaip galite naudoti skubų papildymą, norėdami papildyti atsargas, kai vietos nurodymui nepavyksta paskirstyti atsargų."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocDirTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: ab1f06951d5daceaf002b2cc23236dd818457985
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---

# <a name="immediate-replenishment"></a><span data-ttu-id="f6e9b-103">Skubus papildymas</span><span class="sxs-lookup"><span data-stu-id="f6e9b-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6e9b-104">Skubus papildymas suteikia galimybę skubiai papildyti atsargas, kai vietos nurodymo eilutei nepavyksta paskirstyti atsargų.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="f6e9b-105">Papildymas pagrįstas viena vietos nurodymo sąrankos eilute.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="f6e9b-106">Jei nėra atsargų, pateikiamų matavimo vienetu, kuris nurodytas toje eilutėje, to matavimo vieneto papildymas pradedamas iš karto.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="f6e9b-107">Skubus papildymas suteikia alternatyvą metodui, kurį naudojant atsargų paskirstymas pagrįstas didesniu vietos nurodymo eilučių skaičiumi, o poreikis sumuojamas paskirstymo pabaigoje ir papildomas naudojant matavimo vienetą, kuris nurodytas vietos nurodymo paskutinėje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="f6e9b-108">Skubaus papildymo naudojimo nauda yra ta, kad papildymą galima apriboti specialiais vienetais, o kiekį galima nukreipti į tam tikras vietas.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="f6e9b-109">Verslo scenarijus</span><span class="sxs-lookup"><span data-stu-id="f6e9b-109">Business scenario</span></span>

<span data-ttu-id="f6e9b-110">Pavyzdžiui, turite sandėlį, kuriame nustatytos atskiros paėmimo sritys, skirtos matavimo vienetams „dėžė“ ir „vnt.“.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="f6e9b-111">Norite optimizuoti išrinkimo procesą paimdami kiek įmanoma daugiau dėžių ir tada paimdami visą likusį kiekį, kuris yra mažesnis nei dėžėje telpantis kiekis, iš srities „vnt.“.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="f6e9b-112">Tokiu atveju galite naudoti skubų papildymą.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="f6e9b-113">Vietos nurodyme galite nustatyti skubų dėžių papildymą, kad poreikio papildymas būtų naudojamas iš karto, kai pritrūksta dėžių, kurias galima paimti poreikio kiekiui patenkinti.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="f6e9b-114">Tokiu būdu optimizuosite išrinkimo procesą, kad paėmimas apimtų kiek įmanoma daugiau dėžių.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="f6e9b-115">Skubus papildymas sukurs dėžių papildymą ir poreikis bus patenkintas, o kiekiai bus paimami naudojant matavimo vienetą „vnt.“.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="f6e9b-116">Kitaip tariant, iš srities „vnt.“ bus paimti tik kiekiai, kuriuos reikia paimti iš srities „vnt.“ (t. y. kiekiai, kurie yra mažesni nei viena dėžė).</span><span class="sxs-lookup"><span data-stu-id="f6e9b-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="f6e9b-117">Jei srityje „vnt.“ pasireikš trūkumas, galėsite paimti tiek tik įmanoma dėžių iš viso poreikio.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="f6e9b-118">Tada likę kiekiai bus paimti iš srities „vnt.“.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="f6e9b-119">Kai taikoma</span><span class="sxs-lookup"><span data-stu-id="f6e9b-119">Where it applies</span></span>

<span data-ttu-id="f6e9b-120">Skubus papildymas naudojamas vykdant bangą, jei nepavyksta paskirstyti vietos nurodymo eilutės, kuriai priskirtas papildymo šablonas.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="f6e9b-121">Skubaus papildymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="f6e9b-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="f6e9b-122">Pasirinkite **Sandėlio valdymas** \> **Sąranka** \> **Vietos nurodymai**, tada skirtuko **Eilutės** sąraše **Skubaus papildymo šablonas** pasirinkite bangos poreikio papildymo šabloną.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-122">Go to **Warehouse management** \> **Setup** \> **Location directives**, and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="f6e9b-123">Papildymo šablonas taikomas, jei vietos nurodymo eilutei nepavyksta paskirstyti kiekio naudojant nurodytą matavimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="f6e9b-124">Trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="f6e9b-124">Troubleshooting</span></span>

<span data-ttu-id="f6e9b-125">Jei vietos nurodymo eilutėje pasirenkamas skubus papildymas, bet nesugeneruojamas joks papildymo darbas, kai naudojate tos vietos nurodymo eilutės poreikio papildymo šablonus, būtina atlikti du pagrindinius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="f6e9b-126">Įsitikinkite, kad taikomas poreikio papildymo šablonas nustatytas naudoti teisingus tipo **Papildymas** vietos šablonus ir darbo šablonus.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="f6e9b-127">Įsitikinkite, kad turimų atsargų pakanka vietose, kuriose poreikio papildymo šablonas ieško turimų papildymo atsargų.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>
