---
title: "Konsolidavimo sąskaitų grupės ir papildomos konsolidavimo sąskaitos"
description: "Šioje temoje pateikiama informacija apie konsolidavimo sąskaitų grupes ir papildomas konsolidavimo sąskaitas bei paaiškinama, kaip jos naudojamos programoje „Microsoft Dynamics 365 for Finance and Operations“ (leidimas „Enterprise‟)."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: eb69b8def1d0a4fc296ccf44490af6c70591cb7b
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="d722f-103">Konsolidavimo sąskaitų grupės ir papildomos konsolidavimo sąskaitos</span><span class="sxs-lookup"><span data-stu-id="d722f-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d722f-104">Šioje temoje pateikiama informacija apie konsolidavimo sąskaitų grupes ir papildomas konsolidavimo sąskaitas bei paaiškinama, kaip jos naudojamos programoje „Microsoft Dynamics 365 for Finance and Operations“ (leidimas „Enterprise‟).</span><span class="sxs-lookup"><span data-stu-id="d722f-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="d722f-105">Konsolidacijos sąskaitų grupės</span><span class="sxs-lookup"><span data-stu-id="d722f-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="d722f-106">Konsolidavimo sąskaitų grupės suteikia galimybę kurti sąskaitų, kurias norite naudoti duomenims konsoliduoti, grupes.</span><span class="sxs-lookup"><span data-stu-id="d722f-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="d722f-107">Dažniausiai konsolidavimo sąskaitų grupė nurodo vyriausybės įgaliotą sąskaitų planą arba susieja sąskaitas su grupe, kurią nurodo įmonės būstinė.</span><span class="sxs-lookup"><span data-stu-id="d722f-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="d722f-108">Konsolidavimo sąskaitų grupes galite rasti modulio **Konsolidavimas** srityje **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="d722f-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="d722f-109">Įtraukdami naują grupę turite įvesti sąskaitų grupės unikalų identifikatorių ir pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="d722f-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="d722f-110">Papildomos konsolidacijos sąskaitos</span><span class="sxs-lookup"><span data-stu-id="d722f-110">Additional consolidation accounts</span></span>
<span data-ttu-id="d722f-111">Papildomos konsolidavimo sąskaitos suteikia galimybę sąskaitą iš esamo sąskaitų plano priskirti konsolidavimo sąskaitų grupei.</span><span class="sxs-lookup"><span data-stu-id="d722f-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="d722f-112">Tada galima nurodyti konsolidavimo sąskaitos vertę ir pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="d722f-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="d722f-113">Papildomas konsolidavimo sąskaitas galite rasti modulio **Konsolidavimas** srityje **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="d722f-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="d722f-114">Kurdami naują konsolidavimo sąskaitą turite nurodyti tolesnę informaciją.</span><span class="sxs-lookup"><span data-stu-id="d722f-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="d722f-115">**Pagrindinė sąskaita** – šis laukas yra peržvalga, kurioje rodomos visos pagrindinės sąskaitos, pagrįstos puslapyje pasirinktu sąskaitų planu.</span><span class="sxs-lookup"><span data-stu-id="d722f-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="d722f-116">Pasirinkus sąskaitą pavadinimas automatiškai įvedamas lauke **Pagrindinės sąskaitos pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="d722f-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="d722f-117">**Konsolidavimo sąskaitų grupė** – naudokite šį lauką norėdami nurodyti grupę, kuriai priskirti sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="d722f-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="d722f-118">Jei konsoliduojate dviem skirtingais būdais, tą pačią sąskaitą turite įtraukti į visas keturias konsolidavimo sąskaitų grupes.</span><span class="sxs-lookup"><span data-stu-id="d722f-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="d722f-119">**Konsolidavimo sąskaita** – įveskite konsoliduotos sąskaitos vertę.</span><span class="sxs-lookup"><span data-stu-id="d722f-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="d722f-120">Ši vertė neprivalo būti sąskaita iš sąskaitų plano.</span><span class="sxs-lookup"><span data-stu-id="d722f-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="d722f-121">Tai gali būti bet kokia jums reikalinga vertė.</span><span class="sxs-lookup"><span data-stu-id="d722f-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="d722f-122">**Konsolidavimo sąskaitos pavadinimas** – įveskite sąskaitos, kurią norite rodyti užklausose ir ataskaitose, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="d722f-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="d722f-123">**SAT lygis** – šis laukas naudojamas norint teikti sąskaitų išrašų ataskaitas Meksikos mokesčių inspekcijai.</span><span class="sxs-lookup"><span data-stu-id="d722f-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="d722f-124">Baigę kurti konsolidavimo sąskaitų grupes ir papildomas konsolidavimo sąskaitas, grupę galite pasirinkti vykdydami procesą Konsoliduoti tinkle.</span><span class="sxs-lookup"><span data-stu-id="d722f-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="d722f-125">Daugiau informacijos žr. [Konsolidavimo grupių ir papildomų konsolidavimo sąskaitų kūrimas](../general-ledger/tasks/create-consolidation-groups.md).</span><span class="sxs-lookup"><span data-stu-id="d722f-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 




