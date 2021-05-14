---
title: Sandėlio užsakymai, skirti debesies ir briaunos skalės vienetams
description: Šioje temoje pateikiama informacija apie sandėlio užsakymo galimybę, naudojamą kaip sandėlio skalės vieneto darbo krūvio dalis.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ff1f13198a7acc35897252f3ca8f6c2b1f56852e
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938281"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="deac1-103">Sandėlio užsakymai, skirti debesies ir briaunos skalės vienetams</span><span class="sxs-lookup"><span data-stu-id="deac1-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="deac1-104">Ne visos verslo funkcijos yra visiškai palaikomos viešojoje peržiūros versijoje, kai naudojami skalės vieneto darbo krūviai.</span><span class="sxs-lookup"><span data-stu-id="deac1-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="deac1-105">Jei naudojate skalės vienetus, įsitikinkite, kad naudojate tik tuos procesus, kuriuos išsamiai aprašo šis skyrius kaip palaikomus.</span><span class="sxs-lookup"><span data-stu-id="deac1-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="deac1-106">Kas yra sandėlio užsakymai?</span><span class="sxs-lookup"><span data-stu-id="deac1-106">What are warehouse orders?</span></span>

<span data-ttu-id="deac1-107">*Sandėlio užsakymai* yra užsakymo, sukurto palaikyti telkinio ir skalės vienetų sandėlio diegimus, tipas.</span><span class="sxs-lookup"><span data-stu-id="deac1-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="deac1-108">Jie leidžia jums gauti atsargas, kai vykdote sandėlio darbo krūvį skalės vienete.</span><span class="sxs-lookup"><span data-stu-id="deac1-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="deac1-109">Šiuo metu jie naudojami tik su pirkimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="deac1-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="deac1-110">Sandėlio užsakymai naudojami kaip sandėlio valdymo apdorojimo dalis, pavyzdžiui, kai sandėlio valdymo mobiliųjų įrenginių programėlė naudojama faktinėms turimoms atsargoms registruoti gaunamo pirkimo užsakymo apdorojimo metu.</span><span class="sxs-lookup"><span data-stu-id="deac1-110">Warehouse orders are used as part of warehouse management processing, such as when the Warehouse Management mobile app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="deac1-111">Sandėlio užsakymai kuriami kaip dalis *Išleidimo į sandėlį* proceso, prieinamo pirkimo užsakymams, kurie nurodo skalės vieneto sandėlį ir prekes, įgalintas naudoti sandėlio valdymo procesus.</span><span class="sxs-lookup"><span data-stu-id="deac1-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="deac1-112">Sandėlio užsakymai galimi tik diegimams, naudojantiems [sandėlio valdymo darbo krūvius debesiui ir briaunai skalės vienetams](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="deac1-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="deac1-113">Sandėlio užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="deac1-113">Create a warehouse order</span></span>

<span data-ttu-id="deac1-114">Norėdami sukurti sandėlio užsakymą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="deac1-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="deac1-115">Prisijunkite prie „Microsoft Dynamics 365 Supply Chain Management“ egzemplioriaus, vykdomo telkinyje.</span><span class="sxs-lookup"><span data-stu-id="deac1-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="deac1-116">(Turite inicijuoti *Išleidimo į sandėlį* procesą, kai esate prisijungę telkinyje.)</span><span class="sxs-lookup"><span data-stu-id="deac1-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="deac1-117">Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="deac1-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="deac1-118">Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="deac1-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="deac1-119">Norėdami peržiūrėti susijusias sandėlio užsakymo eilutes, atidarykite reikiamą pirkimo užsakymą, pasirinkite eilutę, esančią skyriuje **Pirkimo užsakymo eilutės** ir tada įrankių juostoje pasirinkite **Sandėlis \> Sandėlio užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="deac1-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="deac1-120">Norėdami peržiūrėti visas eilutes, eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Sandėlio užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="deac1-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

<span data-ttu-id="deac1-121">Taip pat procesą *Išleisti į sandėlį* galima paleisti iš paketinės užduoties, einant į **Sandėlio tvarkymas > Išleisti į sandėlį > Automatinis pirkimo užsakymų išleidimas**.</span><span class="sxs-lookup"><span data-stu-id="deac1-121">You can also trigger the *Release to warehouse* process from a batch job by going to **Warehouse management > Release to warehouse > Automatic release of purchase orders**.</span></span> <span data-ttu-id="deac1-122">Nustatydami paketinę užduotį galite pasirinkti konkrečias pirkimo užsakymo eilutes pagal užklausą.</span><span class="sxs-lookup"><span data-stu-id="deac1-122">When setting up the batch job, you can select specific purchase order lines based on a query.</span></span> <span data-ttu-id="deac1-123">Įprastas scenarijus būtų nustatyti pasikartojančią paketinę užduotį, kuri išleidžia visas patvirtintas pirkimo užsakymo eilutes, kurias numatoma gauti kitą dieną.</span><span class="sxs-lookup"><span data-stu-id="deac1-123">A typical scenario would be to set up a recurrent batch job that releases all the confirmed purchase order lines expected to arrive the next day.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="deac1-124">Sandėlio užsakymo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="deac1-124">Cancel a warehouse order</span></span>

<span data-ttu-id="deac1-125">Kaip *Išleidimo į sandėlį* proceso dalis, pirkimo užsakymo atsargų operacijos yra susietos su sandėlio užsakymais ir jų negalima atnaujinti telkinyje.</span><span class="sxs-lookup"><span data-stu-id="deac1-125">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="deac1-126">Jeigu suklydote išleisdami prekes į sandėlį ar turite kitą priežastį atšaukti sandėlio užsakymo eilučių sukūrimą, galite pateikti sandėlio užsakymo eilučių atšaukimo užklausą.</span><span class="sxs-lookup"><span data-stu-id="deac1-126">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="deac1-127">Norėdami atšaukti sandėlio užsakymo eilutes, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="deac1-127">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="deac1-128">Prisijunkite prie „Supply Chain Management“ egzemplioriaus, vykdomo telkinyje.</span><span class="sxs-lookup"><span data-stu-id="deac1-128">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="deac1-129">Eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Sandėlio užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="deac1-129">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="deac1-130">Pasirinkite reikalingą eilutę.</span><span class="sxs-lookup"><span data-stu-id="deac1-130">Select the relevant line.</span></span>
1. <span data-ttu-id="deac1-131">Veiksmų srityje pasirinkite **Atšaukti sandėlio užsakymo eilutes**.</span><span class="sxs-lookup"><span data-stu-id="deac1-131">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="deac1-132">Eilučių atšaukimo prašymas bus atmestas bet kurioms eilutėms, kurios jau laukia atšaukimo arba kurios aktyviai apdorojamos sandėlyje, kuriame vykdomas jos darbo krūvis skalės vienetais.</span><span class="sxs-lookup"><span data-stu-id="deac1-132">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="deac1-133">Sandėlio užsakymo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="deac1-133">Monitor a warehouse order</span></span>

<span data-ttu-id="deac1-134">Rodinyje **Sandėlio užsakymo eilutės** galite stebėti gavimo eigą peržiūrėdami **Likęs gautinas kiekis** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="deac1-134">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="deac1-135">Norėdami peržiūrėti su darbu susijusią išsamią informaciją naudojant sandėlio valdymo mobiliųjų įrenginių programėlę, atlikite vieną iš šių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="deac1-135">To view details that are related to work that is done by using the Warehouse Management mobile app, follow one of these steps.</span></span>

- <span data-ttu-id="deac1-136">Eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Sandėlio užsakymo eilutės** ir naudokite filtrą rasti ieškomoms eilutėms.</span><span class="sxs-lookup"><span data-stu-id="deac1-136">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="deac1-137">Eikite į **Įsigijimas ir šaltiniai \> Pirkimo užsakymai \> Visi pirkimo užsakymai** ir atidarykite reikiamą pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="deac1-137">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="deac1-138">Skyriuje **Pirkimo užsakymo eilutės** pasirinkite vieną ar daugiau eilučių ir tada įrankių juostoje pasirinkite **Sandėlis \> Sandėlio gavimo įrašai**.</span><span class="sxs-lookup"><span data-stu-id="deac1-138">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
