---
title: Prieiga prie privačių adresų pagal saugos vaidmenį
description: Šiame straipsnyje aiškinama, kaip išspręsti problemą, kai klientas negali pasiekti privačių adresų.
author: andreabichsel
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8daee1b645836e96a4bf3057cb317d5409d4583a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803926"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="1465e-103">Prieiga prie asmeninių adresų pagal saugos vaidmenį</span><span class="sxs-lookup"><span data-stu-id="1465e-103">Access to private addresses by security role</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1465e-104">**Problema**</span><span class="sxs-lookup"><span data-stu-id="1465e-104">**Issue**</span></span>

<span data-ttu-id="1465e-105">Klientui sukūrus saugos vaidmens dublikatų ir prisijungus naujuoju vaidmeniu, nerodomi adresai, kurie buvo pažymėti kaip privatūs.</span><span class="sxs-lookup"><span data-stu-id="1465e-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="1465e-106">**Skiriamoji geba**</span><span class="sxs-lookup"><span data-stu-id="1465e-106">**Resolution**</span></span>

<span data-ttu-id="1465e-107">Norėdamas išspręsti šią problemą, klientas turi atlikti nurodytus besidubliuojančio saugos vaidmens veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1465e-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="1465e-108">Eikite į **Organizacijos administravimas \> Visuotinė adresų knygelė \> Visuotinės adresų knygelės parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1465e-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="1465e-109">Skirtuke **Privačios vietos sauga** naują saugos vaidmenį iš sąrašo **Galimi vaidmenys** perkelkite į sąrašą **Pasirinkti vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="1465e-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="1465e-110">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1465e-110">Select **Save**.</span></span>

![Visuotinės adresų knygelės parametrų puslapis](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]