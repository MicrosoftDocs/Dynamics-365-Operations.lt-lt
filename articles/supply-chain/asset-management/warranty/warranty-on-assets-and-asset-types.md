---
title: Turto ir jo tipų garantijos
description: Šioje temoje paaiškinama, kaip modulyje Turto valdymas nustatyti turto ir jo tipų garantijas.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b13f8aba7e1d2448495f97a4772eb573e08c025
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874606"
---
# <a name="warranty-on-assets-and-asset-types"></a><span data-ttu-id="0faf6-103">Turto ir jo tipų garantija</span><span class="sxs-lookup"><span data-stu-id="0faf6-103">Warranty on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="0faf6-104">Šioje temoje paaiškinama, kaip modulyje Turto valdymas nustatyti turto ir jo tipų garantijas.</span><span class="sxs-lookup"><span data-stu-id="0faf6-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="0faf6-105">Turto tipo garantijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="0faf6-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="0faf6-106">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turto tipai** \> **Turto tipai**.</span><span class="sxs-lookup"><span data-stu-id="0faf6-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="0faf6-107">Kairiojoje srityje pasirinkite turto tipą, prie kurio norite pridėti tiekėjo garantijos sutartį, tada pasirinkite **Numatytosios turto tipo reikšmės**.</span><span class="sxs-lookup"><span data-stu-id="0faf6-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="0faf6-108">„FastTab“ konteinerio **Bendra** lauke **Tiekėjo garantija** pasirinkite sutartį.</span><span class="sxs-lookup"><span data-stu-id="0faf6-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="0faf6-109">Turto garantijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="0faf6-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="0faf6-110">Pasirinkite **Turto valdymas** \> **Bendra** \> **Turtas** \> **Visas turtas**.</span><span class="sxs-lookup"><span data-stu-id="0faf6-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="0faf6-111">Pasirinkite turtą, tada – **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="0faf6-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="0faf6-112">„FastTab“ konteinerio **Tiekėjas** skyriaus **Tiekėjo garantija** lauke **Garantija** pasirinkite garantijos sutartį.</span><span class="sxs-lookup"><span data-stu-id="0faf6-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="0faf6-113">Laukuose **Garantijos pradžia** ir **Garantijos pabaiga** pasirinkite pradžios bei pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="0faf6-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="0faf6-114">Jei darbo užsakymo lauke **Garantijos pradžia** yra pasirinkta data, darbo užsakymo garantija pradeda galioti tą dieną.</span><span class="sxs-lookup"><span data-stu-id="0faf6-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="0faf6-115">Kuriant darbo užsakymą, laukas **Garantijos pradžia** automatiškai nustatomas kaip sukūrimo data.</span><span class="sxs-lookup"><span data-stu-id="0faf6-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="0faf6-116">Tačiau šią datą galite pakeisti, kad jį atitiktų, pavyzdžiui, garantijos sutarties pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="0faf6-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![1 pav.](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="0faf6-118">Jei, kuriant turto, kuriam taikoma tiekėjo garantija, darbo užsakymą, yra numatyta darbo užsakymo garantijos laikotarpio pradžios data, gaunate pranešimą apie garantijos sutartį.</span><span class="sxs-lookup"><span data-stu-id="0faf6-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="0faf6-119">Tada, jei reikia, darbo užsakymą galite atšaukti.</span><span class="sxs-lookup"><span data-stu-id="0faf6-119">You can then cancel the work order, as you require.</span></span>
