---
title: Vidinės įmonės užsakymų filtravimas siekiant išvengti užsakymų ir jų eilučių sinchronizavimo
description: Šioje temoje paaiškinama, kaip filtruoti vidinės įmonės užsakymus, kad objektai Užsakymai ir Užsakymų eilutės nebūtų sinchronizuojami.
author: negudava
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 123427db61782490d348489c23e0eaf5f8b513c9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748646"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="30619-103">Vidinės įmonės užsakymų filtravimas siekiant išvengti užsakymų ir jų eilučių sinchronizavimo</span><span class="sxs-lookup"><span data-stu-id="30619-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30619-104">Galite filtruoti vidinės įmonės užsakymus, kad lentelės **Užsakymų** ir **Užsakymų eilutės** nebūtų sinchronizuojamos.</span><span class="sxs-lookup"><span data-stu-id="30619-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="30619-105">Kai kuriais atvejais vidinės įmonės užsakymo informacija nėra reikalinga „Customer Engagement” programoje.</span><span class="sxs-lookup"><span data-stu-id="30619-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="30619-106">Kiekviena iš standartinių „Dataverse“ lentelių yra išplečiamas per nuorodomis į **Vidinės įmonės užsakymas** lauką, o dvejopo rašymo žemėlapiai modifikuojami, kad būtų galima nurodyti papildomus filtrų stulpelius.</span><span class="sxs-lookup"><span data-stu-id="30619-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="30619-107">Todėl vidinės įmonės užsakymai yra nebesinchronizuojami.</span><span class="sxs-lookup"><span data-stu-id="30619-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="30619-108">Šis procesas padeda neleisti nereikalingų duomenų „Customer Engagement“ programoje.</span><span class="sxs-lookup"><span data-stu-id="30619-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="30619-109">Išplėskite **CDS pardavimo užsakymų antraštės** lentelę įtraukdami nuorodą į **Vidinės įmonės užsakymo** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="30619-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="30619-110">Šis stulpelis pildomas tik vidinės įmonės užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="30619-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="30619-111">Stulpelis **Vidinės įmonės užsakymas** prieinamas **Pardavimo lentelė** lentelėje.</span><span class="sxs-lookup"><span data-stu-id="30619-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Susieti išdėstymą su paskirties vietos puslapiu CDS pardavimo užsakymo antraštėms":::

2. <span data-ttu-id="30619-113">Išplėtus **CDS pardavimo užsakymų antraštės**, stulpelį **Vidinės įmonės užsakymas** galima susieti.</span><span class="sxs-lookup"><span data-stu-id="30619-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="30619-114">Taikykite filtrą su `INTERCOMPANYORDER == ""` užklausos eilute.</span><span class="sxs-lookup"><span data-stu-id="30619-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Redaguoti CDS pardavimo užsakymo antraščių užklausos dialogo langą":::

3. <span data-ttu-id="30619-116">Išplėskite **CDS pardavimo užsakymų eilutės** lentelę įtraukdami nuorodą į **Vidinės įmonės TransId** stulpelį.</span><span class="sxs-lookup"><span data-stu-id="30619-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="30619-117">Šis stulpelis pildomas tik vidinės įmonės užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="30619-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="30619-118">Stulpelis **Vidinės įmonės TransId** prieinamas **Pardavimo eilutė** lentelėje.</span><span class="sxs-lookup"><span data-stu-id="30619-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Susieti išdėstymą su paskirties vietos puslapiu CDS pardavimo užsakymo eilutėms":::

4. <span data-ttu-id="30619-120">Išplėtus **CDS pardavimo užsakymų eilutės**, stulpelį **IntercompanyInventTransId** galima susieti.</span><span class="sxs-lookup"><span data-stu-id="30619-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="30619-121">Taikykite filtrą su `INTERCOMPANYINVENTTRANSID == ""` užklausos eilute.</span><span class="sxs-lookup"><span data-stu-id="30619-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Redaguoti CDS pardavimo užsakymo eilučių užklausos dialogo langą":::

5. <span data-ttu-id="30619-123">Norėdami išplėsti lentelę **Pardavimo sąskaitos faktūros antraštė V2** ir pridėti filtro užklausą, pakartokite 1 ir 2 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="30619-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="30619-124">Šiuo atveju naudokite `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` filtro užklausos eilutę.</span><span class="sxs-lookup"><span data-stu-id="30619-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Susieti išdėstymą su paskirties vietos puslapiu pardavimo sąskaitos faktūros antraštei V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Redaguoti pardavimo sąskaitos faktūros antraštės V2 užklausos dialogo langą":::

6. <span data-ttu-id="30619-127">Norėdami išplėsti lentelę **Pardavimo sąskaitos faktūros eilutės V2** ir pridėti filtro užklausą, pakartokite 3 ir 4 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="30619-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="30619-128">Šiuo atveju naudokite `INTERCOMPANYINVENTTRANSID == ""` filtro užklausos eilutę.</span><span class="sxs-lookup"><span data-stu-id="30619-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Redaguoti pardavimo sąskaitos faktūros eilutės V2 užklausos dialogo langą":::

7. <span data-ttu-id="30619-130">Lentelė **Pasiūlymai** neturi vidinės įmonės ryšio.</span><span class="sxs-lookup"><span data-stu-id="30619-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="30619-131">Jei kuris nors iš vidinės įmonės klientų sukuria pasiūlymą, galite naudoti stulpelį **Pasirinktinė grupė** tam, kad įdėtumėte šiuos visus klientus į vieną klientų grupę.</span><span class="sxs-lookup"><span data-stu-id="30619-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="30619-132">Įtraukdami stulpelį **Pasirinktinė grupė** galite išplėsti antraštę ir eilutes, o tada filtruoti, kad ta grupė nebūtų įtraukta.</span><span class="sxs-lookup"><span data-stu-id="30619-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Susieti išdėstymą su paskirties vietos puslapiu CDS pardavimų pasiūlymų antraštei":::

8. <span data-ttu-id="30619-134">Po to, kai **Pasiūlymai** išplečiami, pritaikykite filtrą su `CUSTGROUP != "<company>"` užklausos eilute.</span><span class="sxs-lookup"><span data-stu-id="30619-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Redaguoti CDS pardavimų pasiūlymo antraštės užklausos dialogo langą":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]