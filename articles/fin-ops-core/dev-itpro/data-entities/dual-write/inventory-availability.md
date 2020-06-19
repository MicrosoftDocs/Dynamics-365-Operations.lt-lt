---
title: Atsargų pasiekiamumas dvigubam rašymui
description: Šioje temoje pateikiama informacija apie atsargų pasiekiamumo tikrinimą dvigubo rašymo funkcijoje.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426987"
---
# <a name="inventory-availability"></a><span data-ttu-id="01a9a-103">Atsargų pasiekiamumas</span><span class="sxs-lookup"><span data-stu-id="01a9a-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="01a9a-104">Naudodami atsargų pasiekiamumą, galite patikrinti savo atsargas prieš įtraukdami produktą į formas **Pasiūlymai**, **Užsakymai** arba **Sąskaitos-faktūros** modeliu grįstose programose programoje „Dynamics 365“.</span><span class="sxs-lookup"><span data-stu-id="01a9a-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="01a9a-105">Pavyzdžiui, atsargų ir įvykdymo datos tikrinimas yra pagrindinė [potencialių klientų pavertime grynaisiais pinigais](dual-write-prospect-to-cash.md) proceso užduotis.</span><span class="sxs-lookup"><span data-stu-id="01a9a-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="01a9a-106">Jeigu nepakanka atsargų, galite įvertinti pristatymo datą pagal suplanuotų atsargų gavimą ir išdavimą.</span><span class="sxs-lookup"><span data-stu-id="01a9a-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="01a9a-107">Taip pat galite patikrinti produkto prieinamų atsargų (ATP) informaciją, kurioje galima rasti ATP kiekį iš anksto apibrėžtame laikotarpyje.</span><span class="sxs-lookup"><span data-stu-id="01a9a-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="01a9a-108">Turimos atsargos</span><span class="sxs-lookup"><span data-stu-id="01a9a-108">On-hand Inventory</span></span> 

<span data-ttu-id="01a9a-109">„Dynamics 365 Sales“ formų **Pasiūlymai**, **Užsakymai** arba **Sąskaitos faktūros** antraštėje įtraukiamas mygtukas **Turimos atsargos**.</span><span class="sxs-lookup"><span data-stu-id="01a9a-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="01a9a-110">Spustelėjus mygtuką, pasirodo dialogo langas, kuriame galite nurodyti įmonę ir produktą, kurio turimas atsargas norite patikrinti.</span><span class="sxs-lookup"><span data-stu-id="01a9a-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="01a9a-111">Jis pateikia atsargų informaciją iš „Dynamics 365 Supply Chain Management“ ir parodo tokią pačią informaciją kaip [Turimos atsargos](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="01a9a-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="01a9a-112">Informaciją sudaro šie kiekiai:</span><span class="sxs-lookup"><span data-stu-id="01a9a-112">The information includes these quantities:</span></span>

- <span data-ttu-id="01a9a-113">**Turimas kiekis**</span><span class="sxs-lookup"><span data-stu-id="01a9a-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="01a9a-114">**Rezervuotas turimas kiekis**</span><span class="sxs-lookup"><span data-stu-id="01a9a-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="01a9a-115">**Pasiekiamas turimas kiekis**</span><span class="sxs-lookup"><span data-stu-id="01a9a-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="01a9a-116">**Užsakytas kiekis**</span><span class="sxs-lookup"><span data-stu-id="01a9a-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="01a9a-117">**Užsakymo kiekis**</span><span class="sxs-lookup"><span data-stu-id="01a9a-117">**On-order Quantity**</span></span>
- <span data-ttu-id="01a9a-118">**Rezervuotas užsakytas kiekis**</span><span class="sxs-lookup"><span data-stu-id="01a9a-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="01a9a-119">**Visas pasiekiamas kiekis**</span><span class="sxs-lookup"><span data-stu-id="01a9a-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="01a9a-120">ATP informacija</span><span class="sxs-lookup"><span data-stu-id="01a9a-120">ATP information</span></span>

<span data-ttu-id="01a9a-121">„Dynamics 365 Sales“ formų **Pasiūlymai**, **Užsakymai** arba **Sąskaitos faktūros** antraštės internetiniuose elementuose įtraukiamas mygtukas **ATP informacija**.</span><span class="sxs-lookup"><span data-stu-id="01a9a-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="01a9a-122">Spustelėjus mygtuką, pasirodo dialogo langas, kuriame galite nurodyti įmonę, produktą, atsargų svetainę, atsargų sandėlį ir užsakymo kiekį.</span><span class="sxs-lookup"><span data-stu-id="01a9a-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="01a9a-123">Jis pateikia **ATP informaciją** iš „Supply Chain Management“ ir parodo parametrus, aprašytus [Užsakymų vykdymo perspektyva](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="01a9a-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="01a9a-124">Informaciją sudaro **ATP kiekis**, **Gaunamas kiekis**, **Išduodamas kiekis**ir **Turimas kiekis**.</span><span class="sxs-lookup"><span data-stu-id="01a9a-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
