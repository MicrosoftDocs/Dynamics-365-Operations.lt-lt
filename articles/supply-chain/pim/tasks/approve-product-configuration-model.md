---
title: Patvirtinti produkto konfigūracijos modelį
description: Norint paleisti šią procedūrą, reikia, kad būtų galimas bent vienas produkto konfigūracijos modelis.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa0027382e08a23c4dc1e782773a20db441d4f27
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208368"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="99e35-103">Patvirtinti produkto konfigūracijos modelį</span><span class="sxs-lookup"><span data-stu-id="99e35-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99e35-104">Norint paleisti šią procedūrą, reikia, kad būtų galimas bent vienas produkto konfigūracijos modelis.</span><span class="sxs-lookup"><span data-stu-id="99e35-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="99e35-105">Šiai procedūrai atlikti naudojamas aukščiausios kokybės garsiakalbio iš modelis demonstracinės įmonės USMF.</span><span class="sxs-lookup"><span data-stu-id="99e35-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="99e35-106">Atkreipkite dėmesį, kad šis modelis jau patvirtintas, bet procedūra padės viso proceso metu.</span><span class="sxs-lookup"><span data-stu-id="99e35-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="99e35-107">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="99e35-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="99e35-108">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="99e35-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="99e35-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="99e35-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="99e35-110">Šiai procedūrai pasirinkite aukščiausios kokybės garsiakalbio modelį.</span><span class="sxs-lookup"><span data-stu-id="99e35-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="99e35-111">Spustelėkite Versijos.</span><span class="sxs-lookup"><span data-stu-id="99e35-111">Click Versions.</span></span>
5. <span data-ttu-id="99e35-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="99e35-112">Click New.</span></span>
6. <span data-ttu-id="99e35-113">Lauke Produkto numeris įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="99e35-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="99e35-114">Nuoroda į produktą nurodo produkto konfigūracijos modelio versiją.</span><span class="sxs-lookup"><span data-stu-id="99e35-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="99e35-115">Šiame sąraše bus rodomi tik bendrieji produktai, kurių technologija yra konfigūravimas pagal apribojimus.</span><span class="sxs-lookup"><span data-stu-id="99e35-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="99e35-116">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="99e35-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="99e35-117">Pasirinkite, kada bus galima naudoti produkto modelio versiją.</span><span class="sxs-lookup"><span data-stu-id="99e35-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="99e35-118">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="99e35-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="99e35-119">Pasirinkite pabaigos datą, kada šio produkto modelio versijos galiojimas baigsis, arba pasirinkite Niekada.</span><span class="sxs-lookup"><span data-stu-id="99e35-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="99e35-120">Spustelėję Tvirtinti atidarysite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="99e35-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="99e35-121">Lauke Patvirtino įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="99e35-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="99e35-122">Pasirinkti asmenį, kuris yra atsakingas už produkto modelių patvirtinimą naudoti operacijų metu.</span><span class="sxs-lookup"><span data-stu-id="99e35-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="99e35-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="99e35-123">Click OK.</span></span>
12. <span data-ttu-id="99e35-124">Lauke Kainodaros pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="99e35-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="99e35-125">Aktyvinkite produkto modelio versiją.</span><span class="sxs-lookup"><span data-stu-id="99e35-125">Activate the product model version.</span></span> <span data-ttu-id="99e35-126">Vienu metu vieno produkto modeliui aktyvus gali būti tik vienas produktas.</span><span class="sxs-lookup"><span data-stu-id="99e35-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="99e35-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="99e35-127">Close the page.</span></span>

