---
title: Prižiūrėti brūkšninių kodų tipus
description: Ši procedūra nurodo, kaip nustatyti naują brūkšninio kodo aprašą, kurį būtų galima naudoti kaip išrinkimo dokumento ataskaitos dalį.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 979726a1d094146b546bbc6d31963367de2c59f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433852"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="8b53b-103">Prižiūrėti brūkšninių kodų tipus</span><span class="sxs-lookup"><span data-stu-id="8b53b-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b53b-104">Ši procedūra nurodo, kaip nustatyti naują brūkšninio kodo aprašą, kurį būtų galima naudoti kaip išrinkimo dokumento ataskaitos dalį.</span><span class="sxs-lookup"><span data-stu-id="8b53b-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="8b53b-105">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="8b53b-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="8b53b-106">Jei naudojate USMF, galite naudoti rodomas pavyzdines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="8b53b-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="8b53b-107">Šias užduotis paprastai turėtų atlikti sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="8b53b-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="8b53b-108">Eiti į brūkšninius kodus.</span><span class="sxs-lookup"><span data-stu-id="8b53b-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="8b53b-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8b53b-109">Click New.</span></span>
3. <span data-ttu-id="8b53b-110">Lauke Brūkšninio kodo sąranka įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="8b53b-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="8b53b-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8b53b-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8b53b-112">Lauke Brūkšninio kodo tipas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="8b53b-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="8b53b-113">Jei naudojate USMF, galite pasirinkti „Kodas 39“.</span><span class="sxs-lookup"><span data-stu-id="8b53b-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="8b53b-114">Lauke Dydis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8b53b-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="8b53b-115">Lauke Didžiausias ilgis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8b53b-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="8b53b-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8b53b-116">Click Save.</span></span>
9. <span data-ttu-id="8b53b-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8b53b-117">Close the page.</span></span>
10. <span data-ttu-id="8b53b-118">Eikite į Atsargų ir sandėlio valdymo parametrus.</span><span class="sxs-lookup"><span data-stu-id="8b53b-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="8b53b-119">Lauke Brūkšninio kodo nustatymas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="8b53b-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="8b53b-120">Pasirinkite anksčiau sukurtą brūkšninio kodo nustatymą, bet turėkite omenyje, kad brūkšninio kodo formatas turi atitikti procese naudojamo įrašo tipo unikalaus identifikatoriaus formatą.</span><span class="sxs-lookup"><span data-stu-id="8b53b-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="8b53b-121">Pavyzdžiui, išrinkimo maršrutų brūkšninio kodo formatas turi atitikti išrinkimo maršruto nuorodos formatą, kuris paprastai yra numerių seka.</span><span class="sxs-lookup"><span data-stu-id="8b53b-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="8b53b-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8b53b-122">Click Save.</span></span>
13. <span data-ttu-id="8b53b-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8b53b-123">Close the page.</span></span>

