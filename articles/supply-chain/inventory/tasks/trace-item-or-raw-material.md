---
title: "Prekės arba žaliavos sekimas"
description: "Ši procedūra parodo, kaip naudoti prekės sekimą ir identifikuoti, kur prekės arba žaliavos buvo naudojamos arba yra naudojamos."
author: pjacobse
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: d7eb282ddf9597385d6660a3fc0ef73f403ab898
ms.contentlocale: lt-lt
ms.lasthandoff: 09/12/2017

---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="0b64f-103">Prekės arba žaliavos sekimas</span><span class="sxs-lookup"><span data-stu-id="0b64f-103">Trace an item or raw material</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b64f-104">Ši procedūra parodo, kaip naudoti prekės sekimą ir identifikuoti, kur prekės arba žaliavos buvo naudojamos arba yra naudojamos.</span><span class="sxs-lookup"><span data-stu-id="0b64f-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="0b64f-105">Naudodami šią procedūrą, galite nustatyti prekę, atsekti jos šaltinį, tada perkelti ją į galutinio produkto gamybą ir pardavimą.</span><span class="sxs-lookup"><span data-stu-id="0b64f-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="0b64f-106">Procesą galima naudoti norint ištirti paveiktus klientus, paveiktus pardavimo užsakymus ir kt.</span><span class="sxs-lookup"><span data-stu-id="0b64f-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="0b64f-107">Šioje procedūroje naudojami demonstracinių duomenų įmonės USP2.</span><span class="sxs-lookup"><span data-stu-id="0b64f-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="0b64f-108">Sekti prekę atgal, naudojant žinomą paketo numerį</span><span class="sxs-lookup"><span data-stu-id="0b64f-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="0b64f-109">Pasirinkite Atsargų valdymas > Užklausos ir ataskaitos > Sekimo dimensijos > Prekės sekimas.</span><span class="sxs-lookup"><span data-stu-id="0b64f-109">Go to Inventory management > Inquiries and reports > Tracking dimensions > Item tracing.</span></span>
2. <span data-ttu-id="0b64f-110">Lauke Prekės numeris pasirinkite P9100.</span><span class="sxs-lookup"><span data-stu-id="0b64f-110">In the Item number field, select P9100.</span></span>
3. <span data-ttu-id="0b64f-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0b64f-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0b64f-112">Lauke Į priekį arba atgal pasirinkite 'Atgal'.</span><span class="sxs-lookup"><span data-stu-id="0b64f-112">In the Forward or backward field, select 'Backward'.</span></span>
5. <span data-ttu-id="0b64f-113">Lauke Paketo numeris pasirinkite as-12-344-01.</span><span class="sxs-lookup"><span data-stu-id="0b64f-113">In the Batch number field, select as-12-344-01.</span></span>
6. <span data-ttu-id="0b64f-114">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0b64f-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="0b64f-115">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0b64f-115">Click OK.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="0b64f-116">Identifikuoti prekę, sekti ją į priekį ir atlikti analizę</span><span class="sxs-lookup"><span data-stu-id="0b64f-116">Identify an item, trace it forward, and make an analysis</span></span>
    * <span data-ttu-id="0b64f-117">Medžio aukščiausias mazgas nurodo pasirinktos prekės ir paketo turimų atsargų kiekį.</span><span class="sxs-lookup"><span data-stu-id="0b64f-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="0b64f-118">Norėdami rasti prekę, kuriai turėtų būti vykdomas sekimas į priekį, turite išplėsti medžio mazgus.</span><span class="sxs-lookup"><span data-stu-id="0b64f-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="0b64f-119">Medyje išplėskite toliau aprašytus mazgus ir pasirinkite paskutinį mazgą.</span><span class="sxs-lookup"><span data-stu-id="0b64f-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    * <span data-ttu-id="0b64f-120">Išplėskite: „P9100 / 1 / 10 / as-12-344-01 ● 2 statinės ● 7,00 gal \P9100 ● Paimta ● Pardavimo užsakymas 000072 ● 2015-12-22  ● -1 statinė ● -4,00 gal ● Vieta=1, Sandėlis=10, Paketo numeris=as-12-344-01 \P9100 ● Gamyba B-000050 ● 2015-12-09● 7 statinės ● 27,00 gal ● Vieta=1,Sandėlis=10,Paketo numeris=as-12-344-01 ● Sudėtiniai produktai: P9101‟ ir pasirinkite tą mazgą.</span><span class="sxs-lookup"><span data-stu-id="0b64f-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="0b64f-121">Medyje išplėskite toliau aprašytą mazgą ir tą mazgą pasirinkite.</span><span class="sxs-lookup"><span data-stu-id="0b64f-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    * <span data-ttu-id="0b64f-122">Pradėdami nuo mazgo, kurį ką tik pasirinkote, išplėskite „M9103 ● Gamybos linija B-000050 ● 2015-12-09  ● -160,00 svar. ● Dydis=70, Spalva=Gerai, Vieta=1, Sandėlis=10, Paketo numeris=App01‟ ir pasirinkite tą mazgą.</span><span class="sxs-lookup"><span data-stu-id="0b64f-122">Starting from the node that you’ve just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="0b64f-123">Spustelėkite Sekti nuo mazgo.</span><span class="sxs-lookup"><span data-stu-id="0b64f-123">Click Trace from node.</span></span>
4. <span data-ttu-id="0b64f-124">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="0b64f-124">Click Forward.</span></span>
5. <span data-ttu-id="0b64f-125">Veiksmų srityje spustelėkite Sekimas.</span><span class="sxs-lookup"><span data-stu-id="0b64f-125">On the Action Pane, click Tracing.</span></span>
    * <span data-ttu-id="0b64f-126">Yra kelios sekimo parinktys, pateikiančios informacijos apie klientus, kuriems turėjo įtakos jūsų sekama prekė ir išsiųstus bei neišsiųstus su ta preke susijusius pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="0b64f-126">There are several tracing options which provide information about the customers impacted by the item that you’re tracing, and the sales orders related to the item which have and haven’t been shipped.</span></span>   
6. <span data-ttu-id="0b64f-127">Spustelėkite Klientai.</span><span class="sxs-lookup"><span data-stu-id="0b64f-127">Click Customers.</span></span>
7. <span data-ttu-id="0b64f-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0b64f-128">Close the page.</span></span>
8. <span data-ttu-id="0b64f-129">Veiksmų srityje spustelėkite Sekimas.</span><span class="sxs-lookup"><span data-stu-id="0b64f-129">On the Action Pane, click Tracing.</span></span>
9. <span data-ttu-id="0b64f-130">Spustelėkite Išsiųsti pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="0b64f-130">Click Shipped sales orders.</span></span>
10. <span data-ttu-id="0b64f-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0b64f-131">Close the page.</span></span>

