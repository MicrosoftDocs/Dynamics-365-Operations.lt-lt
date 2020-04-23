---
title: Darbo užsakymų iš priežiūros užklausų kūrimas
description: Šioje temoje paaiškinama, kaip sukurti darbo užsakymą iš priežiūros užklausos turto valdyme.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6bd98796140ab7aa3e7813ff1526413504554c5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205212"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="ab34a-103">Darbo užsakymų iš priežiūros užklausų kūrimas</span><span class="sxs-lookup"><span data-stu-id="ab34a-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="ab34a-104">Sukūrę priežiūros užklausas, galite lengvai jas konvertuoti į darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="ab34a-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="ab34a-105">Šioje temoje aprašomas greičiausias būdas dirbti su priežiūros užklausomis, atnaujinti kelias priežiūros užklausas vienu metu, o tada sukurti darbo užsakymą kelioms priežiūros užklausoms tuo pačiu metu.</span><span class="sxs-lookup"><span data-stu-id="ab34a-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="ab34a-106">Puslapiuose **Aktyvios priežiūros užklausos** arba **Mano funkcinės vietos priežiūros užklausos** galite vienu metu dirbti su viena priežiūros užklausa ir konvertuoti vieną priežiūros užklausą į darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ab34a-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="ab34a-107">Kiekviena priežiūros užklausa gali būti susijusi tik su vienu darbo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="ab34a-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="ab34a-108">Tačiau kelias priežiūros užklausas galima įtraukti į vieną darbo užsakymą, net jei priežiūros užklausos turi skirtingas lėšas.</span><span class="sxs-lookup"><span data-stu-id="ab34a-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="ab34a-109">Pasirinkite **Turto valdymas**\>**Bendra**\>**priežiūros užklausos**\>**Visos priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="ab34a-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="ab34a-110">Prieš kurdami darbo užsakymą pagal priežiūros užklausas, turite pasirinkti bent priežiūros užklausų priežiūros užduoties tipą, taip pat priežiūros užduoties tipo variantą ir prekybą, jei ši informacija yra aktuali.</span><span class="sxs-lookup"><span data-stu-id="ab34a-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="ab34a-111">Tinklelio rodinyje galite lengvai atnaujinti informaciją apie priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="ab34a-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="ab34a-112">Kai būsite pasirengę kurti darbo užsakymą, pasirinkite priežiūros užklausas, kurias į jį įtrauksite.</span><span class="sxs-lookup"><span data-stu-id="ab34a-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="ab34a-113">Jei pasirenkate kelias priežiūros užklausas, kurias konvertuosite į darbo užsakymą, prieš kurdami darbo užsakymą, turite nustatyti laukus **„Turtas“** ir **„Priežiūros užduoties tipas“**.</span><span class="sxs-lookup"><span data-stu-id="ab34a-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="ab34a-114">Jei pasirenkate vieną priežiūros užklausą, kurią konvertuosite į darbo užsakymą, prieš kurdami darbo užsakymą, turite nustatyti tik lauką **Turtas**.</span><span class="sxs-lookup"><span data-stu-id="ab34a-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="ab34a-115">Tačiau kurdami darbo užsakymą, dialogo lange **„Kurti darbo užsakymą“** galite pasirinkti priežiūros užduoties tipą (ir susijusį priežiūros užduoties tipo variantą ir prekybą, jei ši informacija yra aktuali).</span><span class="sxs-lookup"><span data-stu-id="ab34a-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="ab34a-116">Pasirinkite **„Darbo užsakymas“**.</span><span class="sxs-lookup"><span data-stu-id="ab34a-116">Select **Work order**.</span></span>
5. <span data-ttu-id="ab34a-117">Dialogo lange **„Kurti darbo užsakymą“** nustatykite laukus ir pasirinkite **„Gerai“**.</span><span class="sxs-lookup"><span data-stu-id="ab34a-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="ab34a-118">Pranešimo juosta gali įspėti, kad sukurtas naujas darbo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="ab34a-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="ab34a-119">Be to, kai sukuriate darbo užsakymą, pagrįstą priežiūros užklausa, jei su priežiūros užklausa susijęs turtas yra įtrauktas į garantijos sutartį, pranešimo juosta įspėja apie garantijos sutartį.</span><span class="sxs-lookup"><span data-stu-id="ab34a-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="ab34a-120">Pasirinkite **Turto valdymas** \> **Bendra** \> **Darbo užsakymai** \> **Darbo užsakymai** ir atidarykite naują darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ab34a-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![Naujo darbo užsakymo atidarymas](media/05-manage-maintenance-requests.png)

