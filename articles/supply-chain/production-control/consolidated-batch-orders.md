---
title: Konsoliduotieji paketiniai užsakymai
description: Šiame straipsnyje aprašyta konsoliduotųjų paketinių užsakymų sąvoka.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: faeb90aa3366a58b746c0b397dd950bfb8c9024f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979480"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="231ae-103">Konsoliduotieji paketiniai užsakymai</span><span class="sxs-lookup"><span data-stu-id="231ae-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="231ae-104">Šiame straipsnyje aprašyta konsoliduotųjų paketinių užsakymų sąvoka.</span><span class="sxs-lookup"><span data-stu-id="231ae-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="231ae-105">Gaminama sudedamoji prekės dalis yra pirminė prekė, o supakuota prekė laikoma antrine preke.</span><span class="sxs-lookup"><span data-stu-id="231ae-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="231ae-106">Sudedamosios prekės dalies ir supakuotos prekės ryšys išreiškiamas konvertuojant sudedamąją prekės dalį.</span><span class="sxs-lookup"><span data-stu-id="231ae-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="231ae-107">Šį sudedamosios prekės dalies konvertavimą apibrėžia pati sudedamosios prekės dalis.</span><span class="sxs-lookup"><span data-stu-id="231ae-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="231ae-108">Supakuotas prekes galima pakuoti į vieno dydžio arba kelių dydžių konteinerius, kurie laikomi vienu vienetu.</span><span class="sxs-lookup"><span data-stu-id="231ae-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="231ae-109">Konsoliduodami sudedamosios prekės dalies užsakymus, matote visus susijusius paketinius užsakymus viename rodinyje, kuris gali padėti nustatyti likusį darbą, kurį reikia atlikti.</span><span class="sxs-lookup"><span data-stu-id="231ae-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="231ae-110">Konsoliduotieji paketiniai užsakymai gali apimti bet kokį toliau nurodytų užsakymų derinį.</span><span class="sxs-lookup"><span data-stu-id="231ae-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="231ae-111">Vienas didelis užsakymas ir keli supakuotų prekių užsakymai</span><span class="sxs-lookup"><span data-stu-id="231ae-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="231ae-112">Keli dideli užsakymai ir keli supakuotų prekių užsakymai</span><span class="sxs-lookup"><span data-stu-id="231ae-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="231ae-113">Keli dideli užsakymai ir vienas supakuotų prekių užsakymas</span><span class="sxs-lookup"><span data-stu-id="231ae-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="231ae-114">Tik supakuotų prekių užsakymai</span><span class="sxs-lookup"><span data-stu-id="231ae-114">Only packed orders</span></span>




