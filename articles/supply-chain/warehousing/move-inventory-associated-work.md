---
title: "Atsargų perkėlimas su susietu darbu modulyje Sandėlio valdymas"
description: "Šioje temoje aprašoma, kaip nustatyti ir taikyti vienetų paėmimo patvirtinimą iš mobiliojo įrenginio."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2889f04017bdd20be05174146ba88a24cbefacbb
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="1cbaa-103">Atsargų perkėlimas su susietu darbu modulyje Sandėlio valdymas</span><span class="sxs-lookup"><span data-stu-id="1cbaa-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cbaa-104">Naudodami atsargų judėjimą, galite nuspręsti, kuriems sandėlio darbininkams leidžiama perkelti rezervuotas atsargas.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="1cbaa-105">Tai suteikia lankstumo reguliuojamuosiuose sandėliuose, kuriuose galite nuspręsti neleisti darbininkui pasirinkti naujos paėmimo darbo paėmimo vietos, kuri jau sukurta.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="1cbaa-106">Tai taip pat suteikia sandėlio vadovui galimybę kontroliuoti, kokias galimybes turėtų turėti mažiau patyrę darbininkai.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="1cbaa-107">Lanksčiau valdyti sandėlio darbininkų kasdienes operacijas gali būti naudinga tokiais atvejais:</span><span class="sxs-lookup"><span data-stu-id="1cbaa-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="1cbaa-108">1 scenarijus</span><span class="sxs-lookup"><span data-stu-id="1cbaa-108">Scenario 1</span></span>
<span data-ttu-id="1cbaa-109">Įmonė turi gana nedidelę gavimo sritį, kuri perpildyta padėklais ir dėžėmis, kurios turi būti atidėtos.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="1cbaa-110">Šią dieną laukiama didelės siuntos, todėl gaunamų prekių klerkas nusprendžia išvalyti gavimo sritį perkeliant dalį padėklų į antrinę gavimo išdėstymo sritį.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="1cbaa-111">2 scenarijus</span><span class="sxs-lookup"><span data-stu-id="1cbaa-111">Scenario 2</span></span>
<span data-ttu-id="1cbaa-112">Patyręs sandėlio darbininkas pastebi sandėlyje galimybę konsoliduoti prekes vienoje vietoje, užuot jas išskirsčius mažais kiekiais 3 netoli viena kitos esančiose vietose.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="1cbaa-113">Darbininkas nori konsoliduoti kiekį perkeldamas prekes iš kiekvienos iš šių vietų į tą pačią vietą ir naudojant tą pačią numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="1cbaa-114">3 scenarijus</span><span class="sxs-lookup"><span data-stu-id="1cbaa-114">Scenario 3</span></span>
<span data-ttu-id="1cbaa-115">Padėklas laukia siuntos išdėstymo vietoje, pvz., STAGE01, kuri yra netoli BAYDOOR01.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="1cbaa-116">Tačiau, pasikeitus planams, suplanuotas sunkvežimio atvykimas į BAYDOOR04.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="1cbaa-117">Siunčiantis klerkas tai žino ir turi užtikrinti, kad sunkvežimiui nereikėtų laukti, kol bus pakrautas iš STAGE01.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="1cbaa-118">Siunčiantis klerkas nusprendžia perkelti tos siuntos prekes iš STAGE01 į STAGE04, kuri yra arčiau naujosios paskirties vietos.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="1cbaa-119">Dabartiniai apribojimai</span><span class="sxs-lookup"><span data-stu-id="1cbaa-119">Current limitations</span></span>

<span data-ttu-id="1cbaa-120">Darbo rezervavimai, kuriuos galite perkelti, yra pardavimo užsakymas, perkėlimo užsakymo išdavimas, perkėlimo užsakymo gavimas, pirkimo užsakymas ir papildymo darbas.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="1cbaa-121">Prekių perkėlimas yra apribotas siekiant išvengti darbo eilučių skaidymo.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="1cbaa-122">Tai reiškia, kad jei turite darbo eilutę 100 vnt. A prekių iš vietos Loc1, negalėsite perkelti tik 30 vnt. A prekių iš tos į kitą vietą.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="1cbaa-123">Dėl to esama darbo eilutė būtų suskaidyta į 30 ir 70, nes dabar skiriasi vietos.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="1cbaa-124">Išdėstymo scenarijų atveju, kai numerio lentelė, iš kurios perkeliate prekes, arba numerio lentelė, į kurią perkeliate prekes, nustatytos kaip darbo užsakymo paskirties LP, leidžiama perkelti tik visą LP, kad nebūtų padalinta paskirties LP.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="1cbaa-125">Šiuo metu palaikomas tik ad hoc perkėlimas.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="1cbaa-126">Tai reiškia, kad negalėsite perkelti rezervuotų atsargų, perkeldami pagal šabloninio mobiliojo įrenginio meniu elementus.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="1cbaa-127">Teisės atskiriems darbininkams perkelti rezervuotas atsargas nustatymas</span><span class="sxs-lookup"><span data-stu-id="1cbaa-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="1cbaa-128">Norėdami pažymėti darbininką, kuriam turėtų būti leidžiama perkelti rezervuotas atsargas, pasirinkite žymės langelį **Leisti perkelti atsargas, susietas su darbu**, esantį dalyje **Sandėlio valdymas** > **Sąranka** > **Darbininkas**.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="1cbaa-129">Perkelta</span><span class="sxs-lookup"><span data-stu-id="1cbaa-129">Backported</span></span>

<span data-ttu-id="1cbaa-130">Ši funkcija taip pat buvo perkelta į „Microsoft Dynamics AX 2012 R3“ ir bus pasiekiama kaip CU12 dalis.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="1cbaa-131">Ją taip pat galima atsisiųsti atskirai KB numeriu 3192548.</span><span class="sxs-lookup"><span data-stu-id="1cbaa-131">It can also be downloaded individually through KB number 3192548.</span></span> 


