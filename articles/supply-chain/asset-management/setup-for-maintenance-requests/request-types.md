---
title: Priežiūros užklausų tipai
description: Šioje temoje aprašoma, kaip nustatyti priežiūros užklausos tipus modulyje „Turto valdymas“.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d353f084e0d3e056f1b5ff5af6437ba211def8ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433705"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="83834-103">Priežiūros užklausų tipai</span><span class="sxs-lookup"><span data-stu-id="83834-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="83834-104">Priežiūros užklausų tipai naudojami priežiūros užklausoms suskirstyti pagal kategorijas.</span><span class="sxs-lookup"><span data-stu-id="83834-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="83834-105">Pavyzdžiui, jūs galite turėti priežiūros užklausos tipus, kurie susiję su prevencine priežiūra ir korekcine priežiūra.</span><span class="sxs-lookup"><span data-stu-id="83834-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="83834-106">Arba galite turėti specialų priežiūros užklausos tipą, kuris naudojamas turto remontui (sandėlio remontui) valdyti.</span><span class="sxs-lookup"><span data-stu-id="83834-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="83834-107">Priežiūros užklausos tipas nurodo sąsają su priežiūros užklausos ciklo būsenos grupe (priežiūros užklausos modeliu).</span><span class="sxs-lookup"><span data-stu-id="83834-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="83834-108">Priežiūros užklausos ciklo modeliai nurodo ciklo būsenas, kurias galima nustatyti priežiūros užklausai.</span><span class="sxs-lookup"><span data-stu-id="83834-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="83834-109">(Priežiūros užklausos ciklo būsenų pavyzdžiai: **Sukurta**, **Aktyvi** ir **Baigta**.)</span><span class="sxs-lookup"><span data-stu-id="83834-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="83834-110">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Priežiūros užklausos** \> **Priežiūros užklausų tipai**.</span><span class="sxs-lookup"><span data-stu-id="83834-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="83834-111">Pasirinkite **Naujas**, kad sukurtumėte priežiūros užklausos tipą.</span><span class="sxs-lookup"><span data-stu-id="83834-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="83834-112">Lauke **Priežiūros užklausos tipas** įveskite priežiūros užklausos tipo ID.</span><span class="sxs-lookup"><span data-stu-id="83834-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="83834-113">Tada lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="83834-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="83834-114">„FastTab“ skirtuko **Bendra** lauke **Priežiūros užklausos ciklo modelis** pasirinkite priežiūros užklausos ciklo modelį.</span><span class="sxs-lookup"><span data-stu-id="83834-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="83834-115">Lauke **Darbo užsakymo tipas** pasirinkite darbo užsakymo tipą.</span><span class="sxs-lookup"><span data-stu-id="83834-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="83834-116">Konvertavus priežiūros užklausą į darbo užsakymą, darbo užsakymui automatiškai priskiriamas su priežiūros užklausos tipu susijęs darbo užsakymo tipas.</span><span class="sxs-lookup"><span data-stu-id="83834-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="83834-117">Paveikslėlyje pateiktas puslapio **Priežiūros užklausos tipai** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="83834-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Priežiūros užklausos tipų puslapis](media/07-setup-for-requests.png)
