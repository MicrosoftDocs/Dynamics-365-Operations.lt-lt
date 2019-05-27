---
title: DUK apie darbo eigas
description: Šioje temoje atsakomi dažnai užduodami klausimai apie darbo eigų sistemą programoje „Microsoft Dynamics 365 for Finance and Operations“.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509296"
---
# <a name="workflow-system"></a><span data-ttu-id="2248d-103">Darbo eigos sistema</span><span class="sxs-lookup"><span data-stu-id="2248d-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2248d-104">Šioje temoje atsakomi dažnai užduodami klausimai apie darbo eigų sistemą programoje „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="2248d-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="2248d-105">Pranešimai</span><span class="sxs-lookup"><span data-stu-id="2248d-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="2248d-106">Kodėl gaunami keli pranešimai, kai atmetamas darbo elementas?</span><span class="sxs-lookup"><span data-stu-id="2248d-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="2248d-107">Kai atmetamas darbo elementas, tas darbo elementas užbaigiamas kaip atmestas.</span><span class="sxs-lookup"><span data-stu-id="2248d-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="2248d-108">Sukuriamas kitas darbo elementas ir priskiriamas iniciatoriui.</span><span class="sxs-lookup"><span data-stu-id="2248d-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="2248d-109">Tai reiškia, kad iniciatorius gaus pranešimą apie atmestą darbo elementą, taip pat atskiras pranešimas bus išsiųstas vartotojui, kuris priskirtas naujam darbo elementui „reikalaujama keisti“.</span><span class="sxs-lookup"><span data-stu-id="2248d-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="2248d-110">Kiekvienas pranešimas skirtas skirtingam darbo elementui, tačiau dėl panašumų gali kilti painiava.</span><span class="sxs-lookup"><span data-stu-id="2248d-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="2248d-111">Ieškome būdų, kaip šią situaciją išspręsti būsimuose leidimuose.</span><span class="sxs-lookup"><span data-stu-id="2248d-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="2248d-112">Kodėl man nepavyksta eksportuoti darbo eigos?</span><span class="sxs-lookup"><span data-stu-id="2248d-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="2248d-113">Šiuo metu darbo eigos eksportavimo funkcija yra ribojama darbo eigos pavadinimams neleidžiant viršyti 48 ženklų.</span><span class="sxs-lookup"><span data-stu-id="2248d-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="2248d-114">Naudojant ilgesnius kaip 48 ženklų pavadinimus, pateikiama klaida „Serveriui nepavyko autentifikuoti užklausos“ ir (arba) neleidžiama eksportuoti failo be failo tipo.</span><span class="sxs-lookup"><span data-stu-id="2248d-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="2248d-115">Šiame tinklaraščio įraše pateikiama išsamesnė informacija [Darbo eigos eksportavimo trikčių šalinimas](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="2248d-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
