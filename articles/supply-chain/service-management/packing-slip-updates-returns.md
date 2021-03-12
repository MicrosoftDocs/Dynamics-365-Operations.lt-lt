---
title: Važtaraščių naujinimas grąžinimams
description: Prieš tai, kai grąžintos prekės bus gautos į atsargas, turi būti atnaujintas užsakymo, kuriam jos priklauso, važtaraštis.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c82e43beddb8bae0a56b0894ce484ca7605b42e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006721"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="f183f-103">Važtaraščių naujinimas grąžinimams</span><span class="sxs-lookup"><span data-stu-id="f183f-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f183f-104">Prieš tai, kai grąžintos prekės bus gautos į atsargas, turi būti atnaujintas užsakymo, kuriam jos priklauso, važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="f183f-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="f183f-105">Tik tada, kai SF atnaujinimo procesas yra finansinės operacijos atnaujinimas, važtaraščio atnaujinimas yra fizinis atsargų įrašo atnaujinimas, t. y. jo metu atliekami atsargų pakeitimai.</span><span class="sxs-lookup"><span data-stu-id="f183f-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="f183f-106">Grąžinimo atvejais važtaraščio atnaujinimo metu atliekami tie žingsniai, kurie priskirti perdavimo veiksmui.</span><span class="sxs-lookup"><span data-stu-id="f183f-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="f183f-107">Važtaraščio atnaujinimas gali būti atliktas arba prekių gavimo žurnale, arba grąžinimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="f183f-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="f183f-108">Vienu iš važtaraščio registravimo proceso metu atliekamų veiksmų gali būti važtaraščio nuorodos numerio, esančio kliento siuntimo dokumentuose, susiejimas su užsakymo eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="f183f-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="f183f-109">Šis susiejimas nėra privalomas ir naudojamas tik kaip nuoroda.</span><span class="sxs-lookup"><span data-stu-id="f183f-109">This association is optional and for reference only.</span></span> <span data-ttu-id="f183f-110">Joks operacijos atnaujinimas nesukuriamas.</span><span class="sxs-lookup"><span data-stu-id="f183f-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="f183f-111">Jei gautos ne visos numatytos grąžinimo prekės, atnaujindami važtaraštį įtraukite tik gautą kiekį.</span><span class="sxs-lookup"><span data-stu-id="f183f-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="f183f-112">Likusias prekes palikite užsakyme, kol bus gauta visa grąžinimo siunta.</span><span class="sxs-lookup"><span data-stu-id="f183f-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="f183f-113">Jei prekė išsiųsta atgal iš sulaikymo į siuntimo ir gavimo padalinį, pvz., kai sulaikymo inspektorius nežino, kur laikyti prekę atsargose, turi būti atnaujintas atitinkamas važtaraštis, kad būtų tinkamai užregistruotas ir veiktų perdavimo kodas, kuris nurodytas kaip sulaikymo rezultatas.</span><span class="sxs-lookup"><span data-stu-id="f183f-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="f183f-114">Kai atnaujinate važtaraštį grąžintai prekei iš pardavimo sutarties, tos prekės pardavimo sutarties įsipareigojimas automatiškai atnaujinamas, kad atspindėtų kiekio ar sumos pokytį.</span><span class="sxs-lookup"><span data-stu-id="f183f-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="f183f-115">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="f183f-115">See also</span></span>

[<span data-ttu-id="f183f-116">SF naujinimas grąžinimams</span><span class="sxs-lookup"><span data-stu-id="f183f-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  


