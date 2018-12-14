---
title: "Prieiga prie asmeninių adresų pagal saugos vaidmenį"
description: "Šioje temoje aiškinama, kaip išspręsti problemą, kai klientas negali pasiekti privačių adresų."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: c1c1c3ce1233408e73d177f9e04f1137f3171a49
ms.contentlocale: lt-lt
ms.lasthandoff: 12/04/2018

---

# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="3c446-103">Prieiga prie asmeninių adresų pagal saugos vaidmenį</span><span class="sxs-lookup"><span data-stu-id="3c446-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3c446-104">**Problema**</span><span class="sxs-lookup"><span data-stu-id="3c446-104">**Issue**</span></span>

<span data-ttu-id="3c446-105">Klientui sukūrus saugos vaidmens dublikatų ir prisijungus naujuoju vaidmeniu, nerodomi adresai, kurie buvo pažymėti kaip privatūs.</span><span class="sxs-lookup"><span data-stu-id="3c446-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="3c446-106">**Skiriamoji geba**</span><span class="sxs-lookup"><span data-stu-id="3c446-106">**Resolution**</span></span>

<span data-ttu-id="3c446-107">Norėdamas išspręsti šią problemą, klientas turi atlikti nurodytus besidubliuojančio saugos vaidmens veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3c446-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="3c446-108">Eikite į **Organizacijos administravimas \> Visuotinė adresų knygelė \> Visuotinės adresų knygelės parametrai**.</span><span class="sxs-lookup"><span data-stu-id="3c446-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="3c446-109">Skirtuke **Privačios vietos sauga** naują saugos vaidmenį iš sąrašo **Galimi vaidmenys** perkelkite į sąrašą **Pasirinkti vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="3c446-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="3c446-110">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3c446-110">Select **Save**.</span></span>

![Visuotinės adresų knygelės parametrų puslapis](media/GAD-parameters.png)

