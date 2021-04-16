---
title: Patvirtinti siunčiamas siuntas naudojant paketines užduotis
description: Ši tema aprašo, kaip nustatyti pakuotės užduotį, kuri automatiškai tvirtina išorės perdavimo užsakymo siuntimus paruoštiems siųsti kroviniams.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 69e61e1c04dd72efbe1d2f028c078100e07176f6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838447"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="63778-103">Patvirtinti siunčiamas siuntas naudojant paketines užduotis</span><span class="sxs-lookup"><span data-stu-id="63778-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63778-104">Ši tema aprašo, kaip nustatyti pakuotės užduotį, kuri automatiškai tvirtina išorės perdavimo užsakymo siuntimus paruoštiems siųsti kroviniams.</span><span class="sxs-lookup"><span data-stu-id="63778-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="63778-105">Čia aprašyta pakuotės užduotis taikoma tik persiunčiamiems užsakymo siuntimams, o ne prekybos užsakymams.</span><span class="sxs-lookup"><span data-stu-id="63778-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="63778-106">Įjunkite išorės siuntimų patvirtinimą pakuotės užduočių funkcijai</span><span class="sxs-lookup"><span data-stu-id="63778-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="63778-107">Norėdami pasinaudoti šia funkcija, ją turite įjungti savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="63778-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="63778-108">Administratoriai gali naudoti [Funkcijas valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) puslapį tam, kad patikrintų funkcijos būseną ir įjungtų ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="63778-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="63778-109">Ši funkcija yra tokia:</span><span class="sxs-lookup"><span data-stu-id="63778-109">The feature is listed as:</span></span>

- <span data-ttu-id="63778-110">**Modulis** - *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="63778-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="63778-111">**Funkcijos pavadinimas** - *Išorės siuntimų patvirtinimas pakuotės užduočių funkcijai*</span><span class="sxs-lookup"><span data-stu-id="63778-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="63778-112">Apdoroti siunčiamas siuntas</span><span class="sxs-lookup"><span data-stu-id="63778-112">Process outbound shipments</span></span>

<span data-ttu-id="63778-113">Pakuotės darbo vykdančio išorės siuntimo patvirtinimą paruoštiems siųsti kroviniams nustatymui:</span><span class="sxs-lookup"><span data-stu-id="63778-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="63778-114">Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Išorės siuntimų apdorojimas**.</span><span class="sxs-lookup"><span data-stu-id="63778-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="63778-115">**Siutimo patvirtinimo** langas atsidaro.</span><span class="sxs-lookup"><span data-stu-id="63778-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="63778-116">„FastTab„ **Įtrauktini įrašai** pasirinkite **Filtruoti**.</span><span class="sxs-lookup"><span data-stu-id="63778-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="63778-117">Užklausos redagavimo langas atsidaro.</span><span class="sxs-lookup"><span data-stu-id="63778-117">The query editor dialog box opens.</span></span> <span data-ttu-id="63778-118">**Diapazonas** skirtuke, įtraukite eilutę su šiomis vertėmis:</span><span class="sxs-lookup"><span data-stu-id="63778-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="63778-119">**Lentelė** - *Kroviniai*</span><span class="sxs-lookup"><span data-stu-id="63778-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="63778-120">**Pristatymų lentelė** - *Kroviniai*</span><span class="sxs-lookup"><span data-stu-id="63778-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="63778-121">**Laukelis** - *Krovinio būsena*</span><span class="sxs-lookup"><span data-stu-id="63778-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="63778-122">**Kriterijai** - *Pakrauta*</span><span class="sxs-lookup"><span data-stu-id="63778-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="63778-123">Pasirinkite **Gerai** grįžimui į **Siuntimo patvirtinimo** teksto langelį.</span><span class="sxs-lookup"><span data-stu-id="63778-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="63778-124">**Vykdyti fone** „FastTab“, nustatykite **Paketo apdorojimą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="63778-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="63778-125">**Vykdyti fone** „FastTab“, pasirinkite **Pakartojimas**.</span><span class="sxs-lookup"><span data-stu-id="63778-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="63778-126">**Nustatyti pakartojimą** langas atsidaro.</span><span class="sxs-lookup"><span data-stu-id="63778-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="63778-127">Vykdykite tvarkaraštį, kaip būtina jūsų organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="63778-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="63778-128">Pasirinkite **Gerai** grįžimui į **Siuntimo patvirtinimo** teksto langelį.</span><span class="sxs-lookup"><span data-stu-id="63778-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="63778-129">Pasirinkite **Gerai** **Siuntimo patvirtinimo** teksto langelyje ir įtraukite pakuotės užduotį į pakuotės eilę.</span><span class="sxs-lookup"><span data-stu-id="63778-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="63778-130">Norėdami gauti daugiau informacijos, žr. [Paketo apdorojimo apžvalgą](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="63778-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]