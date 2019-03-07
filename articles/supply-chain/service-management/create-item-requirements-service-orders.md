---
title: Prekės poreikių kūrimas pagal aptarnavimo užsakymus
description: Jei aptarnavimo užsakymui reikia rezervuoti konkrečių prekių, galite jam sukurti atsargų prekių poreikių.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5a730ae945af15c7bd4020c734bac971d8186e2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "312214"
---
# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="41fb0-103">Prekės poreikių kūrimas pagal aptarnavimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="41fb0-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="41fb0-104">Galite kurti aptarnavimo užsakymą, jei norite sekti ir valdyti klientams teikiamas paslaugas.</span><span class="sxs-lookup"><span data-stu-id="41fb0-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="41fb0-105">Jei aptarnavimo užsakymui reikia rezervuoti konkrečių prekių, galite jam sukurti atsargų prekių poreikių.</span><span class="sxs-lookup"><span data-stu-id="41fb0-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="41fb0-106">Prekės poreikį galima nedelsiant panaudoti iš atsargų, arba jis gali inicijuoti tos prekės gamybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="41fb0-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="41fb0-107">Naudodami prekės poreikį vietoje prekės operacijos, galite planuoti pristatymą prieš faktiškai naudojant prekę, kurti pirkimo užsakymą, įtraukti prekę į prekybos sutarties sistemą bei įtraukti prekės poreikį į gamybos planavimą.</span><span class="sxs-lookup"><span data-stu-id="41fb0-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="41fb0-108">Prekės poreikiai aptarnavimo užsakymuose apdorojami vykdant projektą.</span><span class="sxs-lookup"><span data-stu-id="41fb0-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="41fb0-109">Norint sukurti prekės poreikį aptarnavimo užsakyme, aptarnavimo užsakymą reikia priskirti prie projekto.</span><span class="sxs-lookup"><span data-stu-id="41fb0-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="41fb0-110">Kai sukuriate aptarnavimo užsakymo prekės poreikį, galite peržiūrėti prekės poreikį pasirinkto projekto formoje **Projektai**.</span><span class="sxs-lookup"><span data-stu-id="41fb0-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="41fb0-111">Prekės poreikio aptarnavimo užsakymui sukūrimas</span><span class="sxs-lookup"><span data-stu-id="41fb0-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="41fb0-112">Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="41fb0-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="41fb0-113">Pažymėkite aptarnavimo užsakymą, kuriam norite sukurti prekės poreikį.</span><span class="sxs-lookup"><span data-stu-id="41fb0-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="41fb0-114">Dalies **Veiksmų sritis** skirtuke **Išsiuntimas** spustelėkite **Prekės poreikis**.</span><span class="sxs-lookup"><span data-stu-id="41fb0-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="41fb0-115">Formoje **Prekių poreikis** įveskite reikiamos prekės informaciją.</span><span class="sxs-lookup"><span data-stu-id="41fb0-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="41fb0-116">Daugiau informacijos apie konkrečius laukus žr. [Prekių poreikis (forma)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="41fb0-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="41fb0-117">Prekės poreikio aptarnavimo sutarčiai sukūrimas</span><span class="sxs-lookup"><span data-stu-id="41fb0-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="41fb0-118">Spustelėkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="41fb0-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="41fb0-119">Atidarykite aptarnavimo sutartį, kuriai norite sukurti prekės poreikį.</span><span class="sxs-lookup"><span data-stu-id="41fb0-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="41fb0-120">„FastTab“ **Eilutės** spustelėję **Pridėti** sukursite naują eilutę.</span><span class="sxs-lookup"><span data-stu-id="41fb0-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="41fb0-121">Lauke **Operacijos tipas** pasirinkite **Prekė**.</span><span class="sxs-lookup"><span data-stu-id="41fb0-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="41fb0-122">Lauke **Prekių nustatymai** pasirinkite **Prekės poreikis**.</span><span class="sxs-lookup"><span data-stu-id="41fb0-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="41fb0-123">Lauke **Prekės numeris** pasirinkite prekę, kurios reikia aptarnavimo sutarčiai.</span><span class="sxs-lookup"><span data-stu-id="41fb0-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="41fb0-124">„FastTab“ **Eilutės informacija** skirtuko **Produktų dimensijos** lauke **Vieta** pasirinkite prekės atsargų vietą.</span><span class="sxs-lookup"><span data-stu-id="41fb0-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="41fb0-125">Norėdami kurti aptarnavimo užsakymą iš sutarties eilutės, „FastTab“ **Eilutės** spustelėkite **Kurti aptarnavimo užsakymus** ir įveskite atitinkamą informaciją formoje **Kurti aptarnavimo užsakymus**.</span><span class="sxs-lookup"><span data-stu-id="41fb0-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="41fb0-126">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="41fb0-126">See also</span></span>

<span data-ttu-id="41fb0-127">[Automatiškai kurti aptarnavimo užsakymus](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="41fb0-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  


