--- 
title: "Prižiūrėti brūkšninių kodų tipus"
description: "Ši procedūra nurodo, kaip nustatyti naują brūkšninio kodo aprašą, kurį būtų galima naudoti kaip išrinkimo dokumento ataskaitos dalį."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a0d7092228f078f528ec1cb9ac56d7034c44bccf
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="maintain-barcode-types"></a><span data-ttu-id="91bc0-103">Prižiūrėti brūkšninių kodų tipus</span><span class="sxs-lookup"><span data-stu-id="91bc0-103">Maintain barcode types</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91bc0-104">Ši procedūra nurodo, kaip nustatyti naują brūkšninio kodo aprašą, kurį būtų galima naudoti kaip išrinkimo dokumento ataskaitos dalį.</span><span class="sxs-lookup"><span data-stu-id="91bc0-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="91bc0-105">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="91bc0-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="91bc0-106">Jei naudojate USMF, galite naudoti rodomas pavyzdines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="91bc0-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="91bc0-107">Šias užduotis paprastai turėtų atlikti sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="91bc0-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="91bc0-108">Eiti į brūkšninius kodus.</span><span class="sxs-lookup"><span data-stu-id="91bc0-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="91bc0-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="91bc0-109">Click New.</span></span>
3. <span data-ttu-id="91bc0-110">Lauke Brūkšninio kodo sąranka įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="91bc0-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="91bc0-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="91bc0-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="91bc0-112">Lauke Brūkšninio kodo tipas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="91bc0-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="91bc0-113">Jei naudojate USMF, galite pasirinkti „Kodas 39“.</span><span class="sxs-lookup"><span data-stu-id="91bc0-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="91bc0-114">Lauke Dydis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="91bc0-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="91bc0-115">Lauke Didžiausias ilgis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="91bc0-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="91bc0-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="91bc0-116">Click Save.</span></span>
9. <span data-ttu-id="91bc0-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="91bc0-117">Close the page.</span></span>
10. <span data-ttu-id="91bc0-118">Eikite į Atsargų ir sandėlio valdymo parametrus.</span><span class="sxs-lookup"><span data-stu-id="91bc0-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="91bc0-119">Lauke Brūkšninio kodo nustatymas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="91bc0-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="91bc0-120">Pasirinkite anksčiau sukurtą brūkšninio kodo nustatymą, bet turėkite omenyje, kad brūkšninio kodo formatas turi atitikti procese naudojamo įrašo tipo unikalaus identifikatoriaus formatą.</span><span class="sxs-lookup"><span data-stu-id="91bc0-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="91bc0-121">Pavyzdžiui, išrinkimo maršrutų brūkšninio kodo formatas turi atitikti išrinkimo maršruto nuorodos formatą, kuris paprastai yra numerių seka.</span><span class="sxs-lookup"><span data-stu-id="91bc0-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="91bc0-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="91bc0-122">Click Save.</span></span>
13. <span data-ttu-id="91bc0-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="91bc0-123">Close the page.</span></span>


