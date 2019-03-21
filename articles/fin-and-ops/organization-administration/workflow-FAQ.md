---
title: DUK apie darbo eigas
description: Šioje temoje atsakomi dažnai užduodami klausimai apie darbo eigų sistemą programoje „Microsoft Dynamics 365 for Finance and Operations“.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
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
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/01/2019
ms.locfileid: "773223"
---
# <a name="workflow-system"></a><span data-ttu-id="e69ff-103">Darbo eigos sistema</span><span class="sxs-lookup"><span data-stu-id="e69ff-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e69ff-104">Šioje temoje atsakomi dažnai užduodami klausimai apie darbo eigų sistemą programoje „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="e69ff-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="e69ff-105">Pranešimai</span><span class="sxs-lookup"><span data-stu-id="e69ff-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="e69ff-106">Kodėl gaunami keli pranešimai, kai atmetamas darbo elementas?</span><span class="sxs-lookup"><span data-stu-id="e69ff-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="e69ff-107">Kai atmetamas darbo elementas, tas darbo elementas užbaigiamas kaip atmestas.</span><span class="sxs-lookup"><span data-stu-id="e69ff-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="e69ff-108">Sukuriamas kitas darbo elementas ir priskiriamas iniciatoriui.</span><span class="sxs-lookup"><span data-stu-id="e69ff-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="e69ff-109">Tai reiškia, kad iniciatorius gaus pranešimą apie atmestą darbo elementą, taip pat atskiras pranešimas bus išsiųstas vartotojui, kuris priskirtas naujam darbo elementui „reikalaujama keisti“.</span><span class="sxs-lookup"><span data-stu-id="e69ff-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="e69ff-110">Kiekvienas pranešimas skirtas skirtingam darbo elementui, tačiau dėl panašumų gali kilti painiava.</span><span class="sxs-lookup"><span data-stu-id="e69ff-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="e69ff-111">Ieškome būdų, kaip šią situaciją išspręsti būsimuose leidimuose.</span><span class="sxs-lookup"><span data-stu-id="e69ff-111">We are looking at ways to improve this in a future release.</span></span>
