---
title: Proceso automatizavimo srautų iškvietimas kokybės užsakymams kurti
description: Šioje temoje pateikiami ištekliai, naudojami „Power Automate” verslo procesams automatizuoti, naudojant kokybės užsakymų pavyzdį.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115204"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="e2107-103">Proceso automatizavimo srautų iškvietimas kokybės užsakymams kurti</span><span class="sxs-lookup"><span data-stu-id="e2107-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="e2107-104">Organizacijos turi didėjantį poreikį automatizuoti standartinius verslo procesus, suteikti patogesnes sąveikas su darbuotojais ir naudoti įvairius duomenų signalus ir sistemas, kad verslo procesai būtų vykdomi automatiškai.</span><span class="sxs-lookup"><span data-stu-id="e2107-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="e2107-105">Naudojant robotinį procesų automatizavimą (RPA) ir „Microsoft Power Automate”, įmonės gali naudoti „jokių kodų” patirtį pasikartojantiems procesams automatizuoti, tokiu būdu didinant efektyvumą ir tikslumą.</span><span class="sxs-lookup"><span data-stu-id="e2107-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="e2107-106">„Supply Chain Management” skirtas automatizavimo sprendimo šablonas parodo, kaip galima naudoti „Power Automate” verslo procesų automatizavimui, naudojant kokybės užsakymus kaip pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="e2107-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="e2107-107">Galite atsisiųsti automatizavimo sprendimo šabloną [čia](https://aka.ms/D365SCMQualityOrderRPASolution).</span><span class="sxs-lookup"><span data-stu-id="e2107-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="e2107-108">Šios funkcijos ir jos galimybių apžvalgą rasite šiame vaizdo įraše: [RPA naudojimas kokybės užsakymams kurti „Dynamics 365 Supply Chain Management” platformoje](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="e2107-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="e2107-109">![Automatizavimo parinktys naudojant RPA](media/rpa-automation-options.png "Automatizavimo parinktys naudojant RPA")</span><span class="sxs-lookup"><span data-stu-id="e2107-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="e2107-110">„Power Automate” sprendimo šablone yra debesies ir darbalaukio automatizavimo srautai, kurie automatizuoja kokybės užsakymų kūrimą „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="e2107-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="e2107-111">Automatizavimą galima pradėti kaip atsaką į daugelį įvykių ir signalų, įskaitant vartotojo įvestį arba mašinų signalus (įskaitant Internetu sąveikaujančius įrenginius („IoT”)).</span><span class="sxs-lookup"><span data-stu-id="e2107-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="e2107-112">*„Q-Order* Power” programos pavyzdys yra įtrauktas į sprendimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="e2107-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="e2107-113">Jis leidžia vartotojui nuskaityti prekės QR kodą, įvesti kiekį ir pridėti paveikslėlius naudojant fotoaparatą.</span><span class="sxs-lookup"><span data-stu-id="e2107-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="e2107-114">Sprendimo parametrai yra įtraukiami, kad būtų konfigūruojamas konkretaus naudojimo atvejo automatizavimas gamybos priemonėje.</span><span class="sxs-lookup"><span data-stu-id="e2107-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="e2107-115">![Kurti kokybės užsakymą](media/rpa-create-quality-roder.png "Kurti kokybės užsakymą")</span><span class="sxs-lookup"><span data-stu-id="e2107-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="e2107-116">Išsamias instrukcijas apie tai, kaip atsisiųsti, įdiegti ir naudoti pavyzdinį sprendimą kokybės užsakymų kūrimui automatizuoti, rasite [Kokybės užsakymų kūrimo automatizavimas „Dynamics 365 Supply Chain Management” su Robotiniu procesų automatizavimu, naudojant „Power Automate Desktop”](/power-automate/desktop-flows/dynamics365-scm-rpa).</span><span class="sxs-lookup"><span data-stu-id="e2107-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

