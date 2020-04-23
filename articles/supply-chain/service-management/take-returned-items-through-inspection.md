---
title: Grąžintų prekių patikrinimas
description: Grąžintų prekių patikrinimas.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa85bf4262216c780c3da523f65baf980fdc200f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206570"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="6d106-103">Grąžintų prekių patikrinimas</span><span class="sxs-lookup"><span data-stu-id="6d106-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="6d106-104">Spustelėkite **Atsargų valdymas** \> **Periodinis** \> **Kokybės valdymas** \> **Sulaikymo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="6d106-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="6d106-105">Raskite užsakymo eilutę, atitinkančią tikrinamą grąžintą prekę.</span><span class="sxs-lookup"><span data-stu-id="6d106-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="6d106-106">Sulaikymo užsakymą galima susieti tik su vienu prekės numeriu.</span><span class="sxs-lookup"><span data-stu-id="6d106-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="6d106-107">Jei 10 prekių su skirtingais prekių numeriais grąžinamos viename siuntinyje ir siunčiamos į sulaikymą, bus sukurta 10 atskirų sulaikymo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="6d106-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="6d106-108">Patikrinę prekę, lauke **Perdavimo kodas** atlikite pasirinkimą ir nurodykite, kas turėtų būti atliekama su preke ir kaip tvarkyti susijusią finansinę operaciją.</span><span class="sxs-lookup"><span data-stu-id="6d106-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="6d106-109">Pavyzdžiai apima prekės grąžinimą į atsargas ir pinigų grąžinimą klientui, išmetimą į atliekas ir pakaitalo siuntimą klientui arba prekės grąžinimą klientui be kredito.</span><span class="sxs-lookup"><span data-stu-id="6d106-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="6d106-110">Jei keleto grąžintų prekių su vienu prekės numeriu paketo negalima priskirti tam pačiam perdavimo kodui, reikia išskaidyti sulaikymo užsakymą (<STRONG>Funkcijos</STRONG> &gt; <STRONG>Skaidyti</STRONG>), kad kiekvienam papildomam paketui būtų priskirtas skirtingas perdavimo kodas.</span><span class="sxs-lookup"><span data-stu-id="6d106-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="6d106-111">Baigę tikrinti spustelėkite **Paskelbti baigtu** ir paleiskite grąžintas prekes bei sukurkite prekių atvykimo žurnalo įrašą.</span><span class="sxs-lookup"><span data-stu-id="6d106-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="6d106-112">Tada prekes gavęs asmuo arba padalinys apdoroja į atsargas grąžintinų prekių žurnalą.</span><span class="sxs-lookup"><span data-stu-id="6d106-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="6d106-113">arba,</span><span class="sxs-lookup"><span data-stu-id="6d106-113">–or–</span></span>
    
    <span data-ttu-id="6d106-114">Pabaikite sulaikymo užsakymą ir naudodami vieną iš mygtuko **Atsargos** funkcijų prekes iš karto perkelkite atgal į atsargas.</span><span class="sxs-lookup"><span data-stu-id="6d106-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="6d106-115">Uždarę formą įrašysite savo pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="6d106-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d106-116">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="6d106-116">See also</span></span>

[<span data-ttu-id="6d106-117">Nustatymas, kaip išmesti grąžintas prekes</span><span class="sxs-lookup"><span data-stu-id="6d106-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  


