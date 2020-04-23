---
title: SF naujinimas grąžinimams
description: Ši funkcija palaiko organizacijų, kurios pasirenka galimybę, kad grąžinimo užsakymai ir pardavimo užsakymai būtų išrašomi tuo pačiu metu ir to paties asmens, verslo procesus.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec803aaa2f750c43a1865c9536730b275e6ef1d4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202150"
---
# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="5388e-103">SF naujinimas grąžinimams</span><span class="sxs-lookup"><span data-stu-id="5388e-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5388e-104">Grąžinimo užsakymas yra pardavimo užsakymo, kuris pažymėtas kaip grąžintas užsakymas, tipas.</span><span class="sxs-lookup"><span data-stu-id="5388e-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="5388e-105">Todėl grąžinimo užsakymams generuoti naudojamas sąrašo puslapis **Visi pardavimo užsakymai**, o ne forma **Grąžinimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="5388e-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="5388e-106">Ši funkcija palaiko organizacijų, kurios pasirenka galimybę, kad grąžinimo užsakymai ir pardavimo užsakymai būtų išrašomi tuo pačiu metu ir to paties asmens, verslo procesus.</span><span class="sxs-lookup"><span data-stu-id="5388e-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="5388e-107">Grąžintos prekės SF suma yra neigiama, todėl ji vadinama kredito nota.</span><span class="sxs-lookup"><span data-stu-id="5388e-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="5388e-108">Kai nustatote paketinio vykdymo SF atnaujinimą, pardavimo užsakymo, kurio tipas **Grąžintas užsakymas**, grąžinimo eilutės būsena turi būti **Gauta**. Tai rodo, kad užsakymo važtaraštis atnaujintas.</span><span class="sxs-lookup"><span data-stu-id="5388e-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="5388e-109">Grąžinimo užsakymo SF registravimas</span><span class="sxs-lookup"><span data-stu-id="5388e-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="5388e-110">Spustelėkite **Gautinos sumos** \> **Bendros** \> **Pardavimo užsakymai** \> **Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="5388e-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="5388e-111">Pasirinkite pardavimo užsakymą, kurio lauke **Užsakymo tipas** rodoma **Grąžintas užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="5388e-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="5388e-112">Veiksmų srities skirtuke **Sąskaita faktūra** esančioje grupėje **Generuoti** spustelėkite **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="5388e-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="5388e-113">Skirtuke **Parametrai** pasirinkite žymės langelį **Registravimas**.</span><span class="sxs-lookup"><span data-stu-id="5388e-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="5388e-114">Peržiūrėkite formoje pateiktą informaciją ir visus reikiamus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="5388e-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="5388e-115">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5388e-115">Click **OK**.</span></span> <span data-ttu-id="5388e-116">Kredito nota užregistruota.</span><span class="sxs-lookup"><span data-stu-id="5388e-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="5388e-117">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="5388e-117">See also</span></span>

[<span data-ttu-id="5388e-118">Važtaraščių naujinimas grąžinimams</span><span class="sxs-lookup"><span data-stu-id="5388e-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  


