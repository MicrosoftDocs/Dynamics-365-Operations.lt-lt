---
title: El. paštu siunčiamų pranešimų šablono nustatymas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti el. paštu siunčiamų pranešimų šabloną.
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d82a1abe68ff6e162acb75c6fdc1e207af11c279
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555312"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="135aa-103">El. paštu siunčiamo pranešimo šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="135aa-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="135aa-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti el. paštu siunčiamų pranešimų šabloną.</span><span class="sxs-lookup"><span data-stu-id="135aa-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="135aa-105">Kurdami kanalus galite nustatyti el. paštu siunčiamo pranešimo profilį.</span><span class="sxs-lookup"><span data-stu-id="135aa-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="135aa-106">Tokiu būdu el. laiškus galima siųsti klientams dėl įvairių operacijų įvykių, pvz., užsakymo sukūrimo, užsakymo siuntimo būsenos ir mokėjimo trikties.</span><span class="sxs-lookup"><span data-stu-id="135aa-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="135aa-107">Papildomos informacijos apie tai, kaip konfigūruoti el. paštą, žr. [El. laiškų konfigūravimas ir siuntimas](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="135aa-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="135aa-108">El. paštu siunčiamų pranešimų šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="135aa-108">Create an email notification profile</span></span>

<span data-ttu-id="135aa-109">Norėdami sukurti el. paštu siunčiamų pranešimų šabloną, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="135aa-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="135aa-110">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Būstinės sąranka \>„Commerce“ el. paštu siunčiamų pranešimų šablonas**.</span><span class="sxs-lookup"><span data-stu-id="135aa-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="135aa-111">Veiksmų srityje spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="135aa-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="135aa-112">Lauke **El. paštu siunčiamų pranešimų šablonas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="135aa-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="135aa-113">Lauke **Aprašas** įveskite tinkamą aprašą.</span><span class="sxs-lookup"><span data-stu-id="135aa-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="135aa-114">Jungiklį **Aktyvusis** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="135aa-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="135aa-115">El. laiško šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="135aa-115">Create an email template</span></span>

<span data-ttu-id="135aa-116">Kad būtų galima įgalinti el. paštu siunčiamo pranešimo tipą, „Commerce“ valdymo srityje reikia sukurti organizacijos el. laiško šabloną.</span><span class="sxs-lookup"><span data-stu-id="135aa-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="135aa-117">Šiame šablone apibrėžiamas kiekvienos norimos palaikyti kalbos el. laiško tema, siuntėjas, numatytoji kalba ir el. laiško tekstas.</span><span class="sxs-lookup"><span data-stu-id="135aa-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="135aa-118">Norėdami sukurti el. pašto šabloną, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="135aa-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="135aa-119">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Parametrai \> Organizacijos el. laiškų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="135aa-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="135aa-120">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="135aa-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="135aa-121">Lauke **El. pašto ID** įveskite šio šablono ID.</span><span class="sxs-lookup"><span data-stu-id="135aa-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="135aa-122">Lauke **Siuntėjo vardas, pavardė** įveskite siuntėjo vardą, pavardę.</span><span class="sxs-lookup"><span data-stu-id="135aa-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="135aa-123">Lauke **El. pašto aprašas** įveskite reikšmingą aprašą.</span><span class="sxs-lookup"><span data-stu-id="135aa-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="135aa-124">Lauke **Siuntėjo el. paštas** įveskite siuntėjo el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="135aa-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="135aa-125">Dalyje **Bendra** pasirinkite numatytąją el. laiško šablono kalbą.</span><span class="sxs-lookup"><span data-stu-id="135aa-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="135aa-126">Numatytoji kalba bus naudojama, kai nėra jokio lokalizuoto šablono nurodyta kalba.</span><span class="sxs-lookup"><span data-stu-id="135aa-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="135aa-127">Išplėskite skyrių **El. laiško turinys** ir pasirinkite **Naujas**, kad sukurtumėte šablono turinį.</span><span class="sxs-lookup"><span data-stu-id="135aa-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="135aa-128">Pasirinkite kiekvieno turinio elemento kalbą ir nurodykite el. pašto temą.</span><span class="sxs-lookup"><span data-stu-id="135aa-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="135aa-129">Jei el. laiške bus teksto, užtikrinkite, kad pažymėtas žymės langelis **Yra teksto**.</span><span class="sxs-lookup"><span data-stu-id="135aa-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="135aa-130">Veiksmų srityje pasirinkite **El. laiško tekstas** ir sukurkite el. laiško teksto šabloną.</span><span class="sxs-lookup"><span data-stu-id="135aa-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="135aa-131">Toliau pateiktame vaizde parodyti keli el. pašto šablonų parametrų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="135aa-131">The following image shows some example email template settings.</span></span>

![El. pašto šablonų parametrai](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="135aa-133">El. laiško įvykio kūrimas</span><span class="sxs-lookup"><span data-stu-id="135aa-133">Create an email event</span></span>

<span data-ttu-id="135aa-134">Norėdami sukurti el. laiško įvykį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="135aa-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="135aa-135">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Būstinės sąranka \>„Commerce“ el. paštu siunčiamų pranešimų šablonas**.</span><span class="sxs-lookup"><span data-stu-id="135aa-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="135aa-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="135aa-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="135aa-137">Išplečiamajame sąraše **El. pašto ID** pasirinkite el. laiško šabloną.</span><span class="sxs-lookup"><span data-stu-id="135aa-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="135aa-138">Išplečiamajame sąraše pasirinkite tinkamą parinktį **El. paštu siunčiamo pranešimo tipas**.</span><span class="sxs-lookup"><span data-stu-id="135aa-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="135aa-139">Pažymėkite žymės langelį **Aktyvusis**.</span><span class="sxs-lookup"><span data-stu-id="135aa-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="135aa-140">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="135aa-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="135aa-141">Toliau pateiktame vaizde parodyti keli įvykių pranešimų parametrų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="135aa-141">The following image shows some example event notification settings.</span></span>

![Įvykio pranešimo parametrai](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="135aa-143">Kiti veiksmai</span><span class="sxs-lookup"><span data-stu-id="135aa-143">Next steps</span></span>

<span data-ttu-id="135aa-144">Kad galėtumėte siųsti laiškus, turite sukonfigūruoti siunčiamo pašto paslaugą ir nustatyti paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="135aa-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="135aa-145">Norėdami gauti daugiau informacijos, žr. [El. laiškų konfigūravimas ir siuntimas](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="135aa-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="135aa-146">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="135aa-146">Additional resources</span></span>

[<span data-ttu-id="135aa-147">El. pašto konfigūravimas ir siuntimas</span><span class="sxs-lookup"><span data-stu-id="135aa-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="135aa-148">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="135aa-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="135aa-149">Kanalo sąrankos būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="135aa-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="135aa-150">Organizacijų ir organizacijų hierarchijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="135aa-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
