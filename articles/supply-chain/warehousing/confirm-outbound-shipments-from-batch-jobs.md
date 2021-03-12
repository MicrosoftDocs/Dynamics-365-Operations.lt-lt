---
title: Patvirtinti siunčiamas siuntas naudojant paketines užduotis
description: Ši tema aprašo, kaip nustatyti pakuotės užduotį, kuri automatiškai tvirtina išorės perdavimo užsakymo siuntimus paruoštiems siųsti kroviniams.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 48257967ce360b1d4969124411d5976b807bf9e4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996306"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="68b0f-103">Patvirtinti siunčiamas siuntas naudojant paketines užduotis</span><span class="sxs-lookup"><span data-stu-id="68b0f-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68b0f-104">Ši tema aprašo, kaip nustatyti pakuotės užduotį, kuri automatiškai tvirtina išorės perdavimo užsakymo siuntimus paruoštiems siųsti kroviniams.</span><span class="sxs-lookup"><span data-stu-id="68b0f-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="68b0f-105">Čia aprašyta pakuotės užduotis taikoma tik persiunčiamiems užsakymo siuntimams, o ne prekybos užsakymams.</span><span class="sxs-lookup"><span data-stu-id="68b0f-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="68b0f-106">Įjunkite išorės siuntimų patvirtinimą pakuotės užduočių funkcijai</span><span class="sxs-lookup"><span data-stu-id="68b0f-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="68b0f-107">Norėdami pasinaudoti šia funkcija, ją turite įjungti savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="68b0f-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="68b0f-108">Administratoriai gali naudoti [Funkcijas valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) puslapį tam, kad patikrintų funkcijos būseną ir įjungtų ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="68b0f-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="68b0f-109">Ši funkcija yra tokia:</span><span class="sxs-lookup"><span data-stu-id="68b0f-109">The feature is listed as:</span></span>

- <span data-ttu-id="68b0f-110">**Modulis** - *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="68b0f-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="68b0f-111">**Funkcijos pavadinimas** - *Išorės siuntimų patvirtinimas pakuotės užduočių funkcijai*</span><span class="sxs-lookup"><span data-stu-id="68b0f-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="68b0f-112">Apdoroti siunčiamas siuntas</span><span class="sxs-lookup"><span data-stu-id="68b0f-112">Process outbound shipments</span></span>

<span data-ttu-id="68b0f-113">Pakuotės darbo vykdančio išorės siuntimo patvirtinimą paruoštiems siųsti kroviniams nustatymui:</span><span class="sxs-lookup"><span data-stu-id="68b0f-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="68b0f-114">Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Išorės siuntimų apdorojimas**.</span><span class="sxs-lookup"><span data-stu-id="68b0f-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="68b0f-115">**Siutimo patvirtinimo** langas atsidaro.</span><span class="sxs-lookup"><span data-stu-id="68b0f-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="68b0f-116">„FastTab„ **Įtrauktini įrašai** pasirinkite **Filtruoti**.</span><span class="sxs-lookup"><span data-stu-id="68b0f-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="68b0f-117">Užklausos redagavimo langas atsidaro.</span><span class="sxs-lookup"><span data-stu-id="68b0f-117">The query editor dialog box opens.</span></span> <span data-ttu-id="68b0f-118">**Diapazonas** skirtuke, įtraukite eilutę su šiomis vertėmis:</span><span class="sxs-lookup"><span data-stu-id="68b0f-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="68b0f-119">**Lentelė** - *Kroviniai*</span><span class="sxs-lookup"><span data-stu-id="68b0f-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="68b0f-120">**Pristatymų lentelė** - *Kroviniai*</span><span class="sxs-lookup"><span data-stu-id="68b0f-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="68b0f-121">**Laukelis** - *Krovinio būsena*</span><span class="sxs-lookup"><span data-stu-id="68b0f-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="68b0f-122">**Kriterijai** - *Pakrauta*</span><span class="sxs-lookup"><span data-stu-id="68b0f-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="68b0f-123">Pasirinkite **Gerai** grįžimui į **Siuntimo patvirtinimo** teksto langelį.</span><span class="sxs-lookup"><span data-stu-id="68b0f-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="68b0f-124">**Vykdyti fone** „FastTab“, nustatykite **Paketo apdorojimą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="68b0f-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="68b0f-125">**Vykdyti fone** „FastTab“, pasirinkite **Pakartojimas**.</span><span class="sxs-lookup"><span data-stu-id="68b0f-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="68b0f-126">**Nustatyti pakartojimą** langas atsidaro.</span><span class="sxs-lookup"><span data-stu-id="68b0f-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="68b0f-127">Vykdykite tvarkaraštį, kaip būtina jūsų organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="68b0f-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="68b0f-128">Pasirinkite **Gerai** grįžimui į **Siuntimo patvirtinimo** teksto langelį.</span><span class="sxs-lookup"><span data-stu-id="68b0f-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="68b0f-129">Pasirinkite **Gerai** **Siuntimo patvirtinimo** teksto langelyje ir įtraukite pakuotės užduotį į pakuotės eilę.</span><span class="sxs-lookup"><span data-stu-id="68b0f-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="68b0f-130">Norėdami gauti daugiau informacijos, žr. [Paketo apdorojimo apžvalgą](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="68b0f-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>
