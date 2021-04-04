---
title: Nustatyti aptarnavimo užsakymų etapus
description: Nustatykite aptarnavimo užsakymų etapus.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9774d5f4e97d3f768366ba552e5928929bacf508
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470934"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="1c088-103">Nustatyti aptarnavimo užsakymų etapus</span><span class="sxs-lookup"><span data-stu-id="1c088-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="1c088-104">Eikite į **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo užsakymai** \> **Aptarnavimo etapai**.</span><span class="sxs-lookup"><span data-stu-id="1c088-104">Go to **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="1c088-105">Pasirinkite **Naujas** naujo įrašo sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="1c088-105">Select **New** to create a new record.</span></span>

3.  <span data-ttu-id="1c088-106">Lauke **Aptarnavimo etapas** ir **Aprašas** nurodykite aptarnavimo etapo ID ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="1c088-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="1c088-107">Pasirinkite atitinkamus etapo parametrus.</span><span class="sxs-lookup"><span data-stu-id="1c088-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="1c088-108">Pasirinkite esamo etapo pirminį etapą arba lauką **Pirminis** palikite tuščią, jei etapas yra pirminis etapo sąrankos etapas.</span><span class="sxs-lookup"><span data-stu-id="1c088-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1c088-109">Įrašius etapą lauko <STRONG>Pirminis</STRONG> keisti nebegalima.</span><span class="sxs-lookup"><span data-stu-id="1c088-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="1c088-110">Todėl galite panaikinti įrašą ir sukurti jį dar kartą, lauke <STRONG>Pirminis</STRONG> naudodami kitą parinktį.</span><span class="sxs-lookup"><span data-stu-id="1c088-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="1c088-111">Taip pat galite sukurti tik vieną etapą, kurio laukas <STRONG>Pirminis</STRONG> tuščias.</span><span class="sxs-lookup"><span data-stu-id="1c088-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="1c088-112">Tai reiškia, kad leidžiamas tik vienas etapas.</span><span class="sxs-lookup"><span data-stu-id="1c088-112">That is, only one initial stage is permitted.</span></span></P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]