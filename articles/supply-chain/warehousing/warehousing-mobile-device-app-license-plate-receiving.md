---
title: Numerio lentelės gavimas naudojant sandėliavimo programą
description: Šioje temoje paaiškinama, kaip nustatyti sandėliavimo programą, kad faktinių atsargų gavimui būtų palaikomas numerio lentelės gavimo proceso naudojimas.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346381"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a><span data-ttu-id="c46e9-103">Numerio lentelės gavimas naudojant sandėliavimo programą</span><span class="sxs-lookup"><span data-stu-id="c46e9-103">License plate receiving via the warehousing app</span></span>

<span data-ttu-id="c46e9-104">Šioje temoje paaiškinama, kaip nustatyti sandėliavimo programą, kad faktinių atsargų gavimui būtų palaikomas numerio lentelės gavimo proceso naudojimas.</span><span class="sxs-lookup"><span data-stu-id="c46e9-104">This topic explains how to set up the warehousing app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="c46e9-105">Šią funkciją galite naudoti norėdami greitai įrašyti gaunamų atsargų gavimą, susijusį su išankstiniu siuntimo pranešimu (ASN).</span><span class="sxs-lookup"><span data-stu-id="c46e9-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="c46e9-106">Sistema automatiškai sukuria ASN, kai sandėlio valdymo procesai naudojami perkėlimo užsakymui siųsti.</span><span class="sxs-lookup"><span data-stu-id="c46e9-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="c46e9-107">Pirkimo užsakymo procese ASN gali būti įrašytas rankiniu būdu arba automatiškai importuotas naudojant gaunamo ASN duomenų objekto procesą.</span><span class="sxs-lookup"><span data-stu-id="c46e9-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="c46e9-108">ASN duomenys yra susieti su kroviniais ir siuntomis naudojant *pakavimo struktūras*, kurių padėkluose (pirminės numerio lentelės) gali būti saugyklos (įdėtosios numerio lentelės).</span><span class="sxs-lookup"><span data-stu-id="c46e9-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="c46e9-109">Kad būtų sumažintas atsargų operacijų skaičius, kai naudojamos pakavimo struktūros, kuriose yra įdėtųjų numerio lentelių, sistema įrašo faktines turimas atsargas pirminėje numerio lentelėje.</span><span class="sxs-lookup"><span data-stu-id="c46e9-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="c46e9-110">Norėdami suaktyvinti faktinių turimų atsargų perkėlimą iš pirminės numerio lentelės į įdėtąsias numerio lenteles, remiantis pakavimo struktūros duomenimis, mobilusis įrenginys turi pateikti meniu elementą, kuris yra pagrįstas darbo kūrimo procesu *Pakavimas su įdėtosiomis numerių lentelėmis*.</span><span class="sxs-lookup"><span data-stu-id="c46e9-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="c46e9-111">Gavimo suvestinės puslapio rodymas arba praleidimas</span><span class="sxs-lookup"><span data-stu-id="c46e9-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="c46e9-112">Galite naudoti funkciją *Kontroliuoti, ar mobiliuosiuose įrenginiuose bus rodomas gavimo suvestinės puslapis*, kad numerio lentelės gavimo proceso metu galėtumėte pasinaudoti papildomu išsamiu sandėliavimo programos srautu.</span><span class="sxs-lookup"><span data-stu-id="c46e9-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed warehousing app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="c46e9-113">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="c46e9-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="c46e9-114">Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją.</span><span class="sxs-lookup"><span data-stu-id="c46e9-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="c46e9-115">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="c46e9-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="c46e9-116">**Modulis:** *sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="c46e9-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c46e9-117">**Funkcijos pavadinimas:** *Kontroliuoti, ar mobiliuosiuose įrenginiuose bus rodomas gavimo suvestinės puslapis*</span><span class="sxs-lookup"><span data-stu-id="c46e9-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="c46e9-118">Kai ši funkcija įjungta, mobiliojo įrenginio meniu elementai, skirti numerio lentelei gauti arba numerio lentelei gauti ir atidėti, teikia parametrą **Rodyti gavimo suvestinės puslapį**.</span><span class="sxs-lookup"><span data-stu-id="c46e9-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="c46e9-119">Šis parametras turi toliau pateiktas parinktis.</span><span class="sxs-lookup"><span data-stu-id="c46e9-119">This setting has the following options:</span></span>

- <span data-ttu-id="c46e9-120">**Rodyti išsamią suvestinę** – numerio lentelės gavimo metu darbuotojai matys papildomą puslapį, kuriame bus rodoma visa ASN informacija.</span><span class="sxs-lookup"><span data-stu-id="c46e9-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="c46e9-121">**Praleisti suvestinę** – darbuotojai nematys visos ASN informacijos.</span><span class="sxs-lookup"><span data-stu-id="c46e9-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="c46e9-122">Sandėlio darbuotojai taip pat negalės nustatyti perdavimo kodo arba pridėti išimtis gavimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="c46e9-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="c46e9-123">Neleisti perkėlimo užsakyme siunčiamų numerio lentelių naudoti ne paskirties sandėlyje</span><span class="sxs-lookup"><span data-stu-id="c46e9-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="c46e9-124">Numerio lentelės gavimo proceso negalima naudoti, jei ASN yra numerio lentelės ID, kuris jau egzistuoja ir turi faktinių turimų duomenų ne sandėlio, kur vyksta numerio lentelės registravimas, vietoje.</span><span class="sxs-lookup"><span data-stu-id="c46e9-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="c46e9-125">Perkėlimo užsakymo scenarijuose, kuriuose tranzito sandėlis neseka numerio lentelių (todėl taip pat neseka kiekvienos numerio lentelės faktinių turimų atsargų), galite naudoti funkciją *Neleisti perkėlimo užsakyme siunčiamų numerio lentelių naudoti ne paskirties sandėlyje*, kad būtų išvengta faktinių turimų numerio lentelių atnaujinimo tranzito metu.</span><span class="sxs-lookup"><span data-stu-id="c46e9-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="c46e9-126">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="c46e9-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="c46e9-127">Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją.</span><span class="sxs-lookup"><span data-stu-id="c46e9-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="c46e9-128">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="c46e9-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="c46e9-129">**Modulis:** *sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="c46e9-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c46e9-130">**Funkcijos pavadinimas:** *Neleisti perkėlimo užsakyme siunčiamų numerio lentelių naudoti ne paskirties sandėlyje*</span><span class="sxs-lookup"><span data-stu-id="c46e9-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="c46e9-131">Norėdami valdyti funkciją, kai ji pasiekiama, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c46e9-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="c46e9-132">Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c46e9-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="c46e9-133">Skirtuko **Bendra** „FastTab“ konteineryje **Numerio lentelės** nustatykite lauką **Tranzito sandėlio numerio lentelių strategijos** į vieną iš toliau pateiktų verčių.</span><span class="sxs-lookup"><span data-stu-id="c46e9-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="c46e9-134">**Leisti pakartotinį nesekamų numerio lentelių naudojimą** – sistema veikia taip pat, kaip veikia, kai nepasiekiama funkcija *Neleisti perkėlimo užsakyme siunčiamų numerio lentelių naudoti ne paskirties sandėlyje*.</span><span class="sxs-lookup"><span data-stu-id="c46e9-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="c46e9-135">Ši vertė yra numatytasis parametras, kai pirmą kartą suaktyvinate funkciją.</span><span class="sxs-lookup"><span data-stu-id="c46e9-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="c46e9-136">**Vengti pakartotinio nesekamų numerio lentelių naudojimo** – kol perkėlimo užsakymas nebus gautas, paskirties sandėlyje bus leidžiami tik turimi atnaujinimai, susieti su siunčiama numerio lentele.</span><span class="sxs-lookup"><span data-stu-id="c46e9-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="c46e9-137">Daugiau informacijos</span><span class="sxs-lookup"><span data-stu-id="c46e9-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="c46e9-138">Daugiau informacijos apie mobiliojo įrenginio meniu elementus žr. [Mobiliųjų įrenginių nustatymas darbui sandėlyje](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="c46e9-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
