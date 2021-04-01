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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e4f622cda62cad13a8146cbc26bc2e5f1a45222
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261194"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="600ca-103">Priežiūros užklausų tipai</span><span class="sxs-lookup"><span data-stu-id="600ca-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="600ca-104">Priežiūros užklausų tipai naudojami priežiūros užklausoms suskirstyti pagal kategorijas.</span><span class="sxs-lookup"><span data-stu-id="600ca-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="600ca-105">Pavyzdžiui, jūs galite turėti priežiūros užklausos tipus, kurie susiję su prevencine priežiūra ir korekcine priežiūra.</span><span class="sxs-lookup"><span data-stu-id="600ca-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="600ca-106">Arba galite turėti specialų priežiūros užklausos tipą, kuris naudojamas turto remontui (sandėlio remontui) valdyti.</span><span class="sxs-lookup"><span data-stu-id="600ca-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="600ca-107">Priežiūros užklausos tipas nurodo sąsają su priežiūros užklausos ciklo būsenos grupe (priežiūros užklausos modeliu).</span><span class="sxs-lookup"><span data-stu-id="600ca-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="600ca-108">Priežiūros užklausos ciklo modeliai nurodo ciklo būsenas, kurias galima nustatyti priežiūros užklausai.</span><span class="sxs-lookup"><span data-stu-id="600ca-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="600ca-109">(Priežiūros užklausos ciklo būsenų pavyzdžiai: **Sukurta**, **Aktyvi** ir **Baigta**.)</span><span class="sxs-lookup"><span data-stu-id="600ca-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="600ca-110">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Priežiūros užklausos** \> **Priežiūros užklausų tipai**.</span><span class="sxs-lookup"><span data-stu-id="600ca-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="600ca-111">Pasirinkite **Naujas**, kad sukurtumėte priežiūros užklausos tipą.</span><span class="sxs-lookup"><span data-stu-id="600ca-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="600ca-112">Lauke **Priežiūros užklausos tipas** įveskite priežiūros užklausos tipo ID.</span><span class="sxs-lookup"><span data-stu-id="600ca-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="600ca-113">Tada lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="600ca-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="600ca-114">„FastTab“ skirtuko **Bendra** lauke **Priežiūros užklausos ciklo modelis** pasirinkite priežiūros užklausos ciklo modelį.</span><span class="sxs-lookup"><span data-stu-id="600ca-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="600ca-115">Lauke **Darbo užsakymo tipas** pasirinkite darbo užsakymo tipą.</span><span class="sxs-lookup"><span data-stu-id="600ca-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="600ca-116">Konvertavus priežiūros užklausą į darbo užsakymą, darbo užsakymui automatiškai priskiriamas su priežiūros užklausos tipu susijęs darbo užsakymo tipas.</span><span class="sxs-lookup"><span data-stu-id="600ca-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="600ca-117">Paveikslėlyje pateiktas puslapio **Priežiūros užklausos tipai** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="600ca-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Priežiūros užklausos tipų puslapis](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]