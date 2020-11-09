---
title: Kurti važtaraštį
description: Šioje temoje aprašoma, kaip kurti važtaraštį, kai naudojami sandėlio valdymo procesai.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd014f5804681936920b47e999709f153def11bc
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016683"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="373f3-103">Kurti važtaraštį</span><span class="sxs-lookup"><span data-stu-id="373f3-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="373f3-104">Šioje temoje aprašoma, kaip kurti važtaraštį, kai naudojami sandėlio valdymo procesai.</span><span class="sxs-lookup"><span data-stu-id="373f3-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="373f3-105">Važtaraštis yra teisinis dokumentas, kurį pasirašo prekes siunčianti įmonė ir vežėjas.</span><span class="sxs-lookup"><span data-stu-id="373f3-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="373f3-106">Dokumentas pridedamas prie išsiųstų prekių ir jis naudojamas kaip siuntos gavimo kvitas, kai prekės pristatomos į paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="373f3-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="373f3-107">Jei naudojate sandėlio valdymą, važtaraštį sukurti galite dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="373f3-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="373f3-108">Kurkite ataskaitą neautomatiniu būdu, naudodami puslapį **Važtaraštis**.</span><span class="sxs-lookup"><span data-stu-id="373f3-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="373f3-109">Generuokite ataskaitą iš **Krovinio planavimo darbo sritis**.</span><span class="sxs-lookup"><span data-stu-id="373f3-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="373f3-110">Jei važtaraštį generuojate iš **Krovinio planavimo darbo sritis** , krovinio būsena turi būti **Išsiųsta.**</span><span class="sxs-lookup"><span data-stu-id="373f3-110">If you generate the bill of lading from the **Load planning workbench** , the load status must be **Shipped.**</span></span> <span data-ttu-id="373f3-111">Jei krovinyje yra daugiau nei viena siunta, sukuriamas kiekvienos siuntos važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="373f3-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="373f3-112">Sukūrus važtaraštį, jį galima keisti puslapyje **Važtaraštis**.</span><span class="sxs-lookup"><span data-stu-id="373f3-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="373f3-113">Pagrindinis važtaraštis</span><span class="sxs-lookup"><span data-stu-id="373f3-113">Master bill of lading</span></span>
<span data-ttu-id="373f3-114">Jei krovinyje yra daugiau nei viena siunta, galite generuoti bendrąjį važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="373f3-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="373f3-115">Jo maketas ir informacija yra tokie pat kaip važtaraščio, bet juose pateikiamas apibendrintas visų siuntų turinys.</span><span class="sxs-lookup"><span data-stu-id="373f3-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="373f3-116">Kai puslapyje **Transportavimo valdymo parametrai** parinktis **Kurti bendrąjį važtaraštį, kai krovinyje yra daugiau nei viena siunta** nustatyta į **Taip** , bendrasis važtaraštis sugeneruojamas automatiškai, jei važtaraštį kuriate iš **Krovinio planavimo darbo sritis** ir jei yra daugiau nei viena siunta.</span><span class="sxs-lookup"><span data-stu-id="373f3-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench** , and there's more than one shipment.</span></span> <span data-ttu-id="373f3-117">Taip pat galite gauti važtaraščių sąrašą, spustelėdami **Susijusi informacija** &gt; **Važtaraštis**.</span><span class="sxs-lookup"><span data-stu-id="373f3-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="373f3-118">Jei važtaraščius kuriate neautomatiniu būdu, bendrąjį važtaraštį galite kurti puslapyje **Važtaraštis**.</span><span class="sxs-lookup"><span data-stu-id="373f3-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>



