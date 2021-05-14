---
title: Kokybės valdymo prekės ėmimas
description: Šioje temoje aprašoma, kaip nustatyti prekės mėginius.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956752"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="d57fe-103">Kokybės valdymo prekės ėmimas</span><span class="sxs-lookup"><span data-stu-id="d57fe-103">Quality management item sampling</span></span>

<span data-ttu-id="d57fe-104">Prekės ėmimas naudojamas kaip kokybės susiejimo dalis.</span><span class="sxs-lookup"><span data-stu-id="d57fe-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="d57fe-105">Jis nurodo dabartinių faktinių atsargų kiekį, kuris turi būti patikrintas.</span><span class="sxs-lookup"><span data-stu-id="d57fe-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="d57fe-106">Pavyzdžių ėmimas gali būti paremtas fiksuotais kiekiais, procentine dalimi arba visa numerio lentele.</span><span class="sxs-lookup"><span data-stu-id="d57fe-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="d57fe-107">Nustatyti prekių pavyzdžių ėmimą</span><span class="sxs-lookup"><span data-stu-id="d57fe-107">Set up item sampling</span></span>

<span data-ttu-id="d57fe-108">Atlikite šiuos žingsnius, kad nustatytumėte prekės mėginius.</span><span class="sxs-lookup"><span data-stu-id="d57fe-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="d57fe-109">Eikite į **Atsargų valdymas \> Nustatymas \> Kokybės kontrolė \> Prekių pavyzdžių ėmimas**.</span><span class="sxs-lookup"><span data-stu-id="d57fe-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="d57fe-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d57fe-110">Select **New**.</span></span>
1. <span data-ttu-id="d57fe-111">Lauke **Prekės pavyzdys** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d57fe-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="d57fe-112">Lauke **Aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d57fe-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="d57fe-113">Lauke **Reikšmė** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d57fe-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="d57fe-114">Ši reikšmė yra susijusi su Kiekio specifikacijos verte, pasirinkta greta esančiame lauke.</span><span class="sxs-lookup"><span data-stu-id="d57fe-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="d57fe-115">Proceso skyriuje pažymėkite visiško blokavimo žymės langelį, jei visa partija arba užsakymo eilutės kiekis turi būti **užblokuoti**, jei tikrinimas **nepavyko**.</span><span class="sxs-lookup"><span data-stu-id="d57fe-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="d57fe-116">Jei šis žymės langelis išvalytas, jei tikrinimas nepavyko, bus blokuojamos tik kokybės užsakymo prekės.</span><span class="sxs-lookup"><span data-stu-id="d57fe-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="d57fe-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d57fe-117">Select **Save**.</span></span>
1. <span data-ttu-id="d57fe-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d57fe-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="d57fe-119">Funkcija *Sandėlio procesų kokybės valdymas* pateikia papildomų prekių pavyzdžių ėmimo galimybių.</span><span class="sxs-lookup"><span data-stu-id="d57fe-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="d57fe-120">Ji įtraukia *prekių pavyzdžių ėmimo aprėpties* sąvoką ir galimybę apibrėžti visą numerio lentelę kaip kiekio specifikaciją.</span><span class="sxs-lookup"><span data-stu-id="d57fe-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="d57fe-121">Jei įgalinote šią funkciją, norėdami gauti išsamios informacijos žr. [Sandėlio procesų kokybės valdymas](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="d57fe-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
