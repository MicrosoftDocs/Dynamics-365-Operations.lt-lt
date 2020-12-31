---
title: Vidinės įmonės užsakymų filtravimas siekiant išvengti užsakymų ir užsakymų eilučių sinchronizavimo
description: Šioje temoje aprašoma, kaip filtruoti vidinės įmonės užsakymus siekiant išvengti užsakymų ir užsakymų eilučių sinchronizavimo.
author: negudava
manager: tfehr
ms.date: 11/09/2020
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
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701038"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="8f5d3-103">Vidinės įmonės užsakymų filtravimas siekiant išvengti užsakymų ir užsakymų eilučių sinchronizavimo</span><span class="sxs-lookup"><span data-stu-id="8f5d3-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f5d3-104">Galite filtruoti vidinės įmonės užsakymus siekdami išvengti **užsakymų** ir **užsakymų eilučių** sinchronizavimo.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="8f5d3-105">Kai kuriais atvejais vidinės įmonės užsakymo informacija nėra būtina kliento programos įjungimo programėlėje.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="8f5d3-106">Kiekvienas iš standartinių „Common Data Service“ objektų yra išplečiamas su nuorodomis į lauką **IntercompanyOrder**, o dvejopo rašymo žemėlapiai modifikuojami, kad būtų galima nurodyti papildomus filtrų laukus.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="8f5d3-107">Rezultatas yra tai, kad vidinės įmonės užsakymai nebėra sinchronizuojami.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="8f5d3-108">Šis procesas padeda išvengti nereikalingų duomenų „Customer Engagement“ programoje.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="8f5d3-109">Įtraukite nuorodą į **IntercompanyOrder** į **CDS pardavimo užsakymų antraštės**.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="8f5d3-110">Jis užpildomas tik vidinės įmonės užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="8f5d3-111">Laukas **IntercompanyOrder** siūlomas **Pardavimo lentelėje**.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Susieti išdėstymą su paskirties vieta, SalesOrderHeader":::
    
2. <span data-ttu-id="8f5d3-113">Išplėtus **CDS pardavimo užsakymų antraštės**, lauką **IntercompanyOrder** galima susieti.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="8f5d3-114">Taikykite filtrą teikdami užklausos eilutę `INTERCOMPANYORDER == ""`.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Pardavimo užsakymų antraštės, redaguoti užklausą":::

3. <span data-ttu-id="8f5d3-116">Įtraukite nuorodą į **IntercompanyInventTransId** į **CDS pardavimo užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="8f5d3-117">Jis užpildomas tik vidinės įmonės užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="8f5d3-118">Laukas **InterCompanyInventTransID** siūlomas **Pardavimo eilutėje**.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Susieti išdėstymą su paskirties vieta, SalesOrderLine":::

4. <span data-ttu-id="8f5d3-120">Išplėtus **CDS pardavimo užsakymų eilutės**, lauką **IntercompanyInventTransId** galima susieti.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="8f5d3-121">Taikykite filtrą teikdami užklausos eilutę `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Pardavimo užsakymo eilutės, redaguoti užklausą":::

5. <span data-ttu-id="8f5d3-123">Išplėskite **Pardavimo SF antraštės V2** ir **Pardavimo SF eilutės V2** taip pat, kaip išplečiate „Common Data Service“ objektus atlikdami 1 ir 2 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="8f5d3-124">Tada pridėkite filtrų užklausas.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-124">Then add the filter queries.</span></span> <span data-ttu-id="8f5d3-125">**Pardavimo SF antraštės V2** filtro eilutė yra `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="8f5d3-126">**Pardavimo SF eilutės V2** filtro eilutė yra `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Susieti išdėstymą su paskirties vieta, Pardavimo SF antraštės":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Pardavimo SF antraštės, redaguoti užklausą":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Pardavimo SF eilutės, redaguoti užklausą":::

6. <span data-ttu-id="8f5d3-130">Objektas **Pasiūlymai** neturi vidinės įmonės ryšio.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="8f5d3-131">Jei kas nors iš vidinės įmonės klientų sukuria pasiūlymą, visi šie klientai gali nustatyti vienoje klientų grupėje naudodami lauką **CustGroup**.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="8f5d3-132">Antraštė ir eilutės gali būti išplėstos, kad būtų galima įtraukti lauką **CustGroup**, o tada filtruoti, kad nebūtų įtraukta ši grupė.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Susieti išdėstymą su paskirties vieta, Pardavimo pasiūlymo antraštė":::

7. <span data-ttu-id="8f5d3-134">Išplėtę objektą **Pasiūlymai**, pritaikykite filtrą su užklausos eilute `CUSTGROUP !=  "<company>"`.</span><span class="sxs-lookup"><span data-stu-id="8f5d3-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Pardavimo pasiūlymo antraštė, redaguoti užklausą":::
