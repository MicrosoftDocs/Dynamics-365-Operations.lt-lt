---
title: Stebėti pardavimo ir maržos efektyvumą
description: Nauodami „Dynamics 365 Commerce“, galite realiu laiku stebėti pardavimo ir maržos našumą.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a7b2b6ba8115b43ef2e52e934bf8364e6f4044e7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023481"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="424cb-103">Pardavimo ir maržos efektyvumo stebėjimas</span><span class="sxs-lookup"><span data-stu-id="424cb-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="424cb-104">Nauodami „Dynamics 365 Commerce“, galite realiu laiku stebėti pardavimo ir maržos našumą.</span><span class="sxs-lookup"><span data-stu-id="424cb-104">You can monitor sales and margin performance in real time using Dynamics 365 Commerce.</span></span>

<span data-ttu-id="424cb-105">„Commerce“ vartotojai gali realiu laiku stebėti pardavimus ir maržos našumą įvairiuose organizacijos lygiuose pagal šias dimensijas:</span><span class="sxs-lookup"><span data-stu-id="424cb-105">As part of Commerce, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="424cb-106">Produktai</span><span class="sxs-lookup"><span data-stu-id="424cb-106">Products</span></span>
- <span data-ttu-id="424cb-107">Kategorijos</span><span class="sxs-lookup"><span data-stu-id="424cb-107">Categories</span></span>
- <span data-ttu-id="424cb-108">Nuolaidos</span><span class="sxs-lookup"><span data-stu-id="424cb-108">Discounts</span></span>
- <span data-ttu-id="424cb-109">Metai kaip laikotarpis</span><span class="sxs-lookup"><span data-stu-id="424cb-109">Years as time period</span></span>
- <span data-ttu-id="424cb-110">Registrai / terminalai</span><span class="sxs-lookup"><span data-stu-id="424cb-110">Registers/terminals</span></span>
- <span data-ttu-id="424cb-111">Personalas / darbuotojai</span><span class="sxs-lookup"><span data-stu-id="424cb-111">Staff/employees</span></span>
- <span data-ttu-id="424cb-112">Klientai</span><span class="sxs-lookup"><span data-stu-id="424cb-112">Customers</span></span>
- <span data-ttu-id="424cb-113">Valdymo vienetai</span><span class="sxs-lookup"><span data-stu-id="424cb-113">Operating units</span></span>

<span data-ttu-id="424cb-114">Be to, dvi unikalios ataskaitos, kuriose naudojama hierarchinio tinklelio struktūra, leidžia vartotojams stebėti pardavimus ir maržos našumą numatytoje produktų kategorijų hierarchijoje, pereinant nuo viršutinės kategorijos mazgo prie atskirų kategorijos lapo mazgų.</span><span class="sxs-lookup"><span data-stu-id="424cb-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default product category hierarchy.</span></span> <span data-ttu-id="424cb-115">Vartotojai taip pat gali detalizuoti, pradedant nuo viršutinio valdymo bloko ir baigiant atskiru kanalu organizacijos hierarchijoje, kuris apibrėžiamas kaip numatytoji organizacijos hierarchija ataskaitoms teikti.</span><span class="sxs-lookup"><span data-stu-id="424cb-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for reporting.</span></span> <span data-ttu-id="424cb-116">Atidaryti ataskaitas galite iš bet kurios iš tolesnių vietų.</span><span class="sxs-lookup"><span data-stu-id="424cb-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="424cb-117">Darbo sritis **Parduotuvių valdymas** &gt; **„Retail and Commerce“** &gt; **Kanalai** &gt; **Parduotuvių valdymas** &gt; **Ataskaitos**</span><span class="sxs-lookup"><span data-stu-id="424cb-117">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="424cb-118">Darbo sritis **Kategorijų ir produktų valdymas** &gt; **„Retail and Commerce“** &gt; **Produktai ir kategorijos** &gt; **Parduotuvių valdymas** &gt; **Ataskaitos**</span><span class="sxs-lookup"><span data-stu-id="424cb-118">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Product and categories** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="424cb-119">Darbo sritis **Kainos ir nuolaidos valdymas** &gt; **„Retail and Commerce“** &gt; **Kainos ir nuolaidos** &gt; **Parduotuvių valdymas** &gt; **Ataskaitos**</span><span class="sxs-lookup"><span data-stu-id="424cb-119">**Pricing and discount management** workspace &gt; **Retail and Commerce** &gt; **Pricing and discounts** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="424cb-120">Skyrius **Užklausos ir ataskaitos** &gt; **„Retail and Commerce“** &gt; **Užklausos ir ataskaitos** &gt; **Pardavimų ataskaitos**</span><span class="sxs-lookup"><span data-stu-id="424cb-120">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>