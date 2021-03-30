---
title: Aptarnavimo užsakymo prekių poreikiai
description: Jei aptarnavimo užsakymui reikia rezervuoti konkrečių prekių, galite jam sukurti atsargų prekių poreikių.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a0ce40c26e3d3028064b73a80a247180d6a9009
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226670"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="db726-103">Aptarnavimo užsakymo prekių poreikiai</span><span class="sxs-lookup"><span data-stu-id="db726-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="db726-104">Galite kurti aptarnavimo užsakymą, jei norite sekti ir valdyti klientams teikiamas paslaugas.</span><span class="sxs-lookup"><span data-stu-id="db726-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="db726-105">Jei aptarnavimo užsakymui reikia rezervuoti konkrečių prekių, galite jam sukurti atsargų prekių poreikių.</span><span class="sxs-lookup"><span data-stu-id="db726-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="db726-106">Prekės poreikį galima nedelsiant panaudoti iš atsargų, arba jis gali inicijuoti tos prekės gamybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="db726-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="db726-107">Naudodami prekės poreikį vietoje prekės operacijos, galite planuoti pristatymą prieš faktiškai naudojant prekę, kurti pirkimo užsakymą, įtraukti prekę į prekybos sutarties sistemą bei įtraukti prekės poreikį į gamybos planavimą.</span><span class="sxs-lookup"><span data-stu-id="db726-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="db726-108">Prekės poreikiai aptarnavimo užsakymuose apdorojami vykdant projektą.</span><span class="sxs-lookup"><span data-stu-id="db726-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="db726-109">Norint sukurti prekės poreikį aptarnavimo užsakyme, aptarnavimo užsakymą reikia pridėti prie projekto.</span><span class="sxs-lookup"><span data-stu-id="db726-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="db726-110">Kai tik sukuriamas aptarnavimo užsakymo prekės poreikis, jį galima peržiūrėti atskiro aptarnavimo užsakymo srityje **Projektas** arba naudojant formą **Pardavimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="db726-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="db726-111">Prekės poreikio pagal aptarnavimo užsakymą peržiūra</span><span class="sxs-lookup"><span data-stu-id="db726-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="db726-112">Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="db726-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="db726-113">Spustelėkite **Išsiųsti**, po to spustelėję **Prekės poreikis** atidarykite formą **Prekių poreikiai**.</span><span class="sxs-lookup"><span data-stu-id="db726-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="db726-114">Spustelėkite skirtuką **Projektas** ir lauke **Aptarnavimo užsakymas** peržiūrėkite prekės poreikio aptarnavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="db726-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="db726-115">Aptarnavimo užsakymų su prekių poreikiais naikinimas</span><span class="sxs-lookup"><span data-stu-id="db726-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="db726-116">Jei prekės poreikis sukurtas aptarnavimo užsakyme, jūs negalite naikinti aptarnavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="db726-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="db726-117">Norėdami naikinti aptarnavimo užsakymą, turite panaikinti prekės poreikį.</span><span class="sxs-lookup"><span data-stu-id="db726-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="db726-118">Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="db726-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="db726-119">Spustelėkite **Išsiųsti**, po to spustelėję **Prekės poreikis** atidarykite formą **Prekių poreikiai**.</span><span class="sxs-lookup"><span data-stu-id="db726-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="db726-120">Šioje formoje išvardyti visi prekių poreikiai, sukurti aptarnavimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="db726-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="db726-121">Pasirinkite norimą naikinti prekės poreikį ir spustelėkite **Naikinti**..</span><span class="sxs-lookup"><span data-stu-id="db726-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="db726-122">arba,</span><span class="sxs-lookup"><span data-stu-id="db726-122">–or–</span></span>

1.  <span data-ttu-id="db726-123">Spustelėkite **Projektų valdymas ir apskaita** \> **Bendra** \> **Projektai** \> **Visi projektai**.</span><span class="sxs-lookup"><span data-stu-id="db726-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="db726-124">Atidarykite projektą su aptarnavimo užsakymu, kuriame sukurtas prekės poreikis.</span><span class="sxs-lookup"><span data-stu-id="db726-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="db726-125">Dešinėje srityje esančioje formoje **Projektai** spustelėkite **Prekių poreikiai**.</span><span class="sxs-lookup"><span data-stu-id="db726-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="db726-126">Formoje **Prekių poreikiai** pateikiami su pasirinktu projektu susieti prekių poreikiai.</span><span class="sxs-lookup"><span data-stu-id="db726-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="db726-127">Pasirinkite norimą naikinti prekės poreikį ir spustelėkite **Naikinti**..</span><span class="sxs-lookup"><span data-stu-id="db726-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="db726-128">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="db726-128">See also</span></span>

<span data-ttu-id="db726-129">[Prekių poreikiai (forma)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="db726-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]