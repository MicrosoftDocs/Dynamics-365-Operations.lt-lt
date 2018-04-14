---
title: "Aptarnavimo šablonai"
description: "Galite apibrėžti aptarnavimo sutartį kaip šabloną ir vėliau nukopijuoti šablono eilutes į kitą aptarnavimo sutartį arba į kitą aptarnavimo užsakymą."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 24b7ffd18e6f69f497597eb12657d09f8d600dcf
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="service-templates"></a><span data-ttu-id="e9d99-103">Aptarnavimo šablonai</span><span class="sxs-lookup"><span data-stu-id="e9d99-103">Service templates</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="e9d99-104">Galite apibrėžti aptarnavimo sutartį kaip šabloną ir vėliau nukopijuoti šablono eilutes į kitą aptarnavimo sutartį arba į kitą aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="e9d99-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="e9d99-105">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e9d99-105">Example</span></span>

<span data-ttu-id="e9d99-106">Klientas, kuriam teikiate aptarnavimo paslaugas, turi vienodus krovininius liftus penkiose skirtingose vietose.</span><span class="sxs-lookup"><span data-stu-id="e9d99-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="e9d99-107">Norite klientui nustatyti penkias aptarnavimo sutartis, po vieną kiekvienai teritorijai.</span><span class="sxs-lookup"><span data-stu-id="e9d99-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="e9d99-108">Siekiant sumažinti pasikartojantį nustatymo darbą ir įsitikinti, kad nustatymo informacija aptarnavimo sutartyse yra identiška, sukuriate aptarnavimo sutartį ir nurodote ją, kaip liftų aptarnavimo darbo šabloną.</span><span class="sxs-lookup"><span data-stu-id="e9d99-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="e9d99-109">Dabar galite kopijuoti šablono eilutes į penkias naujas aptarnavimo sutartis taip, kad kiekviena aptarnavimo sutartis turėtų eilučių iš šablono.</span><span class="sxs-lookup"><span data-stu-id="e9d99-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="e9d99-110">Kurti šabloną</span><span class="sxs-lookup"><span data-stu-id="e9d99-110">Create a template</span></span>

<span data-ttu-id="e9d99-111">Kurdami aptarnavimo šabloną, sukuriate aptarnavimo sutartį, reikiamas eilutes joje ir pridedate aptarnavimo sutartį prie aptarnavimo šablono grupės.</span><span class="sxs-lookup"><span data-stu-id="e9d99-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="e9d99-112">Aptarnavimo sutartis gali būti apibrėžiama kaip šablonas tik tuo atveju, jei prie jos nėra prijungtų aptarnavimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="e9d99-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="e9d99-113">Taip pat iš aptarnavimo sutarties, kuri yra apibrėžta kaip šablonas, negalima sugeneruoti aptarnavimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="e9d99-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="e9d99-114">Kopijuoti šablono eilutes</span><span class="sxs-lookup"><span data-stu-id="e9d99-114">Copy template lines</span></span>

<span data-ttu-id="e9d99-115">Galite kopijuoti šablono eilutes iš aptarnavimo šablono į kitą aptarnavimo sutartį arba aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="e9d99-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="e9d99-116">Jums kopijuojant šablono eilutes į aptarnavimo užsakymus ar aptarnavimo sutartis, jūsų šablonų grupės rodomos medžio rodinyje, kuriame kiekviena grupė gali būti išplėsta.</span><span class="sxs-lookup"><span data-stu-id="e9d99-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="e9d99-117">Toks rodymo būdas leidžia jums peržiūrėti kiekvieną šabloną ir šablono eilutę.</span><span class="sxs-lookup"><span data-stu-id="e9d99-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="e9d99-118">Lengviau nustatyti, kurias aptarnavimo šablono eilutes norite kopijuoti, jei sugrupavote šablonus pagal pavadinimus, atspindinčius šablonų naudojimą.</span><span class="sxs-lookup"><span data-stu-id="e9d99-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9d99-119">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="e9d99-119">Related topics</span></span>

[<span data-ttu-id="e9d99-120">Aptarnavimo šablonų eilučių kopijavimas</span><span class="sxs-lookup"><span data-stu-id="e9d99-120">Copy service templates lines</span></span>](copy-service-template-lines.md)

