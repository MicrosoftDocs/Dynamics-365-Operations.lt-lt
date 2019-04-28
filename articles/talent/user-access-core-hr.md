---
title: Vartotojas gali pasiekti „Core HR“, bet ne programas „Onboard“ ar „Attract“
description: Šioje temoje aiškinama, kaip išspręsti problemą, kai vartotojas gali pasiekti „Microsoft Dynamics 365 for Talent Core HR“, bet negali pasiekti programų „Attract“ arba „Onboard“.
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
ms.openlocfilehash: ece6a81c54ef1421284fc79ab82ed3e31a972255
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/19/2019
ms.locfileid: "855661"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="0ff7b-103">Vartotojas gali pasiekti „Core HR“, bet ne programas „Onboard“ ar „Attract“</span><span class="sxs-lookup"><span data-stu-id="0ff7b-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0ff7b-104">**Aplinkos informacija**</span><span class="sxs-lookup"><span data-stu-id="0ff7b-104">**Environment details**</span></span>

- <span data-ttu-id="0ff7b-105">„Microsoft Dynamics Lifecycle Services“ (LCS) diegimą atliko vartotojas A.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="0ff7b-106">Vartotojas A įtraukė vartotojo B kaip „Microsoft Dynamics 365 for Talent Core HR“ vartotoją.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="0ff7b-107">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="0ff7b-107">**Issue**</span></span>

<span data-ttu-id="0ff7b-108">Vartotojas B gali pasiekti „Core HR“, bet negali pasiekti programų „Talent: Attract“ arba „Talent: Onboard“.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="0ff7b-109">Vietoj to, vartotojui bandant apsilankyti **„Experience“ programose** jis nukreipiamas į bandomosios versijos aplinką.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="0ff7b-110">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="0ff7b-110">**Solution**</span></span>

<span data-ttu-id="0ff7b-111">B vartotojas turi būti priskirtas prie teisių, suteikiančių galimybę peržiūrėti „Microsoft PowerApps“ aplinką, kurią vartotojas A sukūrė parengimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="0ff7b-112">Daugiau informacijos ieškokite dalyje [„Talent“ parengimas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="0ff7b-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="0ff7b-113">**Ilgalaikis sprendimas**</span><span class="sxs-lookup"><span data-stu-id="0ff7b-113">**Long-term solution**</span></span>

<span data-ttu-id="0ff7b-114">„Microsoft“ ketina automatiškai priskirti atitinkamas teises „Onboard“ arba „Attract“, kai vartotojas įtraukiamas į „Core HR“.</span><span class="sxs-lookup"><span data-stu-id="0ff7b-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
