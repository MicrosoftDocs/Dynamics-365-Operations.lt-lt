---
title: Vartotojas gali pasiekti „Core HR“, bet ne programas „Onboard“ ar „Attract“
description: Šioje temoje aiškinama, kaip išspręsti problemą, kai vartotojas gali pasiekti „Microsoft“ „Dynamics 365 Talent – Core HR“, bet negali pasiekti programų „Attract“ arba „Onboard“.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a86936d756d8375761ce50c9d9bf33dc638dfad
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772924"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a><span data-ttu-id="55696-103">Vartotojas gali pasiekti „Core HR“, bet ne programas „Onboard“ ar „Attract“</span><span class="sxs-lookup"><span data-stu-id="55696-103">User can access Core HR but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="55696-104">**Aplinkos informacija**</span><span class="sxs-lookup"><span data-stu-id="55696-104">**Environment details**</span></span>

- <span data-ttu-id="55696-105">„Microsoft Dynamics Lifecycle Services“ (LCS) diegimą atliko vartotojas A.</span><span class="sxs-lookup"><span data-stu-id="55696-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="55696-106">Vartotojas A įtraukė vartotoją B kaip „Microsoft“ „Dynamics 365 Talent: Core HR Core HR“ vartotoją.</span><span class="sxs-lookup"><span data-stu-id="55696-106">User A added user B as a user to Microsoft Dynamics 365 Talent: Core HR.</span></span>

<span data-ttu-id="55696-107">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="55696-107">**Issue**</span></span>

<span data-ttu-id="55696-108">Vartotojas B gali pasiekti „Core HR“, bet negali pasiekti programų „Talent: Attract“ arba „Talent: Onboard“.</span><span class="sxs-lookup"><span data-stu-id="55696-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="55696-109">Vietoj to, vartotojui bandant apsilankyti **„Experience“ programose** jis nukreipiamas į bandomosios versijos aplinką.</span><span class="sxs-lookup"><span data-stu-id="55696-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="55696-110">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="55696-110">**Solution**</span></span>

<span data-ttu-id="55696-111">B vartotojas turi būti priskirtas prie teisių, suteikiančių galimybę peržiūrėti „Microsoft Power Apps“ aplinką, kurią vartotojas A sukūrė parengimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="55696-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="55696-112">Daugiau informacijos ieškokite dalyje [„Talent“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="55696-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="55696-113">**Ilgalaikis sprendimas**</span><span class="sxs-lookup"><span data-stu-id="55696-113">**Long-term solution**</span></span>

<span data-ttu-id="55696-114">„Microsoft“ ketina automatiškai priskirti atitinkamas teises „Onboard“ arba „Attract“, kai vartotojas įtraukiamas į „Core HR“.</span><span class="sxs-lookup"><span data-stu-id="55696-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
