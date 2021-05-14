---
title: Neatitikimų diagnostikos tipai
description: Šioje temoje aprašoma, kaip naudoti ir kurti diagnozės tipus, kurie gali būti naudojami su neatitiktimis.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19fcd57e28efabd6ca32c444ab961b876bde424d
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956753"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="2d5de-103">Neatitikimų diagnostikos tipai</span><span class="sxs-lookup"><span data-stu-id="2d5de-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d5de-104">Šioje temoje aprašoma, kaip naudoti ir kurti diagnozės tipus, kurie gali būti naudojami su neatitiktimis.</span><span class="sxs-lookup"><span data-stu-id="2d5de-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="2d5de-105">Naudodami puslapį **Diagnostikos tipai** nurodykite diagnostikos veiksmų klasifikaciją.</span><span class="sxs-lookup"><span data-stu-id="2d5de-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="2d5de-106">Tada, kai sukuriate neatitikties pataisymą, pasirenkate diagnostiką.</span><span class="sxs-lookup"><span data-stu-id="2d5de-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="2d5de-107">Koregavimu nurodoma, kurio diagnostinio veiksmo turi būti imtasi, atsiradus patvirtintai neatitikčiai, ir kas turėtų imtis veiksmų.</span><span class="sxs-lookup"><span data-stu-id="2d5de-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="2d5de-108">Juo taip pat nurodoma pageidaujama užbaigimo data ir planuojama užbaigimo data.</span><span class="sxs-lookup"><span data-stu-id="2d5de-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="2d5de-109">Diagnostikos tipų pavyzdžiai:</span><span class="sxs-lookup"><span data-stu-id="2d5de-109">Examples of diagnostic types</span></span>

<span data-ttu-id="2d5de-110">Jūs dirbate gamybos įmonei ir kelių prekių kokybės bandymai nesėkmingi.</span><span class="sxs-lookup"><span data-stu-id="2d5de-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="2d5de-111">Šios prekės perkeliamos į sulaikymo sritį ir pažymėtos kaip neatitikties produktai.</span><span class="sxs-lookup"><span data-stu-id="2d5de-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="2d5de-112">Sukuriamas neatitikties įrašas taip, kad „Microsoft Dynamics 365 Supply Chain Management“ būtų galima stebėti išsamią informaciją naudojant išdavimo sprendimą.</span><span class="sxs-lookup"><span data-stu-id="2d5de-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="2d5de-113">Tokiu atveju kokybės problemos atsiranda dėl to, kad gamybos mašinos, kuri pakuoja prekes, buvo blogos ir yra per daug viršinės.</span><span class="sxs-lookup"><span data-stu-id="2d5de-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="2d5de-114">Šios problemos sprendimas yra pakeisti įrenginio dalis.</span><span class="sxs-lookup"><span data-stu-id="2d5de-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="2d5de-115">Konfigūruokite diagnozės tipus, galite sukurti kelis įrašus, iš kurių kiekvienas nurodo skirtingą mašinos problemų tipą.</span><span class="sxs-lookup"><span data-stu-id="2d5de-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="2d5de-116">Arba galite sukurti vieną bendrąjį diagnostikos tipą, kuris pristato mašinos remontą.</span><span class="sxs-lookup"><span data-stu-id="2d5de-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="2d5de-117">Diagnozės tipo kūrimas</span><span class="sxs-lookup"><span data-stu-id="2d5de-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="2d5de-118">Pasirinkite **Atsargų valdymas \> Nustatymas \> Kokybės valdymas \> Diagnostikos tipai**.</span><span class="sxs-lookup"><span data-stu-id="2d5de-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="2d5de-119">Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="2d5de-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="2d5de-120">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="2d5de-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="2d5de-121">**Diagnostika** – Įveskite unikalų ID ar diagnostikos tipo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="2d5de-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="2d5de-122">**Aprašas** – įveskite išsamų diagnostikos tipo aprašą.</span><span class="sxs-lookup"><span data-stu-id="2d5de-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="2d5de-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2d5de-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d5de-124">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2d5de-124">Additional resources</span></span>

- [<span data-ttu-id="2d5de-125">Kokybės valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="2d5de-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="2d5de-126">Įjungti kiekio ir neatitikties valdymą</span><span class="sxs-lookup"><span data-stu-id="2d5de-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="2d5de-127">Darbuotojai, atsakingi už neatitikties tvirtinimą</span><span class="sxs-lookup"><span data-stu-id="2d5de-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="2d5de-128">Neatitikimų sulaikymo zonos</span><span class="sxs-lookup"><span data-stu-id="2d5de-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="2d5de-129">Neatitikimų diagnostikos problemos</span><span class="sxs-lookup"><span data-stu-id="2d5de-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="2d5de-130">Neatitikimų kokybės mokesčiai</span><span class="sxs-lookup"><span data-stu-id="2d5de-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="2d5de-131">Neatitikties operacijos</span><span class="sxs-lookup"><span data-stu-id="2d5de-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="2d5de-132">Sandėlio procesų kokybės valdymas</span><span class="sxs-lookup"><span data-stu-id="2d5de-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
