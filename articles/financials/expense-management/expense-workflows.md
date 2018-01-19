---
title: "Išlaidų darbo eigų nustatymas"
description: "Galite nustatyti darbo eigos procesą, naudojamą kelionių ir išlaidų dokumentams peržiūrėti bei tvirtinti."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: fb729a56919eb50cdff8318138986152bb65a083
ms.contentlocale: lt-lt
ms.lasthandoff: 01/19/2018

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="8c717-103">Išlaidų darbo eigų nustatymas</span><span class="sxs-lookup"><span data-stu-id="8c717-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="8c717-104"> Galite nustatyti darbo eigos procesą, naudojamą kelionių ir išlaidų dokumentams peržiūrėti bei tvirtinti.</span><span class="sxs-lookup"><span data-stu-id="8c717-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="8c717-105">Dokumentai, kurių darbo eigas galima apibrėžti – tai išlaidų ataskaitos, kelionių paraiškos ir avanso grynaisiais pinigais užklausos.</span><span class="sxs-lookup"><span data-stu-id="8c717-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="8c717-106">Darbo eiga rodo verslo procesą.</span><span class="sxs-lookup"><span data-stu-id="8c717-106">A workflow represents a business process.</span></span> <span data-ttu-id="8c717-107">Ji nustato dokumento kelią sistemoje ir parodo, kas turi atlikti užduotį arba patvirtinti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="8c717-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="8c717-108">Darbo eigos sistemos naudojimas jūsų organizacijoje duoda keleriopos naudos:</span><span class="sxs-lookup"><span data-stu-id="8c717-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="8c717-109">**Procesų nuoseklumas** — galite nustatyti konkrečių dokumentų, pvz., pirkimo paraiškų ir išlaidų ataskaitų, patvirtinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="8c717-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="8c717-110">Darbo eigos sistemos naudojimas padeda užtikrinti, kad dokumentai bus apdoroti ir patvirtinti nuosekliai ir veiksmingai.</span><span class="sxs-lookup"><span data-stu-id="8c717-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="8c717-111">Proceso matomumas — galite sekti konkretaus darbo eigos egzemplioriaus efektyvumo metriką.</span><span class="sxs-lookup"><span data-stu-id="8c717-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="8c717-112">Tai padeda nustatyti, ar reikia atlikti darbo eigos pokyčius, siekiant gerinti efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="8c717-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="8c717-113">Centralizuotas darbų sąrašas — vartotojai norėdami sužinoti jiems priskirtas darbo eigos užduotis ir patvirtinimus gali peržiūrėti centralizuotų darbų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="8c717-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="8c717-114">**Darbo eigų tipai, kuriuos galite sukurti**</span><span class="sxs-lookup"><span data-stu-id="8c717-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="8c717-115">Toliau pateiktoje lentelėje išvardyti darbo eigų tipai, kuriuos galite sukurti srityje **Išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="8c717-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="8c717-116">**Tipas**</span><span class="sxs-lookup"><span data-stu-id="8c717-116">**Type**</span></span>                           | <span data-ttu-id="8c717-117">**Naudokite šį tipą norėdami**</span><span class="sxs-lookup"><span data-stu-id="8c717-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="8c717-118">**Išlaidų ataskaita**</span><span class="sxs-lookup"><span data-stu-id="8c717-118">**Expense report**</span></span>                 | <span data-ttu-id="8c717-119">Kurti išlaidų ataskaitų tvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="8c717-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="8c717-120">**Automatinis išlaidų ataskaitos registravimas**</span><span class="sxs-lookup"><span data-stu-id="8c717-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="8c717-121">Kurti išlaidų ataskaitų automatinio registravimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="8c717-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="8c717-122">**Išlaidų eilutės elementas**</span><span class="sxs-lookup"><span data-stu-id="8c717-122">**Expense line item**</span></span>              | <span data-ttu-id="8c717-123">Kurti išlaidų ataskaitų eilučių elementų tvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="8c717-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="8c717-124">**Išlaidų eilutės prekės automatinis registravimas**</span><span class="sxs-lookup"><span data-stu-id="8c717-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="8c717-125">Kurti išlaidų ataskaitų eilučių elementų automatinio registravimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="8c717-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="8c717-126">**Kelionės paraiška**</span><span class="sxs-lookup"><span data-stu-id="8c717-126">**Travel requisition**</span></span>             | <span data-ttu-id="8c717-127">Kurti pirkimo paraiškų tvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="8c717-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="8c717-128">**Avanso grynaisiais pinigais prašymas**</span><span class="sxs-lookup"><span data-stu-id="8c717-128">**Cash advance request**</span></span>           | <span data-ttu-id="8c717-129">Kurti avanso grynaisiais pinigais užklausų tvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="8c717-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="8c717-130">**PVM susigrąžinimas**</span><span class="sxs-lookup"><span data-stu-id="8c717-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="8c717-131">Kurti pridėtinės vertės mokesčio (PVM) susigrąžinimo tvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="8c717-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

