---
title: Pavojingų medžiagų apžvalga
description: Šioje temoje pateikiama funkcijų, susijusių su pavojingų medžiagų tvarkymu ir fiksavimu produkto informacijos valdymo ir sandėlio valdymo metu, apžvalga.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 227111f4703d9dc381270382dcb796874d7de937
ms.sourcegitcommit: c009ec75f53872272f11c92a1ce81a391e3845a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/18/2020
ms.locfileid: "3699641"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="be62a-103">Pavojingų medžiagų apžvalga</span><span class="sxs-lookup"><span data-stu-id="be62a-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be62a-104">Jog atitiktų siuntimo ir transportavimo nuostatas, organizacijos, siunčiančios medžiagas, klasifikuojamas kaip pavojingos prekės, į savo siuntas privalo įtraukti papildomus popierinius dokumentus.</span><span class="sxs-lookup"><span data-stu-id="be62a-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="be62a-105">Pavojingų medžiagų funkcija leidžia klientams saugoti informaciją, susijusią su paleistomis prekėmis.</span><span class="sxs-lookup"><span data-stu-id="be62a-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="be62a-106">Ši informacija gali būti naudojama ruošiant siuntimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="be62a-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="be62a-107">Organizacija, siunčianti pavojingas prekes, privalo turėti savo siuntimo proceso valdymo procesus ir procedūras.</span><span class="sxs-lookup"><span data-stu-id="be62a-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="be62a-108">„Microsoft Dynamics 365 Supply Chain Management” yra tik įrankis, galintis padėti generuoti reikalingus dokumentus.</span><span class="sxs-lookup"><span data-stu-id="be62a-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="be62a-109">Ši diagrama iliustruoja veiksmus, reikalingus pavojingų medžiagų funkcijos nustatymui ir naudojimui.</span><span class="sxs-lookup"><span data-stu-id="be62a-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="be62a-110">![Pavojingų medžiagos funkcijos nustatymas ir naudojimas](media/hazmat-overview.png "Pavojingų medžiagų funkcijos nustatymas ir naudojimas")</span><span class="sxs-lookup"><span data-stu-id="be62a-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="be62a-111">Pavojingų medžiagų funkcija yra nustatoma Produkto informacijos valdyme ir pateikia dokumentus, kuriuos galima atsispaudinti per Sandėlio valdymą.</span><span class="sxs-lookup"><span data-stu-id="be62a-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="be62a-112">Taigi, apskritai kalbant, minėtos sritys yra dvi pagrindinės sritys, kuriose Jūs peržiūrėsite, nustatysite ir naudosite šią funkciją:</span><span class="sxs-lookup"><span data-stu-id="be62a-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="be62a-113">**Produkto informacijos valdymas** – nustatyti kodus, kurie bus taikomi išleistam produktui.</span><span class="sxs-lookup"><span data-stu-id="be62a-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="be62a-114">**Sandėlio valdymas** – darbas su papildomais dokumentais, kurie bus atspausdinti siuntoms.</span><span class="sxs-lookup"><span data-stu-id="be62a-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be62a-115">Pavojingų medžiagų funkcijos Supply Chain Management suteikia naudingų produkto informacijos laukų kolekciją ir susijusią funkciją, galinčią padėti Jums įrašyti ir nurodyti informaciją, susijusią su Jūsų pavojingais produktais.</span><span class="sxs-lookup"><span data-stu-id="be62a-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="be62a-116">Šios funkcijos taip pat gali padėti jums kurti ir spausdinti siuntimo dokumentus, kuriuose yra tam tikra informacija apie bet kokias pavojingas medžiagas, kurias siunčiate.</span><span class="sxs-lookup"><span data-stu-id="be62a-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="be62a-117">Tačiau sistema automatiškai neatitiks visų nuostatų, taikomų jūsų šalyje arba regione.</span><span class="sxs-lookup"><span data-stu-id="be62a-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="be62a-118">Nors šios priemonės skirtos tam, kad būtų lengviau laikytis bendrųjų nuostatų, jos nėra pakankamos ar garantuotos tokiomis būti.</span><span class="sxs-lookup"><span data-stu-id="be62a-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="be62a-119">Jūsų organizacija yra atsakinga už visų taikomų nuostatų žinojimą ir visų jų laikymuisi būtinų veiksmų atlikimą.</span><span class="sxs-lookup"><span data-stu-id="be62a-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="be62a-120">Produkto informacijos valdymas</span><span class="sxs-lookup"><span data-stu-id="be62a-120">Product information management</span></span>

<span data-ttu-id="be62a-121">Produkto informacijos valdymas pateikia nustatymo lentelių diapazoną, kuriame Jūs galite įvesti nuorodos informaciją apie įvairius pavojingų prekių sąrašus sausumos, oro ir jūros transportu.</span><span class="sxs-lookup"><span data-stu-id="be62a-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="be62a-122">Į šias bendrąsias nuostatas buvo atsižvelgta kuriant šią funkciją:</span><span class="sxs-lookup"><span data-stu-id="be62a-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="be62a-123">**ADR** – nuostatos, susijusios su tarptautiniu pavojingų krovinių vežimu keliais</span><span class="sxs-lookup"><span data-stu-id="be62a-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="be62a-124">**CFR 49** – pavojingų prekių gabenimo Jungtinėse Valstijose nuostatos</span><span class="sxs-lookup"><span data-stu-id="be62a-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="be62a-125">**IMDG** – Tarptautinis pavojingų krovinių vežimo jūra (IMDG) kodeksas</span><span class="sxs-lookup"><span data-stu-id="be62a-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="be62a-126">**IATA** – Tarptautinės oro transporto asociacijos (IATA) pavojingų prekių gabenimo nuostatos</span><span class="sxs-lookup"><span data-stu-id="be62a-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="be62a-127">Kiekvienas nuostatų rinkinys pateikia standartizuotus pavojingų prekių sąrašus ir nuorodų kodus.</span><span class="sxs-lookup"><span data-stu-id="be62a-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="be62a-128">Taigi, Supply Chain Management pateikia tų sąrašų bendrųjų kodų nuorodų lentelę.</span><span class="sxs-lookup"><span data-stu-id="be62a-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="be62a-129">Kiekvienas sąrašas turi kelius unikalius kodus, kuriuos Jūs galite apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="be62a-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="be62a-130">Daugiau informacijos apie tai, kaip nustatyti pavojingų medžiagų nuostatas ir reikšmes ir kaip priskirti reikšmes atitinkamiems produktams, žr. šias temas:</span><span class="sxs-lookup"><span data-stu-id="be62a-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="be62a-131">Pavojingų medžiagų nustatymas</span><span class="sxs-lookup"><span data-stu-id="be62a-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="be62a-132">Pavojingos medžiagos produktuose, siuntose ir kroviniuose</span><span class="sxs-lookup"><span data-stu-id="be62a-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="be62a-133">Sandėlio valdymas</span><span class="sxs-lookup"><span data-stu-id="be62a-133">Warehouse management</span></span>

<span data-ttu-id="be62a-134">Kai ruošite siuntą Sandėlio valdyme, galėsite atspaudinti kelias naujas ataskaitas, naudojančias informaciją, kurią nustatėte Produkto informacijos valdyme.</span><span class="sxs-lookup"><span data-stu-id="be62a-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="be62a-135">Norėdami gauti daugiau informacijos apie galimas ataskaitas ir kaip jas naudoti, žr. [Pavojingų medžiagų užklausos ir ataskaitos](hazmat-reports.md).</span><span class="sxs-lookup"><span data-stu-id="be62a-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>
