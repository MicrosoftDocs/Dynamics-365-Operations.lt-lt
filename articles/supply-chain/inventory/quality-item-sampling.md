---
title: Kokybės valdymo prekės ėmimas
description: Šioje temoje aprašoma, kaip nustatyti prekės mėginius.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022233"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="48eac-103">Kokybės valdymo prekės ėmimas</span><span class="sxs-lookup"><span data-stu-id="48eac-103">Quality management item sampling</span></span>

<span data-ttu-id="48eac-104">Prekės ėmimas naudojamas kaip kokybės susiejimo dalis.</span><span class="sxs-lookup"><span data-stu-id="48eac-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="48eac-105">Jis nurodo dabartinių faktinių atsargų kiekį, kuris turi būti patikrintas.</span><span class="sxs-lookup"><span data-stu-id="48eac-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="48eac-106">Pavyzdžių ėmimas gali būti paremtas fiksuotais kiekiais, procentine dalimi arba visa numerio lentele.</span><span class="sxs-lookup"><span data-stu-id="48eac-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="48eac-107">Nustatyti prekių pavyzdžių ėmimą</span><span class="sxs-lookup"><span data-stu-id="48eac-107">Set up item sampling</span></span>

<span data-ttu-id="48eac-108">Atlikite šiuos žingsnius, kad nustatytumėte prekės mėginius.</span><span class="sxs-lookup"><span data-stu-id="48eac-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="48eac-109">Eikite į **Atsargų valdymas \> Nustatymas \> Kokybės kontrolė \> Prekių pavyzdžių ėmimas**.</span><span class="sxs-lookup"><span data-stu-id="48eac-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="48eac-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="48eac-110">Select **New**.</span></span>
1. <span data-ttu-id="48eac-111">Lauke **Prekės pavyzdys** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="48eac-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="48eac-112">Lauke **Aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="48eac-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="48eac-113">Lauke **Reikšmė** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="48eac-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="48eac-114">Ši reikšmė yra susijusi su Kiekio specifikacijos verte, pasirinkta greta esančiame lauke.</span><span class="sxs-lookup"><span data-stu-id="48eac-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="48eac-115">Proceso skyriuje pažymėkite visiško blokavimo žymės langelį, jei visa partija arba užsakymo eilutės kiekis turi būti **užblokuoti**, jei tikrinimas **nepavyko**.</span><span class="sxs-lookup"><span data-stu-id="48eac-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="48eac-116">Jei šis žymės langelis išvalytas, jei tikrinimas nepavyko, bus blokuojamos tik kokybės užsakymo prekės.</span><span class="sxs-lookup"><span data-stu-id="48eac-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="48eac-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="48eac-117">Select **Save**.</span></span>
1. <span data-ttu-id="48eac-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="48eac-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="48eac-119">Funkcija *Sandėlio procesų kokybės valdymas* pateikia papildomų prekių pavyzdžių ėmimo galimybių.</span><span class="sxs-lookup"><span data-stu-id="48eac-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="48eac-120">Ji įtraukia *prekių pavyzdžių ėmimo aprėpties* sąvoką ir galimybę apibrėžti visą numerio lentelę kaip kiekio specifikaciją.</span><span class="sxs-lookup"><span data-stu-id="48eac-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="48eac-121">Jei įgalinote šią funkciją, norėdami gauti išsamios informacijos žr. [Sandėlio procesų kokybės valdymas](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="48eac-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
