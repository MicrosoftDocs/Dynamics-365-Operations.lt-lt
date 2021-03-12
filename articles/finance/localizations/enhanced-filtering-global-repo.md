---
title: RCS patobulintas filtravimas RCS / bendrojoje saugykloje
description: Šioje temoje aprašomos išplėstos RCS visuotinės saugyklos filtravimo galimybės, dėl kurių galima įtraukti papildomus filtrus.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a67a4345271cbeffc100fc1d9077cc866846a4d4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005847"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="a55b1-103">RCS patobulintos filtravimo parinktys, ieškant konfigūracijų RCS / bendrojoje saugykloje</span><span class="sxs-lookup"><span data-stu-id="a55b1-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a55b1-104">Šioje temoje aprašomos patobulintos „Regulatory Configuration Service“ (RCS) bendrosios saugyklos galimybės, dėl kurių galima filtruoti, kai taikomi toliau nurodyti kriterijai.</span><span class="sxs-lookup"><span data-stu-id="a55b1-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="a55b1-105">**Šalis / regionas** – pagal ISO šalių kodus</span><span class="sxs-lookup"><span data-stu-id="a55b1-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="a55b1-106">**Žymų** tipai, skirti toliau nurodytiems dalykams.</span><span class="sxs-lookup"><span data-stu-id="a55b1-106">**Tags** types for:</span></span>
  - <span data-ttu-id="a55b1-107">Funkcinė sritis</span><span class="sxs-lookup"><span data-stu-id="a55b1-107">Functional area</span></span>
  - <span data-ttu-id="a55b1-108">Funkcijos sritis</span><span class="sxs-lookup"><span data-stu-id="a55b1-108">Feature area</span></span>
  - <span data-ttu-id="a55b1-109">Rinka</span><span class="sxs-lookup"><span data-stu-id="a55b1-109">Industry</span></span> 
  - <span data-ttu-id="a55b1-110">Verslo dokumentas</span><span class="sxs-lookup"><span data-stu-id="a55b1-110">Business document</span></span> 

<span data-ttu-id="a55b1-111">Norėdami lengviau rasti konkrečias arba susijusias konfigūracijas, galite taikyti filtrus atskirai arba kaip grupę.</span><span class="sxs-lookup"><span data-stu-id="a55b1-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="a55b1-112">Pavyzdžiui, norėdami rasti vieno tipo konfigūruojamus verslo dokumentus, susijusius su tiekėjo SF, galite taikyti filtrą **Verslo dokumento tipas** to tipo dokumentui ieškoti.</span><span class="sxs-lookup"><span data-stu-id="a55b1-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="a55b1-113">[![Filtravimo sekcija bendrajai saugyklai](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="a55b1-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="a55b1-114">Galite patikslinti iešką pasirinkdami dokumento tipą, pvz., tiekėjo SF, ir spustelėti **Taikyti filtrą**.</span><span class="sxs-lookup"><span data-stu-id="a55b1-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="a55b1-115">Toliau pateikiamame pavyzdyje parodomi rezultatai, gauti filtruojant **Verslo dokumento tipas**, įtraukus dokumento tipą.</span><span class="sxs-lookup"><span data-stu-id="a55b1-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="a55b1-116">[![Verslo dokumento tipo filtravimas ir importavimas](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="a55b1-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="a55b1-117">Filtruotus rezultatus galima importuoti į vartotojo RCS saugyklą arba „Dynamics 365 Finance” aplinką atskirai arba kaip rinkinį.</span><span class="sxs-lookup"><span data-stu-id="a55b1-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="a55b1-118">Norėdami tai atlikti, pasirinkite konfigūracijų grupę ir spustelėkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="a55b1-118">To do this, select the group of configurations, and click **Import**.</span></span>
