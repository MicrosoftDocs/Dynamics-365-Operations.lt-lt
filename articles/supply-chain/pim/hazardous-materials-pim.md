---
title: Pavojingos medžiagos
description: Šioje temoje pateikiama informacija apie pavojingos medžiagos dokumentus ir informaciją, saugomą jūsų aplinkoje.
author: lachlancashMS
manager: tfehr
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
ms.openlocfilehash: 54e5dca38b31c9310d44bdda5f5af14ca1515541
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802706"
---
# <a name="hazardous-materials"></a><span data-ttu-id="a855c-103">Pavojingos medžiagos</span><span class="sxs-lookup"><span data-stu-id="a855c-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a855c-104">Informacija apie pavojingas medžiagas nustatoma produkto informacijos valdyme.</span><span class="sxs-lookup"><span data-stu-id="a855c-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="a855c-105">Be to, šiame modulyje pateikiami dokumentai, kuriuos galima atspausdinti per sandėlio valdymą.</span><span class="sxs-lookup"><span data-stu-id="a855c-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="a855c-106">Kai siunčiate medžiagas, kurios klasifikuojamos kaip pavojingos prekės, prie siuntų turi būti pridėti papildomi dokumentai.</span><span class="sxs-lookup"><span data-stu-id="a855c-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="a855c-107">Pavojingų medžiagų funkcijose klientai gali išsaugoti klasifikacijos informaciją ir susieti ją su leidimo prekėmis.</span><span class="sxs-lookup"><span data-stu-id="a855c-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="a855c-108">Ši informacija gali būti naudojama ruošiant siuntimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="a855c-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a855c-109">Pavojingų medžiagų funkcijos „Microsoft Dynamics 365 Supply Chain Management” teikia naudingų produkto informacijos laukų ir susijusių funkcijų kolekciją, kuri gali padėti jums įrašyti ir nurodyti informaciją, susijusią su pavojingais produktais.</span><span class="sxs-lookup"><span data-stu-id="a855c-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="a855c-110">Šios funkcijos taip pat gali padėti jums kurti ir spausdinti siuntimo dokumentus, kuriuose yra tam tikra informacija apie bet kokias pavojingas medžiagas, kurias siunčiate.</span><span class="sxs-lookup"><span data-stu-id="a855c-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="a855c-111">Tačiau sistema automatiškai neatitiks visų nuostatų, taikomų jūsų šalyje arba regione.</span><span class="sxs-lookup"><span data-stu-id="a855c-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="a855c-112">Nors šios priemonės skirtos tam, kad būtų lengviau laikytis bendrųjų nuostatų, jos nėra pakankamos ar garantuotos tokiomis būti.</span><span class="sxs-lookup"><span data-stu-id="a855c-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="a855c-113">Jūsų organizacija yra atsakinga už visų taikomų nuostatų žinojimą ir visų jų laikymuisi būtinų veiksmų atlikimą.</span><span class="sxs-lookup"><span data-stu-id="a855c-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="a855c-114">Kad galėtumėte naudoti šią funkciją, reikia nustatyti šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="a855c-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="a855c-115">**Produkto informacijos valdymas:** nustatykite kodus, kurie gali būti taikomi išleistoms prekėms.</span><span class="sxs-lookup"><span data-stu-id="a855c-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="a855c-116">**Sandėlio valdymas:** norėdami spausdinti siuntimo informaciją, naudokite papildomus siuntimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="a855c-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="a855c-117">Produkto informacijos valdymas</span><span class="sxs-lookup"><span data-stu-id="a855c-117">Product information management</span></span>

<span data-ttu-id="a855c-118">Produkto informacijos valdyme yra sąrankos lentelių, kuriose galite pridėti nuorodos informaciją, pateikiamą pavojingų prekių sąrašuose, skirtuose kelių, oro ir jūrų transportui.</span><span class="sxs-lookup"><span data-stu-id="a855c-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="a855c-119">Čia pateiktos kai kurios dažnai nurodomos nuostatos:</span><span class="sxs-lookup"><span data-stu-id="a855c-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="a855c-120">**ADR** – nuostatos, susijusios su tarptautiniu pavojingų krovinių vežimu keliais</span><span class="sxs-lookup"><span data-stu-id="a855c-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="a855c-121">**CFR 49** – pavojingų krovinių gabenimo Jungtinėse Valstijose nuostatos</span><span class="sxs-lookup"><span data-stu-id="a855c-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="a855c-122">**IMDG** – Tarptautinis jūra gabenamų pavojingų krovinių (IMDG) kodeksas</span><span class="sxs-lookup"><span data-stu-id="a855c-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="a855c-123">**IATA** – Tarptautinės oro transporto asociacijos (IATA) pavojingų prekių gabenimo nuostatos</span><span class="sxs-lookup"><span data-stu-id="a855c-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="a855c-124">Kiekviena iš šių nuostatų turi pavojingų prekių sąrašą, kuriame pateikiami nuorodų kodai.</span><span class="sxs-lookup"><span data-stu-id="a855c-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="a855c-125">Kiekvienos transportavimo rūšies sąrašai sujungiami į bendrai naudojamas tarptautines klasifikacijas.</span><span class="sxs-lookup"><span data-stu-id="a855c-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="a855c-126">„Supply Chain Management“ pateikia tų sąrašų bendrai naudojamų kodų nuorodų lentelę.</span><span class="sxs-lookup"><span data-stu-id="a855c-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="a855c-127">Kiekviename sąraše taip pat yra keli unikalūs kodai, kuriuos galima apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="a855c-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="a855c-128">Norėdami pirmiausia konfigūruoti šią informaciją, sukurkite nuostatą, kurią galėtumėte naudoti pradiniams parametrams konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="a855c-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="a855c-129">Sandėlio valdymas</span><span class="sxs-lookup"><span data-stu-id="a855c-129">Warehouse management</span></span>

<span data-ttu-id="a855c-130">Kai ruošiama siunta, galima atspausdinti kelias naujas ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="a855c-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="a855c-131">Šiose ataskaitose naudojama informacija, nustatyta produkto informacijos valdyme.</span><span class="sxs-lookup"><span data-stu-id="a855c-131">These reports use the information that you set up in Product information management.</span></span>
