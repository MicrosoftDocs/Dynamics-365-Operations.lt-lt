---
title: "Grąžintų prekių dalinių pristatymų gavimas"
description: "Daliniai pristatymai apibrėžiami kalbant apie grąžinimo užsakymo eilutes, ne apie grąžinimo užsakymo siuntas."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e2b7bfad1e0d80675848353d4118960d44f2dc01
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---

# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="3358a-103">Grąžintų prekių dalinių pristatymų gavimas</span><span class="sxs-lookup"><span data-stu-id="3358a-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3358a-104">Daliniai pristatymai apibrėžiami kalbant apie grąžinimo užsakymo eilutes, ne apie grąžinimo užsakymo siuntas.</span><span class="sxs-lookup"><span data-stu-id="3358a-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="3358a-105">Tai reiškia, kad, jei gaunate visą kiekį, nurodytą vienoje grąžinimo užsakymo eilutėje, bet nieko negaunate iš kitose grąžinimo užsakymo eilutėse nurodyto kiekio, šis pristatymas nėra dalinis.</span><span class="sxs-lookup"><span data-stu-id="3358a-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="3358a-106">Tačiau, jei grąžinimo užsakymo eilutėje nurodyta grąžinti 10 konkrečios prekės vienetų, bet gaunate tik keturis, tai yra dalinis pristatymas.</span><span class="sxs-lookup"><span data-stu-id="3358a-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="3358a-107">Jei grąžinimo siuntą sudaro ne visas grąžinimo užsakymo eilutėje nurodytas kiekis, siuntą galite atidėti į šalį ir laukti, kol bus pristatyta likusi grąžinto kiekio dalis, arba galite užregistruoti dalinį kiekį.</span><span class="sxs-lookup"><span data-stu-id="3358a-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="3358a-108">Dalinio kiekio registravimas</span><span class="sxs-lookup"><span data-stu-id="3358a-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="3358a-109">Pasirinkę gautiną grąžinimo užsakymą formoje **Gavimų peržiūra – sandėlis: %1, rampa: %2, žurnalo pavadinimas: %3** spustelėkite **Pradėti gavimo žurnalą**, kad sukurtumėte gavimo žurnalą, ir spustelėkite **Žurnalai** \> **Rodyti gavimų žurnalus pagal gavimus**, kad atidarytumėte formą **Vietos žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="3358a-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="3358a-110">Pasirinkite eilutę iš žurnalo, su kuriuo norite dirbti, tada spustelėkite **Eilutės**, kad atidarytumėte formą **Žurnalo eilutės, vietos**.</span><span class="sxs-lookup"><span data-stu-id="3358a-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="3358a-111">Pasirinkite prekės, kurios dalinis kiekis buvo pristatytas, numerio eilutę, tada spustelėję **Funkcijos** \> **Skaidyti** atidarykite formą **Skaidyti**.</span><span class="sxs-lookup"><span data-stu-id="3358a-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="3358a-112">Lauke **Skaidyti kiekį** įveskite bendrą gautų prekių skaičių, tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3358a-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="3358a-113">Formoje **Žurnalo eilutės, vietos** pasirinkite pristatytų prekių kiekio eilutę, tada spustelėkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="3358a-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="3358a-114">Pristačius prekes, galite registruoti eilutę papildomam kiekiui.</span><span class="sxs-lookup"><span data-stu-id="3358a-114">You can post the line for the additional quantity after the items have arrived.</span></span>





