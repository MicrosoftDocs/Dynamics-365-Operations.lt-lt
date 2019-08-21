---
title: Išlaidų darbo eigų nustatymas
description: Galite nustatyti darbo eigos procesą, naudojamą kelionių ir išlaidų dokumentams peržiūrėti bei tvirtinti.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86cadf7277fbb7e08dad4b5dc2a46e1c6ce5a888
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840966"
---
# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="7baa9-103">Išlaidų darbo eigų nustatymas</span><span class="sxs-lookup"><span data-stu-id="7baa9-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7baa9-104"> Galite nustatyti darbo eigos procesą, naudojamą kelionių ir išlaidų dokumentams peržiūrėti bei tvirtinti.</span><span class="sxs-lookup"><span data-stu-id="7baa9-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="7baa9-105">Dokumentai, kurių darbo eigas galima apibrėžti – tai išlaidų ataskaitos, kelionių paraiškos ir avanso grynaisiais pinigais užklausos.</span><span class="sxs-lookup"><span data-stu-id="7baa9-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="7baa9-106">Darbo eiga rodo verslo procesą.</span><span class="sxs-lookup"><span data-stu-id="7baa9-106">A workflow represents a business process.</span></span> <span data-ttu-id="7baa9-107">Ji nustato dokumento kelią sistemoje ir parodo, kas turi atlikti užduotį arba patvirtinti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="7baa9-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="7baa9-108">Darbo eigos sistemos naudojimas jūsų organizacijoje duoda keleriopos naudos:</span><span class="sxs-lookup"><span data-stu-id="7baa9-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="7baa9-109">**Procesų nuoseklumas** — galite nustatyti konkrečių dokumentų, pvz., pirkimo paraiškų ir išlaidų ataskaitų, patvirtinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="7baa9-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="7baa9-110">Darbo eigos sistemos naudojimas padeda užtikrinti, kad dokumentai bus apdoroti ir patvirtinti nuosekliai ir veiksmingai.</span><span class="sxs-lookup"><span data-stu-id="7baa9-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="7baa9-111">Proceso matomumas — galite sekti konkretaus darbo eigos egzemplioriaus efektyvumo metriką.</span><span class="sxs-lookup"><span data-stu-id="7baa9-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="7baa9-112">Tai padeda nustatyti, ar reikia atlikti darbo eigos pokyčius, siekiant gerinti efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="7baa9-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="7baa9-113">Centralizuotas darbų sąrašas — vartotojai norėdami sužinoti jiems priskirtas darbo eigos užduotis ir patvirtinimus gali peržiūrėti centralizuotų darbų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="7baa9-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="7baa9-114">**Darbo eigų tipai, kuriuos galite sukurti**</span><span class="sxs-lookup"><span data-stu-id="7baa9-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="7baa9-115">Toliau pateiktoje lentelėje išvardyti darbo eigų tipai, kuriuos galite sukurti srityje **Išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="7baa9-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="7baa9-116"><strong>Tipas</strong></span><span class="sxs-lookup"><span data-stu-id="7baa9-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="7baa9-117"><strong>Naudokite šį tipą norėdami</strong></span><span class="sxs-lookup"><span data-stu-id="7baa9-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="7baa9-118"><strong>Išlaidų ataskaita</strong></span><span class="sxs-lookup"><span data-stu-id="7baa9-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="7baa9-119">Kurti išlaidų ataskaitų tvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="7baa9-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="7baa9-120"><strong>Automatinis išlaidų ataskaitos registravimas</strong></span><span class="sxs-lookup"><span data-stu-id="7baa9-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="7baa9-121">Kurti išlaidų ataskaitų automatinio registravimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="7baa9-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="7baa9-122"><strong>Išlaidų eilutės elementas</strong></span><span class="sxs-lookup"><span data-stu-id="7baa9-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="7baa9-123">Kurti išlaidų ataskaitų eilučių elementų tvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="7baa9-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="7baa9-124"><strong>Išlaidų eilutės prekės automatinis registravimas</strong></span><span class="sxs-lookup"><span data-stu-id="7baa9-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="7baa9-125">Kurti išlaidų ataskaitų eilučių elementų automatinio registravimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="7baa9-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="7baa9-126"><strong>Kelionės paraiška</strong></span><span class="sxs-lookup"><span data-stu-id="7baa9-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="7baa9-127">Kurti pirkimo paraiškų tvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="7baa9-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="7baa9-128"><strong>Avanso grynaisiais pinigais prašymas</strong></span><span class="sxs-lookup"><span data-stu-id="7baa9-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="7baa9-129">Kurti avanso grynaisiais pinigais užklausų tvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="7baa9-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="7baa9-130"><strong>PVM susigrąžinimas</strong></span><span class="sxs-lookup"><span data-stu-id="7baa9-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="7baa9-131">Kurti pridėtinės vertės mokesčio (PVM) susigrąžinimo tvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="7baa9-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

