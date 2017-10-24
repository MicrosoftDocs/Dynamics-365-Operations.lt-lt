---
title: "Konsoliduotieji paketiniai užsakymai"
description: "Šiame straipsnyje aprašyta konsoliduotųjų paketinių užsakymų sąvoka."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3ca9c920ea333bd21defebc29b40243d3a618a3d
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="consolidated-batch-orders"></a><span data-ttu-id="0dd18-103">Konsoliduotieji paketiniai užsakymai</span><span class="sxs-lookup"><span data-stu-id="0dd18-103">Consolidated batch orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0dd18-104">Šiame straipsnyje aprašyta konsoliduotųjų paketinių užsakymų sąvoka.</span><span class="sxs-lookup"><span data-stu-id="0dd18-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="0dd18-105">Gaminama sudedamoji prekės dalis yra pirminė prekė, o supakuota prekė laikoma antrine preke.</span><span class="sxs-lookup"><span data-stu-id="0dd18-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="0dd18-106">Sudedamosios prekės dalies ir supakuotos prekės ryšys išreiškiamas konvertuojant sudedamąją prekės dalį.</span><span class="sxs-lookup"><span data-stu-id="0dd18-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="0dd18-107">Šį sudedamosios prekės dalies konvertavimą apibrėžia pati sudedamosios prekės dalis.</span><span class="sxs-lookup"><span data-stu-id="0dd18-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="0dd18-108">Supakuotas prekes galima pakuoti į vieno dydžio arba kelių dydžių konteinerius, kurie laikomi vienu vienetu.</span><span class="sxs-lookup"><span data-stu-id="0dd18-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="0dd18-109">Konsoliduodami sudedamosios prekės dalies užsakymus, matote visus susijusius paketinius užsakymus viename rodinyje, kuris gali padėti nustatyti likusį darbą, kurį reikia atlikti.</span><span class="sxs-lookup"><span data-stu-id="0dd18-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="0dd18-110">Konsoliduotieji paketiniai užsakymai gali apimti bet kokį toliau nurodytų užsakymų derinį.</span><span class="sxs-lookup"><span data-stu-id="0dd18-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="0dd18-111">Vienas didelis užsakymas ir keli supakuotų prekių užsakymai</span><span class="sxs-lookup"><span data-stu-id="0dd18-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="0dd18-112">Keli dideli užsakymai ir keli supakuotų prekių užsakymai</span><span class="sxs-lookup"><span data-stu-id="0dd18-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="0dd18-113">Keli dideli užsakymai ir vienas supakuotų prekių užsakymas</span><span class="sxs-lookup"><span data-stu-id="0dd18-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="0dd18-114">Tik supakuotų prekių užsakymai</span><span class="sxs-lookup"><span data-stu-id="0dd18-114">Only packed orders</span></span>





