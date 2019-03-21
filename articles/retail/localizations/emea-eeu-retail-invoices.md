---
title: „Retail” kliento SF ir grąžinimo pardavimo užsakymai Rytų Europos šalyse
description: Šioje temoje aprašoma, kaip nustatyti informaciją apie kliento SF ir grąžinimo pardavimo užsakymus Rytų Europos šalyse.
author: epopov
manager: annbe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 34a31cee817447697b5d7d3e3ea2cfd2865d2bb1
ms.sourcegitcommit: 2cf5498098e7a5ade1c16eac6df26bc98e4565cd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/26/2019
ms.locfileid: "760711"
---
# <a name="retail-customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a><span data-ttu-id="aea94-103">„Retail” kliento SF ir grąžinimo pardavimo užsakymai Rytų Europos šalyse</span><span class="sxs-lookup"><span data-stu-id="aea94-103">Retail customer invoices and return sales orders in Eastern European countries</span></span>


[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aea94-104">Šioje temoje aprašoma, kaip nustatyti informaciją apie kliento SF ir grąžinimo pardavimo užsakymus Rytų Europos šalyse.</span><span class="sxs-lookup"><span data-stu-id="aea94-104">This topic describes how to set up information for customer invoices and return sales orders in Eastern European countries.</span></span>

<span data-ttu-id="aea94-105">Galite nustatyti toliau nurodytą kliento SF ir grąžinimo pardavimo užsakymų, sugeneruotų naudojantis mažmeninės prekybos elektroniniu kasos aparatu (EKA), informaciją.</span><span class="sxs-lookup"><span data-stu-id="aea94-105">You can set up the following information for customer invoices and return sales orders that are generated in Retail point of sale (POS).</span></span>

- <span data-ttu-id="aea94-106">Norėdami apdoroti grąžinimus naudodami grąžinimo pardavimo užsakymus, galite naudoti PVM grupes.</span><span class="sxs-lookup"><span data-stu-id="aea94-106">You can use sales tax groups to process returns by using return sales orders.</span></span> <span data-ttu-id="aea94-107">Eikite į **Mažmeninė prekyba \> Būstinės sąranka \> Parametrai \> Mažmeninės prekybos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="aea94-107">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="aea94-108">Atidarykite skirtuką **Registravimas \> Sąskaita faktūra**, tada nustatykite funkcijos **Taikyti PVM grupę grąžinimams** parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="aea94-108">Open the **Posting \> Invoice** tab, and then set **Use sales tax group for returns** to **Yes**.</span></span>

    * <span data-ttu-id="aea94-109">Norėdami nurodyti kliento atliktų grąžinimų PVM grupę, puslapyje **Klientai**, „FastTab“ skirtuko **Mažmeninė prekyba** lauke **PVM grupė, taikoma grąžinimams**, pasirinkite PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="aea94-109">To specify the sales tax group for returns that are made by a customer, on the **Customers** page, on the **Retail** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="aea94-110">Kai registruojate kliento grąžinimo pardavimo užsakymą, grąžinimo pardavimo užsakymo eilutė atnaujinama įtraukiant formoje **Klientas** nurodytą grąžinimų PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="aea94-110">When you post a return sales order for a customer, the return sales order line is updated with the sales tax group for returns that is specified in the **Customers** form.</span></span>
    * <span data-ttu-id="aea94-111">Norėdami nurodyti „Retail POS“ kliento atliktų grąžinimų PVM grupę, puslapyje **Parduotuvės**, „FastTab“ skirtuko **Bendra** lauke **PVM grupė, taikoma grąžinimams**, pasirinkite PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="aea94-111">To specify a sales tax group for returns that are made at a retail POS by a customer, on the **Stores** page, on the **General** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="aea94-112">Kai registruojate mažmeninės prekybos parduotuvės kliento grąžinimo pardavimo užsakymą, grąžinimo pardavimo užsakymo eilutė atnaujinama įtraukiant puslapyje **Parduotuvės** nurodytų grąžinimų PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="aea94-112">When you post a return sales order for a customer of a retail store, the return sales order line is updated with the sales tax group for returns that are specified on the **Stores** page.</span></span>

- <span data-ttu-id="aea94-113">Jei sąskaita faktūra arba grąžinimas neturi numatytosios pardavimo datos, kaip sąskaitos faktūros arba grąžinimo pardavimo datą galite naudoti mažmeninės prekybos kliento SF arba grąžinimo SF registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="aea94-113">You can use the posting date of a retail customer invoice or a return sales order as the sales date of the invoice or return if the invoice or return does not have a default sales date.</span></span> <span data-ttu-id="aea94-114">Eikite į **Mažmeninė prekyba \> Būstinės sąranka \> Parametrai \> Mažmeninės prekybos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="aea94-114">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="aea94-115">Atidarykite skirtuką **Registravimas \> Sąskaita faktūra**, paskui nustatykite funkcijos **Naudoti registravimo datą kaip pardavimo datą** parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="aea94-115">Open the **Posting \> Invoice** tab, and then set **Use posting date as sales date** to **Yes**.</span></span>
- <span data-ttu-id="aea94-116">Numeruodami Latvijos ir Lietuvos klientų SF ir grąžinimo pardavimo užsakymus galite naudoti mokesčių institucijų nurodytą numeraciją.</span><span class="sxs-lookup"><span data-stu-id="aea94-116">You can use the number range that is provided by the tax authorities to number Latvian and Lithuanian customer invoices and return sales orders.</span></span>

    * <span data-ttu-id="aea94-117">Pasirinkite **Organizacijos administravimas \> Numeracijos \> Skaitiklių valdymas**.</span><span class="sxs-lookup"><span data-stu-id="aea94-117">Go to **Organization administration \> Number sequences \> Counters management**.</span></span> <span data-ttu-id="aea94-118">Turi būti įrašas, kuriame **Modulis** = **Pardavimas** ir **Tipas** = **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="aea94-118">There should be a record where **Module** = **Sales** and **Type** = **Invoice**.</span></span>
    * <span data-ttu-id="aea94-119">Pasirinkite **Organizacijos administravimas \> Numeracijos \> SF numeravimo nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="aea94-119">Go to **Organization administration \> Number sequences \> Invoice numbering setup**.</span></span> <span data-ttu-id="aea94-120">Pažymėkite numeracijos eilutės, naudojamos kliento SF numeruoti, žymės langelį **Mažmeninė prekyba**.</span><span class="sxs-lookup"><span data-stu-id="aea94-120">Select the **Retail** check box for the number sequence line that is used to number the customer invoices.</span></span>
