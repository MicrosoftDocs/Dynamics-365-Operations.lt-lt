---
title: DUK apie darbo eigas
description: Šioje temoje atsakomi dažnai užduodami klausimai apie darbo eigų sistemą programoje „Microsoft Dynamics 365 for Finance and Operations“.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
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
ms.openlocfilehash: 7ca04433937d0d7a16b450f190cd3814533e270d
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741061"
---
# <a name="workflow-faq"></a><span data-ttu-id="0ff23-103">DUK apie darbo eigas</span><span class="sxs-lookup"><span data-stu-id="0ff23-103">Workflow FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ff23-104">Šioje temoje atsakomi dažnai užduodami klausimai apie darbo eigų sistemą programoje „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="0ff23-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="0ff23-105">Kodėl gaunami keli pranešimai, kai atmetamas darbo elementas?</span><span class="sxs-lookup"><span data-stu-id="0ff23-105">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="0ff23-106">Kai atmetamas darbo elementas, tas darbo elementas užbaigiamas kaip atmestas.</span><span class="sxs-lookup"><span data-stu-id="0ff23-106">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="0ff23-107">Sukuriamas kitas darbo elementas ir priskiriamas iniciatoriui.</span><span class="sxs-lookup"><span data-stu-id="0ff23-107">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="0ff23-108">Tai reiškia, kad iniciatorius gaus pranešimą apie atmestą darbo elementą, taip pat atskiras pranešimas bus išsiųstas vartotojui, kuris priskirtas naujam darbo elementui „reikalaujama keisti“.</span><span class="sxs-lookup"><span data-stu-id="0ff23-108">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="0ff23-109">Kiekvienas pranešimas skirtas skirtingam darbo elementui, tačiau dėl panašumų gali kilti painiava.</span><span class="sxs-lookup"><span data-stu-id="0ff23-109">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="0ff23-110">Ieškome būdų, kaip šią situaciją išspręsti būsimuose leidimuose.</span><span class="sxs-lookup"><span data-stu-id="0ff23-110">We are looking at ways to improve this in a future release.</span></span>

## <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="0ff23-111">Kodėl man nepavyksta eksportuoti darbo eigos?</span><span class="sxs-lookup"><span data-stu-id="0ff23-111">Why are my workflow exports failing?</span></span>
<span data-ttu-id="0ff23-112">Šiuo metu darbo eigos eksportavimo funkcija yra ribojama darbo eigos pavadinimams neleidžiant viršyti 48 ženklų.</span><span class="sxs-lookup"><span data-stu-id="0ff23-112">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="0ff23-113">Naudojant ilgesnius kaip 48 ženklų pavadinimus, pateikiama klaida „Serveriui nepavyko autentifikuoti užklausos“ ir (arba) neleidžiama eksportuoti failo be failo tipo.</span><span class="sxs-lookup"><span data-stu-id="0ff23-113">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="0ff23-114">Šiame tinklaraščio įraše pateikiama išsamesnė informacija [Darbo eigos eksportavimo trikčių šalinimas](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="0ff23-114">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a><span data-ttu-id="0ff23-115">Ar darbo eigos pateikėjas gali ją taip pat ir tvirtinti?</span><span class="sxs-lookup"><span data-stu-id="0ff23-115">Can the submitter of a workflow also approve the workflow?</span></span>
<span data-ttu-id="0ff23-116">Taip, darbo eigos pateikėjas taip pat gali ją tvirtinti, jei darbo eiga taip sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="0ff23-116">Yes, a submitter of a workflow can also approve the workflow if it is configured that way.</span></span> <span data-ttu-id="0ff23-117">Jei norite to neleisti, nustatykite **Darbo eigos parametrai > Bendra > Tvirtintojas > Neleisti tvirtinti pateikėjui** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0ff23-117">To prevent this behavior, set **Workflow parameters > General > Approver > Disallow approval by submitter** to **Yes**.</span></span>

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a><span data-ttu-id="0ff23-118">Ar galiu įtraukti įspėjimų į darbo eigas, kad vartotojams būtų teikiami pranešimai?</span><span class="sxs-lookup"><span data-stu-id="0ff23-118">Can I add alerts to workflows to provide notifications to users?</span></span>
<span data-ttu-id="0ff23-119">Toliau pateikiamos kelios pagrindinės sritys, susijusios su įspėjimų įtraukimų į darbo sritis norint teikti pranešimus vartotojams, į kurias reikia atkreipti dėmesį.</span><span class="sxs-lookup"><span data-stu-id="0ff23-119">Here are a few key areas to note about adding alerts to workflows to provide notifications:</span></span>
- <span data-ttu-id="0ff23-120">Įspėjimų palyginimas su darbo eigų pranešimų mechanizmais</span><span class="sxs-lookup"><span data-stu-id="0ff23-120">Alerts versus workflow notification mechanisms</span></span>
    - <span data-ttu-id="0ff23-121">Galima nustatyti įrašų pakeitimų įspėjimus.</span><span class="sxs-lookup"><span data-stu-id="0ff23-121">Alerts can be set up for record changes.</span></span> <span data-ttu-id="0ff23-122">Darbo eigos keičia įrašus, todėl galima nustatyti įspėjimą, susijusį su darbo eigos inicijuotu įrašo pakeitimu.</span><span class="sxs-lookup"><span data-stu-id="0ff23-122">Workflows change records, so it's possible to set up an alert related to a record change caused by a workflow.</span></span> <span data-ttu-id="0ff23-123">Vis dėlto, įspėjimų naudojimas nėra tobulas sprendimas, nes darbo eigose įtaisytos skirtingos pranešimų parinktys.</span><span class="sxs-lookup"><span data-stu-id="0ff23-123">However, because workflows have different built-in notification options, using alerts isn’t ideal.</span></span>
- <span data-ttu-id="0ff23-124">Standartiniai darbo eigų pranešimai</span><span class="sxs-lookup"><span data-stu-id="0ff23-124">Standard notifications from workflows</span></span> 
    - <span data-ttu-id="0ff23-125">Darbo eigose yra įtaisytų el. pašto pranešimų.</span><span class="sxs-lookup"><span data-stu-id="0ff23-125">Workflows have built in email notifications.</span></span> <span data-ttu-id="0ff23-126">Klientas gali konfigūruoti pranešimus, kad vartotojams būtų siunčiami el. laiškai.</span><span class="sxs-lookup"><span data-stu-id="0ff23-126">A customer can configure the notifications so that the users are sent emails.</span></span> <span data-ttu-id="0ff23-127">Šie pranešimai neinicijuoja veiksmų centro pranešimų vartotojams.</span><span class="sxs-lookup"><span data-stu-id="0ff23-127">Those notifications don’t result in Action Center messages for users.</span></span>
    - <span data-ttu-id="0ff23-128">Būsimame naujinime veiksmų centro pranešimą, kad vartotojui būtų priskirtas darbo eigos darbo elementas.</span><span class="sxs-lookup"><span data-stu-id="0ff23-128">In a future update we will be adding an Action Center message so a user is assigned a workflow work item.</span></span> 
- <span data-ttu-id="0ff23-129">Pranešimų įtraukimas į darbo eigas</span><span class="sxs-lookup"><span data-stu-id="0ff23-129">Adding notifications to workflows</span></span>
    - <span data-ttu-id="0ff23-130">Galima sukurti veiksmų centro pranešimų konkretiems vartotojams, pvz., darbo eigos pranešimų, sukurtų naudojant X++.</span><span class="sxs-lookup"><span data-stu-id="0ff23-130">Action Center messages can be created for specific users, such as a message created from a workflow in X++.</span></span>
    - <span data-ttu-id="0ff23-131">[Darbo eigose yra verslo įvykių](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow), kuriuos klientas gali naudoti norėdamas suaktyvinti srautus su ieškomais pranešimais.</span><span class="sxs-lookup"><span data-stu-id="0ff23-131">[Workflows have Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) that the customer could use to trigger Flows have the notifications that they are looking for.</span></span>   

<span data-ttu-id="0ff23-132">Apibendrinant, jei vartotojas negauna tinkamo pranešimo iš veiksmų centro, kai jam priskiriamas darbo eigos darbo elementas, naudokite [darbo eigos verslo įvykius](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) programoje „Microsoft Flow, kad pateiktumėte papildomų arba kitokių pranešimų.</span><span class="sxs-lookup"><span data-stu-id="0ff23-132">In summary, if a user does not get the proper notification from the Action Center when they are assigned a workflow work item, then leverage [Workflow Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) with Microsoft Flow to provide additional or different notifications.</span></span>
