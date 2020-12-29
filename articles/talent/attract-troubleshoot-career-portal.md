---
title: Programos „Attract“ vartotojai negali kandidatuoti į darbus iš karjeros portalo
description: Šiame skyriuje paaiškinama, kaip šalinti problemą, kada „Attract“ naudotojas negali kreiptis dėl darbų karjeros portale.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461961"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="24a47-103">Programos „Attract“ vartotojai negali kandidatuoti į darbus iš karjeros portalo</span><span class="sxs-lookup"><span data-stu-id="24a47-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="24a47-104">Išdavimas</span><span class="sxs-lookup"><span data-stu-id="24a47-104">Issue</span></span>

<span data-ttu-id="24a47-105">„Attract“ naudotojai negali kreiptis dėl darbų karjeros portale.</span><span class="sxs-lookup"><span data-stu-id="24a47-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="24a47-106">Jiems bandant kreiptis dėl darbo, kuris buvo sukurtas „Dynamics 365 Talent: Attract“, naršyklė nuolatos įkelia puslapį ir neužbaigia veiksmo.</span><span class="sxs-lookup"><span data-stu-id="24a47-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="24a47-107">Priežastis</span><span class="sxs-lookup"><span data-stu-id="24a47-107">Cause</span></span>

<span data-ttu-id="24a47-108">Ši problema atsitinka kai „Talent Relationship Team“ neturi „Talent“ naudotojo vaidmens.</span><span class="sxs-lookup"><span data-stu-id="24a47-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="24a47-109">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="24a47-109">Resolution</span></span>

<span data-ttu-id="24a47-110">Priskikrite „Talent“ naudotojo vaidmenį „Talent Relationship Team“.</span><span class="sxs-lookup"><span data-stu-id="24a47-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="24a47-111">Prisijunkite prie [„Power Platform“ administravimo centro](https://admin.powerplatform.microsoft.com) su bet kuriais iš toliau įvardytų administratoriaus prisijungimo duomenų:</span><span class="sxs-lookup"><span data-stu-id="24a47-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="24a47-112">„Dynamics 365“ administratorius</span><span class="sxs-lookup"><span data-stu-id="24a47-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="24a47-113">Globalus administratorius</span><span class="sxs-lookup"><span data-stu-id="24a47-113">Global admin</span></span>
   - <span data-ttu-id="24a47-114">„Power Platform“ administratorius</span><span class="sxs-lookup"><span data-stu-id="24a47-114">Power Platform admin</span></span>

2. <span data-ttu-id="24a47-115">Naršymo juostoje pasirinkite **Aplinkos** ir tuomet pasirinkite aplinką, kurioje norite priskirite „Talent“ naudotojo vaidmenį „Talent Relationship Team“.</span><span class="sxs-lookup"><span data-stu-id="24a47-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![Pasirinkite aplinką](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="24a47-117">**Aplinkų** juostoje pasirinkite **Aplinkos URL** ir prisijunkite prie aplinkos administravimo portalo (pavyzdžiui, https:<orgname>.crm.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="24a47-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="24a47-118">Pasirinkite **Nustatymai**, rinkitės **Sistema** ir tada rinkitės **Sauga**.</span><span class="sxs-lookup"><span data-stu-id="24a47-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![Eikite į saugą](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="24a47-120">Rinkitės **Komandos**.</span><span class="sxs-lookup"><span data-stu-id="24a47-120">Select **Teams**.</span></span>

   ![Rinkitės Komandos](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="24a47-122">Ieškokite **„Talent Relationship Team“** paieškos laukelyje ir tada pasirinkite komandą iš paieškos rezultatų.</span><span class="sxs-lookup"><span data-stu-id="24a47-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="24a47-123">Pasirinkite **TVARKYTI VAIDMENIS** juostoje.</span><span class="sxs-lookup"><span data-stu-id="24a47-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="24a47-124">Teksto laukelyje **Tvarkyti komandos vaidmenis** pasirinkite **„Talent“ naudotojas** iš esamo vaidmenų sąrašo ir rinkitės **GERAI** tam, kad taikytumėte vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="24a47-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![Taikykite vaidmenį](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="24a47-126">Išbandykite savo pokyčius:</span><span class="sxs-lookup"><span data-stu-id="24a47-126">Test your changes:</span></span>

   1. <span data-ttu-id="24a47-127">Prisijunkite prie karjeros portalo per naują naršyklės langą.</span><span class="sxs-lookup"><span data-stu-id="24a47-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="24a47-128">Taikykite darbą iš karjeros portalo.</span><span class="sxs-lookup"><span data-stu-id="24a47-128">Apply for the job from the career portal.</span></span> 