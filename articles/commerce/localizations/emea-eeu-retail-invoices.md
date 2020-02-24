---
title: Klientų SF ir grąžinimo pardavimo užsakymai Rytų Europos šalyse
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
ms.openlocfilehash: a00a960142b0e3955c80d75f7963f4827209bf75
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004708"
---
# <a name="customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a><span data-ttu-id="c6b51-103">Klientų SF ir grąžinimo pardavimo užsakymai Rytų Europos šalyse</span><span class="sxs-lookup"><span data-stu-id="c6b51-103">Customer invoices and return sales orders in Eastern European countries</span></span>


[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6b51-104">Šioje temoje aprašoma, kaip nustatyti informaciją apie kliento SF ir grąžinimo pardavimo užsakymus Rytų Europos šalyse.</span><span class="sxs-lookup"><span data-stu-id="c6b51-104">This topic describes how to set up information for customer invoices and return sales orders in Eastern European countries.</span></span>

<span data-ttu-id="c6b51-105">Galite nustatyti toliau nurodytą kliento SF ir grąžinimo pardavimo užsakymų, sugeneruotų naudojantis mažmeninės prekybos elektroniniu kasos aparatu (EKA), informaciją.</span><span class="sxs-lookup"><span data-stu-id="c6b51-105">You can set up the following information for customer invoices and return sales orders that are generated in Retail point of sale (POS).</span></span>

- <span data-ttu-id="c6b51-106">Norėdami apdoroti grąžinimus naudodami grąžinimo pardavimo užsakymus, galite naudoti PVM grupes.</span><span class="sxs-lookup"><span data-stu-id="c6b51-106">You can use sales tax groups to process returns by using return sales orders.</span></span> <span data-ttu-id="c6b51-107">Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Parametrai \> Prekybos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c6b51-107">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="c6b51-108">Atidarykite skirtuką **Registravimas \> Sąskaita faktūra**, tada nustatykite funkcijos **Taikyti PVM grupę grąžinimams** parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="c6b51-108">Open the **Posting \> Invoice** tab, and then set **Use sales tax group for returns** to **Yes**.</span></span>

    * <span data-ttu-id="c6b51-109">Norėdami nurodyti kliento atliktų grąžinimų PVM grupę, puslapyje **Klientai**, „FastTab“ **Prekyba** lauke **PVM grupė, taikoma grąžinimams**, pasirinkite PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="c6b51-109">To specify the sales tax group for returns that are made by a customer, on the **Customers** page, on the **Commerce** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="c6b51-110">Kai registruojate kliento grąžinimo pardavimo užsakymą, grąžinimo pardavimo užsakymo eilutė atnaujinama įtraukiant formoje **Klientas** nurodytą grąžinimų PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="c6b51-110">When you post a return sales order for a customer, the return sales order line is updated with the sales tax group for returns that is specified in the **Customers** form.</span></span>
    * <span data-ttu-id="c6b51-111">Norėdami nurodyti „Retail POS“ kliento atliktų grąžinimų PVM grupę, puslapyje **Parduotuvės**, „FastTab“ skirtuko **Bendra** lauke **PVM grupė, taikoma grąžinimams**, pasirinkite PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="c6b51-111">To specify a sales tax group for returns that are made at a retail POS by a customer, on the **Stores** page, on the **General** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="c6b51-112">Kai registruojate parduotuvės kliento grąžinimo pardavimo užsakymą, grąžinimo pardavimo užsakymo eilutė atnaujinama įtraukiant puslapyje **Parduotuvės** nurodytų grąžinimų PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="c6b51-112">When you post a return sales order for a customer of a  store, the return sales order line is updated with the sales tax group for returns that are specified on the **Stores** page.</span></span>

- <span data-ttu-id="c6b51-113">Jei sąskaita faktūra arba grąžinimas neturi numatytosios pardavimo datos, kaip sąskaitos faktūros arba grąžinimo pardavimo datą galite naudoti kliento SF arba grąžinimo SF registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="c6b51-113">You can use the posting date of a customer invoice or a return sales order as the sales date of the invoice or return if the invoice or return does not have a default sales date.</span></span> <span data-ttu-id="c6b51-114">Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Parametrai \> Prekybos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c6b51-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="c6b51-115">Atidarykite skirtuką **Registravimas \> Sąskaita faktūra**, paskui nustatykite funkcijos **Naudoti registravimo datą kaip pardavimo datą** parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="c6b51-115">Open the **Posting \> Invoice** tab, and then set **Use posting date as sales date** to **Yes**.</span></span>
- <span data-ttu-id="c6b51-116">Numeruodami Latvijos ir Lietuvos klientų SF ir grąžinimo pardavimo užsakymus galite naudoti mokesčių institucijų nurodytą numeraciją.</span><span class="sxs-lookup"><span data-stu-id="c6b51-116">You can use the number range that is provided by the tax authorities to number Latvian and Lithuanian customer invoices and return sales orders.</span></span>

    * <span data-ttu-id="c6b51-117">Pasirinkite **Organizacijos administravimas \> Numeracijos \> Skaitiklių valdymas**.</span><span class="sxs-lookup"><span data-stu-id="c6b51-117">Go to **Organization administration \> Number sequences \> Counters management**.</span></span> <span data-ttu-id="c6b51-118">Turi būti įrašas, kuriame **Modulis** = **Pardavimas** ir **Tipas** = **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="c6b51-118">There should be a record where **Module** = **Sales** and **Type** = **Invoice**.</span></span>
    * <span data-ttu-id="c6b51-119">Pasirinkite **Organizacijos administravimas \> Numeracijos \> SF numeravimo nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="c6b51-119">Go to **Organization administration \> Number sequences \> Invoice numbering setup**.</span></span> <span data-ttu-id="c6b51-120">Pažymėkite numeracijos eilutės, naudojamos kliento SF numeruoti, žymės langelį **Prekyba**.</span><span class="sxs-lookup"><span data-stu-id="c6b51-120">Select the **Commerce** check box for the number sequence line that is used to number the customer invoices.</span></span>
