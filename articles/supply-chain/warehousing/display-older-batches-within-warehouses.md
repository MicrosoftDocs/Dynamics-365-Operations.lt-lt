---
title: "Senesnių paketų sandėlyje rodymo konfigūravimas mobiliajame įrenginyje"
description: "Šioje temoje aprašoma, kaip nustatyti mobilųjį įrenginį, kad jame būtų rodomas vietų su senesniais už dabartinę darbo eilutės vietą paketų vietų sąrašas."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 3e9386f6da7b8bdc1cbb817a78f72c225cbaa9bc
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---

# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="29c91-103">Senesnių paketų sandėlyje rodymo konfigūravimas mobiliajame įrenginyje</span><span class="sxs-lookup"><span data-stu-id="29c91-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="29c91-104">Konfigūracija **Rodyti senesnius paketus sandėlyje** leidžia rodyti vietų su senesniais už dabartinę darbo eilutės vietą paketų vietų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="29c91-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="29c91-105">Rodomame vietų sąraše pateikiama informacija apie senesnius toje vietoje paketus ir galiojimo data bei kiekvieno paketo faktinės atsargos.</span><span class="sxs-lookup"><span data-stu-id="29c91-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="29c91-106">Galite pasirinkti paėmimą iš naujos vietos arba tęsti paėmimą iš dabartinės vietos.</span><span class="sxs-lookup"><span data-stu-id="29c91-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="29c91-107">Paėmimas iš naujos vietos – jei pasirinksite naują vietą, iš kurios norite atlikti paėmimą, dabartinė darbo eilutė bus atnaujinta į naują vietą, o darbas bus tęsiamas įprastai naujoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="29c91-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="29c91-108">Kad nauja vieta būtų tinkama, joje turi būti pakankamai kiekio, kad jo užtektų visai darbo eilutei.</span><span class="sxs-lookup"><span data-stu-id="29c91-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="29c91-109">Jei reikalaujamo kiekio nėra, darbo eilutė atnaujinta nebus ir bus rodomas sąrašas.</span><span class="sxs-lookup"><span data-stu-id="29c91-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="29c91-110">Paėmimo tęsimas iš dabartinės vietos – jei ir toliau naudosite dabartinės darbo eilutės vietą, darbo eilutės kiekiai toliau bus imami iš pradinės vietos.</span><span class="sxs-lookup"><span data-stu-id="29c91-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="29c91-111">Kai taikoma</span><span class="sxs-lookup"><span data-stu-id="29c91-111">Where it applies</span></span>
<span data-ttu-id="29c91-112">Parinktis Senesnių paketų sandėlyje rodymas sukonfigūruota mobiliojo įrenginio meniu elementuose ir paveikia toliau nurodytus paketo paėmimo elementus.</span><span class="sxs-lookup"><span data-stu-id="29c91-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="29c91-113">Parinkties Senesnių paketų sandėlyje rodymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="29c91-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="29c91-114">Konfigūraciją **Senesnių paketų sandėlyje rodymas** galima naudoti mobiliojo įrenginio meniu elementams, kai parinktis **Paimti seniausią paketą** nustatyta į **Įspėti**.</span><span class="sxs-lookup"><span data-stu-id="29c91-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="29c91-115">Parinktyje **Sandėlio valdymas** > **Sąranka** > **Mobilusis įrenginys** > **Mobiliojo įrenginio meniu elementai** nustatykite meniu elemento parinktį **Naudoti esamą darbą** į **Taip** ir lauke **Paimti seniausią paketą** pasirinkite **Įspėti**.</span><span class="sxs-lookup"><span data-stu-id="29c91-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 

