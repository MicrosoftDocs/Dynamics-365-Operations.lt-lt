---
title: "Integravimas su „Microsoft Dynamics 365 for Field Service“"
description: "Šioje temoje pateikiama integravimo su „Microsoft Dynamics 365 for Field Service“ apžvalga."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d32a4e376770fc73c79b94924d5ae062d201d84a
ms.openlocfilehash: a224962152e80293f6cf3425dea74d73a283e31a
ms.contentlocale: lt-lt
ms.lasthandoff: 04/12/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="69c67-103">Integravimas su „Microsoft Dynamics 365 for Field Service“</span><span class="sxs-lookup"><span data-stu-id="69c67-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="69c67-104">„Microsoft Dynamics 365 for Finance and Operations“ leidžia sinchronizuoti verslo procesus tarp „Finance and Operations“ ir „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="69c67-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="69c67-105">Integravimo scenarijai sukonfigūruojami naudojant išplečiamuosius duomenų integratoriaus šablonus ir „Common Data Service“ (CDS), kad būtų galima sinchronizuoti verslo procesus.</span><span class="sxs-lookup"><span data-stu-id="69c67-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="69c67-106">[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="69c67-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="69c67-107">Pirmasis integravimo tarp „Field Service“ ir „Finance and Operations“ etapas orientuotas į darbo užsakymų ir sutarčių įgalinimą „Field Service“, kad „Finance and Operations“ būtų galima išrašyti SF.</span><span class="sxs-lookup"><span data-stu-id="69c67-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="69c67-108">Palaikomas srautas pradedamas „Field Service“, kai darbo užsakymų informacija su „Finance and Operations“ sinchronizuojama kaip pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="69c67-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="69c67-109">Programoje „Finance and Operations“ pardavimo užsakymams išrašomos SF, kad būtų sugeneruoti SF dokumentai.</span><span class="sxs-lookup"><span data-stu-id="69c67-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="69c67-110">Be to, „Field Service“ pateikiama sutarčių SF informacija sinchronizuojama su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="69c67-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="69c67-111">„Microsoft Dynamics 365“ duomenų integratorius sinchronizuoja duomenis panaudodamas pritaikomus projektus.</span><span class="sxs-lookup"><span data-stu-id="69c67-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="69c67-112">Standartiniai šablonai gali būti naudojami, siekiant sukurti pasirinktinius integravimo projektus, kuriuose papildomus standartinius ir pasirinktinius laukus bei objektus būtų galima susieti norint pakoreguoti integravimą ir atitikti specifinius reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="69c67-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="69c67-113">Pirmame integravimo tarp „Field Service“ ir „Finance and Operations“ etape galima sinchronizuoti toliau nurodytus elementus elementus.</span><span class="sxs-lookup"><span data-stu-id="69c67-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="69c67-114">„Finance and Operations“ produktus su „Field Service“ produktais, kuriuose pateikiama produkto tipo informacija</span><span class="sxs-lookup"><span data-stu-id="69c67-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="69c67-115">„Field Service“ darbo užsakymus su „Finance and Operations“ pardavimo užsakymais</span><span class="sxs-lookup"><span data-stu-id="69c67-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="69c67-116">„Field Service“ SF su „Finance and Operations“ laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="69c67-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="69c67-117">„Finance and Operations“ sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="69c67-117">System requirements for Finance and Operations</span></span>
<span data-ttu-id="69c67-118">„Field Service“ integravimas palaikomas toliau nurodytose versijose.</span><span class="sxs-lookup"><span data-stu-id="69c67-118">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="69c67-119">„Dynamics 365 for Finance and Operations‟ 8.0 (2018 m. balandžio mėn.) ar naujesnėje versijoje</span><span class="sxs-lookup"><span data-stu-id="69c67-119">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="69c67-120">„Dynamics 365 for Finance and Operations“ 8.0 (2018 m. balandžio mėn.) versija buvo išleista 2018 m. balandį. Programos versijos numeris – 8.0.30.8020 su 15 platformos naujinimu (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="69c67-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="69c67-121">„Field Service“ sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="69c67-121">System requirements for Field Service</span></span>
<span data-ttu-id="69c67-122">Norėdami naudoti sprendimą „Field Service“, turite įdiegti toliau nurodytus komponentus.</span><span class="sxs-lookup"><span data-stu-id="69c67-122">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="69c67-123">„Microsoft Dynamics 365 for Field Service“ 9.0 arba naujesnę versiją</span><span class="sxs-lookup"><span data-stu-id="69c67-123">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="69c67-124">„Dynamics 365 for Field Service“ 1612 versiją (9.0.1.733) (DB 9.0.1.733) internete arba naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="69c67-124">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="69c67-125">„Dynamics 365“ skirtą sprendimą „Potencialūs klientai ir grynieji pinigai“ (P2C), 1.15.0.1 arba naujesnė versija.</span><span class="sxs-lookup"><span data-stu-id="69c67-125">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="69c67-126">Sprendimą galima atsisiųsti iš [„AppSource“](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="69c67-126">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="69c67-127">„Dynamics 365“ skirtas „Field Service“ integravimo sprendimas, 1.0.0.0 arba naujesnė versija.</span><span class="sxs-lookup"><span data-stu-id="69c67-127">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="69c67-128">Sprendimą galima atsisiųsti iš „AppSource“.</span><span class="sxs-lookup"><span data-stu-id="69c67-128">The solution is available for download from AppSource.</span></span> <span data-ttu-id="69c67-129">**(LAUKIAMA LEIDIMO)**</span><span class="sxs-lookup"><span data-stu-id="69c67-129">**(PENDING RELEASE)**</span></span>

