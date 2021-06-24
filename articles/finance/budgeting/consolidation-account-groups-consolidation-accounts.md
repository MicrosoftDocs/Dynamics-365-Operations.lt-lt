---
title: Konsolidavimo sąskaitų grupės ir papildomos konsolidavimo sąskaitos
description: Šioje temoje pateikiama informacija apie konsolidavimo sąskaitų grupes ir papildomas konsolidavimo sąskaitas bei paaiškinama, kaip jos naudojamos programoje „Microsoft Dynamics 365 Finance“.
author: aprilolson
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 245b61c8cb85ab1282a921ac99b9ac7c2efbadc5
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189426"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="f0662-103">Konsolidavimo sąskaitų grupės ir papildomos konsolidavimo sąskaitos</span><span class="sxs-lookup"><span data-stu-id="f0662-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0662-104">Šioje temoje pateikiama informacija apie konsolidavimo sąskaitų grupes ir papildomas konsolidavimo sąskaitas bei paaiškinama, kaip jos naudojamos programoje „Microsoft Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="f0662-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 Finance.</span></span>

## <a name="consolidation-account-groups"></a><span data-ttu-id="f0662-105">Konsolidacijos sąskaitų grupės</span><span class="sxs-lookup"><span data-stu-id="f0662-105">Consolidation account groups</span></span>

<span data-ttu-id="f0662-106">Konsolidavimo sąskaitų grupės suteikia galimybę kurti sąskaitų, kurias norite naudoti duomenims konsoliduoti, grupes.</span><span class="sxs-lookup"><span data-stu-id="f0662-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="f0662-107">Dažniausiai konsolidavimo sąskaitų grupė nurodo vyriausybės įgaliotą sąskaitų planą arba susieja sąskaitas su grupe, kurią nurodo įmonės būstinė.</span><span class="sxs-lookup"><span data-stu-id="f0662-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="f0662-108">Konsolidavimo sąskaitų grupes galite rasti modulio **Konsolidavimas** srityje **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="f0662-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="f0662-109">Įtraukdami naują grupę turite įvesti sąskaitų grupės unikalų identifikatorių ir pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f0662-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="f0662-110">Papildomos konsolidacijos sąskaitos</span><span class="sxs-lookup"><span data-stu-id="f0662-110">Additional consolidation accounts</span></span>
<span data-ttu-id="f0662-111">Papildomos konsolidavimo sąskaitos suteikia galimybę sąskaitą iš esamo sąskaitų plano priskirti konsolidavimo sąskaitų grupei.</span><span class="sxs-lookup"><span data-stu-id="f0662-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="f0662-112">Tada galima nurodyti konsolidavimo sąskaitos vertę ir pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f0662-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="f0662-113">Papildomas konsolidavimo sąskaitas galite rasti modulio **Konsolidavimas** srityje **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="f0662-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="f0662-114">Kurdami naują konsolidavimo sąskaitą turite nurodyti tolesnę informaciją.</span><span class="sxs-lookup"><span data-stu-id="f0662-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="f0662-115">**Pagrindinė sąskaita** – šis laukas yra peržvalga, kurioje rodomos visos pagrindinės sąskaitos, pagrįstos puslapyje pasirinktu sąskaitų planu.</span><span class="sxs-lookup"><span data-stu-id="f0662-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="f0662-116">Pasirinkus sąskaitą pavadinimas automatiškai įvedamas lauke **Pagrindinės sąskaitos pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="f0662-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="f0662-117">**Konsolidavimo sąskaitų grupė** – naudokite šį lauką norėdami nurodyti grupę, kuriai priskirti sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="f0662-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="f0662-118">Jei konsoliduojate dviem skirtingais būdais, tą pačią sąskaitą turite įtraukti į visas keturias konsolidavimo sąskaitų grupes.</span><span class="sxs-lookup"><span data-stu-id="f0662-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="f0662-119">**Konsolidavimo sąskaita** – įveskite konsoliduotos sąskaitos vertę.</span><span class="sxs-lookup"><span data-stu-id="f0662-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="f0662-120">Ši vertė neprivalo būti sąskaita iš sąskaitų plano.</span><span class="sxs-lookup"><span data-stu-id="f0662-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="f0662-121">Tai gali būti bet kokia jums reikalinga vertė.</span><span class="sxs-lookup"><span data-stu-id="f0662-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="f0662-122">**Konsolidavimo sąskaitos pavadinimas** – įveskite sąskaitos, kurią norite rodyti užklausose ir ataskaitose, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f0662-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="f0662-123">**SAT lygis** – šis laukas naudojamas norint teikti sąskaitų išrašų ataskaitas Meksikos mokesčių inspekcijai.</span><span class="sxs-lookup"><span data-stu-id="f0662-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="f0662-124">Baigę kurti konsolidavimo sąskaitų grupes ir papildomas konsolidavimo sąskaitas, grupę galite pasirinkti vykdydami procesą Konsoliduoti tinkle.</span><span class="sxs-lookup"><span data-stu-id="f0662-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="f0662-125">Daugiau informacijos žr. [Konsolidavimo grupių ir papildomų konsolidavimo sąskaitų kūrimas](../general-ledger/tasks/create-consolidation-groups.md).</span><span class="sxs-lookup"><span data-stu-id="f0662-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]