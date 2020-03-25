---
title: Pavojingos medžiagos
description: Šioje temoje pateikiama informacija apie pavojingos medžiagos dokumentus ir informaciją, saugomą jūsų aplinkoje.
author: lachlancashMS
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 443d2eb545b2b7592e27ae037009720db0a71997
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092550"
---
# <a name="hazardous-materials"></a><span data-ttu-id="0add3-103">Pavojingos medžiagos</span><span class="sxs-lookup"><span data-stu-id="0add3-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0add3-104">Informacija apie pavojingas medžiagas nustatoma produkto informacijos valdyme.</span><span class="sxs-lookup"><span data-stu-id="0add3-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="0add3-105">Be to, šiame modulyje pateikiami dokumentai, kuriuos galima atspausdinti per sandėlio valdymą.</span><span class="sxs-lookup"><span data-stu-id="0add3-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="0add3-106">Kai siunčiate medžiagas, kurios klasifikuojamos kaip pavojingos prekės, prie siuntų turi būti pridėti papildomi dokumentai.</span><span class="sxs-lookup"><span data-stu-id="0add3-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="0add3-107">Pavojingų medžiagų funkcijose klientai gali išsaugoti klasifikacijos informaciją ir susieti ją su leidimo prekėmis.</span><span class="sxs-lookup"><span data-stu-id="0add3-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="0add3-108">Ši informacija gali būti naudojama ruošiant siuntimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="0add3-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0add3-109">Kad būtų lengviau tvarkyti pavojingų prekių siuntas, „Microsoft Dynamics 365 Supply Chain Management“ galite nustatyti papildomą nuorodos informaciją, susijusią su produktais.</span><span class="sxs-lookup"><span data-stu-id="0add3-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="0add3-110">Taip pat galite nustatyti papildomus siuntos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="0add3-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="0add3-111">Tačiau sistema automatiškai neatitinka jūsų šalies arba regiono nuostatų.</span><span class="sxs-lookup"><span data-stu-id="0add3-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="0add3-112">Tai priemonė, kuri gali būti naudinga jūsų bendrajai programai.</span><span class="sxs-lookup"><span data-stu-id="0add3-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="0add3-113">Kad galėtumėte naudoti šią funkciją, reikia nustatyti šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="0add3-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="0add3-114">**Produkto informacijos valdymas:** nustatykite kodus, kurie gali būti taikomi išleistoms prekėms.</span><span class="sxs-lookup"><span data-stu-id="0add3-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="0add3-115">**Sandėlio valdymas:** norėdami spausdinti siuntimo informaciją, naudokite papildomus siuntimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="0add3-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="0add3-116">Produkto informacijos valdymas</span><span class="sxs-lookup"><span data-stu-id="0add3-116">Product information management</span></span>

<span data-ttu-id="0add3-117">Produkto informacijos valdyme yra sąrankos lentelių, kuriose galite pridėti nuorodos informaciją, pateikiamą pavojingų prekių sąrašuose, skirtuose kelių, oro ir jūrų transportui.</span><span class="sxs-lookup"><span data-stu-id="0add3-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="0add3-118">Čia pateiktos kai kurios dažnai nurodomos nuostatos:</span><span class="sxs-lookup"><span data-stu-id="0add3-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="0add3-119">**ADR** – nuostatos, susijusios su tarptautiniu pavojingų krovinių vežimu keliais</span><span class="sxs-lookup"><span data-stu-id="0add3-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="0add3-120">**CFR 49** – pavojingų prekių gabenimo Jungtinėse Valstijose nuostatos</span><span class="sxs-lookup"><span data-stu-id="0add3-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="0add3-121">**IMDG** – Tarptautinis pavojingų krovinių vežimo jūra (IMDG) kodeksas</span><span class="sxs-lookup"><span data-stu-id="0add3-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="0add3-122">**IATA** – Tarptautinės oro transporto asociacijos (IATA) pavojingų prekių gabenimo nuostatos</span><span class="sxs-lookup"><span data-stu-id="0add3-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="0add3-123">Kiekviena iš šių nuostatų turi pavojingų prekių sąrašą, kuriame pateikiami nuorodų kodai.</span><span class="sxs-lookup"><span data-stu-id="0add3-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="0add3-124">Kiekvienos transportavimo rūšies sąrašai sujungiami į bendrai naudojamas tarptautines klasifikacijas.</span><span class="sxs-lookup"><span data-stu-id="0add3-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="0add3-125">„Supply Chain Management“ pateikia tų sąrašų bendrai naudojamų kodų nuorodų lentelę.</span><span class="sxs-lookup"><span data-stu-id="0add3-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="0add3-126">Kiekviename sąraše taip pat yra keli unikalūs kodai, kuriuos galima apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="0add3-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="0add3-127">Norėdami pirmiausia konfigūruoti šią informaciją, sukurkite nuostatą, kurią galėtumėte naudoti pradiniams parametrams konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="0add3-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="0add3-128">Sandėlio valdymas</span><span class="sxs-lookup"><span data-stu-id="0add3-128">Warehouse management</span></span>

<span data-ttu-id="0add3-129">Kai ruošiama siunta, galima atspausdinti kelias naujas ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="0add3-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="0add3-130">Šiose ataskaitose naudojama informacija, nustatyta produkto informacijos valdyme.</span><span class="sxs-lookup"><span data-stu-id="0add3-130">These reports use the information that you set up in Product information management.</span></span>
