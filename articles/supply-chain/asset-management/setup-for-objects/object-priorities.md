---
title: Pasirinkite paslaugos lygį.
description: Šioje temoje pasakojama apie turto aptarnavimo lygius, esančius modulyje „Turto valdymas“.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2730dad0a130dfd3916ae51e9be6d81f97c22b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238091"
---
# <a name="asset-service-levels"></a><span data-ttu-id="7de8d-103">Pasirinkite paslaugos lygį.</span><span class="sxs-lookup"><span data-stu-id="7de8d-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7de8d-104">Šioje temoje pasakojama apie turto aptarnavimo lygius, esančius modulyje „Turto valdymas“.</span><span class="sxs-lookup"><span data-stu-id="7de8d-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="7de8d-105">Turto aptarnavimo lygiai yra susiję su turtu ir perkeliami į priežiūros užklausas ir darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="7de8d-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="7de8d-106">Planuojant darbo užsakymą, jie yra naudojami apskaičiuoti darbo užsakymų prioritetą.</span><span class="sxs-lookup"><span data-stu-id="7de8d-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="7de8d-107">Prireikus, galima keisti turto aptarnavimo lygius.</span><span class="sxs-lookup"><span data-stu-id="7de8d-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="7de8d-108">Daugiau informacijos apie konfigūraciją, susijusią su darbo užsakymo planavimo vertinimo rezultatų skaičiavimu, žr. [Turto valdymo parametrai](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7de8d-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="7de8d-109">Turite nustatyti bent vieną turto aptarnavimo lygio numatytąjį įrašą.</span><span class="sxs-lookup"><span data-stu-id="7de8d-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="7de8d-110">Šis numatytasis įrašas naudojamas, jei planuojant darbo užsakymą, nerandama kitų atitikčių.</span><span class="sxs-lookup"><span data-stu-id="7de8d-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="7de8d-111">**1 pavyzdys:** Numatytasis paslaugų lygis, naudojamas, jei nerandama kita atitiktis.</span><span class="sxs-lookup"><span data-stu-id="7de8d-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="7de8d-112">Šiame įraše pažymite tik aptarnavimo lygį.</span><span class="sxs-lookup"><span data-stu-id="7de8d-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="7de8d-113">**2 pavyzdys:** Aukštas aptarnavimo lygis, naudojamas planuojant „Volvo“ sunkvežimio variklio darbus.</span><span class="sxs-lookup"><span data-stu-id="7de8d-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="7de8d-114">Šiame įraše pažymite atitinkamą turto tipą (pvz., **sunkvežimio variklis**), gamintoją (**„Volvo“**) ir aptarnavimo lygį.</span><span class="sxs-lookup"><span data-stu-id="7de8d-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="7de8d-115">Nustatykite paslaugos lygį.</span><span class="sxs-lookup"><span data-stu-id="7de8d-115">Set up asset service levels</span></span>

1. <span data-ttu-id="7de8d-116">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turto paslaugų lygiai**.</span><span class="sxs-lookup"><span data-stu-id="7de8d-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="7de8d-117">Pasirinkite **Naujas** pranešimui sukurti.</span><span class="sxs-lookup"><span data-stu-id="7de8d-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="7de8d-118">Atsižvelgdami į reikiamą turto aptarnavimo lygio informacijos lygį, pažymėkite atitinkamus duomenis laukuose **Funkcinė vieta**, **Turto tipas**, **Gamintojas**, **Modelis**, **Turtas**, **Darbo užsakymo tipas** ir **Aptarnavimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="7de8d-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7de8d-119">Kai turto aptarnavimo lygis naudojamas dirbant su priežiūros užklausomis ir darbo užsakymais, modulis „Turto valdymas“ apdoroja visus turto dokumentų įrašus ir ieško galimos atitikties.</span><span class="sxs-lookup"><span data-stu-id="7de8d-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="7de8d-120">Jis visada pirmiausiai tikrina konkrečiausius derinius.</span><span class="sxs-lookup"><span data-stu-id="7de8d-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="7de8d-121">Kitaip tariant, modulyje „Turto valdymas“ visų pirma ieškoma lauko **Darbo užsakymo tipas** atitikties.</span><span class="sxs-lookup"><span data-stu-id="7de8d-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="7de8d-122">Jei atitiktis nerasta, ieškoma lauko **Turtas** atitikties ir t. t.</span><span class="sxs-lookup"><span data-stu-id="7de8d-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="7de8d-123">Kaip matote pagal puslapio **Turto aptarnavimo lygiai** išdėstymą, toks paieškos metodas reiškia, kad, siekiant rasti konkrečiausią derinį, modulyje „Turto valdymas“, kiekviename įraše atitikčių ieškoma iš dešinės į kairę.</span><span class="sxs-lookup"><span data-stu-id="7de8d-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="7de8d-124">Jei atitikties rasti nepavyksta, naudojamas numatytasis įrašas, kuris tuose laukuose pasirinkčių neturi.</span><span class="sxs-lookup"><span data-stu-id="7de8d-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="7de8d-125">Lauke **Aptarnavimo lygis** pasirinkite skaičių, nurodantį aptarnavimo lygį (prioritetą).</span><span class="sxs-lookup"><span data-stu-id="7de8d-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="7de8d-126">Jei puslapyje **Turto aptarnavimo lygiai** pakeisite turto aptarnavimo lygio įrašą, kurį jau naudojote darbo užsakyme, priežiūros užklausų ir darbo užsakymų aptarnavimo lygis nebus atitinkamai atnaujintas.</span><span class="sxs-lookup"><span data-stu-id="7de8d-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]