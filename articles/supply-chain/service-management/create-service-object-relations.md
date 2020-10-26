---
title: Aptarnavimo objekto ryšių kūrimas
description: Šioje temoje aprašoma, kaip sukurti aptarnavimo objekto ryšius aptarnavimo sutarčiai ir aptarnavimo užsakymui.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 352d3b790da340102b7dbe116d9deeb2f3cbfc4e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985974"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="81c09-103">Aptarnavimo objekto ryšių kūrimas</span><span class="sxs-lookup"><span data-stu-id="81c09-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="81c09-104">Šioje temoje aprašoma, kaip sukurti aptarnavimo objekto ryšius aptarnavimo sutarčiai ir aptarnavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="81c09-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="81c09-105">Kurdami aptarnavimo objekto ryšį, aptarnavimo objektą susiejate su aptarnavimo sutartimi arba aptarnavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="81c09-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="81c09-106">Kai klientas pateikia prekės, kuri yra aptarnavimo objektas, aptarnavimo užklausą, galite pasirinkti aptarnavimo objektą iš aptarnavimo objekto ryšių sąrašo.</span><span class="sxs-lookup"><span data-stu-id="81c09-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="81c09-107">Aptarnavimo objekto ryšio kūrimas aptarnavimo sutarčiai</span><span class="sxs-lookup"><span data-stu-id="81c09-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="81c09-108">Norėdami sukurti aptarnavimo objekto ryšį aptarnavimo sutarčiai, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="81c09-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="81c09-109">Spustelėkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="81c09-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="81c09-110">Sąraše **Aptarnavimo sutartys** pasirinkite esamą aptarnavimo sutartį arba spustelėkite **Nauja** norėdami sukurti naują aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="81c09-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="81c09-111">Formos **Aptarnavimo sutartys**, esančios **Veiksmų sritis**, skirtuko **Aptarnavimo sutartis** grupėje **Ryšiai** spustelėkite **Aptarnavimo objektai**.</span><span class="sxs-lookup"><span data-stu-id="81c09-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="81c09-112">Formoje **Aptarnavimo objektai** spustelėkite **Naujas** ir pasirinkite šios aptarnavimo sutarties aptarnavimo objektą.</span><span class="sxs-lookup"><span data-stu-id="81c09-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="81c09-113">Norėdami priskirti šabloninę komplektavimo specifikaciją (KS) aptarnavimo sutarčiai, spustelėkite **Funkcijos**, tada pasirinkite **Pridėti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="81c09-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="81c09-114">Formos **Pasirinkti šabloninę KS** lauke **Šabloninė KS** pasirinkite šabloną.</span><span class="sxs-lookup"><span data-stu-id="81c09-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="81c09-115">Aptarnavimo objekto ryšio kūrimas aptarnavimo užsakymui</span><span class="sxs-lookup"><span data-stu-id="81c09-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="81c09-116">Norėdami sukurti aptarnavimo objekto ryšį aptarnavimo užsakymui, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="81c09-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="81c09-117">Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="81c09-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="81c09-118">Sąraše **Aptarnavimo užsakymai** pasirinkite esamą aptarnavimo užsakymą arba sukurkite naują aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="81c09-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="81c09-119">Formos **Aptarnavimo užsakymai**, esančios **Veiksmų sritis**, skirtuko **Aptarnavimo užsakymas** grupėje **Ryšiai** spustelėkite **Aptarnavimo objektai**.</span><span class="sxs-lookup"><span data-stu-id="81c09-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="81c09-120">Formoje **Aptarnavimo objektai** spustelėkite **Naujas** ir pasirinkite šio aptarnavimo užsakymo aptarnavimo objektą.</span><span class="sxs-lookup"><span data-stu-id="81c09-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="81c09-121">Norėdami priskirti šabloninę KS aptarnavimo sutarčiai, spustelėkite **Funkcijos**, tada pasirinkite **Pridėti šabloninę KS**.</span><span class="sxs-lookup"><span data-stu-id="81c09-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="81c09-122">Formos **Pasirinkti šabloninę KS** lauke **Šabloninė KS** pasirinkite šabloną.</span><span class="sxs-lookup"><span data-stu-id="81c09-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="81c09-123">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="81c09-123">See also</span></span>

[<span data-ttu-id="81c09-124">Aptarnavimo objektų apžvalga</span><span class="sxs-lookup"><span data-stu-id="81c09-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="81c09-125">Aptarnavimo objekto ryšiai</span><span class="sxs-lookup"><span data-stu-id="81c09-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="81c09-126">Šabloninės KS</span><span class="sxs-lookup"><span data-stu-id="81c09-126">Template BOMs</span></span>](template-boms.md)

  


