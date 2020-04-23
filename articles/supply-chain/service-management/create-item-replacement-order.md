---
title: Prekės pakeitimo užsakymo kūrimas
description: Prekių pakeitimo užsakymai dažniausiai kuriami tada, kai produktas yra jau grąžintas ir patikrintas.
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b92c4400f2c852af49c78e9e94fdffa2e498b45c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202887"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="1e1c2-103">Prekės pakeitimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="1e1c2-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1e1c2-104">Prekių pakeitimo užsakymai dažniausiai kuriami tada, kai produktas yra jau grąžintas ir patikrintas.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="1e1c2-105">Tačiau, jei prekė turi būti pakeista anksčiau, nei ji grąžinama, ar kai originali prekė nebus grąžinta, galite sukurti prekės pakeitimo užsakymą iškart po to, kai sukūrėte grąžinimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="1e1c2-106">Kurti pakeitimo užsakymą gavus prekę, kuri yra grąžinama</span><span class="sxs-lookup"><span data-stu-id="1e1c2-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="1e1c2-107">Spustelėkite **Pardavimas ir rinkodara** \> **Bendra** \> **Grąžinimo užsakymai** \> **Visi grąžinimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="1e1c2-108">Sukurkite naują grąžinimo užsakymą arba pasirinkite grąžintą užsakymą iš sąrašo, kad atidarytumėte formą **Grąžinimo užsakymas – RMA numeris: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="1e1c2-109">Spustelėkite **Grąžinimo eilutė**, tada pasirinkite **Prekės pakaitalas**.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="1e1c2-110">Pasirinkite prekę, kuria norite pakeisti grąžinamą prekę.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="1e1c2-111">Įveskite prekės specifikacijas, ir tada spustelėkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="1e1c2-112">Spustelėję **Važtaraštis** generuokite grąžinimo užsakymo važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="1e1c2-113">Pardavimo užsakymas yra sugeneruotas keičiamai prekei, kurią pasirinkote.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="1e1c2-114">Keičiamai prekei sukūrus pardavimo užsakymą, pardavimo sutartys yra ieškomos automatiškai, jei yra taikoma pardavimo sutartis, ji taikoma šiam pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="1e1c2-115">Kurti pakeitimo užsakymą, kol gausite elementą, kuris bus grąžintas</span><span class="sxs-lookup"><span data-stu-id="1e1c2-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="1e1c2-116">Spustelėkite **Pardavimas ir rinkodara** \> **Bendra** \> **Grąžinimo užsakymai** \> **Visi grąžinimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="1e1c2-117">Sukurkite naują grąžinimo užsakymą arba pasirinkite grąžinimo užsakymą iš sąrašo, kad atidarytumėte formą **Grąžinimo užsakymas – RMA numeris: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="1e1c2-118">Jei norite nustatyti grąžintos prekės pardavimo užsakymą, spustelėkite **Rasti pardavimo užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="1e1c2-119">Užpildykite formą **Rasti pardavimo užsakymą** ir spustelėję **Gerai** uždarykite formą ir grįžkite į formą **Grąžinimo užsakymas – RMA numeris: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="1e1c2-120">Pardavimo užsakymo eilutė, skirta grąžintai prekei, nukopijuojama į grąžinimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="1e1c2-121">Spustelėję **Pakeitimo užsakymas** atidarykite formą **Kurti pardavimo užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="1e1c2-122">Pažymėkite žymės langelį **Kopijuoti grąžinimo užsakymo eilutes**, jei norite perkelti informaciją iš jūsų pasirinkto grąžinimo užsakymo formoje **Grąžinimo užsakymas – RMA numeris: %1, %2** į šį pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="1e1c2-123">Įveskite arba modifikuokite informaciją kaip reikia.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="1e1c2-124">Jei nustatėte pardavimo užsakymą 3 veiksme, ir jei grąžintos prekės pardavimo užsakymo eilutė yra susieta su pardavimo sutartimi, taikomos pardavimo sutarties dėl prekės pakeitimo užsakymo identifikatorius bus automatiškai rodomas lauke **Pardavimo sutarties ID**.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="1e1c2-125">Spustelėję **Gerai** uždarykite formą **Kurti pardavimo užsakymą** ir atidarykite formą **Pardavimo užsakymas**, kur galite toliau įvesti informaciją apie naują pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="1e1c2-126">Visos taikomos grąžinimo užsakymo eilutės bus nukopijuotos į naują pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="1e1c2-127">Jei pardavimo sutarties identifikatorius automatiškai rodomas lauke **Pardavimo sutarties ID**, tada pardavimo sutartis buvo susieta su prekės pakeitimo užsakymo pardavimo užsakymo antrašte.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="1e1c2-128">Jei yra taikomas dar neįvykdytas įsipareigojimas pardavimo sutartyje, ir pardavimo užsakymas sukurtas iki pardavimo sutarties galiojimo pabaigos, yra nustatomas saitas tarp pardavimo sutarties eilutės ir pardavimo užsakymo eilutės.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="1e1c2-129">Todėl informacija iš pardavimo sutarties, pvz., prekės kaina, kopijuojama į naują pardavimo užsakymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  


