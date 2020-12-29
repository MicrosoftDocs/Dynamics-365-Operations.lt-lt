---
title: Hibridiniai kliento užsakymai
description: Hibridinis kliento užsakymas yra vienas užsakymas, apimantis produktus, kuriuos klientas gali išsinešti iš parduotuvės pats, ir produktus, kurie bus paimti arba išsiųsti vėliau.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1c2105aa99e0489d7643d076e84123eec628679e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414433"
---
# <a name="hybrid-customer-orders"></a><span data-ttu-id="95ffe-103">Hibridiniai kliento užsakymai</span><span class="sxs-lookup"><span data-stu-id="95ffe-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="95ffe-104">Hibridinis kliento užsakymas yra vienas užsakymas, apimantis produktus, kuriuos klientas gali išsinešti iš parduotuvės pats, ir produktus, kurie bus paimti arba išsiųsti vėliau.</span><span class="sxs-lookup"><span data-stu-id="95ffe-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="95ffe-105">Programoje „Commerce“ galite pasirinkti išsinešti visus arba pasirinktus kliento užsakymo produktus.</span><span class="sxs-lookup"><span data-stu-id="95ffe-105">In Commerce, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="95ffe-106">Sukūrus užsakymą automatiškai išrašoma SF už produktų eilutes, pažymėtas išsinešti; tai taip pat taikoma užsakymui, kurio produktai bus paimti po užsakymo sukūrimo.</span><span class="sxs-lookup"><span data-stu-id="95ffe-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="95ffe-107">Hibridinių užsakymų mokėtina suma nustatoma sudėjus paimtinų ir siųstinų produktų eilučių depozito procentą ir visą išsinešti pažymėtų produktų eilučių sumą.</span><span class="sxs-lookup"><span data-stu-id="95ffe-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="95ffe-108">Kai naudojami hibridiniai užsakymai, sistema perjungia kliento užsakymo režimą ir atsiskaitymo grynaisiais režimą, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="95ffe-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

- <span data-ttu-id="95ffe-109">Jei visi produktai krepšelyje yra nustatyti kaip **Išsineština**, užsakymas bus tvarkomas kaip atsiskaitymo grynaisiais operacija.</span><span class="sxs-lookup"><span data-stu-id="95ffe-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
- <span data-ttu-id="95ffe-110">Jei visos ar bent viena eilutė krepšelyje yra nustatyti kaip **Paimtina** arba **Išsiųstina**, užsakymas bus tvarkomas kaip kliento užsakymo operacija.</span><span class="sxs-lookup"><span data-stu-id="95ffe-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="95ffe-111">Pasirinkus krepšelio eilutę ir parinktį **Išrinkti pasirinktus**, **Išsiųsti pasirinktus** arba **Išsinešti pasirinktus**, toks pristatymo būdas nustatomas tik konkrečiai krepšelio eilutei.</span><span class="sxs-lookup"><span data-stu-id="95ffe-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="95ffe-112">Tokiu atveju operacijos proceso pabaigos srautas tęsiamas įprastai.</span><span class="sxs-lookup"><span data-stu-id="95ffe-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="95ffe-113">Tačiau, jei pažymėta parinktis **Išrinkti pasirinktus**, **Išsiųsti pasirinktus** arba **Išsinešti pasirinktus**, bet nepasirinkta jokia krepšelio eilutė, atidaromas naujas puslapis, kuriame pateikiamos visos krepšelio eilutės.</span><span class="sxs-lookup"><span data-stu-id="95ffe-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="95ffe-114">Tame ekrane galite vienu metu pasirinkti kelias eilutes ir nustatyti jų pristatymo būdą.</span><span class="sxs-lookup"><span data-stu-id="95ffe-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="95ffe-115">Pritaikius tą būdą pasirinktoms eilutėms, perrašomas bet koks ankstesnis toms eilutėms priskirtas pristatymo būdas.</span><span class="sxs-lookup"><span data-stu-id="95ffe-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95ffe-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="95ffe-116">Additional resources</span></span>

[<span data-ttu-id="95ffe-117">Klientų užsakymai naudojant „Modern POS“ (MPOS)</span><span class="sxs-lookup"><span data-stu-id="95ffe-117">Customer orders in Modern POS (MPOS)</span></span>](customer-orders-overview.md)
