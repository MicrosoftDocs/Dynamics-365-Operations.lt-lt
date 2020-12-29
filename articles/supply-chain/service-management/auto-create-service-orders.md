---
title: Automatinis aptarnavimo užsakymų kūrimas
description: Galite generuoti aptarnavimo užsakymus, pagrįstus aptarnavimo sutartimi, skirta galiojančiam aptarnavimo sutarties laikotarpiui.
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
ms.openlocfilehash: 08fb7363ab87fd6a7f3d38406e72b1f542dc2c2a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433772"
---
# <a name="automatically-create-service-orders"></a><span data-ttu-id="e4e26-103">Automatinis aptarnavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="e4e26-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e4e26-104">Galite generuoti aptarnavimo užsakymus, pagrįstus aptarnavimo sutartimi, skirta galiojančiam aptarnavimo sutarties laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="e4e26-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="e4e26-105">Aptarnavimo užsakymai, kurie generuojami iš aptarnavimo sutarties, pridedami prie tos aptarnavimo sutarties.</span><span class="sxs-lookup"><span data-stu-id="e4e26-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="e4e26-106">Aptarnavimo užsakymai generuojami automatiškai, naudojant šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="e4e26-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="e4e26-107">Aptarnavimo sutarties intervalas, kuris nustatytas aptarnavimo sutarties eilutėse.</span><span class="sxs-lookup"><span data-stu-id="e4e26-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="e4e26-108">Aptarnavimo sutarties intervalas rodo dažnumą, kuriuo sukuriamos aptarnavimo užsakymo eilutės.</span><span class="sxs-lookup"><span data-stu-id="e4e26-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="e4e26-109">Daugiau informacijos žr. [Aptarnavimo intervalai](service-intervals.md).</span><span class="sxs-lookup"><span data-stu-id="e4e26-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="e4e26-110">Laikotarpis, nustatomas apibrėžti aptarnavimo laikotarpį laukuose **Pradžios data** ir **Pabaigos data**, esančiuose formoje **Kurti aptarnavimo užsakymus**.</span><span class="sxs-lookup"><span data-stu-id="e4e26-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="e4e26-111">Daugiau informacijos žr. [Automatiškai kurti aptarnavimo užsakymus](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="e4e26-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="e4e26-112">Parinktis **Jungti aptarnavimo užsakymus** aptarnavimo sutarties antraštėje.</span><span class="sxs-lookup"><span data-stu-id="e4e26-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="e4e26-113">Ši parinktis apibrėžia, ar aptarnavimo užsakymo eilutės, sugeneruotos iš aptarnavimo sutarties, sujungia aptarnavimo užsakymus pagal darbuotoją, aptarnavimo užduotį, aptarnavimo objektą arba aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="e4e26-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="e4e26-114">Daugiau informacijos žr. [Jungti aptarnavimo užsakymus](combine-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="e4e26-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="e4e26-115">Parinktis **Laiko langas** aptarnavimo sutarties eilutėje.</span><span class="sxs-lookup"><span data-stu-id="e4e26-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="e4e26-116">Laiko langas apibrėžia, kiek aptarnavimo užsakymo eilutė gali būti perkelta, atsižvelgiant į jos apskaičiuotą datą.</span><span class="sxs-lookup"><span data-stu-id="e4e26-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="e4e26-117">Daugiau informacijos žr. [Laiko langai](time-windows.md).</span><span class="sxs-lookup"><span data-stu-id="e4e26-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="e4e26-118">Jeigu aptarnavimo užsakymui nurodyta diena neatidaryta kalendoriuje, kurį pasirinkote formoje <STRONG>Aptarnavimo valdymo parametrai</STRONG>, gausite pranešimą, kad yra kalendoriaus konfliktas.</span><span class="sxs-lookup"><span data-stu-id="e4e26-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="e4e26-119">Galima saugiai nepaisyti pranešimo; aptarnavimo užsakymas bus sukurtas net jei diena kalendoriuje uždaryta.</span><span class="sxs-lookup"><span data-stu-id="e4e26-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="e4e26-120">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e4e26-120">Example 1</span></span>

<span data-ttu-id="e4e26-121">Aptarnavimo sutartis galioja nuo 2012 m. sausio 1 d. iki 2012 m. gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="e4e26-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="e4e26-122">Jei aptarnavimo laikotarpis, kurį nurodėte formoje **Kurti aptarnavimo užsakymus** yra nuo 2012 m. lapkričio 1 d. iki 2013 m. vasario 1 d., aptarnavimo užsakymai kuriami nuo 2012 m. lapkričio 1 d. iki 2012 iki 2012 m. gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="e4e26-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="e4e26-123">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e4e26-123">Example 2</span></span>

<span data-ttu-id="e4e26-124">Aptarnavimo sutartis galioja nuo 2012 m. sausio 1 d. iki 2012 m. gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="e4e26-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="e4e26-125">Dvi aptarnavimo sutarties eilutės pridėtos prie aptarnavimo sutarties.</span><span class="sxs-lookup"><span data-stu-id="e4e26-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="e4e26-126">Pirmosios aptarnavimo sutarties eilutės pradžios data yra 2012 m. sausio 2 d., o pabaigos data yra 2012 m. kovo 1 d.</span><span class="sxs-lookup"><span data-stu-id="e4e26-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="e4e26-127">Antrosios aptarnavimo sutarties eilutės pradžios data yra 2012 m. balandžio 1 d., o pabaigos data yra 2012 m. gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="e4e26-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="e4e26-128">Formoje **Kurti aptarnavimo užsakymus** galite nurodyti laikotarpį nuo 2012 m. spalio 1 d. iki 2012 m. gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="e4e26-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="e4e26-129">Todėl aptarnavimo užsakymai generuojami tik antrai sutarties eilutei, nes pirmos sutarties eilutės pradžios data ir pabaigos data yra ankstesnės nei aptarnavimo užsakyme nurodytas laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="e4e26-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  


