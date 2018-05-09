---
title: "Transportavimo mokesčių derinimo valdymas"
description: "Šiame straipsnyje aprašomas transportavimo mokesčių derinimo procesas."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c52d92b08c2832541fbebe2bf14c942bb79b1540
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="c6d91-103">Transportavimo mokesčių derinimo valdymas</span><span class="sxs-lookup"><span data-stu-id="c6d91-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6d91-104">Šiame straipsnyje aprašomas transportavimo mokesčių derinimo procesas.</span><span class="sxs-lookup"><span data-stu-id="c6d91-104">This article describes the freight reconciliation process.</span></span>

<span data-ttu-id="c6d91-105">Transportavimo mokesčius galima suderinti neautomatiniu arba automatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="c6d91-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="c6d91-106">Norėdami transportavimo mokesčius derinti automatiškai, turite nustatyti pagrindinį auditą ir jame nurodyti kriterijus, pagal kuriuos nustatoma, kurios transportavimo sąskaitos bus derinamos automatiškai.</span><span class="sxs-lookup"><span data-stu-id="c6d91-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="c6d91-107">Transportavimo mokesčių derinimo procesas</span><span class="sxs-lookup"><span data-stu-id="c6d91-107">The freight reconciliation process</span></span>
<span data-ttu-id="c6d91-108">Transportavimo tarifus skaičiuoja tarifų mechanizmas, kuris yra susijęs su atitinkamu siuntimo vežėju.</span><span class="sxs-lookup"><span data-stu-id="c6d91-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="c6d91-109">Jeigu krovinys yra patvirtintas, sugeneruojama transportavimo sąskaita ir į ją įvedami transportavimo tarifai.</span><span class="sxs-lookup"><span data-stu-id="c6d91-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="c6d91-110">Transportavimo tarifai kaip papildomos išlaidos yra paskiriami atitinkamam šaltinio dokumentui (pirkimo užsakymo, pardavimo užsakymo ir (arba) perdavimo užsakymo), atsižvelgiant į sąranką, naudojamą įprastame atsiskaitymo procese.</span><span class="sxs-lookup"><span data-stu-id="c6d91-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="c6d91-111">Transportavimo mokesčių derinimo procesas (taip pat vadinamas gretinimo procesu) gali prasidėti iškart, kai iš vežėjo gaunama transportavimo SF.</span><span class="sxs-lookup"><span data-stu-id="c6d91-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="c6d91-112">SF galima gauti elektroniniu būdu arba išspausdintą ant popieriaus.</span><span class="sxs-lookup"><span data-stu-id="c6d91-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="c6d91-113">Jei SF gauta išspausdinta ant popieriaus, galite generuoti elektroninę SF, transportavimo sąskaitą naudodami kaip šabloną.</span><span class="sxs-lookup"><span data-stu-id="c6d91-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="c6d91-114">[![Transportavimo mokesčių derinimo procesas](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="c6d91-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="c6d91-115">Neautomatinis derinimas</span><span class="sxs-lookup"><span data-stu-id="c6d91-115">Manual reconciliation</span></span>
<span data-ttu-id="c6d91-116">Jei norite transportavimo mokesčius derinti neautomatiniu būdu, kiekvieną krovinio, kuriam išrašoma SF, SF eilutę turite suderinti su transportavimo sąskaitos eilute arba eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="c6d91-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="c6d91-117">Šis derinimas atliekamas puslapyje **Transportavimo sąskaitos ir SF gretinimas**.</span><span class="sxs-lookup"><span data-stu-id="c6d91-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="c6d91-118">Jei SF eilutės suma nesutampa su transportavimo sąskaitos suma, turite pasirinkti skirtumo suderinimo priežastį.</span><span class="sxs-lookup"><span data-stu-id="c6d91-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="c6d91-119">Jei yra kelios suderinimo priežastys, joms galite padalinti nesuderintą sumą.</span><span class="sxs-lookup"><span data-stu-id="c6d91-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="c6d91-120">Suderinimo priežastis lemia, kaip skirtumo sumos registruojamos DK.</span><span class="sxs-lookup"><span data-stu-id="c6d91-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="c6d91-121">Kai atskaitomas visos SF sumos suderinimas, jis pateikiamas patvirtinti, o tada žurnalas užregistruojamas.</span><span class="sxs-lookup"><span data-stu-id="c6d91-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="c6d91-122">Toliau pateiktoje iliustracijoje parodyta, kaip generuoti transportavimo sąskaitą faktūrą ir derinti transportavimo mokesčius sprendime „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="c6d91-122">The following illustration shows how to generate a freight invoice and do freight reconciliation in Microsoft Dynamics 365 for Finance and Operations.</span></span> 
<span data-ttu-id="c6d91-123">[![Transportavimo mokesčių derinimo užduotys programoje „Dynamics AX“](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="c6d91-123">[![Freight reconcilation tasks in Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="c6d91-124">Automatinis derinimas</span><span class="sxs-lookup"><span data-stu-id="c6d91-124">Automatic reconciliation</span></span>
<span data-ttu-id="c6d91-125">Norėdami derinti automatiškai, turite nurodyti derinimo grafiką ir SF bei siuntimo vežėjus, kuriuos reikia naudoti.</span><span class="sxs-lookup"><span data-stu-id="c6d91-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="c6d91-126">SF eilutės ir transportavimo sąskaitos yra derinamos pagal pagrindinio audito sąranką ir transportavimo sąskaitos tipą.</span><span class="sxs-lookup"><span data-stu-id="c6d91-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="c6d91-127">Įvykdę automatinį suderinimą, turite sutvarkyti visas SF, kurių sistemai nepavyko suderinti.</span><span class="sxs-lookup"><span data-stu-id="c6d91-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="c6d91-128">Tada turite šias SF apdoroti neautomatiniu būdu, kad galėtumėte užregistruoti visas mokėjimo SF.</span><span class="sxs-lookup"><span data-stu-id="c6d91-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>




