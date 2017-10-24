---
title: "Valdyti parduotuvės atsargas"
description: "Šiame straipsnyje aprašyti dokumentų, kuriuos galite naudoti atsargoms valdyti, tipai."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1fd37bcd7155c61492f5f4990685203ea97bca36
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="manage-store-inventory"></a><span data-ttu-id="92ad8-103">Valdyti parduotuvės atsargas</span><span class="sxs-lookup"><span data-stu-id="92ad8-103">Manage store inventory</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="92ad8-104">Šiame straipsnyje aprašyti dokumentų, kuriuos galite naudoti atsargoms valdyti, tipai.</span><span class="sxs-lookup"><span data-stu-id="92ad8-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="92ad8-105">Valdyti savo organizacijos atsargoms galite naudoti tolesnius dokumentų tipus.</span><span class="sxs-lookup"><span data-stu-id="92ad8-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="92ad8-106">Pirkimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="92ad8-106">Purchase orders</span></span>
<span data-ttu-id="92ad8-107">Pirkimo užsakymai kuriami pagrindiniame biure.</span><span class="sxs-lookup"><span data-stu-id="92ad8-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="92ad8-108">Jei mažmeninės prekybos sandėlis įtrauktas į pirkimo užsakymo antraštę, užsakymą parduotuvėje galima gauti naudojant modernų EKA (MPOS) arba debesies EKA, esančius programoje „Microsoft Dynamics 365 for Retail“.</span><span class="sxs-lookup"><span data-stu-id="92ad8-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="92ad8-109">Kai parduotuvės pageidauti kiekiai įvedami, juos galima įrašyti vietoje ir papildomai modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="92ad8-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="92ad8-110">Taip pat kiekiai gali būti fiksuojami ir siunčiami į pagrindinį biurą.</span><span class="sxs-lookup"><span data-stu-id="92ad8-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="92ad8-111">Pagrindiniame biure parduotuvėje gauti kiekiai rodomi programoje „Dynamics 365 for Retail“, pirkimo užsakymo lauke **Gauti dabar**.</span><span class="sxs-lookup"><span data-stu-id="92ad8-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="92ad8-112">Perkėlimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="92ad8-112">Transfer orders</span></span>
<span data-ttu-id="92ad8-113">Perkėlimo užsakyme galima nurodyti, kad tam tikra parduotuvė yra vieta, iš kurios gali būti siunčiamos prekės.</span><span class="sxs-lookup"><span data-stu-id="92ad8-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="92ad8-114">Šiuo atveju perkėlimo užsakymas parduotuvėje rodomas kaip MPOS arba debesies EKA paėmimo užklausa.</span><span class="sxs-lookup"><span data-stu-id="92ad8-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="92ad8-115">Kai pageidauti kiekiai paimami, jie fiksuojami ir siunčiami į pagrindinį biurą.</span><span class="sxs-lookup"><span data-stu-id="92ad8-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="92ad8-116">Pagrindiniame biure parduotuvėje paimti kiekiai rodomi programoje „Dynamics 365 for Retail‟, perkėlimo užsakymo lauke **Siųsti dabar**.</span><span class="sxs-lookup"><span data-stu-id="92ad8-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="92ad8-117">Perkėlimo užsakyme galima nurodyti, kad tam tikra parduotuvė yra vieta, į kurią gali būti siunčiamos prekės.</span><span class="sxs-lookup"><span data-stu-id="92ad8-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="92ad8-118">Šiuo atveju perkėlimo užsakymas parduotuvėje rodomas kaip MPOS arba debesies EKA gavimo užklausa.</span><span class="sxs-lookup"><span data-stu-id="92ad8-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="92ad8-119">Kai parduotuvės pageidauti kiekiai įvedami, juos galima įrašyti vietoje ir papildomai modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="92ad8-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="92ad8-120">Taip pat kiekiai gali būti fiksuojami ir siunčiami į pagrindinį biurą.</span><span class="sxs-lookup"><span data-stu-id="92ad8-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="92ad8-121">Pagrindiniame biure parduotuvėje gauti kiekiai rodomi programoje „Dynamics 365 for Retail“, perkėlimo užsakymo lauke **Gauti dabar**.</span><span class="sxs-lookup"><span data-stu-id="92ad8-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="92ad8-122">Inventorizacijos</span><span class="sxs-lookup"><span data-stu-id="92ad8-122">Stock counts</span></span>
<span data-ttu-id="92ad8-123">Inventorizacijos gali būti planinės arba neplaninės.</span><span class="sxs-lookup"><span data-stu-id="92ad8-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="92ad8-124">Planinės inventorizacijos inicijuojamos pagrindiniame biure, kuris nurodo, kurias prekes reikia skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="92ad8-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="92ad8-125">Pagrindinis biuras sukuria inventorizavimo dokumentą, kurį galima gauti parduotuvėje, kurioje faktinių turimų atsargų kiekiai įvedami į MPOS arba debesies EKA.</span><span class="sxs-lookup"><span data-stu-id="92ad8-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="92ad8-126">Neplaninės inventorizacijos inicijuojamos parduotuvėje, o faktinių turimų atsargų kiekiai atnaujinami MPOS arba debesies EKA.</span><span class="sxs-lookup"><span data-stu-id="92ad8-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="92ad8-127">Skirtingai nei planinės inventorizacijos, neplaninės inventorizacijos neturi iš anksto apibrėžto prekių sąrašo.</span><span class="sxs-lookup"><span data-stu-id="92ad8-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="92ad8-128">Alikus bet kurio tipo inventorizaciją, ji fiksuojama ir siunčiama į pagrindinį biurą.</span><span class="sxs-lookup"><span data-stu-id="92ad8-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="92ad8-129">Pagrindiniame biure inventorizacija patikrinama ir registruojama.</span><span class="sxs-lookup"><span data-stu-id="92ad8-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="92ad8-130">Atsargų peržvalga</span><span class="sxs-lookup"><span data-stu-id="92ad8-130">Inventory lookup</span></span>
<span data-ttu-id="92ad8-131">Dabar keliose parduotuvėse ir sandėliuose turimą produktų kiekį galima peržiūrėti atsargų peržvalgos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="92ad8-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="92ad8-132">Neskaitant dabartinio turimo kiekio, galima pamatyti kiekvienos atskiros parduotuvės būsimus prieinamų atsargų (ATP) kiekius.</span><span class="sxs-lookup"><span data-stu-id="92ad8-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="92ad8-133">Norėdami tai padaryti pasirinkite parduotuvę, kurios ATP norite peržiūrėti, ir tada spustelėkite **Rodyti parduotuvės pasiekiamumą**.</span><span class="sxs-lookup"><span data-stu-id="92ad8-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





