---
title: Kūrimo apžvalga
description: Šiame kūrėjo vadove pateikiama API ir pasirinktinių laukų rekomendacija. Jame taip pat pateikiama informacija apie integravimą su kitomis programomis.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8e390592b000c8f6006aa489fd3823c4f15cb2cb
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467800"
---
# <a name="development-overview"></a><span data-ttu-id="cf809-104">Kūrimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="cf809-104">Development overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="cf809-105">Šiame kūrėjo vadove pateikiama API ir pasirinktinių laukų rekomendacija.</span><span class="sxs-lookup"><span data-stu-id="cf809-105">This Developer Guide provides an API and custom fields reference.</span></span> <span data-ttu-id="cf809-106">Jame taip pat pateikiama informacija apie integravimą su kitomis programomis.</span><span class="sxs-lookup"><span data-stu-id="cf809-106">It also provides information on integrating with other apps.</span></span>

- [<span data-ttu-id="cf809-107">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="cf809-107">Overview</span></span>](hr-developer-overview.md)

- [<span data-ttu-id="cf809-108">Išplėtimas su „Power Apps“ ir „Power Automate“</span><span class="sxs-lookup"><span data-stu-id="cf809-108">Extend with Power Apps and Power Automate</span></span>](hr-developer-power-apps.md)

- [<span data-ttu-id="cf809-109">„Human Resources“ objektai programoje „Dataverse“</span><span class="sxs-lookup"><span data-stu-id="cf809-109">Human Resources entities in Dataverse</span></span>](hr-developer-entities.md)

- [<span data-ttu-id="cf809-110">Pasirinktiniai laukai</span><span class="sxs-lookup"><span data-stu-id="cf809-110">Custom fields</span></span>](hr-developer-custom-fields.md)

- <span data-ttu-id="cf809-111">Duomenų integravimo sąranka</span><span class="sxs-lookup"><span data-stu-id="cf809-111">Set up data integration</span></span>
  - [<span data-ttu-id="cf809-112">Duomenų integravimo technologijos pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="cf809-112">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)
  - [<span data-ttu-id="cf809-113">„Dataverse“ integravimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cf809-113">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)
  - [<span data-ttu-id="cf809-114">Integravimo su „Finance“ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cf809-114">Configure integration with Finance</span></span>](hr-admin-integration-finance.md)
  - [<span data-ttu-id="cf809-115">Integravimo su „Dayforce“ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cf809-115">Configure integration with Dayforce</span></span>](hr-admin-integration-dayforce.md)
  - [<span data-ttu-id="cf809-116">Pasikartojančių duomenų eksportavimo programos kūrimas</span><span class="sxs-lookup"><span data-stu-id="cf809-116">Create a recurring data export app</span></span>](hr-admin-integration-recurring-data-export.md)
  - <span data-ttu-id="cf809-117">Integravimas su „Office“</span><span class="sxs-lookup"><span data-stu-id="cf809-117">Integrate with Office</span></span>
    - [<span data-ttu-id="cf809-118">„Office“ integravimo mokomoji programa</span><span class="sxs-lookup"><span data-stu-id="cf809-118">Office integration tutorial</span></span>](../dev-itpro/office-integration/office-integration-tutorial.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="cf809-119">Objekto duomenų naujinimas programoje „Excel“</span><span class="sxs-lookup"><span data-stu-id="cf809-119">Update entity data in Excel</span></span>](../dev-itpro/office-integration/use-excel-add-in.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="cf809-120">Atidarymo programoje „Excel“ patirčių kūrimas</span><span class="sxs-lookup"><span data-stu-id="cf809-120">Create Open in Excel experiences</span></span>](../dev-itpro/office-integration/office-integration-edit-excel.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="cf809-121">„Office“ integravimo trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="cf809-121">Troubleshoot Office integration</span></span>](../dev-itpro/office-integration/office-integration-troubleshooting.md?toc=/dynamics365/unified-operations/talent/toc.json)

- <span data-ttu-id="cf809-122">Objekto API nuoroda</span><span class="sxs-lookup"><span data-stu-id="cf809-122">Entity API reference</span></span>
  - [<span data-ttu-id="cf809-123">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="cf809-123">Authentication</span></span>](hr-developer-api-authentication.md)
  - <span data-ttu-id="cf809-124">Objektai</span><span class="sxs-lookup"><span data-stu-id="cf809-124">Entities</span></span>
    - [<span data-ttu-id="cf809-125">MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="cf809-125">MyLeaveRequests</span></span>](hr-developer-api-myleaverequests-overview.md)
    - [<span data-ttu-id="cf809-126">Prašymo išeiti atostogų pateikimas darbo eigai</span><span class="sxs-lookup"><span data-stu-id="cf809-126">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)

## <a name="see-also"></a><span data-ttu-id="cf809-127">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="cf809-127">See also</span></span>

- [<span data-ttu-id="cf809-128">Kas nauja ar pasikeitė programoje „Human Resources”</span><span class="sxs-lookup"><span data-stu-id="cf809-128">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="cf809-129">Administratoriaus vadovas</span><span class="sxs-lookup"><span data-stu-id="cf809-129">Administrator Guide</span></span>](hr-admin-overview.md)
- [<span data-ttu-id="cf809-130">Vartotojo vadovas</span><span class="sxs-lookup"><span data-stu-id="cf809-130">User Guide</span></span>](hr-hrpro-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]