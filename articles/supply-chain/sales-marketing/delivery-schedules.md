---
title: Pristatymo grafikai
description: Naudojant pristatymo grafikus galima sekti užsakymo eilučių kiekį, kai išsiunčiate kelis pardavimo užsakymus, pardavimo pasiūlymus ar pirkimo užsakymus.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dbd66d499b5d5f9f8ef21c0ce3752031a5f4672
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193787"
---
# <a name="delivery-schedules"></a><span data-ttu-id="38bb2-103">Pristatymo grafikai</span><span class="sxs-lookup"><span data-stu-id="38bb2-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38bb2-104">Naudojant pristatymo grafikus galima sekti užsakymo eilučių kiekį, kai išsiunčiate kelis pardavimo užsakymus, pardavimo pasiūlymus ar pirkimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="38bb2-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="38bb2-105">Naudokite pristatymo grafiką, kai bendras užsakymo ar pasiūlymo eilutės kiekis turi būti pristatytas keliomis siuntomis.</span><span class="sxs-lookup"><span data-stu-id="38bb2-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="38bb2-106">Atskiras siuntas nurodo pristatymo eilutės.</span><span class="sxs-lookup"><span data-stu-id="38bb2-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="38bb2-107">Dvi ar daugiau pristatymo eilučių sudaro vieną pristatymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="38bb2-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="38bb2-108">Pristatymo eilutėse gali skirtis pristatymo datos, kiekiai, pristatymo būdai ir saugojimo dimensijos, pvz., teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="38bb2-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="38bb2-109">**Pristatymo grafiko pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="38bb2-109">**Example of a delivery schedule**</span></span>

| <span data-ttu-id="38bb2-110">Produktas</span><span class="sxs-lookup"><span data-stu-id="38bb2-110">Item</span></span>                              | <span data-ttu-id="38bb2-111">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="38bb2-111">Value</span></span>                                    |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="38bb2-112">Bendrasis užsakymas (pradinė užsakymo eilutė)</span><span class="sxs-lookup"><span data-stu-id="38bb2-112">Total order (original order line)</span></span> | <span data-ttu-id="38bb2-113">600 kėdžių</span><span class="sxs-lookup"><span data-stu-id="38bb2-113">600 chairs</span></span>                               |
| <span data-ttu-id="38bb2-114">Pageidaujamas pristatymo grafikas</span><span class="sxs-lookup"><span data-stu-id="38bb2-114">Requested delivery schedule</span></span>       | <span data-ttu-id="38bb2-115">100 kėdžių per mėnesį</span><span class="sxs-lookup"><span data-stu-id="38bb2-115">100 chairs per month</span></span>                     |
| <span data-ttu-id="38bb2-116">Pageidaujama pristatymo laikotarpis</span><span class="sxs-lookup"><span data-stu-id="38bb2-116">Requested time frame for delivery</span></span> | <span data-ttu-id="38bb2-117">6 mėnesiai, pristatant kiekvieno mėnesio pirmą dieną</span><span class="sxs-lookup"><span data-stu-id="38bb2-117">6 months, on the first day of each month</span></span> |

<span data-ttu-id="38bb2-118">Pagal šį scenarijų klientas reikalauja pristatyti 600 kėdžių 100 kėdžių paketais per šešis mėnesius.</span><span class="sxs-lookup"><span data-stu-id="38bb2-118">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="38bb2-119">Norėdami sekti pristatymo reikalavimus, galite kurti pristatymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="38bb2-119">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="38bb2-120">Puslapyje Pristatymo grafikas galite kurti šešias atskiras pristatymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="38bb2-120">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="38bb2-121">Kiekvienoje eilutėje nurodyta 100 kėdžių ir jų pristatymo data.</span><span class="sxs-lookup"><span data-stu-id="38bb2-121">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="38bb2-122">Šiuo atveju kiekviena eilutė yra korespondentė pirmąjį iš šešių mėnesių.</span><span class="sxs-lookup"><span data-stu-id="38bb2-122">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="38bb2-123">Kai kuriate pristatymo grafiką, pradinės užsakymo eilutės tipas automatiškai pakeičiamas į **Užsakymo eilutė su keliais pristatymais**.</span><span class="sxs-lookup"><span data-stu-id="38bb2-123">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="38bb2-124">Šio tipo eilutė vadinama komercine eilute ir yra pažymėta piktograma.</span><span class="sxs-lookup"><span data-stu-id="38bb2-124">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="38bb2-125">Pristatymo eilutė pažymima kita piktograma.</span><span class="sxs-lookup"><span data-stu-id="38bb2-125">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="38bb2-126">Pakeitus pristatymo eilutės kiekį, prekybos eilutė atnaujinama bendruoju pristatymo grafiko kiekiu.</span><span class="sxs-lookup"><span data-stu-id="38bb2-126">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="38bb2-127">Jei prekybos sutartyje nurodyta bendra užsakymo nuolaida, pristatymo grafikas užtikrina, kad jūsų užsakymui būtų taikoma bendra užsakymo nuolaida, net kai užsakymas yra padalintas į atskirus pristatymus.</span><span class="sxs-lookup"><span data-stu-id="38bb2-127">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="38bb2-128">Užsakymai, turintys pristatymo grafiką, apdorojamos pagal pristatymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="38bb2-128">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="38bb2-129">Apdorojimo metu registruojami važtaraščiai, produktų gavimo kvitai ir išrašomos SF.</span><span class="sxs-lookup"><span data-stu-id="38bb2-129">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="38bb2-130">Užsakymų ir pasiūlymų, turinčių pristatymo grafiką, dokumentų spaudiniuose rodomos tik pristatymo eilutės.</span><span class="sxs-lookup"><span data-stu-id="38bb2-130">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="38bb2-131">Juose nerodomos pradinės eilutės (komercinės eilutės).</span><span class="sxs-lookup"><span data-stu-id="38bb2-131">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="38bb2-132">**Pastaba:** be to, rodomos tik pristatymo eilutės, kai atliekate toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="38bb2-132">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="38bb2-133">Skelbti</span><span class="sxs-lookup"><span data-stu-id="38bb2-133">Post</span></span>
-   <span data-ttu-id="38bb2-134">Kopijuoti puslapius</span><span class="sxs-lookup"><span data-stu-id="38bb2-134">Copy pages</span></span>
-   <span data-ttu-id="38bb2-135">Naršyti sąrašo puslapius ir ataskaitas</span><span class="sxs-lookup"><span data-stu-id="38bb2-135">Browse list pages and reports</span></span>

<span data-ttu-id="38bb2-136">Kai patvirtinsite pardavimo pasiūlymus, gautuose pardavimo užsakymuose rodomas visas pristatymo grafikas, įskaitant net užsakymo eilutes, turinčias kelis pristatymus.</span><span class="sxs-lookup"><span data-stu-id="38bb2-136">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="38bb2-137">Be to, visas pristatymo grafikas yra rodomas visuose pagrindiniuose puslapiuose, pvz., pardavimo užsakymuose, pardavimo pasiūlymuose ir pirkimo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="38bb2-137">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]