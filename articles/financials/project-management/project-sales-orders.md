---
title: Projekto pardavimo užsakymai
description: Šioje temoje paaiškinama, kaip kurti pojektinius pardavimo užsakymus dirbant su laiko ir medžiagų projektais.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/12/2019
ms.locfileid: "976684"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="0cb22-103">Laiko ir medžiagų projektų pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="0cb22-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="0cb22-104">Šioje temoje aprašoma, kaip sukurti projekto pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="0cb22-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="0cb22-105">Pardavimo užsakymus galima sukurti tik tiems projektams, kurių tipas **laikas ir medžiagos**.</span><span class="sxs-lookup"><span data-stu-id="0cb22-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="0cb22-106">Jei laiko ir medžiagų projekto sutartyje nurodyti keli lėšų skyrimo šaltiniai, puslapyje **Projektų valdymo ir apskaitos parametrai** būtina įjungti parametrą **Leisti projektų su keliais lėšų skyrimo šaltiniais pardavimo užsakymus**.</span><span class="sxs-lookup"><span data-stu-id="0cb22-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="0cb22-107">Projektų pardavimo užsakymai su keliais lėšų skyrimo šaltiniais palaikomi naudojant programos versiją 10.0.2 ir naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="0cb22-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="0cb22-108">2020 m. balandžio mėn. leidime parametras, skirtas įjungti projektų pardavimo užsakymų su keliais lėšų skyrimo šaltiniais palaikymą, bus panaikintas, taigi vėliau išleistose versijose funkcija bus visada įjungta.</span><span class="sxs-lookup"><span data-stu-id="0cb22-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="0cb22-109">Projektinius pardavimo užsakymus galite kurti dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="0cb22-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="0cb22-110">Eikite į patį projektą.</span><span class="sxs-lookup"><span data-stu-id="0cb22-110">Go to the project itself.</span></span> <span data-ttu-id="0cb22-111">Veiksmų srityje pasirinkite **Valdyti > Prekių užduotys > Pardavimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="0cb22-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="0cb22-112">Projekto informacijoje nurodomas numatytasis projekto pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="0cb22-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="0cb22-113">Jei projekto sutartyje nurodytas daugiau nei vienas lėšų skyrimo šaltinis, norėdami nustatyti pardavimo užsakymo klientą, turėsite pasirinkti lėšų skyrimo šaltinį.</span><span class="sxs-lookup"><span data-stu-id="0cb22-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="0cb22-114">Jei yra tik vienas projekto lėšų skyrimo šaltinis, klientas nustatomas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="0cb22-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="0cb22-115">Eikite į sąrašo puslapį **Visi pardavimo užsakymai** ir sukurkite naują pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="0cb22-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="0cb22-116">Turite pasirinkti projektą, kuriam kuriamas pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="0cb22-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="0cb22-117">Pasirinkus projektą, klientas nustatomas pagal lėšų skyrimo šaltinį arba, jei projekto sutartyje nurodyti keli lėšų skyrimo šaltiniai, turėsite pasirinkti lėšų skyrimo šaltinį.</span><span class="sxs-lookup"><span data-stu-id="0cb22-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

