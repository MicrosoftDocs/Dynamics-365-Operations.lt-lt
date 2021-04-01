---
title: Kanalų apžvalga
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ kanalų apžvalga.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8ac188832bdaeba430eed7f08e91a9c2214a0e15
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219106"
---
# <a name="channels-overview"></a><span data-ttu-id="d9b18-103">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="d9b18-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d9b18-104">Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ kanalų apžvalga.</span><span class="sxs-lookup"><span data-stu-id="d9b18-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="d9b18-105">Jame pateikiama informacija apie užduotis, kurias turite atlikti prieš ir po kiekvieno kanalo nustatymo.</span><span class="sxs-lookup"><span data-stu-id="d9b18-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="d9b18-106">Kanalų tipai</span><span class="sxs-lookup"><span data-stu-id="d9b18-106">Types of Channels</span></span>

<span data-ttu-id="d9b18-107">„Dynamics 365 Commerce“ palaiko tris skirtingus kanalų tipus: mažmeninė prekyba, skambučių centras ir interneto kanalai.</span><span class="sxs-lookup"><span data-stu-id="d9b18-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="d9b18-108">Mažmeninės prekybos kanalai</span><span class="sxs-lookup"><span data-stu-id="d9b18-108">Retail channels</span></span>

<span data-ttu-id="d9b18-109">Mažmeninės prekybos kanalai yra standartinės fizinės parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="d9b18-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="d9b18-110">Kiekvienoje parduotuvėje yra nuosavi elektroninių kasos aparatų (EKA) registrai, pajamų ir išlaidų sąskaitos bei darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="d9b18-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="d9b18-111">Skambučių centro kanalai</span><span class="sxs-lookup"><span data-stu-id="d9b18-111">Call center channels</span></span>

<span data-ttu-id="d9b18-112">Skambučių centro kanalai – tai skambučių centro užsakymai ir klientų valdymas.</span><span class="sxs-lookup"><span data-stu-id="d9b18-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="d9b18-113">Interneto kanalai</span><span class="sxs-lookup"><span data-stu-id="d9b18-113">Online channels</span></span>

<span data-ttu-id="d9b18-114">Interneto kanalai internetinės el. prekybos vitrinos.</span><span class="sxs-lookup"><span data-stu-id="d9b18-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="d9b18-115">Kai sukurtas interneto kanalas, reikia sukurti saitą naudojant „Microsoft Dynamics 365 Commerce“ svetainės generatoriaus įrankį arba kitą trečiosios šalies el. prekybos sprendimą.</span><span class="sxs-lookup"><span data-stu-id="d9b18-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="d9b18-116">Kanalo sąrankos pagrindai</span><span class="sxs-lookup"><span data-stu-id="d9b18-116">Channel setup basics</span></span>

<span data-ttu-id="d9b18-117">Kanalų nustatymas atliekamas naudojant „Commerce“ įrankį.</span><span class="sxs-lookup"><span data-stu-id="d9b18-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="d9b18-118">Kiekvienas kanalas gali turėti savo mokėjimo metodus, kainų grupes, produktų hierarchijas, asortimentus ir produktų rinkinius.</span><span class="sxs-lookup"><span data-stu-id="d9b18-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="d9b18-119">Kai sukuriate kanalą, galite priskirti produktus, kuriuos norite, kad jis platintų ir parduotų.</span><span class="sxs-lookup"><span data-stu-id="d9b18-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="d9b18-120">Kiekvienas kanalo tipas turi unikalų funkcijų rinkinį, kurį gali reikėti sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="d9b18-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="d9b18-121">Pavyzdžiui, mažmeninės prekybos kanalui reikia priskirti darbuotojus, registrus ir klientus.</span><span class="sxs-lookup"><span data-stu-id="d9b18-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="d9b18-122">Sukūrus naują kanalą, jis turi būti priskirtas organizacijos hierarchijai.</span><span class="sxs-lookup"><span data-stu-id="d9b18-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="d9b18-123">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="d9b18-123">Channel setup prerequisites</span></span>

<span data-ttu-id="d9b18-124">Kad galėtumėte nustatyti kanalą, turite atlikti keletą būtinųjų užduočių pagal kanalo tipą.</span><span class="sxs-lookup"><span data-stu-id="d9b18-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="d9b18-125">Daugiau informacijos žr. [Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="d9b18-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="d9b18-126">Kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d9b18-126">Set up a channel</span></span>

<span data-ttu-id="d9b18-127">Pabaigę būtinąsias užduotis, tolesnes nustatymo funkcijas žr. toliau pateiktuose saituose.</span><span class="sxs-lookup"><span data-stu-id="d9b18-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="d9b18-128">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d9b18-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="d9b18-129">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d9b18-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="d9b18-130">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d9b18-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="d9b18-131">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d9b18-131">Additional resources</span></span>

[<span data-ttu-id="d9b18-132">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="d9b18-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="d9b18-133">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d9b18-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="d9b18-134">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d9b18-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="d9b18-135">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d9b18-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="d9b18-136">Organizacijų hierarchijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="d9b18-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]