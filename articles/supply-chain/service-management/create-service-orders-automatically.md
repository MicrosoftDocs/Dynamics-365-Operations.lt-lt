---
title: Automatinis aptarnavimo užsakymų kūrimas
description: Galite kurti vienos ar kelių aptarnavimo sutarčių aptarnavimo užsakymus.
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 914df1626b02110264b895e82dc9301f3aa0afce
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985123"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="285e0-103">Automatinis aptarnavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="285e0-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="285e0-104">Galite kurti vienos ar kelių aptarnavimo sutarčių aptarnavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="285e0-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="285e0-105">Sukūrę aptarnavimo užsakymus, galite juos peržiūrėti formoje **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="285e0-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="285e0-106">Kuriami tik aptarnavimo sutarties galiojančio laikotarpio aptarnavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="285e0-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="285e0-107">Jei intervalas, kurį nurodote formoje **Kurti aptarnavimo užsakymus**, yra ankstesnis, nei aptarnavimo sutarties pradžios data, arba vėlesnis, nei aptarnavimo sutarties pabaigos data, kuriami tik tie aptarnavimo užsakymai, kurie apima intervalo dalį, kurią apima aptarnavimo sutarties datos.</span><span class="sxs-lookup"><span data-stu-id="285e0-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="285e0-108">Kai aptarnavimo užsakymus kuriate rankiniu arba automatiniu būdu iš aptarnavimo sutarties eilutės, aptarnavimo užsakymas turi būti tame pačiame laiko intervale, kuris nurodytas eilutės pradžios ir pabaigos data, nebent eilutėje nenurodėte pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="285e0-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="285e0-109">Aptarnavimo sutarties aptarnavimo užsakymų kūrimas automatiniu būdu</span><span class="sxs-lookup"><span data-stu-id="285e0-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="285e0-110">Spustelėkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="285e0-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="285e0-111">Pasirinkite aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="285e0-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="285e0-112">Spustelėkite skirtuką **Pristatyti**, tada spustelėkite **Suplanuoti aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="285e0-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="285e0-113">Laukuose **Pradžios data** ir **Pabaigos data** nurodykite datas, kad apibrėžtumėte aptarnavimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="285e0-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="285e0-114">Pažymėkite žymės langelį **Rodyti sistemos pranešimą**, kad būtų rodomas sukurtų aptarnavimo užsakymų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="285e0-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="285e0-115">Pasirinkite operacijų tipus laukų grupėje **Įtraukti operacijų tipus**.</span><span class="sxs-lookup"><span data-stu-id="285e0-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="285e0-116">Operacijų tipai vaizduoja eilutes, sukurtas aptarnavimo sutartyje, o kiekvienas pasirinktas operacijos tipas generuoja kelis aptarnavimo užsakymus, atsižvelgiant į aptarnavimo intervalą, nurodytą aptarnavimo sutarties eilutėje.</span><span class="sxs-lookup"><span data-stu-id="285e0-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="285e0-117">Pažymėkite žymės langelį **Ištisinis**, jei norite kurti visus aptarnavimo užsakymus, kurių trūksta nuoseklioje aptarnavimo užsakymų serijoje.</span><span class="sxs-lookup"><span data-stu-id="285e0-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="285e0-118">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="285e0-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="285e0-119">Kelių aptarnavimo sutarčių aptarnavimo užsakymų kūrimas automatiniu būdu</span><span class="sxs-lookup"><span data-stu-id="285e0-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="285e0-120">Spustelėkite **Aptarnavimo valdymas** \> **Periodinis** \> **Aptarnavimo užsakymai** \> **Kurti aptarnavimo užsakymus**.</span><span class="sxs-lookup"><span data-stu-id="285e0-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="285e0-121">Spustelėkite **Pasirinkti**, kad pridėtumėte arba pašalintumėte kriterijus, kurie bus naudojami aptarnavimo užsakymams kurti.</span><span class="sxs-lookup"><span data-stu-id="285e0-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="285e0-122">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="285e0-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="285e0-123">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="285e0-123">See also</span></span>

[<span data-ttu-id="285e0-124">Aptarnavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="285e0-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="285e0-125">Automatinis aptarnavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="285e0-125">Automatically create service orders</span></span>](auto-create-service-orders.md)

  


