---
title: Vidinės įmonės išlaidos
description: Darbininkas, kurį yra įdarbinęs vienas organizacijos juridinis subjektas, gali dirbti kitam tos pačios organizacijos juridiniam subjektui. Šioje situacijoje, naudodami vidinės įmonės išlaidų funkciją, darbininko išlaidas galite priskirti tam juridiniam subjektui, kuriam darbas buvo atliekamas.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390889"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="14e77-104">Vidinės įmonės išlaidos</span><span class="sxs-lookup"><span data-stu-id="14e77-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14e77-105">Darbininkas, kurį yra įdarbinęs vienas organizacijos juridinis subjektas, gali dirbti kitam tos pačios organizacijos juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="14e77-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="14e77-106">Šioje situacijoje, naudodami vidinės įmonės išlaidų funkciją, darbininko išlaidas galite priskirti tam juridiniam subjektui, kuriam darbas buvo atliekamas.</span><span class="sxs-lookup"><span data-stu-id="14e77-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="14e77-107">Juridinis subjektas, kuris įdarbina darbuotoją, vadinamas skolinančiuoju juridiniu subjektu.</span><span class="sxs-lookup"><span data-stu-id="14e77-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="14e77-108">Juridinis subjektas, kuriam priskiriamos darbininko išlaidos, vadinamas besiskolinančiuoju juridiniu subjektu.</span><span class="sxs-lookup"><span data-stu-id="14e77-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="14e77-109">Kad darbininkas galėtų kurti ir teikti išlaidas už darbą, atliekamą kitam juridiniam subjektui, skolinančiojo juridinio subjekto dalies puslapyje **Išlaidų valdymo parametrai** pasirinkite parinktį **Leisti vidinės įmonės išlaidų eilutes**.</span><span class="sxs-lookup"><span data-stu-id="14e77-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="14e77-110">Vidinės įmonės išlaidų mokesčių registravimas</span><span class="sxs-lookup"><span data-stu-id="14e77-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14e77-111">Jei savo išlaidų ataskaitoje norite naudoti mokesčių grupes, kurios yra susietos su skolinančiuoju (šaltinio) juridiniu subjektu, o ne su besiskolinančiuoju (paskirties) juridiniu subjektu, turėsite tai sukonfigūruoti Didžiosios knygos PVM sąrankoje.</span><span class="sxs-lookup"><span data-stu-id="14e77-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="14e77-112">Kai Didžiosios knygos parametro **Vidinės įmonės mokesčių registravimo juridinis subjektas** reikšmė nustatyta kaip **Šaltinis**, o parametro **Taikyti PVM mokesčio apmokestinimo taisykles** reikšmė nustatyta kaip **Ne**, bus naudojamas skolinančiam juridiniam subjektui taikomas mokesčių derinys.</span><span class="sxs-lookup"><span data-stu-id="14e77-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="14e77-113">Kai tas pats parametras nustatytas kaip **Paskirtis**, bus naudojamas besiskolinančiam juridiniam subjektui taikomas mokesčių derinys.</span><span class="sxs-lookup"><span data-stu-id="14e77-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="14e77-114">Jei tai yra JAV juridiniai subjektai, kai parametras nustatytas kaip **Šaltinis**, laukas **Gautinas PVM** taip pat turi būti sukonfigūruotas naujajame puslapyje **DK registravimo grupės**.</span><span class="sxs-lookup"><span data-stu-id="14e77-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="14e77-115">Apskaitos mechanizmas naudos šio lauko informaciją su mokesčiu susijusiam apskaitos įrašui.</span><span class="sxs-lookup"><span data-stu-id="14e77-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="14e77-116">Toks pat veiksmas atliekamas su išlaidų eilutėmis, užregistruotomis su projektu arba be jo.</span><span class="sxs-lookup"><span data-stu-id="14e77-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
