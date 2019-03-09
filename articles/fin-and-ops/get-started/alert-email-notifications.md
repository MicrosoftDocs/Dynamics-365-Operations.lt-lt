---
title: Kliento įspėjimų pranešimai el. paštu
description: Šioje temoje pateikiama informacija apie tai, kaip nustatyti taisykles, kurios siunčia el. pašto pranešimus įvykus iš anksto nurodytiems įvykiams.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 314f04eec04a75aed058c9c38066738e8758f653
ms.sourcegitcommit: 440ebe14ad26574ba227d23ee8370f6b6110645b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2019
ms.locfileid: "373803"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="4154e-103">Kliento įspėjimų pranešimai el. paštu</span><span class="sxs-lookup"><span data-stu-id="4154e-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="4154e-104">„Microsoft Dynamics 365 for Finance and Operations“ galite nustatyti pasirinktines įspėjimo taisykles, kurios stebi filtruotus duomenų rodinius ir automatiškai siunčia el. pašto pranešimus, kai įvyksta iš anksto nurodyti įvykiai.</span><span class="sxs-lookup"><span data-stu-id="4154e-104">In Microsoft Dynamics 365 for Finance and Operations, you can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="4154e-105">Parinktis siųsti el. pašto pranešimus suteikiama pasirinkus bet kurį palaikomą įspėjimo tipą ir ją taip pat galima įjungti pasirinkus esamas įspėjimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="4154e-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="4154e-106">Taip pat galite naudoti integruotus valdiklius, kad sukurtumėte įspėjimo taisykles, kurios stebi sistemos paketinių užduočių filtruotą vaizdą.</span><span class="sxs-lookup"><span data-stu-id="4154e-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="4154e-107">Stebėdami lauko **Būsena** reikšmę, taip pat galite sukonfigūruoti įspėjimo taisykles, kurios siunčia el. laišką, kai paketinės užduoties vykdymas nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="4154e-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="4154e-108">Sukūrę šias įspėjimo taisykles, galėsite nebetikrinti verslo duomenų pakeitimų ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="4154e-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="4154e-109">Vietoj to „Finance and Operations“ išmanioji pakeitimų atlikimo tarnyba gali stebėti už jus.</span><span class="sxs-lookup"><span data-stu-id="4154e-109">Instead, you can let the Finance and Operations intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="4154e-110">Kliento įspėjimai priklauso nuo el. pašto posistemės, kuri teikiama integruojant su „Microsoft Office“.</span><span class="sxs-lookup"><span data-stu-id="4154e-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="4154e-111">Rekomenduojame naudoti „Simple Mail Transfer Protocol“ (SMTP) teikėją, el. laiškų pristatymas nepriklausytų tik nuo vietos pašto kliento.</span><span class="sxs-lookup"><span data-stu-id="4154e-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="4154e-112">Norėdami siųsti pranešimus el. paštu, klientai turi sukonfigūruoti integruotas el. pašto paslaugas.</span><span class="sxs-lookup"><span data-stu-id="4154e-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="4154e-113">El. pašto pranešimai siunčiami gavėjams įspėjimo savininkų vardu.</span><span class="sxs-lookup"><span data-stu-id="4154e-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="4154e-114">Daugiau informacijos apie tai, kaip konfigūruoti el. paštą naudojant „Finance and Operations“ žr. [El. laiškų konfigūravimas ir siuntimas](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="4154e-114">For more information about how to configure email in Finance and Operations, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="4154e-115">Toliau pateiktame vaizde rodomas dialogo langas **Kurti įspėjimo taisyklę**, į kurį dabar įtraukta parinktis **Siųsti el. laišką**.</span><span class="sxs-lookup"><span data-stu-id="4154e-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="4154e-116">[![Dialogo langas Kurti įspėjimo taisyklę, kuriame parinktis Siųsti el. laišką nustatyta į Taip](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="4154e-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="4154e-117">Kai parinktis **Siųsti el. laišką** nustatyta į **Taip**, įspėjimo pranešimai bus toliau pristatomi iš veiksmų centro.</span><span class="sxs-lookup"><span data-stu-id="4154e-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="4154e-118">Įspėjimo pranešimų el. pašto šablonai</span><span class="sxs-lookup"><span data-stu-id="4154e-118">Alert notification email templates</span></span>

<span data-ttu-id="4154e-119">Paslauga siunčia el. pašto pranešimus naudodama iš anksto nustatytus el. laiškų šablonus, kad pristatytų pagrindinę įspėjimo pranešimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="4154e-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span> <span data-ttu-id="4154e-120">Šie duomenys apima tiesioginį saitą į puslapį, kuriame įspėjimo taisyklė buvo nustatyta.</span><span class="sxs-lookup"><span data-stu-id="4154e-120">These details include a direct link to the page where the alert rule was defined.</span></span>

<span data-ttu-id="4154e-121">Toliau pateiktame vaizde rodoma įspėjimo pranešimų struktūra juos gavus el. paštu.</span><span class="sxs-lookup"><span data-stu-id="4154e-121">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="4154e-122">[![Įrašų kūrimo, laukų pakeitimo ir šablonų naikinimo įspėjimo pranešimai, pagrįsti šablonu](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="4154e-122">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>