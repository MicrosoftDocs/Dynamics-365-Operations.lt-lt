---
title: "Skambučių centro katalogai"
description: "Šiame straipsnyje aprašyta konkreti skambučių centro funkcija, skirta katalogams „Microsoft Dynamics 365 for Retail“."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e5a97ab749259fcc97b269b0134792820ebf13af
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="call-center-catalogs"></a><span data-ttu-id="dcc17-103">Skambučių centro katalogai</span><span class="sxs-lookup"><span data-stu-id="dcc17-103">Call center catalogs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="dcc17-104">Šiame straipsnyje aprašyta konkreti skambučių centro funkcija, skirta katalogams „Microsoft Dynamics 365 for Retail“.</span><span class="sxs-lookup"><span data-stu-id="dcc17-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="dcc17-105">Skambučių centre naudodami produktų katalogus galite identifikuoti produktus, kuriuos norite siūlyti klientams.</span><span class="sxs-lookup"><span data-stu-id="dcc17-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="dcc17-106">Skambučių centruose paprastai naudojami spausdinti katalogai.</span><span class="sxs-lookup"><span data-stu-id="dcc17-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="dcc17-107">Spausdintas katalogas maketuojamas ir tvarkomas ne „Dynamics 365 for Retail“.</span><span class="sxs-lookup"><span data-stu-id="dcc17-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="dcc17-108">Tačiau galite kurti ir saugoti katalogą skaitmenine forma naudodami tuos pačius puslapius, kuriuos naudojate interneto mažmeninės prekybos katalogams nustatyti.</span><span class="sxs-lookup"><span data-stu-id="dcc17-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="dcc17-109">Prieš kuriant katalogą, reikia nustatyti produktų asortimentus ir priskirti juos skambučių centrui.</span><span class="sxs-lookup"><span data-stu-id="dcc17-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="dcc17-110">Tada įtraukite produktų į katalogą rinkdamiesi juos iš asortimentų.</span><span class="sxs-lookup"><span data-stu-id="dcc17-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="dcc17-111">Įtraukus produktų į katalogą ir baigus katalogą, reikia patikrinti duomenis tikrinant katalogą.</span><span class="sxs-lookup"><span data-stu-id="dcc17-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="dcc17-112">Tada reikia pateikti katalogą peržiūrai ir patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="dcc17-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="dcc17-113">Kai katalogas patvirtintas, jis gali būti publikuojamas.</span><span class="sxs-lookup"><span data-stu-id="dcc17-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="dcc17-114">Sukūrę skambučių centro katalogą, galite padaryti momentinę katalogo duomenų nuotrauką, kai katalogas publikuojamas.</span><span class="sxs-lookup"><span data-stu-id="dcc17-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="dcc17-115">Ši momentinės kopijos funkcija suteikia galimybę pasiekti konkrečią katalogo versiją, net jei vėliau katalogas pakeičiamas ir atnaujinamas.</span><span class="sxs-lookup"><span data-stu-id="dcc17-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="dcc17-116">Be to, skambučių centro katalogus galima nustatyti taip, kad juose būtų šios pasirinktinės funkcijos:</span><span class="sxs-lookup"><span data-stu-id="dcc17-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="dcc17-117">**Šaltinio kodai**– šaltinio kodai naudojami klientų atsakui į konkrečius katalogų laiškus sekti.</span><span class="sxs-lookup"><span data-stu-id="dcc17-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="dcc17-118">**Nemokami produktai** – produktai gali būti įtraukti į kliento užsakymą be papildomo mokesčio.</span><span class="sxs-lookup"><span data-stu-id="dcc17-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="dcc17-119">Šie produktai automatiškai įtraukiami į užsakymą, kai užsakyme įvedamas katalogo šaltinio kodas.</span><span class="sxs-lookup"><span data-stu-id="dcc17-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="dcc17-120">**Scenarijai** – scenarijai yra tekstai, kuriuos skambučių centro darbuotojas skaito klientui, kai kuriamas pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="dcc17-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="dcc17-121">Scenarijai gali apimti sveikinimus arba pasiūlymus pirkti.</span><span class="sxs-lookup"><span data-stu-id="dcc17-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="dcc17-122">**Puslapio maketas** – puslapio maketas fiksuoja spausdintame kataloge esančių produktų padėtį puslapyje.</span><span class="sxs-lookup"><span data-stu-id="dcc17-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="dcc17-123">Ši informacija naudojama katalogo srities analizės ataskaitai.</span><span class="sxs-lookup"><span data-stu-id="dcc17-123">This information is used for the catalog area analysis report.</span></span>





