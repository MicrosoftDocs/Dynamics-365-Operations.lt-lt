---
title: Stebėti pardavimo ir maržos efektyvumą
description: Naudodami „Dynamics 365 Commerce“, galite realiu laiku stebėti pardavimo ir maržos našumą.
author: ashishmsft
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a7ea2bd9388e2fcfc6ae5f17d61054092cbac58c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796951"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="d7ba2-103">Pardavimo ir maržos efektyvumo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="d7ba2-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d7ba2-104">Naudodami „Dynamics 365 Commerce“, galite realiu laiku stebėti pardavimo ir maržos našumą.</span><span class="sxs-lookup"><span data-stu-id="d7ba2-104">You can monitor sales and margin performance in real time using Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d7ba2-105">„Commerce“ vartotojai gali realiu laiku stebėti pardavimus ir maržos našumą įvairiuose organizacijos lygiuose pagal šias dimensijas:</span><span class="sxs-lookup"><span data-stu-id="d7ba2-105">As part of Commerce, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="d7ba2-106">Produktai</span><span class="sxs-lookup"><span data-stu-id="d7ba2-106">Products</span></span>
- <span data-ttu-id="d7ba2-107">Kategorijos</span><span class="sxs-lookup"><span data-stu-id="d7ba2-107">Categories</span></span>
- <span data-ttu-id="d7ba2-108">Nuolaidos</span><span class="sxs-lookup"><span data-stu-id="d7ba2-108">Discounts</span></span>
- <span data-ttu-id="d7ba2-109">Metai kaip laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d7ba2-109">Years as time period</span></span>
- <span data-ttu-id="d7ba2-110">Registrai / terminalai</span><span class="sxs-lookup"><span data-stu-id="d7ba2-110">Registers/terminals</span></span>
- <span data-ttu-id="d7ba2-111">Personalas / darbuotojai</span><span class="sxs-lookup"><span data-stu-id="d7ba2-111">Staff/employees</span></span>
- <span data-ttu-id="d7ba2-112">Klientai</span><span class="sxs-lookup"><span data-stu-id="d7ba2-112">Customers</span></span>
- <span data-ttu-id="d7ba2-113">Valdymo vienetai</span><span class="sxs-lookup"><span data-stu-id="d7ba2-113">Operating units</span></span>

<span data-ttu-id="d7ba2-114">Be to, dvi unikalios ataskaitos, kuriose naudojama hierarchinio tinklelio struktūra, leidžia vartotojams stebėti pardavimus ir maržos našumą numatytoje produktų kategorijų hierarchijoje, pereinant nuo viršutinės kategorijos mazgo prie atskirų kategorijos lapo mazgų.</span><span class="sxs-lookup"><span data-stu-id="d7ba2-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default product category hierarchy.</span></span> <span data-ttu-id="d7ba2-115">Vartotojai taip pat gali detalizuoti, pradedant nuo viršutinio valdymo bloko ir baigiant atskiru kanalu organizacijos hierarchijoje, kuris apibrėžiamas kaip numatytoji organizacijos hierarchija ataskaitoms teikti.</span><span class="sxs-lookup"><span data-stu-id="d7ba2-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for reporting.</span></span> <span data-ttu-id="d7ba2-116">Atidaryti ataskaitas galite iš bet kurios iš tolesnių vietų.</span><span class="sxs-lookup"><span data-stu-id="d7ba2-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="d7ba2-117">Darbo sritis **Parduotuvių valdymas** &gt; **Mažmeninė prekyba ir komercija** &gt; **Kanalai** &gt; **Parduotuvių valdymas** &gt; **Ataskaitos**</span><span class="sxs-lookup"><span data-stu-id="d7ba2-117">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="d7ba2-118">Darbo sritis **Kategorijų ir produktų valdymas** &gt; **Mažmeninė prekyba ir komercija** &gt; **Produktai ir kategorijos** &gt; **Parduotuvių valdymas** &gt; **Ataskaitos**</span><span class="sxs-lookup"><span data-stu-id="d7ba2-118">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Product and categories** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="d7ba2-119">Darbo sritis **Kainos ir nuolaidos valdymas** &gt; **Mažmeninė prekyba ir komercija** &gt; **Kainos ir nuolaidos** &gt; **Parduotuvių valdymas** &gt; **Ataskaitos**</span><span class="sxs-lookup"><span data-stu-id="d7ba2-119">**Pricing and discount management** workspace &gt; **Retail and Commerce** &gt; **Pricing and discounts** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="d7ba2-120">Skyrius **Užklausos ir ataskaitos** &gt; **Mažmeninė prekyba ir komercija** &gt; **Užklausos ir ataskaitos** &gt; **Pardavimų ataskaitos**</span><span class="sxs-lookup"><span data-stu-id="d7ba2-120">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]