---
title: Sandėlio paketo ir serijos rezervavimo hierarchijų trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti dažnas klaidas, su kuriomis galite susidurti dirbdami su rezervavimo hierarchijomis, naudojančiomis paketo arba serijos dimensijas.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a1abb6f8657484d43d434076e5ee38d1c63fe2ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838183"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="a0a2e-103">Sandėlio paketo ir serijos rezervavimo hierarchijų trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="a0a2e-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0a2e-104">Šioje temoje aprašoma, kaip ištaisyti dažnas klaidas, su kuriomis galite susidurti dirbdami su rezervavimo hierarchijomis, naudojančiomis paketo arba serijos dimensijas.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="a0a2e-105">Dėl išsamesnės informacijos, žr. [Lanksti sandėlio lygmens matmenų rezervacijos politika](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="a0a2e-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="a0a2e-106">Prekės rezervavimo hierarchija diktuoja saugojimo dimensijų, kurios turi būti užpildytos poreikio užsakymo vietos priskyrimui, reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="a0a2e-107">Šios dimensijos gali būti apibūdinamos kaip *dimensijos aukščiau vietos* visoms dimensijoms, kurios turi būti užpildytos prieš priskiriant vietą, ir *dimensijos žemiau vietos* toms dimensijoms, kurios gali būti paskirstytos po to, kai poreikio užsakymui buvo priskirta vieta.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="a0a2e-108">Šios rezervavimo hierarchijos taip pat žinomos kaip *paketas aukščiau* ir *paketas žemiau* rezervavimo hierarchijos arba *serija aukščiau* ir *serija žemiau* rezervavimo hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="a0a2e-109">Atsargas galima sėkmingai paskirstyti tik tada, jei dimensijose aukščiau vietos nėra tarpų.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="a0a2e-110">Pavyzdžiui, rezervavimo hierarchijoje *paketas aukščiau* tikitės, jog dimensijos **Saitas,** **Sandėlis** ir **Paketo numeris** bus nurodytos poreikio užsakyme.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="a0a2e-111">Jeigu trūksta bet kurios iš šių dimensijų, paskirstymo procesas nepavyks.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="a0a2e-112">Priešingai, *paketas žemiau* ar *serija žemiau* rezervavimo hierarchijoje paketo arba serijos numeris gali būti nurodytas poreikio užsakyme, tačiau jis nebūtinas paskirstymo procesui.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="a0a2e-113">Gaunu tolesnį klaidos pranešimą: „Tam kad būtų priskirtos prie bangos, krovinio eilutės turi nurodyti dimensijas virš vietos.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="a0a2e-114">Norėdami priskirti šias dimensijas, rezervuokite ir iš naujo sukurkite krovinio eilutę."</span><span class="sxs-lookup"><span data-stu-id="a0a2e-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a0a2e-115">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="a0a2e-115">Issue description</span></span>

<span data-ttu-id="a0a2e-116">Jums naudojant prekę, turinčią *paketas aukščiau* rezervavimo hierarchiją, puslapyje **Krovinio planavimo darbo sritis** esanti komanda **Išleisti į sandėlį** neveikia, jeigu bandote išleisti krovinį daliniam kiekiui.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="a0a2e-117">Gaunate šį klaidos pranešimą ir joks darbas nesukuriamas daliniam kiekiui.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="a0a2e-118">Tačiau, kai naudojate prekę, turinčią *paketas žemiau* rezervavimo hierarchiją, galite išleisti krovinį daliniam kiekiui iš **Krovinio planavimo darbo srities** puslapio.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="a0a2e-119">Problemos priežastis</span><span class="sxs-lookup"><span data-stu-id="a0a2e-119">Issue cause</span></span>

<span data-ttu-id="a0a2e-120">Kai dimensija yra virš **Vietos** dimensijos rezervacijos hierarchijoje, ji turi būti nurodytas prieš išleidimą į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="a0a2e-121">Daliniai kiekiai negali būti išleisti, jei viena ar kelios dimensijos virš **Vietos** nenurodyti.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="a0a2e-122">Automatinio rezervavimo raginimas įvesti paketo numerį yra suaktyvinamas, net jei yra galimų atsargų.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a0a2e-123">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="a0a2e-123">Issue description</span></span>

<span data-ttu-id="a0a2e-124">Kai naudojate prekę, turinčią *paketas aukščiau* rezervavimo hierarchiją sandėlyje, kuriame neįgalinti sandėlio procesai ir įgalintas automatinis rezervavimas, yra rodomas automatinio rezervavimo raginimas įvesti paketo numerį, net jeigu tik vienas paketas yra galimas paėmimui.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="a0a2e-125">Tačiau, kai naudojate tą pačią prekę sandėlyje, kuriame įgalinti sandėlio procesai, automatinio rezervavimo raginimas nėra rodomas.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="a0a2e-126">Problemos priežastis</span><span class="sxs-lookup"><span data-stu-id="a0a2e-126">Issue cause</span></span>

<span data-ttu-id="a0a2e-127">Jei rezervavimo hierarchija apibrėžta kaip *paketas aukščiau* ar *serija aukščiau*, nurodyta dimensija (**Paketo numeris** arba **Serijos numeris**) visada turi būti nurodyta poreikio užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="a0a2e-128">Sandėlio procesai gali sugebėti užpildyti informaciją, jei yra vienas paketas ar serijos numeris.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="a0a2e-129">Tačiau, kadangi sandėlis nėra įgalintas sandėlio procesams, vartotojas visada turi nurodyti visas dimensijas, esančias virš **Vietos**.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="a0a2e-130">Intervalo šablonai, turintys atsižvelgti į turimas atsargas intervalo kriterijų, neatsižvelgia į dabartines turimas atsargas, skirtas įjungto paketo prekėms.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="a0a2e-131">Daugiau informacijos rasite [Sandėlio intervalas](warehouse-slotting.md).</span><span class="sxs-lookup"><span data-stu-id="a0a2e-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="a0a2e-132">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="a0a2e-132">Issue description</span></span>

<span data-ttu-id="a0a2e-133">Intervalo šablonai, turintys *Atsižvelgti į turimas atsargas* intervalo kriterijų, neatsižvelgia į dabartines turimas atsargas, skirtas *paketas aukščiau* prekėms.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="a0a2e-134">Jie atsižvelkite į jas tik tuo atveju, jei pardavimo užsakymo eilutėje nurodytas paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="a0a2e-135">Tačiau, kai naudojate *paketas žemiau* prekes, laikoma, kad dabartinės turimos atsargos yra tikėtinos.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="a0a2e-136">Problemos priežastis</span><span class="sxs-lookup"><span data-stu-id="a0a2e-136">Issue cause</span></span>

<span data-ttu-id="a0a2e-137">Intervalo šablono antraštę galima nurodyti *Užsakyta*, *Rezervuota* arba *Išleista* poreikio strategijoms.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="a0a2e-138">Poreikio strategijai *Užsakyta* taikomi tie patys rezervavimo hierarchijos reikalavimai, kurie taikomi ir rezervavimo arba išleidimo į sandėlio procesams.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="a0a2e-139">Todėl prekių, turinčių *paketas aukščiau* ir *serija žemiau* rezervavimo hierarchijas, poreikio užsakyme (pardavimo arba perkėlimo) turi būti nurodytas paketo arba serijos numeris.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="a0a2e-140">Taip pat, galima naudoti poreikio strategiją *Rezervuota* pasirinkti paketo arba serijos numerį prieš generuojant sandėlio intervalo poreikį.</span><span class="sxs-lookup"><span data-stu-id="a0a2e-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
