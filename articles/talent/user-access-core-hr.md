---
title: Vartotojas gali pasiekti „Human Resources“, bet ne „Onboard“ ar „Attract“
description: Šioje temoje aiškinama, kaip išspręsti problemą, kai vartotojas gali pasiekti „Microsoft Dynamics 365 Talent – „Human Resources”, bet negali pasiekti programų „Attract“ arba „Onboard“.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006315"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="1ed03-103">Vartotojas gali pasiekti „Human Resources“, bet ne „Onboard“ ar „Attract“</span><span class="sxs-lookup"><span data-stu-id="1ed03-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1ed03-104">**Aplinkos informacija**</span><span class="sxs-lookup"><span data-stu-id="1ed03-104">**Environment details**</span></span>

- <span data-ttu-id="1ed03-105">„Microsoft Dynamics Lifecycle Services“ (LCS) diegimą atliko vartotojas A.</span><span class="sxs-lookup"><span data-stu-id="1ed03-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="1ed03-106">Vartotojas A įtraukė vartotoją B kaip „Microsoft“ „Dynamics 365 Human Resources Core HR“ vartotoją.</span><span class="sxs-lookup"><span data-stu-id="1ed03-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="1ed03-107">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="1ed03-107">**Issue**</span></span>

<span data-ttu-id="1ed03-108">Vartotojas B gali pasiekti „Human Resources“, bet negali pasiekti programų „Talent: Attract“ arba „Talent: Onboard“.</span><span class="sxs-lookup"><span data-stu-id="1ed03-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="1ed03-109">Vietoj to, vartotojui bandant apsilankyti **„Experience“ programose** jis nukreipiamas į bandomosios versijos aplinką.</span><span class="sxs-lookup"><span data-stu-id="1ed03-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="1ed03-110">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="1ed03-110">**Solution**</span></span>

<span data-ttu-id="1ed03-111">B vartotojas turi būti priskirtas prie teisių, suteikiančių galimybę peržiūrėti „Microsoft Power Apps“ aplinką, kurią vartotojas A sukūrė parengimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="1ed03-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="1ed03-112">Daugiau informacijos ieškokite dalyje [„Talent“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="1ed03-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="1ed03-113">**Ilgalaikis sprendimas**</span><span class="sxs-lookup"><span data-stu-id="1ed03-113">**Long-term solution**</span></span>

<span data-ttu-id="1ed03-114">„Microsoft“ ketina automatiškai priskirti atitinkamas teises „Onboard“ arba „Attract“, kai vartotojas įtraukiamas į „Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="1ed03-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
