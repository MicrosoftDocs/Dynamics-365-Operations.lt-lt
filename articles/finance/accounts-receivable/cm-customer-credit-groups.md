---
title: Kliento kredito grupės
description: Šioje temoje pateikiama informacijos apie klientų kredito grupes.
author: mikefalkner
manager: AnnBe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76b1e93d562e66cb8d4c5819a749459ea8783b1e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237547"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="8a6fa-103">Kliento kredito grupės</span><span class="sxs-lookup"><span data-stu-id="8a6fa-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a6fa-104">Galite apibrėžti klientų grupes, kurių kredito limitas yra bendrai naudojamas.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="8a6fa-105">Taip pat nagrinėjamas individualus kredito limitas, apibrėžtas kliento SF sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="8a6fa-106">Kliento kredito grupės nariai gali būti pasirenkami iš skirtingų juridinių subjektų.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="8a6fa-107">Kai į kliento kredito grupę įtraukiate klientą į klientų sąrašą klientų kredito grupėje, kiekvieno kliento kredito limito galiojimo data pakeičiama į galiojimo datą, kuri priskirta grupei.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="8a6fa-108">Puslapyje **Klientų kredito grupės** galite nustatyti klientų kredito grupes (**Kreditų valdymo \> Klientų kredito grupės \> Klientų kredito grupės**).</span><span class="sxs-lookup"><span data-stu-id="8a6fa-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="8a6fa-109">Laukuose **Grupės numeris** ir **Aprašas** įveskite grupės identifikatorių ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="8a6fa-110">Laukuose **Kedito limitas** ir **Valiuta** įveskite kredito limitą ir valiutą, kuri turėtų būti naudojama, kai sistema patikrina visų grupės narių kredito limitą.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="8a6fa-111">Lauke **Kredito limito pabaigos data** įveskite datą, kada baigiasi kredito limito galiojimo laikas.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="8a6fa-112">Klientų kredito grupės turi turėti galiojimo datą.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="8a6fa-113">Kai baigsite nustatyti klientų kredito grupę, į ją galite įtraukti klientų nurodydami jų juridinį subjektą ir kliento sąskaitos ID.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="8a6fa-114">Kai į klientų kredito grupę įtraukiate naują klientą, sistema ieško to paties kliento sąskaitos visuose juridiniuose subjektuose ir paragina ją įtraukti į klientų kredito grupę.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="8a6fa-115">Norėdami peržiūrėti išsamią informaciją apie visų SF klientų, esančių kliento kredito grupėje, skirstymo pagal terminus balansą, naudokite meniu **Suskirstyti pagal terminus balansai**.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="8a6fa-116">Puslapyje **Suskirstyti pagal terminus balansai** pateikiama SF kliento sąskaitų pagal terminus suskirstytų balansų suvestinė.</span><span class="sxs-lookup"><span data-stu-id="8a6fa-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]