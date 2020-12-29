---
title: Tinkinti perlaidų el. paštus pagal pristatymo būdą
description: Šioje temoje aprašoma, kaip nustatyti tinkintus el. pašto šablonus konkretiems pranešimų tipams ir pristatymo būdams „Microsoft Dynamics 365 Commerce“.
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: faf5fba70bf9297727464e6046806696ab725001
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594984"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="27846-103">Tinkinti perlaidų el. paštus pagal pristatymo būdą</span><span class="sxs-lookup"><span data-stu-id="27846-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="27846-104">Šioje temoje aprašoma, kaip nustatyti tinkintus el. pašto šablonus konkretiems pranešimų tipams ir pristatymo būdams „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="27846-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="27846-105">Perdavimo el. paštai gali būti dabar tinkinami pranešimo tipo deriniams (pavyzdžiui, **Sukurtas užsakymas**, **Paimtas užsakymas** ar **Išrašytas į sąskaitą užsakymas**) ir pristatymo būdas (pavyzdžiui, per naktį, atsiėmimas parduotuvėje ar atsiėmimas per langelį).</span><span class="sxs-lookup"><span data-stu-id="27846-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="27846-106">Tinkinti perlaidos el. laiškai leidžia mažmeniniams prekiautojams pateikti jų klientams užsakymą su patirčių įgyvendinimu, kuris būtų pritaikytas prie užsakymo pristatymo būdo.</span><span class="sxs-lookup"><span data-stu-id="27846-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="27846-107">Pavyzdžiui, „supakuoto užsakymo“ įvykis gali būti tinkintas taip, kad jis pateiktų atsiėmimo per langelį instrukcijas klientams, kurie tokį pasirenka.</span><span class="sxs-lookup"><span data-stu-id="27846-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="27846-108">Kitu atveju, jis gali pateikti pristatymo vežėją ir informaciją klientams, kurie pasirenka siųsti savo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="27846-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="27846-109">Norėdami naudoti tinkintos perlaidos el. laiškų funkciją, turite pirmiausia įjungti **Tinktintos perlaidos el. laiškų šablonai pagal pristatymo būdą** funkciją patekę į **Darbo aplinkos \> Funkcijų valdymas** „Commerce“ štabe.</span><span class="sxs-lookup"><span data-stu-id="27846-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="27846-110">El. laiškai gali būti tinkinti pagal pristatymo būdą tolesniems pranešimo tipams:</span><span class="sxs-lookup"><span data-stu-id="27846-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="27846-111">**Užsakymo atšaukimas** – Šis el. laiško pranešimo tipas yra naujas.</span><span class="sxs-lookup"><span data-stu-id="27846-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="27846-112">**Užsakymas sukurtas**</span><span class="sxs-lookup"><span data-stu-id="27846-112">**Order created**</span></span>
- <span data-ttu-id="27846-113">**Užsakymas patvirtintas**</span><span class="sxs-lookup"><span data-stu-id="27846-113">**Order confirmed**</span></span>
- <span data-ttu-id="27846-114">**Užsakymo įrašymas į sąskaitą** – Šis el. laiško pranešimo tipas yra naujas.</span><span class="sxs-lookup"><span data-stu-id="27846-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="27846-115">Jis gali būti naudojamas vietoje **Išsiųsto užsakymo** pranešimo tipas, kuris nusiųs pranešimą bet kurios sąskaitos įvykiui su pristatymo siuntimo būdu (ne atsiėmimo, vykdymo ar elektroninio pristatymo būdu).</span><span class="sxs-lookup"><span data-stu-id="27846-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="27846-116">**Užsakymas paimtas**</span><span class="sxs-lookup"><span data-stu-id="27846-116">**Order picked**</span></span>
- <span data-ttu-id="27846-117">**Užsakymas supakuotas**</span><span class="sxs-lookup"><span data-stu-id="27846-117">**Order packed**</span></span>
- <span data-ttu-id="27846-118">**Užsakymas pasrengtas atsiėmimui** – Šis pranešimo tipas gali būti tinkintas pagal pristatymo būdą tik jei **Palaikyti keletą atsiėmimo pristatymo būdų** funkcija yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="27846-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="27846-119">Tokiu atveju, šis pranešimo tipas yra funkcija lygi **Supakuotas užsakymas** pranešimo tipui.</span><span class="sxs-lookup"><span data-stu-id="27846-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="27846-120">**Mokėjimo atlikti nepavyko**</span><span class="sxs-lookup"><span data-stu-id="27846-120">**Payment failed**</span></span>
- <span data-ttu-id="27846-121">**Pakeitimo užsakymas sukurtas**</span><span class="sxs-lookup"><span data-stu-id="27846-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="27846-122">Konfigūruoti el. laiško šablonus konkrečiam pristatymo būdui</span><span class="sxs-lookup"><span data-stu-id="27846-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="27846-123">Šiai procedūrai, yra prielaida, kad jau sukūrėte naują, tinkintą el. laiško šabloną ir įtraukėte jį į **Organizacijos el. laiško šablonus** puslapį.</span><span class="sxs-lookup"><span data-stu-id="27846-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="27846-124">Dėl informacijos apie tai, kaip sukurti ir naujinti el. laiškų šablonus, žr. [Sukurti el. laiško šablonus perlaidų įvykiams](email-templates-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="27846-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="27846-125">Siekiant konfigūruoti el. laiško šablonus konkretiems pristatymo būdams „Commerce“ štabe, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="27846-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="27846-126">Eikite į **Komercijos el. laiško pranešimo profilis**.</span><span class="sxs-lookup"><span data-stu-id="27846-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="27846-127">Skyriuje **Mažmeninės prekybos įvykio pranešimo nustatymai**, pasirinkite esantį pranešimo tipą.</span><span class="sxs-lookup"><span data-stu-id="27846-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="27846-128">Pasirinkus pranešimo tipą, pasirinkite **Konfigūruoti pristatymo būdus**.</span><span class="sxs-lookup"><span data-stu-id="27846-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="27846-129">Teksto laukelyje **Pristatymo būdai** rinkitės **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="27846-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="27846-130">Naujoje eilutėje **Pristatymo būdas** laukelyje, rinkitės pristatymo būdą.</span><span class="sxs-lookup"><span data-stu-id="27846-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="27846-131">Laukelyje **El. pašto ID**, rinkitės el. laiško šabloną, kad talpintumėte į žemėlapį pristatymo būdą.</span><span class="sxs-lookup"><span data-stu-id="27846-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="27846-132">Pažymėkite žymės langelį **Aktyvusis**.</span><span class="sxs-lookup"><span data-stu-id="27846-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="27846-133">Pakartokite žingsnius nuo 4 iki 7, kad įtrauktumėte daugiau pristatymo būdų.</span><span class="sxs-lookup"><span data-stu-id="27846-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="27846-134">Pabaigus, rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="27846-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="27846-135">Kai daugiau nei vienas pristatymo būdas yra tarp eilučių prekybos užsakyme, bus naudojamas nustatytasis šablonas.</span><span class="sxs-lookup"><span data-stu-id="27846-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="27846-136">Nustatytasis šablonas yra šablonas, kuris patalpintas prie pranešimo tipo, puslapyje **„Commerce“ el. laiško pranešimo profilyje**.</span><span class="sxs-lookup"><span data-stu-id="27846-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="27846-137">Jei prekybos užsakymas turi prisitatymo būdą, kuris nėra sukonfigūruotas tinkintam el. laiško šablonui, bus naudojamas numatytasis šablonas.</span><span class="sxs-lookup"><span data-stu-id="27846-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27846-138">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="27846-138">Additional resources</span></span>

[<span data-ttu-id="27846-139">Skambučių centro užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="27846-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="27846-140">Pristatymo režimo keitimas EKA</span><span class="sxs-lookup"><span data-stu-id="27846-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)
