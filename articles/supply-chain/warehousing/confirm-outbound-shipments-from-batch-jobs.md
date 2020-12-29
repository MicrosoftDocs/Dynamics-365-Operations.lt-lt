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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 41dbfb90b7b19c964e725ee0a4c769402414fb17
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433358"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="df765-103">Patvirtinti siunčiamas siuntas naudojant paketines užduotis</span><span class="sxs-lookup"><span data-stu-id="df765-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df765-104">Ši tema aprašo, kaip nustatyti pakuotės užduotį, kuri automatiškai tvirtina išorės perdavimo užsakymo siuntimus paruoštiems siųsti kroviniams.</span><span class="sxs-lookup"><span data-stu-id="df765-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="df765-105">Čia aprašyta pakuotės užduotis taikoma tik persiunčiamiems užsakymo siuntimams, o ne prekybos užsakymams.</span><span class="sxs-lookup"><span data-stu-id="df765-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="df765-106">Įjunkite išorės siuntimų patvirtinimą pakuotės užduočių funkcijai</span><span class="sxs-lookup"><span data-stu-id="df765-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="df765-107">Norėdami pasinaudoti šia funkcija, ją turite įjungti savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="df765-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="df765-108">Administratoriai gali naudoti [Funkcijas valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) puslapį tam, kad patikrintų funkcijos būseną ir įjungtų ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="df765-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="df765-109">Ši funkcija yra tokia:</span><span class="sxs-lookup"><span data-stu-id="df765-109">The feature is listed as:</span></span>

- <span data-ttu-id="df765-110">**Modulis** - *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="df765-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="df765-111">**Funkcijos pavadinimas** - *Išorės siuntimų patvirtinimas pakuotės užduočių funkcijai*</span><span class="sxs-lookup"><span data-stu-id="df765-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="df765-112">Apdoroti siunčiamas siuntas</span><span class="sxs-lookup"><span data-stu-id="df765-112">Process outbound shipments</span></span>

<span data-ttu-id="df765-113">Pakuotės darbo vykdančio išorės siuntimo patvirtinimą paruoštiems siųsti kroviniams nustatymui:</span><span class="sxs-lookup"><span data-stu-id="df765-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="df765-114">Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Išorės siuntimų apdorojimas**.</span><span class="sxs-lookup"><span data-stu-id="df765-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="df765-115">**Siutimo patvirtinimo** langas atsidaro.</span><span class="sxs-lookup"><span data-stu-id="df765-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="df765-116">„FastTab„ **Įtrauktini įrašai** pasirinkite **Filtruoti**.</span><span class="sxs-lookup"><span data-stu-id="df765-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="df765-117">Užklausos redagavimo langas atsidaro.</span><span class="sxs-lookup"><span data-stu-id="df765-117">The query editor dialog box opens.</span></span> <span data-ttu-id="df765-118">**Diapazonas** skirtuke, įtraukite eilutę su šiomis vertėmis:</span><span class="sxs-lookup"><span data-stu-id="df765-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="df765-119">**Lentelė** - *Kroviniai*</span><span class="sxs-lookup"><span data-stu-id="df765-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="df765-120">**Pristatymų lentelė** - *Kroviniai*</span><span class="sxs-lookup"><span data-stu-id="df765-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="df765-121">**Laukelis** - *Krovinio būsena*</span><span class="sxs-lookup"><span data-stu-id="df765-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="df765-122">**Kriterijai** - *Pakrauta*</span><span class="sxs-lookup"><span data-stu-id="df765-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="df765-123">Pasirinkite **Gerai** grįžimui į **Siuntimo patvirtinimo** teksto langelį.</span><span class="sxs-lookup"><span data-stu-id="df765-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="df765-124">**Vykdyti fone** „FastTab“, nustatykite **Paketo apdorojimą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="df765-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="df765-125">**Vykdyti fone** „FastTab“, pasirinkite **Pakartojimas**.</span><span class="sxs-lookup"><span data-stu-id="df765-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="df765-126">**Nustatyti pakartojimą** langas atsidaro.</span><span class="sxs-lookup"><span data-stu-id="df765-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="df765-127">Vykdykite tvarkaraštį, kaip būtina jūsų organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="df765-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="df765-128">Pasirinkite **Gerai** grįžimui į **Siuntimo patvirtinimo** teksto langelį.</span><span class="sxs-lookup"><span data-stu-id="df765-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="df765-129">Pasirinkite **Gerai** **Siuntimo patvirtinimo** teksto langelyje ir įtraukite pakuotės užduotį į pakuotės eilę.</span><span class="sxs-lookup"><span data-stu-id="df765-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="df765-130">Norėdami gauti daugiau informacijos, žr. [Paketo apdorojimo apžvalgą](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="df765-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>
