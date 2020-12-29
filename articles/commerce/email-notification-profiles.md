---
title: El. paštu siunčiamų pranešimų šablono nustatymas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti el. paštu siunčiamų pranešimų šabloną.
author: samjarawan
manager: annbe
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c0ab56c15a37313d0a88b1174d5bcf51d391dcec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414260"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="32403-103">El. paštu siunčiamų pranešimų šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="32403-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="32403-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti el. paštu siunčiamų pranešimų šabloną.</span><span class="sxs-lookup"><span data-stu-id="32403-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="32403-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="32403-105">Overview</span></span>

<span data-ttu-id="32403-106">Prieš kurdami kanalus, nustatykite šabloną, kad būtų užtikrinta, jog el. paštu siunčiami pranešimai būtų siunčiami įvairių įvykių, pvz., užsakymo kūrimo, užsakymo siuntimo būsenos ir mokėjimo klaidos, atvejais.</span><span class="sxs-lookup"><span data-stu-id="32403-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="32403-107">Papildomos informacijos apie tai, kaip konfigūruoti el. paštą, žr. [El. laiškų konfigūravimas ir siuntimas](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="32403-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="32403-108">El. paštu siunčiamų pranešimų šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="32403-108">Create an email notification profile</span></span>

<span data-ttu-id="32403-109">Norėdami sukurti el. paštu siunčiamų pranešimų šabloną, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="32403-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="32403-110">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Būstinės sąranka \>„Commerce“ el. paštu siunčiamų pranešimų šablonas**.</span><span class="sxs-lookup"><span data-stu-id="32403-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="32403-111">Veiksmų srityje spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="32403-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="32403-112">Lauke **El. paštu siunčiamų pranešimų šablonas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="32403-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="32403-113">Lauke **Aprašas** įveskite tinkamą aprašą.</span><span class="sxs-lookup"><span data-stu-id="32403-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="32403-114">Jungiklį **Aktyvusis** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="32403-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="32403-115">El. laiško šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="32403-115">Create an email template</span></span>

<span data-ttu-id="32403-116">Prieš sukuriant el. paštu siunčiamą pranešimą, reikia sukurti organizacijos el. pašto šabloną, kuriame būtų siuntėjo el. pašto informacija ir el. pašto šablonas.</span><span class="sxs-lookup"><span data-stu-id="32403-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="32403-117">Norėdami sukurti el. pašto šabloną, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="32403-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="32403-118">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Parametrai \> Organizacijos el. laiškų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="32403-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="32403-119">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="32403-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="32403-120">Lauke **El. pašto ID** įveskite šio šablono ID.</span><span class="sxs-lookup"><span data-stu-id="32403-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="32403-121">Lauke **Siuntėjo vardas, pavardė** įveskite siuntėjo vardą, pavardę.</span><span class="sxs-lookup"><span data-stu-id="32403-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="32403-122">Lauke **El. pašto aprašas** įveskite reikšmingą aprašą.</span><span class="sxs-lookup"><span data-stu-id="32403-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="32403-123">Lauke **Siuntėjo el. paštas** įveskite siuntėjo el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="32403-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="32403-124">Skyriuje **Bendra** įrašykite visą reikiamą neprivalomą informaciją (pvz., el. pašto prioritetą).</span><span class="sxs-lookup"><span data-stu-id="32403-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="32403-125">Išplėskite skyrių **El. laiško turinys** ir pasirinkite **Naujas**, kad sukurtumėte šablono turinį.</span><span class="sxs-lookup"><span data-stu-id="32403-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="32403-126">Pasirinkite kiekvieno turinio elemento kalbą ir nurodykite el. pašto temą.</span><span class="sxs-lookup"><span data-stu-id="32403-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="32403-127">Jei el. laiške bus teksto, užtikrinkite, kad pažymėtas žymės langelis **Yra teksto**.</span><span class="sxs-lookup"><span data-stu-id="32403-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="32403-128">Veiksmų srityje pasirinkite **El. laiško tekstas** ir sukurkite el. laiško teksto šabloną.</span><span class="sxs-lookup"><span data-stu-id="32403-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="32403-129">Toliau pateiktame vaizde parodyti keli el. pašto šablonų parametrų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="32403-129">The following image shows some example email template settings.</span></span>

![El. pašto šablonų parametrai](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="32403-131">El. laiško įvykio kūrimas</span><span class="sxs-lookup"><span data-stu-id="32403-131">Create an email event</span></span>

<span data-ttu-id="32403-132">Norėdami sukurti el. laiško įvykį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="32403-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="32403-133">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Būstinės sąranka \>„Commerce“ el. paštu siunčiamų pranešimų šablonas**.</span><span class="sxs-lookup"><span data-stu-id="32403-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="32403-134">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="32403-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="32403-135">Išplečiamajame sąraše **El. pašto ID** pasirinkite el. laiško šabloną.</span><span class="sxs-lookup"><span data-stu-id="32403-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="32403-136">Išplečiamajame sąraše pasirinkite tinkamą parinktį **El. paštu siunčiamo pranešimo tipas**.</span><span class="sxs-lookup"><span data-stu-id="32403-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="32403-137">Pažymėkite žymės langelį **Aktyvusis**.</span><span class="sxs-lookup"><span data-stu-id="32403-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="32403-138">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="32403-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="32403-139">Toliau pateiktame vaizde parodyti keli įvykių pranešimų parametrų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="32403-139">The following image shows some example event notification settings.</span></span>

![Įvykio pranešimo parametrai](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="32403-141">Kiti veiksmai</span><span class="sxs-lookup"><span data-stu-id="32403-141">Next steps</span></span>

<span data-ttu-id="32403-142">Kad galėtumėte siųsti laiškus, turite sukonfigūruoti siunčiamo pašto paslaugą ir nustatyti paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="32403-142">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="32403-143">Norėdami gauti daugiau informacijos, žr. [El. laiškų konfigūravimas ir siuntimas](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="32403-143">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="32403-144">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="32403-144">Additional resources</span></span>

[<span data-ttu-id="32403-145">El. pašto konfigūravimas ir siuntimas</span><span class="sxs-lookup"><span data-stu-id="32403-145">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="32403-146">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="32403-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="32403-147">Kanalo sąrankos būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="32403-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="32403-148">Organizacijų ir organizacijų hierarchijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="32403-148">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
