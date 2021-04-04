---
title: Pašalintos arba nebenaudojamos „Lifecycle Services” (LCS) funkcijos
description: Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama šalinti iš „Microsoft Dynamics“ „Lifecycle Services“ (LCS).
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b49a6f26b4c2fa895fe0e49f716ce423c3c0057
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559090"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="7bcde-103">Pašalintos arba nebenaudojamos „Lifecycle Services” (LCS) funkcijos</span><span class="sxs-lookup"><span data-stu-id="7bcde-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7bcde-104">Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba nebėra naudojamos „Microsoft Dynamics“ „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="7bcde-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="7bcde-105">*Pašalinta* funkcija nebėra įtraukta į paslaugą.</span><span class="sxs-lookup"><span data-stu-id="7bcde-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="7bcde-106">*Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta ateityje išleidus naujinį.</span><span class="sxs-lookup"><span data-stu-id="7bcde-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="7bcde-107">Šis sąrašas pateikiamas, kad galėtumėte atsižvelgti į pašalintas ir nebenaudojamas funkcijas, planuodami savo darbą.</span><span class="sxs-lookup"><span data-stu-id="7bcde-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="7bcde-108">2019 m. spalio mėn. pranešimai</span><span class="sxs-lookup"><span data-stu-id="7bcde-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="7bcde-109">Struktūrinės schemos verslo procesų modeliavimo įrankyje</span><span class="sxs-lookup"><span data-stu-id="7bcde-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="7bcde-110"><strong>Nebenaudojimo / pašalinimo priežastis</strong></span><span class="sxs-lookup"><span data-stu-id="7bcde-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="7bcde-111">Verslo procesų modeliavimo įrankio (BPM) struktūrinių schemų komponentas tampa nebenaudojamas, nes dėl senstelėjusio dizaino sumažėjo naudojimas.</span><span class="sxs-lookup"><span data-stu-id="7bcde-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7bcde-112"><strong>Pakeitė kita funkcija?</strong></span><span class="sxs-lookup"><span data-stu-id="7bcde-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="7bcde-113">Ne</span><span class="sxs-lookup"><span data-stu-id="7bcde-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7bcde-114"><strong>Paveiktos sritys</strong></span><span class="sxs-lookup"><span data-stu-id="7bcde-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="7bcde-115">Verslo procesų modeliavimo įrankis</span><span class="sxs-lookup"><span data-stu-id="7bcde-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7bcde-116"><strong>Būsena</strong></span><span class="sxs-lookup"><span data-stu-id="7bcde-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="7bcde-117">Nebenaudojama: tikimasi, kad BPM struktūrinės schemos diagramų komponentas bus pašalintas 2020 m.</span><span class="sxs-lookup"><span data-stu-id="7bcde-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="7bcde-118">Toliau nurodytos funkcijos bus nepasiekiamos.</span><span class="sxs-lookup"><span data-stu-id="7bcde-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="7bcde-119">Visas struktūrines schemas bus galima tik skaityti. Jų redaguoti bus negalima.</span><span class="sxs-lookup"><span data-stu-id="7bcde-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="7bcde-120">Formų ypatybės, susietos su struktūrinės schemos veiklomis, bus taip pat nepasiekiamos.</span><span class="sxs-lookup"><span data-stu-id="7bcde-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="7bcde-121">Šios struktūrinės schemos apima ir numatytąsias struktūrines schemas, kurios yra automatiškai generuojamos, ir pritaikytas struktūrines schemas, modifikuojamas pagal minėtas numatytąsias struktūrines schemas.</span><span class="sxs-lookup"><span data-stu-id="7bcde-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="7bcde-122">Proceso veiksmus galite tik skaityti ir negalima jų redaguoti.</span><span class="sxs-lookup"><span data-stu-id="7bcde-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="7bcde-123">Senstelėjusi tinkamumo / trūkumų analizės funkcija nebus pasiekiama.</span><span class="sxs-lookup"><span data-stu-id="7bcde-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="7bcde-124">Todėl trūkumų sąrašas nebus automatiškai sukuriamas ir jo nebus galima eksportuoti.</span><span class="sxs-lookup"><span data-stu-id="7bcde-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="7bcde-125"><strong>Pastaba.</strong> Ši funkcija anksčiau tapo nebenaudojama ir ją pakeitė „Microsoft Azure DevOps“ integracijos.</span><span class="sxs-lookup"><span data-stu-id="7bcde-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="7bcde-126">Struktūrinių schemų versijų retrospektyva nebus pasiekiama.</span><span class="sxs-lookup"><span data-stu-id="7bcde-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]